---
title: Соответствие требованиям HoloLens 2 и GDPR
description: Документация по GDPR
keywords: HoloLens, GDPR, конфиденциальность, личных данных
author: joyjaz
ms.author: v-jjaswinski
ms.reviewer: skerewala, evmiller
ms.date: 02/05/2021
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 8b795513d83c9d23f70b8dd8365e703d1fc43a51
ms.sourcegitcommit: 76a99370ab841c06e533cc2f4a0c78c1fb7eac70
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "11324880"
---
# Заявление о конфиденциальности HoloLens 2

Одним из основных элементов GDPR является "защита данных по дизайну". Эта концепция особенно применима к мобильным устройствам, таким как HoloLens 2, из-за их переносимости, неограниченного количества подключений к Интернету и открытых каналов связи. В результате безопасность HoloLens 2 [](https://docs.microsoft.com/hololens/security-architecture) была изменена, чтобы обеспечить расширенные, инновационные средства защиты безопасности и конфиденциальности, включив в себя как подход Корпорации Майкрософт к конфиденциальности, так и нормативные акты [GDPR.](https://privacy.microsoft.com/)

 >[!NOTE]
> Этот документ не относится к HoloLens (1-е поколения).

## Обзор конфиденциальности

HoloLens 2 — это автономный компьютер с Windows под управлением Windows Holographic, на котором запускаются приложения и решения в иммерсивной смешанной реальности. Его можно использовать в качестве безопасного автономного устройства или развернуть в качестве управляемого [устройства](https://docs.microsoft.com/mem/intune/fundamentals/windows-holographic-for-business) в организации. Чтобы понять, как HoloLens 2 и Майкрософт используют и защищают ваши данные, см. следующие ссылки:
1. [Заявление о конфиденциальности (Майкрософт) — HoloLens](https://privacy.microsoft.com/privacystatement) — разоритет раздел **"Корпоративный"** и "Разработчик" в левом меню навигации и выберите программное обеспечение и устройства для разработчиков. **** Перейдите в раздел **HoloLens.**
2.  [Windows 10 и веб-службы](https://privacy.microsoft.com/windows10privacy)
3.  [Руководство "Windows 10 и соответствие требованиям к конфиденциальности"](https://docs.microsoft.com/windows/privacy/windows-10-and-privacy-compliance)
4.  [Конфиденциальность и персональные данные в Intune](https://docs.microsoft.com/mem/intune/protect/privacy-personal-data)

## Сетевая безопасность
После распространенных сценариев развертывания HoloLens [2](https://docs.microsoft.com/hololens/common-scenarios)ваши данные будут защищены соответствием мирового класса [Azure](https://docs.microsoft.com/azure/compliance/) наряду с интеграцией юридических и нормативных стандартов. Если вы не впервые в Azure AD и Dynamics 365 Remote Assist, ознакомьтесь с контрольным списком готовности к подотчетности Azure и [Dynamics 365 в GDPR.](https://docs.microsoft.com/compliance/regulatory/gdpr-arc-azure-dynamics)

Кроме того, Защитник Windows брандмауэр предоставляет критически важные функции для защиты подключения устройств. При использовании HoloLens 2 брандмауэр всегда включен, и возможность отключить его программными средствами или с помощью пользовательского интерфейса не предусмотрена. При развертывании HoloLens 2 в качестве управляемого устройства с помощью [Intune](https://docs.microsoft.com/mem/intune/protect/device-compliance-get-started)доступны дополнительные функции обеспечения соответствия требованиям благодаря интеграции конечной точки с [Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/advanced-threat-protection) как решение Mobile Threat Defense. 

Узнайте больше о безопасности и архитектуре HoloLens [2.](https://docs.microsoft.com/hololens/security-architecture)

## Безопасность ОС
Обновления обновляются автоматически (по умолчанию), поэтому HoloLens 2 всегда находится в курсе последних выпусков Windows Holographic и всех установленных приложений. Чтобы узнать больше о том, как защищена наша ОС, см. следующие следующую информацию:
1. [Разделение состояний и изоляция](https://docs.microsoft.com/hololens/security-state-separation-isolation)
1. [Операционная система, не защищенная администратором](https://docs.microsoft.com/hololens/security-adminless-os)
1. [Ограничение использования паролей](https://docs.microsoft.com/hololens/security-limiting-password-use)

## Физическая безопасность
HoloLens 2 имеет память флэш-памяти, защищенную шифрованием [BitLocker.](https://docs.microsoft.com/hololens/security-encryption-data-protection) Устройство и его локальные данные можно перехитрить в автономном режиме с помощью компаньона [advanced Recovery Companion](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8#activetab=pivot:overviewtab) или удаленно стереть с помощью MDM, если оно было развернуто как управляемое устройство.

## Защита данных
Обновления Windows запускаются автоматически (по умолчанию), а интеграция [Azure](https://docs.microsoft.com/hololens/security-encryption-data-protection#Azure-integration) защищает данные, которые перемещаются между собой и облаком. 

При развертывании HoloLens 2 на внешних клиентах удаленная помощь [Dynamics 365](https://docs.microsoft.com/hololens/hololens2-deployment-guide) гарантирует, что конфиденциальные данные и ресурсы компании являются как отдельными, так и безопасными. 

Совместное использование диагностических данных с корпорацией Майкрософт может быть вручную настроено MDM или пользователем во время OOBE. Существует два варианта: необязательные диагностические данные и необходимые диагностические данные. Если исходный параметр диагностики необходимо изменить позже для устранения неполадок, пользователь может изменить его в параметрах **-> Конфиденциальность -> Diagnostics & Feedback** или ИТ-администратор (MDM), если это управляемое устройство. Узнайте больше о [диагностике, отзывах и конфиденциальности в Windows 10.](https://support.microsoft.com/windows/diagnostics-feedback-and-privacy-in-windows-10-28808a2b-a31b-dd73-dcd3-4559a5199319)

> [!Important]
> Журналы диагностики устройств содержат персональные данные (PII), например о процессах или приложениях, которые пользователь начинает во время типичных операций. Если устройство HoloLens совместно используется несколькими пользователями (например, пользователи входить на одно устройство с помощью различных учетных записей Microsoft Azure Active Directory (Azure AD), журналы диагностики могут содержать сведения о pii, которые применяются к нескольким пользователям.

 

Существует несколько [методов сбора данных](https://docs.microsoft.com/hololens/hololens-diagnostic-logs) и политик хранения данных для сбора диагностических данных с HoloLens 2.  Дополнительные сведения о том, как корпорация Майкрософт собирает и использует диагностические данные, см. в заявлении [о](https://privacy.microsoft.com/privacystatement) конфиденциальности (диагностика) **Windows** в левом меню навигации и выборе **"Диагностика".** Перейдите в **раздел "Диагностика".**
