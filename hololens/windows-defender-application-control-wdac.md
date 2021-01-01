---
title: Управление приложениями в Защитнике Windows — WDAC
description: Общие сведения о WDAC и использовании для управления устройствами HoloLens.
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
ms.openlocfilehash: d337f9856eaeac433524d7bb8b60e9a24e264b80
ms.sourcegitcommit: fc268335e5df529a1cedc2c6b88fa86245fe1b9b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/31/2020
ms.locfileid: "11252650"
---
# <span data-ttu-id="f1de2-103">Управление приложениями в Защитнике Windows — WDAC</span><span class="sxs-lookup"><span data-stu-id="f1de2-103">Windows Defender Application Control - WDAC</span></span>

<span data-ttu-id="f1de2-104">WDAC позволяет ИТ-администратору настраивать свои устройства на блокировку запуска приложений на устройствах.</span><span class="sxs-lookup"><span data-stu-id="f1de2-104">WDAC allows an IT Admin to configure their devices to block the launch of apps on devices.</span></span> <span data-ttu-id="f1de2-105">Это отличается от методов ограничения устройств, таких как режим терминала, где пользователь получает пользовательский интерфейс, который скрывает приложения на устройстве, но их можно запускать.</span><span class="sxs-lookup"><span data-stu-id="f1de2-105">This is different than methods of device restriction such as Kiosk mode, where  the user is presented with a UI that hides the apps on the device but they can still be launched.</span></span> <span data-ttu-id="f1de2-106">При реализации WDAC приложения по-прежнему видны в списке "Все приложения", но WDAC останавливает запуск этих приложений и процессов пользователем устройства.</span><span class="sxs-lookup"><span data-stu-id="f1de2-106">While WDAC is implemented, the apps are still visible in the All Apps list but WDAC stops those apps and processes from being able to be launched by the device user.</span></span>

<span data-ttu-id="f1de2-107">Устройству может быть назначено несколько политик WDAC.</span><span class="sxs-lookup"><span data-stu-id="f1de2-107">A device may be assigned more than one WDAC policy.</span></span> <span data-ttu-id="f1de2-108">Если в системе установлено несколько политик WDAC, в силу вступает большинство ограничительных политик.</span><span class="sxs-lookup"><span data-stu-id="f1de2-108">If multiple WDAC policies are set on a system, most restrictive ones take effect.</span></span> 

> [!NOTE]
> <span data-ttu-id="f1de2-109">Когда конечные пользователи пытаются запустить приложение, заблокированное WDAC, на HoloLens они не получат уведомление о том, что не смогут запустить это приложение.</span><span class="sxs-lookup"><span data-stu-id="f1de2-109">When end users attempt to launch an app that is blocked by WDAC, on HoloLens they will not receive a notification about not being able to launch that app.</span></span>

<span data-ttu-id="f1de2-110">Ниже приводится руководство для пользователей, чтобы узнать, как использовать WDAC и Windows PowerShell, чтобы разрешить или заблокировать приложения на [устройствах HoloLens 2 с Помощью Microsoft Intune.](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens)</span><span class="sxs-lookup"><span data-stu-id="f1de2-110">The following is a guide for users to learn how to [use WDAC and Windows PowerShell to allow or block apps on HoloLens 2 devices with Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens).</span></span>

<span data-ttu-id="f1de2-111">При поиске приложений, установленных на компьютере с Windows 10 с помощью первого примера, может потребоваться несколько попыток сузить результаты.</span><span class="sxs-lookup"><span data-stu-id="f1de2-111">When users search for apps installed on their Windows 10 PC using the first example step, they may need to make a few attempts to narrow down the results.</span></span>

```powershell
$package1 = Get-AppxPackage -name *<applicationname>*
``` 

<span data-ttu-id="f1de2-112">If you don't know the full name of the package, you may need to run 'Get-AppxPackage -name \*YourBestGuess\*' a few times to find it.</span><span class="sxs-lookup"><span data-stu-id="f1de2-112">If you don’t know the full name of the package, you may need to run ‘Get-AppxPackage -name \*YourBestGuess\*’ a few times to find it.</span></span> <span data-ttu-id="f1de2-113">После этого запустите имя "$package 1 = Get-AppxPackage -name Actual.PackageName"</span><span class="sxs-lookup"><span data-stu-id="f1de2-113">Then once you have the name run ‘$package1 = Get-AppxPackage -name Actual.PackageName‘</span></span>

<span data-ttu-id="f1de2-114">Например, при запуске следующего для Microsoft Edge будет возвращено несколько результатов, но из этого списка можно определить, что вам нужно полное имя Microsoft.MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="f1de2-114">For example running the following for Microsoft Edge will return more than one result, but from that list you can identify that the full name you need is Microsoft.MicrosoftEdge.</span></span>

```powershell
Get-AppxPackage -name *edge*
``` 

## <span data-ttu-id="f1de2-115">Имена семей пакетов для приложений на HoloLens</span><span class="sxs-lookup"><span data-stu-id="f1de2-115">Package Family Names for apps on HoloLens</span></span>

<span data-ttu-id="f1de2-116">В руководстве, связанном выше, можно вручную изменить newPolicy.xml и добавить правила для приложений, которые установлены только на HoloLens с именами их семейство пакетов.</span><span class="sxs-lookup"><span data-stu-id="f1de2-116">In the guide linked above, you can manually edit newPolicy.xml and add rules for applications that are only installed on HoloLens with their package family names.</span></span> <span data-ttu-id="f1de2-117">Иногда вы можете использовать приложения, которые не находятся на настольном компьютере, который вы хотите добавить в политику.</span><span class="sxs-lookup"><span data-stu-id="f1de2-117">Sometimes there are apps you may use to use that are not on your desktop PC that you wish to add to policy.</span></span>

<span data-ttu-id="f1de2-118">Вот список часто используемых и In-Box приложений для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="f1de2-118">Here is a list of commonly used and In-Box apps for HoloLens 2 devices.</span></span>

| <span data-ttu-id="f1de2-119">Имя приложения</span><span class="sxs-lookup"><span data-stu-id="f1de2-119">App Name</span></span>                   | <span data-ttu-id="f1de2-120">Имя семейства пакетов</span><span class="sxs-lookup"><span data-stu-id="f1de2-120">Package Family Name</span></span>                                |
|----------------------------|----------------------------------------------------|
| <span data-ttu-id="f1de2-121">Средство 3D-просмотра</span><span class="sxs-lookup"><span data-stu-id="f1de2-121">3D Viewer</span></span>                  | <span data-ttu-id="f1de2-122">Microsoft.Microsoft3DViewer_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-122">Microsoft.Microsoft3DViewer_8wekyb3d8bbwe</span></span>          |
| <span data-ttu-id="f1de2-123">Установщик приложений</span><span class="sxs-lookup"><span data-stu-id="f1de2-123">App Installer</span></span>              | <span data-ttu-id="f1de2-124">Microsoft.DesktopAppInstaller_8wekyb3d8bbwe <sup> 1</span><span class="sxs-lookup"><span data-stu-id="f1de2-124">Microsoft.DesktopAppInstaller_8wekyb3d8bbwe <sup>1</span></span></sup>         |
| <span data-ttu-id="f1de2-125">Календарь</span><span class="sxs-lookup"><span data-stu-id="f1de2-125">Calendar</span></span>                   | <span data-ttu-id="f1de2-126">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-126">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span></span>  |
| <span data-ttu-id="f1de2-127">Камера</span><span class="sxs-lookup"><span data-stu-id="f1de2-127">Camera</span></span>                     | <span data-ttu-id="f1de2-128">HoloCamera_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="f1de2-128">HoloCamera_cw5n1h2txyewy</span></span>                           |
| <span data-ttu-id="f1de2-129">Кортана</span><span class="sxs-lookup"><span data-stu-id="f1de2-129">Cortana</span></span>                    | <span data-ttu-id="f1de2-130">Microsoft.549981C3F5F10_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-130">Microsoft.549981C3F5F10_8wekyb3d8bbwe</span></span>              |
| <span data-ttu-id="f1de2-131">Руководства по Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f1de2-131">Dynamics 365 Guides</span></span>        | <span data-ttu-id="f1de2-132">Microsoft.Dynamics365.Guides_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-132">Microsoft.Dynamics365.Guides_8wekyb3d8bbwe</span></span>         |
| <span data-ttu-id="f1de2-133">Dynamics 365 Remote Assist</span><span class="sxs-lookup"><span data-stu-id="f1de2-133">Dynamics 365 Remote Assist</span></span> | <span data-ttu-id="f1de2-134">Microsoft.MicrosoftRemoteAssist_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-134">Microsoft.MicrosoftRemoteAssist_8wekyb3d8bbwe</span></span>      |
| <span data-ttu-id="f1de2-135">Центр отзывов</span><span class="sxs-lookup"><span data-stu-id="f1de2-135">Feedback Hub</span></span>               | <span data-ttu-id="f1de2-136">Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-136">Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe</span></span>         |
| <span data-ttu-id="f1de2-137">Проводник</span><span class="sxs-lookup"><span data-stu-id="f1de2-137">File Explorer</span></span>              | <span data-ttu-id="f1de2-138">c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="f1de2-138">c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy</span></span> |
| <span data-ttu-id="f1de2-139">Mail</span><span class="sxs-lookup"><span data-stu-id="f1de2-139">Mail</span></span>                       | <span data-ttu-id="f1de2-140">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-140">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span></span>  |
| <span data-ttu-id="f1de2-141">Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="f1de2-141">Microsoft Store</span></span>            | <span data-ttu-id="f1de2-142">Microsoft.WindowsStore_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-142">Microsoft.WindowsStore_8wekyb3d8bbwe</span></span>               |
| <span data-ttu-id="f1de2-143">Кино и ТВ</span><span class="sxs-lookup"><span data-stu-id="f1de2-143">Movies & TV</span></span>                | <span data-ttu-id="f1de2-144">Microsoft.ZuneVideo_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-144">Microsoft.ZuneVideo_8wekyb3d8bbwe</span></span>                  |
| <span data-ttu-id="f1de2-145">OneDrive</span><span class="sxs-lookup"><span data-stu-id="f1de2-145">OneDrive</span></span>                   | <span data-ttu-id="f1de2-146">microsoft.microsoftskydrive_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-146">microsoft.microsoftskydrive_8wekyb3d8bbwe</span></span>          |
| <span data-ttu-id="f1de2-147">Фотографии</span><span class="sxs-lookup"><span data-stu-id="f1de2-147">Photos</span></span>                     | <span data-ttu-id="f1de2-148">Microsoft.Windows.Photos_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-148">Microsoft.Windows.Photos_8wekyb3d8bbwe</span></span>             |
| <span data-ttu-id="f1de2-149">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1de2-149">Settings</span></span>                   | <span data-ttu-id="f1de2-150">HolographicSystemSettings_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="f1de2-150">HolographicSystemSettings_cw5n1h2txyewy</span></span>            |
| <span data-ttu-id="f1de2-151">Советы</span><span class="sxs-lookup"><span data-stu-id="f1de2-151">Tips</span></span>                       | <span data-ttu-id="f1de2-152">Microsoft.HoloLensTips_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="f1de2-152">Microsoft.HoloLensTips_8wekyb3d8bbwe</span></span>               |

- <span data-ttu-id="f1de2-153">1 — блокирующий установщик приложений блокирует только приложение установщика приложений, а не приложения, установленные из других источников, таких как Microsoft Store или из вашего решения MDM.</span><span class="sxs-lookup"><span data-stu-id="f1de2-153">1 - Blocking App Installer will only block the App Installer app, and not apps installed from other sources such as the Microsoft Store or from your MDM solution.</span></span>

### <span data-ttu-id="f1de2-154">Как найти имя семейства пакетов</span><span class="sxs-lookup"><span data-stu-id="f1de2-154">How to find a Package Family Name</span></span>

<span data-ttu-id="f1de2-155">Если приложения нет в этом списке, пользователь может воспользоваться порталом устройств, подключенным к HoloLens 2, на который установлено приложение, которое должно быть заблокировано, чтобы определить PackageRelativeID, а затем получить PackageFamilyName.</span><span class="sxs-lookup"><span data-stu-id="f1de2-155">If an app is not on this list, then a user may use Device Portal, connected to a HoloLens 2 that has installed the app wished to be blocked, to determine the PackageRelativeID and from there get the PackageFamilyName.</span></span>

1. <span data-ttu-id="f1de2-156">Установите приложение на устройство HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="f1de2-156">Install the app on your HoloLens 2 device.</span></span> 
1. <span data-ttu-id="f1de2-157">Откройте параметры -> обновления & безопасности -> для разработчиков, в \*\*\*\* режиме разработчика и на **портале устройств.**</span><span class="sxs-lookup"><span data-stu-id="f1de2-157">Open Settings -> Updates & Security -> For developers, and enable **Developer mode** and then **Device portal**.</span></span> 
    1. <span data-ttu-id="f1de2-158">Дополнительные сведения об установке и использовании портала устройств можно узнать [здесь.](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal)</span><span class="sxs-lookup"><span data-stu-id="f1de2-158">More more details instructions read more about [setup and use of device portal here](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).</span></span>
1. <span data-ttu-id="f1de2-159">После подключения портала устройств \*\*\*\* перейдите к представлениям, а затем **к приложениям.**</span><span class="sxs-lookup"><span data-stu-id="f1de2-159">Once Device Portal is connected, navigate to **Views** then **Apps**.</span></span> 
1. <span data-ttu-id="f1de2-160">На панели "Установленные приложения" выберите установленное приложение с помощью dropdown.</span><span class="sxs-lookup"><span data-stu-id="f1de2-160">Within the Installed Apps panel, use the dropdown to select the installed app.</span></span> 
1. <span data-ttu-id="f1de2-161">Найдите PackageRelativeID.</span><span class="sxs-lookup"><span data-stu-id="f1de2-161">Locate the PackageRelativeID.</span></span> 
1. <span data-ttu-id="f1de2-162">Скопируйте символы приложения перед !, эти символы будут вашими packageFamilyName.</span><span class="sxs-lookup"><span data-stu-id="f1de2-162">Copy app characters before the !, these characters will be your PackageFamilyName.</span></span>


