---
title: Требования к лицензиям
description: Оставайтесь в курсе всех требований и рекомендаций по лицензированию для управления мобильными устройствами, HoloLens и Удаленной поддержки.
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
ms.openlocfilehash: 2f7af532d2172dcaa6514ee11dbb0d6ab5631929
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283970"
---
# Требования к лицензиям

## Руководство по лицензированию управления мобильными устройствами (MDM)

Если вы планируете управлять устройствами HoloLens, вам потребуется Azure AD и MDM. Служба Active Directory (AD) не используется для управления устройствами HoloLens.
Если вы планируете использовать систему MDM, отличную от Intune, то потребуются [лицензии Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis).
Если вы планируете использовать Intune в качестве MDM, ознакомьтесь со [списком наборов,](https://docs.microsoft.com/intune/fundamentals/licenses) которые включают лицензии Intune. **Обратите внимание, что Azure AD входит в большинство этих наборов.**

## Определение лицензий, необходимых для вашего сценария и продуктов

### Требования к лицензиям HoloLens (1-го поколения)

Возможно, вам потребуется обновить устройство HoloLens 1-го поколения до Windows Holographic for Business. (См. [Коммерческие функции HoloLens](holoLens-commercial-features.md#feature-comparison-between-editions) для определения необходимости обновления).

 Если это так, вам нужно будет сделать следующее:

- Получить XML-файл лицензии HoloLens Enterprise
- Примените файл XML к HoloLens. Это можно сделать с помощью [пакета подготовки](hololens-provisioning.md) или с помощью [диспетчера мобильных устройств](https://docs.microsoft.com/intune/configuration/holographic-upgrade)

### Требования к лицензии для Удаленной поддержки

Убедитесь, что у вас есть необходимые лицензии и устройство, которые можно проверить в [документации по требованиям.](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements)

1. [Лицензия для Удаленной поддержки](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist)
    1. Или воспользуйтесь [пробной версией удаленной поддержки](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist)
1. [Teams Freemium/Teams](https://products.office.com/microsoft-teams/free)
1. [Лицензия для Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)

Если вы планируете реализовать **[этот межклиентный сценарий](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants)**, вам может потребоваться лицензия на Информационные барьеры. Чтобы определить, требуется ли лицензия на Информационные барьеры, ознакомьтесь с [этой статьей](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary).

### Требования к лицензии для руководств

Проверьте [обновленные требования к лицензированию и устройству.](https://docs.microsoft.com/dynamics365/mixed-reality/guides/requirements)

1. [Лицензия для Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
1. [Power BI](https://powerbi.microsoft.com/desktop/)
1. [Рекомендации](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup)
