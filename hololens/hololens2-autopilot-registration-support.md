---
title: Поддержка регистрации в Windows Autopilot для HoloLens 2
description: Сведения о том, как получить поддержку регистрации в Autopilot для устройств HoloLens 2.
author: joyjaz
ms.author: v-jjaswinski
ms.date: 5/20/2021
ms.prod: hololens
ms.topic: article
ms.custom:
- CI 116283
- CSSTroubleshooting
audience: ITPro
ms.localizationpriority: high
keywords: autopilot
manager: ylempidakis
ms.openlocfilehash: 2304e7ec18eb531cce431fb93c7abf38f2c9a1cef30f0d6c6fcaac6c95281f8e
ms.sourcegitcommit: f8e7cc2fbdcdf8962700fd50b9c017bd83d1ad65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "115661788"
---
# <a name="hololens-2-registration-support-for-autopilot"></a>Поддержка регистрации HoloLens 2 в Autopilot

Клиенты и поставщики облачных решений теперь могут регистрировать устройства Hololens 2, напрямую отправляя запросы в службу поддержки Microsoft. На этой странице перечислены требования для выполнения следующих поддерживаемых сценариев регистрации в Autopilot:

- **Регистрация устройства HoloLens 2 в Autopilot.** Отправка запроса на регистрацию устройств HoloLens 2 в Windows Autopilot.
- **Запрос аппаратного хэша для устройства HoloLens 2.** Отправка запроса в службу поддержки Microsoft на получение аппаратных хэшей, с помощью которых клиенты и поставщики облачных решений могут самостоятельно зарегистрировать устройства через Microsoft Intune или Центр партнеров Майкрософт.
- **Отмена регистрации устройства HoloLens 2 в Autopilot.** Отправка запроса на удаление устройств из Windows Autopilot; обычно применяется в конце жизненного цикла устройства.

В следующей таблице приводится информация, которую вам следует собрать *до* отправки запроса на регистрацию в службу поддержки Microsoft.

| Необходимая информация | Описание | Регистрация в Autopilot  | Запрос аппаратного хэша | Отмена регистрации в Autopilot |
------------|-------------------------------|--------------------------------------------------|------------------------------|--------------------------------|
|  Идентификатор клиента Azure Active Directory    |    Идентификатор клиента Azure Active Directory представляет собой глобально уникальный идентификатор (GUID), который не имеет прямого отношения к названию организации или имени домена.    Чтобы узнать свой идентификатор клиента, войдите на [портал Azure](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).    |     ✔️                         |                              |                         ✔️                        |
|  Доменное имя Azure Active Directory    |   Имя вашего домена верхнего уровня, например contoso.com.    |     ✔️                         |                              |                         ✔️                        |
|  Подтверждение владения    |   Чтобы подтвердить право владения, отправьте оригинальный файл счета или счета-фактуры в формате PDF. Снимка с экрана будет недостаточно. В счете или счете-фактуре должны быть указаны серийные номера устройств и название компании.     |     ✔️                         |              ✔️                |                         ✔️                        |
|  Серийные номера устройств    |   Отправьте файл Excel в формате CSV, где в каждой строчке указан отдельный серийный номер устройства.     |     ✔️                         |              ✔️                |                         ✔️                        |

## <a name="submit-support-requests"></a>Отправка запроса на поддержку

> [!div class="nextstepaction"]
> [Отправка заявки на регистрацию в Autopilot для HoloLens 2](https://prod.support.services.microsoft.com/supportrequestform/0d8bf192-cab7-6d39-143d-5a17840b9f5f)
