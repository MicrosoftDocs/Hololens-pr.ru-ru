---
title: Регистрация HoloLens в MDM
description: Регистрация HoloLens в системе управления мобильными устройствами (MDM) для упрощения управления несколькими устройствами.
ms.prod: hololens
ms.sitesec: library
ms.assetid: 2a9b3fca-8370-44ec-8b57-fb98b8d317b0
author: scooley
ms.author: scooley
ms.topic: article
ms.localizationpriority: medium
ms.date: 07/15/2019
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 054c4ded7496957671c055e3161a1297de7abc1a
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10828694"
---
# <span data-ttu-id="e6fc6-103">Регистрация HoloLens в MDM</span><span class="sxs-lookup"><span data-stu-id="e6fc6-103">Enroll HoloLens in MDM</span></span>

<span data-ttu-id="e6fc6-104">Вы можете управлять несколькими устройствами Microsoft HoloLens одновременно с помощью таких решений, как [Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business).</span><span class="sxs-lookup"><span data-stu-id="e6fc6-104">You can manage multiple Microsoft HoloLens devices simultaneously using solutions like [Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business).</span></span> <span data-ttu-id="e6fc6-105">Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-105">You will be able to manage settings, select apps to install and set security configurations tailored to your organization's need.</span></span> <span data-ttu-id="e6fc6-106">См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).</span><span class="sxs-lookup"><span data-stu-id="e6fc6-106">See [Manage devices running Windows Holographic with Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), the [configuration service providers (CSPs) that are supported in Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens), and the [policies supported by Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).</span></span>

> [!NOTE]
> <span data-ttu-id="e6fc6-107">Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="e6fc6-107">Mobile device management (MDM), including the VPN, Bitlocker, and kiosk mode features, is only available when you [upgrade to Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span></span>

## <span data-ttu-id="e6fc6-108">Требования</span><span class="sxs-lookup"><span data-stu-id="e6fc6-108">Requirements</span></span>

 <span data-ttu-id="e6fc6-109">Для управления устройствами HoloLens вашей организации потребуется настройка управления мобильными устройствами (MDM).</span><span class="sxs-lookup"><span data-stu-id="e6fc6-109">Your organization will need to have Mobile Device Management (MDM) set up in order to manage HoloLens devices.</span></span> <span data-ttu-id="e6fc6-110">Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-110">Your MDM provider can be Microsoft Intune or a 3rd party provider that uses Microsoft MDM APIs.</span></span>

## <span data-ttu-id="e6fc6-111">Автоматическая регистрация в MDM</span><span class="sxs-lookup"><span data-stu-id="e6fc6-111">Auto-enrollment in MDM</span></span>

<span data-ttu-id="e6fc6-112">Если ваша организация использует Azure Active Directory (Azure AD) и решение MDM, принимающее маркер AAD для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ваш ИТ-администратор может настроить Azure AD, чтобы автоматически разрешить регистрацию в MDM после входа пользователя с учетной записью Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-112">If your organization uses Azure Active Directory (Azure AD) and an MDM solution that accepts an AAD token for authentication (currently, only supported in Microsoft Intune and AirWatch), your IT admin can configure Azure AD to automatically allow MDM enrollment after the user signs in with their Azure AD account.</span></span> [<span data-ttu-id="e6fc6-113">Сведения о настройке регистрации в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-113">Learn how to configure Azure AD enrollment.</span></span>](https://docs.microsoft.com/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

<span data-ttu-id="e6fc6-114">Если автоматическая регистрация включена, дополнительные действия по регистрации вручную не требуются.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-114">When auto-enrollment is enabled, no additional manual enrollment is needed.</span></span> <span data-ttu-id="e6fc6-115">Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-115">When the user signs in with an Azure AD account, the device is enrolled in MDM after completing the first-run experience.</span></span>

## <span data-ttu-id="e6fc6-116">Регистрация через приложение «Параметры»</span><span class="sxs-lookup"><span data-stu-id="e6fc6-116">Enroll through Settings app</span></span>

 <span data-ttu-id="e6fc6-117">Если устройство не проходит регистрацию в MDM во время первого запуска, пользователь может вручную зарегистрировать это устройство на сервере MDM организации с помощью приложения «Параметры».</span><span class="sxs-lookup"><span data-stu-id="e6fc6-117">When the device is not enrolled in MDM during the first-run experience, the user can manually enroll the device with the organization's MDM server using the Settings app.</span></span>

1. <span data-ttu-id="e6fc6-118">Перейдите в меню **Параметры** > **Учетные записи** > **Рабочий доступ**.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-118">Go to **Settings** > **Accounts** > **Work access**.</span></span>
1. <span data-ttu-id="e6fc6-119">Выберите **Регистрация в системе управления устройствами** и введите свою учетную запись организации.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-119">Select **Enroll into device management** and enter your organizational account.</span></span> <span data-ttu-id="e6fc6-120">Вы будете перенаправлены на страницу входа вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-120">You will be redirected to your organization's sign in page.</span></span>
1. <span data-ttu-id="e6fc6-121">После успешной проверки подлинности на сервере MDM отобразится сообщение об успехе.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-121">Upon successful authentication to the MDM server, a success message is shown.</span></span>

<span data-ttu-id="e6fc6-122">Устройство теперь зарегистрировано на вашем сервере MDM.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-122">Your device is now enrolled with your MDM server.</span></span> <span data-ttu-id="e6fc6-123">Приложение «Параметры» теперь отражает, что устройство зарегистрировано в системе управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-123">The Settings app will now reflect that the device is enrolled in device management.</span></span>

## <span data-ttu-id="e6fc6-124">Отмена регистрации HoloLens из Intune</span><span class="sxs-lookup"><span data-stu-id="e6fc6-124">Unenroll HoloLens from Intune</span></span>

<span data-ttu-id="e6fc6-125">Невозможно удаленно [отменить регистрацию](https://docs.microsoft.com/intune-user-help/unenroll-your-device-from-intune-windows) устройства HoloLens в Intune.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-125">You cannot [unenroll](https://docs.microsoft.com/intune-user-help/unenroll-your-device-from-intune-windows) HoloLens from Intune remotely.</span></span> <span data-ttu-id="e6fc6-126">Если администратор отменит регистрацию устройства с помощью MDM, оно будет удалено из информационной панели Intune.</span><span class="sxs-lookup"><span data-stu-id="e6fc6-126">If the administrator unenrolls the device using MDM, the device will age out of the Intune dashboard.</span></span>
