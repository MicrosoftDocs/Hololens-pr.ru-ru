---
title: Перезапуск, сброс и восстановление HoloLens 1
ms.reviewer: Both basic and advanced instructions for rebooting or resetting your HoloLens.
description: Сведения о том, как с помощью Windows Device Recovery Tool восстановить образ на устройство HoloLens первого поколения.
keywords: инструкции, перезагрузка, сброс, восстановление, аппаратный сброс, программный сброс, включение и выключение питания, HoloLens, завершение работы, wdrt, windows device recovery tool
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: v-evmill
ms.date: 06/01/2020
ms.custom:
- CI 111456
- CSSTroubleshooting
ms.topic: article
ms.localizationpriority: high
manager: yannisle
appliesto:
- HoloLens (1st gen)
ms.openlocfilehash: 36192315e234db16c7747457e69d6d6281c31bfe
ms.sourcegitcommit: 29755f5af0086a43c532fb5a9a4ae65c36bc82de
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2020
ms.locfileid: "10857737"
---
# <span data-ttu-id="872b9-104">Перезапуск, сброс и восстановление HoloLens (1-е поколение)</span><span class="sxs-lookup"><span data-stu-id="872b9-104">Restart, reset, or recover HoloLens (1st Gen)</span></span>

<span data-ttu-id="872b9-105">Если у вас возникли проблемы с HoloLens, попробуйте выполнить перезагрузку или сброс устройства или даже восстановление образа.</span><span class="sxs-lookup"><span data-stu-id="872b9-105">If you're experiencing problems with your HoloLens you may want to try a restart, reset, or even re-flash with device recovery.</span></span>

<span data-ttu-id="872b9-106">Ниже описаны действия, которые следует выполнить, если возникли ошибки в работе HoloLens.</span><span class="sxs-lookup"><span data-stu-id="872b9-106">Here are some things to try if your HoloLens isn't running well.</span></span>  <span data-ttu-id="872b9-107">В этой статье вы найдете инструкции по выполнению рекомендуемого восстановления.</span><span class="sxs-lookup"><span data-stu-id="872b9-107">This article will guide you through the recommended recovery steps in succession.</span></span>

<span data-ttu-id="872b9-108">Если требуется восстановить HoloLens 2, перейдите к разделу [Восстановление HoloLens 2](https://docs.microsoft.com/hololens/hololens-recovery), так как для этой версии процесс восстановления несколько отличается..</span><span class="sxs-lookup"><span data-stu-id="872b9-108">If you are looking to recover a HoloLens 2, please view the page for [Recovering a HoloLens 2](https://docs.microsoft.com/hololens/hololens-recovery), as there are differences in the processes.</span></span>

<span data-ttu-id="872b9-109">В данной статье рассматривается устройство HoloLens и программное обеспечение для него. Информацию о влиянии факторов окружающей среды на качество голограмм можно найти в [этой статье](hololens-environment-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="872b9-109">This article focuses on the HoloLens device and software, if your holograms don't look right, [this article](hololens-environment-considerations.md) talks about environmental factors that improve hologram quality.</span></span>

## <span data-ttu-id="872b9-110">«Перезапуск»</span><span class="sxs-lookup"><span data-stu-id="872b9-110">Restart</span></span>

### <span data-ttu-id="872b9-111">Безопасный перезапуск с помощью Кортаны</span><span class="sxs-lookup"><span data-stu-id="872b9-111">Perform a safe restart by using Cortana</span></span>

<span data-ttu-id="872b9-112">Самый безопасный способ перезапустить HoloLens— с использованием Кортаны.</span><span class="sxs-lookup"><span data-stu-id="872b9-112">The safest way to restart the HoloLens is by using Cortana.</span></span> <span data-ttu-id="872b9-113">Обычно это самый простой первый шаг устранения неполадок в работе HoloLens.</span><span class="sxs-lookup"><span data-stu-id="872b9-113">This is generally an easy first-step when experiencing an issue with HoloLens.</span></span> 

> [!NOTE]
> <span data-ttu-id="872b9-114">Кортана доступна</span><span class="sxs-lookup"><span data-stu-id="872b9-114">Cortana is not avalible on all devices.</span></span> <span data-ttu-id="872b9-115">на всех устройствах HoloLens (1-е поколение),</span><span class="sxs-lookup"><span data-stu-id="872b9-115">Cortana is avalible to all HoloLens (1st Gen) devices.</span></span>
> <span data-ttu-id="872b9-116">а также на устройствах HoloLens 2 с версией Windows Holographic до обновления 2004.</span><span class="sxs-lookup"><span data-stu-id="872b9-116">Cortana is avalible on HoloLens 2 devices on a build prior to the Windows Holograpic, Version 2004 update.</span></span>

1. <span data-ttu-id="872b9-117">Наденьте устройство.</span><span class="sxs-lookup"><span data-stu-id="872b9-117">Put on your device</span></span>
1. <span data-ttu-id="872b9-118">Убедитесь, что устройство включено, вход в учетную запись выполнен, и устройство не ожидает ввода пароля для разблокировки.</span><span class="sxs-lookup"><span data-stu-id="872b9-118">Make sure it's powered on, a user is logged in, and the device is not waiting for a password to unlock it.</span></span>
1. <span data-ttu-id="872b9-119">Произнесите фразу "Привет, Кортана, перезагрузка" или "Привет, Кортана, перезапуск".</span><span class="sxs-lookup"><span data-stu-id="872b9-119">Say "Hey Cortana, reboot" or "Hey Cortana, restart."</span></span>
1. <span data-ttu-id="872b9-120">Кортана запросит подтверждение команды.</span><span class="sxs-lookup"><span data-stu-id="872b9-120">When she acknowledges she will ask you for confirmation.</span></span> <span data-ttu-id="872b9-121">Дождитесь звукового сигнала после ее вопроса, указывающего на то, что она ожидает вашего ответа, и произнесите "Да".</span><span class="sxs-lookup"><span data-stu-id="872b9-121">Wait a second for a sound to play after she has finished her question, indicating she is listening to you and then say "Yes."</span></span>
1. <span data-ttu-id="872b9-122">Устройство перезагрузится.</span><span class="sxs-lookup"><span data-stu-id="872b9-122">The device will now restart.</span></span>

### <span data-ttu-id="872b9-123">Безопасный перезапуск с помощью кнопки питания</span><span class="sxs-lookup"><span data-stu-id="872b9-123">Perform a safe restart by using the power button</span></span>

<span data-ttu-id="872b9-124">Если перезапустить устройство не получилось, попробуйте выполнить перезапуск с помощью кнопки питания.</span><span class="sxs-lookup"><span data-stu-id="872b9-124">If you still can't restart your device, you can try to restart it by using the power button:</span></span>

1. <span data-ttu-id="872b9-125">Нажмите и удерживайте кнопку питания в течение 5секунд.</span><span class="sxs-lookup"><span data-stu-id="872b9-125">Press and hold the power button for five seconds.</span></span>
   1. <span data-ttu-id="872b9-126">Через одну секунду загорятся все светодиодные индикаторы, а затем начнут медленно гаснуть по очереди справа налево.</span><span class="sxs-lookup"><span data-stu-id="872b9-126">After one second, you will see all five LEDs illuminate, then slowly turn off from right to left.</span></span>
   1. <span data-ttu-id="872b9-127">Через 5секунд все светодиодные индикаторы погаснут. Это означает, что устройство получило команду завершения работы.</span><span class="sxs-lookup"><span data-stu-id="872b9-127">After five seconds, all LEDs will be off, indicating the shutdown command was issued successfully.</span></span>
   1. <span data-ttu-id="872b9-128">Крайне важно отпустить кнопку питания сразу после того, как погаснут все светодиодные индикаторы.</span><span class="sxs-lookup"><span data-stu-id="872b9-128">Note that it's important to stop pressing the button immediately after all the LEDs have turned off.</span></span>
1. <span data-ttu-id="872b9-129">Подождите одну минуту, пока устройство завершит работу.</span><span class="sxs-lookup"><span data-stu-id="872b9-129">Wait one minute for the shutdown to cleanly succeed.</span></span> <span data-ttu-id="872b9-130">Этот процесс может все еще выполняться, даже если все индикаторы погасли.</span><span class="sxs-lookup"><span data-stu-id="872b9-130">Note that the shutdown may still be in progress even if the displays are turned off.</span></span>
1. <span data-ttu-id="872b9-131">Нажмите и удерживайте кнопку питания в течение 1секунды, чтобы вновь включить устройство.</span><span class="sxs-lookup"><span data-stu-id="872b9-131">Power on the device again by pressing and holding the power button for one second.</span></span>

### <span data-ttu-id="872b9-132">Безопасный перезапуск с помощью портала устройств Windows</span><span class="sxs-lookup"><span data-stu-id="872b9-132">Perform a safe restart by using Windows Device Portal</span></span>

> [!NOTE]
> <span data-ttu-id="872b9-133">Чтобы воспользоваться этой функцией, необходимо перевести HoloLens в режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="872b9-133">To do this, HoloLens has to be configured as a developer device.</span></span>  
> <span data-ttu-id="872b9-134">Дополнительные сведения см. в статье по использованию [портала устройств Windows](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span><span class="sxs-lookup"><span data-stu-id="872b9-134">Read more about [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span></span>

<span data-ttu-id="872b9-135">Если вам не удалось перезагрузить устройство с помощью описанных выше методов, попробуйте воспользоваться для этого [порталом устройств Windows](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span><span class="sxs-lookup"><span data-stu-id="872b9-135">If the previous procedure doesn't work, you can try to restart the device by using [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span></span> <span data-ttu-id="872b9-136">Кнопки перезапуска и выключения устройства расположены в правом верхнем углу окна.</span><span class="sxs-lookup"><span data-stu-id="872b9-136">In the upper right corner, there is an option to restart or shut down the device.</span></span>

### <span data-ttu-id="872b9-137">Небезопасный принудительный перезапуск</span><span class="sxs-lookup"><span data-stu-id="872b9-137">Perform an unsafe forced restart</span></span>

<span data-ttu-id="872b9-138">Если ни один из предыдущих способов не помог перезагрузить устройство, можно выполнить принудительный перезапуск.</span><span class="sxs-lookup"><span data-stu-id="872b9-138">If none of the previous methods are able to successfully restart your device, you can force a restart.</span></span> <span data-ttu-id="872b9-139">По своей сути этот метод аналогичен извлечению батареи из HoloLens.</span><span class="sxs-lookup"><span data-stu-id="872b9-139">This method is equivalent to pulling the battery from the HoloLens.</span></span>  <span data-ttu-id="872b9-140">Это опасный метод, так как в результате устройство может остаться в ошибочном состоянии.</span><span class="sxs-lookup"><span data-stu-id="872b9-140">It is a dangerous operation which may leave your device in a corrupt state.</span></span>  <span data-ttu-id="872b9-141">Если такое произойдет, потребуется восстановить образ на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="872b9-141">If that happens, you'll have to flash your HoloLens.</span></span>  

> [!WARNING]
> <span data-ttu-id="872b9-142">Это потенциально опасный способ, и его следует использовать только в том случае, если не сработал ни один из приведенных выше способов.</span><span class="sxs-lookup"><span data-stu-id="872b9-142">This is a potentially harmful method and should only be used in the event none of the above methods work.</span></span>

1. <span data-ttu-id="872b9-143">Нажмите и удерживайте кнопку питания в течение не менее 10секунд.</span><span class="sxs-lookup"><span data-stu-id="872b9-143">Press and hold the power button for at least 10 seconds.</span></span>
   - <span data-ttu-id="872b9-144">Кнопку можно удерживать и более 10секунд.</span><span class="sxs-lookup"><span data-stu-id="872b9-144">It's okay to hold the button for longer than 10 seconds.</span></span>
   - <span data-ttu-id="872b9-145">Состояние светодиодных индикаторов можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="872b9-145">It's safe to ignore any LED activity.</span></span>
1. <span data-ttu-id="872b9-146">Отпустите кнопку и подождите 2–3секунды.</span><span class="sxs-lookup"><span data-stu-id="872b9-146">Release the button and wait for two or three seconds.</span></span>
1. <span data-ttu-id="872b9-147">Нажмите и удерживайте кнопку питания в течение 1секунды, чтобы вновь включить устройство.</span><span class="sxs-lookup"><span data-stu-id="872b9-147">Power on the device again by pressing and holding the power button for one second.</span></span>
<span data-ttu-id="872b9-148">Если проблему устранить не удалось, нажмите и удерживайте кнопку питания в течение 4секунд, пока не погаснет индикатор заряда батареи и на экране не перестанут отображаться голограммы.</span><span class="sxs-lookup"><span data-stu-id="872b9-148">If you're still having problems, press the power button for 4 seconds, until all of the battery indicators fade out and the screen stops displaying holograms.</span></span> <span data-ttu-id="872b9-149">Через 1минуту вновь нажмите кнопку питания, чтобы включить устройство.</span><span class="sxs-lookup"><span data-stu-id="872b9-149">Wait 1 minute, then press the power button again to turn on the device.</span></span>

## <span data-ttu-id="872b9-150">Восстановление заводских настроек</span><span class="sxs-lookup"><span data-stu-id="872b9-150">Reset to factory settings</span></span>

> [!NOTE]
> <span data-ttu-id="872b9-151">Сброс устройства можно выполнить при заряде батареи не менее 40%.</span><span class="sxs-lookup"><span data-stu-id="872b9-151">The battery needs at least 40 percent charge to reset.</span></span>

<span data-ttu-id="872b9-152">Если перезапуск не помог устранить проблемы в работе HoloLens, попробуйте восстановить на устройстве заводские настройки.</span><span class="sxs-lookup"><span data-stu-id="872b9-152">If your HoloLens is still experiencing issues after restarting, try resetting it to factory state.</span></span>  <span data-ttu-id="872b9-153">В результате этой операции на устройстве сохраняется установленная версия программного обеспечения Windows Holographic. Все остальные настройки возвращаются в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="872b9-153">Resetting your HoloLens keeps the version of the Windows Holographic software that's installed on it and returns everything else to factory settings.</span></span>

<span data-ttu-id="872b9-154">При сбросе устройства удаляются все личные данные, приложения и параметры, в том числе сбрасывается доверенный платформенный модуль (TPM).</span><span class="sxs-lookup"><span data-stu-id="872b9-154">If you reset your device, all your personal data, apps, and settings will be erased, including TPM reset.</span></span> <span data-ttu-id="872b9-155">На устройстве будет установлена только последняя имевшаяся на нем версия Windows Holographic. Вам потребуется повторить процедуру инициализации (калибровка, подключение к Wi-Fi, создание учетной записи, загрузка приложений и т.д.).</span><span class="sxs-lookup"><span data-stu-id="872b9-155">Resetting will only install the latest installed version of Windows Holographic and you will have to redo all the initialization steps (calibrate, connect to Wi-Fi, create a user account, download apps, and so forth).</span></span>

1. <span data-ttu-id="872b9-156">Запустите приложение "Параметры" и выберите **Обновление** > **Сброс**.</span><span class="sxs-lookup"><span data-stu-id="872b9-156">Launch the Settings app, and then select **Update** > **Reset**.</span></span>
1. <span data-ttu-id="872b9-157">Выберите вариант **Сброс устройства** и ознакомьтесь с сообщением подтверждения.</span><span class="sxs-lookup"><span data-stu-id="872b9-157">Select the **Reset device** option and read the confirmation message.</span></span>
1. <span data-ttu-id="872b9-158">После вашего согласия на продолжение устройство перезагрузится, и на экране появятся вращающиеся шестеренки и индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="872b9-158">If you agree to reset your device, the device will restart and display a set of spinning gears with a progress bar.</span></span>
1. <span data-ttu-id="872b9-159">Дождитесь завершения операции (она займет около 30минут).</span><span class="sxs-lookup"><span data-stu-id="872b9-159">Wait about 30 minutes for this process to complete.</span></span>
1. <span data-ttu-id="872b9-160">По окончании сброса устройство загрузится в заводском состоянии.</span><span class="sxs-lookup"><span data-stu-id="872b9-160">The reset will complete and the device will restart into the out-of-the-box experience.</span></span>

## <span data-ttu-id="872b9-161">Переустановка операционной системы</span><span class="sxs-lookup"><span data-stu-id="872b9-161">Re-install the operating system</span></span>

<span data-ttu-id="872b9-162">Если перезагрузка и сброс не помогли устранить проблемы в работе устройства, воспользуйтесь доступным на компьютере средством восстановления, чтобы переустановить операционную систему и встроенное ПО HoloLens.</span><span class="sxs-lookup"><span data-stu-id="872b9-162">If the device is still having a problem after rebooting and resetting, you can use a recovery tool on your computer to reinstall the HoloLens' operating system and firmware.</span></span>  

<span data-ttu-id="872b9-163">Все необходимые для этого данные упакованы в файл установки с расширением FFU (средство для пакетного применения образов).</span><span class="sxs-lookup"><span data-stu-id="872b9-163">All of the data HoloLens needs to reset is packaged in a Full Flash Update (ffu).</span></span>  <span data-ttu-id="872b9-164">Этот формат аналогичен форматам ISO, WIM и VHD.</span><span class="sxs-lookup"><span data-stu-id="872b9-164">This is similar to an iso, wim, or vhd.</span></span>  [<span data-ttu-id="872b9-165">(Сведения о формате FFU см. в этой статье.)</span><span class="sxs-lookup"><span data-stu-id="872b9-165">Learn about FFU image file formats.</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/wim-vs-ffu-image-file-formats)

<span data-ttu-id="872b9-166">При необходимости на HoloLens (1-е поколение) можно установить новую операционную систему с помощью средства Windows Device Recovery Tool.</span><span class="sxs-lookup"><span data-stu-id="872b9-166">If necessary, you can install a completely new operating system on your HoloLens (1st gen) with the Windows Device Recovery Tool.</span></span>

<span data-ttu-id="872b9-167">Прежде чем воспользоваться этим средством, попробуйте устранить проблемы с помощью перезагрузки или сброса HoloLens.</span><span class="sxs-lookup"><span data-stu-id="872b9-167">Before you use this tool, determine if restarting or resetting your HoloLens fixes the problem.</span></span> <span data-ttu-id="872b9-168">Процесс восстановления может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="872b9-168">The recovery process may take some time.</span></span>  <span data-ttu-id="872b9-169">По окончании на HoloLens будет установлена последняя версия программного обеспечения Windows Holographic, одобренная для вашего устройства.</span><span class="sxs-lookup"><span data-stu-id="872b9-169">When you're done, the latest version of the Windows Holographic software approved for your HoloLens will be installed.</span></span>

<span data-ttu-id="872b9-170">Чтобы воспользоваться средством восстановления, вам потребуется компьютер с ОС Windows10 или более поздней версией и не менее 4ГБ свободного дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="872b9-170">To use the tool, you'll need a computer running Windows 10 or later, with at least 4 GB of free storage space.</span></span>  <span data-ttu-id="872b9-171">Обратите внимание, что средство нельзя запустить на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="872b9-171">Please note that you can't run this tool on a virtual machine.</span></span>

### <span data-ttu-id="872b9-172">Восстановление HoloLens</span><span class="sxs-lookup"><span data-stu-id="872b9-172">Recover your HoloLens:</span></span>

1. <span data-ttu-id="872b9-173">Скачайте и установите средство [Windows Device Recovery Tool](https://support.microsoft.com/help/12379/windows-10-mobile-device-recovery-tool-faq) на компьютере.</span><span class="sxs-lookup"><span data-stu-id="872b9-173">Download and install the [Windows Device Recovery Tool](https://support.microsoft.com/help/12379/windows-10-mobile-device-recovery-tool-faq) on your computer.</span></span>
1. <span data-ttu-id="872b9-174">Подключите HoloLens (1-е поколение) к компьютеру с помощью входящего в комплект кабеля Micro-USB.</span><span class="sxs-lookup"><span data-stu-id="872b9-174">Connect the HoloLens (1st gen) to your computer using the Micro USB cable that came with your HoloLens.</span></span>
1. <span data-ttu-id="872b9-175">Запустите средство Windows Device Recovery Tool и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="872b9-175">Run the Windows Device Recovery Tool and follow the instructions.</span></span>

<span data-ttu-id="872b9-176">Если устройство HoloLens (1-е поколение) не будет обнаружено автоматически, выберите **Мое устройство не обнаружено** и следуйте инструкциям, чтобы перевести устройство в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="872b9-176">If the HoloLens (1st gen) isn't automatically detected, select **My device was not detected** and follow the instructions to put your device into recovery mode.</span></span>

### <span data-ttu-id="872b9-177">Ручной режим восстановления образа</span><span class="sxs-lookup"><span data-stu-id="872b9-177">Manual Flashing Mode:</span></span>

<span data-ttu-id="872b9-178">Если устройство не обнаружено, воспользуйтесь следующим способом, чтобы вручную перевести устройство в режим восстановления образа.</span><span class="sxs-lookup"><span data-stu-id="872b9-178">In the event that your device is not being detected please use the following method to manually place it into flashing mode.</span></span>

1. <span data-ttu-id="872b9-179">Отсоедините устройство от всех источников питания.</span><span class="sxs-lookup"><span data-stu-id="872b9-179">Unplug the device from all power sources.</span></span>
1. <span data-ttu-id="872b9-180">Если устройство включено, нажмите и удерживайте кнопку питания, пока оно не выключится.</span><span class="sxs-lookup"><span data-stu-id="872b9-180">If the device is on please hold down the power button until it is completely off.</span></span>
1. <span data-ttu-id="872b9-181">Нажмите и удерживайте кнопку **увеличения громкости**, а затем кратковременно нажмите **кнопку питания**.</span><span class="sxs-lookup"><span data-stu-id="872b9-181">Hold the **Volume Up** button, and breifly tap the **Power button**.</span></span> 
1. <span data-ttu-id="872b9-182">Устройство перезагрузится, и отобразится только средний светодиодный индикатор.</span><span class="sxs-lookup"><span data-stu-id="872b9-182">The device should boot and then display only the middle LED light.</span></span>
1. <span data-ttu-id="872b9-183">Подключите устройство к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="872b9-183">Plug the device into your PC.</span></span>
1. <span data-ttu-id="872b9-184">Запустите Windows Device Recovery Tool.</span><span class="sxs-lookup"><span data-stu-id="872b9-184">Launch Windows Device Recovery Tool.</span></span>
1. <span data-ttu-id="872b9-185">Выберите \*Мое устройство не обнаружено\*\*, а затем— **HoloLens**.</span><span class="sxs-lookup"><span data-stu-id="872b9-185">You will need to select \*My device was not detected\*\*, and then select **HoloLens**.</span></span> 
1. <span data-ttu-id="872b9-186">Следуйте инструкциям для восстановления устройства</span><span class="sxs-lookup"><span data-stu-id="872b9-186">Follow the instructions to recover your device.</span></span>
