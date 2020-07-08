---
title: Общие сценарии развертывания инфраструктуры
ms.assetid: 651d0430-bfbc-4685-a4fd-db7c33ce9325
ms.date: 6/30/2020
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
ms.openlocfilehash: f8d69fc988afabad5f4ae1cce9003381ceb8e68c
ms.sourcegitcommit: 29755f5af0086a43c532fb5a9a4ae65c36bc82de
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2020
ms.locfileid: "10857923"
---
# <span data-ttu-id="16114-103">Общие сценарии развертывания инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="16114-103">Common Infrastructure Deployment Scenarios</span></span>
<span data-ttu-id="16114-104">Ниже приведены сведения о высокоуровневой архитектуре для трех распространенных сценариев при развертывании и управлении устройствами Microsoft HoloLens 2 внутри предприятия.</span><span class="sxs-lookup"><span data-stu-id="16114-104">This following information provides a high-level architecture overview for three common scenarios when deploying and managing Microsoft HoloLens 2 devices within the enterprise.</span></span>

## <span data-ttu-id="16114-105">Сценарии</span><span class="sxs-lookup"><span data-stu-id="16114-105">Scenarios</span></span>

<span data-ttu-id="16114-106">На схеме ниже представлены три стандартных сценария для развертываний HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="16114-106">The diagram below represents three typical scenarios for HoloLens 2 deployments.</span></span> 
![сценарий](images/scenarios.jpg)

### <span data-ttu-id="16114-108">Сценарий A</span><span class="sxs-lookup"><span data-stu-id="16114-108">Scenario A</span></span>

<span data-ttu-id="16114-109">HoloLens 2 развернут для использования преимущественно в средах, внешних для корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="16114-109">HoloLens 2 is deployed for use primarily in environments external to a corporate network.</span></span> <span data-ttu-id="16114-110">Корпоративные ресурсы не обращаются к сети и могут быть ограничены через VPN.</span><span class="sxs-lookup"><span data-stu-id="16114-110">Corporate resources are not accessed or may be limited through VPN.</span></span> <span data-ttu-id="16114-111">Это развертывание очень похоже на управляемые мобильные устройства в пределах компании.</span><span class="sxs-lookup"><span data-stu-id="16114-111">This is a deployment very similar to managed mobile devices within a company.</span></span>
 * <span data-ttu-id="16114-112">Основные распространенные конфигурации</span><span class="sxs-lookup"><span data-stu-id="16114-112">Basic Common Configurations</span></span>
   * <span data-ttu-id="16114-113">Сети Wi-Fi обычно полностью открыты для Интернета и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="16114-113">Wi-Fi networks are typically fully open to the Internet and Cloud services.</span></span>
   * <span data-ttu-id="16114-114">Присоединение к Azure AD с автоматическим регистрацией MDM — управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="16114-114">Azure AD Join with MDM Auto Enrollment -- MDM (Intune) Managed</span></span>
   * <span data-ttu-id="16114-115">Вход в систему с помощью своей корпоративной учетной записи (AAD)</span><span class="sxs-lookup"><span data-stu-id="16114-115">Users sign in with their own corporate account (AAD)</span></span> 
     * <span data-ttu-id="16114-116">Поддерживается один или несколько пользователей на устройстве</span><span class="sxs-lookup"><span data-stu-id="16114-116">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="16114-117">Различные уровни аппаратных конфигураций блокировки применяются на основании конкретных вариантов использования, начиная с полного открытия на отдельное приложение.</span><span class="sxs-lookup"><span data-stu-id="16114-117">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="16114-118">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="16114-118">One or more applications are deployed via MDM</span></span>

* <span data-ttu-id="16114-119">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="16114-119">Common Challenges</span></span>
   * <span data-ttu-id="16114-120">Определение конфигураций MDM, применяемых к HoloLens 2 на основе требований сценария.</span><span class="sxs-lookup"><span data-stu-id="16114-120">Determining which MDM configurations to apply to the HoloLens 2 based on scenario requirements.</span></span>

### <span data-ttu-id="16114-121">Сценарий B</span><span class="sxs-lookup"><span data-stu-id="16114-121">Scenario B</span></span>

<span data-ttu-id="16114-122">HoloLens 2 разворачивается для использования преимущественно в корпоративной сети и имеет доступ к внутренним корпоративным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="16114-122">HoloLens 2 is deployed for use primarily on the corporate network with access to internal corporate resources.</span></span> <span data-ttu-id="16114-123">Интернет-и облачные службы могут быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="16114-123">Internet and cloud services may be limited.</span></span> <span data-ttu-id="16114-124">Это типичное развертывание большинства компьютеров с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="16114-124">This is a typical deployment for most Windows 10 PCs.</span></span>
 * <span data-ttu-id="16114-125">Основные распространенные конфигурации</span><span class="sxs-lookup"><span data-stu-id="16114-125">Basic Common Configurations</span></span>
   * <span data-ttu-id="16114-126">Сеть Wi-Fi — это внутренняя корпоративная сеть, исключающая доступ к внутренним ресурсам и ограниченный доступ к Интернету или облачным службам.</span><span class="sxs-lookup"><span data-stu-id="16114-126">Wi-Fi network is an internal corporate network with access to internal resources, and limited access to the internet or Cloud services.</span></span>
   * <span data-ttu-id="16114-127">Присоединение к Azure AD с автоматической регистрацией MDM</span><span class="sxs-lookup"><span data-stu-id="16114-127">Azure AD Join with MDM Auto Enrollment</span></span> 
   * <span data-ttu-id="16114-128">Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="16114-128">MDM (Intune) Managed</span></span>
   * <span data-ttu-id="16114-129">Вход в систему с помощью своей корпоративной учетной записи (AAD)</span><span class="sxs-lookup"><span data-stu-id="16114-129">Users sign in with their own corporate account (AAD)</span></span>
     * <span data-ttu-id="16114-130">Поддерживается один или несколько пользователей на устройстве</span><span class="sxs-lookup"><span data-stu-id="16114-130">Single or multiple users per device supported</span></span>
   * <span data-ttu-id="16114-131">Различные уровни аппаратных конфигураций блокировки применяются на основании конкретных вариантов использования, начиная с полного открытия на отдельное приложение.</span><span class="sxs-lookup"><span data-stu-id="16114-131">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk.</span></span>
   * <span data-ttu-id="16114-132">Одно или несколько приложений развертываются с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="16114-132">One or more applications are deployed via MDM</span></span>

 * <span data-ttu-id="16114-133">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="16114-133">Common Challenges</span></span>
   * <span data-ttu-id="16114-134">HoloLens 2 не поддерживает локальную службу связи или SCCM.</span><span class="sxs-lookup"><span data-stu-id="16114-134">HoloLens 2 does not support on premises AD join or SCCM.</span></span> <span data-ttu-id="16114-135">Только присоединение к Azure AD с MDM.</span><span class="sxs-lookup"><span data-stu-id="16114-135">Only Azure AD join with MDM.</span></span> <span data-ttu-id="16114-136">Многие компании сегодня развертывают ПК с Windows 10 на локальных подключенных к ДОМЕНных устройствах, которые управляются с помощью System Center Configuration Manager (SCCM) и не имеют инфраструктуры, развернутой и настроенной для управления внутренними устройствами с Windows 10 с помощью облачных решений MDM.</span><span class="sxs-lookup"><span data-stu-id="16114-136">Many companies today still deploy Windows 10 PCs in this scenario as on premises AD joined devices, managed by System Center Configuration Manager (SCCM) and may not have the infrastructure deployed/configured for managing internal Windows 10 devices via cloud based MDM solutions.</span></span>
   * <span data-ttu-id="16114-137">Поскольку HoloLens 2 — это облачное первое устройство, оно сильно зависит от Интернет-и облачных служб для проверки подлинности пользователей, обновления ОС, управления MDM и т. д. При подключении к корпоративной сети необходимо настроить правила прокси-сервера и брандмауэра, чтобы разрешить доступ для HoloLens 2 и приложений, которые будут работать на нем.</span><span class="sxs-lookup"><span data-stu-id="16114-137">As HoloLens 2 is a cloud first device, it relies heavily on internet and cloud connected services for User authentication, OS updates, MDM management, etc. When connecting to a corporate network, Proxy/Firewall rules will most likely need to be adjusted to enable access for HoloLens 2 and the applications that run on it.</span></span> 
   * <span data-ttu-id="16114-138">Для Организации подключения к сети Wi-Fi обычно требуются сертификаты для проверки подлинности устройства или пользователя в сеть.</span><span class="sxs-lookup"><span data-stu-id="16114-138">Corporate Wi-Fi connectivity typically requires certificates to authenticate the device or user to the network.</span></span> <span data-ttu-id="16114-139">Настройка необходимой инфраструктуры или параметров для развертывания сертификатов на устройствах с Windows 10 через MDM может быть непростой.</span><span class="sxs-lookup"><span data-stu-id="16114-139">The required infrastructure or settings to deploy certificates to Windows 10 devices through MDM can be challenging to configure.</span></span>

### <span data-ttu-id="16114-140">Сценарий C</span><span class="sxs-lookup"><span data-stu-id="16114-140">Scenario C</span></span>

<span data-ttu-id="16114-141">HoloLens 2 развернут для использования в автономном режиме без доступа к сети или Интернету.</span><span class="sxs-lookup"><span data-stu-id="16114-141">HoloLens 2 is deployed for use primarily offline with no network or internet access.</span></span> <span data-ttu-id="16114-142">Это типичное развертывание для надежных и конфиденциальных расположений.</span><span class="sxs-lookup"><span data-stu-id="16114-142">This is a typical deployment for highly secure or confidential locations.</span></span>
 * <span data-ttu-id="16114-143">Основные распространенные конфигурации</span><span class="sxs-lookup"><span data-stu-id="16114-143">Basic Common Configurations</span></span>
   * <span data-ttu-id="16114-144">Подключение Wi-Fi отключено.</span><span class="sxs-lookup"><span data-stu-id="16114-144">Wi-Fi connectivity is disabled.</span></span> <span data-ttu-id="16114-145">При необходимости для подключения к локальной сети может быть включена поддержка Ethernet через USB.</span><span class="sxs-lookup"><span data-stu-id="16114-145">Ethernet via USB may be enabled for LAN connectivity if required.</span></span>
   * <span data-ttu-id="16114-146">Неуправляемый.</span><span class="sxs-lookup"><span data-stu-id="16114-146">Not Managed.</span></span>
   * <span data-ttu-id="16114-147">Локальная учетная запись пользователя для входа на устройство.</span><span class="sxs-lookup"><span data-stu-id="16114-147">Local user account for device sign in.</span></span>
     * <span data-ttu-id="16114-148">HoloLens 2 поддерживает только 1 локальную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="16114-148">HoloLens 2 supports only 1 local account.</span></span>
   * <span data-ttu-id="16114-149">Различные уровни конфигураций блокировки устройств применяются посредством пакетов подготовки на основе конкретных вариантов использования.</span><span class="sxs-lookup"><span data-stu-id="16114-149">Varying levels of device lockdown configurations are applied via Provisioning Packages based on specific use cases.</span></span> <span data-ttu-id="16114-150">Эти конфигурации обычно очень ограничены в соответствии с требованиями безопасной среды.</span><span class="sxs-lookup"><span data-stu-id="16114-150">These configurations are typically very restricted due to secure environment requirements.</span></span>
   * <span data-ttu-id="16114-151">Одно или несколько приложений развертываются с помощью пакета подготовки</span><span class="sxs-lookup"><span data-stu-id="16114-151">One or more applications are deployed via Provisioning Package</span></span>

 * <span data-ttu-id="16114-152">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="16114-152">Common Challenges</span></span>
   * <span data-ttu-id="16114-153">Существует ограниченный набор конфигураций, которые можно использовать в пакетах подготовки</span><span class="sxs-lookup"><span data-stu-id="16114-153">There are a limited set of configurations available through Provisioning Packages</span></span>
   * <span data-ttu-id="16114-154">Облачные службы не могут использоваться, поэтому ограничения на использование HoloLens 2 не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="16114-154">Cloud services are not able to be leveraged, therefore limiting the HoloLens 2 capabilities.</span></span>
   * <span data-ttu-id="16114-155">Более высокие затраты на администрирование, так как эти устройства должны настраиваться, настраиваться и обновляться вручную.</span><span class="sxs-lookup"><span data-stu-id="16114-155">Higher administrative overhead since these devices have to be setup, configured, and updated manually.</span></span>
