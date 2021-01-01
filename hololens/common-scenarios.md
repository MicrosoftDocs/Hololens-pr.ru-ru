---
title: Распространенные сценарии развертывания инфраструктуры
description: Некоторые распространенные сценарии развертывания на основе различных общих инфраструктур
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
ms.openlocfilehash: a7d847e2d2d335f2e2388535a5cf9d5246bb330b
ms.sourcegitcommit: 96dcd015ad24169295690a8ed13ea1bf480e4b9e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/01/2021
ms.locfileid: "11253076"
---
# <span data-ttu-id="a0a4c-104">Общие сценарии развертывания инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="a0a4c-104">Common Infrastructure Deployment Scenarios Overview</span></span>

<span data-ttu-id="a0a4c-105">Ниже представлен общий обзор архитектуры для трех распространенных сценариев развертывания устройств Microsoft HoloLens 2 на предприятии и управления им.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-105">This following information provides a high-level architecture overview for three common scenarios when deploying and managing Microsoft HoloLens 2 devices within the enterprise.</span></span> <span data-ttu-id="a0a4c-106">Зачастую управление устройствами и доступ к ресурсам организации во многом зависит от уже имеющихся факторов.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-106">Often how you manage your devices and how to access your organization's resources is largely determined by factors already in place.</span></span> <span data-ttu-id="a0a4c-107">В зависимости от существующей инфраструктуры мы предлагаем вам просмотреть общий стиль управления устройствами в следующих сценариях и опробуйте наши руководства по развертыванию в сценарии, который соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-107">Based on the existing infrastructure we invite you to review the common device management style in the following scenarios, and try out our guides for deploying in the scenario matching your needs.</span></span>

## <span data-ttu-id="a0a4c-108">Сценарии</span><span class="sxs-lookup"><span data-stu-id="a0a4c-108">Scenarios</span></span>

<span data-ttu-id="a0a4c-109">На схеме ниже представлены три типичных сценария развертывания HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-109">The diagram below represents three typical scenarios for HoloLens 2 deployments.</span></span>
![Схема сценариев](images/scenarios.jpg)

### <span data-ttu-id="a0a4c-111">Сценарий А. Развертывание на устройствах с облачным подключением</span><span class="sxs-lookup"><span data-stu-id="a0a4c-111">Scenario A: Deploy to cloud connect devices</span></span>

<span data-ttu-id="a0a4c-112">HoloLens 2 развертывается для использования в основном в средах, внешних по сети предприятия.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-112">HoloLens 2 is deployed for use primarily in environments external to a corporate network.</span></span> <span data-ttu-id="a0a4c-113">Корпоративные ресурсы не доступны или могут быть ограничены через VPN.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-113">Corporate resources are not accessed or may be limited through VPN.</span></span> <span data-ttu-id="a0a4c-114">Это развертывание аналогично управляемым мобильным устройствам в компании.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-114">This  deployment is similar to managed mobile devices within a company.</span></span>
 * <span data-ttu-id="a0a4c-115">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="a0a4c-115">Basic Common Configurations</span></span>
   * <span data-ttu-id="a0a4c-116">Wi-Fi сети обычно полностью открыты для Интернета и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-116">Wi-Fi networks are typically fully open to the Internet and Cloud services.</span></span>
   * <span data-ttu-id="a0a4c-117">Регистрация в Azure AD с помощью MDM Auto Enrollment--MDM (Intune) Managed</span><span class="sxs-lookup"><span data-stu-id="a0a4c-117">Azure AD Join with MDM Auto Enrollment--MDM (Intune) Managed</span></span>
   * <span data-ttu-id="a0a4c-118">Вход пользователей с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="a0a4c-118">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="a0a4c-119">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="a0a4c-119">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="a0a4c-120">Различные уровни конфигураций блокировки устройств применяются в зависимости от конкретных случаев использования— от полного открытия до терминала с одним приложением.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-120">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="a0a4c-121">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="a0a4c-121">One or more applications are deployed via MDM</span></span>

* <span data-ttu-id="a0a4c-122">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="a0a4c-122">Common Challenges</span></span>
   * <span data-ttu-id="a0a4c-123">Определение конфигураций MDM для применения к HoloLens 2 на основе требований сценария.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-123">Determining which MDM configurations to apply to the HoloLens 2 based on scenario requirements.</span></span>

<span data-ttu-id="a0a4c-124">Руководство по развертыванию, аналогичное сценарию, рассмотрено в нашем руководстве по [облачному подключению HoloLens 2 с удаленной помощью.](hololens2-cloud-connected-overview.md)</span><span class="sxs-lookup"><span data-stu-id="a0a4c-124">For a deployment guide that is similar to scenario A review our guide for [Cloud connected HoloLens 2 with Remote Assist](hololens2-cloud-connected-overview.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="a0a4c-125">Руководство по развертыванию — HoloLens 2, подключенный к облаку с помощью удаленной помощи</span><span class="sxs-lookup"><span data-stu-id="a0a4c-125">Deployment Guide – Cloud connected HoloLens 2 with Remote Assist</span></span>](hololens2-cloud-connected-overview.md)

### <span data-ttu-id="a0a4c-126">Сценарий Б. Развертывание в сети организации</span><span class="sxs-lookup"><span data-stu-id="a0a4c-126">Scenario B: Deploy inside your organization's network</span></span>

<span data-ttu-id="a0a4c-127">HoloLens 2 развертывается для использования в основном в корпоративной сети с доступом к внутренним корпоративным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-127">HoloLens 2 is deployed for use primarily on the corporate network with access to internal corporate resources.</span></span> <span data-ttu-id="a0a4c-128">Интернет-службы и облачные службы могут быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-128">Internet and cloud services may be limited.</span></span> <span data-ttu-id="a0a4c-129">Такое развертывание является типичным развертыванием для большинства компьютеров с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-129">This deployment is a typical deployment for most Windows 10 PCs.</span></span>

 * <span data-ttu-id="a0a4c-130">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="a0a4c-130">Basic Common Configurations</span></span>
   * <span data-ttu-id="a0a4c-131">Wi-Fi это внутренняя корпоративная сеть с доступом к внутренним ресурсам и ограниченным доступом к Интернету или облачным службам.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-131">Wi-Fi network is an internal corporate network with access to internal resources, and limited access to the internet or Cloud services.</span></span>
   * <span data-ttu-id="a0a4c-132">Регистрация в Azure AD с помощью автоматической регистрации в MDM</span><span class="sxs-lookup"><span data-stu-id="a0a4c-132">Azure AD Join with MDM Auto Enrollment</span></span>
   * <span data-ttu-id="a0a4c-133">Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="a0a4c-133">MDM (Intune) Managed</span></span>
   * <span data-ttu-id="a0a4c-134">Вход пользователей с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="a0a4c-134">Users sign in with their own corporate account (Azure AD)</span></span>
     * <span data-ttu-id="a0a4c-135">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="a0a4c-135">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="a0a4c-136">Различные уровни конфигураций блокировки устройств применяются в зависимости от конкретных случаев использования— от полного открытия до терминала с одним приложением.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-136">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="a0a4c-137">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="a0a4c-137">One or more applications are deployed via MDM</span></span>

 * <span data-ttu-id="a0a4c-138">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="a0a4c-138">Common Challenges</span></span>
   * <span data-ttu-id="a0a4c-139">HoloLens 2 не поддерживает локальное присоединиться к AD или SCCM.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-139">HoloLens 2 does not support on premises AD join or SCCM.</span></span> <span data-ttu-id="a0a4c-140">Только Azure AD присоединяется к MDM.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-140">Only Azure AD join with MDM.</span></span> <span data-ttu-id="a0a4c-141">В настоящее время многие компании по-прежнему развертывают компьютеры с Windows 10 в этом сценарии как устройства с локальной службой AD, которые управляются System Center Configuration Manager (SCCM) и могут не иметь инфраструктуры, развернутой или настроенной для управления внутренними устройствами с Windows 10 с помощью облачных решений MDM.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-141">Many companies today still deploy Windows 10 PCs in this scenario as on premises AD joined devices, managed by System Center Configuration Manager (SCCM) and may not have the infrastructure deployed/configured for managing internal Windows 10 devices via cloud-based MDM solutions.</span></span>
   * <span data-ttu-id="a0a4c-142">Так как HoloLens 2 — это первое облачное устройство, он активно использует подключенные к Интернету и облачные службы для проверки подлинности пользователей, обновлений ОС, управления MDM и т. д. При подключении к корпоративной сети, скорее всего, потребуется скорректировать правила прокси-сервера или брандмауэра, чтобы включить доступ для HoloLens 2 и приложений, которые на нем работают.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-142">As HoloLens 2 is a cloud first device, it relies heavily on internet and cloud connected services for User authentication, OS updates, MDM management, etc. When connecting to a corporate network, Proxy/Firewall rules will most likely need to be adjusted to enable access for HoloLens 2 and the applications that run on it.</span></span>
   * <span data-ttu-id="a0a4c-143">Для Wi-Fi корпоративного подключения обычно требуются сертификаты для проверки подлинности устройства или пользователя в сети.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-143">Corporate Wi-Fi connectivity typically requires certificates to authenticate the device or user to the network.</span></span> <span data-ttu-id="a0a4c-144">Требуемая инфраструктура или параметры для развертывания сертификатов на устройствах с Windows 10 с помощью MDM могут быть сложно настроить.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-144">The required infrastructure or settings to deploy certificates to Windows 10 devices through MDM can be challenging to configure.</span></span>

### <span data-ttu-id="a0a4c-145">Сценарий В. Развертывание в безопасной автономной среде</span><span class="sxs-lookup"><span data-stu-id="a0a4c-145">Scenario C: Deploy in secure offline environment</span></span>

<span data-ttu-id="a0a4c-146">HoloLens 2 развертывается для использования в основном в автономном режиме без доступа к сети или Интернету.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-146">HoloLens 2 is deployed for use primarily offline with no network or internet access.</span></span> <span data-ttu-id="a0a4c-147">Это типичное развертывание для строго безопасных или конфиденциальных местоположений.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-147">This is a typical deployment for highly secure or confidential locations.</span></span>
 * <span data-ttu-id="a0a4c-148">Основные общие конфигурации</span><span class="sxs-lookup"><span data-stu-id="a0a4c-148">Basic Common Configurations</span></span>
   * <span data-ttu-id="a0a4c-149">Wi-Fi подключение отключено.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-149">Wi-Fi connectivity is disabled.</span></span> <span data-ttu-id="a0a4c-150">Ethernet через USB может быть включен для подключения к локальной сети при необходимости.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-150">Ethernet via USB may be enabled for LAN connectivity if necessary.</span></span>
   * <span data-ttu-id="a0a4c-151">Не управляется.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-151">Not Managed.</span></span>
   * <span data-ttu-id="a0a4c-152">Учетная запись локального пользователя для регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-152">Local user account for device sign in.</span></span>
     * <span data-ttu-id="a0a4c-153">HoloLens 2 поддерживает только одну локализованную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-153">HoloLens 2 supports only one local account.</span></span>
   * <span data-ttu-id="a0a4c-154">Различные уровни конфигураций блокировки устройств применяются с помощью пакетов предоставления в зависимости от конкретных случаев использования.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-154">Varying levels of device lockdown configurations are applied via Provisioning Packages based on specific use cases.</span></span> <span data-ttu-id="a0a4c-155">Эти конфигурации обычно очень ограничены из-за требований к безопасной среде.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-155">These configurations are typically very restricted due to secure environment requirements.</span></span>
   * <span data-ttu-id="a0a4c-156">Одно или несколько приложений развертываются с помощью пакета предоставления</span><span class="sxs-lookup"><span data-stu-id="a0a4c-156">One or more applications are deployed via Provisioning Package</span></span>

 * <span data-ttu-id="a0a4c-157">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="a0a4c-157">Common Challenges</span></span>
   * <span data-ttu-id="a0a4c-158">Существует ограниченный набор конфигураций, доступных через пакеты подготовка</span><span class="sxs-lookup"><span data-stu-id="a0a4c-158">There is a limited set of configurations available through Provisioning Packages</span></span>
   * <span data-ttu-id="a0a4c-159">Облачные службы не могут быть задействолены, поэтому ограничивают возможности HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-159">Cloud services are not able to be leveraged, therefore limiting the HoloLens 2 capabilities.</span></span>
   * <span data-ttu-id="a0a4c-160">Более высокие административные издержки, так как эти устройства необходимо настраивать, настраивать и обновлять вручную.</span><span class="sxs-lookup"><span data-stu-id="a0a4c-160">Higher administrative overhead since these devices have to be setup, configured, and updated manually.</span></span>

<span data-ttu-id="a0a4c-161">Руководство по развертыванию, аналогичное этому сценарию, можно найти в нашем руководстве [по автономному безопасному развертыванию.](hololens-common-scenarios-offline-secure.md)</span><span class="sxs-lookup"><span data-stu-id="a0a4c-161">For a deployment guide that is similar to this scenario review our [Offline Secure Deployment Guide](hololens-common-scenarios-offline-secure.md).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="a0a4c-162">Руководство по развертыванию — автономный безопасный HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="a0a4c-162">Deployment Guide – Offline Secure HoloLens 2</span></span>](hololens-common-scenarios-offline-secure.md)
