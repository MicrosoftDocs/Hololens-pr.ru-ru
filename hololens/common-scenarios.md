---
title: Распространенные сценарии развертывания инфраструктуры
description: Узнайте о некоторых наиболее распространенных сценариях развертывания, основанных на различных развертываниях инфраструктуры для смешанной реальности.
ms.assetid: 651d0430-bfbc-4685-a4fd-db7c33ce9325
ms.date: 3/24/2021
keywords: hololens
manager: yannisle
ms.prod: hololens
ms.sitesec: library
author: scooley
ms.author: v-evmill
ms.topic: article
audience: ITPro
ms.localizationpriority: medium
appliesto:
- HoloLens 2
ms.openlocfilehash: 4b9bd4335e45180276d69af2ce5f33a38ecb800f
ms.sourcegitcommit: d7c86ccad7be32f7223d4b801083798454fda740
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2021
ms.locfileid: "11448497"
---
# <a name="common-infrastructure-deployment-scenarios-overview"></a><span data-ttu-id="4d7a6-104">Общие сценарии развертывания инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="4d7a6-104">Common Infrastructure Deployment Scenarios Overview</span></span>

<span data-ttu-id="4d7a6-105">Эти следующие сведения предоставляют обзор архитектуры высокого уровня для трех распространенных сценариев при развертывании и управлении устройствами Microsoft HoloLens 2 на предприятии.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-105">This following information provides a high-level architecture overview for three common scenarios when deploying and managing Microsoft HoloLens 2 devices within the enterprise.</span></span> <span data-ttu-id="4d7a6-106">Часто управление устройствами и доступ к ресурсам организации во многом определяется уже на месте факторами.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-106">Often how you manage your devices and how to access your organization's resources is largely determined by factors already in place.</span></span> <span data-ttu-id="4d7a6-107">На основе существующей инфраструктуры мы приглашаем вас просмотреть общий стиль управления устройствами в следующих сценариях и опробуете наши руководства для развертывания в сценарии, который соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-107">Based on the existing infrastructure we invite you to review the common device management style in the following scenarios, and try out our guides for deploying in the scenario matching your needs.</span></span>

## <a name="scenarios"></a><span data-ttu-id="4d7a6-108">Сценарии</span><span class="sxs-lookup"><span data-stu-id="4d7a6-108">Scenarios</span></span>

<span data-ttu-id="4d7a6-109">На приведенной ниже схеме представлены три типичных сценария развертывания HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-109">The diagram below represents three typical scenarios for HoloLens 2 deployments.</span></span>
![Схема сценариев](images/scenarios.jpg)

### <a name="scenario-a-deploy-to-cloud-connect-devices"></a><span data-ttu-id="4d7a6-111">Сценарий A. Развертывание устройств облачного подключения</span><span class="sxs-lookup"><span data-stu-id="4d7a6-111">Scenario A: Deploy to cloud connect devices</span></span>

<span data-ttu-id="4d7a6-112">HoloLens 2 развертывается для использования в основном в средах, внешних для корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-112">HoloLens 2 is deployed for use primarily in environments external to a corporate network.</span></span> <span data-ttu-id="4d7a6-113">Корпоративные ресурсы не доступны или могут быть ограничены через VPN.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-113">Corporate resources aren't accessed or may be limited through VPN.</span></span> <span data-ttu-id="4d7a6-114">Это развертывание аналогично управляемым мобильным устройствам в компании.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-114">This  deployment is similar to managed mobile devices within a company.</span></span>
 * <span data-ttu-id="4d7a6-115">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="4d7a6-115">Basic Common Configurations</span></span>
   * <span data-ttu-id="4d7a6-116">Wi-Fi сети обычно полностью открыты для интернет-служб и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-116">Wi-Fi networks are typically fully open to the Internet and Cloud services.</span></span>
   * <span data-ttu-id="4d7a6-117">Azure AD присоединяется к автоматической регистрации для управления мобильными устройствами (MDM) — управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="4d7a6-117">Azure AD Join with Mobile Device Management (MDM) Auto Enrollment--MDM (Intune) Managed</span></span>
   * <span data-ttu-id="4d7a6-118">Пользователи во входе с собственной корпоративной учетной записью (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="4d7a6-118">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="4d7a6-119">Отдельные или несколько пользователей на одно устройство, поддерживаемые</span><span class="sxs-lookup"><span data-stu-id="4d7a6-119">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="4d7a6-120">Различные уровни конфигураций блокировки устройств применяются в зависимости от конкретных случаев использования, от полностью открытого до единого киоска приложений.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-120">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="4d7a6-121">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="4d7a6-121">One or more applications are deployed via MDM</span></span>

* <span data-ttu-id="4d7a6-122">Общие проблемы</span><span class="sxs-lookup"><span data-stu-id="4d7a6-122">Common Challenges</span></span>
   * <span data-ttu-id="4d7a6-123">Определение конфигураций MDM для применения к HoloLens 2 в зависимости от требований к сценарию.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-123">Determining which MDM configurations to apply to the HoloLens 2 based on scenario requirements.</span></span>

<span data-ttu-id="4d7a6-124">Для руководства по развертыванию, аналогичного сценарию A review our guide for [Cloud connected HoloLens 2 with Remote Assist.](hololens2-cloud-connected-overview.md)</span><span class="sxs-lookup"><span data-stu-id="4d7a6-124">For a deployment guide that is similar to scenario A review our guide for [Cloud connected HoloLens 2 with Remote Assist](hololens2-cloud-connected-overview.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4d7a6-125">Руководство по развертыванию — облачное подключение HoloLens 2 с удаленной помощью</span><span class="sxs-lookup"><span data-stu-id="4d7a6-125">Deployment Guide – Cloud connected HoloLens 2 with Remote Assist</span></span>](hololens2-cloud-connected-overview.md)

### <a name="scenario-b-deploy-inside-your-organizations-network"></a><span data-ttu-id="4d7a6-126">Сценарий B. Развертывание в сети организации</span><span class="sxs-lookup"><span data-stu-id="4d7a6-126">Scenario B: Deploy inside your organization's network</span></span>

<span data-ttu-id="4d7a6-127">HoloLens 2 развертывается для использования в основном в корпоративной сети с доступом к внутренним корпоративным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-127">HoloLens 2 is deployed for use primarily on the corporate network with access to internal corporate resources.</span></span> <span data-ttu-id="4d7a6-128">Интернет и облачные службы могут быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-128">Internet and cloud services may be limited.</span></span> <span data-ttu-id="4d7a6-129">Это развертывание является типичным развертыванием для большинства компьютеров с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-129">This deployment is a typical deployment for most Windows 10 PCs.</span></span>

 * <span data-ttu-id="4d7a6-130">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="4d7a6-130">Basic Common Configurations</span></span>
   * <span data-ttu-id="4d7a6-131">Wi-Fi является внутренней корпоративной сетью с доступом к внутренним ресурсам и ограниченным доступом к интернету или облачным службам.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-131">Wi-Fi network is an internal corporate network with access to internal resources, and limited access to the internet or Cloud services.</span></span>
   * <span data-ttu-id="4d7a6-132">Azure AD Присоединитесь к автозачислению MDM</span><span class="sxs-lookup"><span data-stu-id="4d7a6-132">Azure AD Join with MDM Auto Enrollment</span></span>
   * <span data-ttu-id="4d7a6-133">Управляемый MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="4d7a6-133">MDM (Intune) Managed</span></span>
   * <span data-ttu-id="4d7a6-134">Пользователи во входе с собственной корпоративной учетной записью (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="4d7a6-134">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="4d7a6-135">Отдельные или несколько пользователей на одно устройство, поддерживаемые</span><span class="sxs-lookup"><span data-stu-id="4d7a6-135">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="4d7a6-136">Различные уровни конфигураций блокировки устройств применяются в зависимости от конкретных случаев использования, от полностью открытого до единого киоска приложений.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-136">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="4d7a6-137">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="4d7a6-137">One or more applications are deployed via MDM</span></span>

 * <span data-ttu-id="4d7a6-138">Общие проблемы</span><span class="sxs-lookup"><span data-stu-id="4d7a6-138">Common Challenges</span></span>
   * <span data-ttu-id="4d7a6-139">HoloLens 2 не поддерживает в помещениях AD join или SCCM.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-139">HoloLens 2 doesn't support on premises AD join or SCCM.</span></span> <span data-ttu-id="4d7a6-140">Только Azure AD присоединяется к MDM.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-140">Only Azure AD join with MDM.</span></span> <span data-ttu-id="4d7a6-141">Многие компании сегодня по-прежнему развертывают компьютеры Windows 10 в этом сценарии, как на устройствах, которые присоединились к AD, управляемые System Center Configuration Manager (SCCM) и не могут иметь инфраструктуру, развернутую или настроенную для управления внутренними устройствами Windows 10 с помощью облачных решений MDM.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-141">Many companies today still deploy Windows 10 PCs in this scenario as on premises AD joined devices, managed by System Center Configuration Manager (SCCM) and may not have the infrastructure deployed/configured for managing internal Windows 10 devices via cloud-based MDM solutions.</span></span>
   * <span data-ttu-id="4d7a6-142">Поскольку HoloLens 2 — это первое облачное устройство, оно в значительной степени зависит от подключенных к Интернету и облачных служб для проверки подлинности пользователей, обновлений ОС, управления MDM и так далее.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-142">As HoloLens 2 is a cloud first device, it relies heavily on internet and cloud connected services for User authentication, OS updates, MDM management, and so on.</span></span> <span data-ttu-id="4d7a6-143">При подключении к корпоративной сети правила прокси/брандмауэра, скорее всего, потребуется скорректировать, чтобы включить доступ к HoloLens 2 и приложениям, которые работают на ней.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-143">When connecting to a corporate network, Proxy/Firewall rules will most likely need to be adjusted to enable access for HoloLens 2 and the applications that run on it.</span></span>
   * <span data-ttu-id="4d7a6-144">Для Wi-Fi подключения обычно требуются сертификаты для проверки подлинности устройства или пользователя в сети.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-144">Corporate Wi-Fi connectivity typically requires certificates to authenticate the device or user to the network.</span></span> <span data-ttu-id="4d7a6-145">Настройка необходимой инфраструктуры или параметров для развертывания сертификатов на устройствах с Windows 10 с помощью MDM может быть сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-145">The required infrastructure or settings to deploy certificates to Windows 10 devices through MDM can be challenging to configure.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4d7a6-146">Руководство по развертыванию — корпоративная связь HoloLens 2 с руководствами dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4d7a6-146">Deployment Guide – Corporate connected HoloLens 2 with Dynamics 365 Guides</span></span>](hololens2-corp-connected-overview.md)

### <a name="scenario-c-deploy-in-secure-offline-environment"></a><span data-ttu-id="4d7a6-147">Сценарий C. Развертывание в безопасной автономной среде</span><span class="sxs-lookup"><span data-stu-id="4d7a6-147">Scenario C: Deploy in secure offline environment</span></span>

<span data-ttu-id="4d7a6-148">HoloLens 2 развертывается для использования в основном в автономном режиме без доступа к сети или Интернету.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-148">HoloLens 2 is deployed for use primarily offline with no network or internet access.</span></span> <span data-ttu-id="4d7a6-149">Это типичное развертывание для высокобезопасных или конфиденциальных местоположений.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-149">This is a typical deployment for highly secure or confidential locations.</span></span>
 * <span data-ttu-id="4d7a6-150">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="4d7a6-150">Basic Common Configurations</span></span>
   * <span data-ttu-id="4d7a6-151">Wi-Fi подключение отключено.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-151">Wi-Fi connectivity is disabled.</span></span> <span data-ttu-id="4d7a6-152">Ethernet через USB может быть включен для подключения к СЕТИ, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-152">Ethernet via USB may be enabled for LAN connectivity if necessary.</span></span>
   * <span data-ttu-id="4d7a6-153">Не управляемый.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-153">Not Managed.</span></span>
   * <span data-ttu-id="4d7a6-154">Учетная запись локального пользователя для регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-154">Local user account for device sign-in.</span></span>
     * <span data-ttu-id="4d7a6-155">HoloLens 2 поддерживает только одну локализованную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-155">HoloLens 2 supports only one local account.</span></span>
   * <span data-ttu-id="4d7a6-156">Различные уровни конфигураций блокировки устройств применяются с помощью пакетов предварительного обеспечения на основе конкретных случаев использования.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-156">Varying levels of device lockdown configurations are applied via Provisioning Packages based on specific use cases.</span></span> <span data-ttu-id="4d7a6-157">Эти конфигурации обычно ограничены из-за требований к безопасной среде.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-157">These configurations are typically restricted because of secure environment requirements.</span></span>
   * <span data-ttu-id="4d7a6-158">Одно или несколько приложений развертываются с помощью пакета подготовка</span><span class="sxs-lookup"><span data-stu-id="4d7a6-158">One or more applications are deployed via Provisioning Package</span></span>

 * <span data-ttu-id="4d7a6-159">Общие проблемы</span><span class="sxs-lookup"><span data-stu-id="4d7a6-159">Common Challenges</span></span>
   * <span data-ttu-id="4d7a6-160">Существует ограниченный набор конфигураций, доступных через пакеты подготовка</span><span class="sxs-lookup"><span data-stu-id="4d7a6-160">There's a limited set of configurations available through Provisioning Packages</span></span>
   * <span data-ttu-id="4d7a6-161">Облачные службы не могут использоваться, что ограничивает возможности HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-161">Cloud services aren't able to be used, therefore limiting the HoloLens 2 capabilities.</span></span>
   * <span data-ttu-id="4d7a6-162">Более высокие административные накладные расходы, так как эти устройства должны настраиваться, настраиваться и обновляться вручную.</span><span class="sxs-lookup"><span data-stu-id="4d7a6-162">Higher administrative overhead since these devices have to be set up, configured, and updated manually.</span></span>

<span data-ttu-id="4d7a6-163">Для руководства по развертыванию, аналогичного этому сценарию, просмотрите наше руководство по безопасному развертыванию в [автономном режиме.](hololens-common-scenarios-offline-secure.md)</span><span class="sxs-lookup"><span data-stu-id="4d7a6-163">For a deployment guide that is similar to this scenario review our [Offline Secure Deployment Guide](hololens-common-scenarios-offline-secure.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4d7a6-164">Руководство по развертыванию — автономный безопасный holoLens 2</span><span class="sxs-lookup"><span data-stu-id="4d7a6-164">Deployment Guide – Offline Secure HoloLens 2</span></span>](hololens-common-scenarios-offline-secure.md)
