---
title: Сетевая безопасность
description: сетевая безопасность
author: jbennett
ms.date: 6/30/2020
ms.topic: article
keywords: безопасность, hololens, сеть, сетевая безопасность
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: ''
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 147401331cb6da732a6fe37e57964d61a10dce99
ms.sourcegitcommit: 47bc3b696936dd7011b3f9dd683deb872ed25b90
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "10883143"
---
# <span data-ttu-id="75fd6-104">Сетевая безопасность</span><span class="sxs-lookup"><span data-stu-id="75fd6-104">Network security</span></span>

## <span data-ttu-id="75fd6-105">Сетевые протоколы</span><span class="sxs-lookup"><span data-stu-id="75fd6-105">Network protocols</span></span>

<span data-ttu-id="75fd6-106">Устаревшая система NetBIOS широко использовалась в прошлом в сценариях локальных сетей — часто для предоставления разрешения имен для компьютеров и общих папок.</span><span class="sxs-lookup"><span data-stu-id="75fd6-106">The outdated NetBIOS (Network Basic Input/Output System) was widely used in the past in LAN scenarios – often for providing name resolution to a computer and shared folders.</span></span> <span data-ttu-id="75fd6-107">Однако со временем NetBIOS оказалась уязвимой перед множеством атак, после чего ее релевантность снизилась, и она уступила место другим, более надежным протоколам.</span><span class="sxs-lookup"><span data-stu-id="75fd6-107">But over time, NetBIOS proved to be susceptible to multiple attacks, and its relevance decreased in favor of other more secure protocols.</span></span> <span data-ttu-id="75fd6-108">Чтобы устранить эту проблему уязвимости, в HoloLens 2 из операционной системы был удален код, связанный с NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="75fd6-108">To remove this vulnerability issue, HoloLens 2 has eliminated the NetBIOS-related code from the operating system.</span></span>

<span data-ttu-id="75fd6-109">Протокол TLS (Transport Layer Security) постоянно развивается.</span><span class="sxs-lookup"><span data-stu-id="75fd6-109">TLS (Transport Layer Security) protocols are constantly evolving.</span></span> <span data-ttu-id="75fd6-110">Чтобы не отставать в защите от различных эксплойтов безопасности, раскрытых в этой области, компьютерная отрасль перешла на новые, более эффективные версии протокола.</span><span class="sxs-lookup"><span data-stu-id="75fd6-110">To keep up with the various security exploits that have been uncovered in this area, the computing industry has graduated to newer and more effective versions.</span></span> <span data-ttu-id="75fd6-111">В связи с тем, что развертывание для внедрения новых версий протокола TLS на всех серверах требует времени, существует возможность использования резервного механизма, благодаря которому клиент и сервер с разными заданными по умолчанию версиями протокола могут взаимодействовать в течение переходного периода.</span><span class="sxs-lookup"><span data-stu-id="75fd6-111">Due to the time required for all server deployments to adopt the new TLS protocol versions, a fallback mechanism can be implemented that permits the client and servers on different default protocol versions to still be able to communicate during the transition period.</span></span>

## <span data-ttu-id="75fd6-112">Безопасное соединение</span><span class="sxs-lookup"><span data-stu-id="75fd6-112">Secure connectivity</span></span> 

<span data-ttu-id="75fd6-113">Брандмауэр Защитника Windows обеспечивает критически важные функции для безопасного соединения устройств.</span><span class="sxs-lookup"><span data-stu-id="75fd6-113">The Windows Defender Firewall delivers critical functionality to secure device connectivity.</span></span> <span data-ttu-id="75fd6-114">При использовании HoloLens 2 брандмауэр всегда включен, и возможность отключить его программными средствами или с помощью пользовательского интерфейса не предусмотрена.</span><span class="sxs-lookup"><span data-stu-id="75fd6-114">With HoloLens 2, the firewall is always enabled and there are no ways to disable it programmatically or through the UI.</span></span>

<span data-ttu-id="75fd6-115">Конфиденциальность удаленного доступа и соединения для мобильных клиентов может быть обеспечена с помощью [платформы подключаемых модулей VPN UWP](https://docs.microsoft.com/uwp/api/Windows.Networking.Vpn?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="75fd6-115">Remote access and connection privacy for mobile clients can be assured through the [UWP VPN plug-in platform](https://docs.microsoft.com/uwp/api/Windows.Networking.Vpn?view=winrt-19041).</span></span> <span data-ttu-id="75fd6-116">Сторонние поставщики VPN могут создавать собственные подключаемые модули с использованием интерфейсов API WinRT, работающие в песочнице AppContainer, что упрощает процесс и устраняет проблемы, часто сопровождающие написание драйверов системного уровня.</span><span class="sxs-lookup"><span data-stu-id="75fd6-116">Third-party VPN providers can create their own plug-ins using WinRT APIs which will run within the AppContainer sandbox, eliminating the complexity and issues often associated with writing system-level drivers.</span></span>
