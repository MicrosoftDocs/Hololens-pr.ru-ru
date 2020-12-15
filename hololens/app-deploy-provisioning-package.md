---
title: Пакет подготовки
description: приложение, развертывание приложений, детерстика корпоративного приложения, подготовка
keywords: приложение, развертывание приложений, разменая подготовка корпоративных приложений, подготовка
author: evmill
ms.author: v-evmill
ms.date: 6/22/2020
ms.prod: hololens
ms.sitesec: library
ms.topic: article
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 60efc454f9e1221372279401da9f8ee918e061e7
ms.sourcegitcommit: efa3fb7e353c5e56ee467cc7fd94ffdfaf46e2e5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/15/2020
ms.locfileid: "11219226"
---
# Пакет подготовки

Пакеты подготовки можно использовать для подготовки и настройки устройств в среде без доступа к управлению конечными точками. Они также могут быть развернуты на устройстве независимо от удостоверения пользователя, состояния регистрации, во время работы с приостановкой (OOBE) или путем применения пакета подготовка во время [установки.](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup)

## Вопросы, которые следует учитывать при упаковке пакетов.
* Не общедоступные приложения
* Только неогрузка USB
* Автоматическое обновление не требуется (требуется ручное обновление с помощью PPKG)

Приложения, установленные с помощью пакета предоставления, должны быть подписаны сертификатом в локальном хранилище компьютеров. Пакеты предоставления могут устанавливать сертификаты только в хранилище устройства (локального компьютера), поэтому приложение и сертификат могут быть установлены через тот же пакет. Если вы развертываете сертификат из MDM [](certificate-manager.md)или устанавливаете его с помощью диспетчера сертификатов, обязательно разверните сертификат в локальном хранилище компьютеров, чтобы подписать установленные таким образом приложения.

Чтобы узнать основы создания пакета подготовки для устройств HoloLens, посетите сайт [подготовки HoloLens.](https://docs.microsoft.com/hololens/hololens-provisioning) Чтобы развернуть приложение, необходимо начать с расширенных настойки.

> [!NOTE]
> HoloLens (1-е поколения) имеет ограниченную поддержку установки приложений **(UniversalAppInstall)** с помощью пакета подготовка. Устройства HoloLens (1-е поколения) поддерживают установку приложения через PPKG только во время OOBE и только при установке контекста пользователя.

## Настройка

В [конструкторе конфигураций Windows](https://www.microsoft.com/store/productId/9NBLGGH4TX22) необходимо предпринять следующие 4 действия.

1. Задайте для ApplicationManagement/AllowAllTrustedApps "Да". См. [applicationManagement/AllowAllTrustedApps.](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)

2. В **области UniversalAppInstall**  >  **UserContextAppLicense** введите **PackageFamilyName.** См. [universalAppInstall](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall). См. также: [UserContextAppLicense](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).

   Портал устройств можно использовать на устройстве, на которое уже установлено приложение. Посетите страницу "Приложения" и посмотрите на строку PackageRelativeID перед строкой "!" Is your **PackageFamilyName**.
    
3. После этого вы увидите, что у вас есть новый раздел **ApplicationFile.** Используйте эту область для отправки пакета appx.

4. В зависимости от того, приобрели ли вы приложение или создали собственное бизнес-приложение, вам потребуется отправить файл лицензии или сертификат безопасности.

    - Для файла лицензии: в **папке UniversalAppInstall**  >  **UserContextAppLience** перейдите к расположению лицензии и загрузите ее. 
    - Для файла безопасности перейдите к **файлу "Сертификаты"** и выберите сертификат для установки вместе с пакетом APPX.

Обязательно сохраните проект в надежном месте. Затем **экспортировать** его в качестве **пакета предоставления.**  
    
См. также: [применение пакета подготовка к HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).
