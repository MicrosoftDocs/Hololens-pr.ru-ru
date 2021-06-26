---
title: Обновление HoloLens 2
description: Узнайте, как проверить номер сборки HoloLens, актуальность обновлений устройств, присоединиться к программе "предварительные оценки" и выполнить откат обновлений.
keywords: практические руководства, обновление, откат, HoloLens, проверка сборки, номер сборки
ms.prod: hololens
ms.sitesec: library
author: scooley
ms.author: scooley
ms.topic: article
ms.localizationpriority: medium
ms.date: 11/27/2019
audience: ITPro
ms.reviewer: ''
manager: jarrettr
appliesto:
- HoloLens 2
ms.openlocfilehash: a27eb1d5eb32a6654f60aac98090cba1aab529d3
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112924117"
---
# <a name="update-hololens-2"></a><span data-ttu-id="dcb81-104">Обновление HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="dcb81-104">Update HoloLens 2</span></span>

<span data-ttu-id="dcb81-105">HoloLens использует Центр обновления Windows, как и другие устройства Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dcb81-105">HoloLens uses Windows Update, just like other Windows 10 devices.</span></span> <span data-ttu-id="dcb81-106">HoloLens автоматически скачивает и устанавливает обновления системы при подключении к электросети и подключению к Интернету, даже если она находится в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="dcb81-106">Your HoloLens will automatically download and install system updates whenever it is plugged-in to power and connected to the Internet, even when it is in standby.</span></span>

<span data-ttu-id="dcb81-107">В этой статье будут рассмотрены средства HoloLens для:</span><span class="sxs-lookup"><span data-stu-id="dcb81-107">This article will walk through HoloLens tools for:</span></span>

- <span data-ttu-id="dcb81-108">Просмотр текущей версии операционной системы (номер сборки)</span><span class="sxs-lookup"><span data-stu-id="dcb81-108">viewing your current operating system version (build number)</span></span>
- <span data-ttu-id="dcb81-109">Проверка наличия обновлений</span><span class="sxs-lookup"><span data-stu-id="dcb81-109">checking for updates</span></span>
- <span data-ttu-id="dcb81-110">Обновление HoloLens вручную</span><span class="sxs-lookup"><span data-stu-id="dcb81-110">manually updating HoloLens</span></span>
- <span data-ttu-id="dcb81-111">откат к более старому обновлению</span><span class="sxs-lookup"><span data-stu-id="dcb81-111">rolling back to an older update</span></span>

## <a name="check-your-operating-system-version-build-number"></a><span data-ttu-id="dcb81-112">Проверка версии операционной системы (номер сборки)</span><span class="sxs-lookup"><span data-stu-id="dcb81-112">Check your operating system version (build number)</span></span>

<span data-ttu-id="dcb81-113">Чтобы проверить номер версии системы (номер сборки), откройте приложение параметры и выберите **система**  >  **о программе**.</span><span class="sxs-lookup"><span data-stu-id="dcb81-113">You can verify the system version number, (build number) by opening the Settings app and selecting **System** > **About**.</span></span>

## <a name="check-for-updates-and-manually-update"></a><span data-ttu-id="dcb81-114">Проверка наличия обновлений и ручное обновление</span><span class="sxs-lookup"><span data-stu-id="dcb81-114">Check for updates and manually update</span></span>

<span data-ttu-id="dcb81-115">Проверить наличие обновлений можно в любое время в параметрах.</span><span class="sxs-lookup"><span data-stu-id="dcb81-115">You can check for updates any time in settings.</span></span>  <span data-ttu-id="dcb81-116">Чтобы просмотреть доступные обновления и проверить наличие новых обновлений, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dcb81-116">To see available updates and check for new updates:</span></span>

1. <span data-ttu-id="dcb81-117">Откройте приложение **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="dcb81-117">Open the **Settings** app.</span></span>
1. <span data-ttu-id="dcb81-118">Перейдите к разделу **Update & Security**  >  **Центр обновления Windows**.</span><span class="sxs-lookup"><span data-stu-id="dcb81-118">Navigate to **Update & Security** > **Windows Update**.</span></span>
1. <span data-ttu-id="dcb81-119">Выберите команду **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="dcb81-119">Select **Check for updates**.</span></span>

<span data-ttu-id="dcb81-120">Если обновление доступно, начнется скачивание новой версии.</span><span class="sxs-lookup"><span data-stu-id="dcb81-120">If an update is available, it will start downloading the new version.</span></span> <span data-ttu-id="dcb81-121">После завершения загрузки нажмите кнопку **Перезагрузить сейчас** , чтобы запустить установку.</span><span class="sxs-lookup"><span data-stu-id="dcb81-121">After the download is complete, select the **Restart Now** button to trigger the installation.</span></span> <span data-ttu-id="dcb81-122">Если устройство находится ниже 40% и не подключено к сети, то при перезапуске установка обновления не начнется.</span><span class="sxs-lookup"><span data-stu-id="dcb81-122">If your device is below 40% and not plugged in, restarting will not start installing the update.</span></span>

<span data-ttu-id="dcb81-123">Хотя HoloLens устанавливает обновление, в нем отображаются вращающиеся устройства и индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dcb81-123">While your HoloLens is installing the update, it will display spinning gears and a progress indicator.</span></span> <span data-ttu-id="dcb81-124">Не отключайте HoloLens в течение этого времени.</span><span class="sxs-lookup"><span data-stu-id="dcb81-124">Do not turn off your HoloLens during this time.</span></span> <span data-ttu-id="dcb81-125">После завершения установки она будет автоматически перезапущена.</span><span class="sxs-lookup"><span data-stu-id="dcb81-125">It will restart automatically once it has completed the installation.</span></span>

<span data-ttu-id="dcb81-126">HoloLens применяет одно обновление за раз.</span><span class="sxs-lookup"><span data-stu-id="dcb81-126">HoloLens applies one update at a time.</span></span>  <span data-ttu-id="dcb81-127">Если HoloLens является более одной версией за последнюю версию, может потребоваться несколько раз выполнить обновление, чтобы полностью обновить его.</span><span class="sxs-lookup"><span data-stu-id="dcb81-127">If your HoloLens is more than one version behind the latest you may need to run through the update process multiple times to get it fully up to date.</span></span>

## <a name="go-back-to-a-previous-version"></a><span data-ttu-id="dcb81-128">Вернуться к предыдущей версии</span><span class="sxs-lookup"><span data-stu-id="dcb81-128">Go back to a previous version</span></span>

<span data-ttu-id="dcb81-129">В некоторых случаях может потребоваться вернуться к предыдущей версии программного обеспечения HoloLens.</span><span class="sxs-lookup"><span data-stu-id="dcb81-129">In some cases, you might want to go back to a previous version of the HoloLens software.</span></span> <span data-ttu-id="dcb81-130">Ниже приведены рекомендуемые действия.</span><span class="sxs-lookup"><span data-stu-id="dcb81-130">The recommended steps are:</span></span>

1. <span data-ttu-id="dcb81-131">Обратитесь в службу поддержки, чтобы узнать, можете ли они устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="dcb81-131">Contact Support to see if they can fix your issue.</span></span>
    1. <span data-ttu-id="dcb81-132">Убедитесь, что включена **необязательная** или **полная** телеметрии. это сделает ошибку более удобной и простой для диагностики.</span><span class="sxs-lookup"><span data-stu-id="dcb81-132">Ensure that **Optional** or **Full** telemetry is enabled -  this makes your bug more actionable and easier for engineers to diagnose.</span></span>
    1. <span data-ttu-id="dcb81-133">[Обратная связь с файлами](hololens-feedback.md) как можно более описательной.</span><span class="sxs-lookup"><span data-stu-id="dcb81-133">[File Feedback](hololens-feedback.md) being as descriptive as possible.</span></span> <span data-ttu-id="dcb81-134">Запишите название или используйте функцию общего доступа, чтобы вы могли поделиться своей ошибкой с поддержкой.</span><span class="sxs-lookup"><span data-stu-id="dcb81-134">Take note of the title or use the share feature so you can share your bug with Support.</span></span>
    1. <span data-ttu-id="dcb81-135">Обратитесь в [службу поддержки](https://aka.ms/hlsupport).</span><span class="sxs-lookup"><span data-stu-id="dcb81-135">Contact [Support](https://aka.ms/hlsupport).</span></span> <span data-ttu-id="dcb81-136">Если вы хотите решить проблему, вернувшись к предыдущей версии, они могут предоставить вам ФФУ для флэш-памяти устройства.</span><span class="sxs-lookup"><span data-stu-id="dcb81-136">If your issue is one that needs to be solved by returning to a previous version, they can supply you the FFU to flash your device.</span></span>

1. <span data-ttu-id="dcb81-137">Если это не поможет, [сбросьте или восзапустите HoloLens 2 с помощью дополнительного помощника по восстановлению](hololens-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="dcb81-137">If that does not work, then [reset or reflash your HoloLens 2 with the Advanced Recovery Companion](hololens-recovery.md).</span></span>
    1. <span data-ttu-id="dcb81-138">На компьютере Скачайте [Расширенный помощник по восстановлению](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) из Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="dcb81-138">On your PC, download the [Advanced Recovery Companion](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) from the Microsoft Store.</span></span>
    1. <span data-ttu-id="dcb81-139">Убедитесь, что у вас нет телефонов или устройств Windows, подключенных к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="dcb81-139">Make sure that you don't have any phones or Windows devices plugged in to your PC.</span></span>
    1. <span data-ttu-id="dcb81-140">Выберите версию для вспышки:</span><span class="sxs-lookup"><span data-stu-id="dcb81-140">Choose which version you want to flash to:</span></span>
        1. <span data-ttu-id="dcb81-141">Вы можете скачать [самый последний выпуск HoloLens 2](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="dcb81-141">You can download the [most recent HoloLens 2 release](https://aka.ms/hololens2download).</span></span>
        1. <span data-ttu-id="dcb81-142">Можно использовать сборку по умолчанию, на которой размещаются дуги.</span><span class="sxs-lookup"><span data-stu-id="dcb81-142">You can use the default build that ARC hosts.</span></span> <span data-ttu-id="dcb81-143">(Если выбран этот параметр, пропустите следующий шаг.)</span><span class="sxs-lookup"><span data-stu-id="dcb81-143">(If you choose this option skip the next step.)</span></span>
        1. <span data-ttu-id="dcb81-144">Вы можете использовать поддержку сборки, предоставленную в.</span><span class="sxs-lookup"><span data-stu-id="dcb81-144">You can use a build Support provided you with.</span></span>
    1. <span data-ttu-id="dcb81-145">После завершения загрузки откройте **файл**  >  **downloads** в проводнике.</span><span class="sxs-lookup"><span data-stu-id="dcb81-145">When you have finished these downloads, open **File Explorer** > **Downloads**.</span></span> <span data-ttu-id="dcb81-146">Щелкните правой кнопкой мыши скачанную ZIP-папку и выберите **извлечь все**  >  **извлечь** , чтобы распаковать ее.</span><span class="sxs-lookup"><span data-stu-id="dcb81-146">Right-click the zipped folder that you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
    1. <span data-ttu-id="dcb81-147">Подключите HoloLens к компьютеру, используя кабель USB-A – USB-C.</span><span class="sxs-lookup"><span data-stu-id="dcb81-147">Connect your HoloLens to your PC using a USB-A to USB-C cable.</span></span> <span data-ttu-id="dcb81-148">(Даже если вы используете другие кабели для подключения HoloLens, это работает наилучшим образом.)</span><span class="sxs-lookup"><span data-stu-id="dcb81-148">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
    1. <span data-ttu-id="dcb81-149">Помощник по расширенному восстановлению автоматически обнаруживает HoloLens.</span><span class="sxs-lookup"><span data-stu-id="dcb81-149">The Advanced Recovery Companion automatically detects your HoloLens.</span></span> <span data-ttu-id="dcb81-150">Выберите плитку **Microsoft HoloLens** .</span><span class="sxs-lookup"><span data-stu-id="dcb81-150">Select the **Microsoft HoloLens** tile.</span></span>
    1. <span data-ttu-id="dcb81-151">На следующем экране выберите **ручной выбор пакетов** , а затем выберите файл установки, содержащийся в папке, которая была распакована на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="dcb81-151">On the next screen, select **Manual package selection** and then select the installation file contained in the folder that you unzipped in step 4.</span></span> <span data-ttu-id="dcb81-152">(Найдите файл с расширением ФФУ.)</span><span class="sxs-lookup"><span data-stu-id="dcb81-152">(Look for a file with the .ffu extension.)</span></span>
    1. <span data-ttu-id="dcb81-153">Выберите **установить программное обеспечение** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="dcb81-153">Select **Install software**, and follow the instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="dcb81-154">При возврате к более ранней версии удаляются личные файлы и параметры.</span><span class="sxs-lookup"><span data-stu-id="dcb81-154">Going back to an earlier version deletes your personal files and settings.</span></span>

<span data-ttu-id="dcb81-155">Кроме того, если вы хотите остаться в текущем установленном выпуске, можно также вручную [приостановить обновления](hololens-updates.md#pause-updates-via-device).</span><span class="sxs-lookup"><span data-stu-id="dcb81-155">Additionally, if you would like to stay on your currently installed release, you can also manually [pause updates](hololens-updates.md#pause-updates-via-device).</span></span> <span data-ttu-id="dcb81-156">Это позволит команде разработчиков решить проблему.</span><span class="sxs-lookup"><span data-stu-id="dcb81-156">This will give the Engineering Team time to fix the issue.</span></span>

## <a name="windows-insider-program-on-hololens"></a><span data-ttu-id="dcb81-157">Программа предварительной оценки Windows в HoloLens</span><span class="sxs-lookup"><span data-stu-id="dcb81-157">Windows Insider Program on HoloLens</span></span>

<span data-ttu-id="dcb81-158">Хотите просмотреть новейшие функции в HoloLens?</span><span class="sxs-lookup"><span data-stu-id="dcb81-158">Want to see the latest features in HoloLens?</span></span>  <span data-ttu-id="dcb81-159">Если да, Присоединяйтесь к программе предварительной оценки Windows; Вы получите доступ к предварительным сборкам обновлений программного обеспечения HoloLens, прежде чем они будут доступны для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="dcb81-159">If so, join the Windows Insider Program; you'll get access to preview builds of HoloLens software updates before they're available to the general public.</span></span>

<span data-ttu-id="dcb81-160">[Получите предварительную версию Windows Insider Preview для Microsoft HoloLens](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="dcb81-160">[Get Windows Insider preview for Microsoft HoloLens](hololens-insider.md).</span></span>
