---
title: Рекомендации по инфраструктуре для HoloLens
description: Ознакомьтесь с рекомендациями по инфраструктуре для устройств HoloLens, включая поддержку беспроводной сети, удаленную поддержку и управление мобильными устройствами.
ms.prod: hololens
ms.sitesec: library
author: pawinfie
ms.author: pawinfie
ms.topic: article
ms.localizationpriority: high
ms.date: 1/23/2020
ms.reviewer: ''
audience: ITPro
manager: bradke
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 4eb55bec56e53de9195ac87e0491eefd91992f3d
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283390"
---
# <span data-ttu-id="69c77-103">Настройка сети для HoloLens</span><span class="sxs-lookup"><span data-stu-id="69c77-103">Configure Your Network for HoloLens</span></span>

<span data-ttu-id="69c77-104">В этом разделе документа требуются следующие пользователи:</span><span class="sxs-lookup"><span data-stu-id="69c77-104">This portion of the document will require the following people:</span></span>

1. <span data-ttu-id="69c77-105">Сетевой администратор с разрешениями на внесение изменений в прокси-сервер или брандмауэр</span><span class="sxs-lookup"><span data-stu-id="69c77-105">Network Admin with permissions to make changes to the proxy/firewall</span></span>
2. <span data-ttu-id="69c77-106">Администратор Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="69c77-106">Azure Active Directory Admin</span></span>
3. <span data-ttu-id="69c77-107">Администратор управления мобильными устройствами</span><span class="sxs-lookup"><span data-stu-id="69c77-107">Mobile Device Manager Admin</span></span>

## <span data-ttu-id="69c77-108">Требования к инфраструктуре</span><span class="sxs-lookup"><span data-stu-id="69c77-108">Infrastructure Requirements</span></span>

<span data-ttu-id="69c77-109">HoloLens — это, по сути, устройство с Windows Mobile, интегрированное с Azure.</span><span class="sxs-lookup"><span data-stu-id="69c77-109">HoloLens is, at its core, a Windows mobile device integrated with Azure.</span></span>  <span data-ttu-id="69c77-110">Она лучше всего подходит для коммерческих сред с поддержкой беспроводных сетей (Wi-Fi) и доступа к службам Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="69c77-110">It works best in commercial environments with wireless network availability (wi-fi) and access to Microsoft services.</span></span>

<span data-ttu-id="69c77-111">В числе критических облачных служб:</span><span class="sxs-lookup"><span data-stu-id="69c77-111">Critical cloud services include:</span></span>

- <span data-ttu-id="69c77-112">Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="69c77-112">Azure active directory (Azure AD)</span></span>
- <span data-ttu-id="69c77-113">Центр обновления Windows (WU)</span><span class="sxs-lookup"><span data-stu-id="69c77-113">Windows Update (WU)</span></span>

<span data-ttu-id="69c77-114">Коммерческим клиентам потребуется инфраструктура управления мобильностью предприятия (EMM) или управления мобильными устройствами (MDM) для управления устройствами HoloLens в масштабе.</span><span class="sxs-lookup"><span data-stu-id="69c77-114">Commercial customers will need enterprise mobility management (EMM) or mobile device management (MDM) infrastructure to manage HoloLens devices at scale.</span></span>  <span data-ttu-id="69c77-115">Это руководство использует в качестве примера [Microsoft Intune](https://www.microsoft.com/enterprise-mobility-security/microsoft-intune), хотя поставщик с полной поддержкой Microsoft Policy поддерживает HoloLens.</span><span class="sxs-lookup"><span data-stu-id="69c77-115">This guide uses [Microsoft Intune](https://www.microsoft.com/enterprise-mobility-security/microsoft-intune) as an example, though any provider with full support for Microsoft Policy can support HoloLens.</span></span>  <span data-ttu-id="69c77-116">Спросите своего поставщика управления мобильными устройствами, поддерживают ли они HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="69c77-116">Ask your mobile device management provider if they support HoloLens 2.</span></span>

<span data-ttu-id="69c77-117">HoloLens действительно поддерживает ограниченный набор отключенных от облака событий.</span><span class="sxs-lookup"><span data-stu-id="69c77-117">HoloLens does support a limited set of cloud disconnected experiences.</span></span>

### <span data-ttu-id="69c77-118">Беспроводная сеть поддержка EAP</span><span class="sxs-lookup"><span data-stu-id="69c77-118">Wireless network EAP support</span></span>

- <span data-ttu-id="69c77-119">PEAP-MS-CHAPv2</span><span class="sxs-lookup"><span data-stu-id="69c77-119">PEAP-MS-CHAPv2</span></span>
- <span data-ttu-id="69c77-120">PEAP-TLS</span><span class="sxs-lookup"><span data-stu-id="69c77-120">PEAP-TLS</span></span>
- <span data-ttu-id="69c77-121">TLS</span><span class="sxs-lookup"><span data-stu-id="69c77-121">TLS</span></span>
- <span data-ttu-id="69c77-122">TTLS CHAP</span><span class="sxs-lookup"><span data-stu-id="69c77-122">TTLS-CHAP</span></span>
- <span data-ttu-id="69c77-123">TTLS-CHAPv2</span><span class="sxs-lookup"><span data-stu-id="69c77-123">TTLS-CHAPv2</span></span>
- <span data-ttu-id="69c77-124">TTLS-MS-CHAPv2</span><span class="sxs-lookup"><span data-stu-id="69c77-124">TTLS-MS-CHAPv2</span></span>
- <span data-ttu-id="69c77-125">TTLS PAP</span><span class="sxs-lookup"><span data-stu-id="69c77-125">TTLS-PAP</span></span>
- <span data-ttu-id="69c77-126">TTLS TLS</span><span class="sxs-lookup"><span data-stu-id="69c77-126">TTLS-TLS</span></span>

### <span data-ttu-id="69c77-127">Специальные требования к сети для HoloLens</span><span class="sxs-lookup"><span data-stu-id="69c77-127">HoloLens Specific Network Requirements</span></span>

<span data-ttu-id="69c77-128">Убедитесь, что конечные точки в[этом списке](hololens-offline.md) разрешены в сетевом брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="69c77-128">Make sure that [this list](hololens-offline.md) of endpoints are allowed on your network firewall.</span></span> <span data-ttu-id="69c77-129">Это обеспечит правильную работу HoloLens.</span><span class="sxs-lookup"><span data-stu-id="69c77-129">This will enable HoloLens to function properly.</span></span>

### <span data-ttu-id="69c77-130">Специальные требования к сети для Удаленной поддержки</span><span class="sxs-lookup"><span data-stu-id="69c77-130">Remote Assist Specific Network Requirements</span></span>

1. <span data-ttu-id="69c77-131">Рекомендуемая пропускная способность для оптимальной производительности Удаленной поддержки составляет 1,5 Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="69c77-131">The recommended bandwidth for optimal performance of Remote Assist is 1.5Mbps.</span></span> <span data-ttu-id="69c77-132">Дополнительные сведения см. в [подробных требованиях к сети](https://docs.microsoft.com/MicrosoftTeams/prepare-network).</span><span class="sxs-lookup"><span data-stu-id="69c77-132">See the [detailed network requirements](https://docs.microsoft.com/MicrosoftTeams/prepare-network) for additional information.</span></span>
**<span data-ttu-id="69c77-133">(Обратите внимание, что если скорость в вашей сети не достигает 1,5 Мбит/с, Удаленная поддержка по-прежнему будет работать.</span><span class="sxs-lookup"><span data-stu-id="69c77-133">(Please note, if you don't network have network speeds of at least 1.5Mbps, Remote Assist will still work.</span></span> <span data-ttu-id="69c77-134">Однако качество может снизиться).</span><span class="sxs-lookup"><span data-stu-id="69c77-134">However, quality may suffer).</span></span>**
1. <span data-ttu-id="69c77-135">Убедитесь, что эти порты и URL-адреса разрешены в сетевом брандмауэре, чтобы обеспечить работу Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="69c77-135">Make sure that these ports and URLs are allowed on your network firewall to enable Microsoft Teams to function.</span></span> <span data-ttu-id="69c77-136">Следите за [актуальным списком портов](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges#skype-for-business-online-and-microsoft-teams).</span><span class="sxs-lookup"><span data-stu-id="69c77-136">Stay up to date with the [latest list of ports](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges#skype-for-business-online-and-microsoft-teams).</span></span>

- <span data-ttu-id="69c77-137">Узнайте больше о конкретных [сетевых требованиях для удаленной поддержки](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="69c77-137">Learn more about the specific [Network Requirements for Remote Assist](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements#network-requirements).</span></span> 
- <span data-ttu-id="69c77-138">Узнайте больше о том, как [подготовить сеть организации для Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/prepare-network)</span><span class="sxs-lookup"><span data-stu-id="69c77-138">Learn more about how to [prepare your organization's network for Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/prepare-network)</span></span>

### <span data-ttu-id="69c77-139">Специальные требования к сети для руководств</span><span class="sxs-lookup"><span data-stu-id="69c77-139">Guides Specific Network Requirements</span></span>

<span data-ttu-id="69c77-140">Руководства требуют сетевого доступа только для скачивания и использования приложения.</span><span class="sxs-lookup"><span data-stu-id="69c77-140">Guides only require network access to download and use the app.</span></span>

## <span data-ttu-id="69c77-141">Руководство по Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="69c77-141">Azure Active Directory Guidance</span></span>

> [!NOTE]
> <span data-ttu-id="69c77-142">Этот этап необходим только в том случае, если ваша организация планирует управлять HoloLens.</span><span class="sxs-lookup"><span data-stu-id="69c77-142">This step is only necessary if your company plans on managing the HoloLens.</span></span>

1. <span data-ttu-id="69c77-143">Убедитесь в том, что у вас есть лицензия на Azure AD.</span><span class="sxs-lookup"><span data-stu-id="69c77-143">Ensure that you have an Azure AD License.</span></span>
<span data-ttu-id="69c77-144">Дополнительные сведения см. в [требованиях к лицензиям для HoloLens](hololens-licenses-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="69c77-144">Please [HoloLens Licenses Requirements](hololens-licenses-requirements.md) for additional information.</span></span>

1. <span data-ttu-id="69c77-145">Если вы планируете использовать автоматическую регистрацию, необходимо [Настроить регистрацию Azure AD.](https://docs.microsoft.com/intune/deploy-use/.set-up-windows-device-management-with-microsoft-intune#azure-active-directory-enrollment)</span><span class="sxs-lookup"><span data-stu-id="69c77-145">If you plan on using Auto Enrollment, you will have to [Configure Azure AD enrollment.](https://docs.microsoft.com/intune/deploy-use/.set-up-windows-device-management-with-microsoft-intune#azure-active-directory-enrollment)</span></span>

1. <span data-ttu-id="69c77-146">Убедитесь, что пользователи вашей организации находятся в службе Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="69c77-146">Ensure that your company's users are in Azure Active Directory (Azure AD).</span></span>
<span data-ttu-id="69c77-147">См. следующие [инструкции](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory) по добавлению пользователей.</span><span class="sxs-lookup"><span data-stu-id="69c77-147">See the following [instructions](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory) for adding users.</span></span>

1. <span data-ttu-id="69c77-148">Мы предлагаем добавлять пользователей, которым понадобятся аналогичные лицензии, в одну группу.</span><span class="sxs-lookup"><span data-stu-id="69c77-148">We suggest that users who need similar licenses are added to the same group.</span></span>
    1. [<span data-ttu-id="69c77-149">Создание группы</span><span class="sxs-lookup"><span data-stu-id="69c77-149">Create a Group</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
    1. [<span data-ttu-id="69c77-150">Добавление пользователей в группы</span><span class="sxs-lookup"><span data-stu-id="69c77-150">Add users to groups</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-members-azure-portal)

1. <span data-ttu-id="69c77-151">Убедитесь, что пользователям вашей организации (или группам пользователей) назначены необходимые лицензии.</span><span class="sxs-lookup"><span data-stu-id="69c77-151">Ensure that your company's users (or group of users) are assigned the necessary licenses.</span></span>
<span data-ttu-id="69c77-152">Если вам нужно назначить лицензии, выполните следующие [инструкции](https://docs.microsoft.com/azure/active-directory/fundamentals/license-users-groups).</span><span class="sxs-lookup"><span data-stu-id="69c77-152">If you need to assign licenses, follow these [directions](https://docs.microsoft.com/azure/active-directory/fundamentals/license-users-groups).</span></span>

1. <span data-ttu-id="69c77-153">Выполняйте этот шаг только в том случае, если ожидается, что пользователи зарегистрируют у вас свои устройства HoloLens / мобильные устройства (есть три варианта). Эти шаги гарантируют, что пользователи вашей компании (или группа пользователей) смогут добавлять устройства.</span><span class="sxs-lookup"><span data-stu-id="69c77-153">Only do this step if users are expected to enroll their HoloLens/Mobile device into you (There are three options) These steps ensure that your company's users (or a group of users) can add devices.</span></span>
    1. <span data-ttu-id="69c77-154">**Вариант 1.** Предоставление всем пользователям разрешения на присоединение устройств к Azure AD.</span><span class="sxs-lookup"><span data-stu-id="69c77-154">**Option 1:** Give all users permission to join devices to Azure AD.</span></span>
<span data-ttu-id="69c77-155">**Войдите на портал Azure в качестве администратора** > **Azure Active Directory** > **Устройства** > **Параметры устройства** >
**Присвойте параметру "Пользователи могут присоединять устройства к Azure AD" значение *Все***</span><span class="sxs-lookup"><span data-stu-id="69c77-155">**Sign in to the Azure portal as an administrator** > **Azure Active Directory** > **Devices** > **Device Settings** >
**Set Users may join devices to Azure AD to *All***</span></span>

    1. <span data-ttu-id="69c77-156">**Вариант 2:** Предоставление выбранным пользователям / группам разрешения присоединяться к устройствам в Azure AD. **Войдите на портал Azure в качестве администратора** > \*\* Azure Active Directory\*\* > \*\*Устройства \*\* > **Параметры устройства** >
 \*\*. Пользователи могут присоединять устройства к Azure AD к \*выбранному\*\*\*
![ изображению, которое показывает конфигурацию подключенных устройств Azure AD.</span><span class="sxs-lookup"><span data-stu-id="69c77-156">**Option 2:** Give selected users/groups permission to join devices to Azure AD **Sign in to the Azure portal as an administrator** > **Azure Active Directory** > **Devices** > **Device Settings** >
\*\*Set Users may join devices to Azure AD to \*Selected\*\*\*
![Image that shows Configuration of Azure AD Joined Devices</span></span>](images/azure-ad-image.png)

    1. <span data-ttu-id="69c77-157">**Вариант 3.** Вы можете заблокировать для всех пользователей доступ к домену.</span><span class="sxs-lookup"><span data-stu-id="69c77-157">**Option 3:** You can block all users from joining their devices to the domain.</span></span> <span data-ttu-id="69c77-158">Это означает, что все устройства придется регистрировать вручную.</span><span class="sxs-lookup"><span data-stu-id="69c77-158">This means that all devices will need to be manually enrolled.</span></span>

## <span data-ttu-id="69c77-159">Руководство диспетчера мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="69c77-159">Mobile Device Manager Guidance</span></span>

### <span data-ttu-id="69c77-160">Постоянное управление устройством</span><span class="sxs-lookup"><span data-stu-id="69c77-160">Ongoing device management</span></span>

> [!NOTE]
> <span data-ttu-id="69c77-161">Этот этап необходим только в том случае, если ваша организация планирует управлять HoloLens.</span><span class="sxs-lookup"><span data-stu-id="69c77-161">This step is only necessary if your company plans to manage the HoloLens.</span></span>

<span data-ttu-id="69c77-162">Текущее управление устройствами будет зависеть от используемой инфраструктуры управления мобильными устройствами.</span><span class="sxs-lookup"><span data-stu-id="69c77-162">Ongoing device management will depend on your mobile device management infrastructure.</span></span>  <span data-ttu-id="69c77-163">Большинство из них имеют одинаковую общую функциональность, но пользовательский интерфейс может сильно различаться.</span><span class="sxs-lookup"><span data-stu-id="69c77-163">Most have the same general functionality but the user interface may vary widely.</span></span>

1. <span data-ttu-id="69c77-164">[CSP (поставщики служб конфигурации)](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference#csps-supported-in-hololens-devices) позволяют создавать и развертывать параметры управления для устройств в вашей сети.</span><span class="sxs-lookup"><span data-stu-id="69c77-164">[CSPs (Configuration Service Providers)](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference#csps-supported-in-hololens-devices) lets you to create and deploy management settings for the devices on your network.</span></span> <span data-ttu-id="69c77-165">См. [список CSP HoloLens](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference#csps-supported-in-hololens-devices) для справки.</span><span class="sxs-lookup"><span data-stu-id="69c77-165">See the [list of HoloLens CSPs](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference#csps-supported-in-hololens-devices) for reference.</span></span>

1. <span data-ttu-id="69c77-166">[Политики соответствия](https://docs.microsoft.com/intune/device-compliance-get-started) — это правила и параметры, которым должны удовлетворять устройства, чтобы соответствовать корпоративной инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="69c77-166">[Compliance policies](https://docs.microsoft.com/intune/device-compliance-get-started) are rules and settings that devices must meet to be compliant in your corporate infrastructure.</span></span> <span data-ttu-id="69c77-167">Используйте эти политики с условным доступом, чтобы заблокировать доступ к ресурсам компании для устройств, которые не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="69c77-167">Use these policies with Conditional Access to block access to company resources for devices that are non-compliant.</span></span> <span data-ttu-id="69c77-168">Например, вы можете создать политику, требующую включения Bitlocker.</span><span class="sxs-lookup"><span data-stu-id="69c77-168">For example, you can create a policy that requires Bitlocker be enabled.</span></span>

1. <span data-ttu-id="69c77-169">[Создать политику соответствия](https://docs.microsoft.com/intune/protect/compliance-policy-create-windows).</span><span class="sxs-lookup"><span data-stu-id="69c77-169">[Create Compliance Policy](https://docs.microsoft.com/intune/protect/compliance-policy-create-windows).</span></span>

1. <span data-ttu-id="69c77-170">Условный доступ разрешает и запрещает мобильным устройствам и мобильным приложениям доступ к ресурсам организации.</span><span class="sxs-lookup"><span data-stu-id="69c77-170">Conditional Access allows/denies mobile devices and mobile applications from accessing company resources.</span></span> <span data-ttu-id="69c77-171">Ознакомьтесь с двумя полезными документами: [Планирование развертывания условного доступа](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) и [Рекомендации](https://docs.microsoft.com/azure/active-directory/conditional-access/best-practices).</span><span class="sxs-lookup"><span data-stu-id="69c77-171">Two documents you may find helpful are [Plan your CA Deployment](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) and [Best Practices](https://docs.microsoft.com/azure/active-directory/conditional-access/best-practices).</span></span>

1. <span data-ttu-id="69c77-172">[В этой статье](https://docs.microsoft.com/intune/fundamentals/windows-holographic-for-business) рассказывается об инструментах управления Intune для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="69c77-172">[This article](https://docs.microsoft.com/intune/fundamentals/windows-holographic-for-business) talks about Intune's management tools for HoloLens.</span></span>

1. [<span data-ttu-id="69c77-173">Создание профиля устройства</span><span class="sxs-lookup"><span data-stu-id="69c77-173">Create a device profile</span></span>](https://docs.microsoft.com/intune/configuration/device-profile-create)

### <span data-ttu-id="69c77-174">Управление обновлениями</span><span class="sxs-lookup"><span data-stu-id="69c77-174">Manage updates</span></span>

<span data-ttu-id="69c77-175">Intune включает функцию под названием «Кольца обновлений» для устройств Windows 10, включая HoloLens 2 и HoloLens v1 (с Holographic for Business).</span><span class="sxs-lookup"><span data-stu-id="69c77-175">Intune includes a feature called Update rings for Windows 10 devices, including HoloLens 2 and HoloLens v1 (with Holographic for Business).</span></span> <span data-ttu-id="69c77-176">Кольца обновлений включают группу параметров, которые определяют, как и когда устанавливаются обновления.</span><span class="sxs-lookup"><span data-stu-id="69c77-176">Update rings include a group of settings that determine how and when updates are installed.</span></span>

<span data-ttu-id="69c77-177">Например, вы можете создать окно обслуживания для установки обновлений или выбрать перезагрузку после установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="69c77-177">For example, you can create a maintenance window to install updates, or choose to restart after updates are installed.</span></span>  <span data-ttu-id="69c77-178">Вы также можете приостановить обновления до тех пор, пока не будете готовы к обновлению.</span><span class="sxs-lookup"><span data-stu-id="69c77-178">You can also choose to pause updates indefinitely until you're ready to update.</span></span>

<span data-ttu-id="69c77-179">Дополнительные сведения см. в статье [настройка обновлений колец с помощью Intune](https://docs.microsoft.com/intune/windows-update-for-business-configure).</span><span class="sxs-lookup"><span data-stu-id="69c77-179">Read more about [configuring update rings with Intune](https://docs.microsoft.com/intune/windows-update-for-business-configure).</span></span>

### <span data-ttu-id="69c77-180">Управление приложениями</span><span class="sxs-lookup"><span data-stu-id="69c77-180">Application management</span></span>

<span data-ttu-id="69c77-181">Управляйте приложениями HoloLens через:</span><span class="sxs-lookup"><span data-stu-id="69c77-181">Manage HoloLens applications through:</span></span>

1. <span data-ttu-id="69c77-182">Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="69c77-182">Microsoft Store</span></span>  
  <span data-ttu-id="69c77-183">Магазин Microsoft - лучший способ распространять и использовать приложения на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="69c77-183">The Microsoft Store is the best way to distribute and consume applications on HoloLens.</span></span>  <span data-ttu-id="69c77-184">В магазине уже есть отличный набор основных приложений HoloLens, или вы можете [опубликовать свое собственное](https://docs.microsoft.com/windows/uwp/publish/).</span><span class="sxs-lookup"><span data-stu-id="69c77-184">There is a great set of core HoloLens applications already available in the store or you can [publish your own](https://docs.microsoft.com/windows/uwp/publish/).</span></span>  
  <span data-ttu-id="69c77-185">Все приложения в магазине доступны всем, но если это неприемлемо, обратитесь в Microsoft Store для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="69c77-185">All applications in the store are available publicly to everyone, but if it isn't acceptable, checkout the Microsoft Store for Business.</span></span>  

1. [<span data-ttu-id="69c77-186">Microsoft Store для бизнеса</span><span class="sxs-lookup"><span data-stu-id="69c77-186">Microsoft Store for Business</span></span>](https://docs.microsoft.com/microsoft-store/)  
  <span data-ttu-id="69c77-187">Магазин Microsoft для бизнеса и образования - это специализированный магазин для вашей корпоративной среды.</span><span class="sxs-lookup"><span data-stu-id="69c77-187">Microsoft Store for Business and Education is a custom store for your corporate environment.</span></span>  <span data-ttu-id="69c77-188">Он позволяет использовать Microsoft Store, встроенный в Windows 10 и HoloLens, для поиска, приобретения, распространения и управления приложениями для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="69c77-188">It lets you use the Microsoft Store built into Windows 10 and HoloLens to find, acquire, distribute, and manage apps for your organization.</span></span>  <span data-ttu-id="69c77-189">Это также позволяет вам развертывать приложения, которые являются специфическими для вашей коммерческой среды, но не для всего мира.</span><span class="sxs-lookup"><span data-stu-id="69c77-189">It also lets you deploy apps that are specific to your commercial environment but not to the world.</span></span>

1. <span data-ttu-id="69c77-190">Развертывание и управление приложениями через Intune или другое решение для управления мобильными устройствами</span><span class="sxs-lookup"><span data-stu-id="69c77-190">Application deployment and management via Intune or another mobile device management solution</span></span>  
  <span data-ttu-id="69c77-191">Большинство решений для управления мобильными устройствами, включая Intune, обеспечивают способ развертывания линейных бизнес-приложений непосредственно на набор зарегистрированных устройств.</span><span class="sxs-lookup"><span data-stu-id="69c77-191">Most mobile device management solutions, including Intune, provide a way to deploy line of business applications directly to a set of enrolled devices.</span></span>  <span data-ttu-id="69c77-192">Ознакомьтесь с этой статьей, посвященной [установке приложения Intune](https://docs.microsoft.com/intune/apps-deploy).</span><span class="sxs-lookup"><span data-stu-id="69c77-192">See this article for [Intune app install](https://docs.microsoft.com/intune/apps-deploy).</span></span>

1. <span data-ttu-id="69c77-193">_не рекомендуется использовать_ портал устройств</span><span class="sxs-lookup"><span data-stu-id="69c77-193">_not recommended_ Device Portal</span></span>  
  <span data-ttu-id="69c77-194">Приложения также могут быть установлены на HoloLens непосредственно с помощью портала устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="69c77-194">Applications can also be installed on HoloLens directly using the Windows Device Portal.</span></span>  <span data-ttu-id="69c77-195">Это не рекомендуется, поскольку режим разработчика должен быть включен для использования портала устройства.</span><span class="sxs-lookup"><span data-stu-id="69c77-195">This isn't recommended since Developer Mode has to be enabled to use the device portal.</span></span>

<span data-ttu-id="69c77-196">Дополнительные сведения см. в статье [установка приложений в HoloLens](https://docs.microsoft.com/hololens/hololens-install-apps).</span><span class="sxs-lookup"><span data-stu-id="69c77-196">Read more about [installing apps on HoloLens](https://docs.microsoft.com/hololens/hololens-install-apps).</span></span>

### <span data-ttu-id="69c77-197">Сертификаты</span><span class="sxs-lookup"><span data-stu-id="69c77-197">Certificates</span></span>

<span data-ttu-id="69c77-198">Распространять сертификаты можно через своего поставщика MDM.</span><span class="sxs-lookup"><span data-stu-id="69c77-198">You can distribute certificates through your MDM provider.</span></span> <span data-ttu-id="69c77-199">Если для вашей организации требуются сертификаты, Intune поддерживает PKCS, PFX и SCEP.</span><span class="sxs-lookup"><span data-stu-id="69c77-199">If your company requires certificates, Intune supports PKCS, PFX, and SCEP.</span></span> <span data-ttu-id="69c77-200">Важно понимать, какой сертификат подходит для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="69c77-200">It is important to understand which certificate is right for your company.</span></span> <span data-ttu-id="69c77-201">Чтобы определить оптимальный сертификат, обратитесь к документации по [конфигурациям сертификатов](https://docs.microsoft.com/intune/protect/certificates-configure).</span><span class="sxs-lookup"><span data-stu-id="69c77-201">Please visit the [certificate configurations](https://docs.microsoft.com/intune/protect/certificates-configure) documentation to determine which cert is best for you.</span></span> <span data-ttu-id="69c77-202">Если вы планируете использовать сертификаты для проверки подлинности HoloLens, вам могут подойти сертификаты PFX или SCEP.</span><span class="sxs-lookup"><span data-stu-id="69c77-202">If you plan to use certificates for HoloLens Authentication, PFX or SCEP may be right for you.</span></span>

<span data-ttu-id="69c77-203">См. следующие действия по использованию [SCEP](https://docs.microsoft.com/intune/protect/certificates-profile-scep).</span><span class="sxs-lookup"><span data-stu-id="69c77-203">See the following steps for using [SCEP](https://docs.microsoft.com/intune/protect/certificates-profile-scep).</span></span>

### <span data-ttu-id="69c77-204">Как перейти на коммерческий пакет Holographics для бизнеса</span><span class="sxs-lookup"><span data-stu-id="69c77-204">How to Upgrade to Holographics for Business Commercial Suite</span></span>

> [!NOTE]
> <span data-ttu-id="69c77-205">Windows Holographics для бизнеса (коммерческие наборы) предназначена только для устройств HoloLens 1-го поколения.</span><span class="sxs-lookup"><span data-stu-id="69c77-205">Windows Holographics for Business (commercial suite) is only intended for HoloLens 1st gen devices.</span></span> <span data-ttu-id="69c77-206">Профиль не будет применен к устройствам HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="69c77-206">The profile will not be applied to HoloLens 2 devices.</span></span>

<span data-ttu-id="69c77-207">Инструкции по переходу на коммерческий пакет доступны в документации по [обновлению Holographic](https://docs.microsoft.com/intune/configuration/holographic-upgrade).</span><span class="sxs-lookup"><span data-stu-id="69c77-207">You can find directions for upgrading to the commercial suite in the [holographic upgrade](https://docs.microsoft.com/intune/configuration/holographic-upgrade) documentation.</span></span>

### <span data-ttu-id="69c77-208">Как настроить режим терминала с помощью Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="69c77-208">How to Configure Kiosk Mode Using Microsoft Intune</span></span>

1. <span data-ttu-id="69c77-209">Синхронизируйте Microsoft Store с Intune (см. следующие [инструкции](https://docs.microsoft.com/intune/apps/windows-store-for-business)).</span><span class="sxs-lookup"><span data-stu-id="69c77-209">Sync Microsoft Store to Intune (See the following [instructions](https://docs.microsoft.com/intune/apps/windows-store-for-business)).</span></span>

1. <span data-ttu-id="69c77-210">Проверьте настройки вашего приложения</span><span class="sxs-lookup"><span data-stu-id="69c77-210">Check your app settings</span></span>
    1. <span data-ttu-id="69c77-211">Войдите в свою учетную запись Microsoft Store для бизнеса</span><span class="sxs-lookup"><span data-stu-id="69c77-211">Log into your Microsoft Store Business account</span></span>
    1. **<span data-ttu-id="69c77-212">Управление > Продукты и услуги > Приложения и программное обеспечение > Выберите приложение для синхронизации > Доступность частного магазина > Выберите параметр "Все пользователи" или "Определенные группы"</span><span class="sxs-lookup"><span data-stu-id="69c77-212">Manage > Products and Services > Apps and Software > Select the app you want to sync > Private Store Availability > Select "Everyone" or "Specific Groups"</span></span>**
        >[!NOTE]
        ><span data-ttu-id="69c77-213">Если вы не видите нужное приложение, вам нужно "получить" его путем поиска в магазине.</span><span class="sxs-lookup"><span data-stu-id="69c77-213">If you don't see the app you want, you will have to "get" the app by searching the store for your app.</span></span> <span data-ttu-id="69c77-214">**Щелкните строку "Поиск" в правом верхнем углу > введите название приложения > щелкните приложение > нажмите "Получить"**.</span><span class="sxs-lookup"><span data-stu-id="69c77-214">**Click the "Search" bar in the upper right-hand corner > type in the name of the app > click on the app > select "Get"**.</span></span>
    1. <span data-ttu-id="69c77-215">Если ваши приложения не отображаются в **Intune > Клиентские приложения > Приложения**, может понадобиться повторить [синхронизацию приложений](https://docs.microsoft.com/intune/apps/windows-store-for-business#synchronize-apps).</span><span class="sxs-lookup"><span data-stu-id="69c77-215">If you do not see your apps in **Intune > Client Apps > Apps** , you may have to [sync your apps](https://docs.microsoft.com/intune/apps/windows-store-for-business#synchronize-apps) again.</span></span>

1. [<span data-ttu-id="69c77-216">Создать профиль устройства для режима киоска</span><span class="sxs-lookup"><span data-stu-id="69c77-216">Create a device profile for Kiosk mode</span></span>](https://docs.microsoft.com/intune/configuration/kiosk-settings#create-the-profile)

> [!NOTE]
> <span data-ttu-id="69c77-217">Вы можете настроить для разных пользователей разные возможности режима терминала, используя параметр "Azure AD" в качестве типа входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="69c77-217">You can configure different users to have different Kiosk Mode experiences by using "Azure AD" as the "User logon type".</span></span> <span data-ttu-id="69c77-218">Однако этот параметр доступен только в режиме терминала для нескольких приложений.</span><span class="sxs-lookup"><span data-stu-id="69c77-218">However, this option is only available in Multi-App kiosk mode.</span></span> <span data-ttu-id="69c77-219">Режим терминала для нескольких приложений будет работать и с единственным приложением, и с несколькими приложениями.</span><span class="sxs-lookup"><span data-stu-id="69c77-219">Multi-App kiosk mode will work with only one app as well as multiple apps.</span></span>

![Изображение настройки режима терминала в Intune](images/aad-kioskmode.png)

<span data-ttu-id="69c77-221">Инструкции по другим службам MDM см. в документации вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="69c77-221">For other MDM services, check your provider's documentation for instructions.</span></span> <span data-ttu-id="69c77-222">Если вам нужно использовать настраиваемый параметр и полную конфигурацию XML для настройки терминала в службе MDM, воспользуйтесь инструкциями [терминала HoloLens](hololens-kiosk.md#use-microsoft-intune-or-other-mdm-to-set-up-a-single-app-or-multi-app-kiosk).</span><span class="sxs-lookup"><span data-stu-id="69c77-222">Refer to the [HoloLens kiosk](hololens-kiosk.md#use-microsoft-intune-or-other-mdm-to-set-up-a-single-app-or-multi-app-kiosk) instructions if you need to use a custom setting and full XML configuration to set up a kiosk in your MDM service.</span></span>

## <span data-ttu-id="69c77-223">Сертификаты и проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="69c77-223">Certificates and Authentication</span></span>

<span data-ttu-id="69c77-224">Сертификаты можно разворачивать с помощью MDM (см. раздел "сертификаты" в [разделе MDM](hololens-commercial-infrastructure.md#mobile-device-manager-guidance)).</span><span class="sxs-lookup"><span data-stu-id="69c77-224">Certificates can be deployed via you MDM (see "certificates" in the [MDM Section](hololens-commercial-infrastructure.md#mobile-device-manager-guidance)).</span></span> <span data-ttu-id="69c77-225">Сертификаты также могут быть развернуты в HoloLens посредством предоставления пакетов.</span><span class="sxs-lookup"><span data-stu-id="69c77-225">Certificates can also be deployed to the HoloLens through package provisioning.</span></span> <span data-ttu-id="69c77-226">Дополнительные сведения см. в статье [Подготовка HoloLens](hololens-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="69c77-226">Please see [HoloLens Provisioning](hololens-provisioning.md) for additional information.</span></span>

### <span data-ttu-id="69c77-227">Дополнительные быстрые ссылки Intune</span><span class="sxs-lookup"><span data-stu-id="69c77-227">Additional Intune Quick Links</span></span>

1. <span data-ttu-id="69c77-228">[Создание профилей.](https://docs.microsoft.com/intune/configuration/device-profile-create) Профили позволяют добавлять и настраивать параметры, отправляемые на устройства в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="69c77-228">[Create Profiles:](https://docs.microsoft.com/intune/configuration/device-profile-create) Profiles allow you to add and configure settings that will be pushed to the devices in your organization.</span></span>

