---
title: Руководство по развертыванию — Корпоративные подключенные HoloLens 2 с руководствами dynamics 365 — подготовка
description: Узнайте, как подготовиться к регистрации устройств HoloLens 2 в корпоративной сети, подключенной к динамическим руководствам 365.
keywords: HoloLens, управление, корпоративное подключение, Руководство по динамике 365, AAD, Azure AD, MDM, Управление мобильными устройствами
author: joyjaz
ms.author: v-jjaswinski
ms.reviewer: aboeger
ms.date: 03/24/2021
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 2ab24aeac371b8d4a17d6121c3adf317cac7daf1
ms.sourcegitcommit: d7c86ccad7be32f7223d4b801083798454fda740
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2021
ms.locfileid: "11448611"
---
# <a name="prepare---corporate-connected-guide"></a><span data-ttu-id="d648a-104">Подготовка — руководство по корпоративным подключениям</span><span class="sxs-lookup"><span data-stu-id="d648a-104">Prepare - Corporate Connected Guide</span></span>
## <a name="infrastructure-essentials"></a><span data-ttu-id="d648a-105">Основные объекты инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="d648a-105">Infrastructure Essentials</span></span>
<span data-ttu-id="d648a-106">Для личных и корпоративных сценариев развертывания система управления мобильными устройствами (MDM) является необходимой инфраструктурой, необходимой для развертывания и управления устройствами Windows 10, особенно HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="d648a-106">For both personal and corporate deployment scenarios, a Mobile Device Management (MDM) system is the essential infrastructure required to deploy and manage Windows 10 devices, especially the HoloLens 2.</span></span> <span data-ttu-id="d648a-107">Подписка [Azure AD Premium](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-get-started-premium) рекомендуется в \*\*\*\* качестве поставщика удостоверений и необходима для поддержки определенных возможностей.</span><span class="sxs-lookup"><span data-stu-id="d648a-107">An [Azure AD Premium subscription](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-get-started-premium) is recommended as an identity provider and **required** to support certain capabilities.</span></span>

> [!NOTE]
> <span data-ttu-id="d648a-108">Несмотря на то, что HoloLens 2 развертывается и управляется как мобильное устройство, оно обычно используется в качестве общего устройства между многими пользователями.</span><span class="sxs-lookup"><span data-stu-id="d648a-108">Although the HoloLens 2 is deployed and managed like a mobile device, it is generally used as a shared device between many users.</span></span>

## <a name="azure-active-directory"></a><span data-ttu-id="d648a-109">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d648a-109">Azure Active Directory</span></span>
<span data-ttu-id="d648a-110">Azure AD— это облачная служба каталогов, обеспечивающая управление удостоверениями и доступом.</span><span class="sxs-lookup"><span data-stu-id="d648a-110">Azure AD is a cloud-based directory service that provides identity and access management.</span></span> <span data-ttu-id="d648a-111">Организации, использующие Microsoft Office 365 или Intune, уже используют Azure AD, которая имеет три выпуска: Free, Premium P1 и Premium P2 (см. в выпуске [Azure Active Directory).](https://azure.microsoft.com/documentation/articles/active-directory-editions)</span><span class="sxs-lookup"><span data-stu-id="d648a-111">Organizations that use Microsoft Office 365 or Intune are already using Azure AD, which has three editions: Free, Premium P1, and Premium P2 (see [Azure Active Directory editions](https://azure.microsoft.com/documentation/articles/active-directory-editions)).</span></span> <span data-ttu-id="d648a-112">Все выпуски поддерживают регистрацию устройств Azure AD, но premium P1 необходим для автоматической регистрации MDM, которую мы будем использовать в этом руководстве позже.</span><span class="sxs-lookup"><span data-stu-id="d648a-112">All editions support Azure AD device registration, but Premium P1 is required to enable MDM auto-enrollment which we will be using in this guide later.</span></span>
> [!Important]
> <span data-ttu-id="d648a-113">Важно иметь Azure AD, так как устройства HoloLens не поддерживают локальное участие в AD.</span><span class="sxs-lookup"><span data-stu-id="d648a-113">It is essential to have an Azure AD as HoloLens devices do not support on-premises AD join.</span></span> <span data-ttu-id="d648a-114">Если у вас еще нет настройка Azure AD, следуйте инструкциям по началу работы и создайте нового клиента [в Azure Active Directory.](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-access-create-new-tenant)</span><span class="sxs-lookup"><span data-stu-id="d648a-114">If you don't already have an Azure AD set up, follow the instructions to get started and [Create a new tenant in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-access-create-new-tenant).</span></span>

## <a name="identity-management"></a><span data-ttu-id="d648a-115">Управление удостоверением</span><span class="sxs-lookup"><span data-stu-id="d648a-115">Identity Management</span></span>
<span data-ttu-id="d648a-116">В этом руководстве [идентификатором](https://docs.microsoft.com/hololens/hololens-identity) будут использоваться учетные записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d648a-116">In this guide, the [Identity](https://docs.microsoft.com/hololens/hololens-identity) used will be Azure AD accounts.</span></span> <span data-ttu-id="d648a-117">Учетные записи Azure AD имеют несколько преимуществ, например:</span><span class="sxs-lookup"><span data-stu-id="d648a-117">There are several benefits to Azure AD accounts, such as:</span></span>
- <span data-ttu-id="d648a-118">Сотрудники используют свою учетную запись Azure AD для регистрации устройства в Azure AD и могут автоматически регистрировать его с помощью решения MDM организации (Azure AD+MDM — требуется подписка [Azure AD Premium).](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-get-started-premium)</span><span class="sxs-lookup"><span data-stu-id="d648a-118">Employees use their Azure AD account to register the device in Azure AD and can automatically enroll it with the organization's MDM solution (Azure AD+MDM – requires an [Azure AD Premium subscription](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-get-started-premium)).</span></span>
- <span data-ttu-id="d648a-119">Учетные записи Azure AD имеют [дополнительные](https://docs.microsoft.com/hololens/hololens-identity) параметры проверки подлинности с [помощью Windows Hello для бизнеса.](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-identity-verification)</span><span class="sxs-lookup"><span data-stu-id="d648a-119">Azure AD accounts have additional [authentication options](https://docs.microsoft.com/hololens/hololens-identity) via [Windows Hello for Business](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-identity-verification).</span></span> <span data-ttu-id="d648a-120">Помимо входа в систему Iris пользователи могут войти с другого устройства или использовать ключи безопасности FIDO.</span><span class="sxs-lookup"><span data-stu-id="d648a-120">In addition to Iris log-in, users can sign in from another device or use FIDO security keys.</span></span>

> [!WARNING] 
> <span data-ttu-id="d648a-121">Сотрудники могут использовать только одну учетную запись для инициализации устройства, поэтому необходимо сначала контролировать, какая учетная **запись включена.**</span><span class="sxs-lookup"><span data-stu-id="d648a-121">Employees can use only one account to initialize a device so **it's imperative that your organization controls which account is enabled first**.</span></span> <span data-ttu-id="d648a-122">Выбранная учетная запись определяет, кто контролирует устройство, и влияет на возможности управления.</span><span class="sxs-lookup"><span data-stu-id="d648a-122">The account chosen will determine who controls the device and influence your management capabilities.</span></span>

## <a name="mobile-device-management"></a><span data-ttu-id="d648a-123">Управление мобильными устройствами</span><span class="sxs-lookup"><span data-stu-id="d648a-123">Mobile Device Management</span></span>
<span data-ttu-id="d648a-124">Microsoft Intune, часть корпоративной мобильности и безопасности, является облачной системой MDM, которая управляет устройствами, подключенными к вашему клиенту.</span><span class="sxs-lookup"><span data-stu-id="d648a-124">Microsoft Intune, part of Enterprise Mobility + Security, is a cloud-based MDM system that manages devices connected to your tenant.</span></span> <span data-ttu-id="d648a-125">Как и Office 365, Intune использует Azure AD для управления удостоверениями, поэтому сотрудники используют те же учетные данные для регистрации устройств в Intune, что и для входа в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d648a-125">Like Office 365, Intune uses Azure AD for identity management, so employees use the same credentials to enroll devices in Intune that they use to sign into Office 365.</span></span> <span data-ttu-id="d648a-126">Intune также поддерживает устройства с другими операционными системами, такими как iOS и Android, для предоставления полного решения MDM.</span><span class="sxs-lookup"><span data-stu-id="d648a-126">Intune also supports devices that run other operating systems, such as iOS and Android, to provide a complete MDM solution.</span></span> <span data-ttu-id="d648a-127">В этом руководстве мы сосредоточимся на использовании Intune для включения развертывания во внутреннюю сеть с помощью HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="d648a-127">For the purposes of this guide, we'll be focusing on using Intune for enabling a deployment to your internal network with HoloLens 2.</span></span>
> [!Important] 
> <span data-ttu-id="d648a-128">Важно иметь управление мобильными устройствами.</span><span class="sxs-lookup"><span data-stu-id="d648a-128">It is essential to have Mobile Device Management.</span></span> <span data-ttu-id="d648a-129">Если она еще не настроена, следуйте этому руководству и привнося в Intune.</span><span class="sxs-lookup"><span data-stu-id="d648a-129">If you don't already have it set up, follow this guide and Get started with Intune.</span></span>

> [!Important]
> <span data-ttu-id="d648a-130">Для использования руководств требуется учетная запись Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d648a-130">In order to use Guides, an Azure AD account is required.</span></span>

> [!Note] 
> <span data-ttu-id="d648a-131">Windows 10 поддерживается несколькими системами MDM, и большинство из них поддерживает сценарии развертывания как персональных, так и корпоративных устройств.</span><span class="sxs-lookup"><span data-stu-id="d648a-131">Multiple MDM systems support Windows 10 and most support personal and corporate device deployment scenarios.</span></span> <span data-ttu-id="d648a-132">Поставщики MDM, поддерживают Windows 10 Holographic, включают: AirWatch, MobileIron и другие.</span><span class="sxs-lookup"><span data-stu-id="d648a-132">MDM providers that support Windows 10 Holographic include: AirWatch, MobileIron, and others.</span></span> <span data-ttu-id="d648a-133">Большинство ведущих поставщиков решений MDM в отрасли уже обеспечивают поддержку интеграции с Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d648a-133">Most industry-leading MDM vendors already support integration with Azure AD.</span></span> <span data-ttu-id="d648a-134">Вы можете найти самый текущий список поставщиков MDM, которые поддерживают Azure AD в [Azure Marketplace.](https://azuremarketplace.microsoft.com/marketplace/apps/category/azure-active-directory-apps)</span><span class="sxs-lookup"><span data-stu-id="d648a-134">You can find the most current list of MDM vendors that support Azure AD in [Azure Marketplace](https://azuremarketplace.microsoft.com/marketplace/apps/category/azure-active-directory-apps).</span></span>

## <a name="network-access"></a><span data-ttu-id="d648a-135">Доступ к сети</span><span class="sxs-lookup"><span data-stu-id="d648a-135">Network Access</span></span> 
<span data-ttu-id="d648a-136">Dynamics 365 Guides — это облачное приложение.</span><span class="sxs-lookup"><span data-stu-id="d648a-136">Dynamics 365 Guides is a cloud-based application.</span></span> <span data-ttu-id="d648a-137">Если у администратора сети есть список утверждений, им может потребоваться добавить IP-адреса и/или конечные точки, необходимые для подключения к серверам Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d648a-137">If your network admin has an approve list, they may need to add IP addresses and/or endpoints that are required to connect to the Dynamics 365 servers.</span></span> <span data-ttu-id="d648a-138">[Узнайте больше о разблокирования IP-адресов и URL-адресов.](https://docs.microsoft.com/power-platform/admin/online-requirements#ip-addresses-and-urls)</span><span class="sxs-lookup"><span data-stu-id="d648a-138">[Learn more about unblocking IP addresses and URLs](https://docs.microsoft.com/power-platform/admin/online-requirements#ip-addresses-and-urls).</span></span>

## <a name="certificates"></a><span data-ttu-id="d648a-139">Сертификаты</span><span class="sxs-lookup"><span data-stu-id="d648a-139">Certificates</span></span>
<span data-ttu-id="d648a-140">Сертификаты помогают повысить безопасность, предоставляя проверку подлинности учетных записей, Wi-Fi проверку подлинности, шифрование VPN и SSL-шифрование веб-контента.</span><span class="sxs-lookup"><span data-stu-id="d648a-140">Certificates help improve security by providing account authentication, Wi-Fi authentication, VPN encryption, and SSL encryption of web content.</span></span> <span data-ttu-id="d648a-141">Несмотря на то, что администраторы могут управлять сертификатами на устройствах вручную с помощью пакетов подготовка, лучше всего использовать систему MDM для управления этими сертификатами на протяжении всего жизненного цикла — от регистрации до обновления и отзыва.</span><span class="sxs-lookup"><span data-stu-id="d648a-141">Although administrators can manage certificates on devices manually through provisioning packages, it’s a best practice to use your MDM system to manage those certificates throughout their entire lifecycle – from enrollment through renewal and revocation.</span></span> 

<span data-ttu-id="d648a-142">Ваша система MDM может автоматически развертывать эти сертификаты в хранилищах сертификатов устройств после их регистрации (если ваша система MDM поддерживает простой протокол регистрации сертификатов **(SCEP)** или стандарты шифрования общедоступных ключей **#12 (PKCS#12)**).</span><span class="sxs-lookup"><span data-stu-id="d648a-142">Your MDM system can automatically deploy these certificates to the devices’ certificate stores after you enroll them (as long as your MDM system supports the **Simple Certificate Enrollment Protocol (SCEP)** or **Public Key Cryptography Standards #12 (PKCS#12)**).</span></span> <span data-ttu-id="d648a-143">[Узнайте о типах и профилях сертификатов, которые вы используете в Microsoft Intune.](https://docs.microsoft.com/mem/intune/protect/certificates-configure)</span><span class="sxs-lookup"><span data-stu-id="d648a-143">[Learn about certificate types and profiles you use with Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/certificates-configure).</span></span> <span data-ttu-id="d648a-144">MDM также может запрашивать и удалять зарегистрированные клиентские сертификаты или запускать новый запрос на регистрацию до истечения срока действия текущего сертификата.</span><span class="sxs-lookup"><span data-stu-id="d648a-144">MDM can also query and delete enrolled client certificates or trigger a new enrollment request before the current certificate is expired.</span></span>
 
<span data-ttu-id="d648a-145">Если ваши системы MDM уже настроены для сертификатов, перенастройте справки Подготовка сертификатов и сетевых профилей [для HoloLens 2,](https://docs.microsoft.com/hololens/hololens-certificates-network) чтобы приступить к развертыванию сертификатов и профилей для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="d648a-145">If your MDM systems is already configured for certificates, reference [Prepare certificates and network profiles for HoloLens 2](https://docs.microsoft.com/hololens/hololens-certificates-network) to start deploying certificates and profiles for your HoloLens 2 devices.</span></span>

## <a name="scep"></a><span data-ttu-id="d648a-146">SCEP</span><span class="sxs-lookup"><span data-stu-id="d648a-146">SCEP</span></span>

<span data-ttu-id="d648a-147">Для развертывания SCEP необходимы следующие службы, за исключением прокси-сервера веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d648a-147">The following services are required for SCEP deployment, with the exception of the Web Application Proxy Server.</span></span>
- [<span data-ttu-id="d648a-148">Управление сертификацией</span><span class="sxs-lookup"><span data-stu-id="d648a-148">Certification Authority</span></span>](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj125375(v=ws.11))
- [<span data-ttu-id="d648a-149">Роль сервера NDES</span><span class="sxs-lookup"><span data-stu-id="d648a-149">NDES Server role</span></span>](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831498(v=ws.11))
- [<span data-ttu-id="d648a-150">Соединитель Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="d648a-150">Microsoft Intune Connector</span></span>](https://docs.microsoft.com/mem/intune/protect/certificates-scep-configure#install-the-microsoft-intune-connector)

<span data-ttu-id="d648a-151">Вы также должны опубликовать URL-адрес NDES вне корпоративной сети с помощью прокси-сервера приложения [Azure AD или прокси-сервера веб-доступа.](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-add-on-premises-application)</span><span class="sxs-lookup"><span data-stu-id="d648a-151">You must also publish your NDES URL external to your corporate network using [Azure AD application proxy or Web Access Proxy](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-add-on-premises-application).</span></span> <span data-ttu-id="d648a-152">Вы также можете использовать другой обратный прокси по вашему выбору.</span><span class="sxs-lookup"><span data-stu-id="d648a-152">You can also use another reverse proxy of your choice.</span></span>

![Поток данных SCEP](./images/hololens2-scep-info-flow.png)

<span data-ttu-id="d648a-154">Если ваша сеть еще не поддерживает SCEP или вы не уверены, правильно ли настроена ваша сеть для SCEP с помощью Intune, направите ссылку Настройте инфраструктуру для поддержки SCEP с  [помощью Intune](https://docs.microsoft.com/mem/intune/protect/certificates-scep-configure).</span><span class="sxs-lookup"><span data-stu-id="d648a-154">If your network does not already support SCEP, or you are unsure if your network is correctly set up for SCEP with Intune, reference  [Configure infrastructure to support SCEP with Intune](https://docs.microsoft.com/mem/intune/protect/certificates-scep-configure).</span></span>

<span data-ttu-id="d648a-155">Если ваша инфраструктура уже поддерживает SCEP, [](https://docs.microsoft.com/mem/intune/protect/certificates-profile-scep) необходимо [](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/create-certificate-profiles) создать профиль для каждого сертификата SCEP, который будет использовать HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="d648a-155">If your infrastructure already supports SCEP, you will need to [create](https://docs.microsoft.com/mem/intune/protect/certificates-profile-scep) a [profile](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/create-certificate-profiles) for each SCEP certificate that the HoloLens 2 will use.</span></span> <span data-ttu-id="d648a-156">Если у вас возникли проблемы с SCEP, используйте использование профилей сертификатов SCEP для предоставления сертификатов [в Microsoft Intune.](https://docs.microsoft.com/troubleshoot/mem/intune/troubleshoot-scep-certificate-profiles)</span><span class="sxs-lookup"><span data-stu-id="d648a-156">If you are having issues with SCEP, use [Troubleshoot use of SCEP certificate profiles to provision certificates with Microsoft Intune](https://docs.microsoft.com/troubleshoot/mem/intune/troubleshoot-scep-certificate-profiles).</span></span>

## <a name="pkcs"></a><span data-ttu-id="d648a-157">PKCS</span><span class="sxs-lookup"><span data-stu-id="d648a-157">PKCS</span></span>
<span data-ttu-id="d648a-158">Intune также поддерживает использование частных и общедоступных сертификатов пары ключей (PKCS).</span><span class="sxs-lookup"><span data-stu-id="d648a-158">Intune also supports the use of private and public key pair (PKCS) certificates.</span></span> <span data-ttu-id="d648a-159">Дополнительные сведения используйте частные и общедоступные сертификаты [ключей в Microsoft Intune.](https://docs.microsoft.com/mem/intune/protect/certificates-pfx-configure)</span><span class="sxs-lookup"><span data-stu-id="d648a-159">Reference [Use private and public key certificates in Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/certificates-pfx-configure) for more information.</span></span>

## <a name="proxy"></a><span data-ttu-id="d648a-160">Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="d648a-160">Proxy</span></span>
<span data-ttu-id="d648a-161">Большинство корпоративных сетей интрасети используют прокси для управления внешним трафиком.</span><span class="sxs-lookup"><span data-stu-id="d648a-161">Most corporate intranet networks leverage a proxy to manage external traffic.</span></span> <span data-ttu-id="d648a-162">С помощью HoloLens 2 можно настроить прокси-сервер для подключений к ethernet, Wi-Fi и VPN.</span><span class="sxs-lookup"><span data-stu-id="d648a-162">With HoloLens 2 you can configure a proxy server for ethernet, Wi-Fi and VPN connections.</span></span>

<span data-ttu-id="d648a-163">Существует несколько различных типов прокси и способов настройки прокси.</span><span class="sxs-lookup"><span data-stu-id="d648a-163">There are a few different types of proxy and ways to configure proxy.</span></span> <span data-ttu-id="d648a-164">Для целей этого руководства мы выбираем **прокси-сервер Wi-Fi,** задающийся по URL-адресу PAC и развернутый с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="d648a-164">For the purposes of this guide, we are opting to choose **Wi-Fi proxy, set via PAC URL, and deployed via MDM**.</span></span> <span data-ttu-id="d648a-165">Это связано с преимуществами автоматического развертывания с помощью MDM, возможности обновлять файл PAC вместо конфигурации сервера:порт и, наконец, с помощью проксиWi-Fi для настройки прокси-сервера, чтобы применяться только к одному подключению Wi-Fi, что позволяет использовать устройства по-прежнему, если подключены в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="d648a-165">This comes with the advantages of being deployed via MDM automatically, being able to update the PAC file instead of using a server:port configuration, and finally using Wi-Fi proxy to configure proxy to only apply to a single Wi-Fi connection allowing the devices to be used still if connected in another location.</span></span> 


<span data-ttu-id="d648a-166">Дополнительные сведения о параметрах прокси для Windows 10 см. в Wi-Fi профиле для устройств [в Microsoft Intune - Azure.](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-configure)</span><span class="sxs-lookup"><span data-stu-id="d648a-166">For more details on proxy settings for Windows 10, see [Create a Wi-Fi profile for devices in Microsoft Intune - Azure](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-configure).</span></span>

## <a name="line-of-business-apps"></a><span data-ttu-id="d648a-167">Линия бизнес-приложений</span><span class="sxs-lookup"><span data-stu-id="d648a-167">Line of Business Apps</span></span> 
<span data-ttu-id="d648a-168">Хотя несколько приложений можно установить через Microsoft Store, скорее всего, у вас есть собственное настраиваемое приложение, созданное специально для использования в смешанной реальности.</span><span class="sxs-lookup"><span data-stu-id="d648a-168">While several apps can be installed via the Microsoft Store, it is likely you have your own custom app that you have created specifically to use in mixed reality.</span></span> <span data-ttu-id="d648a-169">Эти настраиваемые приложения, распространяемые по всей организации для вашего бизнеса, называются приложениями Line of Business (LOB).</span><span class="sxs-lookup"><span data-stu-id="d648a-169">These custom apps distributed throughout your organization for your business are called Line of Business (LOB) apps.</span></span>
  
<span data-ttu-id="d648a-170">Существует несколько способов развертывания приложений на устройствах HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="d648a-170">There are multiple ways to deploy applications to HoloLens 2 devices.</span></span> <span data-ttu-id="d648a-171">Приложения можно развертывать непосредственно через MDM, Microsoft Store для бизнеса (MSfB) или в пакете предварительной загрузки.</span><span class="sxs-lookup"><span data-stu-id="d648a-171">Apps can be deployed directly through MDM, the Microsoft Store for Business(MSfB), or sideloaded through a Provisioning Package.</span></span> <span data-ttu-id="d648a-172">Для этого руководства мы будем развертывать приложения через MDM с помощью обязательной установки приложения.</span><span class="sxs-lookup"><span data-stu-id="d648a-172">For the sake of this guide, we will be deploying apps via MDM, through the use of required app install.</span></span> <span data-ttu-id="d648a-173">Это позволит автоматически загружать приложения LOB на устройства HoloLens после завершения регистрации.</span><span class="sxs-lookup"><span data-stu-id="d648a-173">This will allow for your LOB apps to be automatically downloaded to your HoloLens devices once they finish enrollment.</span></span>

<span data-ttu-id="d648a-174">Для тех из вас, у кого нет собственного LOB, мы предокаст пример приложения для проверки этого потока развертывания.</span><span class="sxs-lookup"><span data-stu-id="d648a-174">For those of you who do not have your own LOB, we will provide a sample app to test this deployment flow.</span></span> <span data-ttu-id="d648a-175">Это приложение будет [приложением примеры MRTK,](https://aka.ms/HoloLensDocs-Sample-MRTK-Examples-App) и уже было предварительно отстроено и упаковано для проверки на доказательство концепции.</span><span class="sxs-lookup"><span data-stu-id="d648a-175">This app will be the [MRTK Examples](https://aka.ms/HoloLensDocs-Sample-MRTK-Examples-App) app, and has already been prebuilt and packaged to test for proof of concept.</span></span>
 
<span data-ttu-id="d648a-176">Дополнительные сведения о развертывании приложений можно найти в [app Management: Обзор](https://docs.microsoft.com/hololens/app-deploy-overview).</span><span class="sxs-lookup"><span data-stu-id="d648a-176">More details regarding app deployment can be found at [App Management: Overview](https://docs.microsoft.com/hololens/app-deploy-overview).</span></span>

> [!NOTE]
> <span data-ttu-id="d648a-177">HoloLens 2 поддерживает запуск только приложений ARM64 UWP.</span><span class="sxs-lookup"><span data-stu-id="d648a-177">HoloLens 2 supports running of UWP ARM64 apps only.</span></span>

## <a name="guides-playbook"></a><span data-ttu-id="d648a-178">Руководство Playbook</span><span class="sxs-lookup"><span data-stu-id="d648a-178">Guides Playbook</span></span>
<span data-ttu-id="d648a-179">Руководство использует среду Microsoft Dataverse в качестве магазина данных для приложений Guides.</span><span class="sxs-lookup"><span data-stu-id="d648a-179">Guides uses a Microsoft Dataverse environment as the datastore for your Guides apps.</span></span> <span data-ttu-id="d648a-180">Важно понимать более масштабную картину взаимодействия среды Dataverse с приложениями Guides и клиентом.</span><span class="sxs-lookup"><span data-stu-id="d648a-180">It’s important to understand the bigger picture of how your Dataverse environment interacts with your Guides apps and your tenant.</span></span> <span data-ttu-id="d648a-181">В этом руководстве мы не будем освещать управление вашей обратной стороной данных, но просмотрите основные концепции развертывания [руководств Dynamics 365 - Dynamics 365 Mixed Reality](https://docs.microsoft.com/dynamics365/mixed-reality/guides/admin-deployment-playbook).</span><span class="sxs-lookup"><span data-stu-id="d648a-181">We won’t be covering how to manage your dataverse in this guide, but please review [Basic concepts for deploying Dynamics 365 Guides - Dynamics 365 Mixed Reality](https://docs.microsoft.com/dynamics365/mixed-reality/guides/admin-deployment-playbook).</span></span>

## <a name="next-step"></a><span data-ttu-id="d648a-182">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="d648a-182">Next step</span></span> 
> [!div class="nextstepaction"]
> [<span data-ttu-id="d648a-183">Развертывание подключенных к корпоративной связи — настройка</span><span class="sxs-lookup"><span data-stu-id="d648a-183">Corporate connected deployment - Configure</span></span>](hololens2-corp-connected-configure.md)