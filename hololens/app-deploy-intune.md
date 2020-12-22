---
title: Intune и портал компании
description: intune, управление приложениями, приложение, портал компании, портал
keywords: intune, управление приложениями, приложение, портал компании, портал, hololens
author: evmill
ms.author: v-evmill
ms.date: 6/22/2020
ms.prod: hololens
ms.custom:
- CI 111456
- CSSTroubleshooting
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 7fcd65d5e49fa9cdd771828401749a0a41e50238
ms.sourcegitcommit: d319ac257b9ace484acf5dcfb16c9d4e19ea50a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2020
ms.locfileid: "11247221"
---
# <span data-ttu-id="be21b-104">Intune и корпоративный портал</span><span class="sxs-lookup"><span data-stu-id="be21b-104">Intune & Company Portal</span></span>

<span data-ttu-id="be21b-105">С помощью управления мобильными устройствами (MDM) вы можете использовать собственные настраиваемые приложения с помощью [Microsoft Endpoint Manager (Intune)](https://docs.microsoft.com/intune/windows-holographic-for-business) для его развертывания непосредственно на устройствах HoloLens.</span><span class="sxs-lookup"><span data-stu-id="be21b-105">With Mobile Device Management (MDM), you can use your own custom apps through [Microsoft Endpoint Manager (Intune)](https://docs.microsoft.com/intune/windows-holographic-for-business) to deploy it directly to your HoloLens devices.</span></span> <span data-ttu-id="be21b-106">Microsoft Intune — это облачная служба, которая фокусируется на управлении мобильными устройствами (MDM) и управлении мобильными приложениями (MAM).</span><span class="sxs-lookup"><span data-stu-id="be21b-106">Microsoft Intune is a cloud-based service that focuses on mobile device management (MDM) and mobile application management (MAM).</span></span> <span data-ttu-id="be21b-107">Intune входит в набор Microsoft [Enterprise Mobility + Security (EMS)](https://www.microsoft.com/microsoft-365/enterprise-mobility-security)и позволяет пользователям работать эффективно, сохраняя защиту данных организации.</span><span class="sxs-lookup"><span data-stu-id="be21b-107">Intune is included in Microsoft's [Enterprise Mobility + Security (EMS) suite](https://www.microsoft.com/microsoft-365/enterprise-mobility-security), and enables users to be productive while keeping your organization data protected.</span></span> <span data-ttu-id="be21b-108">Чтобы узнать больше о Intune, прочитайте статью ["Что такое Intune".](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune)</span><span class="sxs-lookup"><span data-stu-id="be21b-108">To learn more about Intune, read [What is Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune).</span></span>

## <span data-ttu-id="be21b-109">Настройка</span><span class="sxs-lookup"><span data-stu-id="be21b-109">Setup</span></span>

1. <span data-ttu-id="be21b-110">Отправка приложения в бизнес-линию или отправка настраиваемого приложения в клиент Intune.</span><span class="sxs-lookup"><span data-stu-id="be21b-110">Upload an app to a Line of Business, or upload a custom app to your Intune tenant.</span></span> <span data-ttu-id="be21b-111">См. также: [управление корпоративными приложениями.](https://docs.microsoft.com/windows/client-management/mdm/enterprise-app-management)</span><span class="sxs-lookup"><span data-stu-id="be21b-111">See also: [Enterprise app management](https://docs.microsoft.com/windows/client-management/mdm/enterprise-app-management).</span></span>

2. <span data-ttu-id="be21b-112">[Назначьте приложение группе.](https://docs.microsoft.com/mem/intune/apps/apps-deploy)</span><span class="sxs-lookup"><span data-stu-id="be21b-112">[Assign your app to a group](https://docs.microsoft.com/mem/intune/apps/apps-deploy).</span></span> <span data-ttu-id="be21b-113">В зависимости от того, какой тип назначения вы выберете, приложение может быть доставлено автоматически или доступно для быстрой оттягивки, если у вас есть выбор приложений.</span><span class="sxs-lookup"><span data-stu-id="be21b-113">Based on the assignment type you choose you can have the app delivered automatically or available to be readily pulled down if you have a selection of apps.</span></span> 

> [!NOTE] 
> <span data-ttu-id="be21b-114">При создании пакета appx обязательно учитывайте архитектуру устройств, на которых вы развертываетсяе.</span><span class="sxs-lookup"><span data-stu-id="be21b-114">When building your appx bundle make sure to account for including the architecture for the device(s) that you are deploying to.</span></span> <span data-ttu-id="be21b-115">HoloLens 2 — ARM64, а HoloLens (1-е поколения) — x86.</span><span class="sxs-lookup"><span data-stu-id="be21b-115">HoloLens 2 is ARM64, and HoloLens (1st Gen) is x86.</span></span> <span data-ttu-id="be21b-116">Если вы планируете разнородную среду устройств, вы можете включить оба пакета приложений.</span><span class="sxs-lookup"><span data-stu-id="be21b-116">You may include both in a single appx bundle if you plan on having a mixed devices environment.</span></span>

## <span data-ttu-id="be21b-117">Типы назначений</span><span class="sxs-lookup"><span data-stu-id="be21b-117">Assignment types</span></span>

<span data-ttu-id="be21b-118">Если вы хотите, чтобы ваше приложение автоматически устанавливалось на \*\*\*\* устройстве после регистрации, необходимо выбрать обязательное для этой группы.</span><span class="sxs-lookup"><span data-stu-id="be21b-118">If you prefer your app to be automatically installed on the device after enrollment, you should select **Required** for that group(s).</span></span>
<span data-ttu-id="be21b-119">Если вы хотите сделать приложение доступным для скачивания на портале компании, выберите "Доступно **для зарегистрированных устройств".**</span><span class="sxs-lookup"><span data-stu-id="be21b-119">If you prefer to make your app available for download to those enrolled through the company portal, select **Available for enrolled devices**.</span></span>


## <span data-ttu-id="be21b-120">Интерфейс конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="be21b-120">End User Experience</span></span>

<span data-ttu-id="be21b-121">После настройки конфигурации в Intune вы будете готовы к тому, чтобы конечные пользователи получили выбранные приложения.</span><span class="sxs-lookup"><span data-stu-id="be21b-121">After you have set up configuration on Intune you are ready for end users to recieve your selected apps.</span></span>

<span data-ttu-id="be21b-122">Выполните следующие действия, чтобы автоматически получить приложения:</span><span class="sxs-lookup"><span data-stu-id="be21b-122">Follow these steps to automatically get your app(s):</span></span>
1. <span data-ttu-id="be21b-123">Зарегистрите свое устройство в клиенте.</span><span class="sxs-lookup"><span data-stu-id="be21b-123">Enroll your device with your tenant.</span></span> 
2. <span data-ttu-id="be21b-124">После регистрации устройства вы должны получить приложение на своем устройстве.</span><span class="sxs-lookup"><span data-stu-id="be21b-124">Once your device has completed enrollment, you should receive the app on your device.</span></span> 
3. <span data-ttu-id="be21b-125">Если вы не видите приложение немедленно, перейдите к сведениям о работе учетных записей параметров или учебному зачету и прокрутите вниз, чтобы просмотреть сведения о состоянии \*\*\*\*  >  \*\*\*\*  >  \*\*\*\*  >  \*\*\*\* установленного приложения.</span><span class="sxs-lookup"><span data-stu-id="be21b-125">If you are not seeing you app immediately, go to **Settings** > **Accounts** > **Work or School** > **youraccount** Info, and scroll down to see information on installed app status.</span></span>

<span data-ttu-id="be21b-126">Как добраться до приложений с помощью портала компании:</span><span class="sxs-lookup"><span data-stu-id="be21b-126">How to get to apps through the Company Portal:</span></span>
1. <span data-ttu-id="be21b-127">Откройте меню **"Пуск"** и выберите **Microsoft Store.**</span><span class="sxs-lookup"><span data-stu-id="be21b-127">Open the **Start Menu** and select **Microsoft Store**.</span></span> 
2. <span data-ttu-id="be21b-128">**Найди "Портал компании"** и скачайте приложение.</span><span class="sxs-lookup"><span data-stu-id="be21b-128">Search for **Company Portal** and download the app.</span></span>
3. <span data-ttu-id="be21b-129">Войте в свою учетную запись.</span><span class="sxs-lookup"><span data-stu-id="be21b-129">Sign into your account.</span></span>
4. <span data-ttu-id="be21b-130">Выберите приложение, которое вы хотите получить, и скачайте его.</span><span class="sxs-lookup"><span data-stu-id="be21b-130">Select the app you wish to receive and download it.</span></span>

> [!Tip]
> <span data-ttu-id="be21b-131">Узнайте больше об [автоматической установке портала](https://docs.microsoft.com/mem/intune/apps/company-portal-app) компании, развертывании приложений и управлении приложениями [в Intune.](https://docs.microsoft.com/mem/intune/fundamentals/windows-holographic-for-business#deploy-and-manage-apps)</span><span class="sxs-lookup"><span data-stu-id="be21b-131">Learn more about [auto-installing the Company Portal](https://docs.microsoft.com/mem/intune/apps/company-portal-app) and [deploying and managing apps in Intune](https://docs.microsoft.com/mem/intune/fundamentals/windows-holographic-for-business#deploy-and-manage-apps).</span></span>
