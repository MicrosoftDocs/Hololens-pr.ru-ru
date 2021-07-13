---
title: управление пользовательскими приложениями для HoloLens (1-й общий)
description: узнайте, как устанавливать, удалять и загружать неопубликованные пользовательские приложения holographic на HoloLens устройствах с помощью портала устройств и Visual Studio.
ms.assetid: 6bd124c4-731c-4bcc-86c7-23f9b67ff616
ms.date: 12/10/2020
manager: v-miegge
keywords: hololens, загружать неопубликованные, Загрузка на стороне сервера, Загрузка, сохранение, UWP, приложение, установка
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
ms.openlocfilehash: a179032978e1fc062273a6754e3b0a1ad50a5211
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113635914"
---
# <a name="manage-custom-apps-for-hololens-1st-gen"></a><span data-ttu-id="6ad8c-104">управление пользовательскими приложениями для HoloLens (1-й общий)</span><span class="sxs-lookup"><span data-stu-id="6ad8c-104">Manage custom apps for HoloLens (1st gen)</span></span>

<span data-ttu-id="6ad8c-105">HoloLens поддерживает множество существующих приложений из Microsoft Store, а также новые приложения, разработанные специально для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-105">HoloLens supports many existing applications from the Microsoft Store, as well as new apps built specifically for HoloLens.</span></span> <span data-ttu-id="6ad8c-106">В этой статье рассматриваются пользовательские приложения Holographic.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-106">This article focuses on custom holographic applications.</span></span>  

<span data-ttu-id="6ad8c-107">Дополнительные сведения о приложениях Магазина см. [в статье Управление приложениями с помощью магазина](holographic-store-apps.md).</span><span class="sxs-lookup"><span data-stu-id="6ad8c-107">For more information about store apps, see [Manage apps with the store](holographic-store-apps.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ad8c-108">следующие сведения были созданы для HoloLens (1-го поколения), также называемого HoloLens Developer Edition.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-108">The following information was created for the HoloLens (1st gen), also called the HoloLens Developer Edition at the time.</span></span> <span data-ttu-id="6ad8c-109">такие приложения для загрузки неопубликованных приложений с помощью портала устройств и установки приложений с помощью Visual Studio были распространены.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-109">As such sideloading apps via device portal and installing apps via Visual Studio were commonplace then.</span></span> <span data-ttu-id="6ad8c-110">Для корпоративных развертываний не рекомендуется включать режим разработчика, который используется обоими методами.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-110">For enterprise deployments we do not recommend enabling Developer Mode, which both of these methods use.</span></span> <span data-ttu-id="6ad8c-111">Если вы заинтересованы в безопасном методе развертывания приложений, ознакомьтесь с нашим [руководством по управлению приложениями: обзор](app-deploy-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6ad8c-111">If you are interested in a secure app deployment method please review our [App Management: Overview](app-deploy-overview.md).</span></span>
>
> <span data-ttu-id="6ad8c-112">если вы ищете метод установки приложения для HoloLens 2 устройств, обратитесь по следующим ссылке:</span><span class="sxs-lookup"><span data-stu-id="6ad8c-112">If you are looking for either developer method of app installation for HoloLens 2 devices please refer to:</span></span>
>
> - [<span data-ttu-id="6ad8c-113">Портал устройств: Установка приложения</span><span class="sxs-lookup"><span data-stu-id="6ad8c-113">Device Portal: Installing an App</span></span>](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal#installing-an-app)
> - [<span data-ttu-id="6ad8c-114">использование Visual Studio для развертывания и отладки приложений</span><span class="sxs-lookup"><span data-stu-id="6ad8c-114">Using Visual Studio to deploy and debug Apps</span></span>](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-visual-studio)

## <a name="install-custom-apps"></a><span data-ttu-id="6ad8c-115">Установка пользовательских приложений</span><span class="sxs-lookup"><span data-stu-id="6ad8c-115">Install custom apps</span></span>

<span data-ttu-id="6ad8c-116">вы можете установить собственные приложения на HoloLens либо с помощью портала устройств, либо путем развертывания приложений из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-116">You can install your own applications on HoloLens either by using the Device Portal or by deploying the apps from Visual Studio.</span></span>

### <a name="installing-an-application-package-with-the-device-portal"></a><span data-ttu-id="6ad8c-117">Установка пакета приложения с помощью портала устройств</span><span class="sxs-lookup"><span data-stu-id="6ad8c-117">Installing an application package with the Device Portal</span></span>

1. <span data-ttu-id="6ad8c-118">Установите подключение с [портала устройств](/windows/mixed-reality/using-the-windows-device-portal) к целевой HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-118">Establish a connection from [Device Portal](/windows/mixed-reality/using-the-windows-device-portal) to the target HoloLens.</span></span>

1. <span data-ttu-id="6ad8c-119">В левой области навигации перейдите на страницу **приложения** .</span><span class="sxs-lookup"><span data-stu-id="6ad8c-119">In the left navigation, navigate to the **Apps** page.</span></span>

1. <span data-ttu-id="6ad8c-120">В разделе **пакет приложения** найдите appx-файл, связанный с вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-120">Under **App Package** browse to the .appx file that is associated with your application.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="6ad8c-121">Обязательно сослаться на все связанные файлы зависимостей и сертификатов.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-121">Make sure to reference any associated dependency and certificate files.</span></span>

1. <span data-ttu-id="6ad8c-122">Выберите **Перейти**.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-122">Select **Go**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="6ad8c-123">![установите форму приложения на портале устройств Windows на Microsoft HoloLens](images/deviceportal-appmanager.jpg)</span><span class="sxs-lookup"><span data-stu-id="6ad8c-123">![Install app form in Windows Device Portal on Microsoft HoloLens](images/deviceportal-appmanager.jpg)</span></span>

### <a name="deploying-from-microsoft-visual-studio-2015"></a><span data-ttu-id="6ad8c-124">развертывание из Microsoft Visual Studio 2015</span><span class="sxs-lookup"><span data-stu-id="6ad8c-124">Deploying from Microsoft Visual Studio 2015</span></span>

1. <span data-ttu-id="6ad8c-125">откройте решение Visual Studio приложения (sln-файл).</span><span class="sxs-lookup"><span data-stu-id="6ad8c-125">Open your app's Visual Studio solution (.sln file).</span></span>

1. <span data-ttu-id="6ad8c-126">Откройте **Свойства** проекта.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-126">Open the project's **Properties**.</span></span>

1. <span data-ttu-id="6ad8c-127">Выберите следующую конфигурацию сборки: **master/x86/удаленный компьютер**.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-127">Select the following build configuration: **Master/x86/Remote Machine**.</span></span>

1. <span data-ttu-id="6ad8c-128">При выборе **удаленного компьютера**:</span><span class="sxs-lookup"><span data-stu-id="6ad8c-128">When you select **Remote Machine**:</span></span>
   - <span data-ttu-id="6ad8c-129">Убедитесь, что адрес указывает на Wi-Fi IP-адрес HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-129">Make sure the address points to the Wi-Fi IP address of your HoloLens.</span></span>
   - <span data-ttu-id="6ad8c-130">Задайте для параметра Проверка подлинности значение **универсальный (незашифрованный протокол)**.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-130">Set authentication to **Universal (Unencrypted Protocol)**.</span></span>
   
1. <span data-ttu-id="6ad8c-131">Выполните построение решения.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-131">Build your solution.</span></span>

1. <span data-ttu-id="6ad8c-132">чтобы развернуть приложение с компьютера разработки на HoloLens, выберите **удаленный компьютер**.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-132">To deploy the app from your development PC to your HoloLens, select **Remote Machine**.</span></span> <span data-ttu-id="6ad8c-133">если у вас уже есть сборка на HoloLens, выберите **да** , чтобы установить эту новую версию.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-133">If you already have an existing build on the HoloLens, select **Yes** to install this newer version.</span></span>  

   ![развертывание удаленного компьютера для приложений для Microsoft HoloLens в Visual Studio](images/vs2015-remotedeployment.jpg)  
   
1. <span data-ttu-id="6ad8c-135">Приложение будет установлено и запущено на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6ad8c-135">The application will install and auto launch on your HoloLens.</span></span>

<span data-ttu-id="6ad8c-136">После установки приложения его можно найти в списке **все приложения** (**запустить**  >  **все приложения**).</span><span class="sxs-lookup"><span data-stu-id="6ad8c-136">After you've installed an app, you'll find it in the **All apps** list (**Start** > **All apps**).</span></span>
