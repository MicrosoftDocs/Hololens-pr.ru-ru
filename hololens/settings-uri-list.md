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
ms.openlocfilehash: f004f39f4b69748e8c36ad93111f4423d14c40f3
ms.sourcegitcommit: 23ee06b659d7a51f3000d386c8f67cbf212d5aa4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "11327393"
---
# Видимость параметров страницы

Одной из управляемых функций для устройств HoloLens является использование [политики Settings/PageVisibilityList](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist), чтобы ограничивать страницы, отображаемые в приложении "Параметры". PageVisibilityList — это политика, позволяющая ИТ-администраторам запрещать отображение или открытие определенных страниц в приложении "Параметры системы" или наоборот — выполнять это для всех страниц, кроме указанных.

> [!NOTE]
> Эта функция доступна только в [Windows Holographic версии 20H2](hololens-release-notes.md#windows-holographic-version-20h2) для устройств HoloLens 2. Обновите устройства, для которых вы собираетесь ее использовать.

> [!NOTE]
> В ближайшее время будут добавлены более 20 новых параметров SettingsURI. Если вы хотите просмотреть этот параметр в предварительной сборке [HoloLens](hololens-insider.md), посетите страницу [Программа предварительной оценки Windows — Новые параметры SettingsURI для видимости параметров страницы](hololens-insider.md#new-settingsuris-for-page-settings-visibility).

В примере ниже показана политика, разрешающая доступ только к страницам сведений и Bluetooth с URI "ms-settings:network-wifi" и "ms-settings:bluetooth" соответственно:
- `showonly:network-wifi;network-proxy;bluetooth`

Чтобы настроить эту политику с помощью пакета подготовки, выполните следующее.

1. При создании пакета в конструкторе конфигураций Windows выберите **Политики > Параметры > PageVisibilityList**
1. Введите строку: **`showonly:network-wifi;network-proxy;bluetooth`**
1. Экспортируйте пакет подготовки.
1. Примените пакет к устройству.
Подробные сведения о создании и применении пакета подготовки см. на [этой странице](hololens-provisioning.md).

Это можно сделать с помощью Intune с использованием OMA-URI.

1. Создайте **пользовательскую политику**.
1. При настройке OMA-URI используйте строку: **`./Device/Vendor/MSFT/Policy/Config/Settings/PageVisibilityList`**
1. При выборе комплекта данных укажите: **Строка**
1. При вводе значения используйте: **`showonly:network-wifi;network-proxy;bluetooth`**
1. Назначьте настраиваемую конфигурацию устройства группе, в которой должно располагаться устройство.

Дополнительные сведения о группах Intune и конфигурации устройств см. в статье [Конфигурация HoloLens в MDM](hololens-mdm-configure.md).

Независимо от выбранного метода ваше устройство должно теперь получать изменения, а пользователи получат следующее приложение "Параметры".

![Снимок экрана: период активности, измененный в приложении "Параметры"](images/hololens-page-visibility-list.jpg)

Чтобы настроить страницы приложения "Параметры" для отображения или скрытия выбранных страниц, просмотрите URI параметров, доступные в HoloLens.

## URI параметров

Устройства HoloLens и Windows 10 имеют разный выбор страниц в приложении "Параметры". На этой странице приведены только параметры, существующие в HoloLens.

### Учетные записи
| Страница параметров           | URI                                            |
|-------------------------|------------------------------------------------|
| Параметры входа         | ` ms-settings:signinoptions `                   |
| Регистрация Iris       | `ms-settings:signinoptions-launchirisenrollment` |
| Доступ на рабочем месте или в учебном учреждении | `ms-settings:workplace`                         |

### Устройства
| Страница параметров | URI                          |
|---------------|------------------------------|
| Bluetooth     | `ms-settings:bluetooth` <br> `ms-settings:connecteddevices` |

### Конфиденциальность
| Страница параметров            | URI                                             |
|--------------------------|-------------------------------------------------|
| Сведения об учетной записи             | `ms-settings:privacy-accountinfo`              |
| Диагностика приложений        | `ms-settings:privacy-appdiagnostics`              |
| Фоновые приложения        | `ms-settings:privacy-backgroundapps`              |
| Движения пользователей           | `ms-settings:privacy-backgroundspatialperception` |
| Файловая система              | `ms-settings:privacy-broadfilesystemaccess`       |
| Календарь                 | `ms-settings:privacy-calendar`                    |
| Журнал вызовов             | `ms-settings:privacy-callhistory`                 |
| Контакты                 | `ms-settings:privacy-contacts`                    |
| Другие устройства            | `ms-settings:privacy-customdevices`               |
| Документы                | `ms-settings:privacy-documents`                   |
| Электронная почта                    | `ms-settings:privacy-email`                       |
| Диагностика и отзывы | `ms-settings:privacy-feedback`                    |
| Расположение                 | `ms-settings:privacy-location`                    |
| Сообщения                | `ms-settings:privacy-messaging`                   |
| Микрофон               | `ms-settings:privacy-microphone`                  |
| Уведомления            | `ms-settings:privacy-notifications`               |
| Изображения                 | `ms-settings:privacy-pictures`                    |
| Радиомодули                   | `ms-settings:privacy-radios`                      |
| Речь                   | `ms-settings:privacy-speech`                      |
| Задачи                    | `ms-settings:privacy-tasks`                       |
| Видео                   | `ms-settings:privacy-videos`                      |
| Голосовая активация       | `ms-settings:privacy-voiceactivation`             |
| Камера                   | `ms-settings:privacy-webcam`                      |

### Сеть и Интернет
| Страница параметров | URI                              |
|---------------|----------------------------------|
| Wi-Fi  | `ms-settings:network-wifi`<br>`ms-settings:network-wifisettings`<br>`ms-settings:network-status`<br>`ms-settings:wifi-provisioning`    |
| VPN   | `ms-settings:network-vpn`          |
| Прокси-сервер | `ms-settings:network-proxy`        |

### Система
| Страница параметров      | URI                                |
|--------------------|------------------------------------|
| Общие возможности | `ms-settings:crossdevice`            |
| Цвета             | `ms-settings:colors`<br>`ms-settings:personalization-colors` |
| Уведомления и действия  | `ms-settings:notifications`          |
| Хранилище            | `ms-settings:storagesense`           |

### Время и язык
| Страница параметров | URI                                           |
|---------------|-----------------------------------------------|
| Region        | `ms-settings:regionformatting`                  |
| Язык      | `ms-settings:regionlanguage`<br>`ms-settings:regionlanguage-adddisplaylanguage`<br>`ms-settings:regionlanguage-setdisplaylanguage` |

### Обновление и безопасность
| Страница параметров                         | URI                                       |
|---------------------------------------|-------------------------------------------|
| Программа предварительной оценки Windows               | `ms-settings:windowsinsider` <br>`ms-settings:windowsinsider-optin`          |
| Центр обновления Windows                        | `ms-settings:windowsupdate`<br> `ms-settings:windowsupdate-activehours`  <br> `ms-settings:windowsupdate-history` <br> `ms-settings:windowsupdate-optionalupdates` <br><sup>1</sup>`ms-settings:windowsupdate-options`<br><sup>1</sup>`ms-settings:windowsupdate-restartoptions` |
| Центр обновления Windows — проверка наличия обновлений | `ms-settings:windowsupdate-action`          |
| Дополнительные параметры                    | `ms-settings:windowsupdate-options`         |

>  <sup>1</sup> Следующие два URI не отправляют вас на страницы **Расширенные параметры** или **Параметры**. Они только блокируют или отображают основную страницу Центра обновления Windows.
> - ms-settings:windowsupdate-options
> - ms-settings:windowsupdate-restartoptions 

Полный список URI параметров Windows 10 см. в документации по [параметрам запуска](https://docs.microsoft.com/windows/uwp/launch-resume/launch-settings-app#ms-settings-uri-scheme-reference).
