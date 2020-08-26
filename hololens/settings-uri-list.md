---
title: URI параметров
description: Список поддерживаемых HoloLens URI для PageVisibilityList
author: evmill
ms.author: v-evmill
ms.date: 8/1/2020
ms.topic: article
keywords: hololens, hololens 2, ограниченный доступ, терминал, страница параметров
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: widuff
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 6b506b36915c8f34b90c455410db67e55a2cca09
ms.sourcegitcommit: 7f48e7103f869a22a0d20a54dc8f9b708b22484c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2020
ms.locfileid: "10963722"
---
# URI параметров

Одной из управляемых функций для устройств HoloLens является использование [политики Settings/PageVisibilityList](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist), чтобы ограничивать страницы, отображаемые в приложении "Параметры". Устройства HoloLens и Windows 10 имеют разный выбор страниц в приложении "Параметры". На этой странице вы найдете только параметры, существующие в HoloLens. 

## Учетные записи
| Страница параметров           | URI                                            |
|-------------------------|------------------------------------------------|
| Параметры входа         | ms-settings:signinoptions                      |
| Регистрация Iris       | ms-settings:signinoptions-launchirisenrollment |
| Доступ на рабочем месте или в учебном учреждении | ms-settings:workplace                          |

## Устройства
| Страница параметров | URI                          |
|---------------|------------------------------|
| Bluetooth     | ms-settings:bluetooth <br> ms-settings:connecteddevices |

## Конфиденциальность
| Страница параметров            | URI                                             |
|--------------------------|-------------------------------------------------|
| Сведения об учетной записи             | ms-settings:privacy-accountinfo                 |
| Диагностика приложений        | ms-settings:privacy-appdiagnostics              |
| Фоновые приложения        | ms-settings:privacy-backgroundapps              |
| Движения пользователей           | ms-settings:privacy-backgroundspatialperception |
| Файловая система              | ms-settings:privacy-broadfilesystemaccess       |
| Календарь                 | ms-settings:privacy-calendar                    |
| Журнал вызовов             | ms-settings:privacy-callhistory                 |
| Контакты                 | ms-settings:privacy-contacts                    |
| Другие устройства            | ms-settings:privacy-customdevices               |
| Документы                | ms-settings:privacy-documents                   |
| Электронная почта                    | ms-settings:privacy-email                       |
| Диагностика и отзывы | ms-settings:privacy-feedback                    |
| Location                 | ms-settings:privacy-location                    |
| Сообщения                | ms-settings:privacy-messaging                   |
| Микрофон               | ms-settings:privacy-microphone                  |
| Уведомления            | ms-settings:privacy-notifications               |
| Изображения                 | ms-settings:privacy-pictures                    |
| Радиомодули                   | ms-settings:privacy-radios                      |
| Речь                   | ms-settings:privacy-speech                      |
| Задачи                    | ms-settings:privacy-tasks                       |
| Видео                   | ms-settings:privacy-videos                      |
| Голосовая активация       | ms-settings:privacy-voiceactivation             |
| Камера                   | ms-settings:privacy-webcam                      |

## Сеть и Интернет
| Страница параметров | URI                              |
|---------------|----------------------------------|
| Wi-Fi  | ms-settings:network-wifi<br>ms-settings:network-wifisettings<br>ms-settings:network-status<br>ms-settings:wifi-provisioning    |
| VPN   | ms-settings:network-vpn          |
| Proxy (Прокси) | ms-settings:network-proxy        |

## Система
| Страница параметров      | URI                                |
|--------------------|------------------------------------|
| Общие возможности | ms-settings:crossdevice            |
| Цвета             | ms-settings:colors<br>ms-settings:personalization-colors |
| Уведомления и действия  | ms-settings:notifications          |
| Хранилище            | ms-settings:storagesense           |

## Время и язык
| Страница параметров | URI                                           |
|---------------|-----------------------------------------------|
| Region        | ms-settings:regionformatting                  |
| Язык      | ms-settings:regionlanguage<br>ms-settings:regionlanguage-adddisplaylanguage<br>ms-settings:regionlanguage-setdisplaylanguage |

## Обновление и безопасность
| Страница параметров                         | URI                                       |
|---------------------------------------|-------------------------------------------|
| Программа предварительной оценки Windows               | ms-settings:windowsinsider <br>ms-settings:windowsinsider-optin          |
| Центр обновления Windows                        | ms-settings:windowsupdate<br> ms-settings:windowsupdate-activehours  <br> ms-settings:windowsupdate-history <br> ms-settings:windowsupdate-optionalupdates <br><sup>1</sup>ms-settings:windowsupdate-options<br><sup>1</sup>ms-settings:windowsupdate-restartoptions |
| Центр обновления Windows — проверка наличия обновлений | ms-settings:windowsupdate-action          |
| Дополнительные параметры                    | ms-settings:windowsupdate-options         |

> [!NOTE]
>  1 Следующие два URI не отправляют вас на страницу расширенных параметров или на страницу обычных параметров. Они только блокируют или отображают основную страницу Центра обновления Windows. 
> - ms-settings:windowsupdate-options
> - ms-settings:windowsupdate-restartoptions 

Полный список URI параметров Windows 10 см. [здесь](https://docs.microsoft.com/windows/uwp/launch-resume/launch-settings-app#ms-settings-uri-scheme-reference). 
