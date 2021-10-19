---
title: Управление обновлениями HoloLens
description: Сведения о том, как администраторы могут использовать управление мобильными устройствами для управления обновлениями устройств HoloLens.
ms.prod: hololens
ms.sitesec: library
author: Teresa-Motiv
ms.author: v-tea
audience: ITPro
ms.topic: article
ms.localizationpriority: high
ms.date: 10/12/2021
ms.reviewer: jarrettr
manager: jarrettr
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.custom:
- CI 116337
- CI 115825
- CI 111456
- CSSTroubleshooting
ms.openlocfilehash: 854e867238de6c87732970fba75abdc8e1fb2c64
ms.sourcegitcommit: 9574db58592b7302bd2386bdf7fda3f6721de818
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2021
ms.locfileid: "129924344"
---
# <a name="manage-hololens-updates"></a>Управление обновлениями HoloLens

HoloLens использует Центр обновления Windows таким же образом, как и другие устройства с Windows 10. Когда обновление становится доступным, оно автоматически скачивается и устанавливается в следующий раз, когда устройство подключается к компьютеру и получает доступ к Интернету. В этой статье описывается управление обновлениями на предприятиях и в других управляемых средах. Сведения о том, как управлять обновлениями для отдельных устройств HoloLens, см. в статье [Обновление HoloLens](hololens-update-hololens.md).

## <a name="manage-updates-automatically"></a>Автоматическое управление обновлениями

### <a name="managing-updates-by-using-windows-update-for-business"></a>Управление обновлениями с помощью Центра обновления Windows для бизнеса

В Windows Holographic для бизнеса можно использовать [Центр обновления Windows для бизнеса](/windows/deployment/update/waas-manage-updates-wufb), чтобы управлять обновлениями. Все устройства HoloLens 2 могут использовать Windows Holographic для бизнеса. Убедитесь, что используется Windows Holographic для бизнеса сборки 10.0.18362.1042 или более поздней. Если у вас есть устройства HoloLens (1-го поколения), вам нужно [обновить их до Windows Holographic для бизнеса](hololens1-upgrade-enterprise.md), чтобы получить возможность управления их обновлениями.

Центр обновления Windows для бизнеса подключает устройства HoloLens непосредственно к службе Центра обновления Windows. Центр обновления Windows для бизнеса позволяет управлять различными аспектами процесса обновления &mdash; вы можете выбирать, какие устройства получают обновления и в какое время. Например, можно развернуть обновления на нескольких устройствах для тестирования, а позднее — на остальных устройствах. Также можно выбрать разные расписания обновления для разных типов обновлений.

> [!NOTE]  
> Для устройств HoloLens можно автоматически управлять обновлениями компонентов (выпускаются дважды в год) и исправлениями (выпускаются ежемесячно или по мере необходимости, включая критические обновления безопасности). Дополнительные сведения о типах обновлений см. в [этой статье](/windows/deployment/update/waas-manage-updates-wufb#types-of-updates-managed-by-windows-update-for-business).

Можно настроить параметры Центра обновления Windows для бизнеса для HoloLens с помощью политик решения для управления мобильными устройствами (MDM), такого как Microsoft Intune.

### <a name="managing-windows-update-for-business-by-using-microsoft-intune"></a>Управление параметрами Центра обновления Windows для бизнеса с помощью Microsoft Intune

Подробные сведения о том, как использовать Intune для настройки Центра обновления Windows для бизнеса, см. в статье [Управление обновлениями ПО Windows 10 в Intune](/intune/protect/windows-update-for-business-configure). Дополнительные сведения о конкретных функциях Intune, поддерживаемых HoloLens, см. в разделе [Функции управления обновлениями Intune, поддерживаемые для HoloLens](#intune-update-management-functions-that-hololens-supports).

> [!IMPORTANT]  
> Intune предоставляет политики двух типов для управления обновлениями: *круг обновлений Windows 10* и *обновление функций Windows 10*. Сейчас тип политики обновления компонентов Windows 10 находится в общедоступной предварительной версии и не поддерживается для HoloLens.
>  
> Вы можете управлять обновлениями HoloLens 2 с помощью политик кругов обновления Windows 10.

### <a name="configure-update-policies-for-hololens-2-or-hololens-1st-gen"></a>Настройка политик обновления для HoloLens 2 или HoloLens (1-го поколения)

В этом разделе описываются политики, с помощью которых можно управлять обновлениями для HoloLens 2 и HoloLens (1-го поколения). Дополнительные сведения о функциональных возможностях, доступных для HoloLens 2, см. в разделе [Планирование и настройка развертывания обновлений для HoloLens 2](#plan-and-configure-update-rollouts-for-hololens-2).

[Поставщик службы конфигурации политик — Update](/windows/client-management/mdm/policy-csp-update) определяет политики настройки Центра обновления Windows для бизнеса.

> [!NOTE]  
> Список определенных поставщиков службы конфигурации (CSP), которые поддерживаются конкретными выпусками HoloLens, см. в статье [Поставщики службы конфигурации политик](/windows/client-management/mdm/policy-configuration-service-provider#policy-csps-supported-by-hololens-devices).

#### <a name="configure-automatic-checks-for-updates"></a>Настройка автоматической проверки обновлений

Вы можете использовать политику **Update/AllowAutoUpdate** для управления автоматическим обновлением, включая проверку наличия обновлений, их скачивание и установку. Дополнительные сведения о доступных параметрах для этой политики см. в разделе [Update/AllowAutoUpdate](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate).

> [!NOTE]  
> В Microsoft Intune вы можете использовать параметр **Поведение автоматического обновления** для изменения этой политики. Дополнительные сведения см. в статье [Управление обновлениями программного обеспечения Windows 10 в Intune](/intune/windows-update-for-business-configure).

#### <a name="configure-an-update-schedule"></a>Настройка расписания обновления

Вы можете настроить порядок и время применения обновлений с помощью следующих политик:

- [Update/ScheduledInstallDay](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)  
  - Значения: **0**–**7** (0 = ежедневно, 1 = воскресенье, 7 = суббота.)
  - Значение по умолчанию: **0** (ежедневно).
- [Update/ScheduledInstallTime](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
  - Значения: 0–23 (0 = полночь, 23 = 23:00).
  - Значение по умолчанию: 15:00.

#### <a name="configure-active-hours"></a>Настройка периода активности
Начиная с [Windows Holographic версии 20H2](hololens-release-notes.md#windows-holographic-version-20h2) ИТ-администраторы могут указывать период активности для устройств HoloLens 2.

Период активности — это период, когда устройство предположительно будет использоваться. Автоматический перезапуск после обновления будет происходить вне часов активности. Указанный диапазон отсчитывается от начала периода активности. Можно использовать MDM, как описано в разделе [Настройка периода активности с помощью MDM](/windows/deployment/update/waas-restart#configuring-active-hours-with-mdm). Для настройки периода активности MDM использует параметры Update/ActiveHoursStart и Update/ActiveHoursEnd, а также Update/ActiveHoursMaxRange в поставщике службы конфигурации политики.

-   [Update/ActiveHoursEnd](/windows/client-management/mdm/policy-csp-update#update-activehoursend) — это значение задает время окончания. Оно может отстоять от времени начала не более чем на 12 часов.
    -   Допустимые значения: 0–23, где 0 — полночь, 1 — 01:00 и т. д.
    -   Значение по умолчанию — 17 (17:00).
-   [Update/ActiveHoursMaxRange](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange) — это значение задает максимальное число часов активности со времени начала.
    -   Поддерживаемые значения — от 8 до 18.
    -   Значение по умолчанию: 18 (часов).
-   [Update/ActiveHoursStart](/windows/client-management/mdm/policy-csp-update#update-activehoursstart) — это значение задает время начала. Оно может отстоять от времени окончания не более чем на 12 часов.
    -   Допустимые значения: 0–23, где 0 — полночь, 1 — 01:00 и т. д.
    -   Значение по умолчанию: 8 (08:00).

#### <a name="for-devices-that-run-windows-10-version-1607-only"></a>Только для устройств под управлением Windows 10 версии 1607

Чтобы получать обновления из службы Windows Server Update Service (WSUS) вместо Центра обновления Windows, можно использовать следующие политики обновления:

- [Update/AllowUpdateService](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
- [Update/RequireUpdateApproval](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
- [Update/UpdateServiceUrl](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)

#### <a name="improved-update-restart-detection-and-notifications"></a>Улучшенные обнаружение перезапуска для обновления и уведомления

- Добавлено в [Windows Holographic версии 21H2](hololens-release-notes.md#windows-holographic-version-21h2).

Вы можете настроить отмену перезагрузки для устройств HoloLens, если они используются, задав время работы и политики для времени установки. Но это также может привести к задержке применения обновлений, если перезагрузки не выполняются для завершения установки нужного обновления. Мы добавили политики, которые позволяют ИТ-специалистам настроить конечные сроки и перезагрузки, а также обеспечить своевременное завершение установки обновлений. Пользователи будут получать уведомления до запуска перезагрузки, а также могут отсрочить перезагрузку в соответствии с ИТ-политикой.

Были добавлены следующие политики обновлений:

- [Update/AutoRestartNotificationSchedule](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
- [Update/AutoRestartRequiredNotificationDismissal](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
- [Update/ConfigureDeadlineForFeatureUpdates](/windows/client-management/mdm/policy-csp-update#update-configuredeadlineforfeatureupdates)
- [Update/ConfigureDeadlineForQualityUpdates](/windows/client-management/mdm/policy-csp-update#update-configuredeadlineforqualityupdates)
- [Update/ConfigureDeadlineGracePeriod](/windows/client-management/mdm/policy-csp-update#update-configuredeadlinegraceperiod)
- [Update/ConfigureDeadlineNoAutoReboot](/windows/client-management/mdm/policy-csp-update#update-configuredeadlinenoautoreboot)
- [Update/ScheduleImminentRestartWarning](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
- [Update/ScheduleRestartWarning](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
- [Update/UpdateNotificationLevel](/windows/client-management/mdm/policy-csp-update#update-updatenotificationlevel)

### <a name="plan-and-configure-update-rollouts-for-hololens-2"></a>Планирование и настройка развертывания обновлений для HoloLens 2

HoloLens 2 поддерживает больше возможностей автоматизации обновления, чем HoloLens (1-го поколения). Это, в частности, касается использования Microsoft Intune для управления политиками Центра обновления Windows для бизнеса. Эти функции упрощают планирование и реализацию развертывания обновлений в организации.

#### <a name="plan-the-update-strategy"></a>Планирование стратегии обновления

Центр обновления Windows для бизнеса поддерживает политики отсрочки. После выпуска обновления корпорацией Майкрософт можно использовать политику отсрочки, чтобы определить, сколько времени ждать до установки этого обновления на устройства. Связывая подмножества устройств (*круги обновления*) с различными политиками отсрочки, можно скоординировать стратегию развертывания для организации.

Например, предположим, что в организации есть 1000 устройств, которые необходимо обновить за пять этапов. В этой организации можно создать пять кругов обновления, как показано в следующей таблице.

|Group |Количество устройств |Отсрочка (дни) |
| ---| :---: | :---: |
|Группа 1 (ИТ-специалисты) |5 |0 |
|Группа 2 (ранние последователи) |50 |60 |
|Группа 3 (основная 1) |250 |120 |
|Группа 4 (основная 2) |300 |150 |
|Группа 5 (основная 3) |395 |180 |

Вот как развертывание будет последовательно осуществляться во всей организации.

![Сроки развертывания обновлений.](./images/hololens-updates-timeline.png)

#### <a name="configure-an-update-deferral-policy"></a>Настройка политики отсрочки обновлений

Политика отсрочки определяет количество дней между датой выпуска обновления и датой, на которую будет предложено установить это обновление на устройство.

Для обновлений компонентов и исправлений можно настроить разные значения отсрочки. В следующей таблице приведены определенные политики для каждого типа и указано максимальное время отсрочки.

|Категория |Политика |Максимальная отсрочка |
| --- | --- | --- |
|Обновления компонентов |DeferFeatureUpdatesPeriodInDays |365 дней |
|Исправления |DeferQualityUpdatesPeriodInDays |30 дней |

#### <a name="pause-updates-via-device"></a>Приостановка обновлений с помощью устройства

Если у пользователя нет доступа к MDM, пользователь может приостановить отдельные обновления на срок до 35 дней для устройства HoloLens 2, использующего [Windows Holographic версии 2004](hololens-release-notes.md#windows-holographic-version-2004) или более поздней. Пользователи могут найти этот параметр, выбрав **Параметры > Обновление и безопасность > Расширенные параметры**, прокрутив до раздела **Приостановка обновлений** и выбрав дату, до которой нужно приостановить обновления. После достижения предельной длительности приостановки потребуется установить обновления на устройство, после чего можно будет снова приостановить обновления. 

Начиная с [Windows Holographic версии 20H2](hololens-release-notes.md#windows-holographic-version-20h2) такую функцию приостановки обновлений можно использовать для устройств HoloLens 2. 
- [Update/SetDisablePauseUXAccess.](/windows/client-management/mdm/policy-csp-update#update-setdisablepauseuxaccess)
    - 0 (по умолчанию) — включено.
    - 1 — отключено.

#### <a name="intune-update-management-functions-that-hololens-supports"></a>Функции управления обновлениями Intune, поддерживаемые для HoloLens

Для управления обновлениями HoloLens можно использовать следующие функции управления обновлениями Intune.

- **Создать** и **Назначить**. Эти функции добавляют круг обновления Windows 10 в список кругов обновления. Дополнительные сведения см. в разделе [Создание и назначение кругов обновления](/mem/intune/protect/windows-update-for-business-configure#create-and-assign-update-rings).

- **Приостановить.** Если при развертывании обновления компонента или исправления возникает проблема, можно приостановить обновление на срок до 35 дней (начиная с указанной даты). При этом обновление не будет устанавливаться на другие устройства, пока вы не решите или не устраните проблему. Если приостановить обновление компонента, исправления будут по-прежнему предлагаться для устройств, чтобы обеспечить их безопасность. Когда тип обновления приостановлен, в области "Обзор" для этого круга отображается количество оставшихся дней до возобновления типа обновления. По окончании указанного времени срок действия приостановки автоматически истекает, и процесс обновления возобновляется.

  Пока круг обновления приостановлен, можно выбрать один из следующих вариантов:

  - **Продлить** — для продления периода приостановки для какого-либо типа обновления на 35 дней.
  - **Возобновить** — для возобновления развертывания для этого круга обновления. При необходимости можно снова приостановить круг обновления.

  > [!NOTE]  
  > Действие **Удалить** для кругов обновления не поддерживается для устройств HoloLens 2.

### <a name="delivery-optimization-preview"></a>Оптимизация поставки (предварительная версия)

[Windows Holographic версии 21H1](hololens-release-notes.md#windows-holographic-version-21h1) предоставляет доступ к ранней предварительной версии для параметров оптимизации доставки, что позволяет уменьшить нагрузку на полосу пропускания при скачивании на нескольких устройствах HoloLens. Полное описание этой функции, а также рекомендуемую конфигурацию сети можно найти в статье [Оптимизация доставки для обновлений Windows 10](/windows/deployment/update/waas-delivery-optimization).

Следующие параметры включены в рамках области управления и [могут быть настроены из Intune](/mem/intune/configuration/delivery-optimization-settings):

- [DOCacheHost](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
- [DOCacheHostSource](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehostsource)
- [DODelayCacheServerFallbackBackground](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodelaycacheserverfallbackbackground)
- [DODelayCacheServerFallbackForeground](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodelaycacheserverfallbackforeground)
- [DODownloadMode](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
- [DOMaxBackgroundDownloadBandwidth](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxbackgrounddownloadbandwidth)
- [DOMaxForegroundDownloadBandwidth](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxforegrounddownloadbandwidth)
- [DOPercentageMaxBackgroundBandwidth](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxbackgroundbandwidth)
- [DOPercentageMaxForegroundBandwidth](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxforegroundbandwidth)
- [DOSetHoursToLimitForegroundDownloadBandwidth](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dosethourstolimitforegrounddownloadbandwidth)
- [DOSetHoursToLimitBackgroundDownloadBandwidth](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dosethourstolimitbackgrounddownloadbandwidth)

Несколько оговорок, касающихся этой предварительной версии:

- Поддержка HoloLens в этой предварительной версии предоставляется только для обновлений ОС.
- Windows Holographic для бизнеса поддерживает только режимы скачивания по HTTP и скачивания из [конечной точки подключенного кэша Майкрософт](/mem/configmgr/core/plan-design/hierarchy/microsoft-connected-cache). Режимы пирингового скачивания и назначения групп для устройств HoloLens сейчас не поддерживаются.
- HoloLens не поддерживает оптимизацию развертывания или доставки для конечных точек Windows Server Update Services.
- Для устранения неполадок потребуется выполнить диагностику на сервере подключенного кэша или трассировку на HoloLens, выбрав **Параметры** > **Обновление и безопасность** >  **Устранение неполадок** >  **Центр обновления Windows**.

## <a name="manually-check-for-updates"></a>Проверка обновлений вручную

Устройства HoloLens периодически проверяют наличие обновлений системы, но в определенных обстоятельствах может потребоваться проверять наличие обновлений вручную.

Чтобы проверить наличие обновлений вручную, выберите **Параметры** > **Обновление и безопасность** > **Проверить наличие обновлений**. Если в приложении "Параметры" указано, что устройство обновлено, это означает, что установлены все доступные обновления.

## <a name="manually-roll-back-an-update"></a>Откат обновления вручную

В некоторых случаях может потребоваться вернуться на предыдущую версию программного обеспечения HoloLens. Эта процедура зависит от типа устройства — HoloLens 2 или HoloLens (1-го поколения).

### <a name="revert-to-a-previous-version-hololens-2"></a>Возврат к предыдущей версии (HoloLens 2)

Можно откатить обновления и вернуться к предыдущей версии HoloLens 2, воспользовавшись приложением [Advanced Recovery Companion](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) для сброса HoloLens на более раннюю версию.

> [!NOTE]
> При возврате к более ранней версии личные файлы и параметры будут удалены.

Для возврата к предыдущей версии HoloLens 2 выполните следующие действия:

1. Убедитесь, что к компьютеру не подключены телефоны или другие устройства с Windows.
1. На компьютере скачайте [Advanced Recovery Companion](https://www.microsoft.com/p/advanced-recovery-companion/9p74z35sfrs8?activetab=pivot:overviewtab) из Microsoft Store.
1. Скачайте [последний выпуск HoloLens 2](https://aka.ms/hololens2download).
1. После завершения скачивания откройте **проводник** > **Загрузки**, щелкните правой кнопкой мыши скачанную сжатую папку (ZIP) и выберите **Извлечь все** > **Извлечь**, чтобы распаковать файл.
1. Подключите устройство HoloLens к компьютеру кабелем USB-A — USB-C. Кабели такого типа подходят лучше всего, даже если вы раньше подключали HoloLens другими кабелями.
1. Программа Advanced Recovery Companion автоматически обнаружит устройство HoloLens. Выберите плитку **Microsoft HoloLens**.
1. На следующем экране щелкните **Выбрать пакет вручную** и откройте ранее распакованную папку.
1. Выберите файл установки (FFU).
1. Выберите **Установить программное обеспечение** и следуйте инструкциям.

### <a name="revert-to-a-previous-version-hololens-1st-gen"></a>Возврат к предыдущей версии (HoloLens (1-го поколения))

Можно откатить обновления и вернуться к предыдущей версии HoloLens (1-го поколения), воспользовавшись приложением [Windows Device Recovery Tool (WDRT)](https://support.microsoft.com/help/12379) для сброса HoloLens на более раннюю версию.

> [!NOTE]
> При возврате к более ранней версии HoloLens личные файлы и параметры будут удалены.

Для возврата к предыдущей версии HoloLens (1-го поколения) выполните следующие действия:

1. Убедитесь, что к компьютеру не подключены телефоны или другие устройства с Windows.
1. На компьютере скачайте [Windows Device Recovery Tool (WDRT)](https://support.microsoft.com/help/12379).
1. Скачайте [пакет восстановления до юбилейного обновления HoloLens](https://aka.ms/hololensrecovery).
1. После завершения скачивания откройте **проводник** > **Загрузки**, щелкните правой кнопкой мыши скачанную сжатую папку (ZIP) и выберите **Извлечь все** > **Извлечь**, чтобы распаковать файл.
1. Подключите устройство HoloLens к компьютеру кабелем micro-USB, который входит в комплект устройства HoloLens. Этот кабель подходит лучше всего, даже если вы раньше подключали HoloLens другими кабелями.
1. Приложение WDRT автоматически обнаружит устройство HoloLens. Выберите плитку **Microsoft HoloLens**.
1. На следующем экране щелкните **Выбрать пакет вручную** и откройте ранее распакованную папку.
1. Выберите файл установки (FFU).
1. Выберите **Установить программное обеспечение** и следуйте инструкциям.

**Если WDRT не обнаруживает устройство**

Если WDRT не обнаруживает устройство HoloLens, попробуйте перезагрузить компьютер. Если это не сработает, выберите **Мое устройство не обнаружено**, выберите **Microsoft HoloLens** и следуйте инструкциям.

## <a name="related-articles"></a>Связанные статьи

- [Заметки о выпуске HoloLens 2](hololens-release-notes.md)
- [Что такое Центр обновления Windows для бизнеса?](/windows/deployment/update/waas-manage-updates-wufb)
- [Назначение устройств каналам обслуживания для обновлений Windows 10](/windows/deployment/update/waas-servicing-channels-windows-10-updates)
- [Управление обновлениями программного обеспечения Windows 10 в Intune](/mem/intune/protect/windows-update-for-business-configure)
