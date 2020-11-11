---
title: Управление приложениями в Защитнике Windows — WDAC
description: Общие сведения о том, что такое WDAC и как использовать для управления устройствами HoloLens.
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: v-evmill
ms.topic: article
ms.localizationpriority: medium
ms.date: 10/26/2020
ms.reviewer: ''
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: b12079142049cce28ec00803ad0a1f8dc92333e1
ms.sourcegitcommit: 108b818130e2627bf08107f4e47ae159dd6ab1d2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "11163124"
---
# <span data-ttu-id="b2aac-103">Управление приложениями в Защитнике Windows — WDAC</span><span class="sxs-lookup"><span data-stu-id="b2aac-103">Windows Defender Application Control - WDAC</span></span>

<span data-ttu-id="b2aac-104">WDAC позволяет ИТ – администратору настроить устройства таким образом, чтобы блокировать запуск приложений на устройствах.</span><span class="sxs-lookup"><span data-stu-id="b2aac-104">WDAC allows an IT Admin to configure their devices to block the launch of apps on devices.</span></span> <span data-ttu-id="b2aac-105">Это отличается от методов ограничения устройств, таких как режим киоска, в котором пользователь представляется в пользовательском интерфейсе, который скрывает приложения на устройстве, но и все еще может запускаться.</span><span class="sxs-lookup"><span data-stu-id="b2aac-105">This is different than methods of device restriction such as Kiosk mode, where  the user is presented with a UI that hides the apps on the device but they can still be launched.</span></span> <span data-ttu-id="b2aac-106">Несмотря на то, что она реализована, приложения по-прежнему отображаются в списке "все приложения", но WDAC останавливает эти приложения и процессы от возможности его запуска пользователем.</span><span class="sxs-lookup"><span data-stu-id="b2aac-106">While WDAC is implemented, the apps are still visible in the All Apps list but WDAC stops those apps and processes from being able to be launched by the device user.</span></span>

<span data-ttu-id="b2aac-107">Устройству может быть назначено больше одной политики WDAC.</span><span class="sxs-lookup"><span data-stu-id="b2aac-107">A device may be assigned more than one WDAC policy.</span></span> <span data-ttu-id="b2aac-108">Если в системе настроено несколько политик WDAC, вступают в силу большинство из них ограничения.</span><span class="sxs-lookup"><span data-stu-id="b2aac-108">If multiple WDAC policies are set on a system, most restrictive ones take effect.</span></span> 

> [!NOTE]
> <span data-ttu-id="b2aac-109">Когда конечные пользователи пытаются запустить приложение, которое заблокировано компанией WDAC, на HoloLens они не получат уведомление о том, что невозможно запустить это приложение.</span><span class="sxs-lookup"><span data-stu-id="b2aac-109">When end users attempt to launch an app that is blocked by WDAC, on HoloLens they will not receive a notification about not being able to launch that app.</span></span>

<span data-ttu-id="b2aac-110">Ниже приведено руководство, в котором описаны способы [использования WDAC и Windows PowerShell для разрешения и блокировки приложений на устройствах HoloLens 2 с помощью Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens).</span><span class="sxs-lookup"><span data-stu-id="b2aac-110">The following is a guide for users to learn how to [use WDAC and Windows PowerShell to allow or block apps on HoloLens 2 devices with Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens).</span></span>

<span data-ttu-id="b2aac-111">При поиске приложений, установленных на компьютере с Windows 10 с помощью первого этапа, вам может потребоваться выполнить несколько попыток сузить результаты.</span><span class="sxs-lookup"><span data-stu-id="b2aac-111">When users search for apps installed on their Windows 10 PC using the first example step they may need to make a few attempts to narrow down the results.</span></span>

```powershell
$package1 = Get-AppxPackage -name *<applicationname>*
``` 

<span data-ttu-id="b2aac-112">Если вы не знаете полное имя пакета, возможно, потребуется выполнить "Get-AppxPackage-Name \ \* YourBestGuess \ \*" несколько раз, чтобы найти его.</span><span class="sxs-lookup"><span data-stu-id="b2aac-112">If you don’t know the full name of the package, you may need to run ‘Get-AppxPackage -name \*YourBestGuess\*’ a few times to find it.</span></span> <span data-ttu-id="b2aac-113">После того как вы запустили имя "$package 1 = Get-AppxPackage-Name Actual. PackageName"</span><span class="sxs-lookup"><span data-stu-id="b2aac-113">Then once you have the name run ‘$package1 = Get-AppxPackage -name Actual.PackageName‘</span></span>

<span data-ttu-id="b2aac-114">Например, при выполнении следующего для Edge будет возвращено больше одного результата, но из этого списка вы можете указать, что полное имя должно быть для Microsoft. MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="b2aac-114">For example running the following for Edge will return more than one result, but from that list you can identify that the full name you need is Microsoft.MicrosoftEdge.</span></span> 

```powershell
Get-AppxPackage -name *edge*
``` 

## <span data-ttu-id="b2aac-115">Имена семейств пакетов для приложений на HoloLens</span><span class="sxs-lookup"><span data-stu-id="b2aac-115">Package Family Names for apps on HoloLens</span></span>

<span data-ttu-id="b2aac-116">В руководстве, описанном выше, вы можете вручную изменить newPolicy.xml и добавить правила для приложений, которые установлены только на HoloLens с их именами семейства пакетов.</span><span class="sxs-lookup"><span data-stu-id="b2aac-116">In the guide linked above, you can manually edit newPolicy.xml and add rules for applications which are only installed on HoloLens with their package family names.</span></span> <span data-ttu-id="b2aac-117">Иногда есть приложения, которые вы можете использовать, а не на настольном компьютере, который вы хотите добавить к политике.</span><span class="sxs-lookup"><span data-stu-id="b2aac-117">Sometimes there are apps you may use to use that are not on your desktop PC that you wish to add to policy.</span></span> 

<span data-ttu-id="b2aac-118">Ниже приведен список часто используемых и In-Box приложений для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="b2aac-118">Here is a list of commonly used and In-Box apps for HoloLens 2 devices.</span></span>

| <span data-ttu-id="b2aac-119">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="b2aac-119">App Name</span></span>                   | <span data-ttu-id="b2aac-120">Имя семейства пакетов</span><span class="sxs-lookup"><span data-stu-id="b2aac-120">Package Family Name</span></span>                                |
|----------------------------|----------------------------------------------------|
| <span data-ttu-id="b2aac-121">Средство 3D-просмотра</span><span class="sxs-lookup"><span data-stu-id="b2aac-121">3D Viewer</span></span>                  | <span data-ttu-id="b2aac-122">Microsoft.Microsoft3DViewer_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-122">Microsoft.Microsoft3DViewer_8wekyb3d8bbwe</span></span>          |
| <span data-ttu-id="b2aac-123">Установщик приложений</span><span class="sxs-lookup"><span data-stu-id="b2aac-123">App Installer</span></span>              | <span data-ttu-id="b2aac-124">Microsoft.DesktopAppInstaller_8wekyb3d8bbwe <sup> 1</span><span class="sxs-lookup"><span data-stu-id="b2aac-124">Microsoft.DesktopAppInstaller_8wekyb3d8bbwe <sup>1</span></span></sup>         |
| <span data-ttu-id="b2aac-125">Календарь</span><span class="sxs-lookup"><span data-stu-id="b2aac-125">Calendar</span></span>                   | <span data-ttu-id="b2aac-126">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-126">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span></span>  |
| <span data-ttu-id="b2aac-127">Камера</span><span class="sxs-lookup"><span data-stu-id="b2aac-127">Camera</span></span>                     | <span data-ttu-id="b2aac-128">HoloCamera_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="b2aac-128">HoloCamera_cw5n1h2txyewy</span></span>                           |
| <span data-ttu-id="b2aac-129">Кортана</span><span class="sxs-lookup"><span data-stu-id="b2aac-129">Cortana</span></span>                    | <span data-ttu-id="b2aac-130">Microsoft.549981C3F5F10_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-130">Microsoft.549981C3F5F10_8wekyb3d8bbwe</span></span>              |
| <span data-ttu-id="b2aac-131">Руководства по Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b2aac-131">Dynamics 365 Guides</span></span>        | <span data-ttu-id="b2aac-132">Microsoft.Dynamics365.Guides_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-132">Microsoft.Dynamics365.Guides_8wekyb3d8bbwe</span></span>         |
| <span data-ttu-id="b2aac-133">Dynamics 365 Remote Assist</span><span class="sxs-lookup"><span data-stu-id="b2aac-133">Dynamics 365 Remote Assist</span></span> | <span data-ttu-id="b2aac-134">Microsoft.MicrosoftRemoteAssist_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-134">Microsoft.MicrosoftRemoteAssist_8wekyb3d8bbwe</span></span>      |
| <span data-ttu-id="b2aac-135">Центр отзывов</span><span class="sxs-lookup"><span data-stu-id="b2aac-135">Feedback Hub</span></span>               | <span data-ttu-id="b2aac-136">Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-136">Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe</span></span>         |
| <span data-ttu-id="b2aac-137">Проводник</span><span class="sxs-lookup"><span data-stu-id="b2aac-137">File Explorer</span></span>              | <span data-ttu-id="b2aac-138">c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="b2aac-138">c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy</span></span> |
| <span data-ttu-id="b2aac-139">Mail</span><span class="sxs-lookup"><span data-stu-id="b2aac-139">Mail</span></span>                       | <span data-ttu-id="b2aac-140">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-140">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span></span>  |
| <span data-ttu-id="b2aac-141">Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="b2aac-141">Microsoft Store</span></span>            | <span data-ttu-id="b2aac-142">Microsoft.WindowsStore_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-142">Microsoft.WindowsStore_8wekyb3d8bbwe</span></span>               |
| <span data-ttu-id="b2aac-143">Кино и ТВ</span><span class="sxs-lookup"><span data-stu-id="b2aac-143">Movies & TV</span></span>                | <span data-ttu-id="b2aac-144">Microsoft.ZuneVideo_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-144">Microsoft.ZuneVideo_8wekyb3d8bbwe</span></span>                  |
| <span data-ttu-id="b2aac-145">OneDrive</span><span class="sxs-lookup"><span data-stu-id="b2aac-145">OneDrive</span></span>                   | <span data-ttu-id="b2aac-146">microsoft.microsoftskydrive_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-146">microsoft.microsoftskydrive_8wekyb3d8bbwe</span></span>          |
| <span data-ttu-id="b2aac-147">Фотографии</span><span class="sxs-lookup"><span data-stu-id="b2aac-147">Photos</span></span>                     | <span data-ttu-id="b2aac-148">Microsoft.Windows.Photos_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-148">Microsoft.Windows.Photos_8wekyb3d8bbwe</span></span>             |
| <span data-ttu-id="b2aac-149">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2aac-149">Settings</span></span>                   | <span data-ttu-id="b2aac-150">HolographicSystemSettings_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="b2aac-150">HolographicSystemSettings_cw5n1h2txyewy</span></span>            |
| <span data-ttu-id="b2aac-151">Советы</span><span class="sxs-lookup"><span data-stu-id="b2aac-151">Tips</span></span>                       | <span data-ttu-id="b2aac-152">Microsoft.HoloLensTips_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="b2aac-152">Microsoft.HoloLensTips_8wekyb3d8bbwe</span></span>               |

- <span data-ttu-id="b2aac-153">1-блокирующей установщик приложения блокирует только приложение установщика приложения, а не приложения, установленные из других источников, таких как Microsoft Store или решение MDM.</span><span class="sxs-lookup"><span data-stu-id="b2aac-153">1 - Blocking App Installer will only block the App Installer app, and not apps installed from other sources such as the Microsoft Store or from your MDM solution.</span></span>

### <span data-ttu-id="b2aac-154">Как найти имя семейства пакетов</span><span class="sxs-lookup"><span data-stu-id="b2aac-154">How to find a Package Family Name</span></span>

<span data-ttu-id="b2aac-155">Если приложение не включено в этот список, пользователь может использовать портал устройств, подключенный к HoloLens 2, на котором установлено приложение, которое нужно заблокировать, чтобы определить PackageRelativeID и от него получится PackageFamilyName.</span><span class="sxs-lookup"><span data-stu-id="b2aac-155">If an app is not on this list then a user may use Device Portal, connected to a HoloLens 2 that has installed the app wished to be blocked, to determine the PackageRelativeID and from there get the PackageFamilyName.</span></span>

1. <span data-ttu-id="b2aac-156">Установите приложение на устройстве HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="b2aac-156">Install the app on your HoloLens 2 device.</span></span> 
1. <span data-ttu-id="b2aac-157">Открыть параметры: > обновления & безопасность — > для разработчиков и включить **режим разработчика** , а затем **портал устройств**.</span><span class="sxs-lookup"><span data-stu-id="b2aac-157">Open Settings -> Updates & Security -> For developers, and enable **Developer mode** and then **Device portal**.</span></span> 
    1. <span data-ttu-id="b2aac-158">Дополнительные сведения о [настройке и использовании на портале устройств](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).</span><span class="sxs-lookup"><span data-stu-id="b2aac-158">More more details instructions read more about [setup and use of device portal here](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).</span></span>
1. <span data-ttu-id="b2aac-159">После подключения к порталу устройств перейдите в раздел " **представления** " и выберите пункт " **приложения**".</span><span class="sxs-lookup"><span data-stu-id="b2aac-159">Once Device Portal is connected, navigate to **Views** then **Apps**.</span></span> 
1. <span data-ttu-id="b2aac-160">На панели установленные приложения выберите установленное приложение с помощью раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="b2aac-160">Within the Installed Apps panel use the dropdown to select the installed app.</span></span> 
1. <span data-ttu-id="b2aac-161">Найдите PackageRelativeID.</span><span class="sxs-lookup"><span data-stu-id="b2aac-161">Locate the PackageRelativeID.</span></span> 
1. <span data-ttu-id="b2aac-162">Скопируйте символы приложения перед знаком! это будет ваша PackageFamilyName.</span><span class="sxs-lookup"><span data-stu-id="b2aac-162">Copy app characters before the !, this will be your PackageFamilyName.</span></span>


