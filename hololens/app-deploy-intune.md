---
title: Intune и портал компании
description: Intune, Управление приложениями, приложение, портал компании, портал
keywords: Intune, Управление приложениями, приложение, портал компании, портал, hololens
author: evmill
ms.author: v-evmill
ms.reviewer: tagran
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
ms.openlocfilehash: 5fc369caa2e5e26c91c07f9270c3984177507dbd
ms.sourcegitcommit: 72ff3174b34d2acaf72547b7d981c66aef8fa82f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11009467"
---
# <span data-ttu-id="19909-104">Intune и корпоративный портал</span><span class="sxs-lookup"><span data-stu-id="19909-104">Intune & Company Portal</span></span>

<span data-ttu-id="19909-105">С помощью управления мобильными устройствами (MDM) вы можете использовать собственные приложения с помощью [Microsoft Endpoint Manager (Intune)](https://docs.microsoft.com/intune/windows-holographic-for-business) , чтобы развернуть его непосредственно на устройствах HoloLens.</span><span class="sxs-lookup"><span data-stu-id="19909-105">With Mobile Device Management (MDM), you can use your own custom apps through [Microsoft Endpoint Manager (Intune)](https://docs.microsoft.com/intune/windows-holographic-for-business) to deploy it directly to your HoloLens devices.</span></span> <span data-ttu-id="19909-106">Microsoft Intune — это облачная служба, ориентированная на управление мобильными устройствами (MDM) и управление мобильными приложениями (MAM).</span><span class="sxs-lookup"><span data-stu-id="19909-106">Microsoft Intune is a cloud-based service that focuses on mobile device management (MDM) and mobile application management (MAM).</span></span> <span data-ttu-id="19909-107">Intune входит в состав[корпоративного семейства Microsoft Mobility + Security + (EMS)](https://www.microsoft.com/microsoft-365/enterprise-mobility-security)и позволяет пользователям работать эффективнее с сохранением защиты данных Организации.</span><span class="sxs-lookup"><span data-stu-id="19909-107">Intune is included in Microsoft's[Enterprise Mobility + Security (EMS) suite](https://www.microsoft.com/microsoft-365/enterprise-mobility-security), and enables users to be productive while keeping your organization data protected.</span></span> <span data-ttu-id="19909-108">Чтобы узнать больше о Intune, ознакомьтесь со статьей [Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune).</span><span class="sxs-lookup"><span data-stu-id="19909-108">To learn more about Intune, please read [What is Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune).</span></span>

## <span data-ttu-id="19909-109">Настройка</span><span class="sxs-lookup"><span data-stu-id="19909-109">Setup</span></span>

1. <span data-ttu-id="19909-110">Добавьте приложение в бизнес-строку или добавьте настраиваемое приложение в клиент Intune.</span><span class="sxs-lookup"><span data-stu-id="19909-110">Upload an app to a Line of Business, or upload a custom app to your Intune tenant.</span></span> <span data-ttu-id="19909-111">Дополнительные сведения: [Управление корпоративными приложениями](https://docs.microsoft.com/windows/client-management/mdm/enterprise-app-management).</span><span class="sxs-lookup"><span data-stu-id="19909-111">See also: [Enterprise app management](https://docs.microsoft.com/windows/client-management/mdm/enterprise-app-management).</span></span>

2. <span data-ttu-id="19909-112">[Назначьте свое приложение группе](https://docs.microsoft.com/mem/intune/apps/apps-deploy).</span><span class="sxs-lookup"><span data-stu-id="19909-112">[Assign your app to a group](https://docs.microsoft.com/mem/intune/apps/apps-deploy).</span></span> <span data-ttu-id="19909-113">В зависимости от выбранного типа задания приложение может быть автоматически доставлено или доступно, если вы выбрали приложения.</span><span class="sxs-lookup"><span data-stu-id="19909-113">Based on the assignment type you choose you can have the app delivered automatically or available to be readily pulled down if you have a selection of apps.</span></span> 

> [!NOTE] 
> <span data-ttu-id="19909-114">При построении пакета Appx убедитесь, что в него включены архитектура для устройств, на которые вы развертываете.</span><span class="sxs-lookup"><span data-stu-id="19909-114">When building your appx bundle make sure to account for including the architecture for the device(s) that you are deploying to.</span></span> <span data-ttu-id="19909-115">HoloLens 2 является ARM64, а HoloLens (1-ом) — x86.</span><span class="sxs-lookup"><span data-stu-id="19909-115">HoloLens 2 is ARM64, and HoloLens (1st Gen) is x86.</span></span> <span data-ttu-id="19909-116">Если вы планируете использовать смешанную среду устройств, вы можете включить оба пакета Appx в один.</span><span class="sxs-lookup"><span data-stu-id="19909-116">You may include both in a single appx bundle if you plan on having a mixed devices environment.</span></span>

## <span data-ttu-id="19909-117">Типы назначений</span><span class="sxs-lookup"><span data-stu-id="19909-117">Assignment types</span></span>

<span data-ttu-id="19909-118">Если вы предпочитаете, чтобы приложение автоматически устанавливалось на устройстве после регистрации, необходимо выбрать параметр **требуется** для этой группы (-ов).</span><span class="sxs-lookup"><span data-stu-id="19909-118">If you prefer your app to be automatically installed on the device after enrollment, you should select **Required** for that group(s).</span></span>
<span data-ttu-id="19909-119">Если вы хотите, чтобы приложение было доступно для загрузки на те, которые зарегистрированы на портале компании, выберите вариант **доступно для зарегистрированных устройств**.</span><span class="sxs-lookup"><span data-stu-id="19909-119">If you prefer to make your app available for download to those enrolled through the company portal, select **Available for enrolled devices**.</span></span>


## <span data-ttu-id="19909-120">Работа с конечными пользователями</span><span class="sxs-lookup"><span data-stu-id="19909-120">End User Experience</span></span>

<span data-ttu-id="19909-121">После того как вы настроили конфигурацию для Intune, конечные пользователи смогут получить доступ к выбранным приложениям.</span><span class="sxs-lookup"><span data-stu-id="19909-121">After you have set up configuration on Intune you are ready for end users to recieve your selected apps.</span></span>

<span data-ttu-id="19909-122">Выполните указанные ниже действия, чтобы автоматически загрузить приложения.</span><span class="sxs-lookup"><span data-stu-id="19909-122">Follow these steps to automatically get your app(s):</span></span>
1. <span data-ttu-id="19909-123">Регистрация устройства в клиенте.</span><span class="sxs-lookup"><span data-stu-id="19909-123">Enroll your device with your tenant.</span></span> 
2. <span data-ttu-id="19909-124">После того как устройство завершит регистрацию, вы должны получить приложение на своем устройстве.</span><span class="sxs-lookup"><span data-stu-id="19909-124">Once your device has completed enrollment, you should receive the app on your device.</span></span> 
3. <span data-ttu-id="19909-125">Если вы не видите приложение немедленно, перейдите в раздел **Параметры**  >  **учетные записи**  >  **рабочей или School**  >  **youraccount** info и прокрутите вниз, чтобы просмотреть сведения о состоянии установленного приложения.</span><span class="sxs-lookup"><span data-stu-id="19909-125">If you are not seeing you app immediately, go to **Settings** > **Accounts** > **Work or School** > **youraccount** Info, and scroll down to see information on installed app status.</span></span>

<span data-ttu-id="19909-126">Как получить доступ к приложениям на портале компании:</span><span class="sxs-lookup"><span data-stu-id="19909-126">How to get to apps through the Company Portal:</span></span>
1. <span data-ttu-id="19909-127">Откройте **меню "Пуск** " и выберите **Microsoft Store**.</span><span class="sxs-lookup"><span data-stu-id="19909-127">Open the **Start Menu** and select **Microsoft Store**.</span></span> 
2. <span data-ttu-id="19909-128">Выполните поиск **портала компании** и скачайте приложение.</span><span class="sxs-lookup"><span data-stu-id="19909-128">Search for **Company Portal** and download the app.</span></span>
3. <span data-ttu-id="19909-129">Войдите в свою учетную запись.</span><span class="sxs-lookup"><span data-stu-id="19909-129">Sign into your account.</span></span>
4. <span data-ttu-id="19909-130">Выберите приложение, которое вы хотите получить и скачать.</span><span class="sxs-lookup"><span data-stu-id="19909-130">Select the app you wish to receive and download it.</span></span>

> [!Tip]
> <span data-ttu-id="19909-131">Узнайте больше о том, как [автоматически установить портал компании](https://docs.microsoft.com/mem/intune/apps/company-portal-app) , а также [развертывать приложения и управлять ими в Intune](https://docs.microsoft.com/mem/intune/fundamentals/windows-holographic-for-business#deploy-and-manage-apps).</span><span class="sxs-lookup"><span data-stu-id="19909-131">Learn more about [auto-installing the Company Portal](https://docs.microsoft.com/mem/intune/apps/company-portal-app) and [deploying and managing apps in Intune](https://docs.microsoft.com/mem/intune/fundamentals/windows-holographic-for-business#deploy-and-manage-apps).</span></span>
