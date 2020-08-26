---
title: Требования к лицензиям
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
ms.openlocfilehash: 3ac86512755620ebb6159dd4d845b488e203dbad
ms.sourcegitcommit: 238d41844116ab94d347a2ffd0fbfa18b8a81947
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/24/2020
ms.locfileid: "10956765"
---
# <span data-ttu-id="78893-102">Требования к лицензиям</span><span class="sxs-lookup"><span data-stu-id="78893-102">License requirements</span></span>

## <span data-ttu-id="78893-103">Руководство по лицензированию управления мобильными устройствами (MDM)</span><span class="sxs-lookup"><span data-stu-id="78893-103">Mobile Device Management (MDM) Licenses Guidance</span></span>

<span data-ttu-id="78893-104">Если вы планируете управлять устройствами HoloLens, вам потребуется Azure AD и MDM.</span><span class="sxs-lookup"><span data-stu-id="78893-104">If you plan on managing your HoloLens devices, you will need Azure AD and an MDM.</span></span> <span data-ttu-id="78893-105">Служба Active Directory (AD) не используется для управления устройствами HoloLens.</span><span class="sxs-lookup"><span data-stu-id="78893-105">Active Director (AD) cannot be used to manage HoloLens devices.</span></span>
<span data-ttu-id="78893-106">Если вы планируете использовать систему MDM, отличную от Intune, потребуются [лицензии Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis).</span><span class="sxs-lookup"><span data-stu-id="78893-106">If you plan on using an MDM other than Intune, an [Azure Active Directory Licenses](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) is required.</span></span>
<span data-ttu-id="78893-107">Если вы планируете использовать Intune в качестве MDM, [здесь](https://docs.microsoft.com/intune/fundamentals/licenses) представлен список наборов, включающих лицензии Intune.</span><span class="sxs-lookup"><span data-stu-id="78893-107">If you plan on using Intune as your MDM,  [here](https://docs.microsoft.com/intune/fundamentals/licenses) are a list of suites that includes Intune licenses.</span></span> **<span data-ttu-id="78893-108">Обратите внимание, что Azure AD входит в большинство этих наборов.</span><span class="sxs-lookup"><span data-stu-id="78893-108">Please note that Azure AD is included in the majority of these suites.</span></span>**

## <span data-ttu-id="78893-109">Определение лицензий, необходимых для вашего сценария и продуктов</span><span class="sxs-lookup"><span data-stu-id="78893-109">Identify the licenses needed for your scenario and products</span></span>

### <span data-ttu-id="78893-110">Требования к лицензиям HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="78893-110">HoloLens (1st gen) Licenses Requirements</span></span>

<span data-ttu-id="78893-111">Возможно, вам потребуется обновить устройство HoloLens 1-го поколения до Windows Holographic for Business.</span><span class="sxs-lookup"><span data-stu-id="78893-111">You may need to upgrade your HoloLens (1st gen) device to Windows Holographic for Business.</span></span> <span data-ttu-id="78893-112">(См. [Коммерческие функции HoloLens](holoLens-commercial-features.md#feature-comparison-between-editions) для определения необходимости обновления).</span><span class="sxs-lookup"><span data-stu-id="78893-112">(See [HoloLens commercial features](holoLens-commercial-features.md#feature-comparison-between-editions) to determine if you need to upgrade).</span></span>

 <span data-ttu-id="78893-113">Если это так, вам нужно будет сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="78893-113">If so, you will need to do the following:</span></span>

- <span data-ttu-id="78893-114">Получить XML-файл лицензии HoloLens Enterprise</span><span class="sxs-lookup"><span data-stu-id="78893-114">Acquire a HoloLens Enterprise license XML file</span></span>
- <span data-ttu-id="78893-115">Примените файл XML к HoloLens.</span><span class="sxs-lookup"><span data-stu-id="78893-115">Apply the XML file to the HoloLens.</span></span> <span data-ttu-id="78893-116">Это можно сделать с помощью [пакета подготовки](hololens-provisioning.md) или с помощью [диспетчера мобильных устройств](https://docs.microsoft.com/intune/configuration/holographic-upgrade)</span><span class="sxs-lookup"><span data-stu-id="78893-116">You can do this through a [Provisioning package](hololens-provisioning.md) or through your [Mobile Device Manager](https://docs.microsoft.com/intune/configuration/holographic-upgrade)</span></span>

### <span data-ttu-id="78893-117">Требования к лицензии для Удаленной поддержки</span><span class="sxs-lookup"><span data-stu-id="78893-117">Remote Assist License Requirements</span></span>

<span data-ttu-id="78893-118">Убедитесь, что у вас есть требуемые лицензии и устройство.</span><span class="sxs-lookup"><span data-stu-id="78893-118">Make sure you have the required licensing and device.</span></span> <span data-ttu-id="78893-119">Обновленные требования к лицензиям и продукту см. [здесь](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements).</span><span class="sxs-lookup"><span data-stu-id="78893-119">Updated licensing and product requirements can be found [here](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements).</span></span>

1. [<span data-ttu-id="78893-120">Лицензия для Удаленной поддержки</span><span class="sxs-lookup"><span data-stu-id="78893-120">Remote Assist License</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist)
    1. <span data-ttu-id="78893-121">Или воспользуйтесь [пробной версией удаленной поддержки](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist)</span><span class="sxs-lookup"><span data-stu-id="78893-121">Or try a [Remote Assist trial](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist)</span></span>
1. [<span data-ttu-id="78893-122">Teams Freemium/Teams</span><span class="sxs-lookup"><span data-stu-id="78893-122">Teams Freemium/Teams</span></span>](https://products.office.com/microsoft-teams/free)
1. [<span data-ttu-id="78893-123">Лицензия для Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="78893-123">Azure Active Directory (Azure AD) License</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)

<span data-ttu-id="78893-124">Если вы планируете реализовать **[этот межклиентный сценарий](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants)**, вам может потребоваться лицензия на Информационные барьеры.</span><span class="sxs-lookup"><span data-stu-id="78893-124">If you plan on implementing **[this cross-tenant scenario](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants)**, you may need an Information Barriers license.</span></span> <span data-ttu-id="78893-125">Чтобы определить, требуется ли лицензия на Информационные барьеры, ознакомьтесь с [этой статьей](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary).</span><span class="sxs-lookup"><span data-stu-id="78893-125">Please see [this article](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary) to determine if an Information Barrier License is required.</span></span>

### <span data-ttu-id="78893-126">Требования к лицензии для руководств</span><span class="sxs-lookup"><span data-stu-id="78893-126">Guides License Requirements</span></span>

<span data-ttu-id="78893-127">Обновленные требования к лицензиям и устройству см. [здесь](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements).</span><span class="sxs-lookup"><span data-stu-id="78893-127">Updated licensing and device requirements can be found [here](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements).</span></span>

1. [<span data-ttu-id="78893-128">Лицензия для Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="78893-128">Azure Active Directory (Azure AD) License</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
1. [<span data-ttu-id="78893-129">Power BI</span><span class="sxs-lookup"><span data-stu-id="78893-129">Power BI</span></span>](https://powerbi.microsoft.com/desktop/)
1. [<span data-ttu-id="78893-130">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="78893-130">Guides</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup)
