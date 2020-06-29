---
title: Предоставление доступа к HoloLens нескольким пользователям
description: Вы можете настроить HoloLens для совместного использования несколькими учетными записями Azure Active Directory или несколькими пользователями с одной учетной записью.
ms.prod: hololens
ms.sitesec: library
author: scooley
ms.author: scooley
ms.topic: article
ms.localizationpriority: medium
ms.date: 09/16/2019
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 39de72bb704ff500b0262f2268d003a08d520eb2
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10829290"
---
# <span data-ttu-id="1d756-103">Предоставление доступа к HoloLens нескольким пользователям</span><span class="sxs-lookup"><span data-stu-id="1d756-103">Share your HoloLens with multiple people</span></span>

<span data-ttu-id="1d756-104">Вы обычно можете поделиться одним HoloLens с большим количеством людей или предоставить доступ к набору устройств HoloLens нескольким людям.</span><span class="sxs-lookup"><span data-stu-id="1d756-104">It's common to share one HoloLens with many people or to have many people share a set of HoloLens devices.</span></span>  <span data-ttu-id="1d756-105">В этой статье описаны различные способы предоставления общего доступа к устройству.</span><span class="sxs-lookup"><span data-stu-id="1d756-105">This article describes the different ways in which you can share a device.</span></span>

## <span data-ttu-id="1d756-106">Предоставление общего доступа нескольким людям с помощью своей учетной записи</span><span class="sxs-lookup"><span data-stu-id="1d756-106">Share with multiple people, each using their own account</span></span>

<span data-ttu-id="1d756-107">**Предварительный компонент**: устройство HoloLens должно работать под управлением Windows 10 версии 1803 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1d756-107">**Prerequisite**: The HoloLens device must be running Windows 10, version 1803 or later.</span></span>  <span data-ttu-id="1d756-108">HoloLens (1-го поколения) также необходимо [Обновить до Windows holographic для бизнеса](hololens-upgrade-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="1d756-108">HoloLens (1st gen) also need to be [upgraded to Windows Holographic for Business](hololens-upgrade-enterprise.md).</span></span>

<span data-ttu-id="1d756-109">Если в них используются собственные учетные записи Azure Active Directory (Azure AD), каждый пользователь может хранить свои собственные параметры пользователя и данные пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="1d756-109">When they use their own Azure Active Directory (Azure AD) accounts, multiple users can each keep their own user settings and user data on the device.</span></span>

<span data-ttu-id="1d756-110">Чтобы сделать так, чтобы несколько пользователей могли использовать собственные учетные записи на HoloLens, выполните указанные ниже действия, чтобы настроить его.</span><span class="sxs-lookup"><span data-stu-id="1d756-110">To make sure that multiple people can use their own accounts on your HoloLens, follow these steps to configure it:</span></span>

1. <span data-ttu-id="1d756-111">Убедитесь, что устройство работает под управлением Windows 10 версии 1803 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1d756-111">Make sure the the device is running Windows 10, version 1803 or later.</span></span>
   > [!IMPORTANT]
   > <span data-ttu-id="1d756-112">Если вы используете устройство HoloLens (1-го поколения), [Обновите устройство до Windows holographic для бизнеса](hololens1-upgrade-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="1d756-112">If you are using a HoloLens (1st gen) device, [upgrade the device to Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span></span>
1. <span data-ttu-id="1d756-113">Когда вы настраиваете устройство, выберите пункт **Моя работа или учебо владеете** и войдите в систему с помощью учетной записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1d756-113">When you set up the device, select **My work or school owns it** and sign in by using an Azure AD account.</span></span>
1. <span data-ttu-id="1d756-114">После завершения установки убедитесь в том, что параметры учетной записи**Settings**(  >  **учетные записи**параметров) включают **других пользователей**.</span><span class="sxs-lookup"><span data-stu-id="1d756-114">After you finish setup, make sure that the account settings (**Settings** > **Accounts**) includes **Other users**.</span></span>

<span data-ttu-id="1d756-115">Чтобы использовать HoloLens, каждый пользователь должен выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1d756-115">To use HoloLens, each user follows these steps:</span></span>

1. <span data-ttu-id="1d756-116">Если вы используете устройство другим пользователем, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="1d756-116">If another user has been using the device, do one of the following:</span></span>
   - <span data-ttu-id="1d756-117">Нажмите кнопку питания один раз, чтобы перейти в режим ожидания, а затем снова нажмите кнопку питания, чтобы вернуться на экран блокировки.</span><span class="sxs-lookup"><span data-stu-id="1d756-117">Press the power button once to go to standby, and then press the power button again to return to the lock screen</span></span>
   - <span data-ttu-id="1d756-118">Пользователи HoloLens 2 могут выбрать плитку пользователя в меню "Пуск", чтобы выйти из текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d756-118">HoloLens 2 users may select the user tile from the Start menu to sign out the current user.</span></span>

1. <span data-ttu-id="1d756-119">Используйте свои учетные данные учетной записи Azure AD, чтобы войти на устройство.</span><span class="sxs-lookup"><span data-stu-id="1d756-119">Use your Azure AD account credentials to sign in to the device.</span></span>  
    <span data-ttu-id="1d756-120">Если вы используете устройство в первый раз, вам придется [откалибровать](hololens-calibration.md) HoloLens с точки зрения своих глаз.</span><span class="sxs-lookup"><span data-stu-id="1d756-120">If this is the first time that you have used the device, you have to [calibrate](hololens-calibration.md) HoloLens to your own eyes.</span></span>

<span data-ttu-id="1d756-121">Чтобы просмотреть список пользователей устройства или удалить пользователя с устройства, перейдите в раздел **Параметры**  >  **учетные записи**  >  **других пользователей**.</span><span class="sxs-lookup"><span data-stu-id="1d756-121">To see a list of the device users or to remove a user from the device, go to **Settings** > **Accounts** > **Other users**.</span></span>

## <span data-ttu-id="1d756-122">Предоставление общего доступа нескольким людям с одной учетной записью</span><span class="sxs-lookup"><span data-stu-id="1d756-122">Share with multiple people, all using the same account</span></span>

<span data-ttu-id="1d756-123">Кроме того, при использовании одной учетной записи пользователи могут совместно использовать устройство HoloLens.</span><span class="sxs-lookup"><span data-stu-id="1d756-123">Multiple users can also share a HoloLens device while using a single user account.</span></span>

<span data-ttu-id="1d756-124">**В HoloLens 2**, когда новый пользователь помещает устройство в заголовке в первый раз (одновременно с тем, что она была зарегистрирована), устройство предлагает новому пользователю быстро откалибровать и настроить режим просмотра.</span><span class="sxs-lookup"><span data-stu-id="1d756-124">**On HoloLens 2**, when a new user puts the device on their head for the first time (while keeping the same account signed in), the device prompts the new user to quickly calibrate and personalize the viewing experience.</span></span> <span data-ttu-id="1d756-125">Устройство может хранить сведения о калибровке, чтобы в будущем устройства могли автоматически оптимизировать качество и удобство просмотра для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d756-125">The device can store the calibration information so that in the future, the device can automatically optimize the quality and comfort of each user's viewing experience.</span></span> <span data-ttu-id="1d756-126">Пользователям не нужно откалибровать устройство еще раз.</span><span class="sxs-lookup"><span data-stu-id="1d756-126">The users do not need to calibrate the device again.</span></span>

<span data-ttu-id="1d756-127">**Для пользователей HoloLens (1-го поколения)** , которые совместно с учетной записью, вам потребуется повторно откалибровать ее в приложении "Параметры".</span><span class="sxs-lookup"><span data-stu-id="1d756-127">**On HoloLens (1st gen)** users sharing an account will need to ask to recalibrate in the Settings app.</span></span>  <span data-ttu-id="1d756-128">Узнайте больше о [калибровке](hololens-calibration.md).</span><span class="sxs-lookup"><span data-stu-id="1d756-128">Read more about [calibration](hololens-calibration.md).</span></span>
