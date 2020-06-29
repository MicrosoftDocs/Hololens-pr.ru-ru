---
title: Управление пользовательскими приложениями для HoloLens
description: Пользовательские приложения для загрузки на HoloLens. Узнайте больше об установке и удалении holographic приложений.
ms.assetid: 6bd124c4-731c-4bcc-86c7-23f9b67ff616
ms.date: 07/01/2019
manager: v-miegge
keywords: hololens, неопубликованного, Загрузка сбоку, боковая загрузка, магазин, UWP, приложение, установка
ms.prod: hololens
ms.sitesec: library
author: mattzmsft
ms.author: mazeller
ms.topic: article
ms.localizationpriority: medium
ms.custom:
- CI 111456
- CSSTroubleshooting
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 12c5eedfab580be8acea48c1fc19b56c1ead08ac
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10828864"
---
# <span data-ttu-id="e7094-105">Управление пользовательскими приложениями для HoloLens</span><span class="sxs-lookup"><span data-stu-id="e7094-105">Manage custom apps for HoloLens</span></span>

<span data-ttu-id="e7094-106">HoloLens поддерживает множество существующих приложений из Microsoft Store, а также новые приложения, разработанные специально для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e7094-106">HoloLens supports many existing applications from the Microsoft Store, as well as new apps built specifically for HoloLens.</span></span> <span data-ttu-id="e7094-107">В этой статье рассматриваются пользовательские приложения Holographic.</span><span class="sxs-lookup"><span data-stu-id="e7094-107">This article focuses on custom holographic applications.</span></span>  

<span data-ttu-id="e7094-108">Дополнительные сведения о приложениях Store можно найти [в разделе Управление приложениями с помощью магазина](holographic-store-apps.md).</span><span class="sxs-lookup"><span data-stu-id="e7094-108">For more information about store apps, see [Manage apps with the store](holographic-store-apps.md).</span></span>

## <span data-ttu-id="e7094-109">Установка настраиваемых приложений</span><span class="sxs-lookup"><span data-stu-id="e7094-109">Install custom apps</span></span>

<span data-ttu-id="e7094-110">Вы можете установить собственные приложения на HoloLens либо с помощью портала устройств, либо путем развертывания приложений из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e7094-110">You can install your own applications on HoloLens either by using the Device Portal or by deploying the apps from Visual Studio.</span></span>

### <span data-ttu-id="e7094-111">Установка пакета приложения с помощью портала устройств</span><span class="sxs-lookup"><span data-stu-id="e7094-111">Installing an application package with the Device Portal</span></span>

1. <span data-ttu-id="e7094-112">Установите соединение с [портала устройств](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal) на целевую HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e7094-112">Establish a connection from [Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal) to the target HoloLens.</span></span>
1. <span data-ttu-id="e7094-113">На панели навигации слева перейдите на страницу **приложения** .</span><span class="sxs-lookup"><span data-stu-id="e7094-113">In the left navigation, navigate to the **Apps** page .</span></span>
1. <span data-ttu-id="e7094-114">В разделе **пакет приложения** найдите appx-файл, связанный с вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="e7094-114">Under **App Package** browse to the .appx file that is associated with your application.</span></span>
   > [!IMPORTANT]
   > <span data-ttu-id="e7094-115">Убедитесь, что вы ссылались на все связанные файлы зависимостей и сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e7094-115">Make sure to reference any associated dependency and certificate files.</span></span>

1. <span data-ttu-id="e7094-116">Нажмите кнопку **Go (перейти**).</span><span class="sxs-lookup"><span data-stu-id="e7094-116">Select **Go**.</span></span>
   ![Установка формы приложения на портале устройств Windows в Microsoft HoloLens](images/deviceportal-appmanager.jpg)

### <span data-ttu-id="e7094-118">Развертывание из Microsoft Visual Studio 2015</span><span class="sxs-lookup"><span data-stu-id="e7094-118">Deploying from Microsoft Visual Studio 2015</span></span>

1. <span data-ttu-id="e7094-119">Откройте решение Visual Studio для приложения (SLN-файл).</span><span class="sxs-lookup"><span data-stu-id="e7094-119">Open your app's Visual Studio solution (.sln file).</span></span>
1. <span data-ttu-id="e7094-120">Откройте **Свойства**проекта.</span><span class="sxs-lookup"><span data-stu-id="e7094-120">Open the project's **Properties**.</span></span>
1. <span data-ttu-id="e7094-121">Выберите следующую конфигурацию сборки: **master/x86/на удаленном компьютере**.</span><span class="sxs-lookup"><span data-stu-id="e7094-121">Select the following build configuration: **Master/x86/Remote Machine**.</span></span>
1. <span data-ttu-id="e7094-122">При выборе **удаленного компьютера**:</span><span class="sxs-lookup"><span data-stu-id="e7094-122">When you select **Remote Machine**:</span></span>
   - <span data-ttu-id="e7094-123">Убедитесь, что адрес указывает на IP-адрес Wi-Fi вашего HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e7094-123">Make sure the address points to the Wi-Fi IP address of your HoloLens.</span></span>
   - <span data-ttu-id="e7094-124">Задайте для проверки подлинности **универсальный (незашифрованный протокол)**.</span><span class="sxs-lookup"><span data-stu-id="e7094-124">Set authentication to **Universal (Unencrypted Protocol)**.</span></span>
1. <span data-ttu-id="e7094-125">Создайте решение.</span><span class="sxs-lookup"><span data-stu-id="e7094-125">Build your solution.</span></span>
1. <span data-ttu-id="e7094-126">Чтобы развернуть приложение с компьютера разработчика на HoloLens, выберите **Удаленный компьютер**.</span><span class="sxs-lookup"><span data-stu-id="e7094-126">To deploy the app from your development PC to your HoloLens, select **Remote Machine**.</span></span> <span data-ttu-id="e7094-127">Если у вас уже есть сборка на HoloLens, нажмите кнопку **Да** , чтобы установить эту новую версию.</span><span class="sxs-lookup"><span data-stu-id="e7094-127">If you already have an existing build on the HoloLens, select **Yes** to install this newer version.</span></span>  

   ![Развертывание удаленного компьютера для приложений в Microsoft HoloLens в Visual Studio](images/vs2015-remotedeployment.jpg)  
1. <span data-ttu-id="e7094-129">Приложение будет установлено и автоматически запускаться на устройстве HoloLens.</span><span class="sxs-lookup"><span data-stu-id="e7094-129">The application will install and auto launch on your HoloLens.</span></span>

<span data-ttu-id="e7094-130">После установки приложения вы увидите его в списке **все приложения** (**запускать**  >  **все приложения**).</span><span class="sxs-lookup"><span data-stu-id="e7094-130">After you've installed an app, you'll find it in the **All apps** list (**Start** > **All apps**).</span></span>
