---
title: Устранение неполадок HoloLens
description: Решения для распространенных проблем с HoloLens.
author: mattzmsft
ms.author: mazeller
ms.date: 12/02/2019
ms.prod: hololens
ms.topic: article
ms.custom:
- CI 111456
- CSSTroubleshooting
audience: ITPro
ms.localizationpriority: medium
keywords: проблемы, ошибки, устранение неполадок, исправление, Справка, поддержка, HoloLens
manager: jarrettr
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 4897d02f4b789c77204d57c0a7750e3c3803d7bb
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10829024"
---
# <span data-ttu-id="87581-104">Устранение неполадок HoloLens</span><span class="sxs-lookup"><span data-stu-id="87581-104">Troubleshoot HoloLens issues</span></span>

<span data-ttu-id="87581-105">В этой статье объясняется, как устранить несколько распространенных проблем с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="87581-105">This article describes how to resolve several common HoloLens issues.</span></span>

## <span data-ttu-id="87581-106">Мой HoloLens не отвечает на запросы и не запускается</span><span class="sxs-lookup"><span data-stu-id="87581-106">My HoloLens is unresponsive or won't start</span></span>

<span data-ttu-id="87581-107">Если HoloLens не запускается, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="87581-107">If your HoloLens won't start:</span></span>

- <span data-ttu-id="87581-108">Если индикаторы рядом с кнопкой выключения питания не выводятся или появляется только один индикатор, может потребоваться [взимать HoloLens.](hololens-recovery.md#charging-the-device)</span><span class="sxs-lookup"><span data-stu-id="87581-108">If the LEDs next to the power button don't light up, or only one LED briefly blinks, you may need to [charge your HoloLens.](hololens-recovery.md#charging-the-device)</span></span>
- <span data-ttu-id="87581-109">Если индикаторы света выводятся при нажатии кнопки Power, но вы не видите ничего на дисплее, [preform аппаратную перегрузку устройства](hololens-recovery.md#hard-reset-procedure).</span><span class="sxs-lookup"><span data-stu-id="87581-109">If the LEDs light up when you press the power button but you can't see anything on the displays, [preform a hard reset of the device](hololens-recovery.md#hard-reset-procedure).</span></span>

<span data-ttu-id="87581-110">Если устройство HoloLens зафиксировано или не отвечает, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="87581-110">If your HoloLens becomes frozen or unresponsive:</span></span>

- <span data-ttu-id="87581-111">Отключите HoloLens, нажав кнопку Power, пока не будут выключены все пять индикаторов, или 15 секунд, если индикаторы не отвечают.</span><span class="sxs-lookup"><span data-stu-id="87581-111">Turn off your HoloLens by pressing the power button until all five of the LEDs turn themselves off, or for 15 seconds if the LEDs are unresponsive.</span></span> <span data-ttu-id="87581-112">Чтобы запустить HoloLens, снова нажмите кнопку Power.</span><span class="sxs-lookup"><span data-stu-id="87581-112">To start your HoloLens, press the power button again.</span></span>

<span data-ttu-id="87581-113">Если эти действия не попытаются устранить, вы можете [восстановить устройство hololens 2](hololens-recovery.md) или [hololens (1-го поколения).](hololens1-recovery.md)</span><span class="sxs-lookup"><span data-stu-id="87581-113">If these steps don't work, you can try [recovering your HoloLens 2 device](hololens-recovery.md) or [HoloLens (1st gen) device.](hololens1-recovery.md)</span></span>

## <span data-ttu-id="87581-114">Самые голограммы плохо выглядят</span><span class="sxs-lookup"><span data-stu-id="87581-114">Holograms don't look good</span></span>

<span data-ttu-id="87581-115">Если ваши голограммы работают нестабильно, переходят или не ищите прямо сейчас, попробуйте выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="87581-115">If your holograms are unstable, jumpy, or don't look right, try:</span></span>

- <span data-ttu-id="87581-116">Очистка гипервизора устройства и линейка датчиков на передней стороне HoloLens.</span><span class="sxs-lookup"><span data-stu-id="87581-116">Cleaning your device visor and sensor bar on the front of your HoloLens.</span></span>
- <span data-ttu-id="87581-117">Увеличение света в комнате.</span><span class="sxs-lookup"><span data-stu-id="87581-117">Increasing the light in your room.</span></span>
- <span data-ttu-id="87581-118">Обходится и просматриваете окружающую обстановку, чтобы HoloLens мог полностью ее просканировать.</span><span class="sxs-lookup"><span data-stu-id="87581-118">Walking around and looking at your surroundings so that HoloLens can scan them more completely.</span></span>
- <span data-ttu-id="87581-119">Калибровка HoloLens для глаз.</span><span class="sxs-lookup"><span data-stu-id="87581-119">Calibrating your HoloLens for your eyes.</span></span> <span data-ttu-id="87581-120">Перейдите в раздел **Параметры**  >  **System**  >  **служебных программ**.</span><span class="sxs-lookup"><span data-stu-id="87581-120">Go to **Settings** > **System** > **Utilities**.</span></span> <span data-ttu-id="87581-121">В разделе **Калибровка** выберите **Открыть калибровку**.</span><span class="sxs-lookup"><span data-stu-id="87581-121">Under **Calibration**, select **Open Calibration**.</span></span>

## <span data-ttu-id="87581-122">HoloLens не реагирует на жесты</span><span class="sxs-lookup"><span data-stu-id="87581-122">HoloLens doesn't respond to gestures</span></span>

<span data-ttu-id="87581-123">Убедитесь в том, что HoloLens может видеть ваши жесты.</span><span class="sxs-lookup"><span data-stu-id="87581-123">To make sure that HoloLens can see your gestures.</span></span>  <span data-ttu-id="87581-124">Сохранение руки в кадре жеста — когда HoloLens может видеть руки, курсор меняется с точки на кольцо.</span><span class="sxs-lookup"><span data-stu-id="87581-124">Keep your hand in the gesture frame - when HoloLens can see your hand, the cursor changes from a dot to a ring.</span></span>

<span data-ttu-id="87581-125">Узнайте больше об использовании жестов в [hololens (1-ом)](hololens1-basic-usage.md#use-hololens-with-your-hands) или [HoloLens 2](hololens2-basic-usage.md#the-hand-tracking-frame).</span><span class="sxs-lookup"><span data-stu-id="87581-125">Learn more about using gestures on [HoloLens (1st gen)](hololens1-basic-usage.md#use-hololens-with-your-hands) or [HoloLens 2](hololens2-basic-usage.md#the-hand-tracking-frame).</span></span>

<span data-ttu-id="87581-126">Если ваша среда слишком темная, она может не отображаться в вашей руки, поэтому убедитесь, что у вас достаточно света.</span><span class="sxs-lookup"><span data-stu-id="87581-126">If your environment is too dark, HoloLens might not see your hand, so make sure that there's enough light.</span></span>

<span data-ttu-id="87581-127">Если у вашего гипервизора есть отпечатки пальцев или палец, используйте чистящую ткань Microfiber, которая поставлялась вместе с HoloLens для аккуратной очистки гипервизора.</span><span class="sxs-lookup"><span data-stu-id="87581-127">If your visor has fingerprints or smudges, use the microfiber cleaning cloth that came with the HoloLens to clean your visor gently.</span></span>

## <span data-ttu-id="87581-128">HoloLens не отвечает на голосовые команды</span><span class="sxs-lookup"><span data-stu-id="87581-128">HoloLens doesn't respond to my voice commands</span></span>

<span data-ttu-id="87581-129">Если Кортана не отвечает на голосовые команды, убедитесь, что Кортана включена.</span><span class="sxs-lookup"><span data-stu-id="87581-129">If Cortana isn't responding to your voice commands, make sure Cortana is turned on.</span></span> <span data-ttu-id="87581-130">В списке все приложения выберите **Cortana**  >  **Menu**  >  **Параметры записной книжки**меню кортаны,  >  **Settings** чтобы внести изменения.</span><span class="sxs-lookup"><span data-stu-id="87581-130">On the All apps list, select **Cortana** > **Menu** > **Notebook** > **Settings** to make changes.</span></span> <span data-ttu-id="87581-131">Дополнительные сведения о том, что можно сказать, см. в статье [Использование голосовых команд с HoloLens](hololens-cortana.md).</span><span class="sxs-lookup"><span data-stu-id="87581-131">To learn more about what you can say, see [Use your voice with HoloLens](hololens-cortana.md).</span></span>

## <span data-ttu-id="87581-132">Не удается разместить голограммы и посмотреть голограммы, которые были ранее помещены</span><span class="sxs-lookup"><span data-stu-id="87581-132">I can't place holograms or see holograms that I previously placed</span></span>

<span data-ttu-id="87581-133">Если HoloLens не может сопоставить или загрузить свое пространство, оно будет переведено в режим ограниченной нагрузки, и вы не сможете размещать самые голограммы или видеть самые загруженные голограммы.</span><span class="sxs-lookup"><span data-stu-id="87581-133">If HoloLens can't map or load your space, it enters Limited mode and you won't be able to place holograms or see holograms that you've placed.</span></span> <span data-ttu-id="87581-134">Можно попытаться сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="87581-134">Here are some things to try:</span></span>

- <span data-ttu-id="87581-135">Убедитесь в том, что в вашей среде достаточно света, чтобы HoloLens мог видеть и сопоставлять пространство.</span><span class="sxs-lookup"><span data-stu-id="87581-135">Make sure that there's enough light in your environment so HoloLens can see and map the space.</span></span>
- <span data-ttu-id="87581-136">Убедитесь в том, что вы подключены к сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="87581-136">Make sure that you're connected to a Wi-Fi network.</span></span> <span data-ttu-id="87581-137">Если вы не подключены к сети Wi-Fi, HoloLens не может определить и загрузить известное пространство.</span><span class="sxs-lookup"><span data-stu-id="87581-137">If you're not connected to Wi-Fi, HoloLens can't identify and load a known space.</span></span>
- <span data-ttu-id="87581-138">Если вам нужно создать новый модуль, подключитесь к сети Wi-Fi, а затем перезапустите HoloLens.</span><span class="sxs-lookup"><span data-stu-id="87581-138">If you need to create a new space, connect to Wi-Fi, then restart your HoloLens.</span></span>
- <span data-ttu-id="87581-139">Чтобы узнать, является ли допустимым пространство активным, или вручную Загрузи пробелы, перейдите в раздел **Параметры**  >  **системы**  >  **Spaces**.</span><span class="sxs-lookup"><span data-stu-id="87581-139">To see if the correct space is active, or to manually load a space, go to **Settings** > **System** > **Spaces**.</span></span>
- <span data-ttu-id="87581-140">Если при загрузке свободного места возникли проблемы, возможно, это может быть вызвано тем, что диск поврежден.</span><span class="sxs-lookup"><span data-stu-id="87581-140">If the correct space is loaded and you're still having problems, the space may be corrupt.</span></span> <span data-ttu-id="87581-141">Чтобы устранить эту проблему, выберите пробел, а затем нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="87581-141">To fix this issue, select the space, then select **Remove**.</span></span> <span data-ttu-id="87581-142">После удаления пробела HoloLens начнет сопоставлять окружающую обстановку и создаст новое пространство.</span><span class="sxs-lookup"><span data-stu-id="87581-142">After you remove the space, HoloLens starts to map your surroundings and create a new space.</span></span>

## <span data-ttu-id="87581-143">HoloLens не может определить, в каком пространстве</span><span class="sxs-lookup"><span data-stu-id="87581-143">My HoloLens can't tell what space I'm in</span></span>

<span data-ttu-id="87581-144">Если HoloLens не может определить и загрузить пространство, которое вы используете автоматически, проверьте указанные ниже факторы.</span><span class="sxs-lookup"><span data-stu-id="87581-144">If your HoloLens can't identify and load the space you're in automatically, check the following factors:</span></span>

- <span data-ttu-id="87581-145">Убедитесь в том, что вы подключены к сети Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="87581-145">Make sure that you're connected to Wi-Fi</span></span>
- <span data-ttu-id="87581-146">Убедитесь в том, что в комнате достаточно света</span><span class="sxs-lookup"><span data-stu-id="87581-146">Make sure that there's plenty of light in the room</span></span>
- <span data-ttu-id="87581-147">Убедитесь в том, что в отношении окружающей среды ничего не изменилось.</span><span class="sxs-lookup"><span data-stu-id="87581-147">Make sure that there haven't been any major changes to the surroundings.</span></span>

<span data-ttu-id="87581-148">Кроме того, вы можете вручную загрузить пробелы или управлять ими, перейдя в **Settings**  >  **системные**  >  **пространства**параметров.</span><span class="sxs-lookup"><span data-stu-id="87581-148">You can also load a space manually or manage your spaces by going to **Settings** > **System** > **Spaces**.</span></span>

## <span data-ttu-id="87581-149">Появляется сообщение об ошибке "недостаточно места на диске"</span><span class="sxs-lookup"><span data-stu-id="87581-149">I'm getting a "low disk space" error</span></span>

<span data-ttu-id="87581-150">Чтобы освободить место, необходимо выполнить одно или несколько из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="87581-150">You'll need to free up some storage space by doing one or more of the following:</span></span>

- <span data-ttu-id="87581-151">Удалите неиспользуемые пробелы.</span><span class="sxs-lookup"><span data-stu-id="87581-151">Delete some unused spaces.</span></span> <span data-ttu-id="87581-152">Перейдите в раздел **Параметры**  >  **системы**  >  **Spaces**, выберите ненужные пробелы и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="87581-152">Go to **Settings** > **System** > **Spaces**, select a space that you no longer need, and then select **Remove**.</span></span>
- <span data-ttu-id="87581-153">Удалите некоторые из уже размещенных голограмм.</span><span class="sxs-lookup"><span data-stu-id="87581-153">Remove some of the holograms that you've placed.</span></span>
- <span data-ttu-id="87581-154">Удалите некоторые изображения и видео из приложения "фотографии".</span><span class="sxs-lookup"><span data-stu-id="87581-154">Delete some pictures and videos from the Photos app.</span></span>
- <span data-ttu-id="87581-155">Удалите некоторые приложения из HoloLens.</span><span class="sxs-lookup"><span data-stu-id="87581-155">Uninstall some apps from your HoloLens.</span></span> <span data-ttu-id="87581-156">В списке **все приложения** нажмите и удерживайте приложение, которое вы хотите удалить, а затем нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="87581-156">In the **All apps** list, tap and hold the app you want to uninstall, and then select **Uninstall**.</span></span>

## <span data-ttu-id="87581-157">Мой HoloLens не может создать новый интервал</span><span class="sxs-lookup"><span data-stu-id="87581-157">My HoloLens can't create a new space</span></span>

<span data-ttu-id="87581-158">Скорее всего, причина в том, что у тебя недостаточно дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="87581-158">The most likely problem is that you're running low on storage space.</span></span> <span data-ttu-id="87581-159">Попробуйте один из [предыдущих советов](#im-getting-a-low-disk-space-error) , чтобы освободить место на диске.</span><span class="sxs-lookup"><span data-stu-id="87581-159">Try one of the [previous tips](#im-getting-a-low-disk-space-error) to free up some disk space.</span></span>

## <span data-ttu-id="87581-160">Эмулятор HoloLens не работает</span><span class="sxs-lookup"><span data-stu-id="87581-160">The HoloLens emulator isn't working</span></span>

<span data-ttu-id="87581-161">Сведения о эмуляторе HoloLens можно найти в документации разработчика.</span><span class="sxs-lookup"><span data-stu-id="87581-161">Information about the HoloLens emulator is located in our developer documentation.</span></span>  <span data-ttu-id="87581-162">Подробнее об [устранении неполадок эмулятора HoloLens](https://docs.microsoft.com/windows/mixed-reality/using-the-hololens-emulator#troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="87581-162">Read more about [troubleshooting the HoloLens emulator](https://docs.microsoft.com/windows/mixed-reality/using-the-hololens-emulator#troubleshooting).</span></span>
