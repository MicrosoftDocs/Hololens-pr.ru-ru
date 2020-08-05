---
title: Поиск и устранение неисправностей
description: Решения для распространенных проблем с HoloLens.
author: mattzmsft
ms.author: mazeller
ms.date: 12/02/2019
ms.prod: hololens
ms.topic: article
audience: HoloLens
ms.localizationpriority: medium
keywords: проблемы, ошибки, устранение неполадок, исправление, Справка, поддержка, HoloLens
manager: jarrettr
ms.custom:
- CI 111456
- CSSTroubleshooting
ms.openlocfilehash: 469848cf306675fcfb99247b5c91b159c204a5fe
ms.sourcegitcommit: 2122490074adb7f63edfc3576441980caa22695f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "10915962"
---
# <span data-ttu-id="ba591-104">Поиск и устранение неисправностей</span><span class="sxs-lookup"><span data-stu-id="ba591-104">Troubleshooting</span></span>

<span data-ttu-id="ba591-105">В этой статье объясняется, как устранить несколько распространенных проблем с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba591-105">This article describes how to resolve several common HoloLens issues.</span></span>

## <span data-ttu-id="ba591-106">Мой HoloLens не отвечает на запросы и не запускается</span><span class="sxs-lookup"><span data-stu-id="ba591-106">My HoloLens is unresponsive or won't start</span></span>

<span data-ttu-id="ba591-107">Если HoloLens не запускается, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="ba591-107">If your HoloLens won't start:</span></span>

- <span data-ttu-id="ba591-108">Если индикаторы рядом с кнопкой выключения питания не выводятся или появляется только один индикатор, может потребоваться [взимать HoloLens.](hololens-recovery.md#charge-the-device)</span><span class="sxs-lookup"><span data-stu-id="ba591-108">If the LEDs next to the power button don't light up, or only one LED briefly blinks, you may need to [charge your HoloLens.](hololens-recovery.md#charge-the-device)</span></span>
- <span data-ttu-id="ba591-109">Если индикаторы света выводятся при нажатии кнопки Power, но вы не видите ничего на дисплее, [preform аппаратную перегрузку устройства](hololens-recovery.md#hard-reset-procedure).</span><span class="sxs-lookup"><span data-stu-id="ba591-109">If the LEDs light up when you press the power button but you can't see anything on the displays, [preform a hard reset of the device](hololens-recovery.md#hard-reset-procedure).</span></span>

<span data-ttu-id="ba591-110">Если устройство HoloLens зафиксировано или не отвечает, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba591-110">If your HoloLens becomes frozen or unresponsive:</span></span>

- <span data-ttu-id="ba591-111">Отключите HoloLens, нажав кнопку Power, пока не будут выключены все пять индикаторов, или 15 секунд, если индикаторы не отвечают.</span><span class="sxs-lookup"><span data-stu-id="ba591-111">Turn off your HoloLens by pressing the power button until all five of the LEDs turn themselves off, or for 15 seconds if the LEDs are unresponsive.</span></span> <span data-ttu-id="ba591-112">Чтобы запустить HoloLens, снова нажмите кнопку Power.</span><span class="sxs-lookup"><span data-stu-id="ba591-112">To start your HoloLens, press the power button again.</span></span>

<span data-ttu-id="ba591-113">Если эти действия не попытаются устранить, вы можете [восстановить устройство hololens 2](hololens-recovery.md) или [hololens (1-го поколения).](hololens1-recovery.md)</span><span class="sxs-lookup"><span data-stu-id="ba591-113">If these steps don't work, you can try [recovering your HoloLens 2 device](hololens-recovery.md) or [HoloLens (1st gen) device.](hololens1-recovery.md)</span></span>

## <span data-ttu-id="ba591-114">Самые голограммы плохо выглядят</span><span class="sxs-lookup"><span data-stu-id="ba591-114">Holograms don't look good</span></span>

<span data-ttu-id="ba591-115">Если ваши голограммы работают нестабильно, переходят или не ищите прямо сейчас, попробуйте выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba591-115">If your holograms are unstable, jumpy, or don't look right, try:</span></span>

- <span data-ttu-id="ba591-116">Очистка гипервизора устройства и линейка датчиков на передней стороне HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba591-116">Cleaning your device visor and sensor bar on the front of your HoloLens.</span></span>
- <span data-ttu-id="ba591-117">Увеличение света в комнате.</span><span class="sxs-lookup"><span data-stu-id="ba591-117">Increasing the light in your room.</span></span>
- <span data-ttu-id="ba591-118">Обходится и просматриваете окружающую обстановку, чтобы HoloLens мог полностью ее просканировать.</span><span class="sxs-lookup"><span data-stu-id="ba591-118">Walking around and looking at your surroundings so that HoloLens can scan them more completely.</span></span>
- <span data-ttu-id="ba591-119">Калибровка HoloLens для глаз.</span><span class="sxs-lookup"><span data-stu-id="ba591-119">Calibrating your HoloLens for your eyes.</span></span> <span data-ttu-id="ba591-120">Перейдите в раздел **Параметры**  >  **System**  >  **служебных программ**.</span><span class="sxs-lookup"><span data-stu-id="ba591-120">Go to **Settings** > **System** > **Utilities**.</span></span> <span data-ttu-id="ba591-121">В разделе **Калибровка** выберите **Открыть калибровку**.</span><span class="sxs-lookup"><span data-stu-id="ba591-121">Under **Calibration**, select **Open Calibration**.</span></span>

## <span data-ttu-id="ba591-122">HoloLens не отвечает на ввод вручную</span><span class="sxs-lookup"><span data-stu-id="ba591-122">HoloLens doesn't respond to hand input</span></span>

<span data-ttu-id="ba591-123">Чтобы элемент HoloLens мог видеть ваши руки, нужно сохранить его в кадре жеста.</span><span class="sxs-lookup"><span data-stu-id="ba591-123">To ensure that HoloLens can see your hands, you need to keep them in the gesture frame.</span></span>  <span data-ttu-id="ba591-124">Домашняя страница "смешанная реальности" предоставляет отзыв, который позволяет узнать, когда ваши руки отслеживаются.</span><span class="sxs-lookup"><span data-stu-id="ba591-124">The Mixed Reality Home provides feedback that lets you know when your hands are tracked.</span></span>  <span data-ttu-id="ba591-125">Отзывы и предложения для разных версий HoloLens различны.</span><span class="sxs-lookup"><span data-stu-id="ba591-125">The feedback is different on different versions of HoloLens:</span></span>
- <span data-ttu-id="ba591-126">Для HoloLens (1-го поколения) курсор взгляда меняется с точки на кольцо.</span><span class="sxs-lookup"><span data-stu-id="ba591-126">On HoloLens (1st gen), the gaze cursor changes from a dot to a ring</span></span>
- <span data-ttu-id="ba591-127">В HoloLens 2 отображается курсор в виде значка с изображением проладони, когда рука находится на планшете, а луч появляется, когда планшеты больше не нужны</span><span class="sxs-lookup"><span data-stu-id="ba591-127">On HoloLens 2, a fingertip cursor appears when your hand is close to a slate, and a hand ray appears when slates are further away</span></span>

<span data-ttu-id="ba591-128">Многие впечатляющие приложения следуют шаблонам ввода, похожим на домашнюю страницу Mixed Reality.</span><span class="sxs-lookup"><span data-stu-id="ba591-128">Many immersive apps follow input patterns that are similar to Mixed Reality Home.</span></span>  <span data-ttu-id="ba591-129">Узнайте больше о том, как использовать ввод с руки на [hololens (1-ом)](hololens1-basic-usage.md#use-hololens-with-your-hands) и [HoloLens 2](hololens2-basic-usage.md#the-hand-tracking-frame).</span><span class="sxs-lookup"><span data-stu-id="ba591-129">Learn more about using hand input on [HoloLens (1st gen)](hololens1-basic-usage.md#use-hololens-with-your-hands) and [HoloLens 2](hololens2-basic-usage.md#the-hand-tracking-frame).</span></span>

<span data-ttu-id="ba591-130">Если ты надето перчатки, обратите внимание на то, что некоторые типы перчатки не работают с отслеживанием.</span><span class="sxs-lookup"><span data-stu-id="ba591-130">If you are wearing gloves, note that some types of gloves do not work with hand tracking.</span></span>  <span data-ttu-id="ba591-131">Распространенный пример — черный перчатки, который обычно используется для связи с инфракрасным излучением, а не на камере глубины.</span><span class="sxs-lookup"><span data-stu-id="ba591-131">A common example is black rubber gloves, which tend to absorb infrared light and are not picked up by the depth camera.</span></span>  <span data-ttu-id="ba591-132">Если вы работаете с резинным перчаткиом, мы рекомендуем использовать более светлый цвет, например синий или серый.</span><span class="sxs-lookup"><span data-stu-id="ba591-132">If your work involves rubber gloves, we recommend trying a lighter color such as blue or gray.</span></span>  <span data-ttu-id="ba591-133">Еще один пример — крупный Baggy перчатки, который, как правило, закрывает форму руки.</span><span class="sxs-lookup"><span data-stu-id="ba591-133">Another example is large baggy gloves, which tend to obscure the shape of your hand.</span></span> <span data-ttu-id="ba591-134">Для достижения наилучших результатов рекомендуется использовать перчатки, как можно лучше подбор форм.</span><span class="sxs-lookup"><span data-stu-id="ba591-134">We recommend using gloves that are as form-fitting as possible for best results.</span></span>

<span data-ttu-id="ba591-135">Если у вашего гипервизора есть отпечатки пальцев или палец, используйте чистящую ткань Microfiber, которая поставлялась вместе с HoloLens для аккуратной очистки гипервизора.</span><span class="sxs-lookup"><span data-stu-id="ba591-135">If your visor has fingerprints or smudges, use the microfiber cleaning cloth that came with the HoloLens to clean your visor gently.</span></span>

## <span data-ttu-id="ba591-136">HoloLens не отвечает на голосовые команды</span><span class="sxs-lookup"><span data-stu-id="ba591-136">HoloLens doesn't respond to my voice commands</span></span>

<span data-ttu-id="ba591-137">Если Кортана не отвечает на голосовые команды, убедитесь, что Кортана включена.</span><span class="sxs-lookup"><span data-stu-id="ba591-137">If Cortana isn't responding to your voice commands, make sure Cortana is turned on.</span></span> <span data-ttu-id="ba591-138">В списке все приложения выберите **Cortana**  >  **Menu**  >  **Параметры записной книжки**меню кортаны,  >  **Settings** чтобы внести изменения.</span><span class="sxs-lookup"><span data-stu-id="ba591-138">On the All apps list, select **Cortana** > **Menu** > **Notebook** > **Settings** to make changes.</span></span> <span data-ttu-id="ba591-139">Дополнительные сведения о том, что можно сказать, см. в статье [Использование голосовых команд с HoloLens](hololens-cortana.md).</span><span class="sxs-lookup"><span data-stu-id="ba591-139">To learn more about what you can say, see [Use your voice with HoloLens](hololens-cortana.md).</span></span>

## <span data-ttu-id="ba591-140">Не удается разместить голограммы и посмотреть голограммы, которые были ранее помещены</span><span class="sxs-lookup"><span data-stu-id="ba591-140">I can't place holograms or see holograms that I previously placed</span></span>

<span data-ttu-id="ba591-141">Если HoloLens не может сопоставить или загрузить свое пространство, оно будет переведено в режим ограниченной нагрузки, и вы не сможете размещать самые голограммы или видеть самые загруженные голограммы.</span><span class="sxs-lookup"><span data-stu-id="ba591-141">If HoloLens can't map or load your space, it enters Limited mode and you won't be able to place holograms or see holograms that you've placed.</span></span> <span data-ttu-id="ba591-142">Можно попытаться сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="ba591-142">Here are some things to try:</span></span>

- <span data-ttu-id="ba591-143">Убедитесь в том, что в вашей среде достаточно света, чтобы HoloLens мог видеть и сопоставлять пространство.</span><span class="sxs-lookup"><span data-stu-id="ba591-143">Make sure that there's enough light in your environment so HoloLens can see and map the space.</span></span>
- <span data-ttu-id="ba591-144">Убедитесь в том, что вы подключены к сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="ba591-144">Make sure that you're connected to a Wi-Fi network.</span></span> <span data-ttu-id="ba591-145">Если вы не подключены к сети Wi-Fi, HoloLens не может определить и загрузить известное пространство.</span><span class="sxs-lookup"><span data-stu-id="ba591-145">If you're not connected to Wi-Fi, HoloLens can't identify and load a known space.</span></span>
- <span data-ttu-id="ba591-146">Если вам нужно создать новый модуль, подключитесь к сети Wi-Fi, а затем перезапустите HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba591-146">If you need to create a new space, connect to Wi-Fi, then restart your HoloLens.</span></span>
- <span data-ttu-id="ba591-147">Чтобы узнать, является ли допустимым пространство активным, или вручную Загрузи пробелы, перейдите в раздел **Параметры**  >  **системы**  >  **Spaces**.</span><span class="sxs-lookup"><span data-stu-id="ba591-147">To see if the correct space is active, or to manually load a space, go to **Settings** > **System** > **Spaces**.</span></span>
- <span data-ttu-id="ba591-148">Если при загрузке свободного места возникли проблемы, возможно, это может быть вызвано тем, что диск поврежден.</span><span class="sxs-lookup"><span data-stu-id="ba591-148">If the correct space is loaded and you're still having problems, the space may be corrupt.</span></span> <span data-ttu-id="ba591-149">Чтобы устранить эту проблему, выберите пробел, а затем нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="ba591-149">To fix this issue, select the space, then select **Remove**.</span></span> <span data-ttu-id="ba591-150">После удаления пробела HoloLens начнет сопоставлять окружающую обстановку и создаст новое пространство.</span><span class="sxs-lookup"><span data-stu-id="ba591-150">After you remove the space, HoloLens starts to map your surroundings and create a new space.</span></span>

## <span data-ttu-id="ba591-151">HoloLens не может определить, в каком пространстве</span><span class="sxs-lookup"><span data-stu-id="ba591-151">My HoloLens can't tell what space I'm in</span></span>

<span data-ttu-id="ba591-152">Если HoloLens не может определить и загрузить пространство, которое вы используете автоматически, проверьте указанные ниже факторы.</span><span class="sxs-lookup"><span data-stu-id="ba591-152">If your HoloLens can't identify and load the space you're in automatically, check the following factors:</span></span>

- <span data-ttu-id="ba591-153">Убедитесь в том, что вы подключены к сети Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="ba591-153">Make sure that you're connected to Wi-Fi</span></span>
- <span data-ttu-id="ba591-154">Убедитесь в том, что в комнате достаточно света</span><span class="sxs-lookup"><span data-stu-id="ba591-154">Make sure that there's plenty of light in the room</span></span>
- <span data-ttu-id="ba591-155">Убедитесь в том, что в отношении окружающей среды ничего не изменилось.</span><span class="sxs-lookup"><span data-stu-id="ba591-155">Make sure that there haven't been any major changes to the surroundings.</span></span>

<span data-ttu-id="ba591-156">Кроме того, вы можете вручную загрузить пробелы или управлять ими, перейдя в **Settings**  >  **системные**  >  **пространства**параметров.</span><span class="sxs-lookup"><span data-stu-id="ba591-156">You can also load a space manually or manage your spaces by going to **Settings** > **System** > **Spaces**.</span></span>

## <span data-ttu-id="ba591-157">Появляется сообщение об ошибке "недостаточно места на диске"</span><span class="sxs-lookup"><span data-stu-id="ba591-157">I'm getting a "low disk space" error</span></span>

<span data-ttu-id="ba591-158">Чтобы освободить место, необходимо выполнить одно или несколько из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="ba591-158">You'll need to free up some storage space by doing one or more of the following:</span></span>

- <span data-ttu-id="ba591-159">Удалите неиспользуемые пробелы.</span><span class="sxs-lookup"><span data-stu-id="ba591-159">Delete some unused spaces.</span></span> <span data-ttu-id="ba591-160">Перейдите в раздел **Параметры**  >  **системы**  >  **Spaces**, выберите ненужные пробелы и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="ba591-160">Go to **Settings** > **System** > **Spaces**, select a space that you no longer need, and then select **Remove**.</span></span>
- <span data-ttu-id="ba591-161">Удалите некоторые из уже размещенных голограмм.</span><span class="sxs-lookup"><span data-stu-id="ba591-161">Remove some of the holograms that you've placed.</span></span>
- <span data-ttu-id="ba591-162">Удалите некоторые изображения и видео из приложения "фотографии".</span><span class="sxs-lookup"><span data-stu-id="ba591-162">Delete some pictures and videos from the Photos app.</span></span>
- <span data-ttu-id="ba591-163">Удалите некоторые приложения из HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba591-163">Uninstall some apps from your HoloLens.</span></span> <span data-ttu-id="ba591-164">В списке **все приложения** нажмите и удерживайте приложение, которое вы хотите удалить, а затем нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="ba591-164">In the **All apps** list, tap and hold the app you want to uninstall, and then select **Uninstall**.</span></span>

## <span data-ttu-id="ba591-165">Мой HoloLens не может создать новый интервал</span><span class="sxs-lookup"><span data-stu-id="ba591-165">My HoloLens can't create a new space</span></span>

<span data-ttu-id="ba591-166">Скорее всего, причина в том, что у тебя недостаточно дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="ba591-166">The most likely problem is that you're running low on storage space.</span></span> <span data-ttu-id="ba591-167">Попробуйте один из [предыдущих советов](#im-getting-a-low-disk-space-error) , чтобы освободить место на диске.</span><span class="sxs-lookup"><span data-stu-id="ba591-167">Try one of the [previous tips](#im-getting-a-low-disk-space-error) to free up some disk space.</span></span>

## <span data-ttu-id="ba591-168">Эмулятор HoloLens не работает</span><span class="sxs-lookup"><span data-stu-id="ba591-168">The HoloLens emulator isn't working</span></span>

<span data-ttu-id="ba591-169">Сведения о эмуляторе HoloLens можно найти в документации разработчика.</span><span class="sxs-lookup"><span data-stu-id="ba591-169">Information about the HoloLens emulator is located in our developer documentation.</span></span>  <span data-ttu-id="ba591-170">Подробнее об [устранении неполадок эмулятора HoloLens](https://docs.microsoft.com/windows/mixed-reality/using-the-hololens-emulator#troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="ba591-170">Read more about [troubleshooting the HoloLens emulator](https://docs.microsoft.com/windows/mixed-reality/using-the-hololens-emulator#troubleshooting).</span></span>
