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
# <a name="windows-defender-application-control---wdac"></a>Управление приложениями в Защитнике Windows — WDAC

WDAC позволяет ИТ – администратору настроить устройства для блокировки запуска приложений на устройствах. Это отличается от методов ограниченного использования устройств, таких как режим киоска, где пользователю предоставляется пользовательский интерфейс, который скрывает приложения на устройстве, но их все еще можно запустить. В то время как WDAC реализован, приложения по-прежнему отображаются в списке все приложения, но при этом эти приложения и процессы не смогут быть запущены пользователем устройства.

Устройству может быть назначено более одной политики WDAC. Если в системе задано несколько политик WDAC, то большинство их максимальных приоритетов вступают в силу. 

> [!NOTE]
> Когда конечные пользователи пытаются запустить приложение, заблокированное WDAC, в HoloLens они не получат уведомление о том, что не сможет запустить это приложение.

Ниже приведено руководство для пользователей о том, как [использовать WDAC и Windows PowerShell для разрешения или блокировки приложений на устройствах HoloLens 2 с Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-profile-hololens).

Когда пользователи выполняют поиск приложений, установленных на компьютере с Windows 10, с помощью первого шага, им может потребоваться несколько попыток уменьшить результаты.

```powershell
$package1 = Get-AppxPackage -name *<applicationname>*
``` 

Если полное имя пакета неизвестно, может потребоваться выполнить команду "Get-AppxPackage-Name \* йоурбестгуесс \* " несколько раз, чтобы найти его. После этого введите имя "$package 1 = Get-AppxPackage-Name Actual. PackageName"

Например, если запустить следующий код для Microsoft ребра, будет возвращено несколько результатов, но из этого списка можно будет выяснить, что требуется полное имя: Microsoft. Микрософтедже.

```powershell
Get-AppxPackage -name *edge*
``` 

## <a name="package-family-names-for-apps-on-hololens"></a>Имена семейств пакетов для приложений в HoloLens

В приведенном выше программном обеспечении можно вручную изменить newPolicy.xml и добавить правила для приложений, которые установлены только в HoloLens с именами семейств пакетов. Иногда есть приложения, которые можно использовать для использования, но не на настольном компьютере, который вы хотите добавить в политику.

Ниже приведен список часто используемых и In-Box приложений для устройств HoloLens 2.

| имя приложения;                   | Имя семейства пакетов                                |
|----------------------------|----------------------------------------------------|
| Средство просмотра 3D-объектов                  | Microsoft.Microsoft3DViewer_8wekyb3d8bbwe          |
| Установщик приложений              | Microsoft.DesktopAppInstaller_8wekyb3d8bbwe <sup>1</sup>         |
| "Календарь"                   | microsoft.windowscommunicationsapps_8wekyb3d8bbwe  |
| Камера                     | HoloCamera_cw5n1h2txyewy                           |
| Кортана                    | Microsoft.549981C3F5F10_8wekyb3d8bbwe              |
| Dynamics 365 Guides        | Microsoft.Dynamics365.Guides_8wekyb3d8bbwe         |
| Dynamics 365 Remote Assist; | Microsoft.MicrosoftRemoteAssist_8wekyb3d8bbwe      |
| Центр отзывов               | Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe         |
| Проводник              | c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy |
| Mail                       | microsoft.windowscommunicationsapps_8wekyb3d8bbwe  |
| Microsoft Store            | Microsoft.WindowsStore_8wekyb3d8bbwe               |
| Кино и ТВ                | Microsoft.ZuneVideo_8wekyb3d8bbwe                  |
| OneDrive                   | microsoft.microsoftskydrive_8wekyb3d8bbwe          |
| Фотографии                     | Microsoft.Windows.Photos_8wekyb3d8bbwe             |
| Параметры                   | HolographicSystemSettings_cw5n1h2txyewy            |
| Советы                       | Microsoft.HoloLensTips_8wekyb3d8bbwe               |

- 1. Блокировка установщика приложений блокирует только приложение установщика приложений, а не приложения, установленные из других источников, таких как Microsoft Store или из решения MDM.

### <a name="how-to-find-a-package-family-name"></a>Как найти имя семейства пакетов

Если приложение не находится в этом списке, пользователь может использовать портал устройств, подключенный к HoloLens 2, который установил приложение, которое нужно заблокировать, чтобы определить Паккажерелативеид и получить Паккажефамилинаме.

1. Установите приложение на устройстве HoloLens 2. 
1. Откройте параметры-> обновления & безопасность-> для разработчиков и включите **режим разработчика** , а затем **портал устройств**. 
    1. Более подробные инструкции см. здесь. Дополнительные сведения о [настройке и использовании портала устройств см. здесь](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).
1. После подключения портала устройств перейдите к **представлениям** , а затем **приложения**. 
1. На панели установленные приложения в раскрывающемся списке выберите установленное приложение. 
1. Нахождение Паккажерелативеид. 
1. Копировать символы приложения перед!, эти символы будут Паккажефамилинаме.


