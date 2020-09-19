---
title: Как загрузить и установить приложения с помощью установщика приложений HoloLens 2
description: Загрузка и установка приложений через пользовательский интерфейс
keywords: Управление приложениями, приложение, hololens, установщик приложений
author: evmill
ms.author: v-evmill
ms.reviewer: qizho
ms.date: 9/17/2020
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 2387c0eb65efc312db4eea7118f3cca44ce6d4b6
ms.sourcegitcommit: 4ad9b6c73913808175b1a448d2be9e33592f65af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "11027486"
---
# <span data-ttu-id="7f366-104">Установка приложений на HoloLens 2 с помощью установщика приложений</span><span class="sxs-lookup"><span data-stu-id="7f366-104">Install Apps on HoloLens 2 via App Installer</span></span>

<span data-ttu-id="7f366-105">Теперь пользователи могут устанавливать приложения через пакеты appx, не требуя включать режим разработчика или использовать портал устройств.</span><span class="sxs-lookup"><span data-stu-id="7f366-105">Users can now install Apps via Appx Bundles now without the need to enable Developer Mode or use Device Portal.</span></span> <span data-ttu-id="7f366-106">Это очень просто для установки приложений на локальных устройствах или предоставления общего доступ к приложению другим пользователям, которые не знакомы с другими методами установки приложений на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="7f366-106">This experience is simple for installing Apps on local devices or sharing an app with someone else who is unfamiliar with other app install methods on HoloLens.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="7f366-107">Эта функция в настоящее время avalible только в сборках участников программы предварительной оценки Windows (19041.1377 +).</span><span class="sxs-lookup"><span data-stu-id="7f366-107">This feature is currently only avalible in Windows Insider builds 19041.1377+.</span></span> <span data-ttu-id="7f366-108">[Узнайте больше о том, как зарегистрироваться в сборках для участников программы предварительной оценки Windows](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="7f366-108">[Learn more on how to enroll in Windows Insider builds](hololens-insider.md).</span></span>

> [!NOTE]
> <span data-ttu-id="7f366-109">Конфигурация решения для вашего приложения должна быть **основной** или **выпуском** , так как установщик приложения будет использовать зависимости из магазина.</span><span class="sxs-lookup"><span data-stu-id="7f366-109">Your app’s Solution Configuration must be either **Master** or **Release** as the App Installer will use dependencies from the store.</span></span> <span data-ttu-id="7f366-110">Ознакомьтесь с дополнительными сведениями о [создании пакетов приложений](https://docs.microsoft.com/windows/msix/app-installer/create-appinstallerfile-vs).</span><span class="sxs-lookup"><span data-stu-id="7f366-110">See more about [creating app packages](https://docs.microsoft.com/windows/msix/app-installer/create-appinstallerfile-vs).</span></span>

1.  <span data-ttu-id="7f366-111">Убедитесь, что устройство HoloLens 2 включено и вы вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="7f366-111">Ensure that your HoloLens 2 device is powered on and you are signed in.</span></span>
1.  <span data-ttu-id="7f366-112">На своем ПК перейдите в свое собственное приложение и скопируйте yourapp. appxbundle в yourdevicename\Internal Storage\Downloads.</span><span class="sxs-lookup"><span data-stu-id="7f366-112">On your PC navigate to your custom app, and copy yourapp.appxbundle to yourdevicename\Internal Storage\Downloads.</span></span> 
    <span data-ttu-id="7f366-113">После того как вы закончите копирование файла, вы можете отключить устройство и завершить установку позже.</span><span class="sxs-lookup"><span data-stu-id="7f366-113">After your finish copying your file you may disconnect your device and finish the install later.</span></span>
1.  <span data-ttu-id="7f366-114">На устройстве HoloLens 2 Откройте **меню Пуск**, выберите **все приложения** и запустите приложение **проводник** .</span><span class="sxs-lookup"><span data-stu-id="7f366-114">From your HoloLens 2 device Open the **Start Menu**, select **All apps** and launch the **File Explorer** app.</span></span>
1.  <span data-ttu-id="7f366-115">Перейдите в папку Downloads (загрузки).</span><span class="sxs-lookup"><span data-stu-id="7f366-115">Navigate to the Downloads folder.</span></span> <span data-ttu-id="7f366-116">Вам может потребоваться сначала выбрать **это устройство** на левой панели приложения, а затем перейти к разделу Downloads (загрузки).</span><span class="sxs-lookup"><span data-stu-id="7f366-116">You may need to on the left panel of the app select **This device** first, then navigate to Downloads.</span></span>
1.  <span data-ttu-id="7f366-117">Выберите файл yourapp. appxbundle.</span><span class="sxs-lookup"><span data-stu-id="7f366-117">Select the yourapp.appxbundle file.</span></span> 
1.  <span data-ttu-id="7f366-118">Запустится установщик приложения.</span><span class="sxs-lookup"><span data-stu-id="7f366-118">The App Installer will launch.</span></span> <span data-ttu-id="7f366-119">Нажмите кнопку " **установить** ", чтобы установить приложение.</span><span class="sxs-lookup"><span data-stu-id="7f366-119">Select the **Install** button to install your app.</span></span> 

<span data-ttu-id="7f366-120">Установленное приложение будет автоматически запускаться после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="7f366-120">The installed app will automatically launch upon the completion of installing.</span></span> 

![Установка примеров MRTK с помощью установщика приложений](images/hololens-app-installer-picture.jpg)

<span data-ttu-id="7f366-122">Если не удалось установить приложение, проверьте следующее:</span><span class="sxs-lookup"><span data-stu-id="7f366-122">If your app failed to install check the following:</span></span>
-   <span data-ttu-id="7f366-123">Ваше приложение является либо главным, либо построением выпуска.</span><span class="sxs-lookup"><span data-stu-id="7f366-123">Your app is either a Master or Release build.</span></span>
-   <span data-ttu-id="7f366-124">Вы [подключены к Интернету](hololens-network.md).</span><span class="sxs-lookup"><span data-stu-id="7f366-124">You are [connected to the internet](hololens-network.md).</span></span>
-   <span data-ttu-id="7f366-125">Ваши [конечные точки для Microsoft Store](hololens-offline.md) настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="7f366-125">Your [endpoints for the Microsoft Store](hololens-offline.md) are correctly configured.</span></span>  
