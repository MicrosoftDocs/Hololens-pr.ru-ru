---
title: Установка локализованных версий HoloLens
description: Узнайте, как установить локализованные версии HoloLens (1-го поколения), включая китайские и японские версии.
ms.prod: hololens
ms.mktglfcycl: manage
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.localizationpriority: medium
ms.date: 9/16/2019
ms.reviewer: ''
manager: jarrettr
appliesto:
- HoloLens (1st gen)
ms.openlocfilehash: 74eb003aafd23218b90988abe113d35f1fc3035a
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108310059"
---
# <a name="install-localized-versions-of-hololens-1st-gen"></a><span data-ttu-id="9e1a7-103">Установка локализованных версий HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="9e1a7-103">Install localized versions of HoloLens (1st gen)</span></span>

<span data-ttu-id="9e1a7-104">Чтобы перейти на версию HoloLens для китайского языка, необходимо использовать средство восстановления устройств Windows (ВДРТ), чтобы скачать сборку для языка на компьютере, а затем установить ее на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-104">In order to switch to the Chinese or Japanese version of HoloLens, you’ll need to use the Windows Device Recovery Tool (WDRT) to download the build for the language on a PC and then install it on your HoloLens.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e1a7-105">Использование ВДРТ для установки на китайском или японском сборках HoloLens удаляет существующие данные, такие как личные файлы и параметры, из HoloLens.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-105">Using WDRT to install the Chinese or Japanese builds of HoloLens deletes existing data, such as personal files and settings, from your HoloLens.</span></span> 

1. <span data-ttu-id="9e1a7-106">На компьютере Скачайте и установите [средство восстановления устройств Windows (вдрт)](https://support.microsoft.com/help/12379).</span><span class="sxs-lookup"><span data-stu-id="9e1a7-106">On your PC, download and install [the Windows Device Recovery Tool (WDRT)](https://support.microsoft.com/help/12379).</span></span>
1. <span data-ttu-id="9e1a7-107">Загрузите пакет для вашего компьютера:  [китайский (упрощенное письмо](https://aka.ms/hololensdownload-ch) или [японский](https://aka.ms/hololensdownload-jp)).</span><span class="sxs-lookup"><span data-stu-id="9e1a7-107">Download the package for the language you want to your PC:  [Simplified Chinese](https://aka.ms/hololensdownload-ch) or [Japanese](https://aka.ms/hololensdownload-jp).</span></span>
1. <span data-ttu-id="9e1a7-108">По завершении загрузки выберите **проводник**  >  **Загрузка** файлов.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-108">When the download finishes, select **File Explorer** > **Downloads**.</span></span> <span data-ttu-id="9e1a7-109">Щелкните правой кнопкой мыши скачанную ZIP-папку и выберите **извлечь все**  >  **извлечь** , чтобы распаковать ее.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-109">Right-click the zipped folder that you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
1. <span data-ttu-id="9e1a7-110">Подключите HoloLens к компьютеру, используя кабель Micro-USB, поставляемый с.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-110">Connect your HoloLens to your PC using the micro-USB cable that it shipped with.</span></span> <span data-ttu-id="9e1a7-111">(Даже если вы используете другие кабели для подключения HoloLens, это работает наилучшим образом.)</span><span class="sxs-lookup"><span data-stu-id="9e1a7-111">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
1. <span data-ttu-id="9e1a7-112">Когда средство автоматически обнаружит HoloLens, выберите плитку Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-112">After the tool automatically detects your HoloLens, select the Microsoft HoloLens tile.</span></span>
1. <span data-ttu-id="9e1a7-113">На следующем экране выберите **Ручное выделение пакетов**   и выберите файл установки, находящийся в папке, которая была распакована на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-113">On the next screen, select **Manual package selection** and select the installation file that resides in the folder that you unzipped in step 4.</span></span> <span data-ttu-id="9e1a7-114">(Найдите файл с расширением ФФУ.)</span><span class="sxs-lookup"><span data-stu-id="9e1a7-114">(Look for a file that has the extension “.ffu”.)</span></span> 
1. <span data-ttu-id="9e1a7-115">Выберите **установить программное обеспечение** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-115">Select **Install software** and follow the instructions.</span></span> 
1. <span data-ttu-id="9e1a7-116">После установки сборки автоматически запускается программа установки HoloLens.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-116">After the build installs, HoloLens setup automatically starts.</span></span> <span data-ttu-id="9e1a7-117">Установите на устройство и следуйте инструкциям по установке.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-117">Put on the device and follow the setup directions.</span></span> 

<span data-ttu-id="9e1a7-118">После завершения установки перейдите в раздел **Параметры**  >  **Обновление & безопасность**  >  **программа предварительной оценки Windows** и убедитесь, что вы настроили получение последней предварительной версии сборок.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-118">When you’re done with setup, go to **Settings** > **Update & Security** > **Windows Insider Program**, and check that you’re configured to receive the latest preview builds.</span></span> <span data-ttu-id="9e1a7-119">Как и в случае с предварительной версией для английского языка, программа предварительной оценки Windows сохраняет на китайском и японском версиях HoloLens последние версии предварительных сборок.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-119">Like the English preview builds, the Windows Insider Program keeps the Chinese and Japanese versions of HoloLens up-to-date with the latest preview builds.</span></span>

> [!NOTE]
>  
> - <span data-ttu-id="9e1a7-120">Нельзя использовать приложение параметров для изменения языка системы между английским, японским и китайским языком.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-120">You can’t use the Settings app to change the system language between English, Japanese, and Chinese.</span></span> <span data-ttu-id="9e1a7-121">Мигание новой сборки — единственный поддерживаемый способ изменения языка системы устройства.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-121">Flashing a new build is the only supported way to change the device system language.</span></span>
> - <span data-ttu-id="9e1a7-122">Хотя вы можете использовать клавиатуру пиньиня на экране для ввода текста на упрощенном китайском или японском языке, использование аппаратной клавиатуры Bluetooth для ввода текста на упрощенном китайском или японском языке в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-122">While you can use the on-screen Pinyin keyboard to enter Simplified Chinese or Japanese text, using a Bluetooth hardware keyboard to type Simplified Chinese or Japanese text is not supported at this time.</span></span>  <span data-ttu-id="9e1a7-123">Однако на китайском или японском HoloLens можно по-прежнему использовать клавиатуру Bluetooth для ввода текста на английском языке (чтобы переключить аппаратную клавиатуру на английский, нажмите клавишу ~).</span><span class="sxs-lookup"><span data-stu-id="9e1a7-123">However, on Chinese or Japanese HoloLens, you can continue to use a Bluetooth keyboard to type in English (to toggle a hardware keyboard to type in English, press the ~ key).</span></span>
