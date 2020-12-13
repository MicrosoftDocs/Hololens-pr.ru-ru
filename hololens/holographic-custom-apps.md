---
title: Управление пользовательскими приложениями для HoloLens
description: Загрузка нео боком пользовательских приложений на HoloLens. Узнайте больше об установке и установке голографических приложений.
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
ms.openlocfilehash: 67a857eb35126435f5642ee60168128300401394
ms.sourcegitcommit: cd2071c12eaabe46c829b53c22d13e21b8af5b53
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "11218636"
---
# <span data-ttu-id="7f183-105">Управление пользовательскими приложениями для HoloLens</span><span class="sxs-lookup"><span data-stu-id="7f183-105">Manage custom apps for HoloLens</span></span>

<span data-ttu-id="7f183-106">Устройство HoloLens поддерживает множество существующих приложений в Microsoft Store, а также новые приложения, разработанные специально для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="7f183-106">HoloLens supports many existing applications from the Microsoft Store, as well as new apps built specifically for HoloLens.</span></span> <span data-ttu-id="7f183-107">В этой статье основное внимание уделяется пользовательским голографическим приложениям.</span><span class="sxs-lookup"><span data-stu-id="7f183-107">This article focuses on custom holographic applications.</span></span>  

<span data-ttu-id="7f183-108">Дополнительные сведения о приложениях Магазина см. в под [управлением приложений с магазином.](holographic-store-apps.md)</span><span class="sxs-lookup"><span data-stu-id="7f183-108">For more information about store apps, see [Manage apps with the store](holographic-store-apps.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f183-109">Для HoloLens (1-е поколения), также называемого в то время выпуском HoloLens Developer Edition, были созданы следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="7f183-109">The following information was created for the HoloLens (1st gen), also called the HoloLens Developer Edition at the time.</span></span> <span data-ttu-id="7f183-110">Например, загрузка неоконтружаемых приложений через портал устройств и установка приложений Visual Studio тогда была распространена.</span><span class="sxs-lookup"><span data-stu-id="7f183-110">As such sideloading apps via device portal and installing apps via Visual Studio were commonplace then.</span></span> <span data-ttu-id="7f183-111">В корпоративных развертываниях не рекомендуется использовать режим разработчика, который используется в обоих этих методах.</span><span class="sxs-lookup"><span data-stu-id="7f183-111">For enterprise deployments we do not recommend enabling Developer Mode, which both of these methods use.</span></span> <span data-ttu-id="7f183-112">Если вы заинтересованы в безопасном способе развертывания приложений, просмотрите наше руководство [по управлению приложениями: обзор.](app-deploy-overview.md)</span><span class="sxs-lookup"><span data-stu-id="7f183-112">If you are interested in a secure app deployment method please review our [App Management: Overview](app-deploy-overview.md).</span></span>
>
> <span data-ttu-id="7f183-113">Если вы ищете способ разработчика установки приложений для устройств HoloLens 2, обратитесь к:</span><span class="sxs-lookup"><span data-stu-id="7f183-113">If you are looking for either developer method of app installation for HoloLens 2 devices please refer to:</span></span>
> - [<span data-ttu-id="7f183-114">Портал устройств: установка приложения</span><span class="sxs-lookup"><span data-stu-id="7f183-114">Device Portal: Installing an App</span></span>](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal#installing-an-app)
> - [<span data-ttu-id="7f183-115">Использование Visual Studio для развертывания и отлаки приложений</span><span class="sxs-lookup"><span data-stu-id="7f183-115">Using Visual Studio to deploy and debug Apps</span></span>](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-visual-studio)

## <span data-ttu-id="7f183-116">Установка пользовательских приложений</span><span class="sxs-lookup"><span data-stu-id="7f183-116">Install custom apps</span></span>

<span data-ttu-id="7f183-117">Вы можете установить собственные приложения на Устройство HoloLens с помощью портала устройств или путем развертывания приложений из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7f183-117">You can install your own applications on HoloLens either by using the Device Portal or by deploying the apps from Visual Studio.</span></span>

### <span data-ttu-id="7f183-118">Установка пакета приложения с помощью портала устройств</span><span class="sxs-lookup"><span data-stu-id="7f183-118">Installing an application package with the Device Portal</span></span>

1. <span data-ttu-id="7f183-119">Установить подключение портала [устройств к](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal) целевому устройству HoloLens.</span><span class="sxs-lookup"><span data-stu-id="7f183-119">Establish a connection from [Device Portal](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal) to the target HoloLens.</span></span>
1. <span data-ttu-id="7f183-120">В области навигации слева перейдите на страницу **"Приложения".**</span><span class="sxs-lookup"><span data-stu-id="7f183-120">In the left navigation, navigate to the **Apps** page .</span></span>
1. <span data-ttu-id="7f183-121">В **папке "Пакет** приложения" перейдите к APPX-файлу, связанному с вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="7f183-121">Under **App Package** browse to the .appx file that is associated with your application.</span></span>
   > [!IMPORTANT]
   > <span data-ttu-id="7f183-122">Обязательно ссылайтесь на все связанные файлы зависимостей и сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7f183-122">Make sure to reference any associated dependency and certificate files.</span></span>

1. <span data-ttu-id="7f183-123">Select **Go**.</span><span class="sxs-lookup"><span data-stu-id="7f183-123">Select **Go**.</span></span>
   ![Установка формы приложения на портале устройств Windows на Microsoft HoloLens](images/deviceportal-appmanager.jpg)

### <span data-ttu-id="7f183-125">Развертывание из Microsoft Visual Studio 2015</span><span class="sxs-lookup"><span data-stu-id="7f183-125">Deploying from Microsoft Visual Studio 2015</span></span>

1. <span data-ttu-id="7f183-126">Откройте решение Visual Studio приложения (SLN-файл).</span><span class="sxs-lookup"><span data-stu-id="7f183-126">Open your app's Visual Studio solution (.sln file).</span></span>
1. <span data-ttu-id="7f183-127">Откройте свойства **проекта.**</span><span class="sxs-lookup"><span data-stu-id="7f183-127">Open the project's **Properties**.</span></span>
1. <span data-ttu-id="7f183-128">Выберите следующую конфигурацию сборки: **Master/x86/Remote Machine.**</span><span class="sxs-lookup"><span data-stu-id="7f183-128">Select the following build configuration: **Master/x86/Remote Machine**.</span></span>
1. <span data-ttu-id="7f183-129">При выборе **удаленного компьютера:**</span><span class="sxs-lookup"><span data-stu-id="7f183-129">When you select **Remote Machine**:</span></span>
   - <span data-ttu-id="7f183-130">Убедитесь, что адрес указывает Wi-Fi IP-адрес holoLens.</span><span class="sxs-lookup"><span data-stu-id="7f183-130">Make sure the address points to the Wi-Fi IP address of your HoloLens.</span></span>
   - <span data-ttu-id="7f183-131">Установите для проверки **подлинности универсальный (незашифрованный протокол).**</span><span class="sxs-lookup"><span data-stu-id="7f183-131">Set authentication to **Universal (Unencrypted Protocol)**.</span></span>
1. <span data-ttu-id="7f183-132">Создайте решение.</span><span class="sxs-lookup"><span data-stu-id="7f183-132">Build your solution.</span></span>
1. <span data-ttu-id="7f183-133">Чтобы развернуть приложение с компьютера разработки на устройство HoloLens, выберите **удаленный компьютер.**</span><span class="sxs-lookup"><span data-stu-id="7f183-133">To deploy the app from your development PC to your HoloLens, select **Remote Machine**.</span></span> <span data-ttu-id="7f183-134">Если у вас уже есть сборка на HoloLens, выберите **"Да",** чтобы установить эту более новую версию.</span><span class="sxs-lookup"><span data-stu-id="7f183-134">If you already have an existing build on the HoloLens, select **Yes** to install this newer version.</span></span>  

   ![Развертывание приложений на удаленном компьютере для Microsoft HoloLens в Visual Studio](images/vs2015-remotedeployment.jpg)  
1. <span data-ttu-id="7f183-136">Приложение установит и автоматически запустится на вашем HoloLens.</span><span class="sxs-lookup"><span data-stu-id="7f183-136">The application will install and auto launch on your HoloLens.</span></span>

<span data-ttu-id="7f183-137">После установки приложения его можно найти в списке "Все **приложения"** (**"Запустить**  >  **все приложения").**</span><span class="sxs-lookup"><span data-stu-id="7f183-137">After you've installed an app, you'll find it in the **All apps** list (**Start** > **All apps**).</span></span>
