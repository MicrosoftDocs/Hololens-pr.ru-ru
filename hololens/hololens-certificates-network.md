---
title: Подготовка сертификатов и сетевых профилей для HoloLens 2
description: Узнайте, как настроить, использовать, развернуть и устранить неполадки сертификатов для сети на устройствах смешанной реальности HoloLens 2.
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: aboeger
ms.topic: article
ms.localizationpriority: high
ms.date: 9/15/2020
ms.reviewer: v-evmill
audience: ITPro
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: de9f2c4f136a26a5956ba8a8f3b9faba1e90ea66
ms.sourcegitcommit: 86dba9e8a5e25f0bf29f4c0580970c25c44b7359
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470057"
---
# <a name="prepare-certificates-and-network-profiles-for-hololens-2"></a>Подготовка сертификатов и сетевых профилей для HoloLens 2

Проверка подлинности на основе сертификатов — это общее требование для клиентов, использующих HoloLens 2. Для подключения к решениям VPN или для доступа к внутренним ресурсам вашей организации вам могут потребоваться сертификаты для доступа к Wi-Fi.

Поскольку устройства HoloLens 2 обычно подключаются к Azure Active Directory (Azure AD) и управляются Intune или другим поставщиком MDM, вам потребуется развернуть такие сертификаты с помощью службы регистрации сертификатов для сетевых устройств (SCEP) или стандартов криптографии с открытым ключом (PKCS), которая интегрирована с вашим решением MDM. 

>[!NOTE]
> Если у вас нет поставщика MDM, вы все равно можете развернуть сертификаты с помощью [пакета подготовки](https://docs.microsoft.com/hololens/hololens-provisioning#steps-for-creating-provisioning-packages) в [конструкторе конфигураций Windows](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?rtc=1&activetab=pivot:regionofsystemrequirementstab) или в [диспетчере сертификатов](https://docs.microsoft.com/hololens/certificate-manager), выбрав **Параметры > Обновление и безопасность > Диспетчер сертификатов**.

## <a name="certificate-requirements"></a>Требования к сертификатам
Корневые сертификаты необходимы для развертывания сертификатов через инфраструктуру SCEP или PKCS. Для других приложений и служб в вашей организации может потребоваться развертывание корневых сертификатов на устройствах HoloLens 2. 

## <a name="wi-fi-connectivity-requirements"></a>Требования по подключению к Wi-Fi
Для автоматического предоставления устройству необходимой конфигурации Wi-Fi для вашей корпоративной сети, вам понадобится профиль конфигурации Wi-Fi. Вы можете настроить Intune или другой поставщик MDM для развертывания этих профилей на ваших устройствах. Если для сетевой безопасности необходимо, чтобы устройства были частью локального домена, вам также может понадобиться оценить вашу сетевую инфраструктуру Wi-Fi, чтобы убедиться, что она совместима с устройствами HoloLens 2 (устройства HoloLens 2 с присоединением к Azure AD).

## <a name="deploy-certificate-infrastructure"></a>Развертывание инфраструктуры сертификата
Если инфраструктур SCEP или PKCS не существует, необходимо подготовить одну из них. Чтобы обеспечить проверку подлинности с использованием сертификатов SCEP или PKCS, Intune требует использовать [соединитель сертификатов](https://docs.microsoft.com/mem/intune/protect/certificate-connectors).

> [!NOTE]
> При использовании SCEP в ЦС Microsoft необходимо также настроить [службу регистрации сертификатов для сетевых устройств (NDES)](https://docs.microsoft.com/mem/intune/protect/certificates-scep-configure#set-up-ndes)

Дополнительные сведения см. в статье [Настройка профиля сертификата для устройств в Microsoft Intune](https://docs.microsoft.com/intune/certificates-configure).

## <a name="deploy-certificates-and-wi-fivpn-profile"></a>Развертывание сертификатов и Wi-Fi/VPN профилей
Чтобы развернуть сертификаты и профили, выполните следующие действия:
1.  Создайте профиль для каждого корневого и промежуточного сертификата (см. [Создание доверенных профилей сертификатов](https://docs.microsoft.com/intune/protect/certificates-configure#create-trusted-certificate-profiles)). Каждый из этих профилей должен иметь описание, включающее дату окончания срока действия в формате дд/мм/гггг. **Профили сертификатов, для которых не указана дата окончания срока действия, не будут развернуты.**
1.  Создайте профиль для каждого сертификата SCEP или PKCS (см. [«Создание профиля сертификата SCEP» или «Создание профиля сертификата PCKS»](https://docs.microsoft.com/intune/protect/certficates-pfx-configure#create-a-pkcs-certificate-profile)). Каждый из этих профилей должен иметь описание, включающее дату окончания срока действия в формате дд/мм/гггг. **Профили сертификатов, для которых не указана дата окончания срока действия, не будут развернуты.**

    > [!NOTE]
    > Поскольку HoloLens 2 — это общее устройство с множеством пользователей на устройство, рекомендуется развертывать сертификаты устройств, а не сертификаты пользователей для проверки подлинности Wi-Fi, где это возможно.

3.  Создайте профиль для каждой корпоративной сети Wi-Fi (см. [Параметры Wi-Fi для устройств с Windows 10 и более поздними версиями](https://docs.microsoft.com/intune/wi-fi-settings-windows)). 
    > [!NOTE]
    > Рекомендуется по возможности [назначать](https://docs.microsoft.com/mem/intune/configuration/device-profile-assign) профиль Wi-Fi группам устройств, а не группам пользователей. 

    > [!TIP]
    > Также можно экспортировать рабочий профиль Wi-Fi с компьютера с Windows 10 в корпоративную сеть. В результате экспорта будет создан XML-файл со всеми текущими параметрами. Затем импортируйте этот файл в Intune и используйте его в качестве профиля Wi-Fi для ваших устройств HoloLens 2. Дополнительные сведения см. в статье [Экспорт и импорт параметров Wi-Fi для устройств с Windows](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-import-windows-8-1).

4.  Создайте профиль для каждой корпоративной VPN (см. [Параметры устройств Windows 10 и Windows Holographic для добавления VPN-подключения с помощью Intune](https://docs.microsoft.com/intune/vpn-settings-windows-10)).

## <a name="troubleshooting-certificates"></a>Устранение неполадок с сертификатами

Если необходимо проверить правильность развертывания сертификата, используйте [диспетчер сертификатов](certificate-manager.md) на устройстве, чтобы убедиться в наличии сертификата.  


