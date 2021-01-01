---
title: Руководство по развертыванию — масштабное развертывание HoloLens 2 с подключением к облаку с помощью удаленной помощи — настройка
description: Настройка конфигураций для регистрации устройств HoloLens в сети Cloud Connected
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
ms.openlocfilehash: 042a29fe436b21ca37a2fcd7921fc53d6a9686d5
ms.sourcegitcommit: 96dcd015ad24169295690a8ed13ea1bf480e4b9e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/01/2021
ms.locfileid: "11253046"
---
# Configure — руководство по подключению к облаку

В этом разделе руководства мы&#39;, как настроить автоматическую регистрацию для вашего клиента и как применить лицензии для Intune и удаленной помощи.

## Пользователи и группы Azure

Azure и Intune с таким расширением используют пользователей и группы для назначения конфигураций и лицензий. Для проверки этого потока развертывания и возможности вызова удаленной помощи от одного пользователя к другому вам&#39;две учетные записи пользователей.

Мы можем сделать одну группу пользователей для назначения лицензий. Мы можем присоединить обоих пользователей к одной группе и применить к ней лицензию на Intune и удаленную помощь.

Если у вас&#39;есть доступ к двум учетным записям Azure AD в группе пользователей, вы можете использовать; вот краткие руководства по началу:

- [Создание пользователя](https://docs.microsoft.com/mem/intune/fundamentals/quickstart-create-user)
- [Создание группы](https://docs.microsoft.com/mem/intune/fundamentals/quickstart-create-group)
- [Добавление пользователей в группу —](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-members-azure-portal) добавление созданных пользователей для создания группы
- [Настройка Azure AD, чтобы разрешить](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan#configure-your-device-settings) группе пользователей присоединяться к устройствам — убедитесь, что у новой группы пользователей есть разрешение на регистрацию устройств в Azure AD

## Автоматическая регистрация на HoloLens 2

Чтобы обеспечить плавность и простоту работы, можно перейти к настройке параметров реализации параметров реализации параметров Azure Active Directory (AADJ) и автоматической регистрации в Intune для устройств HoloLens 2. Это позволит пользователям вводить учетные данные для входа в организацию во время OOBE и автоматически регистрироваться в Azure AD и регистрировать устройство в MDM.

С помощью [Microsoft Endpoint Manager](https://endpoint.microsoft.com/#home)можно выбрать службы и перейти на несколько страниц, пока не будет выбрана пробная версия "Получить премиум". Вы можете заметить, что для автоматической регистрации P1 достаточно Azure Active Directory Premium 1 и 2. Мы можем выбрать Intune, выбрать область пользователя для автоматической регистрации и выбрать группу, которая была создана ранее.

Подробные сведения и действия см. в руководстве о том, как включить автоматическую регистрацию [для Intune.](https://docs.microsoft.com/mem/intune/enrollment/quickstart-setup-auto-enrollment)

## Лицензии приложений

Лицензия приложения позволяет пользователю установить приобретенные компанией приложения или обновить бесплатную пробную версию до полной версии приложения. Лицензии приложений могут применяться к пользователям, группам пользователей или группам устройств. Вам&#39;лицензии удаленной помощи, чтобы пользователи в организации могли использовать удаленную помощь. В этом руководстве мы назначим лицензии удаленной поддержки группе пользователей, созданной выше в [azure Users and Groups.](hololens2-cloud-connected-configure.md#azure-users-and-groups)

Требования к лицензиям могут быть разными в зависимости от того, будет ли пользователь звонить удаленной помощи с устройства или будет удаленным соавтором из Microsoft Teams. По умолчанию флажки "Удаленная помощь" и "Teams" помечаются. В этом руководстве мы рекомендуем оставить флажки по умолчанию.

1. Узнайте больше о различных [требованиях к лицензированию и продуктам для ролей.](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/requirements#licensing-and-product-requirements-per-role) Существует несколько различных типов лицензий удаленной помощи, поэтому не забудьте получить правильные лицензии для ваших потребностей.
2. Вам&#39;[лицензию.](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/buy-remote-assist)
3. [Примените лицензии](https://docs.microsoft.com/dynamics365/mixed-reality/remote-assist/deploy-remote-assist) к группе.

## Дальнейшие действия

> [!div class="nextstepaction"]
> [Развертывание с подключением к облаку — развертывание](hololens2-cloud-connected-deploy.md)