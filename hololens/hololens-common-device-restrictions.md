---
title: Общие ограничения устройств
description: Restrctions устройства обычно устанавливаются на HoloLens.
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
ms.openlocfilehash: 744d54a344867c5c38681781580f5357e0a0da70
ms.sourcegitcommit: 108b818130e2627bf08107f4e47ae159dd6ab1d2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "11162961"
---
# Общие ограничения устройств 

Это руководство поможет ИТ-специалистам понять наиболее распространенные параметры управления, доступные для ОС Windows 10 holographic в масштабах предприятия. Изучите документацию по системе MDM, чтобы понять, каким образом данные политики реализуются вашим поставщиком MDM. Не все системы MDM поддерживают все настройки, описанные в данном руководстве. Некоторые поддерживают пользовательские политики посредством XML-файлов OMA-URI. См. раздел [Поддержка пользовательских политик Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-settings-windows-10). Различные поставщики MDM также могут использовать различные соглашения об именовании.

## Запрет на изменение параметров
Сотрудникам, как правило, разрешено изменять на персональном устройстве определенные параметры, изменение которых на корпоративных устройствах рекомендуется запретить. Сотрудники могут настраивать определенные параметры HoloLens через пользовательский интерфейс параметров. С помощью MDM можно ограничить изменения, которые могут вносить пользователи. Ниже перечислены часто используемые параметры MDM, которые поддерживаются в Windows 10 holographic для настройки ограничений на параметры.
-   [Разрешить VPN:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn) Позволяет пользователю изменить параметры VPN.
-   [Разрешить конфигурацию WiFi вручную:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration) Разрешает пользователям выполнять Wi-Fi подключений за пределами преднастроенных сетей MDM
-   [Разрешить отмену регистрации в MDM вручную](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment) Разрешено ли пользователям удалять учетную запись рабочего места (например, отменить регистрацию устройства в системе MDM)

Добавлено в [Windows holographic версии 20H2](hololens-release-notes.md#windows-holographic-version-20h2) для устройств HoloLens 2:
- [Разрешить добавление пакета подготовки:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage) Переключение, если пользователи могут добавлять новые пакеты подготовки, переписывая новые значения.
- [Разрешить удаление пакета подготовки:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage) Переключите, если пользователи могут удалять пакеты подготовки, разрешая им переключать ранее заблокированные параметры.

Дополнительные сведения о параметрах политики в [cspх](https://docs.microsoft.com/windows/client-management/mdm/policy-csps-supported-by-hololens2) , поддерживаемых HoloLens

## Аппаратные ограничения
Устройства с Windows 10 holographic используют встроенную технологию, которая включает в себя популярные аппаратные функции, такие как камеры, микрофоны, динамики, интерфейсы USB, интерфейсы Bluetooth и Wi-Fi. Аппаратные ограничения также можно использовать, чтобы контролировать доступность этих функций.
Ниже перечислены типичные параметры MDM, которые поддерживаются в Windows 10 holographic для настройки аппаратных ограничений.

> [!NOTE]
> Некоторые из этих ограничений оборудования влияют на связь и способствуют защите данных.

-   [Разрешить Wi-Fi:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi) Могут ли пользователи включать и использовать радиомодульы Wi-Fi на своих устройствах.
-   [Разрешить USB-подключение:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowusbconnection) Включено ли USB-подключение (не влияет на зарядку USB-портов).
-   [Разрешить Bluetooth:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth) Могут ли пользователи включать и использовать радиомодуль Bluetooth на своих устройствах.
-   [Ограничить камеру:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera) Указывает, могут ли приложения для Windows получать доступ к камере.
-   [Ограничить Микрофоны:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone) Указывает, могут ли приложения для Windows получать доступ к микрофону.

Добавлено в [Windows holographic, Verison 20H2](hololens-release-notes.md#windows-holographic-version-20h2) для устройств HoloLens 2. 
- [DisplayOffTimeoutOnBattery](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery) Установите время, по истечении которого монитор выключается, и отключая экран, блокирует устройство. 
- [DisplayOffTimeoutPluggedIn](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin) Установите время, по истечении которого монитор выключается, и отключая экран, блокирует устройство. 
