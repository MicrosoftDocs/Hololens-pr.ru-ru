---
title: Обзор — Управление приложениями
description: Приступите к работе с обзором управления приложениями смешанной реальности с помощью управления мобильными устройствами, магазина Майкрософт для бизнеса и подготовки пакетов.
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
ms.openlocfilehash: ca87f34718319d489b69ba33ad24731628d87fac
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113635557"
---
# <a name="app-management-overview"></a><span data-ttu-id="55e91-104">Управление приложениями: обзор</span><span class="sxs-lookup"><span data-stu-id="55e91-104">App Management: Overview</span></span>

<span data-ttu-id="55e91-105">вы можете развертывать приложения на четырех разных путях: **управление мобильными устройствами (MDM)**, **Microsoft Store для бизнеса**, **Microsoft Store** или путем их установки с помощью **подготовки**.</span><span class="sxs-lookup"><span data-stu-id="55e91-105">You can deploy apps on four different paths: **Mobile Device Management (MDM)**, **Microsoft Store for Business**, **Microsoft Store**, or by installing them via **Provisioning**.</span></span>

## <a name="mobile-device-management-mdm"></a><span data-ttu-id="55e91-106">Управление мобильными устройствами (MDM)</span><span class="sxs-lookup"><span data-stu-id="55e91-106">Mobile Device Management (MDM)</span></span>

<span data-ttu-id="55e91-107">Решение MDM позволяет руководителям и администраторам в частном порядке устанавливать (отправлять) свои собственные бизнес-приложения или покупать приложения в магазине для группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="55e91-107">An MDM solution enables IT decision-makers and administrators to privately auto-install (push) their in-house, line-of-business apps, or purchase apps through the store for a group of users.</span></span> <span data-ttu-id="55e91-108">HoloLens устройства лучше работают с Microsoft Endpoint Manager (Intune) для [управления приложениями](app-deploy-intune.md).</span><span class="sxs-lookup"><span data-stu-id="55e91-108">HoloLens devices work best with Microsoft Endpoint Manager (Intune) for [application management](app-deploy-intune.md).</span></span> <span data-ttu-id="55e91-109">Intune также предлагает пользователям более детализированный контроль над управляемыми ит-приложениями с помощью Корпоративный портал загружаемого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="55e91-109">Intune also offers users finer-grained control over IT-managed apps through the Company Portal downloadable experience.</span></span>

> [!NOTE]
> <span data-ttu-id="55e91-110">Приведенные ниже инструкции предназначены для пользователей, которым требуется управлять приложениями с помощью Intune.</span><span class="sxs-lookup"><span data-stu-id="55e91-110">The following instructions are for users who want to manage their applications with Intune.</span></span> <span data-ttu-id="55e91-111">Корпорация Майкрософт рекомендует использовать Intune для управления приложениями и устройствами.</span><span class="sxs-lookup"><span data-stu-id="55e91-111">Microsoft recommends using Intune for application and device management.</span></span>

<span data-ttu-id="55e91-112">Управление мобильными устройствами (MDM) применимо для:</span><span class="sxs-lookup"><span data-stu-id="55e91-112">Mobile Device Management (MDM) is applicable for:</span></span>

* <span data-ttu-id="55e91-113">развертывание MDM + Корпоративный портал</span><span class="sxs-lookup"><span data-stu-id="55e91-113">MDM deployed + Company Portal</span></span>
* <span data-ttu-id="55e91-114">Бизнес-приложения (не являющиеся общедоступными)</span><span class="sxs-lookup"><span data-stu-id="55e91-114">Line of Business (non-public) apps</span></span>
* <span data-ttu-id="55e91-115">установка доступных приложений вручную с помощью Корпоративный портал</span><span class="sxs-lookup"><span data-stu-id="55e91-115">Manual installation of available applications through Company Portal</span></span>
* <span data-ttu-id="55e91-116">Принудительная отправка администратором политики MDM</span><span class="sxs-lookup"><span data-stu-id="55e91-116">Admin push through MDM policy</span></span>
* <span data-ttu-id="55e91-117">Автоматическое обновление через MDM</span><span class="sxs-lookup"><span data-stu-id="55e91-117">Auto update through MDM</span></span>

## <a name="microsoft-store-for-business"></a><span data-ttu-id="55e91-118">Microsoft Store для бизнеса</span><span class="sxs-lookup"><span data-stu-id="55e91-118">Microsoft Store for Business</span></span>

<span data-ttu-id="55e91-119">[Microsoft Store для бизнеса](app-deploy-store-business.md) предоставляет ит-специалистам и администраторам в организации возможность поиска, получения и распространения бесплатных и платных приложений, а также управления ими.</span><span class="sxs-lookup"><span data-stu-id="55e91-119">The [Microsoft Store for Business](app-deploy-store-business.md) provides IT decision-makers and administrators in businesses to find, acquire, manage, and distribute free and paid apps.</span></span> <span data-ttu-id="55e91-120">ит-администраторы могут управлять Microsoft Store приложениями и частными бизнес-приложениями в одном модуле инвентаризации, а также назначать и повторно использовать лицензии по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="55e91-120">IT administrators can manage Microsoft Store apps and private line-of-business apps in one inventory, plus assign and reuse licenses as needed.</span></span> <span data-ttu-id="55e91-121">дополнительные сведения см. [в статье предварительные требования для использования Microsoft Store для бизнеса](/microsoft-store/prerequisites-microsoft-store-for-business).</span><span class="sxs-lookup"><span data-stu-id="55e91-121">For more information, visit [Prerequisites for using the Microsoft Store for Business](/microsoft-store/prerequisites-microsoft-store-for-business).</span></span>

<span data-ttu-id="55e91-122">Microsoft Store для бизнеса применимо для:</span><span class="sxs-lookup"><span data-stu-id="55e91-122">The Microsoft Store for Business is applicable for:</span></span>

* <span data-ttu-id="55e91-123">Общедоступные или бизнес-приложения</span><span class="sxs-lookup"><span data-stu-id="55e91-123">Public or Line of Business apps</span></span>
* <span data-ttu-id="55e91-124">Автоматическая установка требуемых приложений с помощью сопоставления MDM</span><span class="sxs-lookup"><span data-stu-id="55e91-124">Automatic installation of required applications through MDM association</span></span>
* <span data-ttu-id="55e91-125">Пользователь загружает приложения вручную</span><span class="sxs-lookup"><span data-stu-id="55e91-125">User manually downloads apps</span></span>
* <span data-ttu-id="55e91-126">Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="55e91-126">Auto Update</span></span>

## <a name="microsoft-store-apps"></a><span data-ttu-id="55e91-127">Приложения Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="55e91-127">Microsoft Store apps</span></span>

<span data-ttu-id="55e91-128">Microsoft Store предоставляет ит-специалистам и администраторам в организации возможность поиска, получения и распространения общедоступных приложений, а также управления ими.</span><span class="sxs-lookup"><span data-stu-id="55e91-128">The Microsoft Store provides IT decision-makers and administrators in businesses to find, acquire, manage, and distribute public apps.</span></span>

<span data-ttu-id="55e91-129">это Microsoft Store применимо для:</span><span class="sxs-lookup"><span data-stu-id="55e91-129">This Microsoft Store is applicable for:</span></span>

* <span data-ttu-id="55e91-130">Только общедоступные приложения</span><span class="sxs-lookup"><span data-stu-id="55e91-130">Public apps only</span></span>
* <span data-ttu-id="55e91-131">Пользователь загружает приложения вручную</span><span class="sxs-lookup"><span data-stu-id="55e91-131">User manually downloads apps</span></span>
* <span data-ttu-id="55e91-132">Автоматическое обновление при подключении к Интернету</span><span class="sxs-lookup"><span data-stu-id="55e91-132">Auto update if connected to Internet</span></span>

<span data-ttu-id="55e91-133">Дополнительные сведения см. на сайте с [приложениями holographic Store](/hololens/holographic-store-apps).</span><span class="sxs-lookup"><span data-stu-id="55e91-133">For more information, visit [Holographic Store Apps](/hololens/holographic-store-apps).</span></span>

## <a name="install-via-provisioning-packages"></a><span data-ttu-id="55e91-134">Установка с помощью пакетов подготовки</span><span class="sxs-lookup"><span data-stu-id="55e91-134">Install via Provisioning Packages</span></span>

<span data-ttu-id="55e91-135">[Пакеты подготовки](app-deploy-provisioning-package.md) позволяют устанавливать настраиваемые или бизнес-приложения, позволяя ИТ-специалистам и администраторам быстро устанавливать приложения на локальные устройства через USB.</span><span class="sxs-lookup"><span data-stu-id="55e91-135">[Provisioning Packages](app-deploy-provisioning-package.md) allow you to install custom or Line of Business apps, allowing IT pros and administrators to quickly install apps to a local device(s) via USB.</span></span> <span data-ttu-id="55e91-136">Эту установку можно выполнить без подключения к Интернету и для любого типа удостоверения.</span><span class="sxs-lookup"><span data-stu-id="55e91-136">This installation can be done without an internet connection and for any identity type.</span></span>

<span data-ttu-id="55e91-137">Установка с помощью пакетов подготовки применима для следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="55e91-137">Installing via Provisioning Packages is applicable for:</span></span>

* <span data-ttu-id="55e91-138">Бизнес-и самостоятельно разработанные (не общедоступные) приложения</span><span class="sxs-lookup"><span data-stu-id="55e91-138">Line of Business / Self-developed (non-public) apps</span></span>
* <span data-ttu-id="55e91-139">Общедоступные приложения (если доступен автономный установщик)</span><span class="sxs-lookup"><span data-stu-id="55e91-139">Public apps (if offline installer is available)</span></span>
* <span data-ttu-id="55e91-140">Только для загрузки с USB</span><span class="sxs-lookup"><span data-stu-id="55e91-140">USB side-loading only</span></span>
* <span data-ttu-id="55e91-141">Без автоматического обновления (требуется обновление вручную с помощью пакета подготовки)</span><span class="sxs-lookup"><span data-stu-id="55e91-141">No auto update (requires manual updates via Provisioning Package)</span></span>

## <a name="install-apps-on-hololens-2-via-app-installer"></a><span data-ttu-id="55e91-142">установка приложений на HoloLens 2 с помощью установщика приложений</span><span class="sxs-lookup"><span data-stu-id="55e91-142">Install Apps on HoloLens 2 via App Installer</span></span>

<span data-ttu-id="55e91-143">С помощью пользователей [установщика приложений](app-deploy-app-installer.md) можно легко устанавливать приложения на локальные устройства или предоставлять общий доступ к приложению другим пользователям, которые не знакомы с другими методами установки приложений на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="55e91-143">Using the [App Installer](app-deploy-app-installer.md) users can have an experience that is simple for installing Apps on local devices or sharing an app with someone else who is unfamiliar with other app install methods on HoloLens.</span></span> <span data-ttu-id="55e91-144">Это можно сделать без необходимости включения режима разработчика или использования портала устройств.</span><span class="sxs-lookup"><span data-stu-id="55e91-144">This can be done without needing to enable Developer Mode or use Device Portal.</span></span> <span data-ttu-id="55e91-145">Это простой способ распространения полностью построенного приложения.</span><span class="sxs-lookup"><span data-stu-id="55e91-145">This is a simple method of distributing a completely built app.</span></span> <span data-ttu-id="55e91-146">независимо от того, хотите ли вы использовать демонстрацию приложения для другого пользователя с HoloLens или хотите развернуть приложение, этот метод работает легко.</span><span class="sxs-lookup"><span data-stu-id="55e91-146">Regardless of if you simply wish to demo your app to another user with a HoloLens, or you'd like to deploy your app this method works easily.</span></span>

<span data-ttu-id="55e91-147">Установка с помощью установщика приложений применима для:</span><span class="sxs-lookup"><span data-stu-id="55e91-147">Installing via App Installer is applicable for:</span></span>

* <span data-ttu-id="55e91-148">Бизнес-и самостоятельно разработанные (не общедоступные) приложения</span><span class="sxs-lookup"><span data-stu-id="55e91-148">Line of Business / Self developed (non-public) apps</span></span>
* <span data-ttu-id="55e91-149">Только загрузка на стороне</span><span class="sxs-lookup"><span data-stu-id="55e91-149">Side-load only</span></span>
* <span data-ttu-id="55e91-150">Не требуется режим разработчика или портал устройств</span><span class="sxs-lookup"><span data-stu-id="55e91-150">Does not require Developer mode or Device portal</span></span>
* <span data-ttu-id="55e91-151">Простота установки конечным пользователем</span><span class="sxs-lookup"><span data-stu-id="55e91-151">Easy for end user to install</span></span>
