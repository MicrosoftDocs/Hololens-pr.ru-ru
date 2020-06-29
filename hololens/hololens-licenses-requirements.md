---
title: Лицензии для развертывания смешанной реальности
description: ''
ms.prod: hololens
ms.sitesec: library
author: pawinfie
ms.author: pawinfie
audience: HoloLens
ms.topic: article
ms.localizationpriority: high
ms.date: 1/23/2020
ms.reviewer: ''
manager: bradke
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 0da2a2337b3b1f361ffbb698607f304efbf6d193
ms.sourcegitcommit: f3cda6c6b3bfb7ba4be5f4da66d8ed5b03ca807d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2020
ms.locfileid: "10830143"
---
# Определение необходимых лицензий

## Руководство по лицензированию управления мобильными устройствами (MDM)

Если вы планируете управлять устройствами HoloLens, вам потребуется Azure AD и MDM. Служба Active Directory (AD) не используется для управления устройствами HoloLens.
Если вы планируете использовать систему MDM, отличную от Intune, потребуются [лицензии Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis).
Если вы планируете использовать Intune в качестве MDM, [здесь](https://docs.microsoft.com/intune/fundamentals/licenses) представлен список наборов, включающих лицензии Intune. **Обратите внимание, что Azure AD входит в большинство этих наборов.**

## Определение лицензий, необходимых для вашего сценария и продуктов

### Требования к лицензиям на HoloLens

Возможно, вам потребуется обновить устройство HoloLens 1-го поколения до Windows Holographic для бизнеса. (См. [Коммерческие функции HoloLens](holoLens-commercial-features.md#feature-comparison-between-editions) для определения необходимости обновления).

 Если это так, вам нужно будет сделать следующее:

- Получить XML-файл лицензии HoloLens Enterprise
- Примените файл XML к HoloLens. Это можно сделать с помощью [пакета подготовки](hololens-provisioning.md) или с помощью [диспетчера мобильных устройств](https://docs.microsoft.com/intune/configuration/holographic-upgrade)

### Требования к лицензии для Удаленной поддержки

Убедитесь, что у вас есть требуемые лицензии и устройство. Обновленные требования к лицензиям и продукту см. [здесь](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements).

1. [Лицензия для Удаленной поддержки](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist)
1. [Teams Freemium/Teams](https://products.office.com/microsoft-teams/free)
1. [Лицензия для Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)

Если вы планируете реализовать **[этот межклиентный сценарий](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants)**, вам может потребоваться лицензия на Информационные барьеры. Чтобы определить, требуется ли лицензия на Информационные барьеры, ознакомьтесь с [этой статьей](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary).

### Требования к лицензии для руководств

Обновленные требования к лицензиям и устройству см. [здесь](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements).

1. [Лицензия для Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
1. [Power BI](https://powerbi.microsoft.com/desktop/)
1. [Рекомендации](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup)
