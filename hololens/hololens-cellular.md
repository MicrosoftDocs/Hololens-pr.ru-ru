---
title: Подключение к мобильной сети и 5G
description: Подключение устройств смешанной реальности HoloLens к сети мобильной связи.
ms.assetid: f1aaadce-8762-41f8-bfeb-3b6067a2ec78
ms.prod: hololens
ms.sitesec: library
author: jbienzms
ms.author: jbienz
ms.topic: article
ms.localizationpriority: high
ms.date: 02/24/2021
manager: evmill
appliesto:
- HoloLens 2
ms.openlocfilehash: 6f7da0263e8637486f0151fd2b9da55da8feccc1
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113635846"
---
# <a name="connect-to-cellular-and-5g"></a><span data-ttu-id="eff20-103">Подключение к мобильной сети и 5G</span><span class="sxs-lookup"><span data-stu-id="eff20-103">Connect to Cellular and 5G</span></span>

<span data-ttu-id="eff20-104">HoloLens 2 поддерживает два способа подключения к сети мобильной связи и сети 5G:</span><span class="sxs-lookup"><span data-stu-id="eff20-104">HoloLens 2 supports two methods for connecting to cellular and 5G networks:</span></span>

- <span data-ttu-id="eff20-105">динамическая сеть Wi-Fi, предоставляемая мобильным устройством (также известная как "хот-спот");</span><span class="sxs-lookup"><span data-stu-id="eff20-105">An ad hoc WiFi network provided by the cellular device, commonly referred to as a "Hotspot"</span></span>
- <span data-ttu-id="eff20-106">подключение через разъем USB-C (поддержка ограничена).</span><span class="sxs-lookup"><span data-stu-id="eff20-106">Limited support for USB-C tethered devices</span></span>

## <a name="hotspot-wifi"></a><span data-ttu-id="eff20-107">Хот-спот (Wi-Fi)</span><span class="sxs-lookup"><span data-stu-id="eff20-107">Hotspot (WiFi)</span></span>

<span data-ttu-id="eff20-108">Хот-спот помогает решить большинство задач, требующих подключения к сети мобильной связи.</span><span class="sxs-lookup"><span data-stu-id="eff20-108">Most cellular connectivity needs can be met with a hotspot.</span></span> <span data-ttu-id="eff20-109">HoloLens 2 поддерживает стандарт Wi-Fi 802.11ac и соответствует требованиям к пропускной способности и задержке, предъявляемым к наиболее распространенным вариантам использования.</span><span class="sxs-lookup"><span data-stu-id="eff20-109">HoloLens 2 WiFi supports 802.11ac, which can provide the bandwidth and latency requirements necessary for most common use cases.</span></span> <span data-ttu-id="eff20-110">Сеть Wi-Fi не требует кабелей и обеспечивает совместимость с большим количеством мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="eff20-110">WiFi is also cable-free and offers compatibility with the largest number of cellular devices.</span></span>

### <a name="connecting-to-a-hotspot"></a><span data-ttu-id="eff20-111">Подключение к хот-спот</span><span class="sxs-lookup"><span data-stu-id="eff20-111">Connecting to a Hotspot</span></span>

1. <span data-ttu-id="eff20-112">Инструкции по включению режима "хот-спот" см. в руководстве по использованию вашего устройства.</span><span class="sxs-lookup"><span data-stu-id="eff20-112">Consult your device's manual on how to enable its hotspot mode.</span></span>
1. <span data-ttu-id="eff20-113">Для включения режима "хот-спот" укажите имя сети и известный пароль.</span><span class="sxs-lookup"><span data-stu-id="eff20-113">Enable hotspot mode, supplying a name for the network as well as a known password.</span></span>
1. <span data-ttu-id="eff20-114">В настройках сети HoloLens 2 найдите сеть Wi-Fi, созданную на шаге 2, и присоединитесь к ней.</span><span class="sxs-lookup"><span data-stu-id="eff20-114">In HoloLens 2 Network settings, locate the WiFi network created in step 2 and join it.</span></span>

## <a name="usb-c-tethering"></a><span data-ttu-id="eff20-115">Подключение через разъем USB-C</span><span class="sxs-lookup"><span data-stu-id="eff20-115">USB-C Tethering</span></span>

<span data-ttu-id="eff20-116">Подключение через разъем USB-C может обеспечить более низкую задержку, которая требуется при больших рабочих нагрузках.</span><span class="sxs-lookup"><span data-stu-id="eff20-116">USB-C tethering can provide lower latency for advanced workloads that need it.</span></span> <span data-ttu-id="eff20-117">Например, подключение через разъем можно использовать для [Удаленной отрисовки Azure](https://azure.microsoft.com/services/remote-rendering).</span><span class="sxs-lookup"><span data-stu-id="eff20-117">[Azure Remote Rendering](https://azure.microsoft.com/services/remote-rendering), for example, can benefit from tethering.</span></span> <span data-ttu-id="eff20-118">Не забывайте, что для такого подключения требуется кабель между мобильным устройством и устройством HoloLens, и что подключение по кабелю поддерживается не всеми устройствами.</span><span class="sxs-lookup"><span data-stu-id="eff20-118">Note that tethering requires a cable between the cellular device and HoloLens, and tethering is supported by a limited number of devices.</span></span>

### <a name="usb-c-compatibility"></a><span data-ttu-id="eff20-119">Совместимость с разъемом USB-C</span><span class="sxs-lookup"><span data-stu-id="eff20-119">USB-C compatibility</span></span>

<span data-ttu-id="eff20-120">С Windows Holographic 2004 и более поздних версий могут использоваться устройства, которые выполняют функции адаптера Ethernet.</span><span class="sxs-lookup"><span data-stu-id="eff20-120">A limited number of devices that present themselves as an ethernet adaptor can be used with Windows Holographic version 2004 and later.</span></span>

<span data-ttu-id="eff20-121">Устройства, которые не выполняют функции адаптера Ethernet, должны поддерживать универсальный драйвер Майкрософт [RNDIS](/windows-hardware/drivers/network/overview-of-remote-ndis--rndis-).</span><span class="sxs-lookup"><span data-stu-id="eff20-121">Devices that do not present themselves as an ethernet adapter must support the generic Microsoft [RNDIS](/windows-hardware/drivers/network/overview-of-remote-ndis--rndis-) driver.</span></span> <span data-ttu-id="eff20-122">Но из этих устройств лишь часть совместима с HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="eff20-122">But, only a limited number of those devices are compatible with HoloLens 2.</span></span> <span data-ttu-id="eff20-123">Для получения сведений о поддержке вашим устройством универсального драйвера Майкрософт RNDIS обратитесь к его производителю.</span><span class="sxs-lookup"><span data-stu-id="eff20-123">Please consult your device's manufacturer for details on whether it supports the generic Microsoft RNDIS driver.</span></span>

<span data-ttu-id="eff20-124">Устройства, которые не совместимы с RNDIS либо требуют установки драйвера или приложения, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="eff20-124">Devices that are not RNDIS compatible, or require a driver or application to be installed, are not supported.</span></span>

<span data-ttu-id="eff20-125">Хотя корпорация Майкрософт не ведет список совместимых устройств, эта тема обсуждается [здесь](https://aka.ms/HLCommunityCell).</span><span class="sxs-lookup"><span data-stu-id="eff20-125">While Microsoft does not maintain a list of compatible devices, there is a community discussion on the topic [here](https://aka.ms/HLCommunityCell).</span></span>

### <a name="connecting-to-a-tethered-device"></a><span data-ttu-id="eff20-126">Подключение к устройству по кабелю</span><span class="sxs-lookup"><span data-stu-id="eff20-126">Connecting to a tethered device</span></span>

1. <span data-ttu-id="eff20-127">Инструкции по включению обмена данными через разъем USB см. в руководстве по использованию вашего устройства.</span><span class="sxs-lookup"><span data-stu-id="eff20-127">Consult your device's manual on how to enable data sharing over USB.</span></span> <span data-ttu-id="eff20-128">Обычно эту возможность называют "подключение через USB", "обмен данными" или "USB-модем".</span><span class="sxs-lookup"><span data-stu-id="eff20-128">This setting is often referred to as "USB Tethering", "Data Sharing" or "USB Modem".</span></span>
1. <span data-ttu-id="eff20-129">Включите обмен данными через разъем USB.</span><span class="sxs-lookup"><span data-stu-id="eff20-129">Enable data sharing over USB.</span></span>
1. <span data-ttu-id="eff20-130">Подключите дополнительное устройство к разъему USB-C устройства HoloLens.</span><span class="sxs-lookup"><span data-stu-id="eff20-130">Connect your device to the HoloLens USB-C port.</span></span>
1. <span data-ttu-id="eff20-131">В настройках сети HoloLens 2 новое устройство автоматически отобразится как подключение Ethernet.</span><span class="sxs-lookup"><span data-stu-id="eff20-131">In HoloLens 2 Network settings, the device will automatically appear as an Ethernet connection.</span></span>
