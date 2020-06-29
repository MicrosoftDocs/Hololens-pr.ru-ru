---
title: Настройка HoloLens в коммерческой среде
description: Узнайте больше о том, как развертывать HoloLens и управлять ими в корпоративных средах.
ms.prod: hololens
ms.sitesec: library
ms.assetid: 88bf50aa-0bac-4142-afa4-20b37c013001
author: scooley
ms.author: scooley
audience: ITPro
ms.topic: article
ms.localizationpriority: medium
ms.date: 07/15/2019
ms.openlocfilehash: 8aa8e0f679ad18a2e47f34c5f1233435a502dc0c
ms.sourcegitcommit: f3cda6c6b3bfb7ba4be5f4da66d8ed5b03ca807d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2020
ms.locfileid: "10830133"
---
# <span data-ttu-id="4d20a-103">Развертывание HoloLens в коммерческой среде</span><span class="sxs-lookup"><span data-stu-id="4d20a-103">Deploy HoloLens in a commercial environment</span></span>

<span data-ttu-id="4d20a-104">Вы можете развернуть и настроить HoloLens на уровне шкалы в коммерческой настройке.</span><span class="sxs-lookup"><span data-stu-id="4d20a-104">You can deploy and configure HoloLens at scale in a commercial setting.</span></span> <span data-ttu-id="4d20a-105">В этой статье приводятся инструкции по развертыванию устройств HoloLens в коммерческой среде.</span><span class="sxs-lookup"><span data-stu-id="4d20a-105">This article provides instructions for deploying HoloLens devices in a commercial environment.</span></span> <span data-ttu-id="4d20a-106">В этом руководстве предполагается, что вы знаете основы работы с HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4d20a-106">This guide assumes basic familiarity with HoloLens.</span></span> <span data-ttu-id="4d20a-107">Чтобы настроить HoloLens в первый раз, следуйте указаниям, приведенным в разделе " [Приступая к работе](hololens1-setup.md) ".</span><span class="sxs-lookup"><span data-stu-id="4d20a-107">Follow the [get started guide](hololens1-setup.md) to set up HoloLens for the first time.</span></span>

<span data-ttu-id="4d20a-108">Кроме того, в этом документе предполагается, что HoloLens был оценен группами безопасности как безопасные для использования в корпоративной сети.</span><span class="sxs-lookup"><span data-stu-id="4d20a-108">This document also assumes that the HoloLens has been evaluated by security teams as safe to use on the corporate network.</span></span> <span data-ttu-id="4d20a-109">Ответы на часто задаваемые вопросы о безопасности можно найти [здесь](hololens-faq-security.md)</span><span class="sxs-lookup"><span data-stu-id="4d20a-109">Frequently asked security questions can be found [here](hololens-faq-security.md)</span></span>

## <span data-ttu-id="4d20a-110">Общие сведения о действиях по развертыванию</span><span class="sxs-lookup"><span data-stu-id="4d20a-110">Overview of Deployment Steps</span></span>

1. [<span data-ttu-id="4d20a-111">Определение необходимых функций</span><span class="sxs-lookup"><span data-stu-id="4d20a-111">Determine what features you need</span></span>](hololens-requirements.md#step-1-determine-what-you-need)
1. [<span data-ttu-id="4d20a-112">Определение необходимых лицензий</span><span class="sxs-lookup"><span data-stu-id="4d20a-112">Determine what licenses you need</span></span>](hololens-licenses-requirements.md)
1. <span data-ttu-id="4d20a-113">[Настройте сеть для HoloLens](hololens-commercial-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="4d20a-113">[Configure your network for HoloLens](hololens-commercial-infrastructure.md).</span></span>
    1. <span data-ttu-id="4d20a-114">Этот раздел содержит требования к пропускной способности, URL-адреса и порты, которые должны быть разрешены в брандмауэре; Руководство по Azure AD; Руководство по управлению мобильными устройствами (MDM); Руководство по развертыванию и управлению приложениями; и руководство по сертификатам.</span><span class="sxs-lookup"><span data-stu-id="4d20a-114">This section includes bandwidth requirements, URL, and ports that need to be allowed on your firewall; Azure AD guidance; Mobile Device Management (MDM) Guidance; app deployment/management guidance; and certificate guidance.</span></span>
1. <span data-ttu-id="4d20a-115">Необязательно [Настройка HoloLens с помощью пакета подготовки](hololens-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="4d20a-115">(Optional) [Configure HoloLens using a provisioning package](hololens-provisioning.md)</span></span>
1. [<span data-ttu-id="4d20a-116">Регистрация устройства</span><span class="sxs-lookup"><span data-stu-id="4d20a-116">Enroll Device</span></span>](hololens-enroll-mdm.md)
1. [<span data-ttu-id="4d20a-117">Настройка обновлений в рамках кругов обновлений для HoloLens</span><span class="sxs-lookup"><span data-stu-id="4d20a-117">Set up ring based updates for HoloLens</span></span>](hololens-updates.md)
1. [<span data-ttu-id="4d20a-118">Включение шифрования устройств Bitlocker для HoloLens</span><span class="sxs-lookup"><span data-stu-id="4d20a-118">Enable Bitlocker device encryption for HoloLens</span></span>](hololens-encryption.md)

## <span data-ttu-id="4d20a-119">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="4d20a-119">Step 1.</span></span> <span data-ttu-id="4d20a-120">Определение необходимых сведений</span><span class="sxs-lookup"><span data-stu-id="4d20a-120">Determine what you need</span></span>

<span data-ttu-id="4d20a-121">Прежде чем развертывать HoloLens в среде, важно сначала определить, какие функции, приложения и типы удостоверений необходимы.</span><span class="sxs-lookup"><span data-stu-id="4d20a-121">Before deploying the HoloLens in your environment, it is important to first determine what features, apps, and type of identities are needed.</span></span> <span data-ttu-id="4d20a-122">Также важно убедиться, что ваша группа безопасности утвердила использование HoloLens в сети компании.</span><span class="sxs-lookup"><span data-stu-id="4d20a-122">It is also important to ensure that your security team has approved of the use of the HoloLens on the company's network.</span></span> <span data-ttu-id="4d20a-123">Дополнительные сведения о безопасности можно найти в разделе [вопросы и ответы по безопасности](hololens-faq-security.md) .</span><span class="sxs-lookup"><span data-stu-id="4d20a-123">Please see [Frequently ask security questions](hololens-faq-security.md) for additional security information.</span></span>

### <span data-ttu-id="4d20a-124">Тип удостоверения</span><span class="sxs-lookup"><span data-stu-id="4d20a-124">Type of Identity</span></span>

<span data-ttu-id="4d20a-125">Определите тип удостоверения, который будет использоваться для входа на устройство.</span><span class="sxs-lookup"><span data-stu-id="4d20a-125">Determine the type of identity that will be used to sign into the device.</span></span>

1. <span data-ttu-id="4d20a-126">**Локальные учетные записи:** Эта учетная запись является локальной для устройства (например, учетной записи локального администратора на компьютере с Windows).</span><span class="sxs-lookup"><span data-stu-id="4d20a-126">**Local Accounts:** This account is local to the device (like a local admin account on a windows PC).</span></span> <span data-ttu-id="4d20a-127">Это позволит только 1 пользователю войти на устройство.</span><span class="sxs-lookup"><span data-stu-id="4d20a-127">This will allow only 1 user to log into the device.</span></span>
2. <span data-ttu-id="4d20a-128">**MSA:** Это личная учетная запись (например, Outlook, Hotmail, Gmail, Yahoo и т. д.) Это позволит только 1 пользователю войти на устройство.</span><span class="sxs-lookup"><span data-stu-id="4d20a-128">**MSA:** This is a personal account (like outlook, hotmail, gmail, yahoo, etc.) This will allow only 1 user to log into the device.</span></span>
3. <span data-ttu-id="4d20a-129">**Учетные записи Azure Active Directory (Azure AD):** Это учетная запись, созданная в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4d20a-129">**Azure Active Directory (Azure AD) accounts:** This is an account created in Azure AD.</span></span> <span data-ttu-id="4d20a-130">Благодаря этому в вашей организации предоставляется возможность управлять устройством HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4d20a-130">This grants your corporation the ability to manage the HoloLens device.</span></span> <span data-ttu-id="4d20a-131">Это позволит нескольким пользователям входить в одноранговый набор "HoloLens 1"/устройство HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="4d20a-131">This will allow multiple users to log into the HoloLens 1st Gen Commercial Suite/the HoloLens 2 device.</span></span>

<span data-ttu-id="4d20a-132">Для получения более подробной информации о типах удостоверений обратитесь к нашей статье [удостоверение HoloLens](hololens-identity.md) .</span><span class="sxs-lookup"><span data-stu-id="4d20a-132">For more detailed information about identity types, please visit our [HoloLens Identity](hololens-identity.md) article.</span></span>

### <span data-ttu-id="4d20a-133">Тип функций</span><span class="sxs-lookup"><span data-stu-id="4d20a-133">Type of Features</span></span>

<span data-ttu-id="4d20a-134">Ваши требования к функциям будут определять, какой HoloLens вам нужен.</span><span class="sxs-lookup"><span data-stu-id="4d20a-134">Your feature requirements will determine which HoloLens you need.</span></span> <span data-ttu-id="4d20a-135">Одной из распространенных функций, которые мы развернут в средах клиентов, часто является режим киоска.</span><span class="sxs-lookup"><span data-stu-id="4d20a-135">One popular feature that we see deployed in customer environments frequently is Kiosk Mode.</span></span> <span data-ttu-id="4d20a-136">Вы [можете найти список](hololens-commercial-features.md)функций ключа HoloLens и выпусков, поддерживающих их.</span><span class="sxs-lookup"><span data-stu-id="4d20a-136">A list of HoloLens key features, and the editions of HoloLens that support them, can be found [here](hololens-commercial-features.md).</span></span>

**<span data-ttu-id="4d20a-137">Что такое режим киоска?</span><span class="sxs-lookup"><span data-stu-id="4d20a-137">What is Kiosk Mode?</span></span>**

<span data-ttu-id="4d20a-138">Режим киоска — это способ ограничения доступа к приложениям, к которым у пользователя есть доступ.</span><span class="sxs-lookup"><span data-stu-id="4d20a-138">Kiosk mode is a way to restrict the apps that a user has access to.</span></span> <span data-ttu-id="4d20a-139">Это означает, что пользователям будет разрешен доступ только к определенным приложениям.</span><span class="sxs-lookup"><span data-stu-id="4d20a-139">This means that users will only be allowed to access certain apps.</span></span>

**<span data-ttu-id="4d20a-140">Что нужен режим киоска?</span><span class="sxs-lookup"><span data-stu-id="4d20a-140">What Kiosk Mode do I require?</span></span>**

<span data-ttu-id="4d20a-141">Существует два типа режимов киосков: одно приложение и несколько приложений.</span><span class="sxs-lookup"><span data-stu-id="4d20a-141">There are two types of Kiosk Modes: Single app and multi-app.</span></span> <span data-ttu-id="4d20a-142">Режим киоска в одном приложении позволяет пользователю получать доступ только к одному приложению, в то время как режим киоска с несколькими приложениями позволяет пользователям получить доступ к нескольким указанным приложениям.</span><span class="sxs-lookup"><span data-stu-id="4d20a-142">Single app kiosk mode allows user to only access one app while multi-app kiosk mode allows users to access multiple, specified apps.</span></span> <span data-ttu-id="4d20a-143">Чтобы определить, какой режим киоска подостанет для вашей организации, необходимо ответить на следующие два вопроса.</span><span class="sxs-lookup"><span data-stu-id="4d20a-143">To determine which kiosk mode is right for your corporation, the following two questions need to be answered:</span></span>

1. **<span data-ttu-id="4d20a-144">Требуются ли другие пользователи для разных функций и ограничений?</span><span class="sxs-lookup"><span data-stu-id="4d20a-144">Do different users require different experiences/restrictions?</span></span>** <span data-ttu-id="4d20a-145">Например, пользователь A является инженером службы полей, которому нужен доступ только к удаленному помощнику.</span><span class="sxs-lookup"><span data-stu-id="4d20a-145">Consider the following example: User A is a field service engineer who only needs access to Remote Assist.</span></span> <span data-ttu-id="4d20a-146">Пользователь B — это учащиеся, которым нужен доступ только к направляющим.</span><span class="sxs-lookup"><span data-stu-id="4d20a-146">User B is a trainee who only needs access to Guides.</span></span>
    1. <span data-ttu-id="4d20a-147">Если да, вам потребуется следующее:</span><span class="sxs-lookup"><span data-stu-id="4d20a-147">If yes, you will require the following:</span></span>
        1. <span data-ttu-id="4d20a-148">Учетные записи Azure AD как способ входа на устройство.</span><span class="sxs-lookup"><span data-stu-id="4d20a-148">Azure AD Accounts as the method of signing into the device.</span></span>
        1. <span data-ttu-id="4d20a-149">Режим киоска **с несколькими приложениями** .</span><span class="sxs-lookup"><span data-stu-id="4d20a-149">**Multi-app** kiosk mode.</span></span>
    1. <span data-ttu-id="4d20a-150">Если нет, нажимайте на вопрос два</span><span class="sxs-lookup"><span data-stu-id="4d20a-150">If no, continue to question two</span></span>
1. **<span data-ttu-id="4d20a-151">Требуется ли вам работать с несколькими приложениями?</span><span class="sxs-lookup"><span data-stu-id="4d20a-151">Do you require a multi-app experience?</span></span>**
    1. <span data-ttu-id="4d20a-152">Если да, требуется **несколько приложений** в режиме киоска</span><span class="sxs-lookup"><span data-stu-id="4d20a-152">If yes, **Multi-app** kiosk is mode is needed</span></span>
    1. <span data-ttu-id="4d20a-153">Если вы ответили на вопрос 1 и 2, вы можете использовать одновременный режим киоска в **одном приложении** .</span><span class="sxs-lookup"><span data-stu-id="4d20a-153">If your answer to question 1 and 2 are both no, **single-app** kiosk mode can be used</span></span>

**<span data-ttu-id="4d20a-154">Как настроить режим киоска, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4d20a-154">How to Configure Kiosk Mode:</span></span>**

<span data-ttu-id="4d20a-155">Существует два основных способа ([подготовка пакетов](hololens-kiosk.md#use-a-provisioning-package-to-set-up-a-single-app-or-multi-app-kiosk) и [MDM](hololens-kiosk.md#use-microsoft-intune-or-other-mdm-to-set-up-a-single-app-or-multi-app-kiosk)) для развертывания режима киоска для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4d20a-155">There are two main ways ([provisioning packages](hololens-kiosk.md#use-a-provisioning-package-to-set-up-a-single-app-or-multi-app-kiosk) and [MDM](hololens-kiosk.md#use-microsoft-intune-or-other-mdm-to-set-up-a-single-app-or-multi-app-kiosk)) to deploy kiosk mode for HoloLens.</span></span> <span data-ttu-id="4d20a-156">Эти параметры будут обсуждаться далее в документе; Однако вы можете воспользоваться приведенными выше ссылками, чтобы перейти к соответствующим разделам в этом документе.</span><span class="sxs-lookup"><span data-stu-id="4d20a-156">These options will be discussed later in the document; however, you can use the links above to jump to the respective sections in this doc.</span></span>

### <span data-ttu-id="4d20a-157">Особые сценарии приложений и приложений</span><span class="sxs-lookup"><span data-stu-id="4d20a-157">Apps and App Specific Scenarios</span></span>

<span data-ttu-id="4d20a-158">Большинство шагов, описанных в данном документе, также применимо к следующим приложениям:</span><span class="sxs-lookup"><span data-stu-id="4d20a-158">The majority of the steps found in this document will also apply to the following apps:</span></span>

| <span data-ttu-id="4d20a-159">Приложение</span><span class="sxs-lookup"><span data-stu-id="4d20a-159">App</span></span> | <span data-ttu-id="4d20a-160">Сценарии для конкретных приложений</span><span class="sxs-lookup"><span data-stu-id="4d20a-160">App Specific Scenarios</span></span> |
| --- | --- |
| <span data-ttu-id="4d20a-161">Удаленная помощь</span><span class="sxs-lookup"><span data-stu-id="4d20a-161">Remote Assist</span></span> | [<span data-ttu-id="4d20a-162">Связь между клиентами</span><span class="sxs-lookup"><span data-stu-id="4d20a-162">Cross Tenant Communication</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview)|
| <span data-ttu-id="4d20a-163">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="4d20a-163">Guides</span></span>  | *<span data-ttu-id="4d20a-164">Скоро</span><span class="sxs-lookup"><span data-stu-id="4d20a-164">Coming Soon</span></span>* |
|<span data-ttu-id="4d20a-165">Пользовательские приложения</span><span class="sxs-lookup"><span data-stu-id="4d20a-165">Custom Apps</span></span> | *<span data-ttu-id="4d20a-166">Скоро</span><span class="sxs-lookup"><span data-stu-id="4d20a-166">Coming Soon</span></span>* |

### <span data-ttu-id="4d20a-167">Определение способа регистрации</span><span class="sxs-lookup"><span data-stu-id="4d20a-167">Determine your enrollment method</span></span>

1. <span data-ttu-id="4d20a-168">Массовая регистрация с помощью маркера безопасности в пакете подготовки.</span><span class="sxs-lookup"><span data-stu-id="4d20a-168">Bulk enrollment with a security token in a provisioning package.</span></span>  
  <span data-ttu-id="4d20a-169">Профессионалы: этот подход является наиболее автоматизированным.</span><span class="sxs-lookup"><span data-stu-id="4d20a-169">Pros: this is the most automated approach\</span></span>
  <span data-ttu-id="4d20a-170">Параметр "против" используется для начальной настройки серверной части</span><span class="sxs-lookup"><span data-stu-id="4d20a-170">Cons: takes initial server-side setup</span></span>  
1. <span data-ttu-id="4d20a-171">Автоматическая регистрация при входе пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d20a-171">Auto-enroll on user sign in.</span></span>  
  <span data-ttu-id="4d20a-172">Профессионалы: простой подход</span><span class="sxs-lookup"><span data-stu-id="4d20a-172">Pros: easiest approach</span></span>  
  <span data-ttu-id="4d20a-173">Противном случае пользователи должны будут выполнить настройку после применения пакета подготовки.</span><span class="sxs-lookup"><span data-stu-id="4d20a-173">Cons: users will need to complete set up after the provisioning package has been applied</span></span>
1. <span data-ttu-id="4d20a-174">_не рекомендуется_ — ручная регистрация после настройки.</span><span class="sxs-lookup"><span data-stu-id="4d20a-174">_not recommended_ - Manually enroll post-setup.</span></span>  
  <span data-ttu-id="4d20a-175">Для профессионалов: возможна регистрация после настройки</span><span class="sxs-lookup"><span data-stu-id="4d20a-175">Pros: possible to enroll after set up</span></span>  
  <span data-ttu-id="4d20a-176">"Против": большинство методов и устройств, которые вы используете вручную, не управляются централизованно, пока они не будут зарегистрированы вручную.</span><span class="sxs-lookup"><span data-stu-id="4d20a-176">Cons: most manual approach and devices aren't centrally manageable until they're manually enrolled.</span></span>

  <span data-ttu-id="4d20a-177">Дополнительные сведения можно найти [здесь](hololens-enroll-mdm.md)</span><span class="sxs-lookup"><span data-stu-id="4d20a-177">More information can be found [here](hololens-enroll-mdm.md)</span></span>

### <span data-ttu-id="4d20a-178">Определение необходимости создания пакета подготовки</span><span class="sxs-lookup"><span data-stu-id="4d20a-178">Determine if you need to create a provisioning package</span></span>

<span data-ttu-id="4d20a-179">Существует два способа настройки устройства HoloLens (подготовка пакетов и MDMs).</span><span class="sxs-lookup"><span data-stu-id="4d20a-179">There are two methods to configure a HoloLens device (Provisioning packages and MDMs).</span></span> <span data-ttu-id="4d20a-180">Мы рекомендуем использовать MDM для настройки устройства HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4d20a-180">We suggest using your MDM to configure you HoloLens device.</span></span> <span data-ttu-id="4d20a-181">Однако существуют некоторые сценарии, в которых использование пакета подготовки является лучшим вариантом.</span><span class="sxs-lookup"><span data-stu-id="4d20a-181">However, there are some scenarios where using a provisioning package is the better choice:</span></span>

1. <span data-ttu-id="4d20a-182">Вы хотите настроить HoloLens для пропуска интерфейса приветствия (OOBE)</span><span class="sxs-lookup"><span data-stu-id="4d20a-182">You want to configure the HoloLens to skip the Out of Box Experience (OOBE)</span></span>
1. <span data-ttu-id="4d20a-183">У вас возникли проблемы при развертывании сертификата в сложной сети.</span><span class="sxs-lookup"><span data-stu-id="4d20a-183">You are having trouble deploying certificate in a complex network.</span></span> <span data-ttu-id="4d20a-184">Большая часть времени, когда вы можете развернуть сертификаты с помощью MDM (даже в сложных средах).</span><span class="sxs-lookup"><span data-stu-id="4d20a-184">The majority of the time you can deploy certificates using MDM (even in complex environments).</span></span> <span data-ttu-id="4d20a-185">Однако в некоторых сценариях для развертывания в пакете подготовки необходимы сертификаты.</span><span class="sxs-lookup"><span data-stu-id="4d20a-185">However, some scenarios require certificates to be deployed through the provisioning package.</span></span>

<span data-ttu-id="4d20a-186">Некоторые из конфигураций HoloLens, которые вы можете применить в пакете обеспечения:</span><span class="sxs-lookup"><span data-stu-id="4d20a-186">Some of the HoloLens configurations you can apply in a provisioning package:</span></span>

- <span data-ttu-id="4d20a-187">Применить сертификаты к устройству</span><span class="sxs-lookup"><span data-stu-id="4d20a-187">Apply certificates to the device</span></span>
- <span data-ttu-id="4d20a-188">Настройка подключения к сети Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="4d20a-188">Set up a Wi-Fi connection</span></span>
- <span data-ttu-id="4d20a-189">Предварительно настройте стандартные вопросы, такие как язык и языковой стандарт</span><span class="sxs-lookup"><span data-stu-id="4d20a-189">Pre-configure out of box questions like language and locale</span></span>
- <span data-ttu-id="4d20a-190">(HoloLens 2) массовая регистрация в управлении мобильными устройствами</span><span class="sxs-lookup"><span data-stu-id="4d20a-190">(HoloLens 2) bulk enroll in mobile device management</span></span>
- <span data-ttu-id="4d20a-191">(HoloLens v1) Применить ключ для включения Windows Holographic для бизнеса</span><span class="sxs-lookup"><span data-stu-id="4d20a-191">(HoloLens v1) Apply key to enable Windows Holographic for Business</span></span>

<span data-ttu-id="4d20a-192">Если вы решите использовать пакеты подготовки, следуйте указаниям, приведенным в [этом руководстве](hololens-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="4d20a-192">If you decide to use provisioning packages, follow [this guide](hololens-provisioning.md).</span></span>

## <span data-ttu-id="4d20a-193">Получить поддержку</span><span class="sxs-lookup"><span data-stu-id="4d20a-193">Get support</span></span>

<span data-ttu-id="4d20a-194">Получение поддержки на сайте службы поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="4d20a-194">Get support through the Microsoft support site.</span></span>

[<span data-ttu-id="4d20a-195">Файл с запросом поддержки</span><span class="sxs-lookup"><span data-stu-id="4d20a-195">File a support request</span></span>](https://support.microsoft.com/supportforbusiness/productselection?sapid=e9391227-fa6d-927b-0fff-f96288631b8f)
