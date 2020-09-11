---
title: Разработка средств безопасности
description: Разработка средств безопасности
author: evmill
ms.author: v-evmill
ms.reviewer: tagran
ms.date: 6/30/2020
ms.topic: article
keywords: безопасность, hololens, безопасность, разработка
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: cecc556841033ee394f36915f4cae8839dad08df
ms.sourcegitcommit: 72ff3174b34d2acaf72547b7d981c66aef8fa82f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11009537"
---
# <span data-ttu-id="9a9ac-104">Разработка средств безопасности</span><span class="sxs-lookup"><span data-stu-id="9a9ac-104">Security engineering</span></span>

<span data-ttu-id="9a9ac-105">У корпорации Майкрософт есть несколько ресурсов и групп, посвященных оптимизации технологических протоколов компании, соблюдению соответствующих требований и обеспечению доверия клиентов.</span><span class="sxs-lookup"><span data-stu-id="9a9ac-105">Microsoft has several resources and teams devoted to optimizing the company’s engineering protocols, addressing compliance, and ensuring customer trust.</span></span> 

  * <span data-ttu-id="9a9ac-106">Дополнительные сведения о методиках разработки безопасности Майкрософт см. в статье [Жизненный цикл безопасной разработки (SDL)](https://www.microsoft.com/securityengineering/sdl).</span><span class="sxs-lookup"><span data-stu-id="9a9ac-106">To learn more about Microsoft’s security engineering development practices, see the [Security Development Lifecycle (SDL)](https://www.microsoft.com/securityengineering/sdl).</span></span>
  * <span data-ttu-id="9a9ac-107">Корпорация Майкрософт и, следовательно, HoloLens 2 дает клиентам возможность выбирать способ и причины сбора и использования данных, что упрощает их изучение в [политике конфиденциальности Майкрософт](https://privacy.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="9a9ac-107">Microsoft, and therefore HoloLens 2, empowers customers to make choices about how and why data is collected and used, which can be further explored in [Microsoft’s Privacy policy](https://privacy.microsoft.com/).</span></span> 
  * <span data-ttu-id="9a9ac-108">[Центр ответов по безопасности Майкрософт (MSRC)](https://www.microsoft.com/msrc) — это часть сообщества защитников, которая обеспечивает создание отчетов об уязвимости, а также эффективную категоризацию и реагирование на ошибки безопасности.</span><span class="sxs-lookup"><span data-stu-id="9a9ac-108">[Microsoft Security Response Center (MSRC)](https://www.microsoft.com/msrc) is part of the defender community, providing an efficient vulnerability reporting experience and an effective categorization and response to security bugs.</span></span> 

## <span data-ttu-id="9a9ac-109">Обновления и исправления</span><span class="sxs-lookup"><span data-stu-id="9a9ac-109">Updates and patches</span></span>

<span data-ttu-id="9a9ac-110">Обновления и исправления для системы безопасности выпускаются каждый второй вторник месяца.</span><span class="sxs-lookup"><span data-stu-id="9a9ac-110">Security updates and patches are released on the second Tuesday of each month.</span></span> <span data-ttu-id="9a9ac-111">Чтобы понять критерии, используемые Майкрософт для оценки следующих шагов обнаружения уязвимости, см. страницу центра ответов по безопасности Майкрософт [Критерии обслуживания безопасности](https://www.microsoft.com/msrc/windows-security-servicing-criteria).</span><span class="sxs-lookup"><span data-stu-id="9a9ac-111">In order to understand the criteria used by Microsoft to evaluate next steps for a reported vulnerability, see the Microsoft Security Response Center’s [Security Servicing Criteria page](https://www.microsoft.com/msrc/windows-security-servicing-criteria).</span></span> 

<span data-ttu-id="9a9ac-112">Инструкции по управлению обновлениями HoloLens 2 через MDM см. в статье [Управление обновлениями HoloLens](https://docs.microsoft.com/hololens/hololens-updates).</span><span class="sxs-lookup"><span data-stu-id="9a9ac-112">For guidance on managing HoloLens 2 updates via MDM, see [Manage HoloLens updates](https://docs.microsoft.com/hololens/hololens-updates).</span></span> <span data-ttu-id="9a9ac-113">Частота обновлений операционной системы для HoloLens 2 такая же, как и для Windows 10; в год выходят два обновления: одно весной, и одно осенью.</span><span class="sxs-lookup"><span data-stu-id="9a9ac-113">The operating system update cadence for HoloLens 2 matches that of Windows 10; there are two updates per year, one taking place in Spring and the other in Fall.</span></span> <span data-ttu-id="9a9ac-114">Дополнительные сведения о защите устройств в процессе обновления ОС см. в статье [Разделение и изоляция состояния](security-state-separation-isolation.md).</span><span class="sxs-lookup"><span data-stu-id="9a9ac-114">For more on how devices are secured during OS updates, see [State separation and isolation](security-state-separation-isolation.md).</span></span> 

<span data-ttu-id="9a9ac-115">ИТ-администраторы могут подробнее узнать о политике обновления в статье [Поставщик служб конфигурации политики. Обновления](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-update).</span><span class="sxs-lookup"><span data-stu-id="9a9ac-115">IT admins can learn more about update policy at [Policy CSP - Update](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-update).</span></span> 
