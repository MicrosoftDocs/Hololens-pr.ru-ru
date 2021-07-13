---
title: Коммерческие функции
description: Узнайте о функциях Microsoft HoloLens Commercial Suite, которые упрощают управление устройствами HoloLens для предприятий.
author: scooley
ms.author: scooley
ms.date: 08/26/2019
ms.custom:
- CI 111456
- CSSTroubleshooting
ms.topic: article
audience: ITPro
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: ''
manager: jarrettr
appliesto:
- HoloLens (1st gen)
- HoloLens 2
keywords: HoloLens, коммерческие, функции, mdm, управление мобильными устройствами, режим терминала
ms.openlocfilehash: 3682a2633477d68f61dba8a674846857947a3d15
ms.sourcegitcommit: 29573e577381a23891e9557884a6dfdaac0c1c48
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110397865"
---
# <a name="commercial-features"></a>Коммерческие функции

HoloLens включает в себя функции, которые упрощают управление устройствами HoloLens на предприятиях.

Для каждого устройства HoloLens 2 доступны коммерческие функции.

Устройство HoloLens (1-е поколение) поставлялось с двумя вариантами лицензирования: лицензия разработчика и коммерческая лицензия. Чтобы получить доступ к коммерческим возможностям HoloLens, обновите лицензию разработчика до коммерческой лицензии. Чтобы приобрести Microsoft HoloLens Commercial Suite, обратитесь к местному менеджеру по работе с клиентами Microsoft.

>[!VIDEO https://www.youtube.com/embed/tNd0e2CiAkE]

## <a name="key-commercial-features"></a>Основные коммерческие функции

- **Режим терминала.** Вы можете использовать HoloLens для демонстрации определенных возможностей в режиме терминала, который ограничивает набор доступных для запуска приложений.

  ![В режиме терминала HoloLens при запуске сразу открывает выбранное вами приложение.](images/201608-kioskmode-400px.png)

- **Управление мобильными устройствами (MDM) для HoloLens.** Ваш ИТ-отдел может управлять несколькими устройствами HoloLens одновременно с помощью таких решений, как Microsoft Intune. В них можно управлять параметрами, выбирать приложения для установки и задавать настройки безопасности в соответствии с потребностями организации.

  ![Управление мобильными устройствами для HoloLens обеспечивает возможности управления корпоративного уровня на нескольких устройствах.](images/201608-enterprisemanagement-400px.png)

- **Центр обновления Windows для бизнеса.** Центр обновления Windows для бизнеса предоставляет контролируемые обновления операционной системы для устройств и поддержку канала долгосрочного обслуживания.
- **Защита данных.** На HoloLens включено шифрование данных BitLocker, которое обеспечивает такой же уровень защиты, как на любом устройстве под управлением Windows.
- **Рабочий доступ.** Любой пользователь в вашей организации может удаленно подключаться к корпоративной сети через виртуальную частную сеть (VPN) с устройства HoloLens. HoloLens также может подключаться к сетям Wi-Fi, для которых требуются учетные данные.
- **Microsoft Store для бизнеса.** Ваш ИТ-отдел может настроить корпоративный частный магазин, в котором есть только приложения вашей компании, предназначенные для определенного сценария использования HoloLens. Это позволяет безопасно распространять корпоративное программное обеспечение среди выбранной группы корпоративных пользователей.

## <a name="feature-comparison-between-editions"></a>Сравнение функций в разных выпусках

|Компоненты |HoloLens (1-го поколения) Development Edition |HoloLens (1-го поколения) Commercial Suite |HoloLens 2 |
|---|:---:|:---:|:---:|
|Шифрование устройства (BitLocker) | |✔️ |✔️ |
|Виртуальная частная сеть (VPN) | |✔️ |✔️ |
|[Полноэкранный режим](hololens-kiosk.md) | |✔️ |✔️ |
|**Управление и развертывание** | | | |
|Управление мобильными устройствами (MDM) | |✔️ |✔️ |
|Возможность блокировки отмены регистрации | |✔️ |✔️ |
|Подключение к корпоративной сети Wi-Fi с использованием сертификатов | |✔️ |✔️ |
|Microsoft Store (потребители) |Потребители |Фильтрация с использованием MDM |Фильтрация с использованием MDM |
|[Портал Store для бизнеса](https://docs.microsoft.com/microsoft-store/working-with-line-of-business-apps) | |✔️ |✔️ |
|**Безопасность и удостоверения** | | | |
|Вход с учетной записью Azure Active Directory (Azure AD) |✔️ |✔️ |✔️ |
|Вход с учетной записью Майкрософт (MSA) |✔️ |✔️ |✔️ |
|Учетные данные следующего поколения с разблокировкой по PIN-коду |✔️ |✔️ |✔️ |
|[Безопасная загрузка](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-secure-boot) |✔️ |✔️ |✔️ |
|**Обслуживание и поддержка** | | | |
|Автоматическое обновление системы по мере поступления обновлений |✔️ |✔️ |✔️ |
|[Центр обновления Windows для бизнеса.](https://docs.microsoft.com/windows/deployment/update/waas-manage-updates-wufb) | |✔️ |✔️ |
|Long-Term Servicing Channel (LTSC) | |✔️ |✔️ |

## <a name="enabling-commercial-features"></a>Включение коммерческих функций

ИТ-администратор вашей организации может настраивать коммерческие функции, например Microsoft Store для бизнеса, режим терминала и доступ к корпоративной сети Wi-Fi. В документации по [Microsoft HoloLens](index.yml) приведены пошаговые инструкции по регистрации устройств и установке приложений из магазина Microsoft Store для бизнеса.

## <a name="see-also"></a>См. также

- [Microsoft HoloLens](index.yml);
- [Полноэкранный режим](hololens-kiosk.md)
- [Поставщики службы конфигурации, поддерживаемые устройствами HoloLens](/windows/client-management/mdm/configuration-service-provider-reference#csps-supported-in-hololens-devices)
- [Microsoft Store для бизнеса и бизнес-приложения](https://blogs.technet.microsoft.com/sbucci/2016/04/13/windows-store-for-business-and-line-of-business-applications/)
- [Работа с бизнес-приложениями](/microsoft-store/working-with-line-of-business-apps)
