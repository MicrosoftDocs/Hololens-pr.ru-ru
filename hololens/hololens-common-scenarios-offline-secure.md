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
ms.openlocfilehash: 8828444a69d7e5d46293340ff771f97eb5eb01e6
ms.sourcegitcommit: 29573e577381a23891e9557884a6dfdaac0c1c48
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110397885"
---
# <a name="common-scenarios--offline-secure-hololens-2"></a><span data-ttu-id="f50d9-104">Распространенные сценарии — автономное безопасное соединение HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="f50d9-104">Common Scenarios – Offline Secure HoloLens 2</span></span>

## <a name="overview"></a><span data-ttu-id="f50d9-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="f50d9-105">Overview</span></span>

<span data-ttu-id="f50d9-106">В этом руководстве приводятся инструкции по применению примера пакета подготовки, который будет блокировать HoloLens 2 для использования в защищенных средах со следующими ограничениями.</span><span class="sxs-lookup"><span data-stu-id="f50d9-106">This guide provides guidance for applying a sample Provisioning Package that will lock down a HoloLens 2 for use in secure environments with the following restrictions:</span></span>

-   <span data-ttu-id="f50d9-107">Отключите Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="f50d9-107">Disable WiFi.</span></span>
-   <span data-ttu-id="f50d9-108">Отключите BlueTooth.</span><span class="sxs-lookup"><span data-stu-id="f50d9-108">Disable BlueTooth.</span></span>
-   <span data-ttu-id="f50d9-109">Отключить микрофоны.</span><span class="sxs-lookup"><span data-stu-id="f50d9-109">Disable Microphones.</span></span>
-   <span data-ttu-id="f50d9-110">Предотвращает добавление или удаление пакетов подготовки.</span><span class="sxs-lookup"><span data-stu-id="f50d9-110">Prevents adding or removing provisioning packages.</span></span>
-   <span data-ttu-id="f50d9-111">Ни один пользователь не может включить ни один из перечисленных выше ограниченных компонентов.</span><span class="sxs-lookup"><span data-stu-id="f50d9-111">No user can enable any of the above restricted components.</span></span>

<span data-ttu-id="f50d9-112">[![Автономный сценарий ](./images/deployment-guides-revised-scenario-c-01.png) защиты](./images/deployment-guides-revised-scenario-c-01.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f50d9-112">[ ![Offline Secure scenario](./images/deployment-guides-revised-scenario-c-01.png) ](./images/deployment-guides-revised-scenario-c-01.png#lightbox)</span></span>

## <a name="prepare"></a><span data-ttu-id="f50d9-113">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="f50d9-113">Prepare</span></span>

<span data-ttu-id="f50d9-114">Программа установки ПК с Windows 10</span><span class="sxs-lookup"><span data-stu-id="f50d9-114">Windows 10 PC Setup</span></span>
1. <span data-ttu-id="f50d9-115">[Скачайте последнюю версию файла операционной системы HoloLens 2](https://aka.ms/hololens2download) непосредственно на компьютер.</span><span class="sxs-lookup"><span data-stu-id="f50d9-115">[Download the latest HoloLens 2 OS file](https://aka.ms/hololens2download) directly to a PC.</span></span> 
   1. <span data-ttu-id="f50d9-116">Поддержка этой конфигурации включена в сборку 19041,1117 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f50d9-116">Support for this configuration is included in Build 19041.1117 and above.</span></span>
1. <span data-ttu-id="f50d9-117">Скачайте или установите средство расширенного помощника по восстановлению (ARC) [из Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) на компьютер.</span><span class="sxs-lookup"><span data-stu-id="f50d9-117">Download/Install the Advanced Recovery Companion(ARC) tool [from the Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) to your PC</span></span>
1. <span data-ttu-id="f50d9-118">Скачайте или установите последнюю версию средства [конструктора конфигураций Windows (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) из Microsoft Store на компьютер.</span><span class="sxs-lookup"><span data-stu-id="f50d9-118">Download/Install the latest [Windows Configuration Designer (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) tool from the Microsoft Store to your PC.</span></span>
1. <span data-ttu-id="f50d9-119">[Скачайте папку OfflineSecureHL2_Sample с файлами проекта](https://aka.ms/HoloLensDocs-SecureOfflineSample) для создания PPKG.</span><span class="sxs-lookup"><span data-stu-id="f50d9-119">[Download the OfflineSecureHL2_Sample folder with the project files](https://aka.ms/HoloLensDocs-SecureOfflineSample) to build the PPKG.</span></span>
1. <span data-ttu-id="f50d9-120">Подготовьте автономное [бизнес-приложение для развертывания PPKG](app-deploy-provisioning-package.md).</span><span class="sxs-lookup"><span data-stu-id="f50d9-120">Prepare your offline [Line of Business application for PPKG deployment](app-deploy-provisioning-package.md).</span></span> 


## <a name="configure"></a><span data-ttu-id="f50d9-121">Configure</span><span class="sxs-lookup"><span data-stu-id="f50d9-121">Configure</span></span>

<span data-ttu-id="f50d9-122">Создание пакета обеспечения безопасной конфигурации</span><span class="sxs-lookup"><span data-stu-id="f50d9-122">Build a Secure Configuration Provisioning Package</span></span>

1. <span data-ttu-id="f50d9-123">Запустите средство WCD на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f50d9-123">Launch the WCD tool on your PC.</span></span>
1. <span data-ttu-id="f50d9-124">Выберите **файл-> открыть проект**.</span><span class="sxs-lookup"><span data-stu-id="f50d9-124">Select **File -> Open project**.</span></span>
  1. <span data-ttu-id="f50d9-125">Перейдите к расположению ранее сохраненной OfflineSecureHL2_Sample папки и выберите: OfflineSecureHL2_Sample.icdproj.xml</span><span class="sxs-lookup"><span data-stu-id="f50d9-125">Navigate to the location of the previously saved OfflineSecureHL2_Sample folder, and select: OfflineSecureHL2_Sample.icdproj.xml</span></span>
1. <span data-ttu-id="f50d9-126">Проект должен быть открыт, и теперь у вас должен быть список доступных настроек:</span><span class="sxs-lookup"><span data-stu-id="f50d9-126">The project should open and you should now have a list of Available Customizations:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="f50d9-127">![Снимок экрана: пакет конфигурации открыт в WCD](images/offline-secure-sample-wcd.png)</span><span class="sxs-lookup"><span data-stu-id="f50d9-127">![Screenshot of the configuration package open in WCD](images/offline-secure-sample-wcd.png)</span></span>

   <span data-ttu-id="f50d9-128">Конфигурации, заданные в этом пакете подготовки:</span><span class="sxs-lookup"><span data-stu-id="f50d9-128">Configurations set in this provisioning package:</span></span>
   
   |     <span data-ttu-id="f50d9-129">Item</span><span class="sxs-lookup"><span data-stu-id="f50d9-129">Item</span></span>                                                |     <span data-ttu-id="f50d9-130">Параметр</span><span class="sxs-lookup"><span data-stu-id="f50d9-130">Setting</span></span>                       |     <span data-ttu-id="f50d9-131">Описание</span><span class="sxs-lookup"><span data-stu-id="f50d9-131">Description</span></span>                                                                                                                    |
   |---------------------------------------------------------|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
   |     <span data-ttu-id="f50d9-132">Учетные записи и пользователи</span><span class="sxs-lookup"><span data-stu-id="f50d9-132">Accounts / Users</span></span>                                    |     <span data-ttu-id="f50d9-133">Имя локального пользователя & пароль</span><span class="sxs-lookup"><span data-stu-id="f50d9-133">Local User Name & Password</span></span>    |     <span data-ttu-id="f50d9-134">Для этих автономных устройств необходимо задать одно имя пользователя и пароль и предоставить общий доступ всем пользователям устройства.</span><span class="sxs-lookup"><span data-stu-id="f50d9-134">For these offline devices, a single user name and password will need to be set and shared by all users of the device.</span></span>          |
   |     <span data-ttu-id="f50d9-135">Первый опыт/HoloLens/Скипкалибратион</span><span class="sxs-lookup"><span data-stu-id="f50d9-135">First Experience / HoloLens / SkipCalibration</span></span>       |     <span data-ttu-id="f50d9-136">Да</span><span class="sxs-lookup"><span data-stu-id="f50d9-136">True</span></span>                          |     <span data-ttu-id="f50d9-137">Пропуск калибровки только во время первоначальной настройки устройства</span><span class="sxs-lookup"><span data-stu-id="f50d9-137">Skips calibration during initial device setup only</span></span>                                                                             |
   |     <span data-ttu-id="f50d9-138">Первый опыт/HoloLens/Скиптраининг</span><span class="sxs-lookup"><span data-stu-id="f50d9-138">First Experience / HoloLens / SkipTraining</span></span>          |     <span data-ttu-id="f50d9-139">Да</span><span class="sxs-lookup"><span data-stu-id="f50d9-139">True</span></span>                          |     <span data-ttu-id="f50d9-140">Пропускает обучение устройств во время первоначальной настройки устройства</span><span class="sxs-lookup"><span data-stu-id="f50d9-140">Skips device training during initial device setup</span></span>                                                                              |
   |     <span data-ttu-id="f50d9-141">Первый опыт, HoloLens или WiFi</span><span class="sxs-lookup"><span data-stu-id="f50d9-141">First Experience / HoloLens / WiFi</span></span>                  |     <span data-ttu-id="f50d9-142">Да</span><span class="sxs-lookup"><span data-stu-id="f50d9-142">True</span></span>                          |     <span data-ttu-id="f50d9-143">Пропуск Wi-Fi конфигурации во время первоначальной настройки устройства</span><span class="sxs-lookup"><span data-stu-id="f50d9-143">Skips Wi-Fi config during initial device setup</span></span>                                                                                 |
   |     <span data-ttu-id="f50d9-144">Политики/подключение/Алловблуетус</span><span class="sxs-lookup"><span data-stu-id="f50d9-144">Policies/Connectivity/AllowBluetooth</span></span>                |     <span data-ttu-id="f50d9-145">Нет</span><span class="sxs-lookup"><span data-stu-id="f50d9-145">No</span></span>                            |     <span data-ttu-id="f50d9-146">Отключение Bluetooth</span><span class="sxs-lookup"><span data-stu-id="f50d9-146">Disables Bluetooth</span></span>                                                                                                             |
   |     <span data-ttu-id="f50d9-147">Политики/опыт/Алловкортана</span><span class="sxs-lookup"><span data-stu-id="f50d9-147">Policies/Experience/AllowCortana</span></span>                    |     <span data-ttu-id="f50d9-148">Нет</span><span class="sxs-lookup"><span data-stu-id="f50d9-148">No</span></span>                            |     <span data-ttu-id="f50d9-149">Отключает Кортану (для устранения потенциальных проблем, так как микрофоны отключены)</span><span class="sxs-lookup"><span data-stu-id="f50d9-149">Disables Cortana (to eliminate potential problems since the microphones are disabled)</span></span>                                          |
   |     <span data-ttu-id="f50d9-150">Policies/Микседреалити/Микрофонедисаблед</span><span class="sxs-lookup"><span data-stu-id="f50d9-150">Policies/MixedReality/MicrophoneDisabled</span></span>            |     <span data-ttu-id="f50d9-151">Да</span><span class="sxs-lookup"><span data-stu-id="f50d9-151">Yes</span></span>                           |     <span data-ttu-id="f50d9-152">Отключает микрофон</span><span class="sxs-lookup"><span data-stu-id="f50d9-152">Disables Microphone</span></span>                                                                                                            |
   |     <span data-ttu-id="f50d9-153">Политики/конфиденциальность/Летаппсакцесслокатион</span><span class="sxs-lookup"><span data-stu-id="f50d9-153">Policies/Privacy/LetAppsAccessLocation</span></span>              |     <span data-ttu-id="f50d9-154">Принудительно запретить</span><span class="sxs-lookup"><span data-stu-id="f50d9-154">Force deny</span></span>                    |     <span data-ttu-id="f50d9-155">Запрещает приложениям доступ к данным расположения (чтобы устранить потенциальные проблемы, так как отслеживание расположения отключено).</span><span class="sxs-lookup"><span data-stu-id="f50d9-155">Prevents Apps from trying to access Location data (to eliminate potential problems since the Location tracking is disabled)</span></span>    |
   |     <span data-ttu-id="f50d9-156">Политики/конфиденциальность/Летаппсакцессмикрофоне</span><span class="sxs-lookup"><span data-stu-id="f50d9-156">Policies/Privacy/LetAppsAccessMicrophone</span></span>            |     <span data-ttu-id="f50d9-157">Принудительно запретить</span><span class="sxs-lookup"><span data-stu-id="f50d9-157">Force deny</span></span>                    |     <span data-ttu-id="f50d9-158">Запрещает приложениям пытаться получить доступ к микрофонам (чтобы устранить потенциальные проблемы, так как микрофоны отключены).</span><span class="sxs-lookup"><span data-stu-id="f50d9-158">Prevents Apps from trying to access Microphones (to eliminate potential problems since the Microphones are disabled)</span></span>           |
   |     <span data-ttu-id="f50d9-159">Политики/безопасность/Алловаддпровисионингпаккаже</span><span class="sxs-lookup"><span data-stu-id="f50d9-159">Policies/Security/AllowAddProvisioningPackage</span></span>       |     <span data-ttu-id="f50d9-160">Нет</span><span class="sxs-lookup"><span data-stu-id="f50d9-160">No</span></span>                            |     <span data-ttu-id="f50d9-161">Предотвращает добавление пакетов подготовки, которые могут попытаться переопределить заблокированные политики.</span><span class="sxs-lookup"><span data-stu-id="f50d9-161">Prevents anyone from adding provisioning packages that might attempt to override locked down policies.</span></span>                         |
   |     <span data-ttu-id="f50d9-162">Политики/безопасность/Алловремовепровисионингпаккаже</span><span class="sxs-lookup"><span data-stu-id="f50d9-162">Policies/Security/AllowRemoveProvisioningPackage</span></span>    |     <span data-ttu-id="f50d9-163">Нет</span><span class="sxs-lookup"><span data-stu-id="f50d9-163">No</span></span>                            |     <span data-ttu-id="f50d9-164">Предотвращает удаление заблокированного пакета подготовки.</span><span class="sxs-lookup"><span data-stu-id="f50d9-164">Prevents anyone from removing this locked down provisioning package.</span></span>                                                           |
   |     <span data-ttu-id="f50d9-165">Политики/система/AllowLocation</span><span class="sxs-lookup"><span data-stu-id="f50d9-165">Policies/System/AllowLocation</span></span>                       |     <span data-ttu-id="f50d9-166">Нет</span><span class="sxs-lookup"><span data-stu-id="f50d9-166">No</span></span>                            |     <span data-ttu-id="f50d9-167">Предотвращает попытки устройства к отслеживанию данных расположения.</span><span class="sxs-lookup"><span data-stu-id="f50d9-167">Prevents the device from trying to track location data.</span></span>                                                                        |
   |     <span data-ttu-id="f50d9-168">Политики/WiFi/Алловвифи</span><span class="sxs-lookup"><span data-stu-id="f50d9-168">Policies/WiFi/AllowWiFi</span></span>                             |     <span data-ttu-id="f50d9-169">Нет</span><span class="sxs-lookup"><span data-stu-id="f50d9-169">No</span></span>                            |     <span data-ttu-id="f50d9-170">Отключает Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="f50d9-170">Disables Wi-Fi</span></span>                                                                                                                 |

1. <span data-ttu-id="f50d9-171">В разделе Параметры среды выполнения выберите **учетные записи/пользователи/имя пользователя: Холо/пароль**.</span><span class="sxs-lookup"><span data-stu-id="f50d9-171">Under Runtime Settings, Select **Accounts / Users / UserName: Holo / Password**.</span></span>

   <span data-ttu-id="f50d9-172">Запишите пароль и при необходимости сбросьте его.</span><span class="sxs-lookup"><span data-stu-id="f50d9-172">Note the password and reset if desired.</span></span>

1. <span data-ttu-id="f50d9-173">Перейдите в раздел Универсалаппинсталл/Усерконтекстапп и [Настройте бизнес-приложение](app-deploy-provisioning-package.md) , которое будет развертываться на этих устройствах.</span><span class="sxs-lookup"><span data-stu-id="f50d9-173">Navigate to UniversalAppInstall / UserContextApp and [configure the LOB app](app-deploy-provisioning-package.md) you will be deploying to these devices.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="f50d9-174">![Снимок экрана добавления приложения в WCD.](images/offline-secure-sample-wcd-usercontextapp2.png)</span><span class="sxs-lookup"><span data-stu-id="f50d9-174">![Screenshot of where to add your app in WCD.](images/offline-secure-sample-wcd-usercontextapp2.png)</span></span>

1. <span data-ttu-id="f50d9-175">После завершения нажмите кнопку "экспорт" и следуйте всем запросам, пока не будет создан пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="f50d9-175">Once complete, select the “Export” button and follow all prompts until your provisioning package is created.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="f50d9-176">![Снимок экрана кнопки экспорта для этого пакета в WCD.](images/offline-secure-sample-wcd-export.png)</span><span class="sxs-lookup"><span data-stu-id="f50d9-176">![Screenshot of the Export button for this package in WCD.](images/offline-secure-sample-wcd-export.png)</span></span>

## <a name="deploy"></a><span data-ttu-id="f50d9-177">Развертывание</span><span class="sxs-lookup"><span data-stu-id="f50d9-177">Deploy</span></span>

1. <span data-ttu-id="f50d9-178">Подключите HL2 к компьютеру с Windows 10 через USB-кабель.</span><span class="sxs-lookup"><span data-stu-id="f50d9-178">Connect the HL2 to your Windows 10 PC via USB cable.</span></span>
1. <span data-ttu-id="f50d9-179">Запустите инструмент ARC и выберите **HoloLens 2** .</span><span class="sxs-lookup"><span data-stu-id="f50d9-179">Launch the ARC tool and select **HoloLens 2**</span></span>

   ![Начальный экран очистки HoloLens 2](images/ARC2.png)

1. <span data-ttu-id="f50d9-181">На следующем экране выберите **Ручное выделение пакетов**.</span><span class="sxs-lookup"><span data-stu-id="f50d9-181">On the next screen select **Manual package selection**.</span></span>

   ![Экран сведений о дуги HoloLens 2](images/arc_device_info.png)

1. <span data-ttu-id="f50d9-183">Перейдите к ранее скачанному файлу. ФФУ и выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="f50d9-183">Navigate to the previously downloaded .ffu file, and select **Open**.</span></span>
1. <span data-ttu-id="f50d9-184">На странице предупреждения нажмите кнопку **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="f50d9-184">At the Warning page select **Continue**.</span></span>

   ![Экран предупреждения по ДУГЕ HoloLens 2](images/arc_warning.png)

1. <span data-ttu-id="f50d9-186">Подождите, пока средство ARC завершит установку ОС HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="f50d9-186">Wait for the ARC tool to complete the HoloLens 2 OS install.</span></span>
1. <span data-ttu-id="f50d9-187">Когда устройство завершит установку и загрузит резервную копию, с компьютера перейдите в проводник и Скопируйте сохраненный ранее файл PPKG в папку Device.</span><span class="sxs-lookup"><span data-stu-id="f50d9-187">Once the device completes the install and boots back up, from your PC navigate to File Explorer and copy the previously saved PPKG file over to the device folder.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="f50d9-188">![PPKG файл на компьютере в окне проводника.](images/offline-secure-file-explorer.png)</span><span class="sxs-lookup"><span data-stu-id="f50d9-188">![PPKG file on PC in File Explorer window.](images/offline-secure-file-explorer.png)</span></span>

1. <span data-ttu-id="f50d9-189">В HoloLens 2 нажмите приведенную ниже кнопку со списком, чтобы запустить пакет подготовки: **одновременно коснитесь** **кнопки питания** .</span><span class="sxs-lookup"><span data-stu-id="f50d9-189">On the HoloLens 2, press the following button combo to run the Provisioning Package: Tap **Volume Down** and **Power Button** at the same time.</span></span>
1. <span data-ttu-id="f50d9-190">Появится запрос на применение пакета подготовки, нажмите кнопку **подтвердить** .</span><span class="sxs-lookup"><span data-stu-id="f50d9-190">You will be prompted to apply the Provisioning Package, select **Confirm**</span></span>
1. <span data-ttu-id="f50d9-191">После завершения пакета подготовки нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f50d9-191">Once the provisioning package completes select **OK**.</span></span>
1. <span data-ttu-id="f50d9-192">После этого вам будет предложено войти на устройство с общей локальной учетной записью и паролем.</span><span class="sxs-lookup"><span data-stu-id="f50d9-192">You should then be prompted to sign into the device with the shared local account and password.</span></span>

## <a name="maintain"></a><span data-ttu-id="f50d9-193">Техническое обслуживание</span><span class="sxs-lookup"><span data-stu-id="f50d9-193">Maintain</span></span>

<span data-ttu-id="f50d9-194">В этой конфигурации рекомендуется перезапустить процесс выше и восстановить устройство с помощью инструмента ARC и применить новый PPKG, чтобы внести изменения в ОС и (или) приложения.</span><span class="sxs-lookup"><span data-stu-id="f50d9-194">With this configuration, it is recommended to restart the process above and reflash the device with the ARC tool and apply a new PPKG to make any updates to the OS and/or application(s).</span></span>
