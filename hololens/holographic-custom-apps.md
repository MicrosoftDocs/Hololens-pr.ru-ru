---
title: Управление пользовательскими приложениями для HoloLens (1-е поколения)
description: Узнайте, как установить, удалить и загрузить неоконченные голографические приложения на устройства HoloLens с помощью портала устройств и Visual Studio.
ms.assetid: 6bd124c4-731c-4bcc-86c7-23f9b67ff616
ms.date: 12/10/2020
manager: v-miegge
keywords: hololens, загрузка нео боковая загрузка, неогрузка, магазин, uwp, приложение, установка
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
ms.openlocfilehash: 721c169c8ad34acab6914448af8ffc6ceec97a0e
ms.sourcegitcommit: 4c6d982bee72195bef955532738711f2b00ac8be
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "11296992"
---
# <span data-ttu-id="4f0e6-104">Управление пользовательскими приложениями для HoloLens (1-е поколения)</span><span class="sxs-lookup"><span data-stu-id="4f0e6-104">Manage custom apps for HoloLens (1st gen)</span></span>

<span data-ttu-id="4f0e6-105">Устройство HoloLens поддерживает множество существующих приложений в Microsoft Store, а также новые приложения, разработанные специально для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-105">HoloLens supports many existing applications from the Microsoft Store, as well as new apps built specifically for HoloLens.</span></span> <span data-ttu-id="4f0e6-106">В этой статье основное внимание уделяется пользовательским голографическим приложениям.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-106">This article focuses on custom holographic applications.</span></span>  

<span data-ttu-id="4f0e6-107">Дополнительные сведения о приложениях Магазина см. в под [управлением приложений с магазином.](holographic-store-apps.md)</span><span class="sxs-lookup"><span data-stu-id="4f0e6-107">For more information about store apps, see [Manage apps with the store](holographic-store-apps.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f0e6-108">Для HoloLens (1-е поколения), также называемого в то время выпуском HoloLens Developer Edition, были созданы следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-108">The following information was created for the HoloLens (1st gen), also called the HoloLens Developer Edition at the time.</span></span> <span data-ttu-id="4f0e6-109">Например, загрузка неоконтружаемых приложений через портал устройств и установка приложений Visual Studio тогда была распространена.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-109">As such sideloading apps via device portal and installing apps via Visual Studio were commonplace then.</span></span> <span data-ttu-id="4f0e6-110">В корпоративных развертываниях не рекомендуется использовать режим разработчика, который используется в обоих этих методах.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-110">For enterprise deployments we do not recommend enabling Developer Mode, which both of these methods use.</span></span> <span data-ttu-id="4f0e6-111">Если вы заинтересованы в безопасном способе развертывания приложений, просмотрите наше руководство [по управлению приложениями: обзор.](app-deploy-overview.md)</span><span class="sxs-lookup"><span data-stu-id="4f0e6-111">If you are interested in a secure app deployment method please review our [App Management: Overview](app-deploy-overview.md).</span></span>
>
> <span data-ttu-id="4f0e6-112">Если вы ищете способ разработчика установки приложений для устройств HoloLens 2, обратитесь к:</span><span class="sxs-lookup"><span data-stu-id="4f0e6-112">If you are looking for either developer method of app installation for HoloLens 2 devices please refer to:</span></span>
> - [<span data-ttu-id="4f0e6-113">Портал устройств: установка приложения</span><span class="sxs-lookup"><span data-stu-id="4f0e6-113">Device Portal: Installing an App</span></span>](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal#installing-an-app)
> - [<span data-ttu-id="4f0e6-114">Использование Visual Studio для развертывания и отлаки приложений</span><span class="sxs-lookup"><span data-stu-id="4f0e6-114">Using Visual Studio to deploy and debug Apps</span></span>](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-visual-studio)

## <span data-ttu-id="4f0e6-115">Установка пользовательских приложений</span><span class="sxs-lookup"><span data-stu-id="4f0e6-115">Install custom apps</span></span>

<span data-ttu-id="4f0e6-116">Вы можете установить собственные приложения на Устройство HoloLens с помощью портала устройств или путем развертывания приложений из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-116">You can install your own applications on HoloLens either by using the Device Portal or by deploying the apps from Visual Studio.</span></span>

### <span data-ttu-id="4f0e6-117">Установка пакета приложения с помощью портала устройств</span><span class="sxs-lookup"><span data-stu-id="4f0e6-117">Installing an application package with the Device Portal</span></span>

1. <span data-ttu-id="4f0e6-118">Установить подключение портала [устройств к](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal) целевому устройству HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-118">Establish a connection from [Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal) to the target HoloLens.</span></span>

1. <span data-ttu-id="4f0e6-119">В области навигации слева перейдите на страницу **"Приложения".**</span><span class="sxs-lookup"><span data-stu-id="4f0e6-119">In the left navigation, navigate to the **Apps** page.</span></span>

1. <span data-ttu-id="4f0e6-120">В **папке "Пакет** приложения" перейдите к APPX-файлу, связанному с вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-120">Under **App Package** browse to the .appx file that is associated with your application.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="4f0e6-121">Обязательно ссылайтесь на все связанные файлы зависимостей и сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-121">Make sure to reference any associated dependency and certificate files.</span></span>

1. <span data-ttu-id="4f0e6-122">Select **Go**.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-122">Select **Go**.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Установка формы приложения на портале устройств Windows на Microsoft HoloLens](images/deviceportal-appmanager.jpg)

### <span data-ttu-id="4f0e6-124">Развертывание из Microsoft Visual Studio 2015</span><span class="sxs-lookup"><span data-stu-id="4f0e6-124">Deploying from Microsoft Visual Studio 2015</span></span>

1. <span data-ttu-id="4f0e6-125">Откройте решение Visual Studio приложения (SLN-файл).</span><span class="sxs-lookup"><span data-stu-id="4f0e6-125">Open your app's Visual Studio solution (.sln file).</span></span>

1. <span data-ttu-id="4f0e6-126">Откройте свойства **проекта.**</span><span class="sxs-lookup"><span data-stu-id="4f0e6-126">Open the project's **Properties**.</span></span>

1. <span data-ttu-id="4f0e6-127">Выберите следующую конфигурацию сборки: **Master/x86/Remote Machine.**</span><span class="sxs-lookup"><span data-stu-id="4f0e6-127">Select the following build configuration: **Master/x86/Remote Machine**.</span></span>

1. <span data-ttu-id="4f0e6-128">При выборе **удаленного компьютера:**</span><span class="sxs-lookup"><span data-stu-id="4f0e6-128">When you select **Remote Machine**:</span></span>
   - <span data-ttu-id="4f0e6-129">Убедитесь, что адрес указывает Wi-Fi IP-адрес holoLens.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-129">Make sure the address points to the Wi-Fi IP address of your HoloLens.</span></span>
   - <span data-ttu-id="4f0e6-130">Установите для проверки **подлинности универсальный (незашифрованный протокол).**</span><span class="sxs-lookup"><span data-stu-id="4f0e6-130">Set authentication to **Universal (Unencrypted Protocol)**.</span></span>
   
1. <span data-ttu-id="4f0e6-131">Создайте решение.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-131">Build your solution.</span></span>

1. <span data-ttu-id="4f0e6-132">Чтобы развернуть приложение с компьютера разработки на устройство HoloLens, выберите **удаленный компьютер.**</span><span class="sxs-lookup"><span data-stu-id="4f0e6-132">To deploy the app from your development PC to your HoloLens, select **Remote Machine**.</span></span> <span data-ttu-id="4f0e6-133">Если у вас уже есть сборка на HoloLens, выберите **"Да",** чтобы установить эту более новую версию.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-133">If you already have an existing build on the HoloLens, select **Yes** to install this newer version.</span></span>  

   ![Развертывание приложений на удаленном компьютере для Microsoft HoloLens в Visual Studio](images/vs2015-remotedeployment.jpg)  
   
1. <span data-ttu-id="4f0e6-135">Приложение установит и автоматически запустится на вашем HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4f0e6-135">The application will install and auto launch on your HoloLens.</span></span>

<span data-ttu-id="4f0e6-136">После установки приложения его можно найти в списке "Все **приложения"** (**"Запустить**  >  **все приложения").**</span><span class="sxs-lookup"><span data-stu-id="4f0e6-136">After you've installed an app, you'll find it in the **All apps** list (**Start** > **All apps**).</span></span>
