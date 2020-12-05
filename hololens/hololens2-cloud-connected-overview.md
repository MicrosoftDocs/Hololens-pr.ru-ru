---
title: 'Руководство по развертыванию: Облако подключено к HoloLens 2 с удаленным помощником "Обзор"'
description: Регистрация устройств HoloLens в сети, подключенной к облаку
keywords: HoloLens, управление, Облако подключено, Remote Assist, AAD, Azure AD, MDM, управление мобильными устройствами
author: evmill
ms.author: v-evmill
ms.reviewer: aboeger
ms.date: 12/04/2020
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: ba3f826360f999a72e671166af7a19d19ce9c567
ms.sourcegitcommit: 8e2c268733adce2662bf320cf96ccfea5919425e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2020
ms.locfileid: "11196370"
---
# Руководство по развертыванию: Облако подключено к HoloLens 2 с удаленным помощником — обзор

Это руководство поможет ИТ-специалистам планировать и развертывать устройства Microsoft HoloLens 2 в своей организации с помощью общей цели, связанной с тем, что эти устройства подключены к вашей организации с помощью Dynamics 365 Remote Assist готово к использованию. Имейте в виду, что это будет служить моделью развертывания экспериментов в Организации в различных вариантах использования HoloLens 2.

В руководстве мы постараемся зарегистрировать устройства в управлении устройствами, применить лицензии по мере необходимости и подтвердить, что ваши конечные пользователи смогут сразу же использовать удаленную помощь при настройке устройства. Для этого мы рассмотрим важные компоненты инфраструктуры, необходимые для настройки и выполнения развертывания в масштабе с помощью HoloLens 2.

## В этом руководстве

Это руководство содержит определенную цель настройки удаленной помощи в вашей организации на устройствах HoloLens. Мы рассмотрим Necessities, необходимые для достижения этой цели. Чтобы настроить фокус на этой цели, необходимо предварительно выбрать определенные подготовительные действия и конфигурации для оптимизации развертывания или уменьшения количества элементов, необходимых для настройки. Вы будете получать уведомления об этих вариантах, а также настраивать развертывание в соответствии с бизнес-потребностями.

Это настройка аналогична [сценарию a: развертывание на облачные устройства](https://docs.microsoft.com/hololens/common-scenarios#scenario-a), что является хорошим вариантом для многих развертываний концепций, которые будут включать:

- Обычно сети Wi-Fi полностью открыты для Интернета и облачных служб.
- Присоединение к Azure AD с автоматическим регистрацией MDM — управление MDM (Intune)
- Вход в систему с помощью своей корпоративной учетной записи (AAD)
  - Поддерживается один или несколько пользователей на устройстве
- Различные уровни конфигураций блокировки устройств применяются на основании конкретных вариантов использования, начиная с полного открытия на единое приложение

![Сценарий с подключением к облаку](./images/cloud-connected-deployment-chart.png)

В этом руководстве не будут применяться дополнительные ограничения на устройства или конфигурации, но мы рекомендуем ознакомиться с этими параметрами после завершения работы.

## Сведения об удаленном помощнике

Функция Remote Assist позволяет проводить совместное обслуживание и ремонт, удаленную инспекцию, а также предоставлять общий доступ к материалам и обучение. Подключив пользователей в разных ролях и расположениях, вы сможете подключиться к службе удаленного взаимодействия в Microsoft Teams с помощью удаленного помощника. Они могут сочетать видео, снимки экрана и заметки для разрешения проблем в реальном времени, даже если они пользующимися&#39;t в том же месте. Удаленные участники могут вставлять эталонные изображения, схематическое и другие полезные данные, которые обслуживаются специалистами по&#39;s, чтобы они могли ссылаться на схематичные и видеоматериалы на HoloLens и без руки.

<iframe width="560" height="315" src="https://www.youtube.com/embed/d3YT8j0yYl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## В этом руководстве вы сможете:

Подготовку

> [!div class="checklist"]
> - [Узнайте об основных возможностях инфраструктуры для устройств HoloLens 2.](hololens2-cloud-connected-prepare.md#infrastructure-essentials)
> - [Узнайте больше о AAD и настройте его, если у вас&#39;нет.](hololens2-cloud-connected-prepare.md#azure-active-directory)
> - [Узнайте о том, как управлять удостоверениями и как лучше настраивать учетные записи AAD.](hololens2-cloud-connected-prepare.md#identity-management)
> - [Ознакомьтесь с дополнительными сведениями о MDM и настройте ее с помощью Intune, если у вас&#39;уже есть.](hololens2-cloud-connected-prepare.md#mobile-device-management)
> - [Узнайте о требованиях к сети удаленного помощника.](hololens2-cloud-connected-prepare.md#network)
> - [Дополнительно: VPN для подключения к ресурсам Организации](/hololens2-cloud-connected-prepare.md#optional-connect-your-hololens-to-vpn)

Строил

> [!div class="checklist"]
> - [Создание пользователей и групп.](hololens2-cloud-connected-configure.md#azure-users-and-groups)
> - [Как настроить автоматическую регистрацию в AAD.](hololens2-cloud-connected-configure.md#auto-enrollment-on-hololens-2)
> - [Назначение лицензий приложения.](hololens2-cloud-connected-configure.md#application-licenses)

Внедрять

> [!div class="checklist"]
> - [Настройте HoloLens 2 и проверяйте регистрацию.](hololens2-cloud-connected-deploy.md#enrollment-validation)
> - [Убедитесь, что вы можете позвонить удаленному помощнику.](hololens2-cloud-connected-deploy.md#remote-assist-call-validation)

Сохранить

> [!div class="checklist"]
> - [Обновление удаленного помощника с помощью приложения Microsoft Store.](hololens2-cloud-connected-maintain.md#updates)
> - [Создание плана поддержки.](hololens2-cloud-connected-maintain.md#support-plan)
> - [План развития.](hololens2-cloud-connected-maintain.md#development-plan)

## Дальнейшие действия

> [!div class="nextstepaction"]
> [Развертывание с подключением к облаку — подготовка](hololens2-cloud-connected-prepare.md)

