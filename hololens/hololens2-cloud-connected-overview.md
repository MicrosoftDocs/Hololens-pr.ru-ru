---
title: Обзор cloud connected HoloLens 2 with Remote Assist
description: Узнайте, как зарегистрировать устройства HoloLens 2 в сети Cloud Connected с помощью удаленной помощи Dynamics 365.
keywords: HoloLens, управление, подключение к облаку, удаленная помощь, AAD, Azure AD, MDM, управление мобильными устройствами
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
ms.openlocfilehash: 69b31657a7efaebd5b25b742023dc8767f9c5038
ms.sourcegitcommit: 39424078a75feaf6a1e9b0547cb7d5de9847faf3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "11312642"
---
# Руководстве по развертыванию. Подключенные к облаку устройства HoloLens 2 с удаленной поддержкой — обзор

Это руководство поможет ИТ-специалистам спланировать и развернуть устройства Microsoft HoloLens 2 в своей организации, чтобы эти устройства были готовы к использованию в облаке организации с помощью удаленной поддержки Dynamics 365. Помните, что это будет служить моделью для проверки концепции развертывания в организации в различных случаях использования HoloLens 2.

В этом руководстве мы охаемся регистрации устройств в управлении устройствами, применяем лицензии по мере необходимости и проверяем, могут ли конечные пользователи сразу использовать удаленную помощь при настройке устройства. Для этого мы проймем важные элементы инфраструктуры, необходимые для работы и развертывания в масштабе с помощью HoloLens 2.

![Баннер, подключенный к облаку](./images/cloud-connected-hololens-large.png)

## В этом руководстве

Цель этого руководства — настройка удаленной помощи в организации на устройствах HoloLens. Мы проявим необходимость, необходимую для достижения этой цели. Для поддержания фокуса на этой цели будет предварительно выбрана определенная подготовка и конфигурации для оптимизации развертывания или сокращения элементов, необходимых для настройки. Вы будете знать об этих вариантах и сможете настроить развертывание в зависимости от потребностей вашей компании.

Это настройка, аналогичная сценарию [А.](https://docs.microsoft.com/hololens/common-scenarios#scenario-a)Развертывание на устройствах с облачным подключением, что является хорошим вариантом для многих развертывание с проверкой концепции, которое включает в себя:

- Wi-Fi сети обычно полностью открыты для интернета и облачных служб
- Регистрация в Azure AD с помощью автоматической регистрации MDM — управление MDM (Intune)
- Вход пользователей с помощью собственной корпоративной учетной записи (Azure AD)
  - Поддерживается один или несколько пользователей на устройство
- Различные уровни конфигураций блокировки устройств применяются в зависимости от конкретных случаев использования: от "Полностью открыто" до "Терминал с одним приложением"

![Сценарий с подключением к облаку](./images/cloud-connected-guide-diagram.png)

В этом руководстве не применяются никакие другие ограничения или конфигурации устройств, однако мы рекомендуем изучить эти параметры после завершения работы.

## Узнайте об удаленной помощи

Удаленная помощь позволяет совместно использовать обслуживание и восстановление, удаленную проверку, а также обмен знаниями и обучение. Подключая людей в различных ролях и расположениях, специалист с помощью удаленной поддержки может подключаться к удаленному соавтору в Microsoft Teams. Они могут комбинировать видео, снимки экрана и аннотации для решения проблем в режиме реального времени, даже если они&#39;в одном расположении. Удаленные соавторы могут вставлять эталонные образы, схемы и другие полезные сведения, которые техники&#39;физическое пространство, чтобы они могли ссылаться на схему при работе на HoloLens.

<iframe width="560" height="315" src="https://www.youtube.com/embed/d3YT8j0yYl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## В этом руководстве вы будете:

Подготовьте:

> [!div class="checklist"]
> - [Узнайте об инфраструктуре, необходимой для устройств HoloLens 2.](hololens2-cloud-connected-prepare.md#infrastructure-essentials)
> - [Узнайте больше об Azure AD и задайте его,&#39;его нет.](hololens2-cloud-connected-prepare.md#azure-active-directory)
> - [Узнайте об управлении удостоверениями и о том, как лучше всего настроить учетные записи Azure AD.](hololens2-cloud-connected-prepare.md#identity-management)
> - [Узнайте больше о MDM и настройте Intune, если вы&#39;еще не готовы.](hololens2-cloud-connected-prepare.md#mobile-device-management)
> - [Узнайте о сетевых требованиях удаленной помощи.](hololens2-cloud-connected-prepare.md#network)
> - [Необязательно: VPN для подключения к ресурсам организации](/hololens2-cloud-connected-prepare.md#optional-connect-your-hololens-to-vpn)

Настройте:

> [!div class="checklist"]
> - [Создание пользователей и групп.](hololens2-cloud-connected-configure.md#azure-users-and-groups)
> - [Настройка автоматической регистрации в Azure AD.](hololens2-cloud-connected-configure.md#auto-enrollment-on-hololens-2)
> - [Назначение лицензий на приложения.](hololens2-cloud-connected-configure.md#application-licenses)

Развернем:

> [!div class="checklist"]
> - [Настройка HoloLens 2 и проверка регистрации.](hololens2-cloud-connected-deploy.md#enrollment-validation)
> - [Убедитесь, что вы можете сделать вызов удаленной помощи.](hololens2-cloud-connected-deploy.md#remote-assist-call-validation)

Обслуживание:

> [!div class="checklist"]
> - [Обновление удаленной поддержки с помощью приложения Microsoft Store.](hololens2-cloud-connected-maintain.md#updates)
> - [Создание плана поддержки.](hololens2-cloud-connected-maintain.md#support-plan)
> - [План разработки.](hololens2-cloud-connected-maintain.md#development-plan)

## Дальнейшие действия

> [!div class="nextstepaction"]
> [Развертывание с подключением к облаку — подготовка](hololens2-cloud-connected-prepare.md)

