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
# <a name="deployment-guide---corporate-connected-hololens-2-with-dynamics-365-guides---overview"></a><span data-ttu-id="7a2b2-104">Руководство по развертыванию — Корпоративные связанные holoLens 2 с руководствами по динамике 365 — Обзор</span><span class="sxs-lookup"><span data-stu-id="7a2b2-104">Deployment Guide - Corporate Connected HoloLens 2 with Dynamics 365 Guides - Overview</span></span>

<span data-ttu-id="7a2b2-105">Это руководство поможет ИТ-специалистам спланировать и развернуть устройства Microsoft HoloLens 2 с помощью руководств dynamics 365 (Guides) для своей организации.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-105">This guide will help IT professionals plan for and deploy Microsoft HoloLens 2 devices with Dynamics 365 Guides (Guides) to their organization.</span></span> <span data-ttu-id="7a2b2-106">Это руководство отлично подходит для пилотов, а также производственных развертывание и аналогично сценарию B. Развертывание в сетевом [руководстве организации.](https://docs.microsoft.com/hololens/common-scenarios#scenario-b-deploy-inside-your-organizations-network)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-106">This guide is great for pilots as well as production deployments and is similar to the [Scenario B: Deploy inside your organization's network](https://docs.microsoft.com/hololens/common-scenarios#scenario-b-deploy-inside-your-organizations-network) guide.</span></span> <span data-ttu-id="7a2b2-107">После тестирования вашей концепции с помощью этого руководства можно перейти к интеграции HoloLens в вашу организацию.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-107">After testing your proof-of-concept, use this guide to move forward with integrating HoloLens into your organization.</span></span>

<span data-ttu-id="7a2b2-108">В этом руководстве мы покроем, как записать устройства в существующее управление устройствами, применить лицензии по мере необходимости, а также проверить, что конечные пользователи могут использовать руководство Dynamics 365, а также использовать настраиваемую линейку бизнес-приложений после настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-108">In this guide, we will cover how to enroll your devices into your existing device management, apply licenses as needed, and validate that your end users are able to operate a Dynamics 365 Guide, as well as use custom line of business apps, after device set up.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="7a2b2-109">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7a2b2-109">Prerequisites</span></span>

<span data-ttu-id="7a2b2-110">Уже должна быть следующая инфраструктура:</span><span class="sxs-lookup"><span data-stu-id="7a2b2-110">The following infrastructure should already be in place:</span></span>
- <span data-ttu-id="7a2b2-111">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="7a2b2-111">Wi-Fi</span></span>
    - <span data-ttu-id="7a2b2-112">Внутренняя корпоративная сеть с доступом к внутренним ресурсам и ограниченным доступом к интернету или облачным службам</span><span class="sxs-lookup"><span data-stu-id="7a2b2-112">Internal corporate network with access to internal resources and limited access to the internet or Cloud services</span></span>
    - <span data-ttu-id="7a2b2-113">Проверка подлинности сертификата на основе устройства.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-113">Device-based certificate authentication.</span></span>
- <span data-ttu-id="7a2b2-114">Azure Active Directory (Azure AD) присоединяется к автозарегистру MDM (необходима подписка[Azure AD P1)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-114">Azure Active Directory (Azure AD) Join with MDM Auto Enrollment ([Azure AD P1 subscription](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) needed)</span></span>
- <span data-ttu-id="7a2b2-115">Управляемый MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-115">MDM (Intune) Managed</span></span>
    - <span data-ttu-id="7a2b2-116">Одно или несколько приложений развертываются с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-116">One or more applications are deployed via MDM.</span></span>
- <span data-ttu-id="7a2b2-117">Network</span><span class="sxs-lookup"><span data-stu-id="7a2b2-117">Network</span></span> 
    - <span data-ttu-id="7a2b2-118">Сертификаты (SCEP или PKCS)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-118">Certificates (SCEP or PKCS)</span></span>
    - <span data-ttu-id="7a2b2-119">Конфигурация прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7a2b2-119">Proxy configuration</span></span>
- <span data-ttu-id="7a2b2-120">Пользователи во входе с собственной корпоративной учетной записью (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-120">Users sign in with their own corporate account (Azure AD)</span></span>
    - <span data-ttu-id="7a2b2-121">Поддерживается один или несколько пользователей на устройство.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-121">Single or multiple users per device is supported.</span></span>
- <span data-ttu-id="7a2b2-122">Различные уровни конфигураций блокировки устройств, применяемые в зависимости от конкретных случаев использования, от полностью открытого до единого киоска приложений.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-122">Varying levels of device lockdown configurations applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>

## [<a name="guides-licensing-and-requirements"></a><span data-ttu-id="7a2b2-123">Руководства по лицензированию и требованиям</span><span class="sxs-lookup"><span data-stu-id="7a2b2-123">Guides Licensing and Requirements</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements#licensing-and-product-requirements)
- <span data-ttu-id="7a2b2-124">Учетная запись Azure AD</span><span class="sxs-lookup"><span data-stu-id="7a2b2-124">Azure AD account</span></span>
- <span data-ttu-id="7a2b2-125">Dynamics 365 Guides applications PC and HoloLens</span><span class="sxs-lookup"><span data-stu-id="7a2b2-125">Dynamics 365 Guides applications PC and HoloLens</span></span>
- <span data-ttu-id="7a2b2-126">Подписка на dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="7a2b2-126">Dynamics 365 Guides subscription</span></span>
    - <span data-ttu-id="7a2b2-127">Microsoft Dataverse (включено)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-127">Microsoft Dataverse (included)</span></span>
    - <span data-ttu-id="7a2b2-128">Power Apps (включено)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-128">Power Apps (included)</span></span>
- <span data-ttu-id="7a2b2-129">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7a2b2-129">Power BI Desktop</span></span>
- <span data-ttu-id="7a2b2-130">Подключение к сети</span><span class="sxs-lookup"><span data-stu-id="7a2b2-130">Network Connectivity</span></span>

![Схема подключенной сети Corp](./images/corpconnected-diagHL2-guides.png)

## <a name="stages-of-deployment"></a><span data-ttu-id="7a2b2-132">Этапы развертывания</span><span class="sxs-lookup"><span data-stu-id="7a2b2-132">Stages of Deployment</span></span>
### <a name="prepare"></a><span data-ttu-id="7a2b2-133">Подготовка</span><span class="sxs-lookup"><span data-stu-id="7a2b2-133">Prepare</span></span>
> [!div class="checklist"]
>- [<span data-ttu-id="7a2b2-134">Узнайте о необходимых для устройств HoloLens 2 инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-134">Learn about the infrastructure essentials for HoloLens 2 devices.</span></span>](hololens2-corp-connected-prepare.md#infrastructure-essentials)
>- [<span data-ttu-id="7a2b2-135">Узнайте больше о Azure AD и установите его, если его нет.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-135">Learn more about Azure AD and set up one if you don't have it.</span></span>](hololens2-corp-connected-prepare.md#azure-active-directory)
>- [<span data-ttu-id="7a2b2-136">Узнайте об управлении удостоверениями и о том, как наилучшим образом настроить учетные записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-136">Learn about Identity management and how to best set up Azure AD accounts.</span></span>](hololens2-corp-connected-prepare.md#identity-management)
>- [<span data-ttu-id="7a2b2-137">Дополнительные информацию о MDM и настройка в Intune, если у вас еще нет готовой.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-137">Learn more about MDM and set up with Intune if you don't already have one ready.</span></span>](hololens2-corp-connected-prepare.md#mobile-device-management)
>- [<span data-ttu-id="7a2b2-138">Ознакомьтесь с Wi-Fi на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-138">Familiarize yourself with certificate-based Wi-Fi.</span></span>](hololens2-corp-connected-prepare.md#certificates)
>- [<span data-ttu-id="7a2b2-139">Ознакомьтесь с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-139">Familiarize yourself with Proxy.</span></span>](hololens2-corp-connected-prepare.md#proxy)
>- [<span data-ttu-id="7a2b2-140">Понимание того, как можно использовать Line of Business Apps.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-140">Understand how you can use Line of Business Apps.</span></span>](hololens2-corp-connected-prepare.md#line-of-business-apps)
>- [<span data-ttu-id="7a2b2-141">Дополнительные новости о том, как можно использовать руководство для организации.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-141">Learn more about the way you can use Guides for your organization.</span></span>](hololens2-corp-connected-prepare.md#guides-playbook)
### <a name="configure"></a><span data-ttu-id="7a2b2-142">Настройка</span><span class="sxs-lookup"><span data-stu-id="7a2b2-142">Configure</span></span>
> [!div class="checklist"]
>- [<span data-ttu-id="7a2b2-143">Создание пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-143">How to create users and groups.</span></span>](hololens2-corp-connected-configure.md#azure-users-and-groups)
>- [<span data-ttu-id="7a2b2-144">Настройка автоматической регистрации.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-144">How to set up Auto Enrollment.</span></span>](hololens2-corp-connected-configure.md#auto-enrollment-on-hololens-2)
>- [<span data-ttu-id="7a2b2-145">Настройка сертификатов Wi-Fi профилей для корпоративных Wi-Fi подключения.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-145">How to set up Wi-Fi certificates and profiles for Corporate Wi-Fi Connectivity.</span></span>](hololens2-corp-connected-configure.md#corporate-wi-fi-connectivity)
>- [<span data-ttu-id="7a2b2-146">Загрузка и назначение пакетов приложений для бизнеса (LOB).</span><span class="sxs-lookup"><span data-stu-id="7a2b2-146">Upload and Assign Line of Business (LOB) App packages.</span></span>](hololens2-corp-connected-configure.md#app-deployment)
>- [<span data-ttu-id="7a2b2-147">Руководство по настройке Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-147">Setup Dynamics 365 Guides.</span></span>](hololens2-corp-connected-configure.md#setup-guides-application-licenses-dataverse-and-authoring)
>- [<span data-ttu-id="7a2b2-148">Настройка режима киоска (необязательный).</span><span class="sxs-lookup"><span data-stu-id="7a2b2-148">How to configure Kiosk Mode (optional).</span></span>](hololens2-corp-connected-configure.md#optional-kiosk-mode)
>- [<span data-ttu-id="7a2b2-149">Настройка WDAC (необязательно).</span><span class="sxs-lookup"><span data-stu-id="7a2b2-149">How to configure WDAC (optional).</span></span>](hololens2-corp-connected-configure.md#optional-wdac)
### <a name="deploy"></a><span data-ttu-id="7a2b2-150">Развертывание</span><span class="sxs-lookup"><span data-stu-id="7a2b2-150">Deploy</span></span>
> [!div class="checklist"]
>-  [<span data-ttu-id="7a2b2-151">Проверка регистрации с помощью устройства и MDM.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-151">Validate enrollment via device and MDM.</span></span>](hololens2-corp-connected-deploy.md#enrollment-validation)
>-  [<span data-ttu-id="7a2b2-152">Проверка Wi-Fi сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-152">Validate Wi-Fi certificates.</span></span>](hololens2-corp-connected-deploy.md#wi-fi-certificate-validation)
>-  [<span data-ttu-id="7a2b2-153">Проверка установки приложения LOB.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-153">Validate LOB app install.</span></span>](hololens2-corp-connected-deploy.md#validate-lob-app-install)
>-  [<span data-ttu-id="7a2b2-154">Проверка руководств с помощью авторинга и работы.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-154">Validate Guides via authoring and operating.</span></span>](hololens2-corp-connected-deploy.md#validate-dynamics-365-guides)
### <a name="maintain"></a><span data-ttu-id="7a2b2-155">Обслуживание</span><span class="sxs-lookup"><span data-stu-id="7a2b2-155">Maintain</span></span>
> [!div class="checklist"]
>- [<span data-ttu-id="7a2b2-156">Обновление HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-156">Update HoloLens 2.</span></span>](hololens2-corp-connected-maintain.md#update-hololens)
>- [<span data-ttu-id="7a2b2-157">Обновление руководств (приложений для хранения).</span><span class="sxs-lookup"><span data-stu-id="7a2b2-157">How to update Guides (store apps).</span></span>](hololens2-corp-connected-maintain.md#how-to-update-dynamics-365-guides-and-other-store-apps)
>- [<span data-ttu-id="7a2b2-158">Обновление приложений LOB.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-158">How to update LOB apps.</span></span>](hololens2-corp-connected-maintain.md#how-to-update-lob-apps) 
>- [<span data-ttu-id="7a2b2-159">План разработки.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-159">Development plan.</span></span>](hololens2-corp-connected-maintain.md#development-plan) 
>- [<span data-ttu-id="7a2b2-160">Создание плана поддержки.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-160">Making a support plan.</span></span>](hololens2-corp-connected-maintain.md#support-plan)
>- [<span data-ttu-id="7a2b2-161">Параметры управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-161">Device management options.</span></span>](hololens2-corp-connected-maintain.md#device-management)

## <a name="next-step"></a><span data-ttu-id="7a2b2-162">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="7a2b2-162">Next step</span></span> 
> [!div class="nextstepaction"]
> [<span data-ttu-id="7a2b2-163">Развертывание подключенных к корпорации — подготовка</span><span class="sxs-lookup"><span data-stu-id="7a2b2-163">Corporate connected deployment - Prepare</span></span>](hololens2-corp-connected-prepare.md)
