---
title: Руководство по развертыванию — масштабное развертывание HoloLens 2 с подключением к облаку с помощью удаленной помощи — настройка
description: Настройка конфигураций для регистрации устройств HoloLens в сети Cloud Connected
keywords: HoloLens, управление, подключение к облаку, удаленная помощь, AAD, Azure AD, MDM, управление мобильными устройствами
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
ms.openlocfilehash: 042a29fe436b21ca37a2fcd7921fc53d6a9686d5
ms.sourcegitcommit: 96dcd015ad24169295690a8ed13ea1bf480e4b9e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/01/2021
ms.locfileid: "11253046"
---
# <span data-ttu-id="1c4a9-104">Configure — руководство по подключению к облаку</span><span class="sxs-lookup"><span data-stu-id="1c4a9-104">Configure - Cloud connected Guide</span></span>

<span data-ttu-id="1c4a9-105">В этом разделе руководства мы&#39;, как настроить автоматическую регистрацию для вашего клиента и как применить лицензии для Intune и удаленной помощи.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-105">In this section of the guide, we&#39;ll go over how to set up Auto Enrollment for your tenant, and how to apply licenses for both Intune and Remote Assist.</span></span>

## <span data-ttu-id="1c4a9-106">Пользователи и группы Azure</span><span class="sxs-lookup"><span data-stu-id="1c4a9-106">Azure Users and Groups</span></span>

<span data-ttu-id="1c4a9-107">Azure и Intune с таким расширением используют пользователей и группы для назначения конфигураций и лицензий.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-107">Azure, and Intune by that extension, uses users and groups to help assign configurations and licenses.</span></span> <span data-ttu-id="1c4a9-108">Для проверки этого потока развертывания и возможности вызова удаленной помощи от одного пользователя к другому вам&#39;две учетные записи пользователей.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-108">For the sake of validating this deployment flow and being able to make a Remote Assist call from one user to another you&#39;ll need two user accounts.</span></span>

<span data-ttu-id="1c4a9-109">Мы можем сделать одну группу пользователей для назначения лицензий.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-109">We can make a single user group for the purpose of assigning licenses.</span></span> <span data-ttu-id="1c4a9-110">Мы можем присоединить обоих пользователей к одной группе и применить к ней лицензию на Intune и удаленную помощь.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-110">We can join both users to the same group and apply a license for Intune and Remote Assist to that group.</span></span>

<span data-ttu-id="1c4a9-111">Если у вас&#39;есть доступ к двум учетным записям Azure AD в группе пользователей, вы можете использовать; вот краткие руководства по началу:</span><span class="sxs-lookup"><span data-stu-id="1c4a9-111">If you don&#39;t already have access to two Azure AD accounts in a user group you can use; here are the quick start guides for:</span></span>

- [<span data-ttu-id="1c4a9-112">Создание пользователя</span><span class="sxs-lookup"><span data-stu-id="1c4a9-112">How to create a user</span></span>](https://docs.microsoft.com/mem/intune/fundamentals/quickstart-create-user)
- [<span data-ttu-id="1c4a9-113">Создание группы</span><span class="sxs-lookup"><span data-stu-id="1c4a9-113">How to create a group</span></span>](https://docs.microsoft.com/mem/intune/fundamentals/quickstart-create-group)
- <span data-ttu-id="1c4a9-114">[Добавление пользователей в группу —](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-members-azure-portal) добавление созданных пользователей для создания группы</span><span class="sxs-lookup"><span data-stu-id="1c4a9-114">[Add users to a group](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-members-azure-portal) – Add created users to create group</span></span>
- <span data-ttu-id="1c4a9-115">[Настройка Azure AD, чтобы разрешить](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan#configure-your-device-settings) группе пользователей присоединяться к устройствам — убедитесь, что у новой группы пользователей есть разрешение на регистрацию устройств в Azure AD</span><span class="sxs-lookup"><span data-stu-id="1c4a9-115">[Configure Azure AD to allow a User Group to join devices](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan#configure-your-device-settings) – Ensure new user group has permission to enroll devices to Azure AD</span></span>

## <span data-ttu-id="1c4a9-116">Автоматическая регистрация на HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="1c4a9-116">Auto Enrollment on HoloLens 2</span></span>

<span data-ttu-id="1c4a9-117">Чтобы обеспечить плавность и простоту работы, можно перейти к настройке параметров реализации параметров реализации параметров Azure Active Directory (AADJ) и автоматической регистрации в Intune для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-117">In order to have a smooth and seamless experience, setting up Azure Active Directory Join (AADJ) and Auto Enrollment to Intune for HoloLens 2 devices is the way to go.</span></span> <span data-ttu-id="1c4a9-118">Это позволит пользователям вводить учетные данные для входа в организацию во время OOBE и автоматически регистрироваться в Azure AD и регистрировать устройство в MDM.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-118">This will allow users to input their organization log-in credentials during OOBE and automatically register with Azure AD and enroll the device into MDM.</span></span>

<span data-ttu-id="1c4a9-119">С помощью [Microsoft Endpoint Manager](https://endpoint.microsoft.com/#home)можно выбрать службы и перейти на несколько страниц, пока не будет выбрана пробная версия "Получить премиум".</span><span class="sxs-lookup"><span data-stu-id="1c4a9-119">By using [Microsoft Endpoint Manager](https://endpoint.microsoft.com/#home), we can select services and navigate a few pages until we can select Get a Premium trial.</span></span> <span data-ttu-id="1c4a9-120">Вы можете заметить, что для автоматической регистрации P1 достаточно Azure Active Directory Premium 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-120">You may notice there is Azure Active Directory Premium 1 and 2, for Automatic Enrollment P1 is sufficient.</span></span> <span data-ttu-id="1c4a9-121">Мы можем выбрать Intune, выбрать область пользователя для автоматической регистрации и выбрать группу, которая была создана ранее.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-121">We can select Intune and select the user scope for automatic enrollment, and select the group that was previously created.</span></span>

<span data-ttu-id="1c4a9-122">Подробные сведения и действия см. в руководстве о том, как включить автоматическую регистрацию [для Intune.](https://docs.microsoft.com/mem/intune/enrollment/quickstart-setup-auto-enrollment)</span><span class="sxs-lookup"><span data-stu-id="1c4a9-122">For full details and steps read the guide on [how to enable auto enrollment for Intune](https://docs.microsoft.com/mem/intune/enrollment/quickstart-setup-auto-enrollment).</span></span>

## <span data-ttu-id="1c4a9-123">Лицензии приложений</span><span class="sxs-lookup"><span data-stu-id="1c4a9-123">Application Licenses</span></span>

<span data-ttu-id="1c4a9-124">Лицензия приложения позволяет пользователю установить приобретенные компанией приложения или обновить бесплатную пробную версию до полной версии приложения.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-124">An application license allows a user to either install company purchased Apps or upgrade from a free trial to the full version of an app.</span></span> <span data-ttu-id="1c4a9-125">Лицензии приложений могут применяться к пользователям, группам пользователей или группам устройств.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-125">Application licenses can be applied to either users, user groups, or device groups.</span></span> <span data-ttu-id="1c4a9-126">Вам&#39;лицензии удаленной помощи, чтобы пользователи в организации могли использовать удаленную помощь.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-126">You&#39;ll need Remote Assist licenses for users in your organization to use Remote Assist.</span></span> <span data-ttu-id="1c4a9-127">В этом руководстве мы назначим лицензии удаленной поддержки группе пользователей, созданной выше в [azure Users and Groups.](hololens2-cloud-connected-configure.md#azure-users-and-groups)</span><span class="sxs-lookup"><span data-stu-id="1c4a9-127">For the purpose of this guide we'll assign Remote Assist licenses to the user group we created above in [Azure Users and Groups](hololens2-cloud-connected-configure.md#azure-users-and-groups).</span></span>

<span data-ttu-id="1c4a9-128">Требования к лицензиям могут быть разными в зависимости от того, будет ли пользователь звонить удаленной помощи с устройства или будет удаленным соавтором из Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-128">The requirements for licenses can be different depending on if the user will be making the Remote Assist call from a device or will be a remote collaborator from Microsoft Teams.</span></span> <span data-ttu-id="1c4a9-129">По умолчанию флажки "Удаленная помощь" и "Teams" помечаются.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-129">By default the Remote Assist and Teams check boxes are both marked.</span></span> <span data-ttu-id="1c4a9-130">В этом руководстве мы рекомендуем оставить флажки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-130">For the purposes of this guide, we suggest leaving the default boxes checked.</span></span>

1. <span data-ttu-id="1c4a9-131">Узнайте больше о различных [требованиях к лицензированию и продуктам для ролей.](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements#licensing-and-product-requirements-per-role)</span><span class="sxs-lookup"><span data-stu-id="1c4a9-131">Learn more about the different [Licensing and product requirements per role](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements#licensing-and-product-requirements-per-role).</span></span> <span data-ttu-id="1c4a9-132">Существует несколько различных типов лицензий удаленной помощи, поэтому не забудьте получить правильные лицензии для ваших потребностей.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-132">There are a few different types of Remote Assist licenses so be sure to get the correct ones for your needs.</span></span>
2. <span data-ttu-id="1c4a9-133">Вам&#39;[лицензию.](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-remote-assist)</span><span class="sxs-lookup"><span data-stu-id="1c4a9-133">You&#39;ll need to [acquire the license](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-remote-assist).</span></span>
3. <span data-ttu-id="1c4a9-134">[Примените лицензии](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/deploy-remote-assist) к группе.</span><span class="sxs-lookup"><span data-stu-id="1c4a9-134">[Apply your licenses](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/deploy-remote-assist) to the group.</span></span>

## <span data-ttu-id="1c4a9-135">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="1c4a9-135">Next step</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="1c4a9-136">Развертывание с подключением к облаку — развертывание</span><span class="sxs-lookup"><span data-stu-id="1c4a9-136">Cloud connected deployment - Deploy</span></span>](hololens2-cloud-connected-deploy.md)