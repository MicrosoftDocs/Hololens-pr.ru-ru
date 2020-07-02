---
title: Использование голосовых команд для работы с HoloLens
description: Кортана поможет вам выполнять все виды действий с гарнитурой HoloLens
ms.assetid: fd96fb0e-6759-4dbe-be1f-58bedad66fed
ms.date: 03/10/2020
keywords: hololens
ms.prod: hololens
ms.sitesec: library
author: Teresa-Motiv
audience: ITPro
ms.author: v-tea
ms.topic: article
manager: jarrettr
ms.localizationpriority: high
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: d6fc83e81ce6f02047cff8a5d1944156f769e056
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10829235"
---
# <span data-ttu-id="aa685-104">Использование голосовых команд для работы с HoloLens</span><span class="sxs-lookup"><span data-stu-id="aa685-104">Use your voice to operate HoloLens</span></span>

<span data-ttu-id="aa685-105">Вы можете использовать голосовые команды для выполнения практически любых действий на HoloLens, таких как быстрая фотосъемка или открытие приложения.</span><span class="sxs-lookup"><span data-stu-id="aa685-105">You can use your voice to do almost anything on HoloLens, such as taking a quick photo or opening an app.</span></span> <span data-ttu-id="aa685-106">Многие голосовые команды встроены в HoloLens, а другие доступны с помощью Кортаны.</span><span class="sxs-lookup"><span data-stu-id="aa685-106">Many voice commands are built into HoloLens, while others are available through Cortana.</span></span>

<span data-ttu-id="aa685-107">В этой статье рассказывается о том, как управлять HoloLens и голографическим миром с помощью голосовых команд и Кортаны.</span><span class="sxs-lookup"><span data-stu-id="aa685-107">This article teaches you how to control HoloLens and your holographic world with your voice and with Cortana.</span></span>

> [!NOTE]
> <span data-ttu-id="aa685-108">Голосовые функции поддерживаются только на [некоторых языках](hololens2-language-support.md).</span><span class="sxs-lookup"><span data-stu-id="aa685-108">Speech is only supported in [some languages](hololens2-language-support.md).</span></span> <span data-ttu-id="aa685-109">Язык голосовых функций зависит от языка интерфейса Windows, а не языка клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="aa685-109">The speech language is based on the Windows display language, not the keyboard language.</span></span>  
>  
> <span data-ttu-id="aa685-110">Чтобы узнать язык интерфейса Windows, выберите **Параметры** > **Время и язык** > **Язык**.</span><span class="sxs-lookup"><span data-stu-id="aa685-110">You can verify the Windows display language by selecting **Settings** > **Time and Language** > **Language**.</span></span>

## <span data-ttu-id="aa685-111">Встроенные голосовые команды</span><span class="sxs-lookup"><span data-stu-id="aa685-111">Built-in voice commands</span></span>

<span data-ttu-id="aa685-112">Работайте с HoloLens быстрее с помощью этих основных команд.</span><span class="sxs-lookup"><span data-stu-id="aa685-112">Get around HoloLens faster with these basic commands.</span></span> <span data-ttu-id="aa685-113">Чтобы воспользоваться ими, при первом запуске устройства включите "Речь" или выберите **Настройки** > **Конфиденциальность** > **Речь**.</span><span class="sxs-lookup"><span data-stu-id="aa685-113">In order to use these, you need to enable Speech during the first run of the device or in **Settings** > **Privacy** > **Speech**.</span></span> <span data-ttu-id="aa685-114">Вы всегда можете узнать, включена ли речь, проверив состояние в верхней части меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="aa685-114">You can always check whether speech is enabled by looking at the status at the top of the Start menu.</span></span> <span data-ttu-id="aa685-115">Для достижения наилучших результатов распознавания речи в HoloLens2 используются облачные службы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="aa685-115">For the best speech recognition results, HoloLens 2 uses the Microsoft cloud-based services.</span></span> <span data-ttu-id="aa685-116">Однако вы можете отключить эту функцию в разделе "Настройки".</span><span class="sxs-lookup"><span data-stu-id="aa685-116">However, you can use Settings to disable this feature.</span></span> <span data-ttu-id="aa685-117">Чтобы сделать это, в разделе "Настройки" отключите **Распознавание речи в сети**.</span><span class="sxs-lookup"><span data-stu-id="aa685-117">To do this, in Settings, turn off **Online speech recognition**.</span></span> <span data-ttu-id="aa685-118">После изменения этого параметра в HoloLens 2 голосовые данные при распознавании команд и диктовке будут обрабатываться только локально, а Кортана будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="aa685-118">After you change this setting, HoloLens 2 will only process voice data locally to recognize commands and dictation, and Cortana will not be available.</span></span>

### <span data-ttu-id="aa685-119">Общие голосовые команды</span><span class="sxs-lookup"><span data-stu-id="aa685-119">General speech commands</span></span>

<span data-ttu-id="aa685-120">Чтобы быстрее приступить к работе, используйте эти команды во всей среде Windows Mixed Reality.</span><span class="sxs-lookup"><span data-stu-id="aa685-120">Use these commands throughout Windows Mixed Reality to get around faster.</span></span> <span data-ttu-id="aa685-121">В некоторых командах используется курсор взгляда, который можно открыть, сказав "select" (выбрать).</span><span class="sxs-lookup"><span data-stu-id="aa685-121">Some commands use the gaze cursor, which you bring up by saying "select."</span></span>

> [!NOTE]
> <span data-ttu-id="aa685-122">Лучи рук не поддерживаются в HoloLens (1-е поколение).</span><span class="sxs-lookup"><span data-stu-id="aa685-122">Hand rays are not supported on HoloLens (1st Gen).</span></span>

| <span data-ttu-id="aa685-123">Команда</span><span class="sxs-lookup"><span data-stu-id="aa685-123">Say this</span></span> | <span data-ttu-id="aa685-124">Действие</span><span class="sxs-lookup"><span data-stu-id="aa685-124">To do this</span></span> |
| - | - |
| <span data-ttu-id="aa685-125">"Select"</span><span class="sxs-lookup"><span data-stu-id="aa685-125">"Select"</span></span> | <span data-ttu-id="aa685-126">Произнесите "select" (выбрать) для отображения курсора взгляда.</span><span class="sxs-lookup"><span data-stu-id="aa685-126">Say "select" to bring up the gaze cursor.</span></span> <span data-ttu-id="aa685-127">Затем поверните голову так, чтобы курсор указывал на элемент, который требуется выбрать, и снова произнесите "select".</span><span class="sxs-lookup"><span data-stu-id="aa685-127">Then, turn your head to position the cursor on the thing you want to select, and say "select" again.</span></span> |
|<span data-ttu-id="aa685-128">Open the Start menu</span><span class="sxs-lookup"><span data-stu-id="aa685-128">Open the Start menu</span></span> | <span data-ttu-id="aa685-129">"Go to Start" ("Перейди в меню "Пуск"").</span><span class="sxs-lookup"><span data-stu-id="aa685-129">"Go to Start"</span></span> |
|<span data-ttu-id="aa685-130">Close the Start menu</span><span class="sxs-lookup"><span data-stu-id="aa685-130">Close the Start menu</span></span> | <span data-ttu-id="aa685-131">"Close" (Закрыть)</span><span class="sxs-lookup"><span data-stu-id="aa685-131">"Close"</span></span> |
|<span data-ttu-id="aa685-132">Leave an immersive app</span><span class="sxs-lookup"><span data-stu-id="aa685-132">Leave an immersive app</span></span> | <span data-ttu-id="aa685-133">Скажите "Go to Start" (Перейди в меню "Пуск"), чтобы открыть меню быстрых действий, а затем скажите "Mixed reality home" (Домашняя смешанная реальность).</span><span class="sxs-lookup"><span data-stu-id="aa685-133">Say "Go to Start" to bring up the quick actions menu, then say "Mixed reality home."</span></span> |
|<span data-ttu-id="aa685-134">Hide and show hand ray</span><span class="sxs-lookup"><span data-stu-id="aa685-134">Hide and show hand ray</span></span> | <span data-ttu-id="aa685-135">"Hide hand ray" (Скрыть лучи рук)/"Show hand ray" (Показать лучи рук)</span><span class="sxs-lookup"><span data-stu-id="aa685-135">"Hide hand ray" / "Show hand ray"</span></span> |
|<span data-ttu-id="aa685-136">See available speech commands</span><span class="sxs-lookup"><span data-stu-id="aa685-136">See available speech commands</span></span> | <span data-ttu-id="aa685-137">"What can I say?" (Что можно говорить?)</span><span class="sxs-lookup"><span data-stu-id="aa685-137">"What can I say?"</span></span> |

<span data-ttu-id="aa685-138">Начиная с версии19041.x в HoloLens2 можно использовать следующие команды.</span><span class="sxs-lookup"><span data-stu-id="aa685-138">Starting with version 19041.x of HoloLens 2, you can also use these commands:</span></span>

| <span data-ttu-id="aa685-139">Команда</span><span class="sxs-lookup"><span data-stu-id="aa685-139">Say this</span></span> | <span data-ttu-id="aa685-140">Действие</span><span class="sxs-lookup"><span data-stu-id="aa685-140">To do this</span></span> |
| - | - |
| <span data-ttu-id="aa685-141">"Restart device"</span><span class="sxs-lookup"><span data-stu-id="aa685-141">"Restart device"</span></span> | <span data-ttu-id="aa685-142">Отображение диалогового окна для подтверждения перезапуска устройства.</span><span class="sxs-lookup"><span data-stu-id="aa685-142">Bring up a dialogue to confirm you want to restart the device.</span></span> <span data-ttu-id="aa685-143">Скажите "yes" (да), чтобы перезапустить.</span><span class="sxs-lookup"><span data-stu-id="aa685-143">You can say "yes" to restart.</span></span> |
| <span data-ttu-id="aa685-144">"Shutdown device"</span><span class="sxs-lookup"><span data-stu-id="aa685-144">"Shutdown device"</span></span> | <span data-ttu-id="aa685-145">Отображение диалогового окна для подтверждения выключения устройства.</span><span class="sxs-lookup"><span data-stu-id="aa685-145">Bring up a dialogue to confirm you want to turn off the device.</span></span> <span data-ttu-id="aa685-146">Скажите "yes" (да), чтобы подтвердить.</span><span class="sxs-lookup"><span data-stu-id="aa685-146">You can say "yes" to confirm.</span></span> |
| <span data-ttu-id="aa685-147">"Brightness up/down"</span><span class="sxs-lookup"><span data-stu-id="aa685-147">"Brightness up/down"</span></span> | <span data-ttu-id="aa685-148">Увеличение или уменьшение яркости дисплея на 10%.</span><span class="sxs-lookup"><span data-stu-id="aa685-148">Increase or decrease the display brightness by 10%.</span></span> |
| <span data-ttu-id="aa685-149">"Volume up/down"</span><span class="sxs-lookup"><span data-stu-id="aa685-149">"Volume up/down"</span></span> | <span data-ttu-id="aa685-150">Увеличение или уменьшение громкости на 10%.</span><span class="sxs-lookup"><span data-stu-id="aa685-150">Increase or decrease the volume by 10%.</span></span> |
| <span data-ttu-id="aa685-151">"What's my IP address"</span><span class="sxs-lookup"><span data-stu-id="aa685-151">"What's my IP address"</span></span> | <span data-ttu-id="aa685-152">Отображение диалогового окна, в котором указан текущий IP-адрес вашего устройства в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="aa685-152">Bring up a dialogue displaying your device's current IP address on the local network.</span></span> |
| <span data-ttu-id="aa685-153">"Take a picture"</span><span class="sxs-lookup"><span data-stu-id="aa685-153">"Take a picture"</span></span> | <span data-ttu-id="aa685-154">Захват изображения, которое вы наблюдаете в смешанной реальности в данный момент.</span><span class="sxs-lookup"><span data-stu-id="aa685-154">Capture a mixed reality photo of what you are currently seeing.</span></span> |
| <span data-ttu-id="aa685-155">"Take a video"</span><span class="sxs-lookup"><span data-stu-id="aa685-155">"Take a video"</span></span> | <span data-ttu-id="aa685-156">Начало записи видео в смешанной реальности.</span><span class="sxs-lookup"><span data-stu-id="aa685-156">Start recording a mixed reality video.</span></span> | 
| <span data-ttu-id="aa685-157">"Stop recording"</span><span class="sxs-lookup"><span data-stu-id="aa685-157">"Stop recording"</span></span> | <span data-ttu-id="aa685-158">Завершение начатой записи видео в смешанной реальности.</span><span class="sxs-lookup"><span data-stu-id="aa685-158">Stops the current mixed reality video recording if one is in progress.</span></span> |

### <span data-ttu-id="aa685-159">Команды с голограммами</span><span class="sxs-lookup"><span data-stu-id="aa685-159">Hologram commands</span></span>

<span data-ttu-id="aa685-160">Чтобы использовать эти команды, посмотрите на трехмерный объект, голограмму или окно приложения.</span><span class="sxs-lookup"><span data-stu-id="aa685-160">To use these commands, gaze at a 3D object, hologram, or app window.</span></span>

| <span data-ttu-id="aa685-161">Команда</span><span class="sxs-lookup"><span data-stu-id="aa685-161">Say this</span></span> | <span data-ttu-id="aa685-162">Задача</span><span class="sxs-lookup"><span data-stu-id="aa685-162">To do this</span></span> |
| - | - |
| <span data-ttu-id="aa685-163">"Bigger"</span><span class="sxs-lookup"><span data-stu-id="aa685-163">"Bigger"</span></span> | <span data-ttu-id="aa685-164">Увеличить</span><span class="sxs-lookup"><span data-stu-id="aa685-164">Make it bigger</span></span> |
| <span data-ttu-id="aa685-165">"Smaller"</span><span class="sxs-lookup"><span data-stu-id="aa685-165">"Smaller"</span></span> | <span data-ttu-id="aa685-166">Уменьшить</span><span class="sxs-lookup"><span data-stu-id="aa685-166">Make it smaller</span></span> |
| <span data-ttu-id="aa685-167">"Face me"</span><span class="sxs-lookup"><span data-stu-id="aa685-167">"Face me"</span></span> | <span data-ttu-id="aa685-168">Повернуть лицом к вам</span><span class="sxs-lookup"><span data-stu-id="aa685-168">Turn it to face you</span></span> |
| <span data-ttu-id="aa685-169">"Move this"</span><span class="sxs-lookup"><span data-stu-id="aa685-169">"Move this"</span></span> | <span data-ttu-id="aa685-170">Переместить (по взгляду)</span><span class="sxs-lookup"><span data-stu-id="aa685-170">Move it (follow your gaze)</span></span> |
| <span data-ttu-id="aa685-171">"Close"</span><span class="sxs-lookup"><span data-stu-id="aa685-171">"Close"</span></span> | <span data-ttu-id="aa685-172">Закрыть</span><span class="sxs-lookup"><span data-stu-id="aa685-172">Close it</span></span> |
| <span data-ttu-id="aa685-173">"Follow me" / "Stop following"</span><span class="sxs-lookup"><span data-stu-id="aa685-173">"Follow me" / "Stop following"</span></span> | <span data-ttu-id="aa685-174">Объект следует за вами, когда вы перемещаетесь</span><span class="sxs-lookup"><span data-stu-id="aa685-174">Make it follow you as you move around</span></span> |

### <span data-ttu-id="aa685-175">Увидеть и сказать</span><span class="sxs-lookup"><span data-stu-id="aa685-175">See it, say it</span></span>

<span data-ttu-id="aa685-176">Многие кнопки и другие элементы в HoloLens также реагируют на ваш голос, например **Follow me** (Следовать за мной) и **Close** (Закрыть) на панели приложения или кнопка **Назад** в Edge.</span><span class="sxs-lookup"><span data-stu-id="aa685-176">Many buttons and other elements on HoloLens also respond to your voice—for example, **Follow me** and **Close** on the app bar, or the **Back** button in Edge.</span></span> <span data-ttu-id="aa685-177">Чтобы узнать, включена ли кнопка с голосовой командой, наведите **курсор на взгляд**, **коснитесь курсора** или на одну **руку** на мгновение.</span><span class="sxs-lookup"><span data-stu-id="aa685-177">To find out if a button is voice-enabled, rest your **gaze cursor**,**touch cursor** or one **hand ray** on it for a moment.</span></span> <span data-ttu-id="aa685-178">Если кнопка включена голосом, вы увидите голосовой совет.</span><span class="sxs-lookup"><span data-stu-id="aa685-178">If the button is voice-enabled, you'll see a voice tip.</span></span>

### <span data-ttu-id="aa685-179">Режим диктовки</span><span class="sxs-lookup"><span data-stu-id="aa685-179">Dictation mode</span></span>

<span data-ttu-id="aa685-180">Устали вводить текст?</span><span class="sxs-lookup"><span data-stu-id="aa685-180">Tired of typing?</span></span> <span data-ttu-id="aa685-181">Перейдите в режим диктовки в любое время, чтобы активировать голографическую клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="aa685-181">Switch to dictation mode any time that the holographic keyboard is active.</span></span> <span data-ttu-id="aa685-182">Чтобы начать работу, нажмите кнопку микрофона или скажите "Start dictating" (Начать диктовку).</span><span class="sxs-lookup"><span data-stu-id="aa685-182">To get started, select the microphone button or say "Start dictating."</span></span> <span data-ttu-id="aa685-183">Чтобы прекратить диктовку, нажмите эту кнопку снова или скажите "Stop dictating" (Прекратить диктовку).</span><span class="sxs-lookup"><span data-stu-id="aa685-183">To stop dictating, select the button again or say "Stop dictating."</span></span> <span data-ttu-id="aa685-184">Чтобы удалить только что продиктованное слово, скажите "Delete that" (Удалить это).</span><span class="sxs-lookup"><span data-stu-id="aa685-184">To delete what you just dictated, say "Delete that."</span></span> 

> [!NOTE]
> <span data-ttu-id="aa685-185">Для использования режима диктовки требуется подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="aa685-185">To use dictation mode, you have to have an internet connection.</span></span>

<span data-ttu-id="aa685-186">Функция диктовки HoloLens использует явные знаки препинания, то есть вам необходимо говорить знак препинания, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="aa685-186">HoloLens dictation uses explicit punctuation, meaning that you say the name of the punctuation you want to use.</span></span> <span data-ttu-id="aa685-187">Например, вы можете сказать "Привет, **запятая** , как дела **вопросительный знак**".</span><span class="sxs-lookup"><span data-stu-id="aa685-187">For instance, you might say "Hey **comma** what are you up to **question mark**."</span></span>

<span data-ttu-id="aa685-188">Ниже перечислены ключевые слова знаков пунктуации, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="aa685-188">Here are the punctuation keywords that you can use:</span></span>

- <span data-ttu-id="aa685-189">Точка, запятая, вопрос, восклицательный знак</span><span class="sxs-lookup"><span data-stu-id="aa685-189">Period, comma, question mark, exclamation point/exclamation mark</span></span>
- <span data-ttu-id="aa685-190">Новая строка/новый абзац</span><span class="sxs-lookup"><span data-stu-id="aa685-190">New line/new paragraph</span></span>
- <span data-ttu-id="aa685-191">Точка с запятой, двоеточие</span><span class="sxs-lookup"><span data-stu-id="aa685-191">Semicolon, colon</span></span>
- <span data-ttu-id="aa685-192">Открыть кавычки, закрыть кавычки</span><span class="sxs-lookup"><span data-stu-id="aa685-192">Open quote(s), close quote(s)</span></span>
- <span data-ttu-id="aa685-193">Хэштег, смайлик, хмурый смайлик, подмигивающий смайлик</span><span class="sxs-lookup"><span data-stu-id="aa685-193">Hashtag, smiley/smiley face, frowny, winky</span></span>
- <span data-ttu-id="aa685-194">Доллар, процент</span><span class="sxs-lookup"><span data-stu-id="aa685-194">Dollar, percent</span></span>

<span data-ttu-id="aa685-195">Иногда бывает полезно говорить такие элементы, как адреса электронной почты, по буквам.</span><span class="sxs-lookup"><span data-stu-id="aa685-195">Sometimes it's helpful to spell out things like email addresses.</span></span> <span data-ttu-id="aa685-196">Например, чтобы продиктовать example@outlook.com, вы можете сказать "E X A M P L E собака outlook точка com".</span><span class="sxs-lookup"><span data-stu-id="aa685-196">For instance, to dictate example@outlook.com, you'd say "E X A M P L E at outlook dot com."</span></span>

## <span data-ttu-id="aa685-197">Делайте больше с помощью Кортаны</span><span class="sxs-lookup"><span data-stu-id="aa685-197">Do more with Cortana</span></span>

<span data-ttu-id="aa685-198">С помощью Кортаны в HoloLens можно делать много всего интересного, но в зависимости от используемой версии Windows Holographic доступные возможности могут отличаться.</span><span class="sxs-lookup"><span data-stu-id="aa685-198">Cortana can help you do all kinds of things on your HoloLens, but depending on which version of Windows Holographic you're using, the capablities may be different.</span></span> <span data-ttu-id="aa685-199">Подробные сведения о новых возможностях последней версии Кортаны приведены [здесь](https://blogs.windows.com/windowsexperience/2020/02/28/cortana-in-the-upcoming-windows-10-release-focused-on-your-productivity-with-enhanced-security-and-privacy/).</span><span class="sxs-lookup"><span data-stu-id="aa685-199">You can learn more about the updated capabilites of the latest version of Cortana [here](https://blogs.windows.com/windowsexperience/2020/02/28/cortana-in-the-upcoming-windows-10-release-focused-on-your-productivity-with-enhanced-security-and-privacy/).</span></span> 

![Привет, Кортана!](images/cortana-on-hololens.png)

<span data-ttu-id="aa685-201">Вот несколько фраз, которые вы можете сказать (сначала скажите "Привет, Кортана!").</span><span class="sxs-lookup"><span data-stu-id="aa685-201">Here are some things you can try saying (remember to say "Hey Cortana" first).</span></span>

<span data-ttu-id="aa685-202">**Hey, Cortana**...</span><span class="sxs-lookup"><span data-stu-id="aa685-202">**Hey, Cortana**...</span></span>

- <span data-ttu-id="aa685-203">What can I say?</span><span class="sxs-lookup"><span data-stu-id="aa685-203">What can I say?</span></span>
- <span data-ttu-id="aa685-204">Launch <*имя приложения*>.</span><span class="sxs-lookup"><span data-stu-id="aa685-204">Launch <*app name*>.</span></span>
- <span data-ttu-id="aa685-205">What time is it?</span><span class="sxs-lookup"><span data-stu-id="aa685-205">What time is it?</span></span>
- <span data-ttu-id="aa685-206">Show me the latest NBA scores.</span><span class="sxs-lookup"><span data-stu-id="aa685-206">Show me the latest NBA scores.</span></span>
- <span data-ttu-id="aa685-207">Tell me a joke.</span><span class="sxs-lookup"><span data-stu-id="aa685-207">Tell me a joke.</span></span>

<span data-ttu-id="aa685-208">В *версии 18362.x и более ранних* можно также использовать следующие команды.</span><span class="sxs-lookup"><span data-stu-id="aa685-208">If you're using *version 18362.x or earlier*, you can also use these commands:</span></span>

<span data-ttu-id="aa685-209">**Hey, Cortana**...</span><span class="sxs-lookup"><span data-stu-id="aa685-209">**Hey, Cortana**...</span></span>

- <span data-ttu-id="aa685-210">Increase the volume.</span><span class="sxs-lookup"><span data-stu-id="aa685-210">Increase the volume.</span></span>
- <span data-ttu-id="aa685-211">Decrease the brightness.</span><span class="sxs-lookup"><span data-stu-id="aa685-211">Decrease the brightness.</span></span>
- <span data-ttu-id="aa685-212">Shut down.</span><span class="sxs-lookup"><span data-stu-id="aa685-212">Shut down.</span></span>
- <span data-ttu-id="aa685-213">Restart.</span><span class="sxs-lookup"><span data-stu-id="aa685-213">Restart.</span></span>
- <span data-ttu-id="aa685-214">Go to sleep.</span><span class="sxs-lookup"><span data-stu-id="aa685-214">Go to sleep.</span></span>
- <span data-ttu-id="aa685-215">Mute.</span><span class="sxs-lookup"><span data-stu-id="aa685-215">Mute.</span></span>
- <span data-ttu-id="aa685-216">Move <*имя приложения*> here (взгляните на место, куда вы хотите переместить приложение).</span><span class="sxs-lookup"><span data-stu-id="aa685-216">Move <*app name*> here (gaze at the spot that you want the app to move to).</span></span>
- <span data-ttu-id="aa685-217">Go to Start.</span><span class="sxs-lookup"><span data-stu-id="aa685-217">Go to Start.</span></span>
- <span data-ttu-id="aa685-218">Take a picture.</span><span class="sxs-lookup"><span data-stu-id="aa685-218">Take a picture.</span></span>
- <span data-ttu-id="aa685-219">Start recording.</span><span class="sxs-lookup"><span data-stu-id="aa685-219">Start recording.</span></span> <span data-ttu-id="aa685-220">(Начинает запись видео.)</span><span class="sxs-lookup"><span data-stu-id="aa685-220">(Starts recording a video.)</span></span>
- <span data-ttu-id="aa685-221">Stop recording.</span><span class="sxs-lookup"><span data-stu-id="aa685-221">Stop recording.</span></span> <span data-ttu-id="aa685-222">(Остановка записи видео.)</span><span class="sxs-lookup"><span data-stu-id="aa685-222">(Stops recording a video.)</span></span>
- <span data-ttu-id="aa685-223">How much battery do I have left?</span><span class="sxs-lookup"><span data-stu-id="aa685-223">How much battery do I have left?</span></span>

<span data-ttu-id="aa685-224">Некоторые функции Кортаны, которые вы используете в Windows на компьютере или телефоне (например, напоминания и уведомления), не поддерживаются в Microsoft HoloLens, а возможности Кортаны зависят от региона.</span><span class="sxs-lookup"><span data-stu-id="aa685-224">Some Cortana features that you're used to from Windows on your PC or phone (for example, reminders and notifications) aren't supported in Microsoft HoloLens, and the Cortana experience may vary from one region to another.</span></span>

### <span data-ttu-id="aa685-225">Отключение Кортаны</span><span class="sxs-lookup"><span data-stu-id="aa685-225">Turn Cortana off</span></span>

<span data-ttu-id="aa685-226">Кортана включается при первом использовании HoloLens при активации голосовых функций.</span><span class="sxs-lookup"><span data-stu-id="aa685-226">Cortana is on the first time you use HoloLens when you enable speech.</span></span> <span data-ttu-id="aa685-227">Кортану можно отключить в разделе параметров Кортаны.</span><span class="sxs-lookup"><span data-stu-id="aa685-227">You can turn her off in Cortana's settings.</span></span> <span data-ttu-id="aa685-228">В списке **Все приложения** выберите **Кортана** > **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="aa685-228">In the **All apps** list, select **Cortana** > **Settings**.</span></span> <span data-ttu-id="aa685-229">Затем отключите параметры Кортаны, чтобы перестать получать рекомендации, идеи, напоминания, оповещения и многое другое.</span><span class="sxs-lookup"><span data-stu-id="aa685-229">Then turn off Cortana can give you suggestions, ideas, reminders, alerts, and more.</span></span>

<span data-ttu-id="aa685-230">Если Кортана не отвечает на фразу "Привет, Кортана!", убедитесь, что голосовые функции включены в меню "Пуск", и перейдите в параметры Кортаны, чтобы убедиться, что она включена.</span><span class="sxs-lookup"><span data-stu-id="aa685-230">If Cortana isn't responding to "Hey Cortana," check that speech is enabled on Start and go to Cortana's settings and check to make sure she's on.</span></span>
