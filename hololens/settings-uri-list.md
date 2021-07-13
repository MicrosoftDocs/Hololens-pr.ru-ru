---
title: Видимость параметров страницы
description: Ознакомьтесь с нашим списком поддерживаемых URI для PageVisibilityList и руководством по устройствам смешанной реальности HoloLens.
author: evmill
ms.author: v-evmill
ms.date: 10/13/2020
ms.topic: article
keywords: hololens, hololens 2, ограниченный доступ, терминал, страница параметров
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: widuff
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: d28994d911532a940d82756aa45609571ee80ac3
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112924338"
---
# <a name="page-settings-visibility"></a><span data-ttu-id="a6296-104">Видимость параметров страницы</span><span class="sxs-lookup"><span data-stu-id="a6296-104">Page Settings Visibility</span></span>

<span data-ttu-id="a6296-105">Одной из управляемых функций для устройств HoloLens является использование [политики Settings/PageVisibilityList](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist) для ограничения страниц, видимых в приложении "Параметры".</span><span class="sxs-lookup"><span data-stu-id="a6296-105">One of the manageable features for HoloLens devices is using the [Settings/PageVisibilityList policy](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist) to restrict the pages seen within the Settings app.</span></span> <span data-ttu-id="a6296-106">Политика PageVisibilityList позволяет ИТ-администраторам запрещать отображение или открытие определенных страниц в системном приложении "Параметры" или всех страниц, кроме указанных.</span><span class="sxs-lookup"><span data-stu-id="a6296-106">PageVisibilityList is a policy that allows IT Admins to either prevent specific pages in the System Settings app from being visible or accessible, or to do so for all pages except those specified.</span></span>

> [!NOTE]
> <span data-ttu-id="a6296-107">Эта возможность для устройств HoloLens 2 есть только в ОС [Windows Holographic версии 20H2](hololens-release-notes.md#windows-holographic-version-20h2) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a6296-107">This feature is only avalible in [Windows Holographic, version 20H2](hololens-release-notes.md#windows-holographic-version-20h2) or higher for HoloLens 2 devices.</span></span> <span data-ttu-id="a6296-108">Обновите устройства, для которых вы собираетесь ее использовать.</span><span class="sxs-lookup"><span data-stu-id="a6296-108">Please ensure devices you intend to use this for are updated.</span></span>

<span data-ttu-id="a6296-109">В примере ниже показана политика, разрешающая доступ только к страницам сведений и Bluetooth с URI "ms-settings:network-wifi" и "ms-settings:bluetooth", соответственно:</span><span class="sxs-lookup"><span data-stu-id="a6296-109">The following example illustrates a policy that would allow access only to the about and bluetooth pages, which have URI "ms-settings:network-wifi" and "ms-settings:bluetooth" respectively:</span></span>
- `showonly:network-wifi;network-proxy;bluetooth`

<span data-ttu-id="a6296-110">Чтобы настроить эту политику с помощью пакета подготовки, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="a6296-110">To set this via a Provisioning Package:</span></span>

1. <span data-ttu-id="a6296-111">При создании пакета в конструкторе конфигураций Windows откройте раздел **Политики > Параметры > PageVisibilityList**.</span><span class="sxs-lookup"><span data-stu-id="a6296-111">While creating your package in Windows Configuration Designer navigate to **Policies > Settings > PageVisibilityList**</span></span>
1. <span data-ttu-id="a6296-112">Введите строку **`showonly:network-wifi;network-proxy;bluetooth`** .</span><span class="sxs-lookup"><span data-stu-id="a6296-112">Enter the string: **`showonly:network-wifi;network-proxy;bluetooth`**</span></span>
1. <span data-ttu-id="a6296-113">Экспортируйте пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="a6296-113">Export your Provisioning Package.</span></span>
1. <span data-ttu-id="a6296-114">Примените этот пакет к устройству.</span><span class="sxs-lookup"><span data-stu-id="a6296-114">Apply the package to your device.</span></span>
<span data-ttu-id="a6296-115">Подробные сведения о создании и применении пакета подготовки см. на [этой странице](hololens-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="a6296-115">For full details on how to create and apply a provisioning package visit [this page](hololens-provisioning.md).</span></span>

<span data-ttu-id="a6296-116">Это можно сделать в Intune с помощью OMA-URI.</span><span class="sxs-lookup"><span data-stu-id="a6296-116">This can be done via Intune using OMA-URI:</span></span>

1. <span data-ttu-id="a6296-117">Создайте **настраиваемую политику**.</span><span class="sxs-lookup"><span data-stu-id="a6296-117">Create a **Custom policy**.</span></span>
1. <span data-ttu-id="a6296-118">При настройке OMA-URI используйте строку **`./Device/Vendor/MSFT/Policy/Config/Settings/PageVisibilityList`** .</span><span class="sxs-lookup"><span data-stu-id="a6296-118">When setting the OMA-URI use the string: **`./Device/Vendor/MSFT/Policy/Config/Settings/PageVisibilityList`**</span></span>
1. <span data-ttu-id="a6296-119">При выборе комплекта данных укажите **Строка**.</span><span class="sxs-lookup"><span data-stu-id="a6296-119">When selecting the data pick choose: **String**</span></span>
1. <span data-ttu-id="a6296-120">При вводе значения укажите **`showonly:network-wifi;network-proxy;bluetooth`** .</span><span class="sxs-lookup"><span data-stu-id="a6296-120">When typing the value use: **`showonly:network-wifi;network-proxy;bluetooth`**</span></span>
1. <span data-ttu-id="a6296-121">Назначьте настраиваемую конфигурацию устройства группе, в которой должно быть устройство.</span><span class="sxs-lookup"><span data-stu-id="a6296-121">Make sure to assign the custom device configuration to a group the device is intended to be in.</span></span>

<span data-ttu-id="a6296-122">Дополнительные сведения о группах и конфигурациях устройств Intune см. в статье [Конфигурация MDM для HoloLens](hololens-mdm-configure.md).</span><span class="sxs-lookup"><span data-stu-id="a6296-122">See [HoloLens MDM configuration](hololens-mdm-configure.md) for more information on Intune groups and device configurations.</span></span>

<span data-ttu-id="a6296-123">Независимо от выбранного метода ваше устройство теперь будет получать изменения и пользователи получат приложение "Параметры", как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="a6296-123">Regardless of method chosen your device should now receive the changes and users will be presented with the following Settings App.</span></span>

![Снимок экрана: изменение периода активности в приложении "Параметры"](images/hololens-page-visibility-list.jpg)

<span data-ttu-id="a6296-125">Чтобы настроить отображение или скрытие выбранных страниц в приложении "Параметры", изучите URI параметров, доступные в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="a6296-125">To configure the Settings app pages to show or hide your own selection of pages, take a look at the Settings URIs available on HoloLens.</span></span>

## <a name="settings-uris"></a><span data-ttu-id="a6296-126">URI параметров</span><span class="sxs-lookup"><span data-stu-id="a6296-126">Settings URIs</span></span>

<span data-ttu-id="a6296-127">Устройства HoloLens и Windows 10 имеют разные наборы страниц в приложении "Параметры".</span><span class="sxs-lookup"><span data-stu-id="a6296-127">HoloLens devices and Windows 10 devices have a different selection of pages within the Settings app.</span></span> <span data-ttu-id="a6296-128">На этой странице приведены только те параметры, которые есть в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="a6296-128">On this page, you will find only the settings that exist on HoloLens.</span></span>

### <a name="accounts"></a><span data-ttu-id="a6296-129">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="a6296-129">Accounts</span></span>
| <span data-ttu-id="a6296-130">Страница «Параметры»</span><span class="sxs-lookup"><span data-stu-id="a6296-130">Settings page</span></span>           | <span data-ttu-id="a6296-131">URI</span><span class="sxs-lookup"><span data-stu-id="a6296-131">URI</span></span>                                            |
|-------------------------|------------------------------------------------|
| <span data-ttu-id="a6296-132">Доступ к учетной записи места работы или учебного заведения</span><span class="sxs-lookup"><span data-stu-id="a6296-132">Access work or school</span></span> | `ms-settings:workplace`                         |
| <span data-ttu-id="a6296-133">Регистрация Iris</span><span class="sxs-lookup"><span data-stu-id="a6296-133">Iris Enrollment</span></span>       | `ms-settings:signinoptions-launchirisenrollment` |
| <span data-ttu-id="a6296-134">Параметры входа</span><span class="sxs-lookup"><span data-stu-id="a6296-134">Sign In Options</span></span>         | ` ms-settings:signinoptions `                   |

### <a name="apps"></a><span data-ttu-id="a6296-135">Приложения</span><span class="sxs-lookup"><span data-stu-id="a6296-135">Apps</span></span>
| <span data-ttu-id="a6296-136">Страница «Параметры»</span><span class="sxs-lookup"><span data-stu-id="a6296-136">Settings page</span></span> | <span data-ttu-id="a6296-137">URI</span><span class="sxs-lookup"><span data-stu-id="a6296-137">URI</span></span>                          |
|---------------|------------------------------|
| <span data-ttu-id="a6296-138">Приложения и компоненты<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-138">Apps & features<sup>2</sup></span></span>     | `ms-settings:appsfeatures` <br> |
| <span data-ttu-id="a6296-139">Приложения и компоненты > Дополнительные параметры <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-139">Apps & features > Advanced Options <sup>2</sup></span></span>     | `ms-settings::appsfeatures-app` <br> |
| <span data-ttu-id="a6296-140">Приложения и компоненты > Автономные карты<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-140">Apps & features > Offline Maps <sup>2</sup></span></span>     | `ms-settings:maps-maps` <br> |
| <span data-ttu-id="a6296-141">Приложения и компоненты > Автономные карты > Скачать карты <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-141">Apps & features > Offline Maps > Download maps <sup>2</sup></span></span>     | `ms-settings:maps-downloadmaps` <br> |

### <a name="devices"></a><span data-ttu-id="a6296-142">Устройства</span><span class="sxs-lookup"><span data-stu-id="a6296-142">Devices</span></span>
| <span data-ttu-id="a6296-143">Страница «Параметры»</span><span class="sxs-lookup"><span data-stu-id="a6296-143">Settings page</span></span> | <span data-ttu-id="a6296-144">URI</span><span class="sxs-lookup"><span data-stu-id="a6296-144">URI</span></span>                          |
|---------------|------------------------------|
| <span data-ttu-id="a6296-145">Bluetooth</span><span class="sxs-lookup"><span data-stu-id="a6296-145">Bluetooth</span></span>     | `ms-settings:bluetooth` <br> `ms-settings:connecteddevices` |
| <span data-ttu-id="a6296-146">Мышь<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-146">Mouse <sup>2</sup></span></span>      | `ms-settings:mouse` <br>  |
| <span data-ttu-id="a6296-147">USB<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-147">USB <sup>2</sup></span></span>      | `ms-settings:usb` <br>  |

### <a name="privacy"></a><span data-ttu-id="a6296-148">Конфиденциальность</span><span class="sxs-lookup"><span data-stu-id="a6296-148">Privacy</span></span>
| <span data-ttu-id="a6296-149">Страница «Параметры»</span><span class="sxs-lookup"><span data-stu-id="a6296-149">Settings page</span></span>            | <span data-ttu-id="a6296-150">URI</span><span class="sxs-lookup"><span data-stu-id="a6296-150">URI</span></span>                                             |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="a6296-151">Сведения об учетной записи</span><span class="sxs-lookup"><span data-stu-id="a6296-151">Account Info</span></span>             | `ms-settings:privacy-accountinfo`              |
| <span data-ttu-id="a6296-152">Диагностика приложений</span><span class="sxs-lookup"><span data-stu-id="a6296-152">App Diagnostics</span></span>        | `ms-settings:privacy-appdiagnostics`              |
| <span data-ttu-id="a6296-153">Фоновые приложения</span><span class="sxs-lookup"><span data-stu-id="a6296-153">Background Apps</span></span>        | `ms-settings:privacy-backgroundapps`              |
| <span data-ttu-id="a6296-154">Календарь</span><span class="sxs-lookup"><span data-stu-id="a6296-154">Calendar</span></span>                 | `ms-settings:privacy-calendar`                    |
| <span data-ttu-id="a6296-155">Журнал вызовов</span><span class="sxs-lookup"><span data-stu-id="a6296-155">Call History</span></span>             | `ms-settings:privacy-callhistory`                 |
| <span data-ttu-id="a6296-156">Камера</span><span class="sxs-lookup"><span data-stu-id="a6296-156">Camera</span></span>                   | `ms-settings:privacy-webcam`                      |
| <span data-ttu-id="a6296-157">Контакты</span><span class="sxs-lookup"><span data-stu-id="a6296-157">Contacts</span></span>                 | `ms-settings:privacy-contacts`                    |
| <span data-ttu-id="a6296-158">Диагностика и отзывы</span><span class="sxs-lookup"><span data-stu-id="a6296-158">Diagnostics & Feedback</span></span> | `ms-settings:privacy-feedback`                    |
| <span data-ttu-id="a6296-159">документы.</span><span class="sxs-lookup"><span data-stu-id="a6296-159">Documents</span></span>                | `ms-settings:privacy-documents`                   |
| <span data-ttu-id="a6296-160">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="a6296-160">Email</span></span>                    | `ms-settings:privacy-email`                       |
| <span data-ttu-id="a6296-161">Файловая система</span><span class="sxs-lookup"><span data-stu-id="a6296-161">File system</span></span>              | `ms-settings:privacy-broadfilesystemaccess`       |
| <span data-ttu-id="a6296-162">Общие<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-162">General <sup>2</sup></span></span>             | `ms-settings:privacy-general`       |
| <span data-ttu-id="a6296-163">Ink & typing personalization (Персонализация рукописного ввода и ввода с клавиатуры)<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-163">Ink & typing personalization <sup>2</sup></span></span>             | `ms-settings:privacy-speechtyping`       |
| <span data-ttu-id="a6296-164">Расположение</span><span class="sxs-lookup"><span data-stu-id="a6296-164">Location</span></span>                 | `ms-settings:privacy-location`                    |
| <span data-ttu-id="a6296-165">Обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="a6296-165">Messaging</span></span>                | `ms-settings:privacy-messaging`                   |
| <span data-ttu-id="a6296-166">Микрофон</span><span class="sxs-lookup"><span data-stu-id="a6296-166">Microphone</span></span>               | `ms-settings:privacy-microphone`                  |
| <span data-ttu-id="a6296-167">Движение<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-167">Motion <sup>2</sup></span></span>               | `ms-settings:privacy-motion`                  |
| <span data-ttu-id="a6296-168">Уведомления</span><span class="sxs-lookup"><span data-stu-id="a6296-168">Notifications</span></span>            | `ms-settings:privacy-notifications`               |
| <span data-ttu-id="a6296-169">Другие устройства</span><span class="sxs-lookup"><span data-stu-id="a6296-169">Other devices</span></span>            | `ms-settings:privacy-customdevices`               |
| <span data-ttu-id="a6296-170">Изображения</span><span class="sxs-lookup"><span data-stu-id="a6296-170">Pictures</span></span>                 | `ms-settings:privacy-pictures`                    |
| <span data-ttu-id="a6296-171">Радиомодули</span><span class="sxs-lookup"><span data-stu-id="a6296-171">Radios</span></span>                   | `ms-settings:privacy-radios`                      |
| <span data-ttu-id="a6296-172">Screenshot borders (Границы снимка экрана)<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-172">Screenshot borders <sup>2</sup></span></span>             | `ms-settings:privacy-graphicsCaptureWithoutBorder`       |
| <span data-ttu-id="a6296-173">Screenshots and apps (Снимки экрана и приложения)<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-173">Screenshots and apps <sup>2</sup></span></span>             | `ms-settings:privacy-graphicsCaptureProgrammatic`       |
| <span data-ttu-id="a6296-174">Речь</span><span class="sxs-lookup"><span data-stu-id="a6296-174">Speech</span></span>                   | `ms-settings:privacy-speech`                      |
| <span data-ttu-id="a6296-175">Задания</span><span class="sxs-lookup"><span data-stu-id="a6296-175">Tasks</span></span>                    | `ms-settings:privacy-tasks`                       |
| <span data-ttu-id="a6296-176">Движения пользователей</span><span class="sxs-lookup"><span data-stu-id="a6296-176">User movements</span></span>           | `ms-settings:privacy-backgroundspatialperception` |
| <span data-ttu-id="a6296-177">Видео</span><span class="sxs-lookup"><span data-stu-id="a6296-177">Videos</span></span>                   | `ms-settings:privacy-videos`                      |
| <span data-ttu-id="a6296-178">Голосовая активация</span><span class="sxs-lookup"><span data-stu-id="a6296-178">Voice Activation</span></span>       | `ms-settings:privacy-voiceactivation`             |

### <a name="network--internet"></a><span data-ttu-id="a6296-179">Сеть и Интернет</span><span class="sxs-lookup"><span data-stu-id="a6296-179">Network & Internet</span></span>
| <span data-ttu-id="a6296-180">Страница «Параметры»</span><span class="sxs-lookup"><span data-stu-id="a6296-180">Settings page</span></span> | <span data-ttu-id="a6296-181">URI</span><span class="sxs-lookup"><span data-stu-id="a6296-181">URI</span></span>                              |
|---------------|----------------------------------|
| <span data-ttu-id="a6296-182">Режим "в самолете"<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-182">Airplane Mode <sup>2</sup></span></span> | `ms-settings:network-airplanemode`        |
| <span data-ttu-id="a6296-183">Proxy (Прокси)</span><span class="sxs-lookup"><span data-stu-id="a6296-183">Proxy</span></span> | `ms-settings:network-proxy`        |
| <span data-ttu-id="a6296-184">VPN</span><span class="sxs-lookup"><span data-stu-id="a6296-184">VPN</span></span>   | `ms-settings:network-vpn`          |
| <span data-ttu-id="a6296-185">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="a6296-185">Wi-Fi</span></span>  | `ms-settings:network-wifi`<br>`ms-settings:network-wifisettings`<br>`ms-settings:network-status`<br>`ms-settings:wifi-provisioning`    |



### <a name="system"></a><span data-ttu-id="a6296-186">Система</span><span class="sxs-lookup"><span data-stu-id="a6296-186">System</span></span>
| <span data-ttu-id="a6296-187">Страница «Параметры»</span><span class="sxs-lookup"><span data-stu-id="a6296-187">Settings page</span></span>      | <span data-ttu-id="a6296-188">URI</span><span class="sxs-lookup"><span data-stu-id="a6296-188">URI</span></span>                                |
|--------------------|------------------------------------|
| <span data-ttu-id="a6296-189">Аккумулятор<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-189">Battery <sup>2</sup></span></span>           | `ms-settings:batterysaver`<br>|
| <span data-ttu-id="a6296-190">Аккумулятор<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-190">Battery <sup>2</sup></span></span>           | `ms-settings:batterysaver-settings`<br>|
| <span data-ttu-id="a6296-191">Цвета</span><span class="sxs-lookup"><span data-stu-id="a6296-191">Colors</span></span>             | `ms-settings:colors`<br>`ms-settings:personalization-colors` |
| <span data-ttu-id="a6296-192">Голограммы<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-192">Holograms <sup>2</sup></span></span>  |  `ms-settings:holograms`  |
| <span data-ttu-id="a6296-193">Калибровка<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-193">Calibration <sup>2</sup></span></span> |  `ms-settings:calibration` |
| <span data-ttu-id="a6296-194">Уведомления и действия</span><span class="sxs-lookup"><span data-stu-id="a6296-194">Notifications & actions</span></span>  | `ms-settings:notifications`          |
| <span data-ttu-id="a6296-195">Общие возможности</span><span class="sxs-lookup"><span data-stu-id="a6296-195">Shared Experiences</span></span> | `ms-settings:crossdevice` 
| <span data-ttu-id="a6296-196">Звук<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-196">Sound <sup>2</sup></span></span>           | `ms-settings:sound`<br>|
| <span data-ttu-id="a6296-197">Звук > App volume and device preference (Громкость приложений и параметры устройства)<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-197">Sound > App volume and device preference <sup>2</sup></span></span>           | `ms-settings:apps-volume`<br>|
| <span data-ttu-id="a6296-198">Звук > Manage sound devices (Управление звуковыми устройствами)<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-198">Sound > Manage sound devices <sup>2</sup></span></span>           | `ms-settings:sound-devices`<br>|
| <span data-ttu-id="a6296-199">Память</span><span class="sxs-lookup"><span data-stu-id="a6296-199">Storage</span></span>            | `ms-settings:storagesense`           |
| <span data-ttu-id="a6296-200">Память > Configure Storage Sense (Настройка контроля памяти)<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-200">Storage > Configure Storage Sense <sup>2</sup></span></span>           | `ms-settings:storagepolicies`<br>|

### <a name="time--language"></a><span data-ttu-id="a6296-201">Время и язык</span><span class="sxs-lookup"><span data-stu-id="a6296-201">Time & Language</span></span>
| <span data-ttu-id="a6296-202">Страница «Параметры»</span><span class="sxs-lookup"><span data-stu-id="a6296-202">Settings page</span></span> | <span data-ttu-id="a6296-203">URI</span><span class="sxs-lookup"><span data-stu-id="a6296-203">URI</span></span>                                           |
|---------------|-----------------------------------------------|
| <span data-ttu-id="a6296-204">Дата и время<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-204">Date & time <sup>2</sup></span></span> | `ms-settings:dateandtime`                  |
| <span data-ttu-id="a6296-205">Клавиатура<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-205">Keyboard <sup>2</sup></span></span> | `ms-settings:keyboard`                  |
| <span data-ttu-id="a6296-206">Язык<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-206">Language <sup>2</sup></span></span> | `ms-settings:language`                  |
| <span data-ttu-id="a6296-207">Язык<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-207">Language <sup>2</sup></span></span> | `ms-settings:regionlanguage-languageoptions`                  |
| <span data-ttu-id="a6296-208">Язык</span><span class="sxs-lookup"><span data-stu-id="a6296-208">Language</span></span>      | `ms-settings:regionlanguage`<br>`ms-settings:regionlanguage-adddisplaylanguage`<br>`ms-settings:regionlanguage-setdisplaylanguage` |
| <span data-ttu-id="a6296-209">Регион</span><span class="sxs-lookup"><span data-stu-id="a6296-209">Region</span></span>        | `ms-settings:regionformatting`                  |

### <a name="update--security"></a><span data-ttu-id="a6296-210">Обновление и безопасность</span><span class="sxs-lookup"><span data-stu-id="a6296-210">Update & Security</span></span>
| <span data-ttu-id="a6296-211">Страница «Параметры»</span><span class="sxs-lookup"><span data-stu-id="a6296-211">Settings page</span></span>                         | <span data-ttu-id="a6296-212">URI</span><span class="sxs-lookup"><span data-stu-id="a6296-212">URI</span></span>                                       |
|---------------------------------------|-------------------------------------------|
| <span data-ttu-id="a6296-213">Дополнительные параметры</span><span class="sxs-lookup"><span data-stu-id="a6296-213">Advanced Options</span></span>                    | `ms-settings:windowsupdate-options`         |
| <span data-ttu-id="a6296-214">Сброс и восстановление <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="a6296-214">Reset & Recovery <sup>2</sup></span></span>      | `ms-settings:reset`         |
| <span data-ttu-id="a6296-215">Программа предварительной оценки Windows</span><span class="sxs-lookup"><span data-stu-id="a6296-215">Windows Insider Program</span></span>               | `ms-settings:windowsinsider` <br>`ms-settings:windowsinsider-optin`          |
| <span data-ttu-id="a6296-216">Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="a6296-216">Windows Update</span></span>                        | `ms-settings:windowsupdate`<br> `ms-settings:windowsupdate-activehours`  <br> `ms-settings:windowsupdate-history` <br> `ms-settings:windowsupdate-optionalupdates` <br><span data-ttu-id="a6296-217"><sup>1</sup>`ms-settings:windowsupdate-options`</span><span class="sxs-lookup"><span data-stu-id="a6296-217"><sup>1</sup>`ms-settings:windowsupdate-options`</span></span><br><span data-ttu-id="a6296-218"><sup>1</sup>`ms-settings:windowsupdate-restartoptions`</span><span class="sxs-lookup"><span data-stu-id="a6296-218"><sup>1</sup>`ms-settings:windowsupdate-restartoptions`</span></span> |
| <span data-ttu-id="a6296-219">Центр обновления Windows — проверка наличия обновлений</span><span class="sxs-lookup"><span data-stu-id="a6296-219">Windows Update - Checks for updates</span></span> | `ms-settings:windowsupdate-action`          |


- <span data-ttu-id="a6296-220"><sup>1</sup> — Для версий Windows Holographic старше 21H1 следующие два URI не перенаправляют на страницы **Дополнительные возможности** или **Параметры**, а только блокируют или отображают основную страницу Центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="a6296-220"><sup>1</sup> - For versions prior to Windows Holographic, version 21H1, the following two URIs do not actually take you to the **Advanced options** or **Options** pages; they will only block or show the main Windows Update page.</span></span>
  -  <span data-ttu-id="a6296-221">ms-settings:windowsupdate-options</span><span class="sxs-lookup"><span data-stu-id="a6296-221">ms-settings:windowsupdate-options</span></span>
  -  <span data-ttu-id="a6296-222">ms-settings:windowsupdate-restartoptions</span><span class="sxs-lookup"><span data-stu-id="a6296-222">ms-settings:windowsupdate-restartoptions</span></span>

- <span data-ttu-id="a6296-223"><sup>2</sup> — доступно в Windows Holographic версии 21H1 и выше.</span><span class="sxs-lookup"><span data-stu-id="a6296-223"><sup>2</sup> - Available in Windows Holographic 21H1 or higher.</span></span>


<span data-ttu-id="a6296-224">Полный список URI параметров для Windows 10 см. в документации по [параметрам запуска](https://docs.microsoft.com/windows/uwp/launch-resume/launch-settings-app#ms-settings-uri-scheme-reference).</span><span class="sxs-lookup"><span data-stu-id="a6296-224">For a full list of Windows 10 Settings URIs, please visit the [launch settings](https://docs.microsoft.com/windows/uwp/launch-resume/launch-settings-app#ms-settings-uri-scheme-reference) documentation.</span></span>
