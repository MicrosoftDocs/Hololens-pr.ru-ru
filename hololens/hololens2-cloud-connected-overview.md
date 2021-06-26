---
title: Общие сведения о облачном подключении HoloLens 2 с помощью удаленного помощника
description: Узнайте, как регистрировать устройства HoloLens 2 через облачную сеть с помощью удаленного помощника Dynamics 365.
keywords: HoloLens, управление, облачное подключение, удаленное помощник, AAD, Azure AD, MDM, управление мобильными устройствами
author: evmill
ms.author: v-evmill
ms.reviewer: aboeger
ms.date: 12/04/2020
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: a44247b4afea747e4b75c974fcae344380909989
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923539"
---
# <a name="deployment-guide--cloud-connected-hololens-2-with-remote-assist--overview"></a><span data-ttu-id="d38fa-104">Руководство по развертыванию: облачное подключение HoloLens 2 с помощью удаленного помощника — обзор</span><span class="sxs-lookup"><span data-stu-id="d38fa-104">Deployment Guide – Cloud connected HoloLens 2 with Remote Assist – Overview</span></span>

<span data-ttu-id="d38fa-105">Это поможет ИТ-специалистам спланировать и развернуть устройства Microsoft HoloLens 2 с помощью удаленной помощи в Организации.</span><span class="sxs-lookup"><span data-stu-id="d38fa-105">This guide will help IT professionals plan for and deploy Microsoft HoloLens 2 devices with Remote Assist to their organization.</span></span> <span data-ttu-id="d38fa-106">Это будет служить моделью для экспериментальных развертываний в Организации в различных вариантах использования HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="d38fa-106">This will serve as a model for proof-of-concept deployments to your organization across a variety of HoloLens 2 use cases.</span></span> <span data-ttu-id="d38fa-107">Программа установки похожа на [сценарий а. Развертывание в устройства Cloud Connect](https://docs.microsoft.com/hololens/common-scenarios#scenario-a).</span><span class="sxs-lookup"><span data-stu-id="d38fa-107">The setup is similar to [Scenario A: Deploy to cloud connect devices](https://docs.microsoft.com/hololens/common-scenarios#scenario-a).</span></span> 

<span data-ttu-id="d38fa-108">В ходе этого руководства мы рассмотрим, как зарегистрировать устройства в управлении устройствами, применить лицензии по мере необходимости и проверить, что конечные пользователи могут немедленно использовать удаленную помощь после настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="d38fa-108">During the guide, we will cover how to enroll your devices into your device management, apply licenses as needed, and validate that your end users are able to immediately use Remote Assist upon device setup.</span></span> <span data-ttu-id="d38fa-109">Для этого мы относимся к важным аспектам инфраструктуры, необходимым для настройки и выполнения, обеспечивая развертывание в масштабе с помощью HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="d38fa-109">To do this, we will go over the important pieces of infrastructure needed to get set up and running – achieving deployment at scale with HoloLens 2.</span></span> <span data-ttu-id="d38fa-110">В этом пошаговом руководству не будут применяться никакие другие ограничения или конфигурации устройств, но мы рекомендуем изучить эти варианты после завершения.</span><span class="sxs-lookup"><span data-stu-id="d38fa-110">No other device restrictions or configurations will be applied in this guide, however, we encourage you to explore those options after finishing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d38fa-111">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="d38fa-111">Prerequisites</span></span>

<span data-ttu-id="d38fa-112">Для развертывания HoloLens 2 должна быть выполнена следующая инфраструктура.</span><span class="sxs-lookup"><span data-stu-id="d38fa-112">The following infrastructure should be in place in order to deploy the HoloLens 2.</span></span> <span data-ttu-id="d38fa-113">Если нет, то в этом руководство включена настройка Azure и Intune.</span><span class="sxs-lookup"><span data-stu-id="d38fa-113">If not, setting up Azure and Intune is included in this guide:</span></span>

- <span data-ttu-id="d38fa-114">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="d38fa-114">Wi-Fi</span></span>
    - <span data-ttu-id="d38fa-115">Сети обычно открываются в Интернете и в облачных службах.</span><span class="sxs-lookup"><span data-stu-id="d38fa-115">Networks are typically open to the Internet and Cloud services</span></span>
- <span data-ttu-id="d38fa-116">Присоединение Azure Active Directory (Azure AD) с автоматической регистрацией MDM (требуется[Подписка Azure AD P1](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) )</span><span class="sxs-lookup"><span data-stu-id="d38fa-116">Azure Active Directory (Azure AD) Join with MDM Auto Enrollment ([Azure AD P1 subscription](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) needed)</span></span>
- <span data-ttu-id="d38fa-117">Управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="d38fa-117">MDM (Intune) Managed</span></span>
    - <span data-ttu-id="d38fa-118">Одно или несколько приложений развертываются с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="d38fa-118">One or more applications are deployed via MDM.</span></span>
- <span data-ttu-id="d38fa-119">Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="d38fa-119">Users sign in with their own corporate account (Azure AD)</span></span>
    - <span data-ttu-id="d38fa-120">Поддерживается одно или несколько пользователей на каждом устройстве.</span><span class="sxs-lookup"><span data-stu-id="d38fa-120">Single or multiple users per device is supported.</span></span>

:::image type="content" alt-text="Сценарий с подключением к облаку" source="./images/deployment-guides-revised-scenario-a.png" lightbox="./images/deployment-guides-revised-scenario-a.png":::


## <a name="learn-about-remote-assist"></a><span data-ttu-id="d38fa-122">Дополнительные сведения об удаленной помощи</span><span class="sxs-lookup"><span data-stu-id="d38fa-122">Learn about Remote Assist</span></span>

<span data-ttu-id="d38fa-123">Служба удаленного помощника позволяет совместное обслуживание и ремонт, удаленную проверку, а также совместное использование и обучение знаний.</span><span class="sxs-lookup"><span data-stu-id="d38fa-123">Remote Assist allows for collaborative maintenance and repair, remote inspection, as well as knowledge sharing and training.</span></span> <span data-ttu-id="d38fa-124">Подключив людей с разными ролями и расположениями, специалист, использующий удаленную помощь, может подключиться с помощью удаленного участника совместной работы с Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d38fa-124">By connecting people in different roles and locations a technician using Remote Assist can connect with a remote collaborator on Microsoft Teams.</span></span> <span data-ttu-id="d38fa-125">Они могут сочетать видео, снимки экрана и заметки для решения проблем в реальном времени, даже если они недопустимые&#39;t в одном расположении.</span><span class="sxs-lookup"><span data-stu-id="d38fa-125">They can combine video, screenshots, and annotations to solve problems in real time even when they aren&#39;t in the same location.</span></span> <span data-ttu-id="d38fa-126">Удаленные участники совместной работы могут вставлять эталонные изображения, графики и другие полезные сведения, которые обслуживаются техническим&#39;s, чтобы они могли ссылаться на схематическое руководство, а на HoloLens — без участия.</span><span class="sxs-lookup"><span data-stu-id="d38fa-126">Remote collaborators can insert reference images, schematics, and other helpful information the technician&#39;s physical space so they can refer to the schematic while working heads-up and hands-free on HoloLens.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/d3YT8j0yYl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### <a name="remote-assist-licensing-and-requirements"></a><span data-ttu-id="d38fa-127">Лицензирование и требования удаленного помощника</span><span class="sxs-lookup"><span data-stu-id="d38fa-127">Remote Assist Licensing and Requirements</span></span>

- <span data-ttu-id="d38fa-128">Учетная запись Azure AD (требуется для приобретения подписки и назначения лицензий)</span><span class="sxs-lookup"><span data-stu-id="d38fa-128">Azure AD account (required for purchasing the subscription and assigning licenses)</span></span>
- <span data-ttu-id="d38fa-129">[Подписка на удаленную помощь](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist) (или [пробная версия удаленного помощника](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist))</span><span class="sxs-lookup"><span data-stu-id="d38fa-129">[Remote Assist subscription](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist) (or [Remote Assist Trial](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist))</span></span>
    
#### <a name="dynamics-365-remote-assist-user"></a><span data-ttu-id="d38fa-130">Пользователь удаленного помощника Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d38fa-130">Dynamics 365 Remote Assist user</span></span>

- <span data-ttu-id="d38fa-131">Лицензия удаленного помощника</span><span class="sxs-lookup"><span data-stu-id="d38fa-131">Remote Assist license</span></span>
- <span data-ttu-id="d38fa-132">Сетевое подключение</span><span class="sxs-lookup"><span data-stu-id="d38fa-132">Network Connectivity</span></span>

#### <a name="microsoft-teams-user"></a><span data-ttu-id="d38fa-133">Пользователь Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d38fa-133">Microsoft Teams user</span></span>

- <span data-ttu-id="d38fa-134">Microsoft Teams или [Teams условно](https://products.office.com/microsoft-teams/free).</span><span class="sxs-lookup"><span data-stu-id="d38fa-134">Microsoft Teams or [Teams Freemium](https://products.office.com/microsoft-teams/free).</span></span>
- <span data-ttu-id="d38fa-135">Возможность подключения к сети</span><span class="sxs-lookup"><span data-stu-id="d38fa-135">Network connectivity</span></span>

<span data-ttu-id="d38fa-136">Если вы планируете реализовать этот [сценарий для разных клиентов](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants), вам может потребоваться лицензия на информационные барьеры.</span><span class="sxs-lookup"><span data-stu-id="d38fa-136">If you plan on implementing this [cross-tenant scenario](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants), you may need an Information Barriers license.</span></span> <span data-ttu-id="d38fa-137">Ознакомьтесь с [этой статьей](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary) , чтобы определить, требуется ли лицензия на информационный барьер.</span><span class="sxs-lookup"><span data-stu-id="d38fa-137">See [this article](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary) to determine if an Information Barrier License is required.</span></span>

## <a name="in-this-guide-you-will"></a><span data-ttu-id="d38fa-138">В руководстве описаны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d38fa-138">In this guide you will:</span></span>

<span data-ttu-id="d38fa-139">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="d38fa-139">Prepare:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="d38fa-140">Ознакомьтесь с основными сведениями об инфраструктуре для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="d38fa-140">Learn about the infrastructure essentials for HoloLens 2 devices.</span></span>](hololens2-cloud-connected-prepare.md#infrastructure-essentials)
> - [<span data-ttu-id="d38fa-141">Узнайте больше об Azure AD и настройте его, если у вас нет&#39;.</span><span class="sxs-lookup"><span data-stu-id="d38fa-141">Learn more about Azure AD and set up one if you don&#39;t have it.</span></span>](hololens2-cloud-connected-prepare.md#azure-active-directory)
> - [<span data-ttu-id="d38fa-142">Узнайте больше об управлении удостоверениями и о том, как лучше настроить учетные записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d38fa-142">Learn about Identity management and how to best set up Azure AD accounts.</span></span>](hololens2-cloud-connected-prepare.md#identity-management)
> - [<span data-ttu-id="d38fa-143">Узнайте больше о MDM и настройте Intune, если вы не&#39;t уже готовы.</span><span class="sxs-lookup"><span data-stu-id="d38fa-143">Learn more about MDM, and set up with Intune if you don&#39;t already have one ready.</span></span>](hololens2-cloud-connected-prepare.md#mobile-device-management)
> - [<span data-ttu-id="d38fa-144">Узнайте о требованиях к сети удаленного помощника.</span><span class="sxs-lookup"><span data-stu-id="d38fa-144">Learn about the networking requirements of Remote Assist.</span></span>](hololens2-cloud-connected-prepare.md#network)
> - [<span data-ttu-id="d38fa-145">Дополнительно: VPN для подключения к ресурсам Организации</span><span class="sxs-lookup"><span data-stu-id="d38fa-145">Optionally: VPN to connect to organizational resources</span></span>](hololens2-cloud-connected-prepare.md#optional-connect-your-hololens-to-vpn)

<span data-ttu-id="d38fa-146">Настройте следующее.</span><span class="sxs-lookup"><span data-stu-id="d38fa-146">Configure:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="d38fa-147">Создание пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="d38fa-147">How to create Users and Groups.</span></span>](hololens2-cloud-connected-configure.md#azure-users-and-groups)
> - [<span data-ttu-id="d38fa-148">Как настроить автоматическую регистрацию в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d38fa-148">How to set up Auto-enrollment within Azure AD.</span></span>](hololens2-cloud-connected-configure.md#auto-enrollment-on-hololens-2)
> - [<span data-ttu-id="d38fa-149">Как назначить лицензии приложения.</span><span class="sxs-lookup"><span data-stu-id="d38fa-149">How to assign your Application licenses.</span></span>](hololens2-cloud-connected-configure.md#application-licenses)

<span data-ttu-id="d38fa-150">Развертывание.</span><span class="sxs-lookup"><span data-stu-id="d38fa-150">Deploy:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="d38fa-151">Настройте HoloLens 2 и проверьте регистрацию.</span><span class="sxs-lookup"><span data-stu-id="d38fa-151">Set up your HoloLens 2 and validate enrollment.</span></span>](hololens2-cloud-connected-deploy.md#enrollment-validation)
> - [<span data-ttu-id="d38fa-152">Проверьте, можно выполнить удаленный вызов помощника.</span><span class="sxs-lookup"><span data-stu-id="d38fa-152">Validate you can make a Remote Assist call.</span></span>](hololens2-cloud-connected-deploy.md#remote-assist-call-validation)

<span data-ttu-id="d38fa-153">Обслуживание:</span><span class="sxs-lookup"><span data-stu-id="d38fa-153">Maintain:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="d38fa-154">Обновление удаленного помощника с помощью Microsoft Store приложения.</span><span class="sxs-lookup"><span data-stu-id="d38fa-154">How to update Remote Assist using the Microsoft Store app.</span></span>](hololens2-cloud-connected-maintain.md#updates)
> - [<span data-ttu-id="d38fa-155">Создание плана поддержки.</span><span class="sxs-lookup"><span data-stu-id="d38fa-155">Making a support plan.</span></span>](hololens2-cloud-connected-maintain.md#support-plan)
> - [<span data-ttu-id="d38fa-156">План разработки.</span><span class="sxs-lookup"><span data-stu-id="d38fa-156">Development plan.</span></span>](hololens2-cloud-connected-maintain.md#development-plan)

## <a name="next-step"></a><span data-ttu-id="d38fa-157">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="d38fa-157">Next step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d38fa-158">Развертывание с подключением к облаку — подготовка</span><span class="sxs-lookup"><span data-stu-id="d38fa-158">Cloud connected deployment - Prepare</span></span>](hololens2-cloud-connected-prepare.md)

