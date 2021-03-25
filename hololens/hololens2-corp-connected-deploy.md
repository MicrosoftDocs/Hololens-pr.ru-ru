---
title: Руководство по развертыванию — корпоративные подключенные HoloLens 2 с руководствами dynamics 365 — развертывание
description: Узнайте, как настроить развертывание устройств HoloLens 2 в корпоративной сети Connected with Dynamics 365 Guides.
keywords: HoloLens, управление, корпоративное подключение, Руководство по динамике 365, AAD, Azure AD, MDM, Управление мобильными устройствами
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
ms.openlocfilehash: febf56f94a5cab623fd7ad08ae7abf7050224717
ms.sourcegitcommit: d7c86ccad7be32f7223d4b801083798454fda740
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2021
ms.locfileid: "11448615"
---
# <a name="deploy---corporate-connected-guide"></a><span data-ttu-id="3d28b-104">Deploy — руководство по корпоративным подключениям</span><span class="sxs-lookup"><span data-stu-id="3d28b-104">Deploy - Corporate Connected Guide</span></span>

<span data-ttu-id="3d28b-105">Важной частью каждого развертывания является правильное настройка развертывания перед самим тестированием, чтобы обеспечить бесперебойную работу для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d28b-105">An important part of each deployment is ensuring that your deployment is properly set up before testing it yourself to ensure a smooth experience for the end user.</span></span>

<span data-ttu-id="3d28b-106">Поскольку мы развертываем Wi-Fi с помощью MDM, нам необходимо сначала настроить HoloLens и записать устройства в открытую сеть Wi-Fi или сеть, которая не требует сертификата.</span><span class="sxs-lookup"><span data-stu-id="3d28b-106">Because we are deploying the Wi-Fi certificate via MDM, we'll need to initially set up HoloLens and enroll devices on an open Wi-Fi network, or a network that doesn't require the certificate.</span></span> <span data-ttu-id="3d28b-107">После завершения OOBE и регистрации HoloLens устройство получит сетевой сертификат и LOB, настроенные ранее, и мы сможем проверить оба полученных устройства.</span><span class="sxs-lookup"><span data-stu-id="3d28b-107">Once the HoloLens has finished OOBE and Enrolled, the device will receive the network certificate and LOB configured previously and we'll be able to validate both were received by the device.</span></span>

<span data-ttu-id="3d28b-108">После этого вы сможете подтвердить, что можете как автор, так и руководство по проверке.</span><span class="sxs-lookup"><span data-stu-id="3d28b-108">Afterwards, you'll be able confirm you can both author and operate a test Guide.</span></span>

## <a name="enrollment-validation"></a><span data-ttu-id="3d28b-109">Проверка регистрации</span><span class="sxs-lookup"><span data-stu-id="3d28b-109">Enrollment Validation</span></span>

<span data-ttu-id="3d28b-110">Теперь, когда все правильно настроено для регистрации Azure AD и MDM, остальное должно быть оснасткой.</span><span class="sxs-lookup"><span data-stu-id="3d28b-110">Now that everything is properly configured for Azure AD and MDM Enrollment, the rest should now be a snap.</span></span> <span data-ttu-id="3d28b-111">Вам потребуется подключение Wi-Fi и устройство HoloLens, а также одна из ранее настроенных учетных записей пользователей Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3d28b-111">You'll need a Wi-Fi connection and the HoloLens device, and one of the previously configured Azure AD user accounts.</span></span>

<span data-ttu-id="3d28b-112">Если ваше устройство в настоящее время не находится в состоянии заводских параметров, сейчас будет хорошее время для перезахощения [устройства.](https://docs.microsoft.com/hololens/hololens-recovery#clean-reflash-the-device)</span><span class="sxs-lookup"><span data-stu-id="3d28b-112">If your device isn't currently sitting in a factory settings state, now would be a good time to [reflash the device](https://docs.microsoft.com/hololens/hololens-recovery#clean-reflash-the-device).</span></span>

1. <span data-ttu-id="3d28b-113">После того как устройство будет в OOBE, вам потребуется приступить к взаимодействию и следуя подсказкам.</span><span class="sxs-lookup"><span data-stu-id="3d28b-113">Once your device is in OOBE, you'll need to start interacting and following the prompts.</span></span>

2. <span data-ttu-id="3d28b-114">Подключение к открытой Wi-Fi, для подключения к Wi-Fi не требуются сертификаты.</span><span class="sxs-lookup"><span data-stu-id="3d28b-114">Connect to an open Wi-Fi network that does not require certificates to join the Wi-Fi.</span></span> <span data-ttu-id="3d28b-115">Это позволит устройству скачать сертификат, который будет использоваться в Wi-Fi организации после начальной установки.</span><span class="sxs-lookup"><span data-stu-id="3d28b-115">This will allow the device to download the certificate to be used on the organization's Wi-Fi after initial setup.</span></span>

3. <span data-ttu-id="3d28b-116">Критический запрос будет, когда вас **спрашивают, кому принадлежит этот HoloLens?**</span><span class="sxs-lookup"><span data-stu-id="3d28b-116">The critical prompt will be when you are asked **Who owns this HoloLens?**</span></span> <span data-ttu-id="3d28b-117">Выберите **свою работу или школу, владеют ней,** и введите учетные данные учетных записей Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3d28b-117">Select **My work or school owns it** and enter your Azure AD account credentials.</span></span>

4. <span data-ttu-id="3d28b-118">Когда регистрация будет успешной, вам будет предложено настроить ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="3d28b-118">When enrollment is successful, you'll be prompted to set up a PIN.</span></span> <span data-ttu-id="3d28b-119">Этот ПИН-код является уникальным для этого устройства для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d28b-119">This PIN is unique to this device for this user.</span></span> <span data-ttu-id="3d28b-120">Вам также будут предложены параметры сканирования радужной оболочки глаза, голосовых данных и телеметрии, и, наконец, вы сможете узнать, как открыть меню пусков и завершить OOBE.</span><span class="sxs-lookup"><span data-stu-id="3d28b-120">You will also be prompted for Iris scans, voice data, and telemetry settings and finally, you'll be able to learn how to open the start menu and complete OOBE.</span></span>

5. <span data-ttu-id="3d28b-121">Как только вы приземлитесь в доме смешанной реальности, откройте меню Пуск с помощью жеста **Пуск,** который вы только что узнали.</span><span class="sxs-lookup"><span data-stu-id="3d28b-121">Once you land in the Mixed Reality Home, open the Start menu using the **Start gesture** you just learned.</span></span>

6. <span data-ttu-id="3d28b-122">Выберите приложение **Параметры** и выберите **System**.</span><span class="sxs-lookup"><span data-stu-id="3d28b-122">Select the **Settings** app and select **System**.</span></span> <span data-ttu-id="3d28b-123">Первая часть информации, которую вы увидите, — это имя устройства, которое для устройства HoloLens 2 будет hololENS, а затем строка из шести &quot; &quot; символов.</span><span class="sxs-lookup"><span data-stu-id="3d28b-123">The first piece of information you'll see is your Device name, which for your HoloLens 2 device will be &quot;HOLOLENS-&quot; followed by a six character string.</span></span>

7. <span data-ttu-id="3d28b-124">Обратите внимание на это имя.</span><span class="sxs-lookup"><span data-stu-id="3d28b-124">Take note of this name.</span></span>

    ![Экран параметров HoloLens 2](./images/hololens2-settings-about.jpg)

8. <span data-ttu-id="3d28b-126">Убедитесь, что ваше устройство успешно присоединилось к Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3d28b-126">Verify that your device is successfully joined to Azure AD.</span></span> <span data-ttu-id="3d28b-127">Существует два способа.</span><span class="sxs-lookup"><span data-stu-id="3d28b-127">There are two ways;</span></span>

    1.  <span data-ttu-id="3d28b-128">Приложение Параметры.</span><span class="sxs-lookup"><span data-stu-id="3d28b-128">The Settings app.</span></span> <span data-ttu-id="3d28b-129">Из **параметров выберите** **работу или**школу доступа  ->  **к учетным записям.**</span><span class="sxs-lookup"><span data-stu-id="3d28b-129">From **Settings** select **Accounts** -> **Access work or school**.</span></span> <span data-ttu-id="3d28b-130">На этом экране можно убедиться, что вы успешно зарегистрированы, увидев подключение к &quot; nameofAAD&#39;Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3d28b-130">From this screen, you can verify you are successfully enrolled by seeing &quot;Connected to nameofAAD&#39;s Azure AD.</span></span> <span data-ttu-id="3d28b-131">Подключено \*\* yourusername@nameofAAD.onmicrosoft.com .</span><span class="sxs-lookup"><span data-stu-id="3d28b-131">Connected by *yourusername@nameofAAD.onmicrosoft.com*.</span></span> <span data-ttu-id="3d28b-132">Это позволит убедиться, что ваше устройство присоединяется к организации&#39;Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3d28b-132">This will verify your device is joined to your organization&#39;s Azure AD.</span></span>

    1. <span data-ttu-id="3d28b-133">Портал [Azure.](https://portal.azure.com/#home)</span><span class="sxs-lookup"><span data-stu-id="3d28b-133">The [Azure portal](https://portal.azure.com/#home).</span></span> <span data-ttu-id="3d28b-134">Перейдите в **Azure Active Directory**  ->  **Devices All**  ->  **devices**и найдите имя устройства.</span><span class="sxs-lookup"><span data-stu-id="3d28b-134">Go to **Azure Active Directory** -> **Devices** -> **All devices**, and search the device name.</span></span> <span data-ttu-id="3d28b-135">В статье Join Type он будет показываться как "Azure AD Joined".</span><span class="sxs-lookup"><span data-stu-id="3d28b-135">Under Join Type, it will show as being 'Azure AD Joined'.</span></span>
        ![Проверка типа "Регистрация" в Azure AD](./images/hololens2-devices-all-devices.png)

9. <span data-ttu-id="3d28b-137">Убедитесь, что ваше устройство зарегистрировано с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="3d28b-137">Verify that your device is enrolled with MDM.</span></span> <span data-ttu-id="3d28b-138">Существует два способа.</span><span class="sxs-lookup"><span data-stu-id="3d28b-138">There are two ways;</span></span>

    1. <span data-ttu-id="3d28b-139">Из **параметров**выберите **работу или школу**доступа к  ->  **учетным записям.**</span><span class="sxs-lookup"><span data-stu-id="3d28b-139">From **Settings**, select **Accounts** -> **Access work or school**.</span></span> <span data-ttu-id="3d28b-140">На этом экране можно убедиться, что вы успешно зарегистрированы, увидев подключение к &quot; nameofAAD&#39;Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3d28b-140">From this screen, you can verify you are successfully enrolled by seeing &quot;Connected to nameofAAD&#39;s Azure AD.</span></span> <span data-ttu-id="3d28b-141">Подключено \*\* yourusername@nameofAAD.onmicrosoft.com .</span><span class="sxs-lookup"><span data-stu-id="3d28b-141">Connected by *yourusername@nameofAAD.onmicrosoft.com*.</span></span> <span data-ttu-id="3d28b-142">Из этой учетной записи Access или учебной учетной записи выберите &quot; connected to nameofAAD&#39;Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3d28b-142">From this Access work or school account by selecting &quot;Connected to nameofAAD&#39;s Azure AD.</span></span> <span data-ttu-id="3d28b-143">Подключение yourusername@nameofAAD.onmicrosoft.com и &quot; выберите **кнопку Info.**</span><span class="sxs-lookup"><span data-stu-id="3d28b-143">Connected by yourusername@nameofAAD.onmicrosoft.com&quot; and select the **Info** button.</span></span>

    1. <span data-ttu-id="3d28b-144">[Центр администрирования менеджеров конечных точек Майкрософт.](https://endpoint.microsoft.com/#home)</span><span class="sxs-lookup"><span data-stu-id="3d28b-144">[Microsoft Endpoint Manager Admin Center](https://endpoint.microsoft.com/#home).</span></span> <span data-ttu-id="3d28b-145">Войдите и выберите **Устройства,** а **затем все устройства.**</span><span class="sxs-lookup"><span data-stu-id="3d28b-145">Log in and select  **Devices**  then  **All devices**.</span></span> <span data-ttu-id="3d28b-146">Отсюда можно найти имя&#39;HoloLens.</span><span class="sxs-lookup"><span data-stu-id="3d28b-146">From here, you can search your HoloLens device&#39;s name.</span></span> <span data-ttu-id="3d28b-147">Вы должны иметь возможность видеть ваши HoloLens, перечисленные в Intune.</span><span class="sxs-lookup"><span data-stu-id="3d28b-147">You should be able to see your HoloLens listed on Intune.</span></span>

        ![Проверка управляемого Intune в Azure AD](./images/hololens2-devices-all-devices2.png)


## <a name="wi-fi-certificate-validation"></a><span data-ttu-id="3d28b-149">Wi-Fi проверки сертификата</span><span class="sxs-lookup"><span data-stu-id="3d28b-149">Wi-Fi certificate validation</span></span>

<span data-ttu-id="3d28b-150">К настоящему времени устройство должно было получить сертификат Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="3d28b-150">By now, the device should have received the Wi-Fi certificate.</span></span> <span data-ttu-id="3d28b-151">Простейшая проверка, которую вы можете сделать, это попытка подключиться к подключению Wi-Fi, для которого&#39;получил сертификат.</span><span class="sxs-lookup"><span data-stu-id="3d28b-151">The simplest validation you can do is attempt to connect to the Wi-Fi connection for which you&#39;ve received the certificate.</span></span> <span data-ttu-id="3d28b-152">Откройте приложение **Параметры** и перейдите в **Сетевой &amp; Интернет**  ->  **Wi-Fi** и выберите подключение к Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="3d28b-152">Open up the **Settings** app and navigate to **Network &amp; Internet** -> **Wi-Fi** and select the Wi-fi connection.</span></span> <span data-ttu-id="3d28b-153">После подключения откройте приложение Microsoft Edge и подтвердив, что вы можете перейти на веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="3d28b-153">Once connected, open up the Microsoft Edge app and confirm you can navigate to a website.</span></span>

<span data-ttu-id="3d28b-154">Чтобы подтвердить, что вы получили сертификат на устройстве, можно использовать [диспетчер сертификатов.](https://docs.microsoft.com/hololens/certificate-manager)</span><span class="sxs-lookup"><span data-stu-id="3d28b-154">To confirm that you have received the certificate on the device, you can use the [Certificate Manager](https://docs.microsoft.com/hololens/certificate-manager).</span></span>

## <a name="validate-lob-app-install"></a><span data-ttu-id="3d28b-155">Проверка установки приложения LOB</span><span class="sxs-lookup"><span data-stu-id="3d28b-155">Validate LOB app install</span></span>

<span data-ttu-id="3d28b-156">Чтобы увидеть ход установки управляемого приложения, вы увидите, установлено ли приложение, или проверьте Параметры.</span><span class="sxs-lookup"><span data-stu-id="3d28b-156">To see a managed app's install progress, you either see if the app is installed or check Settings.</span></span> <span data-ttu-id="3d28b-157">Настраивая приложение LOB в качестве необходимой установки для нашей группы, после регистрации HoloLens с пользователем в назначенной группе приложение автоматически загружается в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="3d28b-157">By configuring a LOB app as a required installation for our group, after enrolling the HoloLens with a user in the assigned group, the app will automatically download to the HoloLens.</span></span>

<span data-ttu-id="3d28b-158">Откройте меню Пуск и выберите **все приложения.**</span><span class="sxs-lookup"><span data-stu-id="3d28b-158">Open the Start menu and select **All apps**.</span></span> <span data-ttu-id="3d28b-159">В зависимости от количества приложений, которые у вас \*\*\*\* есть, возможно, потребуется использовать страницу вверх или **страницы вниз** кнопки.</span><span class="sxs-lookup"><span data-stu-id="3d28b-159">Depending on the number of apps you have, you may need to use the **page up** or **page down** buttons.</span></span>

<span data-ttu-id="3d28b-160">Чтобы проверить установку приложения на устройстве, \*\*\*\* вы можете сделать это с помощью работы или учебного доступа к учетным записям параметров; выберите учетную запись, а затем кнопку Info и прокрутите вниз, чтобы просмотреть различные конфигурации и приложения, применяемые к устройству из  ->  \*\*\*\*  ->  \*\*\*\* MDM. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3d28b-160">To validate the installation of the app on device, you can do so via **Settings** -> **Accounts** -> **Access work or school**; select the account then the **Info** button, and scroll down to see different configurations and apps applied to the device from MDM.</span></span>

<span data-ttu-id="3d28b-161">Чтобы проверить установку из Intune, перейдите на портал [MEM](https://endpoint.microsoft.com/#home)Apps -> Все приложения, на странице установки состояния устройства  ->  \*\*\*\* \*\*\*\*  -> *TheNameOfYourApp.*  ->  \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3d28b-161">To validate the install from Intune, navigate to the [MEM portal](https://endpoint.microsoft.com/#home) -> **Apps** -> All **apps** ->*TheNameOfYourApp* -> **Device install status** page.</span></span>

<span data-ttu-id="3d28b-162">Дополнительные. [Развертывание приложений Intune для HoloLens](https://docs.microsoft.com/hololens/app-deploy-intune)</span><span class="sxs-lookup"><span data-stu-id="3d28b-162">See more: [Intune App Deployment for HoloLens](https://docs.microsoft.com/hololens/app-deploy-intune)</span></span>

## <a name="validate-dynamics-365-guides"></a><span data-ttu-id="3d28b-163">Проверка руководства по динамике 365</span><span class="sxs-lookup"><span data-stu-id="3d28b-163">Validate Dynamics 365 Guides</span></span>

<span data-ttu-id="3d28b-164">В HoloLens существуют режимы для приложения Guides, которые являются автором и операционным.</span><span class="sxs-lookup"><span data-stu-id="3d28b-164">There are modes for the Guides app on HoloLens, authoring and operating.</span></span> <span data-ttu-id="3d28b-165">Вам необходимо завершить авторство руководства перед его эксплуатацией.</span><span class="sxs-lookup"><span data-stu-id="3d28b-165">You'll need to finish authoring a guide before operating it.</span></span>

### <a name="authoring-the-guide"></a><span data-ttu-id="3d28b-166">Автор руководства</span><span class="sxs-lookup"><span data-stu-id="3d28b-166">Authoring the Guide</span></span>

<span data-ttu-id="3d28b-167">Нам не нужно делать много для этой быстрой проверки.</span><span class="sxs-lookup"><span data-stu-id="3d28b-167">We don't need to do much for this quick validation.</span></span> <span data-ttu-id="3d28b-168">Просто выберите руководство, подготовленную на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3d28b-168">Simply select the guide you prepared on your PC.</span></span> <span data-ttu-id="3d28b-169">Вам потребуется закрепить [руководство,](https://docs.microsoft.comdynamics365/mixed-reality/guides/hololens-app-anchor)для быстрой проверки можно использовать голографический якорь.</span><span class="sxs-lookup"><span data-stu-id="3d28b-169">You'll need to [anchor the guide](https://docs.microsoft.comdynamics365/mixed-reality/guides/hololens-app-anchor), for a quick validation you can use a holographic anchor.</span></span> <span data-ttu-id="3d28b-170">После этого необходимо разместить [шаги и модели.](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-orientation)</span><span class="sxs-lookup"><span data-stu-id="3d28b-170">Afterwards, you should [place your steps and models](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-orientation).</span></span>

>[!NOTE]
> <span data-ttu-id="3d28b-171">Вам потребуется роль **автора** для входа на компьютер и автора на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="3d28b-171">You will need the **Authoring** role to login to the PC and author on the HoloLens.</span></span> <span data-ttu-id="3d28b-172">Роль оператора является доступной только для чтения и не имеет доступа к приложению для ПК.</span><span class="sxs-lookup"><span data-stu-id="3d28b-172">The Operator role is read-only and has no access to the PC app.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/poE7s7_zWDE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### <a name="operating-the-guide"></a><span data-ttu-id="3d28b-173">Эксплуатация руководства</span><span class="sxs-lookup"><span data-stu-id="3d28b-173">Operating the Guide</span></span>

<span data-ttu-id="3d28b-174">После того как голограммы будут на месте, вы сможете проверить работу руководства.</span><span class="sxs-lookup"><span data-stu-id="3d28b-174">Once your holograms are in place, you can test out operating your guide.</span></span> 
- <span data-ttu-id="3d28b-175">Выбор **режима Оператора**</span><span class="sxs-lookup"><span data-stu-id="3d28b-175">Select **Operator mode**</span></span>
- <span data-ttu-id="3d28b-176">Щелкните по шагам руководства.</span><span class="sxs-lookup"><span data-stu-id="3d28b-176">Click through the steps of your guide.</span></span>

<span data-ttu-id="3d28b-177">Дополнительные рекомендации по работе с руководством можно найти в этих ресурсах:</span><span class="sxs-lookup"><span data-stu-id="3d28b-177">For more in-depth guidance on how to operate a guide, check out these resources:</span></span>

[<span data-ttu-id="3d28b-178">Обзор работы руководства в Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="3d28b-178">Overview of operating a guide in Dynamics 365 Guides</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/operator-overview)

[<span data-ttu-id="3d28b-179">Ориентируйся с помощью карточки Step в качестве оператора в руководстве Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3d28b-179">Get oriented with the Step card as an operator in Dynamics 365 Guides</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/operator-step-card-orientation)

<iframe width="560" height="315" src="https://www.youtube.com/embed/9s41BKGHVL8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <a name="next-step"></a><span data-ttu-id="3d28b-180">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="3d28b-180">Next step</span></span> 
> [!div class="nextstepaction"]
> [<span data-ttu-id="3d28b-181">Развертывание подключенных к корпоративной связи — обслуживание</span><span class="sxs-lookup"><span data-stu-id="3d28b-181">Corporate connected deployment - Maintain</span></span>](hololens2-corp-connected-maintain.md)
