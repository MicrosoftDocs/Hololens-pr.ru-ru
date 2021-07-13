---
title: Планирование развертывания HoloLens 2 в коммерческой среде
description: изучите основные потребности развертывания и управления HoloLens в корпоративных средах, включая инфраструктуру, azure active directory и управление мобильными устройствами.
ms.prod: hololens
ms.sitesec: library
ms.assetid: 88bf50aa-0bac-4142-afa4-20b37c013001
author: joyjaz
ms.author: v-jjaswinski
audience: ITPro
ms.topic: article
ms.localizationpriority: medium
ms.date: 05/21/2021
appliesto:
- HoloLens 2
ms.openlocfilehash: 2fb58345f623a0b70c1fda10b9fb550de70f4c6d
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113635795"
---
# <a name="planning-hololens-2-deployment-in-a-commercial-environment"></a><span data-ttu-id="1fca7-103">Планирование развертывания HoloLens 2 в коммерческой среде</span><span class="sxs-lookup"><span data-stu-id="1fca7-103">Planning HoloLens 2 deployment in a commercial environment</span></span>

## <a name="overview"></a><span data-ttu-id="1fca7-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="1fca7-104">Overview</span></span>
> [!NOTE]
> <span data-ttu-id="1fca7-105">этот обзор предназначен для того, чтобы помочь ит-специалистам в понимании вопросов развертывания и управления устройствами Microsoft HoloLens 2 в организации.</span><span class="sxs-lookup"><span data-stu-id="1fca7-105">This overview is intended to help IT professionals understand considerations for deploying and managing Microsoft HoloLens 2 devices within an organization.</span></span> <span data-ttu-id="1fca7-106">сведения для конечных пользователей устройств см. в статье [подготовка HoloLens 2 к использованию](hololens2-setup.md) для начала работы.</span><span class="sxs-lookup"><span data-stu-id="1fca7-106">For device end users, see [Get your HoloLens 2 ready to use](hololens2-setup.md) to get started.</span></span>

<span data-ttu-id="1fca7-107">HoloLens 2 работает на Windows 10 Holographic, который предоставляет организации надежные, гибкие, встроенные технологии управления мобильными устройствами и приложениями.</span><span class="sxs-lookup"><span data-stu-id="1fca7-107">HoloLens 2 runs on Windows 10 Holographic which provides organizations with robust, flexible, built-in mobile device and app management technologies.</span></span> <span data-ttu-id="1fca7-108">Windows 10 Holographic поддерживает комплексное управление жизненным циклом устройств для предоставления компаниям контроля над устройствами, данными и приложениями.</span><span class="sxs-lookup"><span data-stu-id="1fca7-108">Windows 10 Holographic supports end-to-end device lifecycle management to give companies control over their devices, data, and apps.</span></span> <span data-ttu-id="1fca7-109">HoloLens 2 можно легко включить в стандартные методы жизненного цикла, от регистрации устройств, настройки и управления приложениями до обслуживания и прекращения использования с помощью комплексного решения по управлению мобильными устройствами.</span><span class="sxs-lookup"><span data-stu-id="1fca7-109">The HoloLens 2 can easily be incorporated into standard lifecycle practices, from device enrollment, configuration, and application management to maintenance and retirement using a comprehensive mobile device management solution.</span></span>

<span data-ttu-id="1fca7-110">следующие шаги и видео помогут вам в процессе HoloLens 2 внедрения в организации.</span><span class="sxs-lookup"><span data-stu-id="1fca7-110">The following steps and video can help guide you through the process of HoloLens 2 adoption within your organization.</span></span>

| | |
|--|--|
| ![Шаг 1](images/1green.png)| <br/> <span data-ttu-id="1fca7-112">**[распространенные сценарии развертывания](hololens-requirements.md)**. ознакомьтесь со сценариями развертывания и изучите основные компоненты, необходимые для развертывания HoloLens 2 устройств.</span><span class="sxs-lookup"><span data-stu-id="1fca7-112">**[Common Deployment Scenarios](hololens-requirements.md)**: Understand deployment scenarios and explore the core components needed to deploy HoloLens 2 devices.</span></span> |
| ![Шаг 2](images/2green.png)| <br/> <span data-ttu-id="1fca7-114">**[Подготовка](#prepare)**. Ознакомьтесь с основными требованиями к инфраструктуре, необходимыми для HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="1fca7-114">**[Prepare](#prepare)**: Become familiar with the infrastructure essentials needed for HoloLens 2.</span></span> |
| ![Шаг 3](images/3green.png) | <br/> <span data-ttu-id="1fca7-116">**[Настройка](#configure)**: Узнайте, как настроить ключевые компоненты для облачного развертывания.</span><span class="sxs-lookup"><span data-stu-id="1fca7-116">**[Configure](#configure)**: Learn how to configure your essential components for a cloud-based deployment.</span></span> |
| ![Шаг 4](images/4green.png) | <br/> <span data-ttu-id="1fca7-118">**[Развертывание](#deploy)**: Узнайте, как развертывать устройства и распространять приложения в безопасном и эффективном режиме.</span><span class="sxs-lookup"><span data-stu-id="1fca7-118">**[Deploy](#deploy)**: Discover how to deploy your devices and distribute your applications securely and efficiently.</span></span> |
| ![Шаг 5](images/5green.png) | <br/> <span data-ttu-id="1fca7-120">**[обслуживание](#maintain)**. узнайте, что необходимо для правильного поддержания состояния устройств HoloLens 2 и обеспечения соответствия требованиям корпоративной политики.</span><span class="sxs-lookup"><span data-stu-id="1fca7-120">**[Maintain](#maintain)**: Find out what's needed to properly maintain the state of your HoloLens 2 devices and ensure compliance with corporate policy.</span></span> |

> [!VIDEO https://channel9.msdn.com/Shows/IT-Ops-Talk/HoloLens-2-Deployment-Overview/player]

## <a name="prepare"></a><span data-ttu-id="1fca7-121">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="1fca7-121">Prepare</span></span>

<span data-ttu-id="1fca7-122">узнайте о необходимых службах инфраструктуры, необходимых для поддержки полного набора возможностей HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="1fca7-122">Learn about essential infrastructure services required to support the full set of HoloLens 2 capabilities.</span></span> 

| <span data-ttu-id="1fca7-123">Компонент</span><span class="sxs-lookup"><span data-stu-id="1fca7-123">Component</span></span> | <span data-ttu-id="1fca7-124">Описание</span><span class="sxs-lookup"><span data-stu-id="1fca7-124">Description</span></span> |
|-----------|------------|
| [<span data-ttu-id="1fca7-125">Azure AD</span><span class="sxs-lookup"><span data-stu-id="1fca7-125">Azure AD</span></span>](hololens-identity.md) | <span data-ttu-id="1fca7-126">Предоставляет управление удостоверениями и доступом для HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="1fca7-126">Provides identity and access management for the HoloLens 2</span></span>  |
| [<span data-ttu-id="1fca7-127">Управление мобильными устройствами (MDM)</span><span class="sxs-lookup"><span data-stu-id="1fca7-127">Mobile Device Management</span></span>](hololens-mdm-configure.md)| <span data-ttu-id="1fca7-128">управляет HoloLens 2 устройствами, подключенными к клиенту</span><span class="sxs-lookup"><span data-stu-id="1fca7-128">Manages HoloLens 2 devices connected to your tenant</span></span>  |
| [<span data-ttu-id="1fca7-129">Сеть Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="1fca7-129">Wi-Fi Network</span></span>](hololens-commercial-infrastructure.md)| <span data-ttu-id="1fca7-130">Доступна Wi-Fi, и устройства могут быть подключены к Интернету.</span><span class="sxs-lookup"><span data-stu-id="1fca7-130">Wi-Fi is available and devices can be connected to the Internet</span></span>  |

## <a name="configure"></a><span data-ttu-id="1fca7-131">Configure</span><span class="sxs-lookup"><span data-stu-id="1fca7-131">Configure</span></span>

<span data-ttu-id="1fca7-132">используйте Intune и автопилотные решения в качестве решений с низкими сенсорами для регистрации и настройки HoloLens 2 в клиенте Azure AD и MDM вашей организации.</span><span class="sxs-lookup"><span data-stu-id="1fca7-132">Use Intune and Autopilot as low-touch solutions for enrolling and configuring HoloLens 2 to your organization’s Azure AD tenant and MDM.</span></span>

| <span data-ttu-id="1fca7-133">Компонент</span><span class="sxs-lookup"><span data-stu-id="1fca7-133">Component</span></span> | <span data-ttu-id="1fca7-134">Описание</span><span class="sxs-lookup"><span data-stu-id="1fca7-134">Description</span></span> |
|-----------|------------|
| [<span data-ttu-id="1fca7-135">Автоматическая регистрация</span><span class="sxs-lookup"><span data-stu-id="1fca7-135">Auto Enrollment</span></span>](hololens-enroll-mdm.md#auto-enrollment-in-mdm) | <span data-ttu-id="1fca7-136">После первоначального входа устройства автоматически регистрируются в Azure AD и регистрируются в MDM.</span><span class="sxs-lookup"><span data-stu-id="1fca7-136">After initial login, devices automatically register with Azure AD and enroll into MDM</span></span>  |
| [<span data-ttu-id="1fca7-137">Лицензии приложений</span><span class="sxs-lookup"><span data-stu-id="1fca7-137">Application Licenses</span></span>](hololens2-cloud-connected-configure.md#application-licenses)| <span data-ttu-id="1fca7-138">Может применяться к пользователям, группам пользователей или группам устройств</span><span class="sxs-lookup"><span data-stu-id="1fca7-138">Can be applied to either users, user groups, or device groups</span></span>  |
| [<span data-ttu-id="1fca7-139">Пользователи и группы Azure</span><span class="sxs-lookup"><span data-stu-id="1fca7-139">Azure Users and Groups</span></span>](hololens2-cloud-connected-configure.md#azure-users-and-groups) | <span data-ttu-id="1fca7-140">Помогает назначать конфигурации и лицензии для HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="1fca7-140">Helps assign configurations and licenses for the HoloLens 2</span></span>  |

## <a name="deploy"></a><span data-ttu-id="1fca7-141">Развертывание</span><span class="sxs-lookup"><span data-stu-id="1fca7-141">Deploy</span></span>

<span data-ttu-id="1fca7-142">распространение устройств HoloLens 2 и проверка их конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1fca7-142">Distribute your HoloLens 2 devices and validate their configuration.</span></span> 

| <span data-ttu-id="1fca7-143">Компонент</span><span class="sxs-lookup"><span data-stu-id="1fca7-143">Component</span></span> | <span data-ttu-id="1fca7-144">Описание</span><span class="sxs-lookup"><span data-stu-id="1fca7-144">Description</span></span> |
|-----------|------------|
| [<span data-ttu-id="1fca7-145">Проверка регистрации</span><span class="sxs-lookup"><span data-stu-id="1fca7-145">Enrollment Validation</span></span>](hololens2-corp-connected-deploy.md#enrollment-validation) | <span data-ttu-id="1fca7-146">проверьте, присоединен ли к устройству azure AD из Параметры или с помощью портала azure.</span><span class="sxs-lookup"><span data-stu-id="1fca7-146">Validate the device has Azure AD Joined from Settings or the Azure Portal</span></span> |
| [<span data-ttu-id="1fca7-147">Проверка сертификатов</span><span class="sxs-lookup"><span data-stu-id="1fca7-147">Certificate Validation</span></span>](hololens2-corp-connected-deploy.md#wi-fi-certificate-validation) | <span data-ttu-id="1fca7-148">Проверьте параметры и проверьте, правильно ли они были распределены.</span><span class="sxs-lookup"><span data-stu-id="1fca7-148">Check settings and validate they have been distributed correctly</span></span> |
| [<span data-ttu-id="1fca7-149">Проверка установок приложения</span><span class="sxs-lookup"><span data-stu-id="1fca7-149">Validate app installs</span></span>](hololens2-corp-connected-deploy.md#validate-lob-app-install) | <span data-ttu-id="1fca7-150">Убедитесь, что приложение имеется и работает на HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="1fca7-150">Confirm the app is present and working on your HoloLens 2</span></span> |

## <a name="maintain"></a><span data-ttu-id="1fca7-151">Техническое обслуживание</span><span class="sxs-lookup"><span data-stu-id="1fca7-151">Maintain</span></span>

<span data-ttu-id="1fca7-152">используйте Центр обновления Windows для бизнеса вместе с системой MDM или Microsoft Store для обновления HoloLens 2 и приложений.</span><span class="sxs-lookup"><span data-stu-id="1fca7-152">Use Windows Update for Business along with your MDM system or the Microsoft Store to keep your fleet of HoloLens 2 and apps updated.</span></span>

| <span data-ttu-id="1fca7-153">Компонент</span><span class="sxs-lookup"><span data-stu-id="1fca7-153">Component</span></span> | <span data-ttu-id="1fca7-154">Описание</span><span class="sxs-lookup"><span data-stu-id="1fca7-154">Description</span></span> |
|-----------|------------|
| [<span data-ttu-id="1fca7-155">Обновление HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="1fca7-155">Update HoloLens 2</span></span>](hololens-updates.md) | <span data-ttu-id="1fca7-156">настройка обновлений по мере необходимости с помощью Windows обновлений для бизнеса</span><span class="sxs-lookup"><span data-stu-id="1fca7-156">Configure updates as needed through Windows Updates for Business</span></span> |
| [<span data-ttu-id="1fca7-157">Обновление приложений</span><span class="sxs-lookup"><span data-stu-id="1fca7-157">Update apps</span></span>](app-deploy-overview.md) | <span data-ttu-id="1fca7-158">Настройка с помощью системы MDM или Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="1fca7-158">Configure through your MDM system or the Microsoft Store</span></span>
