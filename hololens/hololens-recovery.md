---
title: Перезапуск, сброс и восстановление HoloLens
ms.reviewer: Basic and advanced instructions for rebooting or resetting your HoloLens.
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
ms.openlocfilehash: 9c9dd12b596d8fafdfe575797193f18e7b96919c
ms.sourcegitcommit: 2122490074adb7f63edfc3576441980caa22695f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "10915973"
---
# <span data-ttu-id="41c02-104">Перезапуск, сброс и восстановление HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="41c02-104">Restart, reset, or recover HoloLens 2</span></span>

## <span data-ttu-id="41c02-105">Зарядка устройства</span><span class="sxs-lookup"><span data-stu-id="41c02-105">Charge the device</span></span>

<span data-ttu-id="41c02-106">Прежде чем приступить к устранению неполадок, по возможности убедитесь, что уровень заряда батареи устройства составляет 20–40%.</span><span class="sxs-lookup"><span data-stu-id="41c02-106">Before you start any troubleshooting procedure, make sure that your device is charged to 20 to 40 percent of battery capacity if possible.</span></span> <span data-ttu-id="41c02-107">Используйте зарядное устройство и кабели USB Type-C, поставляемые вместе с устройством HoloLens2.</span><span class="sxs-lookup"><span data-stu-id="41c02-107">Use the charger and the USB Type-C cables that come with the HoloLens2 device.</span></span> <span data-ttu-id="41c02-108">Если эти принадлежности недоступны, убедитесь, что имеющееся в наличии зарядное устройство обеспечивает мощность не менее 15Вт.</span><span class="sxs-lookup"><span data-stu-id="41c02-108">If those accessories aren't available, make sure the charger that's available can support at least 15 W of power.</span></span>

> [!NOTE]
> <span data-ttu-id="41c02-109">По возможности не заряжайте устройство через USB-порт ПК, поскольку это медленный способ зарядки.</span><span class="sxs-lookup"><span data-stu-id="41c02-109">If possible, avoid using a PC to charge the device over USB, which is slow.</span></span>

<span data-ttu-id="41c02-110">Если устройство правильно загружено и запущено, существует три способа проверить уровень заряда батареи.</span><span class="sxs-lookup"><span data-stu-id="41c02-110">If the device is correctly booted and running, there are three ways to check the battery charge level:</span></span>

- <span data-ttu-id="41c02-111">С помощью главного меню пользовательского интерфейса устройства HoloLens.</span><span class="sxs-lookup"><span data-stu-id="41c02-111">From the main menu of the HoloLens device UI.</span></span>
- <span data-ttu-id="41c02-112">По светодиодному индикатору, расположенному рядом с кнопкой питания (при заряде 40% должны постоянно гореть как минимум два светодиода).</span><span class="sxs-lookup"><span data-stu-id="41c02-112">View the LED close to the power button (for a 40-percent charge, you should see at least two solid LEDS).</span></span>
- <span data-ttu-id="41c02-113">На главном компьютере откройте проводник и найдите устройство HoloLens2 слева в разделе **Этот компьютер**.</span><span class="sxs-lookup"><span data-stu-id="41c02-113">On your host PC, open File Explorer and look for your HoloLens 2 device on left side under **This PC**.</span></span> <span data-ttu-id="41c02-114">Щелкните на устройстве правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="41c02-114">Right-click the device, and select **Properties**.</span></span> <span data-ttu-id="41c02-115">В диалоговом окне отобразится уровень заряда батареи.</span><span class="sxs-lookup"><span data-stu-id="41c02-115">A dialog box will show the battery charge level.</span></span>

   ![Экран свойств HoloLens2 с информацией об уровне заряда батареи](images/ResetRecovery2.png)

<span data-ttu-id="41c02-117">Если устройство при загрузке не может перейти в меню запуска, обратите внимание на вид светодиодного индикатора и перечисление устройств на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="41c02-117">If the device can't boot to the startup menu, note the LED appearance and device enumeration on the host PC.</span></span> <span data-ttu-id="41c02-118">Затем следуйте указаниям в [руководстве по устранению неполадок](https://docs.microsoft.com/hololens/hololens-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="41c02-118">Then follow the [troubleshooting guide](https://docs.microsoft.com/hololens/hololens-troubleshooting).</span></span> <span data-ttu-id="41c02-119">Если состояние устройства не соответствует ни одному из состояний, перечисленных в руководстве по устранению неполадок, подключите устройство к источнику питания (не к главному компьютеру) и выполните *аппаратный сброс*.</span><span class="sxs-lookup"><span data-stu-id="41c02-119">If the state of the device doesn't match any of the states listed in the troubleshooting guide, do the *hard reset procedure* with the device connected to the power supply, not to your host PC.</span></span> <span data-ttu-id="41c02-120">Подождите не менее часа, чтобы устройство зарядилось.</span><span class="sxs-lookup"><span data-stu-id="41c02-120">Wait at least one hour for the device to charge.</span></span>

## <span data-ttu-id="41c02-121">Сброс устройства</span><span class="sxs-lookup"><span data-stu-id="41c02-121">Reset the device</span></span>

<span data-ttu-id="41c02-122">При определенных обстоятельствах, возможно, вам придется сбросить устройство вручную без использования программного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="41c02-122">Under certain circumstances, you may have to manually reset the device without using the SW UI.</span></span>

### <span data-ttu-id="41c02-123">Стандартная процедура</span><span class="sxs-lookup"><span data-stu-id="41c02-123">Standard procedure</span></span>
1. <span data-ttu-id="41c02-124">Отключите устройство от источника питания или главного компьютера, отсоединив кабель USB Type-C.</span><span class="sxs-lookup"><span data-stu-id="41c02-124">Unplug the Type-C cable to disconnect the device from the power supply or the host PC.</span></span>

2. <span data-ttu-id="41c02-125">Нажмите и удерживайте **кнопку питания** в течение 15секунд.</span><span class="sxs-lookup"><span data-stu-id="41c02-125">Press and hold the **power** button for 15 seconds.</span></span> <span data-ttu-id="41c02-126">Все светодиодные индикаторы должны быть выключены.</span><span class="sxs-lookup"><span data-stu-id="41c02-126">All LEDs should be off.</span></span>

3. <span data-ttu-id="41c02-127">Подождите 2–3секунды, а затем нажмите **кнопку питания**.</span><span class="sxs-lookup"><span data-stu-id="41c02-127">Wait 2-3 seconds, and then short-press the **power** button.</span></span> <span data-ttu-id="41c02-128">Загорятся светодиоды, расположенные рядом с кнопкой питания, и начнется запуск устройства.</span><span class="sxs-lookup"><span data-stu-id="41c02-128">The LEDs close to the power button will light up, and the device will begin to start up.</span></span>

4. <span data-ttu-id="41c02-129">Подключите устройство к главному компьютеру и откройте диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="41c02-129">Connect the device to the host PC, and then open Device Manager.</span></span> <span data-ttu-id="41c02-130">(в Windows10 нажмите клавишу **Windows**+**Х** и выберите пункт **Диспетчер устройств**). Убедитесь, что устройство правильно указано в виде *Microsoft HoloLens*, как показано на изображении ниже.</span><span class="sxs-lookup"><span data-stu-id="41c02-130">(For Windows 10, press the **Windows** key and then the **X** key, and then select **Device Manager**.) Make sure the device enumerates correctly as *Microsoft HoloLens* as shown in the following image:</span></span>

   ![HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLens_DeviceManager.png)

### <span data-ttu-id="41c02-132">Процедура аппаратного сброса</span><span class="sxs-lookup"><span data-stu-id="41c02-132">Hard-reset procedure</span></span>

<span data-ttu-id="41c02-133">Если стандартная процедура сброса не сработала, выполните аппаратный сброс следующим образом.</span><span class="sxs-lookup"><span data-stu-id="41c02-133">If the standard reset procedure didn't work, use the hard-reset procedure:</span></span>

1. <span data-ttu-id="41c02-134">Отключите устройство от источника питания или главного компьютера, отсоединив кабель USB Type-C.</span><span class="sxs-lookup"><span data-stu-id="41c02-134">Unplug the Type-C cable to disconnect the device from the power supply or the host PC.</span></span>

2. <span data-ttu-id="41c02-135">Удерживайте нажатыми **кнопку уменьшения громкости** + **кнопку питания** в течение 15секунд.</span><span class="sxs-lookup"><span data-stu-id="41c02-135">Hold down the **volume down** + **power** buttons for 15 seconds.</span></span> <span data-ttu-id="41c02-136">Устройство автоматически перезапустится.</span><span class="sxs-lookup"><span data-stu-id="41c02-136">The device will automatically restart.</span></span>

4. <span data-ttu-id="41c02-137">Подключите устройство к главному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="41c02-137">Connect the device to the host PC.</span></span>
5. <span data-ttu-id="41c02-138">Откройте диспетчер устройств (в Windows10 нажмите клавишу **Windows**+**X** и выберите пункт **Диспетчер устройств**).</span><span class="sxs-lookup"><span data-stu-id="41c02-138">Open Device Manager (for Windows 10 press the **Windows** key and then the **X** key, and then select **Device Manager**).</span></span> <span data-ttu-id="41c02-139">Убедитесь, что устройство правильно указано в виде *Microsoft HoloLens*, как показано на изображении ниже.</span><span class="sxs-lookup"><span data-stu-id="41c02-139">Make sure the device enumerates correctly as *Microsoft HoloLens* as shown in the following image:</span></span>

   ![HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLens_DeviceManager.png)

## <span data-ttu-id="41c02-141">Установка чистого образа на устройство</span><span class="sxs-lookup"><span data-stu-id="41c02-141">Clean-reflash the device</span></span>

<span data-ttu-id="41c02-142">В чрезвычайных ситуациях, возможно, вам придется установить чистый образ HoloLens2.</span><span class="sxs-lookup"><span data-stu-id="41c02-142">In extraordinary situations, you may have to "clean-flash" the HoloLens 2.</span></span> <span data-ttu-id="41c02-143">Переустановить образ устройства можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="41c02-143">There are two ways to reflash the device.</span></span> <span data-ttu-id="41c02-144">В обоих случаях сначала необходимо установить [приложение Advanced Recovery Companion из Магазина Windows](https://www.microsoft.com/store/productId/9P74Z35SFRS8).</span><span class="sxs-lookup"><span data-stu-id="41c02-144">For both, you must first install [Advanced Recovery Companion from the Windows Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8).</span></span>

>[!WARNING]
><span data-ttu-id="41c02-145">При переустановке образа на устройство удаляются все личные данные, приложения и параметры, в том числе сведения о сбросе доверенного платформенного модуля (TPM).</span><span class="sxs-lookup"><span data-stu-id="41c02-145">If you reflash your device, all your personal data, apps, and settings will be erased, including TPM-reset information.</span></span>

<span data-ttu-id="41c02-146">В настоящее время приложение Advanced Recovery Companion по умолчанию настроено на скачивание сборки выпуска с новыми функциями для [Windows Holographic 2004](hololens-release-notes.md#windows-holographic-version-2004).</span><span class="sxs-lookup"><span data-stu-id="41c02-146">By default, Advanced Recovery Companion is currently set to download the feature release build for [Windows Holographic 2004](hololens-release-notes.md#windows-holographic-version-2004).</span></span> <span data-ttu-id="41c02-147">Чтобы получить новейшую версию пакета HoloLens2 Full Flash Update (FFU) для установки образа на устройство с помощью Advanced Recovery Companion, [скачайте его здесь](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="41c02-147">To get the latest HoloLens 2 Full Flash Update (FFU) package to reflash your device via Advanced Recovery Companion, [download it here](https://aka.ms/hololens2download).</span></span> <span data-ttu-id="41c02-148">Данная версия представляет собой новейшую общедоступную сборку.</span><span class="sxs-lookup"><span data-stu-id="41c02-148">This version is the latest generally available build.</span></span>

<span data-ttu-id="41c02-149">Прежде чем начать переустановку образа, установите и запустите приложение на компьютере с Windows10 и подготовьте его к обнаружению устройства.</span><span class="sxs-lookup"><span data-stu-id="41c02-149">Before you start the reflash procedure, make sure the app is installed and running on your Windows 10 PC and ready to detect the device.</span></span>

![Установка чистого образа HoloLens2— снимок экрана](images/ARC1.png)

### <span data-ttu-id="41c02-151">Нормальная процедура</span><span class="sxs-lookup"><span data-stu-id="41c02-151">Normal procedure</span></span>

1. <span data-ttu-id="41c02-152">Подключите работающее устройство HoloLens к компьютеру с Windows10, на котором предварительно было открыто приложение Advanced Recovery Companion.</span><span class="sxs-lookup"><span data-stu-id="41c02-152">While the HoloLens device is running, connect it to the Windows 10 PC where you previously opened the Advanced Recovery Companion app.</span></span>
 
   <span data-ttu-id="41c02-153">Устройство будет обнаружено автоматически, а пользовательский интерфейс приложения Advanced Recovery Companion запустит процесс обновления.</span><span class="sxs-lookup"><span data-stu-id="41c02-153">The device will be automatically detected, and the Advanced Recovery Companion app UI will start the update process:</span></span>

   ![Первоначальный экран установки чистого образа HoloLens2](images/ARC2.png)

3. <span data-ttu-id="41c02-155">Выберите устройство HoloLens2 в пользовательском интерфейсе приложения Advanced Recovery Companion и следуйте инструкциям, чтобы завершить установку образа.</span><span class="sxs-lookup"><span data-stu-id="41c02-155">Select the HoloLens 2 device in the Advanced Recovery Companion app UI, and follow the instructions to complete the reflash.</span></span>

### <span data-ttu-id="41c02-156">Ручная процедура</span><span class="sxs-lookup"><span data-stu-id="41c02-156">Manual procedure</span></span>

<span data-ttu-id="41c02-157">Если устройство HoloLens2 запускается неправильно, возможно, вам придется перевести его в режим восстановления следующим образом.</span><span class="sxs-lookup"><span data-stu-id="41c02-157">If the HoloLens 2 doesn't start correctly, you may need to put the device into Recovery mode:</span></span>

1. <span data-ttu-id="41c02-158">Отключите устройство от источника питания или главного компьютера, отсоединив кабель USB Type-C.</span><span class="sxs-lookup"><span data-stu-id="41c02-158">Unplug the Type-C cable to disconnect the device from the power supply or the host PC.</span></span>

2. <span data-ttu-id="41c02-159">Нажмите и удерживайте **кнопку питания** в течение 15секунд.</span><span class="sxs-lookup"><span data-stu-id="41c02-159">Press and hold the **power** button for 15 seconds.</span></span> <span data-ttu-id="41c02-160">Все светодиодные индикаторы должны быть выключены.</span><span class="sxs-lookup"><span data-stu-id="41c02-160">All LEDs should turn off.</span></span>

3. <span data-ttu-id="41c02-161">Нажав **кнопку увеличения громкости**, нажмите и отпустите **кнопку питания**, чтобы запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="41c02-161">While pressing the **volume up** button, press and release the **power** button to start the device.</span></span> <span data-ttu-id="41c02-162">Подождите 15секунд, а затем отпустите **кнопку увеличения громкости**.</span><span class="sxs-lookup"><span data-stu-id="41c02-162">Wait 15 seconds, and then release the **volume up** button.</span></span> <span data-ttu-id="41c02-163">Загорится только средний из пяти светодиодов.</span><span class="sxs-lookup"><span data-stu-id="41c02-163">Only the middle LED of the five LEDs will light up.</span></span>

4. <span data-ttu-id="41c02-164">Подключите устройство к главному компьютеру и откройте диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="41c02-164">Connect the device to the host PC, and open Device Manager.</span></span> <span data-ttu-id="41c02-165">(в Windows10 нажмите клавишу **Windows**+**Х** и выберите пункт **Диспетчер устройств**). Убедитесь, что устройство правильно указано в виде Microsoft HoloLens, как показано на изображении ниже.</span><span class="sxs-lookup"><span data-stu-id="41c02-165">(For Windows 10 press the **Windows** key, and then the **X** key, and then select **Device Manager**.) Make sure the device enumerates correctly as Microsoft HoloLens as shown in the following image:</span></span>

   ![HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLensRecovery.png)

   <span data-ttu-id="41c02-167">Устройство будет обнаружено автоматически, а пользовательский интерфейс приложения Advanced Recovery Companion запустит процесс обновления.</span><span class="sxs-lookup"><span data-stu-id="41c02-167">The device will be automatically detected, and the Advanced Recovery Companion app UI will start the update process:</span></span>

   ![Экран установки чистого образа HoloLens2](images/ARC2.png)

6. <span data-ttu-id="41c02-169">Выберите устройство HoloLens2 в пользовательском интерфейсе приложения Advanced Recovery Companion и следуйте инструкциям, чтобы завершить установку образа.</span><span class="sxs-lookup"><span data-stu-id="41c02-169">Select the HoloLens 2 device in the Advanced Recovery Companion app UI, and then follow the instructions to complete the reflash.</span></span>

## <span data-ttu-id="41c02-170">Скачивание ARC без использования магазина приложений</span><span class="sxs-lookup"><span data-stu-id="41c02-170">Download ARC without using the app store</span></span>

<span data-ttu-id="41c02-171">Если ИТ-среда не позволяет использовать Магазин Windows или ограничивает доступ к розничному магазину, ИТ-администратор может предоставить доступ к этому приложению, применив "автономный" способ развертывания.</span><span class="sxs-lookup"><span data-stu-id="41c02-171">If the IT environment prevents the use of the Windows Store app or limits access to the retail store, the IT administrator can make this app available through an "offline" deployment path.</span></span>

 >[!NOTE] 
 > - <span data-ttu-id="41c02-172">ИТ-администраторы также могут распространять это приложение с помощью System Center Configuration Manager (SCCM) или Intune.</span><span class="sxs-lookup"><span data-stu-id="41c02-172">IT administrators can also distribute this app through System Center Configuration Manager (SCCM) or Intune.</span></span>
 > - <span data-ttu-id="41c02-173">Данное руководство посвящено Advanced Recovery Companion, но описанную процедуру можно использовать и для других "автономных" приложений.</span><span class="sxs-lookup"><span data-stu-id="41c02-173">This guide focuses on Advanced Recovery Companion, but the process can also be used for other "offline" apps.</span></span>

<span data-ttu-id="41c02-174">Указанный способ развертывания описан ниже.</span><span class="sxs-lookup"><span data-stu-id="41c02-174">Follow these steps to enable the deployment path:</span></span>
1. <span data-ttu-id="41c02-175">Перейдите на веб-сайт [Microsoft Store для бизнеса](https://businessstore.microsoft.com) и выполните вход с помощью удостоверения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="41c02-175">Go to the [Microsoft Store for Business](https://businessstore.microsoft.com) and sign in using an Azure Active Directory identity.</span></span>

1. <span data-ttu-id="41c02-176">Перейдите в меню **Управление– Параметры**.</span><span class="sxs-lookup"><span data-stu-id="41c02-176">Go to **Manage – Settings**.</span></span> <span data-ttu-id="41c02-177">В разделе **Покупки** включите параметр **Показать автономные приложения**.</span><span class="sxs-lookup"><span data-stu-id="41c02-177">Turn on **Show offline apps** under **Shopping experience**.</span></span> 
1. <span data-ttu-id="41c02-178">Перейдите в раздел **Купить для моей группы** и найдите приложение [***Advanced Recovery Companion***](https://businessstore.microsoft.com/store/details/advanced-recovery-companion/9P74Z35SFRS8).</span><span class="sxs-lookup"><span data-stu-id="41c02-178">Go to **shop for my group**, and search for [***Advanced Recovery Companion***](https://businessstore.microsoft.com/store/details/advanced-recovery-companion/9P74Z35SFRS8).</span></span>
1. <span data-ttu-id="41c02-179">Измените значение параметра **Тип лицензии** на ***автономная работа*** и нажмите **Управлять**.</span><span class="sxs-lookup"><span data-stu-id="41c02-179">Change the **License Type** to ***offline***, and select **Manage**.</span></span>
1. <span data-ttu-id="41c02-180">В разделе **Скачивание пакета для автономного использования** нажмите вторую синюю кнопку **Скачать**.</span><span class="sxs-lookup"><span data-stu-id="41c02-180">Under **Download the package for offline use**, select the second blue **Download** button.</span></span> <span data-ttu-id="41c02-181">Убедитесь, что файл имеет расширение *.appxbundle*.</span><span class="sxs-lookup"><span data-stu-id="41c02-181">Make sure that the file extension is *.appxbundle*.</span></span>

    - <span data-ttu-id="41c02-182">Если на этом этапе у компьютера есть доступ к Интернету, дважды щелкните на пакете, чтобы установить приложение.</span><span class="sxs-lookup"><span data-stu-id="41c02-182">At this stage, if the Desktop PC has internet access, double-click the package to install the app.</span></span>


    - <span data-ttu-id="41c02-183">Если на целевом компьютере нет подключения к Интернету, выполните следующее.</span><span class="sxs-lookup"><span data-stu-id="41c02-183">If the desination PC has no internet connectivity, follow these steps:</span></span> 
       1. <span data-ttu-id="41c02-184">Выберите некодированную лицензию и нажмите **Создать лицензию**.</span><span class="sxs-lookup"><span data-stu-id="41c02-184">Select the unencoded license, and then select **Generate license**.</span></span>
       2. <span data-ttu-id="41c02-185">В разделе **Необходимые платформы** нажмите **Скачать**.</span><span class="sxs-lookup"><span data-stu-id="41c02-185">Under **Required Frameworks**, select **Download**.</span></span>
       3. <span data-ttu-id="41c02-186">Используйте DISM, чтобы применить пакет с зависимостью и лицензией.</span><span class="sxs-lookup"><span data-stu-id="41c02-186">Use DISM to apply the package with the dependency and license.</span></span> <span data-ttu-id="41c02-187">В командной строке администратора выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="41c02-187">From an administrator command prompt, run the following command:</span></span>

          ```console
          C:\WINDOWS\system32>dism /online /Add-ProvisionedAppxPackage /PackagePath:"C:\ARCoffline\Microsoft.AdvancedRecoveryCompanion_1.19050.1301.0_neutral_~_8wekyb3d8bbwe.appxbundle" /DependencyPackagePath:"C:\ARCoffline\Microsoft.VCLibs.140.00.UWPDesktop_14.0.27629.0_x86__8wekyb3d8bbwe.appx" /LicensePath:"C:\ARCoffline\Microsoft.AdvancedRecoveryCompanion_8wekyb3d8bbwe_f72ce112-dd2e-d771-8827-9cbcbf89f8b5.xml" /Region:all
          ```
            > [!NOTE]
            > <span data-ttu-id="41c02-188">Номер версии в этом примере кода может не соответствовать текущей доступной версии.</span><span class="sxs-lookup"><span data-stu-id="41c02-188">The version number in this code example may not match the currently available version.</span></span> <span data-ttu-id="41c02-189">Вы также можете выбрать место для скачивания, отличающееся от указанного в данном примере.</span><span class="sxs-lookup"><span data-stu-id="41c02-189">You may have also chosen a different download location than in the example.</span></span> <span data-ttu-id="41c02-190">При необходимости внесите в команду соответствующие изменения.</span><span class="sxs-lookup"><span data-stu-id="41c02-190">Make any changes to the command as needed.</span></span>

> [!TIP]
> <span data-ttu-id="41c02-191">Если вы планируете использовать Advanced Recovery Companion для установки FFU в автономном режиме, рекомендуется скачать устанавливаемый образ.</span><span class="sxs-lookup"><span data-stu-id="41c02-191">When you plan to use Advanced Recovery Companion to install an FFU offline, it may be useful to download your flash image.</span></span> <span data-ttu-id="41c02-192">[**Текущий образ для HoloLens2**](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="41c02-192">[**Download the current image for HoloLens 2**](https://aka.ms/hololens2download).</span></span> 

<span data-ttu-id="41c02-193">Другие ресурсы:</span><span class="sxs-lookup"><span data-stu-id="41c02-193">Other resources:</span></span>
- [<span data-ttu-id="41c02-194">Распространение автономных приложений</span><span class="sxs-lookup"><span data-stu-id="41c02-194">Distribute offline apps</span></span>](https://docs.microsoft.com/microsoft-store/distribute-offline-apps) 
- [<span data-ttu-id="41c02-195">Параметры командной строки для пакета приложения DISM (.appx или .appxbundle)</span><span class="sxs-lookup"><span data-stu-id="41c02-195">DISM app package (.appx or .appxbundle) servicing command-line options</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options)
