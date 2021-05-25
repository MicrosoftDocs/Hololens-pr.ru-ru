---
title: Руководство по развертыванию — корпоративное подключение HoloLens 2 с помощью Dynamics 365 Guides-Overview
description: Узнайте, как зарегистрировать устройства HoloLens 2 в руководствах по Dynamics 365 через подключенную корпоративную сеть.
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
ms.openlocfilehash: ee6c24f65e5990f1e84a71d86b24dd782cf9f4cc
ms.sourcegitcommit: 29573e577381a23891e9557884a6dfdaac0c1c48
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110397209"
---
# <a name="deployment-guide---corporate-connected-hololens-2-with-dynamics-365-guides---overview"></a><span data-ttu-id="c35be-104">Руководство по развертыванию — корпоративное подключение HoloLens 2 с помощью Dynamics 365 Guides-Overview</span><span class="sxs-lookup"><span data-stu-id="c35be-104">Deployment Guide - Corporate Connected HoloLens 2 with Dynamics 365 Guides - Overview</span></span>

<span data-ttu-id="c35be-105">Это руководство поможет ИТ-специалистам спланировать и развернуть устройства Microsoft HoloLens 2 с помощью Dynamics 365 Guides (руководства) в своей организации.</span><span class="sxs-lookup"><span data-stu-id="c35be-105">This guide will help IT professionals plan for and deploy Microsoft HoloLens 2 devices with Dynamics 365 Guides (Guides) to their organization.</span></span> <span data-ttu-id="c35be-106">Это руководство отлично подходит для пилотных проектов, а также для развертывания в рабочей среде и аналогично [сценарию б. Разверните руководство по сети организации](https://docs.microsoft.com/hololens/common-scenarios#scenario-b-deploy-inside-your-organizations-network) .</span><span class="sxs-lookup"><span data-stu-id="c35be-106">This guide is great for pilots as well as production deployments and is similar to the [Scenario B: Deploy inside your organization's network](https://docs.microsoft.com/hololens/common-scenarios#scenario-b-deploy-inside-your-organizations-network) guide.</span></span> <span data-ttu-id="c35be-107">После проверки концепции воспользуйтесь этим руководством, чтобы перейти к интеграции HoloLens в вашу организацию.</span><span class="sxs-lookup"><span data-stu-id="c35be-107">After testing your proof-of-concept, use this guide to move forward with integrating HoloLens into your organization.</span></span>

<span data-ttu-id="c35be-108">В этом руководство мы рассмотрим, как зарегистрировать устройства в существующем управлении устройствами, применить лицензии по мере необходимости и проверить, что конечные пользователи могут работать с руководством по Dynamics 365, а также использовать настраиваемые бизнес-приложения после настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="c35be-108">In this guide, we will cover how to enroll your devices into your existing device management, apply licenses as needed, and validate that your end users are able to operate a Dynamics 365 Guide, as well as use custom line of business apps, after device set up.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="c35be-109">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="c35be-109">Prerequisites</span></span>

<span data-ttu-id="c35be-110">Уже должна быть выполнена следующая инфраструктура:</span><span class="sxs-lookup"><span data-stu-id="c35be-110">The following infrastructure should already be in place:</span></span>
- <span data-ttu-id="c35be-111">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="c35be-111">Wi-Fi</span></span>
    - <span data-ttu-id="c35be-112">Внутренняя корпоративная сеть с доступом к внутренним ресурсам и ограниченный доступ к Интернету или облачным службам.</span><span class="sxs-lookup"><span data-stu-id="c35be-112">Internal corporate network with access to internal resources and limited access to the internet or Cloud services</span></span>
    - <span data-ttu-id="c35be-113">Проверка подлинности сертификата на основе устройства.</span><span class="sxs-lookup"><span data-stu-id="c35be-113">Device-based certificate authentication.</span></span>
- <span data-ttu-id="c35be-114">Присоединение Azure Active Directory (Azure AD) с автоматической регистрацией MDM (требуется[Подписка Azure AD P1](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) )</span><span class="sxs-lookup"><span data-stu-id="c35be-114">Azure Active Directory (Azure AD) Join with MDM Auto Enrollment ([Azure AD P1 subscription](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) needed)</span></span>
- <span data-ttu-id="c35be-115">Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="c35be-115">MDM (Intune) Managed</span></span>
    - <span data-ttu-id="c35be-116">Одно или несколько приложений развертываются с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="c35be-116">One or more applications are deployed via MDM.</span></span>
- <span data-ttu-id="c35be-117">Сеть</span><span class="sxs-lookup"><span data-stu-id="c35be-117">Network</span></span> 
    - <span data-ttu-id="c35be-118">Сертификаты (SCEP или PKCS)</span><span class="sxs-lookup"><span data-stu-id="c35be-118">Certificates (SCEP or PKCS)</span></span>
    - <span data-ttu-id="c35be-119">настройки прокси-сервера;</span><span class="sxs-lookup"><span data-stu-id="c35be-119">Proxy configuration</span></span>
- <span data-ttu-id="c35be-120">Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="c35be-120">Users sign in with their own corporate account (Azure AD)</span></span>
    - <span data-ttu-id="c35be-121">Поддерживается одно или несколько пользователей на каждом устройстве.</span><span class="sxs-lookup"><span data-stu-id="c35be-121">Single or multiple users per device is supported.</span></span>
- <span data-ttu-id="c35be-122">Различные уровни конфигурации блокировки устройств, применяемые на основе конкретных вариантов использования, от полного открытия до одного киоска приложения.</span><span class="sxs-lookup"><span data-stu-id="c35be-122">Varying levels of device lockdown configurations applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>

## <a name="guides-licensing-and-requirements"></a>[<span data-ttu-id="c35be-123">Руководства по лицензированию и требованиям</span><span class="sxs-lookup"><span data-stu-id="c35be-123">Guides Licensing and Requirements</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements#licensing-and-product-requirements)
- <span data-ttu-id="c35be-124">Учетная запись Azure AD</span><span class="sxs-lookup"><span data-stu-id="c35be-124">Azure AD account</span></span>
- <span data-ttu-id="c35be-125">Dynamics 365 руководства по приложениям PC и HoloLens</span><span class="sxs-lookup"><span data-stu-id="c35be-125">Dynamics 365 Guides applications PC and HoloLens</span></span>
- <span data-ttu-id="c35be-126">Подписка на Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="c35be-126">Dynamics 365 Guides subscription</span></span>
    - <span data-ttu-id="c35be-127">Microsoft Инверсия (включена)</span><span class="sxs-lookup"><span data-stu-id="c35be-127">Microsoft Dataverse (included)</span></span>
    - <span data-ttu-id="c35be-128">Приложения Power Apps (включенные)</span><span class="sxs-lookup"><span data-stu-id="c35be-128">Power Apps (included)</span></span>
- <span data-ttu-id="c35be-129">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="c35be-129">Power BI Desktop</span></span>
- <span data-ttu-id="c35be-130">Сетевое подключение</span><span class="sxs-lookup"><span data-stu-id="c35be-130">Network Connectivity</span></span>

<span data-ttu-id="c35be-131">[![Схема сети с подключенной корпоративной сетью, этап 1 ](./images/deployment-guides-revised-scenario-b-01-1.png)](./images/deployment-guides-revised-scenario-b-01-1.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c35be-131">[ ![Corp connected network diagram, stage 1](./images/deployment-guides-revised-scenario-b-01-1.png) ](./images/deployment-guides-revised-scenario-b-01-1.png#lightbox)</span></span>

<span data-ttu-id="c35be-132">[![Схема сетей, подключенных к корпоративной сети, этап 2 ](./images/deployment-guides-revised-scenario-b-02-1.png)](./images/deployment-guides-revised-scenario-b-02-1.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c35be-132">[ ![Corp connected network diagram, stage 2](./images/deployment-guides-revised-scenario-b-02-1.png) ](./images/deployment-guides-revised-scenario-b-02-1.png#lightbox)</span></span>

## <a name="in-this-guide-you-will"></a><span data-ttu-id="c35be-133">В руководстве описаны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c35be-133">In this guide you will:</span></span>
### <a name="prepare"></a><span data-ttu-id="c35be-134">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="c35be-134">Prepare</span></span>
> [!div class="checklist"]
>- [<span data-ttu-id="c35be-135">Ознакомьтесь с основными сведениями об инфраструктуре для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="c35be-135">Learn about the infrastructure essentials for HoloLens 2 devices.</span></span>](hololens2-corp-connected-prepare.md#infrastructure-essentials)
>- [<span data-ttu-id="c35be-136">Узнайте больше об Azure AD и настройте его, если у вас его нет.</span><span class="sxs-lookup"><span data-stu-id="c35be-136">Learn more about Azure AD and set up one if you don't have it.</span></span>](hololens2-corp-connected-prepare.md#azure-active-directory)
>- [<span data-ttu-id="c35be-137">Узнайте больше об управлении удостоверениями и о том, как лучше настроить учетные записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c35be-137">Learn about Identity management and how to best set up Azure AD accounts.</span></span>](hololens2-corp-connected-prepare.md#identity-management)
>- [<span data-ttu-id="c35be-138">Ознакомьтесь с дополнительными сведениями об MDM и настройте Intune, если у вас ее еще нет.</span><span class="sxs-lookup"><span data-stu-id="c35be-138">Learn more about MDM and set up with Intune if you don't already have one ready.</span></span>](hololens2-corp-connected-prepare.md#mobile-device-management)
>- [<span data-ttu-id="c35be-139">Ознакомьтесь с Wi-Fi на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c35be-139">Familiarize yourself with certificate-based Wi-Fi.</span></span>](hololens2-corp-connected-prepare.md#certificates)
>- [<span data-ttu-id="c35be-140">Ознакомьтесь с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="c35be-140">Familiarize yourself with Proxy.</span></span>](hololens2-corp-connected-prepare.md#proxy)
>- [<span data-ttu-id="c35be-141">Узнайте, как можно использовать бизнес-приложения.</span><span class="sxs-lookup"><span data-stu-id="c35be-141">Understand how you can use Line of Business Apps.</span></span>](hololens2-corp-connected-prepare.md#line-of-business-apps)
>- [<span data-ttu-id="c35be-142">Узнайте больше о том, как можно использовать руководства для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="c35be-142">Learn more about the way you can use Guides for your organization.</span></span>](hololens2-corp-connected-prepare.md#guides-playbook)
### <a name="configure"></a><span data-ttu-id="c35be-143">Configure</span><span class="sxs-lookup"><span data-stu-id="c35be-143">Configure</span></span>
> [!div class="checklist"]
>- [<span data-ttu-id="c35be-144">Создание пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="c35be-144">How to create users and groups.</span></span>](hololens2-corp-connected-configure.md#azure-users-and-groups)
>- [<span data-ttu-id="c35be-145">Как настроить автоматическую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="c35be-145">How to set up Auto Enrollment.</span></span>](hololens2-corp-connected-configure.md#auto-enrollment-on-hololens-2)
>- [<span data-ttu-id="c35be-146">Как настроить сертификаты и профили Wi-Fi для корпоративного Wi-Fi подключения.</span><span class="sxs-lookup"><span data-stu-id="c35be-146">How to set up Wi-Fi certificates and profiles for Corporate Wi-Fi Connectivity.</span></span>](hololens2-corp-connected-configure.md#corporate-wi-fi-connectivity)
>- [<span data-ttu-id="c35be-147">Отправка и назначение пакетов бизнес-приложений (LOB).</span><span class="sxs-lookup"><span data-stu-id="c35be-147">Upload and Assign Line of Business (LOB) App packages.</span></span>](hololens2-corp-connected-configure.md#app-deployment)
>- [<span data-ttu-id="c35be-148">Настройка руководств по Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c35be-148">Setup Dynamics 365 Guides.</span></span>](hololens2-corp-connected-configure.md#setup-guides-application-licenses-dataverse-and-authoring)
>- [<span data-ttu-id="c35be-149">Настройка режима киоска (необязательно).</span><span class="sxs-lookup"><span data-stu-id="c35be-149">How to configure Kiosk Mode (optional).</span></span>](hololens2-corp-connected-configure.md#optional-kiosk-mode)
>- [<span data-ttu-id="c35be-150">Настройка WDAC (необязательно).</span><span class="sxs-lookup"><span data-stu-id="c35be-150">How to configure WDAC (optional).</span></span>](hololens2-corp-connected-configure.md#optional-wdac)
### <a name="deploy"></a><span data-ttu-id="c35be-151">Развертывание</span><span class="sxs-lookup"><span data-stu-id="c35be-151">Deploy</span></span>
> [!div class="checklist"]
>-  [<span data-ttu-id="c35be-152">Проверка регистрации через устройство и MDM.</span><span class="sxs-lookup"><span data-stu-id="c35be-152">Validate enrollment via device and MDM.</span></span>](hololens2-corp-connected-deploy.md#enrollment-validation)
>-  [<span data-ttu-id="c35be-153">Проверка сертификатов Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="c35be-153">Validate Wi-Fi certificates.</span></span>](hololens2-corp-connected-deploy.md#wi-fi-certificate-validation)
>-  [<span data-ttu-id="c35be-154">Проверка установки бизнес-приложения.</span><span class="sxs-lookup"><span data-stu-id="c35be-154">Validate LOB app install.</span></span>](hololens2-corp-connected-deploy.md#validate-lob-app-install)
>-  [<span data-ttu-id="c35be-155">Проверка руководств с помощью разработки и работы.</span><span class="sxs-lookup"><span data-stu-id="c35be-155">Validate Guides via authoring and operating.</span></span>](hololens2-corp-connected-deploy.md#validate-dynamics-365-guides)
### <a name="maintain"></a><span data-ttu-id="c35be-156">Техническое обслуживание</span><span class="sxs-lookup"><span data-stu-id="c35be-156">Maintain</span></span>
> [!div class="checklist"]
>- [<span data-ttu-id="c35be-157">Обновите HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="c35be-157">Update HoloLens 2.</span></span>](hololens2-corp-connected-maintain.md#update-hololens)
>- [<span data-ttu-id="c35be-158">Инструкции по обновлению руководств (приложений магазина).</span><span class="sxs-lookup"><span data-stu-id="c35be-158">How to update Guides (store apps).</span></span>](hololens2-corp-connected-maintain.md#how-to-update-dynamics-365-guides-and-other-store-apps)
>- [<span data-ttu-id="c35be-159">Обновление бизнес-приложений.</span><span class="sxs-lookup"><span data-stu-id="c35be-159">How to update LOB apps.</span></span>](hololens2-corp-connected-maintain.md#how-to-update-lob-apps) 
>- [<span data-ttu-id="c35be-160">План разработки.</span><span class="sxs-lookup"><span data-stu-id="c35be-160">Development plan.</span></span>](hololens2-corp-connected-maintain.md#development-plan) 
>- [<span data-ttu-id="c35be-161">Создание плана поддержки.</span><span class="sxs-lookup"><span data-stu-id="c35be-161">Making a support plan.</span></span>](hololens2-corp-connected-maintain.md#support-plan)
>- [<span data-ttu-id="c35be-162">Параметры управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="c35be-162">Device management options.</span></span>](hololens2-corp-connected-maintain.md#device-management)

## <a name="next-step"></a><span data-ttu-id="c35be-163">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="c35be-163">Next step</span></span> 
> [!div class="nextstepaction"]
> [<span data-ttu-id="c35be-164">Развертывание с корпоративным подключением — подготовка</span><span class="sxs-lookup"><span data-stu-id="c35be-164">Corporate connected deployment - Prepare</span></span>](hololens2-corp-connected-prepare.md)
