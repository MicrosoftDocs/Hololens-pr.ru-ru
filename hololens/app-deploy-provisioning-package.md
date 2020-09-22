---
title: Пакет подготовки
description: приложение, развертывание приложений, корпоративное приложение demployment, подготовка
keywords: приложение, развертывание приложений, корпоративное приложение demployment, подготовка
author: evmill
ms.author: v-evmill
ms.date: 6/22/2020
ms.prod: hololens
ms.sitesec: library
ms.topic: article
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 0803b5f1b77ac7f123d534d101cd24903b87094c
ms.sourcegitcommit: 89ce6cdc0fc6d70a88217791c5f6d613778af614
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "11052586"
---
# <span data-ttu-id="4df94-104">Пакет подготовки</span><span class="sxs-lookup"><span data-stu-id="4df94-104">Provisioning Package</span></span>

<span data-ttu-id="4df94-105">Пакеты подготовки можно использовать для подготовки и настройки устройств в среде без доступа к управлению конечными точками.</span><span class="sxs-lookup"><span data-stu-id="4df94-105">Provisioning packages can be used to prepare and configure devices in an environment without access to endpoint management.</span></span> <span data-ttu-id="4df94-106">Кроме того, они могут быть развернуты на устройстве независимо от удостоверения пользователя, состояния регистрации, при использовании функции "Исходящие" (OOBE) или путем [применения пакета подготовки во время настройки](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup).</span><span class="sxs-lookup"><span data-stu-id="4df94-106">They can also be deployed to a device regardless of identity of the user, enrollment status, during the Out of Box Experience (OOBE), or by [applying a provisioning package during setup](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup).</span></span>

## <span data-ttu-id="4df94-107">Общие сведения о пакетах подготовки:</span><span class="sxs-lookup"><span data-stu-id="4df94-107">Provisioning Packages considerations:</span></span>
* <span data-ttu-id="4df94-108">Приложения, не являющиеся общими</span><span class="sxs-lookup"><span data-stu-id="4df94-108">Non-Public apps</span></span>
* <span data-ttu-id="4df94-109">USB-Загрузка только на полях</span><span class="sxs-lookup"><span data-stu-id="4df94-109">USB side-load only</span></span>
* <span data-ttu-id="4df94-110">Без автоматического обновления (требуется обновление вручную через PPKGs)</span><span class="sxs-lookup"><span data-stu-id="4df94-110">No auto update (requires manual updates via PPKGs)</span></span>

> [!NOTE] 
> <span data-ttu-id="4df94-111">Чтобы узнать основы создания пакета подготовки для устройств HoloLens, перейдите на страницу [Подготовка HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning).</span><span class="sxs-lookup"><span data-stu-id="4df94-111">To learn the basics of creating a Provisioning Package for HoloLens devices, visit [HoloLens Provisioning](https://docs.microsoft.com/hololens/hololens-provisioning).</span></span> <span data-ttu-id="4df94-112">Чтобы развернуть приложение, необходимо запустить расширенную подготовку.</span><span class="sxs-lookup"><span data-stu-id="4df94-112">To deploy an app, you must start with advanced provisioning.</span></span> 

> [!NOTE] 
> <span data-ttu-id="4df94-113">HoloLens (1-ой gen) имеет ограниченную поддержку установки приложений (**UniversalAppInstall**) с помощью пакета подготовки.</span><span class="sxs-lookup"><span data-stu-id="4df94-113">HoloLens (1st gen) has limited support installing apps (**UniversalAppInstall**) by using a provisioning package.</span></span> <span data-ttu-id="4df94-114">Устройства HoloLens (1-го поколения) поддерживают только установку приложения с помощью PPKG только во время OOBE и только при установке контекста пользователя.</span><span class="sxs-lookup"><span data-stu-id="4df94-114">HoloLens (1st gen) devices only support installing an app via PPKG only during OOBE and only with user context installs.</span></span>

## <span data-ttu-id="4df94-115">Настройка</span><span class="sxs-lookup"><span data-stu-id="4df94-115">Setup</span></span>

<span data-ttu-id="4df94-116">В [конструкторе конфигураций Windows](https://www.microsoft.com/store/productId/9NBLGGH4TX22) выполните действия, описанные ниже 4.</span><span class="sxs-lookup"><span data-stu-id="4df94-116">Within [Windows Configuration Designer](https://www.microsoft.com/store/productId/9NBLGGH4TX22) take following 4 steps.</span></span>

1. <span data-ttu-id="4df94-117">Установите для ApplicationManagement/AllowAllTrustedApps значение "Да".</span><span class="sxs-lookup"><span data-stu-id="4df94-117">Set ApplicationManagement/AllowAllTrustedApps To “Yes”.</span></span> <span data-ttu-id="4df94-118">Смотрите: [ApplicationManagement/AllowAllTrustedApps](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps).</span><span class="sxs-lookup"><span data-stu-id="4df94-118">See: [ApplicationManagement/AllowAllTrustedApps](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps).</span></span>
2. <span data-ttu-id="4df94-119">В разделе **UniversalAppInstall**  >  **UserContextAppLicense** введите **PackageFamilyName**.</span><span class="sxs-lookup"><span data-stu-id="4df94-119">Under **UniversalAppInstall** > **UserContextAppLicense** please enter the **PackageFamilyName**.</span></span> <span data-ttu-id="4df94-120">Смотрите [UniversalAppInstall](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall).</span><span class="sxs-lookup"><span data-stu-id="4df94-120">See [UniversalAppInstall](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall).</span></span> <span data-ttu-id="4df94-121">Смотрите также: [UserContextAppLicense](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).</span><span class="sxs-lookup"><span data-stu-id="4df94-121">See also: [UserContextAppLicense](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).</span></span>
    - <span data-ttu-id="4df94-122">Если вы не знаете это, вы можете использовать портал устройств на устройстве, на котором уже установлено приложение.</span><span class="sxs-lookup"><span data-stu-id="4df94-122">If you don’t know this, you can use Device Portal on a device you have already installed your app to.</span></span> <span data-ttu-id="4df94-123">Перейдите на страницу "приложения" и ознакомьтесь со строкой "PackageRelativeID", а также сведениями до "!". **PackageFamilyName**.</span><span class="sxs-lookup"><span data-stu-id="4df94-123">Visit the Apps page, and look at the PackageRelativeID line, all the information before the "!" Is your **PackageFamilyName**.</span></span>
3. <span data-ttu-id="4df94-124">Вы увидите, что у вас новый раздел, **ApplicationFile**.</span><span class="sxs-lookup"><span data-stu-id="4df94-124">You will then see that you have a new section, **ApplicationFile**.</span></span> <span data-ttu-id="4df94-125">Используйте эту область для отправки пакета Appx.</span><span class="sxs-lookup"><span data-stu-id="4df94-125">Use this area to upload your appx bundle.</span></span> 
4. <span data-ttu-id="4df94-126">В зависимости от того, приобрели ли вы приложение или создали собственное бизнес-приложение, вам нужно будет загрузить файл лицензии или сертификат безопасности.</span><span class="sxs-lookup"><span data-stu-id="4df94-126">Depending on if you have purchased your app or built your own LOB app, you will need to upload the license file or security certificate.</span></span>
    - <span data-ttu-id="4df94-127">Для файла лицензии: в разделе **UniversalAppInstall**  >  **UserContextAppLience** и перейдите в папку, в которой находится лицензия, и отправьте ее.</span><span class="sxs-lookup"><span data-stu-id="4df94-127">For license file: Under **UniversalAppInstall** > **UserContextAppLience** and browse to the location of your license and upload it.</span></span> 
    - <span data-ttu-id="4df94-128">В разделе "файл безопасности" перейдите в раздел " **Сертификаты** " и выберите сертификат, который нужно установить вместе с пакетом Appx.</span><span class="sxs-lookup"><span data-stu-id="4df94-128">For security file navigate to **Certificates** and select your certificate to install alongside your .appx bundle.</span></span> 

<span data-ttu-id="4df94-129">Не забудьте сохранить проект в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="4df94-129">Make sure to save your project to a secure location.</span></span> <span data-ttu-id="4df94-130">Затем **экспортируйте** его как **пакет подготовки**.</span><span class="sxs-lookup"><span data-stu-id="4df94-130">Then **Export** it as a **Provisioning Package**.</span></span>  
    
<span data-ttu-id="4df94-131">Дополнительные сведения: [Применение пакета provisiong к HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).</span><span class="sxs-lookup"><span data-stu-id="4df94-131">See also: [Apply your provisiong package to HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).</span></span>
