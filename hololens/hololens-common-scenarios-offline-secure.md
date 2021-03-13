---
title: Распространенные сценарии — автономные безопасные устройства HoloLens 2
description: Узнайте, как настроить сценарий автономного безопасного развертывания и развертывания приложений с помощью подготовка для устройств HoloLens.
keywords: HoloLens, управление, автономное, автономное обеспечение
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
ms.sourcegitcommit: 04b7e789fe69615a60571b769e13a01a9d7aee70
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "11407598"
---
# <a name="common-scenarios--offline-secure-hololens-2"></a><span data-ttu-id="d4ecf-104">Распространенные сценарии — автономные безопасные устройства HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="d4ecf-104">Common Scenarios – Offline Secure HoloLens 2</span></span>

## <a name="overview"></a><span data-ttu-id="d4ecf-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="d4ecf-105">Overview</span></span>

<span data-ttu-id="d4ecf-106">В этом руководстве приводится руководство по использованию примера пакета предварительного обеспечения, который блокирует HoloLens 2 для использования в безопасных средах со следующими ограничениями:</span><span class="sxs-lookup"><span data-stu-id="d4ecf-106">This guide provides guidance for applying a sample Provisioning Package that will lock down a HoloLens 2 for use in secure environments with the following restrictions:</span></span>

-   <span data-ttu-id="d4ecf-107">Отключение Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-107">Disable WiFi.</span></span>
-   <span data-ttu-id="d4ecf-108">Отключить BlueTooth.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-108">Disable BlueTooth.</span></span>
-   <span data-ttu-id="d4ecf-109">Отключить микрофоны.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-109">Disable Microphones.</span></span>
-   <span data-ttu-id="d4ecf-110">Предотвращает добавление или удаление пакетов подготовка.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-110">Prevents adding or removing provisioning packages.</span></span>
-   <span data-ttu-id="d4ecf-111">Ни один пользователь не может включить любой из вышеуказанных компонентов с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-111">No user can enable any of the above restricted components.</span></span>

## <a name="prepare"></a><span data-ttu-id="d4ecf-112">Подготовка</span><span class="sxs-lookup"><span data-stu-id="d4ecf-112">Prepare</span></span>

<span data-ttu-id="d4ecf-113">Настройка ПК в Windows 10</span><span class="sxs-lookup"><span data-stu-id="d4ecf-113">Windows 10 PC Setup</span></span>
1. <span data-ttu-id="d4ecf-114">[Скачайте последний os-файл HoloLens 2](https://aka.ms/hololens2download) непосредственно на компьютер.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-114">[Download the latest HoloLens 2 OS file](https://aka.ms/hololens2download) directly to a PC.</span></span> 
   1. <span data-ttu-id="d4ecf-115">Поддержка этой конфигурации включена в сборку 19041.1117 и выше.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-115">Support for this configuration is included in Build 19041.1117 and above.</span></span>
1. <span data-ttu-id="d4ecf-116">Загрузка и установка средства Advanced Recovery Companion (ARC) из [Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) на компьютер</span><span class="sxs-lookup"><span data-stu-id="d4ecf-116">Download/Install the Advanced Recovery Companion(ARC) tool [from the Microsoft Store](https://www.microsoft.com/store/productId/9P74Z35SFRS8) to your PC</span></span>
1. <span data-ttu-id="d4ecf-117">Скачивание и установка последнего средства конструктора конфигурации [Windows (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) из Microsoft Store на компьютер.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-117">Download/Install the latest [Windows Configuration Designer (WCD)](https://www.microsoft.com/p/windows-configuration-designer/9nblggh4tx22?activetab=pivot:overviewtab) tool from the Microsoft Store to your PC.</span></span>
1. <span data-ttu-id="d4ecf-118">[Загрузите OfflineSecureHL2_Sample папку с файлами проекта для](https://aka.ms/HoloLensDocs-SecureOfflineSample) создания PPKG.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-118">[Download the OfflineSecureHL2_Sample folder with the project files](https://aka.ms/HoloLensDocs-SecureOfflineSample) to build the PPKG.</span></span>
1. <span data-ttu-id="d4ecf-119">Подготовка автономного [приложения Line of Business для развертывания PPKG.](app-deploy-provisioning-package.md)</span><span class="sxs-lookup"><span data-stu-id="d4ecf-119">Prepare your offline [Line of Business application for PPKG deployment](app-deploy-provisioning-package.md).</span></span> 


## <a name="configure"></a><span data-ttu-id="d4ecf-120">Настройка</span><span class="sxs-lookup"><span data-stu-id="d4ecf-120">Configure</span></span>

<span data-ttu-id="d4ecf-121">Создание пакета обеспечения безопасной конфигурации</span><span class="sxs-lookup"><span data-stu-id="d4ecf-121">Build a Secure Configuration Provisioning Package</span></span>

1. <span data-ttu-id="d4ecf-122">Запустите средство WCD на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-122">Launch the WCD tool on your PC.</span></span>
1. <span data-ttu-id="d4ecf-123">Выберите **файл -> Open project**.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-123">Select **File -> Open project**.</span></span>
  1. <span data-ttu-id="d4ecf-124">Перейдите к расположению сохраненной ранее OfflineSecureHL2_Sample и выберите: OfflineSecureHL2_Sample.icdproj.xml</span><span class="sxs-lookup"><span data-stu-id="d4ecf-124">Navigate to the location of the previously saved OfflineSecureHL2_Sample folder, and select: OfflineSecureHL2_Sample.icdproj.xml</span></span>
1. <span data-ttu-id="d4ecf-125">Проект должен открыться, и теперь у вас должен быть список доступных настроек:</span><span class="sxs-lookup"><span data-stu-id="d4ecf-125">The project should open and you should now have a list of Available Customizations:</span></span>

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана пакета конфигурации, открытого в WCD](images/offline-secure-sample-wcd.png)

   <span data-ttu-id="d4ecf-127">Конфигурации, заданной в этом пакете подготовка:</span><span class="sxs-lookup"><span data-stu-id="d4ecf-127">Configurations set in this provisioning package:</span></span>
   
   |     <span data-ttu-id="d4ecf-128">Элемент</span><span class="sxs-lookup"><span data-stu-id="d4ecf-128">Item</span></span>                                                |     <span data-ttu-id="d4ecf-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="d4ecf-129">Setting</span></span>                       |     <span data-ttu-id="d4ecf-130">Описание</span><span class="sxs-lookup"><span data-stu-id="d4ecf-130">Description</span></span>                                                                                                                    |
   |---------------------------------------------------------|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
   |     <span data-ttu-id="d4ecf-131">Учетные записи / Пользователи</span><span class="sxs-lookup"><span data-stu-id="d4ecf-131">Accounts / Users</span></span>                                    |     <span data-ttu-id="d4ecf-132">Имя локального пользователя & пароль</span><span class="sxs-lookup"><span data-stu-id="d4ecf-132">Local User Name & Password</span></span>    |     <span data-ttu-id="d4ecf-133">Для этих автономных устройств необходимо установить одно имя пользователя и пароль и делиться им со всеми пользователями устройства.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-133">For these offline devices, a single user name and password will need to be set and shared by all users of the device.</span></span>          |
   |     <span data-ttu-id="d4ecf-134">Первый опыт / HoloLens / SkipCalibration</span><span class="sxs-lookup"><span data-stu-id="d4ecf-134">First Experience / HoloLens / SkipCalibration</span></span>       |     <span data-ttu-id="d4ecf-135">True</span><span class="sxs-lookup"><span data-stu-id="d4ecf-135">True</span></span>                          |     <span data-ttu-id="d4ecf-136">Пропускает калибровку только при начальной настройке устройства</span><span class="sxs-lookup"><span data-stu-id="d4ecf-136">Skips calibration during initial device setup only</span></span>                                                                             |
   |     <span data-ttu-id="d4ecf-137">First Experience / HoloLens / SkipTraining</span><span class="sxs-lookup"><span data-stu-id="d4ecf-137">First Experience / HoloLens / SkipTraining</span></span>          |     <span data-ttu-id="d4ecf-138">True</span><span class="sxs-lookup"><span data-stu-id="d4ecf-138">True</span></span>                          |     <span data-ttu-id="d4ecf-139">Пропускает обучение устройств во время начальной установки устройства</span><span class="sxs-lookup"><span data-stu-id="d4ecf-139">Skips device training during initial device setup</span></span>                                                                              |
   |     <span data-ttu-id="d4ecf-140">First Experience / HoloLens / WiFi</span><span class="sxs-lookup"><span data-stu-id="d4ecf-140">First Experience / HoloLens / WiFi</span></span>                  |     <span data-ttu-id="d4ecf-141">True</span><span class="sxs-lookup"><span data-stu-id="d4ecf-141">True</span></span>                          |     <span data-ttu-id="d4ecf-142">Пропускает Wi-Fi при начальной настройке устройства</span><span class="sxs-lookup"><span data-stu-id="d4ecf-142">Skips Wi-Fi config during initial device setup</span></span>                                                                                 |
   |     <span data-ttu-id="d4ecf-143">Политики/Подключение/AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="d4ecf-143">Policies/Connectivity/AllowBluetooth</span></span>                |     <span data-ttu-id="d4ecf-144">Нет</span><span class="sxs-lookup"><span data-stu-id="d4ecf-144">No</span></span>                            |     <span data-ttu-id="d4ecf-145">Отключение Bluetooth</span><span class="sxs-lookup"><span data-stu-id="d4ecf-145">Disables Bluetooth</span></span>                                                                                                             |
   |     <span data-ttu-id="d4ecf-146">Политики/Опыт/AllowCortana</span><span class="sxs-lookup"><span data-stu-id="d4ecf-146">Policies/Experience/AllowCortana</span></span>                    |     <span data-ttu-id="d4ecf-147">Нет</span><span class="sxs-lookup"><span data-stu-id="d4ecf-147">No</span></span>                            |     <span data-ttu-id="d4ecf-148">Отключение Кортаны (для устранения потенциальных проблем с отключением микрофонов)</span><span class="sxs-lookup"><span data-stu-id="d4ecf-148">Disables Cortana (to eliminate potential problems since the microphones are disabled)</span></span>                                          |
   |     <span data-ttu-id="d4ecf-149">Политики/Смешанная реальность/MicrophoneDisabled</span><span class="sxs-lookup"><span data-stu-id="d4ecf-149">Policies/MixedReality/MicrophoneDisabled</span></span>            |     <span data-ttu-id="d4ecf-150">Да</span><span class="sxs-lookup"><span data-stu-id="d4ecf-150">Yes</span></span>                           |     <span data-ttu-id="d4ecf-151">Отключение микрофона</span><span class="sxs-lookup"><span data-stu-id="d4ecf-151">Disables Microphone</span></span>                                                                                                            |
   |     <span data-ttu-id="d4ecf-152">Политики/Конфиденциальность/LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="d4ecf-152">Policies/Privacy/LetAppsAccessLocation</span></span>              |     <span data-ttu-id="d4ecf-153">Отказ в силе</span><span class="sxs-lookup"><span data-stu-id="d4ecf-153">Force deny</span></span>                    |     <span data-ttu-id="d4ecf-154">Предотвращает попытки приложений получить доступ к данным о местоположении (чтобы устранить возможные проблемы с отключением отслеживания местоположения)</span><span class="sxs-lookup"><span data-stu-id="d4ecf-154">Prevents Apps from trying to access Location data (to eliminate potential problems since the Location tracking is disabled)</span></span>    |
   |     <span data-ttu-id="d4ecf-155">Политики/Конфиденциальность/LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="d4ecf-155">Policies/Privacy/LetAppsAccessMicrophone</span></span>            |     <span data-ttu-id="d4ecf-156">Отказ в силе</span><span class="sxs-lookup"><span data-stu-id="d4ecf-156">Force deny</span></span>                    |     <span data-ttu-id="d4ecf-157">Предотвращает попытки приложений получить доступ к микрофонам (чтобы устранить возможные проблемы с отключением микрофонов)</span><span class="sxs-lookup"><span data-stu-id="d4ecf-157">Prevents Apps from trying to access Microphones (to eliminate potential problems since the Microphones are disabled)</span></span>           |
   |     <span data-ttu-id="d4ecf-158">Политики/Безопасность/AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="d4ecf-158">Policies/Security/AllowAddProvisioningPackage</span></span>       |     <span data-ttu-id="d4ecf-159">Нет</span><span class="sxs-lookup"><span data-stu-id="d4ecf-159">No</span></span>                            |     <span data-ttu-id="d4ecf-160">Предотвращает добавление пакетов подготовка, которые могут пытаться переопределять заблокированные политики.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-160">Prevents anyone from adding provisioning packages that might attempt to override locked down policies.</span></span>                         |
   |     <span data-ttu-id="d4ecf-161">Политики/безопасность/AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="d4ecf-161">Policies/Security/AllowRemoveProvisioningPackage</span></span>    |     <span data-ttu-id="d4ecf-162">Нет</span><span class="sxs-lookup"><span data-stu-id="d4ecf-162">No</span></span>                            |     <span data-ttu-id="d4ecf-163">Предотвращает удаление этого заблокированного пакета предварительного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-163">Prevents anyone from removing this locked down provisioning package.</span></span>                                                           |
   |     <span data-ttu-id="d4ecf-164">Политики/Система/AllowLocation</span><span class="sxs-lookup"><span data-stu-id="d4ecf-164">Policies/System/AllowLocation</span></span>                       |     <span data-ttu-id="d4ecf-165">Нет</span><span class="sxs-lookup"><span data-stu-id="d4ecf-165">No</span></span>                            |     <span data-ttu-id="d4ecf-166">Предотвращает попытки устройства отслеживать данные о расположении.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-166">Prevents the device from trying to track location data.</span></span>                                                                        |
   |     <span data-ttu-id="d4ecf-167">Политики/WiFi/AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="d4ecf-167">Policies/WiFi/AllowWiFi</span></span>                             |     <span data-ttu-id="d4ecf-168">Нет</span><span class="sxs-lookup"><span data-stu-id="d4ecf-168">No</span></span>                            |     <span data-ttu-id="d4ecf-169">Отключение Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="d4ecf-169">Disables Wi-Fi</span></span>                                                                                                                 |

1. <span data-ttu-id="d4ecf-170">В соответствии с настройками времени запуска выберите **учетные записи / Пользователи / Имя пользователя: Holo / Пароль**.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-170">Under Runtime Settings, Select **Accounts / Users / UserName: Holo / Password**.</span></span>

   <span data-ttu-id="d4ecf-171">Обратите внимание на пароль и сброс при желании.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-171">Note the password and reset if desired.</span></span>

1. <span data-ttu-id="d4ecf-172">Перейдите в UniversalAppInstall / UserContextApp и настройте приложение [LOB,](app-deploy-provisioning-package.md) которое будет развернуто на этих устройствах.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-172">Navigate to UniversalAppInstall / UserContextApp and [configure the LOB app](app-deploy-provisioning-package.md) you will be deploying to these devices.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана, где добавить приложение в WCD.](images/offline-secure-sample-wcd-usercontextapp2.png)

1. <span data-ttu-id="d4ecf-174">После завершения выберите кнопку "Экспорт" и выполните все запросы, пока не будет создан пакет подготовка.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-174">Once complete, select the “Export” button and follow all prompts until your provisioning package is created.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана кнопки Экспорт для этого пакета в WCD.](images/offline-secure-sample-wcd-export.png)

## <a name="deploy"></a><span data-ttu-id="d4ecf-176">Развертывание</span><span class="sxs-lookup"><span data-stu-id="d4ecf-176">Deploy</span></span>

1. <span data-ttu-id="d4ecf-177">Подключите HL2 к компьютеру Windows 10 с помощью USB-кабеля.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-177">Connect the HL2 to your Windows 10 PC via USB cable.</span></span>
1. <span data-ttu-id="d4ecf-178">Запустите инструмент ARC и выберите **HoloLens 2**</span><span class="sxs-lookup"><span data-stu-id="d4ecf-178">Launch the ARC tool and select **HoloLens 2**</span></span>

   ![Первоначальный экран установки чистого образа HoloLens2](images/ARC2.png)

1. <span data-ttu-id="d4ecf-180">На следующем экране выберите **ручной выбор пакета.**</span><span class="sxs-lookup"><span data-stu-id="d4ecf-180">On the next screen select **Manual package selection**.</span></span>

   ![Информационный экран HoloLens 2 ARC](images/arc_device_info.png)

1. <span data-ttu-id="d4ecf-182">Перейдите к ранее загруженным файлу .ffu и выберите **Open**.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-182">Navigate to the previously downloaded .ffu file, and select **Open**.</span></span>
1. <span data-ttu-id="d4ecf-183">На странице Предупреждение выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-183">At the Warning page select **Continue**.</span></span>

   ![Экран предупреждения HoloLens 2 ARC](images/arc_warning.png)

1. <span data-ttu-id="d4ecf-185">Подождите, пока инструмент ARC завершит установку ОС HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-185">Wait for the ARC tool to complete the HoloLens 2 OS install.</span></span>
1. <span data-ttu-id="d4ecf-186">После того как устройство завершит установку и сапоги обратно, с компьютера перейдите на файл Explorer и скопируйте ранее сохраненный файл PPKG в папку устройства.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-186">Once the device completes the install and boots back up, from your PC navigate to File Explorer and copy the previously saved PPKG file over to the device folder.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Файл PPKG на компьютере в окне File Explorer.](images/offline-secure-file-explorer.png)

1. <span data-ttu-id="d4ecf-188">На holoLens 2 нажмите следующую комбо кнопки, чтобы \*\*\*\* запустить пакет подготовка: нажмите кнопку Вниз громкости и **power Button** одновременно.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-188">On the HoloLens 2, press the following button combo to run the Provisioning Package: Tap **Volume Down** and **Power Button** at the same time.</span></span>
1. <span data-ttu-id="d4ecf-189">Вам будет предложено применить пакет подготовка, выберите **Подтверждение**</span><span class="sxs-lookup"><span data-stu-id="d4ecf-189">You will be prompted to apply the Provisioning Package, select **Confirm**</span></span>
1. <span data-ttu-id="d4ecf-190">После завершения пакета подготовка выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-190">Once the provisioning package completes select **OK**.</span></span>
1. <span data-ttu-id="d4ecf-191">После этого вам будет предложено войти в устройство с общей локальной учетной записью и паролем.</span><span class="sxs-lookup"><span data-stu-id="d4ecf-191">You should then be prompted to sign into the device with the shared local account and password.</span></span>

## <a name="maintain"></a><span data-ttu-id="d4ecf-192">Обслуживание</span><span class="sxs-lookup"><span data-stu-id="d4ecf-192">Maintain</span></span>

<span data-ttu-id="d4ecf-193">В этой конфигурации рекомендуется перезапустить процесс выше и перезапустить устройство с помощью инструмента ARC и применить новый PPKG для обновления оси и/или приложения(ы).</span><span class="sxs-lookup"><span data-stu-id="d4ecf-193">With this configuration, it is recommended to restart the process above and reflash the device with the ARC tool and apply a new PPKG to make any updates to the OS and/or application(s).</span></span>
