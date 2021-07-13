---
title: Предварительная версия Microsoft HoloLens
description: Узнайте, как приступить к работе со сборками Insider Preview, и предоставьте ценные сведения о следующем основном обновлении операционной системы для HoloLens.
ms.prod: hololens
ms.sitesec: library
author: scooley
ms.author: scooley
ms.topic: article
ms.custom:
- CI 111456
- CSSTroubleshooting
ms.localizationpriority: medium
audience: ITPro
ms.date: 04/01/2021
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens 2
ms.openlocfilehash: 87b606e634d4035da02802ddd1a8e1a980f1f1d6
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113636099"
---
# <a name="insider-preview-for-microsoft-hololens"></a><span data-ttu-id="f59c2-103">Предварительная версия Microsoft HoloLens</span><span class="sxs-lookup"><span data-stu-id="f59c2-103">Insider preview for Microsoft HoloLens</span></span>

<span data-ttu-id="f59c2-104">Добро пожаловать в новейшие сборки Insider Preview для HoloLens!</span><span class="sxs-lookup"><span data-stu-id="f59c2-104">Welcome to the latest Insider Preview builds for HoloLens!</span></span> <span data-ttu-id="f59c2-105">Вы можете легко [приступить к работе](hololens-insider.md#start-receiving-insider-builds) и предоставить ценные отзывы о следующем основном обновлении операционной системы для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f59c2-105">It's simple to [get started](hololens-insider.md#start-receiving-insider-builds) and provide valuable feedback for our next major operating system update for HoloLens.</span></span>

## <a name="windows-insider-release-notes"></a><span data-ttu-id="f59c2-106">Windows Заметки о выпуске Insider</span><span class="sxs-lookup"><span data-stu-id="f59c2-106">Windows Insider Release Notes</span></span>

<span data-ttu-id="f59c2-107">мы рады приступить к полетом новых функций, чтобы снова Windowsся для участников предварительной оценки.</span><span class="sxs-lookup"><span data-stu-id="f59c2-107">We're excited to start flighting new features to Windows Insiders again.</span></span> <span data-ttu-id="f59c2-108">Новые сборки будут передаваться на каналы разработки и бета-версии для последних обновлений.</span><span class="sxs-lookup"><span data-stu-id="f59c2-108">New builds will be flighting to the Dev and Beta Channels for the latest updates.</span></span> <span data-ttu-id="f59c2-109">мы будем обновлять эту страницу по мере добавления новых функций и обновлений в сборки Insider Windows.</span><span class="sxs-lookup"><span data-stu-id="f59c2-109">We will continue to update this page as we add more features and updates to our Windows Insider builds.</span></span> <span data-ttu-id="f59c2-110">Приготовьтесь к работе над этими обновлениями в реальности.</span><span class="sxs-lookup"><span data-stu-id="f59c2-110">Get excited and ready to mix these updates into your reality.</span></span>

| <span data-ttu-id="f59c2-111">Функция</span><span class="sxs-lookup"><span data-stu-id="f59c2-111">Feature</span></span>                 | <span data-ttu-id="f59c2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f59c2-112">Description</span></span>                | <span data-ttu-id="f59c2-113">Пользователь или сценарий</span><span class="sxs-lookup"><span data-stu-id="f59c2-113">User or Scenario</span></span> | <span data-ttu-id="f59c2-114">Сборка введена</span><span class="sxs-lookup"><span data-stu-id="f59c2-114">Build introduced</span></span> |
|-------------------------|----------------------------|--------------|------------------|
| [<span data-ttu-id="f59c2-115">изменения CSP для сведений о HoloLens отчетов</span><span class="sxs-lookup"><span data-stu-id="f59c2-115">CSP changes for reporting HoloLens details</span></span>](#csp-changes-for-reporting-hololens-details) | <span data-ttu-id="f59c2-116">Новые CSP для запроса данных</span><span class="sxs-lookup"><span data-stu-id="f59c2-116">New CSPs for to query data</span></span> | <span data-ttu-id="f59c2-117">ИТ – администраторы</span><span class="sxs-lookup"><span data-stu-id="f59c2-117">IT Admins</span></span>    | <span data-ttu-id="f59c2-118">20348,1403</span><span class="sxs-lookup"><span data-stu-id="f59c2-118">20348.1403</span></span>                 |
| [<span data-ttu-id="f59c2-119">Политика автоматического входа, управляемая CSP</span><span class="sxs-lookup"><span data-stu-id="f59c2-119">Auto login policy controlled by CSP</span></span>](#auto-login-policy-controlled-by-csp) | <span data-ttu-id="f59c2-120">Используется для автоматического входа в учетную запись</span><span class="sxs-lookup"><span data-stu-id="f59c2-120">Used to log in an account automatically</span></span> | <span data-ttu-id="f59c2-121">ИТ – администраторы</span><span class="sxs-lookup"><span data-stu-id="f59c2-121">IT Admins</span></span> | <span data-ttu-id="f59c2-122">20348,1405</span><span class="sxs-lookup"><span data-stu-id="f59c2-122">20348.1405</span></span> |
| [<span data-ttu-id="f59c2-123">Поддержка PFX-файлов для диспетчера сертификатов</span><span class="sxs-lookup"><span data-stu-id="f59c2-123">PFX file support for Certificate Manager</span></span>](#pfx-file-support-for-certificate-manager) | <span data-ttu-id="f59c2-124">добавление сертификатов PFX с помощью пользовательского интерфейса Параметры</span><span class="sxs-lookup"><span data-stu-id="f59c2-124">Add PFX certs via Settings UI</span></span> | <span data-ttu-id="f59c2-125">Конечный пользователь</span><span class="sxs-lookup"><span data-stu-id="f59c2-125">End User</span></span> | <span data-ttu-id="f59c2-126">20348,1405</span><span class="sxs-lookup"><span data-stu-id="f59c2-126">20348.1405</span></span> |
| [<span data-ttu-id="f59c2-127">просмотр расширенного диагностического отчета в Параметры на HoloLens</span><span class="sxs-lookup"><span data-stu-id="f59c2-127">View advanced diagnostic report in Settings on HoloLens</span></span>](#view-advanced-diagnostic-report-in-settings-on-hololens) | <span data-ttu-id="f59c2-128">Просмотр журналов диагностики MDM на устройстве</span><span class="sxs-lookup"><span data-stu-id="f59c2-128">View MDM diagnostic logs on device</span></span> | <span data-ttu-id="f59c2-129">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="f59c2-129">Troubleshooting</span></span> | <span data-ttu-id="f59c2-130">20348,1405</span><span class="sxs-lookup"><span data-stu-id="f59c2-130">20348.1405</span></span> |
| [<span data-ttu-id="f59c2-131">Автономные уведомления диагностики</span><span class="sxs-lookup"><span data-stu-id="f59c2-131">Offline Diagnostics notifications</span></span>](#offline-diagnostics-notifications) | <span data-ttu-id="f59c2-132">Аудиовизуального отзыв о сборе журналов</span><span class="sxs-lookup"><span data-stu-id="f59c2-132">Audiovisual feedback for log collection</span></span> | <span data-ttu-id="f59c2-133">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="f59c2-133">Troubleshooting</span></span> | <span data-ttu-id="f59c2-134">20348,1405</span><span class="sxs-lookup"><span data-stu-id="f59c2-134">20348.1405</span></span> |


### <a name="csp-changes-for-reporting-hololens-details"></a><span data-ttu-id="f59c2-135">изменения CSP для сведений о HoloLens отчетов</span><span class="sxs-lookup"><span data-stu-id="f59c2-135">CSP changes for reporting HoloLens details</span></span>

- <span data-ttu-id="f59c2-136">введено в Windows Insider build, 20348,1403</span><span class="sxs-lookup"><span data-stu-id="f59c2-136">Introduced in Windows Insider build, 20348.1403</span></span>

<span data-ttu-id="f59c2-137">следующие поставщики служб (csp) были обновлены новыми способами передачи информации с устройств HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f59c2-137">The following CSPs have been updated with new ways to report information from your HoloLens devices.</span></span>

#### <a name="devdetail-csp---free-storage"></a><span data-ttu-id="f59c2-138">DevDetail CSP — бесплатная служба хранилища</span><span class="sxs-lookup"><span data-stu-id="f59c2-138">DevDetail CSP - Free Storage</span></span>

<span data-ttu-id="f59c2-139">DevDetail CSP теперь также сообщает о свободном месте на HoloLens устройстве.</span><span class="sxs-lookup"><span data-stu-id="f59c2-139">DevDetail CSP now also reports free storage space on HoloLens device.</span></span> <span data-ttu-id="f59c2-140">это значение должно приблизительно соответствовать значению, показанному на странице служба хранилища приложения Параметры.</span><span class="sxs-lookup"><span data-stu-id="f59c2-140">This should approximately match with the value shown in Settings App's Storage page.</span></span> <span data-ttu-id="f59c2-141">Ниже приведен конкретный узел, содержащий эти сведения.</span><span class="sxs-lookup"><span data-stu-id="f59c2-141">Following is the specific node containing this information.</span></span>

- <span data-ttu-id="f59c2-142">./Девдетаил/екст/Микрософт/фристораже (только операция GET)</span><span class="sxs-lookup"><span data-stu-id="f59c2-142">./DevDetail/Ext/Microsoft/FreeStorage (GET operation only)</span></span>

#### <a name="devicestatus-csp---ssid-and-bssid"></a><span data-ttu-id="f59c2-143">Девицестатус CSP — SSID и BSSID</span><span class="sxs-lookup"><span data-stu-id="f59c2-143">DeviceStatus CSP - SSID and BSSID</span></span>

<span data-ttu-id="f59c2-144">CSP девицестатус теперь также сообщает SSID и BSSID Wi-Fi сети, с которой HoloLens активно подключено.</span><span class="sxs-lookup"><span data-stu-id="f59c2-144">DeviceStatus CSP now also reports SSID and BSSID of Wi-Fi network with which HoloLens is actively connected.</span></span> <span data-ttu-id="f59c2-145">Ниже приведены конкретные узлы, содержащие эти сведения.</span><span class="sxs-lookup"><span data-stu-id="f59c2-145">Following are the specific nodes containing this information.</span></span>

- <span data-ttu-id="f59c2-146">./Вендор/мсфт/девицестатус/нетворкидентифиерс/*MAC-адрес адаптера Wi-Fi*/ссид</span><span class="sxs-lookup"><span data-stu-id="f59c2-146">./Vendor/MSFT/DeviceStatus/NetworkIdentifiers/*mac address of Wi-Fi adapter*/SSID</span></span>
- <span data-ttu-id="f59c2-147">./Вендор/мсфт/девицестатус/нетворкидентифиерс/*MAC-адрес адаптера Wi-Fi*/бссид</span><span class="sxs-lookup"><span data-stu-id="f59c2-147">./Vendor/MSFT/DeviceStatus/NetworkIdentifiers/*mac address of Wi-Fi adapter*/BSSID</span></span>

<span data-ttu-id="f59c2-148">Пример большого двоичного объекта SyncML (для поставщиков MDM) для запроса Нетворкидентифиерс</span><span class="sxs-lookup"><span data-stu-id="f59c2-148">Example syncml blob (for MDM vendors) to query for NetworkIdentifiers</span></span>

```xml
<SyncML>
<SyncBody>
    <Get>
        <CmdID>$CmdID$</CmdID>
        <Item>
            <Target>
            <LocURI>
                ./Vendor/MSFT/DeviceStatus/NetworkIdentifiers?list=StructData
            </LocURI>
            </Target>
        </Item>
    </Get>
    <Final/>
</SyncBody>
</SyncML>
```

### <a name="auto-login-policy-controlled-by-csp"></a><span data-ttu-id="f59c2-149">Политика автоматического входа, управляемая CSP</span><span class="sxs-lookup"><span data-stu-id="f59c2-149">Auto login policy controlled by CSP</span></span>

<span data-ttu-id="f59c2-150">Эта новая политика Аутологонусер определяет, будет ли пользователь автоматически входить в систему.</span><span class="sxs-lookup"><span data-stu-id="f59c2-150">This new AutoLogonUser policy controls whether a user will be automatically logged on.</span></span> <span data-ttu-id="f59c2-151">Некоторым клиентам нужно настроить устройства, привязанные к удостоверению, но не требующие входа в систему.</span><span class="sxs-lookup"><span data-stu-id="f59c2-151">Some customers want to set up devices that are tied to an identity but don't want any sign-in experience.</span></span> <span data-ttu-id="f59c2-152">Imagine выбор устройства и немедленное использование удаленного помощника.</span><span class="sxs-lookup"><span data-stu-id="f59c2-152">Imagine picking up a device and using remote assist immediately.</span></span> <span data-ttu-id="f59c2-153">также можно воспользоваться преимуществами быстрого распространения HoloLens устройств и предоставить их конечным пользователям для ускорения входа.</span><span class="sxs-lookup"><span data-stu-id="f59c2-153">Or have a benefit of being able to rapidly  distribute HoloLens devices and enable their end users to expedite login.</span></span>

<span data-ttu-id="f59c2-154">Если для политики задано непустое значение, он указывает адрес электронной почты пользователя, запускающего автоматический вход.</span><span class="sxs-lookup"><span data-stu-id="f59c2-154">When the policy is set to a non-empty value, it specifies the email address of the auto-logon user.</span></span> <span data-ttu-id="f59c2-155">Указанный пользователь должен войти на устройство по крайней мере один раз, чтобы включить автоматический вход.</span><span class="sxs-lookup"><span data-stu-id="f59c2-155">The specified user must logon to the device at least once to enable auto-logon.</span></span>

<span data-ttu-id="f59c2-156">OMA-URI нового `./Device/Vendor/MSFT/Policy/Config/MixedReality/AutoLogonUser` строкового значения политики</span><span class="sxs-lookup"><span data-stu-id="f59c2-156">The OMA-URI of new policy `./Device/Vendor/MSFT/Policy/Config/MixedReality/AutoLogonUser` String value</span></span>

- <span data-ttu-id="f59c2-157">Пользователь с тем же адресом электронной почты будет включать автоматический вход.</span><span class="sxs-lookup"><span data-stu-id="f59c2-157">User with the same email address will have auto logon enabled.</span></span>

<span data-ttu-id="f59c2-158">На устройстве, где настроена эта политика, пользователь, указанный в политике, должен войти в систему по крайней мере один раз.</span><span class="sxs-lookup"><span data-stu-id="f59c2-158">On a device where this policy is configured, the user specified in the policy will need to logon at least once.</span></span> <span data-ttu-id="f59c2-159">Последующие перезагрузки устройства после первого входа будут автоматически входить в систему указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f59c2-159">Subsequent reboots of the device after the first logon will have the specified user automatically logged on.</span></span> <span data-ttu-id="f59c2-160">Поддерживается только один пользователь, поддерживающий автоматический вход.</span><span class="sxs-lookup"><span data-stu-id="f59c2-160">Only a single auto-logon user is supported.</span></span> <span data-ttu-id="f59c2-161">После включения автоматически вошедший в систему пользователь не сможет выйти из нее вручную.</span><span class="sxs-lookup"><span data-stu-id="f59c2-161">Once enabled, the automatically logged on user will not be able to log out manually.</span></span> <span data-ttu-id="f59c2-162">Чтобы войти в систему от имени другого пользователя, необходимо сначала отключить эту политику.</span><span class="sxs-lookup"><span data-stu-id="f59c2-162">To logon as a different user, the policy must first be disabled.</span></span>

> [!NOTE]
> - <span data-ttu-id="f59c2-163">Некоторые события, например основные обновления ОС, могут потребовать, чтобы указанный пользователь снова мог войти на устройство и возобновить режим автоматического входа.</span><span class="sxs-lookup"><span data-stu-id="f59c2-163">Some events such as major OS updates may require the specified user to logon to the device again to resume auto-logon behavior.</span></span> 
> - <span data-ttu-id="f59c2-164">Автоматический вход в систему поддерживается только для пользователей MSA и AAD.</span><span class="sxs-lookup"><span data-stu-id="f59c2-164">Auto-logon is only supported for MSA and AAD users.</span></span>

### <a name="pfx-file-support-for-certificate-manager"></a><span data-ttu-id="f59c2-165">Поддержка PFX-файлов для диспетчера сертификатов</span><span class="sxs-lookup"><span data-stu-id="f59c2-165">PFX file support for Certificate Manager</span></span>

<span data-ttu-id="f59c2-166">введено в Windows Insider build 20348,1405.</span><span class="sxs-lookup"><span data-stu-id="f59c2-166">Introduced in Windows Insider build 20348.1405.</span></span> <span data-ttu-id="f59c2-167">Мы добавили поддержку [диспетчера сертификатов](certificate-manager.md) , чтобы использовать PFX-сертификаты.</span><span class="sxs-lookup"><span data-stu-id="f59c2-167">We’ve added support to the [Certificate Manager](certificate-manager.md) to now use .pfx certificates.</span></span> <span data-ttu-id="f59c2-168">когда пользователь переходит к **Параметры**  >  **Update &**  >  **сертификаты** безопасности и выбирает **установить сертификат** , пользовательский интерфейс теперь поддерживает pfx-файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="f59c2-168">When users navigate to **Settings** > **Update & Security** > **Certificates**, and select **Install a certificate** the UI now supports .pfx certificate file.</span></span>
<span data-ttu-id="f59c2-169">Пользователи могут импортировать PFX-сертификат с закрытым ключом в хранилище пользователей или хранилище компьютера.</span><span class="sxs-lookup"><span data-stu-id="f59c2-169">Users can import .pfx certificate, with private key, to user store or machine store.</span></span>

### <a name="view-advanced-diagnostic-report-in-settings-on-hololens"></a><span data-ttu-id="f59c2-170">просмотр расширенного диагностического отчета в Параметры на HoloLens</span><span class="sxs-lookup"><span data-stu-id="f59c2-170">View advanced diagnostic report in Settings on HoloLens</span></span>

<span data-ttu-id="f59c2-171">Для управляемых устройств при устранении неполадок Проверка применения ожидаемой конфигурации политики является важным шагом.</span><span class="sxs-lookup"><span data-stu-id="f59c2-171">For managed devices when troubleshooting behavior, confirming that an expected policy configuration is applied is an important step.</span></span> <span data-ttu-id="f59c2-172">ранее для этой новой функции это было необходимо сделать на устройстве с помощью MDM или вблизи устройства после экспорта журналов диагностики mdm, собранных с помощью **Параметры**  ->  **учетных записей**  >  , в **рабочую или учебную** систему, а также выбрать **экспорт журналов управления** и просмотр на ближайшем компьютере.</span><span class="sxs-lookup"><span data-stu-id="f59c2-172">Previously to this new feature, this had to be done off device via MDM or near the device after exporting MDM diagnostic logs gathered via **Settings** -> **Accounts** > **Access work or school**, and select **Export your management logs** and viewed on a nearby PC.</span></span>

<span data-ttu-id="f59c2-173">Теперь можно просмотреть диагностику MDM на устройстве с помощью браузера пограничной сети.</span><span class="sxs-lookup"><span data-stu-id="f59c2-173">Now the MDM Diagnostics can be viewed on device using the Edge browser.</span></span> <span data-ttu-id="f59c2-174">Чтобы упростить просмотр диагностического отчета MDM, перейдите на страницу доступа к рабочей или учебной системе и выберите **просмотреть расширенный диагностический отчет**.</span><span class="sxs-lookup"><span data-stu-id="f59c2-174">To more easily view the MDM Diagnostic report navigate to the Access work or school page, and select **View advanced diagnostic report**.</span></span> <span data-ttu-id="f59c2-175">При этом отчет будет создан и открыт в новом пограничном окне.</span><span class="sxs-lookup"><span data-stu-id="f59c2-175">This will generate and open the report in a new Edge window.</span></span>

![просмотр расширенного диагностического отчета в Параметры приложении.](./images/view-advanced-diagnostic-report.jpg)

### <a name="offline-diagnostics-notifications"></a><span data-ttu-id="f59c2-177">Автономные уведомления диагностики</span><span class="sxs-lookup"><span data-stu-id="f59c2-177">Offline Diagnostics notifications</span></span>

<span data-ttu-id="f59c2-178">Это обновление для существующей функции, называемой [автономной диагностикой](hololens-diagnostic-logs.md#offline-diagnostics).</span><span class="sxs-lookup"><span data-stu-id="f59c2-178">This an update for an existing feature called [Offline Diagnostics](hololens-diagnostic-logs.md#offline-diagnostics).</span></span> <span data-ttu-id="f59c2-179">Ранее не было четкого индикатора для пользователей о том, что они активировали сбор диагностических сведений или завершились.</span><span class="sxs-lookup"><span data-stu-id="f59c2-179">Previously, there was no clear indicator to users that they had triggered diagnostic collection or it had completed.</span></span>
<span data-ttu-id="f59c2-180">теперь в сборки предварительной версии Windows есть две формы отзывов аудиовизуального для автономной диагностики.</span><span class="sxs-lookup"><span data-stu-id="f59c2-180">Now added in Windows Insider builds, there are two forms of audiovisual feedback for Offline Diagnostics.</span></span> <span data-ttu-id="f59c2-181">Первое уведомление, отображаемое при запуске и завершении сбора.</span><span class="sxs-lookup"><span data-stu-id="f59c2-181">The first being toasts notifications displayed for both when collection starts and completes.</span></span> <span data-ttu-id="f59c2-182">Они будут отображаться, когда пользователь вошел в систему и имеет визуальные элементы.</span><span class="sxs-lookup"><span data-stu-id="f59c2-182">These will be displayed when the user is logged in and has visuals.</span></span>

![Всплывающее уведомление для сбора журналов.](./images/logcollection1.jpg)

![Всплывающее уведомление после завершения сбора журналов.](./images/logcollection2.jpg)
 
<span data-ttu-id="f59c2-185">Так как пользователи часто используют автономную диагностику в качестве резервного механизма для сбора журналов, когда они не имеют доступа к дисплею, не могут войти в систему или по-прежнему находятся в OOBE. при сборе журналов также будет использоваться звуковая подсказка.</span><span class="sxs-lookup"><span data-stu-id="f59c2-185">Because users often use Offline Diagnostics as a fallback log gathering mechanism for when they don’t have access to a display, can’t log-in or are still in OOBE there will also be an audio cue played when logs are gathered.</span></span> <span data-ttu-id="f59c2-186">Этот звук будет воспроизводиться в дополнение к всплывающему уведомлению.</span><span class="sxs-lookup"><span data-stu-id="f59c2-186">This sound will be played in addition to the toast notification.</span></span>

<span data-ttu-id="f59c2-187">Эта новая функция будет включена при обновлении устройства и не требует включения или управления.</span><span class="sxs-lookup"><span data-stu-id="f59c2-187">This new feature will be enabled when your device updates, and doesn’t need to be enabled or managed.</span></span> <span data-ttu-id="f59c2-188">В любом случае, если этот новый отзыв не может быть отображен или слышен, Автономная диагностика будет по-прежнему создана.</span><span class="sxs-lookup"><span data-stu-id="f59c2-188">In any event that this new feedback cannot be displayed or heard, Offline Diagnostics will still be generated.</span></span>

<span data-ttu-id="f59c2-189">Мы надеемся, что с этим новым дополнением аудиовизуального Feedback проще собирать диагностические данные и быстрее выполнять устранение неполадок.</span><span class="sxs-lookup"><span data-stu-id="f59c2-189">We hope with this newer addition of audiovisual feedback it is easier to gather diagnostic data, and more quickly be able to troubleshoot your problems.</span></span>



### <a name="fixes-and-improvements"></a><span data-ttu-id="f59c2-190">Исправления и улучшения:</span><span class="sxs-lookup"><span data-stu-id="f59c2-190">Fixes and improvements:</span></span>

- <span data-ttu-id="f59c2-191">Исправлена [известная проблема на портале устройств, при которой не было выводится запрос на загрузку заблокированных файлов.](hololens-troubleshooting.md#downloading-locked-files-doesnt-error)</span><span class="sxs-lookup"><span data-stu-id="f59c2-191">Fixed a [known issue for Device Portal where there was no prompt downloading locked files.](hololens-troubleshooting.md#downloading-locked-files-doesnt-error)</span></span>
- <span data-ttu-id="f59c2-192">Исправлена [известная проблема с порталом устройств с истечением времени ожидания при отправке и скачивании файлов.](hololens-troubleshooting.md#device-portal-file-uploaddownload-times-out)</span><span class="sxs-lookup"><span data-stu-id="f59c2-192">Fixed a [known issue for Device Portal with file upload and download time outs.](hololens-troubleshooting.md#device-portal-file-uploaddownload-times-out)</span></span>


## <a name="start-receiving-insider-builds"></a><span data-ttu-id="f59c2-193">Начало получения сборок для предварительной оценки</span><span class="sxs-lookup"><span data-stu-id="f59c2-193">Start receiving Insider builds</span></span>

> [!NOTE]
> <span data-ttu-id="f59c2-194">Если вы не обновлялись недавно, перезагрузите устройство, чтобы обновить состояние и получить последнюю сборку.</span><span class="sxs-lookup"><span data-stu-id="f59c2-194">If you haven’t updated recently, please reboot your device to update state and get the latest build.</span></span>
> - <span data-ttu-id="f59c2-195">Голосовая команда "перезагрузить устройство" работает нормально.</span><span class="sxs-lookup"><span data-stu-id="f59c2-195">The “Reboot device” voice command works well.</span></span> 
> - <span data-ttu-id="f59c2-196">можно также нажать кнопку перезапустить в программе предварительной оценки Параметры или Windows.</span><span class="sxs-lookup"><span data-stu-id="f59c2-196">You can also choose the restart button in Settings/Windows Insider Program.</span></span>
>
> <span data-ttu-id="f59c2-197">В серверной части возникла ошибка, которая могла быть обнаружена, и это позволит вам вернуться к отслеживанию.</span><span class="sxs-lookup"><span data-stu-id="f59c2-197">We had a bug on the back-end that you may have encountered and this will get you back on track.</span></span>

<span data-ttu-id="f59c2-198">на HoloLens 2 устройстве перейдите в раздел **Параметры**  >  **обновление & безопасность**  >  **Windows программа предварительной оценки** и выберите **начать работу**.</span><span class="sxs-lookup"><span data-stu-id="f59c2-198">On a HoloLens 2 device go to **Settings** > **Update & Security** > **Windows Insider Program** and select **Get started**.</span></span> <span data-ttu-id="f59c2-199">свяжите учетную запись, которую вы использовали для регистрации в качестве Windowsной предварительной оценки.</span><span class="sxs-lookup"><span data-stu-id="f59c2-199">Link the account you used to register as a Windows Insider.</span></span>

<span data-ttu-id="f59c2-200">теперь Windows предварительная сборка перемещается на каналы.</span><span class="sxs-lookup"><span data-stu-id="f59c2-200">Windows insider is now moving to Channels.</span></span> <span data-ttu-id="f59c2-201">**Быстрый** звонок станет **каналом разработки**, а **медленный** звонок станет **бета-каналом**, а **выпуск предварительной** версии будет стать **каналом предварительной** версии.</span><span class="sxs-lookup"><span data-stu-id="f59c2-201">The **Fast** ring will become the **Dev Channel**, the **Slow** ring will become the **Beta Channel**, and the **Release Preview** ring will become the **Release Preview Channel**.</span></span> <span data-ttu-id="f59c2-202">Это сопоставление выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f59c2-202">Here is what that mapping looks like:</span></span>

![Windows Пояснения к каналам предварительной оценки](images/WindowsInsiderChannels.png)

<span data-ttu-id="f59c2-204">дополнительные сведения см. в статье [введение Windows участников предварительной оценки](https://blogs.windows.com/windowsexperience/2020/06/15/introducing-windows-insider-channels) в блогах Windows.</span><span class="sxs-lookup"><span data-stu-id="f59c2-204">For more information, see [Introducing Windows Insider Channels](https://blogs.windows.com/windowsexperience/2020/06/15/introducing-windows-insider-channels) on Windows Blogs.</span></span>
<span data-ttu-id="f59c2-205">затем выберите **активная разработка Windows**, выберите, хотите ли вы получить сборки **канала разработки** или **бета-канала** и просмотрите условия программы.</span><span class="sxs-lookup"><span data-stu-id="f59c2-205">Then, select **Active development of Windows**, choose whether you'd like to receive **Dev Channel** or **Beta Channel** builds, and review the program terms.</span></span>
<span data-ttu-id="f59c2-206">Нажмите кнопку **подтвердить, > Перезагрузить сейчас** , чтобы завершить работу.</span><span class="sxs-lookup"><span data-stu-id="f59c2-206">Select **Confirm > Restart Now** to finish up.</span></span> <span data-ttu-id="f59c2-207">после перезагрузки устройства перейдите в раздел **Параметры > обновление & безопасность > проверить наличие обновлений** , чтобы получить последнюю сборку.</span><span class="sxs-lookup"><span data-stu-id="f59c2-207">After your device has rebooted, go to **Settings > Update & Security > Check for updates** to get the latest build.</span></span>

### <a name="update-error-0x80070490-work-around"></a><span data-ttu-id="f59c2-208">Ошибка обновления 0x80070490 обойти</span><span class="sxs-lookup"><span data-stu-id="f59c2-208">Update error 0x80070490 work-around</span></span>

<span data-ttu-id="f59c2-209">Если при обновлении на канале разработки или бета-версии возникла ошибка обновления 0x80070490, попробуйте выполнить следующие краткосрочные решения.</span><span class="sxs-lookup"><span data-stu-id="f59c2-209">If you encounter an update error 0x80070490 when updating on the Dev or Beta channel, try the following short-term work around.</span></span> <span data-ttu-id="f59c2-210">Сюда входит перемещение вашего канала Insider Preview, выбор обновления и последующее перемещение обратного канала предварительной оценки.</span><span class="sxs-lookup"><span data-stu-id="f59c2-210">It involves moving your insider channel, picking up the update and then moving your Insider channel back.</span></span>

#### <a name="stage-one---release-preview"></a><span data-ttu-id="f59c2-211">Предварительная версия первого этапа</span><span class="sxs-lookup"><span data-stu-id="f59c2-211">Stage one - Release Preview</span></span>

1.  <span data-ttu-id="f59c2-212">Параметры, обновления & безопасности Windows программы предварительной оценки, выберите **канал предварительной версии**.</span><span class="sxs-lookup"><span data-stu-id="f59c2-212">Settings, Update & Security, Windows Insider Program, select **Release Preview Channel**.</span></span>

2.  <span data-ttu-id="f59c2-213">Параметры, обновление & безопасности Центр обновления Windows, **проверка наличия обновлений**.</span><span class="sxs-lookup"><span data-stu-id="f59c2-213">Settings, Update & Security, Windows Update, **Check for updates**.</span></span> <span data-ttu-id="f59c2-214">После обновления перейдите к этапу 2.</span><span class="sxs-lookup"><span data-stu-id="f59c2-214">After the update, continue on to Stage two.</span></span>

#### <a name="stage-two---dev-channel"></a><span data-ttu-id="f59c2-215">Второй этап — канал для разработки</span><span class="sxs-lookup"><span data-stu-id="f59c2-215">Stage two - Dev Channel</span></span>

1. <span data-ttu-id="f59c2-216">Параметры, обновления & безопасности Windows программы предварительной оценки, выберите **канал разработки**.</span><span class="sxs-lookup"><span data-stu-id="f59c2-216">Settings, Update & Security, Windows Insider Program, select **Dev Channel**.</span></span>

2. <span data-ttu-id="f59c2-217">Параметры, обновление & безопасности Центр обновления Windows, **проверка наличия обновлений**.</span><span class="sxs-lookup"><span data-stu-id="f59c2-217">Settings, Update & Security, Windows Update, **Check for updates**.</span></span>

## <a name="ffu-download-and-flash-directions"></a><span data-ttu-id="f59c2-218">ФФУ загрузки и Flash</span><span class="sxs-lookup"><span data-stu-id="f59c2-218">FFU download and flash directions</span></span>

<span data-ttu-id="f59c2-219">Чтобы протестировать с помощью ФФУ, подписанного с помощью Flight, сначала необходимо попытаться закрепить устройство перед миганием рейса, подписанного ФФУ.</span><span class="sxs-lookup"><span data-stu-id="f59c2-219">To test with a flight signed ffu, you first have to flight unlock your device prior to flashing the flight signed ffu.</span></span>

1. <span data-ttu-id="f59c2-220">На компьютере:</span><span class="sxs-lookup"><span data-stu-id="f59c2-220">On PC:</span></span>
    1. <span data-ttu-id="f59c2-221">Скачайте ФФУ на компьютер с [https://aka.ms/hololenspreviewdownload](https://aka.ms/hololenspreviewdownload) .</span><span class="sxs-lookup"><span data-stu-id="f59c2-221">Download ffu to your PC from [https://aka.ms/hololenspreviewdownload](https://aka.ms/hololenspreviewdownload).</span></span>
    
    1. <span data-ttu-id="f59c2-222">Установите ДУГУ (дополнительный помощник по восстановлению) из Microsoft Store: [https://www.microsoft.com/store/productId/9P74Z35SFRS8](https://www.microsoft.com/store/productId/9P74Z35SFRS8) .</span><span class="sxs-lookup"><span data-stu-id="f59c2-222">Install ARC (Advanced Recovery Companion) from the Microsoft Store: [https://www.microsoft.com/store/productId/9P74Z35SFRS8](https://www.microsoft.com/store/productId/9P74Z35SFRS8).</span></span>
    
1. <span data-ttu-id="f59c2-223">на HoloLens. разблокировка рейса: откройте **Параметры**  >  **обновление & безопасность**  >  **Windows программа предварительной оценки** , затем подпишитесь и перезагрузите устройство.</span><span class="sxs-lookup"><span data-stu-id="f59c2-223">On HoloLens - Flight Unlock: Open **Settings** > **Update & Security** > **Windows Insider Program** then sign up, reboot device.</span></span>

1. <span data-ttu-id="f59c2-224">Flash ФФУ — теперь вы можете мгновенно протестировать рейс, подписанный ФФУ, с помощью дуги.</span><span class="sxs-lookup"><span data-stu-id="f59c2-224">Flash FFU - Now you can flash the flight signed FFU using ARC.</span></span>

### <a name="provide-feedback-and-report-issues"></a><span data-ttu-id="f59c2-225">Предоставление отзывов и отчетов о проблемах</span><span class="sxs-lookup"><span data-stu-id="f59c2-225">Provide feedback and report issues</span></span>

<span data-ttu-id="f59c2-226">используйте [приложение центра отзывов](hololens-feedback.md) на HoloLens для предоставления отзывов и отчетов о проблемах.</span><span class="sxs-lookup"><span data-stu-id="f59c2-226">Please use [the Feedback Hub app](hololens-feedback.md) on your HoloLens to provide feedback and report issues.</span></span> <span data-ttu-id="f59c2-227">Использование центра обратной связи гарантирует, что все необходимые диагностические сведения были добавлены, чтобы помочь нашим специалистам быстро отладить и устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="f59c2-227">Using Feedback Hub ensures that all necessary diagnostics information is included to help our engineers quickly debug and resolve the problem.</span></span>  <span data-ttu-id="f59c2-228">проблемы с китайским и японской версиями HoloLens должны выводиться одинаковым образом.</span><span class="sxs-lookup"><span data-stu-id="f59c2-228">Issues with the Chinese and Japanese version of HoloLens should be reported the same way.</span></span>

> [!NOTE]
> <span data-ttu-id="f59c2-229">Не забудьте принять приглашение, запрашивающее, нужен ли центр отзывов для доступа к папке документов (выберите **Да** при появлении запроса).</span><span class="sxs-lookup"><span data-stu-id="f59c2-229">Be sure to accept the prompt that asks whether you'd like Feedback Hub to access your Documents folder (select **Yes** when prompted).</span></span>

## <a name="note-for-developers"></a><span data-ttu-id="f59c2-230">Примечание для разработчиков</span><span class="sxs-lookup"><span data-stu-id="f59c2-230">Note for developers</span></span>

<span data-ttu-id="f59c2-231">Вы можете попробовать разрабатывать приложения с помощью сборок Insider HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f59c2-231">You are welcome and encouraged to try developing your applications using Insider builds of HoloLens.</span></span>  <span data-ttu-id="f59c2-232">чтобы приступить к работе, ознакомьтесь с [документацией по HoloLens разработчиков](https://developer.microsoft.com/windows/mixed-reality/development) .</span><span class="sxs-lookup"><span data-stu-id="f59c2-232">Check out the [HoloLens Developer Documentation](https://developer.microsoft.com/windows/mixed-reality/development) to get started.</span></span> <span data-ttu-id="f59c2-233">Эти же инструкции работают с предварительными сборками HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f59c2-233">Those same instructions work with Insider builds of HoloLens.</span></span>  <span data-ttu-id="f59c2-234">вы можете использовать те же сборки Unity и Visual Studio, которые вы уже используете для разработки HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f59c2-234">You can use the same builds of Unity and Visual Studio that you're already using for HoloLens development.</span></span>

## <a name="stop-receiving-insider-builds"></a><span data-ttu-id="f59c2-235">Прерывать получение сборок Insider</span><span class="sxs-lookup"><span data-stu-id="f59c2-235">Stop receiving Insider builds</span></span>

<span data-ttu-id="f59c2-236">если вы больше не хотите получить предварительные сборки Windows holographic, вы можете отказаться от того, когда на HoloLens выполняется рабочая сборка, или [восстановить устройство](hololens-recovery.md) с помощью расширенного помощника по восстановлению, чтобы восстановить его до версии, не являющейся предварительной версией Windows holographic.</span><span class="sxs-lookup"><span data-stu-id="f59c2-236">If you no longer want to receive Insider builds of Windows Holographic, you can opt out when your HoloLens is running a production build, or you can [recover your device](hololens-recovery.md) using the Advanced Recovery Companion to recover your device to a non-Insider version of Windows Holographic.</span></span>

> [!CAUTION]
> <span data-ttu-id="f59c2-237">Существует известная ситуация, при которой пользователям, которые отменяют регистрацию в предварительной версии Insider Preview после ручной переустановки новой предварительной версии сборки, будет появляться синий экран.</span><span class="sxs-lookup"><span data-stu-id="f59c2-237">There is a known issue in which users who un-enroll from Insider Preview builds after manually reinstalling a fresh preview build would experience a blue screen.</span></span> <span data-ttu-id="f59c2-238">После этого необходимо вручную восстановить устройство.</span><span class="sxs-lookup"><span data-stu-id="f59c2-238">Afterwards they must manually recover their device.</span></span> <span data-ttu-id="f59c2-239">Дополнительные сведения о том, если вы повлияли на это, см. в этой [известной ошибке](hololens-troubleshooting.md#blue-screen-after-unenrolling-from-insider-preview-on-a-device-flashed-with-an-insider-build).</span><span class="sxs-lookup"><span data-stu-id="f59c2-239">For full details on if you would be impacted or not, please view more on this [Known Issue](hololens-troubleshooting.md#blue-screen-after-unenrolling-from-insider-preview-on-a-device-flashed-with-an-insider-build).</span></span>

<span data-ttu-id="f59c2-240">чтобы убедиться, что на HoloLens выполняется рабочая сборка, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f59c2-240">To verify that your HoloLens is running a production build:</span></span>

1. <span data-ttu-id="f59c2-241">последовательно выберите **Параметры > система > о программе** и найдите номер сборки.</span><span class="sxs-lookup"><span data-stu-id="f59c2-241">Go to **Settings > System > About**, and find the build number.</span></span>

1. <span data-ttu-id="f59c2-242">[См. заметки о выпуске для номеров производственных сборок](hololens-release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="f59c2-242">[See the release notes for production build numbers](hololens-release-notes.md).</span></span>

<span data-ttu-id="f59c2-243">Чтобы отказаться от сборок для участников программы предварительной оценки:</span><span class="sxs-lookup"><span data-stu-id="f59c2-243">To opt out of Insider builds:</span></span>

1. <span data-ttu-id="f59c2-244">на HoloLens, где выполняется рабочая сборка, перейдите в раздел **Параметры > обновление & безопасность > программы предварительной оценки** и выберите пункт **закончить сборки Insider**.</span><span class="sxs-lookup"><span data-stu-id="f59c2-244">On a HoloLens running a production build, go to **Settings > Update & Security > Windows Insider Program**, and select **Stop Insider builds**.</span></span>

1. <span data-ttu-id="f59c2-245">Следуйте инструкциям, чтобы отказаться от устройства.</span><span class="sxs-lookup"><span data-stu-id="f59c2-245">Follow the instructions to opt out your device.</span></span>
