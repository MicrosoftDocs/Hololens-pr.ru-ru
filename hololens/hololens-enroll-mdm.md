---
title: Регистрация HoloLens в MDM
description: узнайте, как регистрировать HoloLens в системе управления мобильными устройствами (MDM) для упрощения управления несколькими устройствами.
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
ms.openlocfilehash: 6c279664fa6051fab2f5e2e8f61e70b55704ae7c
ms.sourcegitcommit: 4c15afc772fba26683d9b75e38c44a018b4889f6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113640412"
---
# <a name="enroll-hololens-in-mdm"></a><span data-ttu-id="ff4cf-103">Регистрация HoloLens в MDM</span><span class="sxs-lookup"><span data-stu-id="ff4cf-103">Enroll HoloLens in MDM</span></span>

<span data-ttu-id="ff4cf-104">вы можете управлять несколькими Microsoft HoloLens устройствами одновременно с помощью таких решений, как [Microsoft Intune](/intune/windows-holographic-for-business).</span><span class="sxs-lookup"><span data-stu-id="ff4cf-104">You can manage multiple Microsoft HoloLens devices simultaneously using solutions like [Microsoft Intune](/intune/windows-holographic-for-business).</span></span> <span data-ttu-id="ff4cf-105">Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-105">You will be able to manage settings, select apps to install and set security configurations tailored to your organization's need.</span></span> <span data-ttu-id="ff4cf-106">См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).</span><span class="sxs-lookup"><span data-stu-id="ff4cf-106">See [Manage devices running Windows Holographic with Microsoft Intune](/intune/windows-holographic-for-business), the [configuration service providers (CSPs) that are supported in Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens), and the [policies supported by Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).</span></span>

> [!NOTE]
> <span data-ttu-id="ff4cf-107">Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="ff4cf-107">Mobile device management (MDM), including the VPN, Bitlocker, and kiosk mode features, is only available when you [upgrade to Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff4cf-108">Требования</span><span class="sxs-lookup"><span data-stu-id="ff4cf-108">Requirements</span></span>

 <span data-ttu-id="ff4cf-109">для управления HoloLens устройствами организации необходимо настроить управление мобильными устройствами (MDM).</span><span class="sxs-lookup"><span data-stu-id="ff4cf-109">Your organization will need to have Mobile Device Management (MDM) set up in order to manage HoloLens devices.</span></span> <span data-ttu-id="ff4cf-110">Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-110">Your MDM provider can be Microsoft Intune or a 3rd party provider that uses Microsoft MDM APIs.</span></span>
 
## <a name="different-ways-to-enroll"></a><span data-ttu-id="ff4cf-111">Различные способы регистрации</span><span class="sxs-lookup"><span data-stu-id="ff4cf-111">Different ways to enroll</span></span>

<span data-ttu-id="ff4cf-112">В зависимости от типа [удостоверения](hololens-identity.md) , выбранного во время OOBE или после входа, существуют различные методы регистрации.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-112">Depending on the type of [identity](hololens-identity.md) chosen either during OOBE or post sign-in, there are different methods of enrollment.</span></span>

- <span data-ttu-id="ff4cf-113">если удостоверение — Azure AD, то во время OOBE или Параметры работы с **приложением**  ->  **или учебного**  ->  **Подключение** .</span><span class="sxs-lookup"><span data-stu-id="ff4cf-113">If Identity is Azure AD, then either during OOBE or **Settings App** -> **Access Work or School** -> **Connect** button.</span></span>
    - <span data-ttu-id="ff4cf-114">Для Azure AD [Автоматическая регистрация MDM](hololens-enroll-mdm.md#auto-enrollment-in-mdm) выполняется, только если в Azure AD настроены URL-адреса регистрации.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-114">For Azure AD, [automatic MDM enrollment](hololens-enroll-mdm.md#auto-enrollment-in-mdm) only occurs if Azure AD has been configured with enrollment URLs.</span></span>
     
- <span data-ttu-id="ff4cf-115">Если удостоверение — Azure AD, а устройство предварительно зарегистрировано в Intune MDM Server с назначенным им особым профилем конфигурации, то Azure AD-Join и [Автоматическая регистрация MDM](hololens-enroll-mdm.md#auto-enrollment-in-mdm) будут выполняться во время Oobe.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-115">If Identity is Azure AD and device has been pre-registered with Intune MDM server with specific configuration profile assigned to it, then Azure AD-Join and [automatic MDM enrollment](hololens-enroll-mdm.md#auto-enrollment-in-mdm) will occur during OOBE.</span></span>
    - <span data-ttu-id="ff4cf-116">Также называется [потоком с автопилотом](hololens2-autopilot.md) , доступным в [сборках 19041.1103 и](hololens-release-notes.md#windows-holographic-version-2004).</span><span class="sxs-lookup"><span data-stu-id="ff4cf-116">Also called [Autopilot flow](hololens2-autopilot.md) Available in [19041.1103+ builds](hololens-release-notes.md#windows-holographic-version-2004).</span></span>
    

- <span data-ttu-id="ff4cf-117">если удостоверение — MSA, воспользуйтесь кнопкой **Параметры**  ->  **доступ к приложениям или учебного**  ->  **Подключение** .</span><span class="sxs-lookup"><span data-stu-id="ff4cf-117">If Identity is MSA, then using **Settings App** -> **Access Work or School** -> **Connect** button.</span></span>
    - <span data-ttu-id="ff4cf-118">Также называется потоком добавления рабочей учетной записи (AWS).</span><span class="sxs-lookup"><span data-stu-id="ff4cf-118">Also called Add Work Account (AWA) flow.</span></span>
- <span data-ttu-id="ff4cf-119">если удостоверение является локальным пользователем, используйте **Параметры**  ->  **доступ к приложению или учебную**  ->  **регистрацию только в связи с управлением устройствами** .</span><span class="sxs-lookup"><span data-stu-id="ff4cf-119">If Identity is Local User, then using **Settings App** -> **Access Work or School** -> **Enroll only in device management** link.</span></span>
    - <span data-ttu-id="ff4cf-120">Также называется чистым потоком регистрации MDM.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-120">Also called pure MDM enrollment flow.</span></span>

<span data-ttu-id="ff4cf-121">после регистрации устройства на сервере MDM приложение Параметры теперь будет отражать, что устройство зарегистрировано в системе управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-121">Once the device is enrolled with your MDM server, the Settings app will now reflect that the device is enrolled in device management.</span></span>

## <a name="auto-enrollment-in-mdm"></a><span data-ttu-id="ff4cf-122">Автоматическая регистрация в MDM</span><span class="sxs-lookup"><span data-stu-id="ff4cf-122">Auto-enrollment in MDM</span></span>

<span data-ttu-id="ff4cf-123">если ваша организация имеет [подписку azure Premium](https://azure.microsoft.com/overview/), использует Azure Active Directory (Azure AD) и решение MDM, которое принимает маркер Azure ad для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ит-администратор может настроить автоматическое разрешение регистрации MDM после входа пользователя с помощью учетной записи Azure ad.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-123">If your organization has an [Azure Premium subscription](https://azure.microsoft.com/overview/), is using Azure Active Directory (Azure AD) and an MDM solution that accepts an Azure AD token for authentication (currently, only supported in Microsoft Intune and AirWatch), your IT admin can configure Azure AD to automatically allow MDM enrollment after the user signs in with their Azure AD account.</span></span> [<span data-ttu-id="ff4cf-124">Сведения о настройке регистрации в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-124">Learn how to configure Azure AD enrollment.</span></span>](/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

<span data-ttu-id="ff4cf-125">Если включена автоматическая регистрация, Дополнительная регистрация вручную не требуется.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-125">When auto-enrollment is enabled, no extra manual enrollment is needed.</span></span> <span data-ttu-id="ff4cf-126">Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-126">When the user signs in with an Azure AD account, the device is enrolled in MDM after completing the first-run experience.</span></span>

<span data-ttu-id="ff4cf-127">Если устройство подключено к Azure AD, оно может повлиять на [владельца устройства](security-adminless-os.md#device-owner).</span><span class="sxs-lookup"><span data-stu-id="ff4cf-127">When a device is Azure AD Joined it may affect who considered the [device owner](security-adminless-os.md#device-owner).</span></span>

## <a name="unenroll-hololens-from-intune"></a><span data-ttu-id="ff4cf-128">отмена регистрации HoloLens из Intune</span><span class="sxs-lookup"><span data-stu-id="ff4cf-128">Unenroll HoloLens from Intune</span></span>

<span data-ttu-id="ff4cf-129">Отмена регистрации устройства может быть недоступна в зависимости от метода регистрации.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-129">Depending on the enrollment method, unenrolling your device may not be available.</span></span>

<span data-ttu-id="ff4cf-130">Если ваше устройство было зарегистрировано в учетной записи Azure AD или на автопилоте, зарегистрировать его в Intune невозможно.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-130">If your device was enrolled with an Azure AD account or Autopilot, it cannot be unenrolled from Intune.</span></span> <span data-ttu-id="ff4cf-131">если вы хотите отменить присоединение HoloLens из Azure ad или повторно присоединить его к другому клиенту azure ad, необходимо [сбросить или восстановить](hololens-recovery.md#reset-the-device) устройство.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-131">If you wish to unjoin HoloLens from Azure AD or rejoin it to a different to Azure AD tenant, you must [reset/reflash](hololens-recovery.md#reset-the-device) the device.</span></span>

<span data-ttu-id="ff4cf-132">Если устройство было зарегистрировано в учетной записи MSA, которая добавила рабочую учетную запись или из локальной учетной записи, зарегистрированной только в управлении устройствами, вы можете отменять регистрацию устройства.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-132">If your device was enrolled from a MSA account that added a work account or from a Local account that enrolled only in device management, then you may unenroll the device.</span></span> <span data-ttu-id="ff4cf-133">откройте меню, а затем выберите **Параметры**  ->  **доступ к приложению работа или школьный**  ->  *йоураккаунт*  ->  **отключить** кнопку.</span><span class="sxs-lookup"><span data-stu-id="ff4cf-133">Open the Start menu and then select **Settings App** -> **Access Work or School** -> *YourAccount* -> **Disconnect** button.</span></span>