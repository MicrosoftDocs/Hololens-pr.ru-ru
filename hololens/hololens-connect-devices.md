---
title: Подключение к устройствам с Bluetooth и USB-C
description: Начните подключение к устройствам с Bluetooth USB-C, а также к аксессуарам устройств смешанной реальности HoloLens.
ms.assetid: 01af0848-3b36-4c13-b797-f38ad3977e30
ms.prod: hololens
ms.sitesec: library
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.localizationpriority: high
ms.date: 03/11/2020
manager: jarrettr
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 1b4f95f43fc60dffa2ca75322466857a0a20a0a7
ms.sourcegitcommit: 145bbabc390f626ba6633fa49423c38656cd2224
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "11302273"
---
# <span data-ttu-id="849ac-103">Подключение к устройствам с Bluetooth и USB-C</span><span class="sxs-lookup"><span data-stu-id="849ac-103">Connect to Bluetooth and USB-C devices</span></span>

> [!NOTE]
> <span data-ttu-id="849ac-104">Внешние микрофоны нельзя использовать.</span><span class="sxs-lookup"><span data-stu-id="849ac-104">External microphones cannot be used.</span></span> <span data-ttu-id="849ac-105">HoloLens 2 использует собственный встроенный [набор микрофонов](hololens2-hardware.md#audio-and-speech).</span><span class="sxs-lookup"><span data-stu-id="849ac-105">HoloLens 2 uses its built-in [microphone array](hololens2-hardware.md#audio-and-speech).</span></span>

## <span data-ttu-id="849ac-106">Связывание устройств с Bluetooth</span><span class="sxs-lookup"><span data-stu-id="849ac-106">Pair Bluetooth devices</span></span>

<span data-ttu-id="849ac-107">HoloLens 2 поддерживает перечисленные ниже классы устройств с Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="849ac-107">HoloLens 2 supports the following classes of Bluetooth devices:</span></span>

- <span data-ttu-id="849ac-108">Мышь</span><span class="sxs-lookup"><span data-stu-id="849ac-108">Mouse</span></span>
- <span data-ttu-id="849ac-109">Клавиатура</span><span class="sxs-lookup"><span data-stu-id="849ac-109">Keyboard</span></span>
- <span data-ttu-id="849ac-110">Устройства с аудиовыходом Bluetooth (A2DP)</span><span class="sxs-lookup"><span data-stu-id="849ac-110">Bluetooth audio output (A2DP) devices</span></span>

<span data-ttu-id="849ac-111">HoloLens (1-го поколения) поддерживает перечисленные ниже классы устройств с Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="849ac-111">HoloLens (1st gen) supports the following classes of Bluetooth devices:</span></span>

- <span data-ttu-id="849ac-112">Мышь</span><span class="sxs-lookup"><span data-stu-id="849ac-112">Mouse</span></span>
- <span data-ttu-id="849ac-113">Клавиатура</span><span class="sxs-lookup"><span data-stu-id="849ac-113">Keyboard</span></span>
- <span data-ttu-id="849ac-114">Пульт HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="849ac-114">HoloLens (1st gen) clicker</span></span>

> [!NOTE]
> <span data-ttu-id="849ac-115">Другие устройства с Bluetooth, такие как динамики, гарнитуры, смартфоны и игровые планшеты, могут быть перечислены в параметрах HoloLens как доступные.</span><span class="sxs-lookup"><span data-stu-id="849ac-115">Other types of Bluetooth devices, such as speakers, headsets, smartphones, and game pads, may be listed as available in HoloLens settings.</span></span> <span data-ttu-id="849ac-116">Однако в HoloLens (1-го поколения ) такие устройства не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="849ac-116">However, these devices aren't supported on HoloLens (1st gen).</span></span> <span data-ttu-id="849ac-117">Дополнительные сведения см. в статье [В параметрах HoloLens устройства указаны как доступные, но они не работают](hololens-FAQ.md#hololens-settings-lists-devices-as-available-but-the-devices-dont-work).</span><span class="sxs-lookup"><span data-stu-id="849ac-117">For more information, see [HoloLens Settings lists devices as available, but the devices don't work](hololens-FAQ.md#hololens-settings-lists-devices-as-available-but-the-devices-dont-work).</span></span>

### <span data-ttu-id="849ac-118">Связывание клавиатуры или мыши с Bluetooth</span><span class="sxs-lookup"><span data-stu-id="849ac-118">Pair a Bluetooth keyboard or mouse</span></span>

1. <span data-ttu-id="849ac-119">Включите клавиатуру или мышь и сделайте их обнаруживаемыми.</span><span class="sxs-lookup"><span data-stu-id="849ac-119">Turn on your keyboard or mouse, and make it discoverable.</span></span> <span data-ttu-id="849ac-120">Чтобы узнать, как сделать устройство обнаруживаемым, посмотрите информацию на самом устройстве (или в документации к нему) или посетите веб-сайт его производителя.</span><span class="sxs-lookup"><span data-stu-id="849ac-120">To learn how to make the device discoverable, look for information on the device (or its documentation) or visit the manufacturer's website.</span></span>

1. <span data-ttu-id="849ac-121">Используйте жест раскрытия ладони (HoloLens (1-го поколения)) или жест запуска (HoloLens 2), чтобы перейти в меню **Пуск**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="849ac-121">Use the bloom gesture (HoloLens (1st gen)) or the start gesture (HoloLens 2) to go to **Start**, and then select **Settings**.</span></span>

1. <span data-ttu-id="849ac-122">Выберите **Устройства** и проверьте, включен ли Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="849ac-122">Select **Devices**, and make sure that Bluetooth is on.</span></span>  

1. <span data-ttu-id="849ac-123">Когда появится имя устройства, нажмите **Связать** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="849ac-123">When you see the device name, select **Pair**, and then follow the instructions.</span></span>

### <span data-ttu-id="849ac-124">HoloLens (1-го поколения): связывание пульта</span><span class="sxs-lookup"><span data-stu-id="849ac-124">HoloLens (1st gen): Pair the clicker</span></span>

1. <span data-ttu-id="849ac-125">Используйте жест раскрытия ладони, чтобы перейти в меню **Пуск**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="849ac-125">Use the bloom gesture to go to **Start**, and then select **Settings**.</span></span>

1. <span data-ttu-id="849ac-126">Выберите **Устройства** и проверьте, включен ли Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="849ac-126">Select **Devices**, and make sure that Bluetooth is on.</span></span>

1. <span data-ttu-id="849ac-127">Нажмите кончиком ручки кнопку связывания пульта и удерживайте ее, пока индикатор состояния пульта не начнет мигать белым цветом.</span><span class="sxs-lookup"><span data-stu-id="849ac-127">Use the tip of a pen to press and hold the clicker pairing button until the clicker status light blinks white.</span></span> <span data-ttu-id="849ac-128">Удерживайте кнопку нажатой до тех пор, пока световой индикатор не начнет мигать.</span><span class="sxs-lookup"><span data-stu-id="849ac-128">Make sure to hold down the button until the light starts blinking.</span></span>  

   <span data-ttu-id="849ac-129">Кнопка связывания находится на нижней стороне пульта, рядом с кольцом для пальца.</span><span class="sxs-lookup"><span data-stu-id="849ac-129">The pairing button is on the underside of the clicker, next to the finger loop.</span></span>

   ![Кнопка связывания находится рядом с кольцом для пальца.](images/use-hololens-clicker-1.png)

1. <span data-ttu-id="849ac-131">На экране связывания выберите **Пульт** > **Связать**.</span><span class="sxs-lookup"><span data-stu-id="849ac-131">On the pairing screen, select **Clicker** > **Pair**.</span></span>

## <span data-ttu-id="849ac-132">Выключите Bluetooth</span><span class="sxs-lookup"><span data-stu-id="849ac-132">Disable Bluetooth</span></span>

<span data-ttu-id="849ac-133">Эта процедура выключает радиочастотные компоненты адаптера Bluetooth и все функции Bluetooth в Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="849ac-133">This procedure turns off the RF components of the Bluetooth radio and disables all Bluetooth functionality on Microsoft HoloLens.</span></span>

1. <span data-ttu-id="849ac-134">Используйте жест раскрытия ладони (HoloLens (1-го поколения)) или жест запуска (HoloLens 2), чтобы перейти в меню **Пуск**, а затем выберите **Параметры** > **Устройства**.</span><span class="sxs-lookup"><span data-stu-id="849ac-134">Use the bloom gesture (HoloLens (1st gen)) or the start gesture (HoloLens 2) to go to **Start**, and then select **Settings** > **Devices**.</span></span>

1. <span data-ttu-id="849ac-135">Переместите ползунок **Bluetooth** в положение**Выключено**.</span><span class="sxs-lookup"><span data-stu-id="849ac-135">Move the slider switch for **Bluetooth** to the **Off** position.</span></span>

## <span data-ttu-id="849ac-136">HoloLens 2: подключение устройств с USB-C</span><span class="sxs-lookup"><span data-stu-id="849ac-136">HoloLens 2: Connect USB-C devices</span></span>

<span data-ttu-id="849ac-137">HoloLens 2 поддерживает перечисленные ниже классы устройств с USB-C.</span><span class="sxs-lookup"><span data-stu-id="849ac-137">HoloLens 2 supports the following classes of USB-C devices:</span></span>

- <span data-ttu-id="849ac-138">Запоминающие устройства (например, USB-накопители)</span><span class="sxs-lookup"><span data-stu-id="849ac-138">Mass storage devices (such as thumb drives)</span></span>
- <span data-ttu-id="849ac-139">Адаптеры Ethernet (включая подключение по сети Ethernet с функцией подзарядки)</span><span class="sxs-lookup"><span data-stu-id="849ac-139">Ethernet adapters (including ethernet plus charging)</span></span>
- <span data-ttu-id="849ac-140">Цифровые звуковые адаптеры-переходники с USB-C на 3,5 мм</span><span class="sxs-lookup"><span data-stu-id="849ac-140">USB-C-to-3.5mm digital audio adapters</span></span>
- <span data-ttu-id="849ac-141">Цифровые аудио гарнитуры USB-C (включая адаптеры гарнитур с функцией подзарядки)</span><span class="sxs-lookup"><span data-stu-id="849ac-141">USB-C digital audio headsets (including headset adapters plus charging)</span></span>
- <span data-ttu-id="849ac-142">Проводная мышь</span><span class="sxs-lookup"><span data-stu-id="849ac-142">Wired mouse</span></span>
- <span data-ttu-id="849ac-143">Проводная клавиатура</span><span class="sxs-lookup"><span data-stu-id="849ac-143">Wired keyboard</span></span>
- <span data-ttu-id="849ac-144">Набор концентраторов с функцией подзарядки PD (USB A и подзарядка PD)</span><span class="sxs-lookup"><span data-stu-id="849ac-144">Combination PD hubs (USB A plus PD charging)</span></span>

> [!NOTE]
> <span data-ttu-id="849ac-145">Некоторые мобильные устройства с подключениями USB-C опознаются в HoloLens в качестве адаптеров Ethernet, поэтому их можно конфигурировать для доступа к мобильным данным, начиная с Windows Holographic, версия 2004.</span><span class="sxs-lookup"><span data-stu-id="849ac-145">Some mobile devices with USB-C connections present themselves to the HoloLens as ethernet adaptors, and therefore could be used in a tethering configuration, starting with Windows Holographic, version 2004.</span></span> <span data-ttu-id="849ac-146">USB-модемы LTE, для которых требуется отдельный драйвер, или приложения, установленные для конфигурирования, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="849ac-146">USB LTE modems that require a separate driver, and/or application installed for configuration are not supported.</span></span>

<span data-ttu-id="849ac-147">В ответ на отзывы клиентов мы добавили ограниченную поддержку мобильного соединения с подключением напрямую к HoloLens через USB-C.</span><span class="sxs-lookup"><span data-stu-id="849ac-147">In response to customer feedback, we have enabled limited support for cellular connectivity tethered directly to the HoloLens via USB-C.</span></span>  <span data-ttu-id="849ac-148">Такое соединение работает только для устройств, которые поддерживают внедрение общего драйвера [RNDIS](https://docs.microsoft.com/windows-hardware/drivers/network/overview-of-remote-ndis--rndis-) Майкрософт и не требуют установки дополнительных драйверов или приложений.</span><span class="sxs-lookup"><span data-stu-id="849ac-148">Tethered connectivity only works for devices that support the generic Microsoft [RNDIS](https://docs.microsoft.com/windows-hardware/drivers/network/overview-of-remote-ndis--rndis-) driver implementation and that don’t require any additional drivers or application installs.</span></span>  <span data-ttu-id="849ac-149">После подключения такое устройство автоматически отображается как новое соединение Ethernet в пользовательском интерфейсе сетевых настроек HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="849ac-149">Such device, when connected, will automatically appear as a new Ethernet connection in the HoloLens 2 Network Settings UI.</span></span> <span data-ttu-id="849ac-150">Проконсультируйтесь с производителем устройства, чтобы узнать, поддерживает ли оно общий драйвер RNDIS Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="849ac-150">Please consult your device’s manufacturer for further details on whether it supports the generic Microsoft RNDIS driver.</span></span>

### <span data-ttu-id="849ac-151">Концентраторы USB-C</span><span class="sxs-lookup"><span data-stu-id="849ac-151">USB-C Hubs</span></span>

<span data-ttu-id="849ac-152">Некоторым пользователям может потребоваться подключить несколько устройств одновременно.</span><span class="sxs-lookup"><span data-stu-id="849ac-152">Some users may need to connect multiple devices at once.</span></span> <span data-ttu-id="849ac-153">Пользователям, которые хотят ознакомиться с предварительной функцией и [использовать микрофон USB-C](hololens-insider.md#usb-c-external-microphone-support) вместе с другим подключенным устройством, подойдут концентраторы USB-C.</span><span class="sxs-lookup"><span data-stu-id="849ac-153">For users who would like to preview an Insider feature and [use a USB-C microphone](hololens-insider.md#usb-c-external-microphone-support) along with another connected device, USB-C hubs may fit the customer's need.</span></span> <span data-ttu-id="849ac-154">Корпорация Майкрософт не тестировала эти устройства и не может рекомендовать какие-либо конкретные торговые марки.</span><span class="sxs-lookup"><span data-stu-id="849ac-154">Microsoft has not tested these devices, nor can we recommend any specific brands.</span></span>

**<span data-ttu-id="849ac-155">Требования к концентратору USB-C и подключенным устройствам:</span><span class="sxs-lookup"><span data-stu-id="849ac-155">Requirements for USB-C hub and connected devices:</span></span>**

- <span data-ttu-id="849ac-156">Подключенные устройства не должны требовать установки драйвера.</span><span class="sxs-lookup"><span data-stu-id="849ac-156">Connected devices must not require a driver to be installed.</span></span>
- <span data-ttu-id="849ac-157">Общая передаваемая мощность всех подключенных устройств не должна превышать 4,5 Ватт.</span><span class="sxs-lookup"><span data-stu-id="849ac-157">The total power draw of all connected devices must be below 4.5 Watts.</span></span>

## <span data-ttu-id="849ac-158">Подключение к Miracast</span><span class="sxs-lookup"><span data-stu-id="849ac-158">Connect to Miracast</span></span>

<span data-ttu-id="849ac-159">Чтобы использовать Miracast, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="849ac-159">To use Miracast, follow these steps:</span></span>

1. <span data-ttu-id="849ac-160">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="849ac-160">Do one of the following:</span></span>  

   - <span data-ttu-id="849ac-161">Откройте меню **Пуск** и выберите значок дисплея.</span><span class="sxs-lookup"><span data-stu-id="849ac-161">Open the **Start** menu, and select the display icon.</span></span>
   - <span data-ttu-id="849ac-162">Произнесите "Подключить", когда вы смотрите на меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="849ac-162">Say "Connect" while you gaze at the **Start** menu.</span></span>  

1. <span data-ttu-id="849ac-163">В появившемся списке устройств выберите доступное устройство.</span><span class="sxs-lookup"><span data-stu-id="849ac-163">On the list of devices that appears, select an available device.</span></span>

1. <span data-ttu-id="849ac-164">Завершите связывание устройств, чтобы начать проецирование.</span><span class="sxs-lookup"><span data-stu-id="849ac-164">Complete the pairing to begin projecting.</span></span>
