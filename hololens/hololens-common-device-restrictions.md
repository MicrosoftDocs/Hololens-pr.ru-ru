---
title: Общие ограничения для устройств
description: получайте актуальные сведения об общих ограничениях устройств и параметрах для устройства HoloLens mixed reality.
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
ms.openlocfilehash: 6a09766a06fff912aae20dc07974b723d812bd370562a33297552dc0d2f7f12c
ms.sourcegitcommit: f8e7cc2fbdcdf8962700fd50b9c017bd83d1ad65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "115664281"
---
# <a name="common-device-restrictions"></a>Общие ограничения для устройств 

это руководство поможет ит-специалистам понять наиболее часто используемые варианты управления, доступные для Windows 10 Holographic ос на предприятии. Изучите документацию по системе MDM, чтобы понять, каким образом данные политики реализуются вашим поставщиком MDM. Не все системы MDM поддерживают все настройки, описанные в данном руководстве. Некоторые поддерживают пользовательские политики посредством XML-файлов OMA-URI. См. раздел [Поддержка пользовательских политик Microsoft Intune](/mem/intune/configuration/custom-settings-windows-10). Различные поставщики MDM также могут использовать различные соглашения об именовании.

## <a name="prevent-changing-of-settings"></a>Запрет на изменение параметров
Сотрудникам, как правило, разрешено изменять на персональном устройстве определенные параметры, изменение которых на корпоративных устройствах рекомендуется запретить. сотрудники могут в интерактивном режиме настраивать определенные параметры HoloLens через пользовательский интерфейс параметров. С помощью MDM можно ограничить изменения, которые могут вносить пользователи. ниже перечислены часто используемые параметры MDM, которые Windows 10 Holographic поддерживаются для настройки ограничений для параметров.
-   [Разрешить VPN:](/windows/client-management/mdm/policy-csp-settings#settings-allowvpn) Разрешает пользователю изменять параметры VPN
-   [Разрешить ручную настройку WiFi:](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration) Разрешает пользователям устанавливать Wi-Fi подключения за пределами подготовленных сетей MDM
-   [Разрешить отмену регистрации MDM вручную](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment) Разрешено ли пользователям удалять учетную запись рабочей области (т. е. отменить регистрацию устройства в системе MDM);

добавлено в [Windows holographic, версия 20H2](hololens-release-notes.md#windows-holographic-version-20h2) для HoloLens 2 устройств:
- [Разрешить добавление пакета подготовки:](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage) Переключите, если пользователи могут добавлять новые пакеты подготовки, перезаписывая их новыми значениями.
- [Разрешить удаление пакета подготовки:](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage) Установите переключатель, если пользователи могут удалять пакеты подготовки, что позволяет им переключать ранее заблокированные параметры.

дополнительные сведения о параметрах политики можно найти в HoloLens поддерживаемых [csp политик](/windows/client-management/mdm/policy-csps-supported-by-hololens2)

## <a name="hardware-restrictions"></a>Аппаратные ограничения
Windows 10 Holographic устройства используют современные технологии, которые включают в себя популярные аппаратные функции, такие как камеры, микрофоны, динамики, USB-интерфейсы, Bluetooth интерфейсы и Wi-Fi. Аппаратные ограничения также можно использовать, чтобы контролировать доступность этих функций.
ниже перечислены типичные параметры MDM, которые Windows 10 Holographic поддерживает для настройки ограничений оборудования.

> [!NOTE]
> Некоторые из этих ограничений оборудования влияют на подключение и помогают в защите данных.

-   [Разрешить Wi-Fi:](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi) Могут ли пользователи включить и использовать радиомодуль Wi-Fi на своих устройствах.
-   [Разрешить USB-подключение:](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowusbconnection) Включено ли USB-подключение (не влияет на зарядку по USB).
-   [Разрешить Bluetooth:](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth) могут ли пользователи включать и использовать радиостанции Bluetooth на своих устройствах.
-   [Ограничить камеру:](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera) указывает, могут ли приложения Windows доступ к камере.
-   [Ограничить Микрофоны:](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone) указывает, могут ли приложения Windows получить доступ к микрофону.

добавлено в [Windows holographic, виртуализации 20H2](hololens-release-notes.md#windows-holographic-version-20h2) для устройств HoloLens 2. 
- [Дисплайоффтимеаутонбаттери](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery) Установите период времени до отключения экрана и отключив экран, заблокирующий устройство. 
- [Дисплайоффтимеаутплугжедин](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin) Установите период времени до отключения экрана и отключив экран, заблокирующий устройство. 
