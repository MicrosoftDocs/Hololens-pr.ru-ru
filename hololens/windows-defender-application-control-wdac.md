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
# Управление приложениями в Защитнике Windows — WDAC

WDAC позволяет ИТ – администратору настроить устройства таким образом, чтобы блокировать запуск приложений на устройствах. Это отличается от методов ограничения устройств, таких как режим киоска, в котором пользователь представляется в пользовательском интерфейсе, который скрывает приложения на устройстве, но и все еще может запускаться. Несмотря на то, что она реализована, приложения по-прежнему отображаются в списке "все приложения", но WDAC останавливает эти приложения и процессы от возможности его запуска пользователем.

Устройству может быть назначено больше одной политики WDAC. Если в системе настроено несколько политик WDAC, вступают в силу большинство из них ограничения. 

> [!NOTE]
> Когда конечные пользователи пытаются запустить приложение, которое заблокировано компанией WDAC, на HoloLens они не получат уведомление о том, что невозможно запустить это приложение.

Ниже приведено руководство, в котором описаны способы [использования WDAC и Windows PowerShell для разрешения и блокировки приложений на устройствах HoloLens 2 с помощью Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens).

При поиске приложений, установленных на компьютере с Windows 10 с помощью первого этапа, вам может потребоваться выполнить несколько попыток сузить результаты.

```powershell
$package1 = Get-AppxPackage -name *<applicationname>*
``` 

Если вы не знаете полное имя пакета, возможно, потребуется выполнить "Get-AppxPackage-Name \ * YourBestGuess \ *" несколько раз, чтобы найти его. После того как вы запустили имя "$package 1 = Get-AppxPackage-Name Actual. PackageName"

Например, при выполнении следующего для Edge будет возвращено больше одного результата, но из этого списка вы можете указать, что полное имя должно быть для Microsoft. MicrosoftEdge. 

```powershell
Get-AppxPackage -name *edge*
``` 

## Имена семейств пакетов для приложений на HoloLens

В руководстве, описанном выше, вы можете вручную изменить newPolicy.xml и добавить правила для приложений, которые установлены только на HoloLens с их именами семейства пакетов. Иногда есть приложения, которые вы можете использовать, а не на настольном компьютере, который вы хотите добавить к политике. 

Ниже приведен список часто используемых и In-Box приложений для устройств HoloLens 2.

| Имя приложения                   | Имя семейства пакетов                                |
|----------------------------|----------------------------------------------------|
| Средство 3D-просмотра                  | Microsoft.Microsoft3DViewer_8wekyb3d8bbwe          |
| Установщик приложений              | Microsoft.DesktopAppInstaller_8wekyb3d8bbwe <sup> 1</sup>         |
| Календарь                   | microsoft.windowscommunicationsapps_8wekyb3d8bbwe  |
| Камера                     | HoloCamera_cw5n1h2txyewy                           |
| Кортана                    | Microsoft.549981C3F5F10_8wekyb3d8bbwe              |
| Руководства по Dynamics 365        | Microsoft.Dynamics365.Guides_8wekyb3d8bbwe         |
| Dynamics 365 Remote Assist | Microsoft.MicrosoftRemoteAssist_8wekyb3d8bbwe      |
| Центр отзывов               | Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe         |
| Проводник              | c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy |
| Mail                       | microsoft.windowscommunicationsapps_8wekyb3d8bbwe  |
| Microsoft Store            | Microsoft.WindowsStore_8wekyb3d8bbwe               |
| Кино и ТВ                | Microsoft.ZuneVideo_8wekyb3d8bbwe                  |
| OneDrive                   | microsoft.microsoftskydrive_8wekyb3d8bbwe          |
| Фотографии                     | Microsoft.Windows.Photos_8wekyb3d8bbwe             |
| Параметры                   | HolographicSystemSettings_cw5n1h2txyewy            |
| Советы                       | Microsoft.HoloLensTips_8wekyb3d8bbwe               |

- 1-блокирующей установщик приложения блокирует только приложение установщика приложения, а не приложения, установленные из других источников, таких как Microsoft Store или решение MDM.

### Как найти имя семейства пакетов

Если приложение не включено в этот список, пользователь может использовать портал устройств, подключенный к HoloLens 2, на котором установлено приложение, которое нужно заблокировать, чтобы определить PackageRelativeID и от него получится PackageFamilyName.

1. Установите приложение на устройстве HoloLens 2. 
1. Открыть параметры: > обновления & безопасность — > для разработчиков и включить **режим разработчика** , а затем **портал устройств**. 
    1. Дополнительные сведения о [настройке и использовании на портале устройств](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).
1. После подключения к порталу устройств перейдите в раздел " **представления** " и выберите пункт " **приложения**". 
1. На панели установленные приложения выберите установленное приложение с помощью раскрывающегося списка. 
1. Найдите PackageRelativeID. 
1. Скопируйте символы приложения перед знаком! это будет ваша PackageFamilyName.


