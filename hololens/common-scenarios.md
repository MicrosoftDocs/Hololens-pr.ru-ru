---
title: Распространенные сценарии развертывания инфраструктуры
description: Узнайте о некоторых наиболее распространенных сценариях развертывания, основанных на различных развертываниях инфраструктуры для смешанной реальности.
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
ms.openlocfilehash: 6f398327ba82e15a15da21c2b3f90222178d257a
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283630"
---
# <span data-ttu-id="0fc49-104">Общие сценарии развертывания инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="0fc49-104">Common Infrastructure Deployment Scenarios Overview</span></span>

<span data-ttu-id="0fc49-105">Ниже представлен общий обзор архитектуры для трех распространенных сценариев развертывания устройств Microsoft HoloLens 2 на предприятии и управления им.</span><span class="sxs-lookup"><span data-stu-id="0fc49-105">This following information provides a high-level architecture overview for three common scenarios when deploying and managing Microsoft HoloLens 2 devices within the enterprise.</span></span> <span data-ttu-id="0fc49-106">Зачастую управление устройствами и доступ к ресурсам организации во многом зависит от уже имеющихся факторов.</span><span class="sxs-lookup"><span data-stu-id="0fc49-106">Often how you manage your devices and how to access your organization's resources is largely determined by factors already in place.</span></span> <span data-ttu-id="0fc49-107">В зависимости от существующей инфраструктуры мы предлагаем вам просмотреть общий стиль управления устройствами в следующих сценариях и опробуйте наши руководства по развертыванию в сценарии, который соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="0fc49-107">Based on the existing infrastructure we invite you to review the common device management style in the following scenarios, and try out our guides for deploying in the scenario matching your needs.</span></span>

## <span data-ttu-id="0fc49-108">Сценарии</span><span class="sxs-lookup"><span data-stu-id="0fc49-108">Scenarios</span></span>

<span data-ttu-id="0fc49-109">На схеме ниже представлены три типичных сценария развертывания HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="0fc49-109">The diagram below represents three typical scenarios for HoloLens 2 deployments.</span></span>
![Схема сценариев](images/scenarios.jpg)

### <span data-ttu-id="0fc49-111">Сценарий А. Развертывание на устройствах с облачным подключением</span><span class="sxs-lookup"><span data-stu-id="0fc49-111">Scenario A: Deploy to cloud connect devices</span></span>

<span data-ttu-id="0fc49-112">HoloLens 2 развертывается для использования в основном в средах, внешних по сети предприятия.</span><span class="sxs-lookup"><span data-stu-id="0fc49-112">HoloLens 2 is deployed for use primarily in environments external to a corporate network.</span></span> <span data-ttu-id="0fc49-113">Корпоративные ресурсы не доступны или могут быть ограничены через VPN.</span><span class="sxs-lookup"><span data-stu-id="0fc49-113">Corporate resources aren't accessed or may be limited through VPN.</span></span> <span data-ttu-id="0fc49-114">Это развертывание аналогично управляемым мобильным устройствам в компании.</span><span class="sxs-lookup"><span data-stu-id="0fc49-114">This  deployment is similar to managed mobile devices within a company.</span></span>
 * <span data-ttu-id="0fc49-115">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="0fc49-115">Basic Common Configurations</span></span>
   * <span data-ttu-id="0fc49-116">Wi-Fi сети обычно полностью открыты для Интернета и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="0fc49-116">Wi-Fi networks are typically fully open to the Internet and Cloud services.</span></span>
   * <span data-ttu-id="0fc49-117">Автоматическое регистрация в Azure AD с помощью управления мобильными устройствами (MDM) — управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="0fc49-117">Azure AD Join with Mobile Device Management (MDM) Auto Enrollment--MDM (Intune) Managed</span></span>
   * <span data-ttu-id="0fc49-118">Вход пользователей с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="0fc49-118">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="0fc49-119">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="0fc49-119">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="0fc49-120">Различные уровни конфигураций блокировки устройств применяются в зависимости от конкретных случаев использования— от полного открытия до терминала с одним приложением.</span><span class="sxs-lookup"><span data-stu-id="0fc49-120">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="0fc49-121">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="0fc49-121">One or more applications are deployed via MDM</span></span>

* <span data-ttu-id="0fc49-122">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="0fc49-122">Common Challenges</span></span>
   * <span data-ttu-id="0fc49-123">Определение конфигураций MDM для применения к HoloLens 2 на основе требований сценария.</span><span class="sxs-lookup"><span data-stu-id="0fc49-123">Determining which MDM configurations to apply to the HoloLens 2 based on scenario requirements.</span></span>

<span data-ttu-id="0fc49-124">Руководство по развертыванию, аналогичное сценарию, рассмотрено в нашем руководстве по [облачному подключению HoloLens 2 с удаленной помощью.](hololens2-cloud-connected-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0fc49-124">For a deployment guide that is similar to scenario A review our guide for [Cloud connected HoloLens 2 with Remote Assist](hololens2-cloud-connected-overview.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="0fc49-125">Руководство по развертыванию — HoloLens 2, подключенный к облаку с помощью удаленной помощи</span><span class="sxs-lookup"><span data-stu-id="0fc49-125">Deployment Guide – Cloud connected HoloLens 2 with Remote Assist</span></span>](hololens2-cloud-connected-overview.md)

### <span data-ttu-id="0fc49-126">Сценарий Б. Развертывание в сети организации</span><span class="sxs-lookup"><span data-stu-id="0fc49-126">Scenario B: Deploy inside your organization's network</span></span>

<span data-ttu-id="0fc49-127">HoloLens 2 развертывается для использования в основном в корпоративной сети с доступом к внутренним корпоративным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="0fc49-127">HoloLens 2 is deployed for use primarily on the corporate network with access to internal corporate resources.</span></span> <span data-ttu-id="0fc49-128">Интернет-службы и облачные службы могут быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="0fc49-128">Internet and cloud services may be limited.</span></span> <span data-ttu-id="0fc49-129">Такое развертывание является типичным развертыванием для большинства компьютеров с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0fc49-129">This deployment is a typical deployment for most Windows 10 PCs.</span></span>

 * <span data-ttu-id="0fc49-130">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="0fc49-130">Basic Common Configurations</span></span>
   * <span data-ttu-id="0fc49-131">Wi-Fi это внутренняя корпоративная сеть с доступом к внутренним ресурсам и ограниченным доступом к Интернету или облачным службам.</span><span class="sxs-lookup"><span data-stu-id="0fc49-131">Wi-Fi network is an internal corporate network with access to internal resources, and limited access to the internet or Cloud services.</span></span>
   * <span data-ttu-id="0fc49-132">Регистрация в Azure AD с помощью автоматической регистрации в MDM</span><span class="sxs-lookup"><span data-stu-id="0fc49-132">Azure AD Join with MDM Auto Enrollment</span></span>
   * <span data-ttu-id="0fc49-133">Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="0fc49-133">MDM (Intune) Managed</span></span>
   * <span data-ttu-id="0fc49-134">Вход пользователей с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="0fc49-134">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="0fc49-135">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="0fc49-135">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="0fc49-136">Различные уровни конфигураций блокировки устройств применяются в зависимости от конкретных случаев использования— от полного открытия до терминала с одним приложением.</span><span class="sxs-lookup"><span data-stu-id="0fc49-136">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="0fc49-137">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="0fc49-137">One or more applications are deployed via MDM</span></span>

 * <span data-ttu-id="0fc49-138">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="0fc49-138">Common Challenges</span></span>
   * <span data-ttu-id="0fc49-139">HoloLens 2 не поддерживает локальное присоединиться к AD или SCCM.</span><span class="sxs-lookup"><span data-stu-id="0fc49-139">HoloLens 2 doesn't support on premises AD join or SCCM.</span></span> <span data-ttu-id="0fc49-140">Только Azure AD присоединяется к MDM.</span><span class="sxs-lookup"><span data-stu-id="0fc49-140">Only Azure AD join with MDM.</span></span> <span data-ttu-id="0fc49-141">В настоящее время многие компании по-прежнему развертывают компьютеры с Windows 10 в этом сценарии как устройства с локальной службой AD, которые управляются System Center Configuration Manager (SCCM) и могут не иметь инфраструктуры, развернутой или настроенной для управления внутренними устройствами с Windows 10 с помощью облачных решений MDM.</span><span class="sxs-lookup"><span data-stu-id="0fc49-141">Many companies today still deploy Windows 10 PCs in this scenario as on premises AD joined devices, managed by System Center Configuration Manager (SCCM) and may not have the infrastructure deployed/configured for managing internal Windows 10 devices via cloud-based MDM solutions.</span></span>
   * <span data-ttu-id="0fc49-142">Так как HoloLens 2 — это первое облачное устройство, он активно использует подключенные к Интернету и облачные службы для проверки подлинности пользователей, обновлений ОС, управления MDM и других служб.</span><span class="sxs-lookup"><span data-stu-id="0fc49-142">As HoloLens 2 is a cloud first device, it relies heavily on internet and cloud connected services for User authentication, OS updates, MDM management, and so on.</span></span> <span data-ttu-id="0fc49-143">При подключении к корпоративной сети, скорее всего, потребуется скорректировать правила прокси-сервера или брандмауэра, чтобы включить доступ для HoloLens 2 и приложений, которые на нем работают.</span><span class="sxs-lookup"><span data-stu-id="0fc49-143">When connecting to a corporate network, Proxy/Firewall rules will most likely need to be adjusted to enable access for HoloLens 2 and the applications that run on it.</span></span>
   * <span data-ttu-id="0fc49-144">Для Wi-Fi корпоративного подключения обычно требуются сертификаты для проверки подлинности устройства или пользователя в сети.</span><span class="sxs-lookup"><span data-stu-id="0fc49-144">Corporate Wi-Fi connectivity typically requires certificates to authenticate the device or user to the network.</span></span> <span data-ttu-id="0fc49-145">Требуемая инфраструктура или параметры для развертывания сертификатов на устройствах с Windows 10 с помощью MDM могут быть сложно настроить.</span><span class="sxs-lookup"><span data-stu-id="0fc49-145">The required infrastructure or settings to deploy certificates to Windows 10 devices through MDM can be challenging to configure.</span></span>

### <span data-ttu-id="0fc49-146">Сценарий В. Развертывание в безопасной автономной среде</span><span class="sxs-lookup"><span data-stu-id="0fc49-146">Scenario C: Deploy in secure offline environment</span></span>

<span data-ttu-id="0fc49-147">HoloLens 2 развертывается для использования в основном в автономном режиме без доступа к сети или Интернету.</span><span class="sxs-lookup"><span data-stu-id="0fc49-147">HoloLens 2 is deployed for use primarily offline with no network or internet access.</span></span> <span data-ttu-id="0fc49-148">Это типичное развертывание для строго безопасных или конфиденциальных местоположений.</span><span class="sxs-lookup"><span data-stu-id="0fc49-148">This is a typical deployment for highly secure or confidential locations.</span></span>
 * <span data-ttu-id="0fc49-149">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="0fc49-149">Basic Common Configurations</span></span>
   * <span data-ttu-id="0fc49-150">Wi-Fi подключение отключено.</span><span class="sxs-lookup"><span data-stu-id="0fc49-150">Wi-Fi connectivity is disabled.</span></span> <span data-ttu-id="0fc49-151">Ethernet через USB может быть включен для подключения к локальной сети при необходимости.</span><span class="sxs-lookup"><span data-stu-id="0fc49-151">Ethernet via USB may be enabled for LAN connectivity if necessary.</span></span>
   * <span data-ttu-id="0fc49-152">Не управляется.</span><span class="sxs-lookup"><span data-stu-id="0fc49-152">Not Managed.</span></span>
   * <span data-ttu-id="0fc49-153">Учетная запись локального пользователя для регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="0fc49-153">Local user account for device sign-in.</span></span>
     * <span data-ttu-id="0fc49-154">HoloLens 2 поддерживает только одну локализованную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="0fc49-154">HoloLens 2 supports only one local account.</span></span>
   * <span data-ttu-id="0fc49-155">Различные уровни конфигураций блокировки устройств применяются с помощью пакетов предоставления в зависимости от конкретных случаев использования.</span><span class="sxs-lookup"><span data-stu-id="0fc49-155">Varying levels of device lockdown configurations are applied via Provisioning Packages based on specific use cases.</span></span> <span data-ttu-id="0fc49-156">Эти конфигурации обычно ограничены из-за требований к безопасной среде.</span><span class="sxs-lookup"><span data-stu-id="0fc49-156">These configurations are typically restricted because of secure environment requirements.</span></span>
   * <span data-ttu-id="0fc49-157">Одно или несколько приложений развертываются с помощью пакета предоставления</span><span class="sxs-lookup"><span data-stu-id="0fc49-157">One or more applications are deployed via Provisioning Package</span></span>

 * <span data-ttu-id="0fc49-158">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="0fc49-158">Common Challenges</span></span>
   * <span data-ttu-id="0fc49-159">Существует ограниченный набор конфигураций, доступных через пакеты подготовка</span><span class="sxs-lookup"><span data-stu-id="0fc49-159">There's a limited set of configurations available through Provisioning Packages</span></span>
   * <span data-ttu-id="0fc49-160">Облачные службы не могут использоваться, поэтому ограничивают возможности HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="0fc49-160">Cloud services aren't able to be used, therefore limiting the HoloLens 2 capabilities.</span></span>
   * <span data-ttu-id="0fc49-161">Более высокая административная нагрузка, так как эти устройства необходимо настраивать, настраивать и обновлять вручную.</span><span class="sxs-lookup"><span data-stu-id="0fc49-161">Higher administrative overhead since these devices have to be set up, configured, and updated manually.</span></span>

<span data-ttu-id="0fc49-162">Руководство по развертыванию, аналогичное этому сценарию, можно найти в нашем руководстве [по автономному безопасному развертыванию.](hololens-common-scenarios-offline-secure.md)</span><span class="sxs-lookup"><span data-stu-id="0fc49-162">For a deployment guide that is similar to this scenario review our [Offline Secure Deployment Guide](hololens-common-scenarios-offline-secure.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="0fc49-163">Руководство по развертыванию — автономный безопасный HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="0fc49-163">Deployment Guide – Offline Secure HoloLens 2</span></span>](hololens-common-scenarios-offline-secure.md)
