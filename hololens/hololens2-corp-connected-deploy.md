---
title: 'руководство по развертыванию: корпоративные подключенные HoloLens 2 с руководствами по Dynamics 365 — развертывание'
description: узнайте, как настроить развертывания HoloLens 2 устройств в корпоративной сети с помощью руководств по Dynamics 365.
keywords: HoloLens, управление, корпоративные подключения, руководства по Dynamics 365, AAD, Azure AD, MDM, управление мобильными устройствами
author: joyjaz
ms.author: v-jjaswinski
ms.reviewer: aboeger
ms.date: 03/24/2021
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 6407517bca9efd02fdaf45a78cba7a215ec05670
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113637070"
---
# <a name="deploy---corporate-connected-guide"></a><span data-ttu-id="24a47-104">Развертывание — интегрированное с корпоративным руководством</span><span class="sxs-lookup"><span data-stu-id="24a47-104">Deploy - Corporate Connected Guide</span></span>

<span data-ttu-id="24a47-105">Важной частью каждого развертывания является обеспечение правильной настройки развертывания перед тестированием, чтобы обеспечить бесперебойную работу конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="24a47-105">An important part of each deployment is ensuring that your deployment is properly set up before testing it yourself to ensure a smooth experience for the end user.</span></span>

<span data-ttu-id="24a47-106">поскольку мы развертываем сертификат Wi-Fi с помощью MDM, сначала необходимо настроить HoloLens и зарегистрировать устройства в открытой Wi-Fi сети или в сети, не требующей сертификата.</span><span class="sxs-lookup"><span data-stu-id="24a47-106">Because we are deploying the Wi-Fi certificate via MDM, we'll need to initially set up HoloLens and enroll devices on an open Wi-Fi network, or a network that doesn't require the certificate.</span></span> <span data-ttu-id="24a47-107">после того как HoloLens завершит работу OOBE и зарегистрировался, устройство получит сетевой сертификат и настроенный ранее бизнес-объект, и мы сможем проверить, были ли они получены устройством.</span><span class="sxs-lookup"><span data-stu-id="24a47-107">Once the HoloLens has finished OOBE and Enrolled, the device will receive the network certificate and LOB configured previously and we'll be able to validate both were received by the device.</span></span>

<span data-ttu-id="24a47-108">После этого вы сможете подтвердить создание и работу с руководством по тестированию.</span><span class="sxs-lookup"><span data-stu-id="24a47-108">Afterwards, you'll be able confirm you can both author and operate a test Guide.</span></span>

## <a name="enrollment-validation"></a><span data-ttu-id="24a47-109">Проверка регистрации</span><span class="sxs-lookup"><span data-stu-id="24a47-109">Enrollment Validation</span></span>

<span data-ttu-id="24a47-110">Теперь, когда все правильно настроено для регистрации Azure AD и MDM, остальное теперь должно быть привязкой.</span><span class="sxs-lookup"><span data-stu-id="24a47-110">Now that everything is properly configured for Azure AD and MDM Enrollment, the rest should now be a snap.</span></span> <span data-ttu-id="24a47-111">вам потребуется подключение Wi-Fi и устройство HoloLens, а также одна из ранее настроенных учетных записей пользователя Azure AD.</span><span class="sxs-lookup"><span data-stu-id="24a47-111">You'll need a Wi-Fi connection and the HoloLens device, and one of the previously configured Azure AD user accounts.</span></span>

<span data-ttu-id="24a47-112">Если ваше устройство в настоящее время не находится в состоянии заводской настройки, теперь пришло время переносить [устройство на флэш-память](/hololens/hololens-recovery#clean-reflash-the-device).</span><span class="sxs-lookup"><span data-stu-id="24a47-112">If your device isn't currently sitting in a factory settings state, now would be a good time to [reflash the device](/hololens/hololens-recovery#clean-reflash-the-device).</span></span>

1. <span data-ttu-id="24a47-113">После того как устройство находится в OOBE, необходимо начать взаимодействие и выполнить следующие запросы.</span><span class="sxs-lookup"><span data-stu-id="24a47-113">Once your device is in OOBE, you'll need to start interacting and following the prompts.</span></span>

2. <span data-ttu-id="24a47-114">Подключение в открытую Wi-Fi сеть, которая не требует сертификатов для подключения к Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="24a47-114">Connect to an open Wi-Fi network that does not require certificates to join the Wi-Fi.</span></span> <span data-ttu-id="24a47-115">Это позволит устройству загрузить сертификат, который будет использоваться в Wi-Fi Организации после начальной настройки.</span><span class="sxs-lookup"><span data-stu-id="24a47-115">This will allow the device to download the certificate to be used on the organization's Wi-Fi after initial setup.</span></span>

3. <span data-ttu-id="24a47-116">при запросе **Кто владельцем этого HoloLens** будет критическое сообщение?</span><span class="sxs-lookup"><span data-stu-id="24a47-116">The critical prompt will be when you are asked **Who owns this HoloLens?**</span></span> <span data-ttu-id="24a47-117">Выберите **Моя рабочая или учебная** сеть и укажите учетные данные учетной записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="24a47-117">Select **My work or school owns it** and enter your Azure AD account credentials.</span></span>

4. <span data-ttu-id="24a47-118">После успешного завершения регистрации вам будет предложено настроить ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="24a47-118">When enrollment is successful, you'll be prompted to set up a PIN.</span></span> <span data-ttu-id="24a47-119">Этот ПИН-код уникален для этого устройства для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="24a47-119">This PIN is unique to this device for this user.</span></span> <span data-ttu-id="24a47-120">Кроме того, вы получите запрос на сканирование IRI, данные голоса и параметры телеметрии, и наконец, сможете узнать, как открыть меню "Пуск" и завершить OOBE.</span><span class="sxs-lookup"><span data-stu-id="24a47-120">You will also be prompted for Iris scans, voice data, and telemetry settings and finally, you'll be able to learn how to open the start menu and complete OOBE.</span></span>

5. <span data-ttu-id="24a47-121">когда вы попадете на домашнюю страницу Mixed Reality, откройте меню с помощью только что полученного **жеста запуска** .</span><span class="sxs-lookup"><span data-stu-id="24a47-121">Once you land in the Mixed Reality Home, open the Start menu using the **Start gesture** you just learned.</span></span>

6. <span data-ttu-id="24a47-122">выберите приложение **Параметры** и выберите **система**.</span><span class="sxs-lookup"><span data-stu-id="24a47-122">Select the **Settings** app and select **System**.</span></span> <span data-ttu-id="24a47-123">первое, что вы увидите, — это имя устройства, которое для устройства HoloLens 2 будет указывать &quot; HoloLens, &quot; за которым следует шесть символьных строк.</span><span class="sxs-lookup"><span data-stu-id="24a47-123">The first piece of information you'll see is your Device name, which for your HoloLens 2 device will be &quot;HOLOLENS-&quot; followed by a six character string.</span></span>

7. <span data-ttu-id="24a47-124">Запишите это имя.</span><span class="sxs-lookup"><span data-stu-id="24a47-124">Take note of this name.</span></span>

    ![экран Параметры HoloLens 2](./images/hololens2-settings-about.jpg)

8. <span data-ttu-id="24a47-126">Убедитесь, что устройство успешно присоединено к Azure AD.</span><span class="sxs-lookup"><span data-stu-id="24a47-126">Verify that your device is successfully joined to Azure AD.</span></span> <span data-ttu-id="24a47-127">Существует два способа.</span><span class="sxs-lookup"><span data-stu-id="24a47-127">There are two ways;</span></span>

    1.  <span data-ttu-id="24a47-128">приложение Параметры.</span><span class="sxs-lookup"><span data-stu-id="24a47-128">The Settings app.</span></span> <span data-ttu-id="24a47-129">на **Параметры** выберите **учетные записи**  ->  **доступ к рабочей или учебной заведению**.</span><span class="sxs-lookup"><span data-stu-id="24a47-129">From **Settings** select **Accounts** -> **Access work or school**.</span></span> <span data-ttu-id="24a47-130">На этом экране вы можете убедиться, что регистрация успешно выполнена, просмотрев &quot; Подключение к намеофаад&#39;s Azure AD.</span><span class="sxs-lookup"><span data-stu-id="24a47-130">From this screen, you can verify you are successfully enrolled by seeing &quot;Connected to nameofAAD&#39;s Azure AD.</span></span> <span data-ttu-id="24a47-131">Соединено *yourusername@nameofAAD.onmicrosoft.com* .</span><span class="sxs-lookup"><span data-stu-id="24a47-131">Connected by *yourusername@nameofAAD.onmicrosoft.com*.</span></span> <span data-ttu-id="24a47-132">Это позволит проверить, присоединено ли ваше устройство к вашей организации&#39;s Azure AD.</span><span class="sxs-lookup"><span data-stu-id="24a47-132">This will verify your device is joined to your organization&#39;s Azure AD.</span></span>

    1. <span data-ttu-id="24a47-133">[Портал Azure](https://portal.azure.com/#home).</span><span class="sxs-lookup"><span data-stu-id="24a47-133">The [Azure portal](https://portal.azure.com/#home).</span></span> <span data-ttu-id="24a47-134">перейдите в **Azure Active Directory**  ->  **устройства**  ->  **все устройства** и выполните поиск по имени устройства.</span><span class="sxs-lookup"><span data-stu-id="24a47-134">Go to **Azure Active Directory** -> **Devices** -> **All devices**, and search the device name.</span></span> <span data-ttu-id="24a47-135">В разделе Тип соединения будет отображаться как "присоединение к Azure AD".</span><span class="sxs-lookup"><span data-stu-id="24a47-135">Under Join Type, it will show as being 'Azure AD Joined'.</span></span>
        <span data-ttu-id="24a47-136">![Проверка типа присоединение в Azure AD](./images/hololens2-devices-all-devices.png)</span><span class="sxs-lookup"><span data-stu-id="24a47-136">![Verify Join Type in Azure AD](./images/hololens2-devices-all-devices.png)</span></span>

9. <span data-ttu-id="24a47-137">Убедитесь, что устройство зарегистрировано в MDM.</span><span class="sxs-lookup"><span data-stu-id="24a47-137">Verify that your device is enrolled with MDM.</span></span> <span data-ttu-id="24a47-138">Существует два способа.</span><span class="sxs-lookup"><span data-stu-id="24a47-138">There are two ways;</span></span>

    1. <span data-ttu-id="24a47-139">на **Параметры** выберите **учетные записи**  ->  **доступ к рабочей или учебной заведению**.</span><span class="sxs-lookup"><span data-stu-id="24a47-139">From **Settings**, select **Accounts** -> **Access work or school**.</span></span> <span data-ttu-id="24a47-140">На этом экране вы можете убедиться, что регистрация успешно выполнена, просмотрев &quot; Подключение к намеофаад&#39;s Azure AD.</span><span class="sxs-lookup"><span data-stu-id="24a47-140">From this screen, you can verify you are successfully enrolled by seeing &quot;Connected to nameofAAD&#39;s Azure AD.</span></span> <span data-ttu-id="24a47-141">Соединено *yourusername@nameofAAD.onmicrosoft.com* .</span><span class="sxs-lookup"><span data-stu-id="24a47-141">Connected by *yourusername@nameofAAD.onmicrosoft.com*.</span></span> <span data-ttu-id="24a47-142">Чтобы получить доступ к рабочей или учебной учетной записи, выберите &quot; Подключение к намеофаад&#39;s Azure AD.</span><span class="sxs-lookup"><span data-stu-id="24a47-142">From this Access work or school account by selecting &quot;Connected to nameofAAD&#39;s Azure AD.</span></span> <span data-ttu-id="24a47-143">Подключено, yourusername@nameofAAD.onmicrosoft.com &quot; и нажмите кнопку **сведения** .</span><span class="sxs-lookup"><span data-stu-id="24a47-143">Connected by yourusername@nameofAAD.onmicrosoft.com&quot; and select the **Info** button.</span></span>

    1. <span data-ttu-id="24a47-144">[центр администрирования Microsoft Endpoint Manager](https://endpoint.microsoft.com/#home).</span><span class="sxs-lookup"><span data-stu-id="24a47-144">[Microsoft Endpoint Manager Admin Center](https://endpoint.microsoft.com/#home).</span></span> <span data-ttu-id="24a47-145">Войдите в систему и выберите  **устройства**  , а затем  **все устройства**.</span><span class="sxs-lookup"><span data-stu-id="24a47-145">Log in and select  **Devices**  then  **All devices**.</span></span> <span data-ttu-id="24a47-146">здесь можно выполнить поиск по имени HoloLens устройства&#39;s.</span><span class="sxs-lookup"><span data-stu-id="24a47-146">From here, you can search your HoloLens device&#39;s name.</span></span> <span data-ttu-id="24a47-147">вы сможете просмотреть HoloLens, перечисленные в Intune.</span><span class="sxs-lookup"><span data-stu-id="24a47-147">You should be able to see your HoloLens listed on Intune.</span></span>

        ![Проверка управления с помощью Intune в Azure AD](./images/hololens2-devices-all-devices2.png)


## <a name="wi-fi-certificate-validation"></a><span data-ttu-id="24a47-149">Проверка сертификата Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="24a47-149">Wi-Fi certificate validation</span></span>

<span data-ttu-id="24a47-150">На данный момент устройство должно получить сертификат Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="24a47-150">By now, the device should have received the Wi-Fi certificate.</span></span> <span data-ttu-id="24a47-151">Простейший способ проверки — попытка подключения к Wi-Fiному подключению, для которого&#39;получен сертификат.</span><span class="sxs-lookup"><span data-stu-id="24a47-151">The simplest validation you can do is attempt to connect to the Wi-Fi connection for which you&#39;ve received the certificate.</span></span> <span data-ttu-id="24a47-152">откройте приложение **Параметры** и перейдите к **сети &amp; интернет**  ->  **wi-Fi** и выберите подключение Wi-fi.</span><span class="sxs-lookup"><span data-stu-id="24a47-152">Open up the **Settings** app and navigate to **Network &amp; Internet** -> **Wi-Fi** and select the Wi-fi connection.</span></span> <span data-ttu-id="24a47-153">после подключения откройте приложение Microsoft Edge и убедитесь, что вы можете перейти на веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="24a47-153">Once connected, open up the Microsoft Edge app and confirm you can navigate to a website.</span></span>

<span data-ttu-id="24a47-154">Чтобы убедиться, что сертификат получен на устройстве, можно использовать [Диспетчер сертификатов](/hololens/certificate-manager).</span><span class="sxs-lookup"><span data-stu-id="24a47-154">To confirm that you have received the certificate on the device, you can use the [Certificate Manager](/hololens/certificate-manager).</span></span>

## <a name="validate-lob-app-install"></a><span data-ttu-id="24a47-155">Проверка установки бизнес-приложения</span><span class="sxs-lookup"><span data-stu-id="24a47-155">Validate LOB app install</span></span>

<span data-ttu-id="24a47-156">чтобы увидеть ход установки управляемого приложения, можно проверить, установлено ли приложение или проверьте Параметры.</span><span class="sxs-lookup"><span data-stu-id="24a47-156">To see a managed app's install progress, you either see if the app is installed or check Settings.</span></span> <span data-ttu-id="24a47-157">настроив бизнес-приложение в качестве обязательной установки для нашей группы, после регистрации HoloLens с пользователем в назначенной группе приложение автоматически скачивается в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="24a47-157">By configuring a LOB app as a required installation for our group, after enrolling the HoloLens with a user in the assigned group, the app will automatically download to the HoloLens.</span></span>

<span data-ttu-id="24a47-158">откройте меню и выберите **все приложения**.</span><span class="sxs-lookup"><span data-stu-id="24a47-158">Open the Start menu and select **All apps**.</span></span> <span data-ttu-id="24a47-159">В зависимости от количества приложений может потребоваться использовать кнопки **Page Up** или **Page Down** .</span><span class="sxs-lookup"><span data-stu-id="24a47-159">Depending on the number of apps you have, you may need to use the **page up** or **page down** buttons.</span></span>

<span data-ttu-id="24a47-160">чтобы проверить установку приложения на устройстве, это можно сделать с помощью **Параметры**  ->  **учетных записей**  ->  **доступ к работе или учебному заведению**; выберите учетную запись, а затем нажмите кнопку " **сведения** " и прокрутите вниз, чтобы просмотреть различные конфигурации и приложения, применяемые к устройству из MDM.</span><span class="sxs-lookup"><span data-stu-id="24a47-160">To validate the installation of the app on device, you can do so via **Settings** -> **Accounts** -> **Access work or school**; select the account then the **Info** button, and scroll down to see different configurations and apps applied to the device from MDM.</span></span>

<span data-ttu-id="24a47-161">Чтобы проверить установку из Intune, перейдите на страницу " [приложения портала MEM](https://endpoint.microsoft.com/#home)"  ->   — > все **приложения**  -> *сенамеофйоурапп*  ->  **состояние установки устройства** .</span><span class="sxs-lookup"><span data-stu-id="24a47-161">To validate the install from Intune, navigate to the [MEM portal](https://endpoint.microsoft.com/#home) -> **Apps** -> All **apps** ->*TheNameOfYourApp* -> **Device install status** page.</span></span>

<span data-ttu-id="24a47-162">Дополнительные сведения: [развертывание приложений Intune для HoloLens](/hololens/app-deploy-intune)</span><span class="sxs-lookup"><span data-stu-id="24a47-162">See more: [Intune App Deployment for HoloLens](/hololens/app-deploy-intune)</span></span>

## <a name="validate-dynamics-365-guides"></a><span data-ttu-id="24a47-163">Проверка руководств по Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="24a47-163">Validate Dynamics 365 Guides</span></span>

<span data-ttu-id="24a47-164">существуют режимы для приложения "руководства" на HoloLens, создания и эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="24a47-164">There are modes for the Guides app on HoloLens, authoring and operating.</span></span> <span data-ttu-id="24a47-165">Перед началом работы с руководством вам потребуется завершить создание руководств.</span><span class="sxs-lookup"><span data-stu-id="24a47-165">You'll need to finish authoring a guide before operating it.</span></span>

### <a name="authoring-the-guide"></a><span data-ttu-id="24a47-166">Создание руководств</span><span class="sxs-lookup"><span data-stu-id="24a47-166">Authoring the Guide</span></span>

<span data-ttu-id="24a47-167">Для этой быстрой проверки не нужно выполнять много усилий.</span><span class="sxs-lookup"><span data-stu-id="24a47-167">We don't need to do much for this quick validation.</span></span> <span data-ttu-id="24a47-168">Просто выберите программное обеспечение, подготовленное на компьютере.</span><span class="sxs-lookup"><span data-stu-id="24a47-168">Simply select the guide you prepared on your PC.</span></span> <span data-ttu-id="24a47-169">Необходимо [привязать руководство](/dynamics365/mixed-reality/guides/hololens-app-anchor)для быстрой проверки, в которой можно использовать привязку Holographic.</span><span class="sxs-lookup"><span data-stu-id="24a47-169">You'll need to [anchor the guide](/dynamics365/mixed-reality/guides/hololens-app-anchor), for a quick validation you can use a holographic anchor.</span></span> <span data-ttu-id="24a47-170">После этого необходимо [разместить шаги и модели](/dynamics365/mixed-reality/guides/hololens-app-orientation).</span><span class="sxs-lookup"><span data-stu-id="24a47-170">Afterwards, you should [place your steps and models](/dynamics365/mixed-reality/guides/hololens-app-orientation).</span></span>

>[!NOTE]
> <span data-ttu-id="24a47-171">Вам потребуется роль **разработки** для входа на ПК и создания на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="24a47-171">You will need the **Authoring** role to login to the PC and author on the HoloLens.</span></span> <span data-ttu-id="24a47-172">Роль оператора доступна только для чтения и не имеет доступа к приложению для ПК.</span><span class="sxs-lookup"><span data-stu-id="24a47-172">The Operator role is read-only and has no access to the PC app.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/poE7s7_zWDE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### <a name="operating-the-guide"></a><span data-ttu-id="24a47-173">Работа с руководством</span><span class="sxs-lookup"><span data-stu-id="24a47-173">Operating the Guide</span></span>

<span data-ttu-id="24a47-174">После того как голограммы будут установлены, вы можете протестировать работу с руководством.</span><span class="sxs-lookup"><span data-stu-id="24a47-174">Once your holograms are in place, you can test out operating your guide.</span></span> 
- <span data-ttu-id="24a47-175">Выбор **режима оператора**</span><span class="sxs-lookup"><span data-stu-id="24a47-175">Select **Operator mode**</span></span>
- <span data-ttu-id="24a47-176">Щелкните шаги, описанные в руководстве.</span><span class="sxs-lookup"><span data-stu-id="24a47-176">Click through the steps of your guide.</span></span>

<span data-ttu-id="24a47-177">Чтобы получить более подробные инструкции по работе с руководством, ознакомьтесь с этими материалами:</span><span class="sxs-lookup"><span data-stu-id="24a47-177">For more in-depth guidance on how to operate a guide, check out these resources:</span></span>

[<span data-ttu-id="24a47-178">Обзор работы руководства в руководствах по Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="24a47-178">Overview of operating a guide in Dynamics 365 Guides</span></span>](/dynamics365/mixed-reality/guides/operator-overview)

[<span data-ttu-id="24a47-179">Приготовьтесь к работе с помощью пошаговой карты в качестве оператора в руководствах по Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="24a47-179">Get oriented with the Step card as an operator in Dynamics 365 Guides</span></span>](/dynamics365/mixed-reality/guides/operator-step-card-orientation)

<iframe width="560" height="315" src="https://www.youtube.com/embed/9s41BKGHVL8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <a name="next-step"></a><span data-ttu-id="24a47-180">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="24a47-180">Next step</span></span> 
> [!div class="nextstepaction"]
> [<span data-ttu-id="24a47-181">Развертывание с корпоративным подключением — обслуживание</span><span class="sxs-lookup"><span data-stu-id="24a47-181">Corporate connected deployment - Maintain</span></span>](hololens2-corp-connected-maintain.md)
