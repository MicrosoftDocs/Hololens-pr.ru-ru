---
title: Общие сведения об управлении приложениями
description: приложение, управление, Управление приложениями
keywords: HoloLens, пользователь, учетная запись, приложение, Управление приложениями,
author: evmill
ms.author: v-evmill
ms.date: 6/22/2020
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: ITPro
manager: yannisle
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 36d86e24cc10d6b8457cfb415528398a8d43aa27
ms.sourcegitcommit: 108b818130e2627bf08107f4e47ae159dd6ab1d2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "11162864"
---
# <span data-ttu-id="6808d-104">Управление приложением: обзор</span><span class="sxs-lookup"><span data-stu-id="6808d-104">App Management: Overview</span></span>

<span data-ttu-id="6808d-105">Вы можете развертывать приложения с четырьмя разными путями: **Управление мобильными устройствами (MDM)**, **Microsoft Store для бизнеса**, **Microsoft Store**или устанавливать их с помощью **подготовки**.</span><span class="sxs-lookup"><span data-stu-id="6808d-105">You can deploy apps on four different paths: **Mobile Device Management (MDM)**, **Microsoft Store for Business**, **Microsoft Store**, or by installing them via **Provisioning**.</span></span> 

## <span data-ttu-id="6808d-106">Управление мобильными устройствами (MDM)</span><span class="sxs-lookup"><span data-stu-id="6808d-106">Mobile Device Management (MDM)</span></span>

<span data-ttu-id="6808d-107">Решение MDM позволяет руководителям ИТ-отдела и администраторам автоматически устанавливать собственные приложения, а также приобретать приложения из магазина для группы пользователей в магазине для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6808d-107">An MDM solution enables IT decision-makers and administrators to privately auto-install (push) their in-house, line-of-business apps, or purchase apps through the store for a group of users.</span></span> <span data-ttu-id="6808d-108">Устройства HoloLens лучше работают с Microsoft Endpoint Manager (Intune) для [управления приложениями](app-deploy-intune.md).</span><span class="sxs-lookup"><span data-stu-id="6808d-108">HoloLens devices work best with Microsoft Endpoint Manager (Intune) for [application management](app-deploy-intune.md).</span></span> <span data-ttu-id="6808d-109">Кроме того, Intune позволяет пользователям более детально управлять управляемыми приложениями с помощью загружаемого приложения с портала компании.</span><span class="sxs-lookup"><span data-stu-id="6808d-109">Intune also offers users finer-grained control over IT-managed apps through the Company Portal downloadable experience.</span></span>

> [!NOTE] 
> <span data-ttu-id="6808d-110">Ниже приведены инструкции для пользователей, которые хотят управлять своими приложениями с помощью Intune.</span><span class="sxs-lookup"><span data-stu-id="6808d-110">The following instructions are for users who want to manage their applications with Intune.</span></span> <span data-ttu-id="6808d-111">Корпорация Microsoft рекомендует использовать Intune для управления приложениями и устройствами.</span><span class="sxs-lookup"><span data-stu-id="6808d-111">Microsoft recommends using Intune for application and device management.</span></span>
    
<span data-ttu-id="6808d-112">Управление мобильными устройствами (MDM) применимо для следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="6808d-112">Mobile Device Management (MDM) is applicable for:</span></span> 
* <span data-ttu-id="6808d-113">Развернутые MDM + корпоративный портал</span><span class="sxs-lookup"><span data-stu-id="6808d-113">MDM deployed + Company Portal</span></span> 
* <span data-ttu-id="6808d-114">Строка из бизнеса (не общедоступных) приложений</span><span class="sxs-lookup"><span data-stu-id="6808d-114">Line of Buisness (non-public) apps</span></span>
* <span data-ttu-id="6808d-115">Ручная установка доступных приложений с помощью корпоративного портала</span><span class="sxs-lookup"><span data-stu-id="6808d-115">Manual installation of available applications through Company Portal</span></span>
* <span data-ttu-id="6808d-116">Политика MDM, принудительная отправка администратором</span><span class="sxs-lookup"><span data-stu-id="6808d-116">Admin push through MDM policy</span></span>
* <span data-ttu-id="6808d-117">Автоматическое обновление через MDM</span><span class="sxs-lookup"><span data-stu-id="6808d-117">Auto update through MDM</span></span>

## <span data-ttu-id="6808d-118">Microsoft Store для бизнеса</span><span class="sxs-lookup"><span data-stu-id="6808d-118">Microsoft Store for Business</span></span>

<span data-ttu-id="6808d-119">[Microsoft Store для бизнеса](app-deploy-store-business.md) предоставляет ИТ-специалистам и администраторам возможность находить, принимать, управлять и распространять бесплатные и платные приложения.</span><span class="sxs-lookup"><span data-stu-id="6808d-119">The [Microsoft Store for Business](app-deploy-store-business.md) provides IT decision-makers and administrators in businesses to find, acquire, manage, and distribute free and paid apps.</span></span> <span data-ttu-id="6808d-120">ИТ-администраторы могут управлять приложениями Microsoft Store и частными бизнес-приложениями, а также назначать и повторно использовать лицензии в соответствии с потребностями.</span><span class="sxs-lookup"><span data-stu-id="6808d-120">IT administrators can manage Microsoft Store apps and private line-of-business apps in one inventory, plus assign and re-use licenses as needed.</span></span> <span data-ttu-id="6808d-121">Дополнительные сведения можно найти [в разделе Предварительные требования для использования Microsoft Store для бизнеса](https://docs.microsoft.com/microsoft-store/prerequisites-microsoft-store-for-business).</span><span class="sxs-lookup"><span data-stu-id="6808d-121">For more information, visit [Prerequisites for using the Microsoft Store for Business](https://docs.microsoft.com/microsoft-store/prerequisites-microsoft-store-for-business).</span></span>
    
<span data-ttu-id="6808d-122">Приложение Microsoft Store для бизнеса применимо для следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="6808d-122">The Microsoft Store for Business is applicable for:</span></span> 
* <span data-ttu-id="6808d-123">Общедоступная или линейная бизнес-приложения</span><span class="sxs-lookup"><span data-stu-id="6808d-123">Public or Line of Business apps</span></span>
* <span data-ttu-id="6808d-124">Автоматическая установка необходимых приложений через ассоциацию MDM</span><span class="sxs-lookup"><span data-stu-id="6808d-124">Automatic installation of required applications through MDM association</span></span>
* <span data-ttu-id="6808d-125">Приложения загружаются вручную</span><span class="sxs-lookup"><span data-stu-id="6808d-125">User manually downloads apps</span></span>
* <span data-ttu-id="6808d-126">Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="6808d-126">Auto Update</span></span>

## <span data-ttu-id="6808d-127">Приложения Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="6808d-127">Microsoft Store apps</span></span>

<span data-ttu-id="6808d-128">Microsoft Store предоставляет ИТ-специалистам и администраторам в Организации возможность находить, принимать, управлять и распространять общедоступные приложения.</span><span class="sxs-lookup"><span data-stu-id="6808d-128">The Microsoft Store provides IT decision-makers and administrators in businesses to find, acquire, manage, and distribute public apps.</span></span>
    
<span data-ttu-id="6808d-129">Это приложение Microsoft Store применимо для следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="6808d-129">This Microsoft Store is applicable for:</span></span> 
* <span data-ttu-id="6808d-130">Только общедоступные приложения</span><span class="sxs-lookup"><span data-stu-id="6808d-130">Public apps only</span></span>
* <span data-ttu-id="6808d-131">Приложения загружаются вручную</span><span class="sxs-lookup"><span data-stu-id="6808d-131">User manually downloads apps</span></span>
* <span data-ttu-id="6808d-132">Автоматическое обновление при подключении к Интернету</span><span class="sxs-lookup"><span data-stu-id="6808d-132">Auto update if connected to Internet</span></span>

<span data-ttu-id="6808d-133">Дополнительные сведения можно найти в [приложениях holographic и магазин](https://docs.microsoft.com/hololens/holographic-store-apps).</span><span class="sxs-lookup"><span data-stu-id="6808d-133">For more information, visit [Holographic Store Apps](https://docs.microsoft.com/hololens/holographic-store-apps).</span></span>

## <span data-ttu-id="6808d-134">Установка через пакеты подготовки</span><span class="sxs-lookup"><span data-stu-id="6808d-134">Install via Provisioning Packages</span></span>

<span data-ttu-id="6808d-135">[Пакеты подготовки](app-deploy-provisioning-package.md) позволяют устанавливать пользовательские или многострочные бизнес-приложения, ПОЗВОЛЯя IT-специалистам и администраторам быстро устанавливать приложения на локальные устройства через USB.</span><span class="sxs-lookup"><span data-stu-id="6808d-135">[Provisioning Packages](app-deploy-provisioning-package.md) allow you to install custom or Line of Business apps, allowing IT pros and administrators to quickly install apps to a local device(s) via USB.</span></span> <span data-ttu-id="6808d-136">Это можно сделать без подключения к Интернету и для какого-либо типа удостоверения.</span><span class="sxs-lookup"><span data-stu-id="6808d-136">This can be done without an internet connection and for any identity type.</span></span>
    
<span data-ttu-id="6808d-137">Установка через пакеты подготовки применима для следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="6808d-137">Installing via Provisioning Packages is applicable for:</span></span> 
* <span data-ttu-id="6808d-138">Бизнеса/собственные приложения (не общедоступные)</span><span class="sxs-lookup"><span data-stu-id="6808d-138">Line of Buisness / Self developed (non-public) apps</span></span>
* <span data-ttu-id="6808d-139">Общедоступные приложения (если доступен автономный установщик)</span><span class="sxs-lookup"><span data-stu-id="6808d-139">Public apps (if offline installer is available)</span></span>
* <span data-ttu-id="6808d-140">USB-Загрузка только на полях</span><span class="sxs-lookup"><span data-stu-id="6808d-140">USB side-load only</span></span>
* <span data-ttu-id="6808d-141">Без автоматического обновления (требуется обновление вручную с помощью пакета подготовки)</span><span class="sxs-lookup"><span data-stu-id="6808d-141">No auto update (requires manual updates via Provisioning Package)</span></span>

## <span data-ttu-id="6808d-142">Установка приложений на HoloLens 2 с помощью установщика приложений</span><span class="sxs-lookup"><span data-stu-id="6808d-142">Install Apps on HoloLens 2 via App Installer</span></span>
<span data-ttu-id="6808d-143">С помощью пользователей [установщика приложений](app-deploy-app-installer.md) можно легко устанавливать приложения на локальные устройства или предоставлять доступ к приложению другим пользователям, которые не знакомы с другими методами установки приложений на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6808d-143">Using the [App Installer](app-deploy-app-installer.md) users can have an experience that is simple for installing Apps on local devices or sharing an app with someone else who is unfamiliar with other app install methods on HoloLens.</span></span> <span data-ttu-id="6808d-144">Это можно сделать без необходимости включать режим разработчика или использовать портал устройств.</span><span class="sxs-lookup"><span data-stu-id="6808d-144">This can be done without needing to enable Developer Mode or use Device Portal.</span></span> <span data-ttu-id="6808d-145">Это простой способ распространения полностью построенного приложения.</span><span class="sxs-lookup"><span data-stu-id="6808d-145">This is a simple method of distributing a completely built app.</span></span> <span data-ttu-id="6808d-146">Независимо от того, требуется ли вам демонстрация приложения для другого пользователя с помощью HoloLens, или вы хотите развернуть приложение, этот метод будет работать легко.</span><span class="sxs-lookup"><span data-stu-id="6808d-146">Regardless of if you simply wish to demo your app to another user with a HoloLens, or you'd like to deploy your app this method works easily.</span></span>

<span data-ttu-id="6808d-147">Установка с помощью установщика приложений применима для следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="6808d-147">Installing via App Installer is applicable for:</span></span> 
* <span data-ttu-id="6808d-148">Бизнеса/собственные приложения (не общедоступные)</span><span class="sxs-lookup"><span data-stu-id="6808d-148">Line of Buisness / Self developed (non-public) apps</span></span>
* <span data-ttu-id="6808d-149">Только для загрузок</span><span class="sxs-lookup"><span data-stu-id="6808d-149">Side-load only</span></span>
* <span data-ttu-id="6808d-150">Не требуется режим разработчика или портал устройств</span><span class="sxs-lookup"><span data-stu-id="6808d-150">Does not require Developer mode or Device portal</span></span>
* <span data-ttu-id="6808d-151">Простота установки конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="6808d-151">Easy for end user to install</span></span>


