---
title: Лицензии для развертывания смешанной реальности
description: ''
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
ms.openlocfilehash: 0da2a2337b3b1f361ffbb698607f304efbf6d193
ms.sourcegitcommit: f3cda6c6b3bfb7ba4be5f4da66d8ed5b03ca807d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2020
ms.locfileid: "10830143"
---
# <span data-ttu-id="6f9ba-102">Определение необходимых лицензий</span><span class="sxs-lookup"><span data-stu-id="6f9ba-102">Determine what licenses you need</span></span>

## <span data-ttu-id="6f9ba-103">Руководство по лицензированию управления мобильными устройствами (MDM)</span><span class="sxs-lookup"><span data-stu-id="6f9ba-103">Mobile Device Management (MDM) Licenses Guidance</span></span>

<span data-ttu-id="6f9ba-104">Если вы планируете управлять устройствами HoloLens, вам потребуется Azure AD и MDM.</span><span class="sxs-lookup"><span data-stu-id="6f9ba-104">If you plan on managing your HoloLens devices, you will need Azure AD and an MDM.</span></span> <span data-ttu-id="6f9ba-105">Служба Active Directory (AD) не используется для управления устройствами HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6f9ba-105">Active Director (AD) cannot be used to manage HoloLens devices.</span></span>
<span data-ttu-id="6f9ba-106">Если вы планируете использовать систему MDM, отличную от Intune, потребуются [лицензии Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis).</span><span class="sxs-lookup"><span data-stu-id="6f9ba-106">If you plan on using an MDM other than Intune, an [Azure Active Directory Licenses](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) is required.</span></span>
<span data-ttu-id="6f9ba-107">Если вы планируете использовать Intune в качестве MDM, [здесь](https://docs.microsoft.com/intune/fundamentals/licenses) представлен список наборов, включающих лицензии Intune.</span><span class="sxs-lookup"><span data-stu-id="6f9ba-107">If you plan on using Intune as your MDM,  [here](https://docs.microsoft.com/intune/fundamentals/licenses) are a list of suites that includes Intune licenses.</span></span> **<span data-ttu-id="6f9ba-108">Обратите внимание, что Azure AD входит в большинство этих наборов.</span><span class="sxs-lookup"><span data-stu-id="6f9ba-108">Please note that Azure AD is included in the majority of these suites.</span></span>**

## <span data-ttu-id="6f9ba-109">Определение лицензий, необходимых для вашего сценария и продуктов</span><span class="sxs-lookup"><span data-stu-id="6f9ba-109">Identify the licenses needed for your scenario and products</span></span>

### <span data-ttu-id="6f9ba-110">Требования к лицензиям на HoloLens</span><span class="sxs-lookup"><span data-stu-id="6f9ba-110">HoloLens Licenses Requirements</span></span>

<span data-ttu-id="6f9ba-111">Возможно, вам потребуется обновить устройство HoloLens 1-го поколения до Windows Holographic для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6f9ba-111">You may need to upgrade your HoloLens 1st Gen Device to Windows Holographic for Business.</span></span> <span data-ttu-id="6f9ba-112">(См. [Коммерческие функции HoloLens](holoLens-commercial-features.md#feature-comparison-between-editions) для определения необходимости обновления).</span><span class="sxs-lookup"><span data-stu-id="6f9ba-112">(See [HoloLens commercial features](holoLens-commercial-features.md#feature-comparison-between-editions) to determine if you need to upgrade).</span></span>

 <span data-ttu-id="6f9ba-113">Если это так, вам нужно будет сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="6f9ba-113">If so, you will need to do the following:</span></span>

- <span data-ttu-id="6f9ba-114">Получить XML-файл лицензии HoloLens Enterprise</span><span class="sxs-lookup"><span data-stu-id="6f9ba-114">Acquire a HoloLens Enterprise license XML file</span></span>
- <span data-ttu-id="6f9ba-115">Примените файл XML к HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6f9ba-115">Apply the XML file to the HoloLens.</span></span> <span data-ttu-id="6f9ba-116">Это можно сделать с помощью [пакета подготовки](hololens-provisioning.md) или с помощью [диспетчера мобильных устройств](https://docs.microsoft.com/intune/configuration/holographic-upgrade)</span><span class="sxs-lookup"><span data-stu-id="6f9ba-116">You can do this through a [Provisioning package](hololens-provisioning.md) or through your [Mobile Device Manager](https://docs.microsoft.com/intune/configuration/holographic-upgrade)</span></span>

### <span data-ttu-id="6f9ba-117">Требования к лицензии для Удаленной поддержки</span><span class="sxs-lookup"><span data-stu-id="6f9ba-117">Remote Assist License Requirements</span></span>

<span data-ttu-id="6f9ba-118">Убедитесь, что у вас есть требуемые лицензии и устройство.</span><span class="sxs-lookup"><span data-stu-id="6f9ba-118">Make sure you have the required licensing and device.</span></span> <span data-ttu-id="6f9ba-119">Обновленные требования к лицензиям и продукту см. [здесь](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements).</span><span class="sxs-lookup"><span data-stu-id="6f9ba-119">Updated licensing and product requirements can be found [here](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements).</span></span>

1. [<span data-ttu-id="6f9ba-120">Лицензия для Удаленной поддержки</span><span class="sxs-lookup"><span data-stu-id="6f9ba-120">Remote Assist License</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist)
1. [<span data-ttu-id="6f9ba-121">Teams Freemium/Teams</span><span class="sxs-lookup"><span data-stu-id="6f9ba-121">Teams Freemium/Teams</span></span>](https://products.office.com/microsoft-teams/free)
1. [<span data-ttu-id="6f9ba-122">Лицензия для Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="6f9ba-122">Azure Active Directory (Azure AD) License</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)

<span data-ttu-id="6f9ba-123">Если вы планируете реализовать **[этот межклиентный сценарий](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants)**, вам может потребоваться лицензия на Информационные барьеры.</span><span class="sxs-lookup"><span data-stu-id="6f9ba-123">If you plan on implementing **[this cross-tenant scenario](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants)**, you may need an Information Barriers license.</span></span> <span data-ttu-id="6f9ba-124">Чтобы определить, требуется ли лицензия на Информационные барьеры, ознакомьтесь с [этой статьей](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary).</span><span class="sxs-lookup"><span data-stu-id="6f9ba-124">Please see [this article](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary) to determine if an Information Barrier License is required.</span></span>

### <span data-ttu-id="6f9ba-125">Требования к лицензии для руководств</span><span class="sxs-lookup"><span data-stu-id="6f9ba-125">Guides License Requirements</span></span>

<span data-ttu-id="6f9ba-126">Обновленные требования к лицензиям и устройству см. [здесь](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements).</span><span class="sxs-lookup"><span data-stu-id="6f9ba-126">Updated licensing and device requirements can be found [here](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements).</span></span>

1. [<span data-ttu-id="6f9ba-127">Лицензия для Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="6f9ba-127">Azure Active Directory (Azure AD) License</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
1. [<span data-ttu-id="6f9ba-128">Power BI</span><span class="sxs-lookup"><span data-stu-id="6f9ba-128">Power BI</span></span>](https://powerbi.microsoft.com/desktop/)
1. [<span data-ttu-id="6f9ba-129">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="6f9ba-129">Guides</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup)
