---
title: Руководство по развертыванию — корпоративные подключенные holoLens 2 с руководствами dynamics 365 — Обзор
description: Узнайте, как зарегистрировать устройства HoloLens 2 с помощью руководств Dynamics 365 по корпоративной подключенной сети.
keywords: HoloLens, управление, корпоративное подключение, Руководство по динамике 365, AAD, Azure AD, MDM, Управление мобильными устройствами
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
ms.openlocfilehash: 3041a31e6a4f8b51385fa02dfddc21d56993721d
ms.sourcegitcommit: d7c86ccad7be32f7223d4b801083798454fda740
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2021
ms.locfileid: "11448613"
---
# <a name="deployment-guide---corporate-connected-hololens-2-with-dynamics-365-guides---overview"></a>Руководство по развертыванию — Корпоративные связанные holoLens 2 с руководствами по динамике 365 — Обзор

Это руководство поможет ИТ-специалистам спланировать и развернуть устройства Microsoft HoloLens 2 с помощью руководств dynamics 365 (Guides) для своей организации. Это руководство отлично подходит для пилотов, а также производственных развертывание и аналогично сценарию B. Развертывание в сетевом [руководстве организации.](https://docs.microsoft.com/hololens/common-scenarios#scenario-b-deploy-inside-your-organizations-network) После тестирования вашей концепции с помощью этого руководства можно перейти к интеграции HoloLens в вашу организацию.

В этом руководстве мы покроем, как записать устройства в существующее управление устройствами, применить лицензии по мере необходимости, а также проверить, что конечные пользователи могут использовать руководство Dynamics 365, а также использовать настраиваемую линейку бизнес-приложений после настройки устройства. 

## <a name="prerequisites"></a>Предварительные условия

Уже должна быть следующая инфраструктура:
- Wi-Fi
    - Внутренняя корпоративная сеть с доступом к внутренним ресурсам и ограниченным доступом к интернету или облачным службам
    - Проверка подлинности сертификата на основе устройства.
- Azure Active Directory (Azure AD) присоединяется к автозарегистру MDM (необходима подписка[Azure AD P1)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
- Управляемый MDM (Intune)
    - Одно или несколько приложений развертываются с помощью MDM.
- Network 
    - Сертификаты (SCEP или PKCS)
    - Конфигурация прокси-сервера
- Пользователи во входе с собственной корпоративной учетной записью (Azure AD)
    - Поддерживается один или несколько пользователей на устройство.
- Различные уровни конфигураций блокировки устройств, применяемые в зависимости от конкретных случаев использования, от полностью открытого до единого киоска приложений.

## [<a name="guides-licensing-and-requirements"></a>Руководства по лицензированию и требованиям](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements#licensing-and-product-requirements)
- Учетная запись Azure AD
- Dynamics 365 Guides applications PC and HoloLens
- Подписка на dynamics 365 Guides
    - Microsoft Dataverse (включено)
    - Power Apps (включено)
- Power BI Desktop
- Подключение к сети

![Схема подключенной сети Corp](./images/corpconnected-diagHL2-guides.png)

## <a name="stages-of-deployment"></a>Этапы развертывания
### <a name="prepare"></a>Подготовка
> [!div class="checklist"]
>- [Узнайте о необходимых для устройств HoloLens 2 инфраструктуре.](hololens2-corp-connected-prepare.md#infrastructure-essentials)
>- [Узнайте больше о Azure AD и установите его, если его нет.](hololens2-corp-connected-prepare.md#azure-active-directory)
>- [Узнайте об управлении удостоверениями и о том, как наилучшим образом настроить учетные записи Azure AD.](hololens2-corp-connected-prepare.md#identity-management)
>- [Дополнительные информацию о MDM и настройка в Intune, если у вас еще нет готовой.](hololens2-corp-connected-prepare.md#mobile-device-management)
>- [Ознакомьтесь с Wi-Fi на основе сертификата.](hololens2-corp-connected-prepare.md#certificates)
>- [Ознакомьтесь с прокси-сервером.](hololens2-corp-connected-prepare.md#proxy)
>- [Понимание того, как можно использовать Line of Business Apps.](hololens2-corp-connected-prepare.md#line-of-business-apps)
>- [Дополнительные новости о том, как можно использовать руководство для организации.](hololens2-corp-connected-prepare.md#guides-playbook)
### <a name="configure"></a>Настройка
> [!div class="checklist"]
>- [Создание пользователей и групп.](hololens2-corp-connected-configure.md#azure-users-and-groups)
>- [Настройка автоматической регистрации.](hololens2-corp-connected-configure.md#auto-enrollment-on-hololens-2)
>- [Настройка сертификатов Wi-Fi профилей для корпоративных Wi-Fi подключения.](hololens2-corp-connected-configure.md#corporate-wi-fi-connectivity)
>- [Загрузка и назначение пакетов приложений для бизнеса (LOB).](hololens2-corp-connected-configure.md#app-deployment)
>- [Руководство по настройке Dynamics 365.](hololens2-corp-connected-configure.md#setup-guides-application-licenses-dataverse-and-authoring)
>- [Настройка режима киоска (необязательный).](hololens2-corp-connected-configure.md#optional-kiosk-mode)
>- [Настройка WDAC (необязательно).](hololens2-corp-connected-configure.md#optional-wdac)
### <a name="deploy"></a>Развертывание
> [!div class="checklist"]
>-  [Проверка регистрации с помощью устройства и MDM.](hololens2-corp-connected-deploy.md#enrollment-validation)
>-  [Проверка Wi-Fi сертификатов.](hololens2-corp-connected-deploy.md#wi-fi-certificate-validation)
>-  [Проверка установки приложения LOB.](hololens2-corp-connected-deploy.md#validate-lob-app-install)
>-  [Проверка руководств с помощью авторинга и работы.](hololens2-corp-connected-deploy.md#validate-dynamics-365-guides)
### <a name="maintain"></a>Обслуживание
> [!div class="checklist"]
>- [Обновление HoloLens 2.](hololens2-corp-connected-maintain.md#update-hololens)
>- [Обновление руководств (приложений для хранения).](hololens2-corp-connected-maintain.md#how-to-update-dynamics-365-guides-and-other-store-apps)
>- [Обновление приложений LOB.](hololens2-corp-connected-maintain.md#how-to-update-lob-apps) 
>- [План разработки.](hololens2-corp-connected-maintain.md#development-plan) 
>- [Создание плана поддержки.](hololens2-corp-connected-maintain.md#support-plan)
>- [Параметры управления устройствами.](hololens2-corp-connected-maintain.md#device-management)

## <a name="next-step"></a>Дальнейшие действия 
> [!div class="nextstepaction"]
> [Развертывание подключенных к корпорации — подготовка](hololens2-corp-connected-prepare.md)
