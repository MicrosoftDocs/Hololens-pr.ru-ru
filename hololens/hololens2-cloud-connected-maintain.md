---
title: Руководство по развертыванию — масштабное развертывание HoloLens 2 с подключением к облаку с помощью удаленной помощи — обслуживание
description: Оставайтесь в курсе наших советов по обслуживанию и поддержке устройств HoloLens по сети Cloud Connected.
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
ms.openlocfilehash: bc34c4e41c5a6cee8f3f9a0a97407ee38d419bbc
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283900"
---
# <span data-ttu-id="882b9-104">Обслуживание — руководство по подключению к облаку</span><span class="sxs-lookup"><span data-stu-id="882b9-104">Maintain - Cloud connected Guide</span></span>

## <span data-ttu-id="882b9-105">Обновления</span><span class="sxs-lookup"><span data-stu-id="882b9-105">Updates</span></span>

<span data-ttu-id="882b9-106">Центр обновления Windows для бизнеса, разработанный корпорацией Майкрософт, дает ИТ-администраторам дополнительные возможности управления, например возможность развертывать обновления на группах устройств и задавать временные периоды установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="882b9-106">Microsoft designed Windows Update for Business to provide IT administrators with additional Windows Update-centric management capabilities, such as the ability to deploy updates to groups of devices and to define maintenance windows for installing updates.</span></span>

<span data-ttu-id="882b9-107">Узнайте, как управлять обновлениями [HoloLens,](https://docs.microsoft.com/hololens/hololens-updates) включая запланированные дни, запланированное время и настройку часов активности на устройстве, чтобы оно обновлялось не в рабочее время.</span><span class="sxs-lookup"><span data-stu-id="882b9-107">Learn how to [manage HoloLens updates](https://docs.microsoft.com/hololens/hololens-updates) including scheduled days, scheduled time, and setting active hours on the device so it will update outside of working hours.</span></span>

<span data-ttu-id="882b9-108">Удаленная помощь — это In-Box, которое можно обновить с помощью приложения Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="882b9-108">Remote Assist is an In-Box app, and can be update through the Microsoft Store app.</span></span> <span data-ttu-id="882b9-109">Для всех приложений, скачаемых через Microsoft Store, их можно обновлять вручную через само приложение [Microsoft Store.](https://docs.microsoft.com/hololens/holographic-store-apps#update-apps)</span><span class="sxs-lookup"><span data-stu-id="882b9-109">For all apps that are downloaded through the Microsoft Store they can be [updated through the Microsoft Store](https://docs.microsoft.com/hololens/holographic-store-apps#update-apps) app itself manually.</span></span>

## <span data-ttu-id="882b9-110">План поддержки</span><span class="sxs-lookup"><span data-stu-id="882b9-110">Support Plan</span></span>

<span data-ttu-id="882b9-111">План поддержки — это отличная возможность на месте.</span><span class="sxs-lookup"><span data-stu-id="882b9-111">A support plan is an excellent thing to have in place.</span></span> <span data-ttu-id="882b9-112">Полезно иметь кого-то или группу, обученную устранять неполадки процесса регистрации на устройствах HoloLens, а также использовать устройство HoloLens в организации.</span><span class="sxs-lookup"><span data-stu-id="882b9-112">Having someone, or a group trained up on troubleshooting the enrollment process on HoloLens devices and also general use of the HoloLens device within your organization is useful.</span></span> <span data-ttu-id="882b9-113">Чтобы пользователи могли быстрее решить свои проблемы, мы рекомендуем, чтобы процесс эскалации обрабатывался аналогично этому порядку:</span><span class="sxs-lookup"><span data-stu-id="882b9-113">In order to allow your users to have the faster resolution of their issues, we suggest that your escalation process is handled in a similar manner to this order:</span></span>

1. <span data-ttu-id="882b9-114">Ваша службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="882b9-114">Your Support desk.</span></span>
2. <span data-ttu-id="882b9-115">Команда экспертов HoloLens</span><span class="sxs-lookup"><span data-stu-id="882b9-115">Your HoloLens Expert team</span></span>
3. <span data-ttu-id="882b9-116">[Документы HoloLens](https://docs.microsoft.com/hololens/)  /  [Устранение неполадок HoloLens в docs](https://docs.microsoft.com/hololens/hololens-troubleshooting)</span><span class="sxs-lookup"><span data-stu-id="882b9-116">[HoloLens Docs](https://docs.microsoft.com/hololens/) / [HoloLens Troubleshooting Docs](https://docs.microsoft.com/hololens/hololens-troubleshooting)</span></span>
4. [<span data-ttu-id="882b9-117">обратитесь в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="882b9-117">Contact Support</span></span>](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=e9391227-fa6d-927b-0fff-f96288631b8f)

## <span data-ttu-id="882b9-118">План разработки</span><span class="sxs-lookup"><span data-stu-id="882b9-118">Development Plan</span></span>

<span data-ttu-id="882b9-119">После успешной регистрации устройства вы готовы развернуть бизнес-приложения (бизнес-приложения) на своих устройствах.</span><span class="sxs-lookup"><span data-stu-id="882b9-119">With your device successfully enrolled you are now prepared to deploy Line of Business apps (LOB apps) to your devices.</span></span> <span data-ttu-id="882b9-120">Это пользовательские приложения, созданные для&#39;организации.</span><span class="sxs-lookup"><span data-stu-id="882b9-120">These are custom apps built for your organization&#39;s needs.</span></span>

<span data-ttu-id="882b9-121">Если у вас уже есть бизнес-приложение, вы&#39;готовы к развертыванию приложения [с помощью MDM.](https://docs.microsoft.com/hololens/app-deploy-intune)</span><span class="sxs-lookup"><span data-stu-id="882b9-121">If you already have a line of business app then you&#39;re ready to [deploy your app through MDM](https://docs.microsoft.com/hololens/app-deploy-intune).</span></span> <span data-ttu-id="882b9-122">Если вы&#39;использовать другой метод, просмотрите обзор развертывания приложений [для HoloLens 2,](https://docs.microsoft.com/hololens/app-deploy-overview) чтобы узнать больше о методах развертывания вашего приложения на устройствах.</span><span class="sxs-lookup"><span data-stu-id="882b9-122">If you&#39;d prefer a different method then review the [application deployment overview for HoloLens 2](https://docs.microsoft.com/hololens/app-deploy-overview) to learn more methods of deploying your LOB app to your devices.</span></span>

<span data-ttu-id="882b9-123">Если вы&#39;еще не создали собственное бизнес-приложение или все еще находитесь в процессе создания, [](https://docs.microsoft.com/windows/mixed-reality/design/design) просмотрите наши документы по разработке смешанной реальности, чтобы приступить к разработке и созданию собственного создания, или изучите основные понятия, которые необходимо приступить к разработке смешанной [реальности.](https://docs.microsoft.com/windows/mixed-reality/discover/get-started-with-mr)</span><span class="sxs-lookup"><span data-stu-id="882b9-123">If you&#39;ve yet to create your own LOB app or are still in the process of creation then review our mixed reality development docs to [start designing and prototyping](https://docs.microsoft.com/windows/mixed-reality/design/design) or learn the core concepts to [get started with mixed reality development.](https://docs.microsoft.com/windows/mixed-reality/discover/get-started-with-mr)</span></span>

## <span data-ttu-id="882b9-124">Управление устройствами</span><span class="sxs-lookup"><span data-stu-id="882b9-124">Device Management</span></span> 

<span data-ttu-id="882b9-125">В этом руководстве речь идет о настройке управления мобильными устройствами (MDM), но не применялось для применения ограничений или политик устройств.</span><span class="sxs-lookup"><span data-stu-id="882b9-125">While this guide talked about setting up Mobile Device Management (MDM) it wasn't employed to apply device restrictions or policies were applied to devices.</span></span> <span data-ttu-id="882b9-126">Управление устройствами можно использовать как для того, чтобы разрешить доступ путем выдачи сертификатов, так и для ограничения доступа с помощью различных ограничений устройств.</span><span class="sxs-lookup"><span data-stu-id="882b9-126">Device management can be used to both to allow access by pushing certificates, or restrict access with a variety of device restrictions.</span></span> 

<span data-ttu-id="882b9-127">Во многих случаях у устройств могут быть ограничения на подключение, такие как Bluetooth, VPN, USB или даже отключение доступа к камере или микрофону.</span><span class="sxs-lookup"><span data-stu-id="882b9-127">In many cases devices can have connectivity restrictions such as Bluetooth, VPN, USB or even turning off access to the camera or microphone.</span></span> <span data-ttu-id="882b9-128">Если какой-либо из этих интересов вас интересует, рекомендуем прочитать нашу общую страницу [ограничений устройств.](hololens-common-device-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="882b9-128">If any of these interests you then we encourage you to read our [common device restrictions page](hololens-common-device-restrictions.md).</span></span>

<span data-ttu-id="882b9-129">Вы можете использовать другие более сложные ограничения устройств.</span><span class="sxs-lookup"><span data-stu-id="882b9-129">There are other more complex device restrictions you can use.</span></span> <span data-ttu-id="882b9-130">Например:</span><span class="sxs-lookup"><span data-stu-id="882b9-130">Such as:</span></span>

- <span data-ttu-id="882b9-131">Ограничение страниц, которые можно просмотреть в приложении "Параметры" с помощью [ПараметрыPageVisibility,](settings-uri-list.md)позволяя пользователям получать доступ только к тем настройкам, которые им нужно настроить, например к изменению Wi-Fi подключения.</span><span class="sxs-lookup"><span data-stu-id="882b9-131">Limiting the pages that can be viewed in the Settings app by using [SettingsPageVisibility](settings-uri-list.md), allowing users to only access the settings they need to adjust such as changing their Wi-Fi connection.</span></span>
- <span data-ttu-id="882b9-132">Используйте [режим терминала,](hololens-kiosk.md) чтобы ограничить пользовательский интерфейс, представленный пользователям на устройстве.</span><span class="sxs-lookup"><span data-stu-id="882b9-132">Use [Kiosk mode](hololens-kiosk.md) to limit the UI presented to users on a device.</span></span> <span data-ttu-id="882b9-133">Вы можете настроить киоски для показа одного приложения или нескольких приложений с настраиваемой стартовой страницей.</span><span class="sxs-lookup"><span data-stu-id="882b9-133">You can set Kiosks to show a single app, or multiple apps with a custom start page.</span></span> <span data-ttu-id="882b9-134">Киоски также могут представлять различные опытом для разных пользователей.</span><span class="sxs-lookup"><span data-stu-id="882b9-134">Kiosks can also present different experiences to different users.</span></span>  
- <span data-ttu-id="882b9-135">[Windows Application Control (WDAC),](windows-defender-application-control-wdac.md) чтобы полностью не запускать определенные приложения или процессы.</span><span class="sxs-lookup"><span data-stu-id="882b9-135">[Windows Application Control (WDAC)](windows-defender-application-control-wdac.md) to keep specific apps or processes from launching entirely.</span></span>

<span data-ttu-id="882b9-136">Если вы хотите узнать больше о различных методах управления устройствами или ограничений устройств, затем считайте следующий шаг и ознакомьтесь с нашим обзором управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="882b9-136">If you'd like to learn about more different methods of device management or device restrictions, then take the next step and read our Device Management Overview.</span></span>

## <span data-ttu-id="882b9-137">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="882b9-137">Next step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="882b9-138">Ознакомьтесь с обзором CSP и управления устройствами</span><span class="sxs-lookup"><span data-stu-id="882b9-138">Read the CSPs and Device Management Overview</span></span>](hololens-csp-policy-overview.md)