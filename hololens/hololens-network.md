---
title: Подключение HoloLens к сети
description: Узнайте, как выполнить настройку и подключиться к Интернету с помощью HoloLens, а также как определить IP-адрес устройства.
ms.assetid: 0895606e-96c0-491e-8b1c-52e56b00365d
author: mattzmsft
ms.author: mazeller
keywords: HoloLens, wifi, беспроводной, интернет, ip, ip-адрес
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: ''
manager: jarrettr
ms.openlocfilehash: f1968afe7d450425776bac24532f2d84c4dc3c62
ms.sourcegitcommit: 9f79ed9f76b930b8ceb97844d5f9eace9316b8a3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "11442599"
---
# <a name="connect-hololens-to-a-network"></a><span data-ttu-id="6060b-104">Подключение HoloLens к сети</span><span class="sxs-lookup"><span data-stu-id="6060b-104">Connect HoloLens to a network</span></span>

<span data-ttu-id="6060b-105">Для выполнения большинства задач на устройстве HoloLens устройство должно быть подключено к сети.</span><span class="sxs-lookup"><span data-stu-id="6060b-105">To do most things on your HoloLens, you have to be connected to a network.</span></span> <span data-ttu-id="6060b-106">HoloLens содержит радиомодуль Wi-Fi 2x2 с поддержкой стандарта 802.11ac. Его подключение к сети происходит так же, как подключение к сети Wi-Fi классического или мобильного устройства с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6060b-106">HoloLens contains a 802.11ac-capable, 2x2 Wi-Fi radio and connecting it to a network is similar to connecting a Windows 10 Desktop or Mobile device to a Wi-Fi network.</span></span> <span data-ttu-id="6060b-107">Это руководство поможет вам:</span><span class="sxs-lookup"><span data-stu-id="6060b-107">This guide will help you:</span></span>

- <span data-ttu-id="6060b-108">Подключиться к сети с помощью Wi-Fi или (только для HoloLens 2) Ethernet через USB-C</span><span class="sxs-lookup"><span data-stu-id="6060b-108">Connect to a network using Wi-Fi or (for HoloLens 2 only) Ethernet over USB-C</span></span>
- <span data-ttu-id="6060b-109">Отключить и повторно включить Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="6060b-109">Disable and re-enable Wi-Fi</span></span>

<span data-ttu-id="6060b-110">Подробнее об [использовании HoloLens в автономном режиме](hololens-offline.md).</span><span class="sxs-lookup"><span data-stu-id="6060b-110">Read more about [using HoloLens offline](hololens-offline.md).</span></span>

## <a name="connecting-for-the-first-time"></a><span data-ttu-id="6060b-111">Первое подключение</span><span class="sxs-lookup"><span data-stu-id="6060b-111">Connecting for the first time</span></span>

<span data-ttu-id="6060b-112">При первом использовании HoloLens вам будет предложено пройти процедуру подключения к сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="6060b-112">The first time you use your HoloLens, you'll be guided through connecting to a Wi-Fi network.</span></span> <span data-ttu-id="6060b-113">При наличии проблем с подключением к сети Wi-Fi во время настройки проверьте, открыта ли ваша сеть или она защищена паролем и имеет ли она портал авторизации.</span><span class="sxs-lookup"><span data-stu-id="6060b-113">If you have trouble connecting to Wi-Fi during setup, make sure that your network is either an open, password-protected network or a captive portal network.</span></span> <span data-ttu-id="6060b-114">Кроме того, убедитесь, что для подключения к сети не требуется использование сертификата.</span><span class="sxs-lookup"><span data-stu-id="6060b-114">Also, confirm that the network doesn't require you to use a certificate to connect.</span></span> <span data-ttu-id="6060b-115">После завершения настройки можно будет подключаться к другим типам сетей Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="6060b-115">After setup, you can connect to other types of Wi-Fi networks.</span></span>

<span data-ttu-id="6060b-116">На устройствах HoloLens 2 пользователь может также [использовать адаптер USB-C/Ethernet](hololens-connect-devices.md#hololens-2-connect-usb-c-devices), чтобы напрямую подключиться к сети Wi-Fi для получения помощи в настройке устройства.</span><span class="sxs-lookup"><span data-stu-id="6060b-116">On HoloLens 2 devices, a user may also [use a USB-C to Ethernet adapter](hololens-connect-devices.md#hololens-2-connect-usb-c-devices) to connect directly to Wi-Fi to help assist in setting up the device.</span></span> <span data-ttu-id="6060b-117">После завершения настройки устройства пользователь может продолжать использовать адаптер или отключить его от устройства и [подключиться к сети Wi-Fi](hololens-network.md#connecting-to-wi-fi-after-setup).</span><span class="sxs-lookup"><span data-stu-id="6060b-117">Once the device has been set up a user may continue to use the adapter or they may disconnect the device from the adapter and [connect to wi-fi after set up](hololens-network.md#connecting-to-wi-fi-after-setup).</span></span> 

## <a name="connecting-to-wi-fi-after-setup"></a><span data-ttu-id="6060b-118">Подключение к сети Wi-Fi после настройки</span><span class="sxs-lookup"><span data-stu-id="6060b-118">Connecting to Wi-Fi after setup</span></span>

1. <span data-ttu-id="6060b-119">Выполните **жест "Пуск"**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="6060b-119">Preform the **Start gesture** and select **Settings**.</span></span> <span data-ttu-id="6060b-120">Приложение "Параметры" будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="6060b-120">The Settings app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="6060b-121">Выберите пункты **Сеть и Интернет** > **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="6060b-121">Select **Network & Internet** > **Wi-Fi**.</span></span> <span data-ttu-id="6060b-122">Убедитесь, что функция Wi-Fi включена.</span><span class="sxs-lookup"><span data-stu-id="6060b-122">Make sure Wi-Fi is turned on.</span></span> <span data-ttu-id="6060b-123">Если вы не видите сеть, прокрутите список вниз.</span><span class="sxs-lookup"><span data-stu-id="6060b-123">If you don't see your network, scroll down the list.</span></span>
1. <span data-ttu-id="6060b-124">Выберите сеть и нажмите **Подключение**.</span><span class="sxs-lookup"><span data-stu-id="6060b-124">Select a network, then select **Connect**.</span></span>
1. <span data-ttu-id="6060b-125">В ответ на соответствующий запрос введите сетевой пароль и нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6060b-125">If you are prompted for a network password type it and then select **Next**.</span></span>

![Параметры Wi-Fi HoloLens](./images/hololens-2-wifi-settings.jpg)

<span data-ttu-id="6060b-127">Чтобы подтвердить подключение к сети Wi-Fi, проверьте состояние Wi-Fi в меню **Пуск**:</span><span class="sxs-lookup"><span data-stu-id="6060b-127">To confirm you are connected to a Wi-Fi network, check the Wi-Fi status in the **Start** menu:</span></span>

1. <span data-ttu-id="6060b-128">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="6060b-128">Open the **Start** menu.</span></span>
1. <span data-ttu-id="6060b-129">Проверьте состояние сети Wi-Fi в верхнем левом углу меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="6060b-129">Look at the top left of the **Start** menu for Wi-Fi status.</span></span> <span data-ttu-id="6060b-130">Будет отображено состояние Wi-Fi и SSID подключенной сети.</span><span class="sxs-lookup"><span data-stu-id="6060b-130">The state of Wi-Fi and the SSID of the connected network will be shown.</span></span>

> [!TIP]
> <span data-ttu-id="6060b-131">Если сеть Wi-Fi недоступна, вы также можете [подключиться к мобильной сети и сети 5G](https://docs.microsoft.com/hololens/hololens-cellular).</span><span class="sxs-lookup"><span data-stu-id="6060b-131">If Wi-Fi is not available, you can also [connect to Cellular and 5G networks](https://docs.microsoft.com/hololens/hololens-cellular).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6060b-132">По умолчанию пользователи не могут настроить в HoloLens 2 действие при перемещении в сетях Wi-Fi. **Единственный способ обновить список Wi-Fi — выключить и снова включить сеть Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="6060b-132">By design, users cannot fine tune the Wi-Fi roaming behavior of the HoloLens 2 - **the only way to refresh the Wi-Fi list is to toggle the Wi-Fi Off and On**.</span></span> <span data-ttu-id="6060b-133">Это предотвращает множество проблем, например с зависанием устройства в точке доступа после выхода из ее диапазона.</span><span class="sxs-lookup"><span data-stu-id="6060b-133">This prevents many issues, like where a device can remain "stuck" to an AP once it is out of range.</span></span>

## <a name="troubleshooting-your-connection-to-wi-fi"></a><span data-ttu-id="6060b-134">Устранение неполадок с подключением к Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="6060b-134">Troubleshooting your connection to Wi-Fi</span></span>

<span data-ttu-id="6060b-135">Если у вас возникают проблемы с подключением к Wi-Fi, см. раздел [Не удается подключиться к Wi-Fi](./hololens-faq.md#i-cant-connect-to-wi-fi).</span><span class="sxs-lookup"><span data-stu-id="6060b-135">If you experience problems connecting to Wi-Fi, see [I can't connect to Wi-Fi](./hololens-faq.md#i-cant-connect-to-wi-fi).</span></span>

<span data-ttu-id="6060b-136">Когда выполняется вход в учетную запись предприятия или организации на устройстве, также может применяться политика управления мобильными устройствами (MDM), если она настроена ИТ-администратором.</span><span class="sxs-lookup"><span data-stu-id="6060b-136">When you sign into an enterprise or organizational account on the device, it may also apply Mobile Device Management (MDM) policy, if the policy is configured by your IT administrator.</span></span>

## <a name="connect-hololens-to-enterprise-wi-fi-network"></a><span data-ttu-id="6060b-137">Подключение HoloLens к сети Wi-Fi предприятия</span><span class="sxs-lookup"><span data-stu-id="6060b-137">Connect HoloLens to Enterprise Wi-Fi Network</span></span>

<span data-ttu-id="6060b-138">В корпоративных Wi-Fi профилях для проверки подлинности подключений по Wi-Fi используется протокол расширенной проверки подлинности (EAP).</span><span class="sxs-lookup"><span data-stu-id="6060b-138">Enterprise Wi-Fi profiles use Extensible Authentication Protocol (EAP) to authenticate Wi-Fi connections.</span></span> <span data-ttu-id="6060b-139">Корпоративный профиль HoloLens для Wi-Fi можно настроить с помощью пакета MDM или пакета подготовки, созданного с помощью [конструктора конфигураций Windows](https://docs.microsoft.com/windows/configuration/provisioning-packages/provisioning-packages).</span><span class="sxs-lookup"><span data-stu-id="6060b-139">HoloLens Enterprise Wi-Fi profile can be configured through MDM or provisioning package created by [Windows Configuration Designer](https://docs.microsoft.com/windows/configuration/provisioning-packages/provisioning-packages).</span></span>

<span data-ttu-id="6060b-140">Инструкции по настройке устройства, управляемого с помощью службы Microsoft Intune, приведены в разделе [Intune](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-windows#enterprise-profile).</span><span class="sxs-lookup"><span data-stu-id="6060b-140">For Microsoft Intune managed device, refer to [Intune](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-windows#enterprise-profile) for configuration instructions.</span></span>

<span data-ttu-id="6060b-141">Чтобы создать пакет подготовки Wi-Fi в конструкторе конфигураций Windows, необходимо наличие файла предварительно настроенного профиля Wi-Fi в формате XML.</span><span class="sxs-lookup"><span data-stu-id="6060b-141">To create a Wi-Fi provisioning package in WCD, a pre-configured Wi-Fi profile .xml file is required.</span></span> <span data-ttu-id="6060b-142">Ниже приведен пример профиля Wi-Fi для WPA2-Enterprise с проверкой подлинности EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="6060b-142">Here is a sample Wi-Fi profile for WPA2-Enterprise with EAP-TLS authentication:</span></span>

``` xml
<?xml version="1.0"?> 
<WLANProfile xmlns="http://www.microsoft.com/networking/WLAN/profile/v1"> 
    <name>SampleEapTlsProfile</name> 
    <SSIDConfig> 
        <SSID> 
            <hex>53616d706c65</hex> 
            <name>Sample</name> 
        </SSID> 
        <nonBroadcast>true</nonBroadcast> 
    </SSIDConfig> 
    <connectionType>ESS</connectionType> 
    <connectionMode>auto</connectionMode> 
    <autoSwitch>false</autoSwitch> 
    <MSM> 
        <security> 
            <authEncryption> 
                <authentication>WPA2</authentication> 
                <encryption>AES</encryption> 
                <useOneX>true</useOneX> 
                <FIPSMode xmlns="http://www.microsoft.com/networking/WLAN/profile/v2">false</FIPSMode> 
            </authEncryption> 
            <PMKCacheMode>disabled</PMKCacheMode> 
            <OneX xmlns="http://www.microsoft.com/networking/OneX/v1"> 
                <authMode>machine</authMode> 
                <EAPConfig> 
                    <EapHostConfig xmlns="http://www.microsoft.com/provisioning/EapHostConfig"> 
                        <EapMethod> 
                            <Type xmlns="http://www.microsoft.com/provisioning/EapCommon">13</Type> 
                            <VendorId xmlns="http://www.microsoft.com/provisioning/EapCommon">0</VendorId> 
                            <VendorType xmlns="http://www.microsoft.com/provisioning/EapCommon">0</VendorType> 
                            <AuthorId xmlns="http://www.microsoft.com/provisioning/EapCommon">0</AuthorId> 
                        </EapMethod> 
                        <Config xmlns="http://www.microsoft.com/provisioning/EapHostConfig"> 
                            <Eap xmlns="http://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1"> 
                                <Type>13</Type> 
                                <EapType xmlns="http://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1"> 
                                    <CredentialsSource><CertificateStore><SimpleCertSelection>true</SimpleCertSelection> 
                                        </CertificateStore> 
                                    </CredentialsSource> 
                                    <ServerValidation> 
                                        <DisableUserPromptForServerValidation>false</DisableUserPromptForServerValidation> 
                                        <ServerNames></ServerNames> 
                                        <TrustedRootCA>00 01 02 03 04 05 06 07 08 09 0a 0b 0c 0d 0e 0f 10 11 12 13</TrustedRootCA> 
                                    </ServerValidation> 
                                    <DifferentUsername>false</DifferentUsername> 
                                    <PerformServerValidation xmlns="http://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV2">true</PerformServerValidation> 
                                    <AcceptServerName xmlns="http://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV2">false</AcceptServerName> 
                                </EapType> 
                            </Eap> 
                        </Config> 
                    </EapHostConfig> 
                </EAPConfig> 
            </OneX> 
        </security> 
    </MSM> 
</WLANProfile> 
```


<span data-ttu-id="6060b-143">Сертификат корневого ЦС сервера и сертификат клиента в зависимости от типа EAP, возможно, придется подготовить на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6060b-143">Server root CA certificate and client certificate may need to be provisioned on the device depending on the EAP type.</span></span>

<span data-ttu-id="6060b-144">Дополнительные ресурсы:</span><span class="sxs-lookup"><span data-stu-id="6060b-144">Additional resources:</span></span>

- <span data-ttu-id="6060b-145">Схема WLANv1Profile: [[MS-GPWL]: Схема профиля беспроводной локальной сети v1 | Документация Майкрософт](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/34054c93-cfcd-44df-89d8-5f2ba7532b67)</span><span class="sxs-lookup"><span data-stu-id="6060b-145">WLANv1Profile Schema: [[MS-GPWL]: Wireless LAN Profile v1 Schema | Microsoft Docs](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/34054c93-cfcd-44df-89d8-5f2ba7532b67)</span></span>
- <span data-ttu-id="6060b-146">Схема EAP-TLS: [[MS-GPWL]: Схема протокола EAP TLS корпорации Майкрософт | Документация Майкрософт](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/9590925c-cba2-4ac5-b9a1-1e5292bb72cb)</span><span class="sxs-lookup"><span data-stu-id="6060b-146">EAP-TLS Schema: [[MS-GPWL]: Microsoft EAP TLS Schema | Microsoft Docs](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/9590925c-cba2-4ac5-b9a1-1e5292bb72cb)</span></span>

### <a name="eap-troubleshooting"></a><span data-ttu-id="6060b-147">Устранение неполадок EAP</span><span class="sxs-lookup"><span data-stu-id="6060b-147">EAP Troubleshooting</span></span>

1. <span data-ttu-id="6060b-148">Необходимо внимательно проверить следующие настройки профиля Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="6060b-148">Double check Wi-Fi profile has right settings:</span></span>
   1. <span data-ttu-id="6060b-149">Правильная настройка типа EAP, распространенные типы EAP: EAP-TLS (13), EAP-TTLS (21) и PEAP (25).</span><span class="sxs-lookup"><span data-stu-id="6060b-149">EAP type is configured correctly, common EAP types: EAP-TLS (13), EAP-TTLS (21) and PEAP (25).</span></span>
   1. <span data-ttu-id="6060b-150">Правильность идентификатора SSID Wi-Fi и его совпадение с шестнадцатеричной строкой.</span><span class="sxs-lookup"><span data-stu-id="6060b-150">Wi-Fi SSID name is right and matches with HEX string.</span></span>
   1. <span data-ttu-id="6060b-151">Наличие для EAP-TLS в TrustedRootCA хэша SHA-1 сертификата доверенного корневого центра сертификации сервера.</span><span class="sxs-lookup"><span data-stu-id="6060b-151">For EAP-TLS, TrustedRootCA contains the SHA-1 hash of server&#39;s trusted root CA certificate.</span></span> <span data-ttu-id="6060b-152">На компьютере с Windows строку хэша SHA-1 сертификата можно увидеть с помощью команды &quot;certutil.exe -dump cert\_file\_name&quot;.</span><span class="sxs-lookup"><span data-stu-id="6060b-152">On Windows PC &quot;certutil.exe -dump cert\_file\_name&quot; command will show a certificate&#39;s SHA-1 hash string.</span></span>
1. <span data-ttu-id="6060b-153">Чтобы узнать, в каких случаях происходит сбой сеанса EAP, запишите сетевые пакеты в журнале точки доступа, контроллера или сервера AAA.</span><span class="sxs-lookup"><span data-stu-id="6060b-153">Collect network packet capture on the Access Point or Controller or AAA server logs to find out where the EAP session fails.</span></span>
   1. <span data-ttu-id="6060b-154">Если удостоверение EAP, предоставленное службой HoloLens, не соответствует ожидаемому, проверьте правильность удостоверения, предоставленного с помощью профиля Wi-Fi или клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="6060b-154">If the EAP identity provided by HoloLens is not expected, check whether the identity has been correctly provisioned through Wi-Fi profile or client certificate.</span></span>
   1. <span data-ttu-id="6060b-155">Если сервер отклонил сертификат клиента HoloLens, убедитесь, что на устройстве был установлен требуемый сертификат клиента.</span><span class="sxs-lookup"><span data-stu-id="6060b-155">If server rejects HoloLens client certificate, check whether the required client certificate has been provisioned on the device.</span></span>
   1. <span data-ttu-id="6060b-156">Если HoloLens отклонил сертификат сервера, убедитесь, что сертификат корневого ЦС сервера был установлен на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6060b-156">If HoloLens rejects server certificate, check if the server root CA certificate has been provisioned on HoloLens.</span></span>
1. <span data-ttu-id="6060b-157">Если профиль предприятия предоставлен с помощью пакета подготовки Wi-Fi, рассмотрите возможность установки пакета подготовки на компьютер с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6060b-157">If the enterprise profile is provisioned through Wi-Fi provisioning package, consider applying the provisioning package on a Windows 10 PC.</span></span> <span data-ttu-id="6060b-158">Если на компьютере с Windows 10 он также не работает, следуйте [инструкциям по устранению неполадок с проверкой подлинности клиента Windows 802.1 x](https://docs.microsoft.com/windows/client-management/advanced-troubleshooting-802-authentication).</span><span class="sxs-lookup"><span data-stu-id="6060b-158">If it also fails on Windows 10 PC, follow the [Windows client 802.1X authentication troubleshooting guide](https://docs.microsoft.com/windows/client-management/advanced-troubleshooting-802-authentication).</span></span>
1. <span data-ttu-id="6060b-159">Отправьте нам отзыв через [Центр отзывов](https://docs.microsoft.com/hololens/hololens-feedback).</span><span class="sxs-lookup"><span data-stu-id="6060b-159">Send us feedback through [Feedback Hub](https://docs.microsoft.com/hololens/hololens-feedback).</span></span>

### <a name="additional-resources"></a><span data-ttu-id="6060b-160">Дополнительные ресурсы:</span><span class="sxs-lookup"><span data-stu-id="6060b-160">Additional resources:</span></span>
- [<span data-ttu-id="6060b-161">Экспорт параметров Wi-Fi с устройства с Windows</span><span class="sxs-lookup"><span data-stu-id="6060b-161">Export Wi-Fi settings from a Windows device</span></span>](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-import-windows-8-1#export-wi-fi-settings-from-a-windows-device)

## <a name="vpn"></a><span data-ttu-id="6060b-162">VPN</span><span class="sxs-lookup"><span data-stu-id="6060b-162">VPN</span></span>
<span data-ttu-id="6060b-163">Подключение к сети VPN позволяет обеспечить более безопасное подключение и доступ к сети организации и Интернету.</span><span class="sxs-lookup"><span data-stu-id="6060b-163">A VPN connection can help provide a more secure connection and access to your company's network and the Internet.</span></span> <span data-ttu-id="6060b-164">HoloLens 2 поддерживает встроенный подключаемый модуль VPN-клиента и универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="6060b-164">HoloLens 2 supports built-in VPN client and Universal Windows Platform (UWP) VPN plug-in.</span></span> 

<span data-ttu-id="6060b-165">Поддерживаемые встроенные протоколы VPN:</span><span class="sxs-lookup"><span data-stu-id="6060b-165">Supported Built-in VPN protocols:</span></span>
- <span data-ttu-id="6060b-166">IKEv2</span><span class="sxs-lookup"><span data-stu-id="6060b-166">IKEv2</span></span>
- <span data-ttu-id="6060b-167">L2TP</span><span class="sxs-lookup"><span data-stu-id="6060b-167">L2TP</span></span>
- <span data-ttu-id="6060b-168">PPTP</span><span class="sxs-lookup"><span data-stu-id="6060b-168">PPTP</span></span>

<span data-ttu-id="6060b-169">Если для проверки подлинности для встроенного VPN-клиента используется сертификат, то необходимый сертификат клиента следует добавить в хранилище сертификатов пользователя.</span><span class="sxs-lookup"><span data-stu-id="6060b-169">If certificate is used for authentication for built-in VPN client, the required client certificate needs to be added to user certificate store.</span></span> <span data-ttu-id="6060b-170">Если подключаемый модуль VPN стороннего производителя поддерживает HoloLens 2, то перейдите в Хранилище, чтобы найти приложение VPN, и проверьте, содержится ли HoloLens в списке поддерживаемых устройств, а на странице требований к системе убедитесь, что приложение поддерживает архитектуру ARM или ARM64.</span><span class="sxs-lookup"><span data-stu-id="6060b-170">To find if a 3rd party VPN plug-in supports HoloLens 2, go to Store to locate VPN app and check if HoloLens is listed as a supported device and in the System Requirement page the app supports ARM or ARM64 architecture.</span></span> <span data-ttu-id="6060b-171">HoloLens поддерживает только приложения универсальной платформы Windows для сторонних сетей VPN.</span><span class="sxs-lookup"><span data-stu-id="6060b-171">HoloLens only supports Universal Windows Platform applications for 3rd party VPN.</span></span>

 <span data-ttu-id="6060b-172">VPN можно управлять с помощью MDM в пункте [Параметры/Разрешить VPN](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn) и настраивать с помощью [политики Vpnv2-csp](https://docs.microsoft.com/windows/client-management/mdm/vpnv2-csp).</span><span class="sxs-lookup"><span data-stu-id="6060b-172">VPN can be managed by MDM via [Settings/AllowVPN](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn), and set via  [Vpnv2-csp policy](https://docs.microsoft.com/windows/client-management/mdm/vpnv2-csp).</span></span>

<span data-ttu-id="6060b-173">Дополнительные сведения о [процедуре настройки VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) можно получить из [этих руководств](https://docs.microsoft.com/windows/security/identity-protection/vpn/vpn-guide).</span><span class="sxs-lookup"><span data-stu-id="6060b-173">Learn more about [how to configure VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) with [these guides](https://docs.microsoft.com/windows/security/identity-protection/vpn/vpn-guide).</span></span>  

### <a name="vpn-via-ui"></a><span data-ttu-id="6060b-174">Настройка VPN с помощью пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="6060b-174">VPN via UI</span></span>

<span data-ttu-id="6060b-175">По умолчанию сеть VPN отключена, но ее можно включить вручную, открыв приложение **Параметры** и перейдя к пункту **Сеть и Интернет > VPN**.</span><span class="sxs-lookup"><span data-stu-id="6060b-175">VPN is not enabled by default but can be enabled manually by opening **Settings** app and navigating to  **Network & Internet -> VPN**.</span></span>
1. <span data-ttu-id="6060b-176">Выберите поставщика услуг VPN.</span><span class="sxs-lookup"><span data-stu-id="6060b-176">Select a VPN provider.</span></span>
1. <span data-ttu-id="6060b-177">Придумайте название подключения.</span><span class="sxs-lookup"><span data-stu-id="6060b-177">Create a connection name.</span></span> 
1. <span data-ttu-id="6060b-178">Введите имя или адрес сервера.</span><span class="sxs-lookup"><span data-stu-id="6060b-178">Enter your server name or address.</span></span>
1. <span data-ttu-id="6060b-179">Выберите тип VPN.</span><span class="sxs-lookup"><span data-stu-id="6060b-179">Select the VPN type.</span></span>
1. <span data-ttu-id="6060b-180">Выберите тип сведений для входа.</span><span class="sxs-lookup"><span data-stu-id="6060b-180">Select type of sign-in info.</span></span> 
1. <span data-ttu-id="6060b-181">При необходимости добавьте имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="6060b-181">Optionally add user name and password.</span></span>
1. <span data-ttu-id="6060b-182">Примените параметры VPN.</span><span class="sxs-lookup"><span data-stu-id="6060b-182">Apply the VPN settings.</span></span> 

![Параметры VPN для HoloLens](./images/vpn-settings-ui.jpg)

### <a name="vpn-set-via-provisioning-package"></a><span data-ttu-id="6060b-184">Настройка VPN с помощью пакета подготовки</span><span class="sxs-lookup"><span data-stu-id="6060b-184">VPN set via Provisioning Package</span></span>

> [!TIP] 
> <span data-ttu-id="6060b-185">В Windows Holographic версии 20H2 мы устранили проблему с конфигурацией прокси-сервера для подключения VPN.</span><span class="sxs-lookup"><span data-stu-id="6060b-185">In our Windows Holographic, version 20H2 we fixed a proxy configuration issue for VPN connection.</span></span> <span data-ttu-id="6060b-186">Если вы планируете использовать этот поток, попробуйте обновить устройства до этой сборки.</span><span class="sxs-lookup"><span data-stu-id="6060b-186">Please consider upgrading devices to this build if you intend to use this flow.</span></span>

1. <span data-ttu-id="6060b-187">Запустите конструктор конфигураций Windows.</span><span class="sxs-lookup"><span data-stu-id="6060b-187">Launch Windows Configuration Designer.</span></span>
1. <span data-ttu-id="6060b-188">Щелкните **Подготовить устройства HoloLens**, затем выберите целевое устройство и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6060b-188">Click **Provision HoloLens devices**, then select target device and **Next**.</span></span>
1. <span data-ttu-id="6060b-189">Введите имя пакета и путь к нему.</span><span class="sxs-lookup"><span data-stu-id="6060b-189">Enter package name and path.</span></span>
1. <span data-ttu-id="6060b-190">Нажмите кнопку **Переключиться в расширенный редактор**.</span><span class="sxs-lookup"><span data-stu-id="6060b-190">Click **Switch to advanced editor**.</span></span>
1. <span data-ttu-id="6060b-191">Откройте **Параметры среды выполнения** -> **ConnectivityProfiles** -> **VPN-** -> **VPNSettings**.</span><span class="sxs-lookup"><span data-stu-id="6060b-191">Open **Runtime settings** -> **ConnectivityProfiles** -> **VPN** -> **VPNSettings**.</span></span>
1. <span data-ttu-id="6060b-192">Настройка параметра VPNProfileName</span><span class="sxs-lookup"><span data-stu-id="6060b-192">Configure VPNProfileName</span></span>
1. <span data-ttu-id="6060b-193">Выберите ProfileType: **Встроенный** или **Стороннего производителя**.</span><span class="sxs-lookup"><span data-stu-id="6060b-193">Select ProfileType: **Native** or **Third Party**.</span></span>
    1. <span data-ttu-id="6060b-194">Для встроенного профиля выберите **NativeProtocolType**, затем настройте сервер, политику маршрутизации, тип проверки подлинности и другие параметры.</span><span class="sxs-lookup"><span data-stu-id="6060b-194">For Native profile, select **NativeProtocolType**, then configure server, routing policy, authentication type and other settings.</span></span>
    1. <span data-ttu-id="6060b-195">Для профиля стороннего производителя настройте URL-адрес сервера, имя семейства пакетов подключаемого модуля приложения VPN (только три имени предварительно заданы) и настраиваемые конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6060b-195">For "Third Party" profile, configure server URL, VPN plug-in App package family name (only 3 predefined) and custom configurations.</span></span>
1. <span data-ttu-id="6060b-196">Экспортируйте пакет.</span><span class="sxs-lookup"><span data-stu-id="6060b-196">Export your package.</span></span>
1. <span data-ttu-id="6060b-197">Подключите HoloLens и скопируйте файл .ppkg на устройство.</span><span class="sxs-lookup"><span data-stu-id="6060b-197">Connect your HoloLens and copy the .ppkg file to the device.</span></span> 
1. <span data-ttu-id="6060b-198">Примените файл .ppkg VPN на HoloLens, открыв меню "Пуск" и выбрав **Параметры** -> **Учетная запись** -> **Рабочий или учебный доступ** -> **Добавление или удаление пакета подготовки** -> Выбор пакета VPN.</span><span class="sxs-lookup"><span data-stu-id="6060b-198">On HoloLens, apply the VPN .ppkg by opening the Start menu and selecting **Settings** -> **Account** -> **Access work or school** -> **Add or remove provisioning package** -> Select your VPN package.</span></span>


### <a name="setting-up-vpn-via-intune"></a><span data-ttu-id="6060b-199">Настройка VPN с помощью Intune</span><span class="sxs-lookup"><span data-stu-id="6060b-199">Setting up VPN via Intune</span></span>
<span data-ttu-id="6060b-200">Чтобы приступить к работе, просто следуйте документации Intune.</span><span class="sxs-lookup"><span data-stu-id="6060b-200">Just follow the Intune documents to get started.</span></span> <span data-ttu-id="6060b-201">При выполнении этих действий следует учитывать встроенные протоколы VPN, поддерживаемые устройствами HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6060b-201">When following these steps please keep in mind the built-in VPN protocols that HoloLens devices support.</span></span> 

<span data-ttu-id="6060b-202">[Создание профилей VPN для подключения к серверам VPN в Intune](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-configure).</span><span class="sxs-lookup"><span data-stu-id="6060b-202">[Create VPN profiles to connect to VPN servers in Intune](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-configure).</span></span>

<span data-ttu-id="6060b-203">[Параметры устройства Windows 10 и Windows Holographic для добавления подключений VPN с помощью Intune](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-windows-10).</span><span class="sxs-lookup"><span data-stu-id="6060b-203">[Windows 10 and Windows Holographic device settings to add VPN connections using Intune](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-windows-10).</span></span>

<span data-ttu-id="6060b-204">После завершения настройки не забудьте [назначить профиль](https://docs.microsoft.com/mem/intune/configuration/device-profile-assign).</span><span class="sxs-lookup"><span data-stu-id="6060b-204">When done please remember to [assign the profile](https://docs.microsoft.com/mem/intune/configuration/device-profile-assign).</span></span>

### <a name="vpn-via-3rd-party-mdm-solutions"></a><span data-ttu-id="6060b-205">Настройка VPN с помощью решений MDM сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="6060b-205">VPN via 3rd party MDM solutions</span></span>
<span data-ttu-id="6060b-206">Пример подключения VPN стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="6060b-206">3rd party VPN connection example:</span></span>
```xml
<!-- Configure VPN Server Name or Address (PhoneNumber=) [Comma Separated]-->
      <Add>
        <CmdID>10001</CmdID>
        <Item>
          <Target>
            <LocURI>./Vendor/MSFT/VPNv2/VPNProfileName/PluginProfile/ServerUrlList</LocURI>
          </Target>
          <Data>selfhost.corp.contoso.com</Data>
        </Item>
      </Add>

      <!-- Configure VPN Plugin AppX Package ID (ThirdPartyProfileInfo=) -->
      <Add>
        <CmdID>10002</CmdID>
        <Item>
          <Target>
            <LocURI>./Vendor/MSFT/VPNv2/VPNProfileName/PluginProfile/PluginPackageFamilyName</LocURI>
          </Target>
          <Data>TestVpnPluginApp-SL_8wekyb3d8bbwe</Data>
        </Item>
      </Add>

      <!-- Configure Microsoft's Custom XML (ThirdPartyProfileInfo=) -->
      <Add>
        <CmdID>10003</CmdID>
        <Item>
          <Target>
            <LocURI>./Vendor/MSFT/VPNv2/VPNProfileName/PluginProfile/CustomConfiguration</LocURI>
          </Target>          <Data><pluginschema><ipAddress>auto</ipAddress><port>443</port><networksettings><routes><includev4><route><address>172.10.10.0</address><prefix>24</prefix></route></includev4></routes><namespaces><namespace><space>.vpnbackend.com</space><dnsservers><server>172.10.10.11</server></dnsservers></namespace></namespaces></networksettings></pluginschema></Data>
        </Item>
      </Add>
```

<span data-ttu-id="6060b-207">Пример встроенного VPN с использованием протокола IKEv2.</span><span class="sxs-lookup"><span data-stu-id="6060b-207">Native IKEv2 VPN example:</span></span>
```xml
      <Add>
        <CmdID>10001</CmdID>
        <Item>
          <Target>
            <LocURI>./Vendor/MSFT/VPNv2/VPNProfileName/NativeProfile/Servers</LocURI>
          </Target>
          <Data>Selfhost.corp.contoso.com</Data>
        </Item>
      </Add>

      <Add>
        <CmdID>10002</CmdID>
        <Item>
          <Target>
            <LocURI>./Vendor/MSFT/VPNv2/VPNProfileName/NativeProfile/RoutingPolicyType</LocURI>
          </Target>
          <Data>ForceTunnel</Data>
        </Item>
      </Add>

      <!-- Configure VPN Protocol Type (L2tp, Pptp, Ikev2) -->
      <Add>
        <CmdID>10003</CmdID>
        <Item>
          <Target>
            <LocURI>./Vendor/MSFT/VPNv2/VPNProfileName/NativeProfile/NativeProtocolType</LocURI>
          </Target>
          <Data>Ikev2</Data>
        </Item>
      </Add>

      <!-- Configure VPN User Method (Mschapv2, Eap) -->
      <Add>
        <CmdID>10004</CmdID>
        <Item>
          <Target>
            <LocURI>./Vendor/MSFT/VPNv2/VPNProfileName/NativeProfile/Authentication/UserMethod</LocURI>
          </Target>
          <Data>Eap</Data>
        </Item>
      </Add>

      <Add>
        <CmdID>10004</CmdID>
        <Item>
          <Target>
            <LocURI>./Vendor/MSFT/VPNv2/VPNProfileName/NativeProfile/Authentication/Eap/Configuration</LocURI>
          </Target>
          <Data>EAP_configuration_xml_content</Data>
        </Item>
      </Add>
```
## <a name="disabling-wi-fi-on-hololens-1st-gen"></a><span data-ttu-id="6060b-208">Отключение Wi-Fi на HoloLens (1 поколение)</span><span class="sxs-lookup"><span data-stu-id="6060b-208">Disabling Wi-Fi on HoloLens (1st gen)</span></span>

### <a name="using-the-settings-app-on-hololens"></a><span data-ttu-id="6060b-209">С помощью приложения "Параметры" на HoloLens</span><span class="sxs-lookup"><span data-stu-id="6060b-209">Using the Settings app on HoloLens</span></span>

1. <span data-ttu-id="6060b-210">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="6060b-210">Open the **Start** menu.</span></span>
1. <span data-ttu-id="6060b-211">Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="6060b-211">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="6060b-212">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="6060b-212">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="6060b-213">Выберите пункт **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="6060b-213">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="6060b-214">Выберите переключатель "Wi-Fi", чтобы переместить его в положение **Выкл.**.</span><span class="sxs-lookup"><span data-stu-id="6060b-214">Select the Wi-Fi slider switch to move it to the **Off** position.</span></span> <span data-ttu-id="6060b-215">Это приведет к отключению радиочастотных компонентов радиомодуля Wi-Fi и отключению всех функций Wi-Fi на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6060b-215">This will turn off the RF components of the Wi-Fi radio and disable all Wi-Fi functionality on HoloLens.</span></span>

    > [!WARNING]
    > <span data-ttu-id="6060b-216">Если радио Wi-Fi отключено, HoloLens не сможет автоматически загружать ваши [пространства](hololens-spaces.md).</span><span class="sxs-lookup"><span data-stu-id="6060b-216">When the Wi-Fi radio is disabled, HoloLens will not be able to automatically load your [spaces](hololens-spaces.md).</span></span>

1. <span data-ttu-id="6060b-217">Переведите переключатель в положение **Вкл.**, чтобы включить радио Wi-Fi и восстановить функции Wi-Fi на Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6060b-217">Move the slider switch to the **On** position to turn on the Wi-Fi radio and restore Wi-Fi functionality on Microsoft HoloLens.</span></span> <span data-ttu-id="6060b-218">Выбранное состояние радио Wi-Fi (**Включено** или **Выключено**) будет сохранено при перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="6060b-218">The selected Wi-Fi radio state (**On** or **Off**) will persist across reboots.</span></span>

## <a name="identifying-the-ip-address-of-your-hololens-on-the-wi-fi-network"></a><span data-ttu-id="6060b-219">Определение IP-адреса HoloLens в сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="6060b-219">Identifying the IP Address of your HoloLens on the Wi-Fi network</span></span>

### <a name="by-using-the-settings-app"></a><span data-ttu-id="6060b-220">С помощью приложения "Параметры"</span><span class="sxs-lookup"><span data-stu-id="6060b-220">By using the Settings app</span></span>

1. <span data-ttu-id="6060b-221">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="6060b-221">Open the **Start** menu.</span></span>
1. <span data-ttu-id="6060b-222">Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="6060b-222">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="6060b-223">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="6060b-223">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="6060b-224">Выберите пункт **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="6060b-224">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="6060b-225">Прокрутите список доступных сетей Wi-Fi вниз до пункта **Свойства оборудования**.</span><span class="sxs-lookup"><span data-stu-id="6060b-225">Scroll down to beneath the list of available Wi-Fi networks and select **Hardware properties**.</span></span>

    ![Свойства оборудования в параметрах Wi-Fi](./images/wifi-hololens-hwdetails.jpg)

   <span data-ttu-id="6060b-227">IP-адрес будет указан рядом с пунктом **IPv4-адрес**.</span><span class="sxs-lookup"><span data-stu-id="6060b-227">The IP address appears next to **IPv4 address**.</span></span>

### <a name="by-using-voice-commands"></a><span data-ttu-id="6060b-228">С использованием голосовых команд</span><span class="sxs-lookup"><span data-stu-id="6060b-228">By using voice commands</span></span>

<span data-ttu-id="6060b-229">В зависимости от сборки вашего устройства на некоторых устройствах можно использовать встроенные голосовые команды или Кортану для отображения вашего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="6060b-229">Depending on your devices build you can either use built in voice commands or Cortana to display your IP address.</span></span> <span data-ttu-id="6060b-230">В сборках версий после [19041,1103](hololens-release-notes.md#windows-holographic-version-2004) произнесите "What's my IP address?" (Какой у меня IP адрес?)</span><span class="sxs-lookup"><span data-stu-id="6060b-230">On builds after [19041.1103](hololens-release-notes.md#windows-holographic-version-2004) speak "What's my IP address?"</span></span> <span data-ttu-id="6060b-231">и он будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="6060b-231">and it will be displayed.</span></span> <span data-ttu-id="6060b-232">Для более ранних сборок или HoloLens (1-ого поколения) произнесите "Hey Cortana, What's my IP address?" (Привет, Кортана! Какой у меня IP-адрес?).</span><span class="sxs-lookup"><span data-stu-id="6060b-232">For earlier builds or HoloLens (1st gen) say "Hey Cortana, What's my IP address?"</span></span> <span data-ttu-id="6060b-233">Кортана отобразит и прочитает ваш IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="6060b-233">and Cortana will display and read out your IP address.</span></span>

### <a name="by-using-windows-device-portal"></a><span data-ttu-id="6060b-234">С помощью портала устройств Windows</span><span class="sxs-lookup"><span data-stu-id="6060b-234">By using Windows Device Portal</span></span>

1. <span data-ttu-id="6060b-235">Откройте [портал устройств](/windows/mixed-reality/using-the-windows-device-portal.md#networking) в веб-браузере на компьютере.</span><span class="sxs-lookup"><span data-stu-id="6060b-235">In a web browser on your PC, open the [device portal](/windows/mixed-reality/using-the-windows-device-portal.md#networking).</span></span>
1. <span data-ttu-id="6060b-236">Перейдите в раздел **Сети**.</span><span class="sxs-lookup"><span data-stu-id="6060b-236">Navigate to the **Networking** section.</span></span>  
   <span data-ttu-id="6060b-237">В этом разделе отображается ваш IP-адрес и другая информация о сети.</span><span class="sxs-lookup"><span data-stu-id="6060b-237">This section displays your IP address and other network information.</span></span> <span data-ttu-id="6060b-238">С помощью этого метода можно скопировать и вставить IP-адрес на компьютер для разработки.</span><span class="sxs-lookup"><span data-stu-id="6060b-238">By using this method, you can copy and paste of the IP address on your development PC.</span></span>
