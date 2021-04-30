---
title: 'Руководство по развертыванию: облачное подключение HoloLens 2 в масштабе с помощью удаленного помощника — обслуживание'
description: Оставайтесь в курсе последних советов по поддержке и поддержке устройств HoloLens в сети, подключенной к облаку.
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
ms.openlocfilehash: bc34c4e41c5a6cee8f3f9a0a97407ee38d419bbc
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309786"
---
# <a name="maintain---cloud-connected-guide"></a><span data-ttu-id="50ebf-104">Управление — подключение к облаку</span><span class="sxs-lookup"><span data-stu-id="50ebf-104">Maintain - Cloud connected Guide</span></span>

## <a name="updates"></a><span data-ttu-id="50ebf-105">Обновления</span><span class="sxs-lookup"><span data-stu-id="50ebf-105">Updates</span></span>

<span data-ttu-id="50ebf-106">Центр обновления Windows для бизнеса, разработанный корпорацией Майкрософт, дает ИТ-администраторам дополнительные возможности управления, например возможность развертывать обновления на группах устройств и задавать временные периоды установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="50ebf-106">Microsoft designed Windows Update for Business to provide IT administrators with additional Windows Update-centric management capabilities, such as the ability to deploy updates to groups of devices and to define maintenance windows for installing updates.</span></span>

<span data-ttu-id="50ebf-107">Узнайте, как [управлять обновлениями HoloLens](https://docs.microsoft.com/hololens/hololens-updates) , включая запланированные дни, запланированное время и устанавливать активные часы на устройстве, чтобы оно работало за пределами рабочих часов.</span><span class="sxs-lookup"><span data-stu-id="50ebf-107">Learn how to [manage HoloLens updates](https://docs.microsoft.com/hololens/hololens-updates) including scheduled days, scheduled time, and setting active hours on the device so it will update outside of working hours.</span></span>

<span data-ttu-id="50ebf-108">Удаленный помощник — это In-Boxное приложение, которое можно обновить с помощью Microsoft Store приложения.</span><span class="sxs-lookup"><span data-stu-id="50ebf-108">Remote Assist is an In-Box app, and can be update through the Microsoft Store app.</span></span> <span data-ttu-id="50ebf-109">Для всех приложений, загружаемых с помощью Microsoft Store они могут быть [обновлены вручную Microsoft Storeным](https://docs.microsoft.com/hololens/holographic-store-apps#update-apps) приложением.</span><span class="sxs-lookup"><span data-stu-id="50ebf-109">For all apps that are downloaded through the Microsoft Store they can be [updated through the Microsoft Store](https://docs.microsoft.com/hololens/holographic-store-apps#update-apps) app itself manually.</span></span>

## <a name="support-plan"></a><span data-ttu-id="50ebf-110">План поддержки</span><span class="sxs-lookup"><span data-stu-id="50ebf-110">Support Plan</span></span>

<span data-ttu-id="50ebf-111">План поддержки — отличная вещь.</span><span class="sxs-lookup"><span data-stu-id="50ebf-111">A support plan is an excellent thing to have in place.</span></span> <span data-ttu-id="50ebf-112">Это полезно для пользователей или групп, обученных в устранении неполадок процесса регистрации на устройствах HoloLens, а также общего использования устройства HoloLens в Организации.</span><span class="sxs-lookup"><span data-stu-id="50ebf-112">Having someone, or a group trained up on troubleshooting the enrollment process on HoloLens devices and also general use of the HoloLens device within your organization is useful.</span></span> <span data-ttu-id="50ebf-113">Чтобы пользователи могли быстрее разрешать свои проблемы, мы рекомендуем, чтобы процесс эскалации обрабатывался так же, как в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="50ebf-113">In order to allow your users to have the faster resolution of their issues, we suggest that your escalation process is handled in a similar manner to this order:</span></span>

1. <span data-ttu-id="50ebf-114">Службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="50ebf-114">Your Support desk.</span></span>
2. <span data-ttu-id="50ebf-115">Группа специалистов по HoloLens</span><span class="sxs-lookup"><span data-stu-id="50ebf-115">Your HoloLens Expert team</span></span>
3. <span data-ttu-id="50ebf-116">[Документы HoloLens](https://docs.microsoft.com/hololens/)  /  [Документация по устранению неполадок HoloLens](https://docs.microsoft.com/hololens/hololens-troubleshooting)</span><span class="sxs-lookup"><span data-stu-id="50ebf-116">[HoloLens Docs](https://docs.microsoft.com/hololens/) / [HoloLens Troubleshooting Docs](https://docs.microsoft.com/hololens/hololens-troubleshooting)</span></span>
4. [<span data-ttu-id="50ebf-117">Обратитесь в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="50ebf-117">Contact Support</span></span>](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=e9391227-fa6d-927b-0fff-f96288631b8f)

## <a name="development-plan"></a><span data-ttu-id="50ebf-118">План разработки</span><span class="sxs-lookup"><span data-stu-id="50ebf-118">Development Plan</span></span>

<span data-ttu-id="50ebf-119">Теперь, когда устройство успешно зарегистрировано, вы готовы к развертыванию бизнес-приложений (LOB) на устройствах.</span><span class="sxs-lookup"><span data-stu-id="50ebf-119">With your device successfully enrolled you are now prepared to deploy Line of Business apps (LOB apps) to your devices.</span></span> <span data-ttu-id="50ebf-120">Это пользовательские приложения, созданные для вашей организации&#39;потребностей.</span><span class="sxs-lookup"><span data-stu-id="50ebf-120">These are custom apps built for your organization&#39;s needs.</span></span>

<span data-ttu-id="50ebf-121">Если у вас уже есть бизнес-приложение, вы&#39;повторно готовы к [развертыванию приложения с помощью MDM](https://docs.microsoft.com/hololens/app-deploy-intune).</span><span class="sxs-lookup"><span data-stu-id="50ebf-121">If you already have a line of business app then you&#39;re ready to [deploy your app through MDM](https://docs.microsoft.com/hololens/app-deploy-intune).</span></span> <span data-ttu-id="50ebf-122">Если вы&#39;предпочитаете другой метод, просмотрите [Обзор развертывания приложений для HoloLens 2](https://docs.microsoft.com/hololens/app-deploy-overview) , чтобы узнать больше о методах развертывания бизнес-приложения на устройствах.</span><span class="sxs-lookup"><span data-stu-id="50ebf-122">If you&#39;d prefer a different method then review the [application deployment overview for HoloLens 2](https://docs.microsoft.com/hololens/app-deploy-overview) to learn more methods of deploying your LOB app to your devices.</span></span>

<span data-ttu-id="50ebf-123">Если вы&#39;создали собственное бизнес-приложение или все еще намерены в процессе создания, просмотрите документацию по разработке смешанной реальности, чтобы приступить к [проектированию и созданию прототипов](https://docs.microsoft.com/windows/mixed-reality/design/design) , или изучите основные понятия, чтобы приступить к [разработке смешанной реальности.](https://docs.microsoft.com/windows/mixed-reality/discover/get-started-with-mr)</span><span class="sxs-lookup"><span data-stu-id="50ebf-123">If you&#39;ve yet to create your own LOB app or are still in the process of creation then review our mixed reality development docs to [start designing and prototyping](https://docs.microsoft.com/windows/mixed-reality/design/design) or learn the core concepts to [get started with mixed reality development.](https://docs.microsoft.com/windows/mixed-reality/discover/get-started-with-mr)</span></span>

## <a name="device-management"></a><span data-ttu-id="50ebf-124">Управление устройствами</span><span class="sxs-lookup"><span data-stu-id="50ebf-124">Device Management</span></span> 

<span data-ttu-id="50ebf-125">Хотя это руководство посвящено настройке управления мобильными устройствами (MDM), оно не использовалось для применения ограничений или политик к устройствам.</span><span class="sxs-lookup"><span data-stu-id="50ebf-125">While this guide talked about setting up Mobile Device Management (MDM) it wasn't employed to apply device restrictions or policies were applied to devices.</span></span> <span data-ttu-id="50ebf-126">Управление устройствами можно использовать для разрешения доступа путем принудительной отправки сертификатов или ограничения доступа с помощью различных ограничений на устройства.</span><span class="sxs-lookup"><span data-stu-id="50ebf-126">Device management can be used to both to allow access by pushing certificates, or restrict access with a variety of device restrictions.</span></span> 

<span data-ttu-id="50ebf-127">Во многих случаях устройства могут иметь такие ограничения подключения, как Bluetooth, VPN, USB или даже отключение доступа к камере или микрофону.</span><span class="sxs-lookup"><span data-stu-id="50ebf-127">In many cases devices can have connectivity restrictions such as Bluetooth, VPN, USB or even turning off access to the camera or microphone.</span></span> <span data-ttu-id="50ebf-128">Если вы какие-то из этих интересов, то рекомендуем ознакомиться со [страницей общих ограничений для устройств](hololens-common-device-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="50ebf-128">If any of these interests you then we encourage you to read our [common device restrictions page](hololens-common-device-restrictions.md).</span></span>

<span data-ttu-id="50ebf-129">Существуют и другие более сложные ограничения устройств, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="50ebf-129">There are other more complex device restrictions you can use.</span></span> <span data-ttu-id="50ebf-130">Например:</span><span class="sxs-lookup"><span data-stu-id="50ebf-130">Such as:</span></span>

- <span data-ttu-id="50ebf-131">Ограничение страниц, которые можно просматривать в приложении "Параметры" с помощью [сеттингспажевисибилити](settings-uri-list.md), что позволяет пользователям получать доступ только к тем параметрам, которые им необходимо изменить, например изменить подключение к Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="50ebf-131">Limiting the pages that can be viewed in the Settings app by using [SettingsPageVisibility](settings-uri-list.md), allowing users to only access the settings they need to adjust such as changing their Wi-Fi connection.</span></span>
- <span data-ttu-id="50ebf-132">Используйте [режим киоска](hololens-kiosk.md) , чтобы ограничить пользовательский интерфейс, предоставленный пользователям на устройстве.</span><span class="sxs-lookup"><span data-stu-id="50ebf-132">Use [Kiosk mode](hololens-kiosk.md) to limit the UI presented to users on a device.</span></span> <span data-ttu-id="50ebf-133">Киоски можно настроить на отображение одного приложения или нескольких приложений с настраиваемой начальной страницей.</span><span class="sxs-lookup"><span data-stu-id="50ebf-133">You can set Kiosks to show a single app, or multiple apps with a custom start page.</span></span> <span data-ttu-id="50ebf-134">Киоски также могут представлять различные возможности для разных пользователей.</span><span class="sxs-lookup"><span data-stu-id="50ebf-134">Kiosks can also present different experiences to different users.</span></span>  
- <span data-ttu-id="50ebf-135">[Элемент управления приложениями Windows (WDAC)](windows-defender-application-control-wdac.md) , позволяющий полностью выполнять запуск конкретных приложений или процессов.</span><span class="sxs-lookup"><span data-stu-id="50ebf-135">[Windows Application Control (WDAC)](windows-defender-application-control-wdac.md) to keep specific apps or processes from launching entirely.</span></span>

<span data-ttu-id="50ebf-136">Если вы хотите узнать больше о различных методах управления устройствами или ограничениях устройств, выполните следующий шаг и ознакомьтесь с нашим обзором управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="50ebf-136">If you'd like to learn about more different methods of device management or device restrictions, then take the next step and read our Device Management Overview.</span></span>

## <a name="next-step"></a><span data-ttu-id="50ebf-137">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="50ebf-137">Next step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="50ebf-138">Ознакомьтесь с обзором CSP и управления устройствами</span><span class="sxs-lookup"><span data-stu-id="50ebf-138">Read the CSPs and Device Management Overview</span></span>](hololens-csp-policy-overview.md)