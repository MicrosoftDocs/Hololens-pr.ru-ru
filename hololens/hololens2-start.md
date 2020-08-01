---
title: Настройка HoloLens 2
description: В этом руководстве описывается первая настройка устройства.  Вам потребуется сеть Wi-Fi, а также учетная запись Майкрософт (MSA) или Azure Active Directory (AAD).
ms.assetid: 507305f4-e85a-47c5-a055-a3400ae8a10e
ms.date: 9/17/2019
keywords: hololens
ms.prod: hololens
ms.sitesec: library
author: scooley
ms.author: scooley
ms.topic: article
ms.localizationpriority: high
appliesto:
- HoloLens 2
ms.openlocfilehash: a0ba32e3caff7695cd284ee3752bb91d80da2194
ms.sourcegitcommit: 7edbb99e0972d3d857e5e87c062c3c64cacc1f41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2020
ms.locfileid: "10903245"
---
# <span data-ttu-id="5acb8-105">Настройка HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="5acb8-105">Set up your HoloLens 2</span></span>

<span data-ttu-id="5acb8-106">При первом включении HoloLens вам будет предложено настроить устройство, выполнить вход с помощью своей учетной записи пользователя и провести калибровку устройства.</span><span class="sxs-lookup"><span data-stu-id="5acb8-106">The first time you turn on your HoloLens, you'll be guided through setting up your device, signing in with a user account, and calibrating the HoloLens to your eyes.</span></span>  <span data-ttu-id="5acb8-107">В этом разделе описан процесс начальной настройки HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="5acb8-107">This section walks through the HoloLens 2 initial setup experience.</span></span>

<span data-ttu-id="5acb8-108">В следующем разделе вы узнаете о том, как работать с HoloLens и взаимодействовать с голограммами.</span><span class="sxs-lookup"><span data-stu-id="5acb8-108">In the next section, you'll learn how to work with HoloLens and interact with holograms.</span></span> <span data-ttu-id="5acb8-109">Чтобы перейти к следующей статье, см. раздел [Начало работы с HoloLens 2](hololens2-basic-usage.md).</span><span class="sxs-lookup"><span data-stu-id="5acb8-109">To skip ahead to that article, see [Get started with HoloLens 2](hololens2-basic-usage.md).</span></span>

## <span data-ttu-id="5acb8-110">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="5acb8-110">Before you start</span></span>

<span data-ttu-id="5acb8-111">Прежде чем начать, убедитесь, что у вас есть следующее:</span><span class="sxs-lookup"><span data-stu-id="5acb8-111">Before you get started, make sure you have the following available:</span></span>

<span data-ttu-id="5acb8-112">**Сетевое подключение**.</span><span class="sxs-lookup"><span data-stu-id="5acb8-112">**A network connection**.</span></span> <span data-ttu-id="5acb8-113">Вам будет необходимо подключить HoloLens к сети Wi-Fi для настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="5acb8-113">You'll need to connect your HoloLens to a network to set it up.</span></span> <span data-ttu-id="5acb8-114">C помощью HoloLens 2 можно подключаться к сети через Wi-Fi или Ethernet (для этого необходим переходник с USB-C на Ethernet).</span><span class="sxs-lookup"><span data-stu-id="5acb8-114">With HoloLens 2, you can connect with Wi-Fi or by using ethernet (you'll need a USB-C-to-Ethernet adapter).</span></span> <span data-ttu-id="5acb8-115">При первом подключении вам потребуется открыть защищенную паролем сеть без перехода на веб-сайт или использования сертификатов для подключения.</span><span class="sxs-lookup"><span data-stu-id="5acb8-115">The first time you connect, you'll need an open or password-protected network that doesn't require navigating to a website or using certificates to connect.</span></span> <span data-ttu-id="5acb8-116">[Дополнительные сведения о веб-сайтах, которые используются HoloLens](hololens-offline.md).</span><span class="sxs-lookup"><span data-stu-id="5acb8-116">[Learn more about the websites that HoloLens uses](hololens-offline.md).</span></span>

<span data-ttu-id="5acb8-117">**Учетная запись Майкрософт**.</span><span class="sxs-lookup"><span data-stu-id="5acb8-117">**A Microsoft account**.</span></span> <span data-ttu-id="5acb8-118">Вам также потребуется выполнить вход в систему HoloLens с учетной записью Майкрософт (или с рабочей учетной записью, если устройство принадлежит организации).</span><span class="sxs-lookup"><span data-stu-id="5acb8-118">You'll also need to sign in to HoloLens with a Microsoft account (or with your work account, if your organization owns the device).</span></span> <span data-ttu-id="5acb8-119">Если у вас еще нет учетной записи Майкрософт, перейдите на веб-сайт [account.microsoft.com](https://account.microsoft.com) и создайте ее бесплатно.</span><span class="sxs-lookup"><span data-stu-id="5acb8-119">If you don't have a Microsoft account, go to [account.microsoft.com](https://account.microsoft.com) and set one up for free.</span></span>

<span data-ttu-id="5acb8-120">**Безопасное, хорошо освещенное пространство, где нельзя споткнуться**.</span><span class="sxs-lookup"><span data-stu-id="5acb8-120">**A safe, well-lit space with no tripping hazards**.</span></span> <span data-ttu-id="5acb8-121">[Инструкции по охране здоровья и технике безопасности](https://go.microsoft.com/fwlink/p/?LinkId=746661)</span><span class="sxs-lookup"><span data-stu-id="5acb8-121">[Health and safety info](https://go.microsoft.com/fwlink/p/?LinkId=746661).</span></span>

<span data-ttu-id="5acb8-122">**Дополнительные принадлежности**, входящие в комплект HoloLens, которые помогут вам отрегулировать размер.</span><span class="sxs-lookup"><span data-stu-id="5acb8-122">**The optional comfort accessories** that came with your HoloLens, to help you get the most comfortable fit.</span></span> <span data-ttu-id="5acb8-123">[Дополнительные сведения о регулировке размера и удобстве использования устройства](hololens2-setup.md#adjust-fit).</span><span class="sxs-lookup"><span data-stu-id="5acb8-123">[More on fit and comfort](hololens2-setup.md#adjust-fit).</span></span>

## <span data-ttu-id="5acb8-124">Настройка Windows</span><span class="sxs-lookup"><span data-stu-id="5acb8-124">Set up Windows</span></span>

<span data-ttu-id="5acb8-125">Во время первого запуска HoloLens 2 ваша первая задача — настроить Windows Holographic.</span><span class="sxs-lookup"><span data-stu-id="5acb8-125">The first time you start your HoloLens 2, your first task is to set up Windows Holographic.</span></span>  <span data-ttu-id="5acb8-126">При запуске HoloLens вы услышите музыку и увидите логотип Windows.</span><span class="sxs-lookup"><span data-stu-id="5acb8-126">When you start your HoloLens, you will hear music and see a Windows logo.</span></span>

![Первый экран при первой загрузке](images/01-magic-moment.png)

<span data-ttu-id="5acb8-128">HoloLens 2 предоставит пошаговые инструкции по выполнению следующих действий.</span><span class="sxs-lookup"><span data-stu-id="5acb8-128">HoloLens 2 will walk you through the following steps:</span></span>

1. <span data-ttu-id="5acb8-129">Выберите язык.</span><span class="sxs-lookup"><span data-stu-id="5acb8-129">Select your language.</span></span>
    ![Выбор языка](images/04-language.png)

1. <span data-ttu-id="5acb8-131">Выберите регион.</span><span class="sxs-lookup"><span data-stu-id="5acb8-131">Select your region.</span></span>
    ![Выбор региона](images/05-region.png)

1. <span data-ttu-id="5acb8-133">Выполните калибровку HoloLens для ваших глаз.</span><span class="sxs-lookup"><span data-stu-id="5acb8-133">Calibrate HoloLens to your eyes.</span></span>  <span data-ttu-id="5acb8-134">Если вы пропустите калибровку, запрос калибровки появится при следующем входе в систему.</span><span class="sxs-lookup"><span data-stu-id="5acb8-134">If you choose to skip calibration, you'll be prompted the next time you log in.</span></span>

    <span data-ttu-id="5acb8-135">Для калибровки вам потребуется посмотреть на набор целей (которые называются драгоценными камнями).</span><span class="sxs-lookup"><span data-stu-id="5acb8-135">To calibrate, you'll look at a set of targets (referred to as gems).</span></span> <span data-ttu-id="5acb8-136">Во время калибровки можно моргать и закрывать глаза, но нельзя смотреть на другие объекты в комнате или пространстве.</span><span class="sxs-lookup"><span data-stu-id="5acb8-136">It's fine if you blink or close your eyes during calibration, but try not to stare at other objects in the room or physical space.</span></span> <span data-ttu-id="5acb8-137">HoloLens использует этот процесс, чтобы узнать о положении ваших глаз для оптимального отображения голографического мира.</span><span class="sxs-lookup"><span data-stu-id="5acb8-137">HoloLens uses this process to learn about your eye position so that it can better render your holographic world.</span></span> <span data-ttu-id="5acb8-138">После калибровки голограммы будут отображаться правильно даже при смещении визора на вашей голове.</span><span class="sxs-lookup"><span data-stu-id="5acb8-138">After calibration, holograms will appear correctly even as the visor shifts on your head.</span></span>

    <span data-ttu-id="5acb8-139">Сведения о калибровке хранятся локально на устройстве и не связываются с какими-либо сведениями учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5acb8-139">Calibration information is stored locally on the device and is not associated with any account information.</span></span> <span data-ttu-id="5acb8-140">Подробнее см. в разделе [Данные калибровки и безопасность](hololens-calibration.md#calibration-data-and-security).</span><span class="sxs-lookup"><span data-stu-id="5acb8-140">For more information, see [Calibration data and security](hololens-calibration.md#calibration-data-and-security).</span></span>

    ![Экран выбора калибровки](images/06-et-corners.png)

1. <span data-ttu-id="5acb8-142">Подключитесь к Интернету (выберите Wi-Fi или подключение Ethernet).</span><span class="sxs-lookup"><span data-stu-id="5acb8-142">Connect to the internet (select Wi-Fi or your ethernet connection).</span></span>
     <span data-ttu-id="5acb8-143">HoloLens задает часовой пояс автоматически на основании информации, полученной из сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="5acb8-143">HoloLens sets your time zone automatically based on information obtained from the Wi-Fi network.</span></span> <span data-ttu-id="5acb8-144">После завершения настройки можно изменить часовой пояс с помощью приложения "Параметры".</span><span class="sxs-lookup"><span data-stu-id="5acb8-144">After setup finishes, you can change the time zone by using the Settings app.</span></span>

    ![Подключитесь к сети Wi-Fi](images/11-network.png)
> [!NOTE] 
> <span data-ttu-id="5acb8-146">Если вы подключились к Wi-Fi и затем захотели переключиться на другую сеть, находясь в процессу установки, можно одновременно нажать кнопки **уменьшения громкости** и **питания**, чтобы вернуться к этому шагу, если вы используете версию ОС, выпущенную в октябре 2019 г., или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="5acb8-146">If you progress past the Wi-Fi step and later need to switch to a different network while still in setup, you can press the **Volume Down** and **Power** buttons simultaneously to return to this step if you are running an OS version from October 2019 or later.</span></span> <span data-ttu-id="5acb8-147">В более ранних версиях может потребоваться [сбросить устройство](hololens-recovery.md) или перезапустить его там, где сеть Wi-Fi недоступна, чтобы предотвратить автоматическое подключение.</span><span class="sxs-lookup"><span data-stu-id="5acb8-147">For earlier versions, you may need to [reset the device](hololens-recovery.md) or restart it in a location where the Wi-Fi network is not available to prevent it from automatically connecting.</span></span>
> 
> <span data-ttu-id="5acb8-148">Также обратите внимание, что во время настройки HoloLens период ожидания учетных данных составляет две минуты.</span><span class="sxs-lookup"><span data-stu-id="5acb8-148">Also note that during HoloLens Setup, there is a credential timeout of two minutes.</span></span> <span data-ttu-id="5acb8-149">Имя пользователя и пароль необходимо ввести в течение двух минут, в противном случае поле имени пользователя будет автоматически очищено.</span><span class="sxs-lookup"><span data-stu-id="5acb8-149">The username/password needs to be entered within two minutes otherwise the username field will be automatically cleared.</span></span>

1. <span data-ttu-id="5acb8-150">Войдите в свою учетную запись.</span><span class="sxs-lookup"><span data-stu-id="5acb8-150">Sign in to your user account.</span></span> <span data-ttu-id="5acb8-151">Вам необходимо выбрать один из вариантов: **Моя компания или учебное заведение является владельцем** или **Я являюсь владельцем**.</span><span class="sxs-lookup"><span data-stu-id="5acb8-151">You'll choose between **My work or school owns it** and **I own it**.</span></span>
    - <span data-ttu-id="5acb8-152">При выборе варианта **Моя компания или учебное заведение является владельцем** необходимо выполнить вход с помощью учетной записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5acb8-152">When you choose **My work or school owns it**, you sign in with an Azure AD account.</span></span> <span data-ttu-id="5acb8-153">Если в вашей организации используется Azure AD Premium и настроена автоматическая регистрация в MDM, устройство HoloLens будет зарегистрировано в MDM автоматически.</span><span class="sxs-lookup"><span data-stu-id="5acb8-153">If your organization uses Azure AD Premium and has configured automatic MDM enrollment, HoloLens automatically enrolls in MDM.</span></span> <span data-ttu-id="5acb8-154">Если ваша организация не использует Azure AD Premium, автоматическая регистрация в MDM недоступна.</span><span class="sxs-lookup"><span data-stu-id="5acb8-154">If your organization does not use Azure AD Premium, automatic MDM enrollment isn't available.</span></span> <span data-ttu-id="5acb8-155">В этом случае необходимо [вручную зарегистрировать HoloLens в системе управления устройствами](hololens-enroll-mdm.md#different-ways-to-enroll).</span><span class="sxs-lookup"><span data-stu-id="5acb8-155">In that case, you need to [manually enroll HoloLens in device management](hololens-enroll-mdm.md#different-ways-to-enroll).</span></span>
        1. <span data-ttu-id="5acb8-156">Введите сведения об учетной записи организации.</span><span class="sxs-lookup"><span data-stu-id="5acb8-156">Enter your organizational account information.</span></span>
        1. <span data-ttu-id="5acb8-157">Примите заявление о конфиденциальности и лицензионное соглашение с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5acb8-157">Accept the privacy statement and the end user license agreement.</span></span>
        1. <span data-ttu-id="5acb8-158">Войдите, используя учетные данные Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5acb8-158">Sign in by using your Azure AD credentials.</span></span> <span data-ttu-id="5acb8-159">Это может перенаправить вас на страницу входа для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="5acb8-159">This may redirect to your organization's sign-in page.</span></span>
        1. <span data-ttu-id="5acb8-160">Продолжите настройку устройства.</span><span class="sxs-lookup"><span data-stu-id="5acb8-160">Continue setting up the device.</span></span>
    - <span data-ttu-id="5acb8-161">При выборе варианта **Я являюсь владельцем** выполните вход с помощью учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5acb8-161">When you choose **I own it**, you sign in with a Microsoft account.</span></span> <span data-ttu-id="5acb8-162">После завершения настройки можно [вручную зарегистрировать HoloLens в системе управления устройствами](hololens-enroll-mdm.md#different-ways-to-enroll).</span><span class="sxs-lookup"><span data-stu-id="5acb8-162">After setup is complete, you can [manually enroll HoloLens in device management](hololens-enroll-mdm.md#different-ways-to-enroll).</span></span>
        1. <span data-ttu-id="5acb8-163">Введите сведения об учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5acb8-163">Enter your Microsoft account information.</span></span>
        2. <span data-ttu-id="5acb8-164">Введите пароль.</span><span class="sxs-lookup"><span data-stu-id="5acb8-164">Enter your password.</span></span> <span data-ttu-id="5acb8-165">Если в вашей учетной записи Майкрософт требуется [двухшаговая проверка подлинности (2FA)](https://blogs.technet.microsoft.com/microsoft_blog/2013/04/17/microsoft-account-gets-more-secure/), завершите процесс проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5acb8-165">If your Microsoft account requires [two-step verification (2FA)](https://blogs.technet.microsoft.com/microsoft_blog/2013/04/17/microsoft-account-gets-more-secure/), complete the verification process.</span></span>

    ![Задайте пользователя](images/13-device-owner.png)

1. <span data-ttu-id="5acb8-167">Укажите, следует ли включить голосовые функции на HoloLens 2, а также следует ли отправлять телеметрические данные диагностики.</span><span class="sxs-lookup"><span data-stu-id="5acb8-167">Select whether to enable speech on HoloLens 2, and whether to send diagnostic telemetry.</span></span>
    ![Включите Кортану](images/22-do-more-with-voice.png)

1. <span data-ttu-id="5acb8-169">Выберите уровень телеметрии.</span><span class="sxs-lookup"><span data-stu-id="5acb8-169">Select your telemetry level.</span></span> <span data-ttu-id="5acb8-170">Если возможно, включите полную телеметрию.</span><span class="sxs-lookup"><span data-stu-id="5acb8-170">If you can, please enable Full telemetry.</span></span> <span data-ttu-id="5acb8-171">Эта информация действительно помогает команде разработчиков HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5acb8-171">This information really helps the HoloLens engineering team.</span></span>
     ![Уровень телеметрии](images/24-telemetry.png)

1. <span data-ttu-id="5acb8-173">Узнайте, как использовать жест "Пуск" на HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="5acb8-173">Learn how to use the start gesture on HoloLens 2.</span></span>
     ![Узнайте, как использовать жест "Пуск", изображение 1](images/26-01-startmenu-learning.png) ![Узнайте, как использовать жест "Пуск", изображение 2](images/26-02-startmenu-learning.png)

<span data-ttu-id="5acb8-175">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="5acb8-175">Congratulations!</span></span>  <span data-ttu-id="5acb8-176">Настройка завершена, и вы готовы к использованию HoloLens!</span><span class="sxs-lookup"><span data-stu-id="5acb8-176">Setup is complete and you're ready to use HoloLens!</span></span>

## <span data-ttu-id="5acb8-177">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="5acb8-177">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="5acb8-178">Начало работы с HoloLens2</span><span class="sxs-lookup"><span data-stu-id="5acb8-178">Get started with HoloLens 2</span></span>](hololens2-basic-usage.md)
