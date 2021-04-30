---
title: Соответствие и GDPR HoloLens 2
description: Документация по GDPR
keywords: HoloLens, GDPR, конфиденциальность, PII
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
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309916"
---
# <a name="hololens-2-privacy-statement"></a>Заявление о конфиденциальности HoloLens 2

Одним из основных элементов GDPR является "Защита данных по проектам". Эта концепция особенно применима к мобильным устройствам, таким как HoloLens 2, из-за их переносимости, неограниченного подключения к Интернету и открытия каналов связи. В результате [Безопасность](https://docs.microsoft.com/hololens/security-architecture) HoloLens 2 была переработана для обеспечения расширенной, инновационной защиты и обеспечения конфиденциальности, включая подход корпорации Майкрософт к [конфиденциальности и GDPR нормативам](https://privacy.microsoft.com/).

 >[!NOTE]
> Этот документ не относится к HoloLens (1-й общий).

## <a name="privacy-overview"></a>Обзор конфиденциальности

HoloLens 2 — это автономный компьютер Windows, работающий под управлением Windows holographic, который запускает приложения и решения в реальной среде смешанной реальности. Его можно использовать в качестве защищенного автономного устройства или развертывания в качестве [управляемого устройства](https://docs.microsoft.com/mem/intune/fundamentals/windows-holographic-for-business) в Организации. Ознакомьтесь со следующими ссылками, чтобы понять, как HoloLens и корпорация Майкрософт используют и защищают ваши данные:
1. [Заявление о конфиденциальности Майкрософт — HoloLens](https://privacy.microsoft.com/privacystatement) — разверните раздел " **предприятие и разработчик** " в левом меню навигации и выберите " **Корпоративные и программное обеспечение и устройства для разработчиков**". Перейдите к разделу **HoloLens** .
2.  [Windows 10 и веб-службы](https://privacy.microsoft.com/windows10privacy)
3.  [Рекомендации по соответствию конфиденциальности Windows 10 &](https://docs.microsoft.com/windows/privacy/windows-10-and-privacy-compliance)
4.  [Конфиденциальность и персональные данные в Intune](https://docs.microsoft.com/mem/intune/protect/privacy-personal-data)

## <a name="network-security"></a>Безопасность сети
Следуя [общим сценариям по развертыванию](https://docs.microsoft.com/hololens/common-scenarios)HoloLens 2, ваши данные будут защищаться с учетом [соответствия требованиям мирового уровня в Azure](https://docs.microsoft.com/azure/compliance/) , а также с юридической и законодательной интеграцией. Если вы не знакомы с Azure AD и удаленным помощником по Dynamics 365, Составьте ссылку на [Контрольный список готовности к использованию Azure и dynamics 365 для GDPR](https://docs.microsoft.com/compliance/regulatory/gdpr-arc-azure-dynamics).

Кроме того, брандмауэр защитника Windows предоставляет важные функции для защиты подключения устройств. При использовании HoloLens 2 брандмауэр всегда включен, и нет способов отключить его программно или через пользовательский интерфейс. При развертывании HoloLens 2 в качестве управляемого устройства с помощью [Intune](https://docs.microsoft.com/mem/intune/protect/device-compliance-get-started)становятся доступны дополнительные функции обеспечения соответствия с интеграцией для [конечной точки с Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/advanced-threat-protection) в качестве решения для защиты мобильных устройств от угроз. 

Узнайте больше о [безопасности и архитектуре](https://docs.microsoft.com/hololens/security-architecture)HoloLens 2.

## <a name="os-security"></a>Безопасность ОС
Обновления выполняются автоматически (по умолчанию), поэтому HoloLens 2 всегда обновляется последним выпуском Windows holographic и всех установленных приложений. Чтобы узнать больше о том, как обеспечивается безопасная версия операционной системы, ознакомьтесь со следующими сведениями.
1. [Разделение и изоляция состояний](https://docs.microsoft.com/hololens/security-state-separation-isolation)
1. [Операционная система без прав администратора](https://docs.microsoft.com/hololens/security-adminless-os)
1. [Ограничение использования пароля](https://docs.microsoft.com/hololens/security-limiting-password-use)

## <a name="physical-security"></a>Физическая безопасность
HoloLens 2 имеет флэш-память, защищенную [шифрованием BitLocker](https://docs.microsoft.com/hololens/security-encryption-data-protection). Ваше устройство и его локальные данные могут быть отключены от сети с помощью [расширенного помощника по восстановлению](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8#activetab=pivot:overviewtab) или удаленно ОЧИЩАТЬ через MDM, если он был развернут как управляемое устройство.

## <a name="data-protection"></a>Защита данных
Обновления Windows запускаются автоматически (по умолчанию), а [Интеграция Azure](https://docs.microsoft.com/hololens/security-encryption-data-protection#Azure-integration) обеспечивает защиту данных, передаваемых между собой и облаком. 

При развертывании HoloLens 2 на внешних клиентах [Служба удаленного помощника Dynamics 365](https://docs.microsoft.com/hololens/hololens2-deployment-guide) гарантирует, что ваши конфиденциальные данные организации и ресурсы будут как самостоятельными, так и надежными. 

Совместное использование диагностических данных с Майкрософт может быть вручную настроено MDM или пользователем во время OOBE. Существует два варианта: необязательные диагностические данные и необходимые диагностические данные. Если исходный параметр диагностики необходимо изменить позже для устранения неполадок, он может быть изменен пользователем в окне " **Параметры" — > "Диагностика конфиденциальности >" & "Отзывы** " или "Администратор ИТ" (MDM), если является управляемым устройством. См. Дополнительные сведения о [диагностике, отзыве и конфиденциальности в Windows 10](https://support.microsoft.com/windows/diagnostics-feedback-and-privacy-in-windows-10-28808a2b-a31b-dd73-dcd3-4559a5199319).

> [!Important]
> В журналах диагностики устройств содержатся персональные данные (PII), например сведения о том, какие процессы или приложения пользователь запускает во время стандартных операций. Если несколько пользователей совместно используют устройство HoloLens (например, пользователи входят на одно устройство, используя разные учетные записи Microsoft Azure Active Directory (Azure AD)), журналы диагностики могут содержать персональные данные, относящиеся к нескольким пользователям.

 

Для сбора диагностических данных из HoloLens 2 существует [несколько методов сбора данных и политик хранения](https://docs.microsoft.com/hololens/hololens-diagnostic-logs) .  Дополнительные сведения о том, как корпорация Майкрософт собирает и использует диагностические данные, см. в разделе [заявление о конфиденциальности Майкрософт — диагностика](https://privacy.microsoft.com/privacystatement) — разверните **окна** в меню навигации слева и выберите **Диагностика**. Перейдите к разделу **Диагностика** .
