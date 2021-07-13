---
title: Поиск и сохранение файлов на HoloLens
description: узнайте, как использовать проводник на HoloLens для открытия, просмотра и управления файлами на устройстве смешанной реальности.
keywords: инструкции по использованию средства выбора файлов, файлов, фотографий, видео, изображений, OneDrive, хранилища, проводника, hololens
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
ms.openlocfilehash: 18dc962b869dafaea9ff9c605eef51fcbb35bfb2
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113636186"
---
# <a name="find-open-and-save-files-on-hololens"></a><span data-ttu-id="5f885-104">Поиск, открытие и сохранение файлов в HoloLens</span><span class="sxs-lookup"><span data-stu-id="5f885-104">Find, open, and save files on HoloLens</span></span>

<span data-ttu-id="5f885-105">файлы, создаваемые на HoloLens, включая фотографии и видео, сохраняются непосредственно на устройстве HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5f885-105">Files you create on HoloLens, including photos and videos, are saved directly to your HoloLens device.</span></span> <span data-ttu-id="5f885-106">Просматривайте их и управляйте ими так же, как и с файлами на Windows 10:</span><span class="sxs-lookup"><span data-stu-id="5f885-106">View and manage them in the same way you would manage files on Windows 10:</span></span>

- <span data-ttu-id="5f885-107">Использование приложения проводника для доступа к локальным папкам.</span><span class="sxs-lookup"><span data-stu-id="5f885-107">Using the File Explorer app to access local folders.</span></span>
- <span data-ttu-id="5f885-108">В хранилище приложения.</span><span class="sxs-lookup"><span data-stu-id="5f885-108">Within an app's storage.</span></span>
- <span data-ttu-id="5f885-109">В особой папке (например, в библиотеке видео или музыкальной библиотеки).</span><span class="sxs-lookup"><span data-stu-id="5f885-109">In a special folder (such as the video or music library).</span></span>
- <span data-ttu-id="5f885-110">Использование службы хранилища, включающей в себя приложение и средство выбора файлов (например, OneDrive).</span><span class="sxs-lookup"><span data-stu-id="5f885-110">Using a storage service that includes an app and file picker (such as OneDrive).</span></span>
- <span data-ttu-id="5f885-111">использование настольного пк, подключенного к HoloLens с помощью USB-кабеля и поддерживающего протокол передачи мультимедиа (MTP).</span><span class="sxs-lookup"><span data-stu-id="5f885-111">Using a desktop PC connected to your HoloLens by using a USB cable, using MTP (Media Transfer Protocol) support.</span></span>

## <a name="view-files-on-hololens-using-file-explorer"></a><span data-ttu-id="5f885-112">просмотр файлов на HoloLens с помощью проводника</span><span class="sxs-lookup"><span data-stu-id="5f885-112">View files on HoloLens using File Explorer</span></span>

> <span data-ttu-id="5f885-113">применяется ко всем HoloLens 2ным устройствам и HoloLens (1-й общий) с [обновлениями Windows 10 апреля 2018 (RS4) для HoloLens](/windows/mixed-reality/release-notes-april-2018).</span><span class="sxs-lookup"><span data-stu-id="5f885-113">Applies to all HoloLens 2 devices and HoloLens (1st gen) as of the [Windows 10 April 2018 Update (RS4) for HoloLens](/windows/mixed-reality/release-notes-april-2018).</span></span>

<span data-ttu-id="5f885-114">используйте проводник на HoloLens для просмотра и управления файлами на устройстве, включая трехмерные объекты, документы и изображения.</span><span class="sxs-lookup"><span data-stu-id="5f885-114">Use File Explorer on HoloLens to view and manage files on your device, including 3D objects, documents, and pictures.</span></span> <span data-ttu-id="5f885-115">Чтобы начать работу, перейдите в раздел **Запуск**   >  **всех приложений**   >  **проводник** .</span><span class="sxs-lookup"><span data-stu-id="5f885-115">Go to **Start**  > **All apps**  > **File Explorer** to get started.</span></span>

> [!TIP]
> <span data-ttu-id="5f885-116">Если в проводнике нет файлов, выберите **это устройство** в верхней левой области.</span><span class="sxs-lookup"><span data-stu-id="5f885-116">If there are no files listed in File Explorer, select **This Device** in the top left pane.</span></span>

<span data-ttu-id="5f885-117">Если в проводнике не отображаются файлы, то фильтр "последние" может быть активным (значок "Часы" выделяется в левой области).</span><span class="sxs-lookup"><span data-stu-id="5f885-117">If you don’t see any files in File Explorer, the "Recent" filter may be active (clock icon is highlighted in left pane).</span></span> <span data-ttu-id="5f885-118">Чтобы устранить эту проблему, щелкните значок документа **этого устройства** в левой области (под значком часов) или откройте меню и выберите **это устройство**.</span><span class="sxs-lookup"><span data-stu-id="5f885-118">To fix this, select the **This Device** document icon in the left pane (beneath the clock icon), or open the menu and select **This Device**.</span></span>

## <a name="find-and-view-your-photos-and-videos"></a><span data-ttu-id="5f885-119">Поиск и просмотр фотографий и видео</span><span class="sxs-lookup"><span data-stu-id="5f885-119">Find and view your photos and videos</span></span>

<span data-ttu-id="5f885-120">[Запись смешанной реальности](holographic-photos-and-videos.md) позволяет использовать фотографии и видеоролики смешанной реальности на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5f885-120">[Mixed reality capture](holographic-photos-and-videos.md) lets you take mixed reality photos and videos on HoloLens.</span></span>  <span data-ttu-id="5f885-121">Эти фотографии и видеозаписи сохраняются в папке рулона камеры устройства.</span><span class="sxs-lookup"><span data-stu-id="5f885-121">These photos and videos are saved to the device's Camera Roll folder.</span></span>

<span data-ttu-id="5f885-122">доступ к фотографиям и видеороликам, созданным с помощью HoloLens, можно получить следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5f885-122">You can access photos and videos taken with HoloLens by:</span></span>

- <span data-ttu-id="5f885-123">доступ к фотоальбому через [приложение Photos](holographic-photos-and-videos.md).</span><span class="sxs-lookup"><span data-stu-id="5f885-123">accessing the Camera Roll directly through the [Photos app](holographic-photos-and-videos.md).</span></span>
- <span data-ttu-id="5f885-124">Отправка фотографий и видео в облачное хранилище путем синхронизации фотографий и видео с OneDrive.</span><span class="sxs-lookup"><span data-stu-id="5f885-124">uploading photos and videos to cloud storage by syncing your photos and videos to OneDrive.</span></span>
- <span data-ttu-id="5f885-125">на странице "запись смешанной реальности" на [портале устройств Windows](/windows/mixed-reality/using-the-windows-device-portal#mixed-reality-capture).</span><span class="sxs-lookup"><span data-stu-id="5f885-125">using the Mixed Reality Capture page of the [Windows Device Portal](/windows/mixed-reality/using-the-windows-device-portal#mixed-reality-capture).</span></span>

### <a name="photos-app"></a><span data-ttu-id="5f885-126">Приложение "Фотографии"</span><span class="sxs-lookup"><span data-stu-id="5f885-126">Photos app</span></span>

<span data-ttu-id="5f885-127">Приложение Photos — одно из приложений по умолчанию в меню " **Пуск** ", которое встроено в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5f885-127">The Photos app is one of the default apps on the **Start** menu, and comes built-in with HoloLens.</span></span> <span data-ttu-id="5f885-128">Дополнительные сведения об [использовании приложения "фотографии" для просмотра содержимого](holographic-photos-and-videos.md).</span><span class="sxs-lookup"><span data-stu-id="5f885-128">Learn more about [using the Photos app to view content](holographic-photos-and-videos.md).</span></span>

<span data-ttu-id="5f885-129">вы также можете установить [OneDrive приложение](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) из Microsoft Store для синхронизации фотографий с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="5f885-129">You can also install the [OneDrive app](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) from the Microsoft Store to sync photos to other devices.</span></span>

### <a name="onedrive-app"></a><span data-ttu-id="5f885-130">Приложение OneDrive</span><span class="sxs-lookup"><span data-stu-id="5f885-130">OneDrive app</span></span>

<span data-ttu-id="5f885-131">[OneDrive](https://onedrive.live.com/) позволяет получать доступ к фотографиям и видео, а также управлять ими с помощью любого устройства и любого пользователя.</span><span class="sxs-lookup"><span data-stu-id="5f885-131">[OneDrive](https://onedrive.live.com/) lets you access, manage, and share your photos and videos with any device and with any user.</span></span> <span data-ttu-id="5f885-132">чтобы получить доступ к фотографиям и видеороликам, захваченным на HoloLens, скачайте [приложение OneDrive](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) из Microsoft Store на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5f885-132">To access the photos and videos captured on HoloLens, download the [OneDrive app](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) from the Microsoft Store on your HoloLens.</span></span> <span data-ttu-id="5f885-133">после скачивания откройте приложение OneDrive и выберите **Параметры**  >  **отправить камеру**, а затем включите **отправку камеры**.</span><span class="sxs-lookup"><span data-stu-id="5f885-133">Once downloaded, open the OneDrive app and select **Settings** > **Camera upload**, and turn on **Camera upload**.</span></span>

### <a name="connect-to-a-pc"></a><span data-ttu-id="5f885-134">Подключение пк</span><span class="sxs-lookup"><span data-stu-id="5f885-134">Connect to a PC</span></span>

<span data-ttu-id="5f885-135">если на HoloLens выполняется [обновление Windows 10 апрель 2018](/windows/mixed-reality/release-notes-april-2018) или более поздней версии, вы можете подключить HoloLens к Windows 10ному компьютеру с помощью USB-кабеля, чтобы просматривать фотографии и видео на устройстве с помощью MTP (протокол передачи мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="5f885-135">If your HoloLens is running the [Windows 10 April 2018 update](/windows/mixed-reality/release-notes-april-2018) or later, you can connect your HoloLens to a Windows 10 PC by using a USB cable to browse photos and videos on the device by using MTP (media transfer protocol).</span></span> <span data-ttu-id="5f885-136">Необходимо убедиться, что устройство разблокировано для просмотра файлов, если на устройстве настроен ПИН-код или пароль.</span><span class="sxs-lookup"><span data-stu-id="5f885-136">You'll need to make sure the device is unlocked to browse files if you have a PIN or password set up on your device.</span></span>  

<span data-ttu-id="5f885-137">если вы включили [портал Windows устройств](/windows/mixed-reality/using-the-windows-device-portal), вы можете использовать его для просмотра, получения и управления фотографиями и видеозаписями, хранящимися на устройстве.</span><span class="sxs-lookup"><span data-stu-id="5f885-137">If you have enabled the [Windows Device Portal](/windows/mixed-reality/using-the-windows-device-portal), you can use it to browse, retrieve, and manage the photos and videos stored on your device.</span></span>

## <a name="access-files-within-an-app"></a><span data-ttu-id="5f885-138">Доступ к файлам в приложении</span><span class="sxs-lookup"><span data-stu-id="5f885-138">Access files within an app</span></span>

<span data-ttu-id="5f885-139">Если приложение сохраняет файлы на устройстве, вы можете использовать это приложение для доступа к ним.</span><span class="sxs-lookup"><span data-stu-id="5f885-139">If an application saves files on your device, you can use that application to access them.</span></span>

### <a name="requesting-files-from-another-app"></a><span data-ttu-id="5f885-140">Запрос файлов из другого приложения</span><span class="sxs-lookup"><span data-stu-id="5f885-140">Requesting files from another app</span></span>

<span data-ttu-id="5f885-141">Приложение может запросить сохранение файла или открыть файл из другого приложения с помощью средств [выбора файлов](/windows/mixed-reality/app-model#file-pickers).</span><span class="sxs-lookup"><span data-stu-id="5f885-141">An application can request to save a file or open a file from another app by using [file pickers](/windows/mixed-reality/app-model#file-pickers).</span></span>

### <a name="known-folders"></a><span data-ttu-id="5f885-142">Известные папки</span><span class="sxs-lookup"><span data-stu-id="5f885-142">Known folders</span></span>

<span data-ttu-id="5f885-143">HoloLens поддерживает несколько [известных папок](/windows/mixed-reality/app-model#known-folders) , которые приложения могут запрашивать разрешение на доступ.</span><span class="sxs-lookup"><span data-stu-id="5f885-143">HoloLens supports a number of [known folders](/windows/mixed-reality/app-model#known-folders) that apps can request permission to access.</span></span>

## <a name="view-hololens-files-on-your-pc"></a><span data-ttu-id="5f885-144">просмотр HoloLens файлов на компьютере</span><span class="sxs-lookup"><span data-stu-id="5f885-144">View HoloLens files on your PC</span></span>

<span data-ttu-id="5f885-145">аналогично другим мобильным устройствам подключите HoloLens к настольному компьютеру с помощью MTP (протокола передачи мультимедиа) и откройте проводник на компьютере, чтобы получить доступ к библиотекам HoloLens для удобного переноса.</span><span class="sxs-lookup"><span data-stu-id="5f885-145">Similar to other mobile devices, connect HoloLens to your desktop PC using MTP (Media Transfer Protocol) and open File Explorer on the PC to access your HoloLens libraries for easy transfer.</span></span>

<span data-ttu-id="5f885-146">чтобы просмотреть файлы HoloLens в проводнике на компьютере, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5f885-146">To see your HoloLens files in File Explorer on your PC:</span></span>

1. <span data-ttu-id="5f885-147">войдите в HoloLens, а затем подключите его к компьютеру, используя USB-кабель, поставляемый с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5f885-147">Sign in to HoloLens, then plug it into the PC using the USB cable that came with the HoloLens.</span></span>

1. <span data-ttu-id="5f885-148">Выберите пункт **открыть устройство, чтобы просмотреть файлы с помощью проводника**, или откройте проводник на компьютере и перейдите к устройству.</span><span class="sxs-lookup"><span data-stu-id="5f885-148">Select **Open Device to view files with File Explorer**, or open File Explorer on the PC and navigate to the device.</span></span>

<span data-ttu-id="5f885-149">чтобы просмотреть сведения о HoloLens, щелкните правой кнопкой мыши имя устройства в проводнике на компьютере и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="5f885-149">To see info about your HoloLens, right-click the device name in File Explorer on your PC, then select **Properties**.</span></span>

> [!NOTE]
> <span data-ttu-id="5f885-150">HoloLens (первое поколение) не поддерживает подключение к внешним жестким дискам или SD-картам.</span><span class="sxs-lookup"><span data-stu-id="5f885-150">HoloLens (1st gen) does not support connecting to external hard drives or SD cards.</span></span>

## <a name="sync-to-the-cloud"></a><span data-ttu-id="5f885-151">Синхронизация с облаком</span><span class="sxs-lookup"><span data-stu-id="5f885-151">Sync to the cloud</span></span>

<span data-ttu-id="5f885-152">чтобы синхронизировать фотографии и другие файлы из HoloLens в облако, установите и настройте OneDrive на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5f885-152">To sync photos and other files from your HoloLens to the cloud, install and set up OneDrive on HoloLens.</span></span> <span data-ttu-id="5f885-153">чтобы получить OneDrive, выполните поиск в Microsoft Store HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5f885-153">To get OneDrive, search for it in the Microsoft Store on your HoloLens.</span></span>

<span data-ttu-id="5f885-154">HoloLens не выполняет резервное копирование файлов и данных приложений, поэтому рекомендуется сохранить важные вещи для OneDrive.</span><span class="sxs-lookup"><span data-stu-id="5f885-154">HoloLens doesn't back up app files and data, so it's a good idea to save your important stuff to OneDrive.</span></span> <span data-ttu-id="5f885-155">Таким образом, если сбросить устройство или удалить приложение, будет создана резервная копия ваших сведений.</span><span class="sxs-lookup"><span data-stu-id="5f885-155">That way, if you reset your device or uninstall an app, your info will be backed up.</span></span>
