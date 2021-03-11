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
ms.openlocfilehash: 44c79a41d7864cd6000ffed1bdd32dab8ffabc39
ms.sourcegitcommit: b437c738f101ac870a29bbdb7fd642eda3d67f00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "11406271"
---
# <a name="find-install-and-uninstall-applications-from-the-microsoft-store"></a><span data-ttu-id="9c368-105">Поиск, установка и удаление приложений из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="9c368-105">Find, install, and uninstall applications from the Microsoft Store</span></span>

<span data-ttu-id="9c368-106">Microsoft Store — это незаменимый источник приложений и игр, которые поддерживают HoloLens.</span><span class="sxs-lookup"><span data-stu-id="9c368-106">The Microsoft Store is your go-to source for apps and games that work with HoloLens.</span></span> <span data-ttu-id="9c368-107">При вашем переходе в Store с помощью вашего устройства HoloLens, на нем будут выполняться любые приложения, которые вы там видите.</span><span class="sxs-lookup"><span data-stu-id="9c368-107">When you go to the Store on your HoloLens, any apps you see there will run on it.</span></span>

<span data-ttu-id="9c368-108">В приложениях, работающих на HoloLens, используется либо двухмерное, либо голографическое представление.</span><span class="sxs-lookup"><span data-stu-id="9c368-108">Apps on HoloLens use either 2D view or holographic view.</span></span> <span data-ttu-id="9c368-109">Приложения, использующие двухмерное представление, выглядят так же, как Windows, и их можно расположить повсюду вокруг вас.</span><span class="sxs-lookup"><span data-stu-id="9c368-109">Apps that use 2D view look like windows and can be positioned all around you.</span></span> <span data-ttu-id="9c368-110">Приложения, использующие голографическое представление, окружают вас и становятся единственным приложением, которое вы видите.</span><span class="sxs-lookup"><span data-stu-id="9c368-110">Apps that use holographic view surround you and become the only app you see.</span></span>

<span data-ttu-id="9c368-111">HoloLens поддерживает многие существующие приложения из Microsoft Store и новые приложения, созданные специально для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="9c368-111">HoloLens supports many existing applications from the Microsoft Store, and new apps built specifically for HoloLens.</span></span>  <span data-ttu-id="9c368-112">Эта статья посвящена голографическим приложениям в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9c368-112">This article focuses on holographic applications from the Microsoft Store.</span></span>

<span data-ttu-id="9c368-113">Дополнительные сведения о том, как установить и запустить пользовательские приложения, читайте в статье [Пользовательские голографические приложения](holographic-custom-apps.md).</span><span class="sxs-lookup"><span data-stu-id="9c368-113">To learn more about installing and running custom apps, read [Custom holographic applications](holographic-custom-apps.md).</span></span>

## <a name="find-apps"></a><span data-ttu-id="9c368-114">Найти приложения</span><span class="sxs-lookup"><span data-stu-id="9c368-114">Find apps</span></span>

<span data-ttu-id="9c368-115">Откройте Microsoft Store в меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="9c368-115">Open the Microsoft Store from the **Start** menu.</span></span> <span data-ttu-id="9c368-116">Затем выполните поиск приложений и игр.</span><span class="sxs-lookup"><span data-stu-id="9c368-116">Then browse for apps and games.</span></span> <span data-ttu-id="9c368-117">Для поиска вы можете использовать [голосовые команды](hololens-cortana.md). Произнесите слово "Поиск", после появления окна поиска — фразу "Начать диктовку", а после соответствующего запроса начните произносить условия поиска.</span><span class="sxs-lookup"><span data-stu-id="9c368-117">You can use [voice commands](hololens-cortana.md) to search by saying "Search", once the search window opens say "Start dictating" and then when prompted begin saying your search terms.</span></span>

> [!NOTE]
> <span data-ttu-id="9c368-118">Требования к системе для устройств HoloLens основаны на архитектуре сборки приложения.</span><span class="sxs-lookup"><span data-stu-id="9c368-118">The System Requirements for HoloLens devices are based on the architecture of the app build.</span></span> <span data-ttu-id="9c368-119">Если сборка приложения для HoloLens (1-го поколения) не была обновлена до более новой версии UWP в магазине для включения пакета архитектуры ARM, она будет недоступна для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="9c368-119">If an app build for HoloLens (1st gen) has not been updated with to a newer UWP in the store to include the ARM architecture package, then it will not be available for HoloLens 2 devices.</span></span> <span data-ttu-id="9c368-120">Точно так же, если приложение HoloLens 2 не включает пакет архитектуры x86, оно будет недоступно для устройств HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="9c368-120">Likewise, if a HoloLens 2 app does not include the x86 architecture package, it will not be available for HoloLens (1st gen) devices.</span></span> <span data-ttu-id="9c368-121">Архитектуры устройств HoloLens:</span><span class="sxs-lookup"><span data-stu-id="9c368-121">HoloLens device architectures:</span></span>
> - <span data-ttu-id="9c368-122">x86 = HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="9c368-122">x86 = HoloLens (1st gen)</span></span>
> - <span data-ttu-id="9c368-123">ARM = HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="9c368-123">ARM = HoloLens 2</span></span>

> [!NOTE]
> <span data-ttu-id="9c368-124">12 января 2021 г. будет завершена поддержка следующих приложений на устройствах HoloLens.</span><span class="sxs-lookup"><span data-stu-id="9c368-124">On January 12, 2021 the following apps will reach End of Support on HoloLens devices.</span></span> <span data-ttu-id="9c368-125">Мы рекомендуем воспользоваться следующей ссылкой на своем устройстве, чтобы использовать веб-версию приложения.</span><span class="sxs-lookup"><span data-stu-id="9c368-125">We encourage you to use the following link on your device to use the web version of the app.</span></span>

| <span data-ttu-id="9c368-126">Приложение</span><span class="sxs-lookup"><span data-stu-id="9c368-126">App</span></span>        | <span data-ttu-id="9c368-127">Link</span><span class="sxs-lookup"><span data-stu-id="9c368-127">Link</span></span>                                          |
|------------|-----------------------------------------------|
| <span data-ttu-id="9c368-128">Excel Mobile;</span><span class="sxs-lookup"><span data-stu-id="9c368-128">Excel mobile</span></span>      | https://office.live.com/start/Excel.aspx      |
| <span data-ttu-id="9c368-129">Word Mobile;</span><span class="sxs-lookup"><span data-stu-id="9c368-129">Word mobile</span></span>       | https://office.live.com/start/Word.aspx       |
| <span data-ttu-id="9c368-130">PowerPoint Mobile;</span><span class="sxs-lookup"><span data-stu-id="9c368-130">PowerPoint mobile</span></span> | https://office.live.com/start/PowerPoint.aspx |

## <a name="install-apps"></a><span data-ttu-id="9c368-131">Установка приложений</span><span class="sxs-lookup"><span data-stu-id="9c368-131">Install apps</span></span>

<span data-ttu-id="9c368-132">Чтобы скачать приложения, необходимо войти в систему с помощью учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9c368-132">To download apps, you'll need to be signed in with a Microsoft account.</span></span> <span data-ttu-id="9c368-133">Некоторые приложения бесплатны, и их можно скачать сразу.</span><span class="sxs-lookup"><span data-stu-id="9c368-133">Some apps are free and can be downloaded right away.</span></span> <span data-ttu-id="9c368-134">Для приложений, требующих покупки, необходимо войти в Store с помощью учетной записи Майкрософт и применить действительный способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="9c368-134">For apps that require a purchase, you must be signed in to the Store with your Microsoft account and have a valid payment method.</span></span>
> [!NOTE]
> <span data-ttu-id="9c368-135">Учетная запись, используемая вами в Microsoft Store, может отличаться от учетной записи, с которой вы вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="9c368-135">The account you use on Microsoft Store does not have to be the same as the account you are signed in with.</span></span> <span data-ttu-id="9c368-136">Если вы используете рабочую или учебную учетную запись на устройстве HoloLens, вам может потребоваться войти в систему с помощью личной учетной записи в приложении Store, чтобы сделать покупку.</span><span class="sxs-lookup"><span data-stu-id="9c368-136">If you are using a Work or School account on your HoloLens then you may need to sign in with your personal account in the Store App to make a purchase.</span></span>

> [!TIP]
> <span data-ttu-id="9c368-137">Чтобы настроить способ оплаты, перейдите на [account.microsoft.com](https://account.microsoft.com/) и выберите **Платеж и выставление счетов** > **Параметры платежей** > **Добавить способ оплаты**.</span><span class="sxs-lookup"><span data-stu-id="9c368-137">To set up a payment method, go to [account.microsoft.com](https://account.microsoft.com/) and select **Payment & billing** > **Payment options** > **Add a payment option**.</span></span>

1. <span data-ttu-id="9c368-138">Чтобы открыть меню [**Пуск**](holographic-home.md), выполните [жест "Пуск"](https://docs.microsoft.com/hololens/hololens2-basic-usage#start-gesture) или жест [раскрытия ладони](hololens1-basic-usage.md) на HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="9c368-138">To open the [**Start** menu](holographic-home.md), perform a [Start gesture](https://docs.microsoft.com/hololens/hololens2-basic-usage#start-gesture) or [bloom](hololens1-basic-usage.md) gesture on HoloLens (1st gen).</span></span>
1. <span data-ttu-id="9c368-139">Выберите приложение Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9c368-139">Select the Microsoft Store app.</span></span> <span data-ttu-id="9c368-140">После открытия приложения Store:</span><span class="sxs-lookup"><span data-stu-id="9c368-140">After the Store app opens:</span></span>
   1. <span data-ttu-id="9c368-141">Используйте панели поиска, чтобы найти приложения.</span><span class="sxs-lookup"><span data-stu-id="9c368-141">Use the search bar to look for applications.</span></span> 
   1. <span data-ttu-id="9c368-142">Выберите основные приложения или приложения, предназначенные специально для HoloLens, в одной из специально подобранных категорий.</span><span class="sxs-lookup"><span data-stu-id="9c368-142">Select essential apps or apps made specifically for HoloLens from one of the curated categories.</span></span>
   1. <span data-ttu-id="9c368-143">В правом верхнем углу приложения Store нажмите кнопку **"..."**, а затем выберите **Моя библиотека** для просмотра любых ранее приобретенных приложений.</span><span class="sxs-lookup"><span data-stu-id="9c368-143">On the top right of the Store app, select the **"..."** button and then select **My Library** to view any previously purchased apps.</span></span>
1. <span data-ttu-id="9c368-144">На странице приложения (может потребоваться его покупка) выберите **Получить** или **Установить**.</span><span class="sxs-lookup"><span data-stu-id="9c368-144">Select **Get** or **Install** on the application's page (a purchase may be required).</span></span>

## <a name="update-apps"></a><span data-ttu-id="9c368-145">Обновление приложений</span><span class="sxs-lookup"><span data-stu-id="9c368-145">Update Apps</span></span>
<span data-ttu-id="9c368-146">Приложение, установленное из Microsoft Store, можно обновить из приложения Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9c368-146">To update an app you installed from the Microsoft Store, you can update the app from the Microsoft Store app.</span></span> <span data-ttu-id="9c368-147">Приложения, установленные из Microsoft Store для бизнеса, также можно обновить из Microsoft Store для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="9c368-147">For apps installed for the Microsoft Store for Business, you can also update those apps from the Microsoft Store for Business.</span></span> 
1. <span data-ttu-id="9c368-148">Чтобы открыть меню [**Пуск**](holographic-home.md), выполните [жест "Пуск"](https://docs.microsoft.com/hololens/hololens2-basic-usage#start-gesture) или жест [раскрытия ладони](hololens1-basic-usage.md) на HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="9c368-148">To open the [**Start** menu](holographic-home.md), perform a [Start gesture](https://docs.microsoft.com/hololens/hololens2-basic-usage#start-gesture) or [bloom](hololens1-basic-usage.md) gesture on HoloLens (1st gen).</span></span>
1. <span data-ttu-id="9c368-149">Выберите приложение Store.</span><span class="sxs-lookup"><span data-stu-id="9c368-149">Select the Store app.</span></span>
1. <span data-ttu-id="9c368-150">Взгляните в правый верхний угол приложения Store.</span><span class="sxs-lookup"><span data-stu-id="9c368-150">Look to the top right of the Store app.</span></span> 
1. <span data-ttu-id="9c368-151">Нажмите кнопку **"..."** или "Дополнительно".</span><span class="sxs-lookup"><span data-stu-id="9c368-151">Select the **"..."** or “See more” button.</span></span>

   > [!div class="mx-imgBorder"]
   > ![Снимок экрана: приложение Microsoft Store.](images/store-update-1.png)

1. <span data-ttu-id="9c368-153">Выберите **Загрузки и обновления**.</span><span class="sxs-lookup"><span data-stu-id="9c368-153">Select **Downloads and updates**.</span></span>
    1. <span data-ttu-id="9c368-154">Если ваше устройство уже обнаружило обновления, может отобразиться стрелка вниз и число, соответствующее ожидающим обновлениям.</span><span class="sxs-lookup"><span data-stu-id="9c368-154">If your device has previously identified updates, there may be a down arrow and a number that represents pending updates.</span></span>
1. <span data-ttu-id="9c368-155">Нажмите **Получить обновления**.</span><span class="sxs-lookup"><span data-stu-id="9c368-155">Select **Get updates**.</span></span> <span data-ttu-id="9c368-156">Ваше устройство начнет поиск обновлений и их подготовку для скачивания и установки.</span><span class="sxs-lookup"><span data-stu-id="9c368-156">Your device will now search for updates and set them to download and install.</span></span> 
 
   > [!div class="mx-imgBorder"]
   > ![Снимок экрана: получение обновлений в приложении Microsoft Store.](images/store-update-2.png.jpg)

> [!NOTE]
> <span data-ttu-id="9c368-158">Если приложения на вашем устройстве распространяются вашей организацией, они могут быть обновлены этими же методами управления коммерческими приложениями.</span><span class="sxs-lookup"><span data-stu-id="9c368-158">If the apps on your device were distrubted by your organization they can be updated through the same commercial app management methods.</span></span> <span data-ttu-id="9c368-159">Если это применимо для вашей ситуации, ознакомьтесь с дополнительными сведениями в нашем [обзоре развертывания коммерческого приложения](app-deploy-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9c368-159">If this applies to your situation, read more via our [overview of commercial app deployment.](app-deploy-overview.md)</span></span>
>
> <span data-ttu-id="9c368-160">Если вы хотите обновить пользовательское приложение (неопубликованное или развернутое), вам потребуется использовать этот же метод для обновленной версии приложения.</span><span class="sxs-lookup"><span data-stu-id="9c368-160">If you would like to update a custom app that has been sideloaded or deployed, you will need to use the same method with the updated version of your app.</span></span> <span data-ttu-id="9c368-161">Дополнительные сведения о том, как установить и запустить пользовательские приложения, см. в статье [Пользовательские голографические приложения](holographic-custom-apps.md).</span><span class="sxs-lookup"><span data-stu-id="9c368-161">To learn more about installing and running custom apps, read [custom holographic applications](holographic-custom-apps.md).</span></span>

## <a name="uninstall-apps"></a><span data-ttu-id="9c368-162">Удаление приложений</span><span class="sxs-lookup"><span data-stu-id="9c368-162">Uninstall apps</span></span>

<span data-ttu-id="9c368-163">Удалить приложения можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="9c368-163">There are two ways to uninstall applications.</span></span>  <span data-ttu-id="9c368-164">Удалить приложения можно в Microsoft Store или в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="9c368-164">You can uninstall applications through the Microsoft Store or Start menu.</span></span>

### <a name="uninstall-from-the-start-menu"></a><span data-ttu-id="9c368-165">Удаление из меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="9c368-165">Uninstall from the Start menu</span></span>

<span data-ttu-id="9c368-166">В меню **Пуск** или в списке **Все приложения** выберите приложение.</span><span class="sxs-lookup"><span data-stu-id="9c368-166">On the **Start** menu or in the **All apps** list, browse to the app.</span></span> <span data-ttu-id="9c368-167">Нажмите и удерживайте его до тех пор, пока не появится меню, а затем выберите пункт **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="9c368-167">Select and hold until the menu appears, then select **Uninstall**.</span></span>

### <a name="uninstall-from-the-microsoft-store"></a><span data-ttu-id="9c368-168">Удаление из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="9c368-168">Uninstall from the Microsoft Store</span></span>

<span data-ttu-id="9c368-169">Откройте Microsoft Store из меню **Пуск** и перейдите к приложению, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9c368-169">Open the Microsoft Store from the **Start** menu, and then browse for the application you want to uninstall.</span></span>  <span data-ttu-id="9c368-170">На странице Store для каждого установленного приложения присутствует кнопка **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="9c368-170">On the Store page, each installed application has an **Uninstall** button.</span></span>
