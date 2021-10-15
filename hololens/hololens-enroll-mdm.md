---
title: Регистрация HoloLens в MDM
description: узнайте, как регистрировать HoloLens в системе управления мобильными устройствами (MDM) для упрощения управления несколькими устройствами.
ms.prod: hololens
ms.sitesec: library
ms.assetid: 2a9b3fca-8370-44ec-8b57-fb98b8d317b0
author: evmill
ms.author: v-evmill
ms.topic: article
ms.localizationpriority: medium
ms.date: 9/15/2021
ms.reviewer: ''
manager: ranjibb
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: fa114633afe70a11a180c67fedbd40eb423ece99
ms.sourcegitcommit: 19d1abb7589cebf14ba45e830f49224f7b4fcfe9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2021
ms.locfileid: "130034184"
---
# <a name="enroll-hololens-in-mdm"></a>Регистрация HoloLens в MDM

вы можете управлять несколькими Microsoft HoloLens устройствами одновременно с помощью таких решений, как [Microsoft Intune](/intune/windows-holographic-for-business). Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации. См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).

> [!NOTE]
> Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).

## <a name="requirements"></a>Требования

 для управления HoloLens устройствами организации необходимо настроить управление мобильными устройствами (MDM). Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.

## <a name="different-ways-to-enroll"></a>Различные способы регистрации

В зависимости от типа [удостоверения](hololens-identity.md) , выбранного во время OOBE или после входа, существуют различные методы регистрации.

- если удостоверение — Azure AD, то во время OOBE или Параметры работы с **приложением**  ->  **или учебного**  ->  **Подключение** .
    - Для Azure AD [Автоматическая регистрация MDM](hololens-enroll-mdm.md#auto-enrollment-in-mdm) выполняется, только если в Azure AD настроены URL-адреса регистрации.

- Если удостоверение — Azure AD, а устройство предварительно зарегистрировано в Intune MDM Server с назначенным им особым профилем конфигурации, то Azure AD-Join и [Автоматическая регистрация MDM](hololens-enroll-mdm.md#auto-enrollment-in-mdm) будут выполняться во время Oobe.
    - Также называется [потоком с автопилотом](hololens2-autopilot.md) , доступным в [сборках 19041.1103 и](hololens-release-notes.md#windows-holographic-version-2004).


- если удостоверение — MSA, воспользуйтесь кнопкой **Параметры**  ->  **доступ к приложениям или учебного**  ->  **Подключение** .
    - Также называется потоком добавления рабочей учетной записи (AWS).
- если удостоверение является локальным пользователем, используйте **Параметры**  ->  **доступ к приложению или учебную**  ->  **регистрацию только в связи с управлением устройствами** .
    - Также называется чистым потоком регистрации MDM.

после регистрации устройства на сервере MDM приложение Параметры теперь будет отражать, что устройство зарегистрировано в системе управления устройствами.

## <a name="auto-enrollment-in-mdm"></a>Автоматическая регистрация в MDM

если ваша организация имеет [подписку azure Premium](https://azure.microsoft.com/overview/), использует Azure Active Directory (Azure AD) и решение MDM, которое принимает маркер Azure ad для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ит-администратор может настроить автоматическое разрешение регистрации MDM после входа пользователя с помощью azure ad. учетной записи. [Сведения о настройке регистрации в Azure AD.](/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

Если включена автоматическая регистрация, Дополнительная регистрация вручную не требуется. Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.

Если устройство подключено к Azure AD, оно может повлиять на [владельца устройства](security-adminless-os.md#device-owner).

## <a name="unenroll-hololens-from-intune"></a>отмена регистрации HoloLens из Intune

Отмена регистрации устройства может быть недоступна в зависимости от метода регистрации.

Если ваше устройство было зарегистрировано в учетной записи Azure AD или на автопилоте, зарегистрировать его в Intune невозможно. если вы хотите отменить присоединение HoloLens из Azure ad или повторно присоединить его к другому клиенту azure ad, необходимо [сбросить или восстановить](hololens-recovery.md#restart-the-device) устройство.

Если устройство было зарегистрировано в учетной записи MSA, которая добавила рабочую учетную запись или из локальной учетной записи, зарегистрированной только в управлении устройствами, вы можете отменять регистрацию устройства. откройте меню, а затем выберите **Параметры**  ->  **доступ к приложению работа или школьный**  ->  *йоураккаунт*  ->  **отключить** кнопку.

## <a name="enrollment-troubleshooting"></a>Устранение неполадок регистрации

### <a name="ensure-valid-license-is-assigned-to-the-user"></a>Убедитесь, что пользователю назначена действительная лицензия.

дополнительные сведения см. в разделе [устранение неполадок, связанных с регистрацией устройств Windows, в Microsoft Intune, в частности в](/troubleshoot/mem/intune/troubleshoot-windows-enrollment-errors) следующих разделах. [проверьте ограничения типа устройства](/troubleshoot/mem/intune/troubleshoot-windows-enrollment-errors#check-device-type-restrictions) и [назначьте пользователю действительную лицензию.](/troubleshoot/mem/intune/troubleshoot-windows-enrollment-errors#assign-a-valid-license-to-the-user)

### <a name="ensure-that-mdm-enrollment-isnt-blocked-for-windows-devices"></a>убедитесь, что регистрация MDM не заблокирована для устройств Windows

чтобы зарегистрироваться в случае успешности, необходимо убедиться, что ваши HoloLens устройства могут быть зарегистрированы. Так как HoloLens считается устройством Windows, ограничения на регистрацию, которые могут заблокировать развертывания, должны отсутствовать. [Ознакомьтесь с этим списком ограничений](/mem/intune/enrollment/enrollment-restrictions-set) и убедитесь, что вы можете зарегистрировать устройства.