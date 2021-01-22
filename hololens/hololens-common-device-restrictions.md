---
title: Общие ограничения устройств
description: Следите в курсе распространенных ограничений и параметров устройства смешанной реальности HoloLens.
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: v-evmill
ms.topic: article
ms.localizationpriority: medium
ms.date: 10/13/2020
ms.reviewer: ''
manager: yannisle
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: e9c44466da375611f8864eae1b6e6ceea3ef9b09
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283360"
---
# Общие ограничения устройств 

Это руководство поможет ИТ-специалистам понять, какие наиболее часто используемые варианты управления доступны для Ос Windows 10 Holographic OS на предприятии. Изучите документацию по системе MDM, чтобы понять, каким образом данные политики реализуются вашим поставщиком MDM. Не все системы MDM поддерживают все настройки, описанные в данном руководстве. Некоторые поддерживают пользовательские политики посредством XML-файлов OMA-URI. См. раздел [Поддержка пользовательских политик Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-settings-windows-10). Различные поставщики MDM также могут использовать различные соглашения об именовании.

## Запрет на изменение параметров
Сотрудникам, как правило, разрешено изменять на персональном устройстве определенные параметры, изменение которых на корпоративных устройствах рекомендуется запретить. Сотрудники могут интерактивно настраивать определенные параметры HoloLens с помощью пользовательского интерфейса параметров. С помощью MDM можно ограничить изменения, которые могут вносить пользователи. Ниже перечислены часто используемые параметры MDM, поддерживаемые Windows 10 Holographic для настройки ограничений параметров.
-   [Разрешить VPN:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn) Позволяет пользователю изменять параметры VPN
-   [Разрешить ручную настройку Wi-Fi:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration) Позволяет пользователям использовать Wi-Fi подключения за пределами сетей, в которые есть MDM
-   [Разрешить ручную открепление MDM](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment) Разрешено ли пользователям удалять рабочая учетная запись (т. е. отопустить устройство из системы MDM)

Добавлено [в Windows Holographic версии 20H2](hololens-release-notes.md#windows-holographic-version-20h2) для устройств HoloLens 2:
- [Разрешить добавление пакета предоставления:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage) Переупакуйте, если пользователи могут добавлять новые пакеты, переоценив новые значения.
- [Разрешить удаление пакета предоставления:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage) Перенимайте, могут ли пользователи удалять пакеты подготовка, позволяя им перегнастраить ранее заблокированные параметры.

Дополнительные сведения о параметрах политики можно найти в поддерживаемых [CPS политики](https://docs.microsoft.com/windows/client-management/mdm/policy-csps-supported-by-hololens2) HoloLens

## Аппаратные ограничения
Устройства с Windows 10 Holographic используют современные технологии, которые включают популярные аппаратные функции, такие как камеры, микрофоны, динамики, интерфейсы USB, интерфейсы Bluetooth и Wi-Fi. Аппаратные ограничения также можно использовать, чтобы контролировать доступность этих функций.
Ниже перечислены часто используемые параметры MDM, поддерживаемые Windows 10 Holographic для настройки аппаратных ограничений.

> [!NOTE]
> Некоторые из этих аппаратных ограничений влияют на возможность подключения и помогают в защите данных.

-   [Разрешить Wi-Fi:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi) Возможность пользователей включить и использовать радио Wi-Fi на своих устройствах.
-   [Разрешить USB-подключение:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowusbconnection) Включено ли USB-подключение (не влияет на зарядку USB).)
-   [Разрешить Bluetooth:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth) Возможность пользователей включить и использовать Bluetooth на своих устройствах.
-   [Ограничение камеры:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera) Указывает, могут ли приложения для Windows получать доступ к камере.
-   [Ограничить микрофоны:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone) Указывает, могут ли приложения для Windows получать доступ к микрофону.

Добавлено [в Windows Holographic, verison 20H2 для](hololens-release-notes.md#windows-holographic-version-20h2) устройств HoloLens 2. 
- [DisplayOffTimeoutOnBattery](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery) Установите время до отключения дисплея и, отключив дисплей, заблокировать устройство. 
- [DisplayOffTimeoutPluggedIn](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin) Установите время до отключения дисплея и, отключив дисплей, заблокировать устройство. 
