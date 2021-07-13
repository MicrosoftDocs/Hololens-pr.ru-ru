---
title: Перезапуск, сброс настроек и восстановление HoloLens
ms.reviewer: Follow along with our basic and advanced instructions for rebooting or resetting your HoloLens 2 device.
description: Сведения о том, как использовать Advanced Recovery Companion для установки образа на HoloLens 2.
keywords: инструкции, перезагрузка, сброс, восстановление, аппаратный сброс, программный сброс, включение и выключение питания, HoloLens, завершение работы, arc, advanced recovery companion
ms.prod: hololens
ms.sitesec: library
author: mattzmsft
ms.author: mazeller
ms.date: 04/27/2020
ms.custom:
- CI 111456
- CSSTroubleshooting
ms.topic: article
ms.localizationpriority: high
manager: jarrettr
appliesto:
- HoloLens 2
ms.openlocfilehash: be33eb5d06ee7d63f1f598792ff75605b0eb4424
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923641"
---
# <a name="restart-reset-or-recover-hololens-2"></a><span data-ttu-id="058ca-104">Перезапуск, сброс и восстановление HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="058ca-104">Restart, reset, or recover HoloLens 2</span></span>

>[!IMPORTANT]
> <span data-ttu-id="058ca-105">Прежде чем приступить к устранению неполадок, по возможности убедитесь, что уровень заряда аккумулятора устройства составляет **20–40 %** .</span><span class="sxs-lookup"><span data-stu-id="058ca-105">Before you start any troubleshooting procedure, make sure that your device is charged to **20 to 40 percent** of battery capacity, if possible.</span></span> <span data-ttu-id="058ca-106">[Индикаторы аккумулятора](hololens2-setup.md#lights-that-indicate-the-battery-level), расположенные под кнопкой питания, позволяют быстро проверить заряд аккумулятора без входа в устройство.</span><span class="sxs-lookup"><span data-stu-id="058ca-106">The [battery indicator lights](hololens2-setup.md#lights-that-indicate-the-battery-level) located under the power button are a quick way to verify the battery capacity without logging into the device.</span></span>

<span data-ttu-id="058ca-107">Используйте [зарядку и кабель USB Type-C](https://www.microsoft.com/en-us/p/microsoft-hololens-2-usb-c-charger-cable/8vj21f2z8pk5?rtc=1), которые поставляются с HoloLens 2, так как это оптимальный способ для зарядки устройства.</span><span class="sxs-lookup"><span data-stu-id="058ca-107">Use the [charger and the USB Type-C cable](https://www.microsoft.com/en-us/p/microsoft-hololens-2-usb-c-charger-cable/8vj21f2z8pk5?rtc=1) that came with the HoloLens 2 as that is the best way to charge your device.</span></span> <span data-ttu-id="058ca-108">Это зарядное устройство обеспечивает мощность 18 Вт (напряжение: 9 В, сила тока: 2 А).</span><span class="sxs-lookup"><span data-stu-id="058ca-108">The charger supplies 18W of power (9V at 2A).</span></span> <span data-ttu-id="058ca-109">Используя зарядное устройство из комплекта, аккумулятор HoloLens 2 можно полностью зарядить менее чем за 65 минут, если устройство находится в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="058ca-109">Using the wall charger supplied, HoloLens 2 devices can charge the battery to full in less than 65 minutes when the device is in standby.</span></span> <span data-ttu-id="058ca-110">Если эти принадлежности недоступны, убедитесь, что имеющееся в наличии зарядное устройство обеспечивает мощность не менее 15 Вт.</span><span class="sxs-lookup"><span data-stu-id="058ca-110">If those accessories aren't available, make sure the charger that's available can support at least 15W of power.</span></span>

> [!NOTE]
> <span data-ttu-id="058ca-111">По возможности не заряжайте устройство через USB-порт ПК, так как это медленный способ зарядки.</span><span class="sxs-lookup"><span data-stu-id="058ca-111">If possible, avoid using a PC to charge the device over USB, which is slow.</span></span>

<span data-ttu-id="058ca-112">Если устройство правильно загружено и запущено, существует три способа проверить уровень заряда аккумулятора:</span><span class="sxs-lookup"><span data-stu-id="058ca-112">If the device is correctly booted and running, there are three ways to check the battery charge level:</span></span>

- <span data-ttu-id="058ca-113">С помощью главного меню пользовательского интерфейса устройства HoloLens.</span><span class="sxs-lookup"><span data-stu-id="058ca-113">From the main menu of the HoloLens device UI.</span></span>
- <span data-ttu-id="058ca-114">По светодиодному индикатору, расположенному рядом с кнопкой питания (при заряде 40 % должны постоянно гореть как минимум два светодиода).</span><span class="sxs-lookup"><span data-stu-id="058ca-114">View the LED close to the power button (for a 40-percent charge, you should see at least two solid LEDs).</span></span>
    - <span data-ttu-id="058ca-115">При зарядке устройства включается индикатор аккумулятора для обозначения текущего уровня заряда.</span><span class="sxs-lookup"><span data-stu-id="058ca-115">When the device is charging, the battery indicator lights up to indicate the current level of charge.</span></span>  <span data-ttu-id="058ca-116">Последний индикатор плавно мигает, обозначая активную зарядку.</span><span class="sxs-lookup"><span data-stu-id="058ca-116">The last light will fade in and out to indicate active charging.</span></span>
    - <span data-ttu-id="058ca-117">Когда устройство HoloLens включено, индикатор заряда аккумулятора отображает уровень заряда в виде пяти ступеней.</span><span class="sxs-lookup"><span data-stu-id="058ca-117">When your HoloLens is on, the battery indicator displays the battery level in five increments.</span></span>
    - <span data-ttu-id="058ca-118">Если горит только один из пяти индикаторов, значит уровень заряда ниже 20 %.</span><span class="sxs-lookup"><span data-stu-id="058ca-118">When only one of the five lights is on, the battery level is below 20 percent.</span></span>
    - <span data-ttu-id="058ca-119">Если уровень заряда аккумулятора имеет критически низкий уровень, при попытке включить устройство быстро мигнет и погаснет один индикатор.</span><span class="sxs-lookup"><span data-stu-id="058ca-119">If the battery level is critically low and you try to turn on the device, one light will blink briefly, then go out.</span></span>
- <span data-ttu-id="058ca-120">На главном компьютере откройте **проводник** и найдите свое устройство HoloLens 2 в левой части раздела **Этот компьютер**.</span><span class="sxs-lookup"><span data-stu-id="058ca-120">On your host PC, open **File Explorer** and look for your HoloLens 2 device on left side under **This PC**.</span></span> <span data-ttu-id="058ca-121">Щелкните устройство правой кнопкой мыши и выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="058ca-121">Right-click the device, and select **Properties**.</span></span> <span data-ttu-id="058ca-122">В диалоговом окне отобразится уровень заряда аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="058ca-122">A dialog box will show the battery charge level.</span></span>

   ![Экран свойств HoloLens 2 с информацией об уровне заряда аккумулятора](images/ResetRecovery2.png)

<span data-ttu-id="058ca-124">Если устройство при загрузке не может перейти в меню запуска, обратите внимание на вид светодиодного индикатора и перечисление устройств на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="058ca-124">If the device can't boot to the startup menu, note the LED appearance and device enumeration on the host PC.</span></span> <span data-ttu-id="058ca-125">Затем выполните [инструкции по устранению неполадок](hololens-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="058ca-125">Then follow the [troubleshooting guide](hololens-troubleshooting.md).</span></span> <span data-ttu-id="058ca-126">Если состояние устройства не соответствует ни одному из состояний, приведенных в руководстве по устранению неполадок, подключите устройство к источнику питания (не к главному компьютеру) и выполните [аппаратный сброс](hololens-recovery.md#hard-reset-procedure).</span><span class="sxs-lookup"><span data-stu-id="058ca-126">If the state of the device doesn't match any of the states listed in the troubleshooting guide, perform the [hard reset procedure](hololens-recovery.md#hard-reset-procedure) with the device connected to the power supply, not to your host PC.</span></span> <span data-ttu-id="058ca-127">Подождите не менее часа, чтобы устройство зарядилось.</span><span class="sxs-lookup"><span data-stu-id="058ca-127">Wait at least one hour for the device to charge.</span></span>

## <a name="reset-the-device"></a><span data-ttu-id="058ca-128">Сброс настроек устройства</span><span class="sxs-lookup"><span data-stu-id="058ca-128">Reset the device</span></span>

<span data-ttu-id="058ca-129">При определенных обстоятельствах вам, возможно, придется сбросить настройки устройства вручную без использования программного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="058ca-129">Under certain circumstances, you may have to manually reset the device without using the software UI.</span></span>

### <a name="standard-procedure"></a><span data-ttu-id="058ca-130">Стандартная процедура</span><span class="sxs-lookup"><span data-stu-id="058ca-130">Standard procedure</span></span>

1. <span data-ttu-id="058ca-131">Отключите устройство от источника питания или главного компьютера, отсоединив кабель USB Type-C.</span><span class="sxs-lookup"><span data-stu-id="058ca-131">Unplug the Type-C cable to disconnect the device from the power supply or the host PC.</span></span>

2. <span data-ttu-id="058ca-132">Нажмите и удерживайте кнопку **питания** в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="058ca-132">Press and hold the **power** button for 15 seconds.</span></span> <span data-ttu-id="058ca-133">Все светодиодные индикаторы должны выключиться.</span><span class="sxs-lookup"><span data-stu-id="058ca-133">All LEDs should be off.</span></span>

3. <span data-ttu-id="058ca-134">Подождите 2–3 секунды, а затем нажмите кнопку **питания**.</span><span class="sxs-lookup"><span data-stu-id="058ca-134">Wait 2-3 seconds, and then short-press the **power** button.</span></span> <span data-ttu-id="058ca-135">Загорятся светодиоды, расположенные рядом с кнопкой питания, и начнется запуск устройства.</span><span class="sxs-lookup"><span data-stu-id="058ca-135">The LEDs close to the power button will light up, and the device will begin to start up.</span></span>

4. <span data-ttu-id="058ca-136">Подключите устройство к главному компьютеру и откройте диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="058ca-136">Connect the device to the host PC, and then open Device Manager.</span></span> <span data-ttu-id="058ca-137">(в Windows 10 нажмите клавишу **Windows** и клавишу **X**, а затем выберите **Диспетчер устройств**). Убедитесь, что устройство правильно указано как устройство *Microsoft HoloLens* (см. изображение ниже):</span><span class="sxs-lookup"><span data-stu-id="058ca-137">(For Windows 10, press the **Windows** key and then the **X** key, and then select **Device Manager**.) Make sure the device enumerates correctly as *Microsoft HoloLens* as shown in the following image:</span></span>

   ![Диспетчер устройства HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLens_DeviceManager.png)

### <a name="hard-reset-procedure"></a><span data-ttu-id="058ca-139">Процедура аппаратного сброса</span><span class="sxs-lookup"><span data-stu-id="058ca-139">Hard-reset procedure</span></span>

<span data-ttu-id="058ca-140">Если стандартная процедура сброса не сработала, выполните аппаратный сброс следующим образом:</span><span class="sxs-lookup"><span data-stu-id="058ca-140">If the standard reset procedure didn't work, use the hard-reset procedure:</span></span>

1. <span data-ttu-id="058ca-141">Отключите устройство от источника питания или главного компьютера, отсоединив кабель USB Type-C.</span><span class="sxs-lookup"><span data-stu-id="058ca-141">Unplug the Type-C cable to disconnect the device from the power supply or the host PC.</span></span>

2. <span data-ttu-id="058ca-142">Удерживайте кнопки **Снижение громкости** + **Питание** в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="058ca-142">Hold down the **volume down** + **power** buttons for 15 seconds.</span></span> <span data-ttu-id="058ca-143">Устройство автоматически перезапустится.</span><span class="sxs-lookup"><span data-stu-id="058ca-143">The device will automatically restart.</span></span>

4. <span data-ttu-id="058ca-144">Подключите устройство к главному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="058ca-144">Connect the device to the host PC.</span></span>

5. <span data-ttu-id="058ca-145">Откройте диспетчер устройств (в Windows 10 нажмите клавишу **Windows** и клавишу **X**, а затем выберите **Диспетчер устройств**).</span><span class="sxs-lookup"><span data-stu-id="058ca-145">Open Device Manager (for Windows 10 press the **Windows** key and then the **X** key, and then select **Device Manager**).</span></span> <span data-ttu-id="058ca-146">Убедитесь, что устройство правильно указано как устройство *Microsoft HoloLens* (см. изображение ниже):</span><span class="sxs-lookup"><span data-stu-id="058ca-146">Make sure the device enumerates correctly as *Microsoft HoloLens* as shown in the following image:</span></span>

   ![Диспетчер устройства HoloLens 2 MicrosoftHoloLensRecovery 2](images/MicrosoftHoloLens_DeviceManager.png)

## <a name="clean-reflash-the-device"></a><span data-ttu-id="058ca-148">Чистая установка образа на устройство</span><span class="sxs-lookup"><span data-stu-id="058ca-148">Clean-reflash the device</span></span>

<span data-ttu-id="058ca-149">В чрезвычайных ситуациях вам, возможно, придется выполнить чистую установку образа HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="058ca-149">In extraordinary situations, you may have to "clean-flash" the HoloLens 2.</span></span> <span data-ttu-id="058ca-150">Обратите внимание, что чистая установка образа не решит следующие проблемы:</span><span class="sxs-lookup"><span data-stu-id="058ca-150">Please note that clean-reflash isn’t expected to affect the following issues:</span></span>
- [<span data-ttu-id="058ca-151">Однородность цветов дисплея.</span><span class="sxs-lookup"><span data-stu-id="058ca-151">Display color uniformity</span></span>](hololens2-display.md)
- <span data-ttu-id="058ca-152">Загрузка со звуком, но без вывода на экран.</span><span class="sxs-lookup"><span data-stu-id="058ca-152">Booting with sound but no display output</span></span>
- [<span data-ttu-id="058ca-153">Мигания светодиодных индикаторов 1-3-5.</span><span class="sxs-lookup"><span data-stu-id="058ca-153">1-3-5-LED pattern</span></span>](hololens2-setup.md#lights-to-indicate-problems)
- [<span data-ttu-id="058ca-154">Перегрев</span><span class="sxs-lookup"><span data-stu-id="058ca-154">Overheating</span></span>](hololens-environment-considerations.md#temperature-and-regulatory-information) 
- <span data-ttu-id="058ca-155">Сбои ОС (отличающиеся от сбоев приложений).</span><span class="sxs-lookup"><span data-stu-id="058ca-155">OS crashes (which are distinct from application crashes)</span></span>

<span data-ttu-id="058ca-156">Переустановить образ на устройстве можно двумя способами:</span><span class="sxs-lookup"><span data-stu-id="058ca-156">There are two ways to reflash the device.</span></span> <span data-ttu-id="058ca-157">Для обоих способов сначала необходимо [установить Advanced Recovery Companion из Windows Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8).</span><span class="sxs-lookup"><span data-stu-id="058ca-157">For both, you must first [install Advanced Recovery Companion from the Windows Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8).</span></span>

>[!WARNING]
><span data-ttu-id="058ca-158">При переустановке образа на устройстве удаляются все личные данные, приложения и параметры, в том числе сведения о сбросе доверенного платформенного модуля (TPM).</span><span class="sxs-lookup"><span data-stu-id="058ca-158">If you reflash your device, all your personal data, apps, and settings will be erased, including TPM-reset information.</span></span>

<span data-ttu-id="058ca-159">По умолчанию приложение Advanced Recovery Companion настроено на скачивание последней сборки выпуска с новыми функциями. Сведения о выпуске с новыми функциями см. в [заметка о выпусках](hololens-release-notes.md#).</span><span class="sxs-lookup"><span data-stu-id="058ca-159">By default, Advanced Recovery Companion is set to download the most recent feature release build, check here to read our [Release notes](hololens-release-notes.md#) to learn about the latest feature release.</span></span> <span data-ttu-id="058ca-160">Чтобы получить последнюю версию пакета с полным образом обновления (FFU) для HoloLens 2 для установки образа на устройство с помощью Advanced Recovery Companion, [щелкните здесь и скачайте последний образ HoloLens 2](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="058ca-160">To get the latest HoloLens 2 Full Flash Update (FFU) package to reflash your device via Advanced Recovery Companion, [click here to download the latest monthly HoloLens 2 image](https://aka.ms/hololens2download).</span></span> <span data-ttu-id="058ca-161">Эта версия представляет собой новейшую общедоступную сборку.</span><span class="sxs-lookup"><span data-stu-id="058ca-161">This version is the latest generally available build.</span></span>

<span data-ttu-id="058ca-162">Прежде чем начать переустановку образа, установите и запустите приложение на компьютере с Windows 10 и подготовьте его к обнаружению устройства.</span><span class="sxs-lookup"><span data-stu-id="058ca-162">Before you start the reflash procedure, make sure the app is installed and running on your Windows 10 PC and ready to detect the device.</span></span> <span data-ttu-id="058ca-163">Также убедитесь, что уровень заряда HoloLens составляет не менее 40 %.</span><span class="sxs-lookup"><span data-stu-id="058ca-163">Also ensure that your HoloLens is charged to a minimum of 40%.</span></span>

![Снимок экрана: чистая установка образа HoloLens 2](images/ARC1.png)

### <a name="normal-procedure"></a><span data-ttu-id="058ca-165">Стандартная процедура</span><span class="sxs-lookup"><span data-stu-id="058ca-165">Normal procedure</span></span>

1. <span data-ttu-id="058ca-166">Подключите работающее устройство HoloLens к компьютеру с Windows 10, на котором предварительно было открыто приложение Advanced Recovery Companion.</span><span class="sxs-lookup"><span data-stu-id="058ca-166">While the HoloLens device is running, connect it to the Windows 10 PC where you previously opened the Advanced Recovery Companion app.</span></span>
 
   <span data-ttu-id="058ca-167">Устройство будет обнаружено автоматически, а пользовательский интерфейс приложения Advanced Recovery Companion запустит процесс обновления:</span><span class="sxs-lookup"><span data-stu-id="058ca-167">The device will be automatically detected, and the Advanced Recovery Companion app UI will start the update process:</span></span>

   ![Первоначальный экран чистой установки образа HoloLens 2](images/ARC2.png)

3. <span data-ttu-id="058ca-169">Выберите устройство HoloLens 2 в пользовательском интерфейсе приложения Advanced Recovery Companion и следуйте инструкциям, чтобы выполнить установку образа.</span><span class="sxs-lookup"><span data-stu-id="058ca-169">Select the HoloLens 2 device in the Advanced Recovery Companion app UI, and follow the instructions to complete the reflash.</span></span>

### <a name="manual-procedure"></a><span data-ttu-id="058ca-170">Выполняемая вручную процедура</span><span class="sxs-lookup"><span data-stu-id="058ca-170">Manual procedure</span></span>

<span data-ttu-id="058ca-171">Если HoloLens 2 не запускается корректно или если Advanced Recovery Companion не может обнаружить устройство, возможно, потребуется запустить режим восстановления на устройстве:</span><span class="sxs-lookup"><span data-stu-id="058ca-171">If the HoloLens 2 doesn't start correctly or if Advanced Recovery Companion cannot detect the device, you may need to put the device into recovery mode:</span></span>

1. <span data-ttu-id="058ca-172">Отключите устройство от источника питания или главного компьютера, отсоединив кабель USB Type-C.</span><span class="sxs-lookup"><span data-stu-id="058ca-172">Unplug the Type-C cable to disconnect the device from the power supply or the host PC.</span></span>

2. <span data-ttu-id="058ca-173">Нажмите и удерживайте кнопку **питания** в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="058ca-173">Press and hold the **power** button for 15 seconds.</span></span> <span data-ttu-id="058ca-174">Все светодиодные индикаторы должны выключиться.</span><span class="sxs-lookup"><span data-stu-id="058ca-174">All LEDs should turn off.</span></span>

3. <span data-ttu-id="058ca-175">При нажатой кнопке **увеличения громкости** нажмите и отпустите кнопку **питания**, чтобы запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="058ca-175">While pressing the **volume up** button, press and release the **power** button to start the device.</span></span> <span data-ttu-id="058ca-176">Подождите 15 секунд, а затем отпустите **кнопку увеличения громкости**.</span><span class="sxs-lookup"><span data-stu-id="058ca-176">Wait 15 seconds, and then release the **volume up** button.</span></span> <span data-ttu-id="058ca-177">Загорится только средний из пяти светодиодов.</span><span class="sxs-lookup"><span data-stu-id="058ca-177">Only the middle LED of the five LEDs will light up.</span></span>

4. <span data-ttu-id="058ca-178">Подключите устройство к главному компьютеру и откройте диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="058ca-178">Connect the device to the host PC, and open Device Manager.</span></span> <span data-ttu-id="058ca-179">(в Windows 10 нажмите клавишу **Windows** и клавишу **X**, а затем выберите **Диспетчер устройств**). Убедитесь, что устройство правильно указано как устройство Microsoft HoloLens (см. изображение ниже):</span><span class="sxs-lookup"><span data-stu-id="058ca-179">(For Windows 10 press the **Windows** key, and then the **X** key, and then select **Device Manager**.) Make sure the device enumerates correctly as Microsoft HoloLens as shown in the following image:</span></span>

   ![HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLensRecovery.png)

   <span data-ttu-id="058ca-181">Устройство будет обнаружено автоматически, а пользовательский интерфейс приложения Advanced Recovery Companion запустит процесс обновления:</span><span class="sxs-lookup"><span data-stu-id="058ca-181">The device will be automatically detected, and the Advanced Recovery Companion app UI will start the update process:</span></span>

   ![Экран чистой установки образа HoloLens 2](images/ARC2.png)

6. <span data-ttu-id="058ca-183">Выберите устройство HoloLens 2 в пользовательском интерфейсе приложения Advanced Recovery Companion и следуйте инструкциям, чтобы выполнить установку образа.</span><span class="sxs-lookup"><span data-stu-id="058ca-183">Select the HoloLens 2 device in the Advanced Recovery Companion app UI, and then follow the instructions to complete the reflash.</span></span>

## <a name="troubleshoot-advanced-recovery-companion"></a><span data-ttu-id="058ca-184">Устранение неполадок с Advanced Recovery Companion</span><span class="sxs-lookup"><span data-stu-id="058ca-184">Troubleshoot Advanced Recovery Companion</span></span>

1. <span data-ttu-id="058ca-185">Прежде чем выполнять установку образа, убедитесь, что устройство имеет заряд не менее 40 %.</span><span class="sxs-lookup"><span data-stu-id="058ca-185">Ensure your device is charged to 40% or more before attempting to flash.</span></span>

2. <span data-ttu-id="058ca-186">Убедитесь, что устройство разблокировано.</span><span class="sxs-lookup"><span data-stu-id="058ca-186">Check that your device is unlocked.</span></span>

3. <span data-ttu-id="058ca-187">Если ARC не обнаруживает устройство, убедитесь, что вы можете подключиться к устройству в проводнике на ПК.</span><span class="sxs-lookup"><span data-stu-id="058ca-187">If ARC does not detect your device, ensure that you can connect to your device via File Explorer on your PC.</span></span> <span data-ttu-id="058ca-188">Если вы не можете этого сделать:</span><span class="sxs-lookup"><span data-stu-id="058ca-188">If you cannot;</span></span>

    1.  <span data-ttu-id="058ca-189">Возможно, на устройстве действуют политики USB, которые блокируют такое подключение.</span><span class="sxs-lookup"><span data-stu-id="058ca-189">It is possible that your device may have USB policies that disable that connection.</span></span> <span data-ttu-id="058ca-190">В этом случае попробуйте [выполнить установку образа вручную](hololens-recovery.md#manual-procedure).</span><span class="sxs-lookup"><span data-stu-id="058ca-190">If so, try [Manual Flashing mode](hololens-recovery.md#manual-procedure).</span></span>
    2.  <span data-ttu-id="058ca-191">Если такие политики отсутствуют, попробуйте использовать другой USB-кабель.</span><span class="sxs-lookup"><span data-stu-id="058ca-191">If there are no policies, try a different USB cable.</span></span>

1. <span data-ttu-id="058ca-192">Убедитесь, что на устройстве не [мигают светодиодные индикаторы 1-3-5](hololens2-setup.md#lights-to-indicate-problems).</span><span class="sxs-lookup"><span data-stu-id="058ca-192">Check that your device doesn't display a [1-3-5-LED pattern](hololens2-setup.md#lights-to-indicate-problems).</span></span>

## <a name="download-arc-without-using-the-app-store"></a><span data-ttu-id="058ca-193">Скачивание ARC без использования магазина приложений</span><span class="sxs-lookup"><span data-stu-id="058ca-193">Download ARC without using the app store</span></span>

<span data-ttu-id="058ca-194">Если ИТ-среда не позволяет использовать Windows Store или ограничивает доступ к розничному магазину, ИТ-администратор может предоставить доступ к этому приложению, применив "автономный" способ развертывания.</span><span class="sxs-lookup"><span data-stu-id="058ca-194">If the IT environment prevents the use of the Windows Store app or limits access to the retail store, the IT administrator can make this app available through an "offline" deployment path.</span></span>

 >[!NOTE]
 > - <span data-ttu-id="058ca-195">ИТ-администраторы также могут распространять это приложение с помощью System Center Configuration Manager (SCCM) или Intune.</span><span class="sxs-lookup"><span data-stu-id="058ca-195">IT administrators can also distribute this app through System Center Configuration Manager (SCCM) or Intune.</span></span>
 > - <span data-ttu-id="058ca-196">Это руководство посвящено Advanced Recovery Companion, но описанную процедуру можно использовать и для других "автономных" приложений.</span><span class="sxs-lookup"><span data-stu-id="058ca-196">This guide focuses on Advanced Recovery Companion, but the process can also be used for other "offline" apps.</span></span>

<span data-ttu-id="058ca-197">Выполните следующие шаги, чтобы воспользоваться таким способом развертывания:</span><span class="sxs-lookup"><span data-stu-id="058ca-197">Follow these steps to enable the deployment path:</span></span>

1. <span data-ttu-id="058ca-198">Откройте [Microsoft Store для бизнеса](https://businessstore.microsoft.com) и войдите с помощью удостоверения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="058ca-198">Go to the [Microsoft Store for Business](https://businessstore.microsoft.com) and sign in using an Azure Active Directory identity.</span></span>

1. <span data-ttu-id="058ca-199">Последовательно выберите **Управление — Параметры**.</span><span class="sxs-lookup"><span data-stu-id="058ca-199">Go to **Manage – Settings**.</span></span> <span data-ttu-id="058ca-200">Включите параметр **Show offline apps** (Показывать автономные приложения) в разделе **Shopping experience** (Покупки).</span><span class="sxs-lookup"><span data-stu-id="058ca-200">Turn on **Show offline apps** under **Shopping experience**.</span></span>

1. <span data-ttu-id="058ca-201">Выберите **Купить для моей группы** и выполните поиск по фразе [**_Advanced Recovery Companion_**](https://businessstore.microsoft.com/store/details/advanced-recovery-companion/9P74Z35SFRS8).</span><span class="sxs-lookup"><span data-stu-id="058ca-201">Go to **shop for my group**, and search for [**_Advanced Recovery Companion_**](https://businessstore.microsoft.com/store/details/advanced-recovery-companion/9P74Z35SFRS8).</span></span>

1. <span data-ttu-id="058ca-202">Задайте для параметра **Тип лицензии** значение **_автономно_ *_ и выберите _* Управление**.</span><span class="sxs-lookup"><span data-stu-id="058ca-202">Change the **License Type** to \**_offline_*_, and select _\* Manage\*\*.</span></span>

1. <span data-ttu-id="058ca-203">В разделе **Скачивание пакета для автономного использования** нажмите вторую синюю кнопку **Скачать**.</span><span class="sxs-lookup"><span data-stu-id="058ca-203">Under **Download the package for offline use**, select the second blue **Download** button.</span></span> <span data-ttu-id="058ca-204">Убедитесь, что файл имеет расширение *.appxbundle*.</span><span class="sxs-lookup"><span data-stu-id="058ca-204">Make sure that the file extension is *.appxbundle*.</span></span>

    - <span data-ttu-id="058ca-205">Если на этом этапе у компьютера есть доступ к Интернету, дважды щелкните пакет, чтобы установить приложение.</span><span class="sxs-lookup"><span data-stu-id="058ca-205">At this stage, if the Desktop PC has internet access, double-click the package to install the app.</span></span>

    - <span data-ttu-id="058ca-206">Если на целевом компьютере нет подключения к Интернету, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="058ca-206">If the destination PC has no internet connectivity, follow these steps:</span></span>
       1. <span data-ttu-id="058ca-207">Выберите незашифрованную лицензию и щелкните **Создать лицензию**.</span><span class="sxs-lookup"><span data-stu-id="058ca-207">Select the unencoded license, and then select **Generate license**.</span></span>
       2. <span data-ttu-id="058ca-208">В разделе **Необходимые платформы** выберите **Скачать**.</span><span class="sxs-lookup"><span data-stu-id="058ca-208">Under **Required Frameworks**, select **Download**.</span></span>
       3. <span data-ttu-id="058ca-209">Используйте DISM, чтобы применить пакет с зависимостью и лицензией.</span><span class="sxs-lookup"><span data-stu-id="058ca-209">Use DISM to apply the package with the dependency and license.</span></span> <span data-ttu-id="058ca-210">В командной строке администратора выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="058ca-210">From an administrator command prompt, run the following command:</span></span>

          ```console
          C:\WINDOWS\system32>dism /online /Add-ProvisionedAppxPackage /PackagePath:"C:\ARCoffline\Microsoft.AdvancedRecoveryCompanion_1.19050.1301.0_neutral_~_8wekyb3d8bbwe.appxbundle" /DependencyPackagePath:"C:\ARCoffline\Microsoft.VCLibs.140.00.UWPDesktop_14.0.27629.0_x86__8wekyb3d8bbwe.appx" /LicensePath:"C:\ARCoffline\Microsoft.AdvancedRecoveryCompanion_8wekyb3d8bbwe_f72ce112-dd2e-d771-8827-9cbcbf89f8b5.xml" /Region:all
          ```
          > [!NOTE]
          > <span data-ttu-id="058ca-211">Номер версии в этом примере кода может не соответствовать текущей доступной версии.</span><span class="sxs-lookup"><span data-stu-id="058ca-211">The version number in this code example may not match the currently available version.</span></span> <span data-ttu-id="058ca-212">Вы также можете выбрать место для скачивания, отличающееся от указанного в этом примере.</span><span class="sxs-lookup"><span data-stu-id="058ca-212">You may have also chosen a different download location than in the example.</span></span> <span data-ttu-id="058ca-213">При необходимости внесите в команду соответствующие изменения.</span><span class="sxs-lookup"><span data-stu-id="058ca-213">Make any changes to the command as needed.</span></span>

> [!TIP]
> <span data-ttu-id="058ca-214">Если вы планируете использовать Advanced Recovery Companion для установки FFU в автономном режиме, рекомендуется скачать устанавливаемый образ.</span><span class="sxs-lookup"><span data-stu-id="058ca-214">When you plan to use Advanced Recovery Companion to install an FFU offline, it may be useful to download your flash image.</span></span> <span data-ttu-id="058ca-215">[**Скачать текущий образ для HoloLens 2**](https://aka.ms/hololens2download)</span><span class="sxs-lookup"><span data-stu-id="058ca-215">[**Download the current image for HoloLens 2**](https://aka.ms/hololens2download).</span></span>


<span data-ttu-id="058ca-216">Другие ресурсы:</span><span class="sxs-lookup"><span data-stu-id="058ca-216">Other resources:</span></span>
- [<span data-ttu-id="058ca-217">Распространение автономных приложений</span><span class="sxs-lookup"><span data-stu-id="058ca-217">Distribute offline apps</span></span>](/microsoft-store/distribute-offline-apps) 
- [<span data-ttu-id="058ca-218">Параметры командной строки для пакета приложения DISM (.appx или .appxbundle)</span><span class="sxs-lookup"><span data-stu-id="058ca-218">DISM app package (.appx or .appxbundle) servicing command-line options</span></span>](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options)
