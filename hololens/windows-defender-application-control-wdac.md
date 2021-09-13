---
title: Управление приложениями в Защитнике Windows (WDAC)
description: общие сведения о том, что такое Защитник Windows управления приложениями и как его использовать для управления устройствами HoloLens смешанной реальности.
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: v-evmill
ms.topic: article
ms.localizationpriority: medium
ms.date: 9/3/2021
ms.reviewer: ''
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: b5c3b55273346f330580b07e5294e7e8e65ea12d
ms.sourcegitcommit: e9f746aa41139859edc12fbc21f926c9461da4b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2021
ms.locfileid: "126033945"
---
# <a name="windows-defender-application-control---wdac"></a>Управление приложениями в Защитнике Windows — WDAC

## <a name="overview"></a>Общие сведения

WDAC позволяет настроить HoloLens для блокировки запуска приложений. Он отличается от режима киоска, в котором пользовательский интерфейс скрывает приложения, но они по-прежнему могут быть запущены. С помощью WDAC вы видите приложения, но не можете их запускать.

> [!NOTE]
> когда конечные пользователи пытаются запустить приложение, заблокированное с помощью WDAC на HoloLens, они не будут уведомлены о том, что не сможет запустить приложение.

Устройству может быть назначено более одной политики WDAC. Если в системе задано несколько политик WDAC, то большинство их максимальных приоритетов вступают в силу. 

ниже приведено руководство для пользователей о том, как [использовать WDAC и Windows PowerShell для разрешения или блокировки приложений на HoloLens 2 устройствах с помощью Microsoft Intune](/mem/intune/configuration/custom-profile-hololens).

когда пользователи выполняют поиск приложений, установленных на Windows 10 компьютере с помощью первого шага, им может потребоваться несколько попыток уменьшить результаты.

```powershell
$package1 = Get-AppxPackage -name *<applicationname>*
``` 

Если полное имя пакета неизвестно, может потребоваться выполнить команду "Get-AppxPackage-Name \* йоурбестгуесс \* " несколько раз, чтобы найти его. После этого введите имя "$package 1 = Get-AppxPackage-Name Actual. PackageName"

например, при выполнении следующего кода для Microsoft Edge будет возвращено несколько результатов, но из этого списка можно будет выяснить, что все необходимое имя — Microsoft. микрософтедже.

```powershell
Get-AppxPackage -name *edge*
``` 

## <a name="package-family-names-for-apps-on-hololens"></a>Имена семейств пакетов для приложений на HoloLens

в приведенном выше программном обеспечении можно вручную изменить newPolicy.xml и добавить правила для приложений, которые установлены только на HoloLens с именами семейств пакетов. Иногда есть приложения, которые можно использовать для использования, но не на настольном компьютере, который вы хотите добавить в политику.

ниже приведен список часто используемых и In-Box приложений для HoloLens 2 устройств.

| имя приложения;                   | Имя семейства пакетов                                |
|----------------------------|----------------------------------------------------|
| Средство 3D-просмотра                  | Microsoft.Microsoft3DViewer_8wekyb3d8bbwe          |
| Установщик приложений              | Microsoft.DesktopAppInstaller_8wekyb3d8bbwe <sup>1</sup>         |
| Календарь                   | microsoft.windowscommunicationsapps_8wekyb3d8bbwe  |
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
| "Фото"                     | NNTP. Windows. Photos_8wekyb3d8bbwe             |
| Параметры                   | HolographicSystemSettings_cw5n1h2txyewy            |
| "Советы"                       | Microsoft.HoloLensTips_8wekyb3d8bbwe               |

- 1. блокировка установщика приложений блокирует только приложение установщика приложений, а не приложения, установленные из других источников, таких как Microsoft Store или из решения MDM.

### <a name="how-to-find-a-package-family-name"></a>Как найти имя семейства пакетов

если приложение не находится в этом списке, пользователь может использовать портал устройств, подключенный к HoloLens 2, на котором установлено приложение с желанием блокироваться, чтобы определить паккажерелативеид и получить паккажефамилинаме.

1. установите приложение на устройство HoloLens 2. 
1. откройте Параметры-> обновления & безопасность — > для разработчиков и включите **режим разработчика** , а затем **портал устройств**. 
    1. Более подробные инструкции см. здесь. Дополнительные сведения о [настройке и использовании портала устройств см. здесь](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal).
1. После подключения портала устройств перейдите к **представлениям** , а затем **приложения**. 
1. На панели установленные приложения в раскрывающемся списке выберите установленное приложение. 
1. Нахождение Паккажерелативеид. 
1. Скопируйте символы приложения перед `!` , эти символы будут паккажефамилинаме.

