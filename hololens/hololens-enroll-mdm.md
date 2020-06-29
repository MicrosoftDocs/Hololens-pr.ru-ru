---
title: Регистрация HoloLens в MDM
description: Регистрация HoloLens в системе управления мобильными устройствами (MDM) для упрощения управления несколькими устройствами.
ms.prod: hololens
ms.sitesec: library
ms.assetid: 2a9b3fca-8370-44ec-8b57-fb98b8d317b0
author: scooley
ms.author: scooley
ms.topic: article
ms.localizationpriority: medium
ms.date: 07/15/2019
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 054c4ded7496957671c055e3161a1297de7abc1a
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10828694"
---
# Регистрация HoloLens в MDM

Вы можете управлять несколькими устройствами Microsoft HoloLens одновременно с помощью таких решений, как [Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business). Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации. См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).

> [!NOTE]
> Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).

## Требования

 Для управления устройствами HoloLens вашей организации потребуется настройка управления мобильными устройствами (MDM). Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.

## Автоматическая регистрация в MDM

Если ваша организация использует Azure Active Directory (Azure AD) и решение MDM, принимающее маркер AAD для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ваш ИТ-администратор может настроить Azure AD, чтобы автоматически разрешить регистрацию в MDM после входа пользователя с учетной записью Azure AD. [Сведения о настройке регистрации в Azure AD.](https://docs.microsoft.com/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

Если автоматическая регистрация включена, дополнительные действия по регистрации вручную не требуются. Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.

## Регистрация через приложение «Параметры»

 Если устройство не проходит регистрацию в MDM во время первого запуска, пользователь может вручную зарегистрировать это устройство на сервере MDM организации с помощью приложения «Параметры».

1. Перейдите в меню **Параметры** > **Учетные записи** > **Рабочий доступ**.
1. Выберите **Регистрация в системе управления устройствами** и введите свою учетную запись организации. Вы будете перенаправлены на страницу входа вашей организации.
1. После успешной проверки подлинности на сервере MDM отобразится сообщение об успехе.

Устройство теперь зарегистрировано на вашем сервере MDM. Приложение «Параметры» теперь отражает, что устройство зарегистрировано в системе управления устройствами.

## Отмена регистрации HoloLens из Intune

Невозможно удаленно [отменить регистрацию](https://docs.microsoft.com/intune-user-help/unenroll-your-device-from-intune-windows) устройства HoloLens в Intune. Если администратор отменит регистрацию устройства с помощью MDM, оно будет удалено из информационной панели Intune.
