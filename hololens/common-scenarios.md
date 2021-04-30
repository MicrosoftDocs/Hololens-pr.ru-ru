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
ms.openlocfilehash: 4b9bd4335e45180276d69af2ce5f33a38ecb800f
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309479"
---
# <a name="common-infrastructure-deployment-scenarios-overview"></a><span data-ttu-id="ec834-104">Общие сведения о сценариях развертывания общих инфраструктур</span><span class="sxs-lookup"><span data-stu-id="ec834-104">Common Infrastructure Deployment Scenarios Overview</span></span>

<span data-ttu-id="ec834-105">Ниже приведены общие сведения о высокоуровневой архитектуре для трех распространенных сценариев при развертывании устройств Microsoft HoloLens 2 и управлении ими на предприятии.</span><span class="sxs-lookup"><span data-stu-id="ec834-105">This following information provides a high-level architecture overview for three common scenarios when deploying and managing Microsoft HoloLens 2 devices within the enterprise.</span></span> <span data-ttu-id="ec834-106">Часто управление устройствами и доступ к ресурсам Организации в основном определяется факторами, уже имеющимися на месте.</span><span class="sxs-lookup"><span data-stu-id="ec834-106">Often how you manage your devices and how to access your organization's resources is largely determined by factors already in place.</span></span> <span data-ttu-id="ec834-107">На основе существующей инфраструктуры мы приглашаем вас ознакомиться с общим стилем управления устройствами в следующих сценариях и испытать руководства по развертыванию в сценарии, соответствующем вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="ec834-107">Based on the existing infrastructure we invite you to review the common device management style in the following scenarios, and try out our guides for deploying in the scenario matching your needs.</span></span>

## <a name="scenarios"></a><span data-ttu-id="ec834-108">Сценарии</span><span class="sxs-lookup"><span data-stu-id="ec834-108">Scenarios</span></span>

<span data-ttu-id="ec834-109">На схеме ниже представлены три типичные ситуации для развертываний HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="ec834-109">The diagram below represents three typical scenarios for HoloLens 2 deployments.</span></span>
<span data-ttu-id="ec834-110">![Схема сценариев](images/scenarios.jpg)</span><span class="sxs-lookup"><span data-stu-id="ec834-110">![Scenarios diagram](images/scenarios.jpg)</span></span>

### <a name="scenario-a-deploy-to-cloud-connect-devices"></a><span data-ttu-id="ec834-111">Сценарий а. развертывание на устройствах Cloud Connect</span><span class="sxs-lookup"><span data-stu-id="ec834-111">Scenario A: Deploy to cloud connect devices</span></span>

<span data-ttu-id="ec834-112">HoloLens 2 развернут для использования в основном в средах, которые являются внешними по отношению к корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="ec834-112">HoloLens 2 is deployed for use primarily in environments external to a corporate network.</span></span> <span data-ttu-id="ec834-113">Корпоративные ресурсы недоступны или могут быть ограничены через VPN.</span><span class="sxs-lookup"><span data-stu-id="ec834-113">Corporate resources aren't accessed or may be limited through VPN.</span></span> <span data-ttu-id="ec834-114">Это развертывание аналогично управлению мобильными устройствами в компании.</span><span class="sxs-lookup"><span data-stu-id="ec834-114">This  deployment is similar to managed mobile devices within a company.</span></span>
 * <span data-ttu-id="ec834-115">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="ec834-115">Basic Common Configurations</span></span>
   * <span data-ttu-id="ec834-116">Обычно Wi-Fi сети полностью открыты для Интернета и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="ec834-116">Wi-Fi networks are typically fully open to the Internet and Cloud services.</span></span>
   * <span data-ttu-id="ec834-117">Присоединение к Azure AD с автоматической регистрацией управления мобильными устройствами (MDM) — Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="ec834-117">Azure AD Join with Mobile Device Management (MDM) Auto Enrollment--MDM (Intune) Managed</span></span>
   * <span data-ttu-id="ec834-118">Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="ec834-118">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="ec834-119">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="ec834-119">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="ec834-120">Различные уровни конфигурации блокировки устройств применяются на основе конкретных вариантов использования, от полного открытия до киоска одного приложения.</span><span class="sxs-lookup"><span data-stu-id="ec834-120">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="ec834-121">Одно или несколько приложений развертываются с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="ec834-121">One or more applications are deployed via MDM</span></span>

* <span data-ttu-id="ec834-122">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="ec834-122">Common Challenges</span></span>
   * <span data-ttu-id="ec834-123">Определение конфигураций MDM, применяемых к HoloLens 2 на основе требований сценария.</span><span class="sxs-lookup"><span data-stu-id="ec834-123">Determining which MDM configurations to apply to the HoloLens 2 based on scenario requirements.</span></span>

<span data-ttu-id="ec834-124">Рекомендации по развертыванию, аналогичные рассмотренным в разделе сценарий, см. в нашем руководством по [облачному подключению HoloLens 2 с помощью удаленного помощника](hololens2-cloud-connected-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ec834-124">For a deployment guide that is similar to scenario A review our guide for [Cloud connected HoloLens 2 with Remote Assist](hololens2-cloud-connected-overview.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ec834-125">Руководство по развертыванию: облачное подключение HoloLens 2 с помощью удаленного помощника</span><span class="sxs-lookup"><span data-stu-id="ec834-125">Deployment Guide – Cloud connected HoloLens 2 with Remote Assist</span></span>](hololens2-cloud-connected-overview.md)

### <a name="scenario-b-deploy-inside-your-organizations-network"></a><span data-ttu-id="ec834-126">Сценарий б. Развертывание в сети Организации</span><span class="sxs-lookup"><span data-stu-id="ec834-126">Scenario B: Deploy inside your organization's network</span></span>

<span data-ttu-id="ec834-127">HoloLens 2 развертывается для использования в основном в корпоративной сети с доступом к внутренним корпоративным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="ec834-127">HoloLens 2 is deployed for use primarily on the corporate network with access to internal corporate resources.</span></span> <span data-ttu-id="ec834-128">Интернет и облачные службы могут быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="ec834-128">Internet and cloud services may be limited.</span></span> <span data-ttu-id="ec834-129">Это обычное развертывание большинства компьютеров с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ec834-129">This deployment is a typical deployment for most Windows 10 PCs.</span></span>

 * <span data-ttu-id="ec834-130">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="ec834-130">Basic Common Configurations</span></span>
   * <span data-ttu-id="ec834-131">Wi-Fi сеть — это внутренняя корпоративная сеть с доступом к внутренним ресурсам и ограниченный доступ к Интернету или облачным службам.</span><span class="sxs-lookup"><span data-stu-id="ec834-131">Wi-Fi network is an internal corporate network with access to internal resources, and limited access to the internet or Cloud services.</span></span>
   * <span data-ttu-id="ec834-132">Присоединение к Azure AD с автоматической регистрацией MDM</span><span class="sxs-lookup"><span data-stu-id="ec834-132">Azure AD Join with MDM Auto Enrollment</span></span>
   * <span data-ttu-id="ec834-133">Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="ec834-133">MDM (Intune) Managed</span></span>
   * <span data-ttu-id="ec834-134">Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="ec834-134">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="ec834-135">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="ec834-135">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="ec834-136">Различные уровни конфигурации блокировки устройств применяются на основе конкретных вариантов использования, от полного открытия до киоска одного приложения.</span><span class="sxs-lookup"><span data-stu-id="ec834-136">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="ec834-137">Одно или несколько приложений развертываются с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="ec834-137">One or more applications are deployed via MDM</span></span>

 * <span data-ttu-id="ec834-138">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="ec834-138">Common Challenges</span></span>
   * <span data-ttu-id="ec834-139">HoloLens 2 не поддерживает локальное соединение AD или SCCM.</span><span class="sxs-lookup"><span data-stu-id="ec834-139">HoloLens 2 doesn't support on premises AD join or SCCM.</span></span> <span data-ttu-id="ec834-140">Только присоединение к Azure AD с MDM.</span><span class="sxs-lookup"><span data-stu-id="ec834-140">Only Azure AD join with MDM.</span></span> <span data-ttu-id="ec834-141">На сегодняшний день многие компании по-прежнему развертывают компьютеры с Windows 10 в этом сценарии, как на локальных подключенных к AD устройствах, управляемых с помощью System Center Configuration Manager (SCCM) и не имеющие инфраструктуры, развернутой или настроенной для управления внутренними устройствами Windows 10 с помощью облачных решений MDM.</span><span class="sxs-lookup"><span data-stu-id="ec834-141">Many companies today still deploy Windows 10 PCs in this scenario as on premises AD joined devices, managed by System Center Configuration Manager (SCCM) and may not have the infrastructure deployed/configured for managing internal Windows 10 devices via cloud-based MDM solutions.</span></span>
   * <span data-ttu-id="ec834-142">Так как HoloLens 2 является облачным первым устройством, оно сильно зависит от служб, подключенных к Интернету и облаку, для проверки подлинности пользователей, обновления ОС, управления MDM и т. д.</span><span class="sxs-lookup"><span data-stu-id="ec834-142">As HoloLens 2 is a cloud first device, it relies heavily on internet and cloud connected services for User authentication, OS updates, MDM management, and so on.</span></span> <span data-ttu-id="ec834-143">При подключении к корпоративной сети, скорее всего, потребуется изменить правила прокси-сервера и брандмауэра, чтобы обеспечить доступ к HoloLens 2 и приложениям, которые выполняются на нем.</span><span class="sxs-lookup"><span data-stu-id="ec834-143">When connecting to a corporate network, Proxy/Firewall rules will most likely need to be adjusted to enable access for HoloLens 2 and the applications that run on it.</span></span>
   * <span data-ttu-id="ec834-144">Для подключения к корпоративной Wi-Fi обычно требуются сертификаты для проверки подлинности устройства или пользователя в сети.</span><span class="sxs-lookup"><span data-stu-id="ec834-144">Corporate Wi-Fi connectivity typically requires certificates to authenticate the device or user to the network.</span></span> <span data-ttu-id="ec834-145">Настройка требуемой инфраструктуры или параметров для развертывания сертификатов на устройствах с Windows 10 через MDM может оказаться сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="ec834-145">The required infrastructure or settings to deploy certificates to Windows 10 devices through MDM can be challenging to configure.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ec834-146">Руководство по развертыванию — корпоративное подключение HoloLens 2 к руководствам по Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ec834-146">Deployment Guide – Corporate connected HoloLens 2 with Dynamics 365 Guides</span></span>](hololens2-corp-connected-overview.md)

### <a name="scenario-c-deploy-in-secure-offline-environment"></a><span data-ttu-id="ec834-147">Сценарий C. Развертывание в безопасной автономной среде</span><span class="sxs-lookup"><span data-stu-id="ec834-147">Scenario C: Deploy in secure offline environment</span></span>

<span data-ttu-id="ec834-148">HoloLens 2 развертывается для использования в основном автономном режиме без доступа к сети или к Интернету.</span><span class="sxs-lookup"><span data-stu-id="ec834-148">HoloLens 2 is deployed for use primarily offline with no network or internet access.</span></span> <span data-ttu-id="ec834-149">Это типичное развертывание для очень безопасных или конфиденциальных расположений.</span><span class="sxs-lookup"><span data-stu-id="ec834-149">This is a typical deployment for highly secure or confidential locations.</span></span>
 * <span data-ttu-id="ec834-150">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="ec834-150">Basic Common Configurations</span></span>
   * <span data-ttu-id="ec834-151">Wi-Fiное подключение отключено.</span><span class="sxs-lookup"><span data-stu-id="ec834-151">Wi-Fi connectivity is disabled.</span></span> <span data-ttu-id="ec834-152">При необходимости для Ethernet через USB может быть разрешено подключение по локальной сети.</span><span class="sxs-lookup"><span data-stu-id="ec834-152">Ethernet via USB may be enabled for LAN connectivity if necessary.</span></span>
   * <span data-ttu-id="ec834-153">Не управляется.</span><span class="sxs-lookup"><span data-stu-id="ec834-153">Not Managed.</span></span>
   * <span data-ttu-id="ec834-154">Учетная запись локального пользователя для входа устройства.</span><span class="sxs-lookup"><span data-stu-id="ec834-154">Local user account for device sign-in.</span></span>
     * <span data-ttu-id="ec834-155">HoloLens 2 поддерживает только одну локальную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="ec834-155">HoloLens 2 supports only one local account.</span></span>
   * <span data-ttu-id="ec834-156">Различные уровни конфигурации блокировки устройств применяются посредством подготовки пакетов на основе конкретных вариантов использования.</span><span class="sxs-lookup"><span data-stu-id="ec834-156">Varying levels of device lockdown configurations are applied via Provisioning Packages based on specific use cases.</span></span> <span data-ttu-id="ec834-157">Эти конфигурации обычно ограничены из-за требований к безопасной среде.</span><span class="sxs-lookup"><span data-stu-id="ec834-157">These configurations are typically restricted because of secure environment requirements.</span></span>
   * <span data-ttu-id="ec834-158">Одно или несколько приложений развертываются с помощью пакета подготовки.</span><span class="sxs-lookup"><span data-stu-id="ec834-158">One or more applications are deployed via Provisioning Package</span></span>

 * <span data-ttu-id="ec834-159">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="ec834-159">Common Challenges</span></span>
   * <span data-ttu-id="ec834-160">Существует ограниченный набор конфигураций, доступных через подготовку пакетов.</span><span class="sxs-lookup"><span data-stu-id="ec834-160">There's a limited set of configurations available through Provisioning Packages</span></span>
   * <span data-ttu-id="ec834-161">Облачные службы не могут использоваться, поэтому они ограничивают возможности HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="ec834-161">Cloud services aren't able to be used, therefore limiting the HoloLens 2 capabilities.</span></span>
   * <span data-ttu-id="ec834-162">Более высокие административные расходы, так как эти устройства должны настраиваться, настраиваться и обновляться вручную.</span><span class="sxs-lookup"><span data-stu-id="ec834-162">Higher administrative overhead since these devices have to be set up, configured, and updated manually.</span></span>

<span data-ttu-id="ec834-163">Рекомендации по развертыванию, аналогичные приведенным в этом сценарии, рассмотрены в нашем [автономном руководством по развертыванию](hololens-common-scenarios-offline-secure.md).</span><span class="sxs-lookup"><span data-stu-id="ec834-163">For a deployment guide that is similar to this scenario review our [Offline Secure Deployment Guide](hololens-common-scenarios-offline-secure.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ec834-164">Руководство по развертыванию — автономная защита HoloLens</span><span class="sxs-lookup"><span data-stu-id="ec834-164">Deployment Guide – Offline Secure HoloLens 2</span></span>](hololens-common-scenarios-offline-secure.md)
