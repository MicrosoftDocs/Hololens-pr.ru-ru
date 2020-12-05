---
title: 'Руководство по развертыванию: Облако подключено к HoloLens 2 при масштабировании с помощью удаленной поддержки.'
description: Советы по поддержке устройств HoloLens в сети, подключенной к облаку
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
ms.openlocfilehash: beee64159415c0635812463f81c0b5565e44e4a8
ms.sourcegitcommit: 8e2c268733adce2662bf320cf96ccfea5919425e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2020
ms.locfileid: "11196364"
---
# <span data-ttu-id="49c4d-104">Обслуживание — Руководство по подключению к облаку</span><span class="sxs-lookup"><span data-stu-id="49c4d-104">Maintain - Cloud connected Guide</span></span>

## <span data-ttu-id="49c4d-105">Обновления</span><span class="sxs-lookup"><span data-stu-id="49c4d-105">Updates</span></span>

<span data-ttu-id="49c4d-106">Центр обновления Windows для бизнеса, разработанный корпорацией Майкрософт, дает ИТ-администраторам дополнительные возможности управления, например возможность развертывать обновления на группах устройств и задавать временные периоды установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="49c4d-106">Microsoft designed Windows Update for Business to provide IT administrators with additional Windows Update-centric management capabilities, such as the ability to deploy updates to groups of devices and to define maintenance windows for installing updates.</span></span>

<span data-ttu-id="49c4d-107">Здесь вы узнаете, как [управлять обновлениями HoloLens](https://docs.microsoft.com/hololens/hololens-updates) , в том числе запланированными днями, запланированным временем и заданием активных часов на устройстве, чтобы оно обновлялось за пределами рабочих часов.</span><span class="sxs-lookup"><span data-stu-id="49c4d-107">Learn how to [manage HoloLens updates](https://docs.microsoft.com/hololens/hololens-updates) including scheduled days, scheduled time, and setting active hours on the device so it will update outside of working hours.</span></span>

<span data-ttu-id="49c4d-108">Remote Assist — это приложение для In-Box, которое можно обновить с помощью приложения Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="49c4d-108">Remote Assist is a In-Box app, and can be update through the Microsoft Store app.</span></span> <span data-ttu-id="49c4d-109">Для всех приложений, которые загружаются в Microsoft Store, они могут быть [обновлены вручную с помощью самого приложения Microsoft Store](https://docs.microsoft.com/hololens/holographic-store-apps#update-apps) .</span><span class="sxs-lookup"><span data-stu-id="49c4d-109">For all apps that are downloaded through the Microsoft Store they can be [updated through the Microsoft Store](https://docs.microsoft.com/hololens/holographic-store-apps#update-apps) app itself manually.</span></span>

## <span data-ttu-id="49c4d-110">План поддержки</span><span class="sxs-lookup"><span data-stu-id="49c4d-110">Support Plan</span></span>

<span data-ttu-id="49c4d-111">План обслуживания — отличная вещь.</span><span class="sxs-lookup"><span data-stu-id="49c4d-111">A support plan is an excellent thing to have in place.</span></span> <span data-ttu-id="49c4d-112">Для пользователей или групп, обученных в разделе Устранение неполадок с регистрацией на устройствах HoloLens, а также общее использование устройства HoloLens в Организации.</span><span class="sxs-lookup"><span data-stu-id="49c4d-112">Having someone, or a group trained up on troubleshooting the enrollment process on HoloLens devices and also general use of the HoloLens device within your organization is useful.</span></span> <span data-ttu-id="49c4d-113">Для того чтобы пользователи могли быстрее разрешать ваши проблемы, мы рекомендуем, чтобы процесс эскалации обрабатывался так, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="49c4d-113">In order to allow your users to have the faster resolution of their issues we suggest that your escalation process is handled in a similar manner to this:</span></span>

1. <span data-ttu-id="49c4d-114">Служба поддержки.</span><span class="sxs-lookup"><span data-stu-id="49c4d-114">Your Support desk.</span></span>
2. <span data-ttu-id="49c4d-115">Группа экспертов по HoloLens</span><span class="sxs-lookup"><span data-stu-id="49c4d-115">Your HoloLens Expert team</span></span>
3. <span data-ttu-id="49c4d-116">[Документы HoloLens](https://docs.microsoft.com/hololens/)  /  [Документы по устранению неполадок HoloLens](https://docs.microsoft.com/hololens/hololens-troubleshooting)</span><span class="sxs-lookup"><span data-stu-id="49c4d-116">[HoloLens Docs](https://docs.microsoft.com/hololens/) / [HoloLens Troubleshooting Docs](https://docs.microsoft.com/hololens/hololens-troubleshooting)</span></span>
4. [<span data-ttu-id="49c4d-117">обратитесь в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="49c4d-117">Contact Support</span></span>](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=e9391227-fa6d-927b-0fff-f96288631b8f)

## <span data-ttu-id="49c4d-118">План развития</span><span class="sxs-lookup"><span data-stu-id="49c4d-118">Development Plan</span></span>

<span data-ttu-id="49c4d-119">После успешной регистрации вашего устройства вы готовы к развертыванию бизнес-приложений на устройствах.</span><span class="sxs-lookup"><span data-stu-id="49c4d-119">With your device successfully enrolled you are now prepared to deploy Line of Business apps (LOB apps) to your devices.</span></span> <span data-ttu-id="49c4d-120">Это пользовательские приложения, разработанные для вашей организации,&#39;потребности.</span><span class="sxs-lookup"><span data-stu-id="49c4d-120">These are custom apps built for your organization&#39;s needs.</span></span>

<span data-ttu-id="49c4d-121">Если у вас уже есть линейное бизнес-приложение, вы&#39;повторно готовы [развернуть приложение с помощью MDM](https://docs.microsoft.com/hololens/app-deploy-intune).</span><span class="sxs-lookup"><span data-stu-id="49c4d-121">If you already have a line of business app then you&#39;re ready to [deploy your app through MDM](https://docs.microsoft.com/hololens/app-deploy-intune).</span></span> <span data-ttu-id="49c4d-122">Если вы&#39;d предпочитаете другой способ, ознакомьтесь со статьей [развертывание приложения для HoloLens 2](https://docs.microsoft.com/hololens/app-deploy-overview) , чтобы узнать больше о том, как РАЗВЕРТЫВАть бизнес-приложение на своих устройствах.</span><span class="sxs-lookup"><span data-stu-id="49c4d-122">If you&#39;d prefer a different method then review the [application deployment overview for HoloLens 2](https://docs.microsoft.com/hololens/app-deploy-overview) to learn more methods of deploying your LOB app to your devices.</span></span>

<span data-ttu-id="49c4d-123">Если вы&#39;хотите создать собственное приложение LOB или все еще находится в процессе создания, ознакомьтесь с документами по разработке в смешанной реальности, чтобы приступить к разработке [и созданию прототипов](https://docs.microsoft.com/windows/mixed-reality/design/design) , а также изучать основные понятия для [начала работы с смешанной реальности.](https://docs.microsoft.com/windows/mixed-reality/discover/get-started-with-mr)</span><span class="sxs-lookup"><span data-stu-id="49c4d-123">If you&#39;ve yet to create your own LOB app or are still in the process of creation then review our mixed reality development docs to [start designing and prototyping](https://docs.microsoft.com/windows/mixed-reality/design/design) or learn the core concepts to [get started with mixed reality development.](https://docs.microsoft.com/windows/mixed-reality/discover/get-started-with-mr)</span></span>

## <span data-ttu-id="49c4d-124">Управление устройствами</span><span class="sxs-lookup"><span data-stu-id="49c4d-124">Device Management</span></span> 

<span data-ttu-id="49c4d-125">Несмотря на то, что в этом руководстве мы говорили о настройке управления мобильными устройствами (MDM), она не использовалась для применения ограничений к устройствам или политик, примененных к устройствам.</span><span class="sxs-lookup"><span data-stu-id="49c4d-125">While this guide talked about setting up Mobile Device Management (MDM) it wasn't employed to apply device restrictions or policies were applied to devices.</span></span> <span data-ttu-id="49c4d-126">Управление устройствами можно использовать как для предоставления доступа, так и для разрешения принудительной отправки сертификатов, или ограничения доступа с использованием различных ограничений устройства.</span><span class="sxs-lookup"><span data-stu-id="49c4d-126">Device management can be used to both to allow access by pushing certificates, or restrict access with a variety of device restrictions.</span></span> 

<span data-ttu-id="49c4d-127">Во многих случаях устройства могут иметь такие ограничения подключения, как Bluetooth, VPN, USB или даже отключение доступа к камере или микрофону.</span><span class="sxs-lookup"><span data-stu-id="49c4d-127">In many cases devices can have connectivity restrictions such as Bluetooth, VPN, USB or even turning off access to the camera or microphone.</span></span> <span data-ttu-id="49c4d-128">Если какой-либо из этих данных вас интересует, мы рекомендуем вам прочитать [страницу "Общие ограничения устройства](hololens-common-device-restrictions.md)".</span><span class="sxs-lookup"><span data-stu-id="49c4d-128">If any of these interest you then we encourage you to read our [common device restrictions page](hololens-common-device-restrictions.md).</span></span>

<span data-ttu-id="49c4d-129">Вы можете использовать и более сложные ограничения для устройств.</span><span class="sxs-lookup"><span data-stu-id="49c4d-129">There are other more complex device restrictions you can use.</span></span> <span data-ttu-id="49c4d-130">Например:</span><span class="sxs-lookup"><span data-stu-id="49c4d-130">Such as:</span></span>

- <span data-ttu-id="49c4d-131">Ограничение страниц, которые можно просматривать в приложении "Параметры" с помощью [SettingsPageVisibility](settings-uri-list.md), что позволяет пользователям получать доступ только к тем параметрам, которые им нужно изменить, например изменить подключение к Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="49c4d-131">Limiting the pages that can be viewed in the Settings app by using [SettingsPageVisibility](settings-uri-list.md), allowing users to only access the settings they need to adjust such as changing their Wi-Fi connection.</span></span>
- <span data-ttu-id="49c4d-132">Использование [режима киоска](hololens-kiosk.md) для ограничения пользовательского интерфейса, представляемого пользователям на устройстве.</span><span class="sxs-lookup"><span data-stu-id="49c4d-132">Use [Kiosk mode](hololens-kiosk.md) to limit the UI presented to users on a device.</span></span> <span data-ttu-id="49c4d-133">Вы можете настроить для киосков отображение одного приложения или нескольких приложений с настраиваемой начальной страницей.</span><span class="sxs-lookup"><span data-stu-id="49c4d-133">You can set Kiosks to show a single app, or multiple apps with a custom start page.</span></span> <span data-ttu-id="49c4d-134">Киоски также могут представлять различные возможности для разных пользователей.</span><span class="sxs-lookup"><span data-stu-id="49c4d-134">Kiosks can also present different experiences to different users.</span></span>  
- <span data-ttu-id="49c4d-135">[Элемент управления приложением Windows (WDAC)](windows-defender-application-control-wdac.md) для полного запуска конкретных приложений или процессов.</span><span class="sxs-lookup"><span data-stu-id="49c4d-135">[Windows Application Control (WDAC)](windows-defender-application-control-wdac.md) to keep specific apps or processes from launching entirely.</span></span>

<span data-ttu-id="49c4d-136">Если вы хотите узнать больше о различных способах управления устройствами или ограничениях устройств, выполните следующее действие и ознакомьтесь с нашим обзором управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="49c4d-136">If you'd like to learn about more different methods of device management or device restrictions then take the next step and read our Device Management Overview.</span></span>

## <span data-ttu-id="49c4d-137">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="49c4d-137">Next step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="49c4d-138">Общие сведения о службах управления правами и управлении устройствами</span><span class="sxs-lookup"><span data-stu-id="49c4d-138">Read the CSPs and Device Management Overview</span></span>](hololens-csp-policy-overview.md)