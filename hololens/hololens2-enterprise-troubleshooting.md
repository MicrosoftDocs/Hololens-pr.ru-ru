---
title: Устранение неполадок с реализацией и управляемыми устройствами HoloLens 2
description: Устранение неполадок с устройствами HoloLens 2 в корпоративной среде
author: JoyJaz
ms.author: v-jjaswinski
ms.date: 6/22/2021
ms.topic: article
keywords: Устранение неполадок
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: ''
appliesto:
- HoloLens 2
ms.openlocfilehash: 911e5b9494eae00ace8007ee6a29b30e6aaf98dd
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112961503"
---
# <a name="troubleshooting-implementation-and-managed-devices"></a><span data-ttu-id="860a7-104">Устранение неполадок с реализацией и управляемыми устройствами</span><span class="sxs-lookup"><span data-stu-id="860a7-104">Troubleshooting implementation and managed devices</span></span> 

<span data-ttu-id="860a7-105">В этой статье описывается, как устранить некоторые проблемы или ответить на вопросы, связанные с реализацией и администрированием HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="860a7-105">This article describes how to resolve several issues or answer questions regarding implementation and management of HoloLens 2.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="860a7-106">Прежде чем приступить к устранению неполадок, по возможности убедитесь, что уровень заряда аккумулятора устройства составляет **20–40 %** .</span><span class="sxs-lookup"><span data-stu-id="860a7-106">Before you start any troubleshooting procedure, make sure that your device is charged to **20 to 40 percent** of battery capacity, if possible.</span></span> <span data-ttu-id="860a7-107">[Индикаторы аккумулятора](hololens2-setup.md#lights-that-indicate-the-battery-level), расположенные под кнопкой питания, позволяют быстро проверить заряд аккумулятора без входа в устройство.</span><span class="sxs-lookup"><span data-stu-id="860a7-107">The [battery indicator lights](hololens2-setup.md#lights-that-indicate-the-battery-level) located under the power button are a quick way to verify the battery capacity without logging into the device.</span></span>


<a id="list"></a>
- [<span data-ttu-id="860a7-108">Устранение неполадок с EAP</span><span class="sxs-lookup"><span data-stu-id="860a7-108">EAP Troubleshooting</span></span>](#eap-troubleshooting)
- [<span data-ttu-id="860a7-109">Устранение неполадок с Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="860a7-109">Wi-Fi Troubleshooting</span></span>](#wi-fi-troubleshooting)
- [<span data-ttu-id="860a7-110">Устранение неполадок с сетью</span><span class="sxs-lookup"><span data-stu-id="860a7-110">Network Troubleshooting</span></span>](#network-troubleshooting)
- [<span data-ttu-id="860a7-111">Не удается войти в настроенное ранее устройство HoloLens</span><span class="sxs-lookup"><span data-stu-id="860a7-111">Can't sign in to a previously setup HoloLens device</span></span>](#cant-sign-in-to-a-previously-setup-hololens-device)
- [<span data-ttu-id="860a7-112">Не удается войти после обновления до Windows Holographic 21H1</span><span class="sxs-lookup"><span data-stu-id="860a7-112">Can't login after updating to Windows Holographic 21H1</span></span>](#cant-login-after-updating-to-windows-holographic-21h1)
- [<span data-ttu-id="860a7-113">Устранение неполадок с Autopilot</span><span class="sxs-lookup"><span data-stu-id="860a7-113">Autopilot Troubleshooting</span></span>](#autopilot-troubleshooting)
- [<span data-ttu-id="860a7-114">Часто задаваемые вопросы об управляемых устройствах HoloLens</span><span class="sxs-lookup"><span data-stu-id="860a7-114">Managed HoloLens Devices FAQs</span></span>](#managed-hololens-devices-faqs)

## <a name="eap-troubleshooting"></a><span data-ttu-id="860a7-115">Устранение неполадок с EAP</span><span class="sxs-lookup"><span data-stu-id="860a7-115">EAP Troubleshooting</span></span>
1. <span data-ttu-id="860a7-116">Необходимо внимательно проверить следующие настройки профиля Wi-Fi:</span><span class="sxs-lookup"><span data-stu-id="860a7-116">Double check Wi-Fi profile has right settings:</span></span>
    - <span data-ttu-id="860a7-117">Правильная настройка типа EAP, распространенные типы EAP: EAP-TLS (13), EAP-TTLS (21) и PEAP (25).</span><span class="sxs-lookup"><span data-stu-id="860a7-117">EAP type is configured correctly, common EAP types: EAP-TLS (13), EAP-TTLS (21) and PEAP (25).</span></span>
    - <span data-ttu-id="860a7-118">Правильность идентификатора SSID Wi-Fi и его совпадение с шестнадцатеричной строкой.</span><span class="sxs-lookup"><span data-stu-id="860a7-118">Wi-Fi SSID name is right and matches with HEX string.</span></span>
    - <span data-ttu-id="860a7-119">Для EAP-TLS: наличие в TrustedRootCA хэша SHA-1 сертификата доверенного корневого центра сертификации сервера.</span><span class="sxs-lookup"><span data-stu-id="860a7-119">For EAP-TLS, TrustedRootCA contains the SHA-1 hash of server's trusted root CA certificate.</span></span> <span data-ttu-id="860a7-120">На ПК с Windows строку хэша SHA-1 для сертификата можно получить с помощью команды certutil.exe -dump cert_file_name.</span><span class="sxs-lookup"><span data-stu-id="860a7-120">On Windows PC "certutil.exe -dump cert_file_name" command will show a certificate's SHA-1 hash string.</span></span>
2. <span data-ttu-id="860a7-121">Чтобы узнать, в каких случаях происходит сбой сеанса EAP, запишите сетевые пакеты в журнале точки доступа, контроллера или сервера AAA.</span><span class="sxs-lookup"><span data-stu-id="860a7-121">Collect network packet capture on the Access Point or Controller or AAA server logs to find out where the EAP session fails.</span></span>
    - <span data-ttu-id="860a7-122">Если удостоверение EAP, предоставленное службой HoloLens, не соответствует ожидаемому, проверьте правильность удостоверения, предоставленного с помощью профиля Wi-Fi или клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="860a7-122">If the EAP identity provided by HoloLens is not expected, check whether the identity has been correctly provisioned through Wi-Fi profile or client certificate.</span></span>
    - <span data-ttu-id="860a7-123">Если сервер отклонил сертификат клиента HoloLens, убедитесь, что на устройстве установлен требуемый сертификат клиента.</span><span class="sxs-lookup"><span data-stu-id="860a7-123">If server rejects HoloLens client certificate, check whether the required client certificate has been provisioned on the device.</span></span>
    - <span data-ttu-id="860a7-124">Если HoloLens отклоняет сертификат сервера, убедитесь, что на HoloLens установлен сертификат корневого ЦС сервера.</span><span class="sxs-lookup"><span data-stu-id="860a7-124">If HoloLens rejects server certificate, check if the server root CA certificate has been provisioned on HoloLens.</span></span>
3. <span data-ttu-id="860a7-125">Если профиль предприятия предоставлен с помощью пакета подготовки Wi-Fi, рассмотрите возможность установки пакета подготовки на компьютер с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="860a7-125">If the enterprise profile is provisioned through Wi-Fi provisioning package, consider applying the provisioning package on a Windows 10 PC.</span></span> <span data-ttu-id="860a7-126">Если при этом на ПК с Windows 10 также возникает сбой, выполните инструкции по устранению неполадок с аутентификацией 802.1X для клиента Windows.</span><span class="sxs-lookup"><span data-stu-id="860a7-126">If it also fails on Windows 10 PC, follow the Windows client 802.1X authentication troubleshooting guide.</span></span>
4. <span data-ttu-id="860a7-127">Отправьте нам отзыв через Центр отзывов.</span><span class="sxs-lookup"><span data-stu-id="860a7-127">Send us feedback through Feedback Hub.</span></span>

[<span data-ttu-id="860a7-128">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="860a7-128">Back to list</span></span>](#list)

## <a name="wi-fi-troubleshooting"></a><span data-ttu-id="860a7-129">Устранение неполадок с Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="860a7-129">Wi-Fi Troubleshooting</span></span>

<span data-ttu-id="860a7-130">Ниже приведены некоторые действия, которые рекомендуется выполнить, если вы не можете подключить HoloLens к сети Wi-Fi:</span><span class="sxs-lookup"><span data-stu-id="860a7-130">Here are some things to try if you can't connect your HoloLens to a Wi-Fi network:</span></span>

1. <span data-ttu-id="860a7-131">Убедитесь, что интерфейс Wi-Fi включен.</span><span class="sxs-lookup"><span data-stu-id="860a7-131">Make sure that Wi-Fi is turned on.</span></span> <span data-ttu-id="860a7-132">Для этого выполните жест "Пуск", а затем выберите "Параметры" > "Сеть и Интернет" > "Wi-Fi".</span><span class="sxs-lookup"><span data-stu-id="860a7-132">To check, use the Start gesture, then select Settings > Network & Internet > Wi-Fi.</span></span> <span data-ttu-id="860a7-133">Если интерфейс Wi-Fi включен, попробуйте отключить его и снова включить.</span><span class="sxs-lookup"><span data-stu-id="860a7-133">If Wi-Fi is on, try turning it off and then on again.</span></span>
2. <span data-ttu-id="860a7-134">Переместитесь ближе к маршрутизатору или точке доступа.</span><span class="sxs-lookup"><span data-stu-id="860a7-134">Move closer to the router or access point.</span></span>
3. <span data-ttu-id="860a7-135">Перезапустите маршрутизатор Wi-Fi, а затем перезапустите HoloLens.</span><span class="sxs-lookup"><span data-stu-id="860a7-135">Restart your Wi-Fi router, then restart HoloLens.</span></span> <span data-ttu-id="860a7-136">Повторите попытку подключения.</span><span class="sxs-lookup"><span data-stu-id="860a7-136">Try connecting again.</span></span>
4. <span data-ttu-id="860a7-137">Если ни одно из этих действий не помогло, убедитесь, что на маршрутизаторе используется последняя версия встроенного ПО.</span><span class="sxs-lookup"><span data-stu-id="860a7-137">If none of these things work, check to make sure that your router is using the latest firmware.</span></span> <span data-ttu-id="860a7-138">Эти сведения можно найти на веб-сайте изготовителя.</span><span class="sxs-lookup"><span data-stu-id="860a7-138">You can find this information on the manufacturer website.</span></span>

<span data-ttu-id="860a7-139">Когда выполняется вход в учетную запись предприятия или организации на устройстве, также может применяться политика управления мобильными устройствами (MDM), если она настроена ИТ-администратором.</span><span class="sxs-lookup"><span data-stu-id="860a7-139">When you sign into an enterprise or organizational account on the device, it may also apply Mobile Device Management (MDM) policy, if the policy is configured by your IT administrator.</span></span>

## <a name="network-troubleshooting"></a><span data-ttu-id="860a7-140">Устранение неполадок с сетью</span><span class="sxs-lookup"><span data-stu-id="860a7-140">Network Troubleshooting</span></span>
<span data-ttu-id="860a7-141">Если проблемы с сетью мешают успешному развертыванию и использованию HoloLens 2 в организации, найти, диагностировать и идентифицировать проблемы вам помогут Fiddler и Wireshark — два популярных инструмента для диагностики сети.</span><span class="sxs-lookup"><span data-stu-id="860a7-141">If network issues are an obstacle to successfully deploying and using HoloLens 2 in your organization, learn how two well-known network diagnostic tools, Fiddler and Wireshark can help you scan, diagnose, and identify problems.</span></span> <span data-ttu-id="860a7-142">Дополнительные сведения см. в этом [блоге](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/diagnose-hololens-2-network-issues-with-fiddler-and-wireshark/ba-p/2322458).</span><span class="sxs-lookup"><span data-stu-id="860a7-142">Check out this [blog](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/diagnose-hololens-2-network-issues-with-fiddler-and-wireshark/ba-p/2322458) for more details.</span></span>

[<span data-ttu-id="860a7-143">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="860a7-143">Back to list</span></span>](#list)

## <a name="cant-sign-in-to-a-previously-setup-hololens-device"></a><span data-ttu-id="860a7-144">Не удается войти в настроенное ранее устройство HoloLens</span><span class="sxs-lookup"><span data-stu-id="860a7-144">Can't sign in to a previously setup HoloLens device</span></span>

<span data-ttu-id="860a7-145">Если устройство было ранее настроено для другого пользователя (клиента или бывшего сотрудника) и у вас нет пароля для разблокировки устройства, с помощью Intune вы можете выполнить удаленную [очистку](https://docs.microsoft.com/intune/remote-actions/devices-wipe) устройства.</span><span class="sxs-lookup"><span data-stu-id="860a7-145">If your device was previously set up for someone else, either for a client or for a former employee, and you don't have their password to unlock the device, you can use Intune to remotely [wipe](https://docs.microsoft.com/intune/remote-actions/devices-wipe) the device.</span></span> <span data-ttu-id="860a7-146">После этого устройство самостоятельно установит нужный образ.</span><span class="sxs-lookup"><span data-stu-id="860a7-146">The device then re-flashes itself.</span></span>  
> [!IMPORTANT]
> <span data-ttu-id="860a7-147">При очистке устройства не устанавливайте флажок **Сохранить состояние регистрации и учетную запись пользователя**.</span><span class="sxs-lookup"><span data-stu-id="860a7-147">When you wipe the device, make sure to leave **Retain enrollment state and user account** unchecked.</span></span>
[<span data-ttu-id="860a7-148">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="860a7-148">Back to list</span></span>](#list)

## <a name="cant-login-after-updating-to-windows-holographic-21h1"></a><span data-ttu-id="860a7-149">Не удается войти после обновления до Windows Holographic 21H1</span><span class="sxs-lookup"><span data-stu-id="860a7-149">Can't login after updating to Windows Holographic 21H1</span></span>

### <a name="symptoms"></a><span data-ttu-id="860a7-150">Симптомы</span><span class="sxs-lookup"><span data-stu-id="860a7-150">Symptoms</span></span>
- <span data-ttu-id="860a7-151">При вводе правильного PIN-кода для входа возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="860a7-151">Using PIN to logon will fail after entering the correct PIN.</span></span>
- <span data-ttu-id="860a7-152">При использовании метода входа через Интернет возникает ошибка после успешного входа на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="860a7-152">Using the web logon method will fail after successfully signing in on the web page.</span></span>
- <span data-ttu-id="860a7-153">Устройство не имеет статуса "Присоединено к Azure AD" на [портале Azure](https://portal.azure.com/) (Azure Active Directory -> Устройства).</span><span class="sxs-lookup"><span data-stu-id="860a7-153">The device is not listed as “Azure AD joined” in [Azure portal](https://portal.azure.com/) -> Azure Active Directory -> Devices.</span></span>

### <a name="cause"></a><span data-ttu-id="860a7-154">Причина</span><span class="sxs-lookup"><span data-stu-id="860a7-154">Cause</span></span>
<span data-ttu-id="860a7-155">Возможно, устройство с ошибкой удалено из арендатора Azure AD.</span><span class="sxs-lookup"><span data-stu-id="860a7-155">The impacted device may have been deleted from the Azure AD tenant.</span></span> <span data-ttu-id="860a7-156">Например, это могло произойти по следующей причине:</span><span class="sxs-lookup"><span data-stu-id="860a7-156">For example, this may happen because:</span></span>

- <span data-ttu-id="860a7-157">Администратор или пользователь удалил устройство на портале Azure или с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="860a7-157">An administrator or user deleted the device in the Azure portal or using PowerShell.</span></span>
- <span data-ttu-id="860a7-158">Устройство было удалено из арендатора Azure AD из-за неактивности.</span><span class="sxs-lookup"><span data-stu-id="860a7-158">The device was removed from the Azure AD tenant due to inactivity.</span></span> <span data-ttu-id="860a7-159">Для эффективного управления средой мы обычно рекомендуем ИТ-администраторам [удалять бездействующие, неактивные устройства из арендатора Azure AD](https://docs.microsoft.com/azure/active-directory/devices/manage-stale-devices).</span><span class="sxs-lookup"><span data-stu-id="860a7-159">For an efficiently managed environment, we typically recommend IT admins to [remove stale, inactive devices from their Azure AD tenant](https://docs.microsoft.com/azure/active-directory/devices/manage-stale-devices).</span></span>

<span data-ttu-id="860a7-160">Когда устройство с ошибкой попытается повторно обратиться к арендатору Azure AD после его удаления, его аутентификация в Azure AD завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="860a7-160">When an impacted device attempts to contact the Azure AD tenant again after it has been deleted it will fail to authenticate with Azure AD.</span></span> <span data-ttu-id="860a7-161">Пользователь устройства часто остается в неведении о такой проблеме, так как кэшируемый вход с помощью PIN-кода будет разрешать пользователю вход.</span><span class="sxs-lookup"><span data-stu-id="860a7-161">This effect is often invisible to the user of the device, as cached logon via PIN will continue to allow the user to logon.</span></span>

### <a name="mitigation"></a><span data-ttu-id="860a7-162">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="860a7-162">Mitigation</span></span>
<span data-ttu-id="860a7-163">Пока нет способа добавить удаленное устройство HoloLens обратно в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="860a7-163">There is currently no way to add a deleted HoloLens device back into Azure AD.</span></span> <span data-ttu-id="860a7-164">Для затронутых устройств необходимо будет выполнить чистую установку образа с помощью [соответствующих инструкций](hololens-recovery.md#clean-reflash-the-device).</span><span class="sxs-lookup"><span data-stu-id="860a7-164">Affected devices will need to be clean-reflashed by following the instructions on [reflashing their device](hololens-recovery.md#clean-reflash-the-device).</span></span>

## <a name="autopilot-troubleshooting"></a><span data-ttu-id="860a7-165">Устранение неполадок с Autopilot</span><span class="sxs-lookup"><span data-stu-id="860a7-165">Autopilot Troubleshooting</span></span>

<span data-ttu-id="860a7-166">Указанные ниже статьи могут быть полезны при сборе информации о проблемах с Autopilot и их устранении, однако следует учитывать, что эти статьи написаны для классических версий Windows 10, и не вся информация в них может быть применима к HoloLens:</span><span class="sxs-lookup"><span data-stu-id="860a7-166">The following articles may be a useful resource for you to learn more information and troubleshoot Autopilot Issues, however please be aware that these articles are based on Windows 10 Desktop and not all information may apply to HoloLens:</span></span>

- [<span data-ttu-id="860a7-167">Известные проблемы с Windows Autopilot</span><span class="sxs-lookup"><span data-stu-id="860a7-167">Windows Autopilot - known issues</span></span>](https://docs.microsoft.com/mem/autopilot/known-issues)
- [<span data-ttu-id="860a7-168">Устранение проблем с регистрацией устройств Windows в Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="860a7-168">Troubleshoot Windows device enrollment problems in Microsoft Intune</span></span>](https://docs.microsoft.com/mem/intune/enrollment/troubleshoot-windows-enrollment-errors)
- [<span data-ttu-id="860a7-169">Windows Autopilot — конфликты политик</span><span class="sxs-lookup"><span data-stu-id="860a7-169">Windows Autopilot - Policy Conflicts</span></span>](https://docs.microsoft.com/mem/autopilot/policy-conflicts)

## <a name="managed-hololens-devices-faqs"></a><span data-ttu-id="860a7-170">Часто задаваемые вопросы об управляемых устройствах HoloLens</span><span class="sxs-lookup"><span data-stu-id="860a7-170">Managed HoloLens Devices FAQs</span></span>

### <a name="can-i-use-system-center-configuration-manager-sccm-to-manage-hololens-devices"></a><span data-ttu-id="860a7-171">Можно ли использовать System Center Configuration Manager (SCCM) для управления устройствами HoloLens?</span><span class="sxs-lookup"><span data-stu-id="860a7-171">Can I use System Center Configuration Manager (SCCM) to manage HoloLens devices?</span></span>

<span data-ttu-id="860a7-172">Нет.</span><span class="sxs-lookup"><span data-stu-id="860a7-172">No.</span></span> <span data-ttu-id="860a7-173">Для управления устройствами HoloLens необходимо использовать систему MDM.</span><span class="sxs-lookup"><span data-stu-id="860a7-173">You have to use an MDM system to manage HoloLens devices.</span></span>

### <a name="can-i-use-active-directory-domain-services-ad-ds-to-manage-hololens-user-accounts"></a><span data-ttu-id="860a7-174">Можно ли использовать доменные службы Active Directory (AD DS) для управления учетными записями пользователей HoloLens?</span><span class="sxs-lookup"><span data-stu-id="860a7-174">Can I use Active Directory Domain Services (AD DS) to manage HoloLens user accounts?</span></span>

<span data-ttu-id="860a7-175">Нет.</span><span class="sxs-lookup"><span data-stu-id="860a7-175">No.</span></span> <span data-ttu-id="860a7-176">Для управления учетными записями пользователей устройств HoloLens необходимо использовать Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="860a7-176">You have to use Azure Active Directory (Azure AD) to manage user accounts for HoloLens devices.</span></span>

### <a name="is-hololens-capable-of-automated-data-capture-systems-adcs-auto-enrollment"></a><span data-ttu-id="860a7-177">Может ли HoloLens выполнять автоматическую регистрацию в системах автоматического сбора данных (ADCS)?</span><span class="sxs-lookup"><span data-stu-id="860a7-177">Is HoloLens capable of Automated Data Capture Systems (ADCS) auto-enrollment?</span></span>

<span data-ttu-id="860a7-178">Нет.</span><span class="sxs-lookup"><span data-stu-id="860a7-178">No.</span></span>

### <a name="can-hololens-participate-in-integrated-windows-authentication"></a><span data-ttu-id="860a7-179">Может ли HoloLens выполнять встроенную аутентификацию Windows?</span><span class="sxs-lookup"><span data-stu-id="860a7-179">Can HoloLens participate in Integrated Windows Authentication?</span></span>

<span data-ttu-id="860a7-180">Нет.</span><span class="sxs-lookup"><span data-stu-id="860a7-180">No.</span></span>

### <a name="does-hololens-support-branding"></a><span data-ttu-id="860a7-181">Поддерживает ли HoloLens фирменную символику?</span><span class="sxs-lookup"><span data-stu-id="860a7-181">Does HoloLens support branding?</span></span>

<span data-ttu-id="860a7-182">Нет.</span><span class="sxs-lookup"><span data-stu-id="860a7-182">No.</span></span> <span data-ttu-id="860a7-183">Но для решения этой проблемы можно воспользоваться одним из следующих подходов:</span><span class="sxs-lookup"><span data-stu-id="860a7-183">However, you can work around this issue by using one of the following approaches:</span></span>

- <span data-ttu-id="860a7-184">Создайте пользовательское приложение, а затем [включите режим киоска](hololens-kiosk.md).</span><span class="sxs-lookup"><span data-stu-id="860a7-184">Create a custom app, and then [enable Kiosk mode](hololens-kiosk.md).</span></span> <span data-ttu-id="860a7-185">Пользовательское приложение может иметь фирменную символику, а также запускать другие приложения (например, Remote Assist).</span><span class="sxs-lookup"><span data-stu-id="860a7-185">The custom app can have branding, and can launch other apps (such as Remote Assist).</span></span>  
- <span data-ttu-id="860a7-186">Измените все изображения профилей пользователей в Azure AD на логотип вашей компании.</span><span class="sxs-lookup"><span data-stu-id="860a7-186">Change all of the user profile pictures in Azure AD to your company logo.</span></span> <span data-ttu-id="860a7-187">Но в некоторых сценариях это может быть нежелательным.</span><span class="sxs-lookup"><span data-stu-id="860a7-187">However, this may not be desirable for all scenarios.</span></span>

### <a name="what-logging-capabilities-does-hololens-2-offer"></a><span data-ttu-id="860a7-188">Какие возможности ведения журналов доступны в HoloLens 2?</span><span class="sxs-lookup"><span data-stu-id="860a7-188">What logging capabilities does HoloLens 2 offer?</span></span>

<span data-ttu-id="860a7-189">Ведение журналов ограничено трассировками, которые могут собираться в сценариях разработки или устранения неполадок, или данными телеметрии, которые устройства отправляют на серверы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="860a7-189">Logging is limited to traces that can be captured in development or troubleshooting scenarios, or telemetry that the devices send to Microsoft servers.</span></span>

## <a name="questions-about-securing-hololens-devices"></a><span data-ttu-id="860a7-190">Вопросы о защите устройств HoloLens</span><span class="sxs-lookup"><span data-stu-id="860a7-190">Questions about securing HoloLens devices</span></span>

<span data-ttu-id="860a7-191">Ознакомьтесь с [информацией о безопасности HoloLens 2](security-overview.md).</span><span class="sxs-lookup"><span data-stu-id="860a7-191">See [our HoloLens 2 security information](security-overview.md).</span></span>
<span data-ttu-id="860a7-192">Дополнительные сведения о HoloLens 1-го поколения см. в [этих часто задаваемых вопросах](hololens1-faq-security.md).</span><span class="sxs-lookup"><span data-stu-id="860a7-192">For HoloLens 1st Gen devices please review [this FAQ](hololens1-faq-security.md).</span></span>

[<span data-ttu-id="860a7-193">Назад к списку</span><span class="sxs-lookup"><span data-stu-id="860a7-193">Back to list</span></span>](#list)
