---
title: 'Руководство по развертыванию: Облако подключено к HoloLens 2 с удаленным помощником "Обзор"'
description: Регистрация устройств HoloLens в сети, подключенной к облаку
keywords: HoloLens, управление, Облако подключено, Remote Assist, AAD, Azure AD, MDM, управление мобильными устройствами
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
ms.openlocfilehash: ba3f826360f999a72e671166af7a19d19ce9c567
ms.sourcegitcommit: 8e2c268733adce2662bf320cf96ccfea5919425e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2020
ms.locfileid: "11196370"
---
# <span data-ttu-id="442dd-104">Руководство по развертыванию: Облако подключено к HoloLens 2 с удаленным помощником — обзор</span><span class="sxs-lookup"><span data-stu-id="442dd-104">Deployment Guide – Cloud connected HoloLens 2 with Remote Assist – Overview</span></span>

<span data-ttu-id="442dd-105">Это руководство поможет ИТ-специалистам планировать и развертывать устройства Microsoft HoloLens 2 в своей организации с помощью общей цели, связанной с тем, что эти устройства подключены к вашей организации с помощью Dynamics 365 Remote Assist готово к использованию.</span><span class="sxs-lookup"><span data-stu-id="442dd-105">This guide helps IT professionals plan for and deploy Microsoft HoloLens 2 devices to their organization with the overall goal of having those devices cloud connected to your organization with Dynamics 365 Remote Assist ready to use.</span></span> <span data-ttu-id="442dd-106">Имейте в виду, что это будет служить моделью развертывания экспериментов в Организации в различных вариантах использования HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="442dd-106">Keep in mind, this will serve as a model for proof-of-concept deployments to your organization across a variety of HoloLens 2 use cases.</span></span>

<span data-ttu-id="442dd-107">В руководстве мы постараемся зарегистрировать устройства в управлении устройствами, применить лицензии по мере необходимости и подтвердить, что ваши конечные пользователи смогут сразу же использовать удаленную помощь при настройке устройства.</span><span class="sxs-lookup"><span data-stu-id="442dd-107">During the guide we will cover how to enroll your devices into your device management, apply licenses as needed, and validate that your end users are able to immediately use Remote Assist upon device set up.</span></span> <span data-ttu-id="442dd-108">Для этого мы рассмотрим важные компоненты инфраструктуры, необходимые для настройки и выполнения развертывания в масштабе с помощью HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="442dd-108">To do this we will go over the important pieces of infrastructure needed to get set up and running – achieving deployment at scale with HoloLens 2.</span></span>

## <span data-ttu-id="442dd-109">В этом руководстве</span><span class="sxs-lookup"><span data-stu-id="442dd-109">In this Guide</span></span>

<span data-ttu-id="442dd-110">Это руководство содержит определенную цель настройки удаленной помощи в вашей организации на устройствах HoloLens.</span><span class="sxs-lookup"><span data-stu-id="442dd-110">This guide has the specific goal of setting up Remote Assist within your organization on your HoloLens devices.</span></span> <span data-ttu-id="442dd-111">Мы рассмотрим Necessities, необходимые для достижения этой цели.</span><span class="sxs-lookup"><span data-stu-id="442dd-111">We will cover the necessities needed to achieve that goal.</span></span> <span data-ttu-id="442dd-112">Чтобы настроить фокус на этой цели, необходимо предварительно выбрать определенные подготовительные действия и конфигурации для оптимизации развертывания или уменьшения количества элементов, необходимых для настройки.</span><span class="sxs-lookup"><span data-stu-id="442dd-112">In order to maintain focus on this goal certain preparations and configurations will be pre-selected in order to optimize for this deployment or to reduce the items needed to configure.</span></span> <span data-ttu-id="442dd-113">Вы будете получать уведомления об этих вариантах, а также настраивать развертывание в соответствии с бизнес-потребностями.</span><span class="sxs-lookup"><span data-stu-id="442dd-113">You will be informed of these choices, and can customize your deployment based on your business needs.</span></span>

<span data-ttu-id="442dd-114">Это настройка аналогична [сценарию a: развертывание на облачные устройства](https://docs.microsoft.com/hololens/common-scenarios#scenario-a), что является хорошим вариантом для многих развертываний концепций, которые будут включать:</span><span class="sxs-lookup"><span data-stu-id="442dd-114">This is a set up similar to [Scenario A: Deploy to cloud connect devices](https://docs.microsoft.com/hololens/common-scenarios#scenario-a), which is a good option for many Proof of Concept deployments which will include:</span></span>

- <span data-ttu-id="442dd-115">Обычно сети Wi-Fi полностью открыты для Интернета и облачных служб.</span><span class="sxs-lookup"><span data-stu-id="442dd-115">Wi-Fi networks are typically fully open to the Internet and Cloud services</span></span>
- <span data-ttu-id="442dd-116">Присоединение к Azure AD с автоматическим регистрацией MDM — управление MDM (Intune)</span><span class="sxs-lookup"><span data-stu-id="442dd-116">Azure AD Join with MDM Auto Enrollment -- MDM (Intune) Managed</span></span>
- <span data-ttu-id="442dd-117">Вход в систему с помощью своей корпоративной учетной записи (AAD)</span><span class="sxs-lookup"><span data-stu-id="442dd-117">Users sign in with their own corporate account (AAD)</span></span>
  - <span data-ttu-id="442dd-118">Поддерживается один или несколько пользователей на устройстве</span><span class="sxs-lookup"><span data-stu-id="442dd-118">Single or multiple users per device supported</span></span>
- <span data-ttu-id="442dd-119">Различные уровни конфигураций блокировки устройств применяются на основании конкретных вариантов использования, начиная с полного открытия на единое приложение</span><span class="sxs-lookup"><span data-stu-id="442dd-119">Varying levels of device lockdown configurations are applied based on specific use cases, from Fully Open to Single App Kiosk</span></span>

![Сценарий с подключением к облаку](./images/cloud-connected-deployment-chart.png)

<span data-ttu-id="442dd-121">В этом руководстве не будут применяться дополнительные ограничения на устройства или конфигурации, но мы рекомендуем ознакомиться с этими параметрами после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="442dd-121">No additional device restrictions or configurations will be applied in this guide, however we encourage you to explore those options after finishing.</span></span>

## <span data-ttu-id="442dd-122">Сведения об удаленном помощнике</span><span class="sxs-lookup"><span data-stu-id="442dd-122">Learn about Remote Assist</span></span>

<span data-ttu-id="442dd-123">Функция Remote Assist позволяет проводить совместное обслуживание и ремонт, удаленную инспекцию, а также предоставлять общий доступ к материалам и обучение.</span><span class="sxs-lookup"><span data-stu-id="442dd-123">Remote Assist allows for collaborative maintenance and repair, remote inspection, as well as knowledge sharing and training.</span></span> <span data-ttu-id="442dd-124">Подключив пользователей в разных ролях и расположениях, вы сможете подключиться к службе удаленного взаимодействия в Microsoft Teams с помощью удаленного помощника.</span><span class="sxs-lookup"><span data-stu-id="442dd-124">By connecting people in different roles and locations a technician using Remote Assist can connect with a remote collaborator on Microsoft Teams.</span></span> <span data-ttu-id="442dd-125">Они могут сочетать видео, снимки экрана и заметки для разрешения проблем в реальном времени, даже если они пользующимися&#39;t в том же месте.</span><span class="sxs-lookup"><span data-stu-id="442dd-125">They can combine video, screenshots, and annotations to solve problems in real time even when they aren&#39;t in the same location.</span></span> <span data-ttu-id="442dd-126">Удаленные участники могут вставлять эталонные изображения, схематическое и другие полезные данные, которые обслуживаются специалистами по&#39;s, чтобы они могли ссылаться на схематичные и видеоматериалы на HoloLens и без руки.</span><span class="sxs-lookup"><span data-stu-id="442dd-126">Remote collaborators can insert reference images, schematics, and other helpful information the technician&#39;s physical space so they can refer to the schematic while working heads-up and hands-free on HoloLens.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/d3YT8j0yYl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <span data-ttu-id="442dd-127">В этом руководстве вы сможете:</span><span class="sxs-lookup"><span data-stu-id="442dd-127">In this guide you will:</span></span>

<span data-ttu-id="442dd-128">Подготовку</span><span class="sxs-lookup"><span data-stu-id="442dd-128">Prepare:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="442dd-129">Узнайте об основных возможностях инфраструктуры для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="442dd-129">Learn about the infrastructure essentials for HoloLens 2 devices.</span></span>](hololens2-cloud-connected-prepare.md#infrastructure-essentials)
> - [<span data-ttu-id="442dd-130">Узнайте больше о AAD и настройте его, если у вас&#39;нет.</span><span class="sxs-lookup"><span data-stu-id="442dd-130">Learn more about AAD and set up one if you don&#39;t have it.</span></span>](hololens2-cloud-connected-prepare.md#azure-active-directory)
> - [<span data-ttu-id="442dd-131">Узнайте о том, как управлять удостоверениями и как лучше настраивать учетные записи AAD.</span><span class="sxs-lookup"><span data-stu-id="442dd-131">Learn about Identity management and how to best set up AAD accounts.</span></span>](hololens2-cloud-connected-prepare.md#identity-management)
> - [<span data-ttu-id="442dd-132">Ознакомьтесь с дополнительными сведениями о MDM и настройте ее с помощью Intune, если у вас&#39;уже есть.</span><span class="sxs-lookup"><span data-stu-id="442dd-132">Learn more about MDM, and set up with Intune if you don&#39;t already have one ready.</span></span>](hololens2-cloud-connected-prepare.md#mobile-device-management)
> - [<span data-ttu-id="442dd-133">Узнайте о требованиях к сети удаленного помощника.</span><span class="sxs-lookup"><span data-stu-id="442dd-133">Learn about the networking requirements of Remote Assist.</span></span>](hololens2-cloud-connected-prepare.md#network)
> - [<span data-ttu-id="442dd-134">Дополнительно: VPN для подключения к ресурсам Организации</span><span class="sxs-lookup"><span data-stu-id="442dd-134">Optionally: VPN to connect to organizational resources</span></span>](/hololens2-cloud-connected-prepare.md#optional-connect-your-hololens-to-vpn)

<span data-ttu-id="442dd-135">Строил</span><span class="sxs-lookup"><span data-stu-id="442dd-135">Configure:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="442dd-136">Создание пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="442dd-136">How to create Users and Groups.</span></span>](hololens2-cloud-connected-configure.md#azure-users-and-groups)
> - [<span data-ttu-id="442dd-137">Как настроить автоматическую регистрацию в AAD.</span><span class="sxs-lookup"><span data-stu-id="442dd-137">How to set up Auto-enrollment within AAD.</span></span>](hololens2-cloud-connected-configure.md#auto-enrollment-on-hololens-2)
> - [<span data-ttu-id="442dd-138">Назначение лицензий приложения.</span><span class="sxs-lookup"><span data-stu-id="442dd-138">How to assign your Application licenses.</span></span>](hololens2-cloud-connected-configure.md#application-licenses)

<span data-ttu-id="442dd-139">Внедрять</span><span class="sxs-lookup"><span data-stu-id="442dd-139">Deploy:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="442dd-140">Настройте HoloLens 2 и проверяйте регистрацию.</span><span class="sxs-lookup"><span data-stu-id="442dd-140">Set up your HoloLens 2 and validate enrollment.</span></span>](hololens2-cloud-connected-deploy.md#enrollment-validation)
> - [<span data-ttu-id="442dd-141">Убедитесь, что вы можете позвонить удаленному помощнику.</span><span class="sxs-lookup"><span data-stu-id="442dd-141">Validate you can make a Remote Assist call.</span></span>](hololens2-cloud-connected-deploy.md#remote-assist-call-validation)

<span data-ttu-id="442dd-142">Сохранить</span><span class="sxs-lookup"><span data-stu-id="442dd-142">Maintain:</span></span>

> [!div class="checklist"]
> - [<span data-ttu-id="442dd-143">Обновление удаленного помощника с помощью приложения Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="442dd-143">How to update Remote Assist using the Microsoft Store app.</span></span>](hololens2-cloud-connected-maintain.md#updates)
> - [<span data-ttu-id="442dd-144">Создание плана поддержки.</span><span class="sxs-lookup"><span data-stu-id="442dd-144">Making a support plan.</span></span>](hololens2-cloud-connected-maintain.md#support-plan)
> - [<span data-ttu-id="442dd-145">План развития.</span><span class="sxs-lookup"><span data-stu-id="442dd-145">Development plan.</span></span>](hololens2-cloud-connected-maintain.md#development-plan)

## <span data-ttu-id="442dd-146">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="442dd-146">Next step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="442dd-147">Развертывание с подключением к облаку — подготовка</span><span class="sxs-lookup"><span data-stu-id="442dd-147">Cloud connected deployment - Prepare</span></span>](hololens2-cloud-connected-prepare.md)

