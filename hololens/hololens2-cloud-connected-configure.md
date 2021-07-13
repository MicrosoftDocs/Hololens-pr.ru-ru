---
title: 'руководство по развертыванию: облачное подключение HoloLens 2 развертывание в масштабе с помощью удаленного помощника — настройка'
description: узнайте, как настроить конфигурацию для регистрации HoloLens устройств через облачную подключенную сеть в масштабе с помощью удаленного помощника.
keywords: HoloLens, управление, облачное подключение, удаленное помощник, AAD, Azure AD, MDM, управление мобильными устройствами
author: evmill
ms.author: v-evmill
ms.reviewer: aboeger
ms.date: 12/04/2020
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: eb96f1cdc799551297c0373268e8cc8f35c6bd06
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113635149"
---
# <a name="configure---cloud-connected-guide"></a><span data-ttu-id="fc0df-104">Настройка — Путеводитель по подключению к облаку</span><span class="sxs-lookup"><span data-stu-id="fc0df-104">Configure - Cloud connected Guide</span></span>

<span data-ttu-id="fc0df-105">В этом разделе руководства мы&#39;все, как настроить автоматическую регистрацию для клиента и как применять лицензии для Intune и удаленного помощника.</span><span class="sxs-lookup"><span data-stu-id="fc0df-105">In this section of the guide, we&#39;ll go over how to set up Auto Enrollment for your tenant, and how to apply licenses for both Intune and Remote Assist.</span></span>

## <a name="azure-users-and-groups"></a><span data-ttu-id="fc0df-106">Пользователи и группы Azure</span><span class="sxs-lookup"><span data-stu-id="fc0df-106">Azure Users and Groups</span></span>

<span data-ttu-id="fc0df-107">Azure и Intune с этим расширением используют пользователей и группы для назначения конфигураций и лицензий.</span><span class="sxs-lookup"><span data-stu-id="fc0df-107">Azure, and Intune by that extension, uses users and groups to help assign configurations and licenses.</span></span> <span data-ttu-id="fc0df-108">Для проверки этого потока развертывания и возможности удаленного вызова помощника от одного пользователя к другому Вам&#39;понадобятся две учетные записи пользователей.</span><span class="sxs-lookup"><span data-stu-id="fc0df-108">For the sake of validating this deployment flow and being able to make a Remote Assist call from one user to another you&#39;ll need two user accounts.</span></span>

<span data-ttu-id="fc0df-109">Для назначения лицензий можно создать одну группу пользователей.</span><span class="sxs-lookup"><span data-stu-id="fc0df-109">We can make a single user group for the purpose of assigning licenses.</span></span> <span data-ttu-id="fc0df-110">Можно присоединить пользователей к одной группе и применить лицензию для Intune и удаленного помощника для этой группы.</span><span class="sxs-lookup"><span data-stu-id="fc0df-110">We can join both users to the same group and apply a license for Intune and Remote Assist to that group.</span></span>

<span data-ttu-id="fc0df-111">Если у вас нет&#39;у вас уже есть доступ к двум учетным записям Azure AD в группе пользователей, которые можно использовать; Ниже приведены краткие руководства по началу работы.</span><span class="sxs-lookup"><span data-stu-id="fc0df-111">If you don&#39;t already have access to two Azure AD accounts in a user group you can use; here are the quick start guides for:</span></span>

- [<span data-ttu-id="fc0df-112">Создание пользователя</span><span class="sxs-lookup"><span data-stu-id="fc0df-112">How to create a user</span></span>](/mem/intune/fundamentals/quickstart-create-user)
- [<span data-ttu-id="fc0df-113">Создание группы</span><span class="sxs-lookup"><span data-stu-id="fc0df-113">How to create a group</span></span>](/mem/intune/fundamentals/quickstart-create-group)
- <span data-ttu-id="fc0df-114">[Добавление пользователей в группу](/azure/active-directory/fundamentals/active-directory-groups-members-azure-portal) — Добавление созданных пользователей для создания группы</span><span class="sxs-lookup"><span data-stu-id="fc0df-114">[Add users to a group](/azure/active-directory/fundamentals/active-directory-groups-members-azure-portal) – Add created users to create group</span></span>
- <span data-ttu-id="fc0df-115">[Настройка Azure AD для предоставления группе пользователей возможности присоединять устройства](/azure/active-directory/devices/azureadjoin-plan#configure-your-device-settings) — убедитесь, что у новой группы пользователей есть разрешение на регистрацию устройств в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="fc0df-115">[Configure Azure AD to allow a User Group to join devices](/azure/active-directory/devices/azureadjoin-plan#configure-your-device-settings) – Ensure new user group has permission to enroll devices to Azure AD</span></span>

## <a name="auto-enrollment-on-hololens-2"></a><span data-ttu-id="fc0df-116">Автоматическая регистрация в HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="fc0df-116">Auto Enrollment on HoloLens 2</span></span>

<span data-ttu-id="fc0df-117">чтобы обеспечить плавность и удобство работы, настройте Azure Active Directory присоединение (AADJ) и автоматическую регистрацию в Intune для HoloLens 2 устройств — это способ перехода.</span><span class="sxs-lookup"><span data-stu-id="fc0df-117">In order to have a smooth and seamless experience, setting up Azure Active Directory Join (AADJ) and Auto Enrollment to Intune for HoloLens 2 devices is the way to go.</span></span> <span data-ttu-id="fc0df-118">Это позволит пользователям вводить учетные данные для входа в Организации во время OOBE и автоматически регистрироваться в Azure AD и регистрировать устройство в MDM.</span><span class="sxs-lookup"><span data-stu-id="fc0df-118">This will allow users to input their organization log-in credentials during OOBE and automatically register with Azure AD and enroll the device into MDM.</span></span>

<span data-ttu-id="fc0df-119">используя [Microsoft Endpoint Manager](https://endpoint.microsoft.com/#home), можно выбрать службы и перейти на несколько страниц, пока не сможете выбрать получить пробную версию Premium.</span><span class="sxs-lookup"><span data-stu-id="fc0df-119">By using [Microsoft Endpoint Manager](https://endpoint.microsoft.com/#home), we can select services and navigate a few pages until we can select Get a Premium trial.</span></span> <span data-ttu-id="fc0df-120">вы можете заметить, что существует Azure Active Directory Premium 1 и 2, что для автоматической регистрации P1 достаточно.</span><span class="sxs-lookup"><span data-stu-id="fc0df-120">You may notice there is Azure Active Directory Premium 1 and 2, for Automatic Enrollment P1 is sufficient.</span></span> <span data-ttu-id="fc0df-121">Мы можем выбрать Intune и выбрать область пользователя для автоматической регистрации и выбрать ранее созданную группу.</span><span class="sxs-lookup"><span data-stu-id="fc0df-121">We can select Intune and select the user scope for automatic enrollment, and select the group that was previously created.</span></span>

<span data-ttu-id="fc0df-122">Полные сведения и инструкции см. в руководстве по [включению автоматической регистрации для Intune](/mem/intune/enrollment/quickstart-setup-auto-enrollment).</span><span class="sxs-lookup"><span data-stu-id="fc0df-122">For full details and steps read the guide on [how to enable auto enrollment for Intune](/mem/intune/enrollment/quickstart-setup-auto-enrollment).</span></span>

## <a name="application-licenses"></a><span data-ttu-id="fc0df-123">Лицензии приложений</span><span class="sxs-lookup"><span data-stu-id="fc0df-123">Application Licenses</span></span>

<span data-ttu-id="fc0df-124">Лицензия на приложение позволяет пользователю либо установить приобретенные продукты компании, либо перейти с бесплатной пробной версии на полную версию приложения.</span><span class="sxs-lookup"><span data-stu-id="fc0df-124">An application license allows a user to either install company purchased Apps or upgrade from a free trial to the full version of an app.</span></span> <span data-ttu-id="fc0df-125">Лицензии на приложения можно применять к пользователям, группам пользователей или группам устройств.</span><span class="sxs-lookup"><span data-stu-id="fc0df-125">Application licenses can be applied to either users, user groups, or device groups.</span></span> <span data-ttu-id="fc0df-126">Чтобы использовать удаленную помощь пользователям в вашей организации, вам&#39;все необходимые лицензии удаленного помощника.</span><span class="sxs-lookup"><span data-stu-id="fc0df-126">You&#39;ll need Remote Assist licenses for users in your organization to use Remote Assist.</span></span> <span data-ttu-id="fc0df-127">В рамках этого руководством мы назовем лицензии удаленного помощника группе пользователей, созданной ранее в разделе [Пользователи и группы Azure](hololens2-cloud-connected-configure.md#azure-users-and-groups).</span><span class="sxs-lookup"><span data-stu-id="fc0df-127">For the purpose of this guide we'll assign Remote Assist licenses to the user group we created above in [Azure Users and Groups](hololens2-cloud-connected-configure.md#azure-users-and-groups).</span></span>

<span data-ttu-id="fc0df-128">Требования к лицензиям могут отличаться в зависимости от того, будет ли пользователь выполнять удаленный помощник для вызова с устройства или удаленный совместный доступ от Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="fc0df-128">The requirements for licenses can be different depending on if the user will be making the Remote Assist call from a device or will be a remote collaborator from Microsoft Teams.</span></span> <span data-ttu-id="fc0df-129">по умолчанию флажки Remote Assist и Teams помечены как.</span><span class="sxs-lookup"><span data-stu-id="fc0df-129">By default the Remote Assist and Teams check boxes are both marked.</span></span> <span data-ttu-id="fc0df-130">В рамках этого руководств мы рекомендуем отказаться от установленных флажков по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc0df-130">For the purposes of this guide, we suggest leaving the default boxes checked.</span></span>

1. <span data-ttu-id="fc0df-131">Узнайте больше о различных [требованиях к лицензированию и продукту для каждой роли](/dynamics365/mixed-reality/remote-assist/requirements#licensing-and-product-requirements-per-role).</span><span class="sxs-lookup"><span data-stu-id="fc0df-131">Learn more about the different [Licensing and product requirements per role](/dynamics365/mixed-reality/remote-assist/requirements#licensing-and-product-requirements-per-role).</span></span> <span data-ttu-id="fc0df-132">Существует несколько различных типов лицензий удаленного помощника, поэтому обязательно получите правильные требования.</span><span class="sxs-lookup"><span data-stu-id="fc0df-132">There are a few different types of Remote Assist licenses so be sure to get the correct ones for your needs.</span></span>
2. <span data-ttu-id="fc0df-133">Вам&#39;все необходимое для [получения лицензии](/dynamics365/mixed-reality/remote-assist/buy-remote-assist).</span><span class="sxs-lookup"><span data-stu-id="fc0df-133">You&#39;ll need to [acquire the license](/dynamics365/mixed-reality/remote-assist/buy-remote-assist).</span></span>
3. <span data-ttu-id="fc0df-134">[Примените лицензии](/dynamics365/mixed-reality/remote-assist/deploy-remote-assist) к группе.</span><span class="sxs-lookup"><span data-stu-id="fc0df-134">[Apply your licenses](/dynamics365/mixed-reality/remote-assist/deploy-remote-assist) to the group.</span></span>

## <a name="next-step"></a><span data-ttu-id="fc0df-135">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="fc0df-135">Next step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="fc0df-136">Развертывание с подключением к облаку — развертывание</span><span class="sxs-lookup"><span data-stu-id="fc0df-136">Cloud connected deployment - Deploy</span></span>](hololens2-cloud-connected-deploy.md)