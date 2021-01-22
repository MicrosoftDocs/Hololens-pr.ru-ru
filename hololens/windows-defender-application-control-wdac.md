---
title: Управление приложениями в Защитнике Windows — WDAC
description: Обзор Защитник Windows управления приложениями и его использования для управления устройствами смешанной реальности HoloLens.
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
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11284140"
---
# Управление приложениями в Защитнике Windows — WDAC

WDAC позволяет ИТ-администратору настраивать свои устройства на блокировку запуска приложений на устройствах. Это отличается от методов ограничения устройств, таких как режим терминала, где пользователь получает пользовательский интерфейс, который скрывает приложения на устройстве, но их можно запускать. При реализации WDAC приложения по-прежнему видны в списке "Все приложения", но WDAC останавливает запуск этих приложений и процессов пользователем устройства.

Устройству может быть назначено несколько политик WDAC. Если в системе установлено несколько политик WDAC, в силу вступает большинство ограничительных политик. 

> [!NOTE]
> Когда конечные пользователи пытаются запустить приложение, заблокированное WDAC, на HoloLens они не получат уведомление о том, что не смогут запустить это приложение.

Ниже приводится руководство для пользователей, чтобы узнать, как использовать WDAC и Windows PowerShell, чтобы разрешить или заблокировать приложения на [устройствах HoloLens 2 с Помощью Microsoft Intune.](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens)

При поиске приложений, установленных на компьютере с Windows 10 с помощью первого примера, может потребоваться несколько попыток сузить результаты.

```powershell
$package1 = Get-AppxPackage -name *<applicationname>*
``` 

If you don't know the full name of the package, you may need to run 'Get-AppxPackage -name \*YourBestGuess\*' a few times to find it. После этого запустите имя "$package 1 = Get-AppxPackage -name Actual.PackageName"

Например, при запуске следующего для Microsoft Edge будет возвращено несколько результатов, но из этого списка можно определить, что вам нужно полное имя Microsoft.MicrosoftEdge.

```powershell
Get-AppxPackage -name *edge*
``` 

## Имена семей пакетов для приложений на HoloLens

В руководстве, связанном выше, можно вручную изменить newPolicy.xml и добавить правила для приложений, которые установлены только на HoloLens с именами их семейство пакетов. Иногда вы можете использовать приложения, которые не находятся на настольном компьютере, который вы хотите добавить в политику.

Вот список часто используемых и In-Box приложений для устройств HoloLens 2.

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

- 1 — блокирующий установщик приложений блокирует только приложение установщика приложений, а не приложения, установленные из других источников, таких как Microsoft Store или из вашего решения MDM.

### Как найти имя семейства пакетов

Если приложения нет в этом списке, пользователь может воспользоваться порталом устройств, подключенным к HoloLens 2, на который установлено приложение, которое должно быть заблокировано, чтобы определить PackageRelativeID, а затем получить PackageFamilyName.

1. Установите приложение на устройство HoloLens 2. 
1. Откройте параметры -> обновления & безопасности -> для разработчиков, в **** режиме разработчика и на **портале устройств.** 
    1. Дополнительные сведения об установке и использовании портала устройств можно узнать [здесь.](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal)
1. После подключения портала устройств **** перейдите к представлениям, а затем **к приложениям.** 
1. На панели "Установленные приложения" выберите установленное приложение с помощью dropdown. 
1. Найдите PackageRelativeID. 
1. Скопируйте символы приложения перед !, эти символы будут вашими packageFamilyName.


