---
title: Пакет подготовки
description: приложение, развертывание приложений, корпоративное приложение demployment, подготовка
keywords: приложение, развертывание приложений, корпоративное приложение demployment, подготовка
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
ms.openlocfilehash: 0803b5f1b77ac7f123d534d101cd24903b87094c
ms.sourcegitcommit: 89ce6cdc0fc6d70a88217791c5f6d613778af614
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "11052586"
---
# Пакет подготовки

Пакеты подготовки можно использовать для подготовки и настройки устройств в среде без доступа к управлению конечными точками. Кроме того, они могут быть развернуты на устройстве независимо от удостоверения пользователя, состояния регистрации, при использовании функции "Исходящие" (OOBE) или путем [применения пакета подготовки во время настройки](https://docs.microsoft.com/hololens/hololens-provisioning##apply-a-provisioning-package-to-hololens-during-setup).

## Общие сведения о пакетах подготовки:
* Приложения, не являющиеся общими
* USB-Загрузка только на полях
* Без автоматического обновления (требуется обновление вручную через PPKGs)

> [!NOTE] 
> Чтобы узнать основы создания пакета подготовки для устройств HoloLens, перейдите на страницу [Подготовка HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning). Чтобы развернуть приложение, необходимо запустить расширенную подготовку. 

> [!NOTE] 
> HoloLens (1-ой gen) имеет ограниченную поддержку установки приложений (**UniversalAppInstall**) с помощью пакета подготовки. Устройства HoloLens (1-го поколения) поддерживают только установку приложения с помощью PPKG только во время OOBE и только при установке контекста пользователя.

## Настройка

В [конструкторе конфигураций Windows](https://www.microsoft.com/store/productId/9NBLGGH4TX22) выполните действия, описанные ниже 4.

1. Установите для ApplicationManagement/AllowAllTrustedApps значение "Да". Смотрите: [ApplicationManagement/AllowAllTrustedApps](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps).
2. В разделе **UniversalAppInstall**  >  **UserContextAppLicense** введите **PackageFamilyName**. Смотрите [UniversalAppInstall](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall). Смотрите также: [UserContextAppLicense](https://docs.microsoft.com/windows/configuration/wcd/wcd-universalappinstall#usercontextapplicense).
    - Если вы не знаете это, вы можете использовать портал устройств на устройстве, на котором уже установлено приложение. Перейдите на страницу "приложения" и ознакомьтесь со строкой "PackageRelativeID", а также сведениями до "!". **PackageFamilyName**.
3. Вы увидите, что у вас новый раздел, **ApplicationFile**. Используйте эту область для отправки пакета Appx. 
4. В зависимости от того, приобрели ли вы приложение или создали собственное бизнес-приложение, вам нужно будет загрузить файл лицензии или сертификат безопасности.
    - Для файла лицензии: в разделе **UniversalAppInstall**  >  **UserContextAppLience** и перейдите в папку, в которой находится лицензия, и отправьте ее. 
    - В разделе "файл безопасности" перейдите в раздел " **Сертификаты** " и выберите сертификат, который нужно установить вместе с пакетом Appx. 

Не забудьте сохранить проект в безопасном месте. Затем **экспортируйте** его как **пакет подготовки**.  
    
Дополнительные сведения: [Применение пакета provisiong к HoloLens](https://docs.microsoft.com/hololens/hololens-provisioning#apply-a-provisioning-package-to-hololens-during-setup).
