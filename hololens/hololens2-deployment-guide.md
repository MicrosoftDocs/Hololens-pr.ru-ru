---
title: Руководство по развертыванию внешних клиентов
description: Руководство по развертыванию для HoloLens 2 для внешних клиентов (например, с помощью удаленной помощи)
ms.prod: hololens
ms.sitesec: library
author: pawinfie
ms.author: pawinfie
ms.topic: article
ms.localizationpriority: medium
ms.date: 1/12/2021
ms.custom: ''
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens 2
ms.openlocfilehash: 56930ceea05cd5713b9c7eb57e0967a9d0cd4988
ms.sourcegitcommit: fbc8ddb17e31fea8667ece43a511592b86ac3947
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "11385591"
---
# <a name="deploying-hololens-2-to-external-clients-with-remote-assist"></a>Развертывание HoloLens 2 на внешних клиентах с помощью удаленной поддержки

Это руководство помогает ИТ-специалистам с помощью следующих целей развернуть устройства Microsoft HoloLens 2 в своей организации:

1. Облачное подключение устройств HoloLens 2
1. Ссуда устройств HoloLens 2 внешним клиентам для использования
1. Безопасные устройства с заемными средствами

В этом руководстве будут действовать общие рекомендации по развертыванию [HoloLens 2,](#general-deployment-recommendations-and-instructions) [](#common-concerns) применимые к большинству сценариев развертывания HoloLens 2, а также общие проблемы, которые у клиентов есть при развертывании удаленной помощи для внешнего использования.

## <a name="scenario-description"></a>Описание сценария

Для этого документа компания Contoso хочет посадить устройство HoloLens 2 на завод внешнего клиента для краткосрочного или долгосрочного использования. Когда клиенту требуется оборудование для обслуживания помощи, клиент входит в устройство HoloLens 2 с использованием учетных данных, предоставленных компанией Contoso, и использует remote Assist для контакта с экспертами компании Contoso.

Дополнительные информацию о удаленной помощи [здесь](https://docs.microsoft.com/hololens/hololens2-cloud-connected-overview#learn-about-remote-assist).

### <a name="requirements-for-this-scenario"></a>Требования к этому сценарию

1. [Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
1. Диспетчер мобильных устройств ( [например, Intune)](https://docs.microsoft.com/mem/intune/fundamentals/free-trial-sign-up)
1. Лицензия для Удаленной поддержки
    1. [Покупка удаленной помощи](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-remote-assist)
    1. [Пробная удаленная помощь](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist)

## <a name="common-concerns"></a>Общие проблемы

- [Как убедиться, что внешние клиенты не имеют возможности общаться друг с другом](#how-to-ensure-that-external-clients-do-not-have-the-ability-to-communicate-with-one-another)
- [Как гарантировать, что клиенты не имеют доступа к ресурсам компании](#how-to-ensure-that-clients-do-not-have-access-to-company-resources)
- [Ограничение приложений](#how-to-restrict-apps)
- [Управление паролями](#how-to-manage-passwords)
- [Как убедиться, что клиенты не имеют доступа к истории чата](#how-to-ensure-that-clients-do-not-have-access-to-chat-history)

### <a name="how-to-ensure-that-external-clients-do-not-have-the-ability-to-communicate-with-one-another"></a>Как убедиться, что внешние клиенты не имеют возможности общаться друг с другом

Так как вызовы Удаленной помощи HoloLens и HoloLens не поддерживаются, клиенты могут искать, но не могут общаться друг с другом. Чтобы еще больше ограничить поиск и вызов  [клиентов,](https://docs.microsoft.com/microsoft-365/compliance/information-barriers?view=o365-worldwide) информационные барьеры могут ограничить, с кем клиент может общаться. Другой вариант, который следует рассмотреть, — это использование [поиска scoped Directory](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search)

 > [!NOTE]
> Так как включен один вход, важно отключить браузер с помощью [**WDAC.**](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) Если внешний клиент открывает браузер и использует веб-версию Teams, клиент будет иметь доступ к истории вызовов и чатов.

### <a name="how-to-ensure-that-clients-do-not-have-access-to-company-resources"></a>Как гарантировать, что клиенты не имеют доступа к ресурсам компании

Существует два варианта.

Первый вариант — это многоуровневый подход:

1. Назначьте только необходимые пользователю лицензии. Если пользователь не назначит пользователю OneDrive, Outlook, SharePoint, Yammer и т. д., он не будет иметь доступа к этим ресурсам. Для начала пользователям потребуется только лицензии remote Assist, Intune и AAD.
1. Блокируют приложения (например, электронную почту), к которые клиенты не могут получить доступ (см. как [ограничить приложения).](#how-to-restrict-apps)
1. Не делитесь именами пользователей и паролем с клиентами. Для входа в HoloLens 2 требуется электронная почта и числимый ПИН-код.

Второй вариант — создание отдельного клиента, в котором размещены клиенты (см. рисунок 1.1).

**Изображение 1.1**

![Изображение клиента службы](./images/hololens-service-tenant-image.png)

### <a name="how-to-restrict-apps"></a>Ограничение приложений

[Режим киоска](https://docs.microsoft.com/hololens/hololens-kiosk) [и(или) WDAC (Защитник Windows управления приложениями)](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) — это варианты ограничения приложений.

### <a name="how-to-manage-passwords"></a>Управление паролями

1. Удаление срока действия пароля. Однако это повышает вероятность того, что учетная запись будет скомпрометирована. Рекомендация пароля NIST — это изменение паролей каждые 30-90 дней.
1. Продлить срок действия пароля для устройств HoloLens 2 до 90 дней.
1. Устройства должны быть возвращены в Contoso для изменения паролей. Однако это может вызвать проблемы, если предполагается, что устройства будут на заводе клиента в течение 90 суток.  
1. Для устройств, которые отправляются нескольким клиентам, сбросить пароли перед отправкой устройства клиентам.

### <a name="how-to-ensure-that-clients-do-not-have-access-to-chat-history"></a>Как убедиться, что клиенты не имеют доступа к истории чата

Remote Assist очищает историю чата после каждого сеанса. Однако история чата будет доступна пользователю Microsoft Teams.

> [!NOTE]
> Так как включен один вход, важно отключить браузер с помощью [**WDAC.**](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) Если внешний клиент открывает браузер и использует веб-версию Teams, у клиента будет доступ к истории вызовов и чатов.

## <a name="general-deployment-recommendations-and-instructions"></a>Общие рекомендации и инструкции по развертыванию

Рекомендуем следующие действия развертывания HoloLens 2:

1. Используйте последний [выпуск ОС HoloLens в](https://aka.ms/hololens2download) качестве базовой сборки.
1. Назначение лицензий на основе пользователей или устройств:
    1. Лицензии на основе пользователей и устройств следуют следующим шагам:
        1. [Создайте группу в AAD и добавьте участников](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal#create-a-basic-group-and-add-members) для пользователей HoloLens/RA.
        1. [Назначьте этой группе](https://docs.microsoft.com/azure/active-directory/enterprise-users/licensing-groups-assign#:~:text=In%20this%20article%201%20Assign%20the%20required%20licenses,3%20Check%20for%20license%20problems%20and%20resolve%20them) лицензии на основе устройств или на основе пользователей.
        1. (Необязательный) Можно нацелить группы для политик MDM.

1. Устройства должны быть AAD присоединяться к вашему клиенту, автозарегистрироваться и настраиваться с помощью [автопилотов.](https://docs.microsoft.com/hololens/hololens2-autopilot) [](https://docs.microsoft.com/hololens/hololens-enroll-mdm#auto-enrollment-in-mdm)
    1. Обратите внимание, что первым пользователем на устройстве будет владелец устройства.
    1. Обратите внимание, что если к устройству присоединяется AAD, то пользователь, исполнив его, является владельцем устройства.
    1. Дополнительные дополнительные см. [в см. в этой ленте Владелец устройства.](https://docs.microsoft.com/hololens/security-adminless-os#device-owner)
1. [Клиент блокирует](https://docs.microsoft.com/hololens/hololens-release-notes#tenantlockdown-csp-and-autopilot) устройство таким образом, чтобы оно можно было присоединять только к вашему клиенту.
    1. **Дополнительная ссылка:** [CSP блокировки клиента](https://docs.microsoft.com/windows/client-management/mdm/tenantlockdown-csp).
1. Настройка киоска с использованием глобального назначенного доступа [к здесь](https://docs.microsoft.com/hololens/hololens-global-assigned-access-kiosk).
1. Рекомендуется отключить дополнительные (необязательные) возможности:
    1. Возможность поместить устройство в режим разработчика [здесь](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock).
    1. Возможность подключения HoloLens к компьютеру для копирования даты [отключит USB.](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowusbconnection)
       > [!NOTE]
        > Если вы не хотите отключить USB, но хотите возможность применить пакет подготовка к устройству с помощью USB, следуйте инструкциям, перечисленным [**здесь**](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage).

1. Используйте [WDAC,](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) чтобы разрешить или заблокировать приложения на устройстве HoloLens 2.
1. Обновление удаленной помощи до последней версии в рамках установки. Существует два варианта:
    1. Это можно сделать, переехав в Магазин Windows **Microsoft Store > удаленной**> и обновить приложение.
    1. [ApplicationManagement/AllowAppStoreAutoUpdate,](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate) которая позволяет автоматически обновлять приложения, включена по умолчанию. Подключение устройства для получения обновлений.
1. [Отключить все страницы параметров,](https://docs.microsoft.com/hololens/settings-uri-list) кроме сетевых параметров, чтобы разрешить пользователям подключаться к гостевых сетях на клиентских сайтах.
1. [Управление обновлениями HoloLens](https://docs.microsoft.com/hololens/hololens-updates)
    1. Возможность управления [обновлениями ОС](https://docs.microsoft.com/mem/intune/protect/windows-update-for-business-configure#create-and-assign-update-rings) или разрешить свободное движение.
1. [Общие ограничения устройства](https://docs.microsoft.com/hololens/hololens-common-device-restrictions).
