---
title: Распространенные сценарии — автономное безопасное соединение HoloLens 2
description: Узнайте, как настроить автономное развертывание и сценарий развертывания приложений с помощью подготовки для устройств HoloLens.
keywords: HoloLens, управление, автономная, Автономная защита
ms.date: 9/25/2020
manager: yannisle
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: v-evmill
ms.reviewer: aboeger
ms.topic: article
audience: ITPro
ms.localizationpriority: medium
appliesto:
- HoloLens 2
ms.openlocfilehash: 7eb084d3de222581fd2b97eaa1c1e2812310810c
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309127"
---
# <a name="common-scenarios--offline-secure-hololens-2"></a><span data-ttu-id="baf0a-104">Распространенные сценарии — автономное безопасное соединение HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="baf0a-104">Common Scenarios – Offline Secure HoloLens 2</span></span>

## <a name="overview"></a><span data-ttu-id="baf0a-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="baf0a-105">Overview</span></span>

<span data-ttu-id="baf0a-106">В этом руководстве приводятся инструкции по применению примера пакета подготовки, который будет блокировать HoloLens 2 для использования в защищенных средах со следующими ограничениями.</span><span class="sxs-lookup"><span data-stu-id="baf0a-106">This guide provides guidance for applying a sample Provisioning Package that will lock down a HoloLens 2 for use in secure environments with the following restrictions:</span></span>

-   <span data-ttu-id="baf0a-107">Отключите Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="baf0a-107">Disable WiFi.</span></span>
-   <span data-ttu-id="baf0a-108">Отключите BlueTooth.</span><span class="sxs-lookup"><span data-stu-id="baf0a-108">Disable BlueTooth.</span></span>
-   <span data-ttu-id="baf0a-109">Отключить микрофоны.</span><span class="sxs-lookup"><span data-stu-id="baf0a-109">Disable Microphones.</span></span>
-   <span data-ttu-id="baf0a-110">Предотвращает добавление или удаление пакетов подготовки.</span><span class="sxs-lookup"><span data-stu-id="baf0a-110">Prevents adding or removing provisioning packages.</span></span>
-   <span data-ttu-id="baf0a-111">Ни один пользователь не может включить ни один из перечисленных выше ограниченных компонентов.</span><span class="sxs-lookup"><span data-stu-id="baf0a-111">No user can enable any of the above restricted components.</span></span>

## <a name="prepare"></a><span data-ttu-id="baf0a-112">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="baf0a-112">Prepare</span></span>

<span data-ttu-id="baf0a-113">Программа установки ПК с Windows 10</span><span class="sxs-lookup"><span data-stu-id="baf0a-113">Windows 10 PC Setup</span></span>
1. <span data-ttu-id="baf0a-114">[Скачайте последнюю версию файла операционной системы HoloLens 2](https://aka.ms/hololens2download) непосредственно на компьютер.</span><span class="sxs-lookup"><span data-stu-id="baf0a-114">[Download the latest HoloLens 2 OS file](https://aka.ms/hololens2download) directly to a PC.</span></span> 
   1. <span data-ttu-id="baf0a-115">Поддержка этой конфигурации включена в сборку 19041,1117 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="baf0a-115">Support for this configuration is included in Build 19041.1117 and above.</span></span>
1. <span data-ttu-id="baf0a-116">Скачайте или установите средство расширенного помощника по восстановлению (ARC) [из Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) на компьютер.</span><span class="sxs-lookup"><span data-stu-id="baf0a-116">Download/Install the Advanced Recovery Companion(ARC) tool [from the Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) to your PC</span></span>
1. <span data-ttu-id="baf0a-117">Скачайте или установите последнюю версию средства [конструктора конфигураций Windows (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) из Microsoft Store на компьютер.</span><span class="sxs-lookup"><span data-stu-id="baf0a-117">Download/Install the latest [Windows Configuration Designer (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) tool from the Microsoft Store to your PC.</span></span>
1. <span data-ttu-id="baf0a-118">[Скачайте папку OfflineSecureHL2_Sample с файлами проекта](https://aka.ms/HoloLensDocs-SecureOfflineSample) для создания PPKG.</span><span class="sxs-lookup"><span data-stu-id="baf0a-118">[Download the OfflineSecureHL2_Sample folder with the project files](https://aka.ms/HoloLensDocs-SecureOfflineSample) to build the PPKG.</span></span>
1. <span data-ttu-id="baf0a-119">Подготовьте автономное [бизнес-приложение для развертывания PPKG](app-deploy-provisioning-package.md).</span><span class="sxs-lookup"><span data-stu-id="baf0a-119">Prepare your offline [Line of Business application for PPKG deployment](app-deploy-provisioning-package.md).</span></span> 


## <a name="configure"></a><span data-ttu-id="baf0a-120">Configure</span><span class="sxs-lookup"><span data-stu-id="baf0a-120">Configure</span></span>

<span data-ttu-id="baf0a-121">Создание пакета обеспечения безопасной конфигурации</span><span class="sxs-lookup"><span data-stu-id="baf0a-121">Build a Secure Configuration Provisioning Package</span></span>

1. <span data-ttu-id="baf0a-122">Запустите средство WCD на компьютере.</span><span class="sxs-lookup"><span data-stu-id="baf0a-122">Launch the WCD tool on your PC.</span></span>
1. <span data-ttu-id="baf0a-123">Выберите **файл-> открыть проект**.</span><span class="sxs-lookup"><span data-stu-id="baf0a-123">Select **File -> Open project**.</span></span>
  1. <span data-ttu-id="baf0a-124">Перейдите к расположению ранее сохраненной OfflineSecureHL2_Sample папки и выберите: OfflineSecureHL2_Sample.icdproj.xml</span><span class="sxs-lookup"><span data-stu-id="baf0a-124">Navigate to the location of the previously saved OfflineSecureHL2_Sample folder, and select: OfflineSecureHL2_Sample.icdproj.xml</span></span>
1. <span data-ttu-id="baf0a-125">Проект должен быть открыт, и теперь у вас должен быть список доступных настроек:</span><span class="sxs-lookup"><span data-stu-id="baf0a-125">The project should open and you should now have a list of Available Customizations:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="baf0a-126">![Снимок экрана: пакет конфигурации открыт в WCD](images/offline-secure-sample-wcd.png)</span><span class="sxs-lookup"><span data-stu-id="baf0a-126">![Screenshot of the configuration package open in WCD](images/offline-secure-sample-wcd.png)</span></span>

   <span data-ttu-id="baf0a-127">Конфигурации, заданные в этом пакете подготовки:</span><span class="sxs-lookup"><span data-stu-id="baf0a-127">Configurations set in this provisioning package:</span></span>
   
   |     <span data-ttu-id="baf0a-128">Элемент</span><span class="sxs-lookup"><span data-stu-id="baf0a-128">Item</span></span>                                                |     <span data-ttu-id="baf0a-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="baf0a-129">Setting</span></span>                       |     <span data-ttu-id="baf0a-130">Описание</span><span class="sxs-lookup"><span data-stu-id="baf0a-130">Description</span></span>                                                                                                                    |
   |---------------------------------------------------------|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
   |     <span data-ttu-id="baf0a-131">Учетные записи и пользователи</span><span class="sxs-lookup"><span data-stu-id="baf0a-131">Accounts / Users</span></span>                                    |     <span data-ttu-id="baf0a-132">Имя локального пользователя & пароль</span><span class="sxs-lookup"><span data-stu-id="baf0a-132">Local User Name & Password</span></span>    |     <span data-ttu-id="baf0a-133">Для этих автономных устройств необходимо задать одно имя пользователя и пароль и предоставить общий доступ всем пользователям устройства.</span><span class="sxs-lookup"><span data-stu-id="baf0a-133">For these offline devices, a single user name and password will need to be set and shared by all users of the device.</span></span>          |
   |     <span data-ttu-id="baf0a-134">Первый опыт/HoloLens/Скипкалибратион</span><span class="sxs-lookup"><span data-stu-id="baf0a-134">First Experience / HoloLens / SkipCalibration</span></span>       |     <span data-ttu-id="baf0a-135">Верно</span><span class="sxs-lookup"><span data-stu-id="baf0a-135">True</span></span>                          |     <span data-ttu-id="baf0a-136">Пропуск калибровки только во время первоначальной настройки устройства</span><span class="sxs-lookup"><span data-stu-id="baf0a-136">Skips calibration during initial device setup only</span></span>                                                                             |
   |     <span data-ttu-id="baf0a-137">Первый опыт/HoloLens/Скиптраининг</span><span class="sxs-lookup"><span data-stu-id="baf0a-137">First Experience / HoloLens / SkipTraining</span></span>          |     <span data-ttu-id="baf0a-138">Верно</span><span class="sxs-lookup"><span data-stu-id="baf0a-138">True</span></span>                          |     <span data-ttu-id="baf0a-139">Пропускает обучение устройств во время первоначальной настройки устройства</span><span class="sxs-lookup"><span data-stu-id="baf0a-139">Skips device training during initial device setup</span></span>                                                                              |
   |     <span data-ttu-id="baf0a-140">Первый опыт, HoloLens или WiFi</span><span class="sxs-lookup"><span data-stu-id="baf0a-140">First Experience / HoloLens / WiFi</span></span>                  |     <span data-ttu-id="baf0a-141">Верно</span><span class="sxs-lookup"><span data-stu-id="baf0a-141">True</span></span>                          |     <span data-ttu-id="baf0a-142">Пропуск Wi-Fi конфигурации во время первоначальной настройки устройства</span><span class="sxs-lookup"><span data-stu-id="baf0a-142">Skips Wi-Fi config during initial device setup</span></span>                                                                                 |
   |     <span data-ttu-id="baf0a-143">Политики/подключение/Алловблуетус</span><span class="sxs-lookup"><span data-stu-id="baf0a-143">Policies/Connectivity/AllowBluetooth</span></span>                |     <span data-ttu-id="baf0a-144">Нет</span><span class="sxs-lookup"><span data-stu-id="baf0a-144">No</span></span>                            |     <span data-ttu-id="baf0a-145">Отключение Bluetooth</span><span class="sxs-lookup"><span data-stu-id="baf0a-145">Disables Bluetooth</span></span>                                                                                                             |
   |     <span data-ttu-id="baf0a-146">Политики/опыт/Алловкортана</span><span class="sxs-lookup"><span data-stu-id="baf0a-146">Policies/Experience/AllowCortana</span></span>                    |     <span data-ttu-id="baf0a-147">Нет</span><span class="sxs-lookup"><span data-stu-id="baf0a-147">No</span></span>                            |     <span data-ttu-id="baf0a-148">Отключает Кортану (для устранения потенциальных проблем, так как микрофоны отключены)</span><span class="sxs-lookup"><span data-stu-id="baf0a-148">Disables Cortana (to eliminate potential problems since the microphones are disabled)</span></span>                                          |
   |     <span data-ttu-id="baf0a-149">Policies/Микседреалити/Микрофонедисаблед</span><span class="sxs-lookup"><span data-stu-id="baf0a-149">Policies/MixedReality/MicrophoneDisabled</span></span>            |     <span data-ttu-id="baf0a-150">Да</span><span class="sxs-lookup"><span data-stu-id="baf0a-150">Yes</span></span>                           |     <span data-ttu-id="baf0a-151">Отключает микрофон</span><span class="sxs-lookup"><span data-stu-id="baf0a-151">Disables Microphone</span></span>                                                                                                            |
   |     <span data-ttu-id="baf0a-152">Политики/конфиденциальность/Летаппсакцесслокатион</span><span class="sxs-lookup"><span data-stu-id="baf0a-152">Policies/Privacy/LetAppsAccessLocation</span></span>              |     <span data-ttu-id="baf0a-153">Принудительно запретить</span><span class="sxs-lookup"><span data-stu-id="baf0a-153">Force deny</span></span>                    |     <span data-ttu-id="baf0a-154">Запрещает приложениям доступ к данным расположения (чтобы устранить потенциальные проблемы, так как отслеживание расположения отключено).</span><span class="sxs-lookup"><span data-stu-id="baf0a-154">Prevents Apps from trying to access Location data (to eliminate potential problems since the Location tracking is disabled)</span></span>    |
   |     <span data-ttu-id="baf0a-155">Политики/конфиденциальность/Летаппсакцессмикрофоне</span><span class="sxs-lookup"><span data-stu-id="baf0a-155">Policies/Privacy/LetAppsAccessMicrophone</span></span>            |     <span data-ttu-id="baf0a-156">Принудительно запретить</span><span class="sxs-lookup"><span data-stu-id="baf0a-156">Force deny</span></span>                    |     <span data-ttu-id="baf0a-157">Запрещает приложениям пытаться получить доступ к микрофонам (чтобы устранить потенциальные проблемы, так как микрофоны отключены).</span><span class="sxs-lookup"><span data-stu-id="baf0a-157">Prevents Apps from trying to access Microphones (to eliminate potential problems since the Microphones are disabled)</span></span>           |
   |     <span data-ttu-id="baf0a-158">Политики/безопасность/Алловаддпровисионингпаккаже</span><span class="sxs-lookup"><span data-stu-id="baf0a-158">Policies/Security/AllowAddProvisioningPackage</span></span>       |     <span data-ttu-id="baf0a-159">Нет</span><span class="sxs-lookup"><span data-stu-id="baf0a-159">No</span></span>                            |     <span data-ttu-id="baf0a-160">Предотвращает добавление пакетов подготовки, которые могут попытаться переопределить заблокированные политики.</span><span class="sxs-lookup"><span data-stu-id="baf0a-160">Prevents anyone from adding provisioning packages that might attempt to override locked down policies.</span></span>                         |
   |     <span data-ttu-id="baf0a-161">Политики/безопасность/Алловремовепровисионингпаккаже</span><span class="sxs-lookup"><span data-stu-id="baf0a-161">Policies/Security/AllowRemoveProvisioningPackage</span></span>    |     <span data-ttu-id="baf0a-162">Нет</span><span class="sxs-lookup"><span data-stu-id="baf0a-162">No</span></span>                            |     <span data-ttu-id="baf0a-163">Предотвращает удаление заблокированного пакета подготовки.</span><span class="sxs-lookup"><span data-stu-id="baf0a-163">Prevents anyone from removing this locked down provisioning package.</span></span>                                                           |
   |     <span data-ttu-id="baf0a-164">Политики/система/AllowLocation</span><span class="sxs-lookup"><span data-stu-id="baf0a-164">Policies/System/AllowLocation</span></span>                       |     <span data-ttu-id="baf0a-165">Нет</span><span class="sxs-lookup"><span data-stu-id="baf0a-165">No</span></span>                            |     <span data-ttu-id="baf0a-166">Предотвращает попытки устройства к отслеживанию данных расположения.</span><span class="sxs-lookup"><span data-stu-id="baf0a-166">Prevents the device from trying to track location data.</span></span>                                                                        |
   |     <span data-ttu-id="baf0a-167">Политики/WiFi/Алловвифи</span><span class="sxs-lookup"><span data-stu-id="baf0a-167">Policies/WiFi/AllowWiFi</span></span>                             |     <span data-ttu-id="baf0a-168">Нет</span><span class="sxs-lookup"><span data-stu-id="baf0a-168">No</span></span>                            |     <span data-ttu-id="baf0a-169">Отключает Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="baf0a-169">Disables Wi-Fi</span></span>                                                                                                                 |

1. <span data-ttu-id="baf0a-170">В разделе Параметры среды выполнения выберите **учетные записи/пользователи/имя пользователя: Холо/пароль**.</span><span class="sxs-lookup"><span data-stu-id="baf0a-170">Under Runtime Settings, Select **Accounts / Users / UserName: Holo / Password**.</span></span>

   <span data-ttu-id="baf0a-171">Запишите пароль и при необходимости сбросьте его.</span><span class="sxs-lookup"><span data-stu-id="baf0a-171">Note the password and reset if desired.</span></span>

1. <span data-ttu-id="baf0a-172">Перейдите в раздел Универсалаппинсталл/Усерконтекстапп и [Настройте бизнес-приложение](app-deploy-provisioning-package.md) , которое будет развертываться на этих устройствах.</span><span class="sxs-lookup"><span data-stu-id="baf0a-172">Navigate to UniversalAppInstall / UserContextApp and [configure the LOB app](app-deploy-provisioning-package.md) you will be deploying to these devices.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="baf0a-173">![Снимок экрана добавления приложения в WCD.](images/offline-secure-sample-wcd-usercontextapp2.png)</span><span class="sxs-lookup"><span data-stu-id="baf0a-173">![Screenshot of where to add your app in WCD.](images/offline-secure-sample-wcd-usercontextapp2.png)</span></span>

1. <span data-ttu-id="baf0a-174">После завершения нажмите кнопку "экспорт" и следуйте всем запросам, пока не будет создан пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="baf0a-174">Once complete, select the “Export” button and follow all prompts until your provisioning package is created.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="baf0a-175">![Снимок экрана кнопки экспорта для этого пакета в WCD.](images/offline-secure-sample-wcd-export.png)</span><span class="sxs-lookup"><span data-stu-id="baf0a-175">![Screenshot of the Export button for this package in WCD.](images/offline-secure-sample-wcd-export.png)</span></span>

## <a name="deploy"></a><span data-ttu-id="baf0a-176">Развернуть</span><span class="sxs-lookup"><span data-stu-id="baf0a-176">Deploy</span></span>

1. <span data-ttu-id="baf0a-177">Подключите HL2 к компьютеру с Windows 10 через USB-кабель.</span><span class="sxs-lookup"><span data-stu-id="baf0a-177">Connect the HL2 to your Windows 10 PC via USB cable.</span></span>
1. <span data-ttu-id="baf0a-178">Запустите инструмент ARC и выберите **HoloLens 2** .</span><span class="sxs-lookup"><span data-stu-id="baf0a-178">Launch the ARC tool and select **HoloLens 2**</span></span>

   ![Начальный экран очистки HoloLens 2](images/ARC2.png)

1. <span data-ttu-id="baf0a-180">На следующем экране выберите **Ручное выделение пакетов**.</span><span class="sxs-lookup"><span data-stu-id="baf0a-180">On the next screen select **Manual package selection**.</span></span>

   ![Экран сведений о дуги HoloLens 2](images/arc_device_info.png)

1. <span data-ttu-id="baf0a-182">Перейдите к ранее скачанному файлу. ФФУ и выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="baf0a-182">Navigate to the previously downloaded .ffu file, and select **Open**.</span></span>
1. <span data-ttu-id="baf0a-183">На странице предупреждения нажмите кнопку **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="baf0a-183">At the Warning page select **Continue**.</span></span>

   ![Экран предупреждения по ДУГЕ HoloLens 2](images/arc_warning.png)

1. <span data-ttu-id="baf0a-185">Подождите, пока средство ARC завершит установку ОС HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="baf0a-185">Wait for the ARC tool to complete the HoloLens 2 OS install.</span></span>
1. <span data-ttu-id="baf0a-186">Когда устройство завершит установку и загрузит резервную копию, с компьютера перейдите в проводник и Скопируйте сохраненный ранее файл PPKG в папку Device.</span><span class="sxs-lookup"><span data-stu-id="baf0a-186">Once the device completes the install and boots back up, from your PC navigate to File Explorer and copy the previously saved PPKG file over to the device folder.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="baf0a-187">![PPKG файл на компьютере в окне проводника.](images/offline-secure-file-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="baf0a-187">![PPKG file on PC in File Explorer window.](images/offline-secure-file-explorer.png)</span></span>

1. <span data-ttu-id="baf0a-188">В HoloLens 2 нажмите приведенную ниже кнопку со списком, чтобы запустить пакет подготовки: **одновременно коснитесь** **кнопки питания** .</span><span class="sxs-lookup"><span data-stu-id="baf0a-188">On the HoloLens 2, press the following button combo to run the Provisioning Package: Tap **Volume Down** and **Power Button** at the same time.</span></span>
1. <span data-ttu-id="baf0a-189">Появится запрос на применение пакета подготовки, нажмите кнопку **подтвердить** .</span><span class="sxs-lookup"><span data-stu-id="baf0a-189">You will be prompted to apply the Provisioning Package, select **Confirm**</span></span>
1. <span data-ttu-id="baf0a-190">После завершения пакета подготовки нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="baf0a-190">Once the provisioning package completes select **OK**.</span></span>
1. <span data-ttu-id="baf0a-191">После этого вам будет предложено войти на устройство с общей локальной учетной записью и паролем.</span><span class="sxs-lookup"><span data-stu-id="baf0a-191">You should then be prompted to sign into the device with the shared local account and password.</span></span>

## <a name="maintain"></a><span data-ttu-id="baf0a-192">Техническое обслуживание</span><span class="sxs-lookup"><span data-stu-id="baf0a-192">Maintain</span></span>

<span data-ttu-id="baf0a-193">В этой конфигурации рекомендуется перезапустить процесс выше и восстановить устройство с помощью инструмента ARC и применить новый PPKG, чтобы внести изменения в ОС и (или) приложения.</span><span class="sxs-lookup"><span data-stu-id="baf0a-193">With this configuration, it is recommended to restart the process above and reflash the device with the ARC tool and apply a new PPKG to make any updates to the OS and/or application(s).</span></span>
