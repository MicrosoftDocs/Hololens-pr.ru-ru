---
title: Настройка HoloLens 2
description: Сведения о том, как выполнить первую настройку HoloLens 2 по сети Wi-Fi с помощью учетной записи Майкрософт (MSA) или Azure Active Directory (AAD).
ms.assetid: 507305f4-e85a-47c5-a055-a3400ae8a10e
ms.date: 6/09/2021
keywords: hololens
ms.prod: hololens
ms.sitesec: library
author: scooley
ms.author: scooley
ms.topic: article
ms.localizationpriority: high
appliesto:
- HoloLens 2
ms.openlocfilehash: 0d087037e94bcaed2cd79d9cff77ed3039919a09
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923917"
---
# <a name="set-up-your-hololens-2"></a><span data-ttu-id="ca144-104">Настройка HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="ca144-104">Set up your HoloLens 2</span></span>

<span data-ttu-id="ca144-105">При первом включении HoloLens вам будет предложено настроить устройство, выполнить вход с помощью своей учетной записи пользователя и провести калибровку устройства для отслеживания глаз.</span><span class="sxs-lookup"><span data-stu-id="ca144-105">The first time you turn on your HoloLens, you'll be guided through setting up your device, signing in with a user account, and calibrating the HoloLens to your eyes.</span></span>  <span data-ttu-id="ca144-106">В этом разделе описан процесс начальной настройки HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="ca144-106">This section walks through the HoloLens 2 initial setup experience.</span></span>

<span data-ttu-id="ca144-107">В следующем разделе вы узнаете о том, как работать с HoloLens и взаимодействовать с голограммами.</span><span class="sxs-lookup"><span data-stu-id="ca144-107">In the next section, you'll learn how to work with HoloLens and interact with holograms.</span></span> <span data-ttu-id="ca144-108">Вы можете сразу перейти к статье [Начало работы с HoloLens 2](hololens2-basic-usage.md).</span><span class="sxs-lookup"><span data-stu-id="ca144-108">To skip ahead to that article, see [Getting around HoloLens 2](hololens2-basic-usage.md).</span></span>

## <a name="before-you-start"></a><span data-ttu-id="ca144-109">Прежде чем начать</span><span class="sxs-lookup"><span data-stu-id="ca144-109">Before you start</span></span>

<span data-ttu-id="ca144-110">Прежде чем начать, проверьте соблюдение следующих условий:</span><span class="sxs-lookup"><span data-stu-id="ca144-110">Before you get started, make sure you have the following available:</span></span>

<span data-ttu-id="ca144-111">**Сетевое подключение.**</span><span class="sxs-lookup"><span data-stu-id="ca144-111">**A network connection**.</span></span> <span data-ttu-id="ca144-112">Вам потребуется подключить HoloLens к сети Wi-Fi для настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="ca144-112">You'll need to connect your HoloLens to a network to set it up.</span></span> <span data-ttu-id="ca144-113">HoloLens 2 можно подключать к сети через Wi-Fi или Ethernet (для этого необходим переходник с USB-C на Ethernet).</span><span class="sxs-lookup"><span data-stu-id="ca144-113">With HoloLens 2, you can connect with Wi-Fi or by using ethernet (you'll need a USB-C-to-Ethernet adapter).</span></span> <span data-ttu-id="ca144-114">При первом подключении вам нужно указать открытую или защищенную паролем сеть, для подключения к которой не требуется вход на веб-сайт или сертификат безопасности.</span><span class="sxs-lookup"><span data-stu-id="ca144-114">The first time you connect, you'll need an open or password-protected network that doesn't require navigating to a website or using certificates to connect.</span></span> <span data-ttu-id="ca144-115">[Дополнительные сведения о веб-сайтах, которые использует HoloLens.](hololens-offline.md)</span><span class="sxs-lookup"><span data-stu-id="ca144-115">[Learn more about the websites that HoloLens uses](hololens-offline.md).</span></span>

<span data-ttu-id="ca144-116">**Учетная запись Майкрософт.**</span><span class="sxs-lookup"><span data-stu-id="ca144-116">**A Microsoft account**.</span></span> <span data-ttu-id="ca144-117">Вам также потребуется выполнить вход в систему HoloLens с учетной записью Майкрософт (или с рабочей учетной записью, если устройство принадлежит организации).</span><span class="sxs-lookup"><span data-stu-id="ca144-117">You'll also need to sign in to HoloLens with a Microsoft account (or with your work account, if your organization owns the device).</span></span> <span data-ttu-id="ca144-118">Если у вас нет учетной записи Майкрософт, откройте страницу [account.microsoft.com](https://account.microsoft.com) и настройте ее бесплатно.</span><span class="sxs-lookup"><span data-stu-id="ca144-118">If you don't have a Microsoft account, go to [account.microsoft.com](https://account.microsoft.com) and set one up for free.</span></span>

<span data-ttu-id="ca144-119">**Надежное, хорошо освещенное пространство без помех, об которые можно споткнуться.**</span><span class="sxs-lookup"><span data-stu-id="ca144-119">**A safe, well-lit space with no tripping hazards**.</span></span> <span data-ttu-id="ca144-120">[Сведения о работоспособности и безопасности.](https://go.microsoft.com/fwlink/p/?LinkId=746661)</span><span class="sxs-lookup"><span data-stu-id="ca144-120">[Health and safety info](https://go.microsoft.com/fwlink/p/?LinkId=746661).</span></span>

<span data-ttu-id="ca144-121">**Необязательные аксессуары для повышения комфорта** использования HoloLens, которые помогут вам носить устройство максимально удобно.</span><span class="sxs-lookup"><span data-stu-id="ca144-121">**The optional comfort accessories** that came with your HoloLens, to help you get the most comfortable fit.</span></span> <span data-ttu-id="ca144-122">[Дополнительные сведения о подгонке и комфорте.](hololens2-setup.md#adjust-fit)</span><span class="sxs-lookup"><span data-stu-id="ca144-122">[More on fit and comfort](hololens2-setup.md#adjust-fit).</span></span>

## <a name="set-up-windows"></a><span data-ttu-id="ca144-123">Настройка Windows</span><span class="sxs-lookup"><span data-stu-id="ca144-123">Set up Windows</span></span>

<span data-ttu-id="ca144-124">При первом включении HoloLens 2 самая первая задача — настроить Windows Holographic.</span><span class="sxs-lookup"><span data-stu-id="ca144-124">The first time you start your HoloLens 2, your first task is to set up Windows Holographic.</span></span>  <span data-ttu-id="ca144-125">При включении HoloLens вы услышите музыку и увидите логотип Windows.</span><span class="sxs-lookup"><span data-stu-id="ca144-125">When you start your HoloLens, you will hear music and see a Windows logo.</span></span>

![Первый экран при первой загрузке](images/01-magic-moment.png)

<span data-ttu-id="ca144-127">HoloLens 2 предоставит пошаговые инструкции по дальнейшим действиям:</span><span class="sxs-lookup"><span data-stu-id="ca144-127">HoloLens 2 will walk you through the following steps:</span></span>

1. <span data-ttu-id="ca144-128">Выберите нужный язык.</span><span class="sxs-lookup"><span data-stu-id="ca144-128">Select your language.</span></span>

    ![Выберите язык.](images/04-language.png)

1. <span data-ttu-id="ca144-130">Выберите нужный регион.</span><span class="sxs-lookup"><span data-stu-id="ca144-130">Select your region.</span></span>

    ![Выбор региона](images/05-region.png)

1. <span data-ttu-id="ca144-132">Выполните калибровку HoloLens для отслеживания глаз.</span><span class="sxs-lookup"><span data-stu-id="ca144-132">Calibrate HoloLens to your eyes.</span></span>  <span data-ttu-id="ca144-133">Если вы пропустите калибровку, запрос калибровки появится при следующем входе в систему.</span><span class="sxs-lookup"><span data-stu-id="ca144-133">If you choose to skip calibration, you'll be prompted the next time you log in.</span></span> 

    1. <span data-ttu-id="ca144-134">Сначала отрегулируйте визор.</span><span class="sxs-lookup"><span data-stu-id="ca144-134">First, you'll adjust your visor.</span></span>
    
        ![Экран выбора калибровки](images/06-et-corners.png)

    2. <span data-ttu-id="ca144-136">Для калибровки вам нужно посмотреть на несколько целей (которые называются драгоценными камнями).</span><span class="sxs-lookup"><span data-stu-id="ca144-136">To calibrate, you'll look at a set of targets (referred to as gems).</span></span> <span data-ttu-id="ca144-137">Во время калибровки можно моргать и закрывать глаза, но старайтесь не фокусироваться на других объектах в комнате или пространстве.</span><span class="sxs-lookup"><span data-stu-id="ca144-137">It's fine if you blink or close your eyes during calibration, but try not to stare at other objects in the room or physical space.</span></span> <span data-ttu-id="ca144-138">Во время этого процесса HoloLens изучает положение ваших глаз для оптимального отображения голографического мира.</span><span class="sxs-lookup"><span data-stu-id="ca144-138">HoloLens uses this process to learn about your eye position so that it can better render your holographic world.</span></span> 

        ![Корректировка для ваших глаз](images/07-adjust-eyes.png)

        <span data-ttu-id="ca144-140">После калибровки голограммы будут отображаться правильно даже в случае смещения визора на голове.</span><span class="sxs-lookup"><span data-stu-id="ca144-140">After calibration, holograms will appear correctly even as the visor shifts on your head.</span></span> <span data-ttu-id="ca144-141">Сведения о калибровке хранятся локально на устройстве и не связываются с какими-либо сведениями учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ca144-141">Calibration information is stored locally on the device and is not associated with any account information.</span></span> <span data-ttu-id="ca144-142">Дополнительные сведения см. в разделе [Данные калибровки и безопасность](hololens-calibration.md#calibration-data-and-security).</span><span class="sxs-lookup"><span data-stu-id="ca144-142">For more information, see [Calibration data and security](hololens-calibration.md#calibration-data-and-security).</span></span>

        ![Калибровка завершена](images/calibration-complete.png)

1. <span data-ttu-id="ca144-144">Подключитесь к Интернету (выберите подключение Wi-Fi или Ethernet).</span><span class="sxs-lookup"><span data-stu-id="ca144-144">Connect to the internet (select Wi-Fi or your ethernet connection).</span></span>

     <span data-ttu-id="ca144-145">HoloLens автоматически настроит часовой пояс на основании информации, полученной от сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="ca144-145">HoloLens sets your time zone automatically based on information obtained from the Wi-Fi network.</span></span> <span data-ttu-id="ca144-146">После завершения настройки часовой пояс можно изменить с помощью приложения "Параметры".</span><span class="sxs-lookup"><span data-stu-id="ca144-146">After setup finishes, you can change the time zone by using the Settings app.</span></span>

    ![Подключение к Wi-Fi](images/11-network.png)

    > [!NOTE] 
    > <span data-ttu-id="ca144-148">Если вы подключились к Wi-Fi и затем захотели переключиться на другую сеть, находясь в процессе настройки, можно одновременно нажать кнопки **уменьшения громкости** и **увеличения громкости**, чтобы вернуться к этому шагу, если вы используете версию ОС от октября 2019 г. или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="ca144-148">If you progress past the Wi-Fi step and later need to switch to a different network while still in setup, you can press the **Volume Down** and **Power** buttons simultaneously to return to this step if you are running an OS version from October 2019 or later.</span></span> <span data-ttu-id="ca144-149">В более ранних версиях может потребоваться [сбросить устройство](hololens-recovery.md) или перезапустить его в таком месте, где выбранная сеть Wi-Fi недоступна, чтобы предотвратить автоматическое подключение.</span><span class="sxs-lookup"><span data-stu-id="ca144-149">For earlier versions, you may need to [reset the device](hololens-recovery.md) or restart it in a location where the Wi-Fi network is not available to prevent it from automatically connecting.</span></span>
    > 
    > <span data-ttu-id="ca144-150">Также обратите внимание, что во время настройки HoloLens период ожидания учетных данных составляет две минуты.</span><span class="sxs-lookup"><span data-stu-id="ca144-150">Also note that during HoloLens Setup, there is a credential timeout of two minutes.</span></span> <span data-ttu-id="ca144-151">Имя пользователя и пароль необходимо ввести в течение двух минут, в противном случае поле имени пользователя будет автоматически очищено.</span><span class="sxs-lookup"><span data-stu-id="ca144-151">The username/password needs to be entered within two minutes otherwise the username field will be automatically cleared.</span></span>

1. <span data-ttu-id="ca144-152">HoloLens 2 найдет и применит профиль Autopilot, если он существует.</span><span class="sxs-lookup"><span data-stu-id="ca144-152">HoloLens 2 will search and apply an Autopilot profile if one exists.</span></span> <span data-ttu-id="ca144-153">На этом экране никаких действий выполнять не нужно.</span><span class="sxs-lookup"><span data-stu-id="ca144-153">No action is needed on this screen.</span></span>
 
    ![Поиск профиля Autopilot](images/autopilot-profile-search.png) 

1. <span data-ttu-id="ca144-155">Щелкните **Принять** на экране лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ca144-155">Click **Accept** on the licensing screen.</span></span>

    ![Лицензионное соглашение Windows](images/windows-license-agreement.png)

1. <span data-ttu-id="ca144-157">Войдите в свою учетную запись.</span><span class="sxs-lookup"><span data-stu-id="ca144-157">Sign in to your user account.</span></span> <span data-ttu-id="ca144-158">Вы можете выбрать варианты **Моя компания или учебное заведения является владельцем** или **Я являюсь владельцем**.</span><span class="sxs-lookup"><span data-stu-id="ca144-158">You'll choose between **My work or school owns it** and **I own it**.</span></span>

    - <span data-ttu-id="ca144-159">При выборе варианта **Моя компания или учебное заведение является владельцем** необходимо выполнить вход с помощью учетной записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ca144-159">When you choose **My work or school owns it**, you sign in with an Azure AD account.</span></span> <span data-ttu-id="ca144-160">Если в вашей организации используется Azure AD Premium и настроена автоматическая регистрация в MDM, устройство HoloLens будет зарегистрировано в MDM автоматически.</span><span class="sxs-lookup"><span data-stu-id="ca144-160">If your organization uses Azure AD Premium and has configured automatic MDM enrollment, HoloLens automatically enrolls in MDM.</span></span> <span data-ttu-id="ca144-161">Если ваша организация не использует Azure AD Premium, автоматическая регистрация в MDM недоступна.</span><span class="sxs-lookup"><span data-stu-id="ca144-161">If your organization does not use Azure AD Premium, automatic MDM enrollment isn't available.</span></span> <span data-ttu-id="ca144-162">В этом случае необходимо [вручную зарегистрировать HoloLens в управлении устройствами](hololens-enroll-mdm.md#different-ways-to-enroll).</span><span class="sxs-lookup"><span data-stu-id="ca144-162">In that case, you need to [manually enroll HoloLens in device management](hololens-enroll-mdm.md#different-ways-to-enroll).</span></span>

        1. <span data-ttu-id="ca144-163">Введите сведения об учетной записи организации.</span><span class="sxs-lookup"><span data-stu-id="ca144-163">Enter your organizational account information.</span></span>
        1. <span data-ttu-id="ca144-164">Примите заявление о конфиденциальности и лицензионное соглашение с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="ca144-164">Accept the privacy statement and the end user license agreement.</span></span>
        1. <span data-ttu-id="ca144-165">Войдите, используя учетные данные Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ca144-165">Sign in by using your Azure AD credentials.</span></span> <span data-ttu-id="ca144-166">Это может перенаправить вас на страницу входа для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ca144-166">This may redirect to your organization's sign-in page.</span></span>
        1. <span data-ttu-id="ca144-167">Продолжите настройку устройства.</span><span class="sxs-lookup"><span data-stu-id="ca144-167">Continue setting up the device.</span></span>

    - <span data-ttu-id="ca144-168">При выборе варианта **Я являюсь владельцем** выполните вход с помощью учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ca144-168">When you choose **I own it**, you sign in with a Microsoft account.</span></span> <span data-ttu-id="ca144-169">После завершения настройки можно [вручную зарегистрировать HoloLens в системе управления устройствами](hololens-enroll-mdm.md#different-ways-to-enroll).</span><span class="sxs-lookup"><span data-stu-id="ca144-169">After setup is complete, you can [manually enroll HoloLens in device management](hololens-enroll-mdm.md#different-ways-to-enroll).</span></span>

        1. <span data-ttu-id="ca144-170">Введите сведения об учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ca144-170">Enter your Microsoft account information.</span></span>
        2. <span data-ttu-id="ca144-171">Введите пароль.</span><span class="sxs-lookup"><span data-stu-id="ca144-171">Enter your password.</span></span> <span data-ttu-id="ca144-172">Если в вашей учетной записи Майкрософт требуется [двухшаговая проверка подлинности (2FA)](https://blogs.technet.microsoft.com/microsoft_blog/2013/04/17/microsoft-account-gets-more-secure/), завершите процесс проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ca144-172">If your Microsoft account requires [two-step verification (2FA)](https://blogs.technet.microsoft.com/microsoft_blog/2013/04/17/microsoft-account-gets-more-secure/), complete the verification process.</span></span>

    ![Настройка пользователя](images/13-device-owner.png)

1. <span data-ttu-id="ca144-174">Настройте вход Iris, щелкнув **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ca144-174">Setup Iris sign-in by selecting **Next**.</span></span> <span data-ttu-id="ca144-175">Следующий процесс будет очень похож на калибровку отслеживания глаз.</span><span class="sxs-lookup"><span data-stu-id="ca144-175">You will go through a similar experience to the eye calibration.</span></span> <span data-ttu-id="ca144-176">Когда сканирование завершится, щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="ca144-176">Select **Done** when the scan is complete.</span></span> <span data-ttu-id="ca144-177">Вы также можете пропустить этот шаг, щелкнув **Пропустить**.</span><span class="sxs-lookup"><span data-stu-id="ca144-177">You may also select **Skip** to bypass this step.</span></span>
    
    <span data-ttu-id="ca144-178">![Настройка Iris](images/setup-iris.png) ![Настройка Iris завершена](images/iris-setup-complete.png)</span><span class="sxs-lookup"><span data-stu-id="ca144-178">![Iris setup](images/setup-iris.png) ![Iris setup completion](images/iris-setup-complete.png)</span></span> 
     
  
1. <span data-ttu-id="ca144-179">Теперь вы настроите PIN-код для входа на устройство.</span><span class="sxs-lookup"><span data-stu-id="ca144-179">You'll setup a PIN to log into the device.</span></span> <span data-ttu-id="ca144-180">Этот PIN-код относится только к конкретному устройству.</span><span class="sxs-lookup"><span data-stu-id="ca144-180">This PIN is device specific.</span></span> 

    ![Настройка Windows Hello](images/setup-windows-hello.png)

    ![Настройка PIN-кода Windows Hello](images/windows-hello-pin.png)

    ![Настройка Windows Hello завершена успешно](images/windows-hello-successful.png) 
    
1. <span data-ttu-id="ca144-184">Выберите, нужно ли включить на HoloLens 2 поддержку речи.</span><span class="sxs-lookup"><span data-stu-id="ca144-184">Select whether to enable speech on HoloLens 2.</span></span>

    ![Включение Кортаны](images/22-do-more-with-voice.png)

1. <span data-ttu-id="ca144-186">Выберите, нужно ли включить на HoloLens 2 отслеживание местоположения.</span><span class="sxs-lookup"><span data-stu-id="ca144-186">Select whether to enable location on HoloLens 2.</span></span>
    
    ![Включение служб определения местоположения](images/setup-location-services.png)

1. <span data-ttu-id="ca144-188">Выберите нужный уровень телеметрии.</span><span class="sxs-lookup"><span data-stu-id="ca144-188">Select your telemetry level.</span></span> <span data-ttu-id="ca144-189">Если возможно, включите необязательную телеметрию.</span><span class="sxs-lookup"><span data-stu-id="ca144-189">If you can, please enable Optional telemetry.</span></span> <span data-ttu-id="ca144-190">Эта информация очень помогает команде разработчиков HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ca144-190">This information really helps the HoloLens engineering team.</span></span>

     ![Уровень телеметрии](images/24-telemetry.png)

1. <span data-ttu-id="ca144-192">Узнайте, как использовать жест "Пуск" на HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="ca144-192">Learn how to use the start gesture on HoloLens 2.</span></span>

     ![Использование жеста "Пуск", изображение 1](images/26-01-startmenu-learning.png)

     ![Использование жеста "Пуск", изображение 2](images/26-02-startmenu-learning.png)

<span data-ttu-id="ca144-195&quot;>Поздравляем!</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;ca144-195&quot;>Congratulations!</span></span>  <span data-ttu-id=&quot;ca144-196&quot;>Настройка завершена, и вы готовы к использованию HoloLens.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;ca144-196&quot;>Setup is complete and you're ready to use HoloLens!</span></span>

## <a name=&quot;next-steps&quot;></a><span data-ttu-id=&quot;ca144-197&quot;>Дальнейшие действия</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;ca144-197&quot;>Next steps</span></span>

1. <span data-ttu-id=&quot;ca144-198&quot;>Начните взаимодействовать со смешанной реальностью и осуществлять навигацию по Windows 10 на вашем устройстве HoloLens. В приложении **Советы** вы найдете пошаговые инструкции по взаимодействию с помощью рук.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;ca144-198&quot;>Start interacting right away with Mixed Reality and navigating Windows 10 on your HoloLens - check out the **Tips** app for hands-on tutorials for hand interactions.</span></span> <span data-ttu-id=&quot;ca144-199&quot;>Используйте жест &quot;Пуск&quot; для перехода в одноименное меню или произнесите &quot;Go to Start&quot; (Перейти в меню &quot;Пуск") и выберите "Советы".</span><span class="sxs-lookup"><span data-stu-id="ca144-199">Use the start gesture to go to Start or say "Go to Start" and select Tips.</span></span>

1. <span data-ttu-id="ca144-200">Щелкните ниже, чтобы продолжить чтение инструкций по началу работы с HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="ca144-200">Click below to continue reading about getting around HoloLens 2.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ca144-201">Знакомство с HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="ca144-201">Getting around HoloLens 2</span></span>](hololens2-basic-usage.md)
