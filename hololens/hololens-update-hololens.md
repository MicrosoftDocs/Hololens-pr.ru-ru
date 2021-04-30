---
title: Обновление HoloLens
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
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: ef1721c60aca82d20e60636cbf4301de81c0177c
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309511"
---
# <a name="update-hololens"></a><span data-ttu-id="f906d-104">Обновление HoloLens</span><span class="sxs-lookup"><span data-stu-id="f906d-104">Update HoloLens</span></span>

<span data-ttu-id="f906d-105">HoloLens использует Центр обновления Windows, как и другие устройства Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f906d-105">HoloLens uses Windows Update, just like other Windows 10 devices.</span></span> <span data-ttu-id="f906d-106">HoloLens автоматически скачивает и устанавливает обновления системы при подключении к электросети и подключению к Интернету, даже если она находится в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="f906d-106">Your HoloLens will automatically download and install system updates whenever it is plugged-in to power and connected to the Internet, even when it is in standby.</span></span>

<span data-ttu-id="f906d-107">В этой статье будут рассмотрены средства HoloLens для:</span><span class="sxs-lookup"><span data-stu-id="f906d-107">This article will walk through HoloLens tools for:</span></span>

- <span data-ttu-id="f906d-108">Просмотр текущей версии операционной системы (номер сборки)</span><span class="sxs-lookup"><span data-stu-id="f906d-108">viewing your current operating system version (build number)</span></span>
- <span data-ttu-id="f906d-109">Проверка наличия обновлений</span><span class="sxs-lookup"><span data-stu-id="f906d-109">checking for updates</span></span>
- <span data-ttu-id="f906d-110">Обновление HoloLens вручную</span><span class="sxs-lookup"><span data-stu-id="f906d-110">manually updating HoloLens</span></span>
- <span data-ttu-id="f906d-111">откат к более старому обновлению</span><span class="sxs-lookup"><span data-stu-id="f906d-111">rolling back to an older update</span></span>

## <a name="check-your-operating-system-version-build-number"></a><span data-ttu-id="f906d-112">Проверка версии операционной системы (номер сборки)</span><span class="sxs-lookup"><span data-stu-id="f906d-112">Check your operating system version (build number)</span></span>

<span data-ttu-id="f906d-113">Чтобы проверить номер версии системы (номер сборки), откройте приложение параметры и выберите **система**  >  **о программе**.</span><span class="sxs-lookup"><span data-stu-id="f906d-113">You can verify the system version number, (build number) by opening the Settings app and selecting **System** > **About**.</span></span>

## <a name="check-for-updates-and-manually-update"></a><span data-ttu-id="f906d-114">Проверка наличия обновлений и ручное обновление</span><span class="sxs-lookup"><span data-stu-id="f906d-114">Check for updates and manually update</span></span>

<span data-ttu-id="f906d-115">Проверить наличие обновлений можно в любое время в параметрах.</span><span class="sxs-lookup"><span data-stu-id="f906d-115">You can check for updates any time in settings.</span></span>  <span data-ttu-id="f906d-116">Чтобы просмотреть доступные обновления и проверить наличие новых обновлений, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f906d-116">To see available updates and check for new updates:</span></span>

1. <span data-ttu-id="f906d-117">Откройте приложение **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="f906d-117">Open the **Settings** app.</span></span>
1. <span data-ttu-id="f906d-118">Перейдите к разделу **Update & Security**  >  **Центр обновления Windows**.</span><span class="sxs-lookup"><span data-stu-id="f906d-118">Navigate to **Update & Security** > **Windows Update**.</span></span>
1. <span data-ttu-id="f906d-119">Выберите команду **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="f906d-119">Select **Check for updates**.</span></span>

<span data-ttu-id="f906d-120">Если обновление доступно, начнется скачивание новой версии.</span><span class="sxs-lookup"><span data-stu-id="f906d-120">If an update is available, it will start downloading the new version.</span></span> <span data-ttu-id="f906d-121">После завершения загрузки нажмите кнопку **Перезагрузить сейчас** , чтобы запустить установку.</span><span class="sxs-lookup"><span data-stu-id="f906d-121">After the download is complete, select the **Restart Now** button to trigger the installation.</span></span> <span data-ttu-id="f906d-122">Если устройство находится ниже 40% и не подключено к сети, то при перезапуске установка обновления не начнется.</span><span class="sxs-lookup"><span data-stu-id="f906d-122">If your device is below 40% and not plugged in, restarting will not start installing the update.</span></span>

<span data-ttu-id="f906d-123">Хотя HoloLens устанавливает обновление, в нем отображаются вращающиеся устройства и индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f906d-123">While your HoloLens is installing the update, it will display spinning gears and a progress indicator.</span></span> <span data-ttu-id="f906d-124">Не отключайте HoloLens в течение этого времени.</span><span class="sxs-lookup"><span data-stu-id="f906d-124">Do not turn off your HoloLens during this time.</span></span> <span data-ttu-id="f906d-125">После завершения установки она будет автоматически перезапущена.</span><span class="sxs-lookup"><span data-stu-id="f906d-125">It will restart automatically once it has completed the installation.</span></span>

<span data-ttu-id="f906d-126">HoloLens применяет одно обновление за раз.</span><span class="sxs-lookup"><span data-stu-id="f906d-126">HoloLens applies one update at a time.</span></span>  <span data-ttu-id="f906d-127">Если HoloLens является более одной версией за последнюю версию, может потребоваться несколько раз выполнить обновление, чтобы полностью обновить его.</span><span class="sxs-lookup"><span data-stu-id="f906d-127">If your HoloLens is more than one version behind the latest you may need to run through the update process multiple times to get it fully up to date.</span></span>

## <a name="go-back-to-a-previous-version---hololens-2"></a><span data-ttu-id="f906d-128">Вернуться к предыдущей версии — HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="f906d-128">Go back to a previous version - HoloLens 2</span></span>

<span data-ttu-id="f906d-129">В некоторых случаях может потребоваться вернуться к предыдущей версии программного обеспечения HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f906d-129">In some cases, you might want to go back to a previous version of the HoloLens software.</span></span> <span data-ttu-id="f906d-130">Это можно сделать с помощью расширенного помощника по восстановлению, чтобы сбросить настройки HoloLens к более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="f906d-130">You can do this by using the Advanced Recovery Companion to reset your HoloLens to the earlier version.</span></span>

> [!NOTE]
> <span data-ttu-id="f906d-131">При возврате к более ранней версии удаляются личные файлы и параметры.</span><span class="sxs-lookup"><span data-stu-id="f906d-131">Going back to an earlier version deletes your personal files and settings.</span></span>

<span data-ttu-id="f906d-132">Чтобы вернуться к предыдущей версии HoloLens 2, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f906d-132">To go back to a previous version of HoloLens 2, follow these steps:</span></span>

1. <span data-ttu-id="f906d-133">Убедитесь, что у вас нет телефонов или устройств Windows, подключенных к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="f906d-133">Make sure that you don't have any phones or Windows devices plugged in to your PC.</span></span>
1. <span data-ttu-id="f906d-134">На компьютере Скачайте [Расширенный помощник по восстановлению](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) из Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f906d-134">On your PC, download the [Advanced Recovery Companion](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) from the Microsoft Store.</span></span>
1. <span data-ttu-id="f906d-135">Скачайте последнюю [версию HoloLens 2](https://aka.ms/hololens2download).</span><span class="sxs-lookup"><span data-stu-id="f906d-135">Download the [most recent HoloLens 2 release](https://aka.ms/hololens2download).</span></span>
1. <span data-ttu-id="f906d-136">После завершения загрузки откройте **файл**  >  **downloads** в проводнике.</span><span class="sxs-lookup"><span data-stu-id="f906d-136">When you have finished these downloads, open **File explorer** > **Downloads**.</span></span> <span data-ttu-id="f906d-137">Щелкните правой кнопкой мыши скачанную ZIP-папку и выберите **извлечь все**  >  **извлечь** , чтобы распаковать ее.</span><span class="sxs-lookup"><span data-stu-id="f906d-137">Right-click the zipped folder that you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
1. <span data-ttu-id="f906d-138">Подключите HoloLens к компьютеру, используя кабель USB-A – USB-C.</span><span class="sxs-lookup"><span data-stu-id="f906d-138">Connect your HoloLens to your PC using a USB-A to USB-C cable.</span></span> <span data-ttu-id="f906d-139">(Даже если вы используете другие кабели для подключения HoloLens, это работает наилучшим образом.)</span><span class="sxs-lookup"><span data-stu-id="f906d-139">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
1. <span data-ttu-id="f906d-140">Помощник по расширенному восстановлению автоматически обнаруживает HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f906d-140">The Advanced Recovery Companion automatically detects your HoloLens.</span></span> <span data-ttu-id="f906d-141">Выберите плитку **Microsoft HoloLens** .</span><span class="sxs-lookup"><span data-stu-id="f906d-141">Select the **Microsoft HoloLens** tile.</span></span>
1. <span data-ttu-id="f906d-142">На следующем экране выберите **ручной выбор пакетов** , а затем выберите файл установки, содержащийся в папке, которая была распакована на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="f906d-142">On the next screen, select **Manual package selection** and then select the installation file contained in the folder that you unzipped in step 4.</span></span> <span data-ttu-id="f906d-143">(Найдите файл с расширением ФФУ.)</span><span class="sxs-lookup"><span data-stu-id="f906d-143">(Look for a file with the .ffu extension.)</span></span>
1. <span data-ttu-id="f906d-144">Выберите **установить программное обеспечение** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="f906d-144">Select **Install software**, and follow the instructions.</span></span>

## <a name="go-back-to-a-previous-version---hololens-1st-gen"></a><span data-ttu-id="f906d-145">Вернуться к предыдущей версии — HoloLens (1-й общий)</span><span class="sxs-lookup"><span data-stu-id="f906d-145">Go back to a previous version - HoloLens (1st Gen)</span></span>

<span data-ttu-id="f906d-146">В некоторых случаях может потребоваться вернуться к предыдущей версии программного обеспечения HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f906d-146">In some cases, you might want to go back to a previous version of the HoloLens software.</span></span> <span data-ttu-id="f906d-147">Это можно сделать с помощью средства восстановления устройств Windows, чтобы сбросить настройки HoloLens до более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="f906d-147">You can do this by using the Windows Device Recovery Tool to reset your HoloLens to the earlier version.</span></span>

> [!NOTE]
> <span data-ttu-id="f906d-148">При возврате к более ранней версии удаляются личные файлы и параметры.</span><span class="sxs-lookup"><span data-stu-id="f906d-148">Going back to an earlier version deletes your personal files and settings.</span></span>

<span data-ttu-id="f906d-149">Чтобы вернуться к предыдущей версии HoloLens 1, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f906d-149">To go back to a previous version of HoloLens 1, follow these steps:</span></span>

1. <span data-ttu-id="f906d-150">Убедитесь, что у вас нет телефонов или устройств Windows, подключенных к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="f906d-150">Make sure that you don't have any phones or Windows devices plugged in to your PC.</span></span>
1. <span data-ttu-id="f906d-151">На компьютере Скачайте [средство восстановления устройств Windows (вдрт)](https://support.microsoft.com/help/12379).</span><span class="sxs-lookup"><span data-stu-id="f906d-151">On your PC, download the [Windows Device Recovery Tool (WDRT)](https://support.microsoft.com/help/12379).</span></span>
1. <span data-ttu-id="f906d-152">Скачайте [пакет восстановления для годовщины HoloLens](https://aka.ms/hololensrecovery).</span><span class="sxs-lookup"><span data-stu-id="f906d-152">Download the [HoloLens Anniversary Update recovery package](https://aka.ms/hololensrecovery).</span></span>
1. <span data-ttu-id="f906d-153">После завершения загрузки откройте **файл**  >  **downloads** в проводнике.</span><span class="sxs-lookup"><span data-stu-id="f906d-153">When the downloads finish, open **File explorer** > **Downloads**.</span></span> <span data-ttu-id="f906d-154">Щелкните правой кнопкой мыши скачанную ZIP-папку и выберите **извлечь все**  >  **извлечь** , чтобы распаковать ее.</span><span class="sxs-lookup"><span data-stu-id="f906d-154">Right-click the zipped folder you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
1. <span data-ttu-id="f906d-155">Подключите HoloLens к компьютеру, используя кабель Micro-USB, поставляемый с ним.</span><span class="sxs-lookup"><span data-stu-id="f906d-155">Connect your HoloLens to your PC using the micro-USB cable that it came with.</span></span> <span data-ttu-id="f906d-156">(Даже если вы используете другие кабели для подключения HoloLens, это работает наилучшим образом.)</span><span class="sxs-lookup"><span data-stu-id="f906d-156">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
1. <span data-ttu-id="f906d-157">ВДРТ будет автоматически обнаруживать HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f906d-157">The WDRT will automatically detect your HoloLens.</span></span> <span data-ttu-id="f906d-158">Выберите плитку **Microsoft HoloLens** .</span><span class="sxs-lookup"><span data-stu-id="f906d-158">Select the **Microsoft HoloLens** tile.</span></span>
1. <span data-ttu-id="f906d-159">На следующем экране выберите **Ручное выделение пакетов** и выберите файл установки, содержащийся в папке, которая была распакована на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="f906d-159">On the next screen, select **Manual package selection** and choose the installation file contained in the folder you unzipped in step 4.</span></span> <span data-ttu-id="f906d-160">(Найдите файл с расширением ФФУ.)</span><span class="sxs-lookup"><span data-stu-id="f906d-160">(Look for a file with the .ffu extension.)</span></span>
1. <span data-ttu-id="f906d-161">Выберите **установить программное обеспечение** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="f906d-161">Select **Install software**, and follow the instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="f906d-162">Если ВДРТ не обнаруживает HoloLens, попробуйте перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="f906d-162">If the WDRT doesn't detect your HoloLens, try restarting your PC.</span></span> <span data-ttu-id="f906d-163">Если это не сработает, выберите пункт **мое устройство не обнаружено**, выберите **Microsoft HoloLens** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="f906d-163">If that doesn't work, select **My device was not detected**, select **Microsoft HoloLens**, and then follow the instructions.</span></span>

## <a name="windows-insider-program-on-hololens"></a><span data-ttu-id="f906d-164">Программа предварительной оценки Windows в HoloLens</span><span class="sxs-lookup"><span data-stu-id="f906d-164">Windows Insider Program on HoloLens</span></span>

<span data-ttu-id="f906d-165">Хотите просмотреть новейшие функции в HoloLens?</span><span class="sxs-lookup"><span data-stu-id="f906d-165">Want to see the latest features in HoloLens?</span></span>  <span data-ttu-id="f906d-166">Если да, Присоединяйтесь к программе предварительной оценки Windows; Вы получите доступ к предварительным сборкам обновлений программного обеспечения HoloLens, прежде чем они будут доступны для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f906d-166">If so, join the Windows Insider Program; you'll get access to preview builds of HoloLens software updates before they're available to the general public.</span></span>

<span data-ttu-id="f906d-167">[Получите предварительную версию Windows Insider Preview для Microsoft HoloLens](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="f906d-167">[Get Windows Insider preview for Microsoft HoloLens](hololens-insider.md).</span></span>
