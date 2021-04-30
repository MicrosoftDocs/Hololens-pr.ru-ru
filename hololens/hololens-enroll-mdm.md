---
title: Регистрация HoloLens в MDM
description: Узнайте, как зарегистрировать HoloLens в управлении мобильными устройствами (MDM) для упрощения управления несколькими устройствами.
ms.prod: hololens
ms.sitesec: library
ms.assetid: 2a9b3fca-8370-44ec-8b57-fb98b8d317b0
author: scooley
ms.author: scooley
ms.topic: article
ms.localizationpriority: medium
ms.date: 10/06/2019
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 624ebd17335820b1d2858f9d39cabb7032a83bfe
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309716"
---
# <a name="enroll-hololens-in-mdm"></a>Регистрация HoloLens в MDM

Вы можете управлять несколькими устройствами Microsoft HoloLens одновременно с помощью таких решений, как [Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business). Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации. См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).

> [!NOTE]
> Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).

## <a name="requirements"></a>Требования

 Для управления устройствами HoloLens в Организации должно быть настроено управление мобильными устройствами (MDM). Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.
 
## <a name="different-ways-to-enroll"></a>Различные способы регистрации

В зависимости от типа [удостоверения](hololens-identity.md) , выбранного во время OOBE или после входа, существуют различные методы регистрации.

- Если удостоверение — Azure AD, то во время OOBE или **настройки приложения**  ->  **доступа к приложению или учебного**  ->  **подключения** .
    - Для Azure AD [Автоматическая регистрация MDM](hololens-enroll-mdm.md#auto-enrollment-in-mdm) выполняется, только если в Azure AD настроены URL-адреса регистрации.
     
- Если удостоверение — Azure AD, а устройство предварительно зарегистрировано в Intune MDM Server с назначенным им особым профилем конфигурации, то Azure AD-Join и [Автоматическая регистрация MDM](hololens-enroll-mdm.md#auto-enrollment-in-mdm) будут выполняться во время Oobe.
    - Также называется [потоком с автопилотом](hololens2-autopilot.md) , доступным в [сборках 19041.1103 и](hololens-release-notes.md#windows-holographic-version-2004).
    

- Если удостоверение — MSA, используйте **Параметры "Настройка**  ->  **доступа к приложениям" или "школьное**  ->  **Подключение** ".
    - Также называется потоком добавления рабочей учетной записи (AWS).
- Если удостоверение является локальным пользователем, используйте параметры "доступ к **приложению**"  ->  **или "Учебная**  ->  **Регистрация" только в окне "Управление устройствами** ".
    - Также называется чистым потоком регистрации MDM.

После регистрации устройства на сервере MDM приложение "Параметры" теперь будет отражать, что устройство зарегистрировано в системе управления устройствами.

## <a name="auto-enrollment-in-mdm"></a>Автоматическая регистрация в MDM

Если ваша организация имеет [подписку Azure](https://azure.microsoft.com/overview/)уровня "Премиум", использует Azure Active Directory (Azure AD) и решение MDM, которое принимает маркер Azure AD для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ИТ-администратор может настроить автоматическое разрешение регистрации MDM после входа пользователя с помощью учетной записи Azure AD. [Сведения о настройке регистрации в Azure AD.](https://docs.microsoft.com/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

Если включена автоматическая регистрация, Дополнительная регистрация вручную не требуется. Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.

Если устройство подключено к Azure AD, оно может повлиять на [владельца устройства](security-adminless-os.md#device-owner).

## <a name="unenroll-hololens-from-intune"></a>Отмена регистрации HoloLens в Intune

Отмена регистрации устройства может быть недоступна в зависимости от метода регистрации.

Если ваше устройство было зарегистрировано в учетной записи Azure AD или на автопилоте, зарегистрировать его в Intune невозможно. Если вы хотите отменить присоединение HoloLens из Azure AD или повторно присоединить его к другому клиенту Azure AD, необходимо [сбросить или восстановить](https://docs.microsoft.com/hololens/hololens-recovery#reset-the-device) устройство.

Если устройство было зарегистрировано в учетной записи MSA, которая добавила рабочую учетную запись или из локальной учетной записи, зарегистрированной только в управлении устройствами, вы можете отменять регистрацию устройства. Откройте меню Пуск и выберите **Параметры**  ->  **доступ к приложению Рабочая или школьный**  ->  *йоураккаунт*  ->  **Отключить** кнопку.