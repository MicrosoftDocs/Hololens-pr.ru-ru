---
title: Обзор настройки CSP и управления устройством
description: Узнайте, как настроить CPS, политику и управление устройствами с помощью управления мобильными устройствами и пакетов подготовка.
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: v-evmill
ms.topic: article
ms.localizationpriority: medium
ms.date: 09/16/2020
ms.reviewer: lavinds
manager: yannisle
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 60e73a9a70a70c5c583edc73a0add2f0f502ef80
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283250"
---
# <span data-ttu-id="36fc1-103">Обзор настройки CSP и управления устройством</span><span class="sxs-lookup"><span data-stu-id="36fc1-103">Configure CSPs and Device Management overview</span></span>

<span data-ttu-id="36fc1-104">ИТ-администраторы могут определять и внедрять параметры политики на HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="36fc1-104">IT Administrators can define and implement policy settings on HoloLens 2.</span></span> <span data-ttu-id="36fc1-105">Выбранный сценарий развертывания определяет рекомендуемые настройки конфигурации, а корпоративные устройства обеспечивают для ИТ-отдела самый широкий выбор инструментов контроля.</span><span class="sxs-lookup"><span data-stu-id="36fc1-105">What configuration settings you use will differ based on the deployment scenario, and corporate devices will offer IT the broadest range of control.</span></span> <span data-ttu-id="36fc1-106">В Windows 10 поставщики служб конфигурации (CSP) — это интерфейс для чтения, настройки, изменения или удаления параметров конфигурации на устройстве.</span><span class="sxs-lookup"><span data-stu-id="36fc1-106">In Windows 10, Configuration Service Providers (CSP)s are an interface to read, set, modify, or delete configuration settings on the device.</span></span> <span data-ttu-id="36fc1-107">Эти параметры сопоставляются разделам реестра или файлам.</span><span class="sxs-lookup"><span data-stu-id="36fc1-107">These settings map to registry keys or files.</span></span> <span data-ttu-id="36fc1-108">Некоторые поставщики служб конфигурации поддерживают формат WAP, другие поддерживают SyncML, а другие поддерживают оба.</span><span class="sxs-lookup"><span data-stu-id="36fc1-108">Some configuration service providers support the WAP format, some support SyncML, and some support both.</span></span>

<span data-ttu-id="36fc1-109">Дополнительные сведения о CPS для управления голографическими устройствами Windows 10 см. в полном списке CSP, поддерживаемых на устройствах [HoloLens.](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference#hololens)</span><span class="sxs-lookup"><span data-stu-id="36fc1-109">For more information about Windows 10 Holographic device management CSPs, see the full list of [CSPs supported in HoloLens devices](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference#hololens).</span></span>
<span data-ttu-id="36fc1-110">ИТ-администраторы также могут управлять CSP политики на устройствах. См. полный список CSP политики, поддерживаемых [HoloLens 2.](https://docs.microsoft.com/windows/client-management/mdm/policy-csps-supported-by-hololens2)</span><span class="sxs-lookup"><span data-stu-id="36fc1-110">IT Administrators can also manage Policy CSP on devices, see the full list of [Policy CSPs supported by HoloLens 2](https://docs.microsoft.com/windows/client-management/mdm/policy-csps-supported-by-hololens2).</span></span>

## <span data-ttu-id="36fc1-111">Методы конфигурации</span><span class="sxs-lookup"><span data-stu-id="36fc1-111">Configuration methods</span></span>

### <span data-ttu-id="36fc1-112">Настройка с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="36fc1-112">Configure with MDM</span></span>

<span data-ttu-id="36fc1-113">Управление политиками и политиками CSP можно легко управлять на любом личном или корпоративном устройстве, зарегистрированных в системе MDM.</span><span class="sxs-lookup"><span data-stu-id="36fc1-113">CSPs and Policies can be easily managed on any personal or corporate device enrolled in an MDM system.</span></span> <span data-ttu-id="36fc1-114">После регистрации устройства в решении MDM вы сможете управлять этим устройством или набором устройств с помощью конфигураций устройств.</span><span class="sxs-lookup"><span data-stu-id="36fc1-114">Once a device is enrolled in your MDM solution, you will be able to manage that device, or set of devices using device configurations.</span></span> <span data-ttu-id="36fc1-115">Узнайте больше об управлении [устройствами HoloLens с помощью MDM.](hololens-mdm-configure.md)</span><span class="sxs-lookup"><span data-stu-id="36fc1-115">Learn more about how to [manage your HoloLens devices through MDM](hololens-mdm-configure.md).</span></span>

### <span data-ttu-id="36fc1-116">Настройка с помощью пакетов подготовка</span><span class="sxs-lookup"><span data-stu-id="36fc1-116">Configure with Provisioning Packages</span></span>

<span data-ttu-id="36fc1-117">HoloLens 2 также поддерживает настройку ограниченного набора конфигураций CSP для устройств HoloLens 2 с помощью пользовательских пакетов подготовка.</span><span class="sxs-lookup"><span data-stu-id="36fc1-117">HoloLens 2 also supports setting a limited set of CSP configurations for HoloLens 2 devices through custom Provisioning Packages.</span></span> <span data-ttu-id="36fc1-118">Пакеты подготовка обычно используются для устройств, не управляемых MDM, и их необходимо вручную применять к каждому устройству.</span><span class="sxs-lookup"><span data-stu-id="36fc1-118">Provisioning Packages are typically leveraged for non-MDM managed devices and require to be manually applied to each device.</span></span> <span data-ttu-id="36fc1-119">Ознакомьтесь с информацией о создании [пользовательских пакетов подготовка для HoloLens.](https://docs.microsoft.com/hololens/hololens-provisioning)</span><span class="sxs-lookup"><span data-stu-id="36fc1-119">Read information on building custom [Provisioning Packages for HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning).</span></span>

## <span data-ttu-id="36fc1-120">Конфигурации</span><span class="sxs-lookup"><span data-stu-id="36fc1-120">Configurations</span></span>

### <span data-ttu-id="36fc1-121">Общие ограничения устройств</span><span class="sxs-lookup"><span data-stu-id="36fc1-121">Common device restrictions</span></span>

<span data-ttu-id="36fc1-122">Некоторые ограничения устройства просты и отключают функции или подключение к устройству.</span><span class="sxs-lookup"><span data-stu-id="36fc1-122">Some device restrictions are as simple and disabling a functionality or connection to the device.</span></span> <span data-ttu-id="36fc1-123">Чтобы узнать больше об этих [ограничениях, ознакомьтесь с общими ограничениями устройств.](hololens-common-device-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="36fc1-123">To learn about these read more about [common device restrictions.](hololens-common-device-restrictions.md)</span></span>

### <span data-ttu-id="36fc1-124">Режимы терминала</span><span class="sxs-lookup"><span data-stu-id="36fc1-124">Kiosk modes</span></span>

<span data-ttu-id="36fc1-125">Используйте режим терминала, чтобы контролировать, какие удостоверения имеют доступ к приложениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36fc1-125">Use Kiosk mode to control which identities have access to which apps by default.</span></span> <span data-ttu-id="36fc1-126">Киоски можно использовать для одного или нескольких пользовательских интерфейсов приложений.</span><span class="sxs-lookup"><span data-stu-id="36fc1-126">Kiosks can be used for a single app or multiple app UI experience.</span></span> <span data-ttu-id="36fc1-127">Конфигурации киоска могут варьироваться от одного приложения для любого, кто использует устройство, до разных наборов приложений для разных групп.</span><span class="sxs-lookup"><span data-stu-id="36fc1-127">Kiosk configurations range from a single app for anyone using the device, to different selections of apps for different groups.</span></span> <span data-ttu-id="36fc1-128">Режим терминала не останавливает запуск "разрешенных приложений" другими приложениями и не предназначен для использования.</span><span class="sxs-lookup"><span data-stu-id="36fc1-128">Kiosk mode does not stop “allowed apps” from launching other apps and was not intended to ever.</span></span> <span data-ttu-id="36fc1-129">Узнайте больше [о режимах терминала и о том, как их использовать.](hololens-kiosk.md)</span><span class="sxs-lookup"><span data-stu-id="36fc1-129">Learn more by [reading about Kiosk modes and how to use them](hololens-kiosk.md).</span></span>

### <span data-ttu-id="36fc1-130">Видимость страницы параметров</span><span class="sxs-lookup"><span data-stu-id="36fc1-130">Settings Page Visibility</span></span>

<span data-ttu-id="36fc1-131">Используйте политику приложения "Параметры", чтобы контролировать, какие удостоверения имеют доступ к настройкам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36fc1-131">Use Settings app policy to control which identities have access to settings by default.</span></span> <span data-ttu-id="36fc1-132">С помощью этой политики приложение "Параметры" можно настроить для показа только выбранных страниц или скрытие всех выбранных страниц.</span><span class="sxs-lookup"><span data-stu-id="36fc1-132">Using this policy the Settings app can be configured to either show only the select pages, or hide all selected pages.</span></span> <span data-ttu-id="36fc1-133">[Узнайте о настройке доступных страниц.](settings-uri-list.md)</span><span class="sxs-lookup"><span data-stu-id="36fc1-133">[Read about how to configure the pages available](settings-uri-list.md).</span></span>

<span data-ttu-id="36fc1-134">В настоящее время эта функция доступна только в [сборках для windows Insider.](hololens-insider.md)</span><span class="sxs-lookup"><span data-stu-id="36fc1-134">This feature is currently only available in [Windows Insider builds](hololens-insider.md).</span></span> <span data-ttu-id="36fc1-135">Убедитесь, что устройства, для которые вы собираетесь использовать эту функцию, находятся в сборке 19041.1349+.</span><span class="sxs-lookup"><span data-stu-id="36fc1-135">Ensure devices you intend to use this feature for are on build 19041.1349+.</span></span>

### <span data-ttu-id="36fc1-136">WDAC</span><span class="sxs-lookup"><span data-stu-id="36fc1-136">WDAC</span></span>

<span data-ttu-id="36fc1-137">Используйте конфигурацию WDAC для управления тем, какие приложения или процессы разрешены или запрещены для запуска независимо от того, находится ли система в режиме терминала или нет.</span><span class="sxs-lookup"><span data-stu-id="36fc1-137">Use WDAC configuration to control which apps / processes are allowed / disallowed to be launched irrespective of whether system is in kiosk mode or not.</span></span>
[<span data-ttu-id="36fc1-138">См. наш обзор WDAC.</span><span class="sxs-lookup"><span data-stu-id="36fc1-138">See our overview for WDAC.</span></span>](windows-defender-application-control-wdac.md)
