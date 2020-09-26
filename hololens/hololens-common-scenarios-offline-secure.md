---
title: 'Распространенные сценарии: автономная служба Secure HoloLens 2'
description: Безопасное развертывание и развертывание приложений в автономном режиме с помощью подготовки.
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
ms.openlocfilehash: d53f9ce19b020a866770b756dde6ab97b8331362
ms.sourcegitcommit: e6885d03c980b33dd0bab5c418cbd1892d5ff123
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2020
ms.locfileid: "11080529"
---
# <span data-ttu-id="06b7b-104">Распространенные сценарии: автономная служба Secure HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="06b7b-104">Common Scenarios – Offline Secure HoloLens 2</span></span>

## <span data-ttu-id="06b7b-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="06b7b-105">Overview</span></span>
<span data-ttu-id="06b7b-106">Это руководство содержит рекомендации по применению примера пакета подготовки, который блокирует использование HoloLens 2 для использования в защищенных средах со следующими ограничениями:</span><span class="sxs-lookup"><span data-stu-id="06b7b-106">This guide provides guidance for applying a sample Provisioning Package that will lock down a HoloLens 2 for use in secure environments with the following restrictions:</span></span>
-   <span data-ttu-id="06b7b-107">Отключите WiFi.</span><span class="sxs-lookup"><span data-stu-id="06b7b-107">Disable WiFi.</span></span>
-   <span data-ttu-id="06b7b-108">Отключите BlueTooth.</span><span class="sxs-lookup"><span data-stu-id="06b7b-108">Disable BlueTooth.</span></span>
-   <span data-ttu-id="06b7b-109">Отключить микрофоны.</span><span class="sxs-lookup"><span data-stu-id="06b7b-109">Disable Microphones.</span></span>
-   <span data-ttu-id="06b7b-110">Запрещает добавление и удаление пакетов подготовки.</span><span class="sxs-lookup"><span data-stu-id="06b7b-110">Prevents adding or removing provisioning packages.</span></span>
-   <span data-ttu-id="06b7b-111">Ни один пользователь не может включить ни один из перечисленных выше компонентов.</span><span class="sxs-lookup"><span data-stu-id="06b7b-111">No user can enable any of the above restricted components.</span></span>

## <span data-ttu-id="06b7b-112">Подготовка</span><span class="sxs-lookup"><span data-stu-id="06b7b-112">Prepare</span></span> 
<span data-ttu-id="06b7b-113">Настройка компьютеров с Windows 10</span><span class="sxs-lookup"><span data-stu-id="06b7b-113">Windows 10 PC Setup</span></span>
1. <span data-ttu-id="06b7b-114">[Загрузи последнюю версию файла операционной системы HoloLens 2](https://aka.ms/hololens2download) на компьютер напрямую.</span><span class="sxs-lookup"><span data-stu-id="06b7b-114">[Download the latest HoloLens 2 OS file](https://aka.ms/hololens2download) directly to a PC.</span></span> 
   1. <span data-ttu-id="06b7b-115">Поддержка этой конфигурации включена в сборку 19041,1117 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="06b7b-115">Support for this configuration is included in Build 19041.1117 and above.</span></span>
1. <span data-ttu-id="06b7b-116">Скачивание и установка средства "расширенного помощника по восстановлению" [из магазина Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) на компьютер</span><span class="sxs-lookup"><span data-stu-id="06b7b-116">Download/Install the Advanced Recovery Companion(ARC) tool [from the Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) to your PC</span></span>
1. <span data-ttu-id="06b7b-117">Скачайте и установите последнюю версию средства [разработки конфигурации Windows (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) из магазина Microsoft Store на компьютер.</span><span class="sxs-lookup"><span data-stu-id="06b7b-117">Download/Install the latest [Windows Configuration Designer (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) tool from the Microsoft Store to your PC.</span></span>
1. <span data-ttu-id="06b7b-118">[Скачайте папку OfflineSecureHL2_Sample с файлами проекта](https://aka.ms/HoloLensDocs-SecureOfflineSample) , чтобы создать PPKG.</span><span class="sxs-lookup"><span data-stu-id="06b7b-118">[Download the OfflineSecureHL2_Sample folder with the project files](https://aka.ms/HoloLensDocs-SecureOfflineSample) to build the PPKG.</span></span>
1. <span data-ttu-id="06b7b-119">Подготовка автономной [строки бизнес-приложения для PPKG развертывания](app-deploy-provisioning-package.md).</span><span class="sxs-lookup"><span data-stu-id="06b7b-119">Prepare your offline [Line of Business application for PPKG deployment](app-deploy-provisioning-package.md).</span></span> 


## <span data-ttu-id="06b7b-120">Настройка</span><span class="sxs-lookup"><span data-stu-id="06b7b-120">Configure</span></span>
<span data-ttu-id="06b7b-121">Создание пакета обеспечения безопасной конфигурации</span><span class="sxs-lookup"><span data-stu-id="06b7b-121">Build a Secure Configuration Provisioning Package</span></span>

1. <span data-ttu-id="06b7b-122">Запустите средство WCD на компьютере.</span><span class="sxs-lookup"><span data-stu-id="06b7b-122">Launch the WCD tool on your PC.</span></span>
1. <span data-ttu-id="06b7b-123">Выберите **файл-> открыть проект**.</span><span class="sxs-lookup"><span data-stu-id="06b7b-123">Select **File -> Open project**.</span></span>
  1. <span data-ttu-id="06b7b-124">Перейдите к расположению ранее сохраненной OfflineSecureHL2_Sample папки, а затем выберите: OfflineSecureHL2_Sample.icdproj.xml</span><span class="sxs-lookup"><span data-stu-id="06b7b-124">Navigate to the location of the previously saved OfflineSecureHL2_Sample folder, and select: OfflineSecureHL2_Sample.icdproj.xml</span></span>
1. <span data-ttu-id="06b7b-125">Проект должен открыться, и теперь у вас должен быть список доступных настроек.</span><span class="sxs-lookup"><span data-stu-id="06b7b-125">The project should open and you should now have a list of Available Customizations:</span></span> 

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана: пакет конфигурации открыт в WCD](images/offline-secure-sample-wcd.png)

<span data-ttu-id="06b7b-127">Конфигурации, настроенные в этом пакете подготовки:</span><span class="sxs-lookup"><span data-stu-id="06b7b-127">Configurations set in this provisioning package:</span></span>

|     <span data-ttu-id="06b7b-128">Элемент</span><span class="sxs-lookup"><span data-stu-id="06b7b-128">Item</span></span>                                                |     <span data-ttu-id="06b7b-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="06b7b-129">Setting</span></span>                       |     <span data-ttu-id="06b7b-130">Описание</span><span class="sxs-lookup"><span data-stu-id="06b7b-130">Description</span></span>                                                                                                                    |
|---------------------------------------------------------|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
|     <span data-ttu-id="06b7b-131">Учетные записи и пользователи</span><span class="sxs-lookup"><span data-stu-id="06b7b-131">Accounts / Users</span></span>                                    |     <span data-ttu-id="06b7b-132">Имя локального пользователя & паролем</span><span class="sxs-lookup"><span data-stu-id="06b7b-132">Local User Name & Password</span></span>    |     <span data-ttu-id="06b7b-133">Для этих автономных устройств необходимо настроить одно имя пользователя и пароль, чтобы они были доступны всем пользователям устройства.</span><span class="sxs-lookup"><span data-stu-id="06b7b-133">For these offline devices, a single user name and password will need to be set and shared by all users of the device.</span></span>          |
|     <span data-ttu-id="06b7b-134">Первый опыт/HoloLens/SkipCalibration</span><span class="sxs-lookup"><span data-stu-id="06b7b-134">First Experience / HoloLens / SkipCalibration</span></span>       |     <span data-ttu-id="06b7b-135">True</span><span class="sxs-lookup"><span data-stu-id="06b7b-135">True</span></span>                          |     <span data-ttu-id="06b7b-136">Пропуск калибровки только на начальном этапе настройки устройства</span><span class="sxs-lookup"><span data-stu-id="06b7b-136">Skips calibration during initial device setup only</span></span>                                                                             |
|     <span data-ttu-id="06b7b-137">Первый опыт/HoloLens/SkipTraining</span><span class="sxs-lookup"><span data-stu-id="06b7b-137">First Experience / HoloLens / SkipTraining</span></span>          |     <span data-ttu-id="06b7b-138">True</span><span class="sxs-lookup"><span data-stu-id="06b7b-138">True</span></span>                          |     <span data-ttu-id="06b7b-139">Пропускает обучение устройства во время первоначальной настройки устройства</span><span class="sxs-lookup"><span data-stu-id="06b7b-139">Skips device training during initial device setup</span></span>                                                                              |
|     <span data-ttu-id="06b7b-140">Первый опыт/HoloLens/WiFi</span><span class="sxs-lookup"><span data-stu-id="06b7b-140">First Experience / HoloLens / WiFi</span></span>                  |     <span data-ttu-id="06b7b-141">True</span><span class="sxs-lookup"><span data-stu-id="06b7b-141">True</span></span>                          |     <span data-ttu-id="06b7b-142">Пропускает конфигурацию Wi-Fi во время первоначальной настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="06b7b-142">Skips Wi-Fi config during initial device setup</span></span>                                                                                 |
|     <span data-ttu-id="06b7b-143">Политики/подключение/AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="06b7b-143">Policies/Connectivity/AllowBluetooth</span></span>                |     <span data-ttu-id="06b7b-144">Нет</span><span class="sxs-lookup"><span data-stu-id="06b7b-144">No</span></span>                            |     <span data-ttu-id="06b7b-145">Отключение Bluetooth</span><span class="sxs-lookup"><span data-stu-id="06b7b-145">Disables Bluetooth</span></span>                                                                                                             |
|     <span data-ttu-id="06b7b-146">Политики/опыт/AllowCortana</span><span class="sxs-lookup"><span data-stu-id="06b7b-146">Policies/Experience/AllowCortana</span></span>                    |     <span data-ttu-id="06b7b-147">Нет</span><span class="sxs-lookup"><span data-stu-id="06b7b-147">No</span></span>                            |     <span data-ttu-id="06b7b-148">Отключение Кортаны (для устранения потенциальных проблем, так как микрофон отключен)</span><span class="sxs-lookup"><span data-stu-id="06b7b-148">Disables Cortana (to eliminate potential problems since the microphones are disabled)</span></span>                                          |
|     <span data-ttu-id="06b7b-149">Политики/MixedReality/MicrophoneDisabled</span><span class="sxs-lookup"><span data-stu-id="06b7b-149">Policies/MixedReality/MicrophoneDisabled</span></span>            |     <span data-ttu-id="06b7b-150">Да</span><span class="sxs-lookup"><span data-stu-id="06b7b-150">Yes</span></span>                           |     <span data-ttu-id="06b7b-151">Отключение микрофона</span><span class="sxs-lookup"><span data-stu-id="06b7b-151">Disables Microphone</span></span>                                                                                                            |
|     <span data-ttu-id="06b7b-152">Политики/конфиденциальность/LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="06b7b-152">Policies/Privacy/LetAppsAccessLocation</span></span>              |     <span data-ttu-id="06b7b-153">Запретить принудительно</span><span class="sxs-lookup"><span data-stu-id="06b7b-153">Force deny</span></span>                    |     <span data-ttu-id="06b7b-154">Приложение не пытается получить доступ к данным о расположении (для устранения потенциальных проблем, так как отслеживание расположения отключено)</span><span class="sxs-lookup"><span data-stu-id="06b7b-154">Prevents Apps from trying to access Location data (to eliminate potential problems since the Location tracking is disabled)</span></span>    |
|     <span data-ttu-id="06b7b-155">Политики/конфиденциальность/LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="06b7b-155">Policies/Privacy/LetAppsAccessMicrophone</span></span>            |     <span data-ttu-id="06b7b-156">Запретить принудительно</span><span class="sxs-lookup"><span data-stu-id="06b7b-156">Force deny</span></span>                    |     <span data-ttu-id="06b7b-157">Запрещает приложениям получать доступ к микрофонам (для устранения потенциальных проблем, так как микрофон отключен)</span><span class="sxs-lookup"><span data-stu-id="06b7b-157">Prevents Apps from trying to access Microphones (to eliminate potential problems since the Microphones are disabled)</span></span>           |
|     <span data-ttu-id="06b7b-158">Политики/безопасность/AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="06b7b-158">Policies/Security/AllowAddProvisioningPackage</span></span>       |     <span data-ttu-id="06b7b-159">Нет</span><span class="sxs-lookup"><span data-stu-id="06b7b-159">No</span></span>                            |     <span data-ttu-id="06b7b-160">Запрещает любому пользователю добавлять пакеты подготовки, которые могут попытаться переопределить заблокированные политики.</span><span class="sxs-lookup"><span data-stu-id="06b7b-160">Prevents anyone from adding provisioning packages that might attempt to override locked down policies.</span></span>                         |
|     <span data-ttu-id="06b7b-161">Политики/безопасность/AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="06b7b-161">Policies/Security/AllowRemoveProvisioningPackage</span></span>    |     <span data-ttu-id="06b7b-162">Нет</span><span class="sxs-lookup"><span data-stu-id="06b7b-162">No</span></span>                            |     <span data-ttu-id="06b7b-163">Запрещает всем пользователям удалять этот заблокированный пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="06b7b-163">Prevents anyone from removing this locked down provisioning package.</span></span>                                                           |
|     <span data-ttu-id="06b7b-164">Политики/система/AllowLocation</span><span class="sxs-lookup"><span data-stu-id="06b7b-164">Policies/System/AllowLocation</span></span>                       |     <span data-ttu-id="06b7b-165">Нет</span><span class="sxs-lookup"><span data-stu-id="06b7b-165">No</span></span>                            |     <span data-ttu-id="06b7b-166">Предотвращает попытки устройства отслеживать данные о местоположении.</span><span class="sxs-lookup"><span data-stu-id="06b7b-166">Prevents the device from trying to track location data.</span></span>                                                                        |
|     <span data-ttu-id="06b7b-167">Политики/WiFi/AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="06b7b-167">Policies/WiFi/AllowWiFi</span></span>                             |     <span data-ttu-id="06b7b-168">Нет</span><span class="sxs-lookup"><span data-stu-id="06b7b-168">No</span></span>                            |     <span data-ttu-id="06b7b-169">Отключение Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="06b7b-169">Disables Wi-Fi</span></span>                                                                                                                 |

4. <span data-ttu-id="06b7b-170">В разделе Параметры среды выполнения выберите **учетные записи/пользователи/имя пользователя: Holo и пароль.**</span><span class="sxs-lookup"><span data-stu-id="06b7b-170">Under Runtime Settings, Select **Accounts / Users / UserName: Holo / Password**</span></span> 
    - <span data-ttu-id="06b7b-171">Запишите пароль и при необходимости измените его.</span><span class="sxs-lookup"><span data-stu-id="06b7b-171">Note the password and reset if desired.</span></span>
5. <span data-ttu-id="06b7b-172">Перейдите на UniversalAppInstall/UserContextApp и [Настройте бизнес-приложение](app-deploy-provisioning-package.md) , которое будет развертываться на этих устройствах.</span><span class="sxs-lookup"><span data-stu-id="06b7b-172">Navigate to UniversalAppInstall / UserContextApp and [configure the LOB app](app-deploy-provisioning-package.md) you will be deploying to these devices.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана, на котором показано, как добавить приложение в WCD.](images/offline-secure-sample-wcd-usercontextapp.png)

6. <span data-ttu-id="06b7b-174">После завершения нажмите кнопку "экспорт" и выполняйте все запросы, пока не будет создан пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="06b7b-174">Once complete, select the “Export” button and follow all prompts until your provisioning package is created.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана: кнопка "экспорт" для этого пакета в WCD.](images/offline-secure-sample-wcd-export.png)


## <span data-ttu-id="06b7b-176">Развертывание</span><span class="sxs-lookup"><span data-stu-id="06b7b-176">Deploy</span></span>
1. <span data-ttu-id="06b7b-177">Подключите HL2 к компьютеру с Windows 10 через USB-кабель.</span><span class="sxs-lookup"><span data-stu-id="06b7b-177">Connect the HL2 to your Windows 10 PC via USB cable.</span></span>
1. <span data-ttu-id="06b7b-178">Запуск инструмента "Дуга" и выбор **HoloLens 2**</span><span class="sxs-lookup"><span data-stu-id="06b7b-178">Launch the ARC tool and select **HoloLens 2**</span></span>

   <img src=images/offline-secure-arc-1.png alt=arc1 width="577" height="322" />

1. <span data-ttu-id="06b7b-179">На следующем экране выберите **ручной набор пакетов**.</span><span class="sxs-lookup"><span data-stu-id="06b7b-179">On the next screen select **Manual package selection**.</span></span>
   
   <img src=images/offline-secure-arc-2.png alt=arc2 width="577" height="322" />

1. <span data-ttu-id="06b7b-180">Перейдите к ранее загруженному FFU файлу и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="06b7b-180">Navigate to the previously downloaded .ffu file, and select **Open**.</span></span>
1. <span data-ttu-id="06b7b-181">На странице предупреждения нажмите кнопку **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="06b7b-181">At the Warning page select **Continue**.</span></span>

   <img src=images/offline-secure-arc-3.png alt=arc3 width="577" height="322" />

1. <span data-ttu-id="06b7b-182">Дождитесь завершения установки системы HoloLens 2 OS.</span><span class="sxs-lookup"><span data-stu-id="06b7b-182">Wait for the ARC tool to complete the HoloLens 2 OS install.</span></span>
1. <span data-ttu-id="06b7b-183">После завершения установки и загрузки устройства на компьютере перейдите в проводник и скопируйте ранее сохраненный файл PPKG в папку устройства.</span><span class="sxs-lookup"><span data-stu-id="06b7b-183">Once the device completes the install and boots back up, from your PC navigate to File Explorer and copy the previously saved PPKG file over to the device folder.</span></span>

   > [!div class="mx-imgBorder"]
   > ![PPKG файл на компьютере с Windows в проводнике.](images/offline-secure-file-explorer.png)

1. <span data-ttu-id="06b7b-185">На HoloLens 2 нажмите приведенную ниже комбинированную кнопку, чтобы запустить пакет подготовки: нажмите **кнопку "** **уменьшить громкость** " и выберите один раз.</span><span class="sxs-lookup"><span data-stu-id="06b7b-185">On the HoloLens 2, press the following button combo to run the Provisioning Package: Tap **Volume Down** and **Power Button** at the same time.</span></span>
1. <span data-ttu-id="06b7b-186">Вам будет предложено применить пакет подготовки, а затем нажмите кнопку **подтвердить** .</span><span class="sxs-lookup"><span data-stu-id="06b7b-186">You will be prompted to apply the Provisioning Package, select **Confirm**</span></span>
1. <span data-ttu-id="06b7b-187">После завершения установки пакета подготовки нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="06b7b-187">Once the provisioning package completes select **OK**.</span></span>
1. <span data-ttu-id="06b7b-188">После этого вам будет предложено войти в устройство с помощью общей локальной учетной записи и пароля.</span><span class="sxs-lookup"><span data-stu-id="06b7b-188">You should then be prompted to sign into the device with the shared local account and password.</span></span>

## <span data-ttu-id="06b7b-189">Обслуживание</span><span class="sxs-lookup"><span data-stu-id="06b7b-189">Maintain</span></span>
<span data-ttu-id="06b7b-190">В этой конфигурации рекомендуется перезапустить описанную выше процедуру и перекрасить устройство с помощью инструмента ARC и применить новый PPKG, чтобы внести изменения в операционную систему и/или приложения.</span><span class="sxs-lookup"><span data-stu-id="06b7b-190">With this configuration, it is recommended to restart the process above and reflash the device with the ARC tool and apply a new PPKG to make any updates to the OS and/or application(s).</span></span> 

