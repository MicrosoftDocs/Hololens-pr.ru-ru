---
title: Обзор cloud connected HoloLens 2 with Remote Assist
description: Узнайте, как зарегистрировать устройства HoloLens 2 в сети Cloud Connected с помощью удаленной помощи Dynamics 365.
keywords: HoloLens, управление, подключение к облаку, удаленная помощь, AAD, Azure AD, MDM, управление мобильными устройствами
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
ms.openlocfilehash: 69b31657a7efaebd5b25b742023dc8767f9c5038
ms.sourcegitcommit: 39424078a75feaf6a1e9b0547cb7d5de9847faf3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "11312642"
---
# <span data-ttu-id="f3779-104">Руководстве по развертыванию. Подключенные к облаку устройства HoloLens 2 с удаленной поддержкой — обзор</span><span class="sxs-lookup"><span data-stu-id="f3779-104">Deployment Guide – Cloud connected HoloLens 2 with Remote Assist – Overview</span></span>

<span data-ttu-id="f3779-105">Это руководство поможет ИТ-специалистам спланировать и развернуть устройства Microsoft HoloLens 2 в своей организации, чтобы эти устройства были готовы к использованию в облаке организации с помощью удаленной поддержки Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f3779-105">This guide helps IT professionals plan for and deploy Microsoft HoloLens 2 devices to their organization with the overall goal of having those devices cloud connected to your organization with Dynamics 365 Remote Assist ready to use.</span></span> <span data-ttu-id="f3779-106">Помните, что это будет служить моделью для проверки концепции развертывания в организации в различных случаях использования HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="f3779-106">Keep in mind, this will serve as a model for proof-of-concept deployments to your organization across a variety of HoloLens 2 use cases.</span></span>

<span data-ttu-id="f3779-107">В этом руководстве мы охаемся регистрации устройств в управлении устройствами, применяем лицензии по мере необходимости и проверяем, могут ли конечные пользователи сразу использовать удаленную помощь при настройке устройства.</span><span class="sxs-lookup"><span data-stu-id="f3779-107">During the guide we will cover how to enroll your devices into your device management, apply licenses as needed, and validate that your end users are able to immediately use Remote Assist upon device setup.</span></span> <span data-ttu-id="f3779-108">Для этого мы проймем важные элементы инфраструктуры, необходимые для работы и развертывания в масштабе с помощью HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="f3779-108">To do this we will go over the important pieces of infrastructure needed to get set up and running – achieving deployment at scale with HoloLens 2.</span></span>

![Баннер, подключенный к облаку](./images/cloud-connected-hololens-large.png)

## <span data-ttu-id="f3779-110">В этом руководстве</span><span class="sxs-lookup"><span data-stu-id="f3779-110">In this Guide</span></span>

<span data-ttu-id="f3779-111">Цель этого руководства — настройка удаленной помощи в организации на устройствах HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f3779-111">This guide has the specific goal of setting up Remote Assist within your organization on your HoloLens devices.</span></span> <span data-ttu-id="f3779-112">Мы проявим необходимость, необходимую для достижения этой цели.</span><span class="sxs-lookup"><span data-stu-id="f3779-112">We will cover the necessities needed to achieve that goal.</span></span> <span data-ttu-id="f3779-113">Для поддержания фокуса на этой цели будет предварительно выбрана определенная подготовка и конфигурации для оптимизации развертывания или сокращения элементов, необходимых для настройки.</span><span class="sxs-lookup"><span data-stu-id="f3779-113">In order to maintain focus on this goal certain preparation and configurations will be pre-selected in order to optimize for this deployment or to reduce the items needed to configure.</span></span> <span data-ttu-id="f3779-114">Вы будете знать об этих вариантах и сможете настроить развертывание в зависимости от потребностей вашей компании.</span><span class="sxs-lookup"><span data-stu-id="f3779-114">You will be informed of these choices, and can customize your deployment based on your business needs.</span></span>

<span data-ttu-id="f3779-115">Это настройка, аналогичная сценарию [А.](https://docs.microsoft.com/hololens/common-scenarios#scenario-a)Развертывание на устройствах с облачным подключением, что является хорошим вариантом для многих развертывание с проверкой концепции, которое включает в себя:</span><span class="sxs-lookup"><span data-stu-id="f3779-115">This is a set up similar to [Scenario A: Deploy to cloud connect devices](https://docs.microsoft.com/hololens/common-scenarios#scenario-a), which is a good option for many Proof of Concept deployments, which will include:</span></span>

- <span data-ttu-id="f3779-116">Wi-Fi сети обычно полностью открыты для интернета и облачных служб</span><span class="sxs-lookup"><span data-stu-id="f3779-116">Wi-Fi networks are typically fully open to the Internet and Cloud services</span></span>
- <span data-ttu-id="f3779-117">Регистрация в Azure AD с помощью автоматической регистрации MDM — управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="f3779-117">Azure AD Join with MDM Auto Enrollment -- MDM (Intune) Managed</span></span>
- <span data-ttu-id="f3779-118">Вход пользователей с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="f3779-118">Users sign in with their own corporate account (Azure AD)</span></span>
  - <span data-ttu-id="f3779-119">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="f3779-119">Single or multiple users per device supported</span></span>
- <span data-ttu-id="f3779-120">Различные уровни конфигураций блокировки устройств применяются в зависимости от конкретных случаев использования: от "Полностью открыто" до "Терминал с одним приложением"</span><span class="sxs-lookup"><span data-stu-id="f3779-120">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk</span></span>

![Сценарий с подключением к облаку](./images/cloud-connected-guide-diagram.png)

<span data-ttu-id="f3779-122">В этом руководстве не применяются никакие другие ограничения или конфигурации устройств, однако мы рекомендуем изучить эти параметры после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="f3779-122">No other device restrictions or configurations will be applied in this guide, however we encourage you to explore those options after finishing.</span></span>

## <span data-ttu-id="f3779-123">Узнайте об удаленной помощи</span><span class="sxs-lookup"><span data-stu-id="f3779-123">Learn about Remote Assist</span></span>

<span data-ttu-id="f3779-124">Удаленная помощь позволяет совместно использовать обслуживание и восстановление, удаленную проверку, а также обмен знаниями и обучение.</span><span class="sxs-lookup"><span data-stu-id="f3779-124">Remote Assist allows for collaborative maintenance and repair, remote inspection, as well as knowledge sharing and training.</span></span> <span data-ttu-id="f3779-125">Подключая людей в различных ролях и расположениях, специалист с помощью удаленной поддержки может подключаться к удаленному соавтору в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f3779-125">By connecting people in different roles and locations a technician using Remote Assist can connect with a remote collaborator on Microsoft Teams.</span></span> <span data-ttu-id="f3779-126">Они могут комбинировать видео, снимки экрана и аннотации для решения проблем в режиме реального времени, даже если они&#39;в одном расположении.</span><span class="sxs-lookup"><span data-stu-id="f3779-126">They can combine video, screenshots, and annotations to solve problems in real time even when they aren&#39;t in the same location.</span></span> <span data-ttu-id="f3779-127">Удаленные соавторы могут вставлять эталонные образы, схемы и другие полезные сведения, которые техники&#39;физическое пространство, чтобы они могли ссылаться на схему при работе на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f3779-127">Remote collaborators can insert reference images, schematics, and other helpful information the technician&#39;s physical space so they can refer to the schematic while working heads-up and hands-free on HoloLens.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/d3YT8j0yYl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <span data-ttu-id="f3779-128">В этом руководстве вы будете:</span><span class="sxs-lookup"><span data-stu-id="f3779-128">In this guide you will:</span></span>

<span data-ttu-id="f3779-129">Подготовьте:</span><span class="sxs-lookup"><span data-stu-id="f3779-129">Prepare:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="f3779-130">Узнайте об инфраструктуре, необходимой для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="f3779-130">Learn about the infrastructure essentials for HoloLens 2 devices.</span></span>](hololens2-cloud-connected-prepare.md#infrastructure-essentials)
> - [<span data-ttu-id="f3779-131">Узнайте больше об Azure AD и задайте его,&#39;его нет.</span><span class="sxs-lookup"><span data-stu-id="f3779-131">Learn more about Azure AD and set up one if you don&#39;t have it.</span></span>](hololens2-cloud-connected-prepare.md#azure-active-directory)
> - [<span data-ttu-id="f3779-132">Узнайте об управлении удостоверениями и о том, как лучше всего настроить учетные записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f3779-132">Learn about Identity management and how to best set up Azure AD accounts.</span></span>](hololens2-cloud-connected-prepare.md#identity-management)
> - [<span data-ttu-id="f3779-133">Узнайте больше о MDM и настройте Intune, если вы&#39;еще не готовы.</span><span class="sxs-lookup"><span data-stu-id="f3779-133">Learn more about MDM, and set up with Intune if you don&#39;t already have one ready.</span></span>](hololens2-cloud-connected-prepare.md#mobile-device-management)
> - [<span data-ttu-id="f3779-134">Узнайте о сетевых требованиях удаленной помощи.</span><span class="sxs-lookup"><span data-stu-id="f3779-134">Learn about the networking requirements of Remote Assist.</span></span>](hololens2-cloud-connected-prepare.md#network)
> - [<span data-ttu-id="f3779-135">Необязательно: VPN для подключения к ресурсам организации</span><span class="sxs-lookup"><span data-stu-id="f3779-135">Optionally: VPN to connect to organizational resources</span></span>](/hololens2-cloud-connected-prepare.md#optional-connect-your-hololens-to-vpn)

<span data-ttu-id="f3779-136">Настройте:</span><span class="sxs-lookup"><span data-stu-id="f3779-136">Configure:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="f3779-137">Создание пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="f3779-137">How to create Users and Groups.</span></span>](hololens2-cloud-connected-configure.md#azure-users-and-groups)
> - [<span data-ttu-id="f3779-138">Настройка автоматической регистрации в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f3779-138">How to set up Auto-enrollment within Azure AD.</span></span>](hololens2-cloud-connected-configure.md#auto-enrollment-on-hololens-2)
> - [<span data-ttu-id="f3779-139">Назначение лицензий на приложения.</span><span class="sxs-lookup"><span data-stu-id="f3779-139">How to assign your Application licenses.</span></span>](hololens2-cloud-connected-configure.md#application-licenses)

<span data-ttu-id="f3779-140">Развернем:</span><span class="sxs-lookup"><span data-stu-id="f3779-140">Deploy:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="f3779-141">Настройка HoloLens 2 и проверка регистрации.</span><span class="sxs-lookup"><span data-stu-id="f3779-141">Set up your HoloLens 2 and validate enrollment.</span></span>](hololens2-cloud-connected-deploy.md#enrollment-validation)
> - [<span data-ttu-id="f3779-142">Убедитесь, что вы можете сделать вызов удаленной помощи.</span><span class="sxs-lookup"><span data-stu-id="f3779-142">Validate you can make a Remote Assist call.</span></span>](hololens2-cloud-connected-deploy.md#remote-assist-call-validation)

<span data-ttu-id="f3779-143">Обслуживание:</span><span class="sxs-lookup"><span data-stu-id="f3779-143">Maintain:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="f3779-144">Обновление удаленной поддержки с помощью приложения Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f3779-144">How to update Remote Assist using the Microsoft Store app.</span></span>](hololens2-cloud-connected-maintain.md#updates)
> - [<span data-ttu-id="f3779-145">Создание плана поддержки.</span><span class="sxs-lookup"><span data-stu-id="f3779-145">Making a support plan.</span></span>](hololens2-cloud-connected-maintain.md#support-plan)
> - [<span data-ttu-id="f3779-146">План разработки.</span><span class="sxs-lookup"><span data-stu-id="f3779-146">Development plan.</span></span>](hololens2-cloud-connected-maintain.md#development-plan)

## <span data-ttu-id="f3779-147">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="f3779-147">Next step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="f3779-148">Развертывание с подключением к облаку — подготовка</span><span class="sxs-lookup"><span data-stu-id="f3779-148">Cloud connected deployment - Prepare</span></span>](hololens2-cloud-connected-prepare.md)

