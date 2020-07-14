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
ms.openlocfilehash: c88a9af7369a6a9d6fb115fb820c0a4da13eafdc
ms.sourcegitcommit: 896bdfccf4612a692a25a6bfaecfa2146860407e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "10865844"
---
# <span data-ttu-id="cb0c9-104">Сетевая безопасность</span><span class="sxs-lookup"><span data-stu-id="cb0c9-104">Network security</span></span>

## <span data-ttu-id="cb0c9-105">Сетевые протоколы</span><span class="sxs-lookup"><span data-stu-id="cb0c9-105">Network protocols</span></span>

<span data-ttu-id="cb0c9-106">Устаревшая система NetBIOS широко использовалась в прошлом в сценариях локальных сетей — часто для предоставления разрешения имен для компьютеров и общих папок.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-106">The outdated NetBIOS (Network Basic Input/Output System) was widely used in the past in LAN scenarios – often for providing name resolution to a computer and shared folders.</span></span> <span data-ttu-id="cb0c9-107">Однако со временем NetBIOS оказалась уязвимой перед множеством атак, после чего ее релевантность снизилась, и она уступила место другим, более надежным протоколам.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-107">But over time, NetBIOS proved to be susceptible to multiple attacks, and its relevance decreased in favor of other more secure protocols.</span></span> <span data-ttu-id="cb0c9-108">Чтобы устранить эту проблему уязвимости, в HoloLens 2 из операционной системы был удален код, связанный с NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-108">To remove this vulnerability issue, HoloLens 2 has eliminated the NetBIOS-related code from the operating system.</span></span>

<span data-ttu-id="cb0c9-109">Протокол TLS (Transport Layer Security) постоянно развивается.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-109">TLS (Transport Layer Security) protocols are constantly evolving.</span></span> <span data-ttu-id="cb0c9-110">Чтобы не отставать в защите от различных эксплойтов безопасности, раскрытых в этой области, компьютерная отрасль перешла на новые, более эффективные версии протокола.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-110">To keep up with the various security exploits that have been uncovered in this area, the computing industry has graduated to newer and more effective versions.</span></span> <span data-ttu-id="cb0c9-111">В связи с тем, что развертывание для внедрения новых версий протокола TLS на всех серверах требует времени, существует возможность использования резервного механизма, благодаря которому клиент и сервер с разными заданными по умолчанию версиями протокола могут взаимодействовать в течение переходного периода.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-111">Due to the time required for all server deployments to adopt the new TLS protocol versions, a fallback mechanism can be implemented that permits the client and servers on different default protocol versions to still be able to communicate during the transition period.</span></span>

<span data-ttu-id="cb0c9-112">Однако такие резервные механизмы увеличивают риски, связанные с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-112">However, such fallback mechanisms increase security risks.</span></span> <span data-ttu-id="cb0c9-113">Ввиду этой проблемы в HoloLens 2 отключена резервная возможность использования TLS 1.2 с TLS 1.1 или 1.0, и пользовательский интерфейс для его включения отсутствует.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-113">Understanding this issue, in HoloLens 2 the fallback from TLS 1.2 to TLS 1.1 or 1.0 has been disabled, and there is no user interface to enable it.</span></span> <span data-ttu-id="cb0c9-114">Более того, в процессе подтверждения TLS клиент запрашивает версию TLS1.2 и не позволяет серверу перейти к более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-114">Furthermore, during the TLS handshake, the client will ask for TLS 1.2, and does not allow the server to downgrade to a lower version.</span></span>

## <span data-ttu-id="cb0c9-115">Безопасное соединение</span><span class="sxs-lookup"><span data-stu-id="cb0c9-115">Secure connectivity</span></span> 

<span data-ttu-id="cb0c9-116">Брандмауэр Защитника Windows обеспечивает критически важные функции для безопасного соединения устройств.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-116">The Windows Defender Firewall delivers critical functionality to secure device connectivity.</span></span> <span data-ttu-id="cb0c9-117">При использовании HoloLens 2 брандмауэр всегда включен, и возможность отключить его программными средствами или с помощью пользовательского интерфейса не предусмотрена.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-117">With HoloLens 2, the firewall is always enabled and there are no ways to disable it programmatically or through the UI.</span></span>

<span data-ttu-id="cb0c9-118">Конфиденциальность удаленного доступа и соединения для мобильных клиентов может быть обеспечена с помощью [платформы подключаемых модулей VPN UWP](https://docs.microsoft.com/uwp/api/Windows.Networking.Vpn?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="cb0c9-118">Remote access and connection privacy for mobile clients can be assured through the [UWP VPN plug-in platform](https://docs.microsoft.com/uwp/api/Windows.Networking.Vpn?view=winrt-19041).</span></span> <span data-ttu-id="cb0c9-119">Сторонние поставщики VPN могут создавать собственные подключаемые модули с использованием интерфейсов API WinRT, работающие в песочнице AppContainer, что упрощает процесс и устраняет проблемы, часто сопровождающие написание драйверов системного уровня.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-119">Third-party VPN providers can create their own plug-ins using WinRT APIs which will run within the AppContainer sandbox, eliminating the complexity and issues often associated with writing system-level drivers.</span></span>
