---
title: Требования к лицензиям
description: Оставайтесь в курсе всех требований и рекомендаций по лицензированию для управления мобильными устройствами, HoloLens и Удаленной поддержки.
ms.prod: hololens
ms.sitesec: library
author: pawinfie
ms.author: pawinfie
audience: HoloLens
ms.topic: article
ms.localizationpriority: high
ms.date: 1/23/2020
ms.reviewer: ''
manager: bradke
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 2f7af532d2172dcaa6514ee11dbb0d6ab5631929
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283970"
---
# <span data-ttu-id="4e7ee-103">Требования к лицензиям</span><span class="sxs-lookup"><span data-stu-id="4e7ee-103">License requirements</span></span>

## <span data-ttu-id="4e7ee-104">Руководство по лицензированию управления мобильными устройствами (MDM)</span><span class="sxs-lookup"><span data-stu-id="4e7ee-104">Mobile Device Management (MDM) Licenses Guidance</span></span>

<span data-ttu-id="4e7ee-105">Если вы планируете управлять устройствами HoloLens, вам потребуется Azure AD и MDM.</span><span class="sxs-lookup"><span data-stu-id="4e7ee-105">If you plan on managing your HoloLens devices, you will need Azure AD and an MDM.</span></span> <span data-ttu-id="4e7ee-106">Служба Active Directory (AD) не используется для управления устройствами HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4e7ee-106">Active Director (AD) cannot be used to manage HoloLens devices.</span></span>
<span data-ttu-id="4e7ee-107">Если вы планируете использовать систему MDM, отличную от Intune, то потребуются [лицензии Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis).</span><span class="sxs-lookup"><span data-stu-id="4e7ee-107">If you plan on using an MDM other than Intune, an [Azure Active Directory Licenses](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) is required.</span></span>
<span data-ttu-id="4e7ee-108">Если вы планируете использовать Intune в качестве MDM, ознакомьтесь со [списком наборов,](https://docs.microsoft.com/intune/fundamentals/licenses) которые включают лицензии Intune.</span><span class="sxs-lookup"><span data-stu-id="4e7ee-108">If you plan on using Intune as your MDM, read up on the [list of suites](https://docs.microsoft.com/intune/fundamentals/licenses) that include Intune licenses.</span></span> **<span data-ttu-id="4e7ee-109">Обратите внимание, что Azure AD входит в большинство этих наборов.</span><span class="sxs-lookup"><span data-stu-id="4e7ee-109">Please note that Azure AD is included in the majority of these suites.</span></span>**

## <span data-ttu-id="4e7ee-110">Определение лицензий, необходимых для вашего сценария и продуктов</span><span class="sxs-lookup"><span data-stu-id="4e7ee-110">Identify the licenses needed for your scenario and products</span></span>

### <span data-ttu-id="4e7ee-111">Требования к лицензиям HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="4e7ee-111">HoloLens (1st gen) Licenses Requirements</span></span>

<span data-ttu-id="4e7ee-112">Возможно, вам потребуется обновить устройство HoloLens 1-го поколения до Windows Holographic for Business.</span><span class="sxs-lookup"><span data-stu-id="4e7ee-112">You may need to upgrade your HoloLens (1st gen) device to Windows Holographic for Business.</span></span> <span data-ttu-id="4e7ee-113">(См. [Коммерческие функции HoloLens](holoLens-commercial-features.md#feature-comparison-between-editions) для определения необходимости обновления).</span><span class="sxs-lookup"><span data-stu-id="4e7ee-113">(See [HoloLens commercial features](holoLens-commercial-features.md#feature-comparison-between-editions) to determine if you need to upgrade).</span></span>

 <span data-ttu-id="4e7ee-114">Если это так, вам нужно будет сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="4e7ee-114">If so, you will need to do the following:</span></span>

- <span data-ttu-id="4e7ee-115">Получить XML-файл лицензии HoloLens Enterprise</span><span class="sxs-lookup"><span data-stu-id="4e7ee-115">Acquire a HoloLens Enterprise license XML file</span></span>
- <span data-ttu-id="4e7ee-116">Примените файл XML к HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4e7ee-116">Apply the XML file to the HoloLens.</span></span> <span data-ttu-id="4e7ee-117">Это можно сделать с помощью [пакета подготовки](hololens-provisioning.md) или с помощью [диспетчера мобильных устройств](https://docs.microsoft.com/intune/configuration/holographic-upgrade)</span><span class="sxs-lookup"><span data-stu-id="4e7ee-117">You can do this through a [Provisioning package](hololens-provisioning.md) or through your [Mobile Device Manager](https://docs.microsoft.com/intune/configuration/holographic-upgrade)</span></span>

### <span data-ttu-id="4e7ee-118">Требования к лицензии для Удаленной поддержки</span><span class="sxs-lookup"><span data-stu-id="4e7ee-118">Remote Assist License Requirements</span></span>

<span data-ttu-id="4e7ee-119">Убедитесь, что у вас есть необходимые лицензии и устройство, которые можно проверить в [документации по требованиям.](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements)</span><span class="sxs-lookup"><span data-stu-id="4e7ee-119">Make sure you have the required licensing and device, which you can check in the [requirements](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements) documentation.</span></span>

1. [<span data-ttu-id="4e7ee-120">Лицензия для Удаленной поддержки</span><span class="sxs-lookup"><span data-stu-id="4e7ee-120">Remote Assist License</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist)
    1. <span data-ttu-id="4e7ee-121">Или воспользуйтесь [пробной версией удаленной поддержки](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist)</span><span class="sxs-lookup"><span data-stu-id="4e7ee-121">Or try a [Remote Assist trial](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist)</span></span>
1. [<span data-ttu-id="4e7ee-122">Teams Freemium/Teams</span><span class="sxs-lookup"><span data-stu-id="4e7ee-122">Teams Freemium/Teams</span></span>](https://products.office.com/microsoft-teams/free)
1. [<span data-ttu-id="4e7ee-123">Лицензия для Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="4e7ee-123">Azure Active Directory (Azure AD) License</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)

<span data-ttu-id="4e7ee-124">Если вы планируете реализовать **[этот межклиентный сценарий](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants)**, вам может потребоваться лицензия на Информационные барьеры.</span><span class="sxs-lookup"><span data-stu-id="4e7ee-124">If you plan on implementing **[this cross-tenant scenario](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants)**, you may need an Information Barriers license.</span></span> <span data-ttu-id="4e7ee-125">Чтобы определить, требуется ли лицензия на Информационные барьеры, ознакомьтесь с [этой статьей](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary).</span><span class="sxs-lookup"><span data-stu-id="4e7ee-125">Please see [this article](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary) to determine if an Information Barrier License is required.</span></span>

### <span data-ttu-id="4e7ee-126">Требования к лицензии для руководств</span><span class="sxs-lookup"><span data-stu-id="4e7ee-126">Guides License Requirements</span></span>

<span data-ttu-id="4e7ee-127">Проверьте [обновленные требования к лицензированию и устройству.](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements)</span><span class="sxs-lookup"><span data-stu-id="4e7ee-127">Check out the [updated licensing and device requirements](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements).</span></span>

1. [<span data-ttu-id="4e7ee-128">Лицензия для Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="4e7ee-128">Azure Active Directory (Azure AD) License</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
1. [<span data-ttu-id="4e7ee-129">Power BI</span><span class="sxs-lookup"><span data-stu-id="4e7ee-129">Power BI</span></span>](https://powerbi.microsoft.com/desktop/)
1. [<span data-ttu-id="4e7ee-130">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="4e7ee-130">Guides</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup)
