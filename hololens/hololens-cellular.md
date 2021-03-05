---
title: Подключение к сети мобильной связи и сети 5G
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
ms.openlocfilehash: 3fd5f6baf05277bcbf2bf4152ba4735ca91e5bd0
ms.sourcegitcommit: fbc8ddb17e31fea8667ece43a511592b86ac3947
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "11385649"
---
# <a name="connect-to-cellular-and-5g"></a><span data-ttu-id="d3170-103">Подключение к сети мобильной связи и сети 5G</span><span class="sxs-lookup"><span data-stu-id="d3170-103">Connect to Cellular and 5G</span></span>

<span data-ttu-id="d3170-104">HoloLens 2 поддерживает два способа подключения к сети мобильной связи и сети 5G:</span><span class="sxs-lookup"><span data-stu-id="d3170-104">HoloLens 2 supports two methods for connecting to cellular and 5G networks:</span></span>

- <span data-ttu-id="d3170-105">Динамическая сеть Wi-Fi, предоставляемая мобильным устройством (также известная как "хот-спот")</span><span class="sxs-lookup"><span data-stu-id="d3170-105">An ad hoc WiFi network provided by the cellular device, commonly referred to as a "Hotspot"</span></span>
- <span data-ttu-id="d3170-106">Подключение через разъем USB-C (поддержка ограничена)</span><span class="sxs-lookup"><span data-stu-id="d3170-106">Limited support for USB-C tethered devices</span></span>

## <a name="hotspot-wifi"></a><span data-ttu-id="d3170-107">Хот-спот (Wi-Fi)</span><span class="sxs-lookup"><span data-stu-id="d3170-107">Hotspot (WiFi)</span></span>

<span data-ttu-id="d3170-108">Большинство потребностей подключения к сети мобильной связи можно удовлетворить с помощью хот-спот.</span><span class="sxs-lookup"><span data-stu-id="d3170-108">Most cellular connectivity needs can be met with a hotspot.</span></span> <span data-ttu-id="d3170-109">HoloLens 2 поддерживает стандарт Wi-Fi 802.11ac и соответствует требованиям к пропускной способности и задержке, предъявляемым к наиболее распространенным случаям использования.</span><span class="sxs-lookup"><span data-stu-id="d3170-109">HoloLens 2 WiFi supports 802.11ac, which can provide the bandwidth and latency requirements necessary for most common use cases.</span></span> <span data-ttu-id="d3170-110">Сеть Wi-Fi также не зависит от кабелей и обеспечивает совместимость с большим количеством мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="d3170-110">WiFi is also cable-free and offers compatibility with the largest number of cellular devices.</span></span>

### <a name="connecting-to-a-hotspot"></a><span data-ttu-id="d3170-111">Подключение к хот-спот</span><span class="sxs-lookup"><span data-stu-id="d3170-111">Connecting to a Hotspot</span></span>

1. <span data-ttu-id="d3170-112">Инструкции по включению режима хот-спот см. в руководстве по использованию вашего устройства.</span><span class="sxs-lookup"><span data-stu-id="d3170-112">Consult your device's manual on how to enable its hotspot mode.</span></span>
1. <span data-ttu-id="d3170-113">Включите режим хот-спот, указав имя сети, а также известный пароль.</span><span class="sxs-lookup"><span data-stu-id="d3170-113">Enable hotspot mode, supplying a name for the network as well as a known password.</span></span>
1. <span data-ttu-id="d3170-114">В настройках сети HoloLens 2 найдите сеть Wi-Fi, созданную на этапе 2, и присоединитесь к ней.</span><span class="sxs-lookup"><span data-stu-id="d3170-114">In HoloLens 2 Network settings, locate the WiFi network created in step 2 and join it.</span></span>

## <a name="usb-c-tethering"></a><span data-ttu-id="d3170-115">Подключение через разъем USB-C</span><span class="sxs-lookup"><span data-stu-id="d3170-115">USB-C Tethering</span></span>

<span data-ttu-id="d3170-116">Подключение через разъем USB-C может обеспечить более низкую задержку, которая требуется при больших рабочих нагрузках.</span><span class="sxs-lookup"><span data-stu-id="d3170-116">USB-C tethering can provide lower latency for advanced workloads that need it.</span></span> <span data-ttu-id="d3170-117">[Удаленная отрисовка Azure](https://azure.microsoft.com/services/remote-rendering), например, может выиграть от подключения по кабелю.</span><span class="sxs-lookup"><span data-stu-id="d3170-117">[Azure Remote Rendering](https://azure.microsoft.com/services/remote-rendering), for example, can benefit from tethering.</span></span> <span data-ttu-id="d3170-118">Обратите внимание, что для подключения требуется кабель между мобильным устройством и устройством HoloLens, и что подключение по кабелю поддерживается ограниченным числом устройств.</span><span class="sxs-lookup"><span data-stu-id="d3170-118">Note that tethering requires a cable between the cellular device and HoloLens, and tethering is supported by a limited number of devices.</span></span>

### <a name="usb-c-compatibility"></a><span data-ttu-id="d3170-119">Совместимость с разъемом USB-C</span><span class="sxs-lookup"><span data-stu-id="d3170-119">USB-C compatibility</span></span>

<span data-ttu-id="d3170-120">Устройства, представляющие собой адаптер Ethernet, могут использоваться с Windows Holographic версии 2004 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="d3170-120">Devices that present themselves as an ethernet adaptor can be used with Windows Holographic version 2004 and later.</span></span>

<span data-ttu-id="d3170-121">Устройства, не представляющие собой адаптер Ethernet, должны поддерживать универсальный драйвер Майкрософт [RNDIS](https://docs.microsoft.com/windows-hardware/drivers/network/overview-of-remote-ndis--rndis-).</span><span class="sxs-lookup"><span data-stu-id="d3170-121">Devices that do not present themselves as an ethernet adapter must support the generic Microsoft [RNDIS](https://docs.microsoft.com/windows-hardware/drivers/network/overview-of-remote-ndis--rndis-) driver.</span></span> <span data-ttu-id="d3170-122">Для получения сведений о поддержке вашим устройством универсального драйвера Майкрософт RNDIS обратитесь к его производителю.</span><span class="sxs-lookup"><span data-stu-id="d3170-122">Please consult your device's manufacturer for details on whether it supports the generic Microsoft RNDIS driver.</span></span>

<span data-ttu-id="d3170-123">Устройства, которые не совместимы с RNDIS или требуют установки драйвера или приложения, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d3170-123">Devices that are not RNDIS compatible, or require a driver or application to be installed, are not supported.</span></span>

<span data-ttu-id="d3170-124">Хотя корпорация Майкрософт не ведет список совместимых устройств, эта тема обсуждается в [сообществе](https://aka.ms/HLCommunityCell).</span><span class="sxs-lookup"><span data-stu-id="d3170-124">While Microsoft does not maintain a list of compatible devices, there is a community discussion on the topic [here](https://aka.ms/HLCommunityCell).</span></span>

### <a name="connecting-to-a-tethered-device"></a><span data-ttu-id="d3170-125">Подключение к устройству по кабелю</span><span class="sxs-lookup"><span data-stu-id="d3170-125">Connecting to a tethered device</span></span>

1. <span data-ttu-id="d3170-126">Инструкции по включению обмена данными через разъем USB см. в руководстве по использованию вашего устройства.</span><span class="sxs-lookup"><span data-stu-id="d3170-126">Consult your device's manual on how to enable data sharing over USB.</span></span> <span data-ttu-id="d3170-127">Этот параметр также называют "подключением через разъем USB", "обменом данными" или "USB-модемом".</span><span class="sxs-lookup"><span data-stu-id="d3170-127">This setting is often referred to as "USB Tethering", "Data Sharing" or "USB Modem".</span></span>
1. <span data-ttu-id="d3170-128">Включите обмен данными через разъем USB.</span><span class="sxs-lookup"><span data-stu-id="d3170-128">Enable data sharing over USB.</span></span>
1. <span data-ttu-id="d3170-129">Подключите устройство к разъему USB-C HoloLens.</span><span class="sxs-lookup"><span data-stu-id="d3170-129">Connect your device to the HoloLens USB-C port.</span></span>
1. <span data-ttu-id="d3170-130">В настройках сети HoloLens 2 устройство автоматически будет отображаться как подключение Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d3170-130">In HoloLens 2 Network settings, the device will automatically appear as an Ethernet connection.</span></span>
