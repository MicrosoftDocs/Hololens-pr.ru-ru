---
title: Рекомендации по развертыванию внешних клиентов
description: Рекомендации по развертыванию для HoloLens 2 для внешних клиентов (с помощью удаленного помощника в качестве примера)
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
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309335"
---
# <a name="deploying-hololens-2-to-external-clients-with-remote-assist"></a>Развертывание HoloLens 2 на внешних клиентах с помощью удаленного помощника

Это руководство поможет ИТ-специалистам со следующими целями развернуть устройства Microsoft HoloLens 2 в своей организации:

1. Устройства Cloud Connect HoloLens 2
1. Использование устройств аренды HoloLens 2 для внешних клиентов
1. Защищенные арендованные устройства

В этом руководством представлены [Общие рекомендации по развертыванию hololens 2](#general-deployment-recommendations-and-instructions) , применимые к большинству вариантов развертывания hololens 2, и [распространенные проблемы](#common-concerns) , с которыми сталкиваются клиенты при развертывании удаленного помощника для внешнего использования.

## <a name="scenario-description"></a>Описание сценария

Для целей этого документа компания Contoso хочет поставлять устройство HoloLens 2 на заводе внешнего клиента для краткосрочного или долгосрочного использования. Когда клиенту требуется помощь обслуживающего оборудования, клиент будет входить на устройство HoloLens 2, используя учетные данные, предоставленные компанией Contoso, и использовать удаленную помощь для связи со специалистами компании Contoso.

Дополнительные сведения об удаленном помощнике см. [здесь](https://docs.microsoft.com/hololens/hololens2-cloud-connected-overview#learn-about-remote-assist).

### <a name="requirements-for-this-scenario"></a>Требования для этого сценария

1. [Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
1. Мобильные диспетчер устройств, например [Intune](https://docs.microsoft.com/mem/intune/fundamentals/free-trial-sign-up)
1. Лицензия удаленного помощника
    1. [Купить удаленного помощника](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-remote-assist)
    1. [Пробная версия удаленного помощника](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/try-remote-assist)

## <a name="common-concerns"></a>Распространенные проблемы

- [Как гарантировать, что внешние клиенты не смогут взаимодействовать друг с другом](#how-to-ensure-that-external-clients-do-not-have-the-ability-to-communicate-with-one-another)
- [Как обеспечить, чтобы клиенты не имели доступа к ресурсам компании](#how-to-ensure-that-clients-do-not-have-access-to-company-resources)
- [Ограничение приложений](#how-to-restrict-apps)
- [Управление паролями](#how-to-manage-passwords)
- [Как убедиться, что у клиентов нет доступа к журналу разговора](#how-to-ensure-that-clients-do-not-have-access-to-chat-history)

### <a name="how-to-ensure-that-external-clients-do-not-have-the-ability-to-communicate-with-one-another"></a>Как гарантировать, что внешние клиенты не смогут взаимодействовать друг с другом

Так как удаленный помощник HoloLens для вызовов HoloLens не поддерживается, клиенты могут выполнять поиск, но не могут взаимодействовать друг с другом. Чтобы ограничить круг лиц, которые могут выполнять поиск и вызов,  [барьеры информации](https://docs.microsoft.com/microsoft-365/compliance/information-barriers?view=o365-worldwide) могут ограничить круг лиц, с которыми может взаимодействовать клиент. Другой вариант, который следует учитывать, — использование поиска в каталоге с заданной [областью](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search)

 > [!NOTE]
> Поскольку единый вход включен, важно отключить браузер с помощью [**WDAC**](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac). Если внешний клиент открывает браузер и использует веб-версию команд, клиент будет иметь доступ к журналу вызовов и разговора.

### <a name="how-to-ensure-that-clients-do-not-have-access-to-company-resources"></a>Как обеспечить, чтобы клиенты не имели доступа к ресурсам компании

Есть два варианта, которые следует учитывать.

Первый вариант — многоуровневый подход:

1. Назначать лицензии, необходимые пользователю; Если вы не назначите пользователю OneDrive, Outlook, SharePoint, Yammer и т. д., он не сможет получить доступ к этим ресурсам. Только те лицензии, которые понадобятся пользователям, — это лицензии удаленной помощи, Intune и AAD.
1. Блокировка приложений (например, электронной почты), к которым клиенты не должны получать доступ (см. раздел [ограничение приложений](#how-to-restrict-apps)).
1. НЕ используйте совместное использование имен пользователей и паролей с клиентами. Для входа в HoloLens 2 требуется электронная почта и числовой ПИН-код.

Второй вариант — создать отдельный клиент, на котором размещаются клиенты (см. образ 1,1).

**Изображение 1,1**

![Образ клиента службы](./images/hololens-service-tenant-image.png)

### <a name="how-to-restrict-apps"></a>Ограничение приложений

[Режим киоска](https://docs.microsoft.com/hololens/hololens-kiosk) и [(или) WDac (Управление приложениями в Защитнике Windows)](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) — это параметры для запрещения приложений.

### <a name="how-to-manage-passwords"></a>Управление паролями

1. Удаление истечения срока действия пароля. Однако это повышает вероятность того, что учетная запись будет скомпрометирована. Пароль NIST меняет пароли каждые 30-90 дней.
1. Продлите срок действия пароля для устройств HoloLens 2 в течение более 90 дней.
1. Чтобы изменить пароли, устройства должны быть возвращены в Contoso. Однако это может вызвать проблемы, если предполагается, что устройства будут находиться на предприятии клиента в течение 90 дней.  
1. Для устройств, которые отправляются нескольким клиентам, следует сбросить пароли перед отправкой устройства клиентам.

### <a name="how-to-ensure-that-clients-do-not-have-access-to-chat-history"></a>Как убедиться, что у клиентов нет доступа к журналу разговора

Удаленная помощь очищает журнал разговора после каждого сеанса. Однако журнал разговора будет доступен для пользователей Microsoft Teams.

> [!NOTE]
> Поскольку единый вход включен, важно отключить браузер с помощью [**WDAC**](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac). Если внешний клиент открывает браузер и использует веб-версию команд, клиент будет иметь доступ к журналу вызовов и разговора.

## <a name="general-deployment-recommendations-and-instructions"></a>Общие рекомендации и инструкции по развертыванию

Для этапов развертывания HoloLens 2 рекомендуется следующее:

1. Используйте [последнюю версию ОС HoloLens](https://aka.ms/hololens2download) в качестве базовой сборки.
1. Назначение лицензий на основе пользователей или устройств:
    1. Лицензии на основе пользователей и устройств выполняются следующим образом.
        1. [Создайте группу в AAD и добавьте участников](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal#create-a-basic-group-and-add-members) для пользователей HOLOLENS/RA.
        1. [Назначьте этой группе лицензии на основе устройства или пользователя](https://docs.microsoft.com/azure/active-directory/enterprise-users/licensing-groups-assign#:~:text=In%20this%20article%201%20Assign%20the%20required%20licenses,3%20Check%20for%20license%20problems%20and%20resolve%20them) .
        1. Используемых Целевые группы можно использовать для политик MDM.

1. Устройства должны быть присоединены к AAD в вашем клиенте, [автоматически регистрироваться](https://docs.microsoft.com/hololens/hololens-enroll-mdm#auto-enrollment-in-mdm)и настраиваться с помощью [автоматического пилотного развертывания](https://docs.microsoft.com/hololens/hololens2-autopilot).
    1. Обратите внимание, что первым пользователем на устройстве будет владелец устройства.
    1. Обратите внимание, что если устройство присоединено к AAD, то пользователь, выполнивший присоединение, становится владельцем устройства.
    1. Дополнительные сведения см. в разделе [Владелец устройства](https://docs.microsoft.com/hololens/security-adminless-os#device-owner).
1. [Клиент блокирует](https://docs.microsoft.com/hololens/hololens-release-notes#tenantlockdown-csp-and-autopilot) устройство, чтобы его можно было присоединить только к вашему клиенту.
    1. **Дополнительная ссылка:** [CSP блокировки клиента](https://docs.microsoft.com/windows/client-management/mdm/tenantlockdown-csp).
1. Настройте киоск с помощью глобального назначенного доступа [здесь](https://docs.microsoft.com/hololens/hololens-global-assigned-access-kiosk).
1. Рекомендуется отключить следующие возможности (необязательно):
    1. Возможность перевести устройство [в режим разработчика](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock).
    1. Возможность подключения HoloLens к компьютеру для копирования даты [отключения USB](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowusbconnection).
       > [!NOTE]
        > Если вы не хотите отключать USB, но хотите иметь возможность применять пакет подготовки к устройству с помощью USB, следуйте приведенным [**здесь**](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)инструкциям.

1. Используйте [WDAC](https://docs.microsoft.com/hololens/windows-defender-application-control-wdac) , чтобы разрешить или заблокировать приложения на устройстве HoloLens 2.
1. Обновление удаленного помощника до последней версии в ходе установки. Это можно сделать двумя способами.
    1. Это можно сделать, перейдя в Windows **Microsoft Store--> удаленный помощник > и обновить приложение**.
    1. [Аппликатионманажемент/алловаппстореаутаупдате](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate) — разрешает автоматическое обновление приложений. по умолчанию включено. Обеспечьте подключение устройства для получения обновлений.
1. [Отключите все страницы параметров](https://docs.microsoft.com/hololens/settings-uri-list) , кроме параметров сети, чтобы разрешить пользователям подключаться к гостевым сетям на клиентских сайтах.
1. [Управление обновлениями HoloLens](https://docs.microsoft.com/hololens/hololens-updates)
    1. Возможность [управлять обновлениями ОС](https://docs.microsoft.com/mem/intune/protect/windows-update-for-business-configure#create-and-assign-update-rings) или разрешать потоку свободно.
1. [Общие ограничения для устройств](https://docs.microsoft.com/hololens/hololens-common-device-restrictions).
