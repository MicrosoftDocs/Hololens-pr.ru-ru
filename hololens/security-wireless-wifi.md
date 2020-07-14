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
# <span data-ttu-id="a5448-104">Беспроводная сеть и Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="a5448-104">Wireless and Wi-Fi</span></span>

<span data-ttu-id="a5448-105">Беспроводная локальная сеть HoloLens 2 поддерживает впечатляющий диапазон новейших стандартов безопасности Wi-Fi, в том числе:</span><span class="sxs-lookup"><span data-stu-id="a5448-105">HoloLens 2 Wireless LAN connectivity supports an impressive range of the latest Wi-Fi security standards, such as:</span></span>
  * <span data-ttu-id="a5448-106">WPA2 (защищенный доступ по протоколу Wi-Fi 2)</span><span class="sxs-lookup"><span data-stu-id="a5448-106">WPA2 (Wi-Fi Protected Access 2)</span></span>  
  * <span data-ttu-id="a5448-107">TEAP (протокол расширенной проверки подлинности туннелей)</span><span class="sxs-lookup"><span data-stu-id="a5448-107">TEAP (Tunnel Extensible Authentication Protocol)</span></span>  
  * <span data-ttu-id="a5448-108">OWE (оппортунистическое беспроводное шифрование)</span><span class="sxs-lookup"><span data-stu-id="a5448-108">OWE (Opportunistic Wireless Encryption)</span></span>

<span data-ttu-id="a5448-109">TEAP, следующее поколение проверки подлинности корпоративной сети, предоставляет возможность безопасно объединить несколько учетных данных в рамках одной транзакции.</span><span class="sxs-lookup"><span data-stu-id="a5448-109">TEAP, the next generation of enterprise network authentication, provides the ability to securely chain multiple credentials into a single transaction.</span></span>  <span data-ttu-id="a5448-110">Это позволяет администраторам использовать более надежную стратегию обеспечения безопасности — стратегию, которая требует наличия допустимых удостоверений и для компьютера, и для пользователя во время одной и той же операции проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a5448-110">This allows administrators to enforce a stronger security stance – one that requires valid identities for both machine and user during the same authentication transaction.</span></span>

<span data-ttu-id="a5448-111">HoloLens 2 включает современные протоколы беспроводных сетей и Wi-Fi, которые обеспечивают максимальную поддержку для клиентов.</span><span class="sxs-lookup"><span data-stu-id="a5448-111">HoloLens 2 has modern wireless and Wi-Fi protocols that enable customers with maximum support.</span></span> <span data-ttu-id="a5448-112">Радиоприемник HoloLens 2 — это решение Qualcomm WCN3990, обеспечивающее высокое качество радиосвязи.</span><span class="sxs-lookup"><span data-stu-id="a5448-112">The HoloLens 2 radio is a Qualcomm WCN3990 solution delivering a premium radio experience.</span></span> <span data-ttu-id="a5448-113">Поддерживаемый стандарт Wi-Fi — 802.11 ac/n.</span><span class="sxs-lookup"><span data-stu-id="a5448-113">The Wi-Fi supported is 802.11 ac/n.</span></span> <span data-ttu-id="a5448-114">Диапазон частот не может настраиваться пользователем и зависит от страны или региона использования.</span><span class="sxs-lookup"><span data-stu-id="a5448-114">The frequency range is not user configurable and depends on the country of use.</span></span> <span data-ttu-id="a5448-115">В Соединенных Штатах для настройки Wi-Fi используются частотные каналы 2,4 ГГц (1-11) и 5 ГГц (36-64, 100-165).</span><span class="sxs-lookup"><span data-stu-id="a5448-115">In the United States, Wi-Fi uses both 2.4GHz (1-11) channels and 5GHz (36-64, 100-165) channels.</span></span> <span data-ttu-id="a5448-116">Ни пользователи, ни устройства не могут создавать списки разрешенных или запрещенных частот.</span><span class="sxs-lookup"><span data-stu-id="a5448-116">Neither user nor device can make allow/deny lists for specific frequencies.</span></span> <span data-ttu-id="a5448-117">Bluetooth SIC Core 5.0 включает выделенную антенну 2,4 ГГц для Bluetooth, которая не используется для Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="a5448-117">Bluetooth SIC Core 5.0 has a dedicated 2.4GHz antenna for Bluetooth which is not shared with Wi-Fi.</span></span> <span data-ttu-id="a5448-118">Стек программного обеспечения HoloLens 2 поддерживает несколько протоколов и профилей, в том числе HID, HOGP, A2DP и GATT.</span><span class="sxs-lookup"><span data-stu-id="a5448-118">HoloLens 2’s software stack supports several protocols and profiles including HID, HOGP, A2DP, and GATT.</span></span> 

<span data-ttu-id="a5448-119">ИТ-администраторы могут выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a5448-119">IT admins can:</span></span> 
  * <span data-ttu-id="a5448-120">Включать или ограничивать [доступ Bluetooth](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)</span><span class="sxs-lookup"><span data-stu-id="a5448-120">Enable or restrict  [Bluetooth access](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)</span></span>
  * <span data-ttu-id="a5448-121">Задавать [локальное имя устройствам Bluetooth](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)</span><span class="sxs-lookup"><span data-stu-id="a5448-121">Set [local Bluetooth device names](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)</span></span>
  * <span data-ttu-id="a5448-122">Разрешать [обнаружение устройств](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)</span><span class="sxs-lookup"><span data-stu-id="a5448-122">Allow [devices to be discoverable](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)</span></span>
  * <span data-ttu-id="a5448-123">Разрешать или запрещать [подключение к сети Wi-Fi](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi).</span><span class="sxs-lookup"><span data-stu-id="a5448-123">Allow/disallow [Wi-Fi connections](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)</span></span> 
  * <span data-ttu-id="a5448-124">Разрешать или запрещать [подключение к сети Wi-Fi вне сетей с установленным сервером MDM](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)</span><span class="sxs-lookup"><span data-stu-id="a5448-124">Allow or disallow [connecting to Wi-Fi outside of MDM server-installed networks](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)</span></span>
