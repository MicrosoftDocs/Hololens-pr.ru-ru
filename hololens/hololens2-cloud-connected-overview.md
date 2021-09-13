---
title: общие сведения о HoloLens 2, подключенных к облаку с помощью удаленного помощника
description: узнайте, как регистрировать устройства HoloLens 2 через облачную сеть с помощью удаленного помощника по Dynamics 365.
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
ms.openlocfilehash: 66e543dd699edbd54ab41474f3ea86fa313bf6ba
ms.sourcegitcommit: e9f746aa41139859edc12fbc21f926c9461da4b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2021
ms.locfileid: "126033520"
---
# <a name="deployment-guide--cloud-connected-hololens-2-with-remote-assist--overview"></a>руководство по развертыванию: облачное подключение HoloLens 2 с помощью удаленного помощника — обзор

это средство поможет специалистам по ит спланировать и развернуть Microsoft HoloLens 2 устройства с помощью удаленной помощи в организации. это будет служить моделью для экспериментальных развертываний в организации в различных HoloLens 2 вариантах использования. Программа установки похожа на [сценарий а. Развертывание в устройства Cloud Connect](common-scenarios.md#scenario-a). 

В ходе этого руководства мы рассмотрим, как зарегистрировать устройства в управлении устройствами, применить лицензии по мере необходимости и проверить, что конечные пользователи могут немедленно использовать удаленную помощь после настройки устройства. Для этого мы перейдем к важным аспектам инфраструктуры, необходимым для настройки и выполнения, обеспечивая развертывание в масштабе с помощью HoloLens 2. В этом пошаговом руководству не будут применяться никакие другие ограничения или конфигурации устройств, но мы рекомендуем изучить эти варианты после завершения.

## <a name="prerequisites"></a>Предварительные требования

Для развертывания HoloLens 2 должна быть выполнена следующая инфраструктура. Если нет, то в этом руководство включена настройка Azure и Intune.

Это программа установки, похожая на ["сценарий а. Развертывание в Cloud Connect Devices](/hololens/common-scenarios#scenario-a)", которая является хорошим вариантом для многих развертываний экспериментов, которые будут включать:

- Обычно Wi-Fi сети полностью открыты для Интернета и облачных служб.
- Присоединение к Azure AD с автоматической регистрацией MDM — управление с помощью MDM (Intune)
- Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)
    - Поддерживаются один или несколько пользователей на каждом устройстве.

:::image type="content" alt-text="Сценарий с подключением к облаку." source="./images/deployment-guides-revised-scenario-a.png" lightbox="./images/deployment-guides-revised-scenario-a.png":::


## <a name="learn-about-remote-assist"></a>Дополнительные сведения об удаленной помощи

Служба удаленного помощника позволяет совместное обслуживание и ремонт, удаленную проверку, а также совместное использование и обучение знаний. Подключив людей в различных ролях и расположениях, специалист, использующий удаленную помощь, может связаться с удаленным совместной работой на Microsoft Teams. Они могут сочетать видео, снимки экрана и заметки для решения проблем в реальном времени, даже если они находятся в разных местах. Удаленные участники совместной работы могут вставлять эталонные изображения, графики и другую полезную информацию, чтобы они могли ссылаться на схематическое руководство, а также не только на HoloLens.

<iframe width="560" height="315" src="https://www.youtube.com/embed/d3YT8j0yYl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### <a name="remote-assist-licensing-and-requirements"></a>Лицензирование и требования удаленного помощника

- Учетная запись Azure AD (требуется для приобретения подписки и назначения лицензий)
- [Подписка на Remote Assist](/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist) (или [пробная версия Remote Assist](/dynamics365/mixed-reality/remote-assist/try-remote-assist))
    
#### <a name="dynamics-365-remote-assist-user"></a>Пользователь Dynamics 365 Remote Assist

- Лицензия Remote Assist
- Сетевое подключение

#### <a name="microsoft-teams-user"></a>Пользователь Microsoft Teams

- Microsoft Teams или [Teams Freemium](https://products.office.com/microsoft-teams/free).
- Возможность подключения к сети

Если вы планируете реализовать этот [сценарий для разных клиентов](/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants), вам может потребоваться лицензия на Информационные барьеры. Чтобы определить, требуется ли лицензия на информационный барьер, ознакомьтесь со статьей [поставщики и клиенты, использующие все возможности удаленного помощника по Dynamics 365](/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation).

## <a name="in-this-guide-you-will"></a>В руководстве описаны следующие действия:

Подготовка.

> [!div class="checklist"]
> - [ознакомьтесь с основными сведениями об инфраструктуре для HoloLens 2 устройств.](hololens2-cloud-connected-prepare.md#infrastructure-essentials)
> - [Узнайте больше об Azure AD и настройте его, если у вас нет&#39;.](hololens2-cloud-connected-prepare.md#azure-active-directory)
> - [Узнайте больше об управлении удостоверениями и о том, как лучше настроить учетные записи Azure AD.](hololens2-cloud-connected-prepare.md#identity-management)
> - [Узнайте больше о MDM и настройте Intune, если вы не&#39;t уже готовы.](hololens2-cloud-connected-prepare.md#mobile-device-management)
> - [Узнайте о требованиях к сети удаленного помощника.](hololens2-cloud-connected-prepare.md#network)
> - [Дополнительно: VPN для подключения к ресурсам Организации](hololens2-cloud-connected-prepare.md#optional-connect-your-hololens-to-vpn)

Настройте следующее.

> [!div class="checklist"]
> - [Создание пользователей и групп.](hololens2-cloud-connected-configure.md#azure-users-and-groups)
> - [Как настроить автоматическую регистрацию в Azure AD.](hololens2-cloud-connected-configure.md#auto-enrollment-on-hololens-2)
> - [Как назначить лицензии приложения.](hololens2-cloud-connected-configure.md#application-licenses)

Развертывание.

> [!div class="checklist"]
> - [настройте HoloLens 2 и проверьте регистрацию.](hololens2-cloud-connected-deploy.md#enrollment-validation)
> - [Проверьте, можно выполнить удаленный вызов помощника.](hololens2-cloud-connected-deploy.md#remote-assist-call-validation)

Обслуживание:

> [!div class="checklist"]
> - [обновление удаленного помощника с помощью Microsoft Store приложения.](hololens2-cloud-connected-maintain.md#updates)
> - [Создание плана поддержки.](hololens2-cloud-connected-maintain.md#support-plan)
> - [План разработки.](hololens2-cloud-connected-maintain.md#development-plan)

## <a name="next-step"></a>Следующий шаг

> [!div class="nextstepaction"]
> [Развертывание с подключением к облаку — подготовка](hololens2-cloud-connected-prepare.md)

