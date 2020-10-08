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
ms.date: 10/06/2019
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 5adc1b48c4603f3a9d3145bef4f1d8aa1867a9d1
ms.sourcegitcommit: 5877c3e51de49f949b35ab840a3312a009a4487a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/07/2020
ms.locfileid: "11102328"
---
# <span data-ttu-id="6ef86-103">Регистрация HoloLens в MDM</span><span class="sxs-lookup"><span data-stu-id="6ef86-103">Enroll HoloLens in MDM</span></span>

<span data-ttu-id="6ef86-104">Вы можете управлять несколькими устройствами Microsoft HoloLens одновременно с помощью таких решений, как [Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business).</span><span class="sxs-lookup"><span data-stu-id="6ef86-104">You can manage multiple Microsoft HoloLens devices simultaneously using solutions like [Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business).</span></span> <span data-ttu-id="6ef86-105">Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации.</span><span class="sxs-lookup"><span data-stu-id="6ef86-105">You will be able to manage settings, select apps to install and set security configurations tailored to your organization's need.</span></span> <span data-ttu-id="6ef86-106">См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).</span><span class="sxs-lookup"><span data-stu-id="6ef86-106">See [Manage devices running Windows Holographic with Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), the [configuration service providers (CSPs) that are supported in Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens), and the [policies supported by Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).</span></span>

> [!NOTE]
> <span data-ttu-id="6ef86-107">Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="6ef86-107">Mobile device management (MDM), including the VPN, Bitlocker, and kiosk mode features, is only available when you [upgrade to Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span></span>

## <span data-ttu-id="6ef86-108">Требования</span><span class="sxs-lookup"><span data-stu-id="6ef86-108">Requirements</span></span>

 <span data-ttu-id="6ef86-109">Для управления устройствами HoloLens вашей организации потребуется настройка управления мобильными устройствами (MDM).</span><span class="sxs-lookup"><span data-stu-id="6ef86-109">Your organization will need to have Mobile Device Management (MDM) set up in order to manage HoloLens devices.</span></span> <span data-ttu-id="6ef86-110">Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.</span><span class="sxs-lookup"><span data-stu-id="6ef86-110">Your MDM provider can be Microsoft Intune or a 3rd party provider that uses Microsoft MDM APIs.</span></span>
 
## <span data-ttu-id="6ef86-111">Различные способы регистрации</span><span class="sxs-lookup"><span data-stu-id="6ef86-111">Different ways to enroll</span></span>

<span data-ttu-id="6ef86-112">В зависимости от типа учетной записи, выбранной во время OOBE или при входе в систему, существуют различные способы регистрации.</span><span class="sxs-lookup"><span data-stu-id="6ef86-112">Depending on the type of identity chosen either during OOBE or post sign-in there are different methods of enrollment.</span></span> <span data-ttu-id="6ef86-113">Дополнительные сведения о каждом типе удостоверений на HoloLens можно найти на [этой странице](hololens-identity.md).</span><span class="sxs-lookup"><span data-stu-id="6ef86-113">To learn more about each type of Identity on HoloLens please visit [this page](hololens-identity.md).</span></span>

- <span data-ttu-id="6ef86-114">Если удостоверение — это AAD, то во время работы в файле Oobe или **Параметры**  ->  **доступа приложения или учебного заведения**  ->  **Connect** .</span><span class="sxs-lookup"><span data-stu-id="6ef86-114">If Identity is AAD, then either during OOBE or **Settings App** -> **Access Work or School** -> **Connect** button.</span></span>
    - <span data-ttu-id="6ef86-115">Для AAD автоматическая регистрация в MDM выполняется только в том случае, если для AAD настроены URL-адреса регистрации.</span><span class="sxs-lookup"><span data-stu-id="6ef86-115">For AAD, automatic MDM enrollment only occurs if AAD has been configured with enrollment URLs.</span></span>
- <span data-ttu-id="6ef86-116">Если удостоверение является приложением AAD и устройство было предварительно зарегистрировано с помощью учетной записи пользователя Intune с определенными профилями конфигурации, то при использовании OOBE вы присоединяетесь к домену, а затем приложение будет автоматически выполняться.</span><span class="sxs-lookup"><span data-stu-id="6ef86-116">If Identity is AAD and device has been pre-registered with Intune MDM server with specific configuration profile assigned to it, then AAD-Join and enrollment will automatically occur during OOBE.</span></span>
    - <span data-ttu-id="6ef86-117">Кроме того, в [сборках 19041.1103 +](hololens-release-notes.md#windows-holographic-version-2004)поддерживается [поток автопилота](hololens2-autopilot.md) .</span><span class="sxs-lookup"><span data-stu-id="6ef86-117">Also called [Autopilot flow](hololens2-autopilot.md) Available in [19041.1103+ builds](hololens-release-notes.md#windows-holographic-version-2004).</span></span>
- <span data-ttu-id="6ef86-118">Если для удостоверения задано MSA, используется **Настройка**  ->  **доступа к приложениям или кнопка учебного**  ->  **соединения** .</span><span class="sxs-lookup"><span data-stu-id="6ef86-118">If Identity is MSA, then using **Settings App** -> **Access Work or School** -> **Connect** button.</span></span>
    - <span data-ttu-id="6ef86-119">Это также называется потоком "добавить рабочую учетную запись" (AWA).</span><span class="sxs-lookup"><span data-stu-id="6ef86-119">Also called Add Work Account (AWA) flow.</span></span>
- <span data-ttu-id="6ef86-120">Если удостоверение является локальным пользователем, то с помощью **параметров**  ->  **доступ к приложениям или учебному заведению**  ->  **только в ссылке Управление устройствами** .</span><span class="sxs-lookup"><span data-stu-id="6ef86-120">If Identity is Local User, then using **Settings App** -> **Access Work or School** -> **Enroll only in device management** link.</span></span>
    - <span data-ttu-id="6ef86-121">Также называется чистым потоком регистрации для MDM.</span><span class="sxs-lookup"><span data-stu-id="6ef86-121">Also called pure MDM enrollment flow.</span></span>

<span data-ttu-id="6ef86-122">После регистрации устройства на сервере MDM приложение "Параметры" теперь будет показывать, что устройство будет зарегистрировано в службе управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="6ef86-122">Once the device is enrolled with your MDM server, the Settings app will now reflect that the device is enrolled in device management.</span></span>

## <span data-ttu-id="6ef86-123">Автоматическая регистрация в MDM</span><span class="sxs-lookup"><span data-stu-id="6ef86-123">Auto-enrollment in MDM</span></span>

<span data-ttu-id="6ef86-124">Если ваша организация использует Azure Active Directory (Azure AD) и решение MDM, принимающее маркер AAD для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ваш ИТ-администратор может настроить Azure AD, чтобы автоматически разрешить регистрацию в MDM после входа пользователя с учетной записью Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6ef86-124">If your organization uses Azure Active Directory (Azure AD) and an MDM solution that accepts an AAD token for authentication (currently, only supported in Microsoft Intune and AirWatch), your IT admin can configure Azure AD to automatically allow MDM enrollment after the user signs in with their Azure AD account.</span></span> [<span data-ttu-id="6ef86-125">Сведения о настройке регистрации в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6ef86-125">Learn how to configure Azure AD enrollment.</span></span>](https://docs.microsoft.com/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

<span data-ttu-id="6ef86-126">Если автоматическая регистрация включена, дополнительные действия по регистрации вручную не требуются.</span><span class="sxs-lookup"><span data-stu-id="6ef86-126">When auto-enrollment is enabled, no additional manual enrollment is needed.</span></span> <span data-ttu-id="6ef86-127">Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.</span><span class="sxs-lookup"><span data-stu-id="6ef86-127">When the user signs in with an Azure AD account, the device is enrolled in MDM after completing the first-run experience.</span></span>

<span data-ttu-id="6ef86-128">Если устройство подключено к AAD, это может повлиять на того, кто является [владельцем устройства](security-adminless-os.md#device-owner).</span><span class="sxs-lookup"><span data-stu-id="6ef86-128">When a device is AAD Joined it may affect who considered the [device owner](security-adminless-os.md#device-owner).</span></span>

## <span data-ttu-id="6ef86-129">Отмена регистрации HoloLens из Intune</span><span class="sxs-lookup"><span data-stu-id="6ef86-129">Unenroll HoloLens from Intune</span></span>

<span data-ttu-id="6ef86-130">Дополнительные сведения о том, как отменять регистрацию устройства, можно найти на [этой странице](https://docs.microsoft.com/windows/client-management/mdm/disconnecting-from-mdm-unenrollment).</span><span class="sxs-lookup"><span data-stu-id="6ef86-130">To learn more about unenrolling a device visit [this page](https://docs.microsoft.com/windows/client-management/mdm/disconnecting-from-mdm-unenrollment).</span></span> 
