---
title: Повышение качества изображения и комфорта
description: Калибровка межзрачкового расстояния может улучшить качество изображения. Как HoloLens, так и иммерсивная гарнитура Windows Mixed Reality Windows Mixed предоставляют возможность настройки расстояния между зрачками.
author: Teresa-Motiv
ms.author: xerxesb
ms.date: 9/13/2019
ms.topic: article
keywords: калибровка, комфорт, визуальные элементы, качество, расстояние между зрачками
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: ''
manager: jarrettr
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 2f2c8afffdc24eedf9cb6b462448f5ed6ffc8d5d
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10828774"
---
# <span data-ttu-id="cfff3-105">Повышение качества изображения и комфорта</span><span class="sxs-lookup"><span data-stu-id="cfff3-105">Improve visual quality and comfort</span></span>

<span data-ttu-id="cfff3-106">HoloLens 2 и HoloLens (1-е поколение) работают лучше, если они откалиброваны под особенности ваших глаз.</span><span class="sxs-lookup"><span data-stu-id="cfff3-106">HoloLens 2 and HoloLens (1st gen) both work better when they're calibrated to your unique eyes.</span></span>

<span data-ttu-id="cfff3-107">Несмотря на то, что оба устройства необходимо откалибровать для оптимального просмотра голограмм, они используют различные технологии и техники калибровки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-107">While both devices need to calibrate for the best hologram viewing experience, they use different calibration technologies and techniques.</span></span>  <span data-ttu-id="cfff3-108">Перейти в раздел [Калибровка HoloLens 2](#calibrating-your-hololens-2) или [Калибровка HoloLens (1-поколение)](#calibrating-your-hololens-1st-gen).</span><span class="sxs-lookup"><span data-stu-id="cfff3-108">Jump to [HoloLens 2 calibration](#calibrating-your-hololens-2) or [HoloLens (1st gen) calibration](#calibrating-your-hololens-1st-gen).</span></span>

## <span data-ttu-id="cfff3-109">Калибровка HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="cfff3-109">Calibrating your HoloLens 2</span></span>

<span data-ttu-id="cfff3-110">HoloLens 2 использует технологию отслеживания движения глаз для улучшения взаимодействия с виртуальной средой.</span><span class="sxs-lookup"><span data-stu-id="cfff3-110">HoloLens 2 uses eye-tracking technology to improve your experience seeing and interacting with the virtual environment.</span></span> <span data-ttu-id="cfff3-111">При калибровке HoloLens 2 обеспечивается точность отслеживания движения ваших глаз (и глаз других пользователей устройства).</span><span class="sxs-lookup"><span data-stu-id="cfff3-111">Calibrating the HoloLens 2 ensures that it can accurately track your eyes (and the eyes of anyone else who uses the device).</span></span> <span data-ttu-id="cfff3-112">Кроме того, это способствует комфорту пользователя, выравниванию голограммы и отслеживанию рук.</span><span class="sxs-lookup"><span data-stu-id="cfff3-112">It also helps with user comfort, hologram alignment, and hand tracking.</span></span> <span data-ttu-id="cfff3-113">После калибровки голограммы будут отображаться правильно даже при смещении визора на вашей голове.</span><span class="sxs-lookup"><span data-stu-id="cfff3-113">After calibration, holograms will appear correctly even as the visor shifts on your head.</span></span>

<span data-ttu-id="cfff3-114">HoloLens 2 предлагает пользователю выполнить калибровку устройства в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="cfff3-114">HoloLens 2 prompts a user to calibrate the device under the following circumstances:</span></span>

- <span data-ttu-id="cfff3-115">Пользователь использует устройство в первый раз.</span><span class="sxs-lookup"><span data-stu-id="cfff3-115">The user is using the device for the first time</span></span>
- <span data-ttu-id="cfff3-116">Пользователь ранее отказался от процесса калибровки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-116">The user previously opted out of the calibration process</span></span>
- <span data-ttu-id="cfff3-117">Не удалось выполнить калибровку при последнем использовании устройства пользователем.</span><span class="sxs-lookup"><span data-stu-id="cfff3-117">The calibration process did not succeed the last time the user used the device</span></span>
- <span data-ttu-id="cfff3-118">Пользователь удалил свои профили калибровки</span><span class="sxs-lookup"><span data-stu-id="cfff3-118">The user has deleted their calibration profiles</span></span>
- <span data-ttu-id="cfff3-119">Устройство снимается и снова надевается в любом из описанных выше случаев</span><span class="sxs-lookup"><span data-stu-id="cfff3-119">The device is taken off and put back on and any of the above circumstances apply</span></span> 


![Запрос на калибровку](./images/07-et-adjust-for-your-eyes.png)

<span data-ttu-id="cfff3-121">В ходе этого процесса вы увидите набор целевых объектов (драгоценных камней).</span><span class="sxs-lookup"><span data-stu-id="cfff3-121">During this process, you'll look at a set of targets (gems).</span></span> <span data-ttu-id="cfff3-122">Во время калибровки можно моргать, но старайтесь концентрироваться на драгоценных камнях и не смотреть на другие объекты в комнате.</span><span class="sxs-lookup"><span data-stu-id="cfff3-122">It's fine if you blink during calibration, but try to stay focused on the gems instead of other objects in the room.</span></span>  <span data-ttu-id="cfff3-123">Это позволяет HoloLens узнать о положении ваших глаз для отображения голографического мира.</span><span class="sxs-lookup"><span data-stu-id="cfff3-123">This allows HoloLens to learn about your eye position to render your holographic world.</span></span>

![Запрос на калибровку](./images/07-et-hold-head-still.png)

![Запрос на калибровку](./images/08-et-gems.png)

![Запрос на калибровку](./images/09-et-adjusting.png)

<span data-ttu-id="cfff3-127">Если калибровка прошла успешно, будет отображен экран "Успешно".</span><span class="sxs-lookup"><span data-stu-id="cfff3-127">If calibration was successful, you'll see a success screen.</span></span>  <span data-ttu-id="cfff3-128">В противном случае ознакомьтесь с более подробной информацией о [диагностике сбоев калибровки](#troubleshooting-hololens-2-calibration).</span><span class="sxs-lookup"><span data-stu-id="cfff3-128">If not, read more about diagnosing calibration failures [here](#troubleshooting-hololens-2-calibration).</span></span>

![Запрос на калибровку](./images/10-et-success.png)

### <span data-ttu-id="cfff3-130">Калибровка при совместном использовании устройства или сеанса</span><span class="sxs-lookup"><span data-stu-id="cfff3-130">Calibration when sharing a device or session</span></span>

<span data-ttu-id="cfff3-131">Несколько пользователей могут совместно использовать устройство HoloLens 2 без необходимости настройки устройства для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="cfff3-131">Multiple users can share a HoloLens 2 device, without a need for each person to go through device setup.</span></span> <span data-ttu-id="cfff3-132">Когда новый пользователь надевает устройство на голову в первый раз, HoloLens 2 автоматически предлагает ему выполнить калибровку визуальных элементов.</span><span class="sxs-lookup"><span data-stu-id="cfff3-132">When a new user puts the device on their head for the first time, HoloLens 2 automatically prompts the user to calibrate visuals.</span></span> <span data-ttu-id="cfff3-133">Когда устройство надевает пользователь, ранее выполнивший калибровку визуальных элементов, экран автоматически корректирует качество изображения и удобство просмотра.</span><span class="sxs-lookup"><span data-stu-id="cfff3-133">When a user that has previously calibrated visuals puts the device on their head, the display seamlessly adjusts for quality and a comfortable viewing experience.</span></span>  

### <span data-ttu-id="cfff3-134">Запуск процесса калибровки вручную</span><span class="sxs-lookup"><span data-stu-id="cfff3-134">Manually starting the calibration process</span></span>

1. <span data-ttu-id="cfff3-135">Выполните жест "Пуск", чтобы открыть [меню **Пуск**](hololens2-basic-usage.md#start-gesture).</span><span class="sxs-lookup"><span data-stu-id="cfff3-135">Use the start gesture to open the [**Start** menu](hololens2-basic-usage.md#start-gesture).</span></span>
1. <span data-ttu-id="cfff3-136">Если приложение «Параметры» не закреплено в меню **Пуск**, выберите **Все приложения**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-136">If the Settings app isn't pinned to **Start**, select **All Apps**.</span></span>
1. <span data-ttu-id="cfff3-137">Выберите **Параметры**, а затем пункты **Система**  >  **Калибровка**  >  **Калибровка для отслеживания взгляда**  >  **Запустить калибровку для отслеживания взгляда**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-137">Select **Settings**, and then select **System** > **Calibration** > **Eye Calibration** > **Run eye calibration**.</span></span>

   ![Приложение «Параметры» с возможностью запуска калибровки для отслеживания взгляда](./images/C-Settings.Calibration.png)

### <span data-ttu-id="cfff3-139">Устранение неполадок калибровки HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="cfff3-139">Troubleshooting HoloLens 2 calibration</span></span>

<span data-ttu-id="cfff3-140">Для большинства пользователей калибровка должна сработать, но в некоторых случаях происходит сбой калибровки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-140">Calibration should work for most people, but there are cases where calibration fails.</span></span>
  
<span data-ttu-id="cfff3-141">Ниже перечислены возможные причины сбоя калибровки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-141">Some potential reasons for calibration failure include:</span></span>

- <span data-ttu-id="cfff3-142">Пользователь отвлекся и не следил за целями калибровки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-142">Getting distracted and not following the calibration targets</span></span>
- <span data-ttu-id="cfff3-143">Загрязненный или поцарапанный визор устройства или визор расположен неправильно.</span><span class="sxs-lookup"><span data-stu-id="cfff3-143">Dirty or scratched device visor or device visor not positioned properly</span></span>
- <span data-ttu-id="cfff3-144">Загрязненные или поцарапанные очки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-144">Dirty or scratched glasses</span></span>
- <span data-ttu-id="cfff3-145">Некоторые типы контактных линз или очков (цветные контактные линзы, некоторые торические контактные линзы, блокирующие инфракрасные лучи очки, медицинские очки с сильной коррекцией, солнечные очки и т. п.)</span><span class="sxs-lookup"><span data-stu-id="cfff3-145">Certain types of contact lenses and glasses (colored contact lenses, some toric contact lenses, IR blocking glasses, some high prescription glasses, sunglasses, or similar)</span></span>
- <span data-ttu-id="cfff3-146">Сильно выраженный макияж и некоторые типы накладных ресниц</span><span class="sxs-lookup"><span data-stu-id="cfff3-146">More-pronounced makeup and some eyelash extensions</span></span>
- <span data-ttu-id="cfff3-147">Волосы или толстая оправа очков, не позволяющие устройству видеть ваши глаза.</span><span class="sxs-lookup"><span data-stu-id="cfff3-147">Hair or thick eyeglass frames if they are blocking the device from seeing your eyes</span></span>
- <span data-ttu-id="cfff3-148">Определенные особенности строения глаз, заболевания глаз или проведенная хирургическая операция на глазах, например узкие глаза, длинные ресницы, амблиопия, нистагм, некоторые случаи ЛАСИКа и других хирургических операций на глазах.</span><span class="sxs-lookup"><span data-stu-id="cfff3-148">Certain eye physiology, eye conditions or eye surgery such as narrow eyes, long eyelashes, amblyopia, nystagmus, some cases of LASIK or other eye surgeries</span></span>

<span data-ttu-id="cfff3-149">При неудачной попытке калибровки выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cfff3-149">If calibration is unsuccessful try:</span></span>

- <span data-ttu-id="cfff3-150">Очистите визор устройства</span><span class="sxs-lookup"><span data-stu-id="cfff3-150">Cleaning your device visor</span></span>
- <span data-ttu-id="cfff3-151">Очистите свои очки</span><span class="sxs-lookup"><span data-stu-id="cfff3-151">Cleaning your glasses</span></span>
- <span data-ttu-id="cfff3-152">Придвиньте визор устройства как можно ближе к глазам</span><span class="sxs-lookup"><span data-stu-id="cfff3-152">Pushing your device visor as close to your eyes as possible</span></span>
- <span data-ttu-id="cfff3-153">Удалите предметы внутри визора (например, волосы)</span><span class="sxs-lookup"><span data-stu-id="cfff3-153">Moving objects in your visor out of the way (such as hair)</span></span>
- <span data-ttu-id="cfff3-154">Включите освещение в комнате или переместитесь вне зоны попадания прямых солнечных лучей</span><span class="sxs-lookup"><span data-stu-id="cfff3-154">Turning on a light in your room or moving out of direct sunlight</span></span>

<span data-ttu-id="cfff3-155">Если вы не прошли все рекомендации, и при этом калибровка не завершились, можно отключить запрос на калибровку в параметрах.</span><span class="sxs-lookup"><span data-stu-id="cfff3-155">If you followed all guidelines and calibration is still failing, you can disable the calibration prompt in Settings.</span></span> <span data-ttu-id="cfff3-156">Кроме того, сообщите нам об этом, отправив свой отзыв в [Центре отзывов и предложений](hololens-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="cfff3-156">Please also let us know by filing feedback in [Feedback Hub](hololens-feedback.md).</span></span>

<span data-ttu-id="cfff3-157">Обратите внимание, что настройка расстояния между зрачками неприменима для Hololens 2, так как расположение глаз вычисляется системой.</span><span class="sxs-lookup"><span data-stu-id="cfff3-157">Note that setting IPD is not applicable for Hololens 2, since eye positions are computed by the system.</span></span> 

### <span data-ttu-id="cfff3-158">Данные калибровки и безопасность</span><span class="sxs-lookup"><span data-stu-id="cfff3-158">Calibration data and security</span></span>

<span data-ttu-id="cfff3-159">Сведения о калибровке хранятся локально на устройстве и не связываются с какими-либо сведениями учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cfff3-159">Calibration information is stored locally on the device and is not associated with any account information.</span></span> <span data-ttu-id="cfff3-160">Записи об использовании устройства без калибровки не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="cfff3-160">There is no record of who has used the device without calibration.</span></span> <span data-ttu-id="cfff3-161">Это означает, что запрос на калибровку устройства получат новые пользователи при первом использовании устройства, а также пользователи, которые ранее отключили калибровку или провели ее неудачно.</span><span class="sxs-lookup"><span data-stu-id="cfff3-161">This mean new users will get prompted to calibrate visuals when they use the device for the first time, as well as users who opted out of calibration previously or if calibration was unsuccessful.</span></span>

<span data-ttu-id="cfff3-162">В устройстве может локально храниться до 50 профилей калибровки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-162">The device can locally store up to 50 calibration profiles.</span></span> <span data-ttu-id="cfff3-163">По истечении этого числа устройство автоматически удаляет самый старый неиспользованный профиль.</span><span class="sxs-lookup"><span data-stu-id="cfff3-163">After this number is reached, the device automatically deletes the oldest unused profile.</span></span>

<span data-ttu-id="cfff3-164">Сведения о калибровке всегда можно удалить с устройства в разделе **Параметры** > **Конфиденциальность** > **Устройство отслеживания взгляда**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-164">Calibration information can always be deleted from the device in **Settings** > **Privacy** > **Eye tracker**.</span></span>  

### <span data-ttu-id="cfff3-165">Отключение калибровки</span><span class="sxs-lookup"><span data-stu-id="cfff3-165">Disable calibration</span></span>

<span data-ttu-id="cfff3-166">Вы также можете отключить запрос на калибровку, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cfff3-166">You can also disable the calibration prompt by following these steps:</span></span>

1. <span data-ttu-id="cfff3-167">Выберите **Параметры** > **Система** > **Калибровка**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-167">Select **Settings** > **System** > **Calibration**.</span></span>
1. <span data-ttu-id="cfff3-168">Отключите параметр **Когда новый пользователь использует это устройство HoloLens, автоматически отображать запрос на выполнение калибровки для отслеживания взгляда**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-168">Turn off **When a new person uses this HoloLens, automatically ask to run eye calibration**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfff3-169">Этот параметр может негативно повлиять на качество и комфорт отображения голограмм.</span><span class="sxs-lookup"><span data-stu-id="cfff3-169">This setting may adversely affect hologram rendering quality and comfort.</span></span>  <span data-ttu-id="cfff3-170">При отключении этого параметра функции, зависящие от отслеживания глаз (например, прокрутка текста), больше не будут работать в иммерсивных приложениях.</span><span class="sxs-lookup"><span data-stu-id="cfff3-170">When you turn off this setting, features that depend on eye tracking (such as text scrolling) no longer work in immersive applications.</span></span>

### <span data-ttu-id="cfff3-171">Технология отслеживания взгляда HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="cfff3-171">HoloLens 2 eye-tracking technology</span></span>

<span data-ttu-id="cfff3-172">Устройство использует технологию отслеживания взгляда для улучшения качества отображения, а также точности расположения голограмм в трехмерном пространстве и комфорта при их просмотре.</span><span class="sxs-lookup"><span data-stu-id="cfff3-172">The device uses its eye-tracking technology to improve display quality, and to ensure that all holograms are positioned accurately and comfortable to view in 3D.</span></span> <span data-ttu-id="cfff3-173">Так как глаза в этой технологии используются в качестве ориентиров, устройство может самостоятельно выполнять корректировку для каждого пользователя и настраивать визуальные элементы при незначительном смещении гарнитуры во время использования.</span><span class="sxs-lookup"><span data-stu-id="cfff3-173">Because it uses the eyes as landmarks, the device can adjust itself for every user and tune its visuals as the headset shifts slightly throughout use.</span></span>  <span data-ttu-id="cfff3-174">Все изменения вносятся в режиме реального времени без необходимости ручной настройки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-174">All adjustments happen on the fly without a need for manual tuning.</span></span>
> [!NOTE]
> <span data-ttu-id="cfff3-175">Настройка расстояния между зрачками неприменима для Hololens 2, так как расположение глаз вычисляется системой.</span><span class="sxs-lookup"><span data-stu-id="cfff3-175">Setting the IPD is not applicable for Hololens 2, since eye positions are computed by the system.</span></span>

<span data-ttu-id="cfff3-176">Приложения HoloLens используют отслеживание взгляда для определения направления вашего взгляда в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="cfff3-176">HoloLens applications use eye tracking to track where you are looking in real time.</span></span> <span data-ttu-id="cfff3-177">Это основная возможность, которую могут использовать разработчики для реализации совершенно нового уровня контекста, понимания человеком и взаимодействия пользователя с голограммами.</span><span class="sxs-lookup"><span data-stu-id="cfff3-177">This is the main capability developers can leverage to enable a whole new level of context, human understanding and interactions within the Holographic experience.</span></span> <span data-ttu-id="cfff3-178">Для использования этой возможности разработчикам не нужно предпринимать никаких действий.</span><span class="sxs-lookup"><span data-stu-id="cfff3-178">Developers don’t need to do anything to leverage this capability.</span></span>

## <span data-ttu-id="cfff3-179">Калибровка HoloLens (1-е поколение)</span><span class="sxs-lookup"><span data-stu-id="cfff3-179">Calibrating your HoloLens (1st gen)</span></span>

<span data-ttu-id="cfff3-180">HoloLens (1-е поколение) корректирует отображение голограммы в соответствии с вашим [расстоянием между зрачками](https://en.wikipedia.org/wiki/Interpupillary_distance).</span><span class="sxs-lookup"><span data-stu-id="cfff3-180">HoloLens (1st gen) adjusts hologram display according to the your [interpupillary distance](https://en.wikipedia.org/wiki/Interpupillary_distance) (IPD).</span></span> <span data-ttu-id="cfff3-181">Если это расстояние определено неточно, голограмма может выглядеть нестабильной или отображаться на неверном расстоянии.</span><span class="sxs-lookup"><span data-stu-id="cfff3-181">If the IPD is not accurate, holograms may appear unstable or at an incorrect distance.</span></span> <span data-ttu-id="cfff3-182">Вы можете улучшить качество изображения с помощью калибровки в соответствии с вашим межзрачковым расстоянием.</span><span class="sxs-lookup"><span data-stu-id="cfff3-182">You can improve the quality of your visuals by calibrating the device to your interpupillary distance (IPD).</span></span>

<span data-ttu-id="cfff3-183">При настройке устройства HoloLens (1-е поколение) оно предложит провести калибровку визуальных элементов после того, как Кортана представится.</span><span class="sxs-lookup"><span data-stu-id="cfff3-183">When you set up your Hololens (1st gen) device, it prompts to calibrate your visuals after Cortana introduces herself.</span></span> <span data-ttu-id="cfff3-184">Рекомендуется выполнить калибровку на этом этапе настройки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-184">It's recommended that you complete the calibration step during this setup phase.</span></span> <span data-ttu-id="cfff3-185">Однако вы можете пропустить калибровку, дождавшись запроса Кортаны и ответив "Skip" ("Пропустить").</span><span class="sxs-lookup"><span data-stu-id="cfff3-185">However you can skip it by waiting until Cortana prompts you and then saying "Skip."</span></span>

<span data-ttu-id="cfff3-186">В процессе калибровки HoloLens предложит направить палец на серию из шести целей на каждый глаз.</span><span class="sxs-lookup"><span data-stu-id="cfff3-186">During the calibration process, HoloLens asks you to align your finger with a series of six targets per eye.</span></span> <span data-ttu-id="cfff3-187">HoloLens использует этот процесс для правильной настройки вашего расстояния между зрачками.</span><span class="sxs-lookup"><span data-stu-id="cfff3-187">HoloLens uses this process to set the IPD correctly for your eyes.</span></span>

![Экран настройки расстояния между зрачками на втором шаге](./images/ipd-finger-alignment-300px.jpg)

### <span data-ttu-id="cfff3-189">Запуск процесса калибровки вручную</span><span class="sxs-lookup"><span data-stu-id="cfff3-189">Manually start the calibration process</span></span>

<span data-ttu-id="cfff3-190">Если вам необходимо обновить калибровку или провести ее для нового пользователя, вы можете в любое время запустить приложение калибровки вручную.</span><span class="sxs-lookup"><span data-stu-id="cfff3-190">If you need to update the calibration or if a new user needs to adjust it, you can manually run the Calibration app at any time.</span></span> <span data-ttu-id="cfff3-191">Приложение калибровки установлено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cfff3-191">The Calibration app is installed by default.</span></span> <span data-ttu-id="cfff3-192">Доступ к нему можно получить с помощью меню **Пуск** или приложения "Параметры".</span><span class="sxs-lookup"><span data-stu-id="cfff3-192">You can access it by using eihter the **Start** menu or the Settings app.</span></span>

<span data-ttu-id="cfff3-193">Чтобы запустить приложение калибровки с помощью меню **Пуск**, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cfff3-193">To use the **Start** menu to run the Calibration app, follow these steps:</span></span>

1. <span data-ttu-id="cfff3-194">Используйте жест [раскрытия ладони](hololens1-basic-usage.md), чтобы открыть меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-194">Use the [bloom](hololens1-basic-usage.md) gesture to open the **Start** menu.</span></span>
1. <span data-ttu-id="cfff3-195">Чтобы просмотреть все приложения, выберите **+**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-195">To view all apps, select **+**.</span></span>
1. <span data-ttu-id="cfff3-196">Выберите пункт **Калибровка**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-196">Select **Calibration**.</span></span>

![Доступ к приложению калибровки из оболочки](./images/calibration-shell.png)

![Приложение калибровки, отображаемое в виде динамического куба после запуска](./images/calibration-livecube-200px.png)

<span data-ttu-id="cfff3-199">Чтобы запустить приложение калибровки с помощью приложения "Параметры", выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cfff3-199">To use the Settings app to run the Calibration app, follow these steps:</span></span>

1. <span data-ttu-id="cfff3-200">Используйте жест [раскрытия ладони](hololens1-basic-usage.md), чтобы открыть меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-200">Use the [bloom](hololens1-basic-usage.md) gesture to open the **Start** menu.</span></span>
1. <span data-ttu-id="cfff3-201">Если приложение **Параметры** не закреплено в меню \*\*Пуск \*\*, выберите **+** для просмотра всех приложений.</span><span class="sxs-lookup"><span data-stu-id="cfff3-201">If **Settings** isn't pinned to **Start**, select **+** to view all apps.</span></span>
1. <span data-ttu-id="cfff3-202">Выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-202">Select **Settings**.</span></span>
1. <span data-ttu-id="cfff3-203">Выберите **Система** > **Служебные программы** > **Запустить приложение "Калибровка"**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-203">Select **System** > **Utilities** > **Open Calibration**.</span></span>

![Запуск приложения калибровки из приложения "Параметры"](./images/calibration-settings-500px.jpg)

## <span data-ttu-id="cfff3-205">Иммерсивные гарнитуры</span><span class="sxs-lookup"><span data-stu-id="cfff3-205">Immersive headsets</span></span>

<span data-ttu-id="cfff3-206">Некоторые иммерсивные гарнитуры предоставляют возможность настраивать параметр расстояния между зрачками.</span><span class="sxs-lookup"><span data-stu-id="cfff3-206">Some immersive headsets provide the ability to customize the IPD setting.</span></span> <span data-ttu-id="cfff3-207">Чтобы изменить расстояние между зрачками для гарнитуры, откройте приложение "Параметры" и выберите **Смешанная реальность** > **Отображение гарнитуры** и передвиньте ползунок регулировки.</span><span class="sxs-lookup"><span data-stu-id="cfff3-207">To change the IPD for your headset, open the Settings app and select **Mixed reality** > **Headset display**, and then move the slider control.</span></span> <span data-ttu-id="cfff3-208">Изменения отображаются на гарнитуре в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="cfff3-208">You’ll see the changes in real time in your headset.</span></span> <span data-ttu-id="cfff3-209">Если вы знаете расстояние между своими зрачками, например после посещения оптометриста, вы также можете ввести точное значение.</span><span class="sxs-lookup"><span data-stu-id="cfff3-209">If you know your IPD, maybe from a visit to the optometrist, you can enter it directly as well.</span></span>

<span data-ttu-id="cfff3-210">Кроме того, вы настроить этот параметр на компьютере, выбрав пункты **Параметры** > **Смешанная реальность** > **Отображение гарнитуры**.</span><span class="sxs-lookup"><span data-stu-id="cfff3-210">You can also adjust this setting on your PC by selecting **Settings** > **Mixed reality** > **Headset display**.</span></span>

<span data-ttu-id="cfff3-211">Если гарнитура не поддерживает настройку расстояния между зрачками, этот параметр будет отключен.</span><span class="sxs-lookup"><span data-stu-id="cfff3-211">If your headset does not support IPD customization, this setting will be disabled.</span></span>
