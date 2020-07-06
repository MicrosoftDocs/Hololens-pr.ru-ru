---
title: Руководство по оценке Windows Autopilot для HoloLens 2
description: ''
author: Teresa-Motiv
ms.author: v-tea
ms.date: 4/10/2020
ms.prod: hololens
ms.topic: article
ms.custom:
- CI 116283
- CSSTroubleshooting
audience: ITPro
ms.localizationpriority: high
keywords: autopilot
manager: jarrettr
appliesto:
- HoloLens 2
ms.openlocfilehash: 3d98e67e79ae10b606c529adbda95dbb61b8fd15
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10829441"
---
# <span data-ttu-id="e704a-103">Руководство по оценке Windows Autopilot для HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="e704a-103">Windows Autopilot for HoloLens 2 evaluation guide</span></span>

<span data-ttu-id="e704a-104">Когда вы настраиваете устройства HoloLens 2 для программы Windows Autopilot, пользователи могут выполнить простую процедуру подготовки устройств из облака.</span><span class="sxs-lookup"><span data-stu-id="e704a-104">When you set up HoloLens 2 devices for the Windows Autopilot program, your users can follow a simple process to provision the devices from the cloud.</span></span>

<span data-ttu-id="e704a-105">Эта программа Autopilot поддерживает режим саморазвертывания Autopilot для подготовки устройств HoloLens 2 как общих устройств в рамках вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="e704a-105">This Autopilot program supports Autopilot self-deploying mode to provision HoloLens 2 devices as shared devices under your tenant.</span></span> <span data-ttu-id="e704a-106">Режим саморазвертывания использует предварительно установленный образ и драйверы OEM устройства в процессе подготовки.</span><span class="sxs-lookup"><span data-stu-id="e704a-106">Self-deploying mode leverages the device's preinstalled OEM image and drivers during the provisioning process.</span></span> <span data-ttu-id="e704a-107">Пользователь может подготовить устройство, не надевая его и не используя интерфейс первого запуска (OOBE).</span><span class="sxs-lookup"><span data-stu-id="e704a-107">A user can provision the device without putting the device on and going through the Out-of-the-box Experience (OOBE).</span></span>  

![Процесс саморазвертывания Autopilot автоматически настраивает общие устройства в режиме "без монитора" с помощью сетевого подключения.](./images/hololens-ap-intro.png)

<span data-ttu-id="e704a-109">Когда пользователь запускает саморазвертывание Autopilot, этот процесс выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e704a-109">When a user starts the Autopilot self-deploying process, the process completes the following steps:</span></span>

1. <span data-ttu-id="e704a-110">Присоединение устройства к Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e704a-110">Join the device to Azure Active Directory (Azure AD).</span></span>
   > [!NOTE]  
   > <span data-ttu-id="e704a-111">Autopilot для HoloLens не поддерживает присоединение к Active Directory или гибридное присоединение к Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e704a-111">Autopilot for HoloLens does not support Active Directory join or Hybrid Azure AD join.</span></span>
1. <span data-ttu-id="e704a-112">Регистрация устройства в Microsoft Intune (или другой службе MDM) с помощью Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e704a-112">Use Azure AD to enroll the device in Microsoft Intune (or another MDM service).</span></span>
1. <span data-ttu-id="e704a-113">Скачивание политик для устройств, приложений для пользователей, сертификатов и сетевых профилей.</span><span class="sxs-lookup"><span data-stu-id="e704a-113">Download the device-targeted policies, user-targeted apps, certificates, and networking profiles.</span></span>
1. <span data-ttu-id="e704a-114">Подготовка устройства.</span><span class="sxs-lookup"><span data-stu-id="e704a-114">Provision the device.</span></span>
1. <span data-ttu-id="e704a-115">Демонстрация экрана входа пользователю.</span><span class="sxs-lookup"><span data-stu-id="e704a-115">Present the sign-in screen to the user.</span></span>

## <span data-ttu-id="e704a-116">Windows Autopilot для HoloLens 2: начало работы</span><span class="sxs-lookup"><span data-stu-id="e704a-116">Windows Autopilot for HoloLens 2: Get started</span></span>

<span data-ttu-id="e704a-117">Следующие действия обобщают процесс настройки вашей среды Windows Autopilot для HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="e704a-117">The following steps summarize the process of setting up your environment for the Windows Autopilot for HoloLens 2.</span></span> <span data-ttu-id="e704a-118">В оставшейся части этого раздела приведены подробные сведения об этих действиях.</span><span class="sxs-lookup"><span data-stu-id="e704a-118">The rest of this section provides the details of these steps.</span></span>

1. <span data-ttu-id="e704a-119">Проверка соответствия требованиям Windows Autopilot для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e704a-119">Make sure that you meet the requirements for Windows Autopilot for HoloLens.</span></span>
1. <span data-ttu-id="e704a-120">Регистрация в программе Windows Autopilot для HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="e704a-120">Enroll in the Windows Autopilot for HoloLens 2 program.</span></span>
1. <span data-ttu-id="e704a-121">Проверка участия клиента в тестировании (зарегистрирован для участия в программе).</span><span class="sxs-lookup"><span data-stu-id="e704a-121">Verify that your tenant is flighted (enrolled to participate in the program).</span></span>
1. <span data-ttu-id="e704a-122">Регистрация устройств в Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="e704a-122">Register devices in Windows Autopilot.</span></span>
1. <span data-ttu-id="e704a-123">Создание группы устройств.</span><span class="sxs-lookup"><span data-stu-id="e704a-123">Create a device group.</span></span>
1. <span data-ttu-id="e704a-124">Создание профиля развертывания.</span><span class="sxs-lookup"><span data-stu-id="e704a-124">Create a deployment profile.</span></span>
1. <span data-ttu-id="e704a-125">Проверка конфигурации ESP.</span><span class="sxs-lookup"><span data-stu-id="e704a-125">Verify the ESP configuration.</span></span>
1. <span data-ttu-id="e704a-126">Настройка собственного профиля конфигурации для устройств HoloLens (известная проблема).</span><span class="sxs-lookup"><span data-stu-id="e704a-126">Configure a custom configuration profile for HoloLens devices (known issue).</span></span>
1. <span data-ttu-id="e704a-127">Проверка состояния профиля устройств HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e704a-127">Verify the profile status of the HoloLens devices.</span></span>

### <span data-ttu-id="e704a-128">1. Проверка соответствия требованиям Windows Autopilot для HoloLens</span><span class="sxs-lookup"><span data-stu-id="e704a-128">1. Make sure that you meet the requirements for Windows Autopilot for HoloLens</span></span>
<span data-ttu-id="e704a-129">Актуальные сведения об участии в программе см. в разделе [Заметки о выпуске для программы предварительной оценки Windows](hololens-insider.md#windows-insider-release-notes).</span><span class="sxs-lookup"><span data-stu-id="e704a-129">For the latest information about how to participate in the program, review [Windows Insider Release Notes](hololens-insider.md#windows-insider-release-notes).</span></span>

<span data-ttu-id="e704a-130">Ознакомьтесь со следующими разделами статьи требований Windows Autopilot:</span><span class="sxs-lookup"><span data-stu-id="e704a-130">Review the following sections of the Windows Autopilot requirements article:</span></span>

- [<span data-ttu-id="e704a-131">Сетевые требования</span><span class="sxs-lookup"><span data-stu-id="e704a-131">Network requirements</span></span>](https://docs.microsoft.com/windows/deployment/windows-autopilot/windows-autopilot-requirements#networking-requirements)  
- [<span data-ttu-id="e704a-132">Требования к лицензированию</span><span class="sxs-lookup"><span data-stu-id="e704a-132">Licensing requirements</span></span>](https://docs.microsoft.com/windows/deployment/windows-autopilot/windows-autopilot-requirements#licensing-requirements)  
- [<span data-ttu-id="e704a-133">Требования к конфигурации</span><span class="sxs-lookup"><span data-stu-id="e704a-133">Configuration requirements</span></span>](https://docs.microsoft.com/windows/deployment/windows-autopilot/windows-autopilot-requirements#configuration-requirements)
> [!IMPORTANT]  
> <span data-ttu-id="e704a-134">Windows Autopilot для HoloLens 2 содержит конкретные требования к операционной системе, в отличие от других программ Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="e704a-134">Unlike other Windows Autopilot programs, Windows Autopilot for HoloLens 2 has specific operating system requirements.</span></span>

<span data-ttu-id="e704a-135">Ознакомьтесь с разделом "[Требования](https://docs.microsoft.com/windows/deployment/windows-autopilot/self-deploying#requirements)" статьи о режиме саморазвертывания Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="e704a-135">Review the "[Requirements](https://docs.microsoft.com/windows/deployment/windows-autopilot/self-deploying#requirements)" section of the Windows Autopilot Self-Deploying mode article.</span></span> <span data-ttu-id="e704a-136">Ваша среда должна соответствовать этим требованиям и стандартным требованиям Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="e704a-136">Your environment has to meet these requirements as well as the standard Windows Autopilot requirements.</span></span>

> [!NOTE]  
> <span data-ttu-id="e704a-137">Вам не требуется проверять в статье разделы "Пошаговое руководство" и "Проверка".</span><span class="sxs-lookup"><span data-stu-id="e704a-137">You do not have to review the "Step by step" and "Validation" sections of the article.</span></span> <span data-ttu-id="e704a-138">Описанные ниже в этой статье процедуры содержат соответствующие действия для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e704a-138">The procedures later in this article provide corresponding steps that are specific to HoloLens.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="e704a-139">Сведения о том, как зарегистрировать устройства и настроить профили, см. в разделах [4. Регистрация устройств в Windows Autopilot](#4-register-devices-in-windows-autopilot) и [6. Создание профиля развертывания](#6-create-a-deployment-profile) этой статьи.</span><span class="sxs-lookup"><span data-stu-id="e704a-139">For information about how to register devices and configure profiles, see [4. Register devices in Windows Autopilot](#4-register-devices-in-windows-autopilot) and [6. Create a deployment profile](#6-create-a-deployment-profile) in this article.</span></span> <span data-ttu-id="e704a-140">В этих разделах приведены инструкции для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e704a-140">These sections provide steps that are specific to HoloLens.</span></span>

<span data-ttu-id="e704a-141">Перед первым запуском и подготовкой убедитесь, что устройства HoloLens соответствуют следующим требованиям:</span><span class="sxs-lookup"><span data-stu-id="e704a-141">Before you start the OOBE and provisioning process, make sure that the HoloLens devices meet the following requirements:</span></span>

- <span data-ttu-id="e704a-142">Устройства еще не являются участниками Azure AD и не зарегистрированы в Intune (или другой системе MDM).</span><span class="sxs-lookup"><span data-stu-id="e704a-142">The devices are not already members of Azure AD, and are not enrolled in Intune (or another MDM system).</span></span> <span data-ttu-id="e704a-143">Эти действия выполняют при саморазвертывании Autopilot.</span><span class="sxs-lookup"><span data-stu-id="e704a-143">The Autopilot self-deploying process completes these steps.</span></span> <span data-ttu-id="e704a-144">Чтобы убедиться, что очищена вся информация, связанная с устройством, проверьте страницы **Устройства** в Azure AD и Intune.</span><span class="sxs-lookup"><span data-stu-id="e704a-144">To make sure that all the device-related information is cleaned up, check the **Devices** pages in both Azure AD and Intune.</span></span>
- <span data-ttu-id="e704a-145">Каждое устройство может подключаться к Интернету.</span><span class="sxs-lookup"><span data-stu-id="e704a-145">Every device can connect to the internet.</span></span> <span data-ttu-id="e704a-146">Вы можете использовать переходники “USB C на Ethernet” для подключения к проводному Интернету или переходники “USB C на Wifi” для подключения к беспроводному Интернету.</span><span class="sxs-lookup"><span data-stu-id="e704a-146">You can use "USB C to Ethernet" adapters for wired internet connectivity or "USB C to Wifi" adapters for wireless internet connectivity.</span></span> 
- <span data-ttu-id="e704a-147">Каждое устройство может подключаться к компьютеру с помощью кабеля USB-C, а на этом компьютере установлена программа [Advanced Recovery Companion (ARC)](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?rtc=1&activetab=pivot:overviewtab)</span><span class="sxs-lookup"><span data-stu-id="e704a-147">Every device can connect to a computer by using a USB-C cable, and that computer has [Advanced Recovery Companion (ARC)](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?rtc=1&activetab=pivot:overviewtab) installed</span></span>
- <span data-ttu-id="e704a-148">Каждое устройство имеет последнее обновление Windows: Windows 10 версии 19041.1002.200107-0909 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="e704a-148">Every device has the latest Windows update: Windows 10, version 19041.1002.200107-0909 or a later version.</span></span>

<span data-ttu-id="e704a-149">Чтобы настроить профили режима саморазвертывания Autopilot и управлять ими, убедитесь, что у вас есть доступ к [Центру администрирования Microsoft Endpoint Manager](https://endpoint.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e704a-149">To configure and manage the Autopilot self-deploying mode profiles, make sure that you have access to [Microsoft Endpoint Manager admin center](https://endpoint.microsoft.com).</span></span>

### <span data-ttu-id="e704a-150">2. Регистрация в программе Windows Autopilot для HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="e704a-150">2. Enroll in the Windows Autopilot for HoloLens 2 program</span></span>

<span data-ttu-id="e704a-151">Чтобы принять участие в программе, вы должны использовать клиент, тестируемый для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e704a-151">To participate in the program, you have to use a tenant that is flighted for HoloLens.</span></span> <span data-ttu-id="e704a-152">Для этого выберите [запрос приватной предварительной версии Windows Autopilot для HoloLens](https://aka.ms/APHoloLensTAP) или используйте следующий QR-код для отправки запроса.</span><span class="sxs-lookup"><span data-stu-id="e704a-152">To do this, go to  [Windows Autopilot for HoloLens Private Preview request](https://aka.ms/APHoloLensTAP) or use the following QR code to submit a request.</span></span>  

![QR-код Autopilot](./images/hololens-ap-qrcode.png)  

<span data-ttu-id="e704a-154">В этом запросе укажите следующие данные:</span><span class="sxs-lookup"><span data-stu-id="e704a-154">In this request, provide the following information:</span></span>

- <span data-ttu-id="e704a-155">Домен клиента</span><span class="sxs-lookup"><span data-stu-id="e704a-155">Tenant domain</span></span>
- <span data-ttu-id="e704a-156">Идентификатор клиента</span><span class="sxs-lookup"><span data-stu-id="e704a-156">Tenant ID</span></span>
- <span data-ttu-id="e704a-157">Количество устройств HoloLens 2, участвующих в оценке</span><span class="sxs-lookup"><span data-stu-id="e704a-157">Number of HoloLens 2 devices that are participating in this evaluation</span></span>
- <span data-ttu-id="e704a-158">Количество устройств HoloLens 2, которые планируется развернуть с помощью режима саморазвертывания Autopilot</span><span class="sxs-lookup"><span data-stu-id="e704a-158">Number of HoloLens 2 devices that you plan to deploy by using Autopilot self-deploying mode</span></span>

### <span data-ttu-id="e704a-159">3. Проверка участия клиента в тестировании</span><span class="sxs-lookup"><span data-stu-id="e704a-159">3. Verify that your tenant is flighted</span></span>

<span data-ttu-id="e704a-160">Чтобы проверить участие в тестировании для программы Autopilot после отправки запроса, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e704a-160">To verify that your tenant is flighted for the Autopilot program after you submit your request, follow these steps:</span></span>

1. <span data-ttu-id="e704a-161">Войдите в [Центр администрирования Microsoft Endpoint Manager](https://endpoint.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e704a-161">Sign in to [Microsoft Endpoint Manager admin center](https://endpoint.microsoft.com).</span></span>
1. <span data-ttu-id="e704a-162">Выберите **Устройства** > **Windows** > **Регистрация Windows** > **Профили развертывания Windows Autopilot** > **Создать профиль**.</span><span class="sxs-lookup"><span data-stu-id="e704a-162">Select **Devices** > **Windows** > **Windows enrollment** > **Windows Autopilot deployment profiles** > **Create profile**.</span></span>  
   
   ![Раскрывающийся список создания профиля содержит элемент HoloLens.](./images/hololens-ap-enrollment-profiles.png)
  <span data-ttu-id="e704a-164">Вы увидите список, включающий **HoloLens**.</span><span class="sxs-lookup"><span data-stu-id="e704a-164">You should see a list that includes **HoloLens**.</span></span> <span data-ttu-id="e704a-165">Если этот параметр не отображается, свяжитесь с нами с помощью одного из параметров [обратной связи](#feedback).</span><span class="sxs-lookup"><span data-stu-id="e704a-165">If this option is not present, use one of the [Feedback](#feedback) options to contact us.</span></span>

### <span data-ttu-id="e704a-166">4. Регистрация устройств в Windows Autopilot</span><span class="sxs-lookup"><span data-stu-id="e704a-166">4. Register devices in Windows Autopilot</span></span>

<span data-ttu-id="e704a-167">Чтобы зарегистрировать устройство HoloLens в программе Windows Autopilot, вам требуется получить аппаратный хэш устройства (другое название — идентификатор оборудования).</span><span class="sxs-lookup"><span data-stu-id="e704a-167">To register a HoloLens device in the Windows Autopilot program, you have to obtain the hardware hash of the device (also known as the hardware ID).</span></span> <span data-ttu-id="e704a-168">Устройство может записывать свой аппаратный хэш в CSV-файл при первом запуске или позже, когда владелец устройства запускает процесс сбора журнала диагностики (описано в следующей процедуре).</span><span class="sxs-lookup"><span data-stu-id="e704a-168">The device can record its hardware hash in a CSV file during the OOBE process, or later when a device owner starts the diagnostic log collection process (described in the following procedure).</span></span> <span data-ttu-id="e704a-169">Как правило, владелец устройства является первым пользователем, входящим в устройство.</span><span class="sxs-lookup"><span data-stu-id="e704a-169">Typically, the device owner is the first user to sign in to the device.</span></span>

**<span data-ttu-id="e704a-170">Извлечение аппаратного хэша устройства</span><span class="sxs-lookup"><span data-stu-id="e704a-170">Retrieve a device hardware hash</span></span>**

1. <span data-ttu-id="e704a-171">Запустите устройство HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="e704a-171">Start the HoloLens 2 device.</span></span>
1. <span data-ttu-id="e704a-172">На устройстве одновременно нажмите кнопки включения и уменьшения звука, а затем отпустите их.</span><span class="sxs-lookup"><span data-stu-id="e704a-172">On the device, press the Power and Volume Down buttons at the same time and then release them.</span></span> <span data-ttu-id="e704a-173">Устройство собирает журналы диагностики и аппаратный хэш и хранит их в наборе ZIP-файлов.</span><span class="sxs-lookup"><span data-stu-id="e704a-173">The device collects diagnostic logs and the hardware hash, and stores them in a set of .zip files.</span></span>
1. <span data-ttu-id="e704a-174">Подключите устройство к компьютеру с помощью кабеля USB-C.</span><span class="sxs-lookup"><span data-stu-id="e704a-174">Use a USB-C cable to connect the device to a computer.</span></span>
1. <span data-ttu-id="e704a-175">На компьютере откройте проводник.</span><span class="sxs-lookup"><span data-stu-id="e704a-175">On the computer, open File Explorer.</span></span> <span data-ttu-id="e704a-176">Откройте **Этот компьютер\\\<*HoloLens device name*>\\Внутреннее хранилище\\Документы** и найдите файл AutopilotDiagnostics.zip.</span><span class="sxs-lookup"><span data-stu-id="e704a-176">Open **This PC\\\<*HoloLens device name*>\\Internal Storage\\Documents**, and locate the AutopilotDiagnostics.zip file.</span></span>  

   > [!NOTE]  
   > <span data-ttu-id="e704a-177">ZIP-файл может быть недоступен сразу.</span><span class="sxs-lookup"><span data-stu-id="e704a-177">The .zip file may not immediately be available.</span></span> <span data-ttu-id="e704a-178">Если файл еще не готов, в папке "Документы" может присутствовать файл HoloLensDiagnostics.temp.</span><span class="sxs-lookup"><span data-stu-id="e704a-178">If the file is not ready yet you may see a HoloLensDiagnostics.temp file in the Documents folder.</span></span> <span data-ttu-id="e704a-179">Чтобы обновить список файлов, обновите окно.</span><span class="sxs-lookup"><span data-stu-id="e704a-179">To update the list of files, refresh the window.</span></span>

1. <span data-ttu-id="e704a-180">Извлеките содержимое файла AutopilotDiagnostics.zip.</span><span class="sxs-lookup"><span data-stu-id="e704a-180">Extract the contents of the AutopilotDiagnostics.zip file.</span></span>
1. <span data-ttu-id="e704a-181">В извлеченных файлах найдите CSV-файл с префиксом DeviceHash в имени файла.</span><span class="sxs-lookup"><span data-stu-id="e704a-181">In the extracted files, locate the CSV file that has a file name prefix of "DeviceHash."</span></span> <span data-ttu-id="e704a-182">Скопируйте этот файл на диск компьютера, где вы сможете получить к нему доступ позже.</span><span class="sxs-lookup"><span data-stu-id="e704a-182">Copy that file to a drive on the computer where you can access it later.</span></span>  
   > [!IMPORTANT]  
   > <span data-ttu-id="e704a-183">Данные в CSV-файле должны использовать следующий формат заголовка и строки:</span><span class="sxs-lookup"><span data-stu-id="e704a-183">The data in the CSV file should use the following header and line format:</span></span>
   > ```
   > Device Serial Number,Windows Product ID,Hardware Hash,Group Tag,Assigned User <serialNumber>,<ProductID>,<hardwareHash>,<optionalGroupTag>,<optionalAssignedUser>
   >```

**<span data-ttu-id="e704a-184">Регистрация устройства в Windows Autopilot</span><span class="sxs-lookup"><span data-stu-id="e704a-184">Register the device in Windows Autopilot</span></span>**

1. <span data-ttu-id="e704a-185">В Центре администрирования Microsoft Endpoint Manager откройте **Устройства** > **Windows** > **Регистрация Windows** и выберите **Устройства** > **Импорт** в разделе **Программа Windows Autopilot Deployment**.</span><span class="sxs-lookup"><span data-stu-id="e704a-185">In Microsoft Endpoint Manager Admin Center, select **Devices** > **Windows** > **Windows enrollment**, and then select **Devices** > **Import** under **Windows Autopilot Deployment Program**.</span></span>

1. <span data-ttu-id="e704a-186">В разделе **Добавление устройств Windows Autopilot** выберите CSV-файл DeviceHash, нажмите **Открыть** и выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="e704a-186">Under **Add Windows Autopilot devices**, select the DeviceHash CSV file, select **Open**, and then select **Import**.</span></span>  
   
   ![Импорт аппаратного хэша с помощью команды импорта.](./images/hololens-ap-hash-import.png)
1. <span data-ttu-id="e704a-188">После завершения импорта выберите **Устройства** > **Windows** > **Регистрация Windows** > **Устройства** > **Синхронизация**. Завершение процесса может занять несколько минут в зависимости от количества синхронизируемых устройств.</span><span class="sxs-lookup"><span data-stu-id="e704a-188">After the import finishes, select **Devices** > **Windows** > **Windows enrollment** > **Devices** > **Sync**. The process might take a few minutes to complete, depending on how many devices are being synchronized.</span></span> <span data-ttu-id="e704a-189">Чтобы просмотреть зарегистрированное устройство, нажмите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="e704a-189">To see the registered device, select **Refresh**.</span></span>  
   
   ![Просмотр списка устройств с помощью команд синхронизации и обновления.](./images/hololens-ap-devices-sync.png)  

### <span data-ttu-id="e704a-191">5. Создание группы устройств</span><span class="sxs-lookup"><span data-stu-id="e704a-191">5. Create a device group</span></span>

1. <span data-ttu-id="e704a-192">В Центре администрирования Microsoft Endpoint Manager выберите **Группы** > **Создать группу**.</span><span class="sxs-lookup"><span data-stu-id="e704a-192">In Microsoft Endpoint Manager admin center, select **Groups** > **New group**.</span></span>
1. <span data-ttu-id="e704a-193">Для параметра **Тип группы** выберите **Группа безопасности** и введите имя группы с описанием.</span><span class="sxs-lookup"><span data-stu-id="e704a-193">For **Group type**, select **Security**, and then enter a group name and description.</span></span>
1. <span data-ttu-id="e704a-194">Для параметра **Тип членства** выберите **Назначенное** или **Динамическое устройство**.</span><span class="sxs-lookup"><span data-stu-id="e704a-194">For **Membership type**, select either **Assigned** or **Dynamic Device**.</span></span>
1. <span data-ttu-id="e704a-195">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="e704a-195">Do one of the following:</span></span>  
   
   - <span data-ttu-id="e704a-196">Если на предыдущем шаге вы выбрали **Назначенное** для параметра **Тип членства**, нажмите **Члены** и добавьте устройства Autopilot в группу.</span><span class="sxs-lookup"><span data-stu-id="e704a-196">If you selected **Assigned** for **Membership type** in the previous step, select **Members**, and then add Autopilot devices to the group.</span></span> <span data-ttu-id="e704a-197">Устройства Autopilot, которые еще не зарегистрированы, указаны с помощью серийного номера устройства в качестве его имени.</span><span class="sxs-lookup"><span data-stu-id="e704a-197">Autopilot devices that aren't yet enrolled are listed by using the device serial number as the device name.</span></span>
   - <span data-ttu-id="e704a-198">Если на предыдущем шаге вы выбрали **Динамическое устройство** для параметра **Тип членства**, нажмите **Динамические члены устройства** и введите код для **расширенного правила**, который выглядит примерно так:</span><span class="sxs-lookup"><span data-stu-id="e704a-198">If you selected **Dynamic Devices** for **Membership type** in the previous step, select **Dynamic device members**, and then enter code in **Advanced rule** that resembles the following:</span></span>
     - <span data-ttu-id="e704a-199">Если вы хотите создать группу, включающую все устройства Autopilot, введите:</span><span class="sxs-lookup"><span data-stu-id="e704a-199">If you want to create a group that includes all of your Autopilot devices, type:</span></span> `(device.devicePhysicalIDs -any _ -contains "[ZTDId]")`
     - <span data-ttu-id="e704a-200">Поле тега группы Intune сопоставляется с атрибутом **OrderID** на устройствах Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e704a-200">Intune's group tag field maps to the **OrderID** attribute on Azure AD devices.</span></span> <span data-ttu-id="e704a-201">Если вы хотите создать группу, включающую все устройства Autopilot с определенным тегом группы (OrderID устройства Azure AD), требуется ввести:</span><span class="sxs-lookup"><span data-stu-id="e704a-201">If you want to create a group that includes all of your Autopilot devices that have a specific group tag (the Azure AD device OrderID), you must type:</span></span> `(device.devicePhysicalIds -any _ -eq "[OrderID]:179887111881")`
     - <span data-ttu-id="e704a-202">Если вы хотите создать группу, включающую все устройства Autopilot с определенным идентификатором заказа на покупку, введите:</span><span class="sxs-lookup"><span data-stu-id="e704a-202">If you want to create a group that includes all your Autopilot devices that have a specific Purchase Order ID, type:</span></span> `(device.devicePhysicalIds -any _ -eq "[PurchaseOrderId]:76222342342")`

     > [!NOTE]  
     > <span data-ttu-id="e704a-203">Эти правила предназначены для атрибутов, являющихся уникальными для устройств Autopilot.</span><span class="sxs-lookup"><span data-stu-id="e704a-203">These rules target attributes that are unique to Autopilot devices.</span></span>
1. <span data-ttu-id="e704a-204">Нажмите **Сохранить**, а затем — **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e704a-204">Select **Save**, and then select **Create**.</span></span>

### <span data-ttu-id="e704a-205">6. Создание профиля развертывания</span><span class="sxs-lookup"><span data-stu-id="e704a-205">6. Create a deployment profile</span></span>

1. <span data-ttu-id="e704a-206">В Центре администрирования Microsoft Endpoint Manager выберите **Устройства** > **Windows** > **Регистрация Windows** > **Профили развертывания Windows Autopilot** > **Создать профиль** > **HoloLens**.</span><span class="sxs-lookup"><span data-stu-id="e704a-206">In Microsoft Endpoint Manager admin center, select **Devices** > **Windows** > **Windows enrollment** > **Windows Autopilot deployment profiles** > **Create profile** > **HoloLens**.</span></span>
1. <span data-ttu-id="e704a-207">Введите имя профиля и описание, а затем нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e704a-207">Enter a profile name and description, and then select **Next**.</span></span>  
   
   ![Добавление имени профиля и описания](./images/hololens-ap-profile-name.png)
1. <span data-ttu-id="e704a-209">На странице **Запуск при первом включении (OOBE)** большинство параметров заранее настроены, чтобы упростить OOBE для этой оценки.</span><span class="sxs-lookup"><span data-stu-id="e704a-209">On the **Out-of-box experience (OOBE)** page, most of the settings are pre-configured to streamline OOBE for this evaluation.</span></span> <span data-ttu-id="e704a-210">При желании вы можете настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="e704a-210">Optionally, you can configure the following settings:</span></span>  

   - <span data-ttu-id="e704a-211">**Язык (регион)**. Выберите язык для OOBE.</span><span class="sxs-lookup"><span data-stu-id="e704a-211">**Language (Region)**: Select the language for OOBE.</span></span> <span data-ttu-id="e704a-212">Рекомендуется выбрать язык из списка [поддерживаемых языков для HoloLens 2](hololens2-language-support.md).</span><span class="sxs-lookup"><span data-stu-id="e704a-212">We recommend that you select a language from the list of [supported languages for HoloLens 2](hololens2-language-support.md).</span></span>
   - <span data-ttu-id="e704a-213">**Автоматическая настройка клавиатуры**. Чтобы обеспечить соответствие клавиатуры выбранному языку, щелкните **Да**.</span><span class="sxs-lookup"><span data-stu-id="e704a-213">**Automatically configure keyboard**: To make sure that the keyboard matches the selected language, select **Yes**.</span></span>
   - <span data-ttu-id="e704a-214">**Применить шаблон имени устройства**. Чтобы автоматически настроить имя устройства при OOBE, выберите **Да** и введите фразу и заполнители шаблона в поле **Введите имя**. Например, введите префикс и `%RAND:4%`&mdash; заполнитель для четырехзначного случайного номера.</span><span class="sxs-lookup"><span data-stu-id="e704a-214">**Apply device name template**: To automatically set the device name during OOBE, select **Yes** and then enter the template phrase and placeholders in **Enter a name** For example, enter a prefix and `%RAND:4%`&mdash;a placeholder for a four-digit random number.</span></span>
     > [!NOTE]  
     > <span data-ttu-id="e704a-215">Если вы используете шаблон имени устройства, процесс OOBE дополнительно перезапустит устройство после применения имени устройства и до присоединения устройства к Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e704a-215">If you use a device name template, the OOBE process restarts the device one additional time after it applies the device name and before it joins the device to Azure AD.</span></span> <span data-ttu-id="e704a-216">Этот перезапуск позволяет применить новое имя.</span><span class="sxs-lookup"><span data-stu-id="e704a-216">This restart enables the new name to take effect.</span></span>  

   ![Настройка параметров OOBE](./images/hololens-ap-profile-oobe.png)
1. <span data-ttu-id="e704a-218">После настройки параметров нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e704a-218">After you configure the settings, select **Next**.</span></span>
1. <span data-ttu-id="e704a-219">На странице **Теги области** при желании добавьте теги областей, которые нужно применить к этому профилю.</span><span class="sxs-lookup"><span data-stu-id="e704a-219">On the **Scope tags** page, optionally add the scope tags that you want to apply to this profile.</span></span> <span data-ttu-id="e704a-220">Дополнительные сведения о тегах областей см. в статье [Использование тегов областей и управления доступом на основе ролей для распределенных ИТ](https://docs.microsoft.com/mem/intune/fundamentals/scope-tags.md).</span><span class="sxs-lookup"><span data-stu-id="e704a-220">For more information about scope tags, see [Use role-based access control and scope tags for distributed IT](https://docs.microsoft.com/mem/intune/fundamentals/scope-tags.md).</span></span> <span data-ttu-id="e704a-221">По завершении нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e704a-221">When finished, select **Next**.</span></span>
1. <span data-ttu-id="e704a-222">На странице **Назначения** установите **Выбранные группы** для параметра **Назначить для**.</span><span class="sxs-lookup"><span data-stu-id="e704a-222">On the **Assignments** page, select **Selected groups** for **Assign to**.</span></span>
1. <span data-ttu-id="e704a-223">В разделе **ВЫБРАННЫЕ ГРУППЫ** нажмите **+ Выбрать группы для включения**.</span><span class="sxs-lookup"><span data-stu-id="e704a-223">Under **SELECTED GROUPS**, select **+ Select groups to include**.</span></span>
1. <span data-ttu-id="e704a-224">В списке **Выбор групп для включения** выберите группу устройств, созданную для устройств Autopilot HoloLens и нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e704a-224">In the **Select groups to include** list, select the device group that you created for the Autopilot HoloLens devices, and then select **Next**.</span></span>  
  
   <span data-ttu-id="e704a-225">Если вы хотите исключить группы, нажмите **Выбрать группы для исключения** и выберите группы, которые нужно исключить.</span><span class="sxs-lookup"><span data-stu-id="e704a-225">If you want to exclude any groups, select **Select groups to exclude**, and select the groups that you want to exclude.</span></span>

   ![Назначение группы устройств для профиля.](./images/hololens-ap-profile-assign-devicegroup.png)
1. <span data-ttu-id="e704a-227">На странице **Проверка и создание** проверьте параметры и нажмите **Создать** для создания профиля.</span><span class="sxs-lookup"><span data-stu-id="e704a-227">On the **Review + Create** page, review the settings and then select **Create** to create the profile.</span></span>  
   
   ![Проверка и создание](./images/hololens-ap-profile-summ.png)

### <span data-ttu-id="e704a-229">7. Проверка конфигурации ESP</span><span class="sxs-lookup"><span data-stu-id="e704a-229">7. Verify the ESP configuration</span></span>

<span data-ttu-id="e704a-230">Страница состояния регистрации (ESP) отображает состояние завершенного процесса настройки устройства, выполняемого при первом входе в устройство пользователя, управляемого MDM.</span><span class="sxs-lookup"><span data-stu-id="e704a-230">The Enrollment Status Page (ESP) displays the status of the complete device configuration process that runs when an MDM managed user signs into a device for the first time.</span></span> <span data-ttu-id="e704a-231">Убедитесь, что ваша конфигурация ESP выглядит примерно следующим образом, и проверьте правильность назначений.</span><span class="sxs-lookup"><span data-stu-id="e704a-231">Make sure that your ESP configuration resembles the following, and verify that the assignments are correct.</span></span>  

![Конфигурация ESP](./images/hololens-ap-profile-settings.png)

### <span data-ttu-id="e704a-233">8. Проверка состояния профиля устройств HoloLens</span><span class="sxs-lookup"><span data-stu-id="e704a-233">8. Verify the profile status of the HoloLens devices</span></span>

1. <span data-ttu-id="e704a-234">В Центре администрирования Microsoft Endpoint Manager выберите **Устройства** > **Windows** > **Регистрация Windows** > **Устройства**.</span><span class="sxs-lookup"><span data-stu-id="e704a-234">In Microsoft Endpoint Manager Admin Center, select **Devices** > **Windows** > **Windows enrollment** > **Devices**.</span></span>
1. <span data-ttu-id="e704a-235">Проверьте, что устройства HoloLens указаны в списке, а состоянием их профиля является **Назначенное**.</span><span class="sxs-lookup"><span data-stu-id="e704a-235">Verify that the HoloLens devices are listed, and that their profile status is **Assigned**.</span></span>  
   > [!NOTE]  
   > <span data-ttu-id="e704a-236">Назначение профиля устройству может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="e704a-236">It may take a few minutes for the profile to be assigned to the device.</span></span>  
   
   ![Назначения устройств и профилей.](./images/hololens-ap-devices-assignments.png)

## <span data-ttu-id="e704a-238">Пользовательский интерфейс Windows Autopilot для HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="e704a-238">Windows Autopilot for HoloLens 2 User Experience</span></span>

<span data-ttu-id="e704a-239">Пользователи HoloLens могут выполнить следующие действия для подготовки устройств HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e704a-239">Your HoloLens users can follow these steps to provision HoloLens devices.</span></span>  

1. <span data-ttu-id="e704a-240">Использование кабеля USB-C, чтобы подключить устройство HoloLens к компьютеру с установленным расширенным помощником по восстановлению (ARC) и скачанным соответствующим обновлением Windows.</span><span class="sxs-lookup"><span data-stu-id="e704a-240">Use the USB-C cable to connect the HoloLens device to a computer that has Advanced Recovery Companion (ARC) installed and has the appropriate Windows update downloaded.</span></span>
1. <span data-ttu-id="e704a-241">Использование ARC для установки образа соответствующей версии Windows на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e704a-241">Use ARC to flash the appropriate version of Windows on to the device.</span></span>
1. <span data-ttu-id="e704a-242">Подключение устройства к сети и перезапуск устройства.</span><span class="sxs-lookup"><span data-stu-id="e704a-242">Connect the device to the network, and then restart the device.</span></span>  
   > [!IMPORTANT]  
   > <span data-ttu-id="e704a-243">Перед запуском интерфейса при первом включении (OOBE) вы должны подключить устройство к сети.</span><span class="sxs-lookup"><span data-stu-id="e704a-243">You must connect the device to the network before the Out-of-the-Box-Experience (OOBE) starts.</span></span> <span data-ttu-id="e704a-244">На первом экране OOBE устройство определяет, подготавливается ли оно как устройство Autopilot.</span><span class="sxs-lookup"><span data-stu-id="e704a-244">The device determines whether it is provisioning as an Autopilot device while on the first OOBE screen.</span></span> <span data-ttu-id="e704a-245">Если устройство не может подключиться к сети или вы решили не подготавливать его в качестве устройства Autopilot, вы не сможете в дальнейшем выбрать подготовку Autopilot.</span><span class="sxs-lookup"><span data-stu-id="e704a-245">If the device cannot connect to the network, or if you choose not to provision the device as an Autopilot device, you cannot change to Autopilot provisioning at a later time.</span></span> <span data-ttu-id="e704a-246">Вместо этого вам потребуется заново начать эту процедуру, чтобы подготовить устройство в качестве устройства Autopilot.</span><span class="sxs-lookup"><span data-stu-id="e704a-246">Instead, you would have to start this procedure over in order to provision the device as an Autopilot device.</span></span>

   <span data-ttu-id="e704a-247">Устройство должно автоматически запустить OOBE.</span><span class="sxs-lookup"><span data-stu-id="e704a-247">The device should automatically start OOBE.</span></span> <span data-ttu-id="e704a-248">Не взаимодействуйте с OOBE.</span><span class="sxs-lookup"><span data-stu-id="e704a-248">Do not interact with OOBE.</span></span> <span data-ttu-id="e704a-249">Откиньтесь на спинку и расслабьтесь!</span><span class="sxs-lookup"><span data-stu-id="e704a-249">Instead sit, back and relax!</span></span> <span data-ttu-id="e704a-250">Позвольте HoloLens 2 определить сетевое подключение и завершить OOBE автоматически.</span><span class="sxs-lookup"><span data-stu-id="e704a-250">Let HoloLens 2 detect network connectivity and allow it complete OOBE automatically.</span></span> <span data-ttu-id="e704a-251">В процессе OOBE устройство может перезапускаться.</span><span class="sxs-lookup"><span data-stu-id="e704a-251">The device may restart during OOBE.</span></span> <span data-ttu-id="e704a-252">Экраны OOBE должны выглядеть примерно следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e704a-252">The OOBE screens should resemble the following.</span></span>
   
   <span data-ttu-id="e704a-253">![Шаг OOBE 1](./images/hololens-ap-uex-1.png)
   ![Шаг OOBE 2](./images/hololens-ap-uex-2.png)
   ![Шаг OOBE 3](./images/hololens-ap-uex-3.png)
   ![Шаг OOBE 4](./images/hololens-ap-uex-4.png)</span><span class="sxs-lookup"><span data-stu-id="e704a-253">![OOBE step 1](./images/hololens-ap-uex-1.png)
![OOBE step 2](./images/hololens-ap-uex-2.png)
![OOBE step 3](./images/hololens-ap-uex-3.png)
![OOBE step 4](./images/hololens-ap-uex-4.png)</span></span>

<span data-ttu-id="e704a-254">В конце OOBE вы можете войти в устройство, используя свое имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="e704a-254">At the end of OOBE, you can sign in to the device by using your user name and password.</span></span>

  ![Шаг OOBE 5](./images/hololens-ap-uex-5.png)

## <span data-ttu-id="e704a-256">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="e704a-256">Known Issues</span></span>

- <span data-ttu-id="e704a-257">Установить приложения, использующие контекст безопасности устройства, невозможно.</span><span class="sxs-lookup"><span data-stu-id="e704a-257">You cannot install applications that use the device security context.</span></span>

## <span data-ttu-id="e704a-258">Отзыв</span><span class="sxs-lookup"><span data-stu-id="e704a-258">Feedback</span></span>

<span data-ttu-id="e704a-259">Чтобы оставить отзыв или сообщить о проблемах, используйте один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="e704a-259">To provide feedback or report issues, use one of the following methods:</span></span>

- <span data-ttu-id="e704a-260">Используйте приложение "Центр отзывов".</span><span class="sxs-lookup"><span data-stu-id="e704a-260">Use the Feedback Hub app.</span></span> <span data-ttu-id="e704a-261">Вы можете найти это приложение на компьютере, подключенном к HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e704a-261">You can find this app on a HoloLens-connected computer.</span></span> <span data-ttu-id="e704a-262">В Центре отзывов выберите категорию **Управление предприятием** > **Устройство**.</span><span class="sxs-lookup"><span data-stu-id="e704a-262">In Feedback Hub, select the **Enterprise Management** > **Device** category.</span></span>  

  <span data-ttu-id="e704a-263">При предоставлении отзыва или сообщении о проблеме добавьте подробное описание.</span><span class="sxs-lookup"><span data-stu-id="e704a-263">When you provide feedback or report an issue, provide a detailed description.</span></span> <span data-ttu-id="e704a-264">При необходимости включите снимки экрана и журналы.</span><span class="sxs-lookup"><span data-stu-id="e704a-264">If applicable, include screenshots and logs.</span></span>
- <span data-ttu-id="e704a-265">Отправьте сообщение электронной почты на адрес [hlappreview@microsoft.com](mailto:hlappreview@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e704a-265">Send an email message to [hlappreview@microsoft.com](mailto:hlappreview@microsoft.com).</span></span> <span data-ttu-id="e704a-266">В качестве темы письма введите **\<*Tenant*>Отзыв с оценкой Autopilot для HoloLens 2** (где \<*Tenant*> — это имя вашего клиента Intune).</span><span class="sxs-lookup"><span data-stu-id="e704a-266">For the email subject, enter **\<*Tenant*> Autopilot for HoloLens 2 evaluation feedback** (where \<*Tenant*> is the name of your Intune tenant).</span></span>

  <span data-ttu-id="e704a-267">Предоставьте подробное описание в своем сообщении.</span><span class="sxs-lookup"><span data-stu-id="e704a-267">Provide a detailed description in your message.</span></span> <span data-ttu-id="e704a-268">Но на включайте такие данные, как снимки экрана или журналы, если сотрудники службы поддержки их не запрашивали.</span><span class="sxs-lookup"><span data-stu-id="e704a-268">However, unless Support personnel specifically request it, do not include data such as screenshots or logs.</span></span> <span data-ttu-id="e704a-269">Такие данные могут содержать личные или персональные сведения (PII).</span><span class="sxs-lookup"><span data-stu-id="e704a-269">Such data might include private or personally identifiable information (PII).</span></span>
