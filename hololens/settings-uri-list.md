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
ms.openlocfilehash: f004f39f4b69748e8c36ad93111f4423d14c40f3
ms.sourcegitcommit: 23ee06b659d7a51f3000d386c8f67cbf212d5aa4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "11327393"
---
# <span data-ttu-id="372d9-104">Видимость параметров страницы</span><span class="sxs-lookup"><span data-stu-id="372d9-104">Page Settings Visibility</span></span>

<span data-ttu-id="372d9-105">Одной из управляемых функций для устройств HoloLens является использование [политики Settings/PageVisibilityList](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist), чтобы ограничивать страницы, отображаемые в приложении "Параметры".</span><span class="sxs-lookup"><span data-stu-id="372d9-105">One of the manageable features for HoloLens devices is using the [Settings/PageVisibilityList policy](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist) to restrict the pages seen within the Settings app.</span></span> <span data-ttu-id="372d9-106">PageVisibilityList — это политика, позволяющая ИТ-администраторам запрещать отображение или открытие определенных страниц в приложении "Параметры системы" или наоборот — выполнять это для всех страниц, кроме указанных.</span><span class="sxs-lookup"><span data-stu-id="372d9-106">PageVisibilityList is a policy that allows IT Admins to either prevent specific pages in the System Settings app from being visible or accessible, or to do so for all pages except those specified.</span></span>

> [!NOTE]
> <span data-ttu-id="372d9-107">Эта функция доступна только в [Windows Holographic версии 20H2](hololens-release-notes.md#windows-holographic-version-20h2) для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="372d9-107">This feature is only avalible in [Windows Holographic, verison 20H2](hololens-release-notes.md#windows-holographic-version-20h2) for HoloLens 2 devices.</span></span> <span data-ttu-id="372d9-108">Обновите устройства, для которых вы собираетесь ее использовать.</span><span class="sxs-lookup"><span data-stu-id="372d9-108">Please ensure devices you intend to use this for are updated.</span></span>

> [!NOTE]
> <span data-ttu-id="372d9-109">В ближайшее время будут добавлены более 20 новых параметров SettingsURI.</span><span class="sxs-lookup"><span data-stu-id="372d9-109">20+ new SettingsURIs are being added soon.</span></span> <span data-ttu-id="372d9-110">Если вы хотите просмотреть этот параметр в предварительной сборке [HoloLens](hololens-insider.md), посетите страницу [Программа предварительной оценки Windows — Новые параметры SettingsURI для видимости параметров страницы](hololens-insider.md#new-settingsuris-for-page-settings-visibility).</span><span class="sxs-lookup"><span data-stu-id="372d9-110">Please view [the Windows Insider page - New SettingsURIs for Page Settings Visibility](hololens-insider.md#new-settingsuris-for-page-settings-visibility) if you are interesting in previewing this setting on a [HoloLens Insider](hololens-insider.md) build.</span></span>

<span data-ttu-id="372d9-111">В примере ниже показана политика, разрешающая доступ только к страницам сведений и Bluetooth с URI "ms-settings:network-wifi" и "ms-settings:bluetooth" соответственно:</span><span class="sxs-lookup"><span data-stu-id="372d9-111">The following example illustrates a policy that would allow access only to the about and bluetooth pages, which have URI "ms-settings:network-wifi" and "ms-settings:bluetooth" respectively:</span></span>
- `showonly:network-wifi;network-proxy;bluetooth`

<span data-ttu-id="372d9-112">Чтобы настроить эту политику с помощью пакета подготовки, выполните следующее.</span><span class="sxs-lookup"><span data-stu-id="372d9-112">To set this via a Provisioning Package:</span></span>

1. <span data-ttu-id="372d9-113">При создании пакета в конструкторе конфигураций Windows выберите **Политики > Параметры > PageVisibilityList**</span><span class="sxs-lookup"><span data-stu-id="372d9-113">While creating your package in Windows Configuration Designer navigate to **Policies > Settings > PageVisibilityList**</span></span>
1. <span data-ttu-id="372d9-114">Введите строку: **`showonly:network-wifi;network-proxy;bluetooth`**</span><span class="sxs-lookup"><span data-stu-id="372d9-114">Enter the string: **`showonly:network-wifi;network-proxy;bluetooth`**</span></span>
1. <span data-ttu-id="372d9-115">Экспортируйте пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="372d9-115">Export your Provisioning Package.</span></span>
1. <span data-ttu-id="372d9-116">Примените пакет к устройству.</span><span class="sxs-lookup"><span data-stu-id="372d9-116">Apply the package to your device.</span></span>
<span data-ttu-id="372d9-117">Подробные сведения о создании и применении пакета подготовки см. на [этой странице](hololens-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="372d9-117">For full details on how to create and apply a provisioning package visit [this page](hololens-provisioning.md).</span></span>

<span data-ttu-id="372d9-118">Это можно сделать с помощью Intune с использованием OMA-URI.</span><span class="sxs-lookup"><span data-stu-id="372d9-118">This can be done via Intune using OMA-URI:</span></span>

1. <span data-ttu-id="372d9-119">Создайте **пользовательскую политику**.</span><span class="sxs-lookup"><span data-stu-id="372d9-119">Create a **Custom policy**.</span></span>
1. <span data-ttu-id="372d9-120">При настройке OMA-URI используйте строку: **`./Device/Vendor/MSFT/Policy/Config/Settings/PageVisibilityList`**</span><span class="sxs-lookup"><span data-stu-id="372d9-120">When setting the OMA-URI use the string: **`./Device/Vendor/MSFT/Policy/Config/Settings/PageVisibilityList`**</span></span>
1. <span data-ttu-id="372d9-121">При выборе комплекта данных укажите: **Строка**</span><span class="sxs-lookup"><span data-stu-id="372d9-121">When selecting the data pick choose: **String**</span></span>
1. <span data-ttu-id="372d9-122">При вводе значения используйте: **`showonly:network-wifi;network-proxy;bluetooth`**</span><span class="sxs-lookup"><span data-stu-id="372d9-122">When typing the value use: **`showonly:network-wifi;network-proxy;bluetooth`**</span></span>
1. <span data-ttu-id="372d9-123">Назначьте настраиваемую конфигурацию устройства группе, в которой должно располагаться устройство.</span><span class="sxs-lookup"><span data-stu-id="372d9-123">Make sure to assign the custom device configuration to a group the device is intended to be in.</span></span>

<span data-ttu-id="372d9-124">Дополнительные сведения о группах Intune и конфигурации устройств см. в статье [Конфигурация HoloLens в MDM](hololens-mdm-configure.md).</span><span class="sxs-lookup"><span data-stu-id="372d9-124">See [HoloLens MDM configuration](hololens-mdm-configure.md) for more information on Intune groups and device configurations.</span></span>

<span data-ttu-id="372d9-125">Независимо от выбранного метода ваше устройство должно теперь получать изменения, а пользователи получат следующее приложение "Параметры".</span><span class="sxs-lookup"><span data-stu-id="372d9-125">Regardless of method chosen your device should now receive the changes and users will be presented with the following Settings App.</span></span>

![Снимок экрана: период активности, измененный в приложении "Параметры"](images/hololens-page-visibility-list.jpg)

<span data-ttu-id="372d9-127">Чтобы настроить страницы приложения "Параметры" для отображения или скрытия выбранных страниц, просмотрите URI параметров, доступные в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="372d9-127">To configure the Settings app pages to show or hide your own selection of pages, take a look at the Settings URIs available on HoloLens.</span></span>

## <span data-ttu-id="372d9-128">URI параметров</span><span class="sxs-lookup"><span data-stu-id="372d9-128">Settings URIs</span></span>

<span data-ttu-id="372d9-129">Устройства HoloLens и Windows 10 имеют разный выбор страниц в приложении "Параметры".</span><span class="sxs-lookup"><span data-stu-id="372d9-129">HoloLens devices and Windows 10 devices have a different selection of pages within the Settings app.</span></span> <span data-ttu-id="372d9-130">На этой странице приведены только параметры, существующие в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="372d9-130">On this page, you will find only the settings that exist on HoloLens.</span></span>

### <span data-ttu-id="372d9-131">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="372d9-131">Accounts</span></span>
| <span data-ttu-id="372d9-132">Страница параметров</span><span class="sxs-lookup"><span data-stu-id="372d9-132">Settings page</span></span>           | <span data-ttu-id="372d9-133">URI</span><span class="sxs-lookup"><span data-stu-id="372d9-133">URI</span></span>                                            |
|-------------------------|------------------------------------------------|
| <span data-ttu-id="372d9-134">Параметры входа</span><span class="sxs-lookup"><span data-stu-id="372d9-134">Sign In Options</span></span>         | ` ms-settings:signinoptions `                   |
| <span data-ttu-id="372d9-135">Регистрация Iris</span><span class="sxs-lookup"><span data-stu-id="372d9-135">Iris Enrollment</span></span>       | `ms-settings:signinoptions-launchirisenrollment` |
| <span data-ttu-id="372d9-136">Доступ на рабочем месте или в учебном учреждении</span><span class="sxs-lookup"><span data-stu-id="372d9-136">Access work or school</span></span> | `ms-settings:workplace`                         |

### <span data-ttu-id="372d9-137">Устройства</span><span class="sxs-lookup"><span data-stu-id="372d9-137">Devices</span></span>
| <span data-ttu-id="372d9-138">Страница параметров</span><span class="sxs-lookup"><span data-stu-id="372d9-138">Settings page</span></span> | <span data-ttu-id="372d9-139">URI</span><span class="sxs-lookup"><span data-stu-id="372d9-139">URI</span></span>                          |
|---------------|------------------------------|
| <span data-ttu-id="372d9-140">Bluetooth</span><span class="sxs-lookup"><span data-stu-id="372d9-140">Bluetooth</span></span>     | `ms-settings:bluetooth` <br> `ms-settings:connecteddevices` |

### <span data-ttu-id="372d9-141">Конфиденциальность</span><span class="sxs-lookup"><span data-stu-id="372d9-141">Privacy</span></span>
| <span data-ttu-id="372d9-142">Страница параметров</span><span class="sxs-lookup"><span data-stu-id="372d9-142">Settings page</span></span>            | <span data-ttu-id="372d9-143">URI</span><span class="sxs-lookup"><span data-stu-id="372d9-143">URI</span></span>                                             |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="372d9-144">Сведения об учетной записи</span><span class="sxs-lookup"><span data-stu-id="372d9-144">Account Info</span></span>             | `ms-settings:privacy-accountinfo`              |
| <span data-ttu-id="372d9-145">Диагностика приложений</span><span class="sxs-lookup"><span data-stu-id="372d9-145">App Diagnostics</span></span>        | `ms-settings:privacy-appdiagnostics`              |
| <span data-ttu-id="372d9-146">Фоновые приложения</span><span class="sxs-lookup"><span data-stu-id="372d9-146">Background Apps</span></span>        | `ms-settings:privacy-backgroundapps`              |
| <span data-ttu-id="372d9-147">Движения пользователей</span><span class="sxs-lookup"><span data-stu-id="372d9-147">User movements</span></span>           | `ms-settings:privacy-backgroundspatialperception` |
| <span data-ttu-id="372d9-148">Файловая система</span><span class="sxs-lookup"><span data-stu-id="372d9-148">File system</span></span>              | `ms-settings:privacy-broadfilesystemaccess`       |
| <span data-ttu-id="372d9-149">Календарь</span><span class="sxs-lookup"><span data-stu-id="372d9-149">Calendar</span></span>                 | `ms-settings:privacy-calendar`                    |
| <span data-ttu-id="372d9-150">Журнал вызовов</span><span class="sxs-lookup"><span data-stu-id="372d9-150">Call History</span></span>             | `ms-settings:privacy-callhistory`                 |
| <span data-ttu-id="372d9-151">Контакты</span><span class="sxs-lookup"><span data-stu-id="372d9-151">Contacts</span></span>                 | `ms-settings:privacy-contacts`                    |
| <span data-ttu-id="372d9-152">Другие устройства</span><span class="sxs-lookup"><span data-stu-id="372d9-152">Other devices</span></span>            | `ms-settings:privacy-customdevices`               |
| <span data-ttu-id="372d9-153">Документы</span><span class="sxs-lookup"><span data-stu-id="372d9-153">Documents</span></span>                | `ms-settings:privacy-documents`                   |
| <span data-ttu-id="372d9-154">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="372d9-154">Email</span></span>                    | `ms-settings:privacy-email`                       |
| <span data-ttu-id="372d9-155">Диагностика и отзывы</span><span class="sxs-lookup"><span data-stu-id="372d9-155">Diagnostics & Feedback</span></span> | `ms-settings:privacy-feedback`                    |
| <span data-ttu-id="372d9-156">Расположение</span><span class="sxs-lookup"><span data-stu-id="372d9-156">Location</span></span>                 | `ms-settings:privacy-location`                    |
| <span data-ttu-id="372d9-157">Сообщения</span><span class="sxs-lookup"><span data-stu-id="372d9-157">Messaging</span></span>                | `ms-settings:privacy-messaging`                   |
| <span data-ttu-id="372d9-158">Микрофон</span><span class="sxs-lookup"><span data-stu-id="372d9-158">Microphone</span></span>               | `ms-settings:privacy-microphone`                  |
| <span data-ttu-id="372d9-159">Уведомления</span><span class="sxs-lookup"><span data-stu-id="372d9-159">Notifications</span></span>            | `ms-settings:privacy-notifications`               |
| <span data-ttu-id="372d9-160">Изображения</span><span class="sxs-lookup"><span data-stu-id="372d9-160">Pictures</span></span>                 | `ms-settings:privacy-pictures`                    |
| <span data-ttu-id="372d9-161">Радиомодули</span><span class="sxs-lookup"><span data-stu-id="372d9-161">Radios</span></span>                   | `ms-settings:privacy-radios`                      |
| <span data-ttu-id="372d9-162">Речь</span><span class="sxs-lookup"><span data-stu-id="372d9-162">Speech</span></span>                   | `ms-settings:privacy-speech`                      |
| <span data-ttu-id="372d9-163">Задачи</span><span class="sxs-lookup"><span data-stu-id="372d9-163">Tasks</span></span>                    | `ms-settings:privacy-tasks`                       |
| <span data-ttu-id="372d9-164">Видео</span><span class="sxs-lookup"><span data-stu-id="372d9-164">Videos</span></span>                   | `ms-settings:privacy-videos`                      |
| <span data-ttu-id="372d9-165">Голосовая активация</span><span class="sxs-lookup"><span data-stu-id="372d9-165">Voice Activation</span></span>       | `ms-settings:privacy-voiceactivation`             |
| <span data-ttu-id="372d9-166">Камера</span><span class="sxs-lookup"><span data-stu-id="372d9-166">Camera</span></span>                   | `ms-settings:privacy-webcam`                      |

### <span data-ttu-id="372d9-167">Сеть и Интернет</span><span class="sxs-lookup"><span data-stu-id="372d9-167">Network & Internet</span></span>
| <span data-ttu-id="372d9-168">Страница параметров</span><span class="sxs-lookup"><span data-stu-id="372d9-168">Settings page</span></span> | <span data-ttu-id="372d9-169">URI</span><span class="sxs-lookup"><span data-stu-id="372d9-169">URI</span></span>                              |
|---------------|----------------------------------|
| <span data-ttu-id="372d9-170">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="372d9-170">Wi-Fi</span></span>  | `ms-settings:network-wifi`<br>`ms-settings:network-wifisettings`<br>`ms-settings:network-status`<br>`ms-settings:wifi-provisioning`    |
| <span data-ttu-id="372d9-171">VPN</span><span class="sxs-lookup"><span data-stu-id="372d9-171">VPN</span></span>   | `ms-settings:network-vpn`          |
| <span data-ttu-id="372d9-172">Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="372d9-172">Proxy</span></span> | `ms-settings:network-proxy`        |

### <span data-ttu-id="372d9-173">Система</span><span class="sxs-lookup"><span data-stu-id="372d9-173">System</span></span>
| <span data-ttu-id="372d9-174">Страница параметров</span><span class="sxs-lookup"><span data-stu-id="372d9-174">Settings page</span></span>      | <span data-ttu-id="372d9-175">URI</span><span class="sxs-lookup"><span data-stu-id="372d9-175">URI</span></span>                                |
|--------------------|------------------------------------|
| <span data-ttu-id="372d9-176">Общие возможности</span><span class="sxs-lookup"><span data-stu-id="372d9-176">Shared Experiences</span></span> | `ms-settings:crossdevice`            |
| <span data-ttu-id="372d9-177">Цвета</span><span class="sxs-lookup"><span data-stu-id="372d9-177">Colors</span></span>             | `ms-settings:colors`<br>`ms-settings:personalization-colors` |
| <span data-ttu-id="372d9-178">Уведомления и действия</span><span class="sxs-lookup"><span data-stu-id="372d9-178">Notifications & actions</span></span>  | `ms-settings:notifications`          |
| <span data-ttu-id="372d9-179">Хранилище</span><span class="sxs-lookup"><span data-stu-id="372d9-179">Storage</span></span>            | `ms-settings:storagesense`           |

### <span data-ttu-id="372d9-180">Время и язык</span><span class="sxs-lookup"><span data-stu-id="372d9-180">Time & Language</span></span>
| <span data-ttu-id="372d9-181">Страница параметров</span><span class="sxs-lookup"><span data-stu-id="372d9-181">Settings page</span></span> | <span data-ttu-id="372d9-182">URI</span><span class="sxs-lookup"><span data-stu-id="372d9-182">URI</span></span>                                           |
|---------------|-----------------------------------------------|
| <span data-ttu-id="372d9-183">Region</span><span class="sxs-lookup"><span data-stu-id="372d9-183">Region</span></span>        | `ms-settings:regionformatting`                  |
| <span data-ttu-id="372d9-184">Язык</span><span class="sxs-lookup"><span data-stu-id="372d9-184">Language</span></span>      | `ms-settings:regionlanguage`<br>`ms-settings:regionlanguage-adddisplaylanguage`<br>`ms-settings:regionlanguage-setdisplaylanguage` |

### <span data-ttu-id="372d9-185">Обновление и безопасность</span><span class="sxs-lookup"><span data-stu-id="372d9-185">Update & Security</span></span>
| <span data-ttu-id="372d9-186">Страница параметров</span><span class="sxs-lookup"><span data-stu-id="372d9-186">Settings page</span></span>                         | <span data-ttu-id="372d9-187">URI</span><span class="sxs-lookup"><span data-stu-id="372d9-187">URI</span></span>                                       |
|---------------------------------------|-------------------------------------------|
| <span data-ttu-id="372d9-188">Программа предварительной оценки Windows</span><span class="sxs-lookup"><span data-stu-id="372d9-188">Windows Insider Program</span></span>               | `ms-settings:windowsinsider` <br>`ms-settings:windowsinsider-optin`          |
| <span data-ttu-id="372d9-189">Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="372d9-189">Windows Update</span></span>                        | `ms-settings:windowsupdate`<br> `ms-settings:windowsupdate-activehours`  <br> `ms-settings:windowsupdate-history` <br> `ms-settings:windowsupdate-optionalupdates` <br><sup><span data-ttu-id="372d9-190">1</span><span class="sxs-lookup"><span data-stu-id="372d9-190">1</span></span></sup>`ms-settings:windowsupdate-options`<br><sup><span data-ttu-id="372d9-191">1</span><span class="sxs-lookup"><span data-stu-id="372d9-191">1</span></span></sup>`ms-settings:windowsupdate-restartoptions` |
| <span data-ttu-id="372d9-192">Центр обновления Windows — проверка наличия обновлений</span><span class="sxs-lookup"><span data-stu-id="372d9-192">Windows Update - Checks for updates</span></span> | `ms-settings:windowsupdate-action`          |
| <span data-ttu-id="372d9-193">Дополнительные параметры</span><span class="sxs-lookup"><span data-stu-id="372d9-193">Advanced Options</span></span>                    | `ms-settings:windowsupdate-options`         |

>  <sup><span data-ttu-id="372d9-194">1</sup> Следующие два URI не отправляют вас на страницы **Расширенные параметры** или **Параметры**. Они только блокируют или отображают основную страницу Центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="372d9-194">1</sup> The following two URIs do not actually take you to the **Advanced options** or **Options** pages; they will only block or show the main Windows Update page.</span></span>
> - <span data-ttu-id="372d9-195">ms-settings:windowsupdate-options</span><span class="sxs-lookup"><span data-stu-id="372d9-195">ms-settings:windowsupdate-options</span></span>
> - <span data-ttu-id="372d9-196">ms-settings:windowsupdate-restartoptions</span><span class="sxs-lookup"><span data-stu-id="372d9-196">ms-settings:windowsupdate-restartoptions</span></span> 

<span data-ttu-id="372d9-197">Полный список URI параметров Windows 10 см. в документации по [параметрам запуска](https://docs.microsoft.com/windows/uwp/launch-resume/launch-settings-app#ms-settings-uri-scheme-reference).</span><span class="sxs-lookup"><span data-stu-id="372d9-197">For a full list of Windows 10 Settings URIs, please visit the [launch settings](https://docs.microsoft.com/windows/uwp/launch-resume/launch-settings-app#ms-settings-uri-scheme-reference) documentation.</span></span>
