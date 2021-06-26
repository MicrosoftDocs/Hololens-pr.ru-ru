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
ms.openlocfilehash: 83e5a746b6900c547778c71a0855426563458032
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112924066"
---
# <a name="use-the-hololens-1st-gen-clicker"></a><span data-ttu-id="4422f-104">Использование пульта HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="4422f-104">Use the HoloLens (1st gen) clicker</span></span>

<span data-ttu-id="4422f-105">Этот щелчок разработан специально для HoloLens (1-го поколения) и предоставляет еще один способ взаимодействия с голограммами.</span><span class="sxs-lookup"><span data-stu-id="4422f-105">The clicker was designed specifically for HoloLens (1st gen) and gives you another way to interact with holograms.</span></span> <span data-ttu-id="4422f-106">Он поставляется с HoloLens (1-го поколения) в отдельном поле.</span><span class="sxs-lookup"><span data-stu-id="4422f-106">It comes with HoloLens (1st gen), in a separate box.</span></span>

<span data-ttu-id="4422f-107">Используйте его вместо жестов руки для выбора, прокрутки, перемещения и изменения размера приложений.</span><span class="sxs-lookup"><span data-stu-id="4422f-107">Use it in place of hand gestures to select, scroll, move, and resize apps.</span></span>

## <a name="clicker-hardware-and-pairing"></a><span data-ttu-id="4422f-108">Щелкните Оборудование и свяжите</span><span class="sxs-lookup"><span data-stu-id="4422f-108">Clicker hardware and pairing</span></span>

<span data-ttu-id="4422f-109">У щелчка по HoloLens (1-го поколения) есть цикл пальца, чтобы упростить его хранение и индикатор индикатора.</span><span class="sxs-lookup"><span data-stu-id="4422f-109">The HoloLens (1st gen) clicker has a finger loop to make it easier to hold, and an indicator light.</span></span>

![Щелчок HoloLens](images/use-hololens-clicker-1.png)

### <a name="clicker-indicator-lights"></a><span data-ttu-id="4422f-111">Индикаторы индикаторов щелчков</span><span class="sxs-lookup"><span data-stu-id="4422f-111">Clicker indicator lights</span></span>

<span data-ttu-id="4422f-112">Вот что означают индикаторы щелчка.</span><span class="sxs-lookup"><span data-stu-id="4422f-112">Here's what the lights on the clicker mean.</span></span>

- <span data-ttu-id="4422f-113">**Мигающий белый цвет**.</span><span class="sxs-lookup"><span data-stu-id="4422f-113">**Blinking white**.</span></span> <span data-ttu-id="4422f-114">Щелчок выполняется в режиме связывания.</span><span class="sxs-lookup"><span data-stu-id="4422f-114">The clicker is in pairing mode.</span></span>
- <span data-ttu-id="4422f-115">**Быстрая мигающий белый цвет**.</span><span class="sxs-lookup"><span data-stu-id="4422f-115">**Fast-blinking white**.</span></span> <span data-ttu-id="4422f-116">Связывание выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="4422f-116">Pairing was successful.</span></span>
- <span data-ttu-id="4422f-117">**Сплошной белый цвет**.</span><span class="sxs-lookup"><span data-stu-id="4422f-117">**Solid white**.</span></span> <span data-ttu-id="4422f-118">Щелчок мыши выдает оплату.</span><span class="sxs-lookup"><span data-stu-id="4422f-118">The clicker is charging.</span></span>
- <span data-ttu-id="4422f-119">**Мигающий оранжевый**.</span><span class="sxs-lookup"><span data-stu-id="4422f-119">**Blinking amber**.</span></span> <span data-ttu-id="4422f-120">Батарея мала.</span><span class="sxs-lookup"><span data-stu-id="4422f-120">The battery is low.</span></span>
- <span data-ttu-id="4422f-121">**Горит оранжевым цветом**.</span><span class="sxs-lookup"><span data-stu-id="4422f-121">**Solid amber**.</span></span> <span data-ttu-id="4422f-122">При нажатии кнопки мыши возникла ошибка, и ее потребуется перезапустить.</span><span class="sxs-lookup"><span data-stu-id="4422f-122">The clicker ran into an error and you'll need to restart it.</span></span> <span data-ttu-id="4422f-123">Нажав кнопку связывания, щелкните и удерживайте ее в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="4422f-123">While pressing the pairing button, click and hold for 15 seconds.</span></span>

### <a name="pair-the-clicker-with-your-hololens-1st-gen"></a><span data-ttu-id="4422f-124">Связывание щелчка с HoloLens (1-й общий)</span><span class="sxs-lookup"><span data-stu-id="4422f-124">Pair the clicker with your HoloLens (1st gen)</span></span>

1. <span data-ttu-id="4422f-125">Используйте жест раскрытия для перехода в **Начало**, выберите **Параметры**  >  **устройства** и убедитесь, что Bluetooth включен.</span><span class="sxs-lookup"><span data-stu-id="4422f-125">Use the bloom gesture to go to **Start**, then select **Settings** > **Devices** and verify that Bluetooth is on.</span></span>
1. <span data-ttu-id="4422f-126">В щелчке мыши нажмите и удерживайте кнопку связывания, пока состояние светло не мигает белым цветом.</span><span class="sxs-lookup"><span data-stu-id="4422f-126">On the clicker, press and hold the pairing button until the status light blinks white.</span></span>
1. <span data-ttu-id="4422f-127">На экране связывания выберите **пункт пара щелчков**  >  .</span><span class="sxs-lookup"><span data-stu-id="4422f-127">On the pairing screen, select **Clicker** > **Pair**.</span></span>

### <a name="charge-the-clicker"></a><span data-ttu-id="4422f-128">Оплата щелчком</span><span class="sxs-lookup"><span data-stu-id="4422f-128">Charge the clicker</span></span>

<span data-ttu-id="4422f-129">Когда батарея разряжена, индикатор батареи мигает оранжевым.</span><span class="sxs-lookup"><span data-stu-id="4422f-129">When the clicker battery is low, the battery indicator will blink amber.</span></span> <span data-ttu-id="4422f-130">Подключите микропорт Micro USB к источнику питания USB для оплаты устройства.</span><span class="sxs-lookup"><span data-stu-id="4422f-130">Plug the Micro USB cable into a USB power supply to charge the device.</span></span>

## <a name="use-the-clicker-with-hololens-1st-gen"></a><span data-ttu-id="4422f-131">Использование щелчка с HoloLens (1-й общий)</span><span class="sxs-lookup"><span data-stu-id="4422f-131">Use the clicker with HoloLens (1st gen)</span></span>

### <a name="hold-the-clicker"></a><span data-ttu-id="4422f-132">Удержание щелчка</span><span class="sxs-lookup"><span data-stu-id="4422f-132">Hold the clicker</span></span>

<span data-ttu-id="4422f-133">Чтобы разместить указатель мыши, проведите цикл по кругу или посередине пальца, чтобы порт Micro USB был направлен на ваш компьютер.</span><span class="sxs-lookup"><span data-stu-id="4422f-133">To put on the clicker, slide the loop over your ring or middle finger so that the Micro USB port faces toward your wrist.</span></span> <span data-ttu-id="4422f-134">Наведите бегунок в отступы.</span><span class="sxs-lookup"><span data-stu-id="4422f-134">Rest your thumb in the indentation.</span></span>

![Как удерживать нажатой клавишу](images/use-hololens-clicker-2.png)

### <a name="clicker-gestures"></a><span data-ttu-id="4422f-136">Жесты щелчка</span><span class="sxs-lookup"><span data-stu-id="4422f-136">Clicker gestures</span></span>

<span data-ttu-id="4422f-137">Жесты щелчка — это небольшие ротации, а не большие перемещения, используемые для жестов, выполняемых в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4422f-137">Clicker gestures are small wrist rotations, not the larger movements used for HoloLens hand gestures.</span></span> <span data-ttu-id="4422f-138">И HoloLens распознает жесты и щелкает, даже если щелчок находится за пределами [фрейма жеста](hololens1-basic-usage.md), поэтому вы можете разместить его в расположении, которое наиболее удобно для вас.</span><span class="sxs-lookup"><span data-stu-id="4422f-138">And HoloLens recognizes your gestures and clicks even if the clicker is outside the [gesture frame](hololens1-basic-usage.md), so you can hold the clicker in the position that's most comfortable for you.</span></span>

- <span data-ttu-id="4422f-139">**Выберите**.</span><span class="sxs-lookup"><span data-stu-id="4422f-139">**Select**.</span></span> <span data-ttu-id="4422f-140">Чтобы выбрать голограмму, кнопку или другой элемент, Взгляните на него, а затем щелкните.</span><span class="sxs-lookup"><span data-stu-id="4422f-140">To select a hologram, button, or other element, gaze at it, then click.</span></span>

- <span data-ttu-id="4422f-141">**Нажмите и удерживайте**.</span><span class="sxs-lookup"><span data-stu-id="4422f-141">**Click and hold**.</span></span> <span data-ttu-id="4422f-142">Щелкните и удерживайте бегунок кнопки, чтобы выполнить некоторые из тех же действий, которые можно коснуться и удерживать, например переместить или изменить размер голограммы.</span><span class="sxs-lookup"><span data-stu-id="4422f-142">Click and hold your thumb down on the button to do some of the same things you would with tap and hold, such as move or resize a hologram.</span></span>

- <span data-ttu-id="4422f-143">**Прокрутка**.</span><span class="sxs-lookup"><span data-stu-id="4422f-143">**Scroll**.</span></span> <span data-ttu-id="4422f-144">На панели приложения выберите **инструмент прокрутки**.</span><span class="sxs-lookup"><span data-stu-id="4422f-144">On the app bar, select **Scroll Tool**.</span></span> <span data-ttu-id="4422f-145">Щелкните и удерживайте, затем поверните щелчком вверх, вниз, влево или вправо.</span><span class="sxs-lookup"><span data-stu-id="4422f-145">Click and hold, then rotate the clicker up, down, left, or right.</span></span> <span data-ttu-id="4422f-146">Чтобы ускорить прокрутку, переместите руку дальше от центра средства прокрутки.</span><span class="sxs-lookup"><span data-stu-id="4422f-146">To scroll faster, move your hand farther from the center of the scroll tool.</span></span>

- <span data-ttu-id="4422f-147">**Масштабирование**.</span><span class="sxs-lookup"><span data-stu-id="4422f-147">**Zoom**.</span></span> <span data-ttu-id="4422f-148">На панели приложения выберите **инструмент Масштаб**.</span><span class="sxs-lookup"><span data-stu-id="4422f-148">On the app bar, select **Zoom Tool**.</span></span> <span data-ttu-id="4422f-149">Щелкните и удерживайте, затем поверните щелчком вверх или вниз, чтобы уменьшить масштаб.</span><span class="sxs-lookup"><span data-stu-id="4422f-149">Click and hold, then rotate the clicker up to zoom in, or down to zoom out.</span></span>

> [!TIP]
> <span data-ttu-id="4422f-150">Чтобы увеличить или уменьшить масштаб при использовании Microsoft ребра, Взгляните на страницу и дважды щелкните.</span><span class="sxs-lookup"><span data-stu-id="4422f-150">To zoom in or out when using Microsoft Edge, gaze at a page and double-click.</span></span>

## <a name="im-having-problems-using-the-hololens-clicker"></a><span data-ttu-id="4422f-151">Возникли проблемы при использовании щелчка HoloLens</span><span class="sxs-lookup"><span data-stu-id="4422f-151">I'm having problems using the HoloLens clicker</span></span>

<span data-ttu-id="4422f-152">Используйте [щелчком мыши](hololens1-clicker.md) , чтобы выбрать, прокрутить, переместить и изменить размер голограмм.</span><span class="sxs-lookup"><span data-stu-id="4422f-152">Use the [clicker](hololens1-clicker.md) to select, scroll, move, and resize holograms.</span></span> <span data-ttu-id="4422f-153">Отдельные приложения могут поддерживать дополнительные жесты щелчка.</span><span class="sxs-lookup"><span data-stu-id="4422f-153">Individual apps may support additional clicker gestures.</span></span>

<span data-ttu-id="4422f-154">Если при использовании щелчка возникли проблемы, убедитесь, что он заряжен и связан с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4422f-154">If you're having trouble using the clicker, make sure that it's charged and paired with your HoloLens.</span></span> <span data-ttu-id="4422f-155">Если батарея низкая, индикатор горит оранжевый.</span><span class="sxs-lookup"><span data-stu-id="4422f-155">If the battery is low, the indicator light blinks amber.</span></span> <span data-ttu-id="4422f-156">Чтобы убедиться, что щелчок связан, перейдите в раздел **Параметры**  >  **устройства** и проверьте, отображается ли он там.</span><span class="sxs-lookup"><span data-stu-id="4422f-156">To verify that the clicker is paired, go to **Settings** > **Devices** and see if it shows up there.</span></span> <span data-ttu-id="4422f-157">Дополнительные сведения см. [в разделе Связывание щелчка](hololens1-clicker.md).</span><span class="sxs-lookup"><span data-stu-id="4422f-157">For more information, see [Pair the clicker](hololens1-clicker.md).</span></span>

<span data-ttu-id="4422f-158">Если при работе с щелчком взимается плата и у вас по-прежнему возникают проблемы, сбросьте ее, удерживая нажатой кнопку Main и кнопку связывания в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="4422f-158">If the clicker is charged and paired and you're still having problems, reset it by holding down the main button and the pairing button for 15 seconds.</span></span> <span data-ttu-id="4422f-159">Затем снова свяжите этот элемент с помощью HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4422f-159">Then pair the clicker with your HoloLens again.</span></span>

<span data-ttu-id="4422f-160">Если сброс параметров щелчка не поможет, см. раздел [перезапуск или восстановление щелчка HoloLens](hololens1-clicker.md#restart-or-recover-the-clicker).</span><span class="sxs-lookup"><span data-stu-id="4422f-160">If resetting the clicker doesn't help, see [Restart or recover the HoloLens clicker](hololens1-clicker.md#restart-or-recover-the-clicker).</span></span>
## <a name="restart-or-recover-the-clicker"></a><span data-ttu-id="4422f-161">Перезапуск или восстановление щелчка</span><span class="sxs-lookup"><span data-stu-id="4422f-161">Restart or recover the clicker</span></span>

<span data-ttu-id="4422f-162">Ниже приведены некоторые действия, которые необходимо выполнить, если щелчок HoloLens не отвечает или не работает правильно.</span><span class="sxs-lookup"><span data-stu-id="4422f-162">Here are some things to try if the HoloLens clicker is unresponsive or isn’t working well.</span></span>

### <a name="restart-the-clicker"></a><span data-ttu-id="4422f-163">Перезапуск щелчка</span><span class="sxs-lookup"><span data-stu-id="4422f-163">Restart the clicker</span></span>

<span data-ttu-id="4422f-164">Используйте кончик пера для нажатия и удерживания кнопки связывания.</span><span class="sxs-lookup"><span data-stu-id="4422f-164">Use the tip of a pen to press and hold the pairing button.</span></span> <span data-ttu-id="4422f-165">В то же время щелкните и удерживайте нажатой кнопку мыши 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="4422f-165">At the same time, click and hold the clicker for 15 seconds.</span></span> <span data-ttu-id="4422f-166">Если щелкнуть уже пару с HoloLens, он останется связанным после перезапуска.</span><span class="sxs-lookup"><span data-stu-id="4422f-166">If the clicker was already paired with your HoloLens, it will stay paired after it restarts.</span></span>

<span data-ttu-id="4422f-167">Если щелчок не переключается или не перезапускается, попробуйте заключить его в зарядное устройство HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4422f-167">If the clicker won't turn on or restart, try charging it by using the HoloLens charger.</span></span> <span data-ttu-id="4422f-168">Если батарея очень низкая, для включения белого индикатора может потребоваться несколько минут.</span><span class="sxs-lookup"><span data-stu-id="4422f-168">If the battery is very low, it might take a few minutes for the white indicator light to turn on.</span></span>

### <a name="re-pair-the-clicker"></a><span data-ttu-id="4422f-169">Повторное связывание щелчка</span><span class="sxs-lookup"><span data-stu-id="4422f-169">Re-pair the clicker</span></span>

<span data-ttu-id="4422f-170">Выберите **Параметры**  >  **устройства** и щелкните мышью.</span><span class="sxs-lookup"><span data-stu-id="4422f-170">Select **Settings** > **Devices** and select the clicker.</span></span> <span data-ttu-id="4422f-171">Выберите **Удалить**, подождите несколько секунд, а затем снова свяжите щелчк.</span><span class="sxs-lookup"><span data-stu-id="4422f-171">Select **Remove**, wait a few seconds, then pair the clicker again.</span></span>

### <a name="recover-the-clicker"></a><span data-ttu-id="4422f-172">Восстановление щелчка</span><span class="sxs-lookup"><span data-stu-id="4422f-172">Recover the clicker</span></span>

<span data-ttu-id="4422f-173">Если перезапуск и повторное связывание не решает проблему, средство восстановления устройств Windows поможет восстановить его.</span><span class="sxs-lookup"><span data-stu-id="4422f-173">If restarting and re-pairing the clicker don’t fix the problem, the Windows Device Recovery Tool can help you recover it.</span></span> <span data-ttu-id="4422f-174">Процесс восстановления может занять некоторое время, и он установит последнюю версию программного обеспечения для щелчка.</span><span class="sxs-lookup"><span data-stu-id="4422f-174">The recovery process may take some time, and it will install the latest version of the clicker software.</span></span> <span data-ttu-id="4422f-175">Чтобы использовать это средство, вам потребуется компьютер под Windows 10 или более поздней версии, имеющий не менее 4 ГБ свободного дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="4422f-175">To use the tool, you’ll need a computer running Windows 10 or later that has at least 4 GB of free storage space.</span></span>

<span data-ttu-id="4422f-176">Восстановление щелчка:</span><span class="sxs-lookup"><span data-stu-id="4422f-176">To recover the clicker:</span></span>

1. <span data-ttu-id="4422f-177">Скачайте и установите [средство восстановления устройств Windows](https://dev.azure.com/ContentIdea/ContentIdea/_queries/query/8a004dbe-73f8-4a32-94bc-368fc2f2a895/) на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4422f-177">Download and install the [Windows Device Recovery Tool](https://dev.azure.com/ContentIdea/ContentIdea/_queries/query/8a004dbe-73f8-4a32-94bc-368fc2f2a895/) on your computer.</span></span>
1. <span data-ttu-id="4422f-178">Подключите его к компьютеру с помощью USB-кабеля Micro, поставляемого с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4422f-178">Connect the clicker to your computer by using the Micro USB cable that came with your HoloLens.</span></span>
1. <span data-ttu-id="4422f-179">Запустите средство восстановления устройств Windows и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="4422f-179">Run the Windows Device Recovery Tool and follow the instructions.</span></span>

<span data-ttu-id="4422f-180">Если щелчок не обнаруживается автоматически, выберите **устройство не было обнаружено** и следуйте инструкциям, чтобы перевести устройство в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="4422f-180">If the clicker isn’t automatically detected, select **My device was not detected** and follow the instructions to put your device into recovery mode.</span></span>

