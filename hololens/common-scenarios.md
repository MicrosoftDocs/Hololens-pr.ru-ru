---
title: Распространенные сценарии развертывания инфраструктуры
description: Некоторые распространенные сценарии развертывания, основанные на разных распространенных инфраструктурах
ms.assetid: 651d0430-bfbc-4685-a4fd-db7c33ce9325
ms.date: 11/04/2020
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
ms.openlocfilehash: e9e91535bb49b5076547e8b9934bdc86808d41fc
ms.sourcegitcommit: 8e2c268733adce2662bf320cf96ccfea5919425e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2020
ms.locfileid: "11195572"
---
# <span data-ttu-id="8123c-104">Общие сведения о сценариях развертывания инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="8123c-104">Common Infrastructure Deployment Scenarios Overview</span></span>

<span data-ttu-id="8123c-105">Ниже приведены сведения о высокоуровневой архитектуре для трех распространенных сценариев при развертывании и управлении устройствами Microsoft HoloLens 2 внутри предприятия.</span><span class="sxs-lookup"><span data-stu-id="8123c-105">This following information provides a high-level architecture overview for three common scenarios when deploying and managing Microsoft HoloLens 2 devices within the enterprise.</span></span> <span data-ttu-id="8123c-106">Частое Управление устройствами и доступ к ресурсам Организации значительно определяются с учетом факторов, которые уже есть на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="8123c-106">Often how you manage your devices and how access your organization's resources is largely determined by factors already in place.</span></span> <span data-ttu-id="8123c-107">На основе существующей инфраструктуры мы предлагаем вам ознакомиться с общим стилем управления устройствами в указанных ниже сценариях и ознакомиться с нашими руководствами по развертыванию в сценарии, отвечающим вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="8123c-107">Based on the existing infrastructure we invite you to review the common device management style in the following scenarios, and try out our guides for deploying in the scenario matching your needs.</span></span>

## <span data-ttu-id="8123c-108">Сценарии</span><span class="sxs-lookup"><span data-stu-id="8123c-108">Scenarios</span></span>

<span data-ttu-id="8123c-109">На схеме ниже представлены три стандартных сценария для развертываний HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="8123c-109">The diagram below represents three typical scenarios for HoloLens 2 deployments.</span></span>
![Схема сценариев](images/scenarios.jpg)

### <span data-ttu-id="8123c-111">Сценарий а. развертывание на облачные устройства с подключением</span><span class="sxs-lookup"><span data-stu-id="8123c-111">Scenario A: Deploy to cloud connect devices</span></span>

<span data-ttu-id="8123c-112">HoloLens 2 развернут для использования преимущественно в средах, внешних для корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="8123c-112">HoloLens 2 is deployed for use primarily in environments external to a corporate network.</span></span> <span data-ttu-id="8123c-113">Корпоративные ресурсы не обращаются к сети и могут быть ограничены через VPN.</span><span class="sxs-lookup"><span data-stu-id="8123c-113">Corporate resources are not accessed or may be limited through VPN.</span></span> <span data-ttu-id="8123c-114">Это развертывание очень похоже на управляемые мобильные устройства в пределах компании.</span><span class="sxs-lookup"><span data-stu-id="8123c-114">This is a deployment very similar to managed mobile devices within a company.</span></span>
 * <span data-ttu-id="8123c-115">Основные распространенные конфигурации</span><span class="sxs-lookup"><span data-stu-id="8123c-115">Basic Common Configurations</span></span>
   * <span data-ttu-id="8123c-116">Обычно Wi-Fi сети полностью открыты для Интернета и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="8123c-116">Wi-Fi networks are typically fully open to the Internet and Cloud services.</span></span>
   * <span data-ttu-id="8123c-117">Присоединение к Azure AD с автоматическим регистрацией MDM — управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="8123c-117">Azure AD Join with MDM Auto Enrollment -- MDM (Intune) Managed</span></span>
   * <span data-ttu-id="8123c-118">Вход в систему с помощью своей корпоративной учетной записи (AAD)</span><span class="sxs-lookup"><span data-stu-id="8123c-118">Users sign in with their own corporate account (AAD)</span></span>
     * <span data-ttu-id="8123c-119">Поддерживается один или несколько пользователей на устройстве</span><span class="sxs-lookup"><span data-stu-id="8123c-119">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="8123c-120">Различные уровни аппаратных конфигураций блокировки применяются на основании конкретных вариантов использования, начиная с полного открытия на отдельное приложение.</span><span class="sxs-lookup"><span data-stu-id="8123c-120">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="8123c-121">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="8123c-121">One or more applications are deployed via MDM</span></span>

* <span data-ttu-id="8123c-122">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="8123c-122">Common Challenges</span></span>
   * <span data-ttu-id="8123c-123">Определение конфигураций MDM, применяемых к HoloLens 2 на основе требований сценария.</span><span class="sxs-lookup"><span data-stu-id="8123c-123">Determining which MDM configurations to apply to the HoloLens 2 based on scenario requirements.</span></span>

<span data-ttu-id="8123c-124">Руководство по развертыванию похоже на этот сценарий, ознакомьтесь с нашим руководством для [облака, подключенного к HoloLens 2 с помощью удаленного помощника](hololens2-cloud-connected-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8123c-124">For a deployment guide that is similar to this scenario please review our guide for [Cloud connected HoloLens 2 with Remote Assist](hololens2-cloud-connected-overview.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8123c-125">Руководство по развертыванию: Облако подключено к HoloLens 2 с удаленным помощником</span><span class="sxs-lookup"><span data-stu-id="8123c-125">Deployment Guide – Cloud connected HoloLens 2 with Remote Assist</span></span>](hololens2-cloud-connected-overview.md)

### <span data-ttu-id="8123c-126">Сценарий B: развертывание в сети Организации</span><span class="sxs-lookup"><span data-stu-id="8123c-126">Scenario B: Deploy inside your organization's network</span></span>

<span data-ttu-id="8123c-127">HoloLens 2 разворачивается для использования преимущественно в корпоративной сети и имеет доступ к внутренним корпоративным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="8123c-127">HoloLens 2 is deployed for use primarily on the corporate network with access to internal corporate resources.</span></span> <span data-ttu-id="8123c-128">Интернет-и облачные службы могут быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="8123c-128">Internet and cloud services may be limited.</span></span> <span data-ttu-id="8123c-129">Это типичное развертывание большинства компьютеров с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8123c-129">This is a typical deployment for most Windows 10 PCs.</span></span>
 * <span data-ttu-id="8123c-130">Основные распространенные конфигурации</span><span class="sxs-lookup"><span data-stu-id="8123c-130">Basic Common Configurations</span></span>
   * <span data-ttu-id="8123c-131">Wi-Fi сеть — это внутренняя корпоративная сеть, на которой есть доступ к внутренним ресурсам и ограниченный доступ к Интернету или облачным службам.</span><span class="sxs-lookup"><span data-stu-id="8123c-131">Wi-Fi network is an internal corporate network with access to internal resources, and limited access to the internet or Cloud services.</span></span>
   * <span data-ttu-id="8123c-132">Присоединение к Azure AD с автоматической регистрацией MDM</span><span class="sxs-lookup"><span data-stu-id="8123c-132">Azure AD Join with MDM Auto Enrollment</span></span>
   * <span data-ttu-id="8123c-133">Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="8123c-133">MDM (Intune) Managed</span></span>
   * <span data-ttu-id="8123c-134">Вход в систему с помощью своей корпоративной учетной записи (AAD)</span><span class="sxs-lookup"><span data-stu-id="8123c-134">Users sign in with their own corporate account (AAD)</span></span>
     * <span data-ttu-id="8123c-135">Поддерживается один или несколько пользователей на устройстве</span><span class="sxs-lookup"><span data-stu-id="8123c-135">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="8123c-136">Различные уровни аппаратных конфигураций блокировки применяются на основании конкретных вариантов использования, начиная с полного открытия на отдельное приложение.</span><span class="sxs-lookup"><span data-stu-id="8123c-136">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="8123c-137">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="8123c-137">One or more applications are deployed via MDM</span></span>

 * <span data-ttu-id="8123c-138">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="8123c-138">Common Challenges</span></span>
   * <span data-ttu-id="8123c-139">HoloLens 2 не поддерживает локальную службу связи или SCCM.</span><span class="sxs-lookup"><span data-stu-id="8123c-139">HoloLens 2 does not support on premises AD join or SCCM.</span></span> <span data-ttu-id="8123c-140">Только присоединение к Azure AD с MDM.</span><span class="sxs-lookup"><span data-stu-id="8123c-140">Only Azure AD join with MDM.</span></span> <span data-ttu-id="8123c-141">Многие компании сегодня развертывают ПК с Windows 10 на локальных подключенных к ДОМЕНных устройствах, которые управляются с помощью System Center Configuration Manager (SCCM) и не имеют инфраструктуры, развернутой и настроенной для управления внутренними устройствами с Windows 10 с помощью облачных решений MDM.</span><span class="sxs-lookup"><span data-stu-id="8123c-141">Many companies today still deploy Windows 10 PCs in this scenario as on premises AD joined devices, managed by System Center Configuration Manager (SCCM) and may not have the infrastructure deployed/configured for managing internal Windows 10 devices via cloud based MDM solutions.</span></span>
   * <span data-ttu-id="8123c-142">Поскольку HoloLens 2 — это облачное первое устройство, оно сильно зависит от Интернет-и облачных служб для проверки подлинности пользователей, обновления ОС, управления MDM и т. д. При подключении к корпоративной сети необходимо настроить правила прокси-сервера и брандмауэра, чтобы разрешить доступ для HoloLens 2 и приложений, которые будут работать на нем.</span><span class="sxs-lookup"><span data-stu-id="8123c-142">As HoloLens 2 is a cloud first device, it relies heavily on internet and cloud connected services for User authentication, OS updates, MDM management, etc. When connecting to a corporate network, Proxy/Firewall rules will most likely need to be adjusted to enable access for HoloLens 2 and the applications that run on it.</span></span>
   * <span data-ttu-id="8123c-143">Корпоративная Wi-Fi для подключения обычно требуются сертификаты для проверки подлинности устройства или пользователя в сети.</span><span class="sxs-lookup"><span data-stu-id="8123c-143">Corporate Wi-Fi connectivity typically requires certificates to authenticate the device or user to the network.</span></span> <span data-ttu-id="8123c-144">Настройка необходимой инфраструктуры или параметров для развертывания сертификатов на устройствах с Windows 10 через MDM может быть непростой.</span><span class="sxs-lookup"><span data-stu-id="8123c-144">The required infrastructure or settings to deploy certificates to Windows 10 devices through MDM can be challenging to configure.</span></span>

### <span data-ttu-id="8123c-145">Сценарий C: развертывание в безопасной автономной среде</span><span class="sxs-lookup"><span data-stu-id="8123c-145">Scenario C: Deploy in secure offline environment</span></span>

<span data-ttu-id="8123c-146">HoloLens 2 развернут для использования в автономном режиме без доступа к сети или Интернету.</span><span class="sxs-lookup"><span data-stu-id="8123c-146">HoloLens 2 is deployed for use primarily offline with no network or internet access.</span></span> <span data-ttu-id="8123c-147">Это типичное развертывание для надежных и конфиденциальных расположений.</span><span class="sxs-lookup"><span data-stu-id="8123c-147">This is a typical deployment for highly secure or confidential locations.</span></span>
 * <span data-ttu-id="8123c-148">Основные распространенные конфигурации</span><span class="sxs-lookup"><span data-stu-id="8123c-148">Basic Common Configurations</span></span>
   * <span data-ttu-id="8123c-149">Wi-Fi подключение отключено.</span><span class="sxs-lookup"><span data-stu-id="8123c-149">Wi-Fi connectivity is disabled.</span></span> <span data-ttu-id="8123c-150">При необходимости для подключения к локальной сети может быть включена поддержка Ethernet через USB.</span><span class="sxs-lookup"><span data-stu-id="8123c-150">Ethernet via USB may be enabled for LAN connectivity if required.</span></span>
   * <span data-ttu-id="8123c-151">Неуправляемый.</span><span class="sxs-lookup"><span data-stu-id="8123c-151">Not Managed.</span></span>
   * <span data-ttu-id="8123c-152">Локальная учетная запись пользователя для входа на устройство.</span><span class="sxs-lookup"><span data-stu-id="8123c-152">Local user account for device sign in.</span></span>
     * <span data-ttu-id="8123c-153">HoloLens 2 поддерживает только 1 локальную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="8123c-153">HoloLens 2 supports only 1 local account.</span></span>
   * <span data-ttu-id="8123c-154">Различные уровни конфигураций блокировки устройств применяются посредством пакетов подготовки на основе конкретных вариантов использования.</span><span class="sxs-lookup"><span data-stu-id="8123c-154">Varying levels of device lockdown configurations are applied via Provisioning Packages based on specific use cases.</span></span> <span data-ttu-id="8123c-155">Эти конфигурации обычно очень ограничены в соответствии с требованиями безопасной среды.</span><span class="sxs-lookup"><span data-stu-id="8123c-155">These configurations are typically very restricted due to secure environment requirements.</span></span>
   * <span data-ttu-id="8123c-156">Одно или несколько приложений развертываются с помощью пакета подготовки</span><span class="sxs-lookup"><span data-stu-id="8123c-156">One or more applications are deployed via Provisioning Package</span></span>

 * <span data-ttu-id="8123c-157">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="8123c-157">Common Challenges</span></span>
   * <span data-ttu-id="8123c-158">Существует ограниченный набор конфигураций, которые можно использовать в пакетах подготовки</span><span class="sxs-lookup"><span data-stu-id="8123c-158">There are a limited set of configurations available through Provisioning Packages</span></span>
   * <span data-ttu-id="8123c-159">Облачные службы не могут использоваться, поэтому ограничения на использование HoloLens 2 не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8123c-159">Cloud services are not able to be leveraged, therefore limiting the HoloLens 2 capabilities.</span></span>
   * <span data-ttu-id="8123c-160">Более высокие затраты на администрирование, так как эти устройства должны настраиваться, настраиваться и обновляться вручную.</span><span class="sxs-lookup"><span data-stu-id="8123c-160">Higher administrative overhead since these devices have to be setup, configured, and updated manually.</span></span>

<span data-ttu-id="8123c-161">Для руководства по развертыванию, похожего на этот сценарий, ознакомьтесь со [справочным руководством по развертыванию в автономном режиме](hololens-common-scenarios-offline-secure.md).</span><span class="sxs-lookup"><span data-stu-id="8123c-161">For a deployment guide that is similar to this scenario please review our [Offline Secure Deployment Guide](hololens-common-scenarios-offline-secure.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8123c-162">Руководство по развертыванию: автономный безопасный сервер HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="8123c-162">Deployment Guide – Offline Secure HoloLens 2</span></span>](hololens-common-scenarios-offline-secure.md)
