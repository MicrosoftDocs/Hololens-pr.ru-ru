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
ms.openlocfilehash: 69b31657a7efaebd5b25b742023dc8767f9c5038
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309110"
---
# <a name="deployment-guide--cloud-connected-hololens-2-with-remote-assist--overview"></a><span data-ttu-id="839c3-104">Руководство по развертыванию: облачное подключение HoloLens 2 с помощью удаленного помощника — обзор</span><span class="sxs-lookup"><span data-stu-id="839c3-104">Deployment Guide – Cloud connected HoloLens 2 with Remote Assist – Overview</span></span>

<span data-ttu-id="839c3-105">Это пошаговое руководством помогает ИТ-специалистам планировать и развертывать устройства Microsoft HoloLens 2 в своей организации с общей целью использования облачных устройств, подключенных к вашей организации, с помощью удаленного помощника Dynamics 365, готового к использованию.</span><span class="sxs-lookup"><span data-stu-id="839c3-105">This guide helps IT professionals plan for and deploy Microsoft HoloLens 2 devices to their organization with the overall goal of having those devices cloud connected to your organization with Dynamics 365 Remote Assist ready to use.</span></span> <span data-ttu-id="839c3-106">Помните, что это будет служить моделью для экспериментальных развертываний в вашей организации в различных вариантах использования HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="839c3-106">Keep in mind, this will serve as a model for proof-of-concept deployments to your organization across a variety of HoloLens 2 use cases.</span></span>

<span data-ttu-id="839c3-107">В рамках руководства мы рассмотрим, как зарегистрировать устройства в управлении устройствами, применить лицензии по мере необходимости и проверить, что конечные пользователи могут немедленно использовать удаленную помощь после настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="839c3-107">During the guide we will cover how to enroll your devices into your device management, apply licenses as needed, and validate that your end users are able to immediately use Remote Assist upon device setup.</span></span> <span data-ttu-id="839c3-108">Для этого мы рассмотрим важные компоненты инфраструктуры, необходимые для настройки и запуска, обеспечивая развертывание в масштабе с помощью HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="839c3-108">To do this we will go over the important pieces of infrastructure needed to get set up and running – achieving deployment at scale with HoloLens 2.</span></span>

![Баннер с подключением к облаку](./images/cloud-connected-hololens-large.png)

## <a name="in-this-guide"></a><span data-ttu-id="839c3-110">В этом руководстве</span><span class="sxs-lookup"><span data-stu-id="839c3-110">In this Guide</span></span>

<span data-ttu-id="839c3-111">В этом руководством содержится конкретная цель настройки удаленного помощника в Организации на устройствах HoloLens.</span><span class="sxs-lookup"><span data-stu-id="839c3-111">This guide has the specific goal of setting up Remote Assist within your organization on your HoloLens devices.</span></span> <span data-ttu-id="839c3-112">Мы рассмотрим необходимые условия, необходимые для достижения этой цели.</span><span class="sxs-lookup"><span data-stu-id="839c3-112">We will cover the necessities needed to achieve that goal.</span></span> <span data-ttu-id="839c3-113">Чтобы поддерживать основное внимание на этой цели, необходимо предварительно выбрать определенную подготовку и конфигурации, чтобы оптимизировать это развертывание или уменьшить количество элементов, необходимых для настройки.</span><span class="sxs-lookup"><span data-stu-id="839c3-113">In order to maintain focus on this goal certain preparation and configurations will be pre-selected in order to optimize for this deployment or to reduce the items needed to configure.</span></span> <span data-ttu-id="839c3-114">Вы будете уведомлены об этих вариантах и можете настроить развертывание в соответствии с потребностями бизнеса.</span><span class="sxs-lookup"><span data-stu-id="839c3-114">You will be informed of these choices, and can customize your deployment based on your business needs.</span></span>

<span data-ttu-id="839c3-115">Это настройка аналогична [сценарию а: развертывание в Cloud Connect Devices](https://docs.microsoft.com/hololens/common-scenarios#scenario-a), что является хорошим вариантом для многих развертываний экспериментов, которые будут включать:</span><span class="sxs-lookup"><span data-stu-id="839c3-115">This is a set up similar to [Scenario A: Deploy to cloud connect devices](https://docs.microsoft.com/hololens/common-scenarios#scenario-a), which is a good option for many Proof of Concept deployments, which will include:</span></span>

- <span data-ttu-id="839c3-116">Обычно Wi-Fi сети полностью открыты для Интернета и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="839c3-116">Wi-Fi networks are typically fully open to the Internet and Cloud services</span></span>
- <span data-ttu-id="839c3-117">Присоединение к Azure AD с автоматической регистрацией MDM — управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="839c3-117">Azure AD Join with MDM Auto Enrollment -- MDM (Intune) Managed</span></span>
- <span data-ttu-id="839c3-118">Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="839c3-118">Users sign in with their own corporate account (Azure AD)</span></span>
  - <span data-ttu-id="839c3-119">Поддерживается один или несколько пользователей на устройство</span><span class="sxs-lookup"><span data-stu-id="839c3-119">Single or multiple users per device supported</span></span>
- <span data-ttu-id="839c3-120">Различные уровни конфигурации блокировки устройств применяются на основе конкретных вариантов использования: от полного открытия до одного киоска приложений</span><span class="sxs-lookup"><span data-stu-id="839c3-120">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk</span></span>

![Сценарий с подключением к облаку](./images/cloud-connected-guide-diagram.png)

<span data-ttu-id="839c3-122">В этом пошаговом руководству не будут применяться никакие другие ограничения или конфигурации устройств, но мы рекомендуем изучить эти варианты после завершения.</span><span class="sxs-lookup"><span data-stu-id="839c3-122">No other device restrictions or configurations will be applied in this guide, however we encourage you to explore those options after finishing.</span></span>

## <a name="learn-about-remote-assist"></a><span data-ttu-id="839c3-123">Дополнительные сведения об удаленной помощи</span><span class="sxs-lookup"><span data-stu-id="839c3-123">Learn about Remote Assist</span></span>

<span data-ttu-id="839c3-124">Служба удаленного помощника позволяет совместное обслуживание и ремонт, удаленную проверку, а также совместное использование и обучение знаний.</span><span class="sxs-lookup"><span data-stu-id="839c3-124">Remote Assist allows for collaborative maintenance and repair, remote inspection, as well as knowledge sharing and training.</span></span> <span data-ttu-id="839c3-125">Подключив людей с разными ролями и расположениями, специалист, использующий удаленную помощь, может подключиться с помощью удаленного участника совместной работы с Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="839c3-125">By connecting people in different roles and locations a technician using Remote Assist can connect with a remote collaborator on Microsoft Teams.</span></span> <span data-ttu-id="839c3-126">Они могут сочетать видео, снимки экрана и заметки для решения проблем в реальном времени, даже если они недопустимые&#39;t в одном расположении.</span><span class="sxs-lookup"><span data-stu-id="839c3-126">They can combine video, screenshots, and annotations to solve problems in real time even when they aren&#39;t in the same location.</span></span> <span data-ttu-id="839c3-127">Удаленные участники совместной работы могут вставлять эталонные изображения, графики и другие полезные сведения, которые обслуживаются техническим&#39;s, чтобы они могли ссылаться на схематическое руководство, а на HoloLens — без участия.</span><span class="sxs-lookup"><span data-stu-id="839c3-127">Remote collaborators can insert reference images, schematics, and other helpful information the technician&#39;s physical space so they can refer to the schematic while working heads-up and hands-free on HoloLens.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/d3YT8j0yYl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <a name="in-this-guide-you-will"></a><span data-ttu-id="839c3-128">В руководстве описаны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="839c3-128">In this guide you will:</span></span>

<span data-ttu-id="839c3-129">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="839c3-129">Prepare:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="839c3-130">Ознакомьтесь с основными сведениями об инфраструктуре для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="839c3-130">Learn about the infrastructure essentials for HoloLens 2 devices.</span></span>](hololens2-cloud-connected-prepare.md#infrastructure-essentials)
> - [<span data-ttu-id="839c3-131">Узнайте больше об Azure AD и настройте его, если у вас нет&#39;.</span><span class="sxs-lookup"><span data-stu-id="839c3-131">Learn more about Azure AD and set up one if you don&#39;t have it.</span></span>](hololens2-cloud-connected-prepare.md#azure-active-directory)
> - [<span data-ttu-id="839c3-132">Узнайте больше об управлении удостоверениями и о том, как лучше настроить учетные записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="839c3-132">Learn about Identity management and how to best set up Azure AD accounts.</span></span>](hololens2-cloud-connected-prepare.md#identity-management)
> - [<span data-ttu-id="839c3-133">Узнайте больше о MDM и настройте Intune, если вы не&#39;t уже готовы.</span><span class="sxs-lookup"><span data-stu-id="839c3-133">Learn more about MDM, and set up with Intune if you don&#39;t already have one ready.</span></span>](hololens2-cloud-connected-prepare.md#mobile-device-management)
> - [<span data-ttu-id="839c3-134">Узнайте о требованиях к сети удаленного помощника.</span><span class="sxs-lookup"><span data-stu-id="839c3-134">Learn about the networking requirements of Remote Assist.</span></span>](hololens2-cloud-connected-prepare.md#network)
> - [<span data-ttu-id="839c3-135">Дополнительно: VPN для подключения к ресурсам Организации</span><span class="sxs-lookup"><span data-stu-id="839c3-135">Optionally: VPN to connect to organizational resources</span></span>](/hololens2-cloud-connected-prepare.md#optional-connect-your-hololens-to-vpn)

<span data-ttu-id="839c3-136">Настройте следующее.</span><span class="sxs-lookup"><span data-stu-id="839c3-136">Configure:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="839c3-137">Создание пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="839c3-137">How to create Users and Groups.</span></span>](hololens2-cloud-connected-configure.md#azure-users-and-groups)
> - [<span data-ttu-id="839c3-138">Как настроить автоматическую регистрацию в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="839c3-138">How to set up Auto-enrollment within Azure AD.</span></span>](hololens2-cloud-connected-configure.md#auto-enrollment-on-hololens-2)
> - [<span data-ttu-id="839c3-139">Как назначить лицензии приложения.</span><span class="sxs-lookup"><span data-stu-id="839c3-139">How to assign your Application licenses.</span></span>](hololens2-cloud-connected-configure.md#application-licenses)

<span data-ttu-id="839c3-140">Развертывание.</span><span class="sxs-lookup"><span data-stu-id="839c3-140">Deploy:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="839c3-141">Настройте HoloLens 2 и проверьте регистрацию.</span><span class="sxs-lookup"><span data-stu-id="839c3-141">Set up your HoloLens 2 and validate enrollment.</span></span>](hololens2-cloud-connected-deploy.md#enrollment-validation)
> - [<span data-ttu-id="839c3-142">Проверьте, можно выполнить удаленный вызов помощника.</span><span class="sxs-lookup"><span data-stu-id="839c3-142">Validate you can make a Remote Assist call.</span></span>](hololens2-cloud-connected-deploy.md#remote-assist-call-validation)

<span data-ttu-id="839c3-143">Обслуживание:</span><span class="sxs-lookup"><span data-stu-id="839c3-143">Maintain:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="839c3-144">Обновление удаленного помощника с помощью Microsoft Store приложения.</span><span class="sxs-lookup"><span data-stu-id="839c3-144">How to update Remote Assist using the Microsoft Store app.</span></span>](hololens2-cloud-connected-maintain.md#updates)
> - [<span data-ttu-id="839c3-145">Создание плана поддержки.</span><span class="sxs-lookup"><span data-stu-id="839c3-145">Making a support plan.</span></span>](hololens2-cloud-connected-maintain.md#support-plan)
> - [<span data-ttu-id="839c3-146">План разработки.</span><span class="sxs-lookup"><span data-stu-id="839c3-146">Development plan.</span></span>](hololens2-cloud-connected-maintain.md#development-plan)

## <a name="next-step"></a><span data-ttu-id="839c3-147">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="839c3-147">Next step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="839c3-148">Развертывание с подключением к облаку — подготовка</span><span class="sxs-lookup"><span data-stu-id="839c3-148">Cloud connected deployment - Prepare</span></span>](hololens2-cloud-connected-prepare.md)

