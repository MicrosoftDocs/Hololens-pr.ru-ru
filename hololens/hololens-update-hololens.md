---
title: Обновление HoloLens
description: Узнайте, как проверять номер сборки HoloLens, обновлять обновления устройств, присоединяться к программе участников программы участников программы и откатывать обновления.
keywords: how-to, update, roll back, HoloLens, check build, build number
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
ms.openlocfilehash: ef1721c60aca82d20e60636cbf4301de81c0177c
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283940"
---
# <span data-ttu-id="786bf-104">Обновление HoloLens</span><span class="sxs-lookup"><span data-stu-id="786bf-104">Update HoloLens</span></span>

<span data-ttu-id="786bf-105">HoloLens использует Windows Update, как и другие устройства с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="786bf-105">HoloLens uses Windows Update, just like other Windows 10 devices.</span></span> <span data-ttu-id="786bf-106">HoloLens автоматически скачивает и устанавливает обновления системы при подключении к сети и подключении к Интернету, даже если он находится в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="786bf-106">Your HoloLens will automatically download and install system updates whenever it is plugged-in to power and connected to the Internet, even when it is in standby.</span></span>

<span data-ttu-id="786bf-107">В этой статье данная статья посвящена средствам HoloLens для:</span><span class="sxs-lookup"><span data-stu-id="786bf-107">This article will walk through HoloLens tools for:</span></span>

- <span data-ttu-id="786bf-108">просмотр текущей версии операционной системы (номер сборки)</span><span class="sxs-lookup"><span data-stu-id="786bf-108">viewing your current operating system version (build number)</span></span>
- <span data-ttu-id="786bf-109">проверка на обновление</span><span class="sxs-lookup"><span data-stu-id="786bf-109">checking for updates</span></span>
- <span data-ttu-id="786bf-110">обновление HoloLens вручную</span><span class="sxs-lookup"><span data-stu-id="786bf-110">manually updating HoloLens</span></span>
- <span data-ttu-id="786bf-111">откат к более старому обновлению</span><span class="sxs-lookup"><span data-stu-id="786bf-111">rolling back to an older update</span></span>

## <span data-ttu-id="786bf-112">Проверка версии операционной системы (номер сборки)</span><span class="sxs-lookup"><span data-stu-id="786bf-112">Check your operating system version (build number)</span></span>

<span data-ttu-id="786bf-113">Номер версии системы (номер сборки) можно проверить, открыв приложение "Параметры" и выбрав **"Система**о  >  **системе".**</span><span class="sxs-lookup"><span data-stu-id="786bf-113">You can verify the system version number, (build number) by opening the Settings app and selecting **System** > **About**.</span></span>

## <span data-ttu-id="786bf-114">Проверка на обновления и обновление вручную</span><span class="sxs-lookup"><span data-stu-id="786bf-114">Check for updates and manually update</span></span>

<span data-ttu-id="786bf-115">Вы можете проверять обновления в любое время в параметрах.</span><span class="sxs-lookup"><span data-stu-id="786bf-115">You can check for updates any time in settings.</span></span>  <span data-ttu-id="786bf-116">Чтобы увидеть доступные обновления и проверить, нет ли новых обновлений:</span><span class="sxs-lookup"><span data-stu-id="786bf-116">To see available updates and check for new updates:</span></span>

1. <span data-ttu-id="786bf-117">Откройте приложение **"Параметры".**</span><span class="sxs-lookup"><span data-stu-id="786bf-117">Open the **Settings** app.</span></span>
1. <span data-ttu-id="786bf-118">Перейдите в **& Обновления**Windows для  >  **системы безопасности.**</span><span class="sxs-lookup"><span data-stu-id="786bf-118">Navigate to **Update & Security** > **Windows Update**.</span></span>
1. <span data-ttu-id="786bf-119">Выберите **"Проверить обновления".**</span><span class="sxs-lookup"><span data-stu-id="786bf-119">Select **Check for updates**.</span></span>

<span data-ttu-id="786bf-120">Если обновление доступно, оно начнет скачивать новую версию.</span><span class="sxs-lookup"><span data-stu-id="786bf-120">If an update is available, it will start downloading the new version.</span></span> <span data-ttu-id="786bf-121">После завершения скачивания выберите кнопку **"Перезапустить сейчас",** чтобы активирует установку.</span><span class="sxs-lookup"><span data-stu-id="786bf-121">After the download is complete, select the **Restart Now** button to trigger the installation.</span></span> <span data-ttu-id="786bf-122">Если устройство меньше 40 % и не подключено к компьютеру, перезагрузка не начнет установку обновления.</span><span class="sxs-lookup"><span data-stu-id="786bf-122">If your device is below 40% and not plugged in, restarting will not start installing the update.</span></span>

<span data-ttu-id="786bf-123">Пока HoloLens устанавливает обновление, он отображает вращающиеся шестеренки и индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="786bf-123">While your HoloLens is installing the update, it will display spinning gears and a progress indicator.</span></span> <span data-ttu-id="786bf-124">Не отключать HoloLens в течение этого времени.</span><span class="sxs-lookup"><span data-stu-id="786bf-124">Do not turn off your HoloLens during this time.</span></span> <span data-ttu-id="786bf-125">Он автоматически перезагружается после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="786bf-125">It will restart automatically once it has completed the installation.</span></span>

<span data-ttu-id="786bf-126">HoloLens применяет по одному обновлению за раз.</span><span class="sxs-lookup"><span data-stu-id="786bf-126">HoloLens applies one update at a time.</span></span>  <span data-ttu-id="786bf-127">Если holoLens более чем на одну версию отстает от последней, может потребоваться несколько раз выполнить процесс обновления, чтобы полностью обновить его.</span><span class="sxs-lookup"><span data-stu-id="786bf-127">If your HoloLens is more than one version behind the latest you may need to run through the update process multiple times to get it fully up to date.</span></span>

## <span data-ttu-id="786bf-128">Вернуться к предыдущей версии — HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="786bf-128">Go back to a previous version - HoloLens 2</span></span>

<span data-ttu-id="786bf-129">В некоторых случаях может потребоваться вернуться на предыдущую версию программного обеспечения HoloLens.</span><span class="sxs-lookup"><span data-stu-id="786bf-129">In some cases, you might want to go back to a previous version of the HoloLens software.</span></span> <span data-ttu-id="786bf-130">Это можно сделать с помощью компаньона advanced Recovery Companion для сброса HoloLens до более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="786bf-130">You can do this by using the Advanced Recovery Companion to reset your HoloLens to the earlier version.</span></span>

> [!NOTE]
> <span data-ttu-id="786bf-131">Если вернуться к более ранней версии, личные файлы и параметры будут удаляться.</span><span class="sxs-lookup"><span data-stu-id="786bf-131">Going back to an earlier version deletes your personal files and settings.</span></span>

<span data-ttu-id="786bf-132">Для возврата к предыдущей версии HoloLens 2 выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="786bf-132">To go back to a previous version of HoloLens 2, follow these steps:</span></span>

1. <span data-ttu-id="786bf-133">Убедитесь, что у вас нет телефонов или устройств с Windows, подключенных к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="786bf-133">Make sure that you don't have any phones or Windows devices plugged in to your PC.</span></span>
1. <span data-ttu-id="786bf-134">На компьютере скачайте [дополнительный](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) помощник по восстановлению из Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="786bf-134">On your PC, download the [Advanced Recovery Companion](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) from the Microsoft Store.</span></span>
1. <span data-ttu-id="786bf-135">Загрузите [последний выпуск HoloLens 2](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="786bf-135">Download the [most recent HoloLens 2 release](https://aka.ms/hololens2download).</span></span>
1. <span data-ttu-id="786bf-136">Завершив скачивание, откройте **файл**  >  \*\*\*\* проводника.</span><span class="sxs-lookup"><span data-stu-id="786bf-136">When you have finished these downloads, open **File explorer** > **Downloads**.</span></span> <span data-ttu-id="786bf-137">Щелкните правой кнопкой мыши только что скачанную запакованную папку и выберите **Извлечь все** > **Извлечь**, чтобы распаковать ее.</span><span class="sxs-lookup"><span data-stu-id="786bf-137">Right-click the zipped folder that you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
1. <span data-ttu-id="786bf-138">Подключите Устройство HoloLens к компьютеру с помощью USB-A-кабеля USB-C.</span><span class="sxs-lookup"><span data-stu-id="786bf-138">Connect your HoloLens to your PC using a USB-A to USB-C cable.</span></span> <span data-ttu-id="786bf-139">(Даже если вы использовали для подключения HoloLens другие кабели, этот работает лучше.)</span><span class="sxs-lookup"><span data-stu-id="786bf-139">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
1. <span data-ttu-id="786bf-140">Дополнительный помощник по восстановлению автоматически обнаруживает HoloLens.</span><span class="sxs-lookup"><span data-stu-id="786bf-140">The Advanced Recovery Companion automatically detects your HoloLens.</span></span> <span data-ttu-id="786bf-141">Выберите плитку **Microsoft HoloLens**.</span><span class="sxs-lookup"><span data-stu-id="786bf-141">Select the **Microsoft HoloLens** tile.</span></span>
1. <span data-ttu-id="786bf-142">На следующем экране \*\*\*\* выберите выбор пакета вручную, а затем выберите установочный файл, содержащийся в папке, которая была растерчена на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="786bf-142">On the next screen, select **Manual package selection** and then select the installation file contained in the folder that you unzipped in step 4.</span></span> <span data-ttu-id="786bf-143">(Найми файл с расширением FFU.)</span><span class="sxs-lookup"><span data-stu-id="786bf-143">(Look for a file with the .ffu extension.)</span></span>
1. <span data-ttu-id="786bf-144">Выберите **"Установить программное**обеспечение" и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="786bf-144">Select **Install software**, and follow the instructions.</span></span>

## <span data-ttu-id="786bf-145">Вернуться к предыдущей версии — HoloLens (1-е поколения)</span><span class="sxs-lookup"><span data-stu-id="786bf-145">Go back to a previous version - HoloLens (1st Gen)</span></span>

<span data-ttu-id="786bf-146">В некоторых случаях может потребоваться вернуться на предыдущую версию программного обеспечения HoloLens.</span><span class="sxs-lookup"><span data-stu-id="786bf-146">In some cases, you might want to go back to a previous version of the HoloLens software.</span></span> <span data-ttu-id="786bf-147">Это можно сделать с помощью средства восстановления устройств с Windows для сброса HoloLens до более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="786bf-147">You can do this by using the Windows Device Recovery Tool to reset your HoloLens to the earlier version.</span></span>

> [!NOTE]
> <span data-ttu-id="786bf-148">Если вернуться к более ранней версии, личные файлы и параметры будут удаляться.</span><span class="sxs-lookup"><span data-stu-id="786bf-148">Going back to an earlier version deletes your personal files and settings.</span></span>

<span data-ttu-id="786bf-149">Чтобы вернуться к предыдущей версии HoloLens 1, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="786bf-149">To go back to a previous version of HoloLens 1, follow these steps:</span></span>

1. <span data-ttu-id="786bf-150">Убедитесь, что у вас нет телефонов или устройств с Windows, подключенных к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="786bf-150">Make sure that you don't have any phones or Windows devices plugged in to your PC.</span></span>
1. <span data-ttu-id="786bf-151">На компьютере скачайте [средство восстановления устройств с Windows (WDRT).](https://support.microsoft.com/help/12379)</span><span class="sxs-lookup"><span data-stu-id="786bf-151">On your PC, download the [Windows Device Recovery Tool (WDRT)](https://support.microsoft.com/help/12379).</span></span>
1. <span data-ttu-id="786bf-152">Загрузите пакет восстановления [HoloLens Anniversary Update](https://aka.ms/hololensrecovery).</span><span class="sxs-lookup"><span data-stu-id="786bf-152">Download the [HoloLens Anniversary Update recovery package](https://aka.ms/hololensrecovery).</span></span>
1. <span data-ttu-id="786bf-153">Когда загрузки будут завершены, **откройте**проводник.  >  \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="786bf-153">When the downloads finish, open **File explorer** > **Downloads**.</span></span> <span data-ttu-id="786bf-154">Щелкните правой кнопкой мыши папку zippped, которая вы только что скачали, и выберите **"Извлечь все**извлечение",  >  \*\*\*\* чтобы отжать ее.</span><span class="sxs-lookup"><span data-stu-id="786bf-154">Right-click the zipped folder you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
1. <span data-ttu-id="786bf-155">Подключите HoloLens к компьютеру с помощью кабеля micro-USB, который он использовал.</span><span class="sxs-lookup"><span data-stu-id="786bf-155">Connect your HoloLens to your PC using the micro-USB cable that it came with.</span></span> <span data-ttu-id="786bf-156">(Даже если вы использовали для подключения HoloLens другие кабели, этот работает лучше.)</span><span class="sxs-lookup"><span data-stu-id="786bf-156">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
1. <span data-ttu-id="786bf-157">WDRT автоматически обнаружит HoloLens.</span><span class="sxs-lookup"><span data-stu-id="786bf-157">The WDRT will automatically detect your HoloLens.</span></span> <span data-ttu-id="786bf-158">Выберите плитку **Microsoft HoloLens**.</span><span class="sxs-lookup"><span data-stu-id="786bf-158">Select the **Microsoft HoloLens** tile.</span></span>
1. <span data-ttu-id="786bf-159">На следующем экране \*\*\*\* выберите выбор пакета вручную и выберите установочный файл, содержащийся в папке, которая была растерчена на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="786bf-159">On the next screen, select **Manual package selection** and choose the installation file contained in the folder you unzipped in step 4.</span></span> <span data-ttu-id="786bf-160">(Найми файл с расширением FFU.)</span><span class="sxs-lookup"><span data-stu-id="786bf-160">(Look for a file with the .ffu extension.)</span></span>
1. <span data-ttu-id="786bf-161">Выберите **"Установить программное**обеспечение" и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="786bf-161">Select **Install software**, and follow the instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="786bf-162">Если WDRT не обнаруживает HoloLens, попробуйте перезапустить компьютер.</span><span class="sxs-lookup"><span data-stu-id="786bf-162">If the WDRT doesn't detect your HoloLens, try restarting your PC.</span></span> <span data-ttu-id="786bf-163">Если это не поможет, выберите **Мое устройство не обнаружено**, выберите **Microsoft HoloLens** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="786bf-163">If that doesn't work, select **My device was not detected**, select **Microsoft HoloLens**, and then follow the instructions.</span></span>

## <span data-ttu-id="786bf-164">Программа insider Windows на HoloLens</span><span class="sxs-lookup"><span data-stu-id="786bf-164">Windows Insider Program on HoloLens</span></span>

<span data-ttu-id="786bf-165">Хотите увидеть последние функции HoloLens?</span><span class="sxs-lookup"><span data-stu-id="786bf-165">Want to see the latest features in HoloLens?</span></span>  <span data-ttu-id="786bf-166">Если да, присоединяйтесь к программе программы программы insider Windows; вы получите доступ к предварительным сборкам обновлений программного обеспечения HoloLens, прежде чем они будут доступны для всех.</span><span class="sxs-lookup"><span data-stu-id="786bf-166">If so, join the Windows Insider Program; you'll get access to preview builds of HoloLens software updates before they're available to the general public.</span></span>

<span data-ttu-id="786bf-167">[Получите предварительную версию Программы предварительной версии Windows для Microsoft HoloLens.](hololens-insider.md)</span><span class="sxs-lookup"><span data-stu-id="786bf-167">[Get Windows Insider preview for Microsoft HoloLens](hololens-insider.md).</span></span>
