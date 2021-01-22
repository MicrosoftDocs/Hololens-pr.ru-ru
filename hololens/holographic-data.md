---
title: Поиск и сохранение файлов на HoloLens
description: Узнайте, как использовать проводник на HoloLens для открытия, просмотра и управления файлами на устройстве смешанной реальности.
keywords: how-to, file picker, files, photos, videos, pictures, OneDrive, storage, file explorer, hololens
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
ms.openlocfilehash: 2d979b2cffd20589ddef7f11db5c7206eaea23cb
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283530"
---
# <span data-ttu-id="c9c8b-104">Поиск, открытие и сохранение файлов в HoloLens</span><span class="sxs-lookup"><span data-stu-id="c9c8b-104">Find, open, and save files on HoloLens</span></span>

<span data-ttu-id="c9c8b-105">Файлы, которые вы создаете на устройстве HoloLens, включая фотографии и видео, сохраняются непосредственно на устройстве HoloLens.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-105">Files you create on HoloLens, including photos and videos, are saved directly to your HoloLens device.</span></span> <span data-ttu-id="c9c8b-106">Просматривайте и управляйте ими так же, как вы бы могли управлять файлами в Windows 10:</span><span class="sxs-lookup"><span data-stu-id="c9c8b-106">View and manage them in the same way you would manage files on Windows 10:</span></span>

- <span data-ttu-id="c9c8b-107">Использование проводника для доступа к локальным папок.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-107">Using the File Explorer app to access local folders.</span></span>
- <span data-ttu-id="c9c8b-108">В хранилище приложения.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-108">Within an app's storage.</span></span>
- <span data-ttu-id="c9c8b-109">В специальной папке (например, в библиотеке видео или музыки).</span><span class="sxs-lookup"><span data-stu-id="c9c8b-109">In a special folder (such as the video or music library).</span></span>
- <span data-ttu-id="c9c8b-110">Использование службы хранения, включаемой в себя приложение и выбор файлов (например, OneDrive).</span><span class="sxs-lookup"><span data-stu-id="c9c8b-110">Using a storage service that includes an app and file picker (such as OneDrive).</span></span>
- <span data-ttu-id="c9c8b-111">Использование настольного компьютера, подключенного к HoloLens с помощью USB-кабеля, с помощью поддержки протокола MTP (media Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="c9c8b-111">Using a desktop PC connected to your HoloLens by using a USB cable, using MTP (Media Transfer Protocol) support.</span></span>

## <span data-ttu-id="c9c8b-112">Просмотр файлов на HoloLens с помощью проводника</span><span class="sxs-lookup"><span data-stu-id="c9c8b-112">View files on HoloLens using File Explorer</span></span>

> <span data-ttu-id="c9c8b-113">Применяется ко всем устройствам HoloLens 2 и HoloLens (1-е поколения) с версии Обновления Windows 10 за апрель [2018 г. (RS4) для HoloLens.](https://docs.microsoft.com/windows/mixed-reality/release-notes-april-2018)</span><span class="sxs-lookup"><span data-stu-id="c9c8b-113">Applies to all HoloLens 2 devices and HoloLens (1st gen) as of the [Windows 10 April 2018 Update (RS4) for HoloLens](https://docs.microsoft.com/windows/mixed-reality/release-notes-april-2018).</span></span>

<span data-ttu-id="c9c8b-114">Используйте проводник на HoloLens для просмотра и управления файлами на устройстве, включая трехd-объекты, документы и изображения.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-114">Use File Explorer on HoloLens to view and manage files on your device, including 3D objects, documents, and pictures.</span></span> <span data-ttu-id="c9c8b-115">Чтобы **приступить к**   >  **работе, перейдите**в проводник   >  \*\*\*\* "Запустить все приложения".</span><span class="sxs-lookup"><span data-stu-id="c9c8b-115">Go to **Start**  > **All apps**  > **File Explorer** to get started.</span></span>

> [!TIP]
> <span data-ttu-id="c9c8b-116">Если в проводнике нет файлов, выберите **это** устройство в верхней левой области.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-116">If there are no files listed in File Explorer, select **This Device** in the top left pane.</span></span>

<span data-ttu-id="c9c8b-117">Если в проводнике нет файлов, фильтр "Последние" может быть активным (значок часов выделен в левой области).</span><span class="sxs-lookup"><span data-stu-id="c9c8b-117">If you don’t see any files in File Explorer, the "Recent" filter may be active (clock icon is highlighted in left pane).</span></span> <span data-ttu-id="c9c8b-118">Чтобы устранить эту проблему, выберите значок документа **"Это** устройство" в левой области (под значком часов) или откройте меню и выберите **"Это устройство".**</span><span class="sxs-lookup"><span data-stu-id="c9c8b-118">To fix this, select the **This Device** document icon in the left pane (beneath the clock icon), or open the menu and select **This Device**.</span></span>

## <span data-ttu-id="c9c8b-119">Поиск и просмотр фотографий и видео</span><span class="sxs-lookup"><span data-stu-id="c9c8b-119">Find and view your photos and videos</span></span>

<span data-ttu-id="c9c8b-120">[Смешанный захват реальности](holographic-photos-and-videos.md) позволяет делать фотографии смешанной реальности и видео на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-120">[Mixed reality capture](holographic-photos-and-videos.md) lets you take mixed reality photos and videos on HoloLens.</span></span>  <span data-ttu-id="c9c8b-121">Эти фотографии и видео сохраняются в папке roll камеры устройства.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-121">These photos and videos are saved to the device's Camera Roll folder.</span></span>

<span data-ttu-id="c9c8b-122">Вы можете получить доступ к фотографиям и видео, снятым с помощью HoloLens, с помощью:</span><span class="sxs-lookup"><span data-stu-id="c9c8b-122">You can access photos and videos taken with HoloLens by:</span></span>

- <span data-ttu-id="c9c8b-123">доступ к камере непосредственно через приложение ["Фотографии".](holographic-photos-and-videos.md)</span><span class="sxs-lookup"><span data-stu-id="c9c8b-123">accessing the Camera Roll directly through the [Photos app](holographic-photos-and-videos.md).</span></span>
- <span data-ttu-id="c9c8b-124">отправка фотографий и видео в облачное хранилище путем синхронизации фотографий и видео в OneDrive;</span><span class="sxs-lookup"><span data-stu-id="c9c8b-124">uploading photos and videos to cloud storage by syncing your photos and videos to OneDrive.</span></span>
- <span data-ttu-id="c9c8b-125">на странице "Смешанный захват реальности" портала [устройств Windows.](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal#mixed-reality-capture)</span><span class="sxs-lookup"><span data-stu-id="c9c8b-125">using the Mixed Reality Capture page of the [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal#mixed-reality-capture).</span></span>

### <span data-ttu-id="c9c8b-126">Приложение "Фотографии"</span><span class="sxs-lookup"><span data-stu-id="c9c8b-126">Photos app</span></span>

<span data-ttu-id="c9c8b-127">Приложение "Фотографии" является одним из \*\*\*\* приложений по умолчанию в меню "Пуск" и встроено в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-127">The Photos app is one of the default apps on the **Start** menu, and comes built-in with HoloLens.</span></span> <span data-ttu-id="c9c8b-128">Узнайте больше об [использовании приложения "Фотографии" для просмотра содержимого.](holographic-photos-and-videos.md)</span><span class="sxs-lookup"><span data-stu-id="c9c8b-128">Learn more about [using the Photos app to view content](holographic-photos-and-videos.md).</span></span>

<span data-ttu-id="c9c8b-129">Вы также можете установить приложение [OneDrive из](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) Microsoft Store, чтобы синхронизировать фотографии с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-129">You can also install the [OneDrive app](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) from the Microsoft Store to sync photos to other devices.</span></span>

### <span data-ttu-id="c9c8b-130">Приложение OneDrive</span><span class="sxs-lookup"><span data-stu-id="c9c8b-130">OneDrive app</span></span>

<span data-ttu-id="c9c8b-131">[OneDrive](https://onedrive.live.com/) позволяет получать доступ к фотографиям и видео, а также делиться ими с любым устройством и любым пользователем, а также управлять ими.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-131">[OneDrive](https://onedrive.live.com/) lets you access, manage, and share your photos and videos with any device and with any user.</span></span> <span data-ttu-id="c9c8b-132">Чтобы получить доступ к фотографиям и видео, захваченным на HoloLens, скачайте приложение [OneDrive](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) из Microsoft Store на holoLens.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-132">To access the photos and videos captured on HoloLens, download the [OneDrive app](https://www.microsoft.com/p/onedrive/9wzdncrfj1p3) from the Microsoft Store on your HoloLens.</span></span> <span data-ttu-id="c9c8b-133">После скачивания откройте приложение OneDrive и выберите **параметры**отправки с камеры и включите  >  \*\*\*\* **отправку с камеры.**</span><span class="sxs-lookup"><span data-stu-id="c9c8b-133">Once downloaded, open the OneDrive app and select **Settings** > **Camera upload**, and turn on **Camera upload**.</span></span>

### <span data-ttu-id="c9c8b-134">Подключение к компьютеру</span><span class="sxs-lookup"><span data-stu-id="c9c8b-134">Connect to a PC</span></span>

<span data-ttu-id="c9c8b-135">Если holoLens использует обновление Windows 10 за апрель [2018](https://docs.microsoft.com/windows/mixed-reality/release-notes-april-2018) г. или более поздней версии, вы можете подключить HoloLens к компьютеру с Windows 10 с помощью USB-кабеля для просмотра фотографий и видео на устройстве с помощью протокола MTP (протокола передачи мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="c9c8b-135">If your HoloLens is running the [Windows 10 April 2018 update](https://docs.microsoft.com/windows/mixed-reality/release-notes-april-2018) or later, you can connect your HoloLens to a Windows 10 PC by using a USB cable to browse photos and videos on the device by using MTP (media transfer protocol).</span></span> <span data-ttu-id="c9c8b-136">Убедитесь, что устройство разблокировано для просмотра файлов, если на вашем устройстве настроен PIN-код или пароль.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-136">You'll need to make sure the device is unlocked to browse files if you have a PIN or password set up on your device.</span></span>  

<span data-ttu-id="c9c8b-137">Если вы включили портал [устройств с Windows,](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal)вы можете использовать его для просмотра, извлечения фотографий и видео, хранимой на вашем устройстве, а также управления ими.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-137">If you have enabled the [Windows Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal), you can use it to browse, retrieve, and manage the photos and videos stored on your device.</span></span>

## <span data-ttu-id="c9c8b-138">Доступ к файлам в приложении</span><span class="sxs-lookup"><span data-stu-id="c9c8b-138">Access files within an app</span></span>

<span data-ttu-id="c9c8b-139">Если приложение сохраняет файлы на вашем устройстве, вы можете использовать это приложение для доступа к ним.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-139">If an application saves files on your device, you can use that application to access them.</span></span>

### <span data-ttu-id="c9c8b-140">Запрос файлов из другого приложения</span><span class="sxs-lookup"><span data-stu-id="c9c8b-140">Requesting files from another app</span></span>

<span data-ttu-id="c9c8b-141">Приложение может запросить сохранение файла или открытие файла из другого приложения с помощью [выборки файлов.](https://docs.microsoft.com/windows/mixed-reality/app-model#file-pickers)</span><span class="sxs-lookup"><span data-stu-id="c9c8b-141">An application can request to save a file or open a file from another app by using [file pickers](https://docs.microsoft.com/windows/mixed-reality/app-model#file-pickers).</span></span>

### <span data-ttu-id="c9c8b-142">Известные папки</span><span class="sxs-lookup"><span data-stu-id="c9c8b-142">Known folders</span></span>

<span data-ttu-id="c9c8b-143">HoloLens поддерживает ряд [](https://docs.microsoft.com/windows/mixed-reality/app-model#known-folders) известных папок, к которые приложения могут запрашивать разрешение на доступ.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-143">HoloLens supports a number of [known folders](https://docs.microsoft.com/windows/mixed-reality/app-model#known-folders) that apps can request permission to access.</span></span>

## <span data-ttu-id="c9c8b-144">Просмотр файлов HoloLens на компьютере</span><span class="sxs-lookup"><span data-stu-id="c9c8b-144">View HoloLens files on your PC</span></span>

<span data-ttu-id="c9c8b-145">Как и на других мобильных устройствах, подключите HoloLens к настольному компьютеру с помощью протокола MTP (media Transfer Protocol) и откройте проводник на компьютере, чтобы получить доступ к библиотекам HoloLens для удобной передачи данных.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-145">Similar to other mobile devices, connect HoloLens to your desktop PC using MTP (Media Transfer Protocol) and open File Explorer on the PC to access your HoloLens libraries for easy transfer.</span></span>

<span data-ttu-id="c9c8b-146">Чтобы увидеть файлы HoloLens в проводнике на компьютере:</span><span class="sxs-lookup"><span data-stu-id="c9c8b-146">To see your HoloLens files in File Explorer on your PC:</span></span>

1. <span data-ttu-id="c9c8b-147">Sign in to HoloLens, then plug it into the PC using the USB cable that came with the HoloLens.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-147">Sign in to HoloLens, then plug it into the PC using the USB cable that came with the HoloLens.</span></span>

1. <span data-ttu-id="c9c8b-148">Выберите **"Открыть устройство", чтобы просмотреть файлы**с помощью проводника, или откройте проводник на компьютере и перейдите на устройство.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-148">Select **Open Device to view files with File Explorer**, or open File Explorer on the PC and navigate to the device.</span></span>

<span data-ttu-id="c9c8b-149">Чтобы увидеть сведения о holoLens, щелкните правой кнопкой мыши имя устройства в проводнике на компьютере и выберите **"Свойства".**</span><span class="sxs-lookup"><span data-stu-id="c9c8b-149">To see info about your HoloLens, right-click the device name in File Explorer on your PC, then select **Properties**.</span></span>

> [!NOTE]
> <span data-ttu-id="c9c8b-150">HoloLens (1-е поколения) не поддерживает подключение к внешним жестким дискам или SD-картам.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-150">HoloLens (1st gen) does not support connecting to external hard drives or SD cards.</span></span>

## <span data-ttu-id="c9c8b-151">Синхронизация с облаком</span><span class="sxs-lookup"><span data-stu-id="c9c8b-151">Sync to the cloud</span></span>

<span data-ttu-id="c9c8b-152">Чтобы синхронизировать фотографии и другие файлы из HoloLens с облаком, установите и установите OneDrive на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-152">To sync photos and other files from your HoloLens to the cloud, install and set up OneDrive on HoloLens.</span></span> <span data-ttu-id="c9c8b-153">Чтобы получить OneDrive, найщите его в Microsoft Store на holoLens.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-153">To get OneDrive, search for it in the Microsoft Store on your HoloLens.</span></span>

<span data-ttu-id="c9c8b-154">HoloLens не сохраняет файлы и данные приложения, поэтому лучше сохранить важные данные в OneDrive.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-154">HoloLens doesn't back up app files and data, so it's a good idea to save your important stuff to OneDrive.</span></span> <span data-ttu-id="c9c8b-155">Таким образом, если вы сбросите устройство или развернете приложение, ваши данные будут сброшены.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-155">That way, if you reset your device or uninstall an app, your info will be backed up.</span></span>
