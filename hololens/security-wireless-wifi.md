---
title: Беспроводная сеть и Wi-Fi
description: Беспроводная сеть и Wi-Fi
author: jbennett
ms.date: 6/30/2020
ms.topic: article
keywords: безопасность, hololens, беспроводная сеть, Wi-Fi
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: ''
manager: yannisl
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 2771e6e5e428b2705fc2f495823480a9514fa71a
ms.sourcegitcommit: 896bdfccf4612a692a25a6bfaecfa2146860407e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "10865772"
---
# Беспроводная сеть и Wi-Fi

Беспроводная локальная сеть HoloLens 2 поддерживает впечатляющий диапазон новейших стандартов безопасности Wi-Fi, в том числе:
  * WPA2 (защищенный доступ по протоколу Wi-Fi 2)  
  * TEAP (протокол расширенной проверки подлинности туннелей)  
  * OWE (оппортунистическое беспроводное шифрование)

TEAP, следующее поколение проверки подлинности корпоративной сети, предоставляет возможность безопасно объединить несколько учетных данных в рамках одной транзакции.  Это позволяет администраторам использовать более надежную стратегию обеспечения безопасности — стратегию, которая требует наличия допустимых удостоверений и для компьютера, и для пользователя во время одной и той же операции проверки подлинности.

HoloLens 2 включает современные протоколы беспроводных сетей и Wi-Fi, которые обеспечивают максимальную поддержку для клиентов. Радиоприемник HoloLens 2 — это решение Qualcomm WCN3990, обеспечивающее высокое качество радиосвязи. Поддерживаемый стандарт Wi-Fi — 802.11 ac/n. Диапазон частот не может настраиваться пользователем и зависит от страны или региона использования. В Соединенных Штатах для настройки Wi-Fi используются частотные каналы 2,4 ГГц (1-11) и 5 ГГц (36-64, 100-165). Ни пользователи, ни устройства не могут создавать списки разрешенных или запрещенных частот. Bluetooth SIC Core 5.0 включает выделенную антенну 2,4 ГГц для Bluetooth, которая не используется для Wi-Fi. Стек программного обеспечения HoloLens 2 поддерживает несколько протоколов и профилей, в том числе HID, HOGP, A2DP и GATT. 

ИТ-администраторы могут выполнять следующие действия: 
  * Включать или ограничивать [доступ Bluetooth](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
  * Задавать [локальное имя устройствам Bluetooth](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
  * Разрешать [обнаружение устройств](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
  * Разрешать или запрещать [подключение к сети Wi-Fi](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi). 
  * Разрешать или запрещать [подключение к сети Wi-Fi вне сетей с установленным сервером MDM](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
