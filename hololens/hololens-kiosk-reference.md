---
title: справочные сведения HoloLens киоска
description: сведения и примеры для киосков на HoloLens устройствах.
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: v-evmill
ms.topic: article
ms.localizationpriority: medium
ms.date: 8/24/2021
ms.reviewer: ''
manager: yannisle
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 9f8cfd0013ac5b8cf85a334cbb89c458440820d9
ms.sourcegitcommit: e9f746aa41139859edc12fbc21f926c9461da4b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2021
ms.locfileid: "126033208"
---
# <a name="hololens-kiosk-reference-information"></a>Справочные сведения о киоске HoloLens

на этой странице содержатся полезные сведения о настройке режима киоска устройства HoloLens. Эти ссылки включают в себя Аумидс для входящих и нахождения ваших приложений, а также несколько примеров XML для полноэкранного режима. это всего лишь несколько изменений, готовых к использованию в нескольких различных сценариях. Сведения о настройке киоска см [. на странице Настройка киоска.](hololens-kiosk.md)

## <a name="hololens-application-user-model-ids-aumids"></a>HoloLens Идентификаторы модели пользователя приложения (Аумидс)  

Общие сведения о выборе приложений киоска см. в разделе [рекомендации по выбору приложения для назначенного доступа (режим киоска)](/windows/configuration/guidelines-for-assigned-access-app).

Если для настройки режима киоска используется система управления мобильными устройствами (MDM) или пакет подготовки, то для указания приложений используется [поставщик службы настройки ассигнедакцесс (CSP)](/windows/client-management/mdm/assignedaccess-csp) . CSP использует [идентификаторы модели пользователя приложения (аумидс)](/windows/configuration/find-the-application-user-model-id-of-an-installed-app) для идентификации приложений. В следующей таблице перечислены Аумидс некоторых встроенных приложений, которые можно использовать в киоске с несколькими приложениями.

<a id="aumids"></a>

|имя приложения; |AUMID |
| --- | --- |
|Средство 3D-просмотра |Microsoft. Microsoft3DViewer \_ 8wekyb3d8bbwe \! Microsoft. Microsoft3DViewer |
|Календарь |Microsoft. виндовскоммуникатионсаппс \_ 8wekyb3d8bbwe \! Microsoft. виндовсливе. Calendar |
|Камера<sup>1, 2</sup> |Холокамера \_ cw5n1h2txyewy \! холокамера |
|Кортана<sup>3</sup> |Приложение Microsoft. 549981C3F5F10 \_ 8wekyb3d8bbwe \! |
|средство выбора устройств на HoloLens (1-й общий) |Холодевицесфлов \_ cw5n1h2txyewy \! холодевицесфлов |
|Средство выбора устройств на HoloLens 2 |NNTP. Windows. Девицесфловхост \_ cw5n1h2txyewy \! Microsoft. Windows. девицесфловхост |
|Dynamics 365 Guides |Microsoft. Dynamics365. Guides \_ 8wekyb3d8bbwe \! микрософтгуидес |
|Dynamics 365 Remote Assist; |Microsoft. Микрософтремотеассист \_ 8wekyb3d8bbwe \! Microsoft. ремотеассист |
|Центр обратной связи &nbsp; |Приложение Microsoft. Виндовсфидбаккхуб \_ 8wekyb3d8bbwe \! |
|Проводник |c5e2524a-ea46-4f67-841f-6a9465d9d515_cw5n1h2txyewy!App |
|Mail |microsoft.windowscommunicationsapps_8wekyb3d8bbwe! Microsoft. виндовсливе. mail |
|Старая Microsoft Edge |Microsoft.MicrosoftEdge_8wekyb3d8bbwe!MicrosoftEdge |
|Новая версия Microsoft Edge |Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe! мседже |
|Microsoft Store |Microsoft.WindowsStore_8wekyb3d8bbwe!App |
|Miracast<sup>4</sup> | &nbsp; |
|Кино и ТВ |Microsoft. Зуневидео \_ 8wekyb3d8bbwe \! Microsoft. зуневидео |
|OneDrive |приложение Microsoft. микрософтскидриве \_ 8wekyb3d8bbwe \! |
|"Фото" |NNTP. Windows. Фото \_ 8wekyb3d8bbwe \! приложение |
|старая Параметры |HolographicSystemSettings_cw5n1h2txyewy! Приложения |
|новые Параметры |BAEAEF15-9BAB-47FC-800B-ACECAD2AE94B_cw5n1h2txyewy! Приложения |
|"Советы" |Microsoft. Хололенстипс \_ 8wekyb3d8bbwe \! хололенстипс |

> <sup>1</sup> чтобы включить запись фотографий или видео, необходимо включить приложение камеры в качестве приложения киоска.  
> <sup>2</sup> при включении приложения Camera учитывайте следующие условия.
> - Меню Быстрые действия содержит кнопки фото и видео.
> - необходимо также включить приложение (например, фотографии, письма или OneDrive), которое может взаимодействовать с изображениями или извлекать их.  
>  
> <sup>3</sup> даже если вы не включаете Кортана в качестве приложения киоска, встроенные voice-команды включены. Однако команды, связанные с отключенными функциями, не действуют.  
> <sup>4</sup> нельзя включить Miracast напрямую. Чтобы включить Miracast в качестве приложения киоска, включите приложение Camera и средство выбора устройств.

Кроме того, Домашняя страница Mixed Reality не может быть задана в качестве приложения киоска.

Возврат к [поддерживаемым сценариям для режима киоска на основе типа удостоверения](hololens-kiosk.md#supported-scenarios-for-kiosk-mode-based-on-identity-type)

## <a name="kiosk-xml-code-samples"></a>Примеры кода XML киоска

1. [Глобальный назначенный профиль доступа для нескольких приложений](#multiple-app-global-assigned-access-profile)
1. [Глобальный назначенный профиль доступа для нескольких приложений, исключая владельцев устройств](#multiple-app-global-assigned-access-profile-excluding-device-owners)
1. [Профиль доступа с несколькими приложениями для локальной учетной записи или учетной записи пользователя AAD](#multiple-app-assigned-access-profile-for-a-local-account-or-aad-user-account)
1. [Несколько профилей доступа с назначенным приложением для двух пользователей AAD или более](#multiple-app-assigned-access-profiles-for-two-aad-users-or-more)
1. [Несколько профилей доступа с назначенным приложением для одной группы AAD](#multiple-app-assigned-access-profile-for-one-aad-group)
1. [Несколько назначенных приложению профилей доступа для двух групп AAD или более](#multiple-app-assigned-access-profile-for-two-aad-groups-or-more)
1. [Несколько профилей доступа с назначенным приложением для одной учетной записи AAD и одной группы AAD](#multiple-app-assigned-access-profile-for-one-aad-account-and-one-aad-group)
1. [Профиль доступа с несколькими приложениями для посетителей](#multiple-app-assigned-access-profile-for-visitors)

> [!NOTE]
> Замените действия TODO в соответствии с вашими требованиями.

### <a name="multiple-app-global-assigned-access-profile"></a>Глобальный назначенный профиль доступа для нескольких приложений

:::code language="xml" source="samples/kiosk-sample-global-multiapp-for-everyone.xml" highlight="18-20":::

[Назад к списку](#kiosk-xml-code-samples) <br>
Возврат к [поддерживаемым сценариям для режима киоска на основе типа удостоверения](hololens-kiosk.md#supported-scenarios-for-kiosk-mode-based-on-identity-type)

### <a name="multiple-app-global-assigned-access-profile-excluding-device-owners"></a>Глобальный назначенный профиль доступа для нескольких приложений, исключая владельцев устройств

:::code language="xml" source="samples/kiosk-sample-global-multiapp-for-everyone-excluding-device-owners.xml" highlight="18-20":::

[Назад к списку](#kiosk-xml-code-samples) <br>
Возврат к [поддерживаемым сценариям для режима киоска на основе типа удостоверения](hololens-kiosk.md#supported-scenarios-for-kiosk-mode-based-on-identity-type)

### <a name="multiple-app-assigned-access-profile-for-a-local-account-or-aad-user-account"></a>Профиль доступа с несколькими приложениями для локальной учетной записи или учетной записи пользователя AAD

:::code language="xml" source="samples/kiosk-sample-multi-app-local-or-aad-user.xml" highlight="18-20,51,55":::

[Назад к списку](#kiosk-xml-code-samples) <br>
Возврат к [поддерживаемым сценариям для режима киоска на основе типа удостоверения](hololens-kiosk.md#supported-scenarios-for-kiosk-mode-based-on-identity-type)

### <a name="multiple-app-assigned-access-profiles-for-two-aad-users-or-more"></a>Несколько профилей доступа с назначенным приложением для двух пользователей AAD или более

:::code language="xml" source="samples/kiosk-sample-multi-app-two-aad-users-or-more.xml" highlight="22-24,52,53,80,88":::

[Назад к списку](#kiosk-xml-code-samples) <br>
Возврат к [поддерживаемым сценариям для режима киоска на основе типа удостоверения](hololens-kiosk.md#supported-scenarios-for-kiosk-mode-based-on-identity-type)

### <a name="multiple-app-assigned-access-profile-for-one-aad-group"></a>Несколько профилей доступа с назначенным приложением для одной группы AAD

:::code language="xml" source="samples/kiosk-sample-multi-app-one-aad-group.xml" highlight="28":::

[Назад к списку](#kiosk-xml-code-samples) <br>
Возврат к [поддерживаемым сценариям для режима киоска на основе типа удостоверения](hololens-kiosk.md#supported-scenarios-for-kiosk-mode-based-on-identity-type)

### <a name="multiple-app-assigned-access-profile-for-two-aad-groups-or-more"></a>Несколько назначенных приложению профилей доступа для двух групп AAD или более

:::code language="xml" source="samples/kiosk-sample-multi-app-two-aad-groups-or-more.xml" highlight="22-24,52,53,83,94":::

[Назад к списку](#kiosk-xml-code-samples) <br>
Возврат к [поддерживаемым сценариям для режима киоска на основе типа удостоверения](hololens-kiosk.md#supported-scenarios-for-kiosk-mode-based-on-identity-type)

### <a name="multiple-app-assigned-access-profile-for-one-aad-account-and-one-aad-group"></a>Несколько профилей доступа с назначенным приложением для одной учетной записи AAD и одной группы AAD

:::code language="xml" source="samples/kiosk-sample-multi-app-for-aad-user-and-aad-group.xml" highlight="22-24,52,53,80,91":::

[Назад к списку](#kiosk-xml-code-samples) <br>
Возврат к [поддерживаемым сценариям для режима киоска на основе типа удостоверения](hololens-kiosk.md#supported-scenarios-for-kiosk-mode-based-on-identity-type)

### <a name="multiple-app-assigned-access-profile-for-visitors"></a>Профиль доступа с несколькими приложениями для посетителей

:::code language="xml" source="samples/kiosk-sample-multi-app-visitor-user.xml" highlight="18-20":::

[Назад к списку](#kiosk-xml-code-samples) <br>
Возврат к [поддерживаемым сценариям для режима киоска на основе типа удостоверения](hololens-kiosk.md#supported-scenarios-for-kiosk-mode-based-on-identity-type)
