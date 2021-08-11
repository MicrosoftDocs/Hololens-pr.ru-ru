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
ms.openlocfilehash: aae4e1dbbf28906c1f93ac7f29620260023f596bb96fc23a3ee78442e70585fa
ms.sourcegitcommit: f8e7cc2fbdcdf8962700fd50b9c017bd83d1ad65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "115663293"
---
# <a name="license-requirements"></a>Требования лицензий

## <a name="overview"></a>Обзор
На этой странице приведен общий обзор лицензий и учетных записей, необходимых для развертывания управляемых и неуправляемых устройств HoloLens 2 в вашей организации. Она также содержит сведения о лицензировании Dynamics 365 [Remote Assist](#dynamics-365-remote-assist) и [Guides](#dynamics-365-guides).

## <a name="hololens-2-license-and-account-requirements"></a>Требуемые лицензии и учетные записи для HoloLens 2

 
|       &nbsp;      | Управляемое устройство HoloLens | Неуправляемое устройство HoloLens |
|-------------------|-----------------|---------------------|
| **Использование для бизнеса** | | |
| [Развертывание на подключенных к облаку устройствах — подтверждение концепции/пилотное развертывание](hololens-requirements.md#scenario-a-deploy-to-cloud-connected-devices)  | ✔️| |
| [Развертывание в сети организации — развертывание в большом масштабе](hololens-requirements.md#scenario-b-deploy-inside-your-organizations-network) | ✔️| |
| [Развертывание в безопасной автономной среде](hololens-requirements.md#scenario-c-deploy-in-secure-offline-environment) | | ✔️ |
| **Лицензии** | | |
| Azure Active Directory | ✔️ | |
| MDM (Intune<sup>1</sup> или <sup>2</sup>) | ✔️  | |
| **Измерение счетов** |  | |
| Учетная запись администратора Azure AD | ✔️ |  |
| Учетная запись пользователя Azure AD | ✔️ | |
| [Учетная запись Майкрософт (MSA)](/windows/security/identity-protection/access-control/microsoft-accounts)| | ✔️ |
| [Локальная учетная запись](/windows/security/identity-protection/access-control/local-accounts)<sup>3</sup> | | ✔️ |
- <sup>1</sup> [Автоматическая регистрация](/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment) при начальной настройке устройства, которая регистрирует устройство, присоединяет его к Azure Active Directory и позволяет управлять им в Intune.
- <sup>2</sup> [Windows Autopilot для HoloLens 2](hololens2-autopilot.md) упрощает процесс подготовки для ИТ-администраторов и конечных пользователей. ИТ-администраторы могут предварительно настроить политики HoloLens 2, и при первой загрузке устройства будут развернуты в состояние готовности к работе без взаимодействия с конечным пользователем.
- <sup>3</sup> Необходимо [подготовить](hololens-provisioning.md#provisioning-package-hololens-wizard) эту учетную запись заранее с помощью Конструктора конфигураций Windows (Windows Configuration Designer, WCD).

> [!IMPORTANT]
> Служба Active Directory (AD) не может использоваться для управления устройствами HoloLens.
 
> [!WARNING]
> Если устройство использует локальную учетную запись или учетную запись Майкрософт, работа на нем нескольких пользователей не поддерживается.

## <a name="dynamics-365-licensing-and-requirements"></a>Лицензирование и требования для Dynamics 365

### <a name="dynamics-365-remote-assist"></a>Dynamics 365 Remote Assist; 

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

- Microsoft Teams или [бесплатная версия Teams](https://products.office.com/microsoft-teams/free)

- Возможность подключения к сети

Если вы планируете реализовать этот [сценарий для разных клиентов](/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants), вам может потребоваться лицензия на Информационные барьеры. Чтобы определить, требуется ли лицензия на Информационные барьеры, ознакомьтесь с [этой статьей](/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary).

### <a name="dynamics-365-guides"></a>Dynamics 365 Guides 

#### <a name="admin"></a>Административный

1. Учетная запись Azure AD (требуется для приобретения подписки и назначения лицензий)
2. [Подписка или пробная версия Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup-step-one)

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
