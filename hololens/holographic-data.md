---
title: Поиск и сохранение файлов на HoloLens
description: Просмотр файлов на устройстве и управление ими с помощью проводника на HoloLens
keywords: инструкции по использованию средств выбора файлов, файлов, фотографий, видео, изображений, OneDrive, системы хранения данных, проводника, а также hololens
ms.assetid: 77d2e357-f65f-43c8-b62f-6cd9bf37070a
author: mattzmsft
ms.author: mazeller
manager: v-miegge
ms.reviewer: jarrettrenshaw
ms.date: 12/30/2019
ms.prod: hololens
ms.sitesec: library
ms.topic: article
audience: ITPro
ms.localizationpriority: medium
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: fb3287f0a074eddeac0c7ee2871e289b93eafcac
ms.sourcegitcommit: 8b56f4b9b5f9c928fc361f18efcbea729055a0b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2020
ms.locfileid: "10919130"
---
# <span data-ttu-id="ba433-104">Поиск, открытие и сохранение файлов в HoloLens</span><span class="sxs-lookup"><span data-stu-id="ba433-104">Find, open, and save files on HoloLens</span></span>

<span data-ttu-id="ba433-105">Файлы, созданные на HoloLens, в том числе фотографии и видео, сохраняются прямо на устройстве HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba433-105">Files you create on HoloLens, including photos and videos, are saved directly to your HoloLens device.</span></span> <span data-ttu-id="ba433-106">Просматривайте эти файлы и управляйте ими так же, как и при управлении файлами в Windows 10:</span><span class="sxs-lookup"><span data-stu-id="ba433-106">View and manage them in the same way you would manage files on Windows 10:</span></span>

- <span data-ttu-id="ba433-107">Использование приложения "Проводник" для доступа к локальным папкам.</span><span class="sxs-lookup"><span data-stu-id="ba433-107">Using the File Explorer app to access local folders.</span></span>
- <span data-ttu-id="ba433-108">В хранилище приложения.</span><span class="sxs-lookup"><span data-stu-id="ba433-108">Within an app's storage.</span></span>
- <span data-ttu-id="ba433-109">В особой папке (например, в библиотеке "видео" или "музыкальная библиотека").</span><span class="sxs-lookup"><span data-stu-id="ba433-109">In a special folder (such as the video or music library).</span></span>
- <span data-ttu-id="ba433-110">С помощью службы хранилища, в которую входит приложение и средство выбора файлов (например, OneDrive).</span><span class="sxs-lookup"><span data-stu-id="ba433-110">Using a storage service that includes an app and file picker (such as OneDrive).</span></span>
- <span data-ttu-id="ba433-111">Использование настольного компьютера, подключенного к HoloLens, с помощью USB-кабеля с помощью протокола MTP (протокол передачи мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="ba433-111">Using a desktop PC connected to your HoloLens by using a USB cable, using MTP (Media Transfer Protocol) support.</span></span>

## <span data-ttu-id="ba433-112">Просмотр файлов на HoloLens с помощью проводника</span><span class="sxs-lookup"><span data-stu-id="ba433-112">View files on HoloLens using File Explorer</span></span>

> <span data-ttu-id="ba433-113">Применимо ко всем устройствам HoloLens 2 и HoloLens (1-го поколения) по состоянию на [Windows 10 апрель 2018 (RS4) для HoloLens](https://docs.microsoft.com/windows/mixed-reality/release-notes-april-2018).</span><span class="sxs-lookup"><span data-stu-id="ba433-113">Applies to all HoloLens 2 devices and HoloLens (1st gen) as of the [Windows 10 April 2018 Update (RS4) for HoloLens](https://docs.microsoft.com/windows/mixed-reality/release-notes-april-2018).</span></span>

<span data-ttu-id="ba433-114">Используйте проводник на HoloLens для просмотра файлов на устройстве, включая трехмерные объекты, документы и изображения, и управления ими.</span><span class="sxs-lookup"><span data-stu-id="ba433-114">Use File Explorer on HoloLens to view and manage files on your device, including 3D objects, documents, and pictures.</span></span> <span data-ttu-id="ba433-115">Чтобы приступить к работе, **запустите**   >  проводник для**всех приложений**   >  **File Explorer** .</span><span class="sxs-lookup"><span data-stu-id="ba433-115">Go to **Start**  > **All apps**  > **File Explorer** to get started.</span></span>

> [!TIP]
> <span data-ttu-id="ba433-116">Если в проводнике нет файлов, выберите **это устройство** в левой верхней области.</span><span class="sxs-lookup"><span data-stu-id="ba433-116">If there are no files listed in File Explorer, select **This Device** in the top left pane.</span></span>

<span data-ttu-id="ba433-117">Если вы не видите ни одного файла в проводнике, фильтр "последние" может быть активен (в левой области выделена кнопка со значком часы).</span><span class="sxs-lookup"><span data-stu-id="ba433-117">If you don’t see any files in File Explorer, the "Recent" filter may be active (clock icon is highlighted in left pane).</span></span> <span data-ttu-id="ba433-118">Чтобы устранить эту проблему, щелкните значок этого документа на **устройстве** в левой области (под значком часов) или откройте меню и выберите нужное **устройство**.</span><span class="sxs-lookup"><span data-stu-id="ba433-118">To fix this, select the **This Device** document icon in the left pane (beneath the clock icon), or open the menu and select **This Device**.</span></span>

## <span data-ttu-id="ba433-119">Поиск и просмотр фотографий и видеороликов</span><span class="sxs-lookup"><span data-stu-id="ba433-119">Find and view your photos and videos</span></span>

<span data-ttu-id="ba433-120">[Смешанный захват реальности](holographic-photos-and-videos.md) позволяет создавать фотографии и видеоролики с разными фотографиями в среде HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba433-120">[Mixed reality capture](holographic-photos-and-videos.md) lets you take mixed reality photos and videos on HoloLens.</span></span>  <span data-ttu-id="ba433-121">Эти фото-и видеофайлы сохраняются в папке рулона камеры устройства.</span><span class="sxs-lookup"><span data-stu-id="ba433-121">These photos and videos are saved to the device's Camera Roll folder.</span></span>

<span data-ttu-id="ba433-122">Вы можете получить доступ к фотографиям и видеороликам, созданным с помощью HoloLens:</span><span class="sxs-lookup"><span data-stu-id="ba433-122">You can access photos and videos taken with HoloLens by:</span></span>

- <span data-ttu-id="ba433-123">доступ к фотоальбому напрямую через [приложение "фотографии](holographic-photos-and-videos.md)".</span><span class="sxs-lookup"><span data-stu-id="ba433-123">accessing the Camera Roll directly through the [Photos app](holographic-photos-and-videos.md).</span></span>
- <span data-ttu-id="ba433-124">отправлять фотографии и видеозаписи в облачное хранилище, синхронизируя фотографии и видео с OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ba433-124">uploading photos and videos to cloud storage by syncing your photos and videos to OneDrive.</span></span>
- <span data-ttu-id="ba433-125">с помощью страницы "смешанная запись в реальности" на [портале устройств Windows](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal#mixed-reality-capture).</span><span class="sxs-lookup"><span data-stu-id="ba433-125">using the Mixed Reality Capture page of the [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal#mixed-reality-capture).</span></span>

### <span data-ttu-id="ba433-126">Приложение "Фотографии"</span><span class="sxs-lookup"><span data-stu-id="ba433-126">Photos app</span></span>

<span data-ttu-id="ba433-127">Приложение "фотографии" — это одно из приложений по умолчанию в меню " **Пуск** ", встроенное в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba433-127">The Photos app is one of the default apps on the **Start** menu, and comes built-in with HoloLens.</span></span> <span data-ttu-id="ba433-128">Узнайте больше о том [, как использовать приложение фото для просмотра содержимого](holographic-photos-and-videos.md).</span><span class="sxs-lookup"><span data-stu-id="ba433-128">Learn more about [using the Photos app to view content](holographic-photos-and-videos.md).</span></span>

<span data-ttu-id="ba433-129">Вы также можете установить [приложение OneDrive](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) из Microsoft Store, чтобы синхронизировать фотографии с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="ba433-129">You can also install the [OneDrive app](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) from the Microsoft Store to sync photos to other devices.</span></span>

### <span data-ttu-id="ba433-130">Приложение OneDrive</span><span class="sxs-lookup"><span data-stu-id="ba433-130">OneDrive app</span></span>

<span data-ttu-id="ba433-131">С помощью [OneDrive](https://onedrive.live.com/) вы можете получать доступ к фотографиям и видеороликам, управлять ими, а также предоставлять к ним доступ с любого устройства и с любым пользователем.</span><span class="sxs-lookup"><span data-stu-id="ba433-131">[OneDrive](https://onedrive.live.com/) lets you access, manage, and share your photos and videos with any device and with any user.</span></span> <span data-ttu-id="ba433-132">Чтобы получить доступ к фотографиям и видеозаписям, собранным на HoloLens, скачайте [приложение OneDrive](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) из Microsoft Store на hololens.</span><span class="sxs-lookup"><span data-stu-id="ba433-132">To access the photos and videos captured on HoloLens, download the [OneDrive app](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) from the Microsoft Store on your HoloLens.</span></span> <span data-ttu-id="ba433-133">После скачивания откройте приложение OneDrive и выберите **Параметры**  >  **отправки камеры**и включите функцию **отправки камеры**.</span><span class="sxs-lookup"><span data-stu-id="ba433-133">Once downloaded, open the OneDrive app and select **Settings** > **Camera upload**, and turn on **Camera upload**.</span></span>

### <span data-ttu-id="ba433-134">Подключение к компьютеру</span><span class="sxs-lookup"><span data-stu-id="ba433-134">Connect to a PC</span></span>

<span data-ttu-id="ba433-135">Если на HoloLens запущено [Обновление Windows 10 апрель 2018](https://docs.microsoft.com/windows/mixed-reality/release-notes-april-2018) или более поздней версии, вы можете подключить HOLOLENS к компьютеру с Windows 10 с помощью USB-кабеля для просмотра фотографий и видео на устройстве с помощью MTP (протокол передачи мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="ba433-135">If your HoloLens is running the [Windows 10 April 2018 update](https://docs.microsoft.com/windows/mixed-reality/release-notes-april-2018) or later, you can connect your HoloLens to a Windows 10 PC by using a USB cable to browse photos and videos on the device by using MTP (media transfer protocol).</span></span> <span data-ttu-id="ba433-136">Необходимо убедиться, что устройство разблокировано для просмотра файлов, если на вашем устройстве установлен ПИН-код или пароль.</span><span class="sxs-lookup"><span data-stu-id="ba433-136">You'll need to make sure the device is unlocked to browse files if you have a PIN or password set up on your device.</span></span>  

<span data-ttu-id="ba433-137">Если вы включили [портал устройств Windows](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal), вы можете использовать его для просмотра и поиска фотографий и видео, сохраненных на устройстве, и управления ими.</span><span class="sxs-lookup"><span data-stu-id="ba433-137">If you have enabled the [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal), you can use it to browse, retrieve, and manage the photos and videos stored on your device.</span></span>

## <span data-ttu-id="ba433-138">Доступ к файлам в приложении</span><span class="sxs-lookup"><span data-stu-id="ba433-138">Access files within an app</span></span>

<span data-ttu-id="ba433-139">Если приложение сохраняет файлы на устройстве, вы можете использовать это приложение для доступа к ним.</span><span class="sxs-lookup"><span data-stu-id="ba433-139">If an application saves files on your device, you can use that application to access them.</span></span>

### <span data-ttu-id="ba433-140">Запрос файлов из другого приложения</span><span class="sxs-lookup"><span data-stu-id="ba433-140">Requesting files from another app</span></span>

<span data-ttu-id="ba433-141">Приложение может запросить сохранение файла или открыть файл из другого приложения с помощью средства [выбора файлов](https://docs.microsoft.com/windows/mixed-reality/app-model#file-pickers).</span><span class="sxs-lookup"><span data-stu-id="ba433-141">An application can request to save a file or open a file from another app by using [file pickers](https://docs.microsoft.com/windows/mixed-reality/app-model#file-pickers).</span></span>

### <span data-ttu-id="ba433-142">Известные папки</span><span class="sxs-lookup"><span data-stu-id="ba433-142">Known folders</span></span>

<span data-ttu-id="ba433-143">HoloLens поддерживает ряд [известных папок](https://docs.microsoft.com/windows/mixed-reality/app-model#known-folders) , которые приложения могут запрашивать разрешение на доступ.</span><span class="sxs-lookup"><span data-stu-id="ba433-143">HoloLens supports a number of [known folders](https://docs.microsoft.com/windows/mixed-reality/app-model#known-folders) that apps can request permission to access.</span></span>

## <span data-ttu-id="ba433-144">Просмотр файлов HoloLens на компьютере</span><span class="sxs-lookup"><span data-stu-id="ba433-144">View HoloLens files on your PC</span></span>

<span data-ttu-id="ba433-145">Как и другие мобильные устройства, подключите HoloLens к классическому компьютеру с помощью MTP (протокол передачи мультимедиа) и откройте проводник на компьютере, чтобы получить доступ к библиотекам HoloLens для упрощения передачи.</span><span class="sxs-lookup"><span data-stu-id="ba433-145">Similar to other mobile devices, connect HoloLens to your desktop PC using MTP (Media Transfer Protocol) and open File Explorer on the PC to access your HoloLens libraries for easy transfer.</span></span>

<span data-ttu-id="ba433-146">Чтобы просмотреть файлы HoloLens в проводнике на компьютере, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba433-146">To see your HoloLens files in File Explorer on your PC:</span></span>

1. <span data-ttu-id="ba433-147">Войдите в HoloLens, затем подключите его к компьютеру с помощью USB-кабеля, который поставляется с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba433-147">Sign in to HoloLens, then plug it into the PC using the USB cable that came with the HoloLens.</span></span>

1. <span data-ttu-id="ba433-148">Выберите команду **открыть устройство для просмотра файлов с помощью проводника**или откройте проводник на компьютере и перейдите к устройству.</span><span class="sxs-lookup"><span data-stu-id="ba433-148">Select **Open Device to view files with File Explorer**, or open File Explorer on the PC and navigate to the device.</span></span>

<span data-ttu-id="ba433-149">Чтобы просмотреть сведения о HoloLens, щелкните правой кнопкой мыши имя устройства в проводнике на компьютере, а затем выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="ba433-149">To see info about your HoloLens, right-click the device name in File Explorer on your PC, then select **Properties**.</span></span>

> [!NOTE]
> <span data-ttu-id="ba433-150">HoloLens (1-го поколения) не поддерживает подключение к внешним жестким дискам и картам SD.</span><span class="sxs-lookup"><span data-stu-id="ba433-150">HoloLens (1st gen) does not support connecting to external hard drives or SD cards.</span></span>

## <span data-ttu-id="ba433-151">Синхронизация с облаком</span><span class="sxs-lookup"><span data-stu-id="ba433-151">Sync to the cloud</span></span>

<span data-ttu-id="ba433-152">Чтобы синхронизировать фотографии и другие файлы из HoloLens с облаком, установите и настройте OneDrive для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba433-152">To sync photos and other files from your HoloLens to the cloud, install and set up OneDrive on HoloLens.</span></span> <span data-ttu-id="ba433-153">Чтобы получить доступ к OneDrive, выполните поиск по запросу в Microsoft Store на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="ba433-153">To get OneDrive, search for it in the Microsoft Store on your HoloLens.</span></span>

<span data-ttu-id="ba433-154">HoloLens не позволяет создавать резервные копии файлов и данных приложения, поэтому рекомендуется сохранить важные данные в OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ba433-154">HoloLens doesn't back up app files and data, so it's a good idea to save your important stuff to OneDrive.</span></span> <span data-ttu-id="ba433-155">Таким образом, при сбросе устройства или удалении приложения ваши данные будут заархивированы.</span><span class="sxs-lookup"><span data-stu-id="ba433-155">That way, if you reset your device or uninstall an app, your info will be backed up.</span></span>
