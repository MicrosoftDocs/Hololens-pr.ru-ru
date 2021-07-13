---
title: HoloLens Устранение неполадок устройства
description: следите за наиболее распространенными решениями HoloLens проблем с устройствами и методов устранения неполадок.
author: mattzmsft
ms.author: mazeller
ms.date: 12/02/2019
ms.prod: hololens
ms.topic: article
audience: HoloLens
ms.localizationpriority: medium
manager: jarrettr
ms.custom:
- CI 111456
- CSSTroubleshooting
keywords: проблемы, ошибка, устранение неполадок, исправление, справка, поддержка, HoloLens, эмулятор
ms.openlocfilehash: b07514e73e43d267aa856c0fb9a256448e565000
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113635455"
---
# <a name="device-troubleshooting"></a><span data-ttu-id="de9a3-104">Устранение неполадок устройства</span><span class="sxs-lookup"><span data-stu-id="de9a3-104">Device Troubleshooting</span></span>

<span data-ttu-id="de9a3-105">в этой статье описывается решение некоторых распространенных проблем HoloLens.</span><span class="sxs-lookup"><span data-stu-id="de9a3-105">This article describes how to resolve several common HoloLens issues.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="de9a3-106">Прежде чем приступать к устранению неполадок, убедитесь, что на устройстве установлено значение от **20 до 40 процентов** от аккумулятора, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="de9a3-106">Before you start any troubleshooting procedure, make sure that your device is charged to **20 to 40 percent** of battery capacity, if possible.</span></span> <span data-ttu-id="de9a3-107">[Индикаторы батареи](hololens2-setup.md#lights-that-indicate-the-battery-level) , расположенные под кнопкой питания, позволяют быстро проверить емкость батареи без входа на устройство.</span><span class="sxs-lookup"><span data-stu-id="de9a3-107">The [battery indicator lights](hololens2-setup.md#lights-that-indicate-the-battery-level) located under the power button are a quick way to verify the battery capacity without logging into the device.</span></span>

<a id="list"></a>

<span data-ttu-id="de9a3-108">**Известные проблемы**</span><span class="sxs-lookup"><span data-stu-id="de9a3-108">**Known Issues**</span></span>
- [<span data-ttu-id="de9a3-109">Видео удаленного помощника зависает через 20 минут</span><span class="sxs-lookup"><span data-stu-id="de9a3-109">Remote Assist video freezes after 20 minutes</span></span>](#remote-assist-video-freezes-after-20-minutes)
- [<span data-ttu-id="de9a3-110">Автоматический вход с запросом на вход</span><span class="sxs-lookup"><span data-stu-id="de9a3-110">Auto-login asks for log-in</span></span>](#auto-login-asks-for-log-in)
- [<span data-ttu-id="de9a3-111">не удается запустить Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="de9a3-111">Microsoft Edge fails to launch</span></span>](#microsoft-edge-fails-to-launch)
- [<span data-ttu-id="de9a3-112">Клавиатура не переключается на специальные символы</span><span class="sxs-lookup"><span data-stu-id="de9a3-112">Keyboard doesn't switch to special characters</span></span>](#keyboard-doesnt-switch-to-special-characters)
- [<span data-ttu-id="de9a3-113">При скачивании заблокированных файлов не отображается сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="de9a3-113">Downloading locked files doesn't show error</span></span>](#downloading-locked-files-doesnt-error)
- [<span data-ttu-id="de9a3-114">Время ожидания отправки или скачивания файла на портале устройств истекло</span><span class="sxs-lookup"><span data-stu-id="de9a3-114">Device Portal file upload/download times out</span></span>](#device-portal-file-uploaddownload-times-out)
- [<span data-ttu-id="de9a3-115">Синий экран после отмены регистрации в предварительной версии программы предварительной оценки на устройстве, на котором произошла Пробная сборка</span><span class="sxs-lookup"><span data-stu-id="de9a3-115">Blue screen after unenrolling from Insider preview on a device flashed with an Insider build</span></span>](#blue-screen-after-unenrolling-from-insider-preview-on-a-device-flashed-with-an-insider-build)
- [<span data-ttu-id="de9a3-116">OneDrive не отправляет изображения автоматически</span><span class="sxs-lookup"><span data-stu-id="de9a3-116">OneDrive doesn't automatically upload pictures</span></span>](#onedrive-doesnt-automatically-upload-pictures)

<span data-ttu-id="de9a3-117">**Общие сведения**</span><span class="sxs-lookup"><span data-stu-id="de9a3-117">**General**</span></span>
- [<span data-ttu-id="de9a3-118">HoloLens не отвечает или не запускается</span><span class="sxs-lookup"><span data-stu-id="de9a3-118">HoloLens is unresponsive or won't start</span></span>](#hololens-is-unresponsive-or-wont-start)
- [<span data-ttu-id="de9a3-119">Ошибка "недостаточно места на диске"</span><span class="sxs-lookup"><span data-stu-id="de9a3-119">"Low Disk Space" error</span></span>](#low-disk-space-error)
- [<span data-ttu-id="de9a3-120">Сбой калибровки</span><span class="sxs-lookup"><span data-stu-id="de9a3-120">Calibration Fails</span></span>](#calibration-fails)
- [<span data-ttu-id="de9a3-121">не удается выполнить вход, поскольку мои HoloLens были ранее настроены для кого-то другого</span><span class="sxs-lookup"><span data-stu-id="de9a3-121">Can't sign in because my HoloLens was previously set up for someone else</span></span>](#cant-sign-in-because-my-hololens-was-previously-set-up-for-someone-else)
- [<span data-ttu-id="de9a3-122">Unity не работает</span><span class="sxs-lookup"><span data-stu-id="de9a3-122">Unity isn't working</span></span>](#unity-isnt-working)
- [<span data-ttu-id="de9a3-123">Windows Портал устройств работает неправильно</span><span class="sxs-lookup"><span data-stu-id="de9a3-123">Windows Device Portal isn't working correctly</span></span>](#windows-device-portal-isnt-working-correctly)
- [<span data-ttu-id="de9a3-124">Emulator HoloLens не работает</span><span class="sxs-lookup"><span data-stu-id="de9a3-124">The HoloLens Emulator isn't working</span></span>](#the-hololens-emulator-isnt-working)

<span data-ttu-id="de9a3-125">**Ввод**</span><span class="sxs-lookup"><span data-stu-id="de9a3-125">**Input**</span></span>
- [<span data-ttu-id="de9a3-126">Команды Voice не работают</span><span class="sxs-lookup"><span data-stu-id="de9a3-126">Voice commands aren't working</span></span>](#voice-commands-arent-working)
- [<span data-ttu-id="de9a3-127">Ввод с руки не работает</span><span class="sxs-lookup"><span data-stu-id="de9a3-127">Hand input isn't working</span></span>](#hand-input-isnt-working)

<span data-ttu-id="de9a3-128">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="de9a3-128">**Connectivity**</span></span>
- [<span data-ttu-id="de9a3-129">Не удается подключиться к Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="de9a3-129">Can't connect to Wi-Fi</span></span>](#cant-connect-to-wi-fi)

<span data-ttu-id="de9a3-130">**Внешние устройства**</span><span class="sxs-lookup"><span data-stu-id="de9a3-130">**External Devices**</span></span> 
- [<span data-ttu-id="de9a3-131">Bluetooth устройства не связаны</span><span class="sxs-lookup"><span data-stu-id="de9a3-131">Bluetooth devices aren't pairing</span></span>](#bluetooth-devices-arent-pairing)
- [<span data-ttu-id="de9a3-132">Микрофон USB-C не работает</span><span class="sxs-lookup"><span data-stu-id="de9a3-132">USB-C Microphone isn't working</span></span>](#usb-c-microphone-isnt-working)
- [<span data-ttu-id="de9a3-133">устройства, перечисленные как доступные в Параметры не работают</span><span class="sxs-lookup"><span data-stu-id="de9a3-133">Devices listed as available in Settings don't work</span></span>](#devices-listed-as-available-in-settings-dont-work)

## <a name="remote-assist-video-freezes-after-20-minutes"></a><span data-ttu-id="de9a3-134">Видео удаленного помощника зависает через 20 минут</span><span class="sxs-lookup"><span data-stu-id="de9a3-134">Remote Assist video freezes after 20 minutes</span></span>

> [!NOTE]
> <span data-ttu-id="de9a3-135">Существует более новая версия удаленного помощника, которая содержит исправление для этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="de9a3-135">There is a newer version of Remote Assist which has a fix for this issue.</span></span> <span data-ttu-id="de9a3-136">[Обновите удаленный помощник](holographic-store-apps.md#update-apps) до последней версии, чтобы избежать этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="de9a3-136">Please [update Remote Assist](holographic-store-apps.md#update-apps) to the latest version to avoid this issue.</span></span>

> [!NOTE]
> <span data-ttu-id="de9a3-137">в связи с серьезностью известных проблем мы временно приостановили доступность Windows holographic, версии 21H1.</span><span class="sxs-lookup"><span data-stu-id="de9a3-137">Due to this Known Issue's severity we had temporarily paused the availability of Windows Holographic, version 21H1.</span></span> <span data-ttu-id="de9a3-138">Сборка 21H1 теперь доступна снова, поэтому устройства могут снова обновиться до последней сборки 21H1.</span><span class="sxs-lookup"><span data-stu-id="de9a3-138">The 21H1 build is now available again, so devices may once again be updated to the latest 21H1 build.</span></span>

<span data-ttu-id="de9a3-139">в последнем выпуске [Windows с версией 21H1 holographic](hololens-release-notes.md#windows-holographic-version-21h1), некоторые пользователи удаленного помощника столкнулись с зависанием видео во время вызовов более 20 минут.</span><span class="sxs-lookup"><span data-stu-id="de9a3-139">On the latest release of [Windows Holographic, version 21H1](hololens-release-notes.md#windows-holographic-version-21h1), some users of Remote Assist have experienced video freezing during calls over 20 minutes.</span></span> <span data-ttu-id="de9a3-140">Это **известная проблема**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-140">This is a **known issue**.</span></span>

### <a name="workarounds"></a><span data-ttu-id="de9a3-141">Методы обхода проблемы</span><span class="sxs-lookup"><span data-stu-id="de9a3-141">Workarounds</span></span>

<span data-ttu-id="de9a3-142">Если не удается обновить удаленную помощь на более новую сборку, попробуйте выполнить следующие обходные изменения.</span><span class="sxs-lookup"><span data-stu-id="de9a3-142">If you are unable to update Remote Assist to a newer build try the following work around.</span></span>

#### <a name="restart-in-between-calls"></a><span data-ttu-id="de9a3-143">Перезапускаться между вызовами</span><span class="sxs-lookup"><span data-stu-id="de9a3-143">Restart in between calls</span></span>

<span data-ttu-id="de9a3-144">Если ваши звонки преобразуются в течение 20 минут и возникла эта проблема, попробуйте перезагрузить устройство.</span><span class="sxs-lookup"><span data-stu-id="de9a3-144">If your calls are going over a length of 20 minutes and you are experiencing this issue, try rebooting your device.</span></span> <span data-ttu-id="de9a3-145">После перезагрузки устройства между вызовами удаленного помощника устройство будет обновлено и переведено в хорошее состояние.</span><span class="sxs-lookup"><span data-stu-id="de9a3-145">Rebooting your device between Remote Assist calls will refresh your device and put it back into a good state.</span></span>

<span data-ttu-id="de9a3-146">чтобы быстро перезапустить устройство на [Windows holographic, 21H1 версии](hololens-release-notes.md#windows-holographic-version-21h1) , откройте меню "пуск" и выберите значок "пользователь", а затем щелкните " **перезапустить**".</span><span class="sxs-lookup"><span data-stu-id="de9a3-146">To quickly restart a device on [Windows Holographic, version 21H1](hololens-release-notes.md#windows-holographic-version-21h1) open the start menu, and select the user icon, then select **Restart**.</span></span>

[<span data-ttu-id="de9a3-147">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-147">Back to list</span></span>](#list)

## <a name="auto-login-asks-for-log-in"></a><span data-ttu-id="de9a3-148">Автоматический вход с запросом на вход</span><span class="sxs-lookup"><span data-stu-id="de9a3-148">Auto-login asks for log-in</span></span>

<span data-ttu-id="de9a3-149">устройство HoloLens 2 можно настроить для автоматического входа в систему через   ->  **учетные записи** Параметры  ->  **параметры входа в систему** — > и в разделе **обязательно** установите значение **никогда**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-149">A HoloLens 2 device can be configured to automatically login in via **Settings** -> **Accounts** -> **Sign-in Options** -> and under **Required** setting the value to **Never**.</span></span> <span data-ttu-id="de9a3-150">При обновлении устройства с существенно большим обновлением, например с обновлением компонентов, некоторым пользователям может потребоваться повторное подключение к устройству.</span><span class="sxs-lookup"><span data-stu-id="de9a3-150">Some users may be required to log-in to the device again when updating a device with a substantially large update, such as a feature update.</span></span> <span data-ttu-id="de9a3-151">Это **известная проблема**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-151">This is a **known issue**.</span></span>

<span data-ttu-id="de9a3-152">Пример, когда это может произойти:</span><span class="sxs-lookup"><span data-stu-id="de9a3-152">Example of when this could occur:</span></span>

- <span data-ttu-id="de9a3-153">обновление устройства с Windows holographic, версия 2004 (сборка 19041. xxxx) до Windows holographic, версия 21H1 (сборка 20346. xxxx)</span><span class="sxs-lookup"><span data-stu-id="de9a3-153">Updating a device from Windows Holographic, version 2004 (Build 19041.xxxx) to Windows Holographic, version 21H1 (Build 20346.xxxx)</span></span>
- <span data-ttu-id="de9a3-154">обновление устройства для выполнения большого обновления одной и той же основной сборки, например Windows holographic, версии 2004 до Windows holographic, версия 20H2</span><span class="sxs-lookup"><span data-stu-id="de9a3-154">Updating a device to take a large update on the same major build, e.g. Windows Holographic, version 2004 to Windows Holographic, version 20H2</span></span>
- <span data-ttu-id="de9a3-155">Обновление устройства с образа фабрики до последнего образа</span><span class="sxs-lookup"><span data-stu-id="de9a3-155">Updating a device from a factory image to the latest image</span></span>

<span data-ttu-id="de9a3-156">Это не должно происходить во время:</span><span class="sxs-lookup"><span data-stu-id="de9a3-156">This should not occur during:</span></span>

- <span data-ttu-id="de9a3-157">Устройства, которые занимают ежемесячное обновление</span><span class="sxs-lookup"><span data-stu-id="de9a3-157">Devices taking a monthly servicing update</span></span>

<span data-ttu-id="de9a3-158">Обойти методы:</span><span class="sxs-lookup"><span data-stu-id="de9a3-158">Work around methods:</span></span>

- <span data-ttu-id="de9a3-159">Такие методы входа, как ПИН-код, пароль, IRI, веб-аутентификация или ключи FIDO2.</span><span class="sxs-lookup"><span data-stu-id="de9a3-159">Sign-in methods such as PIN, Password, Iris, Web Authentication, or FIDO2 keys.</span></span>
- <span data-ttu-id="de9a3-160">Если ПИН-код устройства не удается запомнить и другие методы проверки подлинности недоступны, пользователь может использовать [режим ручной](hololens-recovery.md#manual-procedure)записи.</span><span class="sxs-lookup"><span data-stu-id="de9a3-160">If device PIN cannot be remembered, and other authentication methods are not available, then a user can use [manual reflashing mode](hololens-recovery.md#manual-procedure).</span></span>

[<span data-ttu-id="de9a3-161">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-161">Back to list</span></span>](#list)

## <a name="microsoft-edge-fails-to-launch"></a><span data-ttu-id="de9a3-162">не удается запустить Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="de9a3-162">Microsoft Edge fails to launch</span></span>

> [!NOTE]
> <span data-ttu-id="de9a3-163">эта проблема была изначально создана с помощью Microsoft Edgeной версии.</span><span class="sxs-lookup"><span data-stu-id="de9a3-163">This issue was originally created with the shipping version of Microsoft Edge in-mind.</span></span> <span data-ttu-id="de9a3-164">Эту проблему можно устранить в [новой Microsoft Edge](hololens-new-edge.md).</span><span class="sxs-lookup"><span data-stu-id="de9a3-164">This issue may be resolved in the [new Microsoft Edge](hololens-new-edge.md).</span></span> <span data-ttu-id="de9a3-165">Если это не так, оставьте отзыв о файле.</span><span class="sxs-lookup"><span data-stu-id="de9a3-165">If it is not, please file feedback.</span></span>

<span data-ttu-id="de9a3-166">некоторые клиенты сообщили о проблемах, когда не удается запустить Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="de9a3-166">A few customers have reported an issue where Microsoft Edge fails to launch.</span></span> <span data-ttu-id="de9a3-167">для этих клиентов проблема сохраняется при перезагрузке и не разрешается с помощью Windows или обновлений приложения.</span><span class="sxs-lookup"><span data-stu-id="de9a3-167">For these customers, the issue persists through reboot and is not resolved with Windows or application updates.</span></span> <span data-ttu-id="de9a3-168">если у вас возникла эта проблема и вы подтвердили, что [Windows актуальна](hololens-updates.md#manually-check-for-updates), зарегистрируйте ошибку в [приложении "центр отзывов](hololens-feedback.md) " со следующей категорией и подкатегорией: установка и обновление > скачивание, установка и настройка Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="de9a3-168">If you're experiencing this issue and you've confirmed [Windows is up-to-date](hololens-updates.md#manually-check-for-updates), please file a bug from the [Feedback Hub app](hololens-feedback.md) with the following category and sub-category: Install and Update > Downloading, installing, and configuring Windows Update.</span></span>

<span data-ttu-id="de9a3-169">Нет известных обходных путей, так как мы не можем устранить проблему до сих пор.</span><span class="sxs-lookup"><span data-stu-id="de9a3-169">There are no known workarounds as we've been unable to root cause the issue so far.</span></span> <span data-ttu-id="de9a3-170">С помощью центра обратной связи вы сможете исследовать ошибку.</span><span class="sxs-lookup"><span data-stu-id="de9a3-170">Filing a bug via Feedback Hub will help our investigation!</span></span> <span data-ttu-id="de9a3-171">Это **известная проблема**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-171">This is a **known issue**.</span></span>

[<span data-ttu-id="de9a3-172">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-172">Back to list</span></span>](#list)

## <a name="keyboard-doesnt-switch-to-special-characters"></a><span data-ttu-id="de9a3-173">Клавиатура не переключается на специальные символы</span><span class="sxs-lookup"><span data-stu-id="de9a3-173">Keyboard doesn't switch to special characters</span></span>

<span data-ttu-id="de9a3-174">Возникла ошибка во время OOBE, когда пользователь выбрал рабочую или учебную учетную запись и вводит пароль, при попытке переключиться на специальные символы на клавиатуре, коснувшись кнопки &123 не меняется на специальные символы.</span><span class="sxs-lookup"><span data-stu-id="de9a3-174">There is an issue during OOBE, where once the user has chosen a work or school account and is entering their password, trying to switch to the special characters on the keyboard by tapping the &123 button does not change to special characters.</span></span> <span data-ttu-id="de9a3-175">Это **известная проблема**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-175">This is a **known issue**.</span></span>

<span data-ttu-id="de9a3-176">Обходные решения:</span><span class="sxs-lookup"><span data-stu-id="de9a3-176">Work-arounds:</span></span>
-   <span data-ttu-id="de9a3-177">Закройте клавиатуру и снова откройте ее, коснувшись текстового поля.</span><span class="sxs-lookup"><span data-stu-id="de9a3-177">Close the keyboard and reopen it by tapping the text field.</span></span>
-   <span data-ttu-id="de9a3-178">Неправильно введите пароль.</span><span class="sxs-lookup"><span data-stu-id="de9a3-178">Incorrectly enter your password.</span></span> <span data-ttu-id="de9a3-179">Когда клавиатура перезапускается в следующий раз, она будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="de9a3-179">When the keyboard is relaunched next time it will then work as expected.</span></span>
- <span data-ttu-id="de9a3-180">Веб-Аутентификация, закройте клавиатуру и выберите **Вход с другого устройства**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-180">Web Authentication, close the keyboard and select **Sign in from another device**.</span></span>
-   <span data-ttu-id="de9a3-181">При вводе только чисел пользователь может нажать и удерживать определенные клавиши, чтобы открыть развернутое меню.</span><span class="sxs-lookup"><span data-stu-id="de9a3-181">If entering only numbers, a user may press and hold certain keys to open an expanded menu.</span></span>
-   <span data-ttu-id="de9a3-182">С помощью клавиатуры USB.</span><span class="sxs-lookup"><span data-stu-id="de9a3-182">Using a USB keyboard.</span></span>

<span data-ttu-id="de9a3-183">Это не влияет на:</span><span class="sxs-lookup"><span data-stu-id="de9a3-183">This does not affect:</span></span>
- <span data-ttu-id="de9a3-184">Пользователи, которые используют личную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="de9a3-184">Users who choose to use a personal account.</span></span>

[<span data-ttu-id="de9a3-185">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-185">Back to list</span></span>](#list)

## <a name="downloading-locked-files-doesnt-error"></a><span data-ttu-id="de9a3-186">Загрузка заблокированных файлов не является ошибкой</span><span class="sxs-lookup"><span data-stu-id="de9a3-186">Downloading locked files doesn't error</span></span>

> [!NOTE]
> <span data-ttu-id="de9a3-187">это **известная проблема** , которая исправлена в Windows сборке Insider, версия 20348,1403.</span><span class="sxs-lookup"><span data-stu-id="de9a3-187">This is a **known issue** that is fixed in Windows Insider build, version 20348.1403.</span></span>

<span data-ttu-id="de9a3-188">в предыдущих сборках Windows holographic при попытке загрузить заблокированный файл результатом будет страница ошибки HTTP.</span><span class="sxs-lookup"><span data-stu-id="de9a3-188">In previous builds of Windows Holographic, when attempting to download a locked file, the result would be an HTTP error page.</span></span> <span data-ttu-id="de9a3-189">в обновлении Windows holographic, version 21H1, попытка загрузить заблокированный файл приведет к незаметному отображению файла — файл не скачивается, и нет ошибок.</span><span class="sxs-lookup"><span data-stu-id="de9a3-189">In the Windows Holographic, version 21H1 update, trying to download a locked file results in nothing visible happening—the file doesn’t download and there’s no error.</span></span>

[<span data-ttu-id="de9a3-190">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-190">Back to list</span></span>](#list)

## <a name="device-portal-file-uploaddownload-times-out"></a><span data-ttu-id="de9a3-191">Время ожидания отправки или скачивания файла на портале устройств истекло</span><span class="sxs-lookup"><span data-stu-id="de9a3-191">Device Portal file upload/download times out</span></span>
> [!NOTE]
> <span data-ttu-id="de9a3-192">это **известная проблема** , которая исправлена в Windows сборке Insider, версия 20348,1403.</span><span class="sxs-lookup"><span data-stu-id="de9a3-192">This is a **known issue** that is fixed in Windows Insider build, version 20348.1403.</span></span> <span data-ttu-id="de9a3-193">Если вы ранее отключили SSL-подключение в рамках обходного пути, мы настоятельно рекомендуем повторно включить его.</span><span class="sxs-lookup"><span data-stu-id="de9a3-193">If you previously disabled SSL Connection as part of the workaround, we highly recommend you re-enable it.</span></span>


<span data-ttu-id="de9a3-194">Некоторые клиенты обнаружили, что при попытке отправить или скачать файлы может показаться, что операция зависает, а затем истекает или не завершится.</span><span class="sxs-lookup"><span data-stu-id="de9a3-194">Some customers have found, when attempting to upload or download files, the operation might appear to hang and then time out or never complete.</span></span> <span data-ttu-id="de9a3-195">это отделено от[известной проблемы "файл заблокирована"](#downloading-locked-files-doesnt-error) — это влияет Windows holographic, версии 2004, 20H2 и 21H1 в сборках на рынке.</span><span class="sxs-lookup"><span data-stu-id="de9a3-195">This is separate from the '[file locked' known issue](#downloading-locked-files-doesnt-error) -- this affects Windows Holographic, versions 2004, 20H2 and 21H1 in-market builds.</span></span> <span data-ttu-id="de9a3-196">Проблема была вызвана ошибкой в обработке определенных запросов на портале устройств, и при использовании протокола HTTPS это происходит чаще всего, чем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="de9a3-196">The problem has been root caused to a bug in Device Portal's handling of certain requests, and is most consistently hit when using https, which is the default.</span></span> 

### <a name="workaround"></a><span data-ttu-id="de9a3-197">Обходной путь</span><span class="sxs-lookup"><span data-stu-id="de9a3-197">Workaround</span></span>

<span data-ttu-id="de9a3-198">Этот обходной путь, который применяется поровну к Wi-Fi и Усбнкм, — отключение параметра Required в разделе "SSL-соединение".</span><span class="sxs-lookup"><span data-stu-id="de9a3-198">This workaround, which applies equally to Wi-Fi and UsbNcm, is to disable the "required" option under "SSL Connection".</span></span> <span data-ttu-id="de9a3-199">Для этого перейдите на портал устройств, **систему** и выберите страницу **предпочтения** .</span><span class="sxs-lookup"><span data-stu-id="de9a3-199">To do so, navigate to Device Portal, **System**, and select the **Preferences** page.</span></span> <span data-ttu-id="de9a3-200">В разделе " **безопасность устройства** " выберите **SSL-подключение** и снимите флажок " **требуется** отключить".</span><span class="sxs-lookup"><span data-stu-id="de9a3-200">In the **Device Security** section, locate **SSL Connection**, and uncheck to disable **Required**.</span></span>

<span data-ttu-id="de9a3-201">После этого пользователь переходит в http://, а не https://(IP-адрес) и такие функции, как отправка и загрузка файлов, будут работать.</span><span class="sxs-lookup"><span data-stu-id="de9a3-201">The user should then go to http://, not https:// (IP address) and features like file upload and download will work.</span></span>

[<span data-ttu-id="de9a3-202">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-202">Back to list</span></span>](#list)

## <a name="blue-screen-after-unenrolling-from-insider-preview-on-a-device-flashed-with-an-insider-build"></a><span data-ttu-id="de9a3-203">Синий экран после отмены регистрации в предварительной версии программы предварительной оценки на устройстве, на котором произошла Пробная сборка</span><span class="sxs-lookup"><span data-stu-id="de9a3-203">Blue screen after unenrolling from Insider preview on a device flashed with an Insider build</span></span>

<span data-ttu-id="de9a3-204">это проблема, влияющая на то, что влияет на пользователей, которые были включены в предварительную версию сборки, а также активировала их HoloLens 2 с новой сборкой предварительной версии insider, а затем отменяя регистрацию в программе предварительной оценки.</span><span class="sxs-lookup"><span data-stu-id="de9a3-204">This is an issue affecting that affects users who are were on an Insider preview build, reflashed their HoloLens 2 with a new insider preview build, and then unenrolled from the Insider program.</span></span> <span data-ttu-id="de9a3-205">Это **известная проблема**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-205">This is a **known issue**.</span></span>

<span data-ttu-id="de9a3-206">Это не влияет на:</span><span class="sxs-lookup"><span data-stu-id="de9a3-206">This does not affect:</span></span>
- <span data-ttu-id="de9a3-207">пользователи, не зарегистрированные в Windowsной программе предварительной оценки</span><span class="sxs-lookup"><span data-stu-id="de9a3-207">Users who are not enrolled in Windows Insider</span></span> 
- <span data-ttu-id="de9a3-208">Предварительной оценки</span><span class="sxs-lookup"><span data-stu-id="de9a3-208">Insiders:</span></span>
    - <span data-ttu-id="de9a3-209">Если устройство было зарегистрировано, так как сборка Insider имеет версию 18362. x</span><span class="sxs-lookup"><span data-stu-id="de9a3-209">If a device has been enrolled since Insider builds were version 18362.x</span></span>
    - <span data-ttu-id="de9a3-210">Если они закрывают сборку с подписью 19041. x и не зарегистрированы в программе предварительной оценки</span><span class="sxs-lookup"><span data-stu-id="de9a3-210">If they flashed an Insider signed 19041.x build AND stay enrolled in the Insider program</span></span>

<span data-ttu-id="de9a3-211">Обходное решение:</span><span class="sxs-lookup"><span data-stu-id="de9a3-211">Work-around:</span></span> 
- <span data-ttu-id="de9a3-212">Избежание проблемы</span><span class="sxs-lookup"><span data-stu-id="de9a3-212">Avoid the issue</span></span> 
    - <span data-ttu-id="de9a3-213">Вспышка сборки без предварительной оценки.</span><span class="sxs-lookup"><span data-stu-id="de9a3-213">Flash a non-insider build.</span></span> <span data-ttu-id="de9a3-214">Одно из регулярных ежемесячных обновлений.</span><span class="sxs-lookup"><span data-stu-id="de9a3-214">One of the regular monthly updates.</span></span>
    - <span data-ttu-id="de9a3-215">Будьте в курсе событий предварительной версии</span><span class="sxs-lookup"><span data-stu-id="de9a3-215">Stay on Insider Preview</span></span>
- <span data-ttu-id="de9a3-216">Восмигать устройство</span><span class="sxs-lookup"><span data-stu-id="de9a3-216">Reflash the device</span></span>

    1. <span data-ttu-id="de9a3-217">переведите [HoloLens 2 в мигающий режим](hololens-recovery.md) вручную, полностью выключая питание, не подключаясь.</span><span class="sxs-lookup"><span data-stu-id="de9a3-217">Put the [HoloLens 2 into flashing mode](hololens-recovery.md) manually by fully powering down while not connect.</span></span> <span data-ttu-id="de9a3-218">Затем при удерживании громкости нажмите кнопку питания.</span><span class="sxs-lookup"><span data-stu-id="de9a3-218">Then while holding Volume up, tap the Power button.</span></span>
    
    1. <span data-ttu-id="de9a3-219">Подключение пк и откройте расширенный помощник по восстановлению.</span><span class="sxs-lookup"><span data-stu-id="de9a3-219">Connect to the PC and open Advanced Recovery Companion.</span></span>
    
    1. <span data-ttu-id="de9a3-220">вспышка HoloLens 2 к сборке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="de9a3-220">Flash the HoloLens 2 to the default build.</span></span>

[<span data-ttu-id="de9a3-221">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-221">Back to list</span></span>](#list)

## <a name="onedrive-doesnt-automatically-upload-pictures"></a><span data-ttu-id="de9a3-222">OneDrive не отправляет изображения автоматически</span><span class="sxs-lookup"><span data-stu-id="de9a3-222">OneDrive doesn't automatically upload pictures</span></span>

<span data-ttu-id="de9a3-223">OneDriveное приложение для HoloLens не поддерживает автоматическую отправку камеры для рабочих или учебных учетных записей.</span><span class="sxs-lookup"><span data-stu-id="de9a3-223">The OneDrive app for HoloLens does not support automatic camera upload for work or school accounts.</span></span> <span data-ttu-id="de9a3-224">Это **известная проблема**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-224">This is a **known issue**.</span></span>

<span data-ttu-id="de9a3-225">Решения.</span><span class="sxs-lookup"><span data-stu-id="de9a3-225">Workarounds:</span></span>

- <span data-ttu-id="de9a3-226">Если это возможно для вашего бизнеса, то в учетных записях пользователей Майкрософт поддерживается автоматическая отправка камеры.</span><span class="sxs-lookup"><span data-stu-id="de9a3-226">If viable for your business, automatic camera upload is supported on consumer Microsoft accounts.</span></span> <span data-ttu-id="de9a3-227">вы можете войти в учетная запись Майкрософт в дополнение к рабочей или учебной учетной записи (приложение OneDrive поддерживает двойной вход).</span><span class="sxs-lookup"><span data-stu-id="de9a3-227">You can sign in to your Microsoft account in addition to your work or school account (the OneDrive app supports dual sign-in).</span></span> <span data-ttu-id="de9a3-228">из профиля учетная запись Майкрософт в OneDrive можно включить автоматическую отправку фоновой камеры.</span><span class="sxs-lookup"><span data-stu-id="de9a3-228">From your Microsoft account profile within OneDrive you can enable automatic, background camera roll upload.</span></span>

- <span data-ttu-id="de9a3-229">если вы не можете безопасно использовать потребительскую учетная запись Майкрософт для автоматической отправки фотографий, вы можете вручную отправить фотографии в рабочую или учебную учетную запись из приложения OneDrive.</span><span class="sxs-lookup"><span data-stu-id="de9a3-229">If you cannot safely use a consumer Microsoft account for uploading your photos automatically, you can manually upload photos to your work or school account from the OneDrive app.</span></span> <span data-ttu-id="de9a3-230">для этого убедитесь, что вы вошли в рабочую или учебную учетную запись в приложении OneDrive.</span><span class="sxs-lookup"><span data-stu-id="de9a3-230">To do that, make sure you're signed into your work or school account in the OneDrive app.</span></span> <span data-ttu-id="de9a3-231">Нажмите **+** кнопку и выберите **upload**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-231">Select the **+** button and choose **Upload**.</span></span> <span data-ttu-id="de9a3-232">Найдите фотографии или видео, которые вы хотите передать, перейдя к **рисунку > рулон камеры**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-232">Find the photos or videos you want to upload by navigating to **Pictures > Camera Roll**.</span></span> <span data-ttu-id="de9a3-233">Выберите фотографии или видео, которые нужно отправить, а затем нажмите кнопку **Открыть** .</span><span class="sxs-lookup"><span data-stu-id="de9a3-233">Select the photos or videos you want to upload, and then select the **Open** button.</span></span>

[<span data-ttu-id="de9a3-234">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-234">Back to list</span></span>](#list)

## <a name="hololens-is-unresponsive-or-wont-start"></a><span data-ttu-id="de9a3-235">HoloLens не отвечает или не запускается</span><span class="sxs-lookup"><span data-stu-id="de9a3-235">HoloLens is unresponsive or won't start</span></span>

<span data-ttu-id="de9a3-236">если HoloLens не запускается:</span><span class="sxs-lookup"><span data-stu-id="de9a3-236">If your HoloLens won't start:</span></span>

- <span data-ttu-id="de9a3-237">Если индикаторы рядом с кнопкой питания не имеют освещения или кратковременно мигает только один светодиодный индикатор, может потребоваться [плата за HoloLens.](hololens2-charging.md#charging-the-device)</span><span class="sxs-lookup"><span data-stu-id="de9a3-237">If the LEDs next to the power button don't light up, or only one LED briefly blinks, you may need to [charge your HoloLens.](hololens2-charging.md#charging-the-device)</span></span>
- <span data-ttu-id="de9a3-238">Если индикаторы будут освещены при нажатии кнопки питания, но на экране ничего не отображается, [выполните жесткий сброс устройства](hololens-recovery.md#hard-reset-procedure).</span><span class="sxs-lookup"><span data-stu-id="de9a3-238">If the LEDs light up when you press the power button but you can't see anything on the displays, [do a hard reset of the device](hololens-recovery.md#hard-reset-procedure).</span></span>

<span data-ttu-id="de9a3-239">если HoloLens зафиксирована или не отвечает:</span><span class="sxs-lookup"><span data-stu-id="de9a3-239">If your HoloLens becomes frozen or unresponsive:</span></span>

- <span data-ttu-id="de9a3-240">отключите HoloLens, нажав кнопку питания, пока все пять индикаторов не будут выключены, или 15 секунд, если индикаторы не отвечают.</span><span class="sxs-lookup"><span data-stu-id="de9a3-240">Turn off your HoloLens by pressing the power button until all five of the LEDs turn themselves off, or for 15 seconds if the LEDs are unresponsive.</span></span> <span data-ttu-id="de9a3-241">чтобы запустить HoloLens, снова нажмите кнопку питания.</span><span class="sxs-lookup"><span data-stu-id="de9a3-241">To start your HoloLens, press the power button again.</span></span>

<span data-ttu-id="de9a3-242">если эти действия не будут выполнены, можно попробовать [восстановить устройство HoloLens 2](hololens-recovery.md) или [HoloLens (1-го поколения).](hololens1-recovery.md)</span><span class="sxs-lookup"><span data-stu-id="de9a3-242">If these steps don't work, you can try [recovering your HoloLens 2 device](hololens-recovery.md) or [HoloLens (1st gen) device.](hololens1-recovery.md)</span></span>

[<span data-ttu-id="de9a3-243">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-243">Back to list</span></span>](#list)

## <a name="low-disk-space-error"></a><span data-ttu-id="de9a3-244">Ошибка "недостаточно места на диске"</span><span class="sxs-lookup"><span data-stu-id="de9a3-244">"Low Disk Space" error</span></span>

<span data-ttu-id="de9a3-245">Вам потребуется освободить дисковое пространство, выполнив одно или несколько из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="de9a3-245">You'll need to free up some storage space by doing one or more of the following:</span></span>

- <span data-ttu-id="de9a3-246">Удалите неиспользуемые пробелы.</span><span class="sxs-lookup"><span data-stu-id="de9a3-246">Delete some unused spaces.</span></span> <span data-ttu-id="de9a3-247">перейдите в раздел **Параметры**  >  **системные**  >  **пространства**, выберите ненужные пробелы и нажмите кнопку **удалить**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-247">Go to **Settings** > **System** > **Spaces**, select a space that you no longer need, and then select **Remove**.</span></span>
- <span data-ttu-id="de9a3-248">Удалите некоторые из размещенных голограмм.</span><span class="sxs-lookup"><span data-stu-id="de9a3-248">Remove some of the holograms that you've placed.</span></span>
- <span data-ttu-id="de9a3-249">Удалите некоторые изображения и видео из приложения "фотографии".</span><span class="sxs-lookup"><span data-stu-id="de9a3-249">Delete some pictures and videos from the Photos app.</span></span>
- <span data-ttu-id="de9a3-250">Удалите некоторые приложения из HoloLens.</span><span class="sxs-lookup"><span data-stu-id="de9a3-250">Uninstall some apps from your HoloLens.</span></span> <span data-ttu-id="de9a3-251">В списке **все приложения** выберите и удерживайте приложение, которое необходимо удалить, а затем нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-251">In the **All apps** list, tap and hold the app you want to uninstall, and then select **Uninstall**.</span></span>

[<span data-ttu-id="de9a3-252">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-252">Back to list</span></span>](#list)

## <a name="calibration-fails"></a><span data-ttu-id="de9a3-253">Сбой калибровки</span><span class="sxs-lookup"><span data-stu-id="de9a3-253">Calibration fails</span></span>

<span data-ttu-id="de9a3-254">Для большинства пользователей калибровка должна работать, но в некоторых случаях происходит сбой калибровки.</span><span class="sxs-lookup"><span data-stu-id="de9a3-254">Calibration should work for most people, but there are cases where calibration fails.</span></span>
  
<span data-ttu-id="de9a3-255">Ниже перечислены некоторые возможные причины сбоя калибровки.</span><span class="sxs-lookup"><span data-stu-id="de9a3-255">Some potential reasons for calibration failure include:</span></span>

- <span data-ttu-id="de9a3-256">Ненужные и не следующие цели калибровки</span><span class="sxs-lookup"><span data-stu-id="de9a3-256">Getting distracted and not following the calibration targets</span></span>
- <span data-ttu-id="de9a3-257">Неправильное расположение "грязного" или "ненормального" гипервизора устройства или гипервизора устройства</span><span class="sxs-lookup"><span data-stu-id="de9a3-257">Dirty or scratched device visor or device visor not positioned properly</span></span>
- <span data-ttu-id="de9a3-258">"Грязный" или "очков"</span><span class="sxs-lookup"><span data-stu-id="de9a3-258">Dirty or scratched glasses</span></span>
- <span data-ttu-id="de9a3-259">Некоторые типы контактов lenses и очков (цветные контакты lenses, некоторые Торик контакт lenses, ие IR очков, некоторые высокие очков, своему солнцезащитных очков или аналогичные).</span><span class="sxs-lookup"><span data-stu-id="de9a3-259">Certain types of contact lenses and glasses (colored contact lenses, some toric contact lenses, IR blocking glasses, some high prescription glasses, sunglasses, or similar)</span></span>
- <span data-ttu-id="de9a3-260">Более произносится описывающего и некоторые расширения эйелаш</span><span class="sxs-lookup"><span data-stu-id="de9a3-260">More-pronounced makeup and some eyelash extensions</span></span>
- <span data-ttu-id="de9a3-261">Перекрестные и толстые эйегласс кадры, если они блокируют устройство от глаза</span><span class="sxs-lookup"><span data-stu-id="de9a3-261">Hair or thick eyeglass frames if they're blocking the device from seeing your eyes</span></span>
- <span data-ttu-id="de9a3-262">Определенные фисиологи глаз, условия глаз или глаз хирургии, такие как узкие глаза, длинные эйелашес, амблйопиа, Нистагмус, некоторые случаи ЛАСИК или другого взгляда суржериес</span><span class="sxs-lookup"><span data-stu-id="de9a3-262">Certain eye physiology, eye conditions, or eye surgery such as narrow eyes, long eyelashes, amblyopia, nystagmus, some cases of LASIK or other eye surgeries</span></span>

<span data-ttu-id="de9a3-263">Если калибровка не будет выполнена, попробуйте:</span><span class="sxs-lookup"><span data-stu-id="de9a3-263">If calibration is unsuccessful try:</span></span>

- <span data-ttu-id="de9a3-264">Очистка аппаратного гипервизора устройства</span><span class="sxs-lookup"><span data-stu-id="de9a3-264">Cleaning your device visor</span></span>
- <span data-ttu-id="de9a3-265">Очистка очков</span><span class="sxs-lookup"><span data-stu-id="de9a3-265">Cleaning your glasses</span></span>
- <span data-ttu-id="de9a3-266">Принудительная передача гипервизора устройства</span><span class="sxs-lookup"><span data-stu-id="de9a3-266">Pushing your device visor as close to your eyes as possible</span></span>
- <span data-ttu-id="de9a3-267">Перемещение объектов на гипервизоре (например, волосы)</span><span class="sxs-lookup"><span data-stu-id="de9a3-267">Moving objects in your visor out of the way (such as hair)</span></span>
- <span data-ttu-id="de9a3-268">Включение освещения в комнате или переход с прямого солнечного света</span><span class="sxs-lookup"><span data-stu-id="de9a3-268">Turning on a light in your room or moving out of direct sunlight</span></span>

<span data-ttu-id="de9a3-269">если были выполнены все рекомендации и калибровка все еще не пройдена, можно отключить запрос на калибровку в Параметры.</span><span class="sxs-lookup"><span data-stu-id="de9a3-269">If you followed all guidelines and calibration is still failing, you can disable the calibration prompt in Settings.</span></span> <span data-ttu-id="de9a3-270">Кроме того, сообщите нам о наличии отзывов в [центре обратной связи](hololens-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="de9a3-270">Also let us know by filing feedback in [Feedback Hub](hololens-feedback.md).</span></span>

<span data-ttu-id="de9a3-271">См. также дополнительные сведения об [устранении неполадок цвета изображения или яркости.](hololens2-fit-comfort-faq.md#hologram-image-color-or-brightness-does-not-look-right)</span><span class="sxs-lookup"><span data-stu-id="de9a3-271">Also see related information for [image color or brightness troubleshooting.](hololens2-fit-comfort-faq.md#hologram-image-color-or-brightness-does-not-look-right)</span></span>

<span data-ttu-id="de9a3-272">установка IPD неприменима для HoloLens 2, так как положения глаз вычисляются системой.</span><span class="sxs-lookup"><span data-stu-id="de9a3-272">Setting IPD is not applicable for HoloLens 2, since eye positions are computed by the system.</span></span> 

[<span data-ttu-id="de9a3-273">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-273">Back to list</span></span>](#list)

## <a name="cant-sign-in-because-my-hololens-was-previously-set-up-for-someone-else"></a><span data-ttu-id="de9a3-274">не удается выполнить вход, поскольку мои HoloLens были ранее настроены для кого-то другого</span><span class="sxs-lookup"><span data-stu-id="de9a3-274">Can't sign in because my HoloLens was previously set up for someone else</span></span>

<span data-ttu-id="de9a3-275">Устройство можно [перевести в **мигающий режим** и использовать расширенный помощник по восстановлению](hololens-recovery.md#clean-reflash-the-device) для восстановления устройства.</span><span class="sxs-lookup"><span data-stu-id="de9a3-275">You can [put the device into **Flashing Mode** and use Advanced Recovery Companion](hololens-recovery.md#clean-reflash-the-device) to recover the device.</span></span>

[<span data-ttu-id="de9a3-276">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-276">Back to list</span></span>](#list)


## <a name="unity-isnt-working"></a><span data-ttu-id="de9a3-277">Unity не работает</span><span class="sxs-lookup"><span data-stu-id="de9a3-277">Unity isn't working</span></span>

- <span data-ttu-id="de9a3-278">см. статью [установка инструментов](/windows/mixed-reality/install-the-tools) для наиболее актуальной версии Unity, рекомендуемой для HoloLens разработки.</span><span class="sxs-lookup"><span data-stu-id="de9a3-278">See [Install the tools](/windows/mixed-reality/install-the-tools) for the most up-to-date version of Unity recommended for HoloLens development.</span></span>
- <span data-ttu-id="de9a3-279">известные проблемы с HoloLensной технической предварительной версией Unity описаны на [форумах HoloLens unity](https://forum.unity3d.com/threads/known-issues.394627/).</span><span class="sxs-lookup"><span data-stu-id="de9a3-279">Known issues with the Unity HoloLens Technical Preview are documented in the [HoloLens Unity forums](https://forum.unity3d.com/threads/known-issues.394627/).</span></span>

[<span data-ttu-id="de9a3-280">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-280">Back to list</span></span>](#list)

## <a name="windows-device-portal-isnt-working-correctly"></a><span data-ttu-id="de9a3-281">Windows Портал устройств работает неправильно</span><span class="sxs-lookup"><span data-stu-id="de9a3-281">Windows Device Portal isn't working correctly</span></span>

- <span data-ttu-id="de9a3-282">Функция интерактивной предварительной версии в записи смешанной реальности может демонстрировать несколько секунд задержки.</span><span class="sxs-lookup"><span data-stu-id="de9a3-282">The Live Preview feature in Mixed Reality capture may exhibit several seconds of latency.</span></span>

- <span data-ttu-id="de9a3-283">На странице Виртуальный ввод элементы управления жестом и прокруткой в разделе Виртуальные жесты не работают.</span><span class="sxs-lookup"><span data-stu-id="de9a3-283">On the Virtual Input page, the Gesture and Scroll controls under the Virtual Gestures section are not functional.</span></span> <span data-ttu-id="de9a3-284">Их использование не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="de9a3-284">Using them will have no effect.</span></span> <span data-ttu-id="de9a3-285">Виртуальная клавиатура на виртуальной странице ввода работает правильно.</span><span class="sxs-lookup"><span data-stu-id="de9a3-285">The virtual keyboard on the virtual input page works correctly.</span></span>

- <span data-ttu-id="de9a3-286">после включения режима разработчика в Параметры для включения портала устройств может потребоваться несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="de9a3-286">After enabling Developer Mode in Settings, it may take a few seconds before the switch to turn on the Device Portal is enabled.</span></span>

[<span data-ttu-id="de9a3-287">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-287">Back to list</span></span>](#list)

## <a name="the-hololens-emulator-isnt-working"></a><span data-ttu-id="de9a3-288">Emulator HoloLens не работает</span><span class="sxs-lookup"><span data-stu-id="de9a3-288">The HoloLens Emulator isn't working</span></span>

<span data-ttu-id="de9a3-289">сведения о эмуляторе HoloLens см. в документации разработчика.</span><span class="sxs-lookup"><span data-stu-id="de9a3-289">Information about the HoloLens emulator is located in our developer documentation.</span></span>  <span data-ttu-id="de9a3-290">дополнительные сведения см. [в статье устранение неполадок в эмуляторе HoloLens](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-hololens-emulator#troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="de9a3-290">Read more about [troubleshooting the HoloLens emulator](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-hololens-emulator#troubleshooting).</span></span>


- <span data-ttu-id="de9a3-291">не все приложения в Microsoft Store совместимы с эмулятором.</span><span class="sxs-lookup"><span data-stu-id="de9a3-291">Not all apps in the Microsoft Store are compatible with the emulator.</span></span> <span data-ttu-id="de9a3-292">Например, Конкеры Титов и фрагменты не работают в эмуляторе.</span><span class="sxs-lookup"><span data-stu-id="de9a3-292">For example, Young Conker and Fragments are not playable on the emulator.</span></span>
- <span data-ttu-id="de9a3-293">Вы не можете использовать веб-камеру на компьютере Emulator.</span><span class="sxs-lookup"><span data-stu-id="de9a3-293">You cannot use the PC webcam in the Emulator.</span></span>
- <span data-ttu-id="de9a3-294">функция интерактивной предварительной версии на портале устройств Windows не работает с эмулятором.</span><span class="sxs-lookup"><span data-stu-id="de9a3-294">The Live Preview feature of the Windows Device Portal does not work with the emulator.</span></span> <span data-ttu-id="de9a3-295">Вы по-прежнему можете записывать видео и изображения смешанной реальности.</span><span class="sxs-lookup"><span data-stu-id="de9a3-295">You can still capture Mixed Reality videos and images.</span></span>

[<span data-ttu-id="de9a3-296">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-296">Back to list</span></span>](#list)

## <a name="voice-commands-arent-working"></a><span data-ttu-id="de9a3-297">Команды Voice не работают</span><span class="sxs-lookup"><span data-stu-id="de9a3-297">Voice commands aren't working</span></span>

<span data-ttu-id="de9a3-298">если Кортана не отвечает на ваши голоса-команды, убедитесь, что Кортана включен.</span><span class="sxs-lookup"><span data-stu-id="de9a3-298">If Cortana isn't responding to your voice commands, make sure Cortana is turned on.</span></span> <span data-ttu-id="de9a3-299">в списке все приложения выберите **Кортана**  >  **меню**  >  **записная книжка**  >  **Параметры** , чтобы внести изменения.</span><span class="sxs-lookup"><span data-stu-id="de9a3-299">On the All apps list, select **Cortana** > **Menu** > **Notebook** > **Settings** to make changes.</span></span> <span data-ttu-id="de9a3-300">Дополнительные сведения о том, что можно сказать, см. в статье [использование голоса с HoloLens](hololens-cortana.md).</span><span class="sxs-lookup"><span data-stu-id="de9a3-300">To learn more about what you can say, see [Use your voice with HoloLens](hololens-cortana.md).</span></span>

<span data-ttu-id="de9a3-301">на HoloLens (первое поколение) встроенное распознавание речи не настраивается.</span><span class="sxs-lookup"><span data-stu-id="de9a3-301">On HoloLens (1st gen), built-in speech recognition is not configurable.</span></span> <span data-ttu-id="de9a3-302">Он всегда включен.</span><span class="sxs-lookup"><span data-stu-id="de9a3-302">It is always turned on.</span></span> <span data-ttu-id="de9a3-303">на HoloLens 2 можно включить распознавание речи и Кортана во время настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="de9a3-303">On HoloLens 2, you can choose whether to turn on both speech recognition and Cortana during device setup.</span></span>

<span data-ttu-id="de9a3-304">если HoloLens 2 не отвечает на ваш голос, убедитесь, что включено распознавание речи.</span><span class="sxs-lookup"><span data-stu-id="de9a3-304">If your HoloLens 2 is not responding to your voice, make sure Speech recognition is turned on.</span></span> <span data-ttu-id="de9a3-305">перейдите в раздел **Start**  >  **Параметры**  >  **конфиденциальность**  >  **речи** и включите **распознавание речи**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-305">Go to **Start** > **Settings** > **Privacy** > **Speech** and turn on **Speech recognition**.</span></span>

[<span data-ttu-id="de9a3-306">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-306">Back to list</span></span>](#list)

## <a name="hand-input-isnt-working"></a><span data-ttu-id="de9a3-307">Ввод с руки не работает</span><span class="sxs-lookup"><span data-stu-id="de9a3-307">Hand input isn't working</span></span>

<span data-ttu-id="de9a3-308">чтобы убедиться, что HoloLens могут видеть ваши руки, их необходимо разместить в кадре жеста.</span><span class="sxs-lookup"><span data-stu-id="de9a3-308">To ensure that HoloLens can see your hands, you need to keep them in the gesture frame.</span></span>  <span data-ttu-id="de9a3-309">Домашняя страница Mixed Reality предоставляет отзыв, который позволяет узнать, когда ваши руки будут отслеживанием.</span><span class="sxs-lookup"><span data-stu-id="de9a3-309">The Mixed Reality Home provides feedback that lets you know when your hands are tracked.</span></span>  <span data-ttu-id="de9a3-310">Отзывы отличаются в разных версиях HoloLens:</span><span class="sxs-lookup"><span data-stu-id="de9a3-310">The feedback is different on different versions of HoloLens:</span></span>
- <span data-ttu-id="de9a3-311">на HoloLens (1-й общий) курсор взгляда меняется с точки на кольцо</span><span class="sxs-lookup"><span data-stu-id="de9a3-311">On HoloLens (1st gen), the gaze cursor changes from a dot to a ring</span></span>
- <span data-ttu-id="de9a3-312">на HoloLens 2, когда рука находится близко к планшету, появляется курсор с изображением</span><span class="sxs-lookup"><span data-stu-id="de9a3-312">On HoloLens 2, a fingertip cursor appears when your hand is close to a slate, and a hand ray appears when slates are further away</span></span>

<span data-ttu-id="de9a3-313">Многие впечатляющие приложения следуют шаблонам ввода, похожим на "смешанная реальность".</span><span class="sxs-lookup"><span data-stu-id="de9a3-313">Many immersive apps follow input patterns that are similar to Mixed Reality Home.</span></span>  <span data-ttu-id="de9a3-314">дополнительные сведения об использовании ввода вручную для [HoloLens (1-го поколения)](hololens1-basic-usage.md#use-hololens-with-your-hands) и [HoloLens 2](hololens2-basic-usage.md#the-hand-tracking-frame).</span><span class="sxs-lookup"><span data-stu-id="de9a3-314">Learn more about using hand input on [HoloLens (1st gen)](hololens1-basic-usage.md#use-hololens-with-your-hands) and [HoloLens 2](hololens2-basic-usage.md#the-hand-tracking-frame).</span></span>

<span data-ttu-id="de9a3-315">Если вы людьми перчатки, обратите внимание, что некоторые типы перчатки не работают с отслеживанием вручную.</span><span class="sxs-lookup"><span data-stu-id="de9a3-315">If you are wearing gloves, note that some types of gloves do not work with hand tracking.</span></span>  <span data-ttu-id="de9a3-316">Распространенным примером является черный резиновой перчатки, который обычно применяет инфракрасное излучение и не забирается на камере глубины.</span><span class="sxs-lookup"><span data-stu-id="de9a3-316">A common example is black rubber gloves, which tend to absorb infrared light and are not picked up by the depth camera.</span></span>  <span data-ttu-id="de9a3-317">Если ваша работа включает резиновой перчатки, рекомендуется использовать более светлый цвет, например синий или серый.</span><span class="sxs-lookup"><span data-stu-id="de9a3-317">If your work involves rubber gloves, we recommend trying a lighter color such as blue or gray.</span></span>  <span data-ttu-id="de9a3-318">Еще один пример — крупный багги перчатки, который, как правило, скрывает форму руки.</span><span class="sxs-lookup"><span data-stu-id="de9a3-318">Another example is large baggy gloves, which tend to obscure the shape of your hand.</span></span> <span data-ttu-id="de9a3-319">Для получения наилучших результатов рекомендуется использовать перчатки, как можно лучше подгонка форм.</span><span class="sxs-lookup"><span data-stu-id="de9a3-319">We recommend using gloves that are as form-fitting as possible for best results.</span></span>

<span data-ttu-id="de9a3-320">если у гипервизора есть отпечатки пальца или палец, используйте чистящую ткань микрофибер, которая поставляется вместе с HoloLens для аккуратной очистки гипервизоров.</span><span class="sxs-lookup"><span data-stu-id="de9a3-320">If your visor has fingerprints or smudges, use the microfiber cleaning cloth that came with the HoloLens to clean your visor gently.</span></span>

[<span data-ttu-id="de9a3-321">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-321">Back to list</span></span>](#list)

## <a name="cant-connect-to-wi-fi"></a><span data-ttu-id="de9a3-322">Не удается подключиться к Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="de9a3-322">Can't connect to Wi-Fi</span></span>

<span data-ttu-id="de9a3-323">ниже приведены некоторые действия, которые следует предпринять, если не удается подключить HoloLens к Wi-Fiной сети.</span><span class="sxs-lookup"><span data-stu-id="de9a3-323">Here are some things to try if you can't connect your HoloLens to a Wi-Fi network:</span></span>

- <span data-ttu-id="de9a3-324">Убедитесь, что Wi-Fi включен.</span><span class="sxs-lookup"><span data-stu-id="de9a3-324">Make sure that Wi-Fi is turned on.</span></span> <span data-ttu-id="de9a3-325">чтобы проверить, используйте жест запуска, а затем выберите **Параметры**  >  **сеть &amp; интернет**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-325">To check, use the Start gesture, then select **Settings** > **Network &amp; Internet** > **Wi-Fi**.</span></span> <span data-ttu-id="de9a3-326">Если Wi-Fi включен, попробуйте отключить его и снова включить.</span><span class="sxs-lookup"><span data-stu-id="de9a3-326">If Wi-Fi is on, try turning it off and then on again.</span></span>
- <span data-ttu-id="de9a3-327">Переместитесь ближе к маршрутизатору или точке доступа.</span><span class="sxs-lookup"><span data-stu-id="de9a3-327">Move closer to the router or access point.</span></span>
- <span data-ttu-id="de9a3-328">Перезапустите маршрутизатор Wi-Fi, а затем [перезапустите HoloLens](hololens-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="de9a3-328">Restart your Wi-Fi router, then [restart HoloLens](hololens-recovery.md).</span></span> <span data-ttu-id="de9a3-329">Повторите попытку подключения.</span><span class="sxs-lookup"><span data-stu-id="de9a3-329">Try connecting again.</span></span>
- <span data-ttu-id="de9a3-330">Если ни одно из этих действий не работает, убедитесь, что маршрутизатор использует последнюю версию встроенного по.</span><span class="sxs-lookup"><span data-stu-id="de9a3-330">If none of these things work, check to make sure that your router is using the latest firmware.</span></span> <span data-ttu-id="de9a3-331">Эти сведения можно найти на веб-сайте изготовителя.</span><span class="sxs-lookup"><span data-stu-id="de9a3-331">You can find this information on the manufacturer website.</span></span>

[<span data-ttu-id="de9a3-332">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-332">Back to list</span></span>](#list)

## <a name="bluetooth-devices-arent-pairing"></a><span data-ttu-id="de9a3-333">Bluetooth устройства не связаны</span><span class="sxs-lookup"><span data-stu-id="de9a3-333">Bluetooth devices aren't pairing</span></span>

<span data-ttu-id="de9a3-334">при возникновении проблем [с связыванием Bluetooth устройства](hololens-connect-devices.md)попробуйте выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="de9a3-334">If you're having problems [pairing a Bluetooth device](hololens-connect-devices.md), try the following:</span></span>

- <span data-ttu-id="de9a3-335">перейдите в **Параметры**  >  **устройства** и убедитесь, что Bluetooth включен.</span><span class="sxs-lookup"><span data-stu-id="de9a3-335">Go to **Settings** > **Devices**, and make sure that Bluetooth is turned on.</span></span> <span data-ttu-id="de9a3-336">Если это так, выключите и снова включите его.</span><span class="sxs-lookup"><span data-stu-id="de9a3-336">If it is, turn it off and on again.</span></span>
- <span data-ttu-id="de9a3-337">убедитесь, что устройство Bluetooth полностью заряжено или имеет новые батареи.</span><span class="sxs-lookup"><span data-stu-id="de9a3-337">Make sure that your Bluetooth device is fully charged or has fresh batteries.</span></span>
- <span data-ttu-id="de9a3-338">Если вы по-прежнему не можете подключиться, [перезапустите HoloLens](hololens-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="de9a3-338">If you still can't connect, [restart the HoloLens](hololens-recovery.md).</span></span>

[<span data-ttu-id="de9a3-339">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-339">Back to list</span></span>](#list)

## <a name="usb-c-microphone-isnt-working"></a><span data-ttu-id="de9a3-340">Микрофон USB-C не работает</span><span class="sxs-lookup"><span data-stu-id="de9a3-340">USB-C Microphone isn't working</span></span>
<span data-ttu-id="de9a3-341">Имейте в виду, что некоторые микротелефоны USB-C неправильно сообщают себя как к микрофону *, так и* к докладчику.</span><span class="sxs-lookup"><span data-stu-id="de9a3-341">Be aware that some USB-C microphones incorrectly report themselves as both a microphone *and* a speaker.</span></span> <span data-ttu-id="de9a3-342">Это проблема с микрофоном, а не с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="de9a3-342">This is a problem with the microphone and not with HoloLens.</span></span> <span data-ttu-id="de9a3-343">при подключении одного из этих микрофонов к HoloLens, звук может быть потерян.</span><span class="sxs-lookup"><span data-stu-id="de9a3-343">When plugging one of these microphones into HoloLens, sound may be lost.</span></span> <span data-ttu-id="de9a3-344">К счастью, существует простое исправление.</span><span class="sxs-lookup"><span data-stu-id="de9a3-344">Fortunately there is a simple fix.</span></span>  

<span data-ttu-id="de9a3-345">в **Параметры**  ->  **системного**  ->  **звука** явным образом установите встроенные динамики **(аналоговый звуковой драйвер аналогового компонента)** в качестве **устройства по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="de9a3-345">In **Settings** -> **System** -> **Sound**, explicitly set the built-in speakers **(Analog Feature Audio Driver)** as the **Default device**.</span></span> <span data-ttu-id="de9a3-346">HoloLens следует запомнить этот параметр, даже если он будет удален и повторно подключен позже.</span><span class="sxs-lookup"><span data-stu-id="de9a3-346">HoloLens should remember this setting even if the microphone is removed and reconnected later.</span></span>

![Устранение неполадок микрофонов USB-C](images/usbc-mic-4.png)

## <a name="devices-listed-as-available-in-settings-dont-work"></a><span data-ttu-id="de9a3-348">устройства, перечисленные как доступные в Параметры не работают</span><span class="sxs-lookup"><span data-stu-id="de9a3-348">Devices listed as available in Settings don't work</span></span>

<span data-ttu-id="de9a3-349">HoloLens (1-й gen) не поддерживает Bluetooth профили аудио.</span><span class="sxs-lookup"><span data-stu-id="de9a3-349">HoloLens (1st gen) doesn't support Bluetooth audio profiles.</span></span> <span data-ttu-id="de9a3-350">Bluetooth звуковые устройства, такие как динамики и гарнитуры, могут отображаться как доступные в параметрах HoloLens, но они не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="de9a3-350">Bluetooth audio devices, such as speakers and headsets, may appear as available in HoloLens settings, but they aren't supported.</span></span>

<span data-ttu-id="de9a3-351">HoloLens 2 поддерживает аудио профиле Bluetooth A2DP для воспроизведения стереозвука.</span><span class="sxs-lookup"><span data-stu-id="de9a3-351">HoloLens 2 supports the Bluetooth A2DP audio profile for stereo playback.</span></span> <span data-ttu-id="de9a3-352">Bluetooth бесплатный профиль, который включает захват микрофона с Bluetoothного периферийного устройства, на HoloLens 2 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="de9a3-352">The Bluetooth Hands Free profile which enables microphone capture from a Bluetooth peripheral is not supported on HoloLens 2.</span></span>

<span data-ttu-id="de9a3-353">если у вас возникают проблемы с Bluetooth устройством, убедитесь, что это устройство поддерживается.</span><span class="sxs-lookup"><span data-stu-id="de9a3-353">If you're having trouble using a Bluetooth device, make sure that it's a supported device.</span></span> <span data-ttu-id="de9a3-354">В число поддерживаемых устройств входят следующие.</span><span class="sxs-lookup"><span data-stu-id="de9a3-354">Supported devices include the following:</span></span>

- <span data-ttu-id="de9a3-355">на английском языке Bluetooth клавиатуры, которые можно использовать в любом месте, где используется клавиатура с holographic.</span><span class="sxs-lookup"><span data-stu-id="de9a3-355">English-language QWERTY Bluetooth keyboards (you can use these anywhere that you use the holographic keyboard).</span></span>
- <span data-ttu-id="de9a3-356">Bluetooth мыши.</span><span class="sxs-lookup"><span data-stu-id="de9a3-356">Bluetooth mice.</span></span>
- <span data-ttu-id="de9a3-357">[HoloLens щелчком мыши](hololens1-clicker.md).</span><span class="sxs-lookup"><span data-stu-id="de9a3-357">The [HoloLens clicker](hololens1-clicker.md).</span></span>

<span data-ttu-id="de9a3-358">вы можете связать другие Bluetooth устройства HID и GATT вместе с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="de9a3-358">You can pair other Bluetooth HID and GATT devices together with your HoloLens.</span></span> <span data-ttu-id="de9a3-359">однако может потребоваться установить соответствующие сопутствующие приложения с Microsoft Store для фактического использования устройств.</span><span class="sxs-lookup"><span data-stu-id="de9a3-359">However, you may have to install corresponding companion apps from Microsoft Store to actually use the devices.</span></span>

[<span data-ttu-id="de9a3-360">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="de9a3-360">Back to list</span></span>](#list)
