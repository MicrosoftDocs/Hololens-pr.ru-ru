---
title: Руководство по развертыванию внешних клиентов
description: рекомендации по развертыванию HoloLens 2 для внешних клиентов (с использованием удаленного помощника в качестве примера)
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
ms.openlocfilehash: acf4b5d730b9a7eee2dedfad2bb3f866931d7455
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113636951"
---
# <a name="deploying-hololens-2-to-external-clients-with-remote-assist"></a>развертывание HoloLens 2 для внешних клиентов с помощью удаленного помощника

это руководство поможет специалистам по информационным технологиям развертывать Microsoft HoloLens 2 устройства в своей организации:

1. HoloLens 2 устройства Cloud connect
1. ссуда HoloLens 2 устройств для использования внешним клиентам
1. Защищенные арендованные устройства

в этом руководством приведены [общие рекомендации по развертыванию HoloLens 2](#general-deployment-recommendations-and-instructions) , применимые к большинству сценариев развертывания HoloLens 2, и [распространенные проблемы](#common-concerns) , с которыми сталкиваются клиенты при развертывании удаленного помощника для внешнего использования.

## <a name="scenario-description"></a>Описание сценария

для целей этого документа компания Contoso хочет поставлять HoloLens 2 устройство на заводе внешнего клиента для краткосрочного или долгосрочного использования. когда клиенту требуется помощь в обслуживании, клиент будет входить в HoloLens 2 устройство, используя учетные данные, предоставленные компанией contoso, и использовать удаленную помощь для связи со специалистами компании contoso.

Дополнительные сведения об удаленном помощнике см. [здесь](/hololens/hololens2-cloud-connected-overview#learn-about-remote-assist).

### <a name="requirements-for-this-scenario"></a>Требования для этого сценария

1. [Azure AD](/azure/active-directory/fundamentals/active-directory-whatis)
1. Мобильные диспетчер устройств, например [Intune](/mem/intune/fundamentals/free-trial-sign-up)
1. Лицензия удаленного помощника
    1. [Купить удаленного помощника](/dynamics365/mixed-reality/remote-assist/buy-remote-assist)
    1. [Пробная версия удаленного помощника](/dynamics365/mixed-reality/remote-assist/try-remote-assist)

## <a name="common-concerns"></a>Распространенные проблемы

- [Как гарантировать, что внешние клиенты не смогут взаимодействовать друг с другом](#how-to-ensure-that-external-clients-do-not-have-the-ability-to-communicate-with-one-another)
- [Как обеспечить, чтобы клиенты не имели доступа к ресурсам компании](#how-to-ensure-that-clients-do-not-have-access-to-company-resources)
- [Ограничение приложений](#how-to-restrict-apps)
- [Управление паролями](#how-to-manage-passwords)
- [Как убедиться, что у клиентов нет доступа к журналу разговора](#how-to-ensure-that-clients-do-not-have-access-to-chat-history)

### <a name="how-to-ensure-that-external-clients-do-not-have-the-ability-to-communicate-with-one-another"></a>Как гарантировать, что внешние клиенты не смогут взаимодействовать друг с другом

поскольку удаленный помощник HoloLens HoloLens вызовы не поддерживаются, клиенты могут выполнять поиск, но не могут взаимодействовать друг с другом. Чтобы ограничить круг лиц, которые могут выполнять поиск и вызов,  [барьеры информации](/microsoft-365/compliance/information-barriers) могут ограничить круг лиц, с которыми может взаимодействовать клиент. Другой вариант, который следует учитывать, — использование поиска в каталоге с заданной [областью](/MicrosoftTeams/teams-scoped-directory-search)

 > [!NOTE]
> Поскольку единый вход включен, важно отключить браузер с помощью [**WDAC**](/hololens/windows-defender-application-control-wdac). если внешний клиент открывает браузер и использует веб-версию Teams, клиент будет иметь доступ к журналу вызовов и разговора.

### <a name="how-to-ensure-that-clients-do-not-have-access-to-company-resources"></a>Как обеспечить, чтобы клиенты не имели доступа к ресурсам компании

Есть два варианта, которые следует учитывать.

Первый вариант — многоуровневый подход:

1. Назначать лицензии, необходимые пользователю; если вы не назначаете пользователю OneDrive, Outlook, SharePoint, Yammer и т. д., он не будет иметь доступа к этим ресурсам. Только те лицензии, которые понадобятся пользователям, — это лицензии удаленной помощи, Intune и AAD.
1. Блокировка приложений (например, электронной почты), к которым клиенты не должны получать доступ (см. раздел [ограничение приложений](#how-to-restrict-apps)).
1. НЕ используйте совместное использование имен пользователей и паролей с клиентами. для входа в HoloLens 2 требуется электронная почта и числовой пин-код.

Второй вариант — создать отдельный клиент, на котором размещаются клиенты (см. образ 1,1).

**Изображение 1,1**

![Образ клиента службы](./images/hololens-service-tenant-image.png)

### <a name="how-to-restrict-apps"></a>Ограничение приложений

[режим киоска](/hololens/hololens-kiosk) и [(или) WDAC (Защитник Windows управления приложениями)](/hololens/windows-defender-application-control-wdac) — это параметры для ограничиваются приложениями.

### <a name="how-to-manage-passwords"></a>Управление паролями

1. Удаление истечения срока действия пароля. Однако это повышает вероятность того, что учетная запись будет скомпрометирована. Пароль NIST меняет пароли каждые 30-90 дней.
1. продление срока действия пароля для HoloLens 2ных устройств должно превышать 90 дней.
1. Чтобы изменить пароли, устройства должны быть возвращены в Contoso. Однако это может вызвать проблемы, если предполагается, что устройства будут находиться на предприятии клиента в течение 90 дней.  
1. Для устройств, которые отправляются нескольким клиентам, следует сбросить пароли перед отправкой устройства клиентам.

### <a name="how-to-ensure-that-clients-do-not-have-access-to-chat-history"></a>Как убедиться, что у клиентов нет доступа к журналу разговора

Удаленная помощь очищает журнал разговора после каждого сеанса. однако журнал разговора будет доступен для Microsoft Teams пользователя.

> [!NOTE]
> Поскольку единый вход включен, важно отключить браузер с помощью [**WDAC**](/hololens/windows-defender-application-control-wdac). если внешний клиент открывает браузер и использует веб-версию Teams, клиент будет иметь доступ к журналу вызовов и разговора.

## <a name="general-deployment-recommendations-and-instructions"></a>общие Рекомендации и инструкции по развертыванию

для HoloLens 2 развертывания рекомендуется выполнить следующие действия.

1. используйте [последнюю версию HoloLens ос](https://aka.ms/hololens2download) в качестве базовой сборки.
1. Назначение лицензий на основе пользователей или устройств:
    1. Лицензии на основе пользователей и устройств выполняются следующим образом.
        1. [создание группы в AAD и добавление членов](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal#create-a-basic-group-and-add-members) для пользователей HoloLens/ра.
        1. [Назначьте этой группе лицензии на основе устройства или пользователя](/azure/active-directory/enterprise-users/licensing-groups-assign#:~:text=In%20this%20article%201%20Assign%20the%20required%20licenses,3%20Check%20for%20license%20problems%20and%20resolve%20them) .
        1. Используемых Целевые группы можно использовать для политик MDM.

1. Устройства должны быть присоединены к AAD в вашем клиенте, [автоматически регистрироваться](/hololens/hololens-enroll-mdm#auto-enrollment-in-mdm)и настраиваться с помощью [автоматического пилотного развертывания](/hololens/hololens2-autopilot).
    1. Обратите внимание, что первым пользователем на устройстве будет владелец устройства.
    1. Обратите внимание, что если устройство присоединено к AAD, то пользователь, выполнивший присоединение, становится владельцем устройства.
    1. Дополнительные сведения см. в разделе [Владелец устройства](/hololens/security-adminless-os#device-owner).
1. [Клиент блокирует](/hololens/hololens-release-notes#tenantlockdown-csp-and-autopilot) устройство, чтобы его можно было присоединить только к вашему клиенту.
    1. **Дополнительная ссылка:** [CSP блокировки клиента](/windows/client-management/mdm/tenantlockdown-csp).
1. Настройте киоск с помощью глобального назначенного доступа [здесь](/hololens/hololens-global-assigned-access-kiosk).
1. Рекомендуется отключить следующие возможности (необязательно):
    1. Возможность перевести устройство [в режим разработчика](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock).
    1. возможность подключения HoloLens к компьютеру для копирования даты [отключения USB](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowusbconnection).
       > [!NOTE]
        > Если вы не хотите отключать USB, но хотите иметь возможность применять пакет подготовки к устройству с помощью USB, следуйте приведенным [**здесь**](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)инструкциям.

1. используйте [WDAC](/hololens/windows-defender-application-control-wdac) , чтобы разрешить или заблокировать приложения на HoloLens 2 устройстве.
1. Обновление удаленного помощника до последней версии в ходе установки. Это можно сделать двумя способами.
    1. это можно сделать, перейдя в Windows **Microsoft Store > Remote Assist--> и Update App**.
    1. [Аппликатионманажемент/алловаппстореаутаупдате](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate) — разрешает автоматическое обновление приложений. по умолчанию включено. Обеспечьте подключение устройства для получения обновлений.
1. [Отключите все страницы параметров](/hololens/settings-uri-list) , кроме параметров сети, чтобы разрешить пользователям подключаться к гостевым сетям на клиентских сайтах.
1. [управление обновлениями HoloLens](/hololens/hololens-updates)
    1. Возможность [управлять обновлениями ОС](/mem/intune/protect/windows-update-for-business-configure#create-and-assign-update-rings) или разрешать потоку свободно.
1. [Общие ограничения для устройств](/hololens/hololens-common-device-restrictions).
