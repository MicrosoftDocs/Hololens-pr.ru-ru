---
title: Перезапуск, сброс и восстановление HoloLens
ms.reviewer: Both basic and advanced instructions for rebooting or resetting your HoloLens.
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
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 5da7f954454b5713823c5aa94742f9c9c0033ca2
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10828597"
---
# <span data-ttu-id="8d7eb-104">Сброс и восстановление HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="8d7eb-104">Reset and Recovery for HoloLens 2</span></span>

## <span data-ttu-id="8d7eb-105">Зарядка устройства</span><span class="sxs-lookup"><span data-stu-id="8d7eb-105">Charging the device</span></span>

<span data-ttu-id="8d7eb-106">Прежде чем приступить к устранению неполадок, по возможности обеспечьте заряд вашего устройства хотя бы от 20 до 40 %.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-106">Before starting any troubleshooting procedure, if possible, ensure that your device is charged at least between 20% and 40%.</span></span>

<span data-ttu-id="8d7eb-107">Используйте зарядное устройство и кабели USB Type-C, поставляемые вместе с устройством HoloLens2.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-107">Please ensure you are using the charger and the USB Type-C cables that come with the HoloLens2 device.</span></span> <span data-ttu-id="8d7eb-108">Если они недоступны, убедитесь, что зарядное устройство поддерживает не менее 15 Вт.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-108">In case they are not available ensure the charger available can support at least 15W of power.</span></span>

> [!NOTE]
> <span data-ttu-id="8d7eb-109">По возможности не используйте ПК для зарядки устройства по USB, так как зарядка при этом выполняется очень медленно.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-109">If possible, do not use a PC to charge the device over USB as this will provide a very slow charge.</span></span>

<span data-ttu-id="8d7eb-110">Если устройство правильно загружено и запущено, существует три различных способа проверить заряд батареи.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-110">If the device is correctly booted and running there are three different ways of checking the charge of your battery.</span></span>

1. <span data-ttu-id="8d7eb-111">В главном меню пользовательского интерфейса устройства HoloLens.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-111">From the main menu of the HoloLens Device UI.</span></span>
2. <span data-ttu-id="8d7eb-112">С помощью светодиода, расположенного рядом с кнопкой питания (при заряде 40 % должны постоянно гореть минимум два светодиодных индикатора).</span><span class="sxs-lookup"><span data-stu-id="8d7eb-112">Using the LED close to the power button (for 40% you should see at least two solid LEDS).</span></span>
3. <span data-ttu-id="8d7eb-113">На главном компьютере откройте окно проводника и найдите устройство HoloLens 2 слева в разделе "Этот компьютер".</span><span class="sxs-lookup"><span data-stu-id="8d7eb-113">On your Host PC open File Explorer window and look for your HoloLens 2 device on left side under “This PC”.</span></span>
    
      <span data-ttu-id="8d7eb-114">а.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-114">a.</span></span> <span data-ttu-id="8d7eb-115">Щелкните правой кнопкой мыши имя устройства и выберите "Свойства".</span><span class="sxs-lookup"><span data-stu-id="8d7eb-115">Right click on the name of the device and select properties.</span></span> <span data-ttu-id="8d7eb-116">Откроется диалоговое окно, демонстрирующее уровень заряда батареи вашего устройства.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-116">A dialog will appear showing the battery level for your device.</span></span>

![HoloLens 2 ResetRecovery](images/ResetRecovery2.png)

<span data-ttu-id="8d7eb-118">Если устройство не удается загрузить в меню запуска, обратите внимание на индикаторы и перечисление на главном компьютере и следуйте инструкциям по устранению неполадок (https://docs.microsoft.com/hololens/hololens-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="8d7eb-118">If the device cannot be booted to the Startup Menu, please take note of the LEDs and enumeration on the host PC and follow the troubleshooting guide (https://docs.microsoft.com/hololens/hololens-troubleshooting).</span></span> <span data-ttu-id="8d7eb-119">Если состояние устройства не соответствует ни одному из указанных состояний в руководстве по устранению неполадок, выполните **аппаратный сброс**, не подключая устройство к основному компьютеру, но подключив его к блоку питания.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-119">In case the state of the device does not fall in any of the states listed in the troubleshooting guide, execute the **hard reset procedure** without reconnecting the device to your host PC, but connect it instead to the power supply.</span></span> <span data-ttu-id="8d7eb-120">Подождите не менее часа, чтобы устройство зарядилось.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-120">Wait for at least one hour for the device to charge.</span></span>

## <span data-ttu-id="8d7eb-121">Сброс устройства</span><span class="sxs-lookup"><span data-stu-id="8d7eb-121">Reset the device</span></span>

<span data-ttu-id="8d7eb-122">При определенных обстоятельствах пользователю может потребоваться вручную сбросить устройство без использования программного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-122">Under certain circumstances the customer may be required to manually reset the device without using the SW UI.</span></span> 

### <span data-ttu-id="8d7eb-123">Стандартная процедура</span><span class="sxs-lookup"><span data-stu-id="8d7eb-123">Standard procedure</span></span>
1. <span data-ttu-id="8d7eb-124">Отключите устройство от блока питания или основного компьютера, отключив кабель Type-C.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-124">Disconnect the device from the power supply or the host PC by unplugging the Type-C cable.</span></span>

2. <span data-ttu-id="8d7eb-125">Нажмите и удерживайте **кнопку питания** в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-125">Press and hold the **power button** for 15 seconds.</span></span> <span data-ttu-id="8d7eb-126">Все светодиодные индикаторы должны быть выключены.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-126">All LEDs should be off.</span></span>

3. <span data-ttu-id="8d7eb-127">Подождите 2–3 секунды и кратковременно нажмите **кнопку питания**. Загорятся светодиодные индикаторы рядом с кнопкой питания, и устройство начнет загружаться.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-127">Wait 2-3 seconds and Short press the **power button**, the LEDs close to the power button will light up and the device will start to boot.</span></span> 

4. <span data-ttu-id="8d7eb-128">Подключите устройство к основному компьютеру, откройте диспетчер устройств (в Windows 10 **нажмите клавишу Windows** + **Х** и выберите "Диспетчер устройств") и убедитесь, что устройство правильно указано как Microsoft HoloLens, как показано на рисунках ниже.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-128">Connect the device to the host PC, open Device Manager (for Windows 10 press the **“Windows” key** and then the **“x” key** and click on “Device Manager”) and make sure the device enumerates correctly as Microsoft HoloLens as shown in the pictures below:</span></span>

![HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLensRecovery.png)

### <span data-ttu-id="8d7eb-130">Процедура аппаратного сброса</span><span class="sxs-lookup"><span data-stu-id="8d7eb-130">Hard-reset procedure</span></span>

<span data-ttu-id="8d7eb-131">Если стандартная процедура сброса не сработала, вы можете использовать аппаратный сброс.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-131">If the standard reset procedure does not work, you can use the hard-reset procedure.</span></span>

1. <span data-ttu-id="8d7eb-132">Отключите устройство от блока питания или основного компьютера, отключив кабель Type-C.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-132">Disconnect the device from the power supply or the host PC by unplugging the Type-C cable.</span></span>

2. <span data-ttu-id="8d7eb-133">Удерживайте нажатыми **кнопку уменьшения громкости + кнопку питания** в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-133">Hold **volume down + power button** for 15 seconds.</span></span>

3. <span data-ttu-id="8d7eb-134">Устройство автоматически перезагрузится.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-134">The device will automatically reboot.</span></span> 

4. <span data-ttu-id="8d7eb-135">Подключите устройство к основному компьютеру, откройте диспетчер устройств (в Windows 10 **нажмите клавишу Windows** + **Х** и выберите "Диспетчер устройств") и убедитесь, что устройство правильно указано как Microsoft HoloLens, как показано на рисунках ниже.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-135">Connect the device to the host PC, open Device Manager (for Windows 10 press the **“Windows” key** and then the **“x” key** and click on “Device Manager”) and make sure the device enumerates correctly as Microsoft HoloLens as shown in the pictures below.</span></span>

![HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLens_DeviceManager.png)

## <span data-ttu-id="8d7eb-137">Установка чистого образа устройства</span><span class="sxs-lookup"><span data-stu-id="8d7eb-137">Clean reflash the device</span></span>

<span data-ttu-id="8d7eb-138">В чрезвычайных ситуациях может потребоваться установить чистый образ устройства.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-138">In extraordinary situations you may be required to clean flash the device.</span></span> <span data-ttu-id="8d7eb-139">Существует два способа переустановки образа устройства HoloLens2.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-139">There are two ways to reflash a HoloLens2 device.</span></span> <span data-ttu-id="8d7eb-140">Во всех процедурах переустановки образа вам потребуется [установить приложение Advanced Recovery Companion из Магазина Windows](https://www.microsoft.com/store/productId/9P74Z35SFRS8).</span><span class="sxs-lookup"><span data-stu-id="8d7eb-140">For all reflashing procedures you will be required to [install the Advanced Recovery Companion app from the Windows Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8).</span></span> <span data-ttu-id="8d7eb-141">При сбросе устройства удаляются все личные данные, приложения и параметры, в том числе сбрасывается доверенный платформенный модуль (TPM).</span><span class="sxs-lookup"><span data-stu-id="8d7eb-141">If you reset your device, all your personal data, apps, and settings will be erased, including TPM reset.</span></span>

<span data-ttu-id="8d7eb-142">В настоящее время приложение Advanced Recovery Companion настроено на скачивание сборки выпуска компонентов для [Windows Holographic 2004](hololens-release-notes.md#windows-holographic-version-2004). Если вы хотите скачать последнюю версию HoloLens 2 FFU для установки образа устройства с помощью Advanced Recovery Companion, вы можете скачать его [здесь](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="8d7eb-142">Advanced Recovery Companion is currently set to download the feature release build for [Windows Holographic 2004](hololens-release-notes.md#windows-holographic-version-2004), if you would like to download the latest HoloLens 2 FFU to flash your device via Advanced Recovery Companion then you may download it from [here](https://aka.ms/hololens2download).</span></span> <span data-ttu-id="8d7eb-143">Это актуальная сборка, соответствующая последней общедоступной сборке.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-143">This is kept up-to-date and will match the latest generally available build.</span></span> 

<span data-ttu-id="8d7eb-144">Перед запуском установки образа установите и запустите приложение на компьютере с Windows 10 и подготовьте его к обнаружению устройства.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-144">Before starting the flashing procedure make sure the app is installed and running on your Windows 10 PC and ready to detect the device.</span></span>

![Установка чистого образа HoloLens 2](images/ARC1.png)

### <span data-ttu-id="8d7eb-146">Нормальная процедура</span><span class="sxs-lookup"><span data-stu-id="8d7eb-146">Normal procedure</span></span>

1. <span data-ttu-id="8d7eb-147">При запущенном устройстве HoloLens подключите его к компьютеру с Windows 10, на котором ранее было запущено приложение Advanced Recovery Companion.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-147">While the HoloLens device is running, connect it to your Windows 10 PC where you previously launched the Advanced Recovery Companion App.</span></span>

2. <span data-ttu-id="8d7eb-148">Устройство будет обнаружено автоматически, а пользовательский интерфейс приложения Advanced Recovery Companion изменится следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8d7eb-148">The device will automatically be detected and the Advanced Recovery Companion App UI will update as follows:</span></span>

![Установка чистого образа HoloLens 2](images/ARC2.png)

3. <span data-ttu-id="8d7eb-150">Выберите устройство HoloLens2 в пользовательском интерфейсе приложения Advanced Recovery Companion и следуйте инструкциям, чтобы завершить установку образа.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-150">Select the HoloLens2 device in the Advanced Recovery Companion App UI and follow the instructions to complete the flashing.</span></span>

### <span data-ttu-id="8d7eb-151">Ручная процедура</span><span class="sxs-lookup"><span data-stu-id="8d7eb-151">Manual procedure</span></span>

<span data-ttu-id="8d7eb-152">Если устройство загружается неправильно, вам может потребоваться перевести устройство HoloLens 2 в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-152">If the device does not boot correctly you may need to put the HoloLens 2 device in Recovery mode.</span></span>

1. <span data-ttu-id="8d7eb-153">Отключите устройство от блока питания или основного компьютера, отключив кабель Type-C.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-153">Disconnect the device from the power supply or the host PC by unplugging the Type-C cable.</span></span> 

2. <span data-ttu-id="8d7eb-154">Нажмите и удерживайте **кнопку питания** в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-154">Press and hold the **power button** for 15 seconds.</span></span> <span data-ttu-id="8d7eb-155">Все светодиодные индикаторы должны быть выключены.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-155">All LEDs should turn off.</span></span> 

3. <span data-ttu-id="8d7eb-156">Нажав **кнопку увеличения громкости**, нажмите и отпустите **кнопку питания**, чтобы загрузить устройство.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-156">While pressing the **volume up button**, press and release the **power button** to boot the device.</span></span> <span data-ttu-id="8d7eb-157">Подождите 15 секунд, прежде чем отпустить кнопку увеличения громкости.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-157">Wait 15 seconds before releasing the volume up button.</span></span> <span data-ttu-id="8d7eb-158">Из пяти светодиодных индикаторов на устройстве будет гореть только средний индикатор.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-158">Out of the 5 LEDs on the device, only the middle LED will light up.</span></span>

4. <span data-ttu-id="8d7eb-159">Подключите устройство к основному компьютеру, откройте диспетчер устройств (в Windows 10 **нажмите клавишу Windows** + **Х** и выберите "Диспетчер устройств") и убедитесь, что устройство правильно указано как Microsoft HoloLens, как показано на изображении ниже.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-159">Connect the device to the host PC, open Device Manager (for Windows 10 press the **“Windows” key** and then the **“x” key** and click on “Device Manager”) and make sure the device enumerates correctly as Microsoft HoloLens as shown in the image below.</span></span>

![HoloLens 2 MicrosoftHoloLensRecovery](images/MicrosoftHoloLensRecovery.png)

5. <span data-ttu-id="8d7eb-161">Устройство будет обнаружено автоматически, а пользовательский интерфейс приложения Advanced Recovery Companion изменится следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8d7eb-161">The device will be automatically detected, and the Advanced Recovery Companion app UI will update as follows:</span></span>

![Установка чистого образа HoloLens 2](images/ARC2.png)

6. <span data-ttu-id="8d7eb-163">Выберите устройство HoloLens 2 в пользовательском интерфейсе приложения Advanced Recovery Companion и следуйте инструкциям, чтобы завершить установку образа.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-163">Select the HoloLens 2 device in the Advanced Recovery Companion app UI and follow the instructions to complete the flashing.</span></span>

## <span data-ttu-id="8d7eb-164">Скачивание ARC без использования App Store</span><span class="sxs-lookup"><span data-stu-id="8d7eb-164">Downloading ARC without using the app store</span></span>

<span data-ttu-id="8d7eb-165">Если ИТ-среда не позволяет использовать приложение Магазина Windows или ограничивает доступ к розничному магазину, ИТ-администраторы могут предоставить доступ к этому приложению другими "автономными" способами развертывания.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-165">If an IT environment prevents the use of the Windows Store app or limits access to the retail store, IT administrators can make this app available through other ‘offline’ deployment paths.</span></span> 

- <span data-ttu-id="8d7eb-166">Этот процесс можно также использовать для других приложений, как показано на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-166">This process may also be used for other apps, as seen in step 2.</span></span> <span data-ttu-id="8d7eb-167">Это руководство посвящено Advanced Recovery Companion, но может быть изменено для других автономных приложений.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-167">This guide will focus on Advanced Recovery Companion, but my be modified for other offline apps.</span></span>  

<span data-ttu-id="8d7eb-168">Этот способ развертывания можно активировать с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-168">This deployment path can be enabled with the following steps:</span></span>
1.  <span data-ttu-id="8d7eb-169">Перейдите на [веб-сайт Store для бизнеса](https://businessstore.microsoft.com) и войдите с помощью удостоверения Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-169">Go to the [Store For Business website](https://businessstore.microsoft.com) and sign-in with an Azure AD identity.</span></span>
1.  <span data-ttu-id="8d7eb-170">Выберите **Управление — Параметры** и включите параметр **Показать автономные приложения** в разделе **Покупки** как описано на странице https://businessstore.microsoft.com/manage/settings/shop</span><span class="sxs-lookup"><span data-stu-id="8d7eb-170">Go to **Manage – Settings**, and turn on **Show offline apps** under **Shopping experience** as described at https://businessstore.microsoft.com/manage/settings/shop</span></span> 
1.  <span data-ttu-id="8d7eb-171">Перейдите в раздел **Купить для моей группы** и найдите приложение [Advanced Recovery Companion](https://businessstore.microsoft.com/store/details/advanced-recovery-companion/9P74Z35SFRS8).</span><span class="sxs-lookup"><span data-stu-id="8d7eb-171">Go to **shop for my group** and search for the [Advanced Recovery Companion](https://businessstore.microsoft.com/store/details/advanced-recovery-companion/9P74Z35SFRS8) app.</span></span>
1.  <span data-ttu-id="8d7eb-172">Измените поле **Тип лицензии** на автономное использование и щелкните **Управление**.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-172">Change the **License Type** box to offline and click **Manage**.</span></span>
1.  <span data-ttu-id="8d7eb-173">В разделе "Скачивание пакета для автономной работы" нажмите вторую синюю кнопку **Скачать**.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-173">Under Download the package for offline use click the second blue **“Download”** button .</span></span> <span data-ttu-id="8d7eb-174">Убедитесь, что файл имеет расширение .appxbundle.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-174">Ensure the file extension is .appxbundle.</span></span>
1.  <span data-ttu-id="8d7eb-175">Если на этом этапе у компьютера есть доступ к Интернету, просто дважды щелкните и установите его.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-175">At this stage, if the Desktop PC has Internet access, simply double click and install.</span></span> 
1.  <span data-ttu-id="8d7eb-176">ИТ-администратор также может распространять это приложение с помощью System Center Configuration Manager (SCCM) или Intune.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-176">The IT administrator can also distribute this app through System Center Configuration Manager (SCCM) or Intune.</span></span>
1.  <span data-ttu-id="8d7eb-177">Если на целевом компьютере нет подключения к Интернету, потребуются дополнительные действия:</span><span class="sxs-lookup"><span data-stu-id="8d7eb-177">If the target PC has no Internet connectivity, some additional steps are needed:</span></span> 
    1.  <span data-ttu-id="8d7eb-178">Выберите некодированную лицензию и щелкните **Создать лицензию**, а затем в разделе **Необходимые платформы** нажмите **Скачать**.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-178">Select the unencoded license and click **“Generate license”** and under **“Required Frameworks”** click **“Download.”**</span></span> 
    1.  <span data-ttu-id="8d7eb-179">На компьютерах без доступа к Интернету потребуется использовать DISM, чтобы применить пакет с зависимостью и лицензией.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-179">PCs without internet access will need to use DISM to apply the package with the dependency and license.</span></span> <span data-ttu-id="8d7eb-180">В командной строке администратора введите:</span><span class="sxs-lookup"><span data-stu-id="8d7eb-180">In an administrator command prompt, type:</span></span>

      ```console
      C:\WINDOWS\system32>dism /online /Add-ProvisionedAppxPackage /PackagePath:"C:\ARCoffline\Microsoft.AdvancedRecoveryCompanion_1.19050.1301.0_neutral_~_8wekyb3d8bbwe.appxbundle" /DependencyPackagePath:"C:\ARCoffline\Microsoft.VCLibs.140.00.UWPDesktop_14.0.27629.0_x86__8wekyb3d8bbwe.appx" /LicensePath:"C:\ARCoffline\Microsoft.AdvancedRecoveryCompanion_8wekyb3d8bbwe_f72ce112-dd2e-d771-8827-9cbcbf89f8b5.xml" /Region:all
      ```
> [!NOTE]
> <span data-ttu-id="8d7eb-181">Номер версии в этом примере кода может не соответствовать текущей доступной версии.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-181">The version number in this code example may not match the currently avalible version.</span></span> <span data-ttu-id="8d7eb-182">Вы также можете выбрать место для скачивания, отличное от этого примера.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-182">You may have also choosen a different download location than in the example given.</span></span> <span data-ttu-id="8d7eb-183">Внесите все необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-183">Please make sure to make any changes as needed.</span></span>

> [!TIP]
> <span data-ttu-id="8d7eb-184">Если вы планируете использовать Advanced Recovery Companion для установки FFU в автономном режиме, рекомендуется скачать устанавливаемый образ, чтобы он был доступен. [Текущий образ для HoloLens 2](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="8d7eb-184">When planning to use Advanced Recovery Companion to install an ffu offline it may be useful to download your flashing image to be availible, here is the [current image for HoloLens 2](https://aka.ms/hololens2download).</span></span> 

<span data-ttu-id="8d7eb-185">Другие ресурсы:</span><span class="sxs-lookup"><span data-stu-id="8d7eb-185">Other resources:</span></span>
- https://docs.microsoft.com/microsoft-store/distribute-offline-apps 
- https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options


