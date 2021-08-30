---
title: развертывание облачных HoloLens 2, подключенных к внешним клиентам
description: рекомендации по развертыванию HoloLens 2 для внешних клиентов (с использованием удаленного помощника в качестве примера)
ms.prod: hololens
ms.sitesec: library
author: qianw211
ms.author: v-qianwen
ms.topic: article
ms.localizationpriority: medium
ms.date: 8/6/2021
ms.custom: ''
ms.reviewer: ''
manager: sekerawa
appliesto:
- HoloLens 2
ms.openlocfilehash: d5cd9c380e0d276f0a8aa9efac14cf44885446e5
ms.sourcegitcommit: f04f631fbe7798a82a57cc01fc56dc2edf13c5f2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/30/2021
ms.locfileid: "123190333"
---
# <a name="deploy-cloud-connected-hololens-2-to-external-clients"></a>развертывание облачных HoloLens 2, подключенных к внешним клиентам

Данное руководством является дополнением к [руководству по развертыванию, подключенному к облаку](hololens2-cloud-connected-overview.md). она используется в ситуациях, когда организации требуется поставлять HoloLens 2 устройства для использования в качестве краткосрочного или долгосрочного пользования. внешний клиент будет входить в HoloLens 2 устройство, используя учетные данные, предоставленные вашей организацией, и использовать [удаленную помощь](/dynamics365/mixed-reality/remote-assist/ra-overview) для связи с экспертами. в этом разделе приведены [общие рекомендации по развертыванию HoloLens 2](#general-deployment-recommendations) , применимые к большинству сценариев развертывания внешних HoloLens 2, и [распространенные проблемы](#common-external-client-deployment-concerns) , с которыми сталкиваются клиенты при развертывании удаленного помощника для внешнего использования. 

## <a name="prerequisites"></a>Предварительные условия

для развертывания HoloLens 2 внешне необходимо использовать следующую инфраструктуру в разделе с [руководством по развертыванию Cloud connected](hololens2-cloud-connected-overview.md) .

- Присоединение к Azure AD с автоматической регистрацией MDM — управление с помощью MDM (Intune)
- Пользователи входят с помощью собственной корпоративной учетной записи (Azure AD)
    - Поддерживаются один или несколько пользователей на каждом устройстве.

### <a name="remote-assist-licensing-and-requirements"></a>Лицензирование и требования удаленного помощника

- Учетная запись Azure AD (требуется для приобретения подписки и назначения лицензий)
- [Подписка на Remote Assist](/dynamics365/mixed-reality/remote-assist/buy-and-deploy-remote-assist) (или [пробная версия Remote Assist](/dynamics365/mixed-reality/remote-assist/try-remote-assist))

См. [Дополнительные сведения об удаленном помощнике](/hololens/hololens2-cloud-connected-overview#learn-about-remote-assist).

### <a name="dynamics-365-remote-assist-user"></a>Пользователь Dynamics 365 Remote Assist

- Лицензия Remote Assist
- Сетевое подключение

### <a name="microsoft-teams-user"></a>Пользователь Microsoft Teams

- Microsoft Teams или [бесплатная версия Teams](https://products.office.com/microsoft-teams/free)
- Возможность подключения к сети

## <a name="general-deployment-recommendations"></a>Общие рекомендации по развертыванию

для развертывания внешних HoloLens 2 рекомендуется выполнить следующие действия.

1. используйте [последнюю версию HoloLens ос](https://aka.ms/hololens2download) в качестве базовой сборки.
1. Назначьте лицензии на основе пользователей или устройств, выполнив следующие действия:
    1. [создание группы в AAD и добавление членов](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal#create-a-basic-group-and-add-members) для пользователей HoloLens/ра.
    1. [Назначьте этой группе лицензии на основе устройства или пользователя](/azure/active-directory/enterprise-users/licensing-groups-assign#:~:text=In%20this%20article%201%20Assign%20the%20required%20licenses,3%20Check%20for%20license%20problems%20and%20resolve%20them) .
    1. Используемых Целевые группы для политик [управления мобильными устройствами (MDM)](hololens-enroll-mdm.md) .

1. Присоединение устройств AAD к клиенту, [Автоматическая регистрация](/hololens/hololens-enroll-mdm#auto-enrollment-in-mdm)и настройка с помощью [автопилота](/hololens/hololens2-autopilot). Дополнительные сведения см. в разделе [Владелец устройства](/hololens/security-adminless-os#device-owner).
    1. Первым пользователем на устройстве будет владелец устройства.
    1. Если устройство присоединено к AAD, то пользователь, выполнивший присоединение, становится владельцем устройства.
    
1. [Клиент блокирует](/hololens/hololens-release-notes#tenantlockdown-csp-and-autopilot) устройство, чтобы его можно было присоединить только к вашему клиенту.
    1. См. также [CSP для блокировки клиента](/windows/client-management/mdm/tenantlockdown-csp).

1. [Настройка режима киоска с использованием глобального назначенного доступа](/hololens/hololens-global-assigned-access-kiosk).

1. Отключите следующие возможности (необязательно):
    1. Возможность перевести устройство [в режим разработчика](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock).
    1. возможность подключения HoloLens к компьютеру для копирования даты [отключения USB](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowusbconnection).
       > [!NOTE]
        > Если вы не хотите отключать USB, но хотите обеспечить возможность применения пакета подготовки к устройству с помощью USB, следуйте [инструкциям в разделе Разрешение установки пакета](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage).

1. используйте [Защитник Windows управления приложениями (WDAC)](/hololens/windows-defender-application-control-wdac) , чтобы разрешить или блокировать приложения на устройстве HoloLens 2.
1. Обновление удаленного помощника до последней версии в ходе установки. Рассмотрим следующие два варианта:
    1. перейдите в раздел Windows **Microsoft Store--> удаленный помощник — > и обновление приложения**.
    1. [Аппликатионманажемент/алловаппстореаутаупдате](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate) — разрешает автоматическое обновление приложений. по умолчанию включено. Обеспечьте подключение устройства для получения обновлений.
1. [Отключите все страницы параметров](/hololens/settings-uri-list) , кроме параметров сети, чтобы разрешить пользователям подключаться к гостевым сетям на клиентских сайтах.
1. [Управление обновлениями HoloLens](/hololens/hololens-updates)
    1. Возможность [управлять обновлениями ОС](/mem/intune/protect/windows-update-for-business-configure#create-and-assign-update-rings) или разрешать потоку свободно.
1. Установка [общих ограничений для устройств](/hololens/hololens-common-device-restrictions).

Теперь ваши внешние клиенты готовы использовать свои HoloLens 2.

## <a name="common-external-client-deployment-concerns"></a>Распространенные проблемы с развертыванием внешнего клиента

- [Обеспечение связи клиентов друг с другом](#ensure-that-external-clients-cant-communicate-with-one-another)
- [Обеспечение доступа клиентов к ресурсам компании](#ensure-that-clients-wont-have-access-to-company-resources)
- [Скрытие или запрещение приложений](#hidden-or-restricted-apps)
- [Управление паролями для клиентов](#password-management-for-your-clients) 
- [Обеспечение доступа клиентов к журналу разговора](#ensure-that-clients-wont-have-access-to-chat-history)

### <a name="ensure-that-external-clients-cant-communicate-with-one-another"></a>Убедитесь, что внешние клиенты не могут взаимодействовать друг с другом

HoloLens удаленного помощника для HoloLens вызовов не поддерживается. Клиенты могут выполнять поиск, но не могут взаимодействовать друг с другом. [информационные барьеры в Microsoft 365](/microsoft-365/compliance/information-barriers) могут дополнительно ограничить возможности поиска и вызова клиентом. кроме того, можно использовать [поиск в каталоге с областью Microsoft Teams](/MicrosoftTeams/teams-scoped-directory-search).

 > [!NOTE]
> поскольку единый вход включен, необходимо отключить браузер с помощью [Защитник Windows управления приложениями (WDAC)](/hololens/windows-defender-application-control-wdac). если внешний клиент открывает браузер и использует веб-версию Teams, клиент будет иметь доступ к журналу разговора.

### <a name="ensure-that-clients-wont-have-access-to-company-resources"></a>Убедитесь, что у клиентов нет доступа к ресурсам компании

Есть два варианта, которые следует учитывать.

Первый вариант — многоуровневый подход:

1. Назначать лицензии, необходимые пользователю; если вы не назначите OneDrive, Outlook, SharePoint, Yammer и т. д., пользователь не сможет получить доступ к этим ресурсам. Только те лицензии, которые понадобятся пользователям, — это лицензии удаленной помощи, Intune и AAD.
1. Блокировка приложений (например, электронной почты), к которым клиенты не должны получать доступ (см. раздел [приложения скрыты или ограничены](#apps are hidden or restricted)).
1. Не сообщайте имена пользователей и пароли клиентам. для входа в HoloLens 2 требуется электронная почта и числовой пин-код.

Второй вариант — создать отдельный клиент, на котором размещаются клиенты (см. образ 1,1).

**Изображение 1,1**

![Образ клиента службы.](./images/hololens-service-tenant-image.png)

### <a name="hidden-or-restricted-apps"></a>Скрытые или ограниченные приложения

[режим киоска](/hololens/hololens-kiosk) и (или [) Защитник Windows управления приложениями (WDAC)](/hololens/windows-efender-application-control-wdac) — это параметры для скрытия и/или запрещения приложений.

### <a name="password-management-for-your-clients"></a>Управление паролями для клиентов

1. Удаление истечения срока действия пароля. Однако этот параметр может увеличить вероятность компрометации учетной записи. Пароль NIST меняет пароли каждые 30-90 дней.
1. продление срока действия пароля для HoloLens 2ных устройств должно превышать 90 дней.
1. Устройства должны быть возвращены в организацию для изменения паролей. Однако этот параметр может вызвать проблемы, если предполагается, что устройства будут находиться на предприятии клиента в течение 90 и более дней.  
1. Для устройств, которые отправляются нескольким клиентам, следует сбросить пароли перед отправкой устройства клиентам.

### <a name="ensure-that-clients-wont-have-access-to-chat-history"></a>Убедитесь, что у клиентов нет доступа к журналу чатов

Удаленная помощь очищает журнал разговора после каждого сеанса. однако журнал разговора будет доступен для Microsoft Teams пользователей.

> [!NOTE]
> поскольку единый вход включен, необходимо отключить браузер с помощью [Защитник Windows управления приложениями (WDAC)](/hololens/windows-defender-application-control-wdac).  если внешний клиент открывает браузер и использует веб-версию Teams, клиент будет иметь доступ к журналу вызовов и разговора.
