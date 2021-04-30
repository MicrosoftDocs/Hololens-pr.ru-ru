---
title: Управление приложениями в Защитнике Windows — WDAC
description: Общие сведения о том, что такое управление приложениями в Защитнике Windows и как его использовать для управления устройствами в смешанной реальности HoloLens.
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
ms.openlocfilehash: 23c9a274387424e8f084a4729ee621e130820716
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309406"
---
# <a name="windows-defender-application-control---wdac"></a><span data-ttu-id="a399f-103">Управление приложениями в Защитнике Windows — WDAC</span><span class="sxs-lookup"><span data-stu-id="a399f-103">Windows Defender Application Control - WDAC</span></span>

<span data-ttu-id="a399f-104">WDAC позволяет ИТ – администратору настроить устройства для блокировки запуска приложений на устройствах.</span><span class="sxs-lookup"><span data-stu-id="a399f-104">WDAC allows an IT Admin to configure their devices to block the launch of apps on devices.</span></span> <span data-ttu-id="a399f-105">Это отличается от методов ограниченного использования устройств, таких как режим киоска, где пользователю предоставляется пользовательский интерфейс, который скрывает приложения на устройстве, но их все еще можно запустить.</span><span class="sxs-lookup"><span data-stu-id="a399f-105">This is different than methods of device restriction such as Kiosk mode, where  the user is presented with a UI that hides the apps on the device but they can still be launched.</span></span> <span data-ttu-id="a399f-106">В то время как WDAC реализован, приложения по-прежнему отображаются в списке все приложения, но при этом эти приложения и процессы не смогут быть запущены пользователем устройства.</span><span class="sxs-lookup"><span data-stu-id="a399f-106">While WDAC is implemented, the apps are still visible in the All Apps list but WDAC stops those apps and processes from being able to be launched by the device user.</span></span>

<span data-ttu-id="a399f-107">Устройству может быть назначено более одной политики WDAC.</span><span class="sxs-lookup"><span data-stu-id="a399f-107">A device may be assigned more than one WDAC policy.</span></span> <span data-ttu-id="a399f-108">Если в системе задано несколько политик WDAC, то большинство их максимальных приоритетов вступают в силу.</span><span class="sxs-lookup"><span data-stu-id="a399f-108">If multiple WDAC policies are set on a system, most restrictive ones take effect.</span></span> 

> [!NOTE]
> <span data-ttu-id="a399f-109">Когда конечные пользователи пытаются запустить приложение, заблокированное WDAC, в HoloLens они не получат уведомление о том, что не сможет запустить это приложение.</span><span class="sxs-lookup"><span data-stu-id="a399f-109">When end users attempt to launch an app that is blocked by WDAC, on HoloLens they will not receive a notification about not being able to launch that app.</span></span>

<span data-ttu-id="a399f-110">Ниже приведено руководство для пользователей о том, как [использовать WDAC и Windows PowerShell для разрешения или блокировки приложений на устройствах HoloLens 2 с Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens).</span><span class="sxs-lookup"><span data-stu-id="a399f-110">The following is a guide for users to learn how to [use WDAC and Windows PowerShell to allow or block apps on HoloLens 2 devices with Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens).</span></span>

<span data-ttu-id="a399f-111">Когда пользователи выполняют поиск приложений, установленных на компьютере с Windows 10, с помощью первого шага, им может потребоваться несколько попыток уменьшить результаты.</span><span class="sxs-lookup"><span data-stu-id="a399f-111">When users search for apps installed on their Windows 10 PC using the first example step, they may need to make a few attempts to narrow down the results.</span></span>

```powershell
$package1 = Get-AppxPackage -name *<applicationname>*
``` 

<span data-ttu-id="a399f-112">Если полное имя пакета неизвестно, может потребоваться выполнить команду "Get-AppxPackage-Name \* йоурбестгуесс \* " несколько раз, чтобы найти его.</span><span class="sxs-lookup"><span data-stu-id="a399f-112">If you don’t know the full name of the package, you may need to run ‘Get-AppxPackage -name \*YourBestGuess\*’ a few times to find it.</span></span> <span data-ttu-id="a399f-113">После этого введите имя "$package 1 = Get-AppxPackage-Name Actual. PackageName"</span><span class="sxs-lookup"><span data-stu-id="a399f-113">Then once you have the name run ‘$package1 = Get-AppxPackage -name Actual.PackageName‘</span></span>

<span data-ttu-id="a399f-114">Например, если запустить следующий код для Microsoft ребра, будет возвращено несколько результатов, но из этого списка можно будет выяснить, что требуется полное имя: Microsoft. Микрософтедже.</span><span class="sxs-lookup"><span data-stu-id="a399f-114">For example running the following for Microsoft Edge will return more than one result, but from that list you can identify that the full name you need is Microsoft.MicrosoftEdge.</span></span>

```powershell
Get-AppxPackage -name *edge*
``` 

## <a name="package-family-names-for-apps-on-hololens"></a><span data-ttu-id="a399f-115">Имена семейств пакетов для приложений в HoloLens</span><span class="sxs-lookup"><span data-stu-id="a399f-115">Package Family Names for apps on HoloLens</span></span>

<span data-ttu-id="a399f-116">В приведенном выше программном обеспечении можно вручную изменить newPolicy.xml и добавить правила для приложений, которые установлены только в HoloLens с именами семейств пакетов.</span><span class="sxs-lookup"><span data-stu-id="a399f-116">In the guide linked above, you can manually edit newPolicy.xml and add rules for applications that are only installed on HoloLens with their package family names.</span></span> <span data-ttu-id="a399f-117">Иногда есть приложения, которые можно использовать для использования, но не на настольном компьютере, который вы хотите добавить в политику.</span><span class="sxs-lookup"><span data-stu-id="a399f-117">Sometimes there are apps you may use to use that are not on your desktop PC that you wish to add to policy.</span></span>

<span data-ttu-id="a399f-118">Ниже приведен список часто используемых и In-Box приложений для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="a399f-118">Here is a list of commonly used and In-Box apps for HoloLens 2 devices.</span></span>

| <span data-ttu-id="a399f-119">имя приложения;</span><span class="sxs-lookup"><span data-stu-id="a399f-119">App Name</span></span>                   | <span data-ttu-id="a399f-120">Имя семейства пакетов</span><span class="sxs-lookup"><span data-stu-id="a399f-120">Package Family Name</span></span>                                |
|----------------------------|----------------------------------------------------|
| <span data-ttu-id="a399f-121">Средство просмотра 3D-объектов</span><span class="sxs-lookup"><span data-stu-id="a399f-121">3D Viewer</span></span>                  | <span data-ttu-id="a399f-122">Microsoft.Microsoft3DViewer_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-122">Microsoft.Microsoft3DViewer_8wekyb3d8bbwe</span></span>          |
| <span data-ttu-id="a399f-123">Установщик приложений</span><span class="sxs-lookup"><span data-stu-id="a399f-123">App Installer</span></span>              | <span data-ttu-id="a399f-124">Microsoft.DesktopAppInstaller_8wekyb3d8bbwe <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="a399f-124">Microsoft.DesktopAppInstaller_8wekyb3d8bbwe <sup>1</sup></span></span>         |
| <span data-ttu-id="a399f-125">"Календарь"</span><span class="sxs-lookup"><span data-stu-id="a399f-125">Calendar</span></span>                   | <span data-ttu-id="a399f-126">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-126">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span></span>  |
| <span data-ttu-id="a399f-127">Камера</span><span class="sxs-lookup"><span data-stu-id="a399f-127">Camera</span></span>                     | <span data-ttu-id="a399f-128">HoloCamera_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="a399f-128">HoloCamera_cw5n1h2txyewy</span></span>                           |
| <span data-ttu-id="a399f-129">Кортана</span><span class="sxs-lookup"><span data-stu-id="a399f-129">Cortana</span></span>                    | <span data-ttu-id="a399f-130">Microsoft.549981C3F5F10_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-130">Microsoft.549981C3F5F10_8wekyb3d8bbwe</span></span>              |
| <span data-ttu-id="a399f-131">Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="a399f-131">Dynamics 365 Guides</span></span>        | <span data-ttu-id="a399f-132">Microsoft.Dynamics365.Guides_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-132">Microsoft.Dynamics365.Guides_8wekyb3d8bbwe</span></span>         |
| <span data-ttu-id="a399f-133">Dynamics 365 Remote Assist;</span><span class="sxs-lookup"><span data-stu-id="a399f-133">Dynamics 365 Remote Assist</span></span> | <span data-ttu-id="a399f-134">Microsoft.MicrosoftRemoteAssist_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-134">Microsoft.MicrosoftRemoteAssist_8wekyb3d8bbwe</span></span>      |
| <span data-ttu-id="a399f-135">Центр отзывов</span><span class="sxs-lookup"><span data-stu-id="a399f-135">Feedback Hub</span></span>               | <span data-ttu-id="a399f-136">Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-136">Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe</span></span>         |
| <span data-ttu-id="a399f-137">Проводник</span><span class="sxs-lookup"><span data-stu-id="a399f-137">File Explorer</span></span>              | <span data-ttu-id="a399f-138">c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="a399f-138">c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy</span></span> |
| <span data-ttu-id="a399f-139">Mail</span><span class="sxs-lookup"><span data-stu-id="a399f-139">Mail</span></span>                       | <span data-ttu-id="a399f-140">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-140">microsoft.windowscommunicationsapps_8wekyb3d8bbwe</span></span>  |
| <span data-ttu-id="a399f-141">Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="a399f-141">Microsoft Store</span></span>            | <span data-ttu-id="a399f-142">Microsoft.WindowsStore_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-142">Microsoft.WindowsStore_8wekyb3d8bbwe</span></span>               |
| <span data-ttu-id="a399f-143">Кино и ТВ</span><span class="sxs-lookup"><span data-stu-id="a399f-143">Movies & TV</span></span>                | <span data-ttu-id="a399f-144">Microsoft.ZuneVideo_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-144">Microsoft.ZuneVideo_8wekyb3d8bbwe</span></span>                  |
| <span data-ttu-id="a399f-145">OneDrive</span><span class="sxs-lookup"><span data-stu-id="a399f-145">OneDrive</span></span>                   | <span data-ttu-id="a399f-146">microsoft.microsoftskydrive_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-146">microsoft.microsoftskydrive_8wekyb3d8bbwe</span></span>          |
| <span data-ttu-id="a399f-147">Фотографии</span><span class="sxs-lookup"><span data-stu-id="a399f-147">Photos</span></span>                     | <span data-ttu-id="a399f-148">Microsoft.Windows.Photos_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-148">Microsoft.Windows.Photos_8wekyb3d8bbwe</span></span>             |
| <span data-ttu-id="a399f-149">Параметры</span><span class="sxs-lookup"><span data-stu-id="a399f-149">Settings</span></span>                   | <span data-ttu-id="a399f-150">HolographicSystemSettings_cw5n1h2txyewy</span><span class="sxs-lookup"><span data-stu-id="a399f-150">HolographicSystemSettings_cw5n1h2txyewy</span></span>            |
| <span data-ttu-id="a399f-151">Советы</span><span class="sxs-lookup"><span data-stu-id="a399f-151">Tips</span></span>                       | <span data-ttu-id="a399f-152">Microsoft.HoloLensTips_8wekyb3d8bbwe</span><span class="sxs-lookup"><span data-stu-id="a399f-152">Microsoft.HoloLensTips_8wekyb3d8bbwe</span></span>               |

- <span data-ttu-id="a399f-153">1. Блокировка установщика приложений блокирует только приложение установщика приложений, а не приложения, установленные из других источников, таких как Microsoft Store или из решения MDM.</span><span class="sxs-lookup"><span data-stu-id="a399f-153">1 - Blocking App Installer will only block the App Installer app, and not apps installed from other sources such as the Microsoft Store or from your MDM solution.</span></span>

### <a name="how-to-find-a-package-family-name"></a><span data-ttu-id="a399f-154">Как найти имя семейства пакетов</span><span class="sxs-lookup"><span data-stu-id="a399f-154">How to find a Package Family Name</span></span>

<span data-ttu-id="a399f-155">Если приложение не находится в этом списке, пользователь может использовать портал устройств, подключенный к HoloLens 2, который установил приложение, которое нужно заблокировать, чтобы определить Паккажерелативеид и получить Паккажефамилинаме.</span><span class="sxs-lookup"><span data-stu-id="a399f-155">If an app is not on this list, then a user may use Device Portal, connected to a HoloLens 2 that has installed the app wished to be blocked, to determine the PackageRelativeID and from there get the PackageFamilyName.</span></span>

1. <span data-ttu-id="a399f-156">Установите приложение на устройстве HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="a399f-156">Install the app on your HoloLens 2 device.</span></span> 
1. <span data-ttu-id="a399f-157">Откройте параметры-> обновления & безопасность-> для разработчиков и включите **режим разработчика** , а затем **портал устройств**.</span><span class="sxs-lookup"><span data-stu-id="a399f-157">Open Settings -> Updates & Security -> For developers, and enable **Developer mode** and then **Device portal**.</span></span> 
    1. <span data-ttu-id="a399f-158">Более подробные инструкции см. здесь. Дополнительные сведения о [настройке и использовании портала устройств см. здесь](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).</span><span class="sxs-lookup"><span data-stu-id="a399f-158">More more details instructions read more about [setup and use of device portal here](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).</span></span>
1. <span data-ttu-id="a399f-159">После подключения портала устройств перейдите к **представлениям** , а затем **приложения**.</span><span class="sxs-lookup"><span data-stu-id="a399f-159">Once Device Portal is connected, navigate to **Views** then **Apps**.</span></span> 
1. <span data-ttu-id="a399f-160">На панели установленные приложения в раскрывающемся списке выберите установленное приложение.</span><span class="sxs-lookup"><span data-stu-id="a399f-160">Within the Installed Apps panel, use the dropdown to select the installed app.</span></span> 
1. <span data-ttu-id="a399f-161">Нахождение Паккажерелативеид.</span><span class="sxs-lookup"><span data-stu-id="a399f-161">Locate the PackageRelativeID.</span></span> 
1. <span data-ttu-id="a399f-162">Копировать символы приложения перед!, эти символы будут Паккажефамилинаме.</span><span class="sxs-lookup"><span data-stu-id="a399f-162">Copy app characters before the !, these characters will be your PackageFamilyName.</span></span>


