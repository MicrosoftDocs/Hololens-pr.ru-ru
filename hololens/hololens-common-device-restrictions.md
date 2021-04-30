---
title: Общие ограничения для устройств
description: Получайте актуальные сведения об общих ограничениях и параметрах устройств для устройства "смешанная реальность".
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
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309087"
---
# <a name="common-device-restrictions"></a>Общие ограничения для устройств 

Это руководство поможет ИТ-специалистам понять наиболее часто используемые возможности управления, доступные для ОС Windows 10 holographic на предприятии. Изучите документацию по системе MDM, чтобы понять, каким образом данные политики реализуются вашим поставщиком MDM. Не все системы MDM поддерживают все настройки, описанные в данном руководстве. Некоторые поддерживают пользовательские политики посредством XML-файлов OMA-URI. См. раздел [Поддержка пользовательских политик Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-settings-windows-10). Различные поставщики MDM также могут использовать различные соглашения об именовании.

## <a name="prevent-changing-of-settings"></a>Запрет на изменение параметров
Сотрудникам, как правило, разрешено изменять на персональном устройстве определенные параметры, изменение которых на корпоративных устройствах рекомендуется запретить. Сотрудники могут в интерактивном режиме настраивать определенные параметры HoloLens через пользовательский интерфейс параметров. С помощью MDM можно ограничить изменения, которые могут вносить пользователи. Ниже перечислены часто используемые параметры MDM, поддерживаемые Windows 10 holographic для настройки ограничений для параметров.
-   [Разрешить VPN:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn) Разрешает пользователю изменять параметры VPN
-   [Разрешить ручную настройку WiFi:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration) Разрешает пользователям устанавливать Wi-Fi подключения за пределами подготовленных сетей MDM
-   [Разрешить отмену регистрации MDM вручную](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment) Разрешено ли пользователям удалять учетную запись рабочей области (т. е. отменить регистрацию устройства в системе MDM);

Добавлено в [Windows holographic, версия 20H2](hololens-release-notes.md#windows-holographic-version-20h2) для устройств HoloLens 2:
- [Разрешить добавление пакета подготовки:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage) Переключите, если пользователи могут добавлять новые пакеты подготовки, перезаписывая их новыми значениями.
- [Разрешить удаление пакета подготовки:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage) Установите переключатель, если пользователи могут удалять пакеты подготовки, что позволяет им переключать ранее заблокированные параметры.

Дополнительные сведения о параметрах политики в [CSP поддерживаемые политики](https://docs.microsoft.com/windows/client-management/mdm/policy-csps-supported-by-hololens2)

## <a name="hardware-restrictions"></a>Аппаратные ограничения
Устройства Windows 10 holographic используют современные технологии, которые включают в себя популярные аппаратные функции, такие как камеры, микрофоны, динамики, USB-интерфейсы, интерфейсы Bluetooth и Wi-Fi. Аппаратные ограничения также можно использовать, чтобы контролировать доступность этих функций.
Ниже перечислены часто используемые параметры MDM, поддерживаемые Windows 10 holographic для настройки ограничений оборудования.

> [!NOTE]
> Некоторые из этих ограничений оборудования влияют на подключение и помогают в защите данных.

-   [Разрешить Wi-Fi:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi) Могут ли пользователи включить и использовать радиомодуль Wi-Fi на своих устройствах.
-   [Разрешить USB-подключение:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowusbconnection) Включено ли USB-подключение (не влияет на зарядку по USB).
-   [Разрешить Bluetooth:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth) Могут ли пользователи включать и использовать радиомодули Bluetooth на своих устройствах.
-   [Ограничить камеру:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera) Указывает, могут ли приложения для Windows получать доступ к камере.
-   [Ограничить Микрофоны:](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone) Указывает, могут ли приложения для Windows получать доступ к микрофону.

Добавлено в [Windows holographic, виртуализации 20H2](hololens-release-notes.md#windows-holographic-version-20h2) для устройств HoloLens 2. 
- [Дисплайоффтимеаутонбаттери](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery) Установите период времени до отключения экрана и отключив экран, заблокирующий устройство. 
- [Дисплайоффтимеаутплугжедин](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin) Установите период времени до отключения экрана и отключив экран, заблокирующий устройство. 
