---
title: Обзор — управление приложениями
description: приложение, управление, управление приложениями
keywords: HoloLens, пользователь, учетная запись, приложение, управление приложениями,
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
ms.openlocfilehash: 2ca0b05b6ed61ddce327a44fedbbcf280b33a106
ms.sourcegitcommit: fc268335e5df529a1cedc2c6b88fa86245fe1b9b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/31/2020
ms.locfileid: "11252670"
---
# <span data-ttu-id="2aa08-104">Управление приложением: обзор</span><span class="sxs-lookup"><span data-stu-id="2aa08-104">App Management: Overview</span></span>

<span data-ttu-id="2aa08-105">Вы можете развернуть приложения по четырем разным путям: управление мобильными устройствами **(MDM),** **Microsoft Store**для бизнеса, **Microsoft Store**или установив их с помощью **программы "Подготовка".**</span><span class="sxs-lookup"><span data-stu-id="2aa08-105">You can deploy apps on four different paths: **Mobile Device Management (MDM)**, **Microsoft Store for Business**, **Microsoft Store**, or by installing them via **Provisioning**.</span></span>

## <span data-ttu-id="2aa08-106">Управление мобильными устройствами (MDM)</span><span class="sxs-lookup"><span data-stu-id="2aa08-106">Mobile Device Management (MDM)</span></span>

<span data-ttu-id="2aa08-107">Решение MDM позволяет ИТ-пользователям и администраторам автоматически устанавливать собственные бизнес-приложения или приобретать приложения через Магазин для группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="2aa08-107">An MDM solution enables IT decision-makers and administrators to privately auto-install (push) their in-house, line-of-business apps, or purchase apps through the store for a group of users.</span></span> <span data-ttu-id="2aa08-108">Устройства HoloLens лучше всего работают с Microsoft Endpoint Manager (Intune) для [управления приложениями.](app-deploy-intune.md)</span><span class="sxs-lookup"><span data-stu-id="2aa08-108">HoloLens devices work best with Microsoft Endpoint Manager (Intune) for [application management](app-deploy-intune.md).</span></span> <span data-ttu-id="2aa08-109">Intune также обеспечивает более точное управление приложениями, управляемыми ИТ-пользователями, с помощью портала компании, который можно загрузить.</span><span class="sxs-lookup"><span data-stu-id="2aa08-109">Intune also offers users finer-grained control over IT-managed apps through the Company Portal downloadable experience.</span></span>

> [!NOTE]
> <span data-ttu-id="2aa08-110">Следующие инструкции для пользователей, которые хотят управлять своими приложениями с помощью Intune.</span><span class="sxs-lookup"><span data-stu-id="2aa08-110">The following instructions are for users who want to manage their applications with Intune.</span></span> <span data-ttu-id="2aa08-111">Корпорация Майкрософт рекомендует использовать Intune для управления приложениями и устройствами.</span><span class="sxs-lookup"><span data-stu-id="2aa08-111">Microsoft recommends using Intune for application and device management.</span></span>

<span data-ttu-id="2aa08-112">Управление мобильными устройствами (MDM) применимо к:</span><span class="sxs-lookup"><span data-stu-id="2aa08-112">Mobile Device Management (MDM) is applicable for:</span></span>

* <span data-ttu-id="2aa08-113">Развернуто MDM + портал компании</span><span class="sxs-lookup"><span data-stu-id="2aa08-113">MDM deployed + Company Portal</span></span>
* <span data-ttu-id="2aa08-114">Бизнес-приложения (не общедоступные)</span><span class="sxs-lookup"><span data-stu-id="2aa08-114">Line of Business (non-public) apps</span></span>
* <span data-ttu-id="2aa08-115">Ручная установка доступных приложений на портале компании</span><span class="sxs-lookup"><span data-stu-id="2aa08-115">Manual installation of available applications through Company Portal</span></span>
* <span data-ttu-id="2aa08-116">Администратор проходит через политику MDM</span><span class="sxs-lookup"><span data-stu-id="2aa08-116">Admin push through MDM policy</span></span>
* <span data-ttu-id="2aa08-117">Автоматическое обновление с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="2aa08-117">Auto update through MDM</span></span>

## <span data-ttu-id="2aa08-118">Microsoft Store для бизнеса</span><span class="sxs-lookup"><span data-stu-id="2aa08-118">Microsoft Store for Business</span></span>

<span data-ttu-id="2aa08-119">[Microsoft Store для бизнеса](app-deploy-store-business.md) предоставляет ИТ-администраторам и ИТ-администраторам в компаниях возможность находить, приобретать и распространять бесплатные и платные приложения, а также управлять ими.</span><span class="sxs-lookup"><span data-stu-id="2aa08-119">The [Microsoft Store for Business](app-deploy-store-business.md) provides IT decision-makers and administrators in businesses to find, acquire, manage, and distribute free and paid apps.</span></span> <span data-ttu-id="2aa08-120">ИТ-администраторы могут управлять приложениями Microsoft Store и частными бизнес-приложениями в одном перечне, а также назначать и повторно использовать лицензии по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="2aa08-120">IT administrators can manage Microsoft Store apps and private line-of-business apps in one inventory, plus assign and reuse licenses as needed.</span></span> <span data-ttu-id="2aa08-121">Дополнительные сведения можно получить на сайте [Prerequisites for using the Microsoft Store for Business.](https://docs.microsoft.com/microsoft-store/prerequisites-microsoft-store-for-business)</span><span class="sxs-lookup"><span data-stu-id="2aa08-121">For more information, visit [Prerequisites for using the Microsoft Store for Business](https://docs.microsoft.com/microsoft-store/prerequisites-microsoft-store-for-business).</span></span>

<span data-ttu-id="2aa08-122">Microsoft Store для бизнеса применим к:</span><span class="sxs-lookup"><span data-stu-id="2aa08-122">The Microsoft Store for Business is applicable for:</span></span>

* <span data-ttu-id="2aa08-123">Общедоступные или бизнес-приложения</span><span class="sxs-lookup"><span data-stu-id="2aa08-123">Public or Line of Business apps</span></span>
* <span data-ttu-id="2aa08-124">Автоматическая установка необходимых приложений с помощью связи mDM</span><span class="sxs-lookup"><span data-stu-id="2aa08-124">Automatic installation of required applications through MDM association</span></span>
* <span data-ttu-id="2aa08-125">Пользователь вручную скачивает приложения</span><span class="sxs-lookup"><span data-stu-id="2aa08-125">User manually downloads apps</span></span>
* <span data-ttu-id="2aa08-126">Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="2aa08-126">Auto Update</span></span>

## <span data-ttu-id="2aa08-127">Приложения Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="2aa08-127">Microsoft Store apps</span></span>

<span data-ttu-id="2aa08-128">Microsoft Store предоставляет ИТ-администраторам и ИТ-администраторам в компаниях возможность находить, приобретать и распространять общедоступные приложения, а также управлять ими.</span><span class="sxs-lookup"><span data-stu-id="2aa08-128">The Microsoft Store provides IT decision-makers and administrators in businesses to find, acquire, manage, and distribute public apps.</span></span>

<span data-ttu-id="2aa08-129">Этот Microsoft Store применим к:</span><span class="sxs-lookup"><span data-stu-id="2aa08-129">This Microsoft Store is applicable for:</span></span>

* <span data-ttu-id="2aa08-130">Только общедоступные приложения</span><span class="sxs-lookup"><span data-stu-id="2aa08-130">Public apps only</span></span>
* <span data-ttu-id="2aa08-131">Пользователь вручную скачивает приложения</span><span class="sxs-lookup"><span data-stu-id="2aa08-131">User manually downloads apps</span></span>
* <span data-ttu-id="2aa08-132">Автоматическое обновление при под подключением к Интернету</span><span class="sxs-lookup"><span data-stu-id="2aa08-132">Auto update if connected to Internet</span></span>

<span data-ttu-id="2aa08-133">Дополнительные сведения см. в [приложениях Магазина Holographic.](https://docs.microsoft.com/hololens/holographic-store-apps)</span><span class="sxs-lookup"><span data-stu-id="2aa08-133">For more information, visit [Holographic Store Apps](https://docs.microsoft.com/hololens/holographic-store-apps).</span></span>

## <span data-ttu-id="2aa08-134">Установка с помощью пакетов подготовка</span><span class="sxs-lookup"><span data-stu-id="2aa08-134">Install via Provisioning Packages</span></span>

<span data-ttu-id="2aa08-135">[Пакеты подготовка](app-deploy-provisioning-package.md) позволяют устанавливать пользовательские или бизнес-приложения, позволяя ИТ-специалисты и администраторам быстро устанавливать приложения на локальные устройства через USB.</span><span class="sxs-lookup"><span data-stu-id="2aa08-135">[Provisioning Packages](app-deploy-provisioning-package.md) allow you to install custom or Line of Business apps, allowing IT pros and administrators to quickly install apps to a local device(s) via USB.</span></span> <span data-ttu-id="2aa08-136">Эту установку можно установить без подключения к Интернету и для любого типа удостоверения.</span><span class="sxs-lookup"><span data-stu-id="2aa08-136">This installation can be done without an internet connection and for any identity type.</span></span>

<span data-ttu-id="2aa08-137">Установка с помощью пакетов подготовка применима к:</span><span class="sxs-lookup"><span data-stu-id="2aa08-137">Installing via Provisioning Packages is applicable for:</span></span>

* <span data-ttu-id="2aa08-138">Бизнес/ самостоятельно разработанные (не общедоступные) приложения</span><span class="sxs-lookup"><span data-stu-id="2aa08-138">Line of Business / Self-developed (non-public) apps</span></span>
* <span data-ttu-id="2aa08-139">Общедоступные приложения (если доступен автономный установщик)</span><span class="sxs-lookup"><span data-stu-id="2aa08-139">Public apps (if offline installer is available)</span></span>
* <span data-ttu-id="2aa08-140">Загрузка только на стороне USB</span><span class="sxs-lookup"><span data-stu-id="2aa08-140">USB side-loading only</span></span>
* <span data-ttu-id="2aa08-141">Автоматическое обновление не требуется (требуется ручное обновление с помощью пакета предоставления)</span><span class="sxs-lookup"><span data-stu-id="2aa08-141">No auto update (requires manual updates via Provisioning Package)</span></span>

## <span data-ttu-id="2aa08-142">Установка приложений на HoloLens 2 с помощью установщика приложений</span><span class="sxs-lookup"><span data-stu-id="2aa08-142">Install Apps on HoloLens 2 via App Installer</span></span>

<span data-ttu-id="2aa08-143">С помощью [установщика](app-deploy-app-installer.md) приложений пользователи могут легко установить приложения на локальных устройствах или поделиться приложением с другими пользователями, не знакомыми с другими методами установки приложений на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="2aa08-143">Using the [App Installer](app-deploy-app-installer.md) users can have an experience that is simple for installing Apps on local devices or sharing an app with someone else who is unfamiliar with other app install methods on HoloLens.</span></span> <span data-ttu-id="2aa08-144">Это можно сделать без необходимости включить режим разработчика или использовать портал устройств.</span><span class="sxs-lookup"><span data-stu-id="2aa08-144">This can be done without needing to enable Developer Mode or use Device Portal.</span></span> <span data-ttu-id="2aa08-145">Это простой способ распространения полностью встроенного приложения.</span><span class="sxs-lookup"><span data-stu-id="2aa08-145">This is a simple method of distributing a completely built app.</span></span> <span data-ttu-id="2aa08-146">Независимо от того, хотите ли вы просто демонстрацию приложения другому пользователю с помощью HoloLens или вы хотите развернуть приложение, этот метод работает легко.</span><span class="sxs-lookup"><span data-stu-id="2aa08-146">Regardless of if you simply wish to demo your app to another user with a HoloLens, or you'd like to deploy your app this method works easily.</span></span>

<span data-ttu-id="2aa08-147">Установка с помощью установщика приложений применима к:</span><span class="sxs-lookup"><span data-stu-id="2aa08-147">Installing via App Installer is applicable for:</span></span>

* <span data-ttu-id="2aa08-148">Бизнес/ Самостоятельно разработанные (не общедоступные) приложения</span><span class="sxs-lookup"><span data-stu-id="2aa08-148">Line of Business / Self developed (non-public) apps</span></span>
* <span data-ttu-id="2aa08-149">Только неогрузка</span><span class="sxs-lookup"><span data-stu-id="2aa08-149">Side-load only</span></span>
* <span data-ttu-id="2aa08-150">Не требуется режим разработчика или портал устройств</span><span class="sxs-lookup"><span data-stu-id="2aa08-150">Does not require Developer mode or Device portal</span></span>
* <span data-ttu-id="2aa08-151">Простое для установки конечным пользователем</span><span class="sxs-lookup"><span data-stu-id="2aa08-151">Easy for end user to install</span></span>
