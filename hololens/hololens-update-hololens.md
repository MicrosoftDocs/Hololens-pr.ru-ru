---
title: Обновление HoloLens
description: Проверьте номер сборки HoloLens, обновите и выполните откат обновлений.
keywords: инструкции, обновление, откат, HoloLens, проверка сборки, номер сборки
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
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: ee007b00b350ea0f80cda34964d32a57dc6dc0c6
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10828594"
---
# <span data-ttu-id="fd775-104">Обновление HoloLens</span><span class="sxs-lookup"><span data-stu-id="fd775-104">Update HoloLens</span></span>

<span data-ttu-id="fd775-105">HoloLens использует Windows Update, как и другие устройства с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fd775-105">HoloLens uses Windows Update, just like other Windows 10 devices.</span></span> <span data-ttu-id="fd775-106">HoloLens будет автоматически скачивать и устанавливать обновления системы при подключении к электросети и подключению к Интернету, даже если они находятся в ждущем режиме.</span><span class="sxs-lookup"><span data-stu-id="fd775-106">Your HoloLens will automatically download and install system updates whenever it is plugged-in to power and connected to the Internet, even when it is in standby.</span></span>

<span data-ttu-id="fd775-107">В этой статье рассматриваются инструменты HoloLens для следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="fd775-107">This article will walk through HoloLens tools for:</span></span>

- <span data-ttu-id="fd775-108">Просмотр текущей версии операционной системы (номер сборки)</span><span class="sxs-lookup"><span data-stu-id="fd775-108">viewing your current operating system version (build number)</span></span>
- <span data-ttu-id="fd775-109">Проверка наличия обновлений</span><span class="sxs-lookup"><span data-stu-id="fd775-109">checking for updates</span></span>
- <span data-ttu-id="fd775-110">Обновление HoloLens вручную</span><span class="sxs-lookup"><span data-stu-id="fd775-110">manually updating HoloLens</span></span>
- <span data-ttu-id="fd775-111">Возврат к более раннему обновлению</span><span class="sxs-lookup"><span data-stu-id="fd775-111">rolling back to an older update</span></span>

## <span data-ttu-id="fd775-112">Проверка версии операционной системы (номер сборки)</span><span class="sxs-lookup"><span data-stu-id="fd775-112">Check your operating system version (build number)</span></span>

<span data-ttu-id="fd775-113">Вы можете проверить номер версии системы (номер сборки), открыв приложение параметры и выбрав пункт **система**  >  **About**.</span><span class="sxs-lookup"><span data-stu-id="fd775-113">You can verify the system version number, (build number) by opening the Settings app and selecting **System** > **About**.</span></span>

## <span data-ttu-id="fd775-114">Проверка наличия обновлений и обновление вручную</span><span class="sxs-lookup"><span data-stu-id="fd775-114">Check for updates and manually update</span></span>

<span data-ttu-id="fd775-115">Вы можете проверять наличие обновлений в любое время в параметрах.</span><span class="sxs-lookup"><span data-stu-id="fd775-115">You can check for updates any time in settings.</span></span>  <span data-ttu-id="fd775-116">Чтобы просмотреть доступные обновления и проверить наличие новых обновлений, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="fd775-116">To see available updates and check for new updates:</span></span>

1. <span data-ttu-id="fd775-117">Откройте приложение **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="fd775-117">Open the **Settings** app.</span></span>
1. <span data-ttu-id="fd775-118">Перейдите к разделу **Обновление системы безопасности &** центра  >  **обновления Windows**.</span><span class="sxs-lookup"><span data-stu-id="fd775-118">Navigate to **Update & Security** > **Windows Update**.</span></span>
1. <span data-ttu-id="fd775-119">Нажмите кнопку **проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="fd775-119">Select **Check for updates**.</span></span>

<span data-ttu-id="fd775-120">Если обновление будет доступно, начнется загрузка новой версии.</span><span class="sxs-lookup"><span data-stu-id="fd775-120">If an update is available, it will start downloading the new version.</span></span> <span data-ttu-id="fd775-121">После завершения загрузки нажмите кнопку **Перезапустить сейчас** , чтобы запустить установку.</span><span class="sxs-lookup"><span data-stu-id="fd775-121">After the download is complete, select the **Restart Now** button to trigger the installation.</span></span> <span data-ttu-id="fd775-122">Если устройство находится менее 40%, а не подключено, перезагрузка не начнет устанавливать обновление.</span><span class="sxs-lookup"><span data-stu-id="fd775-122">If your device is below 40% and not plugged in, restarting will not start installing the update.</span></span>

<span data-ttu-id="fd775-123">В то время как HoloLens устанавливает обновление, на нем отображаются вращающиеся индикаторы и индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="fd775-123">While your HoloLens is installing the update, it will display spinning gears and a progress indicator.</span></span> <span data-ttu-id="fd775-124">В этот раз не выключайте HoloLens.</span><span class="sxs-lookup"><span data-stu-id="fd775-124">Do not turn off your HoloLens during this time.</span></span> <span data-ttu-id="fd775-125">После завершения установки она будет перезапущена автоматически.</span><span class="sxs-lookup"><span data-stu-id="fd775-125">It will restart automatically once it has completed the installation.</span></span>

<span data-ttu-id="fd775-126">HoloLens применяет одно обновление за раз.</span><span class="sxs-lookup"><span data-stu-id="fd775-126">HoloLens applies one update at a time.</span></span>  <span data-ttu-id="fd775-127">Если HoloLens является более одной версией за последнюю, вам может потребоваться выполнить процесс обновления несколько дольше, чтобы полностью обновить ее актуальность.</span><span class="sxs-lookup"><span data-stu-id="fd775-127">If your HoloLens is more than one version behind the latest you may need to run through the update process multiple times to get it fully up to date.</span></span>

## <span data-ttu-id="fd775-128">Вернуться к предыдущей версии — HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="fd775-128">Go back to a previous version - HoloLens 2</span></span>

<span data-ttu-id="fd775-129">В некоторых случаях может потребоваться вернуться к предыдущей версии программного обеспечения HoloLens.</span><span class="sxs-lookup"><span data-stu-id="fd775-129">In some cases, you might want to go back to a previous version of the HoloLens software.</span></span> <span data-ttu-id="fd775-130">Это можно сделать с помощью расширенного помощника по восстановлению, чтобы сбросить параметры HoloLens до более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="fd775-130">You can do this by using the Advanced Recovery Companion to reset your HoloLens to the earlier version.</span></span>

> [!NOTE]
> <span data-ttu-id="fd775-131">При переходе к более ранней версии удаляются личные файлы и параметры.</span><span class="sxs-lookup"><span data-stu-id="fd775-131">Going back to an earlier version deletes your personal files and settings.</span></span>

<span data-ttu-id="fd775-132">Чтобы вернуться к предыдущей версии HoloLens 2, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="fd775-132">To go back to a previous version of HoloLens 2, follow these steps:</span></span>

1. <span data-ttu-id="fd775-133">Убедитесь, что на вашем компьютере не подключены ни телефоны, ни устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="fd775-133">Make sure that you don't have any phones or Windows devices plugged in to your PC.</span></span>
1. <span data-ttu-id="fd775-134">На компьютере загрузите [Расширенный помощник по восстановлению](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) из Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="fd775-134">On your PC, download the [Advanced Recovery Companion](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) from the Microsoft Store.</span></span>
1. <span data-ttu-id="fd775-135">Загрузите [последнюю версию HoloLens 2](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="fd775-135">Download the [most recent HoloLens 2 release](https://aka.ms/hololens2download).</span></span>
1. <span data-ttu-id="fd775-136">После того как вы закончите загрузку, откройте **файл**  >  **download**Explorer.</span><span class="sxs-lookup"><span data-stu-id="fd775-136">When you have finished these downloads, open **File explorer** > **Downloads**.</span></span> <span data-ttu-id="fd775-137">Щелкните правой кнопкой мыши только что скачанную запакованную папку и выберите **Извлечь все** > **Извлечь**, чтобы распаковать ее.</span><span class="sxs-lookup"><span data-stu-id="fd775-137">Right-click the zipped folder that you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
1. <span data-ttu-id="fd775-138">Подключите HoloLens к компьютеру с помощью USB-A и USB-C.</span><span class="sxs-lookup"><span data-stu-id="fd775-138">Connect your HoloLens to your PC using a USB-A to USB-C cable.</span></span> <span data-ttu-id="fd775-139">(Даже если вы использовали для подключения HoloLens другие кабели, этот работает лучше.)</span><span class="sxs-lookup"><span data-stu-id="fd775-139">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
1. <span data-ttu-id="fd775-140">Помощник по расширенному восстановлению автоматически обнаруживает HoloLens.</span><span class="sxs-lookup"><span data-stu-id="fd775-140">The Advanced Recovery Companion automatically detects your HoloLens.</span></span> <span data-ttu-id="fd775-141">Выберите плитку **Microsoft HoloLens** .</span><span class="sxs-lookup"><span data-stu-id="fd775-141">Select the **Microsoft HoloLens** tile.</span></span>
1. <span data-ttu-id="fd775-142">На следующем экране выберите **вариант ручной выбор пакетов** и выберите установочный файл, содержащийся в папке, которую вы распаковать в действии 4.</span><span class="sxs-lookup"><span data-stu-id="fd775-142">On the next screen, select **Manual package selection** and then select the installation file contained in the folder that you unzipped in step 4.</span></span> <span data-ttu-id="fd775-143">(Найдите файл с расширением FFU.)</span><span class="sxs-lookup"><span data-stu-id="fd775-143">(Look for a file with the .ffu extension.)</span></span>
1. <span data-ttu-id="fd775-144">Выберите **Установка программного обеспечения**и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="fd775-144">Select **Install software**, and follow the instructions.</span></span>

## <span data-ttu-id="fd775-145">Возврат к предыдущей версии — HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="fd775-145">Go back to a previous version - HoloLens (1st Gen)</span></span>

<span data-ttu-id="fd775-146">В некоторых случаях может потребоваться вернуться к предыдущей версии программного обеспечения HoloLens.</span><span class="sxs-lookup"><span data-stu-id="fd775-146">In some cases, you might want to go back to a previous version of the HoloLens software.</span></span> <span data-ttu-id="fd775-147">Это можно сделать с помощью средства восстановления устройств Windows, чтобы сбросить параметры HoloLens до более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="fd775-147">You can do this by using the Windows Device Recovery Tool to reset your HoloLens to the earlier version.</span></span>

> [!NOTE]
> <span data-ttu-id="fd775-148">При переходе к более ранней версии удаляются личные файлы и параметры.</span><span class="sxs-lookup"><span data-stu-id="fd775-148">Going back to an earlier version deletes your personal files and settings.</span></span>

<span data-ttu-id="fd775-149">Чтобы вернуться к предыдущей версии HoloLens 1, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="fd775-149">To go back to a previous version of HoloLens 1, follow these steps:</span></span>

1. <span data-ttu-id="fd775-150">Убедитесь, что на вашем компьютере не подключены ни телефоны, ни устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="fd775-150">Make sure that you don't have any phones or Windows devices plugged in to your PC.</span></span>
1. <span data-ttu-id="fd775-151">На компьютере загрузите [средство восстановления устройств Windows (WDRT)](https://support.microsoft.com/help/12379).</span><span class="sxs-lookup"><span data-stu-id="fd775-151">On your PC, download the [Windows Device Recovery Tool (WDRT)](https://support.microsoft.com/help/12379).</span></span>
1. <span data-ttu-id="fd775-152">Скачайте [пакет восстановления для годовщины HoloLens](https://aka.ms/hololensrecovery).</span><span class="sxs-lookup"><span data-stu-id="fd775-152">Download the [HoloLens Anniversary Update recovery package](https://aka.ms/hololensrecovery).</span></span>
1. <span data-ttu-id="fd775-153">После завершения загрузки откройте **файл**  >  **download**Explorer.</span><span class="sxs-lookup"><span data-stu-id="fd775-153">When the downloads finish, open **File explorer** > **Downloads**.</span></span> <span data-ttu-id="fd775-154">Щелкните правой кнопкой мыши папку ZIP, которую вы только что загрузили, и выберите **извлечь все**  >  **извлечь** , чтобы распаковать ее.</span><span class="sxs-lookup"><span data-stu-id="fd775-154">Right-click the zipped folder you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
1. <span data-ttu-id="fd775-155">Подключите HoloLens к компьютеру с помощью USB-кабеля с микропортом, с которым он поставлялся.</span><span class="sxs-lookup"><span data-stu-id="fd775-155">Connect your HoloLens to your PC using the micro-USB cable that it came with.</span></span> <span data-ttu-id="fd775-156">(Даже если вы использовали для подключения HoloLens другие кабели, этот работает лучше.)</span><span class="sxs-lookup"><span data-stu-id="fd775-156">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
1. <span data-ttu-id="fd775-157">WDRT будет автоматически определять HoloLens.</span><span class="sxs-lookup"><span data-stu-id="fd775-157">The WDRT will automatically detect your HoloLens.</span></span> <span data-ttu-id="fd775-158">Выберите плитку **Microsoft HoloLens** .</span><span class="sxs-lookup"><span data-stu-id="fd775-158">Select the **Microsoft HoloLens** tile.</span></span>
1. <span data-ttu-id="fd775-159">На следующем экране выберите вариант **пакет вручную** и выберите файл установки, который находится в папке, которую вы распаковать в действии 4.</span><span class="sxs-lookup"><span data-stu-id="fd775-159">On the next screen, select **Manual package selection** and choose the installation file contained in the folder you unzipped in step 4.</span></span> <span data-ttu-id="fd775-160">(Найдите файл с расширением FFU.)</span><span class="sxs-lookup"><span data-stu-id="fd775-160">(Look for a file with the .ffu extension.)</span></span>
1. <span data-ttu-id="fd775-161">Выберите **Установка программного обеспечения**и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="fd775-161">Select **Install software**, and follow the instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="fd775-162">Если WDRT не обнаруживает HoloLens, попробуйте перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="fd775-162">If the WDRT doesn't detect your HoloLens, try restarting your PC.</span></span> <span data-ttu-id="fd775-163">Если это не поможет, выберите **устройство не обнаружено**, выберите **Microsoft HoloLens**и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="fd775-163">If that doesn't work, select **My device was not detected**, select **Microsoft HoloLens**, and then follow the instructions.</span></span>

## <span data-ttu-id="fd775-164">Программа предварительной оценки Windows на HoloLens</span><span class="sxs-lookup"><span data-stu-id="fd775-164">Windows Insider Program on HoloLens</span></span>

<span data-ttu-id="fd775-165">Хотите просмотреть последние функции в HoloLens?</span><span class="sxs-lookup"><span data-stu-id="fd775-165">Want to see the latest features in HoloLens?</span></span>  <span data-ttu-id="fd775-166">Если да, Присоединяйтесь к программе предварительной оценки Windows; Вы получите доступ к предварительным сборкам обновлений программного обеспечения для HoloLens, прежде чем они будут доступны для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="fd775-166">If so, join the Windows Insider Program; you'll get access to preview builds of HoloLens software updates before they're available to the general public.</span></span>

<span data-ttu-id="fd775-167">[Скачать предварительную версию программы предварительной оценки Windows для Microsoft HoloLens](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="fd775-167">[Get Windows Insider preview for Microsoft HoloLens](hololens-insider.md).</span></span>
