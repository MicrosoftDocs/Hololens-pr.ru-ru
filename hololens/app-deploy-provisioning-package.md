---
title: Пакет подготовки
description: приложение, развертывание приложений, детерстика корпоративного приложения, подготовка
keywords: приложение, развертывание приложений, разменая подготовка корпоративных приложений, подготовка
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
ms.openlocfilehash: 60efc454f9e1221372279401da9f8ee918e061e7
ms.sourcegitcommit: efa3fb7e353c5e56ee467cc7fd94ffdfaf46e2e5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/15/2020
ms.locfileid: "11219226"
---
# <span data-ttu-id="7ac9b-104">Пакет подготовки</span><span class="sxs-lookup"><span data-stu-id="7ac9b-104">Provisioning Package</span></span>

<span data-ttu-id="7ac9b-105">Пакеты подготовки можно использовать для подготовки и настройки устройств в среде без доступа к управлению конечными точками.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-105">Provisioning packages can be used to prepare and configure devices in an environment without access to endpoint management.</span></span> <span data-ttu-id="7ac9b-106">Они также могут быть развернуты на устройстве независимо от удостоверения пользователя, состояния регистрации, во время работы с приостановкой (OOBE) или путем применения пакета подготовка во время [установки.](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup)</span><span class="sxs-lookup"><span data-stu-id="7ac9b-106">They can also be deployed to a device regardless of identity of the user, enrollment status, during the Out of Box Experience (OOBE), or by [applying a provisioning package during setup](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup).</span></span>

## <span data-ttu-id="7ac9b-107">Вопросы, которые следует учитывать при упаковке пакетов.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-107">Provisioning Packages considerations:</span></span>
* <span data-ttu-id="7ac9b-108">Не общедоступные приложения</span><span class="sxs-lookup"><span data-stu-id="7ac9b-108">Non-Public apps</span></span>
* <span data-ttu-id="7ac9b-109">Только неогрузка USB</span><span class="sxs-lookup"><span data-stu-id="7ac9b-109">USB side-load only</span></span>
* <span data-ttu-id="7ac9b-110">Автоматическое обновление не требуется (требуется ручное обновление с помощью PPKG)</span><span class="sxs-lookup"><span data-stu-id="7ac9b-110">No auto update (requires manual updates via PPKGs)</span></span>

<span data-ttu-id="7ac9b-111">Приложения, установленные с помощью пакета предоставления, должны быть подписаны сертификатом в локальном хранилище компьютеров.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-111">Apps installed via a provisioning package must be signed by a certificate in the local machine store.</span></span> <span data-ttu-id="7ac9b-112">Пакеты предоставления могут устанавливать сертификаты только в хранилище устройства (локального компьютера), поэтому приложение и сертификат могут быть установлены через тот же пакет.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-112">Provisioning packages can only install certificates to the device (local machine) store, therefore the app and certificate may be installed via the same provisioning package.</span></span> <span data-ttu-id="7ac9b-113">Если вы развертываете сертификат из MDM [](certificate-manager.md)или устанавливаете его с помощью диспетчера сертификатов, обязательно разверните сертификат в локальном хранилище компьютеров, чтобы подписать установленные таким образом приложения.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-113">If you are deploying your certificate from MDM or installing via the [Certificate Manager](certificate-manager.md), please make sure to deploy the certificate to the local machine store to sign apps installed this way.</span></span>

<span data-ttu-id="7ac9b-114">Чтобы узнать основы создания пакета подготовки для устройств HoloLens, посетите сайт [подготовки HoloLens.](https://docs.microsoft.com/hololens/hololens-provisioning)</span><span class="sxs-lookup"><span data-stu-id="7ac9b-114">To learn the basics of creating a Provisioning Package for HoloLens devices, visit [HoloLens Provisioning](https://docs.microsoft.com/hololens/hololens-provisioning).</span></span> <span data-ttu-id="7ac9b-115">Чтобы развернуть приложение, необходимо начать с расширенных настойки.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-115">To deploy an app, you must start with advanced provisioning.</span></span>

> [!NOTE]
> <span data-ttu-id="7ac9b-116">HoloLens (1-е поколения) имеет ограниченную поддержку установки приложений **(UniversalAppInstall)** с помощью пакета подготовка.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-116">HoloLens (1st gen) has limited support installing apps (**UniversalAppInstall**) by using a provisioning package.</span></span> <span data-ttu-id="7ac9b-117">Устройства HoloLens (1-е поколения) поддерживают установку приложения через PPKG только во время OOBE и только при установке контекста пользователя.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-117">HoloLens (1st gen) devices only support installing an app via PPKG only during OOBE and only with user context installs.</span></span>

## <span data-ttu-id="7ac9b-118">Настройка</span><span class="sxs-lookup"><span data-stu-id="7ac9b-118">Setup</span></span>

<span data-ttu-id="7ac9b-119">В [конструкторе конфигураций Windows](https://www.microsoft.com/store/productId/9NBLGGH4TX22) необходимо предпринять следующие 4 действия.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-119">Within [Windows Configuration Designer](https://www.microsoft.com/store/productId/9NBLGGH4TX22) take following 4 steps.</span></span>

1. <span data-ttu-id="7ac9b-120">Задайте для ApplicationManagement/AllowAllTrustedApps "Да".</span><span class="sxs-lookup"><span data-stu-id="7ac9b-120">Set ApplicationManagement/AllowAllTrustedApps To “Yes”.</span></span> <span data-ttu-id="7ac9b-121">См. [applicationManagement/AllowAllTrustedApps.](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)</span><span class="sxs-lookup"><span data-stu-id="7ac9b-121">See: [ApplicationManagement/AllowAllTrustedApps](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps).</span></span>

2. <span data-ttu-id="7ac9b-122">В **области UniversalAppInstall**  >  **UserContextAppLicense** введите **PackageFamilyName.**</span><span class="sxs-lookup"><span data-stu-id="7ac9b-122">Under **UniversalAppInstall** > **UserContextAppLicense** please enter the **PackageFamilyName**.</span></span> <span data-ttu-id="7ac9b-123">См. [universalAppInstall](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall).</span><span class="sxs-lookup"><span data-stu-id="7ac9b-123">See [UniversalAppInstall](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall).</span></span> <span data-ttu-id="7ac9b-124">См. также: [UserContextAppLicense](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).</span><span class="sxs-lookup"><span data-stu-id="7ac9b-124">See also: [UserContextAppLicense](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).</span></span>

   <span data-ttu-id="7ac9b-125">Портал устройств можно использовать на устройстве, на которое уже установлено приложение.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-125">You can use Device Portal on a device you have already installed your app to.</span></span> <span data-ttu-id="7ac9b-126">Посетите страницу "Приложения" и посмотрите на строку PackageRelativeID перед строкой "!" Is your **PackageFamilyName**.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-126">Visit the Apps page, and look at the PackageRelativeID line, all the information before the "!" Is your **PackageFamilyName**.</span></span>
    
3. <span data-ttu-id="7ac9b-127">После этого вы увидите, что у вас есть новый раздел **ApplicationFile.**</span><span class="sxs-lookup"><span data-stu-id="7ac9b-127">You will then see that you have a new section, **ApplicationFile**.</span></span> <span data-ttu-id="7ac9b-128">Используйте эту область для отправки пакета appx.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-128">Use this area to upload your appx bundle.</span></span>

4. <span data-ttu-id="7ac9b-129">В зависимости от того, приобрели ли вы приложение или создали собственное бизнес-приложение, вам потребуется отправить файл лицензии или сертификат безопасности.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-129">Depending on if you have purchased your app or built your own LOB app, you will need to upload the license file or security certificate.</span></span>

    - <span data-ttu-id="7ac9b-130">Для файла лицензии: в **папке UniversalAppInstall**  >  **UserContextAppLience** перейдите к расположению лицензии и загрузите ее.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-130">For license file: Under **UniversalAppInstall** > **UserContextAppLience** and browse to the location of your license and upload it.</span></span> 
    - <span data-ttu-id="7ac9b-131">Для файла безопасности перейдите к **файлу "Сертификаты"** и выберите сертификат для установки вместе с пакетом APPX.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-131">For security file navigate to **Certificates** and select your certificate to install alongside your .appx bundle.</span></span>

<span data-ttu-id="7ac9b-132">Обязательно сохраните проект в надежном месте.</span><span class="sxs-lookup"><span data-stu-id="7ac9b-132">Make sure to save your project to a secure location.</span></span> <span data-ttu-id="7ac9b-133">Затем **экспортировать** его в качестве **пакета предоставления.**</span><span class="sxs-lookup"><span data-stu-id="7ac9b-133">Then **Export** it as a **Provisioning Package**.</span></span>  
    
<span data-ttu-id="7ac9b-134">См. также: [применение пакета подготовка к HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).</span><span class="sxs-lookup"><span data-stu-id="7ac9b-134">See also: [Apply your provisiong package to HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).</span></span>
