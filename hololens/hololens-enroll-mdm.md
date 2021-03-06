---
title: Регистрация HoloLens в MDM
description: Узнайте, как зарегистрировать HoloLens в управлении мобильными устройствами (MDM) для более простого управления несколькими устройствами.
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
ms.openlocfilehash: 5613c69bda8bbf70722a050ac5ce4ebeab95d332
ms.sourcegitcommit: 771e53feefbcc6bce18577515ad7d3f6a7f33840
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399387"
---
# <a name="enroll-hololens-in-mdm"></a><span data-ttu-id="dff05-103">Регистрация HoloLens в MDM</span><span class="sxs-lookup"><span data-stu-id="dff05-103">Enroll HoloLens in MDM</span></span>

<span data-ttu-id="dff05-104">Вы можете управлять несколькими устройствами Microsoft HoloLens одновременно с помощью решений, таких как [Microsoft Intune.](https://docs.microsoft.com/intune/windows-holographic-for-business)</span><span class="sxs-lookup"><span data-stu-id="dff05-104">You can manage multiple Microsoft HoloLens devices simultaneously using solutions like [Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business).</span></span> <span data-ttu-id="dff05-105">Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации.</span><span class="sxs-lookup"><span data-stu-id="dff05-105">You will be able to manage settings, select apps to install and set security configurations tailored to your organization's need.</span></span> <span data-ttu-id="dff05-106">См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).</span><span class="sxs-lookup"><span data-stu-id="dff05-106">See [Manage devices running Windows Holographic with Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), the [configuration service providers (CSPs) that are supported in Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens), and the [policies supported by Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).</span></span>

> [!NOTE]
> <span data-ttu-id="dff05-107">Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="dff05-107">Mobile device management (MDM), including the VPN, Bitlocker, and kiosk mode features, is only available when you [upgrade to Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dff05-108">Требования</span><span class="sxs-lookup"><span data-stu-id="dff05-108">Requirements</span></span>

 <span data-ttu-id="dff05-109">Для управления устройствами HoloLens организации необходимо настроить управление мобильными устройствами (MDM).</span><span class="sxs-lookup"><span data-stu-id="dff05-109">Your organization will need to have Mobile Device Management (MDM) set up in order to manage HoloLens devices.</span></span> <span data-ttu-id="dff05-110">Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.</span><span class="sxs-lookup"><span data-stu-id="dff05-110">Your MDM provider can be Microsoft Intune or a 3rd party provider that uses Microsoft MDM APIs.</span></span>
 
## <a name="different-ways-to-enroll"></a><span data-ttu-id="dff05-111">Различные способы регистрации</span><span class="sxs-lookup"><span data-stu-id="dff05-111">Different ways to enroll</span></span>

<span data-ttu-id="dff05-112">В зависимости от типа удостоверения, выбранного во время OOBE или после регистрации, существуют различные методы регистрации.</span><span class="sxs-lookup"><span data-stu-id="dff05-112">Depending on the type of identity chosen either during OOBE or post sign-in there are different methods of enrollment.</span></span> <span data-ttu-id="dff05-113">Дополнительные данные о каждом типе identity на HoloLens можно найти на [этой странице.](hololens-identity.md)</span><span class="sxs-lookup"><span data-stu-id="dff05-113">To learn more about each type of Identity on HoloLens please visit [this page](hololens-identity.md).</span></span>

- <span data-ttu-id="dff05-114">Если Identity — Azure AD, то либо во время работы OOBE или **Параметры работы**доступа к приложениям,  ->  **либо кнопки Подключения**  ->  **к** школе.</span><span class="sxs-lookup"><span data-stu-id="dff05-114">If Identity is Azure AD, then either during OOBE or **Settings App** -> **Access Work or School** -> **Connect** button.</span></span>
    - <span data-ttu-id="dff05-115">Для Azure AD автоматическая регистрация MDM происходит только в том случае, если Azure AD настроен с URL-адресами регистрации.</span><span class="sxs-lookup"><span data-stu-id="dff05-115">For Azure AD, automatic MDM enrollment only occurs if Azure AD has been configured with enrollment URLs.</span></span>
- <span data-ttu-id="dff05-116">Если Identity — Это Azure AD и устройство было предварительно зарегистрировано на сервере Intune MDM с определенным профилем конфигурации, назначенного ему, AD-Join и регистрация будет автоматически происходить во время OOBE.</span><span class="sxs-lookup"><span data-stu-id="dff05-116">If Identity is Azure AD and device has been pre-registered with Intune MDM server with specific configuration profile assigned to it, then Azure AD-Join and enrollment will automatically occur during OOBE.</span></span>
    - <span data-ttu-id="dff05-117">Также называется [поток автопилота,](hololens2-autopilot.md) доступный в [сборках 19041.1103+](hololens-release-notes.md#windows-holographic-version-2004).</span><span class="sxs-lookup"><span data-stu-id="dff05-117">Also called [Autopilot flow](hololens2-autopilot.md) Available in [19041.1103+ builds](hololens-release-notes.md#windows-holographic-version-2004).</span></span>
- <span data-ttu-id="dff05-118">Если identity — это MSA, то с помощью кнопки **Параметры Работы доступа**к приложениям  ->  **или кнопки Подключения**  ->  **к школе.**</span><span class="sxs-lookup"><span data-stu-id="dff05-118">If Identity is MSA, then using **Settings App** -> **Access Work or School** -> **Connect** button.</span></span>
    - <span data-ttu-id="dff05-119">Также называется поток Add Work Account (AWA).</span><span class="sxs-lookup"><span data-stu-id="dff05-119">Also called Add Work Account (AWA) flow.</span></span>
- <span data-ttu-id="dff05-120">Если identity — локальный пользователь, то с помощью **Параметры Работы по**доступу к приложениям или регистрации в школе  ->  \*\*\*\*  ->  **только в ссылке управления устройствами.**</span><span class="sxs-lookup"><span data-stu-id="dff05-120">If Identity is Local User, then using **Settings App** -> **Access Work or School** -> **Enroll only in device management** link.</span></span>
    - <span data-ttu-id="dff05-121">Также называется чистый поток регистрации MDM.</span><span class="sxs-lookup"><span data-stu-id="dff05-121">Also called pure MDM enrollment flow.</span></span>

<span data-ttu-id="dff05-122">После регистрации устройства на сервере MDM приложение Settings теперь будет отражать, что устройство зачислилось в управление устройствами.</span><span class="sxs-lookup"><span data-stu-id="dff05-122">Once the device is enrolled with your MDM server, the Settings app will now reflect that the device is enrolled in device management.</span></span>

## <a name="auto-enrollment-in-mdm"></a><span data-ttu-id="dff05-123">Автоматическая регистрация в MDM</span><span class="sxs-lookup"><span data-stu-id="dff05-123">Auto-enrollment in MDM</span></span>

<span data-ttu-id="dff05-124">Если ваша организация использует Azure Active Directory (Azure AD) и решение MDM, которое принимает маркер Azure AD для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ИТ-администратор может настроить Azure AD, чтобы автоматически разрешить регистрацию MDM после того, как пользователь включит свою учетную запись Azure AD.</span><span class="sxs-lookup"><span data-stu-id="dff05-124">If your organization uses Azure Active Directory (Azure AD) and an MDM solution that accepts an Azure AD token for authentication (currently, only supported in Microsoft Intune and AirWatch), your IT admin can configure Azure AD to automatically allow MDM enrollment after the user signs in with their Azure AD account.</span></span> [<span data-ttu-id="dff05-125">Сведения о настройке регистрации в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="dff05-125">Learn how to configure Azure AD enrollment.</span></span>](https://docs.microsoft.com/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

<span data-ttu-id="dff05-126">Если автоматическая регистрация включена, дополнительные действия по регистрации вручную не требуются.</span><span class="sxs-lookup"><span data-stu-id="dff05-126">When auto-enrollment is enabled, no additional manual enrollment is needed.</span></span> <span data-ttu-id="dff05-127">Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.</span><span class="sxs-lookup"><span data-stu-id="dff05-127">When the user signs in with an Azure AD account, the device is enrolled in MDM after completing the first-run experience.</span></span>

<span data-ttu-id="dff05-128">Если устройство является Azure AD Joined, это может повлиять на то, кто [считался владельцем устройства.](security-adminless-os.md#device-owner)</span><span class="sxs-lookup"><span data-stu-id="dff05-128">When a device is Azure AD Joined it may affect who considered the [device owner](security-adminless-os.md#device-owner).</span></span>

## <a name="unenroll-hololens-from-intune"></a><span data-ttu-id="dff05-129">Unenroll HoloLens из Intune</span><span class="sxs-lookup"><span data-stu-id="dff05-129">Unenroll HoloLens from Intune</span></span>

<span data-ttu-id="dff05-130">Хотя HoloLens 2 — это устройство с Windows 10, его нельзя просто отсоединить от Intune.</span><span class="sxs-lookup"><span data-stu-id="dff05-130">Although HoloLens 2 is Windows 10 device, it cannot be simply unenrolled from Intune.</span></span> <span data-ttu-id="dff05-131">Если вы хотите отсоединить HoloLens из Azure AD или присоединить его к другому клиенту Azure AD, необходимо сбросить [или](https://docs.microsoft.com/hololens/hololens-recovery#reset-the-device) перезагрузить устройство.</span><span class="sxs-lookup"><span data-stu-id="dff05-131">If you wish to unjoin HoloLens from Azure AD or rejoin it to a different to Azure AD tenant, you must [reset/reflash](https://docs.microsoft.com/hololens/hololens-recovery#reset-the-device) the device.</span></span>