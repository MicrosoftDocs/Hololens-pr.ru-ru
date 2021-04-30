---
title: Совместное использование HoloLens с несколькими людьми
description: Можно настроить использование HoloLens для совместного использования несколькими учетными записями Azure Active Directory или несколькими пользователями, использующими одну учетную запись.
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
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309550"
---
# <a name="share-your-hololens-with-multiple-people"></a><span data-ttu-id="b1d2a-103">Совместное использование HoloLens с несколькими людьми</span><span class="sxs-lookup"><span data-stu-id="b1d2a-103">Share your HoloLens with multiple people</span></span>

<span data-ttu-id="b1d2a-104">Общий доступ к одному HoloLens можно предоставить нескольким людям или нескольким людям, которые совместно используют набор устройств HoloLens.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-104">It's common to share one HoloLens with many people or to have many people share a set of HoloLens devices.</span></span>  <span data-ttu-id="b1d2a-105">В этой статье описываются различные способы предоставления общего доступа к устройству.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-105">This article describes the different ways in which you can share a device.</span></span>

## <a name="share-with-multiple-people-each-using-their-own-account"></a><span data-ttu-id="b1d2a-106">Предоставление общего доступа нескольким людям с использованием собственной учетной записи</span><span class="sxs-lookup"><span data-stu-id="b1d2a-106">Share with multiple people, each using their own account</span></span>

<span data-ttu-id="b1d2a-107">**Предварительные требования**. устройство HoloLens должно работать под управлением Windows 10 версии 1803 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-107">**Prerequisite**: The HoloLens device must be running Windows 10, version 1803 or later.</span></span>  <span data-ttu-id="b1d2a-108">Также необходимо обновить HoloLens (1-го поколения) [до Windows holographic for Business](hololens-upgrade-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="b1d2a-108">HoloLens (1st gen) also need to be [upgraded to Windows Holographic for Business](hololens-upgrade-enterprise.md).</span></span>

<span data-ttu-id="b1d2a-109">При использовании собственных учетных записей Azure Active Directory (Azure AD) несколько пользователей могут использовать собственные параметры пользователя и данные пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-109">When they use their own Azure Active Directory (Azure AD) accounts, multiple users can each keep their own user settings and user data on the device.</span></span>

<span data-ttu-id="b1d2a-110">Чтобы убедиться, что несколько пользователей могут использовать собственные учетные записи в HoloLens, выполните следующие действия, чтобы настроить его.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-110">To make sure that multiple people can use their own accounts on your HoloLens, follow these steps to configure it:</span></span>

1. <span data-ttu-id="b1d2a-111">Убедитесь, что устройство работает под управлением Windows 10 версии 1803 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-111">Make sure the the device is running Windows 10, version 1803 or later.</span></span>
   > [!IMPORTANT]
   > <span data-ttu-id="b1d2a-112">При использовании устройства HoloLens (1-го поколения) [Обновите устройство до Windows holographic для бизнеса](hololens1-upgrade-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="b1d2a-112">If you are using a HoloLens (1st gen) device, [upgrade the device to Windows Holographic for Business](hololens1-upgrade-enterprise.md).</span></span>
1. <span data-ttu-id="b1d2a-113">Когда вы настроите устройство, выберите **Моя работа или учебный заведение** , а затем выполните вход с помощью учетной записи Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-113">When you set up the device, select **My work or school owns it** and sign in by using an Azure AD account.</span></span>
1. <span data-ttu-id="b1d2a-114">После завершения установки убедитесь, что параметры учетной записи (  >  **учетные записи** параметров) включают **других пользователей**.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-114">After you finish setup, make sure that the account settings (**Settings** > **Accounts**) includes **Other users**.</span></span>

<span data-ttu-id="b1d2a-115">Чтобы использовать HoloLens, каждый пользователь выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b1d2a-115">To use HoloLens, each user follows these steps:</span></span>

1. <span data-ttu-id="b1d2a-116">Если устройство используется другим пользователем, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-116">If another user has been using the device, do one of the following:</span></span>
   - <span data-ttu-id="b1d2a-117">Нажмите кнопку питания один раз, чтобы вернуться в режим ожидания, а затем снова нажмите кнопку питания, чтобы вернуться на экран блокировки.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-117">Press the power button once to go to standby, and then press the power button again to return to the lock screen</span></span>
   - <span data-ttu-id="b1d2a-118">Пользователи HoloLens 2 могут выбрать плитку пользователя в меню "Пуск" для выхода текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-118">HoloLens 2 users may select the user tile from the Start menu to sign out the current user.</span></span>

1. <span data-ttu-id="b1d2a-119">Используйте учетные данные учетной записи Azure AD для входа на устройство.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-119">Use your Azure AD account credentials to sign in to the device.</span></span>  
    <span data-ttu-id="b1d2a-120">Если устройство используется впервые, необходимо [откалибровать](hololens-calibration.md) HoloLens от собственных глаз.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-120">If this is the first time that you have used the device, you have to [calibrate](hololens-calibration.md) HoloLens to your own eyes.</span></span>

<span data-ttu-id="b1d2a-121">Чтобы просмотреть список пользователей устройства или удалить пользователя с устройства, выберите **Параметры**  >  **учетные записи**  >  **другие пользователи**.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-121">To see a list of the device users or to remove a user from the device, go to **Settings** > **Accounts** > **Other users**.</span></span>

## <a name="share-with-multiple-people-all-using-the-same-account"></a><span data-ttu-id="b1d2a-122">Поделиться с несколькими людьми, используя одну и ту же учетную запись</span><span class="sxs-lookup"><span data-stu-id="b1d2a-122">Share with multiple people, all using the same account</span></span>

<span data-ttu-id="b1d2a-123">При использовании одной учетной записи пользователя несколько пользователей также могут совместно использовать устройство HoloLens.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-123">Multiple users can also share a HoloLens device while using a single user account.</span></span>

<span data-ttu-id="b1d2a-124">**В HoloLens 2**, когда новый пользователь помещает устройство в свое головное меню в первый раз (одновременно с сохранением той же учетной записи), устройство предлагает новому пользователю быстро откалибровать и персонализировать процесс просмотра.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-124">**On HoloLens 2**, when a new user puts the device on their head for the first time (while keeping the same account signed in), the device prompts the new user to quickly calibrate and personalize the viewing experience.</span></span> <span data-ttu-id="b1d2a-125">Устройство может хранить сведения о калибровке, чтобы в будущем устройство может автоматически оптимизировать качество и удобство работы пользователя.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-125">The device can store the calibration information so that in the future, the device can automatically optimize the quality and comfort of each user's viewing experience.</span></span> <span data-ttu-id="b1d2a-126">Пользователям не нужно выполнять калибровку устройства еще раз.</span><span class="sxs-lookup"><span data-stu-id="b1d2a-126">The users do not need to calibrate the device again.</span></span>

<span data-ttu-id="b1d2a-127">Для пользователей **HoloLens (1-го поколения)** , совместно использующих учетную запись, необходимо запросить перекалибровку в приложении "Параметры".</span><span class="sxs-lookup"><span data-stu-id="b1d2a-127">**On HoloLens (1st gen)** users sharing an account will need to ask to recalibrate in the Settings app.</span></span>  <span data-ttu-id="b1d2a-128">Подробнее о [калибровке](hololens-calibration.md).</span><span class="sxs-lookup"><span data-stu-id="b1d2a-128">Read more about [calibration](hololens-calibration.md).</span></span>
