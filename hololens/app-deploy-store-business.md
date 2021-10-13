---
title: Microsoft Store для бизнеса
description: узнайте, как работать с Microsoft Store для бизнеса для публикации приложений смешанной реальности в бизнесе.
keywords: Microsoft Store для бизнеса, мсфб, развертывание приложений, магазин
author: evmill
ms.author: v-evmill
ms.date: 10/13/2021
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
ms.openlocfilehash: 5bc719539aaa254b8aacb05e24554152231f7e5a
ms.sourcegitcommit: 9574db58592b7302bd2386bdf7fda3f6721de818
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2021
ms.locfileid: "129924324"
---
# <a name="microsoft-store-for-business"></a>Microsoft Store для бизнеса

эта [Microsoft Store для бизнеса](/microsoft-store/microsoft-store-for-business-overview) разработана главным образом для ит-руководителей и администраторов в организациях и предприятиях с помощью гибкого способа поиска, получения, управления и распространения бесплатных и платных приложений на выбранных рынках для Windows 10 устройств в томе. 

вы можете управлять Microsoft Store приложениями и частными бизнес-приложениями в одном средстве инвентаризации, а также назначать и повторно использовать лицензии по мере необходимости. вы также можете выбрать оптимальный метод распространения для вашей организации: напрямую назначать приложения отдельным пользователям и группам, публиковать приложения на частных страницах в Microsoft Store или подключаться к решениям управления для получения дополнительных параметров.

если Microsoft Store для бизнеса используется конечным пользователем, он запустит приложение Microsoft Store. После запуска пользователь сможет выбрать вкладку с именем своей организации, после чего будут представлены приложения, доступные для них или устройства.

> [!Note]
> Microsoft Store для бизнеса не скачивает автоматически приложения (push-уведомления) на устройствах. однако приложения из Microsoft Store для бизнеса могут быть связаны с сервером управления устройствами (MDM) для целевой платформы и синхронизации приложений с устройствами.

дополнительные сведения об использовании Microsoft Store для бизнеса см. на следующих страницах:

* [Уровни разрешений, используемые для установки приложений](/mem/intune/configuration/device-restrictions-windows-holographic#app-store)
* [Как добавить приложение в магазин для бизнеса](/mem/intune/apps/store-apps-windows)
* [Назначение приложений группам сотрудников](/mem/intune/apps/windows-store-for-business)

чтобы связать Microsoft Store для бизнеса, перейдите на страницу [связывание Microsoft Store для бизнеса с Intune](/mem/intune/apps/windows-store-for-business#associate-your-microsoft-store-for-business-account-with-intune).

> [!Tip]
> дополнительные сведения о [распределении автономных приложений](/microsoft-store/distribute-offline-apps) при использовании таких приложений, как расширенный помощник по восстановлению (ARC) и конструктор конфигураций Windows (WCD).

## <a name="use-only-private-store-apps-for-microsoft-store"></a>Используйте только приложения частного магазина для Microsoft Store

- введено в [Windows holographic, version 21H2](hololens-release-notes.md#windows-holographic-version-21h2).

Политика Рекуиреприватестореонли включена для HoloLens. эта политика позволяет настроить приложение Microsoft Store для отображения только частного хранилища, настроенного для вашей организации. Ограничение доступа только для приложений, которые были сделаны доступными.

Дополнительные сведения о [аппликатионманажемент и рекуиреприватестореонли](http://windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)

## <a name="smart-retry-for-app-updates"></a>Интеллектуальная повторная попытка обновления приложения

- введено в [Windows holographic, version 21H2](hololens-release-notes.md#windows-holographic-version-21h2).

теперь для HoloLens включена новая политика, которая позволяет ит-администраторам устанавливать повторяющуюся или одноразовую дату перезапуска приложений, обновление которых завершилось сбоем из-за того, что приложение в настоящий момент используется, что позволяет применить обновление. Их можно задать на основе нескольких различных триггеров, таких как запланированное время или вход в систему. Дополнительные сведения об использовании этой политики см. в статье [аппликатионманажемент/счедулефорцерестартфорупдатефаилурес](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-scheduleforcerestartforupdatefailures).