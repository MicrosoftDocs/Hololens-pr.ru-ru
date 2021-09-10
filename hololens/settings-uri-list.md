---
title: Видимость параметров страницы
description: Ознакомьтесь с нашим списком поддерживаемых URI для PageVisibilityList и руководством по устройствам смешанной реальности HoloLens.
author: evmill
ms.author: v-evmill
ms.date: 10/13/2020
ms.topic: article
keywords: hololens, hololens 2, ограниченный доступ, терминал, страница параметров
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: widuff
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 92040019b093c5ef63d74f095dcb3809112ae7a0
ms.sourcegitcommit: f04f631fbe7798a82a57cc01fc56dc2edf13c5f2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/30/2021
ms.locfileid: "123190435"
---
# <a name="page-settings-visibility"></a>Видимость параметров страницы

Одной из управляемых функций для устройств HoloLens является использование [политики Settings/PageVisibilityList](/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist) для ограничения страниц, видимых в приложении "Параметры". Политика PageVisibilityList позволяет ИТ-администраторам запрещать отображение или открытие определенных страниц в системном приложении "Параметры" или всех страниц, кроме указанных.

> [!NOTE]
> Эта возможность для устройств HoloLens 2 есть только в ОС [Windows Holographic версии 20H2](hololens-release-notes.md#windows-holographic-version-20h2) и более поздних версий. Обновите устройства, для которых вы собираетесь ее использовать.


## <a name="examples"></a>Примеры
Страницы идентифицируются по сокращенной версии опубликованного URI (за вычетом префикса "ms-settings:").

В примере ниже показана политика, разрешающая доступ только к страницам сведений и Bluetooth с URI "network-wifi" и "bluetooth" соответственно:
- `showonly:network-wifi;network-proxy;bluetooth`

В следующем примере показана политика, которая скрывает страницу сброса операционной системы:
- `hide:reset`


## <a name="deploying-this-policy-via-intune"></a>Развертывание этой политики с помощью Intune

Это значения параметров конфигурации, которые будут переданы в Intune:

- **Имя:** предпочитаемое отображаемое имя администратора для профиля.
- **URI OMA:** полный URI страницы параметров, включая ее [область](/windows/client-management/mdm/policy-configuration-service-provider). В этом примере на этой странице используется область `./Device`.
- **Значение:** строковое значение, указывающее, следует ли скрывать или отображать *только* указанные страницы. Возможные значения: `hide:<pagename>` и `showonly:<pagename>`. 
 
Можно указать несколько страниц, разделив их точками с запятой. Список основных страниц можно найти ниже.

1. Создайте **настраиваемую политику**.
1. При указании **URI OMA** введите URI с полной областью. Например: **`./Device/Vendor/MSFT/Policy/Config/Settings/PageVisibilityList`**
1. При выборе комплекта данных укажите **Строка**.
1. При указании **Значения** используйте приведенные выше рекомендации. Например: **`showonly:network-wifi;network-proxy;bluetooth`** или **`hide:reset`** 
> [!IMPORTANT]
> Назначьте настраиваемую конфигурацию устройства группе, в которой должно быть устройство. Если этот шаг не выполнен, политика будет отправлена, но не будет применена.

Дополнительные сведения о группах и конфигурациях устройств Intune см. в статье [Конфигурация MDM для HoloLens](hololens-mdm-configure.md).


## <a name="deploying-this-policy-via-a-provisioning-package"></a>Развертывание этой политики с помощью пакета подготовки

Это значения параметров конфигурации, которые будут указаны в Конструкторе конфигураций Windows:

**Значение:** строковое значение, указывающее, следует ли скрывать или отображать *только* указанные страницы. Возможные значения: `hide:<pagename>` и `showonly:<pagename>`. Можно указать несколько страниц, разделив их точками с запятой. Список основных страниц можно найти ниже.


1. При создании пакета в конструкторе конфигураций Windows откройте раздел **Политики > Параметры > PageVisibilityList**.
1. Введите строку **`showonly:network-wifi;network-proxy;bluetooth`** .
1. Экспортируйте пакет подготовки.
1. Примените этот пакет к устройству.
Подробные сведения о том, как создать и применить пакет подготовки, см. на [странице подготовки HoloLens](hololens-provisioning.md).


Независимо от выбранного метода ваше устройство теперь будет получать изменения и пользователи получат приложение "Параметры", как показано ниже.

![Снимок экрана: изменение периода активности в приложении "Параметры".](images/hololens-page-visibility-list.jpg)

Чтобы настроить отображение или скрытие выбранных страниц в приложении "Параметры", изучите URI параметров, доступные в HoloLens.

## <a name="settings-uris"></a>URI параметров

Устройства HoloLens и Windows 10 имеют разные наборы страниц в приложении "Параметры". На этой странице приведены только те параметры, которые есть в HoloLens.

### <a name="accounts"></a>Учетные записи
| Страница «Параметры»           | URI                                            |
|-------------------------|------------------------------------------------|
| Доступ к учетной записи места работы или учебного заведения | `workplace`                         |
| Регистрация Iris       | `signinoptions-launchirisenrollment` |
| Параметры входа         | ` signinoptions `                   |

### <a name="apps"></a>Приложения
| Страница «Параметры» | URI                          |
|---------------|------------------------------|
| Приложения и компоненты <sup>2</sup>     | `appsfeatures` <br> |
| Приложения и компоненты > Дополнительные параметры <sup>2</sup>     | `appsfeatures-app` <br> |
| Приложения и компоненты > Автономные карты<sup>2</sup>     | `maps-maps` <br> |
| Приложения и компоненты > Автономные карты > Скачать карты <sup>2</sup>     | `maps-downloadmaps` <br> |

### <a name="devices"></a>Устройства
| Страница «Параметры» | URI                          |
|---------------|------------------------------|
| Bluetooth     | `bluetooth` <br> `connecteddevices` |
| Мышь<sup>2</sup>      | `mouse` <br>  |
| USB<sup>2</sup>      | `usb` <br>  |

### <a name="privacy"></a>Конфиденциальность
| Страница «Параметры»            | URI                                             |
|--------------------------|-------------------------------------------------|
| Сведения об учетной записи             | `privacy-accountinfo`              |
| Диагностика приложений        | `privacy-appdiagnostics`              |
| Фоновые приложения        | `privacy-backgroundapps`              |
| Календарь                 | `privacy-calendar`                    |
| Журнал вызовов             | `privacy-callhistory`                 |
| Камера                   | `privacy-webcam`                      |
| Контакты                 | `privacy-contacts`                    |
| Диагностика и отзывы | `privacy-feedback`                    |
| документы.                | `privacy-documents`                   |
| Электронная почта                    | `privacy-email`                       |
| Файловая система              | `privacy-broadfilesystemaccess`       |
| Общие<sup>2</sup>             | `privacy-general`       |
| Ink & typing personalization (Персонализация рукописного ввода и ввода с клавиатуры)<sup>2</sup>             | `privacy-speechtyping`       |
| Расположение                 | `privacy-location`                    |
| Обмен сообщениями                | `privacy-messaging`                   |
| Микрофон               | `privacy-microphone`                  |
| Движение<sup>2</sup>               | `privacy-motion`                  |
| Уведомления            | `privacy-notifications`               |
| Другие устройства            | `privacy-customdevices`               |
| Изображения                 | `privacy-pictures`                    |
| Радиомодули                   | `privacy-radios`                      |
| Screenshot borders (Границы снимка экрана)<sup>2</sup>             | `privacy-graphicsCaptureWithoutBorder`       |
| Screenshots and apps (Снимки экрана и приложения)<sup>2</sup>             | `privacy-graphicsCaptureProgrammatic`       |
| Речь                   | `privacy-speech`                      |
| Задания                    | `privacy-tasks`                       |
| Движения пользователей           | `privacy-backgroundspatialperception` |
| Видео                   | `privacy-videos`                      |
| Голосовая активация       | `privacy-voiceactivation`             |

### <a name="network--internet"></a>Сеть и Интернет
| Страница «Параметры» | URI                              |
|---------------|----------------------------------|
| Режим "в самолете"<sup>2</sup> | `network-airplanemode`        |
| Proxy (Прокси) | `network-proxy`        |
| VPN   | `network-vpn`          |
| Wi-Fi  | `network-wifi`<br>`network-wifisettings`<br>`network-status`<br>`wifi-provisioning`    |



### <a name="system"></a>Система
| Страница «Параметры»      | URI                                |
|--------------------|------------------------------------|
| Аккумулятор<sup>2</sup>           | `batterysaver`<br>|
| Аккумулятор<sup>2</sup>           | `batterysaver-settings`<br>|
| Цвета             | `colors`<br>`personalization-colors` |
| Голограммы<sup>2</sup>  |  `holograms`  |
| Калибровка<sup>2</sup> |  `calibration` |
| Уведомления и действия  | `notifications`          |
| Общие возможности | `crossdevice` 
| Звук<sup>2</sup>           | `sound`<br>|
| Звук > App volume and device preference (Громкость приложений и параметры устройства)<sup>2</sup>           | `apps-volume`<br>|
| Звук > Manage sound devices (Управление звуковыми устройствами)<sup>2</sup>           | `sound-devices`<br>|
| Память            | `storagesense`           |
| Память > Configure Storage Sense (Настройка контроля памяти)<sup>2</sup>           | `storagepolicies`<br>|

### <a name="time--language"></a>Время и язык
| Страница «Параметры» | URI                                           |
|---------------|-----------------------------------------------|
| Дата и время<sup>2</sup> | `dateandtime`                  |
| Клавиатура<sup>2</sup> | `keyboard`                  |
| Язык<sup>2</sup> | `language`                  |
| Язык<sup>2</sup> | `regionlanguage-languageoptions`                  |
| Язык      | `regionlanguage`<br>`regionlanguage-adddisplaylanguage`<br>`regionlanguage-setdisplaylanguage` |
| Регион        | `regionformatting`                  |

### <a name="update--security"></a>Обновление и безопасность
| Страница «Параметры»                         | URI                                       |
|---------------------------------------|-------------------------------------------|
| Дополнительные параметры                    | `windowsupdate-options`         |
| Сброс и восстановление <sup>2</sup>      | `reset`         |
| Программа предварительной оценки Windows               | `windowsinsider` <br>`windowsinsider-optin`          |
| Центр обновления Windows                        | `windowsupdate`<br> `windowsupdate-activehours`  <br> `windowsupdate-history` <br> `windowsupdate-optionalupdates` <br><sup>1</sup>`windowsupdate-options`<br><sup>1</sup>`windowsupdate-restartoptions` |
| Центр обновления Windows — проверка наличия обновлений | `windowsupdate-action`          |


- <sup>1</sup> — Для версий Windows Holographic старше 21H1 следующие два URI не перенаправляют на страницы **Дополнительные возможности** или **Параметры**, а только блокируют или отображают основную страницу Центра обновления Windows.
  -  windowsupdate-options
  -  windowsupdate-restartoptions

- <sup>2</sup> — доступно в Windows Holographic версии 21H1 и выше.


Полный список URI параметров для Windows 10 см. в документации по [параметрам запуска](/windows/uwp/launch-resume/launch-settings-app#ms-settings-uri-scheme-reference).
