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
ms.openlocfilehash: d28994d911532a940d82756aa45609571ee80ac3
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112924338"
---
# <a name="page-settings-visibility"></a>Видимость параметров страницы

Одной из управляемых функций для устройств HoloLens является использование [политики Settings/PageVisibilityList](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist) для ограничения страниц, видимых в приложении "Параметры". Политика PageVisibilityList позволяет ИТ-администраторам запрещать отображение или открытие определенных страниц в системном приложении "Параметры" или всех страниц, кроме указанных.

> [!NOTE]
> Эта возможность для устройств HoloLens 2 есть только в ОС [Windows Holographic версии 20H2](hololens-release-notes.md#windows-holographic-version-20h2) и более поздних версий. Обновите устройства, для которых вы собираетесь ее использовать.

В примере ниже показана политика, разрешающая доступ только к страницам сведений и Bluetooth с URI "ms-settings:network-wifi" и "ms-settings:bluetooth", соответственно:
- `showonly:network-wifi;network-proxy;bluetooth`

Чтобы настроить эту политику с помощью пакета подготовки, сделайте следующее:

1. При создании пакета в конструкторе конфигураций Windows откройте раздел **Политики > Параметры > PageVisibilityList**.
1. Введите строку **`showonly:network-wifi;network-proxy;bluetooth`** .
1. Экспортируйте пакет подготовки.
1. Примените этот пакет к устройству.
Подробные сведения о создании и применении пакета подготовки см. на [этой странице](hololens-provisioning.md).

Это можно сделать в Intune с помощью OMA-URI.

1. Создайте **настраиваемую политику**.
1. При настройке OMA-URI используйте строку **`./Device/Vendor/MSFT/Policy/Config/Settings/PageVisibilityList`** .
1. При выборе комплекта данных укажите **Строка**.
1. При вводе значения укажите **`showonly:network-wifi;network-proxy;bluetooth`** .
1. Назначьте настраиваемую конфигурацию устройства группе, в которой должно быть устройство.

Дополнительные сведения о группах и конфигурациях устройств Intune см. в статье [Конфигурация MDM для HoloLens](hololens-mdm-configure.md).

Независимо от выбранного метода ваше устройство теперь будет получать изменения и пользователи получат приложение "Параметры", как показано ниже.

![Снимок экрана: изменение периода активности в приложении "Параметры"](images/hololens-page-visibility-list.jpg)

Чтобы настроить отображение или скрытие выбранных страниц в приложении "Параметры", изучите URI параметров, доступные в HoloLens.

## <a name="settings-uris"></a>URI параметров

Устройства HoloLens и Windows 10 имеют разные наборы страниц в приложении "Параметры". На этой странице приведены только те параметры, которые есть в HoloLens.

### <a name="accounts"></a>Учетные записи
| Страница «Параметры»           | URI                                            |
|-------------------------|------------------------------------------------|
| Доступ к учетной записи места работы или учебного заведения | `ms-settings:workplace`                         |
| Регистрация Iris       | `ms-settings:signinoptions-launchirisenrollment` |
| Параметры входа         | ` ms-settings:signinoptions `                   |

### <a name="apps"></a>Приложения
| Страница «Параметры» | URI                          |
|---------------|------------------------------|
| Приложения и компоненты<sup>2</sup>     | `ms-settings:appsfeatures` <br> |
| Приложения и компоненты > Дополнительные параметры <sup>2</sup>     | `ms-settings::appsfeatures-app` <br> |
| Приложения и компоненты > Автономные карты<sup>2</sup>     | `ms-settings:maps-maps` <br> |
| Приложения и компоненты > Автономные карты > Скачать карты <sup>2</sup>     | `ms-settings:maps-downloadmaps` <br> |

### <a name="devices"></a>Устройства
| Страница «Параметры» | URI                          |
|---------------|------------------------------|
| Bluetooth     | `ms-settings:bluetooth` <br> `ms-settings:connecteddevices` |
| Мышь<sup>2</sup>      | `ms-settings:mouse` <br>  |
| USB<sup>2</sup>      | `ms-settings:usb` <br>  |

### <a name="privacy"></a>Конфиденциальность
| Страница «Параметры»            | URI                                             |
|--------------------------|-------------------------------------------------|
| Сведения об учетной записи             | `ms-settings:privacy-accountinfo`              |
| Диагностика приложений        | `ms-settings:privacy-appdiagnostics`              |
| Фоновые приложения        | `ms-settings:privacy-backgroundapps`              |
| Календарь                 | `ms-settings:privacy-calendar`                    |
| Журнал вызовов             | `ms-settings:privacy-callhistory`                 |
| Камера                   | `ms-settings:privacy-webcam`                      |
| Контакты                 | `ms-settings:privacy-contacts`                    |
| Диагностика и отзывы | `ms-settings:privacy-feedback`                    |
| документы.                | `ms-settings:privacy-documents`                   |
| Электронная почта                    | `ms-settings:privacy-email`                       |
| Файловая система              | `ms-settings:privacy-broadfilesystemaccess`       |
| Общие<sup>2</sup>             | `ms-settings:privacy-general`       |
| Ink & typing personalization (Персонализация рукописного ввода и ввода с клавиатуры)<sup>2</sup>             | `ms-settings:privacy-speechtyping`       |
| Расположение                 | `ms-settings:privacy-location`                    |
| Обмен сообщениями                | `ms-settings:privacy-messaging`                   |
| Микрофон               | `ms-settings:privacy-microphone`                  |
| Движение<sup>2</sup>               | `ms-settings:privacy-motion`                  |
| Уведомления            | `ms-settings:privacy-notifications`               |
| Другие устройства            | `ms-settings:privacy-customdevices`               |
| Изображения                 | `ms-settings:privacy-pictures`                    |
| Радиомодули                   | `ms-settings:privacy-radios`                      |
| Screenshot borders (Границы снимка экрана)<sup>2</sup>             | `ms-settings:privacy-graphicsCaptureWithoutBorder`       |
| Screenshots and apps (Снимки экрана и приложения)<sup>2</sup>             | `ms-settings:privacy-graphicsCaptureProgrammatic`       |
| Речь                   | `ms-settings:privacy-speech`                      |
| Задания                    | `ms-settings:privacy-tasks`                       |
| Движения пользователей           | `ms-settings:privacy-backgroundspatialperception` |
| Видео                   | `ms-settings:privacy-videos`                      |
| Голосовая активация       | `ms-settings:privacy-voiceactivation`             |

### <a name="network--internet"></a>Сеть и Интернет
| Страница «Параметры» | URI                              |
|---------------|----------------------------------|
| Режим "в самолете"<sup>2</sup> | `ms-settings:network-airplanemode`        |
| Proxy (Прокси) | `ms-settings:network-proxy`        |
| VPN   | `ms-settings:network-vpn`          |
| Wi-Fi  | `ms-settings:network-wifi`<br>`ms-settings:network-wifisettings`<br>`ms-settings:network-status`<br>`ms-settings:wifi-provisioning`    |



### <a name="system"></a>Система
| Страница «Параметры»      | URI                                |
|--------------------|------------------------------------|
| Аккумулятор<sup>2</sup>           | `ms-settings:batterysaver`<br>|
| Аккумулятор<sup>2</sup>           | `ms-settings:batterysaver-settings`<br>|
| Цвета             | `ms-settings:colors`<br>`ms-settings:personalization-colors` |
| Голограммы<sup>2</sup>  |  `ms-settings:holograms`  |
| Калибровка<sup>2</sup> |  `ms-settings:calibration` |
| Уведомления и действия  | `ms-settings:notifications`          |
| Общие возможности | `ms-settings:crossdevice` 
| Звук<sup>2</sup>           | `ms-settings:sound`<br>|
| Звук > App volume and device preference (Громкость приложений и параметры устройства)<sup>2</sup>           | `ms-settings:apps-volume`<br>|
| Звук > Manage sound devices (Управление звуковыми устройствами)<sup>2</sup>           | `ms-settings:sound-devices`<br>|
| Память            | `ms-settings:storagesense`           |
| Память > Configure Storage Sense (Настройка контроля памяти)<sup>2</sup>           | `ms-settings:storagepolicies`<br>|

### <a name="time--language"></a>Время и язык
| Страница «Параметры» | URI                                           |
|---------------|-----------------------------------------------|
| Дата и время<sup>2</sup> | `ms-settings:dateandtime`                  |
| Клавиатура<sup>2</sup> | `ms-settings:keyboard`                  |
| Язык<sup>2</sup> | `ms-settings:language`                  |
| Язык<sup>2</sup> | `ms-settings:regionlanguage-languageoptions`                  |
| Язык      | `ms-settings:regionlanguage`<br>`ms-settings:regionlanguage-adddisplaylanguage`<br>`ms-settings:regionlanguage-setdisplaylanguage` |
| Регион        | `ms-settings:regionformatting`                  |

### <a name="update--security"></a>Обновление и безопасность
| Страница «Параметры»                         | URI                                       |
|---------------------------------------|-------------------------------------------|
| Дополнительные параметры                    | `ms-settings:windowsupdate-options`         |
| Сброс и восстановление <sup>2</sup>      | `ms-settings:reset`         |
| Программа предварительной оценки Windows               | `ms-settings:windowsinsider` <br>`ms-settings:windowsinsider-optin`          |
| Центр обновления Windows                        | `ms-settings:windowsupdate`<br> `ms-settings:windowsupdate-activehours`  <br> `ms-settings:windowsupdate-history` <br> `ms-settings:windowsupdate-optionalupdates` <br><sup>1</sup>`ms-settings:windowsupdate-options`<br><sup>1</sup>`ms-settings:windowsupdate-restartoptions` |
| Центр обновления Windows — проверка наличия обновлений | `ms-settings:windowsupdate-action`          |


- <sup>1</sup> — Для версий Windows Holographic старше 21H1 следующие два URI не перенаправляют на страницы **Дополнительные возможности** или **Параметры**, а только блокируют или отображают основную страницу Центра обновления Windows.
  -  ms-settings:windowsupdate-options
  -  ms-settings:windowsupdate-restartoptions

- <sup>2</sup> — доступно в Windows Holographic версии 21H1 и выше.


Полный список URI параметров для Windows 10 см. в документации по [параметрам запуска](https://docs.microsoft.com/windows/uwp/launch-resume/launch-settings-app#ms-settings-uri-scheme-reference).
