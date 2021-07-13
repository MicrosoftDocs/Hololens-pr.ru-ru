---
title: Подключение к устройствам с Bluetooth и USB-C
description: Сведения о том, как подключать устройства смешанной реальности HoloLens к устройствам Bluetooth, USB-C и другим аксессуарам.
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
ms.openlocfilehash: e02950bf6cb70e381e3bc5850509bc65267759c1
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112924185"
---
# <a name="connect-to-bluetooth-and-usb-c-devices"></a><span data-ttu-id="c1795-103">Подключение к устройствам с Bluetooth и USB-C</span><span class="sxs-lookup"><span data-stu-id="c1795-103">Connect to Bluetooth and USB-C devices</span></span>

## <a name="pair-bluetooth-devices"></a><span data-ttu-id="c1795-104">Связывание устройств Bluetooth</span><span class="sxs-lookup"><span data-stu-id="c1795-104">Pair Bluetooth devices</span></span>

<span data-ttu-id="c1795-105">HoloLens 2 поддерживает следующие классы устройств Bluetooth:</span><span class="sxs-lookup"><span data-stu-id="c1795-105">HoloLens 2 supports the following classes of Bluetooth devices:</span></span>

- <span data-ttu-id="c1795-106">[HID](https://docs.microsoft.com/windows-hardware/drivers/hid/):</span><span class="sxs-lookup"><span data-stu-id="c1795-106">[HID](https://docs.microsoft.com/windows-hardware/drivers/hid/):</span></span>
    - <span data-ttu-id="c1795-107">Мышь</span><span class="sxs-lookup"><span data-stu-id="c1795-107">Mouse</span></span>
    - <span data-ttu-id="c1795-108">Клавиатура</span><span class="sxs-lookup"><span data-stu-id="c1795-108">Keyboard</span></span>
- <span data-ttu-id="c1795-109">Устройства для вывода аудио (A2DP).</span><span class="sxs-lookup"><span data-stu-id="c1795-109">Audio output (A2DP) devices</span></span>

<span data-ttu-id="c1795-110">HoloLens 2 поддерживает следующие API Bluetooth:</span><span class="sxs-lookup"><span data-stu-id="c1795-110">HoloLens 2 supports the following Bluetooth APIs:</span></span>
- <span data-ttu-id="c1795-111">[Сервер](https://docs.microsoft.com/windows/uwp/devices-sensors/gatt-server) и [клиент](https://docs.microsoft.com/windows/uwp/devices-sensors/gatt-client) GATT.</span><span class="sxs-lookup"><span data-stu-id="c1795-111">GATT [Server](https://docs.microsoft.com/windows/uwp/devices-sensors/gatt-server) and [Client](https://docs.microsoft.com/windows/uwp/devices-sensors/gatt-client)</span></span>
- [<span data-ttu-id="c1795-112">RFCOMM</span><span class="sxs-lookup"><span data-stu-id="c1795-112">RFCOMM</span></span>](https://docs.microsoft.com/windows/uwp/devices-sensors/send-or-receive-files-with-rfcomm)
>[!IMPORTANT]
> <span data-ttu-id="c1795-113">Возможно, вам придется установить соответствующие дополнительные приложения из Microsoft Store, чтобы получить возможность работать с устройствами HID и GATT.</span><span class="sxs-lookup"><span data-stu-id="c1795-113">You may have to install corresponding companion apps from Microsoft Store to actually use the HID and GATT devices.</span></span>

<span data-ttu-id="c1795-114">HoloLens (1-го поколения) поддерживает следующие классы устройств с Bluetooth:</span><span class="sxs-lookup"><span data-stu-id="c1795-114">HoloLens (1st gen) supports the following classes of Bluetooth devices:</span></span>

- <span data-ttu-id="c1795-115">Мышь</span><span class="sxs-lookup"><span data-stu-id="c1795-115">Mouse</span></span>
- <span data-ttu-id="c1795-116">Клавиатура</span><span class="sxs-lookup"><span data-stu-id="c1795-116">Keyboard</span></span>
- [<span data-ttu-id="c1795-117">Пульт HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="c1795-117">HoloLens (1st gen) clicker</span></span>](https://docs.microsoft.com/hololens/hololens1-clicker)

> [!NOTE]
> <span data-ttu-id="c1795-118">Другие устройства Bluetooth, такие как динамики, гарнитуры, смартфоны и игровые планшеты, могут быть указаны в параметрах HoloLens как доступные.</span><span class="sxs-lookup"><span data-stu-id="c1795-118">Other types of Bluetooth devices, such as speakers, headsets, smartphones, and game pads, may be listed as available in HoloLens settings.</span></span> <span data-ttu-id="c1795-119">Однако в HoloLens (1-го поколения ) такие устройства не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c1795-119">However, these devices aren't supported on HoloLens (1st gen).</span></span> <span data-ttu-id="c1795-120">Дополнительные сведения см. в разделе [Устройства, указанные как доступные в параметрах, не работают](hololens-troubleshooting.md#devices-listed-as-available-in-settings-dont-work).</span><span class="sxs-lookup"><span data-stu-id="c1795-120">For more information, see [HoloLens Settings lists devices as available, but the devices don't work](hololens-troubleshooting.md#devices-listed-as-available-in-settings-dont-work).</span></span>

### <a name="pair-a-bluetooth-keyboard-or-mouse"></a><span data-ttu-id="c1795-121">Связывание клавиатуры или мыши Bluetooth</span><span class="sxs-lookup"><span data-stu-id="c1795-121">Pair a Bluetooth keyboard or mouse</span></span>

1. <span data-ttu-id="c1795-122">Включите клавиатуру или мышь и включите на них поддержку обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c1795-122">Turn on your keyboard or mouse, and make it discoverable.</span></span> <span data-ttu-id="c1795-123">Чтобы узнать, как включить обнаружение, посмотрите информацию на самом устройстве, в документации к нему или на веб-сайте соответствующего производителя.</span><span class="sxs-lookup"><span data-stu-id="c1795-123">To learn how to make the device discoverable, look for information on the device (or its documentation) or visit the manufacturer's website.</span></span>

1. <span data-ttu-id="c1795-124">Используйте жест раскрытия ладони (HoloLens (1-го поколения)) или жест "Пуск" (HoloLens 2), чтобы перейти в меню **Пуск**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="c1795-124">Use the bloom gesture (HoloLens (1st gen)) or the start gesture (HoloLens 2) to go to **Start**, and then select **Settings**.</span></span>

1. <span data-ttu-id="c1795-125">Выберите **Устройства** и убедитесь, что Bluetooth включен.</span><span class="sxs-lookup"><span data-stu-id="c1795-125">Select **Devices**, and make sure that Bluetooth is on.</span></span>  

1. <span data-ttu-id="c1795-126">Когда появится имя устройства, выберите **Подключить** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="c1795-126">When you see the device name, select **Pair**, and then follow the instructions.</span></span>

## <a name="disable-bluetooth"></a><span data-ttu-id="c1795-127">Отключение Bluetooth</span><span class="sxs-lookup"><span data-stu-id="c1795-127">Disable Bluetooth</span></span>

<span data-ttu-id="c1795-128">Эта процедура выключает радиочастотные компоненты адаптера Bluetooth и отключает все возможности Bluetooth в Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="c1795-128">This procedure turns off the RF components of the Bluetooth radio and disables all Bluetooth functionality on Microsoft HoloLens.</span></span>

1. <span data-ttu-id="c1795-129">Используйте жест раскрытия ладони (HoloLens (1-го поколения)) или жест "Пуск" (HoloLens 2), чтобы перейти в меню **Пуск**, а затем выберите **Параметры** > **Устройства**.</span><span class="sxs-lookup"><span data-stu-id="c1795-129">Use the bloom gesture (HoloLens (1st gen)) or the start gesture (HoloLens 2) to go to **Start**, and then select **Settings** > **Devices**.</span></span>

1. <span data-ttu-id="c1795-130">Переместите ползунок **Bluetooth** в положение **Выкл.**</span><span class="sxs-lookup"><span data-stu-id="c1795-130">Move the slider switch for **Bluetooth** to the **Off** position.</span></span>

## <a name="hololens-2-connect-usb-c-devices"></a><span data-ttu-id="c1795-131">HoloLens 2: подключение устройств через USB-C</span><span class="sxs-lookup"><span data-stu-id="c1795-131">HoloLens 2: Connect USB-C devices</span></span>

<span data-ttu-id="c1795-132">HoloLens 2 поддерживает следующие классы устройств USB-C:</span><span class="sxs-lookup"><span data-stu-id="c1795-132">HoloLens 2 supports the following classes of USB-C devices:</span></span>

- <span data-ttu-id="c1795-133">Запоминающие устройства (например, USB-накопители).</span><span class="sxs-lookup"><span data-stu-id="c1795-133">Mass storage devices (such as thumb drives)</span></span>
- <span data-ttu-id="c1795-134">Адаптеры Ethernet (в том числе Ethernet с функцией подзарядки).</span><span class="sxs-lookup"><span data-stu-id="c1795-134">Ethernet adapters (including ethernet plus charging)</span></span>
- <span data-ttu-id="c1795-135">Цифровые звуковые адаптеры (переходники) с USB-C на 3,5 мм.</span><span class="sxs-lookup"><span data-stu-id="c1795-135">USB-C-to-3.5mm digital audio adapters</span></span>
- <span data-ttu-id="c1795-136">Цифровые аудио гарнитуры USB-C (в том числе с функцией подзарядки).</span><span class="sxs-lookup"><span data-stu-id="c1795-136">USB-C digital audio headsets (including headset adapters plus charging)</span></span>
- <span data-ttu-id="c1795-137">Внешние микрофоны USB-C ([Windows Holographic, версии 21H1](hololens-release-notes.md#windows-holographic-version-21h1) и выше).</span><span class="sxs-lookup"><span data-stu-id="c1795-137">USB-C External Microphones ([Windows Holographic, version 21H1](hololens-release-notes.md#windows-holographic-version-21h1) and higher)</span></span>
- <span data-ttu-id="c1795-138">Проводная мышь.</span><span class="sxs-lookup"><span data-stu-id="c1795-138">Wired mouse</span></span>
- <span data-ttu-id="c1795-139">Проводная клавиатура.</span><span class="sxs-lookup"><span data-stu-id="c1795-139">Wired keyboard</span></span>
- <span data-ttu-id="c1795-140">Набор концентраторов с функцией подзарядки PD (USB A и подзарядка PD).</span><span class="sxs-lookup"><span data-stu-id="c1795-140">Combination PD hubs (USB A plus PD charging)</span></span>


> [!NOTE]
> <span data-ttu-id="c1795-141">В ответ на отзывы клиентов мы добавили ограниченную поддержку мобильного соединения с подключением напрямую к HoloLens через USB-C.</span><span class="sxs-lookup"><span data-stu-id="c1795-141">In response to customer feedback, we have enabled limited support for cellular connectivity tethered directly to the HoloLens via USB-C.</span></span> <span data-ttu-id="c1795-142">Дополнительные сведения см. в статье [Подключение к мобильной сети и 5G](hololens-cellular.md).</span><span class="sxs-lookup"><span data-stu-id="c1795-142">See [Connect to Cellular and 5G](hololens-cellular.md) for more information.</span></span>

### <a name="usb-c-external-microphone-support"></a><span data-ttu-id="c1795-143">Поддержка внешнего микрофона USB-C</span><span class="sxs-lookup"><span data-stu-id="c1795-143">USB-C External Microphone Support</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c1795-144">**Включение микрофона USB не включает его автоматически как устройство ввода.**</span><span class="sxs-lookup"><span data-stu-id="c1795-144">Plugging in **a USB mic will not automatically set it as the input device**.</span></span> <span data-ttu-id="c1795-145">Пользователи быстро привыкают, что включении наушников USB-C приводит к автоматическому переключению аудиовыхода на эти наушники, но для микрофона ОС HoloLens всегда отдает приоритет встроенному устройству.</span><span class="sxs-lookup"><span data-stu-id="c1795-145">When plugging in a set of USB-C headphones, users will observe that the headphone's audio will automatically be redirected to the headphones, but the HoloLens OS prioritizes the internal microphone array above any other input device.</span></span> <span data-ttu-id="c1795-146">**Чтобы переключиться на использование микрофона USB-C, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="c1795-146">**In order to use a USB-C microphone follow the steps below.**</span></span>

> [!NOTE]
> <span data-ttu-id="c1795-147">Внешние микрофоны невозможно использовать в сборках до [Windows Holographic версии 21H1](hololens-release-notes.md#windows-holographic-version-21h1).</span><span class="sxs-lookup"><span data-stu-id="c1795-147">External microphones cannot be used in builds prior to [Windows Holographic, version 21H1](hololens-release-notes.md#windows-holographic-version-21h1) and higher.</span></span> 

<span data-ttu-id="c1795-148">Пользователь может выбрать внешний микрофон, подключенный через USB-C, на панели настроек **Звук**.</span><span class="sxs-lookup"><span data-stu-id="c1795-148">Users can select USB-C connected external microphones using the **Sound** settings panel.</span></span> <span data-ttu-id="c1795-149">Микрофоны USB-C можно использовать для телефонных звонков, записи аудио и т. п.</span><span class="sxs-lookup"><span data-stu-id="c1795-149">USB-C microphones can be used for calling, recording, etc.</span></span>

<span data-ttu-id="c1795-150">Откройте приложение **Параметры** и выберите **Система** > **Звук**.</span><span class="sxs-lookup"><span data-stu-id="c1795-150">Open the **Settings** app and select **System** > **Sound**.</span></span>

![Параметры звука](images/usbc-mic-1.jpg)

> [!IMPORTANT]
> <span data-ttu-id="c1795-152">Чтобы использовать внешние микрофоны для **Remote Assist**, пользователю нужно щелкнуть гиперссылку "Manage sound devices" (Управление звуковыми устройствами).</span><span class="sxs-lookup"><span data-stu-id="c1795-152">To use external microphones with **Remote Assist**, users will need to click the “Manage sound devices” hyperlink.</span></span>
>
> <span data-ttu-id="c1795-153">После этого в раскрывающемся списке нужно выбрать внешний микрофон как устройство **Default** (По умолчанию) или **Communications Default** (По умолчанию для коммуникаций).</span><span class="sxs-lookup"><span data-stu-id="c1795-153">Then use the drop-down to set the external microphone as either **Default** or **Communications Default.**</span></span> <span data-ttu-id="c1795-154">Вариант **Default** (По умолчанию) означает, что внешний микрофон будет использоваться во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="c1795-154">Choosing **Default** means that the external microphone will be used everywhere.</span></span>
>
> <span data-ttu-id="c1795-155">Вариант **Communications Default** (По умолчанию для коммуникаций) означает, что внешний микрофон будет использоваться в Remote Assist и в других приложениях для коммуникации, но для других задач по-прежнему будет использоваться встроенный набор микрофонов HoloLens.</span><span class="sxs-lookup"><span data-stu-id="c1795-155">Choosing **Communications Default** means that the external microphone will be used in Remote Assist and other communications apps, but the HoloLens mic array may still be used for other tasks.</span></span>

![Управление звуковыми устройствами](images/usbc-mic-2.png)

<br>

![Настройка микрофона по умолчанию](images/usbc-mic-3.jpg)

#### <a name="what-about-bluetooth-microphone-support"></a><span data-ttu-id="c1795-158">Какая поддержка предоставляется для микрофона Bluetooth?</span><span class="sxs-lookup"><span data-stu-id="c1795-158">What about Bluetooth microphone support?</span></span>

<span data-ttu-id="c1795-159">К сожалению, микрофоны Bluetooth пока еще не поддерживаются на HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="c1795-159">Unfortunately, Bluetooth microphones are still not currently supported on HoloLens 2.</span></span>

### <a name="usb-c-hubs"></a><span data-ttu-id="c1795-160">Концентраторы USB-C</span><span class="sxs-lookup"><span data-stu-id="c1795-160">USB-C Hubs</span></span>

<span data-ttu-id="c1795-161">Некоторым пользователям может потребоваться подключить несколько устройств одновременно.</span><span class="sxs-lookup"><span data-stu-id="c1795-161">Some users may need to connect multiple devices at once.</span></span> <span data-ttu-id="c1795-162">Например, если нужно использовать [микрофон USB-C](#usb-c-external-microphone-support) одновременно с другим устройством, потребуется концентратор USB-C.</span><span class="sxs-lookup"><span data-stu-id="c1795-162">For users who would like to use a [USB-C microphone](#usb-c-external-microphone-support) along with another connected device, USB-C hubs may fit the customer's need.</span></span> <span data-ttu-id="c1795-163">Корпорация Майкрософт не тестировала эти устройства и не может рекомендовать какие-либо конкретные торговые марки.</span><span class="sxs-lookup"><span data-stu-id="c1795-163">Microsoft has not tested these devices, nor can we recommend any specific brands.</span></span>

<span data-ttu-id="c1795-164">**Требования к концентратору USB-C и подключенным устройствам:**</span><span class="sxs-lookup"><span data-stu-id="c1795-164">**Requirements for USB-C hub and connected devices:**</span></span>

- <span data-ttu-id="c1795-165">Подключенные устройства не должны требовать установки драйвера.</span><span class="sxs-lookup"><span data-stu-id="c1795-165">Connected devices must not require a driver to be installed.</span></span>
- <span data-ttu-id="c1795-166">Общая потребляемая мощность всех подключенных устройств не должна превышать 4,5 Вт.</span><span class="sxs-lookup"><span data-stu-id="c1795-166">The total power draw of all connected devices must be below 4.5 Watts.</span></span>

## <a name="connect-to-miracast"></a><span data-ttu-id="c1795-167">Подключение к Miracast</span><span class="sxs-lookup"><span data-stu-id="c1795-167">Connect to Miracast</span></span>

<span data-ttu-id="c1795-168">Чтобы использовать Miracast, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c1795-168">To use Miracast, follow these steps:</span></span>

1. <span data-ttu-id="c1795-169">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c1795-169">Do one of the following:</span></span>  

   - <span data-ttu-id="c1795-170">Откройте меню **Пуск** и выберите значок **Дисплей**.</span><span class="sxs-lookup"><span data-stu-id="c1795-170">Open the **Start** menu, and select the **Display** icon.</span></span>
   - <span data-ttu-id="c1795-171">Произнесите "Connect" (Подключить), удерживая взгляд на меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="c1795-171">Say "Connect" while you gaze at the **Start** menu.</span></span>  

1. <span data-ttu-id="c1795-172">В появившемся списке устройств выберите любое доступное устройство.</span><span class="sxs-lookup"><span data-stu-id="c1795-172">On the list of devices that appears, select an available device.</span></span>

1. <span data-ttu-id="c1795-173">Завершите связывание устройств, чтобы начать проецирование.</span><span class="sxs-lookup"><span data-stu-id="c1795-173">Complete the pairing to begin projecting.</span></span>
