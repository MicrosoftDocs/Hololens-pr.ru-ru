---
title: Перезапуск, сброс или восстановление HoloLens 1
ms.reviewer: Keep up to date on the basic and advanced instructions for rebooting or resetting your HoloLens mixed reality device.
description: Использование средства восстановления устройств Windows для мгновенного создания образа в HoloLens 1-го поколения.
keywords: практические руководства, перезагрузка, сброс, восстановление, жесткий сброс, мягкий сброс, цикл электропитания, HoloLens, завершение работы, вдрт, средство восстановления устройств Windows
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: v-evmill
ms.date: 06/01/2020
ms.custom:
- CI 111456
- CSSTroubleshooting
ms.topic: article
ms.localizationpriority: medium
manager: yannisle
appliesto:
- HoloLens (1st gen)
ms.openlocfilehash: 5963be84a5fbb186c77965d9bbf112713fea8242
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923522"
---
# <a name="restart-reset-or-recover-hololens-1st-gen"></a><span data-ttu-id="ad184-104">Перезапуск, сброс или восстановление HoloLens (1-й общий)</span><span class="sxs-lookup"><span data-stu-id="ad184-104">Restart, reset, or recover HoloLens (1st Gen)</span></span>

<span data-ttu-id="ad184-105">При возникновении проблем с HoloLens может потребоваться выполнить перезагрузку или сбросить или даже восстановить устройство с помощью восстановления устройства.</span><span class="sxs-lookup"><span data-stu-id="ad184-105">If you're experiencing problems with your HoloLens, you may want to try a restart or reset, or even reflash the device by using device recovery.</span></span> <span data-ttu-id="ad184-106">В этой статье описываются рекомендуемые шаги по восстановлению по порядку.</span><span class="sxs-lookup"><span data-stu-id="ad184-106">This article guides you through the recommended recovery steps in order.</span></span>

<span data-ttu-id="ad184-107">Если вы хотите восстановить HoloLens 2, см. раздел [Восстановление hololens 2](hololens-recovery.md), так как этот процесс отличается.</span><span class="sxs-lookup"><span data-stu-id="ad184-107">If you're looking to recover a HoloLens 2, see [Recovering a HoloLens 2](hololens-recovery.md), as that process differs.</span></span>

> [!NOTE]
> <span data-ttu-id="ad184-108">В этой статье основное внимание уделяется устройству и программному обеспечению HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ad184-108">This article focuses on the HoloLens device and software.</span></span> <span data-ttu-id="ad184-109">Если ваши голограммы не выглядят правильно, см. сведения о факторах, повышающих качество голограмм, в разделе **[рекомендации по окружению HoloLens](hololens-environment-considerations.md)** .</span><span class="sxs-lookup"><span data-stu-id="ad184-109">If your holograms don't look right, see **[HoloLens environment considerations](hololens-environment-considerations.md)** for information about factors that improve hologram quality.</span></span>

## <a name="restart"></a><span data-ttu-id="ad184-110">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="ad184-110">Restart</span></span>

### <a name="do-a-safe-restart-by-using-cortana"></a><span data-ttu-id="ad184-111">Выполнить надежную перезагрузку с помощью Кортаны</span><span class="sxs-lookup"><span data-stu-id="ad184-111">Do a safe restart by using Cortana</span></span>

<span data-ttu-id="ad184-112">Самым надежным способом перезапуска HoloLens является использование Кортаны, что обычно является первым делом при возникновении проблемы с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ad184-112">The safest way to restart the HoloLens is by using Cortana, which is generally the first thing to try when you experience an issue with HoloLens.</span></span>

> [!NOTE] 
> <span data-ttu-id="ad184-113">Кортана недоступна на всех устройствах.</span><span class="sxs-lookup"><span data-stu-id="ad184-113">Cortana is not available on all devices.</span></span>
> - <span data-ttu-id="ad184-114">Кортана доступна на всех устройствах HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="ad184-114">Cortana is available on all HoloLens (1st Gen) devices.</span></span> 
> - <span data-ttu-id="ad184-115">Кортана доступна на устройствах HoloLens 2 в сборках, предшествовавших версии Windows Холограпик с обновлением 2004.</span><span class="sxs-lookup"><span data-stu-id="ad184-115">Cortana is available on HoloLens 2 devices on builds prior to the Windows Holograpic, Version 2004 update.</span></span>

1. <span data-ttu-id="ad184-116">Включите HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ad184-116">Turn on your HoloLens.</span></span>
1. <span data-ttu-id="ad184-117">Убедитесь, что пользователь вошел в систему, а устройство не ожидает пароль для его разблокировки.</span><span class="sxs-lookup"><span data-stu-id="ad184-117">Make sure that a user is logged in and the device isn't waiting for a password to unlock it.</span></span>
2. <span data-ttu-id="ad184-118">Скажите "Привет, Кортана, перезагрузка" или "Привет, Кортана, перезапуск".</span><span class="sxs-lookup"><span data-stu-id="ad184-118">Say "Hey Cortana, reboot" or "Hey Cortana, restart."</span></span>
3. <span data-ttu-id="ad184-119">Кортана ответит и отобразит запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ad184-119">Cortana will respond and prompt you to confirm.</span></span> <span data-ttu-id="ad184-120">Дождитесь воспроизведения звука после вопроса, а затем скажите «Да».</span><span class="sxs-lookup"><span data-stu-id="ad184-120">Wait for a sound to play after the question, and then say "Yes."</span></span> <span data-ttu-id="ad184-121">Устройство будет перезапущено.</span><span class="sxs-lookup"><span data-stu-id="ad184-121">The device will restart.</span></span>

### <a name="use-the-power-button-to-do-a-safe-restart"></a><span data-ttu-id="ad184-122">Использование кнопки питания для безопасного перезапуска</span><span class="sxs-lookup"><span data-stu-id="ad184-122">Use the power button to do a safe restart</span></span>

<span data-ttu-id="ad184-123">Если вы по-прежнему не можете перезапустить устройство, попробуйте перезапустить его с помощью кнопки **питания** :</span><span class="sxs-lookup"><span data-stu-id="ad184-123">If you still can't restart your device, try to restart it by using the **power** button:</span></span>

1. <span data-ttu-id="ad184-124">Нажмите и удерживайте кнопку **питания** в течение 5 секунд.</span><span class="sxs-lookup"><span data-stu-id="ad184-124">Press and hold the **power** button for 5 seconds.</span></span> <span data-ttu-id="ad184-125">Через 1 секунду все пять индикаторов будут освещены и постепенно отключаются друг от друга справа налево.</span><span class="sxs-lookup"><span data-stu-id="ad184-125">After 1 second, all five LEDs will illuminate and then slowly turn off one by one from right to left.</span></span> <span data-ttu-id="ad184-126">Через 5 секунд все индикаторы будут отключены, что означает успешное завершение работы.</span><span class="sxs-lookup"><span data-stu-id="ad184-126">After 5 seconds, all LEDs will be off, indicating successful shutdown.</span></span>
      
   > [!IMPORTANT]
   > <span data-ttu-id="ad184-127">Нажмите кнопку "Отмена" сразу после выключения всех индикаторов.</span><span class="sxs-lookup"><span data-stu-id="ad184-127">Stop pressing the button immediately after all the LEDs have turned off.</span></span>
1. <span data-ttu-id="ad184-128">Подождите 1 минуту завершения работы.</span><span class="sxs-lookup"><span data-stu-id="ad184-128">Wait 1 minute for the shutdown to complete.</span></span> <span data-ttu-id="ad184-129">Завершение работы может по-прежнему выполняться даже после выключения отображения.</span><span class="sxs-lookup"><span data-stu-id="ad184-129">The shutdown may still be in progress even after the displays are turned off.</span></span>
2. <span data-ttu-id="ad184-130">Снова включите устройство, нажав и удерживая кнопку **питания** в течение 1 секунды.</span><span class="sxs-lookup"><span data-stu-id="ad184-130">Turn on the device again by pressing and holding the **power** button for 1 second.</span></span>

### <a name="do-a-safe-restart-by-using-windows-device-portal"></a><span data-ttu-id="ad184-131">Выполните запуск безопасного перезапуска с помощью портала устройств Windows</span><span class="sxs-lookup"><span data-stu-id="ad184-131">Do a safe restart by using Windows Device Portal</span></span>

> [!NOTE]
> <span data-ttu-id="ad184-132">Для этого процесса HoloLens должен быть настроен в качестве устройства разработчика.</span><span class="sxs-lookup"><span data-stu-id="ad184-132">For this process, HoloLens has to be configured as a developer device.</span></span> <span data-ttu-id="ad184-133">Дополнительные сведения см. на [портале устройств Windows](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span><span class="sxs-lookup"><span data-stu-id="ad184-133">Learn more at [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span></span>

<span data-ttu-id="ad184-134">Если предыдущая процедура не работала, попробуйте перезапустить устройство с помощью [портала устройств Windows](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span><span class="sxs-lookup"><span data-stu-id="ad184-134">If the previous procedure didn't work, try to restart the device by using [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span></span> <span data-ttu-id="ad184-135">В правом верхнем углу найдите параметр для перезапуска или завершения работы устройства.</span><span class="sxs-lookup"><span data-stu-id="ad184-135">In the upper-right corner, find the option to restart or shut down the device.</span></span>

### <a name="do-an-unsafe-forced-restart"></a><span data-ttu-id="ad184-136">Выполнить ненадежное принудительное перезагрузку</span><span class="sxs-lookup"><span data-stu-id="ad184-136">Do an unsafe forced restart</span></span>

<span data-ttu-id="ad184-137">Если предыдущие методы не перезапускают HoloLens, выполните принудительную перезагрузку.</span><span class="sxs-lookup"><span data-stu-id="ad184-137">If the previous methods didn't restart your HoloLens, force a restart.</span></span> <span data-ttu-id="ad184-138">Этот метод эквивалентен удалению и переустановке аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="ad184-138">This method is equivalent to removing and reinstalling the battery.</span></span> <span data-ttu-id="ad184-139">Это опасно, так как оно может повредить устройство в поврежденном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ad184-139">It's dangerous because it might leave your device in a corrupted state.</span></span> <span data-ttu-id="ad184-140">В этом случае вам придется зафлэшировать HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ad184-140">If that happens, you'll have to flash your HoloLens.</span></span>  

> [!WARNING]
> <span data-ttu-id="ad184-141">Это потенциально опасный метод, который следует использовать только в том случае, если ранее упомянутые методы не работали.</span><span class="sxs-lookup"><span data-stu-id="ad184-141">This is a potentially harmful method and should only be used if the previously cited methods didn't work.</span></span>

1. <span data-ttu-id="ad184-142">Нажмите и удерживайте кнопку **питания** не менее 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="ad184-142">Press and hold the **power** button for at least 10 seconds.</span></span>
   - <span data-ttu-id="ad184-143">Можно удерживать кнопку дольше 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="ad184-143">It's okay to hold the button for longer than 10 seconds.</span></span>
   - <span data-ttu-id="ad184-144">Можно спокойно пропускать любые действия, которые привели к свету.</span><span class="sxs-lookup"><span data-stu-id="ad184-144">It's safe to ignore any LED activity.</span></span>
1. <span data-ttu-id="ad184-145">Отпустите кнопку и подождите 2-3 секунд.</span><span class="sxs-lookup"><span data-stu-id="ad184-145">Release the button and wait for 2-3 seconds.</span></span>
1. <span data-ttu-id="ad184-146">Нажмите и удерживайте кнопку **питания** в течение 1 секунды.</span><span class="sxs-lookup"><span data-stu-id="ad184-146">Press and hold the **power** button for 1  second.</span></span>
1. <span data-ttu-id="ad184-147">Если проблемы по-прежнему возникают, нажмите кнопку **питания** в течение 4 секунд, пока все индикаторы батареи не будут отображены, а экран не отобразит голограммы.</span><span class="sxs-lookup"><span data-stu-id="ad184-147">If you still have problems, press the **power** button for 4 seconds, until all the battery indicators fade out and the screen stops displaying holograms.</span></span> <span data-ttu-id="ad184-148">Подождите 1 минуту, а затем снова нажмите кнопку **питания** , чтобы включить устройство.</span><span class="sxs-lookup"><span data-stu-id="ad184-148">Wait 1 minute, and then press the **power** button again to turn on the device.</span></span>

## <a name="go-back-to-a-previous-version---hololens-1st-gen"></a><span data-ttu-id="ad184-149">Вернуться к предыдущей версии — HoloLens (1-й общий)</span><span class="sxs-lookup"><span data-stu-id="ad184-149">Go back to a previous version - HoloLens (1st Gen)</span></span>

<span data-ttu-id="ad184-150">В некоторых случаях может потребоваться вернуться к предыдущей версии программного обеспечения HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ad184-150">In some cases, you might want to go back to a previous version of the HoloLens software.</span></span> <span data-ttu-id="ad184-151">Это можно сделать с помощью средства восстановления устройств Windows, чтобы сбросить настройки HoloLens до более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="ad184-151">You can do this by using the Windows Device Recovery Tool to reset your HoloLens to the earlier version.</span></span>

> [!NOTE]
> <span data-ttu-id="ad184-152">При возврате к более ранней версии удаляются личные файлы и параметры.</span><span class="sxs-lookup"><span data-stu-id="ad184-152">Going back to an earlier version deletes your personal files and settings.</span></span>

<span data-ttu-id="ad184-153">Чтобы вернуться к предыдущей версии HoloLens 1, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ad184-153">To go back to a previous version of HoloLens 1, follow these steps:</span></span>

1. <span data-ttu-id="ad184-154">Убедитесь, что у вас нет телефонов или устройств Windows, подключенных к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="ad184-154">Make sure that you don't have any phones or Windows devices plugged in to your PC.</span></span>
1. <span data-ttu-id="ad184-155">На компьютере Скачайте [средство восстановления устройств Windows (вдрт)](https://support.microsoft.com/help/12379).</span><span class="sxs-lookup"><span data-stu-id="ad184-155">On your PC, download the [Windows Device Recovery Tool (WDRT)](https://support.microsoft.com/help/12379).</span></span>
1. <span data-ttu-id="ad184-156">Скачайте [пакет восстановления для годовщины HoloLens](https://aka.ms/hololensrecovery).</span><span class="sxs-lookup"><span data-stu-id="ad184-156">Download the [HoloLens Anniversary Update recovery package](https://aka.ms/hololensrecovery).</span></span>
1. <span data-ttu-id="ad184-157">После завершения загрузки откройте **файл**  >  **downloads** в проводнике.</span><span class="sxs-lookup"><span data-stu-id="ad184-157">When the downloads finish, open **File explorer** > **Downloads**.</span></span> <span data-ttu-id="ad184-158">Щелкните правой кнопкой мыши скачанную ZIP-папку и выберите **извлечь все**  >  **извлечь** , чтобы распаковать ее.</span><span class="sxs-lookup"><span data-stu-id="ad184-158">Right-click the zipped folder you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
1. <span data-ttu-id="ad184-159">Подключите HoloLens к компьютеру, используя кабель Micro-USB, поставляемый с ним.</span><span class="sxs-lookup"><span data-stu-id="ad184-159">Connect your HoloLens to your PC using the micro-USB cable that it came with.</span></span> <span data-ttu-id="ad184-160">(Даже если вы используете другие кабели для подключения HoloLens, это работает наилучшим образом.)</span><span class="sxs-lookup"><span data-stu-id="ad184-160">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
1. <span data-ttu-id="ad184-161">ВДРТ будет автоматически обнаруживать HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ad184-161">The WDRT will automatically detect your HoloLens.</span></span> <span data-ttu-id="ad184-162">Выберите плитку **Microsoft HoloLens** .</span><span class="sxs-lookup"><span data-stu-id="ad184-162">Select the **Microsoft HoloLens** tile.</span></span>
1. <span data-ttu-id="ad184-163">На следующем экране выберите **Ручное выделение пакетов** и выберите файл установки, содержащийся в папке, которая была распакована на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="ad184-163">On the next screen, select **Manual package selection** and choose the installation file contained in the folder you unzipped in step 4.</span></span> <span data-ttu-id="ad184-164">(Найдите файл с расширением ФФУ.)</span><span class="sxs-lookup"><span data-stu-id="ad184-164">(Look for a file with the .ffu extension.)</span></span>
1. <span data-ttu-id="ad184-165">Выберите **установить программное обеспечение** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="ad184-165">Select **Install software**, and follow the instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="ad184-166">Если ВДРТ не обнаруживает HoloLens, попробуйте перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="ad184-166">If the WDRT doesn't detect your HoloLens, try restarting your PC.</span></span> <span data-ttu-id="ad184-167">Если это не сработает, выберите пункт **мое устройство не обнаружено**, выберите **Microsoft HoloLens** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="ad184-167">If that doesn't work, select **My device was not detected**, select **Microsoft HoloLens**, and then follow the instructions.</span></span>

## <a name="reset-to-factory-settings"></a><span data-ttu-id="ad184-168">Сбросить до заводских настроек</span><span class="sxs-lookup"><span data-stu-id="ad184-168">Reset to factory settings</span></span>

> [!NOTE]
> <span data-ttu-id="ad184-169">Для сброса батареи требуется по крайней мере 40 процентов времени.</span><span class="sxs-lookup"><span data-stu-id="ad184-169">The battery needs at least a 40-percent charge to reset.</span></span>

<span data-ttu-id="ad184-170">Если у HoloLens по-прежнему возникла проблема, попробуйте сбросить его в состояние Factory.</span><span class="sxs-lookup"><span data-stu-id="ad184-170">If your HoloLens still has a problem, try resetting it to factory state.</span></span> <span data-ttu-id="ad184-171">Этот шаг позволяет сохранить установленную на нем программное обеспечение Windows holographic и возвратить все остальное в заводские настройки.</span><span class="sxs-lookup"><span data-stu-id="ad184-171">This step keeps the version of the Windows Holographic software that's installed on it and returns everything else to factory settings.</span></span>

>[!WARNING]
> <span data-ttu-id="ad184-172">При сбросе устройства все персональные данные, приложения и параметры будут удалены, включая сведения о сбросе TPM.</span><span class="sxs-lookup"><span data-stu-id="ad184-172">If you reset your device, all your personal data, apps, and settings will be erased, including TPM reset information.</span></span> <span data-ttu-id="ad184-173">При сбросе будет установлена только последняя установленная версия Windows Holographic.</span><span class="sxs-lookup"><span data-stu-id="ad184-173">Resetting will only install the latest installed version of Windows Holographic.</span></span> <span data-ttu-id="ad184-174">Вам потребуется повторить все этапы инициализации (калибровка, подключение к Wi-Fi, создание учетной записи пользователя, скачивание приложений и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ad184-174">You'll have to redo all the initialization steps (calibrate, connect to Wi-Fi, create a user account, download apps, and so on).</span></span>

1. <span data-ttu-id="ad184-175">Откройте приложение параметры и выберите **Обновить**  >  **Восстановление**.</span><span class="sxs-lookup"><span data-stu-id="ad184-175">Open the Settings app, and then select **Update** > **Recovery**.</span></span>
1. <span data-ttu-id="ad184-176">Выберите параметр **сбросить устройство** и прочтите сообщение с подтверждением.</span><span class="sxs-lookup"><span data-stu-id="ad184-176">Select the **Reset device** option and read the confirmation message.</span></span>
1. <span data-ttu-id="ad184-177">Подтвердите сброс.</span><span class="sxs-lookup"><span data-stu-id="ad184-177">Confirm the reset.</span></span> <span data-ttu-id="ad184-178">Устройство будет перезапущено и отобразится набор вращающихся шестеренк и индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="ad184-178">The device will restart and display a set of spinning gears and a progress bar.</span></span>
1. <span data-ttu-id="ad184-179">Подождите около 30 минут, пока этот процесс завершится.</span><span class="sxs-lookup"><span data-stu-id="ad184-179">Wait about 30 minutes for this process to complete.</span></span> <span data-ttu-id="ad184-180">После этого устройство будет перезагружено в "встроенное" взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="ad184-180">When it's done, the device will restart into the "out-of-the-box" experience.</span></span>

## <a name="reinstall-the-operating-system"></a><span data-ttu-id="ad184-181">Переустановка операционной системы</span><span class="sxs-lookup"><span data-stu-id="ad184-181">Reinstall the operating system</span></span>

<span data-ttu-id="ad184-182">Если после перезапуска и сброса устройства все еще возникают проблемы, можно использовать средство восстановления на компьютере, чтобы переустановить операционную систему HoloLens и встроенное по.</span><span class="sxs-lookup"><span data-stu-id="ad184-182">If the device is still having a problem after restart and reset, you can use a recovery tool on your computer to reinstall the HoloLens operating system and firmware.</span></span>  

<span data-ttu-id="ad184-183">Данные, необходимые для сброса, упаковываются в полноценное обновление Flash (ФФУ), которое аналогично ISO-, WIM-или файловым VHD-файлам.</span><span class="sxs-lookup"><span data-stu-id="ad184-183">The data that HoloLens needs for the reset is packaged in a Full Flash Update (FFU), which is similar to an .iso, .wim, or .vhd file.</span></span> [<span data-ttu-id="ad184-184">Сведения о форматах файлов изображений ФФУ.</span><span class="sxs-lookup"><span data-stu-id="ad184-184">Learn about FFU image file formats.</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/wim-vs-ffu-image-file-formats)

<span data-ttu-id="ad184-185">Новую операционную систему можно установить в HoloLens (1-й общий) с помощью средства восстановления устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="ad184-185">You can install a new operating system on your HoloLens (1st gen) by using the Windows Device Recovery Tool.</span></span> <span data-ttu-id="ad184-186">Перед тем как использовать это средство, см. статью Устранение неполадок при перезапуске или сбросе HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ad184-186">Before you use that tool, see if restarting or resetting your HoloLens fixes the problem.</span></span>

<span data-ttu-id="ad184-187">Процесс восстановления может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="ad184-187">The recovery process may take a while.</span></span> <span data-ttu-id="ad184-188">После этого будет установлена последняя версия программного обеспечения Windows Holographic.</span><span class="sxs-lookup"><span data-stu-id="ad184-188">When it's done, the latest version of the Windows Holographic software will be installed.</span></span>

<span data-ttu-id="ad184-189">Для использования этого средства требуется компьютер под Windows 10 или более поздней версии с объемом памяти не менее 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="ad184-189">To use the tool, you need a computer running Windows 10 or later with at least 4 GB of free storage space.</span></span> <span data-ttu-id="ad184-190">Это средство нельзя запустить на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ad184-190">You can't run this tool on a virtual machine.</span></span>

### <a name="recover-your-hololens"></a><span data-ttu-id="ad184-191">Восстановление HoloLens</span><span class="sxs-lookup"><span data-stu-id="ad184-191">Recover your HoloLens</span></span>

1. <span data-ttu-id="ad184-192">Скачайте и установите [средство восстановления устройств Windows](https://support.microsoft.com/help/12379/windows-10-mobile-device-recovery-tool-faq) на компьютере.</span><span class="sxs-lookup"><span data-stu-id="ad184-192">Download and install the [Windows Device Recovery Tool](https://support.microsoft.com/help/12379/windows-10-mobile-device-recovery-tool-faq) on your computer.</span></span>
1. <span data-ttu-id="ad184-193">Подключение HoloLens (1-го поколения) к компьютеру с помощью USB-кабеля Micro, поставляемого с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ad184-193">Connect the HoloLens (1st gen) to your computer by using the Micro USB cable that came with your HoloLens.</span></span>
1. <span data-ttu-id="ad184-194">Откройте средство восстановления устройств Windows и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="ad184-194">Open the Windows Device Recovery Tool and follow the instructions.</span></span>

<span data-ttu-id="ad184-195">Если HoloLens (первое поколение) не обнаруживается автоматически, выберите пункт **мое устройство не обнаружено**.</span><span class="sxs-lookup"><span data-stu-id="ad184-195">If the HoloLens (1st gen) isn't automatically detected, select **My device was not detected**.</span></span> <span data-ttu-id="ad184-196">Затем следуйте инструкциям, чтобы перевести устройство в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="ad184-196">Then follow the instructions to put the device into recovery mode.</span></span>

### <a name="manual-flashing-mode"></a><span data-ttu-id="ad184-197">Ручной режим мигания</span><span class="sxs-lookup"><span data-stu-id="ad184-197">Manual flashing mode</span></span>

<span data-ttu-id="ad184-198">Если устройство не обнаружено, выполните следующие действия, чтобы перевести его в мигающий режим:</span><span class="sxs-lookup"><span data-stu-id="ad184-198">If your device isn't detected, follow these steps to put it into flashing mode:</span></span>

1. <span data-ttu-id="ad184-199">Отключите устройство от любого источника питания.</span><span class="sxs-lookup"><span data-stu-id="ad184-199">Unplug the device from any power source.</span></span>
1. <span data-ttu-id="ad184-200">Если устройство включено, удерживайте нажатой кнопку **питания** , пока она не будет полностью выключена.</span><span class="sxs-lookup"><span data-stu-id="ad184-200">If the device is on, hold down the **power** button until it completely turns off.</span></span>
2. <span data-ttu-id="ad184-201">Удерживайте кнопку **Громкость** и ненадолго коснитесь кнопки **питания** .</span><span class="sxs-lookup"><span data-stu-id="ad184-201">Hold the **volume up** button, and briefly tap the **power** button.</span></span> <span data-ttu-id="ad184-202">Устройство должно запуститься и отображать только средний индикатор.</span><span class="sxs-lookup"><span data-stu-id="ad184-202">The device should start and display only the middle LED.</span></span>
3. <span data-ttu-id="ad184-203">Подключите устройство к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="ad184-203">Plug the device into your PC.</span></span>
4. <span data-ttu-id="ad184-204">Откройте средство восстановления устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="ad184-204">Open the Windows Device Recovery Tool.</span></span>
5. <span data-ttu-id="ad184-205">Выберите **мое устройство не обнаружено** , а затем **HoloLens**.</span><span class="sxs-lookup"><span data-stu-id="ad184-205">Select **My device was not detected** and then **HoloLens**.</span></span> 
6. <span data-ttu-id="ad184-206">Следуйте инструкциям по восстановлению устройства.</span><span class="sxs-lookup"><span data-stu-id="ad184-206">Follow the instructions to recover your device.</span></span>
