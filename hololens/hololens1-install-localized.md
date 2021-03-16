---
title: Установка локализованных версий HoloLens
description: Узнайте, как установить локализованные версии HoloLens (1-го поколения), включая версии для китайского и японского языков.
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
ms.sourcegitcommit: 01c0b0a789e156a9d29aaf6f61e36dfd09b8c01a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439015"
---
# <a name="install-localized-versions-of-hololens-1st-gen"></a><span data-ttu-id="e72ea-103">Установка локализованных версий HoloLens (1-е поколение)</span><span class="sxs-lookup"><span data-stu-id="e72ea-103">Install localized versions of HoloLens (1st gen)</span></span>

<span data-ttu-id="e72ea-104">Чтобы переключиться на версию HoloLens для китайского или японского языка, необходимо использовать средство Windows Device Recovery Tool (WDRT) для загрузки сборку для нужного языка на компьютере, а затем установить ее на ваше устройство HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e72ea-104">In order to switch to the Chinese or Japanese version of HoloLens, you’ll need to use the Windows Device Recovery Tool (WDRT) to download the build for the language on a PC and then install it on your HoloLens.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e72ea-105">При использовании WDRT для установки китайской или японской сборки для HoloLens удаляются существующие данные, такие как личные файлы и параметры.</span><span class="sxs-lookup"><span data-stu-id="e72ea-105">Using WDRT to install the Chinese or Japanese builds of HoloLens deletes existing data, such as personal files and settings, from your HoloLens.</span></span> 

1. <span data-ttu-id="e72ea-106">Скачайте и установите средство [Windows Device Recovery Tool (WDRT)](https://support.microsoft.com/help/12379) на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e72ea-106">On your PC, download and install [the Windows Device Recovery Tool (WDRT)](https://support.microsoft.com/help/12379).</span></span>
1. <span data-ttu-id="e72ea-107">Скачайте на компьютер пакет для языка, который вы хотите использовать: [китайский (упрощенное письмо)](https://aka.ms/hololensdownload-ch) или [японский](https://aka.ms/hololensdownload-jp).</span><span class="sxs-lookup"><span data-stu-id="e72ea-107">Download the package for the language you want to your PC:  [Simplified Chinese](https://aka.ms/hololensdownload-ch) or [Japanese](https://aka.ms/hololensdownload-jp).</span></span>
1. <span data-ttu-id="e72ea-108">После завершения загрузки выберите **Проводник** > **Загрузки**.</span><span class="sxs-lookup"><span data-stu-id="e72ea-108">When the download finishes, select **File Explorer** > **Downloads**.</span></span> <span data-ttu-id="e72ea-109">Щелкните правой кнопкой мыши только что скачанную запакованную папку и выберите **Извлечь все** > **Извлечь**, чтобы распаковать ее.</span><span class="sxs-lookup"><span data-stu-id="e72ea-109">Right-click the zipped folder that you just downloaded, and select **Extract all** > **Extract** to unzip it.</span></span>
1. <span data-ttu-id="e72ea-110">Подключите HoloLens к компьютеру с помощью кабеля micro-USB, входящего в комплект поставки.</span><span class="sxs-lookup"><span data-stu-id="e72ea-110">Connect your HoloLens to your PC using the micro-USB cable that it shipped with.</span></span> <span data-ttu-id="e72ea-111">(Даже если вы использовали для подключения HoloLens другие кабели, этот работает лучше.)</span><span class="sxs-lookup"><span data-stu-id="e72ea-111">(Even if you've been using other cables to connect your HoloLens, this one works best.)</span></span>
1. <span data-ttu-id="e72ea-112">После того как средство автоматически обнаружит HoloLens, выберите плитку Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e72ea-112">After the tool automatically detects your HoloLens, select the Microsoft HoloLens tile.</span></span>
1. <span data-ttu-id="e72ea-113">На следующем экране выберите **Выбрать пакет вручную** , а затем файл установки, расположенный в папке, которую вы распаковали на 4-м шаге.</span><span class="sxs-lookup"><span data-stu-id="e72ea-113">On the next screen, select **Manual package selection** and select the installation file that resides in the folder that you unzipped in step 4.</span></span> <span data-ttu-id="e72ea-114">(Вам необходимо файл с расширением FFU.)</span><span class="sxs-lookup"><span data-stu-id="e72ea-114">(Look for a file that has the extension “.ffu”.)</span></span> 
1. <span data-ttu-id="e72ea-115">Выберите  **Установить программное обеспечение** и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="e72ea-115">Select **Install software** and follow the instructions.</span></span> 
1. <span data-ttu-id="e72ea-116">После установки сборки HoloLens автоматически запустится.</span><span class="sxs-lookup"><span data-stu-id="e72ea-116">After the build installs, HoloLens setup automatically starts.</span></span> <span data-ttu-id="e72ea-117">Наденьте устройство и следуйте указаниям по установке.</span><span class="sxs-lookup"><span data-stu-id="e72ea-117">Put on the device and follow the setup directions.</span></span> 

<span data-ttu-id="e72ea-118">После завершения установки перейдите в раздел **Параметры** > **Обновление и безопасность** > **Программа предварительной оценки Windows** и убедитесь, что выполнена настройка для получения последних предварительных сборок.</span><span class="sxs-lookup"><span data-stu-id="e72ea-118">When you’re done with setup, go to **Settings** > **Update & Security** > **Windows Insider Program**, and check that you’re configured to receive the latest preview builds.</span></span> <span data-ttu-id="e72ea-119">Как и в случае с английской предварительной сборкой, Программа предварительной оценки Windows поддерживает китайские и японские версии HoloLens в актуальном состоянии с помощью последних предварительных сборок.</span><span class="sxs-lookup"><span data-stu-id="e72ea-119">Like the English preview builds, the Windows Insider Program keeps the Chinese and Japanese versions of HoloLens up-to-date with the latest preview builds.</span></span>

> [!NOTE]
>  
> - <span data-ttu-id="e72ea-120">Приложение "Параметры" нельзя использовать для изменения языка системы с английского на японский или китайский языки или обратно.</span><span class="sxs-lookup"><span data-stu-id="e72ea-120">You can’t use the Settings app to change the system language between English, Japanese, and Chinese.</span></span> <span data-ttu-id="e72ea-121">Установка новой сборки — это единственный поддерживаемый способ изменить язык системы устройства.</span><span class="sxs-lookup"><span data-stu-id="e72ea-121">Flashing a new build is the only supported way to change the device system language.</span></span>
> - <span data-ttu-id="e72ea-122">Вы можете использовать экранную клавиатуру "Пиньинь" для ввода текста на китайском (упрощенное письмо) или японском языке, однако использование аппаратной клавиатуры Bluetooth для ввода текста на китайском (упрощенное письмо) или японском языках в данный момент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e72ea-122">While you can use the on-screen Pinyin keyboard to enter Simplified Chinese or Japanese text, using a Bluetooth hardware keyboard to type Simplified Chinese or Japanese text is not supported at this time.</span></span>  <span data-ttu-id="e72ea-123">При этом в китайской или японской сборке HoloLens вы можете продолжить использовать клавиатуру Bluetooth для ввода текста на английском языке (чтобы переключить аппаратную клавиатуру на английский, нажмите клавишу ~).</span><span class="sxs-lookup"><span data-stu-id="e72ea-123">However, on Chinese or Japanese HoloLens, you can continue to use a Bluetooth keyboard to type in English (to toggle a hardware keyboard to type in English, press the ~ key).</span></span>
