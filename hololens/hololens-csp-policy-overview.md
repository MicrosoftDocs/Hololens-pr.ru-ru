---
title: Обзор настройки CSP и управления устройствами
description: Узнайте, как настраивать CSP, политики и управление устройствами с помощью управления мобильными устройствами и подготовки пакетов.
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
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309719"
---
# <a name="configure-csps-and-device-management-overview"></a><span data-ttu-id="36989-103">Обзор настройки CSP и управления устройствами</span><span class="sxs-lookup"><span data-stu-id="36989-103">Configure CSPs and Device Management overview</span></span>

<span data-ttu-id="36989-104">ИТ администраторы могут определять и реализовывать параметры политики в HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="36989-104">IT Administrators can define and implement policy settings on HoloLens 2.</span></span> <span data-ttu-id="36989-105">Выбранный сценарий развертывания определяет рекомендуемые настройки конфигурации, а корпоративные устройства обеспечивают для ИТ-отдела самый широкий выбор инструментов контроля.</span><span class="sxs-lookup"><span data-stu-id="36989-105">What configuration settings you use will differ based on the deployment scenario, and corporate devices will offer IT the broadest range of control.</span></span> <span data-ttu-id="36989-106">В Windows 10 поставщики службы настройки (CSP) — это интерфейс для чтения, установки, изменения или удаления параметров конфигурации на устройстве.</span><span class="sxs-lookup"><span data-stu-id="36989-106">In Windows 10, Configuration Service Providers (CSP)s are an interface to read, set, modify, or delete configuration settings on the device.</span></span> <span data-ttu-id="36989-107">Эти параметры сопоставляются с разделами или файлами реестра.</span><span class="sxs-lookup"><span data-stu-id="36989-107">These settings map to registry keys or files.</span></span> <span data-ttu-id="36989-108">Некоторые поставщики служб конфигурации поддерживают формат WAP, некоторые поддерживают SyncML, а некоторые поддерживают оба варианта.</span><span class="sxs-lookup"><span data-stu-id="36989-108">Some configuration service providers support the WAP format, some support SyncML, and some support both.</span></span>

<span data-ttu-id="36989-109">Дополнительные сведения о CSP для управления устройствами Windows 10 holographic см. в полном списке CSP, [поддерживаемых на устройствах HoloLens](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference#hololens).</span><span class="sxs-lookup"><span data-stu-id="36989-109">For more information about Windows 10 Holographic device management CSPs, see the full list of [CSPs supported in HoloLens devices](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference#hololens).</span></span>
<span data-ttu-id="36989-110">ИТ администраторы также могут управлять CSP политики на устройствах. полный список [CSP политик, поддерживаемых HoloLens 2](https://docs.microsoft.com/windows/client-management/mdm/policy-csps-supported-by-hololens2).</span><span class="sxs-lookup"><span data-stu-id="36989-110">IT Administrators can also manage Policy CSP on devices, see the full list of [Policy CSPs supported by HoloLens 2](https://docs.microsoft.com/windows/client-management/mdm/policy-csps-supported-by-hololens2).</span></span>

## <a name="configuration-methods"></a><span data-ttu-id="36989-111">Методы настройки</span><span class="sxs-lookup"><span data-stu-id="36989-111">Configuration methods</span></span>

### <a name="configure-with-mdm"></a><span data-ttu-id="36989-112">Настройка с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="36989-112">Configure with MDM</span></span>

<span data-ttu-id="36989-113">CSP и политики можно легко управлять на любом персональном или корпоративном устройстве, зарегистрированном в системе MDM.</span><span class="sxs-lookup"><span data-stu-id="36989-113">CSPs and Policies can be easily managed on any personal or corporate device enrolled in an MDM system.</span></span> <span data-ttu-id="36989-114">После регистрации устройства в решении MDM вы сможете управлять этим устройством или набором устройств с помощью конфигураций устройств.</span><span class="sxs-lookup"><span data-stu-id="36989-114">Once a device is enrolled in your MDM solution, you will be able to manage that device, or set of devices using device configurations.</span></span> <span data-ttu-id="36989-115">Дополнительные сведения об [управлении устройствами HoloLens с помощью MDM](hololens-mdm-configure.md).</span><span class="sxs-lookup"><span data-stu-id="36989-115">Learn more about how to [manage your HoloLens devices through MDM](hololens-mdm-configure.md).</span></span>

### <a name="configure-with-provisioning-packages"></a><span data-ttu-id="36989-116">Настройка с помощью пакетов подготовки</span><span class="sxs-lookup"><span data-stu-id="36989-116">Configure with Provisioning Packages</span></span>

<span data-ttu-id="36989-117">HoloLens 2 также поддерживает задание ограниченного набора конфигураций CSP для устройств HoloLens 2 с помощью настраиваемых пакетов подготовки.</span><span class="sxs-lookup"><span data-stu-id="36989-117">HoloLens 2 also supports setting a limited set of CSP configurations for HoloLens 2 devices through custom Provisioning Packages.</span></span> <span data-ttu-id="36989-118">Пакеты подготовки обычно используются для устройств под управлением, не являющихся управляемыми MDM, и их необходимо вручную применять к каждому устройству.</span><span class="sxs-lookup"><span data-stu-id="36989-118">Provisioning Packages are typically leveraged for non-MDM managed devices and require to be manually applied to each device.</span></span> <span data-ttu-id="36989-119">Ознакомьтесь со сведениями о создании пользовательских [пакетов подготовки для HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning).</span><span class="sxs-lookup"><span data-stu-id="36989-119">Read information on building custom [Provisioning Packages for HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning).</span></span>

## <a name="configurations"></a><span data-ttu-id="36989-120">Конфигурации</span><span class="sxs-lookup"><span data-stu-id="36989-120">Configurations</span></span>

### <a name="common-device-restrictions"></a><span data-ttu-id="36989-121">Общие ограничения для устройств</span><span class="sxs-lookup"><span data-stu-id="36989-121">Common device restrictions</span></span>

<span data-ttu-id="36989-122">Некоторые ограничения на устройства являются простыми и отключают функциональность или подключение к устройству.</span><span class="sxs-lookup"><span data-stu-id="36989-122">Some device restrictions are as simple and disabling a functionality or connection to the device.</span></span> <span data-ttu-id="36989-123">Дополнительные сведения об [общих ограничениях устройств см.](hololens-common-device-restrictions.md) в этой статье.</span><span class="sxs-lookup"><span data-stu-id="36989-123">To learn about these read more about [common device restrictions.](hololens-common-device-restrictions.md)</span></span>

### <a name="kiosk-modes"></a><span data-ttu-id="36989-124">Режимы киоска</span><span class="sxs-lookup"><span data-stu-id="36989-124">Kiosk modes</span></span>

<span data-ttu-id="36989-125">Используйте режим киоска для управления тем, какие удостоверения имеют доступ к каким приложениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36989-125">Use Kiosk mode to control which identities have access to which apps by default.</span></span> <span data-ttu-id="36989-126">Киоски можно использовать для одного приложения или интерфейса нескольких приложений.</span><span class="sxs-lookup"><span data-stu-id="36989-126">Kiosks can be used for a single app or multiple app UI experience.</span></span> <span data-ttu-id="36989-127">Конфигурации киоска находятся в одном приложении для всех пользователей, использующих устройство, для различных групп приложений.</span><span class="sxs-lookup"><span data-stu-id="36989-127">Kiosk configurations range from a single app for anyone using the device, to different selections of apps for different groups.</span></span> <span data-ttu-id="36989-128">Режим киоска не останавливает запуск других приложений с "разрешенных приложений" и не предназначался для этого.</span><span class="sxs-lookup"><span data-stu-id="36989-128">Kiosk mode does not stop “allowed apps” from launching other apps and was not intended to ever.</span></span> <span data-ttu-id="36989-129">Дополнительные сведения см. в статье [о режимах киоска и способах их использования](hololens-kiosk.md).</span><span class="sxs-lookup"><span data-stu-id="36989-129">Learn more by [reading about Kiosk modes and how to use them](hololens-kiosk.md).</span></span>

### <a name="settings-page-visibility"></a><span data-ttu-id="36989-130">Видимость страницы параметров</span><span class="sxs-lookup"><span data-stu-id="36989-130">Settings Page Visibility</span></span>

<span data-ttu-id="36989-131">Используйте параметры Политика приложений, чтобы указать, какие удостоверения имеют доступ к параметрам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36989-131">Use Settings app policy to control which identities have access to settings by default.</span></span> <span data-ttu-id="36989-132">С помощью этой политики приложение параметров может быть настроено на отображение только страниц выбора или скрытие всех выбранных страниц.</span><span class="sxs-lookup"><span data-stu-id="36989-132">Using this policy the Settings app can be configured to either show only the select pages, or hide all selected pages.</span></span> <span data-ttu-id="36989-133">[Ознакомьтесь со сведениями о настройке доступных страниц](settings-uri-list.md).</span><span class="sxs-lookup"><span data-stu-id="36989-133">[Read about how to configure the pages available](settings-uri-list.md).</span></span>

<span data-ttu-id="36989-134">В настоящее время эта функция доступна только в [сборках программы предварительной оценки Windows](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="36989-134">This feature is currently only available in [Windows Insider builds](hololens-insider.md).</span></span> <span data-ttu-id="36989-135">Убедитесь, что устройства, для которых планируется использовать эту функцию, включены в сборку 19041.1349 +.</span><span class="sxs-lookup"><span data-stu-id="36989-135">Ensure devices you intend to use this feature for are on build 19041.1349+.</span></span>

### <a name="wdac"></a><span data-ttu-id="36989-136">WDAC</span><span class="sxs-lookup"><span data-stu-id="36989-136">WDAC</span></span>

<span data-ttu-id="36989-137">Используйте конфигурацию WDAC, чтобы указать, какие приложения и процессы разрешены и запрещены для запуска независимо от того, находится ли система в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="36989-137">Use WDAC configuration to control which apps / processes are allowed / disallowed to be launched irrespective of whether system is in kiosk mode or not.</span></span>
[<span data-ttu-id="36989-138">См. наш обзор для WDAC.</span><span class="sxs-lookup"><span data-stu-id="36989-138">See our overview for WDAC.</span></span>](windows-defender-application-control-wdac.md)
