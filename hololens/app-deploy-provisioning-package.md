---
title: Подготовка пакета
description: Дополнительные сведения о пакетировании приложений, подготовке, развертывании и развертывании корпоративных приложений для устройств HoloLens.
keywords: приложение, развертывание приложений, развертывание корпоративного приложения, подготовка
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
ms.openlocfilehash: 9c73b03e6a8dca6baf6c58fed091df96994c3780
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309407"
---
# <a name="provisioning-package"></a><span data-ttu-id="5734c-104">Подготовка пакета</span><span class="sxs-lookup"><span data-stu-id="5734c-104">Provisioning Package</span></span>

<span data-ttu-id="5734c-105">Пакеты подготовки можно использовать для подготовки и настройки устройств в среде без доступа к управлению конечными точками.</span><span class="sxs-lookup"><span data-stu-id="5734c-105">Provisioning packages can be used to prepare and configure devices in an environment without access to endpoint management.</span></span> <span data-ttu-id="5734c-106">Кроме того, их можно развернуть на устройстве независимо от удостоверения пользователя, состояния регистрации, во время работы при первом включении (OOBE) или путем [применения пакета подготовки во время установки](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup).</span><span class="sxs-lookup"><span data-stu-id="5734c-106">They can also be deployed to a device regardless of identity of the user, enrollment status, during the Out of Box Experience (OOBE), or by [applying a provisioning package during setup](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup).</span></span>

## <a name="provisioning-packages-considerations"></a><span data-ttu-id="5734c-107">Рекомендации по подготовке пакетов:</span><span class="sxs-lookup"><span data-stu-id="5734c-107">Provisioning Packages considerations:</span></span>

* <span data-ttu-id="5734c-108">Приложения, не являющиеся общедоступными</span><span class="sxs-lookup"><span data-stu-id="5734c-108">Non-Public apps</span></span>
* <span data-ttu-id="5734c-109">Только для загрузки с USB</span><span class="sxs-lookup"><span data-stu-id="5734c-109">USB side-load only</span></span>
* <span data-ttu-id="5734c-110">Без автоматического обновления (требуется обновление вручную через Ппкгс)</span><span class="sxs-lookup"><span data-stu-id="5734c-110">No auto update (requires manual updates via PPKGs)</span></span>

<span data-ttu-id="5734c-111">Приложения, установленные с помощью пакета подготовки, должны быть подписаны сертификатом в хранилище локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="5734c-111">Apps installed via a provisioning package must be signed by a certificate in the local machine store.</span></span> <span data-ttu-id="5734c-112">Пакеты подготовки могут устанавливать сертификаты только в хранилище устройства (локальный компьютер), поэтому приложение и сертификат могут быть установлены с помощью одного и того же пакета подготовки.</span><span class="sxs-lookup"><span data-stu-id="5734c-112">Provisioning packages can only install certificates to the device (local machine) store, therefore an app and certificate may be installed via the same provisioning package.</span></span> <span data-ttu-id="5734c-113">Если вы развертываете сертификат из MDM или устанавливаете с помощью [диспетчера сертификатов](certificate-manager.md), не забудьте развернуть сертификат в хранилище локального компьютера, чтобы подписывать установленные таким образом приложения.</span><span class="sxs-lookup"><span data-stu-id="5734c-113">If you are deploying your certificate from MDM or installing via the [Certificate Manager](certificate-manager.md), make sure to deploy the certificate to the local machine store to sign apps installed this way.</span></span>

<span data-ttu-id="5734c-114">Чтобы узнать основные сведения о создании пакета подготовки для устройств HoloLens, перейдите на страницу [подготовки hololens](https://docs.microsoft.com/hololens/hololens-provisioning).</span><span class="sxs-lookup"><span data-stu-id="5734c-114">To learn the basics of creating a Provisioning Package for HoloLens devices, visit [HoloLens Provisioning](https://docs.microsoft.com/hololens/hololens-provisioning).</span></span> <span data-ttu-id="5734c-115">Чтобы развернуть приложение, необходимо начать с расширенной подготовки.</span><span class="sxs-lookup"><span data-stu-id="5734c-115">To deploy an app, you must start with advanced provisioning.</span></span>

> [!NOTE]
> <span data-ttu-id="5734c-116">HoloLens (1 общий) имеет ограниченную поддержку установки приложений (**универсалаппинсталл**) с помощью пакета подготовки.</span><span class="sxs-lookup"><span data-stu-id="5734c-116">HoloLens (1st gen) has limited support installing apps (**UniversalAppInstall**) by using a provisioning package.</span></span> <span data-ttu-id="5734c-117">Устройства HoloLens (1-го поколения) поддерживают установку только с помощью PPKG только во время OOBE и только при установке контекста пользователя.</span><span class="sxs-lookup"><span data-stu-id="5734c-117">HoloLens (1st gen) devices only support installing an app via PPKG only during OOBE and only with user context installs.</span></span>

## <a name="setup"></a><span data-ttu-id="5734c-118">Настройка</span><span class="sxs-lookup"><span data-stu-id="5734c-118">Setup</span></span>

<span data-ttu-id="5734c-119">В [конструкторе конфигурации Windows](https://www.microsoft.com/store/productId/9NBLGGH4TX22) выполните следующие четыре шага.</span><span class="sxs-lookup"><span data-stu-id="5734c-119">Within [Windows Configuration Designer](https://www.microsoft.com/store/productId/9NBLGGH4TX22) take following four steps.</span></span>

1. <span data-ttu-id="5734c-120">Задайте для Аппликатионманажемент/AllowAllTrustedApps значение "Да".</span><span class="sxs-lookup"><span data-stu-id="5734c-120">Set ApplicationManagement/AllowAllTrustedApps To “Yes”.</span></span> <span data-ttu-id="5734c-121">См. раздел: [аппликатионманажемент/AllowAllTrustedApps](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps).</span><span class="sxs-lookup"><span data-stu-id="5734c-121">See: [ApplicationManagement/AllowAllTrustedApps](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps).</span></span>

2. <span data-ttu-id="5734c-122">Перейдите к **универсалаппинсталл**  >  **усерконтекстапплиценсе** введите **паккажефамилинаме**.</span><span class="sxs-lookup"><span data-stu-id="5734c-122">Navigate to **UniversalAppInstall** > **UserContextAppLicense** enter the **PackageFamilyName**.</span></span> <span data-ttu-id="5734c-123">См. [универсалаппинсталл](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall).</span><span class="sxs-lookup"><span data-stu-id="5734c-123">See [UniversalAppInstall](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall).</span></span> <span data-ttu-id="5734c-124">См. также: [усерконтекстапплиценсе](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).</span><span class="sxs-lookup"><span data-stu-id="5734c-124">See also: [UserContextAppLicense](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).</span></span>

   <span data-ttu-id="5734c-125">Вы можете использовать портал устройств на устройстве, на котором вы уже установили приложение.</span><span class="sxs-lookup"><span data-stu-id="5734c-125">You can use Device Portal on a device you have already installed your app to.</span></span> <span data-ttu-id="5734c-126">Посетите страницу приложений и взгляните на строку Паккажерелативеид, всю информацию до "!" **Паккажефамилинаме**.</span><span class="sxs-lookup"><span data-stu-id="5734c-126">Visit the Apps page, and look at the PackageRelativeID line, all the information before the "!" Is your **PackageFamilyName**.</span></span>

3. <span data-ttu-id="5734c-127">Вы увидите, что у вас есть новый раздел **аппликатионфиле**.</span><span class="sxs-lookup"><span data-stu-id="5734c-127">You will then see that you have a new section, **ApplicationFile**.</span></span> <span data-ttu-id="5734c-128">Используйте эту область для отправки пакета Appx.</span><span class="sxs-lookup"><span data-stu-id="5734c-128">Use this area to upload your appx bundle.</span></span>

4. <span data-ttu-id="5734c-129">В зависимости от того, приобретено ли приложение или создано собственное бизнес-приложение, необходимо отправить файл лицензии или сертификат безопасности.</span><span class="sxs-lookup"><span data-stu-id="5734c-129">Depending on if you have purchased your app or built your own LOB app, you will need to upload the license file or security certificate.</span></span>

    - <span data-ttu-id="5734c-130">В поле файл лицензии: перейдите по адресу **универсалаппинсталл**  >  **усерконтекстапплиценце** и перейдите к расположению лицензии и отправьте его.</span><span class="sxs-lookup"><span data-stu-id="5734c-130">For license file: navigate to **UniversalAppInstall** > **UserContextAppLicence** and browse to the location of your license and upload it.</span></span>
    - <span data-ttu-id="5734c-131">Для файла безопасности перейдите к разделу **Сертификаты** и выберите сертификат для установки вместе с пакетом Appx.</span><span class="sxs-lookup"><span data-stu-id="5734c-131">For the security file, navigate to **Certificates** and select your certificate to install alongside your .appx bundle.</span></span>

<span data-ttu-id="5734c-132">Обязательно сохраните проект в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="5734c-132">Make sure to save your project to a secure location.</span></span> <span data-ttu-id="5734c-133">Затем **экспортируйте** его как **пакет подготовки**.</span><span class="sxs-lookup"><span data-stu-id="5734c-133">Then **Export** it as a **Provisioning Package**.</span></span>  

<span data-ttu-id="5734c-134">См. также: [Применение пакета подготовки к HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).</span><span class="sxs-lookup"><span data-stu-id="5734c-134">See also: [Apply your provisioning package to HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).</span></span>
