---
title: Планирование развертывания HoloLens 2 в коммерческой среде
description: Изучите основные потребности в развертывании и управлении HoloLens в корпоративных средах, включая инфраструктуру, Azure Active Directory и управление мобильными устройствами.
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
ms.openlocfilehash: 684059b1ab91860dc6af63cbd6f0927876fefb8c
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112961480"
---
# <a name="planning-hololens-2-deployment-in-a-commercial-environment"></a><span data-ttu-id="ff349-103">Планирование развертывания HoloLens 2 в коммерческой среде</span><span class="sxs-lookup"><span data-stu-id="ff349-103">Planning HoloLens 2 deployment in a commercial environment</span></span>

## <a name="overview"></a><span data-ttu-id="ff349-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="ff349-104">Overview</span></span>
> [!NOTE]
> <span data-ttu-id="ff349-105">Этот обзор предназначен для того, чтобы помочь ИТ-специалистам понять вопросы развертывания устройств Microsoft HoloLens 2 в Организации и управления ими.</span><span class="sxs-lookup"><span data-stu-id="ff349-105">This overview is intended to help IT professionals understand considerations for deploying and managing Microsoft HoloLens 2 devices within an organization.</span></span> <span data-ttu-id="ff349-106">Для конечных пользователей устройств ознакомьтесь с [основами](hololens2-setup.md) , чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="ff349-106">For device end users, see [The Basics](hololens2-setup.md) to get started.</span></span>

<span data-ttu-id="ff349-107">HoloLens 2 работает в Windows 10 holographic, который предоставляет Организации надежные, гибкие, встроенные технологии управления мобильными устройствами и приложениями.</span><span class="sxs-lookup"><span data-stu-id="ff349-107">HoloLens 2 runs on Windows 10 Holographic which provides organizations with robust, flexible, built-in mobile device and app management technologies.</span></span> <span data-ttu-id="ff349-108">Windows 10 holographic поддерживает комплексное управление жизненным циклом устройств для предоставления компаниям контроля над устройствами, данными и приложениями.</span><span class="sxs-lookup"><span data-stu-id="ff349-108">Windows 10 Holographic supports end-to-end device lifecycle management to give companies control over their devices, data, and apps.</span></span> <span data-ttu-id="ff349-109">HoloLens 2 можно легко включить в стандартные методы жизненного цикла, от регистрации устройств, настройки и управления приложениями до обслуживания и прекращения работы с помощью комплексного решения по управлению мобильными устройствами.</span><span class="sxs-lookup"><span data-stu-id="ff349-109">The HoloLens 2 can easily be incorporated into standard lifecycle practices, from device enrollment, configuration, and application management to maintenance and retirement using a comprehensive mobile device management solution.</span></span>

<span data-ttu-id="ff349-110">Следующие шаги помогут вам в процессе внедрения HoloLens 2 в Организации.</span><span class="sxs-lookup"><span data-stu-id="ff349-110">The following steps can help guide you through the process of HoloLens 2 adoption within your organization.</span></span>

| | |
|--|--|
| ![Шаг 1](images/1green.png)| <br/> <span data-ttu-id="ff349-112">**[Распространенные сценарии развертывания](hololens-requirements.md)**. Ознакомьтесь со сценариями развертывания и изучите основные компоненты, необходимые для развертывания устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="ff349-112">**[Common Deployment Scenarios](hololens-requirements.md)**: Understand deployment scenarios and explore the core components needed to deploy HoloLens 2 devices.</span></span> |
| ![Шаг 2](images/2green.png)| <br/> <span data-ttu-id="ff349-114">**[Подготовка](#prepare)**. Познакомьтесь с основными требованиями к инфраструктуре, необходимыми для HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="ff349-114">**[Prepare](#prepare)**: Become familiar with the infrastructure essentials needed for HoloLens 2.</span></span> |
| ![Шаг 3](images/3green.png) | <br/> <span data-ttu-id="ff349-116">**[Настройка](#configure)**: Узнайте, как настроить ключевые компоненты для облачного развертывания.</span><span class="sxs-lookup"><span data-stu-id="ff349-116">**[Configure](#configure)**: Learn how to configure your essential components for a cloud-based deployment.</span></span> |
| ![Шаг 4](images/4green.png) | <br/> <span data-ttu-id="ff349-118">**[Развертывание](#deploy)**: Узнайте, как развертывать устройства и распространять приложения в безопасном и эффективном режиме.</span><span class="sxs-lookup"><span data-stu-id="ff349-118">**[Deploy](#deploy)**: Discover how to deploy your devices and distribute your applications securely and efficiently.</span></span> |
| ![Шаг 5](images/5green.png) | <br/> <span data-ttu-id="ff349-120">**[Обслуживание](#maintain)**. Узнайте, что необходимо для правильного поддержания состояния устройств HoloLens 2 и обеспечения соответствия требованиям корпоративной политики.</span><span class="sxs-lookup"><span data-stu-id="ff349-120">**[Maintain](#maintain)**: Find out what's needed to properly maintain the state of your HoloLens 2 devices and ensure compliance with corporate policy.</span></span> |

## <a name="prepare"></a><span data-ttu-id="ff349-121">Подготовка</span><span class="sxs-lookup"><span data-stu-id="ff349-121">Prepare</span></span>

<span data-ttu-id="ff349-122">Сведения о базовых службах инфраструктуры, необходимых для поддержки полного набора возможностей HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="ff349-122">Learn about essential infrastructure services required to support the full set of HoloLens 2 capabilities.</span></span> 

| <span data-ttu-id="ff349-123">Компонент</span><span class="sxs-lookup"><span data-stu-id="ff349-123">Component</span></span> | <span data-ttu-id="ff349-124">Описание</span><span class="sxs-lookup"><span data-stu-id="ff349-124">Description</span></span> |
|-----------|------------|
| [<span data-ttu-id="ff349-125">Azure AD</span><span class="sxs-lookup"><span data-stu-id="ff349-125">Azure AD</span></span>](hololens-identity.md) | <span data-ttu-id="ff349-126">Предоставляет управление удостоверениями и доступом для HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="ff349-126">Provides identity and access management for the HoloLens 2</span></span>  |
| [<span data-ttu-id="ff349-127">Управление мобильными устройствами (MDM)</span><span class="sxs-lookup"><span data-stu-id="ff349-127">Mobile Device Management</span></span>](hololens-mdm-configure.md)| <span data-ttu-id="ff349-128">Управляет устройствами HoloLens 2, подключенными к вашему клиенту</span><span class="sxs-lookup"><span data-stu-id="ff349-128">Manages HoloLens 2 devices connected to your tenant</span></span>  |
| [<span data-ttu-id="ff349-129">Сеть Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="ff349-129">Wi-Fi Network</span></span>](hololens-commercial-infrastructure.md)| <span data-ttu-id="ff349-130">Доступна Wi-Fi, и устройства могут быть подключены к Интернету.</span><span class="sxs-lookup"><span data-stu-id="ff349-130">Wi-Fi is available and devices can be connected to the Internet</span></span>  |

## <a name="configure"></a><span data-ttu-id="ff349-131">Configure</span><span class="sxs-lookup"><span data-stu-id="ff349-131">Configure</span></span>

<span data-ttu-id="ff349-132">Используйте Intune и автопилотные решения в качестве решений с низкими сенсорами для регистрации и настройки HoloLens 2 в клиенте Azure AD и MDM вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ff349-132">Use Intune and Autopilot as low-touch solutions for enrolling and configuring HoloLens 2 to your organization’s Azure AD tenant and MDM.</span></span>

| <span data-ttu-id="ff349-133">Компонент</span><span class="sxs-lookup"><span data-stu-id="ff349-133">Component</span></span> | <span data-ttu-id="ff349-134">Описание</span><span class="sxs-lookup"><span data-stu-id="ff349-134">Description</span></span> |
|-----------|------------|
| [<span data-ttu-id="ff349-135">Автоматическая регистрация</span><span class="sxs-lookup"><span data-stu-id="ff349-135">Auto Enrollment</span></span>](hololens-enroll-mdm.md#auto-enrollment-in-mdm) | <span data-ttu-id="ff349-136">После первоначального входа устройства автоматически регистрируются в Azure AD и регистрируются в MDM.</span><span class="sxs-lookup"><span data-stu-id="ff349-136">After initial login, devices automatically register with Azure AD and enroll into MDM</span></span>  |
| [<span data-ttu-id="ff349-137">Лицензии приложений</span><span class="sxs-lookup"><span data-stu-id="ff349-137">Application Licenses</span></span>](hololens2-cloud-connected-configure.md#application-licenses)| <span data-ttu-id="ff349-138">Может применяться к пользователям, группам пользователей или группам устройств</span><span class="sxs-lookup"><span data-stu-id="ff349-138">Can be applied to either users, user groups, or device groups</span></span>  |
| [<span data-ttu-id="ff349-139">Пользователи и группы Azure</span><span class="sxs-lookup"><span data-stu-id="ff349-139">Azure Users and Groups</span></span>](hololens2-cloud-connected-configure.md#azure-users-and-groups) | <span data-ttu-id="ff349-140">Помогает назначать конфигурации и лицензии для HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="ff349-140">Helps assign configurations and licenses for the HoloLens 2</span></span>  |

## <a name="deploy"></a><span data-ttu-id="ff349-141">Развернуть</span><span class="sxs-lookup"><span data-stu-id="ff349-141">Deploy</span></span>

<span data-ttu-id="ff349-142">Распределите устройства HoloLens 2 и проверяйте их конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ff349-142">Distribute your HoloLens 2 devices and validate their configuration.</span></span> 

| <span data-ttu-id="ff349-143">Компонент</span><span class="sxs-lookup"><span data-stu-id="ff349-143">Component</span></span> | <span data-ttu-id="ff349-144">Описание</span><span class="sxs-lookup"><span data-stu-id="ff349-144">Description</span></span> |
|-----------|------------|
| [<span data-ttu-id="ff349-145">Проверка регистрации</span><span class="sxs-lookup"><span data-stu-id="ff349-145">Enrollment Validation</span></span>](hololens2-corp-connected-deploy.md#enrollment-validation) | <span data-ttu-id="ff349-146">Проверьте, присоединен ли Azure AD к устройству из параметров или с помощью портала Azure.</span><span class="sxs-lookup"><span data-stu-id="ff349-146">Validate the device has Azure AD Joined from Settings or the Azure Portal</span></span> |
| [<span data-ttu-id="ff349-147">Проверка сертификатов</span><span class="sxs-lookup"><span data-stu-id="ff349-147">Certificate Validation</span></span>](hololens2-corp-connected-deploy.md#wi-fi-certificate-validation) | <span data-ttu-id="ff349-148">Проверьте параметры и проверьте, правильно ли они были распределены.</span><span class="sxs-lookup"><span data-stu-id="ff349-148">Check settings and validate they have been distributed correctly</span></span> |
| [<span data-ttu-id="ff349-149">Проверка установок приложения</span><span class="sxs-lookup"><span data-stu-id="ff349-149">Validate app installs</span></span>](hololens2-corp-connected-deploy.md#validate-lob-app-install) | <span data-ttu-id="ff349-150">Убедитесь, что приложение имеется и работает в HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="ff349-150">Confirm the app is present and working on your HoloLens 2</span></span> |

## <a name="maintain"></a><span data-ttu-id="ff349-151">Техническое обслуживание</span><span class="sxs-lookup"><span data-stu-id="ff349-151">Maintain</span></span>

<span data-ttu-id="ff349-152">Используйте Центр обновления Windows для бизнеса вместе с системой MDM или Microsoft Store, чтобы не обновлять парк HoloLens 2 и приложений.</span><span class="sxs-lookup"><span data-stu-id="ff349-152">Use Windows Update for Business along with your MDM system or the Microsoft Store to keep your fleet of HoloLens 2 and apps updated.</span></span>

| <span data-ttu-id="ff349-153">Компонент</span><span class="sxs-lookup"><span data-stu-id="ff349-153">Component</span></span> | <span data-ttu-id="ff349-154">Описание</span><span class="sxs-lookup"><span data-stu-id="ff349-154">Description</span></span> |
|-----------|------------|
| [<span data-ttu-id="ff349-155">Обновление HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="ff349-155">Update HoloLens 2</span></span>](hololens-updates.md) | <span data-ttu-id="ff349-156">Настройка обновлений по мере необходимости с помощью обновлений Windows для бизнеса</span><span class="sxs-lookup"><span data-stu-id="ff349-156">Configure updates as needed through Windows Updates for Business</span></span> |
| [<span data-ttu-id="ff349-157">Обновление приложений</span><span class="sxs-lookup"><span data-stu-id="ff349-157">Update apps</span></span>](app-deploy-overview.md) | <span data-ttu-id="ff349-158">Настройка с помощью системы MDM или Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="ff349-158">Configure through your MDM system or the Microsoft Store</span></span>
