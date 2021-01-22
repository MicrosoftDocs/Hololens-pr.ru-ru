---
title: Перезапуск, сброс и восстановление HoloLens 1
ms.reviewer: Keep up to date on the basic and advanced instructions for rebooting or resetting your HoloLens mixed reality device.
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
ms.openlocfilehash: f0aa400be56d09a843a1b7c9bae78346551ad8af
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283920"
---
# <span data-ttu-id="587a0-104">Перезапуск, сброс и восстановление HoloLens (1-е поколение)</span><span class="sxs-lookup"><span data-stu-id="587a0-104">Restart, reset, or recover HoloLens (1st Gen)</span></span>

<span data-ttu-id="587a0-105">Если у вас возникли проблемы с HoloLens, попробуйте выполнить перезагрузку, сброс устройства или даже переустановку образа с использованием функции восстановления.</span><span class="sxs-lookup"><span data-stu-id="587a0-105">If you're experiencing problems with your HoloLens, you may want to try a restart or reset, or even reflash the device by using device recovery.</span></span> <span data-ttu-id="587a0-106">В этой статье вы найдете рекомендации по выполнению восстановления.</span><span class="sxs-lookup"><span data-stu-id="587a0-106">This article guides you through the recommended recovery steps in order.</span></span>

<span data-ttu-id="587a0-107">Если вам нужно восстановить HoloLens2, см. статью [Восстановление HoloLens2](https://docs.microsoft.com/hololens/hololens-recovery), поскольку это другой процесс.</span><span class="sxs-lookup"><span data-stu-id="587a0-107">If you're looking to recover a HoloLens 2, see [Recovering a HoloLens 2](https://docs.microsoft.com/hololens/hololens-recovery), as that process differs.</span></span>

> [!NOTE]
> <span data-ttu-id="587a0-108">В этой статье рассматривается устройство и программное обеспечение HoloLens.</span><span class="sxs-lookup"><span data-stu-id="587a0-108">This article focuses on the HoloLens device and software.</span></span> <span data-ttu-id="587a0-109">Если ваши голограммы выглядят неправильно, см. статью **[Требования к среде для HoloLens ](hololens-environment-considerations.md)**, где рассказывается о факторах, влияющих на качество голограмм.</span><span class="sxs-lookup"><span data-stu-id="587a0-109">If your holograms don't look right, see **[HoloLens environment considerations](hololens-environment-considerations.md)** for information about factors that improve hologram quality.</span></span>

## <span data-ttu-id="587a0-110">«Перезапуск»</span><span class="sxs-lookup"><span data-stu-id="587a0-110">Restart</span></span>

### <span data-ttu-id="587a0-111">Безопасный перезапуск с помощью Кортаны</span><span class="sxs-lookup"><span data-stu-id="587a0-111">Do a safe restart by using Cortana</span></span>

<span data-ttu-id="587a0-112">Самый надежный способ перезапуска HoloLens заключается в использовании Кортаны. Это первое, что следует сделать, если у вас возникла проблема с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="587a0-112">The safest way to restart the HoloLens is by using Cortana, which is generally the first thing to try when you experience an issue with HoloLens.</span></span>

> [!NOTE] 
> <span data-ttu-id="587a0-113">Кортана доступна не на всех устройствах.</span><span class="sxs-lookup"><span data-stu-id="587a0-113">Cortana is not available on all devices.</span></span>
> - <span data-ttu-id="587a0-114">Кортана доступна на всех устройствах HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="587a0-114">Cortana is available on all HoloLens (1st Gen) devices.</span></span> 
> - <span data-ttu-id="587a0-115">Кортана доступна на устройствах HoloLens 2 с версией Windows Holographic до обновления 2004.</span><span class="sxs-lookup"><span data-stu-id="587a0-115">Cortana is available on HoloLens 2 devices on builds prior to the Windows Holograpic, Version 2004 update.</span></span>

1. <span data-ttu-id="587a0-116">Включите HoloLens.</span><span class="sxs-lookup"><span data-stu-id="587a0-116">Turn on your HoloLens.</span></span>
1. <span data-ttu-id="587a0-117">Убедитесь, что вход в учетную запись выполнен, и устройство не ожидает ввода пароля для разблокировки.</span><span class="sxs-lookup"><span data-stu-id="587a0-117">Make sure that a user is logged in and the device isn't waiting for a password to unlock it.</span></span>
2. <span data-ttu-id="587a0-118">Произнесите фразу "Привет, Кортана, перезагрузка" или "Привет, Кортана, перезапуск".</span><span class="sxs-lookup"><span data-stu-id="587a0-118">Say "Hey Cortana, reboot" or "Hey Cortana, restart."</span></span>
3. <span data-ttu-id="587a0-119">Кортана ответит и предложит подтвердить команду.</span><span class="sxs-lookup"><span data-stu-id="587a0-119">Cortana will respond and prompt you to confirm.</span></span> <span data-ttu-id="587a0-120">Дождитесь звука после вопроса, а затем произнесите "Да".</span><span class="sxs-lookup"><span data-stu-id="587a0-120">Wait for a sound to play after the question, and then say "Yes."</span></span> <span data-ttu-id="587a0-121">Устройство перезапустится.</span><span class="sxs-lookup"><span data-stu-id="587a0-121">The device will restart.</span></span>

### <span data-ttu-id="587a0-122">Безопасный перезапуск с использованием кнопки питания.</span><span class="sxs-lookup"><span data-stu-id="587a0-122">Use the power button to do a safe restart</span></span>

<span data-ttu-id="587a0-123">Если вам пока не удалось перезапустить устройство, попробуйте это сделать с помощью кнопки **питания** следующим образом.</span><span class="sxs-lookup"><span data-stu-id="587a0-123">If you still can't restart your device, try to restart it by using the **power** button:</span></span>

1. <span data-ttu-id="587a0-124">Нажмите и удерживайте кнопку **питания** в течение 5секунд.</span><span class="sxs-lookup"><span data-stu-id="587a0-124">Press and hold the **power** button for 5 seconds.</span></span> <span data-ttu-id="587a0-125">Через 1 секунду все пять светодиодных индикаторов загорятся и начнут медленно гаснуть один за другим справа налево.</span><span class="sxs-lookup"><span data-stu-id="587a0-125">After 1 second, all five LEDs will illuminate and then slowly turn off one by one from right to left.</span></span> <span data-ttu-id="587a0-126">Через 5 секунд все индикаторы погаснут, означая завершение работы.</span><span class="sxs-lookup"><span data-stu-id="587a0-126">After 5 seconds, all LEDs will be off, indicating successful shutdown.</span></span>
      
   > [!IMPORTANT]
   > <span data-ttu-id="587a0-127">Отпустите кнопку питания сразу после того, как погаснут все светодиодные индикаторы.</span><span class="sxs-lookup"><span data-stu-id="587a0-127">Stop pressing the button immediately after all the LEDs have turned off.</span></span>
1. <span data-ttu-id="587a0-128">Подождите 1 минуту для полного завершения работы.</span><span class="sxs-lookup"><span data-stu-id="587a0-128">Wait 1 minute for the shutdown to complete.</span></span> <span data-ttu-id="587a0-129">Этот процесс может все еще выполняться, даже если все индикаторы уже погасли.</span><span class="sxs-lookup"><span data-stu-id="587a0-129">The shutdown may still be in progress even after the displays are turned off.</span></span>
2. <span data-ttu-id="587a0-130">Нажмите и удерживайте кнопку **питания** в течение 1секунды, чтобы вновь включить устройство.</span><span class="sxs-lookup"><span data-stu-id="587a0-130">Turn on the device again by pressing and holding the **power** button for 1 second.</span></span>

### <span data-ttu-id="587a0-131">Безопасный перезапуск с помощью портала устройств Windows</span><span class="sxs-lookup"><span data-stu-id="587a0-131">Do a safe restart by using Windows Device Portal</span></span>

> [!NOTE]
> <span data-ttu-id="587a0-132">Чтобы воспользоваться этой функцией, необходимо перевести HoloLens в режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="587a0-132">For this process, HoloLens has to be configured as a developer device.</span></span> <span data-ttu-id="587a0-133">Дополнительные сведения см. на [портале устройств Windows](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span><span class="sxs-lookup"><span data-stu-id="587a0-133">Learn more at [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span></span>

<span data-ttu-id="587a0-134">Если вам не удалось перезапустить устройство с помощью описанных выше методов, попробуйте воспользоваться [порталом устройств Windows](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span><span class="sxs-lookup"><span data-stu-id="587a0-134">If the previous procedure didn't work, try to restart the device by using [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal).</span></span> <span data-ttu-id="587a0-135">Кнопки перезапуска и выключения устройства расположены в правом верхнем углу окна.</span><span class="sxs-lookup"><span data-stu-id="587a0-135">In the upper-right corner, find the option to restart or shut down the device.</span></span>

### <span data-ttu-id="587a0-136">Небезопасный принудительный перезапуск</span><span class="sxs-lookup"><span data-stu-id="587a0-136">Do an unsafe forced restart</span></span>

<span data-ttu-id="587a0-137">Если описанные выше методы не помогли перезапустить HoloLens, выполните принудительный перезапуск.</span><span class="sxs-lookup"><span data-stu-id="587a0-137">If the previous methods didn't restart your HoloLens, force a restart.</span></span> <span data-ttu-id="587a0-138">По своей сути этот метод аналогичен извлечению батареи из HoloLens и ее повторной установке.</span><span class="sxs-lookup"><span data-stu-id="587a0-138">This method is equivalent to removing and reinstalling the battery.</span></span> <span data-ttu-id="587a0-139">Это опасно, поскольку может привести к повреждению устройства.</span><span class="sxs-lookup"><span data-stu-id="587a0-139">It's dangerous because it might leave your device in a corrupted state.</span></span> <span data-ttu-id="587a0-140">Если такое произойдет, потребуется восстановить образ на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="587a0-140">If that happens, you'll have to flash your HoloLens.</span></span>  

> [!WARNING]
> <span data-ttu-id="587a0-141">Это потенциально опасный способ, и его следует использовать только в том случае, если не сработал ни один из приведенных выше способов.</span><span class="sxs-lookup"><span data-stu-id="587a0-141">This is a potentially harmful method and should only be used if the previously cited methods didn't work.</span></span>

1. <span data-ttu-id="587a0-142">Нажмите и удерживайте кнопку **питания** не менее 10секунд.</span><span class="sxs-lookup"><span data-stu-id="587a0-142">Press and hold the **power** button for at least 10 seconds.</span></span>
   - <span data-ttu-id="587a0-143">Кнопку можно удерживать и более 10секунд.</span><span class="sxs-lookup"><span data-stu-id="587a0-143">It's okay to hold the button for longer than 10 seconds.</span></span>
   - <span data-ttu-id="587a0-144">Состояние светодиодных индикаторов можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="587a0-144">It's safe to ignore any LED activity.</span></span>
1. <span data-ttu-id="587a0-145">Отпустите кнопку и подождите 2–3секунды.</span><span class="sxs-lookup"><span data-stu-id="587a0-145">Release the button and wait for 2-3 seconds.</span></span>
1. <span data-ttu-id="587a0-146">Нажмите и удерживайте кнопку **питания** в течение 1секунды.</span><span class="sxs-lookup"><span data-stu-id="587a0-146">Press and hold the **power** button for 1  second.</span></span>
1. <span data-ttu-id="587a0-147">Если проблему устранить не удалось, нажмите и удерживайте кнопку **питания** в течение 4секунд, пока не погаснет индикатор заряда батареи и на экране не перестанут отображаться голограммы.</span><span class="sxs-lookup"><span data-stu-id="587a0-147">If you still have problems, press the **power** button for 4 seconds, until all the battery indicators fade out and the screen stops displaying holograms.</span></span> <span data-ttu-id="587a0-148">Через 1минуту вновь нажмите кнопку **питания**, чтобы включить устройство.</span><span class="sxs-lookup"><span data-stu-id="587a0-148">Wait 1 minute, and then press the **power** button again to turn on the device.</span></span>

## <span data-ttu-id="587a0-149">Восстановление заводских настроек</span><span class="sxs-lookup"><span data-stu-id="587a0-149">Reset to factory settings</span></span>

> [!NOTE]
> <span data-ttu-id="587a0-150">Сброс устройства можно выполнить при заряде батареи не менее 40%.</span><span class="sxs-lookup"><span data-stu-id="587a0-150">The battery needs at least a 40-percent charge to reset.</span></span>

<span data-ttu-id="587a0-151">Если проблема с HoloLens не устранена, попробуйте сбросить устройство с восстановлением заводских настроек.</span><span class="sxs-lookup"><span data-stu-id="587a0-151">If your HoloLens still has a problem, try resetting it to factory state.</span></span> <span data-ttu-id="587a0-152">В результате этой операции на устройстве сохраняется установленная версия программного обеспечения Windows Holographic. Все остальные настройки возвращаются в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="587a0-152">This step keeps the version of the Windows Holographic software that's installed on it and returns everything else to factory settings.</span></span>

>[!WARNING]
> <span data-ttu-id="587a0-153">При сбросе устройства удаляются все личные данные, приложения и параметры, в том числе сбрасывается доверенный платформенный модуль (TPM).</span><span class="sxs-lookup"><span data-stu-id="587a0-153">If you reset your device, all your personal data, apps, and settings will be erased, including TPM reset information.</span></span> <span data-ttu-id="587a0-154">После сброса сохранится только последняя установленная версия Windows Holographic.</span><span class="sxs-lookup"><span data-stu-id="587a0-154">Resetting will only install the latest installed version of Windows Holographic.</span></span> <span data-ttu-id="587a0-155">Вам потребуется заново выполнить все этапы первоначальной настройки (калибровку, подключение к Wi-Fi, создание учетной записи пользователя, скачивание приложений и т.д.).</span><span class="sxs-lookup"><span data-stu-id="587a0-155">You'll have to redo all the initialization steps (calibrate, connect to Wi-Fi, create a user account, download apps, and so on).</span></span>

1. <span data-ttu-id="587a0-156">Откройте приложение "Параметры" и выберите **Обновление** > **Восстановление**.</span><span class="sxs-lookup"><span data-stu-id="587a0-156">Open the Settings app, and then select **Update** > **Recovery**.</span></span>
1. <span data-ttu-id="587a0-157">Выберите вариант **Сброс устройства** и ознакомьтесь с сообщением подтверждения.</span><span class="sxs-lookup"><span data-stu-id="587a0-157">Select the **Reset device** option and read the confirmation message.</span></span>
1. <span data-ttu-id="587a0-158">Подтвердите сброс.</span><span class="sxs-lookup"><span data-stu-id="587a0-158">Confirm the reset.</span></span> <span data-ttu-id="587a0-159">Устройство перезапустится, и на экране появятся вращающиеся шестеренки и индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="587a0-159">The device will restart and display a set of spinning gears and a progress bar.</span></span>
1. <span data-ttu-id="587a0-160">Дождитесь завершения операции (она займет около 30минут).</span><span class="sxs-lookup"><span data-stu-id="587a0-160">Wait about 30 minutes for this process to complete.</span></span> <span data-ttu-id="587a0-161">По окончании сброса устройство перезапустится в заводском состоянии.</span><span class="sxs-lookup"><span data-stu-id="587a0-161">When it's done, the device will restart into the "out-of-the-box" experience.</span></span>

## <span data-ttu-id="587a0-162">Переустановка операционной системы</span><span class="sxs-lookup"><span data-stu-id="587a0-162">Reinstall the operating system</span></span>

<span data-ttu-id="587a0-163">Если перезапуск и сброс не помогли устранить проблемы в работе устройства, воспользуйтесь имеющимся на компьютере средством восстановления, чтобы переустановить операционную систему и встроенное ПО HoloLens.</span><span class="sxs-lookup"><span data-stu-id="587a0-163">If the device is still having a problem after restart and reset, you can use a recovery tool on your computer to reinstall the HoloLens operating system and firmware.</span></span>  

<span data-ttu-id="587a0-164">Данные, необходимые HoloLens для сброса, упакованы в файл средства для пакетного применения образов (FFU), аналогичный файлу .iso, .wim или .vhd.</span><span class="sxs-lookup"><span data-stu-id="587a0-164">The data that HoloLens needs for the reset is packaged in a Full Flash Update (FFU), which is similar to an .iso, .wim, or .vhd file.</span></span> [<span data-ttu-id="587a0-165">(Сведения о формате FFU см. в этой статье.)</span><span class="sxs-lookup"><span data-stu-id="587a0-165">Learn about FFU image file formats.</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/wim-vs-ffu-image-file-formats)

<span data-ttu-id="587a0-166">На HoloLens (1-го поколения) можно установить новую операционную систему с помощью средства Windows Device Recovery Tool.</span><span class="sxs-lookup"><span data-stu-id="587a0-166">You can install a new operating system on your HoloLens (1st gen) by using the Windows Device Recovery Tool.</span></span> <span data-ttu-id="587a0-167">Прежде чем воспользоваться этим средством, попробуйте устранить проблемы с помощью перезагрузки или сброса HoloLens.</span><span class="sxs-lookup"><span data-stu-id="587a0-167">Before you use that tool, see if restarting or resetting your HoloLens fixes the problem.</span></span>

<span data-ttu-id="587a0-168">Процесс восстановления может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="587a0-168">The recovery process may take a while.</span></span> <span data-ttu-id="587a0-169">По окончании на HoloLens будет установлена последняя версия программного обеспечения Windows Holographic.</span><span class="sxs-lookup"><span data-stu-id="587a0-169">When it's done, the latest version of the Windows Holographic software will be installed.</span></span>

<span data-ttu-id="587a0-170">Чтобы воспользоваться средством восстановления, вам потребуется компьютер с ОС Windows10 или более поздней версии и не менее 4ГБ свободного дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="587a0-170">To use the tool, you need a computer running Windows 10 or later with at least 4 GB of free storage space.</span></span> <span data-ttu-id="587a0-171">Средство нельзя запустить на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="587a0-171">You can't run this tool on a virtual machine.</span></span>

### <span data-ttu-id="587a0-172">Восстановление HoloLens</span><span class="sxs-lookup"><span data-stu-id="587a0-172">Recover your HoloLens</span></span>

1. <span data-ttu-id="587a0-173">Скачайте и установите средство [Windows Device Recovery Tool](https://support.microsoft.com/help/12379/windows-10-mobile-device-recovery-tool-faq) на компьютере.</span><span class="sxs-lookup"><span data-stu-id="587a0-173">Download and install the [Windows Device Recovery Tool](https://support.microsoft.com/help/12379/windows-10-mobile-device-recovery-tool-faq) on your computer.</span></span>
1. <span data-ttu-id="587a0-174">Подключите HoloLens (1-го поколения) к компьютеру с помощью входящего в комплект кабеля Micro-USB.</span><span class="sxs-lookup"><span data-stu-id="587a0-174">Connect the HoloLens (1st gen) to your computer by using the Micro USB cable that came with your HoloLens.</span></span>
1. <span data-ttu-id="587a0-175">Откройте средство Windows Device Recovery Tool и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="587a0-175">Open the Windows Device Recovery Tool and follow the instructions.</span></span>

<span data-ttu-id="587a0-176">Если HoloLens (1-го поколения) не найден автоматически, щелкните **Мое устройство не обнаружено**.</span><span class="sxs-lookup"><span data-stu-id="587a0-176">If the HoloLens (1st gen) isn't automatically detected, select **My device was not detected**.</span></span> <span data-ttu-id="587a0-177">Затем следуйте инструкциям, чтобы перевести устройство в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="587a0-177">Then follow the instructions to put the device into recovery mode.</span></span>

### <span data-ttu-id="587a0-178">Ручной режим установки образа</span><span class="sxs-lookup"><span data-stu-id="587a0-178">Manual flashing mode</span></span>

<span data-ttu-id="587a0-179">Если устройство не найдено, выполните указанные ниже действия, чтобы перевести его в режим установки образа.</span><span class="sxs-lookup"><span data-stu-id="587a0-179">If your device isn't detected, follow these steps to put it into flashing mode:</span></span>

1. <span data-ttu-id="587a0-180">Отсоедините устройство от всех источников питания.</span><span class="sxs-lookup"><span data-stu-id="587a0-180">Unplug the device from any power source.</span></span>
1. <span data-ttu-id="587a0-181">Если устройство включено, нажмите и удерживайте кнопку **питания**, пока оно полностью не выключится.</span><span class="sxs-lookup"><span data-stu-id="587a0-181">If the device is on, hold down the **power** button until it completely turns off.</span></span>
2. <span data-ttu-id="587a0-182">Нажмите и удерживайте кнопку **увеличения громкости**, а затем кратковременно нажмите **кнопку питания**.</span><span class="sxs-lookup"><span data-stu-id="587a0-182">Hold the **volume up** button, and briefly tap the **power** button.</span></span> <span data-ttu-id="587a0-183">Устройство запустится, и отобразится только средний светодиодный индикатор.</span><span class="sxs-lookup"><span data-stu-id="587a0-183">The device should start and display only the middle LED light.</span></span>
3. <span data-ttu-id="587a0-184">Подключите устройство к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="587a0-184">Plug the device into your PC.</span></span>
4. <span data-ttu-id="587a0-185">Откройте Windows Device Recovery Tool.</span><span class="sxs-lookup"><span data-stu-id="587a0-185">Open the Windows Device Recovery Tool.</span></span>
5. <span data-ttu-id="587a0-186">Выберите **Мое устройство не обнаружено**, а затем— **HoloLens**.</span><span class="sxs-lookup"><span data-stu-id="587a0-186">Select **My device was not detected** and then **HoloLens**.</span></span> 
6. <span data-ttu-id="587a0-187">Следуйте инструкциям для восстановления устройства</span><span class="sxs-lookup"><span data-stu-id="587a0-187">Follow the instructions to recover your device.</span></span>
