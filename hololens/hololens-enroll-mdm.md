---
title: Регистрация HoloLens в MDM
description: Узнайте, как зарегистрировать HoloLens в управлении мобильными устройствами (MDM) для более простого управления несколькими устройствами.
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
ms.openlocfilehash: 5613c69bda8bbf70722a050ac5ce4ebeab95d332
ms.sourcegitcommit: 771e53feefbcc6bce18577515ad7d3f6a7f33840
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399387"
---
# <a name="enroll-hololens-in-mdm"></a>Регистрация HoloLens в MDM

Вы можете управлять несколькими устройствами Microsoft HoloLens одновременно с помощью решений, таких как [Microsoft Intune.](https://docs.microsoft.com/intune/windows-holographic-for-business) Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации. См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).

> [!NOTE]
> Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).

## <a name="requirements"></a>Требования

 Для управления устройствами HoloLens организации необходимо настроить управление мобильными устройствами (MDM). Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.
 
## <a name="different-ways-to-enroll"></a>Различные способы регистрации

В зависимости от типа удостоверения, выбранного во время OOBE или после регистрации, существуют различные методы регистрации. Дополнительные данные о каждом типе identity на HoloLens можно найти на [этой странице.](hololens-identity.md)

- Если Identity — Azure AD, то либо во время работы OOBE или **Параметры работы**доступа к приложениям,  ->  **либо кнопки Подключения**  ->  **к** школе.
    - Для Azure AD автоматическая регистрация MDM происходит только в том случае, если Azure AD настроен с URL-адресами регистрации.
- Если Identity — Это Azure AD и устройство было предварительно зарегистрировано на сервере Intune MDM с определенным профилем конфигурации, назначенного ему, AD-Join и регистрация будет автоматически происходить во время OOBE.
    - Также называется [поток автопилота,](hololens2-autopilot.md) доступный в [сборках 19041.1103+](hololens-release-notes.md#windows-holographic-version-2004).
- Если identity — это MSA, то с помощью кнопки **Параметры Работы доступа**к приложениям  ->  **или кнопки Подключения**  ->  **к школе.**
    - Также называется поток Add Work Account (AWA).
- Если identity — локальный пользователь, то с помощью **Параметры Работы по**доступу к приложениям или регистрации в школе  ->  ****  ->  **только в ссылке управления устройствами.**
    - Также называется чистый поток регистрации MDM.

После регистрации устройства на сервере MDM приложение Settings теперь будет отражать, что устройство зачислилось в управление устройствами.

## <a name="auto-enrollment-in-mdm"></a>Автоматическая регистрация в MDM

Если ваша организация использует Azure Active Directory (Azure AD) и решение MDM, которое принимает маркер Azure AD для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ИТ-администратор может настроить Azure AD, чтобы автоматически разрешить регистрацию MDM после того, как пользователь включит свою учетную запись Azure AD. [Сведения о настройке регистрации в Azure AD.](https://docs.microsoft.com/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

Если автоматическая регистрация включена, дополнительные действия по регистрации вручную не требуются. Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.

Если устройство является Azure AD Joined, это может повлиять на то, кто [считался владельцем устройства.](security-adminless-os.md#device-owner)

## <a name="unenroll-hololens-from-intune"></a>Unenroll HoloLens из Intune

Хотя HoloLens 2 — это устройство с Windows 10, его нельзя просто отсоединить от Intune. Если вы хотите отсоединить HoloLens из Azure AD или присоединить его к другому клиенту Azure AD, необходимо сбросить [или](https://docs.microsoft.com/hololens/hololens-recovery#reset-the-device) перезагрузить устройство.