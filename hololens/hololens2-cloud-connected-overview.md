---
title: Общие сведения о облачном подключении HoloLens 2 с помощью удаленного помощника
description: Узнайте, как регистрировать устройства HoloLens 2 через облачную сеть с помощью удаленного помощника Dynamics 365.
keywords: HoloLens, управление, облачное подключение, удаленное помощник, AAD, Azure AD, MDM, управление мобильными устройствами
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
ms.openlocfilehash: 43fbcc3a841f6c3f15006f285188e55d22f10599
ms.sourcegitcommit: 29573e577381a23891e9557884a6dfdaac0c1c48
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110397655"
---
# <a name="deployment-guide--cloud-connected-hololens-2-with-remote-assist--overview"></a>Руководство по развертыванию: облачное подключение HoloLens 2 с помощью удаленного помощника — обзор

Это пошаговое руководством помогает ИТ-специалистам планировать и развертывать устройства Microsoft HoloLens 2 в своей организации с общей целью использования облачных устройств, подключенных к вашей организации, с помощью удаленного помощника Dynamics 365, готового к использованию. Помните, что это будет служить моделью для экспериментальных развертываний в вашей организации в различных вариантах использования HoloLens 2.

В рамках руководства мы рассмотрим, как зарегистрировать устройства в управлении устройствами, применить лицензии по мере необходимости и проверить, что конечные пользователи могут немедленно использовать удаленную помощь после настройки устройства. Для этого мы рассмотрим важные компоненты инфраструктуры, необходимые для настройки и запуска, обеспечивая развертывание в масштабе с помощью HoloLens 2.

[![Сценарий ](./images/deployment-guides-revised-scenario-a.png) с подключением к облаку](./images/deployment-guides-revised-scenario-a.png#lightbox)
## <a name="in-this-guide"></a>В этом руководстве

В этом руководством содержится конкретная цель настройки удаленного помощника в Организации на устройствах HoloLens. Мы рассмотрим необходимые условия, необходимые для достижения этой цели. Чтобы поддерживать основное внимание на этой цели, необходимо предварительно выбрать определенную подготовку и конфигурации, чтобы оптимизировать это развертывание или уменьшить количество элементов, необходимых для настройки. Вы будете уведомлены об этих вариантах и можете настроить развертывание в соответствии с потребностями бизнеса.

Это настройка аналогична [сценарию а: развертывание в Cloud Connect Devices](https://docs.microsoft.com/hololens/common-scenarios#scenario-a), что является хорошим вариантом для многих развертываний экспериментов, которые будут включать:

- Обычно Wi-Fi сети полностью открыты для Интернета и облачных служб.
- Присоединение к Azure AD с автоматической регистрацией MDM — управление MDM (Intune)
- Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)
  - Поддерживается один или несколько пользователей на устройство
- Различные уровни конфигурации блокировки устройств применяются на основе конкретных вариантов использования: от полного открытия до одного киоска приложений



В этом пошаговом руководству не будут применяться никакие другие ограничения или конфигурации устройств, но мы рекомендуем изучить эти варианты после завершения.

## <a name="learn-about-remote-assist"></a>Дополнительные сведения об удаленной помощи

Служба удаленного помощника позволяет совместное обслуживание и ремонт, удаленную проверку, а также совместное использование и обучение знаний. Подключив людей с разными ролями и расположениями, специалист, использующий удаленную помощь, может подключиться с помощью удаленного участника совместной работы с Microsoft Teams. Они могут сочетать видео, снимки экрана и заметки для решения проблем в реальном времени, даже если они недопустимые&#39;t в одном расположении. Удаленные участники совместной работы могут вставлять эталонные изображения, графики и другие полезные сведения, которые обслуживаются техническим&#39;s, чтобы они могли ссылаться на схематическое руководство, а на HoloLens — без участия.

<iframe width="560" height="315" src="https://www.youtube.com/embed/d3YT8j0yYl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## <a name="in-this-guide-you-will"></a>В руководстве описаны следующие действия:

Подготовка.

> [!div class="checklist"]
> - [Ознакомьтесь с основными сведениями об инфраструктуре для устройств HoloLens 2.](hololens2-cloud-connected-prepare.md#infrastructure-essentials)
> - [Узнайте больше об Azure AD и настройте его, если у вас нет&#39;.](hololens2-cloud-connected-prepare.md#azure-active-directory)
> - [Узнайте больше об управлении удостоверениями и о том, как лучше настроить учетные записи Azure AD.](hololens2-cloud-connected-prepare.md#identity-management)
> - [Узнайте больше о MDM и настройте Intune, если вы не&#39;t уже готовы.](hololens2-cloud-connected-prepare.md#mobile-device-management)
> - [Узнайте о требованиях к сети удаленного помощника.](hololens2-cloud-connected-prepare.md#network)
> - [Дополнительно: VPN для подключения к ресурсам Организации](/hololens2-cloud-connected-prepare.md#optional-connect-your-hololens-to-vpn)

Настройте следующее.

> [!div class="checklist"]
> - [Создание пользователей и групп.](hololens2-cloud-connected-configure.md#azure-users-and-groups)
> - [Как настроить автоматическую регистрацию в Azure AD.](hololens2-cloud-connected-configure.md#auto-enrollment-on-hololens-2)
> - [Как назначить лицензии приложения.](hololens2-cloud-connected-configure.md#application-licenses)

Развертывание.

> [!div class="checklist"]
> - [Настройте HoloLens 2 и проверьте регистрацию.](hololens2-cloud-connected-deploy.md#enrollment-validation)
> - [Проверьте, можно выполнить удаленный вызов помощника.](hololens2-cloud-connected-deploy.md#remote-assist-call-validation)

Обслуживание:

> [!div class="checklist"]
> - [Обновление удаленного помощника с помощью Microsoft Store приложения.](hololens2-cloud-connected-maintain.md#updates)
> - [Создание плана поддержки.](hololens2-cloud-connected-maintain.md#support-plan)
> - [План разработки.](hololens2-cloud-connected-maintain.md#development-plan)

## <a name="next-step"></a>Следующий шаг

> [!div class="nextstepaction"]
> [Развертывание с подключением к облаку — подготовка](hololens2-cloud-connected-prepare.md)

