---
title: Требования лицензий
description: Оставайтесь в курсе всех требований и рекомендаций по лицензированию для управления мобильными устройствами, HoloLens и Remote Assist.
ms.prod: hololens
ms.sitesec: library
author: pawinfie
ms.author: pawinfie
audience: HoloLens
ms.topic: article
ms.localizationpriority: high
ms.date: 1/23/2020
ms.reviewer: ''
manager: bradke
appliesto:
- HoloLens 2
ms.openlocfilehash: bd7a7d03c81dced4fb66d8ebb176887811e823c9
ms.sourcegitcommit: 4c15afc772fba26683d9b75e38c44a018b4889f6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113640290"
---
# <a name="license-requirements"></a>Требования лицензий

## <a name="hololens-2-device-managed"></a>Устройство HoloLens 2 (управляемое)

[Учетная запись Azure AD](/azure/active-directory/)

> [!IMPORTANT]
> Служба Active Directory (AD) не может использоваться для управления устройствами HoloLens.

[Microsoft Intune](/mem/intune/fundamentals/what-is-intune) или другая система управления мобильными устройствами.
- [Windows Autopilot для HoloLens 2](hololens2-autopilot.md) — упрощает процесс подготовки как для ИТ-администраторов, так и для конечных пользователей. ИТ-администраторы могут предварительно настроить политики HoloLens 2, и при первой загрузке устройства будут развернуты в состояние готовности к работе без взаимодействия с конечным пользователем. 

  > [!NOTE]
  > Для использования Windows Autopilot и развертывания устройства с минимальным вмешательством пользователя необходимо иметь выпуск [Azure P1](/azure/active-directory/fundamentals/active-directory-whatis) и включить [Автоматическую регистрацию](/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment). 

### <a name="business-use-case"></a>Вариант использования для бизнеса: 

- [Сценарий развертывания A](hololens-requirements.md#scenario-a-deploy-to-cloud-connected-devices) — развертывание для проверки концепции или пилотное развертывание.

- [Сценарий развертывания B](hololens-requirements.md#scenario-b-deploy-inside-your-organizations-network) — развертывание в масштабе.

## <a name="hololens-2-device-only-non-managed"></a>Только устройство HoloLens 2 (неуправляемое)

При использовании учетной записи Майкрософт (MSA) или локальной учетной записи для этих учетных записей не требуются дополнительные лицензии.

[Локальная учетная запись](/windows/security/identity-protection/access-control/local-accounts)

- Эта учетная запись должна быть [подготовлена](hololens-provisioning.md#provisioning-package-hololens-wizard) заранее с помощью Конструктора конфигураций Windows (WCD).

[Учетная запись Майкрософт (MSA)](/windows/security/identity-protection/access-control/microsoft-accounts)

> [!WARNING]
> Для устройств, использующих любую из этих учетных записей, не поддерживается работа нескольких пользователей.

### <a name="business-use-case"></a>Вариант использования для бизнеса: 

- [Сценарий развертывания C](hololens-requirements.md#scenario-c-deploy-in-secure-offline-environment) — автономное или безопасное развертывание.
 
## <a name="dynamics-365-licensing-and-requirements"></a>Лицензирование и требования для Dynamics 365

### <a name="dynamics-365-remote-assist"></a>Dynamics 365 Remote Assist 

#### <a name="admin"></a>Административный

- Учетная запись Azure AD (требуется для приобретения подписки и назначения лицензий)
- [Подписка на Remote Assist](/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist) (или [пробная версия Remote Assist](/dynamics365/mixed-reality/remote-assist/try-remote-assist))
    
#### <a name="dynamics-365-remote-assist-user"></a>Пользователь Dynamics 365 Remote Assist

- Учетная запись Azure AD

- Лицензия Remote Assist 

  > [!NOTE]
  > Remote Assist входит в состав Microsoft Teams

- Сетевое подключение

#### <a name="microsoft-teams-user"></a>Пользователь Microsoft Teams

- Учетная запись Azure AD

- Microsoft Teams или [Teams Freemium](https://products.office.com/microsoft-teams/free).

- Возможность подключения к сети

Если вы планируете реализовать этот [сценарий для разных клиентов](/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants), вам может потребоваться лицензия на Информационные барьеры. Чтобы определить, требуется ли лицензия на Информационные барьеры, ознакомьтесь с [этой статьей](/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary).

### <a name="dynamics-365-guides"></a>Dynamics 365 Guides 

#### <a name="admin"></a>Административный

- Учетная запись Azure AD (требуется для приобретения подписки и назначения лицензий)
- [Подписка или пробная версия Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup-step-one)

#### <a name="guides-author"></a>Автор Guides

1. Учетная запись Azure AD
1. [Лицензия Dynamics 365 Guides](/dynamics365/mixed-reality/guides/requirements)
1. Приложение Dynamics 365 Guides, установленное на ПК или устройстве HoloLens
1. [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (используется для просмотра панели мониторинга аналитики)
1. Роль автора (для создания руководств)
1. Сетевое подключение

#### <a name="guides-user"></a>Пользователь Guides

1. Учетная запись Azure AD
1. [Лицензия Dynamics 365 Guides](/dynamics365/mixed-reality/guides/requirements)
1. Приложение Dynamics 365 Guides, установленное на устройстве HoloLens
1. Роль оператора (для тестирования или использования руководств)
1. Сетевое подключение
