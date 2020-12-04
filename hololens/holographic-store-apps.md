---
title: Поиск, установка и удаление приложений
description: Microsoft Store — это источник приложений и игр, которые поддерживают HoloLens.  Узнайте больше о поиске, установке и удалении голографических приложений.
ms.assetid: cbe9aa3a-884f-4a92-bf54-8d4917bc3435
ms.reviewer: v-miegge
ms.date: 10/27/2020
manager: jarrettr
keywords: hololens, store, uwp, приложение, установка
ms.prod: hololens
ms.sitesec: library
author: mattzmsft
ms.author: mazeller
ms.topic: article
ms.localizationpriority: high
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 06768203459827a83d8b6e891dfc8c46e33c3da2
ms.sourcegitcommit: 1f37a06cde037f3acdc4ef3767a9384953d97c33
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2020
ms.locfileid: "11194869"
---
# <span data-ttu-id="10ca6-105">Поиск, установка и удаление приложений из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="10ca6-105">Find, install, and uninstall applications from the Microsoft Store</span></span>

<span data-ttu-id="10ca6-106">Microsoft Store — это незаменимый источник приложений и игр, которые поддерживают HoloLens.</span><span class="sxs-lookup"><span data-stu-id="10ca6-106">The Microsoft Store is your go-to source for apps and games that work with HoloLens.</span></span> <span data-ttu-id="10ca6-107">При вашем переходе в Store с помощью вашего устройства HoloLens, на нем будут выполняться любые приложения, которые вы там видите.</span><span class="sxs-lookup"><span data-stu-id="10ca6-107">When you go to the Store on your HoloLens, any apps you see there will run on it.</span></span>

<span data-ttu-id="10ca6-108">В приложениях, работающих на HoloLens, используется либо двухмерное, либо голографическое представление.</span><span class="sxs-lookup"><span data-stu-id="10ca6-108">Apps on HoloLens use either 2D view or holographic view.</span></span> <span data-ttu-id="10ca6-109">Приложения, использующие двухмерное представление, выглядят так же, как Windows, и их можно расположить повсюду вокруг вас.</span><span class="sxs-lookup"><span data-stu-id="10ca6-109">Apps that use 2D view look like windows and can be positioned all around you.</span></span> <span data-ttu-id="10ca6-110">Приложения, использующие голографическое представление, окружают вас и становятся единственным приложением, которое вы видите.</span><span class="sxs-lookup"><span data-stu-id="10ca6-110">Apps that use holographic view surround you and become the only app you see.</span></span>

<span data-ttu-id="10ca6-111">Устройство HoloLens поддерживает множество существующих приложений в Microsoft Store, а также новые приложения, разработанные специально для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="10ca6-111">HoloLens supports many existing applications from the Microsoft Store, as well as new apps built specifically for HoloLens.</span></span>  <span data-ttu-id="10ca6-112">Эта статья посвящена голографическим приложениям в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="10ca6-112">This article focuses on holographic applications from the Microsoft Store.</span></span>

<span data-ttu-id="10ca6-113">Дополнительные сведения о том, как установить и запустить пользовательские приложения, читайте в статье [Пользовательские голографические приложения](holographic-custom-apps.md).</span><span class="sxs-lookup"><span data-stu-id="10ca6-113">To learn more about installing and running custom apps, read [Custom holographic applications](holographic-custom-apps.md).</span></span>

## <span data-ttu-id="10ca6-114">Найти приложения</span><span class="sxs-lookup"><span data-stu-id="10ca6-114">Find apps</span></span>

<span data-ttu-id="10ca6-115">Откройте Microsoft Store в меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="10ca6-115">Open the Microsoft Store from the **Start** menu.</span></span> <span data-ttu-id="10ca6-116">Затем выполните поиск приложений и игр.</span><span class="sxs-lookup"><span data-stu-id="10ca6-116">Then browse for apps and games.</span></span> <span data-ttu-id="10ca6-117">Для поиска вы можете использовать [голосовые команды](hololens-cortana.md). Произнесите слово "Поиск", после появления окна поиска — фразу "Начать диктовку", а после соответствующего запроса начните произносить условия поиска.</span><span class="sxs-lookup"><span data-stu-id="10ca6-117">You can use [voice commands](hololens-cortana.md) to search by saying "Search", once the search window opens say "Start dictating" and then when prompted begin saying your search terms.</span></span>

> [!NOTE]
> <span data-ttu-id="10ca6-118">Требования к системе для устройств HoloLens основаны на архитектуре сборки приложения.</span><span class="sxs-lookup"><span data-stu-id="10ca6-118">The System Requirements for HoloLens devices are based on the architecture of the app build.</span></span> <span data-ttu-id="10ca6-119">Если сборка приложения для HoloLens (1-го поколения) не была обновлена до более новой версии UWP в магазине для включения пакета архитектуры ARM, она будет недоступна для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="10ca6-119">If an app build for HoloLens (1st gen) has not been updated with to a newer UWP in the store to include the ARM architecture package, then it will not be available for HoloLens 2 devices.</span></span> <span data-ttu-id="10ca6-120">Точно так же, если приложение HoloLens 2 не включает пакет архитектуры x86, оно будет недоступно для устройств HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="10ca6-120">Likewise, if a HoloLens 2 app does not include the x86 architecture package, it will not be available for HoloLens (1st gen) devices.</span></span> <span data-ttu-id="10ca6-121">Архитектуры устройств HoloLens:</span><span class="sxs-lookup"><span data-stu-id="10ca6-121">HoloLens device architectures:</span></span>
> - <span data-ttu-id="10ca6-122">x86 = HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="10ca6-122">x86 = HoloLens (1st gen)</span></span>
> - <span data-ttu-id="10ca6-123">ARM = HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="10ca6-123">ARM = HoloLens 2</span></span>

> [!NOTE]
> <span data-ttu-id="10ca6-124">12 января 2021 г. будет завершена поддержка следующих приложений на устройствах HoloLens.</span><span class="sxs-lookup"><span data-stu-id="10ca6-124">On January 12, 2021 the following apps will reach End of Support on HoloLens devices.</span></span> <span data-ttu-id="10ca6-125">Мы рекомендуем воспользоваться следующей ссылкой на своем устройстве, чтобы использовать веб-версию приложения.</span><span class="sxs-lookup"><span data-stu-id="10ca6-125">We encourage you to use the following link on your device to use the web version of the app.</span></span>

| <span data-ttu-id="10ca6-126">Приложение</span><span class="sxs-lookup"><span data-stu-id="10ca6-126">App</span></span>        | <span data-ttu-id="10ca6-127">Link</span><span class="sxs-lookup"><span data-stu-id="10ca6-127">Link</span></span>                                          |
|------------|-----------------------------------------------|
| <span data-ttu-id="10ca6-128">Excel Mobile;</span><span class="sxs-lookup"><span data-stu-id="10ca6-128">Excel mobile</span></span>      | https://office.live.com/start/Excel.aspx      |
| <span data-ttu-id="10ca6-129">Word Mobile;</span><span class="sxs-lookup"><span data-stu-id="10ca6-129">Word mobile</span></span>       | https://office.live.com/start/Word.aspx       |
| <span data-ttu-id="10ca6-130">PowerPoint Mobile;</span><span class="sxs-lookup"><span data-stu-id="10ca6-130">PowerPoint mobile</span></span> | https://office.live.com/start/PowerPoint.aspx |

## <span data-ttu-id="10ca6-131">Установка приложений</span><span class="sxs-lookup"><span data-stu-id="10ca6-131">Install apps</span></span>

<span data-ttu-id="10ca6-132">Чтобы скачать приложения, необходимо войти в систему с помощью учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="10ca6-132">To download apps, you'll need to be signed in with a Microsoft account.</span></span> <span data-ttu-id="10ca6-133">Некоторые приложения бесплатны, и их можно скачать сразу.</span><span class="sxs-lookup"><span data-stu-id="10ca6-133">Some apps are free and can be downloaded right away.</span></span> <span data-ttu-id="10ca6-134">Для приложений, требующих покупки, необходимо войти в Store с помощью учетной записи Майкрософт и применить действительный способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="10ca6-134">Apps that require a purchase require you to be signed in to the Store with your Microsoft account and have a valid payment method.</span></span>
> [!NOTE]
> <span data-ttu-id="10ca6-135">Учетная запись, используемая вами в Microsoft Store, не должна совпадать с учетной записью, с которой вы вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="10ca6-135">The account you use on Microsoft Store does not have to be the same as the account you are signed in with.</span></span> <span data-ttu-id="10ca6-136">Если вы используете рабочую или учебную учетную запись на устройстве HoloLens, вам может потребоваться войти в систему с помощью личной учетной записи в приложении Store, чтобы сделать покупку.</span><span class="sxs-lookup"><span data-stu-id="10ca6-136">If you are using a Work or School account on your HoloLens then you may need to sign in with your personal account in the Store App to make a purchase.</span></span>

<span data-ttu-id="10ca6-137">Чтобы настроить способ оплаты, перейдите на [account.microsoft.com](https://account.microsoft.com/) и выберите **Платеж и выставление счетов** > **Параметры платежей** > **Добавить способ оплаты**.</span><span class="sxs-lookup"><span data-stu-id="10ca6-137">To set up a payment method, go to [account.microsoft.com](https://account.microsoft.com/) and select **Payment & billing** > **Payment options** > **Add a payment option**.</span></span>

1. <span data-ttu-id="10ca6-138">Чтобы открыть меню [**Пуск**](holographic-home.md), выполните [Жест “Пуск”](https://docs.microsoft.com/hololens/hololens2-basic-usage#start-gesture) или жест [раскрытия ладони](hololens1-basic-usage.md) на HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="10ca6-138">To open the [**Start** menu](holographic-home.md), perform a [Start gesture](https://docs.microsoft.com/hololens/hololens2-basic-usage#start-gesture) or [bloom](hololens1-basic-usage.md) gesture on HoloLens (1st gen).</span></span>
1. <span data-ttu-id="10ca6-139">Выберите приложение Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="10ca6-139">Select the Microsoft Store app.</span></span> <span data-ttu-id="10ca6-140">После того как откроется приложение Store:</span><span class="sxs-lookup"><span data-stu-id="10ca6-140">Once the Store app opens:</span></span>
   1. <span data-ttu-id="10ca6-141">Используйте панель поиска для поиска любых нужных приложений.</span><span class="sxs-lookup"><span data-stu-id="10ca6-141">Use the search bar to look for any desired applications.</span></span> 
   1. <span data-ttu-id="10ca6-142">Выберите основные приложения или приложения, предназначенные специально для HoloLens, в одной из специально подобранных категорий.</span><span class="sxs-lookup"><span data-stu-id="10ca6-142">Select essential apps or apps made specifically for HoloLens from one of the curated categories.</span></span>
   1. <span data-ttu-id="10ca6-143">В правом верхнем углу приложения Store нажмите кнопку **"..."**, а затем выберите **Моя библиотека** для просмотра любых ранее приобретенных приложений.</span><span class="sxs-lookup"><span data-stu-id="10ca6-143">On the top right of the Store app, select the **"..."** button and then select **My Library** to view any previously purchased apps.</span></span>
1. <span data-ttu-id="10ca6-144">На странице приложения (может потребоваться его покупка) выберите **Получить** или **Установить**.</span><span class="sxs-lookup"><span data-stu-id="10ca6-144">Select **Get** or **Install** on the application's page (a purchase may be required).</span></span>

## <span data-ttu-id="10ca6-145">Обновление приложений</span><span class="sxs-lookup"><span data-stu-id="10ca6-145">Update Apps</span></span>
<span data-ttu-id="10ca6-146">Приложение, установленное из приложения Microsoft Store, можно обновить из этого же приложения Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="10ca6-146">To update an app you have installed from the Microsoft Store app you can also update the same app from the Microsoft Store app.</span></span> <span data-ttu-id="10ca6-147">Это также применимо к приложениям, установленным из Microsoft Store для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="10ca6-147">This also applies to apps installed for Microsoft Store for Business.</span></span> 
1. <span data-ttu-id="10ca6-148">Чтобы открыть меню [**Пуск**](holographic-home.md), выполните [Жест “Пуск”](https://docs.microsoft.com/hololens/hololens2-basic-usage#start-gesture) или жест [раскрытия ладони](hololens1-basic-usage.md) на HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="10ca6-148">To open the [**Start** menu](holographic-home.md), perform a [Start gesture](https://docs.microsoft.com/hololens/hololens2-basic-usage#start-gesture) or [bloom](hololens1-basic-usage.md) gesture on HoloLens (1st gen).</span></span>
1. <span data-ttu-id="10ca6-149">Выберите приложение Store.</span><span class="sxs-lookup"><span data-stu-id="10ca6-149">Select the Store app.</span></span>
1. <span data-ttu-id="10ca6-150">Взгляните в правый верхний угол приложения Store.</span><span class="sxs-lookup"><span data-stu-id="10ca6-150">Look to the top right of the Store app.</span></span> 
1. <span data-ttu-id="10ca6-151">Нажмите кнопку **"..."** или "Дополнительно".</span><span class="sxs-lookup"><span data-stu-id="10ca6-151">Select the **"..."** or “See more” button.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана: приложение Microsoft Store.](images/store-update-1.png)

1. <span data-ttu-id="10ca6-153">Выберите **Загрузки и обновления**.</span><span class="sxs-lookup"><span data-stu-id="10ca6-153">Select **Downloads and updates**.</span></span>
    1. <span data-ttu-id="10ca6-154">Если ваше устройство уже обнаружило обновления, может отобразиться стрелка вниз и число, соответствующее ожидающим обновлениям.</span><span class="sxs-lookup"><span data-stu-id="10ca6-154">If your device has previously identified updates you may see a down arrow and a number, this represents pending updates.</span></span>
1. <span data-ttu-id="10ca6-155">Нажмите **Получить обновления**.</span><span class="sxs-lookup"><span data-stu-id="10ca6-155">Select **Get updates**.</span></span> <span data-ttu-id="10ca6-156">Ваше устройство начнет поиск обновлений и их подготовку для скачивания и установки.</span><span class="sxs-lookup"><span data-stu-id="10ca6-156">Your device will now search for updates and set them to download and install.</span></span> 
 
   > [!div class="mx-imgBorder"]
   > ![Снимок экрана: получение обновлений в приложении Microsoft Store.](images/store-update-2.png.jpg)

> [!NOTE]
> <span data-ttu-id="10ca6-158">Если приложения на вашем устройстве распространяются вашей организацией, они могут быть обновлены этими же методами управления коммерческими приложениями.</span><span class="sxs-lookup"><span data-stu-id="10ca6-158">If the apps on your device were distrubted by your organization they can be updated through the same commercial app management methods.</span></span> <span data-ttu-id="10ca6-159">Если это применимо для вашей ситуации, ознакомьтесь с дополнительными сведениями в нашем [обзоре развертывания коммерческого приложения](app-deploy-overview.md).</span><span class="sxs-lookup"><span data-stu-id="10ca6-159">If this applies to your situation, read more via our [overview of commercial app deployment.](app-deploy-overview.md)</span></span>
>
> <span data-ttu-id="10ca6-160">Если вы хотите обновить пользовательское приложение (неопубликованное или развернутое), вам потребуется использовать этот же метод для обновленной версии приложения.</span><span class="sxs-lookup"><span data-stu-id="10ca6-160">If you would like to update a custom app that has been sideloaded or deployed, you will need to use the same method with the updated version of your app.</span></span> <span data-ttu-id="10ca6-161">Дополнительные сведения о том, как установить и запустить пользовательские приложения, см. в статье [Пользовательские голографические приложения](holographic-custom-apps.md).</span><span class="sxs-lookup"><span data-stu-id="10ca6-161">To learn more about installing and running custom apps, read [custom holographic applications](holographic-custom-apps.md).</span></span>

## <span data-ttu-id="10ca6-162">Удаление приложений</span><span class="sxs-lookup"><span data-stu-id="10ca6-162">Uninstall apps</span></span>

<span data-ttu-id="10ca6-163">Удалить приложения можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="10ca6-163">There are two ways to uninstall applications.</span></span>  <span data-ttu-id="10ca6-164">Удалить приложения можно в Microsoft Store или в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="10ca6-164">You can uninstall applications through the Microsoft Store or Start menu.</span></span>

### <span data-ttu-id="10ca6-165">Удаление из меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="10ca6-165">Uninstall from the Start menu</span></span>

<span data-ttu-id="10ca6-166">В меню **Пуск** или в списке **Все приложения** выберите приложение.</span><span class="sxs-lookup"><span data-stu-id="10ca6-166">On the **Start** menu or in the **All apps** list, browse to the app.</span></span> <span data-ttu-id="10ca6-167">Нажмите и удерживайте его до тех пор, пока не появится меню, а затем выберите пункт **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="10ca6-167">Select and hold until the menu appears, then select **Uninstall**.</span></span>

### <span data-ttu-id="10ca6-168">Удалить из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="10ca6-168">Uninstall from the Microsoft Store</span></span>

<span data-ttu-id="10ca6-169">Откройте Microsoft Store из меню **Пуск**, а затем найдите приложение, которое вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="10ca6-169">Open the Microsoft Store from the **Start** menu, and then browse for the application you'd like to uninstall.</span></span>  <span data-ttu-id="10ca6-170">На странице Store для каждого установленного приложения присутствует кнопка **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="10ca6-170">On the Store page, each application that you have installed has an **Uninstall** button.</span></span>
