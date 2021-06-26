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
ms.openlocfilehash: a44247b4afea747e4b75c974fcae344380909989
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923539"
---
# <a name="deployment-guide--cloud-connected-hololens-2-with-remote-assist--overview"></a>Руководство по развертыванию: облачное подключение HoloLens 2 с помощью удаленного помощника — обзор

Это поможет ИТ-специалистам спланировать и развернуть устройства Microsoft HoloLens 2 с помощью удаленной помощи в Организации. Это будет служить моделью для экспериментальных развертываний в Организации в различных вариантах использования HoloLens 2. Программа установки похожа на [сценарий а. Развертывание в устройства Cloud Connect](https://docs.microsoft.com/hololens/common-scenarios#scenario-a). 

В ходе этого руководства мы рассмотрим, как зарегистрировать устройства в управлении устройствами, применить лицензии по мере необходимости и проверить, что конечные пользователи могут немедленно использовать удаленную помощь после настройки устройства. Для этого мы относимся к важным аспектам инфраструктуры, необходимым для настройки и выполнения, обеспечивая развертывание в масштабе с помощью HoloLens 2. В этом пошаговом руководству не будут применяться никакие другие ограничения или конфигурации устройств, но мы рекомендуем изучить эти варианты после завершения.

## <a name="prerequisites"></a>Предварительные требования

Для развертывания HoloLens 2 должна быть выполнена следующая инфраструктура. Если нет, то в этом руководство включена настройка Azure и Intune.

- Wi-Fi
    - Сети обычно открываются в Интернете и в облачных службах.
- Присоединение Azure Active Directory (Azure AD) с автоматической регистрацией MDM (требуется[Подписка Azure AD P1](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) )
- Управление MDM (Intune)
    - Одно или несколько приложений развертываются с помощью MDM.
- Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)
    - Поддерживается одно или несколько пользователей на каждом устройстве.

:::image type="content" alt-text="Сценарий с подключением к облаку" source="./images/deployment-guides-revised-scenario-a.png" lightbox="./images/deployment-guides-revised-scenario-a.png":::


## <a name="learn-about-remote-assist"></a>Дополнительные сведения об удаленной помощи

Служба удаленного помощника позволяет совместное обслуживание и ремонт, удаленную проверку, а также совместное использование и обучение знаний. Подключив людей с разными ролями и расположениями, специалист, использующий удаленную помощь, может подключиться с помощью удаленного участника совместной работы с Microsoft Teams. Они могут сочетать видео, снимки экрана и заметки для решения проблем в реальном времени, даже если они недопустимые&#39;t в одном расположении. Удаленные участники совместной работы могут вставлять эталонные изображения, графики и другие полезные сведения, которые обслуживаются техническим&#39;s, чтобы они могли ссылаться на схематическое руководство, а на HoloLens — без участия.

<iframe width="560" height="315" src="https://www.youtube.com/embed/d3YT8j0yYl0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### <a name="remote-assist-licensing-and-requirements"></a>Лицензирование и требования удаленного помощника

- Учетная запись Azure AD (требуется для приобретения подписки и назначения лицензий)
- [Подписка на удаленную помощь](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist) (или [пробная версия удаленного помощника](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist))
    
#### <a name="dynamics-365-remote-assist-user"></a>Пользователь удаленного помощника Dynamics 365

- Лицензия удаленного помощника
- Сетевое подключение

#### <a name="microsoft-teams-user"></a>Пользователь Microsoft Teams

- Microsoft Teams или [Teams условно](https://products.office.com/microsoft-teams/free).
- Возможность подключения к сети

Если вы планируете реализовать этот [сценарий для разных клиентов](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-overview#scenario-2-leasing-services-to-other-tenants), вам может потребоваться лицензия на информационные барьеры. Ознакомьтесь с [этой статьей](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/cross-tenant-licensing-implementation#step-1-determine-if-information-barriers-are-necessary) , чтобы определить, требуется ли лицензия на информационный барьер.

## <a name="in-this-guide-you-will"></a>В руководстве описаны следующие действия:

Подготовка.

> [!div class="checklist"]
> - [Ознакомьтесь с основными сведениями об инфраструктуре для устройств HoloLens 2.](hololens2-cloud-connected-prepare.md#infrastructure-essentials)
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

