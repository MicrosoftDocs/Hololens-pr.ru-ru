---
title: Пакет подготовки
description: приложение, развертывание приложений, корпоративное приложение demployment, подготовка
keywords: приложение, развертывание приложений, корпоративное приложение demployment, подготовка
author: v-jodben
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
ms.openlocfilehash: 7417f9e8cf1921d9fdb57dbd96fff094e21c44f9
ms.sourcegitcommit: 29755f5af0086a43c532fb5a9a4ae65c36bc82de
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2020
ms.locfileid: "10857950"
---
# <span data-ttu-id="73018-104">Пакет подготовки</span><span class="sxs-lookup"><span data-stu-id="73018-104">Provisioning Package</span></span>

<span data-ttu-id="73018-105">Пакеты подготовки можно использовать для подготовки и настройки устройств в среде без доступа к управлению конечными точками.</span><span class="sxs-lookup"><span data-stu-id="73018-105">Provisioning packages can be used to prepare and configure devices in an environment without access to endpoint management.</span></span> <span data-ttu-id="73018-106">Кроме того, они могут быть развернуты на устройстве независимо от удостоверения пользователя, состояния регистрации, при использовании функции "Исходящие" (OOBE) или путем [применения пакета подготовки во время настройки](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup).</span><span class="sxs-lookup"><span data-stu-id="73018-106">They can also be deployed to a device regardless of identity of the user, enrollment status, during the Out of Box Experience (OOBE), or by [applying a provisioning package during setup](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup).</span></span>

## <span data-ttu-id="73018-107">Общие сведения о пакетах подготовки:</span><span class="sxs-lookup"><span data-stu-id="73018-107">Provisioning Packages considerations:</span></span>
* <span data-ttu-id="73018-108">Приложения, не являющиеся общими</span><span class="sxs-lookup"><span data-stu-id="73018-108">Non-Public apps</span></span>
* <span data-ttu-id="73018-109">USB-Загрузка только на полях</span><span class="sxs-lookup"><span data-stu-id="73018-109">USB side-load only</span></span>
* <span data-ttu-id="73018-110">Без автоматического обновления (требуется обновление вручную через PPKGs)</span><span class="sxs-lookup"><span data-stu-id="73018-110">No auto update (requires manual updates via PPKGs)</span></span>

> [!NOTE] 
> <span data-ttu-id="73018-111">Чтобы узнать основы создания пакета подготовки для устройств HoloLens, перейдите на страницу [Подготовка HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning).</span><span class="sxs-lookup"><span data-stu-id="73018-111">To learn the basics of creating a Provisioning Package for HoloLens devices, visit [HoloLens Provisioning](https://docs.microsoft.com/hololens/hololens-provisioning).</span></span> <span data-ttu-id="73018-112">Чтобы развернуть приложение, необходимо запустить расширенную подготовку.</span><span class="sxs-lookup"><span data-stu-id="73018-112">To deploy an app, you must start with advanced provisioning.</span></span> 

## <span data-ttu-id="73018-113">Настройка</span><span class="sxs-lookup"><span data-stu-id="73018-113">Setup</span></span>

<span data-ttu-id="73018-114">В [конструкторе конфигураций Windows](https://www.microsoft.com/store/productId/9NBLGGH4TX22) выполните действия, описанные ниже 4.</span><span class="sxs-lookup"><span data-stu-id="73018-114">Within [Windows Configuration Designer](https://www.microsoft.com/store/productId/9NBLGGH4TX22) take following 4 steps.</span></span>

1. <span data-ttu-id="73018-115">Установите для ApplicationManagement/AllowAllTrustedApps значение "Да".</span><span class="sxs-lookup"><span data-stu-id="73018-115">Set ApplicationManagement/AllowAllTrustedApps To “Yes”.</span></span> <span data-ttu-id="73018-116">Смотрите: [ApplicationManagement/AllowAllTrustedApps](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps).</span><span class="sxs-lookup"><span data-stu-id="73018-116">See: [ApplicationManagement/AllowAllTrustedApps](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps).</span></span>
2. <span data-ttu-id="73018-117">В разделе **UniversalAppInstall**  >  **UserContextAppLicense** введите **PackageFamilyName**.</span><span class="sxs-lookup"><span data-stu-id="73018-117">Under **UniversalAppInstall** > **UserContextAppLicense** please enter the **PackageFamilyName**.</span></span> <span data-ttu-id="73018-118">Смотрите [UniversalAppInstall](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall).</span><span class="sxs-lookup"><span data-stu-id="73018-118">See [UniversalAppInstall](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall).</span></span> <span data-ttu-id="73018-119">Смотрите также: [UserContextAppLicense](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).</span><span class="sxs-lookup"><span data-stu-id="73018-119">See also: [UserContextAppLicense](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).</span></span>
    - <span data-ttu-id="73018-120">Если вы не знаете это, вы можете использовать портал устройств на устройстве, на котором уже установлено приложение.</span><span class="sxs-lookup"><span data-stu-id="73018-120">If you don’t know this, you can use Device Portal on a device you have already installed your app to.</span></span> <span data-ttu-id="73018-121">Перейдите на страницу "приложения" и ознакомьтесь со строкой "PackageRelativeID", а также сведениями до "!". **PackageFamilyName**.</span><span class="sxs-lookup"><span data-stu-id="73018-121">Visit the Apps page, and look at the PackageRelativeID line, all the information before the "!" Is your **PackageFamilyName**.</span></span>
3. <span data-ttu-id="73018-122">Вы увидите, что у вас новый раздел, **ApplicationFile**.</span><span class="sxs-lookup"><span data-stu-id="73018-122">You will then see that you have a new section, **ApplicationFile**.</span></span> <span data-ttu-id="73018-123">Используйте эту область для отправки пакета Appx.</span><span class="sxs-lookup"><span data-stu-id="73018-123">Use this area to upload your appx bundle.</span></span> 
4. <span data-ttu-id="73018-124">В зависимости от того, приобрели ли вы приложение или создали собственное бизнес-приложение, вам нужно будет загрузить файл лицензии или сертификат безопасности.</span><span class="sxs-lookup"><span data-stu-id="73018-124">Depending on if you have purchased your app or built your own LOB app, you will need to upload the license file or security certificate.</span></span>
    - <span data-ttu-id="73018-125">Для файла лицензии: в разделе **UniversalAppInstall**  >  **UserContextAppLience** и перейдите в папку, в которой находится лицензия, и отправьте ее.</span><span class="sxs-lookup"><span data-stu-id="73018-125">For license file: Under **UniversalAppInstall** > **UserContextAppLience** and browse to the location of your license and upload it.</span></span> 
    - <span data-ttu-id="73018-126">В разделе "файл безопасности" перейдите в раздел " **Сертификаты** " и выберите сертификат, который нужно установить вместе с пакетом Appx.</span><span class="sxs-lookup"><span data-stu-id="73018-126">For security file navigate to **Certificates** and select your certificate to install alongside your .appx bundle.</span></span> 

<span data-ttu-id="73018-127">Не забудьте сохранить проект в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="73018-127">Make sure to save your project to a secure location.</span></span> <span data-ttu-id="73018-128">Затем **экспортируйте** его как **пакет подготовки**.</span><span class="sxs-lookup"><span data-stu-id="73018-128">Then **Export** it as a **Provisioning Package**.</span></span>  
    
<span data-ttu-id="73018-129">Дополнительные сведения: [Применение пакета provisiong к HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).</span><span class="sxs-lookup"><span data-stu-id="73018-129">See also: [Apply your provisiong package to HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).</span></span>
