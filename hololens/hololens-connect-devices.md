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
ms.openlocfilehash: 728bf8547315be96f879ff94a1290c1e2b3e7bf8
ms.sourcegitcommit: fbc8ddb17e31fea8667ece43a511592b86ac3947
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "11385486"
---
# <a name="connect-to-bluetooth-and-usb-c-devices"></a><span data-ttu-id="07324-103">Подключение к устройствам с Bluetooth и USB-C</span><span class="sxs-lookup"><span data-stu-id="07324-103">Connect to Bluetooth and USB-C devices</span></span>

> [!NOTE]
> <span data-ttu-id="07324-104">Внешние микрофоны нельзя использовать.</span><span class="sxs-lookup"><span data-stu-id="07324-104">External microphones cannot be used.</span></span> <span data-ttu-id="07324-105">HoloLens 2 использует собственный встроенный [набор микрофонов](hololens2-hardware.md#audio-and-speech).</span><span class="sxs-lookup"><span data-stu-id="07324-105">HoloLens 2 uses its built-in [microphone array](hololens2-hardware.md#audio-and-speech).</span></span>

## <a name="pair-bluetooth-devices"></a><span data-ttu-id="07324-106">Связывание устройств с Bluetooth</span><span class="sxs-lookup"><span data-stu-id="07324-106">Pair Bluetooth devices</span></span>

<span data-ttu-id="07324-107">HoloLens 2 поддерживает перечисленные ниже классы устройств с Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="07324-107">HoloLens 2 supports the following classes of Bluetooth devices:</span></span>

- <span data-ttu-id="07324-108">Мышь</span><span class="sxs-lookup"><span data-stu-id="07324-108">Mouse</span></span>
- <span data-ttu-id="07324-109">Клавиатура</span><span class="sxs-lookup"><span data-stu-id="07324-109">Keyboard</span></span>
- <span data-ttu-id="07324-110">Устройства с аудиовыходом Bluetooth (A2DP)</span><span class="sxs-lookup"><span data-stu-id="07324-110">Bluetooth audio output (A2DP) devices</span></span>

<span data-ttu-id="07324-111">HoloLens (1-го поколения) поддерживает перечисленные ниже классы устройств с Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="07324-111">HoloLens (1st gen) supports the following classes of Bluetooth devices:</span></span>

- <span data-ttu-id="07324-112">Мышь</span><span class="sxs-lookup"><span data-stu-id="07324-112">Mouse</span></span>
- <span data-ttu-id="07324-113">Клавиатура</span><span class="sxs-lookup"><span data-stu-id="07324-113">Keyboard</span></span>
- [<span data-ttu-id="07324-114">Пульт HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="07324-114">HoloLens (1st gen) clicker</span></span>](https://docs.microsoft.com/hololens/hololens1-clicker)

> [!NOTE]
> <span data-ttu-id="07324-115">Другие устройства с Bluetooth, такие как динамики, гарнитуры, смартфоны и игровые планшеты, могут быть перечислены в параметрах HoloLens как доступные.</span><span class="sxs-lookup"><span data-stu-id="07324-115">Other types of Bluetooth devices, such as speakers, headsets, smartphones, and game pads, may be listed as available in HoloLens settings.</span></span> <span data-ttu-id="07324-116">Однако в HoloLens (1-го поколения ) такие устройства не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="07324-116">However, these devices aren't supported on HoloLens (1st gen).</span></span> <span data-ttu-id="07324-117">Дополнительные сведения см. в статье [В параметрах HoloLens устройства указаны как доступные, но они не работают](hololens-FAQ.md#hololens-settings-lists-devices-as-available-but-the-devices-dont-work).</span><span class="sxs-lookup"><span data-stu-id="07324-117">For more information, see [HoloLens Settings lists devices as available, but the devices don't work](hololens-FAQ.md#hololens-settings-lists-devices-as-available-but-the-devices-dont-work).</span></span>

### <a name="pair-a-bluetooth-keyboard-or-mouse"></a><span data-ttu-id="07324-118">Связывание клавиатуры или мыши с Bluetooth</span><span class="sxs-lookup"><span data-stu-id="07324-118">Pair a Bluetooth keyboard or mouse</span></span>

1. <span data-ttu-id="07324-119">Включите клавиатуру или мышь и сделайте их обнаруживаемыми.</span><span class="sxs-lookup"><span data-stu-id="07324-119">Turn on your keyboard or mouse, and make it discoverable.</span></span> <span data-ttu-id="07324-120">Чтобы узнать, как сделать устройство обнаруживаемым, посмотрите информацию на самом устройстве (или в документации к нему) или посетите веб-сайт его производителя.</span><span class="sxs-lookup"><span data-stu-id="07324-120">To learn how to make the device discoverable, look for information on the device (or its documentation) or visit the manufacturer's website.</span></span>

1. <span data-ttu-id="07324-121">Используйте жест раскрытия ладони (HoloLens (1-го поколения)) или жест запуска (HoloLens 2), чтобы перейти в меню **Пуск**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="07324-121">Use the bloom gesture (HoloLens (1st gen)) or the start gesture (HoloLens 2) to go to **Start**, and then select **Settings**.</span></span>

1. <span data-ttu-id="07324-122">Выберите **Устройства** и проверьте, включен ли Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="07324-122">Select **Devices**, and make sure that Bluetooth is on.</span></span>  

1. <span data-ttu-id="07324-123">Когда появится имя устройства, нажмите **Связать** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="07324-123">When you see the device name, select **Pair**, and then follow the instructions.</span></span>

## <a name="disable-bluetooth"></a><span data-ttu-id="07324-124">Отключение Bluetooth</span><span class="sxs-lookup"><span data-stu-id="07324-124">Disable Bluetooth</span></span>

<span data-ttu-id="07324-125">Эта процедура выключает радиочастотные компоненты адаптера Bluetooth и все функции Bluetooth в Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="07324-125">This procedure turns off the RF components of the Bluetooth radio and disables all Bluetooth functionality on Microsoft HoloLens.</span></span>

1. <span data-ttu-id="07324-126">Используйте жест раскрытия ладони (HoloLens (1-го поколения)) или жест запуска (HoloLens 2), чтобы перейти в меню **Пуск**, а затем выберите **Параметры** > **Устройства**.</span><span class="sxs-lookup"><span data-stu-id="07324-126">Use the bloom gesture (HoloLens (1st gen)) or the start gesture (HoloLens 2) to go to **Start**, and then select **Settings** > **Devices**.</span></span>

1. <span data-ttu-id="07324-127">Переместите ползунок **Bluetooth** в положение**Выключено**.</span><span class="sxs-lookup"><span data-stu-id="07324-127">Move the slider switch for **Bluetooth** to the **Off** position.</span></span>

## <a name="hololens-2-connect-usb-c-devices"></a><span data-ttu-id="07324-128">HoloLens 2: подключение устройств с USB-C</span><span class="sxs-lookup"><span data-stu-id="07324-128">HoloLens 2: Connect USB-C devices</span></span>

<span data-ttu-id="07324-129">HoloLens 2 поддерживает перечисленные ниже классы устройств с USB-C.</span><span class="sxs-lookup"><span data-stu-id="07324-129">HoloLens 2 supports the following classes of USB-C devices:</span></span>

- <span data-ttu-id="07324-130">Запоминающие устройства (например, USB-накопители)</span><span class="sxs-lookup"><span data-stu-id="07324-130">Mass storage devices (such as thumb drives)</span></span>
- <span data-ttu-id="07324-131">Адаптеры Ethernet (включая подключение по сети Ethernet с функцией подзарядки)</span><span class="sxs-lookup"><span data-stu-id="07324-131">Ethernet adapters (including ethernet plus charging)</span></span>
- <span data-ttu-id="07324-132">Цифровые звуковые адаптеры-переходники с USB-C на 3,5 мм</span><span class="sxs-lookup"><span data-stu-id="07324-132">USB-C-to-3.5mm digital audio adapters</span></span>
- <span data-ttu-id="07324-133">Цифровые аудио гарнитуры USB-C (включая адаптеры гарнитур с функцией подзарядки)</span><span class="sxs-lookup"><span data-stu-id="07324-133">USB-C digital audio headsets (including headset adapters plus charging)</span></span>
- <span data-ttu-id="07324-134">Проводная мышь</span><span class="sxs-lookup"><span data-stu-id="07324-134">Wired mouse</span></span>
- <span data-ttu-id="07324-135">Проводная клавиатура</span><span class="sxs-lookup"><span data-stu-id="07324-135">Wired keyboard</span></span>
- <span data-ttu-id="07324-136">Набор концентраторов с функцией подзарядки PD (USB A и подзарядка PD)</span><span class="sxs-lookup"><span data-stu-id="07324-136">Combination PD hubs (USB A plus PD charging)</span></span>

> [!NOTE]
> <span data-ttu-id="07324-137">В ответ на отзывы клиентов мы добавили ограниченную поддержку мобильного соединения с подключением напрямую к HoloLens через USB-C.</span><span class="sxs-lookup"><span data-stu-id="07324-137">In response to customer feedback we have enabled limited support for cellular connectivity tethered directly to the HoloLens via USB-C.</span></span> <span data-ttu-id="07324-138">Подробнее см. в статье [Подключение к мобильной сети и 5G.](hololens-cellular.md)</span><span class="sxs-lookup"><span data-stu-id="07324-138">See [Connect to Cellular and 5G](hololens-cellular.md) for more information.</span></span>

### <a name="usb-c-hubs"></a><span data-ttu-id="07324-139">Концентраторы USB-C</span><span class="sxs-lookup"><span data-stu-id="07324-139">USB-C Hubs</span></span>

<span data-ttu-id="07324-140">Некоторым пользователям может потребоваться подключить несколько устройств одновременно.</span><span class="sxs-lookup"><span data-stu-id="07324-140">Some users may need to connect multiple devices at once.</span></span> <span data-ttu-id="07324-141">Пользователям, которые хотят ознакомиться с предварительной функцией и [использовать микрофон USB-C](hololens-insider.md#usb-c-external-microphone-support) вместе с другим подключенным устройством, подойдут концентраторы USB-C.</span><span class="sxs-lookup"><span data-stu-id="07324-141">For users who would like to preview an Insider feature and [use a USB-C microphone](hololens-insider.md#usb-c-external-microphone-support) along with another connected device, USB-C hubs may fit the customer's need.</span></span> <span data-ttu-id="07324-142">Корпорация Майкрософт не тестировала эти устройства и не может рекомендовать какие-либо конкретные торговые марки.</span><span class="sxs-lookup"><span data-stu-id="07324-142">Microsoft has not tested these devices, nor can we recommend any specific brands.</span></span>

**<span data-ttu-id="07324-143">Требования к концентратору USB-C и подключенным устройствам:</span><span class="sxs-lookup"><span data-stu-id="07324-143">Requirements for USB-C hub and connected devices:</span></span>**

- <span data-ttu-id="07324-144">Подключенные устройства не должны требовать установки драйвера.</span><span class="sxs-lookup"><span data-stu-id="07324-144">Connected devices must not require a driver to be installed.</span></span>
- <span data-ttu-id="07324-145">Общая передаваемая мощность всех подключенных устройств не должна превышать 4,5 Ватт.</span><span class="sxs-lookup"><span data-stu-id="07324-145">The total power draw of all connected devices must be below 4.5 Watts.</span></span>

## <a name="connect-to-miracast"></a><span data-ttu-id="07324-146">Подключение к Miracast</span><span class="sxs-lookup"><span data-stu-id="07324-146">Connect to Miracast</span></span>

<span data-ttu-id="07324-147">Чтобы использовать Miracast, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="07324-147">To use Miracast, follow these steps:</span></span>

1. <span data-ttu-id="07324-148">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="07324-148">Do one of the following:</span></span>  

   - <span data-ttu-id="07324-149">Откройте меню **Пуск** и выберите значок дисплея.</span><span class="sxs-lookup"><span data-stu-id="07324-149">Open the **Start** menu, and select the display icon.</span></span>
   - <span data-ttu-id="07324-150">Произнесите "Подключить", когда вы смотрите на меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="07324-150">Say "Connect" while you gaze at the **Start** menu.</span></span>  

1. <span data-ttu-id="07324-151">В появившемся списке устройств выберите доступное устройство.</span><span class="sxs-lookup"><span data-stu-id="07324-151">On the list of devices that appears, select an available device.</span></span>

1. <span data-ttu-id="07324-152">Завершите связывание устройств, чтобы начать проецирование.</span><span class="sxs-lookup"><span data-stu-id="07324-152">Complete the pairing to begin projecting.</span></span>
