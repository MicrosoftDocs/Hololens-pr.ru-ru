---
title: Руководство по развертыванию
description: Руководство по развертыванию HoloLens 2 (например, с помощью удаленной помощи)
ms.prod: hololens
ms.sitesec: library
author: pawinfie
ms.author: pawinfie
ms.topic: article
ms.localizationpriority: medium
ms.date: 1/7/2021
ms.custom: ''
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens 2
ms.openlocfilehash: 0cd75fdbe5f6a4e6da87770768ce9f22bce491c0
ms.sourcegitcommit: 58bffba63ed581351d80d13b1437aca74d7ed64a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "11266380"
---
# Развертывание HoloLens 2 на внешних клиентах с помощью удаленной помощи

Этот документ помогает ИТ-юристам планировать и развертывать устройства HoloLens 2, уделяя особое внимание удаленной помощи. [Узнайте больше об удаленной помощи.](https://docs.microsoft.com/hololens/hololens2-cloud-connected-overview#learn-about-remote-assist)

## Описание сценария

В этом документе компания Contoso хочет погружать устройство HoloLens 2 на завод внешнего клиента для краткосрочного или долгосрочного использования. Когда клиенту требуется помощь в обслуживании, он входит на устройство HoloLens 2, используя учетные данные компании Contoso, и использует удаленную поддержку для связи со специалистами компании Contoso.

### Требования для этого сценария

1. [Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
1. Диспетчер мобильных устройств , например [Intune](https://docs.microsoft.com/mem/intune/fundamentals/free-trial-sign-up)
1. Лицензия для Удаленной поддержки
    1. [Покупка удаленной помощи](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-remote-assist)
    1. [Пробная удаленная помощь](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist)

## Общие проблемы

- [Как убедиться, что внешние клиенты не могут взаимодействовать друг с другом](#how-to-ensure-that-external-clients-do-not-have-the-ability-to-communicate-with-one-another)
- [Как гарантировать, что клиенты не имеют доступа к ресурсам компании](#how-to-ensure-that-clients-do-not-have-access-to-company-resources)
- [Ограничение приложений](#how-to-restrict-apps)
- [Управление паролями](#how-to-manage-passwords)
- [Как убедиться, что клиенты не имеют доступа к истории чата](#how-to-ensure-that-clients-do-not-have-access-to-chat-history)

### Как убедиться, что внешние клиенты не могут взаимодействовать друг с другом

Так как вызовы HoloLens удаленной помощи и HoloLens не поддерживаются, клиенты могут искать, но не могут взаимодействовать друг с другом. Чтобы еще больше ограничить пользователей, которые могут искать и  [звонить,](https://docs.microsoft.com/microsoft-365/compliance/information-barriers?view=o365-worldwide) информационные барьеры могут ограничивать пользователей, с которыми клиент может взаимодействовать. Другой вариант, который следует рассмотреть, — использование поиска [в каталоге с за областью действия](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search)

 > [!NOTE]
> Так как единый вход включен, важно отключить браузер с помощью [**WDAC.**](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) Если внешний клиент открывает браузер и использует веб-версию Teams, у клиента будет доступ к истории вызовов и чатов.

### Как гарантировать, что клиенты не имеют доступа к ресурсам компании

Существует два варианта, которые следует учитывать.

Первый вариант — многоуровневый подход:

1. Назначать только лицензии, необходимые пользователю. Если вы не назначите пользователю OneDrive, Outlook, SharePoint, Yammer и т. д., у него не будет доступа к этим ресурсам. Пользователям потребуется только лицензии удаленной поддержки, Intune и AAD.
1. Блокируют приложения (например, электронную почту), к ним не должны получать доступ клиенты [(см. "Как ограничить доступ к приложениям").](#how-to-restrict-apps)
1. Не делиться именами пользователей и паролями с клиентами. Для входа в HoloLens 2 требуется электронное письмо и числовой ПИН-код.

Второй вариант — создать отдельный клиент, в котором размещены клиенты (см. изображение 1.1).

**Изображение 1.1**

![Образ клиента службы](./images/hololens-service-tenant-image.png)

### Ограничение приложений

[Режим терминала](https://docs.microsoft.com/hololens/hololens-kiosk) и(или) [WDAC (Защитник Windows Application Control)](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) — это параметры для ограничения приложений.

### Управление паролями

1. Удаление срока действия пароля. Однако это повышает вероятность компрометации учетной записи. Рекомендация NIST в отношении паролей это изменение паролей каждые 30-90 дней.
1. Срок действия пароля для устройств HoloLens 2 должен превышать 90 дней.
1. Устройства должны быть возвращены в Contoso для изменения паролей. Однако это может привести к проблемам, если ожидается, что устройства находятся на заводе клиента в течение 90 и более дней.  
1. Для устройств, которые отправляются на несколько клиентов, сбросйте пароли перед отправкой устройства клиентам.

### Как убедиться, что клиенты не имеют доступа к истории чата

Удаленная помощь очищает историю чата после каждого сеанса. Однако для пользователя Microsoft Teams будет доступна история чатов.

> [!NOTE]
> Так как единый вход включен, важно отключить браузер с помощью [**WDAC.**](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) Если внешний клиент открывает браузер и использует веб-версию Teams, у клиента будет доступ к истории вызовов и чатов.

## Общие рекомендации и инструкции по развертыванию

Для развертывания HoloLens 2 рекомендуется следующее:

1. Используйте последний [выпуск ОС HoloLens](https://aka.ms/hololens2download) в качестве базовой сборки.
1. Назначьте лицензии на основе пользователей или устройств:
    1. Для лицензий на основе пользователей и устройств необходимо выполнять следующие действия.
        1. [Создайте группу в AAD и добавьте участников](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal#create-a-basic-group-and-add-members) для пользователей HoloLens/RA.
        1. [Назначьте этой группе лицензии](https://docs.microsoft.com/azure/active-directory/enterprise-users/licensing-groups-assign#:~:text=In%20this%20article%201%20Assign%20the%20required%20licenses,3%20Check%20for%20license%20problems%20and%20resolve%20them) на основе устройств или пользователей.
        1. (Необязательно) Можно нацелить группы для политик MDM.

1. Устройства должны присоединяться к вашему арендатору с помощью [AAD,](https://docs.microsoft.com/hololens/hololens-enroll-mdm#auto-enrollment-in-mdm)автоматически регистрироваться и настраиваться с помощью [автоматического пилотного проекта.](https://docs.microsoft.com/hololens/hololens2-autopilot)
    1. Обратите внимание, что первым пользователем на устройстве будет владелец устройства.
    1. Обратите внимание, что если устройство присоединилось к AAD, то пользователь, который выполнил это присоединить устройство, будет владельцем устройства.
    1. Дополнительные см. [в под этой теме.](https://docs.microsoft.com/hololens/security-adminless-os#device-owner)
1. [Клиент блокирует](https://docs.microsoft.com/hololens/hololens-release-notes#tenantlockdown-csp-and-autopilot) устройство, чтобы оно можно было присоединять только к вашему арендатору.
    1. **Дополнительная ссылка: CSP** [блокировки клиента.](https://docs.microsoft.com/windows/client-management/mdm/tenantlockdown-csp)
1. Настройка терминала с использованием глобального назначенного доступа к [этой области.](https://docs.microsoft.com/hololens/hololens-global-assigned-access-kiosk)
1. Мы рекомендуем отключить возможности, которые следуют (необязательные):
    1. Возможность переналожить устройство в режим [разработчика.](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock)
    1. Возможность подключения HoloLens к компьютеру для копирования даты [отключена USB.](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowusbconnection)
       > [!NOTE]
        > Если вы не хотите отключать USB, но хотите применить пакеты подготовка к устройству с помощью USB, следуйте инструкциям, указанным [**здесь.**](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)

1. Используйте [WDAC,](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) чтобы разрешить или использовать черные приложения на устройстве HoloLens 2.
1. Обновим удаленную помощь до последней версии в рамках установки. Это можно сделать двумя вариантами:
    1. Для этого можно ходить в Windows **Microsoft Store --> Удаленная помощь --> и обновить приложение.**
    1. Другой способ — оставить HoloLens 2 подключенным в ночное время для автоматического обновления.
1. [Отключать все страницы параметров,](https://docs.microsoft.com/hololens/settings-uri-list) кроме сетевых параметров, чтобы разрешить пользователям подключаться к гостевых сетях на клиентских сайтах.
1. [Управление обновлениями HoloLens](https://docs.microsoft.com/hololens/hololens-updates)
    1. Возможность управления [обновлениями ОС или](https://docs.microsoft.com/mem/intune/protect/windows-update-for-business-configure#create-and-assign-update-rings) возможность свободного потока.
1. [Общие ограничения устройств.](https://docs.microsoft.com/hololens/hololens-common-device-restrictions)
