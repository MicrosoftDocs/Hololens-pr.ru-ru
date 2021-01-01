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
ms.openlocfilehash: 7c17cbf88fc2e7a6dcd9aa600ad6e6910edb29a8
ms.sourcegitcommit: 96dcd015ad24169295690a8ed13ea1bf480e4b9e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/01/2021
ms.locfileid: "11253236"
---
# Регистрация HoloLens в MDM

Вы можете управлять несколькими устройствами Microsoft HoloLens одновременно с помощью таких решений, как [Microsoft Intune.](https://docs.microsoft.com/intune/windows-holographic-for-business) Вы сможете изменять параметры, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями вашей организации. См. разделы [Управление устройствами с Windows Holographic с помощью Microsoft Intune](https://docs.microsoft.com/intune/windows-holographic-for-business), [Поставщики служб конфигурации (CSP), которые поддерживаются в среде Windows Holographic](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/configuration-service-provider-reference#hololens) и [Политики, поддерживаемые Windows Holographic for Business](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/policy-configuration-service-provider#hololenspolicies).

> [!NOTE]
> Управление мобильными устройствами (MDM), включая VPN, Bitlocker и возможности режима полного экрана, доступны только после [обновления до Windows Holographic for Business](hololens1-upgrade-enterprise.md).

## Требования

 Для управления устройствами HoloLens в вашей организации необходимо настроить управление мобильными устройствами (MDM). Поставщиком MDM может быть Microsoft Intune или сторонний поставщик, использующий интерфейсы API Microsoft MDM.
 
## Различные способы регистрации

В зависимости от типа удостоверения, выбранного во время OOBE или после регистрации, существуют разные методы регистрации. Чтобы узнать больше о каждом типе удостоверения на HoloLens, посетите [эту страницу.](hololens-identity.md)

- Если удостоверение — Azure AD, то во время запуска при включении или кнопки **"Настройка работы приложения**  ->  **или School**  ->  **Connect".**
    - Автоматическая регистрация в MDM в Azure AD происходит только в том случае, если в Azure AD настроены URL-адреса регистрации.
- Если удостоверение — Это Azure AD, а устройство предварительно зарегистрировано на сервере Intune MDM с определенным профилем конфигурации, azure AD-Join и регистрация будет автоматически происходить во время OOBE.
    - Также называется [поток Autopilot,](hololens2-autopilot.md) доступный в сборках [19041.1103 и](hololens-release-notes.md#windows-holographic-version-2004)более .
- Если удостоверение — MSA, то с помощью кнопки **"Параметры работы**  ->  **приложения" или "School**  ->  **Connect".**
    - Также называется потоком добавления учетной записи работы (AWA).
- Если удостоверение — локальный пользователь, то с помощью параметра **"Работа**с доступом к приложениям" или "Регистрация в учебном загонке" можно только по ссылке "Управление  ->  ****  ->  **устройствами".**
    - Также называется потоком регистрации в MDM.

После регистрации устройства на сервере MDM приложение "Параметры" отразит, что устройство зарегистрировать в управлении устройствами.

## Автоматическая регистрация в MDM

Если ваша организация использует Azure Active Directory (Azure AD) и решение MDM, которое принимает маркер Azure AD для проверки подлинности (в настоящее время поддерживается только в Microsoft Intune и AirWatch), ИТ-администратор может настроить Azure AD, чтобы автоматически разрешал регистрацию в MDM после того, как пользователь войдет в свою учетную запись Azure AD. [Сведения о настройке регистрации в Azure AD.](https://docs.microsoft.com/mem/intune/enrollment/windows-enroll#enable-windows-10-automatic-enrollment)

Если автоматическая регистрация включена, дополнительные действия по регистрации вручную не требуются. Когда пользователь входит в систему с использованием учетной записи Azure AD, устройство регистрируется в MDM после завершения процесса первого запуска.

Если устройство присоединяется к Azure AD, это может повлиять на того, кто считается [владельцем устройства.](security-adminless-os.md#device-owner)

## Unenroll HoloLens from Intune

Чтобы узнать больше об откреплении устройства, посетите [эту страницу.](https://docs.microsoft.com/windows/client-management/mdm/disconnecting-from-mdm-unenrollment) 
