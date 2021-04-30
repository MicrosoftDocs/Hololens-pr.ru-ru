---
title: Использование щелчка HoloLens
description: В этой статье описывается, как использовать щелчком HoloLens, включая связывание с помощью щелчка, заряжается и восстановление.
ms.assetid: 7d4a30fd-cf1d-4c9a-8eb1-1968ccecbe59
ms.date: 09/16/2019
manager: jarrettr
keywords: hololens
ms.prod: hololens
ms.sitesec: library
author: v-miegge
ms.author: v-miegge
ms.topic: article
ms.localizationpriority: medium
appliesto:
- HoloLens (1st gen)
ms.openlocfilehash: 4b17fc134846a66046a819c56755d87206c5643e
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309999"
---
# <a name="use-the-hololens-1st-gen-clicker"></a><span data-ttu-id="73fdf-104">Использование щелчка HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="73fdf-104">Use the HoloLens (1st gen) clicker</span></span>

<span data-ttu-id="73fdf-105">Этот щелчок разработан специально для HoloLens (1-го поколения) и предоставляет еще один способ взаимодействия с голограммами.</span><span class="sxs-lookup"><span data-stu-id="73fdf-105">The clicker was designed specifically for HoloLens (1st gen) and gives you another way to interact with holograms.</span></span> <span data-ttu-id="73fdf-106">Он поставляется с HoloLens (1-го поколения) в отдельном поле.</span><span class="sxs-lookup"><span data-stu-id="73fdf-106">It comes with HoloLens (1st gen), in a separate box.</span></span>

<span data-ttu-id="73fdf-107">Используйте его вместо жестов руки для выбора, прокрутки, перемещения и изменения размера приложений.</span><span class="sxs-lookup"><span data-stu-id="73fdf-107">Use it in place of hand gestures to select, scroll, move, and resize apps.</span></span>

## <a name="clicker-hardware-and-pairing"></a><span data-ttu-id="73fdf-108">Щелкните Оборудование и свяжите</span><span class="sxs-lookup"><span data-stu-id="73fdf-108">Clicker hardware and pairing</span></span>

<span data-ttu-id="73fdf-109">У щелчка по HoloLens (1-го поколения) есть цикл пальца, чтобы упростить его хранение и индикатор индикатора.</span><span class="sxs-lookup"><span data-stu-id="73fdf-109">The HoloLens (1st gen) clicker has a finger loop to make it easier to hold, and an indicator light.</span></span>

![Щелчок HoloLens](images/use-hololens-clicker-1.png)

### <a name="clicker-indicator-lights"></a><span data-ttu-id="73fdf-111">Индикаторы индикаторов щелчков</span><span class="sxs-lookup"><span data-stu-id="73fdf-111">Clicker indicator lights</span></span>

<span data-ttu-id="73fdf-112">Вот что означают индикаторы щелчка.</span><span class="sxs-lookup"><span data-stu-id="73fdf-112">Here's what the lights on the clicker mean.</span></span>

- <span data-ttu-id="73fdf-113">**Мигающий белый цвет**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-113">**Blinking white**.</span></span> <span data-ttu-id="73fdf-114">Щелчок выполняется в режиме связывания.</span><span class="sxs-lookup"><span data-stu-id="73fdf-114">The clicker is in pairing mode.</span></span>
- <span data-ttu-id="73fdf-115">**Быстрая мигающий белый цвет**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-115">**Fast-blinking white**.</span></span> <span data-ttu-id="73fdf-116">Связывание выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="73fdf-116">Pairing was successful.</span></span>
- <span data-ttu-id="73fdf-117">**Сплошной белый цвет**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-117">**Solid white**.</span></span> <span data-ttu-id="73fdf-118">Щелчок мыши выдает оплату.</span><span class="sxs-lookup"><span data-stu-id="73fdf-118">The clicker is charging.</span></span>
- <span data-ttu-id="73fdf-119">**Мигающий оранжевый**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-119">**Blinking amber**.</span></span> <span data-ttu-id="73fdf-120">Батарея мала.</span><span class="sxs-lookup"><span data-stu-id="73fdf-120">The battery is low.</span></span>
- <span data-ttu-id="73fdf-121">**Горит оранжевым цветом**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-121">**Solid amber**.</span></span> <span data-ttu-id="73fdf-122">При нажатии кнопки мыши возникла ошибка, и ее потребуется перезапустить.</span><span class="sxs-lookup"><span data-stu-id="73fdf-122">The clicker ran into an error and you'll need to restart it.</span></span> <span data-ttu-id="73fdf-123">Нажав кнопку связывания, щелкните и удерживайте ее в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="73fdf-123">While pressing the pairing button, click and hold for 15 seconds.</span></span>

### <a name="pair-the-clicker-with-your-hololens-1st-gen"></a><span data-ttu-id="73fdf-124">Связывание щелчка с HoloLens (1-й общий)</span><span class="sxs-lookup"><span data-stu-id="73fdf-124">Pair the clicker with your HoloLens (1st gen)</span></span>

1. <span data-ttu-id="73fdf-125">Используйте жест раскрытия для перехода в **Начало**, выберите **Параметры**  >  **устройства** и убедитесь, что Bluetooth включен.</span><span class="sxs-lookup"><span data-stu-id="73fdf-125">Use the bloom gesture to go to **Start**, then select **Settings** > **Devices** and verify that Bluetooth is on.</span></span>
1. <span data-ttu-id="73fdf-126">В щелчке мыши нажмите и удерживайте кнопку связывания, пока состояние светло не мигает белым цветом.</span><span class="sxs-lookup"><span data-stu-id="73fdf-126">On the clicker, press and hold the pairing button until the status light blinks white.</span></span>
1. <span data-ttu-id="73fdf-127">На экране связывания выберите **пункт пара щелчков**  >  .</span><span class="sxs-lookup"><span data-stu-id="73fdf-127">On the pairing screen, select **Clicker** > **Pair**.</span></span>

### <a name="charge-the-clicker"></a><span data-ttu-id="73fdf-128">Оплата щелчком</span><span class="sxs-lookup"><span data-stu-id="73fdf-128">Charge the clicker</span></span>

<span data-ttu-id="73fdf-129">Когда батарея разряжена, индикатор батареи мигает оранжевым.</span><span class="sxs-lookup"><span data-stu-id="73fdf-129">When the clicker battery is low, the battery indicator will blink amber.</span></span> <span data-ttu-id="73fdf-130">Подключите микропорт Micro USB к источнику питания USB для оплаты устройства.</span><span class="sxs-lookup"><span data-stu-id="73fdf-130">Plug the Micro USB cable into a USB power supply to charge the device.</span></span>

## <a name="use-the-clicker-with-hololens-1st-gen"></a><span data-ttu-id="73fdf-131">Использование щелчка с HoloLens (1-й общий)</span><span class="sxs-lookup"><span data-stu-id="73fdf-131">Use the clicker with HoloLens (1st gen)</span></span>

### <a name="hold-the-clicker"></a><span data-ttu-id="73fdf-132">Удержание щелчка</span><span class="sxs-lookup"><span data-stu-id="73fdf-132">Hold the clicker</span></span>

<span data-ttu-id="73fdf-133">Чтобы разместить указатель мыши, проведите цикл по кругу или посередине пальца, чтобы порт Micro USB был направлен на ваш компьютер.</span><span class="sxs-lookup"><span data-stu-id="73fdf-133">To put on the clicker, slide the loop over your ring or middle finger so that the Micro USB port faces toward your wrist.</span></span> <span data-ttu-id="73fdf-134">Наведите бегунок в отступы.</span><span class="sxs-lookup"><span data-stu-id="73fdf-134">Rest your thumb in the indentation.</span></span>

![Как удерживать нажатой клавишу](images/use-hololens-clicker-2.png)

### <a name="clicker-gestures"></a><span data-ttu-id="73fdf-136">Жесты щелчка</span><span class="sxs-lookup"><span data-stu-id="73fdf-136">Clicker gestures</span></span>

<span data-ttu-id="73fdf-137">Жесты щелчка — это небольшие ротации, а не большие перемещения, используемые для жестов, выполняемых в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="73fdf-137">Clicker gestures are small wrist rotations, not the larger movements used for HoloLens hand gestures.</span></span> <span data-ttu-id="73fdf-138">И HoloLens распознает жесты и щелкает, даже если щелчок находится за пределами [фрейма жеста](hololens1-basic-usage.md), поэтому вы можете разместить его в расположении, которое наиболее удобно для вас.</span><span class="sxs-lookup"><span data-stu-id="73fdf-138">And HoloLens recognizes your gestures and clicks even if the clicker is outside the [gesture frame](hololens1-basic-usage.md), so you can hold the clicker in the position that's most comfortable for you.</span></span>

- <span data-ttu-id="73fdf-139">**Выберите**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-139">**Select**.</span></span> <span data-ttu-id="73fdf-140">Чтобы выбрать голограмму, кнопку или другой элемент, Взгляните на него, а затем щелкните.</span><span class="sxs-lookup"><span data-stu-id="73fdf-140">To select a hologram, button, or other element, gaze at it, then click.</span></span>

- <span data-ttu-id="73fdf-141">**Нажмите и удерживайте**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-141">**Click and hold**.</span></span> <span data-ttu-id="73fdf-142">Щелкните и удерживайте бегунок кнопки, чтобы выполнить некоторые из тех же действий, которые можно коснуться и удерживать, например переместить или изменить размер голограммы.</span><span class="sxs-lookup"><span data-stu-id="73fdf-142">Click and hold your thumb down on the button to do some of the same things you would with tap and hold, such as move or resize a hologram.</span></span>

- <span data-ttu-id="73fdf-143">**Прокрутка**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-143">**Scroll**.</span></span> <span data-ttu-id="73fdf-144">На панели приложения выберите **инструмент прокрутки**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-144">On the app bar, select **Scroll Tool**.</span></span> <span data-ttu-id="73fdf-145">Щелкните и удерживайте, затем поверните щелчком вверх, вниз, влево или вправо.</span><span class="sxs-lookup"><span data-stu-id="73fdf-145">Click and hold, then rotate the clicker up, down, left, or right.</span></span> <span data-ttu-id="73fdf-146">Чтобы ускорить прокрутку, переместите руку дальше от центра средства прокрутки.</span><span class="sxs-lookup"><span data-stu-id="73fdf-146">To scroll faster, move your hand farther from the center of the scroll tool.</span></span>

- <span data-ttu-id="73fdf-147">**Масштабирование**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-147">**Zoom**.</span></span> <span data-ttu-id="73fdf-148">На панели приложения выберите **инструмент Масштаб**.</span><span class="sxs-lookup"><span data-stu-id="73fdf-148">On the app bar, select **Zoom Tool**.</span></span> <span data-ttu-id="73fdf-149">Щелкните и удерживайте, затем поверните щелчком вверх или вниз, чтобы уменьшить масштаб.</span><span class="sxs-lookup"><span data-stu-id="73fdf-149">Click and hold, then rotate the clicker up to zoom in, or down to zoom out.</span></span>

> [!TIP]
> <span data-ttu-id="73fdf-150">Чтобы увеличить или уменьшить масштаб при использовании Microsoft ребра, Взгляните на страницу и дважды щелкните.</span><span class="sxs-lookup"><span data-stu-id="73fdf-150">To zoom in or out when using Microsoft Edge, gaze at a page and double-click.</span></span>

## <a name="restart-or-recover-the-clicker"></a><span data-ttu-id="73fdf-151">Перезапуск или восстановление щелчка</span><span class="sxs-lookup"><span data-stu-id="73fdf-151">Restart or recover the clicker</span></span>

<span data-ttu-id="73fdf-152">Ниже приведены некоторые действия, которые необходимо выполнить, если щелчок HoloLens не отвечает или не работает правильно.</span><span class="sxs-lookup"><span data-stu-id="73fdf-152">Here are some things to try if the HoloLens clicker is unresponsive or isn’t working well.</span></span>

### <a name="restart-the-clicker"></a><span data-ttu-id="73fdf-153">Перезапуск щелчка</span><span class="sxs-lookup"><span data-stu-id="73fdf-153">Restart the clicker</span></span>

<span data-ttu-id="73fdf-154">Используйте кончик пера для нажатия и удерживания кнопки связывания.</span><span class="sxs-lookup"><span data-stu-id="73fdf-154">Use the tip of a pen to press and hold the pairing button.</span></span> <span data-ttu-id="73fdf-155">В то же время щелкните и удерживайте нажатой кнопку мыши 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="73fdf-155">At the same time, click and hold the clicker for 15 seconds.</span></span> <span data-ttu-id="73fdf-156">Если щелкнуть уже пару с HoloLens, он останется связанным после перезапуска.</span><span class="sxs-lookup"><span data-stu-id="73fdf-156">If the clicker was already paired with your HoloLens, it will stay paired after it restarts.</span></span>

<span data-ttu-id="73fdf-157">Если щелчок не переключается или не перезапускается, попробуйте заключить его в зарядное устройство HoloLens.</span><span class="sxs-lookup"><span data-stu-id="73fdf-157">If the clicker won't turn on or restart, try charging it by using the HoloLens charger.</span></span> <span data-ttu-id="73fdf-158">Если батарея очень низкая, для включения белого индикатора может потребоваться несколько минут.</span><span class="sxs-lookup"><span data-stu-id="73fdf-158">If the battery is very low, it might take a few minutes for the white indicator light to turn on.</span></span>

### <a name="re-pair-the-clicker"></a><span data-ttu-id="73fdf-159">Повторное связывание щелчка</span><span class="sxs-lookup"><span data-stu-id="73fdf-159">Re-pair the clicker</span></span>

<span data-ttu-id="73fdf-160">Выберите **Параметры**  >  **устройства** и щелкните мышью.</span><span class="sxs-lookup"><span data-stu-id="73fdf-160">Select **Settings** > **Devices** and select the clicker.</span></span> <span data-ttu-id="73fdf-161">Выберите **Удалить**, подождите несколько секунд, а затем снова свяжите щелчк.</span><span class="sxs-lookup"><span data-stu-id="73fdf-161">Select **Remove**, wait a few seconds, then pair the clicker again.</span></span>

### <a name="recover-the-clicker"></a><span data-ttu-id="73fdf-162">Восстановление щелчка</span><span class="sxs-lookup"><span data-stu-id="73fdf-162">Recover the clicker</span></span>

<span data-ttu-id="73fdf-163">Если перезапуск и повторное связывание не решает проблему, средство восстановления устройств Windows поможет восстановить его.</span><span class="sxs-lookup"><span data-stu-id="73fdf-163">If restarting and re-pairing the clicker don’t fix the problem, the Windows Device Recovery Tool can help you recover it.</span></span> <span data-ttu-id="73fdf-164">Процесс восстановления может занять некоторое время, и он установит последнюю версию программного обеспечения для щелчка.</span><span class="sxs-lookup"><span data-stu-id="73fdf-164">The recovery process may take some time, and it will install the latest version of the clicker software.</span></span> <span data-ttu-id="73fdf-165">Чтобы использовать это средство, вам потребуется компьютер под Windows 10 или более поздней версии, имеющий не менее 4 ГБ свободного дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="73fdf-165">To use the tool, you’ll need a computer running Windows 10 or later that has at least 4 GB of free storage space.</span></span>

<span data-ttu-id="73fdf-166">Восстановление щелчка:</span><span class="sxs-lookup"><span data-stu-id="73fdf-166">To recover the clicker:</span></span>

1. <span data-ttu-id="73fdf-167">Скачайте и установите [средство восстановления устройств Windows](https://dev.azure.com/ContentIdea/ContentIdea/_queries/query/8a004dbe-73f8-4a32-94bc-368fc2f2a895/) на компьютере.</span><span class="sxs-lookup"><span data-stu-id="73fdf-167">Download and install the [Windows Device Recovery Tool](https://dev.azure.com/ContentIdea/ContentIdea/_queries/query/8a004dbe-73f8-4a32-94bc-368fc2f2a895/) on your computer.</span></span>
1. <span data-ttu-id="73fdf-168">Подключите его к компьютеру с помощью USB-кабеля Micro, поставляемого с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="73fdf-168">Connect the clicker to your computer by using the Micro USB cable that came with your HoloLens.</span></span>
1. <span data-ttu-id="73fdf-169">Запустите средство восстановления устройств Windows и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="73fdf-169">Run the Windows Device Recovery Tool and follow the instructions.</span></span>

<span data-ttu-id="73fdf-170">Если щелчок не обнаруживается автоматически, выберите **устройство не было обнаружено** и следуйте инструкциям, чтобы перевести устройство в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="73fdf-170">If the clicker isn’t automatically detected, select **My device was not detected** and follow the instructions to put your device into recovery mode.</span></span>
