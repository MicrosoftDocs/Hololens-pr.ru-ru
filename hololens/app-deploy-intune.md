---
title: Intune и Корпоративный портал
description: Узнайте, как настроить, назначить и создать удобство работы пользователей с помощью Intune, управления мобильными устройствами и корпоративного портала.
keywords: Intune, Управление приложениями, приложение, корпоративный портал, портал, hololens
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
ms.openlocfilehash: b192732f5e7edffaa1d0ab081454e4034c416191
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113635506"
---
# <a name="intune--company-portal"></a><span data-ttu-id="fb042-104">Intune и Корпоративный портал</span><span class="sxs-lookup"><span data-stu-id="fb042-104">Intune & Company Portal</span></span>

<span data-ttu-id="fb042-105">с помощью управления мобильными устройствами (MDM) вы можете использовать собственные пользовательские приложения с помощью [Microsoft Endpoint Manager (Intune)](/intune/windows-holographic-for-business) , чтобы развернуть его непосредственно на HoloLens устройствах.</span><span class="sxs-lookup"><span data-stu-id="fb042-105">With Mobile Device Management (MDM), you can use your own custom apps through [Microsoft Endpoint Manager (Intune)](/intune/windows-holographic-for-business) to deploy it directly to your HoloLens devices.</span></span> <span data-ttu-id="fb042-106">Microsoft Intune — это облачная служба, в которой основное внимание уделяется управлению мобильными устройствами (MDM) и управлению мобильными приложениями (MAM).</span><span class="sxs-lookup"><span data-stu-id="fb042-106">Microsoft Intune is a cloud-based service that focuses on mobile device management (MDM) and mobile application management (MAM).</span></span> <span data-ttu-id="fb042-107">Intune входит в состав пакета Microsoft [Enterprise Mobility + Security (EMS)](https://www.microsoft.com/microsoft-365/enterprise-mobility-security) и позволяет пользователям быть продуктивными, обеспечивая защиту данных организации.</span><span class="sxs-lookup"><span data-stu-id="fb042-107">Intune is included in Microsoft's [Enterprise Mobility + Security (EMS) suite](https://www.microsoft.com/microsoft-365/enterprise-mobility-security), and enables users to be productive while keeping your organization data protected.</span></span> <span data-ttu-id="fb042-108">Дополнительные сведения о Intune см. в статье [что такое Intune](/mem/intune/fundamentals/what-is-intune).</span><span class="sxs-lookup"><span data-stu-id="fb042-108">To learn more about Intune, read [What is Intune](/mem/intune/fundamentals/what-is-intune).</span></span>

## <a name="setup"></a><span data-ttu-id="fb042-109">Настройка</span><span class="sxs-lookup"><span data-stu-id="fb042-109">Setup</span></span>

1. <span data-ttu-id="fb042-110">Upload приложение в отрасль или передать пользовательское приложение в клиент Intune.</span><span class="sxs-lookup"><span data-stu-id="fb042-110">Upload an app to a Line of Business, or upload a custom app to your Intune tenant.</span></span> <span data-ttu-id="fb042-111">см. также: [Enterprise управления приложениями](/windows/client-management/mdm/enterprise-app-management).</span><span class="sxs-lookup"><span data-stu-id="fb042-111">See also: [Enterprise app management](/windows/client-management/mdm/enterprise-app-management).</span></span>

2. <span data-ttu-id="fb042-112">[Назначьте свое приложение группе](/mem/intune/apps/apps-deploy).</span><span class="sxs-lookup"><span data-stu-id="fb042-112">[Assign your app to a group](/mem/intune/apps/apps-deploy).</span></span> <span data-ttu-id="fb042-113">В зависимости от выбранного типа назначения приложение может быть доставлено автоматически или доступно, если у вас есть выбранные приложения.</span><span class="sxs-lookup"><span data-stu-id="fb042-113">Based on the assignment type you choose, the app can be delivered automatically or available to be readily pulled down if you have a selection of apps.</span></span>

> [!NOTE]
> <span data-ttu-id="fb042-114">При сборке пакета Appx необходимо учитывать, включая архитектуру для устройств, на которые выполняется развертывание.</span><span class="sxs-lookup"><span data-stu-id="fb042-114">When building your appx bundle make sure to account for including the architecture for the device(s) that you are deploying to.</span></span> <span data-ttu-id="fb042-115">HoloLens 2 ARM64, а HoloLens (1 Gen) — x86.</span><span class="sxs-lookup"><span data-stu-id="fb042-115">HoloLens 2 is ARM64, and HoloLens (1st Gen) is x86.</span></span> <span data-ttu-id="fb042-116">Если вы планируете использовать среду со смешанными устройствами, вы можете включить оба варианта в один пакет Appx.</span><span class="sxs-lookup"><span data-stu-id="fb042-116">You may include both in a single appx bundle if you plan on having a mixed devices environment.</span></span>

## <a name="assignment-types"></a><span data-ttu-id="fb042-117">Типы назначений</span><span class="sxs-lookup"><span data-stu-id="fb042-117">Assignment types</span></span>

<span data-ttu-id="fb042-118">Чтобы приложение было автоматически установлено на устройстве после регистрации, необходимо выбрать параметр **требуется** для этих групп.</span><span class="sxs-lookup"><span data-stu-id="fb042-118">To have your app to be automatically installed on the device after enrollment, you should select **Required** for that group(s).</span></span>
<span data-ttu-id="fb042-119">Чтобы сделать приложение доступным для загрузки на устройства, зарегистрированные на корпоративном портале, выберите **доступно для зарегистрированных устройств**.</span><span class="sxs-lookup"><span data-stu-id="fb042-119">To make your app available for download to devices enrolled through the company portal, select **Available for enrolled devices**.</span></span>

## <a name="end-user-experience"></a><span data-ttu-id="fb042-120">Проверьте взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="fb042-120">End-User Experience</span></span>

<span data-ttu-id="fb042-121">После настройки конфигурации в Intune можно приступать к получению выбранных приложений конечными пользователями.</span><span class="sxs-lookup"><span data-stu-id="fb042-121">After you have set up configuration on Intune, you are ready for end users to receive your selected apps.</span></span>

<span data-ttu-id="fb042-122">Выполните следующие действия, чтобы автоматически получить ваши приложения:</span><span class="sxs-lookup"><span data-stu-id="fb042-122">Follow these steps to automatically get your app(s):</span></span>

1. <span data-ttu-id="fb042-123">Зарегистрируйте устройство в клиенте.</span><span class="sxs-lookup"><span data-stu-id="fb042-123">Enroll your device with your tenant.</span></span>
2. <span data-ttu-id="fb042-124">После завершения регистрации устройства вы должны получить приложение на устройстве.</span><span class="sxs-lookup"><span data-stu-id="fb042-124">Once your device has completed enrollment, you should receive the app on your device.</span></span>
3. <span data-ttu-id="fb042-125">если вы не видите приложение немедленно, перейдите в раздел **Параметры**  >  **учетные записи**  >  **рабочие или учебные**  >  данные *учетной записи* и прокрутите вниз, чтобы просмотреть сведения о состоянии установленного приложения.</span><span class="sxs-lookup"><span data-stu-id="fb042-125">If you are not seeing you app immediately, go to **Settings** > **Accounts** > **Work or School** > *your account* Info, and scroll down to see information on installed app status.</span></span>

<span data-ttu-id="fb042-126">как перейти к приложениям с помощью Корпоративный портал:</span><span class="sxs-lookup"><span data-stu-id="fb042-126">How to get to apps through the Company Portal:</span></span>

1. <span data-ttu-id="fb042-127">Откройте **меню Пуск** и выберите **Microsoft Store**.</span><span class="sxs-lookup"><span data-stu-id="fb042-127">Open the **Start Menu** and select **Microsoft Store**.</span></span>
2. <span data-ttu-id="fb042-128">найдите **Корпоративный портал** и скачайте приложение.</span><span class="sxs-lookup"><span data-stu-id="fb042-128">Search for **Company Portal** and download the app.</span></span>
3. <span data-ttu-id="fb042-129">Войдите в свою учетную запись.</span><span class="sxs-lookup"><span data-stu-id="fb042-129">Sign into your account.</span></span>
4. <span data-ttu-id="fb042-130">Выберите приложение, которое вы хотите получить, и скачайте его.</span><span class="sxs-lookup"><span data-stu-id="fb042-130">Select the app you wish to receive and download it.</span></span>

> [!Tip]
> <span data-ttu-id="fb042-131">дополнительные сведения об [автоматической установке Корпоративный портал](/mem/intune/apps/company-portal-app) и [развертывании приложений и управлении ими в Intune](/mem/intune/fundamentals/windows-holographic-for-business#deploy-and-manage-apps).</span><span class="sxs-lookup"><span data-stu-id="fb042-131">Learn more about [auto-installing the Company Portal](/mem/intune/apps/company-portal-app) and [deploying and managing apps in Intune](/mem/intune/fundamentals/windows-holographic-for-business#deploy-and-manage-apps).</span></span>
