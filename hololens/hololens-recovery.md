---
title: Перезапуск, сброс и восстановление HoloLens
ms.reviewer: Follow along with our basic and advanced instructions for rebooting or resetting your HoloLens 2 device.
description: Использование Advanced Recovery Companion для установки образа в HoloLens 2.
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
ms.openlocfilehash: b5b9568bab5afebe4ac3e9d57645c18837c71cb6
ms.sourcegitcommit: fdae5b561d56d3d4e62da4db15f07bc10249398a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408429"
---
# <a name="restart-reset-or-recover-hololens-2"></a><span data-ttu-id="755be-104">Перезапуск, сброс и восстановление HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="755be-104">Restart, reset, or recover HoloLens 2</span></span>

## <a name="charge-the-device"></a><span data-ttu-id="755be-105">Зарядка устройства</span><span class="sxs-lookup"><span data-stu-id="755be-105">Charge the device</span></span>

<span data-ttu-id="755be-106">Прежде чем приступить к устранению неполадок, по возможности убедитесь, что уровень заряда батареи устройства составляет 20–40%.</span><span class="sxs-lookup"><span data-stu-id="755be-106">Before you start any troubleshooting procedure, make sure that your device is charged to 20 to 40 percent of battery capacity if possible.</span></span> <span data-ttu-id="755be-107">Используйте [зарядное устройство и кабель USB Type-C](https://www.microsoft.com/en-us/p/microsoft-hololens-2-usb-c-charger-cable/8vj21f2z8pk5?rtc=1), поставляемые с устройством HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="755be-107">Use the [charger and the USB Type-C cable](https://www.microsoft.com/en-us/p/microsoft-hololens-2-usb-c-charger-cable/8vj21f2z8pk5?rtc=1) that come with the HoloLens 2 device.</span></span> <span data-ttu-id="755be-108">Блок питания и кабель USB-C-to-C, поставляемые с устройством, являются оптимальным механизмом для зарядки HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="755be-108">The power supply and USB-C-to-C cable that come with the device are the best way to charge your HoloLens 2.</span></span> <span data-ttu-id="755be-109">Зарядное устройство обеспечивает мощность 18Вт (напряжение: 9В, сила тока: 2А).</span><span class="sxs-lookup"><span data-stu-id="755be-109">The charger supplies 18W of power (9V at 2A).</span></span> <span data-ttu-id="755be-110">Используя предоставляемое сетевое зарядное устройство, аккумулятор HoloLens 2 можно полностью зарядить менее чем за 65 минут, когда устройство находится в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="755be-110">Using the wall charger supplied, HoloLens 2 devices can charge the battery to full in less than 65 minutes when the device is in standby.</span></span> <span data-ttu-id="755be-111">Если эти принадлежности недоступны, убедитесь, что имеющееся в наличии зарядное устройство обеспечивает мощность не менее 15Вт.</span><span class="sxs-lookup"><span data-stu-id="755be-111">If those accessories aren't available, make sure the charger that's available can support at least 15W of power.</span></span>

> [!NOTE]
> <span data-ttu-id="755be-112">По возможности не заряжайте устройство через USB-порт ПК, поскольку это медленный способ зарядки.</span><span class="sxs-lookup"><span data-stu-id="755be-112">If possible, avoid using a PC to charge the device over USB, which is slow.</span></span>

<span data-ttu-id="755be-113">Если устройство правильно загружено и запущено, существует три способа проверить уровень заряда батареи.</span><span class="sxs-lookup"><span data-stu-id="755be-113">If the device is correctly booted and running, there are three ways to check the battery charge level:</span></span>

- <span data-ttu-id="755be-114">С помощью главного меню пользовательского интерфейса устройства HoloLens.</span><span class="sxs-lookup"><span data-stu-id="755be-114">From the main menu of the HoloLens device UI.</span></span>
- <span data-ttu-id="755be-115">По светодиодному индикатору, расположенному рядом с кнопкой питания (при заряде 40% должны постоянно гореть как минимум два светодиода).</span><span class="sxs-lookup"><span data-stu-id="755be-115">View the LED close to the power button (for a 40-percent charge, you should see at least two solid LEDS).</span></span>
    - <span data-ttu-id="755be-116">При зарядке устройства включается индикатор батареи для обозначения текущего уровня заряда.</span><span class="sxs-lookup"><span data-stu-id="755be-116">When the device is charging, the battery indicator lights up to indicate the current level of charge.</span></span>  <span data-ttu-id="755be-117">Последний индикатор плавно мигает, обозначая активную зарядку.</span><span class="sxs-lookup"><span data-stu-id="755be-117">The last light will fade in and out to indicate active charging.</span></span>
    - <span data-ttu-id="755be-118">Когда устройство HoloLens включено, индикатор заряда батареи отображает уровень заряда батареи в виде пяти шагов.</span><span class="sxs-lookup"><span data-stu-id="755be-118">When your HoloLens is on, the battery indicator displays the battery level in five increments.</span></span>
    - <span data-ttu-id="755be-119">Если горит только один из пяти индикаторов, уровень заряда батареи меньше 20%.</span><span class="sxs-lookup"><span data-stu-id="755be-119">When only one of the five lights is on, the battery level is below 20 percent.</span></span>
    - <span data-ttu-id="755be-120">При попытке включить устройство при критически низком уровне заряда батареи один индикатор быстро мигнет и погаснет.</span><span class="sxs-lookup"><span data-stu-id="755be-120">If the battery level is critically low and you try to turn on the device, one light will blink briefly, then go out.</span></span>
- <span data-ttu-id="755be-121">На главном компьютере откройте **проводник** и найдите устройство HoloLens2 слева в разделе **Этот компьютер**.</span><span class="sxs-lookup"><span data-stu-id="755be-121">On your host PC, open **File Explorer** and look for your HoloLens 2 device on left side under **This PC**.</span></span> <span data-ttu-id="755be-122">Щелкните на устройстве правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="755be-122">Right-click the device, and select **Properties**.</span></span> <span data-ttu-id="755be-123">В диалоговом окне отобразится уровень заряда батареи.</span><span class="sxs-lookup"><span data-stu-id="755be-123">A dialog box will show the battery charge level.</span></span>

   ![Экран свойств HoloLens2 с информацией об уровне заряда батареи](images/ResetRecovery2.png)

<span data-ttu-id="755be-125">Если устройство при загрузке не может перейти в меню запуска, обратите внимание на вид светодиодного индикатора и перечисление устройств на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="755be-125">If the device can't boot to the startup menu, note the LED appearance and device enumeration on the host PC.</span></span> <span data-ttu-id="755be-126">Затем следуйте указаниям в [руководстве по устранению неполадок](https://docs.microsoft.com/hololens/hololens-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="755be-126">Then follow the [troubleshooting guide](https://docs.microsoft.com/hololens/hololens-troubleshooting).</span></span> <span data-ttu-id="755be-127">Если состояние устройства не соответствует ни одному из состояний, перечисленных в руководстве по устранению неполадок, подключите устройство к источнику питания (не к главному компьютеру) и выполните [аппаратный сброс](hololens-recovery.md#hard-reset-procedure).</span><span class="sxs-lookup"><span data-stu-id="755be-127">If the state of the device doesn't match any of the states listed in the troubleshooting guide, preform the [hard reset procedure](hololens-recovery.md#hard-reset-procedure) with the device connected to the power supply, not to your host PC.</span></span> <span data-ttu-id="755be-128">Подождите не менее часа, чтобы устройство зарядилось.</span><span class="sxs-lookup"><span data-stu-id="755be-128">Wait at least one hour for the device to charge.</span></span>

## <a name="reset-the-device"></a><span data-ttu-id="755be-129">Сброс устройства</span><span class="sxs-lookup"><span data-stu-id="755be-129">Reset the device</span></span>

<span data-ttu-id="755be-130">При определенных обстоятельствах, возможно, вам придется сбросить устройство вручную без использования программного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="755be-130">Under certain circumstances, you may have to manually reset the device without using the software UI.</span></span>

### <a name="standard-procedure"></a><span data-ttu-id="755be-131">Стандартная процедура</span><span class="sxs-lookup"><span data-stu-id="755be-131">Standard procedure</span></span>

1. <span data-ttu-id="755be-132">Отключите устройство от источника питания или главного компьютера, отсоединив кабель USB Type-C.</span><span class="sxs-lookup"><span data-stu-id="755be-132">Unplug the Type-C cable to disconnect the device from the power supply or the host PC.</span></span>

2. <span data-ttu-id="755be-133">Нажмите и удерживайте **кнопку питания** в течение 15секунд.</span><span class="sxs-lookup"><span data-stu-id="755be-133">Press and hold the **power** button for 15 seconds.</span></span> <span data-ttu-id="755be-134">Все светодиодные индикаторы должны быть выключены.</span><span class="sxs-lookup"><span data-stu-id="755be-134">All LEDs should be off.</span></span>

3. <span data-ttu-id="755be-135">Подождите 2–3секунды, а затем нажмите **кнопку питания**.</span><span class="sxs-lookup"><span data-stu-id="755be-135">Wait 2-3 seconds, and then short-press the **power** button.</span></span> <span data-ttu-id="755be-136">Загорятся светодиоды, расположенные рядом с кнопкой питания, и начнется запуск устройства.</span><span class="sxs-lookup"><span data-stu-id="755be-136">The LEDs close to the power button will light up, and the device will begin to start up.</span></span>

4. <span data-ttu-id="755be-137">Подключите устройство к главному компьютеру и откройте диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="755be-137">Connect the device to the host PC, and then open Device Manager.</span></span> <span data-ttu-id="755be-138">(в Windows10 нажмите клавишу **Windows**+**Х** и выберите пункт **Диспетчер устройств**). Убедитесь, что устройство правильно указано в виде *Microsoft HoloLens*, как показано на изображении ниже.</span><span class="sxs-lookup"><span data-stu-id="755be-138">(For Windows 10, press the **Windows** key and then the **X** key, and then select **Device Manager**.) Make sure the device enumerates correctly as *Microsoft HoloLens* as shown in the following image:</span></span>

   ![Диспетчер устройства HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLens_DeviceManager.png)

### <a name="hard-reset-procedure"></a><span data-ttu-id="755be-140">Процедура аппаратного сброса</span><span class="sxs-lookup"><span data-stu-id="755be-140">Hard-reset procedure</span></span>

<span data-ttu-id="755be-141">Если стандартная процедура сброса не сработала, выполните аппаратный сброс следующим образом.</span><span class="sxs-lookup"><span data-stu-id="755be-141">If the standard reset procedure didn't work, use the hard-reset procedure:</span></span>

1. <span data-ttu-id="755be-142">Отключите устройство от источника питания или главного компьютера, отсоединив кабель USB Type-C.</span><span class="sxs-lookup"><span data-stu-id="755be-142">Unplug the Type-C cable to disconnect the device from the power supply or the host PC.</span></span>

2. <span data-ttu-id="755be-143">Удерживайте нажатыми **кнопку уменьшения громкости** + **кнопку питания** в течение 15секунд.</span><span class="sxs-lookup"><span data-stu-id="755be-143">Hold down the **volume down** + **power** buttons for 15 seconds.</span></span> <span data-ttu-id="755be-144">Устройство автоматически перезапустится.</span><span class="sxs-lookup"><span data-stu-id="755be-144">The device will automatically restart.</span></span>

4. <span data-ttu-id="755be-145">Подключите устройство к главному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="755be-145">Connect the device to the host PC.</span></span>
5. <span data-ttu-id="755be-146">Откройте диспетчер устройств (в Windows10 нажмите клавишу **Windows**+**X** и выберите пункт **Диспетчер устройств**).</span><span class="sxs-lookup"><span data-stu-id="755be-146">Open Device Manager (for Windows 10 press the **Windows** key and then the **X** key, and then select **Device Manager**).</span></span> <span data-ttu-id="755be-147">Убедитесь, что устройство правильно указано в виде *Microsoft HoloLens*, как показано на изображении ниже.</span><span class="sxs-lookup"><span data-stu-id="755be-147">Make sure the device enumerates correctly as *Microsoft HoloLens* as shown in the following image:</span></span>

   ![Диспетчер устройства HoloLens 2 MicrosoftHoloLensRecovery 2](images/MicrosoftHoloLens_DeviceManager.png)

## <a name="clean-reflash-the-device"></a><span data-ttu-id="755be-149">Установка чистого образа на устройство</span><span class="sxs-lookup"><span data-stu-id="755be-149">Clean-reflash the device</span></span>

<span data-ttu-id="755be-150">В чрезвычайных ситуациях, возможно, вам придется установить чистый образ HoloLens2.</span><span class="sxs-lookup"><span data-stu-id="755be-150">In extraordinary situations, you may have to "clean-flash" the HoloLens 2.</span></span> <span data-ttu-id="755be-151">Обратите внимание, что установка чистого образа не повлияет на следующие проблемы:</span><span class="sxs-lookup"><span data-stu-id="755be-151">Please note that clean-reflash isn’t expected to affect the following issues:</span></span>
- [<span data-ttu-id="755be-152">Однородность цветов дисплея</span><span class="sxs-lookup"><span data-stu-id="755be-152">Display color uniformity</span></span>](hololens2-display.md)
- <span data-ttu-id="755be-153">Загрузка со звуком, но без вывода на экран</span><span class="sxs-lookup"><span data-stu-id="755be-153">Booting with sound but no display output</span></span>
- [<span data-ttu-id="755be-154">Мигания светоиндикатора 1-3-5</span><span class="sxs-lookup"><span data-stu-id="755be-154">1-3-5-LED pattern</span></span>](hololens2-setup.md#lights-to-indicate-problems)
- [<span data-ttu-id="755be-155">Перегрев</span><span class="sxs-lookup"><span data-stu-id="755be-155">Overheating</span></span>](hololens-environment-considerations.md#temperature-and-regulatory-information) 
- <span data-ttu-id="755be-156">Сбои ОС (отличающиеся от сбоев приложений)</span><span class="sxs-lookup"><span data-stu-id="755be-156">OS crashes (which are distinct from application crashes)</span></span>

<span data-ttu-id="755be-157">Переустановить образ устройства можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="755be-157">There are two ways to reflash the device.</span></span> <span data-ttu-id="755be-158">В обоих случаях сначала необходимо установить [приложение Advanced Recovery Companion из Магазина Windows](https://www.microsoft.com/store/productId/9P74Z35SFRS8).</span><span class="sxs-lookup"><span data-stu-id="755be-158">For both, you must first [install Advanced Recovery Companion from the Windows Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8).</span></span>

>[!WARNING]
><span data-ttu-id="755be-159">При переустановке образа на устройство удаляются все личные данные, приложения и параметры, в том числе сведения о сбросе доверенного платформенного модуля (TPM).</span><span class="sxs-lookup"><span data-stu-id="755be-159">If you reflash your device, all your personal data, apps, and settings will be erased, including TPM-reset information.</span></span>

<span data-ttu-id="755be-160">По умолчанию приложение Advanced Recovery Companion настроено на скачивание сборки выпуска с новейшими функциями. Сведения о выпуске новейших функций см. в [заметках о выпуске](hololens-release-notes.md#).</span><span class="sxs-lookup"><span data-stu-id="755be-160">By default, Advanced Recovery Companion is set to download the most recent feature release build, check here to read our [Release notes](hololens-release-notes.md#) to learn about the latest feature release.</span></span> <span data-ttu-id="755be-161">Чтобы получить новейшую версию пакета HoloLens2 Full Flash Update (FFU) для установки образа на устройство с помощью Advanced Recovery Companion, щелкните [здесь](https://aka.ms/hololens2download) для скачивания новейшего ежемесячного образа HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="755be-161">To get the latest HoloLens 2 Full Flash Update (FFU) package to reflash your device via Advanced Recovery Companion, [click here to download the latest monthly HoloLens 2 image](https://aka.ms/hololens2download).</span></span> <span data-ttu-id="755be-162">Данная версия представляет собой новейшую общедоступную сборку.</span><span class="sxs-lookup"><span data-stu-id="755be-162">This version is the latest generally available build.</span></span>

<span data-ttu-id="755be-163">Прежде чем начать переустановку образа, установите и запустите приложение на компьютере с Windows10 и подготовьте его к обнаружению устройства.</span><span class="sxs-lookup"><span data-stu-id="755be-163">Before you start the reflash procedure, make sure the app is installed and running on your Windows 10 PC and ready to detect the device.</span></span> <span data-ttu-id="755be-164">Кроме того, убедитесь, что с HoloLens взимается как минимум 40 %.</span><span class="sxs-lookup"><span data-stu-id="755be-164">Also ensure that your HoloLens is charged to a minimum of 40%.</span></span>

![Снимок экрана установки чистого образа HoloLens2](images/ARC1.png)

### <a name="normal-procedure"></a><span data-ttu-id="755be-166">Нормальная процедура</span><span class="sxs-lookup"><span data-stu-id="755be-166">Normal procedure</span></span>

1. <span data-ttu-id="755be-167">Подключите работающее устройство HoloLens к компьютеру с Windows10, на котором предварительно было открыто приложение Advanced Recovery Companion.</span><span class="sxs-lookup"><span data-stu-id="755be-167">While the HoloLens device is running, connect it to the Windows 10 PC where you previously opened the Advanced Recovery Companion app.</span></span>
 
   <span data-ttu-id="755be-168">Устройство будет обнаружено автоматически, а пользовательский интерфейс приложения Advanced Recovery Companion запустит процесс обновления.</span><span class="sxs-lookup"><span data-stu-id="755be-168">The device will be automatically detected, and the Advanced Recovery Companion app UI will start the update process:</span></span>

   ![Первоначальный экран установки чистого образа HoloLens2](images/ARC2.png)

3. <span data-ttu-id="755be-170">Выберите устройство HoloLens2 в пользовательском интерфейсе приложения Advanced Recovery Companion и следуйте инструкциям, чтобы завершить установку образа.</span><span class="sxs-lookup"><span data-stu-id="755be-170">Select the HoloLens 2 device in the Advanced Recovery Companion app UI, and follow the instructions to complete the reflash.</span></span>

### <a name="manual-procedure"></a><span data-ttu-id="755be-171">Ручная процедура</span><span class="sxs-lookup"><span data-stu-id="755be-171">Manual procedure</span></span>

<span data-ttu-id="755be-172">Если устройство HoloLens2 запускается неправильно, возможно, вам придется перевести его в режим восстановления следующим образом.</span><span class="sxs-lookup"><span data-stu-id="755be-172">If the HoloLens 2 doesn't start correctly, you may need to put the device into Recovery mode:</span></span>

1. <span data-ttu-id="755be-173">Отключите устройство от источника питания или главного компьютера, отсоединив кабель USB Type-C.</span><span class="sxs-lookup"><span data-stu-id="755be-173">Unplug the Type-C cable to disconnect the device from the power supply or the host PC.</span></span>

2. <span data-ttu-id="755be-174">Нажмите и удерживайте **кнопку питания** в течение 15секунд.</span><span class="sxs-lookup"><span data-stu-id="755be-174">Press and hold the **power** button for 15 seconds.</span></span> <span data-ttu-id="755be-175">Все светодиодные индикаторы должны быть выключены.</span><span class="sxs-lookup"><span data-stu-id="755be-175">All LEDs should turn off.</span></span>

3. <span data-ttu-id="755be-176">Нажав **кнопку увеличения громкости**, нажмите и отпустите **кнопку питания**, чтобы запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="755be-176">While pressing the **volume up** button, press and release the **power** button to start the device.</span></span> <span data-ttu-id="755be-177">Подождите 15секунд, а затем отпустите **кнопку увеличения громкости**.</span><span class="sxs-lookup"><span data-stu-id="755be-177">Wait 15 seconds, and then release the **volume up** button.</span></span> <span data-ttu-id="755be-178">Загорится только средний из пяти светодиодов.</span><span class="sxs-lookup"><span data-stu-id="755be-178">Only the middle LED of the five LEDs will light up.</span></span>

4. <span data-ttu-id="755be-179">Подключите устройство к главному компьютеру и откройте диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="755be-179">Connect the device to the host PC, and open Device Manager.</span></span> <span data-ttu-id="755be-180">(в Windows10 нажмите клавишу **Windows**+**Х** и выберите пункт **Диспетчер устройств**). Убедитесь, что устройство правильно указано в виде Microsoft HoloLens, как показано на изображении ниже.</span><span class="sxs-lookup"><span data-stu-id="755be-180">(For Windows 10 press the **Windows** key, and then the **X** key, and then select **Device Manager**.) Make sure the device enumerates correctly as Microsoft HoloLens as shown in the following image:</span></span>

   ![HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLensRecovery.png)

   <span data-ttu-id="755be-182">Устройство будет обнаружено автоматически, а пользовательский интерфейс приложения Advanced Recovery Companion запустит процесс обновления.</span><span class="sxs-lookup"><span data-stu-id="755be-182">The device will be automatically detected, and the Advanced Recovery Companion app UI will start the update process:</span></span>

   ![Экран установки чистого образа HoloLens2](images/ARC2.png)

6. <span data-ttu-id="755be-184">Выберите устройство HoloLens2 в пользовательском интерфейсе приложения Advanced Recovery Companion и следуйте инструкциям, чтобы завершить установку образа.</span><span class="sxs-lookup"><span data-stu-id="755be-184">Select the HoloLens 2 device in the Advanced Recovery Companion app UI, and then follow the instructions to complete the reflash.</span></span>

## <a name="download-arc-without-using-the-app-store"></a><span data-ttu-id="755be-185">Скачивание ARC без использования магазина приложений</span><span class="sxs-lookup"><span data-stu-id="755be-185">Download ARC without using the app store</span></span>

<span data-ttu-id="755be-186">Если ИТ-среда не позволяет использовать Магазин Windows или ограничивает доступ к розничному магазину, ИТ-администратор может предоставить доступ к этому приложению, применив "автономный" способ развертывания.</span><span class="sxs-lookup"><span data-stu-id="755be-186">If the IT environment prevents the use of the Windows Store app or limits access to the retail store, the IT administrator can make this app available through an "offline" deployment path.</span></span>

 >[!NOTE]
 > - <span data-ttu-id="755be-187">ИТ-администраторы также могут распространять это приложение с помощью System Center Configuration Manager (SCCM) или Intune.</span><span class="sxs-lookup"><span data-stu-id="755be-187">IT administrators can also distribute this app through System Center Configuration Manager (SCCM) or Intune.</span></span>
 > - <span data-ttu-id="755be-188">Данное руководство посвящено Advanced Recovery Companion, но описанную процедуру можно использовать и для других "автономных" приложений.</span><span class="sxs-lookup"><span data-stu-id="755be-188">This guide focuses on Advanced Recovery Companion, but the process can also be used for other "offline" apps.</span></span>

<span data-ttu-id="755be-189">Указанный способ развертывания описан ниже.</span><span class="sxs-lookup"><span data-stu-id="755be-189">Follow these steps to enable the deployment path:</span></span>
1. <span data-ttu-id="755be-190">Перейдите на веб-сайт [Microsoft Store для бизнеса](https://businessstore.microsoft.com) и выполните вход с помощью удостоверения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="755be-190">Go to the [Microsoft Store for Business](https://businessstore.microsoft.com) and sign in using an Azure Active Directory identity.</span></span>

1. <span data-ttu-id="755be-191">Перейдите в меню **Управление– Параметры**.</span><span class="sxs-lookup"><span data-stu-id="755be-191">Go to **Manage – Settings**.</span></span> <span data-ttu-id="755be-192">В разделе **Покупки** включите параметр **Показать автономные приложения**.</span><span class="sxs-lookup"><span data-stu-id="755be-192">Turn on **Show offline apps** under **Shopping experience**.</span></span>
1. <span data-ttu-id="755be-193">Перейдите в раздел **Купить для моей группы** и найдите приложение [**_Advanced Recovery Companion_**](https://businessstore.microsoft.com/store/details/advanced-recovery-companion/9P74Z35SFRS8).</span><span class="sxs-lookup"><span data-stu-id="755be-193">Go to **shop for my group**, and search for [**_Advanced Recovery Companion_**](https://businessstore.microsoft.com/store/details/advanced-recovery-companion/9P74Z35SFRS8).</span></span>
1. <span data-ttu-id="755be-194">Измените **Тип лицензии** на **_автономное использование_* и щелкните _* Управление\*\*.</span><span class="sxs-lookup"><span data-stu-id="755be-194">Change the **License Type** to \**_offline_*_, and select _\* Manage\*\*.</span></span>
1. <span data-ttu-id="755be-195">В разделе **Скачивание пакета для автономного использования** нажмите вторую синюю кнопку **Скачать**.</span><span class="sxs-lookup"><span data-stu-id="755be-195">Under **Download the package for offline use**, select the second blue **Download** button.</span></span> <span data-ttu-id="755be-196">Убедитесь, что файл имеет расширение *.appxbundle*.</span><span class="sxs-lookup"><span data-stu-id="755be-196">Make sure that the file extension is *.appxbundle*.</span></span>

    - <span data-ttu-id="755be-197">Если на этом этапе у компьютера есть доступ к Интернету, дважды щелкните пакет, чтобы установить приложение.</span><span class="sxs-lookup"><span data-stu-id="755be-197">At this stage, if the Desktop PC has internet access, double-click the package to install the app.</span></span>

    - <span data-ttu-id="755be-198">Если на целевом компьютере нет подключения к Интернету, выполните следующее.</span><span class="sxs-lookup"><span data-stu-id="755be-198">If the destination PC has no internet connectivity, follow these steps:</span></span>
       1. <span data-ttu-id="755be-199">Выберите незакодированную лицензию и нажмите **Создать лицензию**.</span><span class="sxs-lookup"><span data-stu-id="755be-199">Select the unencoded license, and then select **Generate license**.</span></span>
       2. <span data-ttu-id="755be-200">В разделе **Необходимые платформы** нажмите **Скачать**.</span><span class="sxs-lookup"><span data-stu-id="755be-200">Under **Required Frameworks**, select **Download**.</span></span>
       3. <span data-ttu-id="755be-201">Используйте DISM, чтобы применить пакет с зависимостью и лицензией.</span><span class="sxs-lookup"><span data-stu-id="755be-201">Use DISM to apply the package with the dependency and license.</span></span> <span data-ttu-id="755be-202">В командной строке администратора выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="755be-202">From an administrator command prompt, run the following command:</span></span>

          ```console
          C:\WINDOWS\system32>dism /online /Add-ProvisionedAppxPackage /PackagePath:"C:\ARCoffline\Microsoft.AdvancedRecoveryCompanion_1.19050.1301.0_neutral_~_8wekyb3d8bbwe.appxbundle" /DependencyPackagePath:"C:\ARCoffline\Microsoft.VCLibs.140.00.UWPDesktop_14.0.27629.0_x86__8wekyb3d8bbwe.appx" /LicensePath:"C:\ARCoffline\Microsoft.AdvancedRecoveryCompanion_8wekyb3d8bbwe_f72ce112-dd2e-d771-8827-9cbcbf89f8b5.xml" /Region:all
          ```
            > [!NOTE]
            > <span data-ttu-id="755be-203">Номер версии в этом примере кода может не соответствовать текущей доступной версии.</span><span class="sxs-lookup"><span data-stu-id="755be-203">The version number in this code example may not match the currently available version.</span></span> <span data-ttu-id="755be-204">Вы также можете выбрать место для скачивания, отличающееся от указанного в данном примере.</span><span class="sxs-lookup"><span data-stu-id="755be-204">You may have also chosen a different download location than in the example.</span></span> <span data-ttu-id="755be-205">При необходимости внесите в команду соответствующие изменения.</span><span class="sxs-lookup"><span data-stu-id="755be-205">Make any changes to the command as needed.</span></span>

> [!TIP]
> <span data-ttu-id="755be-206">Если вы планируете использовать Advanced Recovery Companion для установки FFU в автономном режиме, рекомендуется скачать устанавливаемый образ.</span><span class="sxs-lookup"><span data-stu-id="755be-206">When you plan to use Advanced Recovery Companion to install an FFU offline, it may be useful to download your flash image.</span></span> <span data-ttu-id="755be-207">[**Текущий образ для HoloLens2**](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="755be-207">[**Download the current image for HoloLens 2**](https://aka.ms/hololens2download).</span></span>

<span data-ttu-id="755be-208">Другие ресурсы:</span><span class="sxs-lookup"><span data-stu-id="755be-208">Other resources:</span></span>
- [<span data-ttu-id="755be-209">Распространение автономных приложений</span><span class="sxs-lookup"><span data-stu-id="755be-209">Distribute offline apps</span></span>](https://docs.microsoft.com/microsoft-store/distribute-offline-apps) 
- [<span data-ttu-id="755be-210">Параметры командной строки для пакета приложения DISM (.appx или .appxbundle)</span><span class="sxs-lookup"><span data-stu-id="755be-210">DISM app package (.appx or .appxbundle) servicing command-line options</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options)
