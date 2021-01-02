---
title: Архитектура безопасности HoloLens
description: Архитектура безопасности
author: evmill
ms.author: v-evmill
ms.reviewer: tagran
ms.date: 6/30/2020
ms.topic: article
keywords: безопасность, hololens, hololens 2, безопасность hololens2, обзор безопасности, архитектура безопасности, архитектура, архитектура hololens 2
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: d8e68f73d05db397a7ee088382e82dfa762177b0
ms.sourcegitcommit: 96dcd015ad24169295690a8ed13ea1bf480e4b9e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/01/2021
ms.locfileid: "11253256"
---
# <span data-ttu-id="3e422-104">Обзор безопасности и архитектуры</span><span class="sxs-lookup"><span data-stu-id="3e422-104">Security overview and architecture</span></span>

<span data-ttu-id="3e422-105">Архитектура безопасности HoloLens 2 с самого начала проектировалась и разрабатывалась так, чтобы не содержать традиционных проблем безопасности и свести к минимуму возможные уязвимости.</span><span class="sxs-lookup"><span data-stu-id="3e422-105">The HoloLens 2 security architecture was designed and engineered from the ground up to be free from legacy security issues, while creating a minimized attack surface.</span></span> <span data-ttu-id="3e422-106">Новая современная архитектура поддерживает защищенные расположения хранения и расширенные элементы безопасности; различные механизмы предохраняют операционную систему от возможных угроз и уязвимостей.</span><span class="sxs-lookup"><span data-stu-id="3e422-106">This new, innovative architecture offers secure storage locations and advanced security elements, with mechanisms capable of shielding operating systems from potential threats and vulnerabilities.</span></span>

<span data-ttu-id="3e422-107">В HoloLens 2 оборудование, программное обеспечение, сетевые решения и службы вместе обеспечивают всестороннюю безопасность и оптимальное удобство пользователей.</span><span class="sxs-lookup"><span data-stu-id="3e422-107">HoloLens 2 combines hardware, software, networking, and services to deliver end-to-end security, while providing the user with an optimal experience.</span></span> <span data-ttu-id="3e422-108">В HoloLens 2 значительная часть функций безопасности автоматически включена, поэтому для правильной настройки операционной системы требуется гораздо меньше действий.</span><span class="sxs-lookup"><span data-stu-id="3e422-108">With HoloLens 2, a large majority of security features are now turned on automatically, minimizing the effort required to correctly set up and configure the operating system.</span></span>

<span data-ttu-id="3e422-109">Архитектура Windows HoloLens 2 и операционной системы поддерживает следующие современные функции безопасности.</span><span class="sxs-lookup"><span data-stu-id="3e422-109">Windows HoloLens 2 and operating system architecture offers these innovative security features:</span></span>

  * <span data-ttu-id="3e422-110">**Разделение состояний и изоляция**: эта новая архитектура защищает от изменений важнейшие части операционной системы HoloLens 2, в том числе необходимые для загрузки в надежное состояние.</span><span class="sxs-lookup"><span data-stu-id="3e422-110">**State separation and isolation**:  This new architecture protects critical portions of the HoloLens 2 operating system from change - such as those required for the core operating system to boot into a trusted state.</span></span> <span data-ttu-id="3e422-111">Технология изоляции применяется для помещения ненадежных приложений в песочницу, чтобы они не могли повлиять на безопасность системы.</span><span class="sxs-lookup"><span data-stu-id="3e422-111">Isolation technology is used to confine untrusted apps in a sandbox area, ensuring that they cannot impact the system security.</span></span> <span data-ttu-id="3e422-112">Вся операционная система разделена на безопасные фрагменты, каждый из которых защищен набором различных технологий безопасности.</span><span class="sxs-lookup"><span data-stu-id="3e422-112">The entire operating system is segmented into secure sections, with each section shielded by a combination of different security technologies.</span></span>
  
  * <span data-ttu-id="3e422-113">**Защита данных**: в случае утери или кражи устройства пользователя HoloLens 2 не позволит несанкционированным приложениям прочесть конфиденциальные сведения. Для этого применяется шифрование данных BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3e422-113">**Data Protection**: If a user’s device is lost or stolen, HoloLens 2 prevents unauthorized applications from reading sensitive information by relying on BitLocker encryption of data.</span></span> 
  
  * <span data-ttu-id="3e422-114">**Операционная система без пароля**: в прежних ОС, где использовались пароли, пользователи могли стать жертвами фишинга, что приводило к компрометации учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3e422-114">**Password-less operating system**:  Older, password-based operating systems could inadvertently expose users to phishing threats and were often responsible for compromised accounts.</span></span> <span data-ttu-id="3e422-115">Windows Holographic for Business исключает использование паролей для входа в MSA и Azure AD и усиливает защиту удостоверений пользователей с помощью Windows Hello™ и FIDO2.</span><span class="sxs-lookup"><span data-stu-id="3e422-115">Windows Holographic for Business eliminates the use of passwords for MSA and Azure AD sign-in and strengthens user-identity protection with Windows Hello™ and FIDO2 sign-in.</span></span> 
  
    > [!NOTE]
    > <span data-ttu-id="3e422-116">Для поддержки FIDO2 в устройстве должно использоваться программное обеспечение сборки 19041 или быть поздней.</span><span class="sxs-lookup"><span data-stu-id="3e422-116">To have FIDO2 support, the device must be on Build 19041 or higher.</span></span> 

  * <span data-ttu-id="3e422-117">**Сетевая безопасность**: в HoloLens 2 реализован более высокий уровень безопасности пользователей в сети за счет применения улучшенных протоколов и параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e422-117">**Network security**: HoloLens 2 offers the user increased network security via improved protocols and default settings.</span></span>
