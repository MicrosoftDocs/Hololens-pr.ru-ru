---
title: 'руководство по развертыванию: корпоративные подключенные HoloLens 2 с руководствами по Dynamics 365 — обзор'
description: узнайте, как регистрировать устройства HoloLens 2 с помощью руководств Dynamics 365 по корпоративной сети.
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
ms.openlocfilehash: 541c1080d7f5fe9491d6cb11179ea98b160f687c
ms.sourcegitcommit: e9f746aa41139859edc12fbc21f926c9461da4b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2021
ms.locfileid: "126033423"
---
# <a name="deployment-guide---corporate-connected-hololens-2-with-dynamics-365-guides---overview"></a>руководство по развертыванию: корпоративные подключенные HoloLens 2 с руководствами по Dynamics 365 — обзор

это руководство поможет ит-специалистам спланировать и развернуть Microsoft HoloLens 2 устройства с помощью руководств Dynamics 365 (руководств) в своей организации. Это руководство отлично подходит для пилотных проектов, а также для развертывания в рабочей среде и аналогично [сценарию б. Разверните руководство по сети организации](/hololens/common-scenarios#scenario-b-deploy-inside-your-organizations-network) . после проверки концепции воспользуйтесь этим руководством, чтобы перейти к интеграции HoloLens в вашу организацию.

В этом руководство мы рассмотрим, как зарегистрировать устройства в существующем управлении устройствами, применить лицензии по мере необходимости и проверить, что конечные пользователи могут работать с руководством по Dynamics 365, а также использовать настраиваемые бизнес-приложения после настройки устройства. 

## <a name="prerequisites"></a>Предварительные требования

Уже должна быть выполнена следующая инфраструктура:
- Wi-Fi
    - Внутренняя корпоративная сеть с доступом к внутренним ресурсам и ограниченный доступ к Интернету или облачным службам.
    - Проверка подлинности сертификата на основе устройства.
- присоединение Azure Active Directory (Azure ad) с автоматической регистрацией MDM (требуется[подписка Azure AD P1](/azure/active-directory/fundamentals/active-directory-whatis) )
- Управление MDM (Intune)
    - Одно или несколько приложений развертываются с помощью MDM.
- Сеть 
    - Сертификаты (SCEP или PKCS)
    - настройки прокси-сервера;
- Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)
    - Поддерживается одно или несколько пользователей на каждом устройстве.
- Различные уровни конфигурации блокировки устройств, применяемые на основе конкретных вариантов использования, от полного открытия до одного киоска приложения.

## <a name="guides-licensing-and-requirements"></a>[Руководства по лицензированию и требованиям](/dynamics365/mixed-reality/guides/requirements#licensing-and-product-requirements)

- Учетная запись Azure AD
- Dynamics 365 предлагает приложениям ПК и HoloLens
- Подписка на Dynamics 365 Guides
    - Microsoft Инверсия (включена)
    - Power Apps (включена)
- Power BI Desktop
- Сетевое подключение

[![Схема сети с подключенной корпоративной сетью, этап 1. ](./images/deployment-guides-revised-scenario-b-01-1.png)](./images/deployment-guides-revised-scenario-b-01-1.png#lightbox)

[![Схема сетей, подключенная к корпоративной сети, этап 2. ](./images/deployment-guides-revised-scenario-b-02-1.png)](./images/deployment-guides-revised-scenario-b-02-1.png#lightbox)

## <a name="in-this-guide-you-will"></a>В руководстве описаны следующие действия:
### <a name="prepare"></a>Подготовка.
> [!div class="checklist"]
>- [ознакомьтесь с основными сведениями об инфраструктуре для HoloLens 2 устройств.](hololens2-corp-connected-prepare.md#infrastructure-essentials)
>- [Узнайте больше об Azure AD и настройте его, если у вас его нет.](hololens2-corp-connected-prepare.md#azure-active-directory)
>- [Узнайте больше об управлении удостоверениями и о том, как лучше настроить учетные записи Azure AD.](hololens2-corp-connected-prepare.md#identity-management)
>- [Ознакомьтесь с дополнительными сведениями об MDM и настройте Intune, если у вас ее еще нет.](hololens2-corp-connected-prepare.md#mobile-device-management)
>- [Ознакомьтесь с Wi-Fi на основе сертификатов.](hololens2-corp-connected-prepare.md#certificates)
>- [Ознакомьтесь с прокси-сервером.](hololens2-corp-connected-prepare.md#proxy)
>- [Узнайте, как можно использовать бизнес-приложения.](hololens2-corp-connected-prepare.md#line-of-business-apps)
>- [Узнайте больше о том, как можно использовать руководства для вашей организации.](hololens2-corp-connected-prepare.md#guides-playbook)
### <a name="configure"></a>Configure
> [!div class="checklist"]
>- [Создание пользователей и групп.](hololens2-corp-connected-configure.md#azure-users-and-groups)
>- [Как настроить автоматическую регистрацию.](hololens2-corp-connected-configure.md#auto-enrollment-on-hololens-2)
>- [Как настроить сертификаты и профили Wi-Fi для корпоративного Wi-Fi подключения.](hololens2-corp-connected-configure.md#corporate-wi-fi-connectivity)
>- [Upload и назначение пакетов бизнес-приложений (LOB).](hololens2-corp-connected-configure.md#app-deployment)
>- [Настройка руководств по Dynamics 365.](hololens2-corp-connected-configure.md#setup-guides-application-licenses-dataverse-and-authoring)
>- [Настройка режима киоска (необязательно).](hololens2-corp-connected-configure.md#optional-kiosk-mode)
>- [Настройка WDAC (необязательно).](hololens2-corp-connected-configure.md#optional-wdac)
### <a name="deploy"></a>Развернуть
> [!div class="checklist"]
>-  [Проверка регистрации через устройство и MDM.](hololens2-corp-connected-deploy.md#enrollment-validation)
>-  [Проверка сертификатов Wi-Fi.](hololens2-corp-connected-deploy.md#wi-fi-certificate-validation)
>-  [Проверка установки бизнес-приложения.](hololens2-corp-connected-deploy.md#validate-lob-app-install)
>-  [Проверка руководств с помощью разработки и работы.](hololens2-corp-connected-deploy.md#validate-dynamics-365-guides)
### <a name="maintain"></a>Техническое обслуживание
> [!div class="checklist"]
>- [Обновление HoloLens 2.](hololens2-corp-connected-maintain.md#update-hololens)
>- [Инструкции по обновлению руководств (приложений магазина).](hololens2-corp-connected-maintain.md#how-to-update-dynamics-365-guides-and-other-store-apps)
>- [Обновление бизнес-приложений.](hololens2-corp-connected-maintain.md#how-to-update-lob-apps) 
>- [План разработки.](hololens2-corp-connected-maintain.md#development-plan) 
>- [Создание плана поддержки.](hololens2-corp-connected-maintain.md#support-plan)
>- [Параметры управления устройствами.](hololens2-corp-connected-maintain.md#device-management)

## <a name="next-step"></a>Следующий шаг 
> [!div class="nextstepaction"]
> [Развертывание с корпоративным подключением — подготовка](hololens2-corp-connected-prepare.md)
