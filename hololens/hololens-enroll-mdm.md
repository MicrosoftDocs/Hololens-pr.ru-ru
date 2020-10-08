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
ms.date: 10/06/2019
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 5adc1b48c4603f3a9d3145bef4f1d8aa1867a9d1
ms.sourcegitcommit: 5877c3e51de49f949b35ab840a3312a009a4487a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/07/2020
ms.locfileid: "11102328"
---
# Регистрация HoloLens в MDM

Вы можете управлять несколькими устройствами Microsoft HoloLens одновременно с помощью таких решений, как [Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business). Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации. См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).

> [!NOTE]
> Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).

## Требования

 Для управления устройствами HoloLens вашей организации потребуется настройка управления мобильными устройствами (MDM). Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.
 
## Различные способы регистрации

В зависимости от типа учетной записи, выбранной во время OOBE или при входе в систему, существуют различные способы регистрации. Дополнительные сведения о каждом типе удостоверений на HoloLens можно найти на [этой странице](hololens-identity.md).

- Если удостоверение — это AAD, то во время работы в файле Oobe или **Параметры**  ->  **доступа приложения или учебного заведения**  ->  **Connect** .
    - Для AAD автоматическая регистрация в MDM выполняется только в том случае, если для AAD настроены URL-адреса регистрации.
- Если удостоверение является приложением AAD и устройство было предварительно зарегистрировано с помощью учетной записи пользователя Intune с определенными профилями конфигурации, то при использовании OOBE вы присоединяетесь к домену, а затем приложение будет автоматически выполняться.
    - Кроме того, в [сборках 19041.1103 +](hololens-release-notes.md#windows-holographic-version-2004)поддерживается [поток автопилота](hololens2-autopilot.md) .
- Если для удостоверения задано MSA, используется **Настройка**  ->  **доступа к приложениям или кнопка учебного**  ->  **соединения** .
    - Это также называется потоком "добавить рабочую учетную запись" (AWA).
- Если удостоверение является локальным пользователем, то с помощью **параметров**  ->  **доступ к приложениям или учебному заведению**  ->  **только в ссылке Управление устройствами** .
    - Также называется чистым потоком регистрации для MDM.

После регистрации устройства на сервере MDM приложение "Параметры" теперь будет показывать, что устройство будет зарегистрировано в службе управления устройствами.

## Автоматическая регистрация в MDM

Если ваша организация использует Azure Active Directory (Azure AD) и решение MDM, принимающее маркер AAD для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ваш ИТ-администратор может настроить Azure AD, чтобы автоматически разрешить регистрацию в MDM после входа пользователя с учетной записью Azure AD. [Сведения о настройке регистрации в Azure AD.](https://docs.microsoft.com/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

Если автоматическая регистрация включена, дополнительные действия по регистрации вручную не требуются. Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.

Если устройство подключено к AAD, это может повлиять на того, кто является [владельцем устройства](security-adminless-os.md#device-owner).

## Отмена регистрации HoloLens из Intune

Дополнительные сведения о том, как отменять регистрацию устройства, можно найти на [этой странице](https://docs.microsoft.com/windows/client-management/mdm/disconnecting-from-mdm-unenrollment). 
