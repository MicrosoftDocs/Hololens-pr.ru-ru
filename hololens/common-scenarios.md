---
title: Распространенные сценарии развертывания инфраструктуры
description: Узнайте о некоторых наиболее распространенных сценариях развертывания на основе различных развертываний инфраструктуры для смешанной реальности.
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
ms.openlocfilehash: 30a35fb0fe5d5b669249df25ebff0228b552596c
ms.sourcegitcommit: 29573e577381a23891e9557884a6dfdaac0c1c48
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110397429"
---
# <a name="common-infrastructure-deployment-scenarios-overview"></a><span data-ttu-id="34591-104">Общие сведения о сценариях развертывания общих инфраструктур</span><span class="sxs-lookup"><span data-stu-id="34591-104">Common Infrastructure Deployment Scenarios Overview</span></span>

<span data-ttu-id="34591-105">Ниже приведены общие сведения о высокоуровневой архитектуре для трех распространенных сценариев при развертывании устройств Microsoft HoloLens 2 и управлении ими на предприятии.</span><span class="sxs-lookup"><span data-stu-id="34591-105">This following information provides a high-level architecture overview for three common scenarios when deploying and managing Microsoft HoloLens 2 devices within the enterprise.</span></span> <span data-ttu-id="34591-106">Часто управление устройствами и доступ к ресурсам Организации в основном определяется факторами, уже имеющимися на месте.</span><span class="sxs-lookup"><span data-stu-id="34591-106">Often how you manage your devices and how to access your organization's resources is largely determined by factors already in place.</span></span> <span data-ttu-id="34591-107">На основе существующей инфраструктуры мы приглашаем вас ознакомиться с общим стилем управления устройствами в следующих сценариях и испытать руководства по развертыванию в сценарии, соответствующем вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="34591-107">Based on the existing infrastructure we invite you to review the common device management style in the following scenarios, and try out our guides for deploying in the scenario matching your needs.</span></span>

## <a name="scenarios"></a><span data-ttu-id="34591-108">Сценарии</span><span class="sxs-lookup"><span data-stu-id="34591-108">Scenarios</span></span>

<span data-ttu-id="34591-109">На схеме ниже представлены два типичных управляемых сценария для развертываний HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="34591-109">The diagram below represents two typical managed scenarios for HoloLens 2 deployments.</span></span>
 

<span data-ttu-id="34591-110">Существует также третий сценарий, позволяющий выполнять автономные безопасные развертывания.</span><span class="sxs-lookup"><span data-stu-id="34591-110">There is also third scenario that allows for offline secure deployments.</span></span>

### <a name="scenario-a-deploy-to-cloud-connected-devices"></a><span data-ttu-id="34591-111">Сценарий а. развертывание на подключенных к облаку устройствах</span><span class="sxs-lookup"><span data-stu-id="34591-111">Scenario A: Deploy to cloud connected devices</span></span>

<span data-ttu-id="34591-112">HoloLens 2 развернут для использования в основном в средах, которые являются внешними по отношению к корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="34591-112">HoloLens 2 is deployed for use primarily in environments external to a corporate network.</span></span> <span data-ttu-id="34591-113">Корпоративные ресурсы недоступны или могут быть ограничены через VPN.</span><span class="sxs-lookup"><span data-stu-id="34591-113">Corporate resources aren't accessed or may be limited through VPN.</span></span> <span data-ttu-id="34591-114">Это развертывание аналогично управлению мобильными устройствами в компании.</span><span class="sxs-lookup"><span data-stu-id="34591-114">This  deployment is similar to managed mobile devices within a company.</span></span>
 * <span data-ttu-id="34591-115">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="34591-115">Basic Common Configurations</span></span>
   * <span data-ttu-id="34591-116">Обычно Wi-Fi сети полностью открыты для Интернета и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="34591-116">Wi-Fi networks are typically fully open to the Internet and Cloud services.</span></span>
   * <span data-ttu-id="34591-117">Присоединение к Azure AD с автоматической регистрацией управления мобильными устройствами (MDM) — Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="34591-117">Azure AD Join with Mobile Device Management (MDM) Auto Enrollment--MDM (Intune) Managed</span></span>
   * <span data-ttu-id="34591-118">Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="34591-118">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="34591-119">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="34591-119">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="34591-120">Различные уровни конфигурации блокировки устройств применяются на основе конкретных вариантов использования, от полного открытия до киоска одного приложения.</span><span class="sxs-lookup"><span data-stu-id="34591-120">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="34591-121">Одно или несколько приложений развертываются с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="34591-121">One or more applications are deployed via MDM</span></span>



* <span data-ttu-id="34591-122">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="34591-122">Common Challenges</span></span>
   * <span data-ttu-id="34591-123">Определение конфигураций MDM, применяемых к HoloLens 2 на основе требований сценария.</span><span class="sxs-lookup"><span data-stu-id="34591-123">Determining which MDM configurations to apply to the HoloLens 2 based on scenario requirements.</span></span>

<span data-ttu-id="34591-124">[![Сценарий. схема ](images/deployment-guides-revised-scenario-a.png)](images/deployment-guides-revised-scenario-a.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="34591-124">[ ![Scenario A diagram](images/deployment-guides-revised-scenario-a.png) ](images/deployment-guides-revised-scenario-a.png#lightbox)</span></span>

<span data-ttu-id="34591-125">Рекомендации по развертыванию, аналогичные рассмотренным в этом сценарии, см. в нашем разделе [руководств по развертыванию облачной среды](hololens2-cloud-connected-overview.md).</span><span class="sxs-lookup"><span data-stu-id="34591-125">For a deployment guide that is similar to this scenario review our guide for [Cloud connected environment deployment guide](hololens2-cloud-connected-overview.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="34591-126">Рекомендации по развертыванию облачного подключенного окружения</span><span class="sxs-lookup"><span data-stu-id="34591-126">Cloud connected environment deployment guide</span></span>](hololens2-cloud-connected-overview.md)
> [!div class="nextstepaction"]
> [<span data-ttu-id="34591-127">Обзор развертывания среды Cloud Connected (внешние клиенты)</span><span class="sxs-lookup"><span data-stu-id="34591-127">Cloud connected environment (External Clients) deployment guide</span></span>](hololens2-deployment-guide.md)

### <a name="scenario-b-deploy-inside-your-organizations-network"></a><span data-ttu-id="34591-128">Сценарий б. Развертывание в сети Организации</span><span class="sxs-lookup"><span data-stu-id="34591-128">Scenario B: Deploy inside your organization's network</span></span>

<span data-ttu-id="34591-129">HoloLens 2 развертывается для использования в основном в корпоративной сети с доступом к внутренним корпоративным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="34591-129">HoloLens 2 is deployed for use primarily on the corporate network with access to internal corporate resources.</span></span> <span data-ttu-id="34591-130">Интернет и облачные службы могут быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="34591-130">Internet and cloud services may be limited.</span></span> <span data-ttu-id="34591-131">Это обычное развертывание большинства компьютеров с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="34591-131">This deployment is a typical deployment for most Windows 10 PCs.</span></span>

 * <span data-ttu-id="34591-132">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="34591-132">Basic Common Configurations</span></span>
   * <span data-ttu-id="34591-133">Wi-Fi сеть — это внутренняя корпоративная сеть с доступом к внутренним ресурсам и ограниченный доступ к Интернету или облачным службам.</span><span class="sxs-lookup"><span data-stu-id="34591-133">Wi-Fi network is an internal corporate network with access to internal resources, and limited access to the internet or Cloud services.</span></span>
   * <span data-ttu-id="34591-134">Присоединение к Azure AD с автоматической регистрацией MDM</span><span class="sxs-lookup"><span data-stu-id="34591-134">Azure AD Join with MDM Auto Enrollment</span></span>
   * <span data-ttu-id="34591-135">Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="34591-135">MDM (Intune) Managed</span></span>
   * <span data-ttu-id="34591-136">Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="34591-136">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="34591-137">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="34591-137">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="34591-138">Различные уровни конфигурации блокировки устройств применяются на основе конкретных вариантов использования, от полного открытия до киоска одного приложения.</span><span class="sxs-lookup"><span data-stu-id="34591-138">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="34591-139">Одно или несколько приложений развертываются с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="34591-139">One or more applications are deployed via MDM</span></span>

 * <span data-ttu-id="34591-140">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="34591-140">Common Challenges</span></span>
   * <span data-ttu-id="34591-141">HoloLens 2 не поддерживает локальное соединение AD или SCCM.</span><span class="sxs-lookup"><span data-stu-id="34591-141">HoloLens 2 doesn't support on premises AD join or SCCM.</span></span> <span data-ttu-id="34591-142">Только присоединение к Azure AD с MDM.</span><span class="sxs-lookup"><span data-stu-id="34591-142">Only Azure AD join with MDM.</span></span> <span data-ttu-id="34591-143">На сегодняшний день многие компании по-прежнему развертывают компьютеры с Windows 10 в этом сценарии, как на локальных подключенных к AD устройствах, управляемых с помощью System Center Configuration Manager (SCCM) и не имеющие инфраструктуры, развернутой или настроенной для управления внутренними устройствами Windows 10 с помощью облачных решений MDM.</span><span class="sxs-lookup"><span data-stu-id="34591-143">Many companies today still deploy Windows 10 PCs in this scenario as on premises AD joined devices, managed by System Center Configuration Manager (SCCM) and may not have the infrastructure deployed/configured for managing internal Windows 10 devices via cloud-based MDM solutions.</span></span>
   * <span data-ttu-id="34591-144">Так как HoloLens 2 является облачным первым устройством, оно сильно зависит от служб, подключенных к Интернету и облаку, для проверки подлинности пользователей, обновления ОС, управления MDM и т. д.</span><span class="sxs-lookup"><span data-stu-id="34591-144">As HoloLens 2 is a cloud first device, it relies heavily on internet and cloud connected services for User authentication, OS updates, MDM management, and so on.</span></span> <span data-ttu-id="34591-145">При подключении к корпоративной сети, скорее всего, потребуется изменить правила прокси-сервера и брандмауэра, чтобы обеспечить доступ к HoloLens 2 и приложениям, которые выполняются на нем.</span><span class="sxs-lookup"><span data-stu-id="34591-145">When connecting to a corporate network, Proxy/Firewall rules will most likely need to be adjusted to enable access for HoloLens 2 and the applications that run on it.</span></span>
   * <span data-ttu-id="34591-146">Для подключения к корпоративной Wi-Fi обычно требуются сертификаты для проверки подлинности устройства или пользователя в сети.</span><span class="sxs-lookup"><span data-stu-id="34591-146">Corporate Wi-Fi connectivity typically requires certificates to authenticate the device or user to the network.</span></span> <span data-ttu-id="34591-147">Настройка требуемой инфраструктуры или параметров для развертывания сертификатов на устройствах с Windows 10 через MDM может оказаться сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="34591-147">The required infrastructure or settings to deploy certificates to Windows 10 devices through MDM can be challenging to configure.</span></span>

<span data-ttu-id="34591-148">[Схема "B1" ![ ](images/deployment-guides-revised-scenario-b-01-1.png)](images/deployment-guides-revised-scenario-b-01-1.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="34591-148">[ ![Scenario B1 diagram](images/deployment-guides-revised-scenario-b-01-1.png) ](images/deployment-guides-revised-scenario-b-01-1.png#lightbox)</span></span>

<span data-ttu-id="34591-149">[![Схема ](images/deployment-guides-revised-scenario-b-02-1.png) сценария B2](images/deployment-guides-revised-scenario-b-02-1.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="34591-149">[ ![Scenario B2 diagram](images/deployment-guides-revised-scenario-b-02-1.png) ](images/deployment-guides-revised-scenario-b-02-1.png#lightbox)</span></span>

<span data-ttu-id="34591-150">Рекомендации по развертыванию, аналогичные рассмотренным в этом сценарии, см. в нашем руководством по [развертыванию корпоративной сети](hololens2-corp-connected-overview.md).</span><span class="sxs-lookup"><span data-stu-id="34591-150">For a deployment guide that is similar to this scenario review our guide for [Corporate network deployment guide](hololens2-corp-connected-overview.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="34591-151">Рекомендации по развертыванию корпоративной сети</span><span class="sxs-lookup"><span data-stu-id="34591-151">Corporate network deployment guide</span></span>](hololens2-corp-connected-overview.md)

### <a name="scenario-c-deploy-in-secure-offline-environment"></a><span data-ttu-id="34591-152">Сценарий C. Развертывание в безопасной автономной среде</span><span class="sxs-lookup"><span data-stu-id="34591-152">Scenario C: Deploy in secure offline environment</span></span>

<span data-ttu-id="34591-153">HoloLens 2 развертывается для использования в основном автономном режиме без доступа к сети или к Интернету.</span><span class="sxs-lookup"><span data-stu-id="34591-153">HoloLens 2 is deployed for use primarily offline with no network or internet access.</span></span> <span data-ttu-id="34591-154">Это типичное развертывание для очень безопасных или конфиденциальных расположений.</span><span class="sxs-lookup"><span data-stu-id="34591-154">This is a typical deployment for highly secure or confidential locations.</span></span>
 * <span data-ttu-id="34591-155">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="34591-155">Basic Common Configurations</span></span>
   * <span data-ttu-id="34591-156">Wi-Fiное подключение отключено.</span><span class="sxs-lookup"><span data-stu-id="34591-156">Wi-Fi connectivity is disabled.</span></span> <span data-ttu-id="34591-157">При необходимости для Ethernet через USB может быть разрешено подключение по локальной сети.</span><span class="sxs-lookup"><span data-stu-id="34591-157">Ethernet via USB may be enabled for LAN connectivity if necessary.</span></span>
   * <span data-ttu-id="34591-158">Не управляется.</span><span class="sxs-lookup"><span data-stu-id="34591-158">Not Managed.</span></span>
   * <span data-ttu-id="34591-159">Учетная запись локального пользователя для входа устройства.</span><span class="sxs-lookup"><span data-stu-id="34591-159">Local user account for device sign-in.</span></span>
     * <span data-ttu-id="34591-160">HoloLens 2 поддерживает только одну локальную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="34591-160">HoloLens 2 supports only one local account.</span></span>
   * <span data-ttu-id="34591-161">Различные уровни конфигурации блокировки устройств применяются посредством подготовки пакетов на основе конкретных вариантов использования.</span><span class="sxs-lookup"><span data-stu-id="34591-161">Varying levels of device lockdown configurations are applied via Provisioning Packages based on specific use cases.</span></span> <span data-ttu-id="34591-162">Эти конфигурации обычно ограничены из-за требований к безопасной среде.</span><span class="sxs-lookup"><span data-stu-id="34591-162">These configurations are typically restricted because of secure environment requirements.</span></span>
   * <span data-ttu-id="34591-163">Одно или несколько приложений развертываются с помощью пакета подготовки.</span><span class="sxs-lookup"><span data-stu-id="34591-163">One or more applications are deployed via Provisioning Package</span></span>

 * <span data-ttu-id="34591-164">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="34591-164">Common Challenges</span></span>
   * <span data-ttu-id="34591-165">Существует ограниченный набор конфигураций, доступных через подготовку пакетов.</span><span class="sxs-lookup"><span data-stu-id="34591-165">There's a limited set of configurations available through Provisioning Packages</span></span>
   * <span data-ttu-id="34591-166">Облачные службы не могут использоваться, поэтому они ограничивают возможности HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="34591-166">Cloud services aren't able to be used, therefore limiting the HoloLens 2 capabilities.</span></span>
   * <span data-ttu-id="34591-167">Более высокие административные расходы, так как эти устройства должны настраиваться, настраиваться и обновляться вручную.</span><span class="sxs-lookup"><span data-stu-id="34591-167">Higher administrative overhead since these devices have to be set up, configured, and updated manually.</span></span>

<span data-ttu-id="34591-168">[![Автономная защита схемы 1 ](images/deployment-guides-revised-scenario-c-01.png)](images/deployment-guides-revised-scenario-c-01.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="34591-168">[ ![Offline Secure diagram 1](images/deployment-guides-revised-scenario-c-01.png) ](images/deployment-guides-revised-scenario-c-01.png#lightbox)</span></span>

<span data-ttu-id="34591-169">Рекомендации [по развертыванию](hololens-common-scenarios-offline-secure.md), аналогичные этим сценариям, рассмотрены в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="34591-169">For a deployment guide that is similar to this scenario review our [Offline secure environment deployment guide](hololens-common-scenarios-offline-secure.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="34591-170">Рекомендации по развертыванию автономной безопасной среды</span><span class="sxs-lookup"><span data-stu-id="34591-170">Offline secure environment deployment guide</span></span>](hololens-common-scenarios-offline-secure.md)
