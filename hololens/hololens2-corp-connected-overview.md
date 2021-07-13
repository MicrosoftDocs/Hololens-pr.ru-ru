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
ms.openlocfilehash: f2f7e1425a208e1f466d995f66118b7e68984242
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113637019"
---
# <a name="deployment-guide---corporate-connected-hololens-2-with-dynamics-365-guides---overview"></a><span data-ttu-id="70b77-104">руководство по развертыванию: корпоративные подключенные HoloLens 2 с руководствами по Dynamics 365 — обзор</span><span class="sxs-lookup"><span data-stu-id="70b77-104">Deployment Guide - Corporate Connected HoloLens 2 with Dynamics 365 Guides - Overview</span></span>

<span data-ttu-id="70b77-105">это руководство поможет ит-специалистам спланировать и развернуть Microsoft HoloLens 2 устройства с помощью руководств Dynamics 365 (руководств) в своей организации.</span><span class="sxs-lookup"><span data-stu-id="70b77-105">This guide will help IT professionals plan for and deploy Microsoft HoloLens 2 devices with Dynamics 365 Guides (Guides) to their organization.</span></span> <span data-ttu-id="70b77-106">Это руководство отлично подходит для пилотных проектов, а также для развертывания в рабочей среде и аналогично [сценарию б. Разверните руководство по сети организации](/hololens/common-scenarios#scenario-b-deploy-inside-your-organizations-network) .</span><span class="sxs-lookup"><span data-stu-id="70b77-106">This guide is great for pilots as well as production deployments and is similar to the [Scenario B: Deploy inside your organization's network](/hololens/common-scenarios#scenario-b-deploy-inside-your-organizations-network) guide.</span></span> <span data-ttu-id="70b77-107">после проверки концепции воспользуйтесь этим руководством, чтобы перейти к интеграции HoloLens в вашу организацию.</span><span class="sxs-lookup"><span data-stu-id="70b77-107">After testing your proof-of-concept, use this guide to move forward with integrating HoloLens into your organization.</span></span>

<span data-ttu-id="70b77-108">В этом руководство мы рассмотрим, как зарегистрировать устройства в существующем управлении устройствами, применить лицензии по мере необходимости и проверить, что конечные пользователи могут работать с руководством по Dynamics 365, а также использовать настраиваемые бизнес-приложения после настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="70b77-108">In this guide, we will cover how to enroll your devices into your existing device management, apply licenses as needed, and validate that your end users are able to operate a Dynamics 365 Guide, as well as use custom line of business apps, after device set up.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="70b77-109">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="70b77-109">Prerequisites</span></span>

<span data-ttu-id="70b77-110">Уже должна быть выполнена следующая инфраструктура:</span><span class="sxs-lookup"><span data-stu-id="70b77-110">The following infrastructure should already be in place:</span></span>
- <span data-ttu-id="70b77-111">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="70b77-111">Wi-Fi</span></span>
    - <span data-ttu-id="70b77-112">Внутренняя корпоративная сеть с доступом к внутренним ресурсам и ограниченный доступ к Интернету или облачным службам.</span><span class="sxs-lookup"><span data-stu-id="70b77-112">Internal corporate network with access to internal resources and limited access to the internet or Cloud services</span></span>
    - <span data-ttu-id="70b77-113">Проверка подлинности сертификата на основе устройства.</span><span class="sxs-lookup"><span data-stu-id="70b77-113">Device-based certificate authentication.</span></span>
- <span data-ttu-id="70b77-114">присоединение Azure Active Directory (Azure ad) с автоматической регистрацией MDM (требуется[подписка Azure AD P1](/azure/active-directory/fundamentals/active-directory-whatis) )</span><span class="sxs-lookup"><span data-stu-id="70b77-114">Azure Active Directory (Azure AD) Join with MDM Auto Enrollment ([Azure AD P1 subscription](/azure/active-directory/fundamentals/active-directory-whatis) needed)</span></span>
- <span data-ttu-id="70b77-115">Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="70b77-115">MDM (Intune) Managed</span></span>
    - <span data-ttu-id="70b77-116">Одно или несколько приложений развертываются с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="70b77-116">One or more applications are deployed via MDM.</span></span>
- <span data-ttu-id="70b77-117">Сеть</span><span class="sxs-lookup"><span data-stu-id="70b77-117">Network</span></span> 
    - <span data-ttu-id="70b77-118">Сертификаты (SCEP или PKCS)</span><span class="sxs-lookup"><span data-stu-id="70b77-118">Certificates (SCEP or PKCS)</span></span>
    - <span data-ttu-id="70b77-119">настройки прокси-сервера;</span><span class="sxs-lookup"><span data-stu-id="70b77-119">Proxy configuration</span></span>
- <span data-ttu-id="70b77-120">Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="70b77-120">Users sign in with their own corporate account (Azure AD)</span></span>
    - <span data-ttu-id="70b77-121">Поддерживается одно или несколько пользователей на каждом устройстве.</span><span class="sxs-lookup"><span data-stu-id="70b77-121">Single or multiple users per device is supported.</span></span>
- <span data-ttu-id="70b77-122">Различные уровни конфигурации блокировки устройств, применяемые на основе конкретных вариантов использования, от полного открытия до одного киоска приложения.</span><span class="sxs-lookup"><span data-stu-id="70b77-122">Varying levels of device lockdown configurations applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>

## <a name="guides-licensing-and-requirements"></a>[<span data-ttu-id="70b77-123">Руководства по лицензированию и требованиям</span><span class="sxs-lookup"><span data-stu-id="70b77-123">Guides Licensing and Requirements</span></span>](/dynamics365/mixed-reality/guides/requirements#licensing-and-product-requirements)

- <span data-ttu-id="70b77-124">Учетная запись Azure AD</span><span class="sxs-lookup"><span data-stu-id="70b77-124">Azure AD account</span></span>
- <span data-ttu-id="70b77-125">Dynamics 365 предлагает приложениям ПК и HoloLens</span><span class="sxs-lookup"><span data-stu-id="70b77-125">Dynamics 365 Guides applications PC and HoloLens</span></span>
- <span data-ttu-id="70b77-126">Подписка на Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="70b77-126">Dynamics 365 Guides subscription</span></span>
    - <span data-ttu-id="70b77-127">Microsoft Инверсия (включена)</span><span class="sxs-lookup"><span data-stu-id="70b77-127">Microsoft Dataverse (included)</span></span>
    - <span data-ttu-id="70b77-128">Power Apps (включена)</span><span class="sxs-lookup"><span data-stu-id="70b77-128">Power Apps (included)</span></span>
- <span data-ttu-id="70b77-129">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="70b77-129">Power BI Desktop</span></span>
- <span data-ttu-id="70b77-130">Сетевое подключение</span><span class="sxs-lookup"><span data-stu-id="70b77-130">Network Connectivity</span></span>

<span data-ttu-id="70b77-131">[![Схема сети с подключенной корпоративной сетью, этап 1 ](./images/deployment-guides-revised-scenario-b-01-1.png)](./images/deployment-guides-revised-scenario-b-01-1.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="70b77-131">[ ![Corp connected network diagram, stage 1](./images/deployment-guides-revised-scenario-b-01-1.png) ](./images/deployment-guides-revised-scenario-b-01-1.png#lightbox)</span></span>

<span data-ttu-id="70b77-132">[![Схема сетей, подключенных к корпоративной сети, этап 2 ](./images/deployment-guides-revised-scenario-b-02-1.png)](./images/deployment-guides-revised-scenario-b-02-1.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="70b77-132">[ ![Corp connected network diagram, stage 2](./images/deployment-guides-revised-scenario-b-02-1.png) ](./images/deployment-guides-revised-scenario-b-02-1.png#lightbox)</span></span>

## <a name="in-this-guide-you-will"></a><span data-ttu-id="70b77-133">В руководстве описаны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="70b77-133">In this guide you will:</span></span>
### <a name="prepare"></a><span data-ttu-id="70b77-134">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="70b77-134">Prepare</span></span>
> [!div class="checklist"]
>- [<span data-ttu-id="70b77-135">ознакомьтесь с основными сведениями об инфраструктуре для HoloLens 2 устройств.</span><span class="sxs-lookup"><span data-stu-id="70b77-135">Learn about the infrastructure essentials for HoloLens 2 devices.</span></span>](hololens2-corp-connected-prepare.md#infrastructure-essentials)
>- [<span data-ttu-id="70b77-136">Узнайте больше об Azure AD и настройте его, если у вас его нет.</span><span class="sxs-lookup"><span data-stu-id="70b77-136">Learn more about Azure AD and set up one if you don't have it.</span></span>](hololens2-corp-connected-prepare.md#azure-active-directory)
>- [<span data-ttu-id="70b77-137">Узнайте больше об управлении удостоверениями и о том, как лучше настроить учетные записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="70b77-137">Learn about Identity management and how to best set up Azure AD accounts.</span></span>](hololens2-corp-connected-prepare.md#identity-management)
>- [<span data-ttu-id="70b77-138">Ознакомьтесь с дополнительными сведениями об MDM и настройте Intune, если у вас ее еще нет.</span><span class="sxs-lookup"><span data-stu-id="70b77-138">Learn more about MDM and set up with Intune if you don't already have one ready.</span></span>](hololens2-corp-connected-prepare.md#mobile-device-management)
>- [<span data-ttu-id="70b77-139">Ознакомьтесь с Wi-Fi на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="70b77-139">Familiarize yourself with certificate-based Wi-Fi.</span></span>](hololens2-corp-connected-prepare.md#certificates)
>- [<span data-ttu-id="70b77-140">Ознакомьтесь с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="70b77-140">Familiarize yourself with Proxy.</span></span>](hololens2-corp-connected-prepare.md#proxy)
>- [<span data-ttu-id="70b77-141">Узнайте, как можно использовать бизнес-приложения.</span><span class="sxs-lookup"><span data-stu-id="70b77-141">Understand how you can use Line of Business Apps.</span></span>](hololens2-corp-connected-prepare.md#line-of-business-apps)
>- [<span data-ttu-id="70b77-142">Узнайте больше о том, как можно использовать руководства для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="70b77-142">Learn more about the way you can use Guides for your organization.</span></span>](hololens2-corp-connected-prepare.md#guides-playbook)
### <a name="configure"></a><span data-ttu-id="70b77-143">Configure</span><span class="sxs-lookup"><span data-stu-id="70b77-143">Configure</span></span>
> [!div class="checklist"]
>- [<span data-ttu-id="70b77-144">Создание пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="70b77-144">How to create users and groups.</span></span>](hololens2-corp-connected-configure.md#azure-users-and-groups)
>- [<span data-ttu-id="70b77-145">Как настроить автоматическую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="70b77-145">How to set up Auto Enrollment.</span></span>](hololens2-corp-connected-configure.md#auto-enrollment-on-hololens-2)
>- [<span data-ttu-id="70b77-146">Как настроить сертификаты и профили Wi-Fi для корпоративного Wi-Fi подключения.</span><span class="sxs-lookup"><span data-stu-id="70b77-146">How to set up Wi-Fi certificates and profiles for Corporate Wi-Fi Connectivity.</span></span>](hololens2-corp-connected-configure.md#corporate-wi-fi-connectivity)
>- [<span data-ttu-id="70b77-147">Upload и назначение пакетов бизнес-приложений (LOB).</span><span class="sxs-lookup"><span data-stu-id="70b77-147">Upload and Assign Line of Business (LOB) App packages.</span></span>](hololens2-corp-connected-configure.md#app-deployment)
>- [<span data-ttu-id="70b77-148">Настройка руководств по Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="70b77-148">Setup Dynamics 365 Guides.</span></span>](hololens2-corp-connected-configure.md#setup-guides-application-licenses-dataverse-and-authoring)
>- [<span data-ttu-id="70b77-149">Настройка режима киоска (необязательно).</span><span class="sxs-lookup"><span data-stu-id="70b77-149">How to configure Kiosk Mode (optional).</span></span>](hololens2-corp-connected-configure.md#optional-kiosk-mode)
>- [<span data-ttu-id="70b77-150">Настройка WDAC (необязательно).</span><span class="sxs-lookup"><span data-stu-id="70b77-150">How to configure WDAC (optional).</span></span>](hololens2-corp-connected-configure.md#optional-wdac)
### <a name="deploy"></a><span data-ttu-id="70b77-151">Развертывание</span><span class="sxs-lookup"><span data-stu-id="70b77-151">Deploy</span></span>
> [!div class="checklist"]
>-  [<span data-ttu-id="70b77-152">Проверка регистрации через устройство и MDM.</span><span class="sxs-lookup"><span data-stu-id="70b77-152">Validate enrollment via device and MDM.</span></span>](hololens2-corp-connected-deploy.md#enrollment-validation)
>-  [<span data-ttu-id="70b77-153">Проверка сертификатов Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="70b77-153">Validate Wi-Fi certificates.</span></span>](hololens2-corp-connected-deploy.md#wi-fi-certificate-validation)
>-  [<span data-ttu-id="70b77-154">Проверка установки бизнес-приложения.</span><span class="sxs-lookup"><span data-stu-id="70b77-154">Validate LOB app install.</span></span>](hololens2-corp-connected-deploy.md#validate-lob-app-install)
>-  [<span data-ttu-id="70b77-155">Проверка руководств с помощью разработки и работы.</span><span class="sxs-lookup"><span data-stu-id="70b77-155">Validate Guides via authoring and operating.</span></span>](hololens2-corp-connected-deploy.md#validate-dynamics-365-guides)
### <a name="maintain"></a><span data-ttu-id="70b77-156">Техническое обслуживание</span><span class="sxs-lookup"><span data-stu-id="70b77-156">Maintain</span></span>
> [!div class="checklist"]
>- [<span data-ttu-id="70b77-157">Обновление HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="70b77-157">Update HoloLens 2.</span></span>](hololens2-corp-connected-maintain.md#update-hololens)
>- [<span data-ttu-id="70b77-158">Инструкции по обновлению руководств (приложений магазина).</span><span class="sxs-lookup"><span data-stu-id="70b77-158">How to update Guides (store apps).</span></span>](hololens2-corp-connected-maintain.md#how-to-update-dynamics-365-guides-and-other-store-apps)
>- [<span data-ttu-id="70b77-159">Обновление бизнес-приложений.</span><span class="sxs-lookup"><span data-stu-id="70b77-159">How to update LOB apps.</span></span>](hololens2-corp-connected-maintain.md#how-to-update-lob-apps) 
>- [<span data-ttu-id="70b77-160">План разработки.</span><span class="sxs-lookup"><span data-stu-id="70b77-160">Development plan.</span></span>](hololens2-corp-connected-maintain.md#development-plan) 
>- [<span data-ttu-id="70b77-161">Создание плана поддержки.</span><span class="sxs-lookup"><span data-stu-id="70b77-161">Making a support plan.</span></span>](hololens2-corp-connected-maintain.md#support-plan)
>- [<span data-ttu-id="70b77-162">Параметры управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="70b77-162">Device management options.</span></span>](hololens2-corp-connected-maintain.md#device-management)

## <a name="next-step"></a><span data-ttu-id="70b77-163">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="70b77-163">Next step</span></span> 
> [!div class="nextstepaction"]
> [<span data-ttu-id="70b77-164">Развертывание с корпоративным подключением — подготовка</span><span class="sxs-lookup"><span data-stu-id="70b77-164">Corporate connected deployment - Prepare</span></span>](hololens2-corp-connected-prepare.md)
