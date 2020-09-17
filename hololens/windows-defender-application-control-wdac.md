---
title: Элемент управления приложением "Защитник Windows" — WDAC
description: Общие сведения о том, что такое WDAC и как использовать для управления устройствами HoloLens.
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: v-evmill
ms.topic: article
ms.localizationpriority: medium
ms.date: 09/16/2020
ms.reviewer: ''
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: d1147b202d3b575fa1f2dd20f620005c786ea9fc
ms.sourcegitcommit: 785ac6f05aecffc0f3980960891617d161711a70
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/17/2020
ms.locfileid: "11016802"
---
# <span data-ttu-id="333c9-103">Элемент управления приложением "Защитник Windows" — WDAC</span><span class="sxs-lookup"><span data-stu-id="333c9-103">Windows Defender Application Control - WDAC</span></span>

<span data-ttu-id="333c9-104">WDAC позволяет ИТ – администратору настроить устройства таким образом, чтобы блокировать запуск приложений на устройствах.</span><span class="sxs-lookup"><span data-stu-id="333c9-104">WDAC allows an IT Admin to configure their devices to block the launch of apps on devices.</span></span> <span data-ttu-id="333c9-105">Это отличается от методов ограничения устройств, таких как режим киоска, в котором пользователь представляется в пользовательском интерфейсе, который скрывает приложения на устройстве, но и все еще может запускаться.</span><span class="sxs-lookup"><span data-stu-id="333c9-105">This is different than methods of device restriction such as Kiosk mode, where  the user is presented with a UI that hides the apps on the device but they can still be launched.</span></span> <span data-ttu-id="333c9-106">Несмотря на то, что она реализована, приложения по-прежнему отображаются в списке "все приложения", но WDAC останавливает эти приложения и процессы от возможности его запуска пользователем.</span><span class="sxs-lookup"><span data-stu-id="333c9-106">While WDAC is implemented, the apps are still visible in the All Apps list but WDAC stops those apps and processes from being able to be launched by the device user.</span></span>

> [!NOTE]
> <span data-ttu-id="333c9-107">Когда конечные пользователи пытаются запустить приложение, которое заблокировано компанией WDAC, на HoloLens они не получат уведомление о том, что невозможно запустить это приложение.</span><span class="sxs-lookup"><span data-stu-id="333c9-107">When end users attempt to launch an app that is blocked by WDAC, on HoloLens they will not receive a notification about not being able to launch that app.</span></span>

<span data-ttu-id="333c9-108">Ниже приведено руководство, в котором описаны способы [использования WDAC и Windows PowerShell для разрешения и блокировки приложений на устройствах HoloLens 2 с помощью Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens).</span><span class="sxs-lookup"><span data-stu-id="333c9-108">The following is a guide for users to learn how to [use WDAC and Windows PowerShell to allow or block apps on HoloLens 2 devices with Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens).</span></span>

<span data-ttu-id="333c9-109">При поиске приложений, установленных на компьютере с Windows 10 с помощью первого этапа, вам может потребоваться выполнить несколько попыток сузить результаты.</span><span class="sxs-lookup"><span data-stu-id="333c9-109">When users search for apps installed on their Windows 10 PC using the first example step they may need to make a few attempts to narrow down the results.</span></span>

```powershell
$package1 = Get-AppxPackage -name *<applicationname>*
``` 

<span data-ttu-id="333c9-110">Если вы не знаете полное имя пакета, возможно, потребуется выполнить "Get-AppxPackage-Name \ \* YourBestGuess \ \*" несколько раз, чтобы найти его.</span><span class="sxs-lookup"><span data-stu-id="333c9-110">If you don’t know the full name of the package, you may need to run ‘Get-AppxPackage -name \*YourBestGuess\*’ a few times to find it.</span></span> <span data-ttu-id="333c9-111">После того как вы запустили имя "$package 1 = Get-AppxPackage-Name Actual. PackageName"</span><span class="sxs-lookup"><span data-stu-id="333c9-111">Then once you have the name run ‘$package1 = Get-AppxPackage -name Actual.PackageName‘</span></span>

<span data-ttu-id="333c9-112">Например, при выполнении следующего для Edge будет возвращено больше одного результата, но из этого списка вы можете указать, что полное имя должно быть для Microsoft. MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="333c9-112">For example running the following for Edge will return more than one result, but from that list you can identify that the full name you need is Microsoft.MicrosoftEdge.</span></span> 

```powershell
Get-AppxPackage -name *edge*
``` 

## <span data-ttu-id="333c9-113">Имена семейств пакетов для приложений на HoloLens</span><span class="sxs-lookup"><span data-stu-id="333c9-113">Package Family Names for apps on HoloLens</span></span>

<span data-ttu-id="333c9-114">В руководстве, описанном выше, вы можете вручную изменить newPolicy.xml и добавить правила для приложений, которые установлены только на HoloLens с их именами семейства пакетов.</span><span class="sxs-lookup"><span data-stu-id="333c9-114">In the guide linked above, you can manually edit newPolicy.xml and add rules for applications which are only installed on HoloLens with their package family names.</span></span> <span data-ttu-id="333c9-115">Иногда есть приложения, которые вы можете использовать, а не на настольном компьютере, который вы хотите добавить к политике.</span><span class="sxs-lookup"><span data-stu-id="333c9-115">Sometimes there are apps you may use to use that are not on your desktop PC that you wish to add to policy.</span></span> 

<span data-ttu-id="333c9-116">Ниже приведен список часто используемых и поблочных приложений для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="333c9-116">Here is a list of commonly used and In-Box apps for HoloLens 2 devices.</span></span>

| <span data-ttu-id="333c9-117">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="333c9-117">App Name</span></span>                   | <span data-ttu-id="333c9-118">Имя семейства пакетов</span><span class="sxs-lookup"><span data-stu-id="333c9-118">Package Family Name</span></span>                                |
|----------------------------|----------------------------------------------------|
| <span data-ttu-id="333c9-119">Средство 3D-просмотра</span><span class="sxs-lookup"><span data-stu-id="333c9-119">3D Viewer</span></span>                  | <span data-ttu-id="333c9-120">Microsoft. Microsoft3DViewer_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-120">Microsoft.Microsoft3DViewer_8wekyb3d8bbwe</span></span>          |
| <span data-ttu-id="333c9-121">Календарь</span><span class="sxs-lookup"><span data-stu-id="333c9-121">Calendar</span></span>                   | <span data-ttu-id="333c9-122">Microsoft. windowscommunicationsapps_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-122">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span></span>  |
| <span data-ttu-id="333c9-123">Камера</span><span class="sxs-lookup"><span data-stu-id="333c9-123">Camera</span></span>                     | <span data-ttu-id="333c9-124">HoloCamera_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="333c9-124">HoloCamera_cw5n1h2txyewy</span></span>                           |
| <span data-ttu-id="333c9-125">Кортана</span><span class="sxs-lookup"><span data-stu-id="333c9-125">Cortana</span></span>                    | <span data-ttu-id="333c9-126">Microsoft. 549981C3F5F10_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-126">Microsoft.549981C3F5F10_8wekyb3d8bbwe</span></span>              |
| <span data-ttu-id="333c9-127">Руководства по Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="333c9-127">Dynamics 365 Guides</span></span>        | <span data-ttu-id="333c9-128">Microsoft. Dynamics365. Guides_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-128">Microsoft.Dynamics365.Guides_8wekyb3d8bbwe</span></span>         |
| <span data-ttu-id="333c9-129">Dynamics 365 Remote Assist</span><span class="sxs-lookup"><span data-stu-id="333c9-129">Dynamics 365 Remote Assist</span></span> | <span data-ttu-id="333c9-130">Microsoft. MicrosoftRemoteAssist_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-130">Microsoft.MicrosoftRemoteAssist_8wekyb3d8bbwe</span></span>      |
| <span data-ttu-id="333c9-131">Центр отзывов</span><span class="sxs-lookup"><span data-stu-id="333c9-131">Feedback Hub</span></span>               | <span data-ttu-id="333c9-132">Microsoft. WindowsFeedbackHub_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-132">Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe</span></span>         |
| <span data-ttu-id="333c9-133">Проводник</span><span class="sxs-lookup"><span data-stu-id="333c9-133">File Explorer</span></span>              | <span data-ttu-id="333c9-134">c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="333c9-134">c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy</span></span> |
| <span data-ttu-id="333c9-135">Mail</span><span class="sxs-lookup"><span data-stu-id="333c9-135">Mail</span></span>                       | <span data-ttu-id="333c9-136">Microsoft. windowscommunicationsapps_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-136">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span></span>  |
| <span data-ttu-id="333c9-137">Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="333c9-137">Microsoft Store</span></span>            | <span data-ttu-id="333c9-138">Microsoft. WindowsStore_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-138">Microsoft.WindowsStore_8wekyb3d8bbwe</span></span>               |
| <span data-ttu-id="333c9-139">Кино и ТВ</span><span class="sxs-lookup"><span data-stu-id="333c9-139">Movies & TV</span></span>                | <span data-ttu-id="333c9-140">Microsoft. ZuneVideo_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-140">Microsoft.ZuneVideo_8wekyb3d8bbwe</span></span>                  |
| <span data-ttu-id="333c9-141">OneDrive</span><span class="sxs-lookup"><span data-stu-id="333c9-141">OneDrive</span></span>                   | <span data-ttu-id="333c9-142">Microsoft. microsoftskydrive_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-142">microsoft.microsoftskydrive_8wekyb3d8bbwe</span></span>          |
| <span data-ttu-id="333c9-143">Фотографии</span><span class="sxs-lookup"><span data-stu-id="333c9-143">Photos</span></span>                     | <span data-ttu-id="333c9-144">Microsoft. Windows. Photos_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-144">Microsoft.Windows.Photos_8wekyb3d8bbwe</span></span>             |
| <span data-ttu-id="333c9-145">Параметры</span><span class="sxs-lookup"><span data-stu-id="333c9-145">Settings</span></span>                   | <span data-ttu-id="333c9-146">HolographicSystemSettings_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="333c9-146">HolographicSystemSettings_cw5n1h2txyewy</span></span>            |
| <span data-ttu-id="333c9-147">Советы</span><span class="sxs-lookup"><span data-stu-id="333c9-147">Tips</span></span>                       | <span data-ttu-id="333c9-148">Microsoft. HoloLensTips_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="333c9-148">Microsoft.HoloLensTips_8wekyb3d8bbwe</span></span>               |

<span data-ttu-id="333c9-149">Если приложение не включено в этот список, пользователь может использовать портал устройств, подключенный к HoloLens 2, на котором установлено приложение, которое нужно заблокировать, чтобы определить PackageRelativeID и от него получится PackageFamilyName.</span><span class="sxs-lookup"><span data-stu-id="333c9-149">If an app is not on this list then a user may use Device Portal, connected to a HoloLens 2 that has installed the app wished to be blocked, to determine the PackageRelativeID and from there get the PackageFamilyName.</span></span>

1. <span data-ttu-id="333c9-150">Установите приложение на устройстве HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="333c9-150">Install the app on your HoloLens 2 device.</span></span> 
1. <span data-ttu-id="333c9-151">Открыть параметры: > обновления & оптимального — > для разработчиков и включить **режим разработчика** , а затем **портал устройств**.</span><span class="sxs-lookup"><span data-stu-id="333c9-151">Open Settings -> Updates & Securtiy -> For developers, and enable **Developer mode** and then **Device portal**.</span></span> 
    1. <span data-ttu-id="333c9-152">Дополнительные сведения о [настройке и использовании на портале устройств](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).</span><span class="sxs-lookup"><span data-stu-id="333c9-152">More more details instructions read more about [setup and use of device portal here](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).</span></span>
1. <span data-ttu-id="333c9-153">После подключения к порталу устройств перейдите в раздел " **представления** " и выберите пункт " **приложения**".</span><span class="sxs-lookup"><span data-stu-id="333c9-153">Once Device Portal is connected, navigate to **Views** then **Apps**.</span></span> 
1. <span data-ttu-id="333c9-154">На панели установленные приложения выберите установленное приложение с помощью раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="333c9-154">Within the Installed Apps panel use the dropdown to select the installed app.</span></span> 
1. <span data-ttu-id="333c9-155">Найдите PackageRelativeID.</span><span class="sxs-lookup"><span data-stu-id="333c9-155">Locate the PackageRelativeID.</span></span> 
1. <span data-ttu-id="333c9-156">Скопируйте символы приложения перед знаком! это будет ваша PackageFamilyName.</span><span class="sxs-lookup"><span data-stu-id="333c9-156">Copy app characters before the !, this will be your PackageFamilyName.</span></span>

