---
title: Руководство по развертыванию — корпоративное подключение HoloLens 2 с помощью Dynamics 365 Guides — подготовка
description: Узнайте, как подготовиться к регистрации устройств HoloLens 2 в корпоративной сети с руководствами по Dynamics 365.
keywords: HoloLens, управление, корпоративные подключения, руководства по Dynamics 365, AAD, Azure AD, MDM, управление мобильными устройствами
author: joyjaz
ms.author: v-jjaswinski
ms.reviewer: aboeger
ms.date: 03/24/2021
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 2ab24aeac371b8d4a17d6121c3adf317cac7daf1
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309494"
---
# <a name="prepare---corporate-connected-guide"></a>Подготовка — корпоративное подключение
## <a name="infrastructure-essentials"></a>Основы инфраструктуры
Как для персональных, так и для корпоративных сценариев развертывания Система управления мобильными устройствами (MDM) является важнейшей инфраструктурой, необходимой для развертывания устройств Windows 10 и управления ими, особенно HoloLens 2. [Azure AD Premiumная подписка](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-get-started-premium) рекомендуется в качестве поставщика удостоверений и **должна** поддерживать определенные возможности.

> [!NOTE]
> Хотя HoloLens 2 развертывается и управляется как мобильное устройство, оно обычно используется в качестве общего устройства для нескольких пользователей.

## <a name="azure-active-directory"></a>Azure Active Directory
Azure AD — это облачная служба каталогов, которая обеспечивает управление удостоверениями и доступом. Организации, использующие Microsoft Office 365 или Intune, уже используют Azure AD с тремя выпусками: Free, Premium P1 и Premium P2 (см. [Azure Active Directory выпуски](https://azure.microsoft.com/documentation/articles/active-directory-editions)). Все выпуски поддерживают регистрацию устройств Azure AD, но для включения автоматической регистрации MDM, которую мы будем использовать в этом пошаговом задании, требуется Premium P1.
> [!Important]
> Важно, чтобы Azure AD в качестве устройств HoloLens не поддерживал локальную службу AD JOIN. Если вы еще не установили Azure AD, следуйте инструкциям, чтобы приступить к работе, и [Создайте новый клиент в Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-access-create-new-tenant).

## <a name="identity-management"></a>Управление удостоверениями
В этом разделе используется [удостоверение](https://docs.microsoft.com/hololens/hololens-identity) , которое будет использоваться в качестве учетных записей Azure AD. Есть несколько преимуществ для учетных записей Azure AD, таких как:
- Сотрудники используют учетную запись Azure AD для регистрации устройства в Azure AD и могут автоматически зарегистрировать его в решении MDM Организации (Azure AD + MDM — требуется [подписка Azure AD Premium](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-get-started-premium)).
- Учетные записи Azure AD имеют дополнительные [Параметры проверки подлинности](https://docs.microsoft.com/hololens/hololens-identity) с помощью [Windows Hello для бизнеса](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-identity-verification). В дополнение к входу в систему IRI пользователи могут входить с другого устройства или использовать ключи безопасности FIDO.

> [!WARNING] 
> Сотрудники могут использовать только одну учетную запись для инициализации устройства, поэтому необходимо **, чтобы ваша организация включала в себя первую учетную запись**. Выбранная учетная запись определяет, кто контролирует устройство, и влияет на возможности управления.

## <a name="mobile-device-management"></a>Управление мобильными устройствами
Microsoft Intune, часть Enterprise Mobility + Security, — это облачная система MDM, которая управляет устройствами, подключенными к вашему клиенту. Как и в Office 365, Intune использует Azure AD для управления удостоверениями, поэтому сотрудники используют одни и те же учетные данные для регистрации устройств в Intune, которые используются для входа в Office 365. Intune также поддерживает устройства под управлением других операционных систем, таких как iOS и Android, для обеспечения полноценного решения MDM. В рамках этого руководств мы будем сосредоточиться на использовании Intune для развертывания внутренней сети с помощью HoloLens 2.
> [!Important] 
> Важно иметь управление мобильными устройствами. Если вы еще не установили его, следуйте указаниям в этом разделе и приступайте к работе с Intune.

> [!Important]
> Для использования руководств требуется учетная запись Azure AD.

> [!Note] 
> Windows 10 поддерживается несколькими системами MDM, и большинство из них поддерживает сценарии развертывания как персональных, так и корпоративных устройств. Поставщики MDM, которые поддерживают Windows 10 holographic, включают: AirWatch, MobileIron и другие. Большинство ведущих поставщиков решений MDM в отрасли уже обеспечивают поддержку интеграции с Azure AD. Вы можете найти самый актуальный список поставщиков MDM, которые поддерживают Azure AD в [Azure Marketplace](https://azuremarketplace.microsoft.com/marketplace/apps/category/azure-active-directory-apps).

## <a name="network-access"></a>Сетевой доступ 
Руководства по Dynamics 365 — это облачное приложение. Если администратор сети имеет список утверждений, ему может потребоваться добавить IP-адреса и (или) конечные точки, необходимые для подключения к серверам Dynamics 365. Дополнительные [сведения о разблокировании IP-адресов и адресов URL](https://docs.microsoft.com/power-platform/admin/online-requirements#ip-addresses-and-urls).

## <a name="certificates"></a>Сертификаты
Сертификаты помогают повысить безопасность, предоставляя проверку подлинности учетной записи, Wi-Fi проверку подлинности, шифрование VPN и шифрование SSL веб-содержимого. Несмотря на то, что администраторы могут управлять сертификатами на устройствах вручную с помощью пакетов подготовки, рекомендуется использовать систему MDM для управления этими сертификатами во всем жизненном цикле — от регистрации до продления и отзыва. 

Система MDM может автоматически развернуть эти сертификаты в хранилищах сертификатов устройств после их регистрации (при условии, что система MDM поддерживает **SCEP (SCEP)** или **стандарты криптографии с открытым ключом #12 (PKCS # 12)**). [Сведения о типах сертификатов и профилях, используемых с Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/certificates-configure). MDM также может запрашивать и удалять зарегистрированные сертификаты клиентов или запускать новый запрос на регистрацию до истечения срока действия текущего сертификата.
 
Если системы MDM уже настроены для сертификатов, создайте ссылки [Подготовка сертификатов и сетевых профилей для HoloLens 2](https://docs.microsoft.com/hololens/hololens-certificates-network) , чтобы начать развертывание сертификатов и профилей для устройств hololens 2.

## <a name="scep"></a>SCEP

Следующие службы необходимы для развертывания SCEP, за исключением прокси-сервера веб – приложения.
- [Центр сертификации](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj125375(v=ws.11))
- [Роль сервера NDES](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831498(v=ws.11))
- [Соединитель Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/certificates-scep-configure#install-the-microsoft-intune-connector)

Кроме того, необходимо опубликовать URL-адрес NDES, внешний в корпоративной сети, с помощью [прокси приложения Azure AD или прокси-сервера веб-доступ](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-add-on-premises-application). Можно также использовать другой обратный прокси-сервер по своему усмотрению.

![Поток данных SCEP](./images/hololens2-scep-info-flow.png)

Если ваша сеть не поддерживает SCEP или вы не уверены, правильно ли настроена сеть для SCEP с Intune, см. ссылку  [Настройка инфраструктуры для поддержки SCEP с Intune](https://docs.microsoft.com/mem/intune/protect/certificates-scep-configure).

Если ваша инфраструктура уже поддерживает SCEP, необходимо [создать](https://docs.microsoft.com/mem/intune/protect/certificates-profile-scep) [профиль](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/create-certificate-profiles) для каждого сертификата SCEP, который будет использовать HoloLens 2. При возникновении проблем с SCEP используйте " [Устранение неполадок при использовании профилей сертификатов SCEP" для инициализации сертификатов с Microsoft Intune](https://docs.microsoft.com/troubleshoot/mem/intune/troubleshoot-scep-certificate-profiles).

## <a name="pkcs"></a>PKCS
Intune также поддерживает использование сертификатов с частным и открытым ключом (PKCS). Дополнительные сведения см. [в разделе Использование сертификатов закрытых и открытых ключей в Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/certificates-pfx-configure) .

## <a name="proxy"></a>Прокси
В большинстве корпоративных сетей интрасети используется прокси-сервер для управления внешним трафиком. С помощью HoloLens 2 можно настроить прокси-сервер для Ethernet, Wi-Fi и VPN-подключений.

Существует несколько различных типов прокси-серверов и способов настройки прокси-сервера. В рамках этого руководств мы будем выбирать **прокси Wi-Fi, задавать URL-адрес PAC и развертывать его через MDM**. Это связано с преимуществами автоматического развертывания в MDM, возможностью обновления файла PAC вместо использования сервера: конфигурации порта и, наконец, использования Wi-Fi прокси-сервера для настройки прокси-сервера для применения только к одному Wi-Fiому подключению, что позволяет использовать устройства по-прежнему, если они подключены в другом расположении. 


Дополнительные сведения о параметрах прокси-сервера для Windows 10 см. [в статье Создание профиля Wi-Fi для устройств в Microsoft Intune-Azure](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-configure).

## <a name="line-of-business-apps"></a>Бизнес-приложения 
Хотя несколько приложений можно установить с помощью Microsoft Store, скорее всего, у вас есть собственное пользовательское приложение, созданное специально для использования в смешанной реальности. Эти настраиваемые приложения, распределенные по всей Организации для вашего бизнеса, называются бизнес-приложениями.
  
Существует несколько способов развертывания приложений на устройствах HoloLens 2. Приложения можно развертывать напрямую с помощью MDM, Microsoft Store для бизнеса (Мсфб) или загруженные неопубликованные с помощью пакета подготовки. Для работы с этим руководством мы будем развертывать приложения с помощью MDM с помощью установки обязательного приложения. Это позволит автоматически загружать бизнес-приложения на устройства HoloLens после завершения регистрации.

Для тех, кто не имеет собственного LOB, мы предоставляем пример приложения для тестирования этого потока развертывания. Это приложение будет примером приложения [мртк](https://aka.ms/HoloLensDocs-Sample-MRTK-Examples-App) , которое уже было предварительно собрано и упаковано для проверки концепции.
 
Дополнительные сведения о развертывании приложений можно найти в статье [Управление приложениями: обзор](https://docs.microsoft.com/hololens/app-deploy-overview).

> [!NOTE]
> HoloLens 2 поддерживает запуск только приложений ARM64 UWP.

## <a name="guides-playbook"></a>Направляющие сборник тренировочных заданий
В руководствах используется среда Microsoft инверсия в качестве хранилища данных для приложений для работы с руководствами. Важно понимать, как работает среда обратной работы с вашими приложениями и клиентом. Мы не будем рассматривать, как управлять вашими данными в этом руководстве, но ознакомьтесь с [основными понятиями по развертыванию руководств по dynamics 365 в dynamics 365 Mixed Reality](https://docs.microsoft.com/dynamics365/mixed-reality/guides/admin-deployment-playbook).

## <a name="next-step"></a>Следующий шаг 
> [!div class="nextstepaction"]
> [Развертывание с корпоративным подключением — Настройка](hololens2-corp-connected-configure.md)