---
title: Распространенные сценарии — автономный безопасный HoloLens 2
description: Узнайте, как настроить сценарий автономного безопасного развертывания и развертывания приложений с помощью программы предоставления устройств HoloLens.
keywords: HoloLens, управление, автономный режим, защита в автономном режиме
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
ms.openlocfilehash: 03003995f1e63708652955e6217e506d53555c1b
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283420"
---
# <span data-ttu-id="5535d-104">Распространенные сценарии — автономный безопасный holoLens 2</span><span class="sxs-lookup"><span data-stu-id="5535d-104">Common Scenarios – Offline Secure HoloLens 2</span></span>

## <span data-ttu-id="5535d-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="5535d-105">Overview</span></span>

<span data-ttu-id="5535d-106">В этом руководстве содержится руководство по использованию примера пакета подготовка, который блокирует HoloLens 2 для использования в безопасных средах со следующими ограничениями:</span><span class="sxs-lookup"><span data-stu-id="5535d-106">This guide provides guidance for applying a sample Provisioning Package that will lock down a HoloLens 2 for use in secure environments with the following restrictions:</span></span>
-   <span data-ttu-id="5535d-107">Отключать Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="5535d-107">Disable WiFi.</span></span>
-   <span data-ttu-id="5535d-108">Отключать BlueTooth.</span><span class="sxs-lookup"><span data-stu-id="5535d-108">Disable BlueTooth.</span></span>
-   <span data-ttu-id="5535d-109">Отключать микрофоны.</span><span class="sxs-lookup"><span data-stu-id="5535d-109">Disable Microphones.</span></span>
-   <span data-ttu-id="5535d-110">Предотвращает добавление или удаление пакетов подготовка.</span><span class="sxs-lookup"><span data-stu-id="5535d-110">Prevents adding or removing provisioning packages.</span></span>
-   <span data-ttu-id="5535d-111">Ни один пользователь не может включить какие-либо из вышеуказанных ограниченных компонентов.</span><span class="sxs-lookup"><span data-stu-id="5535d-111">No user can enable any of the above restricted components.</span></span>

## <span data-ttu-id="5535d-112">Подготовка</span><span class="sxs-lookup"><span data-stu-id="5535d-112">Prepare</span></span>

<span data-ttu-id="5535d-113">Установка компьютера с Windows 10</span><span class="sxs-lookup"><span data-stu-id="5535d-113">Windows 10 PC Setup</span></span>
1. <span data-ttu-id="5535d-114">[Скачайте последний файл ОС HoloLens 2](https://aka.ms/hololens2download) непосредственно на компьютер.</span><span class="sxs-lookup"><span data-stu-id="5535d-114">[Download the latest HoloLens 2 OS file](https://aka.ms/hololens2download) directly to a PC.</span></span> 
   1. <span data-ttu-id="5535d-115">Поддержка этой конфигурации включена в сборку 19041.1117 и выше.</span><span class="sxs-lookup"><span data-stu-id="5535d-115">Support for this configuration is included in Build 19041.1117 and above.</span></span>
1. <span data-ttu-id="5535d-116">Скачивание и установка средства Advanced Recovery Companion(ARC) из [Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) на компьютер</span><span class="sxs-lookup"><span data-stu-id="5535d-116">Download/Install the Advanced Recovery Companion(ARC) tool [from the Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) to your PC</span></span>
1. <span data-ttu-id="5535d-117">Скачайте и установите последнюю версию конструктора конфигураций [Windows (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) из Microsoft Store на компьютер.</span><span class="sxs-lookup"><span data-stu-id="5535d-117">Download/Install the latest [Windows Configuration Designer (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) tool from the Microsoft Store to your PC.</span></span>
1. <span data-ttu-id="5535d-118">[Загрузите OfflineSecureHL2_Sample папку с файлами проекта](https://aka.ms/HoloLensDocs-SecureOfflineSample) для сборки PPKG.</span><span class="sxs-lookup"><span data-stu-id="5535d-118">[Download the OfflineSecureHL2_Sample folder with the project files](https://aka.ms/HoloLensDocs-SecureOfflineSample) to build the PPKG.</span></span>
1. <span data-ttu-id="5535d-119">Подготовьте [автономное бизнес-приложение для развертывания PPKG.](app-deploy-provisioning-package.md)</span><span class="sxs-lookup"><span data-stu-id="5535d-119">Prepare your offline [Line of Business application for PPKG deployment](app-deploy-provisioning-package.md).</span></span> 


## <span data-ttu-id="5535d-120">Настройка</span><span class="sxs-lookup"><span data-stu-id="5535d-120">Configure</span></span>

<span data-ttu-id="5535d-121">Создание пакета безопасной настройки</span><span class="sxs-lookup"><span data-stu-id="5535d-121">Build a Secure Configuration Provisioning Package</span></span>

1. <span data-ttu-id="5535d-122">Запустите средство WCD на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5535d-122">Launch the WCD tool on your PC.</span></span>
1. <span data-ttu-id="5535d-123">Select **File -> Open project**.</span><span class="sxs-lookup"><span data-stu-id="5535d-123">Select **File -> Open project**.</span></span>
  1. <span data-ttu-id="5535d-124">Перейдите к расположению ранее сохраненной OfflineSecureHL2_Sample и выберите: OfflineSecureHL2_Sample.icdproj.xml</span><span class="sxs-lookup"><span data-stu-id="5535d-124">Navigate to the location of the previously saved OfflineSecureHL2_Sample folder, and select: OfflineSecureHL2_Sample.icdproj.xml</span></span>
1. <span data-ttu-id="5535d-125">Проект должен открыться, и теперь у вас должен быть список доступных настроек:</span><span class="sxs-lookup"><span data-stu-id="5535d-125">The project should open and you should now have a list of Available Customizations:</span></span> 

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана: пакет конфигурации, открытый в WCD](images/offline-secure-sample-wcd.png)

<span data-ttu-id="5535d-127">Конфигурации, заданная в этом пакете предоставления:</span><span class="sxs-lookup"><span data-stu-id="5535d-127">Configurations set in this provisioning package:</span></span>

|     <span data-ttu-id="5535d-128">Элемент</span><span class="sxs-lookup"><span data-stu-id="5535d-128">Item</span></span>                                                |     <span data-ttu-id="5535d-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="5535d-129">Setting</span></span>                       |     <span data-ttu-id="5535d-130">Описание</span><span class="sxs-lookup"><span data-stu-id="5535d-130">Description</span></span>                                                                                                                    |
|---------------------------------------------------------|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
|     <span data-ttu-id="5535d-131">Учетные записи и пользователи</span><span class="sxs-lookup"><span data-stu-id="5535d-131">Accounts / Users</span></span>                                    |     <span data-ttu-id="5535d-132">Локальный пароль & пользователя</span><span class="sxs-lookup"><span data-stu-id="5535d-132">Local User Name & Password</span></span>    |     <span data-ttu-id="5535d-133">Для таких автономных устройств необходимо установить одно имя пользователя и пароль, которые будут общими для всех пользователей устройства.</span><span class="sxs-lookup"><span data-stu-id="5535d-133">For these offline devices, a single user name and password will need to be set and shared by all users of the device.</span></span>          |
|     <span data-ttu-id="5535d-134">First Experience / HoloLens / SkipCalibration</span><span class="sxs-lookup"><span data-stu-id="5535d-134">First Experience / HoloLens / SkipCalibration</span></span>       |     <span data-ttu-id="5535d-135">True</span><span class="sxs-lookup"><span data-stu-id="5535d-135">True</span></span>                          |     <span data-ttu-id="5535d-136">Пропускает калибровку только при начальной настройке устройства</span><span class="sxs-lookup"><span data-stu-id="5535d-136">Skips calibration during initial device setup only</span></span>                                                                             |
|     <span data-ttu-id="5535d-137">First Experience / HoloLens / SkipTraining</span><span class="sxs-lookup"><span data-stu-id="5535d-137">First Experience / HoloLens / SkipTraining</span></span>          |     <span data-ttu-id="5535d-138">True</span><span class="sxs-lookup"><span data-stu-id="5535d-138">True</span></span>                          |     <span data-ttu-id="5535d-139">Пропускает обучение устройств во время начальной настройки устройства</span><span class="sxs-lookup"><span data-stu-id="5535d-139">Skips device training during initial device setup</span></span>                                                                              |
|     <span data-ttu-id="5535d-140">First Experience / HoloLens / WiFi</span><span class="sxs-lookup"><span data-stu-id="5535d-140">First Experience / HoloLens / WiFi</span></span>                  |     <span data-ttu-id="5535d-141">True</span><span class="sxs-lookup"><span data-stu-id="5535d-141">True</span></span>                          |     <span data-ttu-id="5535d-142">Пропускает Wi-Fi конфигурацию во время начальной настройки устройства</span><span class="sxs-lookup"><span data-stu-id="5535d-142">Skips Wi-Fi config during initial device setup</span></span>                                                                                 |
|     <span data-ttu-id="5535d-143">Policies/Connectivity/AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="5535d-143">Policies/Connectivity/AllowBluetooth</span></span>                |     <span data-ttu-id="5535d-144">Нет</span><span class="sxs-lookup"><span data-stu-id="5535d-144">No</span></span>                            |     <span data-ttu-id="5535d-145">Отключает Bluetooth</span><span class="sxs-lookup"><span data-stu-id="5535d-145">Disables Bluetooth</span></span>                                                                                                             |
|     <span data-ttu-id="5535d-146">Policies/Experience/AllowCortana</span><span class="sxs-lookup"><span data-stu-id="5535d-146">Policies/Experience/AllowCortana</span></span>                    |     <span data-ttu-id="5535d-147">Нет</span><span class="sxs-lookup"><span data-stu-id="5535d-147">No</span></span>                            |     <span data-ttu-id="5535d-148">Отключает Кортану (чтобы устранить возможные проблемы, так как микрофоны отключены)</span><span class="sxs-lookup"><span data-stu-id="5535d-148">Disables Cortana (to eliminate potential problems since the microphones are disabled)</span></span>                                          |
|     <span data-ttu-id="5535d-149">Policies/MixedReality/MicrophoneDisabled</span><span class="sxs-lookup"><span data-stu-id="5535d-149">Policies/MixedReality/MicrophoneDisabled</span></span>            |     <span data-ttu-id="5535d-150">Да</span><span class="sxs-lookup"><span data-stu-id="5535d-150">Yes</span></span>                           |     <span data-ttu-id="5535d-151">Отключает микрофон</span><span class="sxs-lookup"><span data-stu-id="5535d-151">Disables Microphone</span></span>                                                                                                            |
|     <span data-ttu-id="5535d-152">Policies/Privacy/LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="5535d-152">Policies/Privacy/LetAppsAccessLocation</span></span>              |     <span data-ttu-id="5535d-153">Принудительное запрет</span><span class="sxs-lookup"><span data-stu-id="5535d-153">Force deny</span></span>                    |     <span data-ttu-id="5535d-154">Предотвращает попытки приложений получить доступ к данным о расположении (чтобы устранить потенциальные проблемы, так как отслеживание расположения отключено)</span><span class="sxs-lookup"><span data-stu-id="5535d-154">Prevents Apps from trying to access Location data (to eliminate potential problems since the Location tracking is disabled)</span></span>    |
|     <span data-ttu-id="5535d-155">Policies/Privacy/LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="5535d-155">Policies/Privacy/LetAppsAccessMicrophone</span></span>            |     <span data-ttu-id="5535d-156">Принудительное запрет</span><span class="sxs-lookup"><span data-stu-id="5535d-156">Force deny</span></span>                    |     <span data-ttu-id="5535d-157">Предотвращает попытки приложений получить доступ к микрофонам (чтобы устранить возможные проблемы, так как микрофоны отключены)</span><span class="sxs-lookup"><span data-stu-id="5535d-157">Prevents Apps from trying to access Microphones (to eliminate potential problems since the Microphones are disabled)</span></span>           |
|     <span data-ttu-id="5535d-158">Policies/Security/AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="5535d-158">Policies/Security/AllowAddProvisioningPackage</span></span>       |     <span data-ttu-id="5535d-159">Нет</span><span class="sxs-lookup"><span data-stu-id="5535d-159">No</span></span>                            |     <span data-ttu-id="5535d-160">Предотвращает добавление пакетов предоставления, которые могут пытаться переопредить заблокированные политики.</span><span class="sxs-lookup"><span data-stu-id="5535d-160">Prevents anyone from adding provisioning packages that might attempt to override locked down policies.</span></span>                         |
|     <span data-ttu-id="5535d-161">Policies/Security/AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="5535d-161">Policies/Security/AllowRemoveProvisioningPackage</span></span>    |     <span data-ttu-id="5535d-162">Нет</span><span class="sxs-lookup"><span data-stu-id="5535d-162">No</span></span>                            |     <span data-ttu-id="5535d-163">Предотвращает удаление этого заблокированного пакета подготовка.</span><span class="sxs-lookup"><span data-stu-id="5535d-163">Prevents anyone from removing this locked down provisioning package.</span></span>                                                           |
|     <span data-ttu-id="5535d-164">Policies/System/AllowLocation</span><span class="sxs-lookup"><span data-stu-id="5535d-164">Policies/System/AllowLocation</span></span>                       |     <span data-ttu-id="5535d-165">Нет</span><span class="sxs-lookup"><span data-stu-id="5535d-165">No</span></span>                            |     <span data-ttu-id="5535d-166">Предотвращает попытки устройства отслеживать данные о расположении.</span><span class="sxs-lookup"><span data-stu-id="5535d-166">Prevents the device from trying to track location data.</span></span>                                                                        |
|     <span data-ttu-id="5535d-167">Policies/WiFi/AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="5535d-167">Policies/WiFi/AllowWiFi</span></span>                             |     <span data-ttu-id="5535d-168">Нет</span><span class="sxs-lookup"><span data-stu-id="5535d-168">No</span></span>                            |     <span data-ttu-id="5535d-169">Отключает Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="5535d-169">Disables Wi-Fi</span></span>                                                                                                                 |

4. <span data-ttu-id="5535d-170">В области "Параметры времени работы" выберите **"Учетные записи/ Пользователи/ Имя пользователя: Holo / Пароль"**</span><span class="sxs-lookup"><span data-stu-id="5535d-170">Under Runtime Settings, Select **Accounts / Users / UserName: Holo / Password**</span></span> 
    - <span data-ttu-id="5535d-171">При желании заметьте пароль и сброс.</span><span class="sxs-lookup"><span data-stu-id="5535d-171">Note the password and reset if desired.</span></span>
5. <span data-ttu-id="5535d-172">Перейдите к universalAppInstall / UserContextApp и настройте приложение [для](app-deploy-provisioning-package.md) развертывания на этих устройствах.</span><span class="sxs-lookup"><span data-stu-id="5535d-172">Navigate to UniversalAppInstall / UserContextApp and [configure the LOB app](app-deploy-provisioning-package.md) you will be deploying to these devices.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана: место добавления приложения в WCD.](images/offline-secure-sample-wcd-usercontextapp.png)

6. <span data-ttu-id="5535d-174">После завершения выберите кнопку "Экспорт" и следуйте всем запросам, пока пакет подготовка не будет создан.</span><span class="sxs-lookup"><span data-stu-id="5535d-174">Once complete, select the “Export” button and follow all prompts until your provisioning package is created.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана с кнопкой "Экспорт" для этого пакета в WCD.](images/offline-secure-sample-wcd-export.png)


## <span data-ttu-id="5535d-176">Развертывание</span><span class="sxs-lookup"><span data-stu-id="5535d-176">Deploy</span></span>

1. <span data-ttu-id="5535d-177">Подключите HL2 к компьютеру с Windows 10 через USB-кабель.</span><span class="sxs-lookup"><span data-stu-id="5535d-177">Connect the HL2 to your Windows 10 PC via USB cable.</span></span>
1. <span data-ttu-id="5535d-178">Запустите средство ARC и выберите **HoloLens 2**</span><span class="sxs-lookup"><span data-stu-id="5535d-178">Launch the ARC tool and select **HoloLens 2**</span></span>

   <img src=images/offline-secure-arc-1.png alt=arc1 width="577" height="322" />

1. <span data-ttu-id="5535d-179">На следующем экране выберите выбор **пакета вручную.**</span><span class="sxs-lookup"><span data-stu-id="5535d-179">On the next screen select **Manual package selection**.</span></span>
   
   <img src=images/offline-secure-arc-2.png alt=arc2 width="577" height="322" />

1. <span data-ttu-id="5535d-180">Перейдите к ранее загруженным FFU-файлу и выберите **"Открыть".**</span><span class="sxs-lookup"><span data-stu-id="5535d-180">Navigate to the previously downloaded .ffu file, and select **Open**.</span></span>
1. <span data-ttu-id="5535d-181">На странице предупреждения выберите **"Продолжить"**.</span><span class="sxs-lookup"><span data-stu-id="5535d-181">At the Warning page select **Continue**.</span></span>

   <img src=images/offline-secure-arc-3.png alt=arc3 width="577" height="322" />

1. <span data-ttu-id="5535d-182">Подождите, пока инструмент ARC завершит установку ОС HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="5535d-182">Wait for the ARC tool to complete the HoloLens 2 OS install.</span></span>
1. <span data-ttu-id="5535d-183">После завершения установки и загрузки устройства перейдите с компьютера в проводник и скопируйте ранее сохраненный файл PPKG в папку устройства.</span><span class="sxs-lookup"><span data-stu-id="5535d-183">Once the device completes the install and boots back up, from your PC navigate to File Explorer and copy the previously saved PPKG file over to the device folder.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Файл PPKG на компьютере в окне проводника.](images/offline-secure-file-explorer.png)

1. <span data-ttu-id="5535d-185">На HoloLens 2 нажмите следующую кнопку со combo \*\*\*\* для одновременного запуска пакета подготовка: коснитесь кнопки "Громкость вниз" и **"Кнопка питания".**</span><span class="sxs-lookup"><span data-stu-id="5535d-185">On the HoloLens 2, press the following button combo to run the Provisioning Package: Tap **Volume Down** and **Power Button** at the same time.</span></span>
1. <span data-ttu-id="5535d-186">Вам будет предложено применить пакет предоставления, выберите **"Подтвердить"**</span><span class="sxs-lookup"><span data-stu-id="5535d-186">You will be prompted to apply the Provisioning Package, select **Confirm**</span></span>
1. <span data-ttu-id="5535d-187">После завершения пакета подготовка выберите **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="5535d-187">Once the provisioning package completes select **OK**.</span></span>
1. <span data-ttu-id="5535d-188">После этого вам будет предложено войти на устройство с помощью общей локальной учетной записи и пароля.</span><span class="sxs-lookup"><span data-stu-id="5535d-188">You should then be prompted to sign into the device with the shared local account and password.</span></span>

## <span data-ttu-id="5535d-189">Обслуживание</span><span class="sxs-lookup"><span data-stu-id="5535d-189">Maintain</span></span>

<span data-ttu-id="5535d-190">При такой конфигурации рекомендуется перезапустить процесс выше и перезапустить устройство с помощью инструмента ARC и применить новый PPKG для внесения любых обновлений в ОС и/или приложениях.</span><span class="sxs-lookup"><span data-stu-id="5535d-190">With this configuration, it is recommended to restart the process above and reflash the device with the ARC tool and apply a new PPKG to make any updates to the OS and/or application(s).</span></span> 

