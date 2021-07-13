---
title: Подключение HoloLens к сети
description: Узнайте, как выполнить настройку и подключиться к Интернету с помощью HoloLens, а также как определить IP-адрес устройства.
ms.assetid: 0895606e-96c0-491e-8b1c-52e56b00365d
author: mattzmsft
ms.author: mazeller
keywords: HoloLens, Wi-Fi, беспроводной, интернет, IP, IP-адрес
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: ''
manager: jarrettr
ms.openlocfilehash: 8564fb0483226a16722ada345de325577cda77d6
ms.sourcegitcommit: d5b2080868d6b74169a1bab2c7bad37dfa5a8b5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923607"
---
# <a name="connect-hololens-to-a-network"></a><span data-ttu-id="1da48-104">Подключение HoloLens к сети</span><span class="sxs-lookup"><span data-stu-id="1da48-104">Connect HoloLens to a network</span></span>

<span data-ttu-id="1da48-105">Для выполнения большинства задач на устройстве HoloLens оно должно быть подключено к сети.</span><span class="sxs-lookup"><span data-stu-id="1da48-105">To do most things on your HoloLens, you have to be connected to a network.</span></span> <span data-ttu-id="1da48-106">Устройство HoloLens оборудовано радиомодулем Wi-Fi 2x2 с поддержкой стандарта 802.11ac. Его подключение к сети осуществляется так же, как подключение к сети Wi-Fi классического или мобильного устройства с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1da48-106">HoloLens contains a 802.11ac-capable, 2x2 Wi-Fi radio and connecting it to a network is similar to connecting a Windows 10 Desktop or Mobile device to a Wi-Fi network.</span></span> <span data-ttu-id="1da48-107">Это руководство поможет вам:</span><span class="sxs-lookup"><span data-stu-id="1da48-107">This guide will help you:</span></span>

- <span data-ttu-id="1da48-108">подключиться к сети с помощью Wi-Fi, а также к (только для HoloLens 2) Wi-Fi Direct или Ethernet через USB-C;</span><span class="sxs-lookup"><span data-stu-id="1da48-108">Connect to a network using Wi-Fi, or for HoloLens 2 only, Wi-Fi Direct or Ethernet over USB-C</span></span>
- <span data-ttu-id="1da48-109">отключить и повторно включить Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="1da48-109">Disable and re-enable Wi-Fi</span></span>

<span data-ttu-id="1da48-110">См. дополнительные сведения об [использовании HoloLens в автономном режиме](hololens-offline.md).</span><span class="sxs-lookup"><span data-stu-id="1da48-110">Read more about [using HoloLens offline](hololens-offline.md).</span></span>

## <a name="connecting-for-the-first-time"></a><span data-ttu-id="1da48-111">Первое подключение</span><span class="sxs-lookup"><span data-stu-id="1da48-111">Connecting for the first time</span></span>

<span data-ttu-id="1da48-112">При первом использовании HoloLens вам будет предложено пройти процедуру подключения к сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="1da48-112">The first time you use your HoloLens, you'll be guided through connecting to a Wi-Fi network.</span></span> <span data-ttu-id="1da48-113">При наличии проблем с подключением к сети Wi-Fi во время настройки проверьте, открыта ли ваша сеть, защищена ли она паролем и имеет ли она портал авторизации.</span><span class="sxs-lookup"><span data-stu-id="1da48-113">If you have trouble connecting to Wi-Fi during setup, make sure that your network is either an open, password-protected network or a captive portal network.</span></span> <span data-ttu-id="1da48-114">Кроме того, убедитесь, что для подключения к сети не требуется использование сертификата.</span><span class="sxs-lookup"><span data-stu-id="1da48-114">Also, confirm that the network doesn't require you to use a certificate to connect.</span></span> <span data-ttu-id="1da48-115">После завершения настройки можно будет подключаться к другим типам сетей Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="1da48-115">After setup, you can connect to other types of Wi-Fi networks.</span></span>

<span data-ttu-id="1da48-116">На устройствах HoloLens 2 пользователь также может [использовать адаптер USB-C для Ethernet](hololens-connect-devices.md#hololens-2-connect-usb-c-devices) для подключения напрямую к Wi-Fi и настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="1da48-116">On HoloLens 2 devices, a user may also [use a USB-C to Ethernet adapter](hololens-connect-devices.md#hololens-2-connect-usb-c-devices) to connect directly to Wi-Fi to help assist in setting up the device.</span></span> <span data-ttu-id="1da48-117">Завершив настройку устройства, пользователь может продолжать использовать адаптер или отключить его от устройства и [подключиться к Wi-Fi после настройки](hololens-network.md#connecting-to-wi-fi-after-setup).</span><span class="sxs-lookup"><span data-stu-id="1da48-117">Once the device has been set up a user may continue to use the adapter or they may disconnect the device from the adapter and [connect to wi-fi after set up](hololens-network.md#connecting-to-wi-fi-after-setup).</span></span> 

## <a name="connecting-to-wi-fi-after-setup"></a><span data-ttu-id="1da48-118">Подключение к сети Wi-Fi после настройки</span><span class="sxs-lookup"><span data-stu-id="1da48-118">Connecting to Wi-Fi after setup</span></span>

1. <span data-ttu-id="1da48-119">Выполните **жест "Пуск"** и выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="1da48-119">Preform the **Start gesture** and select **Settings**.</span></span> <span data-ttu-id="1da48-120">Приложение "Параметры" будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="1da48-120">The Settings app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="1da48-121">Выберите **Сеть и Интернет** > **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="1da48-121">Select **Network & Internet** > **Wi-Fi**.</span></span> <span data-ttu-id="1da48-122">Убедитесь, что функция Wi-Fi включена.</span><span class="sxs-lookup"><span data-stu-id="1da48-122">Make sure Wi-Fi is turned on.</span></span> <span data-ttu-id="1da48-123">Если вы не видите сеть, прокрутите список вниз.</span><span class="sxs-lookup"><span data-stu-id="1da48-123">If you don't see your network, scroll down the list.</span></span>
1. <span data-ttu-id="1da48-124">Выберите сеть и щелкните **Подключить**.</span><span class="sxs-lookup"><span data-stu-id="1da48-124">Select a network, then select **Connect**.</span></span>
1. <span data-ttu-id="1da48-125">В ответ на соответствующий запрос введите пароль от сети и щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1da48-125">If you are prompted for a network password type it and then select **Next**.</span></span>

![Параметры Wi-Fi для HoloLens](./images/hololens-2-wifi-settings.jpg)

<span data-ttu-id="1da48-127">Чтобы подтвердить подключение к сети Wi-Fi, проверьте состояние Wi-Fi в меню **Пуск**:</span><span class="sxs-lookup"><span data-stu-id="1da48-127">To confirm you are connected to a Wi-Fi network, check the Wi-Fi status in the **Start** menu:</span></span>

1. <span data-ttu-id="1da48-128">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="1da48-128">Open the **Start** menu.</span></span>
1. <span data-ttu-id="1da48-129">Проверьте состояние сети Wi-Fi в верхнем левом углу меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="1da48-129">Look at the top left of the **Start** menu for Wi-Fi status.</span></span> <span data-ttu-id="1da48-130">Будет отображено состояние Wi-Fi и SSID подключенной сети.</span><span class="sxs-lookup"><span data-stu-id="1da48-130">The state of Wi-Fi and the SSID of the connected network will be shown.</span></span>

> [!TIP]
> <span data-ttu-id="1da48-131">Если сеть Wi-Fi недоступна, вы также можете [подключиться к сотовым сетям или сетям 5G](hololens-cellular.md).</span><span class="sxs-lookup"><span data-stu-id="1da48-131">If Wi-Fi is not available, you can also [connect to Cellular and 5G networks](hololens-cellular.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1da48-132">Пользователи не могут точно настраивать поведение HoloLens 2 при поиске сетей Wi-Fi — **единственный способ обновить список Wi-Fi заключается в отключении и включении Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="1da48-132">By design, users cannot fine tune the Wi-Fi roaming behavior of the HoloLens 2 - **the only way to refresh the Wi-Fi list is to toggle the Wi-Fi Off and On**.</span></span> <span data-ttu-id="1da48-133">Это предотвращает множество проблем, например с зависанием устройства в точке доступа после выхода из диапазона.</span><span class="sxs-lookup"><span data-stu-id="1da48-133">This prevents many issues, like where a device can remain "stuck" to an AP once it is out of range.</span></span>

## <a name="connect-hololens-to-enterprise-wi-fi-network"></a><span data-ttu-id="1da48-134">Подключение HoloLens к корпоративной сети Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="1da48-134">Connect HoloLens to Enterprise Wi-Fi Network</span></span>

<span data-ttu-id="1da48-135">В корпоративных профилях Wi-Fi для аутентификации подключений по Wi-Fi используется протокол расширенной аутентификации (EAP).</span><span class="sxs-lookup"><span data-stu-id="1da48-135">Enterprise Wi-Fi profiles use Extensible Authentication Protocol (EAP) to authenticate Wi-Fi connections.</span></span> <span data-ttu-id="1da48-136">Корпоративный профиль HoloLens для Wi-Fi можно настроить с помощью MDM или пакета подготовки, созданного с помощью [конструктора конфигураций Windows](https://docs.microsoft.com/windows/configuration/provisioning-packages/provisioning-packages).</span><span class="sxs-lookup"><span data-stu-id="1da48-136">HoloLens Enterprise Wi-Fi profile can be configured through MDM or provisioning package created by [Windows Configuration Designer](https://docs.microsoft.com/windows/configuration/provisioning-packages/provisioning-packages).</span></span>

<span data-ttu-id="1da48-137">Инструкции по настройке устройства, управляемого с помощью службы Microsoft Intune, см. [здесь](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-windows#enterprise-profile).</span><span class="sxs-lookup"><span data-stu-id="1da48-137">For Microsoft Intune managed device, refer to [Intune](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-windows#enterprise-profile) for configuration instructions.</span></span>

<span data-ttu-id="1da48-138">Чтобы создать пакет подготовки Wi-Fi в конструкторе конфигураций Windows, требуется файл предварительно настроенного профиля Wi-Fi в формате XML.</span><span class="sxs-lookup"><span data-stu-id="1da48-138">To create a Wi-Fi provisioning package in WCD, a pre-configured Wi-Fi profile .xml file is required.</span></span> <span data-ttu-id="1da48-139">Ниже приведен пример профиля Wi-Fi для WPA2-Enterprise с аутентификацией EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="1da48-139">Here is a sample Wi-Fi profile for WPA2-Enterprise with EAP-TLS authentication:</span></span>

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


<span data-ttu-id="1da48-140">Сертификат корневого ЦС сервера и сертификат клиента, возможно, нужно будет подготовить на устройстве, в зависимости от типа EAP.</span><span class="sxs-lookup"><span data-stu-id="1da48-140">Server root CA certificate and client certificate may need to be provisioned on the device depending on the EAP type.</span></span>

<span data-ttu-id="1da48-141">Дополнительные ресурсы:</span><span class="sxs-lookup"><span data-stu-id="1da48-141">Additional resources:</span></span>

- <span data-ttu-id="1da48-142">Схема WLANv1Profile: [[MS-GPWL]: Схема LAN Profile v1 | Документация Майкрософт](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/34054c93-cfcd-44df-89d8-5f2ba7532b67)</span><span class="sxs-lookup"><span data-stu-id="1da48-142">WLANv1Profile Schema: [[MS-GPWL]: Wireless LAN Profile v1 Schema | Microsoft Docs](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/34054c93-cfcd-44df-89d8-5f2ba7532b67)</span></span>
- <span data-ttu-id="1da48-143">Схема EAP-TLS: [[MS-GPWL]: Схема Microsoft EAP TLS | Документация Майкрософт](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/9590925c-cba2-4ac5-b9a1-1e5292bb72cb)</span><span class="sxs-lookup"><span data-stu-id="1da48-143">EAP-TLS Schema: [[MS-GPWL]: Microsoft EAP TLS Schema | Microsoft Docs](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/9590925c-cba2-4ac5-b9a1-1e5292bb72cb)</span></span>

<span data-ttu-id="1da48-144">Если при подключении к Wi-Fi возникают проблемы, см. рекомендации по [устранению неполадок](hololens2-enterprise-troubleshooting.md#).</span><span class="sxs-lookup"><span data-stu-id="1da48-144">Check our [Troubleshooting](hololens2-enterprise-troubleshooting.md#) page if you are having problems connecting to your Wi-Fi.</span></span>

## <a name="configure-network-proxy"></a><span data-ttu-id="1da48-145">Настройка сетевого прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="1da48-145">Configure Network Proxy</span></span>

<span data-ttu-id="1da48-146">В этом разделе рассматривается сетевой прокси-сервер для ОС HoloLens и приложений UWP с использованием стека HTTP Windows.</span><span class="sxs-lookup"><span data-stu-id="1da48-146">This section covers network proxy for HoloLens OS and Universal Windows Platform (UWP) Apps using Windows HTTP stack.</span></span> <span data-ttu-id="1da48-147">Приложения, использующие стек HTTP без Windows, могут иметь собственную конфигурацию прокси-сервера и средства работы с ним.</span><span class="sxs-lookup"><span data-stu-id="1da48-147">Applications using non-Windows HTTP stack may have their own proxy configuration and handling.</span></span> 

### <a name="proxy-configurations"></a><span data-ttu-id="1da48-148">Конфигурации прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="1da48-148">Proxy Configurations</span></span> 

- <span data-ttu-id="1da48-149">Скрипт автоматической конфигурации прокси-сервера (PAC): [файл PAC](https://developer.mozilla.org/en-US/docs/Web/HTTP/Proxy_servers_and_tunneling/Proxy_Auto-Configuration_PAC_file) (открывает сайт, не принадлежащий Майкрософт) содержит функцию JavaScript FindProxyForURL(url, host).</span><span class="sxs-lookup"><span data-stu-id="1da48-149">Proxy Auto-Config (PAC) script: a [PAC file](https://developer.mozilla.org/en-US/docs/Web/HTTP/Proxy_servers_and_tunneling/Proxy_Auto-Configuration_PAC_file) (opens a non-Microsoft site) contains a JavaScript function FindProxyForURL(url, host).</span></span> 
- <span data-ttu-id="1da48-150">Статический прокси-сервер: в формате сервер:порт.</span><span class="sxs-lookup"><span data-stu-id="1da48-150">Static Proxy: in the form of Server:Port.</span></span>  
- <span data-ttu-id="1da48-151">Протокол автоматического обнаружения прокси-сервера (WPAD): предоставляет URL-адрес для файла конфигурации прокси-сервера по DHCP или DNS.</span><span class="sxs-lookup"><span data-stu-id="1da48-151">Web Proxy Auto-Discovery Protocol (WPAD): provide URL of proxy configuration file through DHCP or DNS.</span></span> 

### <a name="proxy-provisioning-methods"></a><span data-ttu-id="1da48-152">Методы подготовки прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="1da48-152">Proxy Provisioning Methods</span></span> 
<span data-ttu-id="1da48-153">Существует три способа для подготовки прокси-серверов:</span><span class="sxs-lookup"><span data-stu-id="1da48-153">There are three ways to provision proxies:</span></span>

 

1.  <span data-ttu-id="1da48-154">**Пользовательский интерфейс "Параметры":**</span><span class="sxs-lookup"><span data-stu-id="1da48-154">**Settings UI:**</span></span> 
    1. <span data-ttu-id="1da48-155">Прокси-сервер на отдельного пользователя (20H2 и более ранних версий):</span><span class="sxs-lookup"><span data-stu-id="1da48-155">Per-user proxy (20H2 or earlier):</span></span>
        1. <span data-ttu-id="1da48-156">Откройте меню "Пуск" и выберите Параметры.</span><span class="sxs-lookup"><span data-stu-id="1da48-156">Open the Start menu and select Settings.</span></span>
        2. <span data-ttu-id="1da48-157">Выберите "Сеть и Интернет", а затем "Прокси-сервер" в меню слева.</span><span class="sxs-lookup"><span data-stu-id="1da48-157">Select Network & Internet and then Proxy on the left menu.</span></span>
        3. <span data-ttu-id="1da48-158">Прокрутите вниз до пункта "Настройка прокси-сервера вручную" и установите переключатель "Использовать прокси-сервер" в положение "Вкл.".</span><span class="sxs-lookup"><span data-stu-id="1da48-158">Scroll down to Manual proxy setup and toggle Use a proxy server to On.</span></span>
        4. <span data-ttu-id="1da48-159">Введите IP-адрес прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="1da48-159">Enter the IP address of the proxy server.</span></span>
        5. <span data-ttu-id="1da48-160">Введите номер порта.</span><span class="sxs-lookup"><span data-stu-id="1da48-160">Enter the port number.</span></span>
        6. <span data-ttu-id="1da48-161">Нажмите кнопку «Сохранить».</span><span class="sxs-lookup"><span data-stu-id="1da48-161">Click Save.</span></span>
      1. <span data-ttu-id="1da48-162">Прокси-сервер WiFi (21H1 и более поздние версии):</span><span class="sxs-lookup"><span data-stu-id="1da48-162">WiFi proxy (21H1 or higher):</span></span>
          1. <span data-ttu-id="1da48-163">Откройте меню "Пуск" и перейдите на страницу свойств сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="1da48-163">Open the Start menu and go to your Wi-Fi Network’s Properties page.</span></span>
          1. <span data-ttu-id="1da48-164">Прокрутите вниз до раздела "Прокси-сервер".</span><span class="sxs-lookup"><span data-stu-id="1da48-164">Scroll down to Proxy</span></span>
          1. <span data-ttu-id="1da48-165">Выберите "Настройка вручную".</span><span class="sxs-lookup"><span data-stu-id="1da48-165">Change to Manual Setup</span></span>
          1. <span data-ttu-id="1da48-166">Введите IP-адрес прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="1da48-166">Enter the IP address of the proxy server.</span></span>
          1. <span data-ttu-id="1da48-167">Введите номер порта.</span><span class="sxs-lookup"><span data-stu-id="1da48-167">Enter the port number.</span></span>
          1. <span data-ttu-id="1da48-168">Нажмите кнопку "Применить".</span><span class="sxs-lookup"><span data-stu-id="1da48-168">Click Apply.</span></span>
        
 2. <span data-ttu-id="1da48-169">**MDM**</span><span class="sxs-lookup"><span data-stu-id="1da48-169">**MDM**</span></span> 
     1. <span data-ttu-id="1da48-170">Intune — выполните эти [шаги](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-windows#enterprise-profile), чтобы настроить прокси-сервер в Intune.</span><span class="sxs-lookup"><span data-stu-id="1da48-170">Intune - Use these [steps](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-windows#enterprise-profile) to configure proxy in Intune.</span></span> <span data-ttu-id="1da48-171">Вам нужно прокрутить в самый низ раздела.</span><span class="sxs-lookup"><span data-stu-id="1da48-171">You will need to scroll to the bottom of the section.</span></span>
     1. <span data-ttu-id="1da48-172">Другие решения MDM сторонних поставщиков — используйте [поставщик службы конфигурации Wi-Fi](https://docs.microsoft.com/windows/client-management/mdm/wifi-csp).</span><span class="sxs-lookup"><span data-stu-id="1da48-172">Other 3rd party MDM solutions - Use a [WiFi CSP](https://docs.microsoft.com/windows/client-management/mdm/wifi-csp).</span></span>

3. <span data-ttu-id="1da48-173">**PPKG**</span><span class="sxs-lookup"><span data-stu-id="1da48-173">**PPKG**</span></span> 
    1. <span data-ttu-id="1da48-174">Откройте конструктор конфигураций Windows.</span><span class="sxs-lookup"><span data-stu-id="1da48-174">Open Windows Configuration Designer</span></span>
    1. <span data-ttu-id="1da48-175">Щелкните "Расширенная подготовка", введите имя нового проекта и щелкните "Далее".</span><span class="sxs-lookup"><span data-stu-id="1da48-175">Click on Advanced Provisioning, enter the name for your new Project and click Next.</span></span>
    1. <span data-ttu-id="1da48-176">Выберите Windows Holographic (HoloLens 2) и щелкните "Далее".</span><span class="sxs-lookup"><span data-stu-id="1da48-176">Select Windows Holographic (HoloLens 2) and click Next.</span></span>
    1. <span data-ttu-id="1da48-177">Импортируйте PPKG (необязательно) и щелкните "Готово".</span><span class="sxs-lookup"><span data-stu-id="1da48-177">Import your PPKG (optional) and click Finish.</span></span>
    1. <span data-ttu-id="1da48-178">Выберите "Параметры среды выполнения" -> "Профили подключения" -> "Беспроводная сеть" -> "Прокси-сервер беспроводной сети".</span><span class="sxs-lookup"><span data-stu-id="1da48-178">Expand Runtime Settings -> Connectivity Profiles -> WLAN -> WLAN Proxy.</span></span>
    1. <span data-ttu-id="1da48-179">Введите идентификатор SSID сети Wi-Fi и щелкните "Добавить".</span><span class="sxs-lookup"><span data-stu-id="1da48-179">Enter the SSID of your Wi-Fi network and click Add.</span></span>
    1. <span data-ttu-id="1da48-180">Выберите свою сеть Wi-Fi в окне слева и настройте нужные параметры.</span><span class="sxs-lookup"><span data-stu-id="1da48-180">Select your Wi-Fi network in the left window and enter your desired customizations.</span></span> <span data-ttu-id="1da48-181">Включенные параметры будут отображаться полужирным шрифтом в меню слева.</span><span class="sxs-lookup"><span data-stu-id="1da48-181">The enabled customizations will show in bold on the left menu.</span></span>
    1. <span data-ttu-id="1da48-182">Щелкните "Сохранить и выйти".</span><span class="sxs-lookup"><span data-stu-id="1da48-182">Click Save and Exit.</span></span>
    1. <span data-ttu-id="1da48-183">[Примените](hololens-provisioning.md#applyremove-a-provisioning-package-to-hololens-after-setup) пакет подготовки к HoloLens.</span><span class="sxs-lookup"><span data-stu-id="1da48-183">[Apply](hololens-provisioning.md#applyremove-a-provisioning-package-to-hololens-after-setup) the provisioning package to the HoloLens.</span></span>

<span data-ttu-id="1da48-184">[Поставщики службы конфигурации](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) стоят за многими задачами и политиками управления для Windows 10 в Microsoft Intune и сторонних поставщиках служб MDM.</span><span class="sxs-lookup"><span data-stu-id="1da48-184">[CSPs](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) are behind many of the management tasks and policies for Windows 10, both in Microsoft Intune and in non-Microsoft MDM service providers.</span></span> <span data-ttu-id="1da48-185">Вы также можете использовать [конструктор конфигураций Windows](https://docs.microsoft.com/windows/configuration/provisioning-packages/provisioning-install-icd) для создания [пакета подготовки](https://docs.microsoft.com/windows/configuration/provisioning-packages/provisioning-packages) и его применения для HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="1da48-185">You can also use [Windows Configuration Designer](https://docs.microsoft.com/windows/configuration/provisioning-packages/provisioning-install-icd) to create a [provisioning package](https://docs.microsoft.com/windows/configuration/provisioning-packages/provisioning-packages) and apply it to the HoloLens 2.</span></span>
<span data-ttu-id="1da48-186">Наиболее вероятные поставщики службы конфигурации, которые будут применены к вашему устройству HoloLens 2:</span><span class="sxs-lookup"><span data-stu-id="1da48-186">The most likely CSPs that will be applied to your HoloLens 2 are:</span></span>

- <span data-ttu-id="1da48-187">[поставщик службы конфигурации WiFi](https://docs.microsoft.com/windows/client-management/mdm/wifi-csp) — прокси-сервер Wi-Fi на каждый профиль.</span><span class="sxs-lookup"><span data-stu-id="1da48-187">[WiFi CSP](https://docs.microsoft.com/windows/client-management/mdm/wifi-csp): per-profile Wi-Fi proxy</span></span> 

[<span data-ttu-id="1da48-188">Другие поставщики службы конфигурации, поддерживаемые устройствами HoloLens.</span><span class="sxs-lookup"><span data-stu-id="1da48-188">Other CSPs supported in HoloLens devices</span></span>](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference#hololens)





## <a name="vpn"></a><span data-ttu-id="1da48-189">Виртуальная частная сеть</span><span class="sxs-lookup"><span data-stu-id="1da48-189">VPN</span></span>
<span data-ttu-id="1da48-190">Подключение к сети VPN позволяет обеспечить более безопасное подключение и доступ к корпоративной сети и Интернету.</span><span class="sxs-lookup"><span data-stu-id="1da48-190">A VPN connection can help provide a more secure connection and access to your company's network and the Internet.</span></span> <span data-ttu-id="1da48-191">HoloLens 2 поддерживает встроенный подключаемый модуль VPN-клиента и универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="1da48-191">HoloLens 2 supports built-in VPN client and Universal Windows Platform (UWP) VPN plug-in.</span></span> 

<span data-ttu-id="1da48-192">Поддерживаемые встроенные протоколы VPN:</span><span class="sxs-lookup"><span data-stu-id="1da48-192">Supported Built-in VPN protocols:</span></span>
- <span data-ttu-id="1da48-193">IKEv2</span><span class="sxs-lookup"><span data-stu-id="1da48-193">IKEv2</span></span>
- <span data-ttu-id="1da48-194">L2TP</span><span class="sxs-lookup"><span data-stu-id="1da48-194">L2TP</span></span>
- <span data-ttu-id="1da48-195">PPTP</span><span class="sxs-lookup"><span data-stu-id="1da48-195">PPTP</span></span>

<span data-ttu-id="1da48-196">Если для аутентификации для встроенного VPN-клиента используется сертификат, требуемый сертификат клиента следует добавить в хранилище сертификатов пользователя.</span><span class="sxs-lookup"><span data-stu-id="1da48-196">If certificate is used for authentication for built-in VPN client, the required client certificate needs to be added to user certificate store.</span></span> <span data-ttu-id="1da48-197">Если подключаемый модуль VPN стороннего производителя поддерживает HoloLens 2, перейдите в Store, чтобы найти приложение VPN, и проверьте, содержится ли HoloLens в списке поддерживаемых устройств, а на странице требований к системе убедитесь, что приложение поддерживает архитектуру ARM или ARM64.</span><span class="sxs-lookup"><span data-stu-id="1da48-197">To find if a 3rd party VPN plug-in supports HoloLens 2, go to Store to locate VPN app and check if HoloLens is listed as a supported device and in the System Requirement page the app supports ARM or ARM64 architecture.</span></span> <span data-ttu-id="1da48-198">HoloLens поддерживает только приложения универсальной платформы Windows для сторонних сетей VPN.</span><span class="sxs-lookup"><span data-stu-id="1da48-198">HoloLens only supports Universal Windows Platform applications for 3rd party VPN.</span></span>

 <span data-ttu-id="1da48-199">VPN можно управлять с помощью MDM, выбрав политику [Settings/AllowVPN](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn) и настроив с помощью [политики Vpnv2-csp](https://docs.microsoft.com/windows/client-management/mdm/vpnv2-csp).</span><span class="sxs-lookup"><span data-stu-id="1da48-199">VPN can be managed by MDM via [Settings/AllowVPN](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn), and set via  [Vpnv2-csp policy](https://docs.microsoft.com/windows/client-management/mdm/vpnv2-csp).</span></span>

<span data-ttu-id="1da48-200">Дополнительные сведения о [настройке VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) см. в [этих руководствах](https://docs.microsoft.com/windows/security/identity-protection/vpn/vpn-guide).</span><span class="sxs-lookup"><span data-stu-id="1da48-200">Learn more about [how to configure VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) with [these guides](https://docs.microsoft.com/windows/security/identity-protection/vpn/vpn-guide).</span></span>  

### <a name="vpn-via-ui"></a><span data-ttu-id="1da48-201">Настройка VPN с помощью пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="1da48-201">VPN via UI</span></span>

<span data-ttu-id="1da48-202">По умолчанию сеть VPN отключена, но ее можно включить вручную, открыв приложение **Параметры** и перейдя к пункту **Сеть и Интернет -> VPN**.</span><span class="sxs-lookup"><span data-stu-id="1da48-202">VPN is not enabled by default but can be enabled manually by opening **Settings** app and navigating to  **Network & Internet -> VPN**.</span></span>
1. <span data-ttu-id="1da48-203">Выберите поставщик услуг VPN.</span><span class="sxs-lookup"><span data-stu-id="1da48-203">Select a VPN provider.</span></span>
1. <span data-ttu-id="1da48-204">Присвойте подключению имя.</span><span class="sxs-lookup"><span data-stu-id="1da48-204">Create a connection name.</span></span> 
1. <span data-ttu-id="1da48-205">Введите имя или адрес сервера.</span><span class="sxs-lookup"><span data-stu-id="1da48-205">Enter your server name or address.</span></span>
1. <span data-ttu-id="1da48-206">Выберите тип VPN.</span><span class="sxs-lookup"><span data-stu-id="1da48-206">Select the VPN type.</span></span>
1. <span data-ttu-id="1da48-207">Выберите тип сведений для входа.</span><span class="sxs-lookup"><span data-stu-id="1da48-207">Select type of sign-in info.</span></span> 
1. <span data-ttu-id="1da48-208">При необходимости добавьте имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="1da48-208">Optionally add user name and password.</span></span>
1. <span data-ttu-id="1da48-209">Примените параметры VPN.</span><span class="sxs-lookup"><span data-stu-id="1da48-209">Apply the VPN settings.</span></span> 

![Параметры VPN для HoloLens](./images/vpn-settings-ui.jpg)

### <a name="vpn-set-via-provisioning-package"></a><span data-ttu-id="1da48-211">Настройка VPN с помощью пакета подготовки</span><span class="sxs-lookup"><span data-stu-id="1da48-211">VPN set via Provisioning Package</span></span>

> [!TIP] 
> <span data-ttu-id="1da48-212">В Windows Holographic версии 20H2 мы устранили проблему с конфигурацией прокси-сервера для подключения VPN.</span><span class="sxs-lookup"><span data-stu-id="1da48-212">In our Windows Holographic, version 20H2 we fixed a proxy configuration issue for VPN connection.</span></span> <span data-ttu-id="1da48-213">Если вы планируете использовать этот поток, попробуйте обновить устройства до этой сборки.</span><span class="sxs-lookup"><span data-stu-id="1da48-213">Please consider upgrading devices to this build if you intend to use this flow.</span></span>

1. <span data-ttu-id="1da48-214">Запустите конструктор конфигураций Windows.</span><span class="sxs-lookup"><span data-stu-id="1da48-214">Launch Windows Configuration Designer.</span></span>
1. <span data-ttu-id="1da48-215">Щелкните **Подготовить устройства HoloLens**, а затем выберите целевое устройство и щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1da48-215">Click **Provision HoloLens devices**, then select target device and **Next**.</span></span>
1. <span data-ttu-id="1da48-216">Введите имя пакета и путь к нему.</span><span class="sxs-lookup"><span data-stu-id="1da48-216">Enter package name and path.</span></span>
1. <span data-ttu-id="1da48-217">Щелкните **Перейти в расширенный редактор**.</span><span class="sxs-lookup"><span data-stu-id="1da48-217">Click **Switch to advanced editor**.</span></span>
1. <span data-ttu-id="1da48-218">Откройте **Параметры среды выполнения** -> **Профили подключений** -> **VPN** -> **Параметры VPN**.</span><span class="sxs-lookup"><span data-stu-id="1da48-218">Open **Runtime settings** -> **ConnectivityProfiles** -> **VPN** -> **VPNSettings**.</span></span>
1. <span data-ttu-id="1da48-219">Настройка параметра VPNProfileName</span><span class="sxs-lookup"><span data-stu-id="1da48-219">Configure VPNProfileName</span></span>
1. <span data-ttu-id="1da48-220">Выберите значение для ProfileType: **Собственный** или **Сторонний**.</span><span class="sxs-lookup"><span data-stu-id="1da48-220">Select ProfileType: **Native** or **Third Party**.</span></span>
    1. <span data-ttu-id="1da48-221">Для собственного профиля выберите **NativeProtocolType**, затем настройте сервер, политику маршрутизации, тип аутентификации и другие параметры.</span><span class="sxs-lookup"><span data-stu-id="1da48-221">For Native profile, select **NativeProtocolType**, then configure server, routing policy, authentication type and other settings.</span></span>
    1. <span data-ttu-id="1da48-222">Для стороннего профиля настройте URL-адрес сервера, имя семейства пакетов подключаемого модуля приложения VPN (только три имени предварительно заданы) и настраиваемые конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1da48-222">For "Third Party" profile, configure server URL, VPN plug-in App package family name (only 3 predefined) and custom configurations.</span></span>
1. <span data-ttu-id="1da48-223">Экспортируйте пакет.</span><span class="sxs-lookup"><span data-stu-id="1da48-223">Export your package.</span></span>
1. <span data-ttu-id="1da48-224">Подключите HoloLens и скопируйте файл .ppkg на устройство.</span><span class="sxs-lookup"><span data-stu-id="1da48-224">Connect your HoloLens and copy the .ppkg file to the device.</span></span> 
1. <span data-ttu-id="1da48-225">На устройстве HoloLens примените файл VPN .ppkg, открыв меню "Пуск" и выбрав **Параметры** -> **Учетные записи** -> **Доступ к учетной записи места работы или учебного заведения** -> **Добавление или удаление пакета подготовки** и выберите свой пакет VPN.</span><span class="sxs-lookup"><span data-stu-id="1da48-225">On HoloLens, apply the VPN .ppkg by opening the Start menu and selecting **Settings** -> **Account** -> **Access work or school** -> **Add or remove provisioning package** -> Select your VPN package.</span></span>


### <a name="setting-up-vpn-via-intune"></a><span data-ttu-id="1da48-226">Настройка VPN с помощью Intune</span><span class="sxs-lookup"><span data-stu-id="1da48-226">Setting up VPN via Intune</span></span>
<span data-ttu-id="1da48-227">Чтобы приступить к работе, просто следуйте документации Intune.</span><span class="sxs-lookup"><span data-stu-id="1da48-227">Just follow the Intune documents to get started.</span></span> <span data-ttu-id="1da48-228">При выполнении этих действий следует учитывать встроенные протоколы VPN, поддерживаемые устройствами HoloLens.</span><span class="sxs-lookup"><span data-stu-id="1da48-228">When following these steps please keep in mind the built-in VPN protocols that HoloLens devices support.</span></span> 

<span data-ttu-id="1da48-229">[Создание профилей VPN для подключения к VPN-серверам в Intune.](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-configure)</span><span class="sxs-lookup"><span data-stu-id="1da48-229">[Create VPN profiles to connect to VPN servers in Intune](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-configure).</span></span>

<span data-ttu-id="1da48-230">[Параметры устройств Windows 10 и Windows Holographic для добавления VPN-подключений с помощью Intune.](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-windows-10)</span><span class="sxs-lookup"><span data-stu-id="1da48-230">[Windows 10 and Windows Holographic device settings to add VPN connections using Intune](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-windows-10).</span></span>

<span data-ttu-id="1da48-231">По завершении не забудьте [назначить профиль](https://docs.microsoft.com/mem/intune/configuration/device-profile-assign).</span><span class="sxs-lookup"><span data-stu-id="1da48-231">When done please remember to [assign the profile](https://docs.microsoft.com/mem/intune/configuration/device-profile-assign).</span></span>

### <a name="vpn-via-3rd-party-mdm-solutions"></a><span data-ttu-id="1da48-232">Настройка VPN с помощью сторонних решений MDM.</span><span class="sxs-lookup"><span data-stu-id="1da48-232">VPN via 3rd party MDM solutions</span></span>
<span data-ttu-id="1da48-233">Пример стороннего подключения VPN:</span><span class="sxs-lookup"><span data-stu-id="1da48-233">3rd party VPN connection example:</span></span>
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

<span data-ttu-id="1da48-234">Пример собственного VPN с использованием протокола IKEv2:</span><span class="sxs-lookup"><span data-stu-id="1da48-234">Native IKEv2 VPN example:</span></span>
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
## <a name="disabling-wi-fi-on-hololens-1st-gen"></a><span data-ttu-id="1da48-235">Отключение Wi-Fi на устройстве HoloLens (1-е поколение)</span><span class="sxs-lookup"><span data-stu-id="1da48-235">Disabling Wi-Fi on HoloLens (1st gen)</span></span>

### <a name="using-the-settings-app-on-hololens"></a><span data-ttu-id="1da48-236">С помощью приложения "Параметры" на устройстве HoloLens</span><span class="sxs-lookup"><span data-stu-id="1da48-236">Using the Settings app on HoloLens</span></span>

1. <span data-ttu-id="1da48-237">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="1da48-237">Open the **Start** menu.</span></span>
1. <span data-ttu-id="1da48-238">Выберите приложение **Параметры** в меню **Пуск** или в списке **Все программы** справа от меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="1da48-238">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="1da48-239">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="1da48-239">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="1da48-240">Выберите **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="1da48-240">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="1da48-241">Выберите переключатель Wi-Fi, чтобы переместить его в положение **Выкл.**</span><span class="sxs-lookup"><span data-stu-id="1da48-241">Select the Wi-Fi slider switch to move it to the **Off** position.</span></span> <span data-ttu-id="1da48-242">Это приведет к отключению радиочастотных компонентов радиомодуля Wi-Fi и отключению всех функций Wi-Fi на устройстве HoloLens.</span><span class="sxs-lookup"><span data-stu-id="1da48-242">This will turn off the RF components of the Wi-Fi radio and disable all Wi-Fi functionality on HoloLens.</span></span>

    > [!WARNING]
    > <span data-ttu-id="1da48-243">Если радиомодуль Wi-Fi отключен, HoloLens не сможет автоматически загружать ваши [пространства](hololens-spaces.md).</span><span class="sxs-lookup"><span data-stu-id="1da48-243">When the Wi-Fi radio is disabled, HoloLens will not be able to automatically load your [spaces](hololens-spaces.md).</span></span>

1. <span data-ttu-id="1da48-244">Переведите переключатель в положение **Вкл.** , чтобы включить радиомодуль Wi-Fi и восстановить функциональность Wi-Fi на устройстве Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="1da48-244">Move the slider switch to the **On** position to turn on the Wi-Fi radio and restore Wi-Fi functionality on Microsoft HoloLens.</span></span> <span data-ttu-id="1da48-245">Выбранное состояние радиомодуля Wi-Fi (**Вкл.** или **Выкл.** ) будет сохранено при перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="1da48-245">The selected Wi-Fi radio state (**On** or **Off**) will persist across reboots.</span></span>

## <a name="identifying-the-ip-address-of-your-hololens-on-the-wi-fi-network"></a><span data-ttu-id="1da48-246">Определение IP-адреса HoloLens в сети Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="1da48-246">Identifying the IP Address of your HoloLens on the Wi-Fi network</span></span>

### <a name="by-using-the-settings-app"></a><span data-ttu-id="1da48-247">С помощью приложения "Параметры"</span><span class="sxs-lookup"><span data-stu-id="1da48-247">By using the Settings app</span></span>

1. <span data-ttu-id="1da48-248">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="1da48-248">Open the **Start** menu.</span></span>
1. <span data-ttu-id="1da48-249">Выберите приложение **Параметры** в меню **Пуск** или в списке **Все программы** справа от меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="1da48-249">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="1da48-250">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="1da48-250">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="1da48-251">Выберите **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="1da48-251">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="1da48-252">Прокрутите список доступных сетей Wi-Fi вниз до пункта **Свойства оборудования**.</span><span class="sxs-lookup"><span data-stu-id="1da48-252">Scroll down to beneath the list of available Wi-Fi networks and select **Hardware properties**.</span></span>

    ![Свойства оборудования в параметрах Wi-Fi](./images/wifi-hololens-hwdetails.jpg)

   <span data-ttu-id="1da48-254">IP-адрес отображается рядом с **адресом IPv4**.</span><span class="sxs-lookup"><span data-stu-id="1da48-254">The IP address appears next to **IPv4 address**.</span></span>

### <a name="by-using-voice-commands"></a><span data-ttu-id="1da48-255">С использованием голосовых команд</span><span class="sxs-lookup"><span data-stu-id="1da48-255">By using voice commands</span></span>

<span data-ttu-id="1da48-256">В зависимости от сборки вашего устройства на некоторых устройствах можно использовать встроенные голосовые команды или Кортану для отображения вашего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="1da48-256">Depending on your devices build you can either use built in voice commands or Cortana to display your IP address.</span></span> <span data-ttu-id="1da48-257">В сборках версий после [19041.1103](hololens-release-notes.md#windows-holographic-version-2004) произнесите What's my IP address? (Какой у меня IP адрес?),</span><span class="sxs-lookup"><span data-stu-id="1da48-257">On builds after [19041.1103](hololens-release-notes.md#windows-holographic-version-2004) speak "What's my IP address?"</span></span> <span data-ttu-id="1da48-258">чтобы отобразить IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="1da48-258">and it will be displayed.</span></span> <span data-ttu-id="1da48-259">Для более ранних сборок или HoloLens (1-ого поколения) произнесите Hey Cortana, What's my IP address? (Привет, Кортана! Какой у меня IP-адрес?).</span><span class="sxs-lookup"><span data-stu-id="1da48-259">For earlier builds or HoloLens (1st gen) say "Hey Cortana, What's my IP address?"</span></span> <span data-ttu-id="1da48-260">Кортана отобразит и прочитает ваш IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="1da48-260">and Cortana will display and read out your IP address.</span></span>

### <a name="by-using-windows-device-portal"></a><span data-ttu-id="1da48-261">С помощью портала устройств Windows</span><span class="sxs-lookup"><span data-stu-id="1da48-261">By using Windows Device Portal</span></span>

1. <span data-ttu-id="1da48-262">В веб-браузере на компьютере откройте [портал устройств](/windows/mixed-reality/using-the-windows-device-portal.md#networking).</span><span class="sxs-lookup"><span data-stu-id="1da48-262">In a web browser on your PC, open the [device portal](/windows/mixed-reality/using-the-windows-device-portal.md#networking).</span></span>
1. <span data-ttu-id="1da48-263">Перейдите к разделу **Сеть**.</span><span class="sxs-lookup"><span data-stu-id="1da48-263">Navigate to the **Networking** section.</span></span>  
   <span data-ttu-id="1da48-264">В этом разделе отображается ваш IP-адрес и другая информация о сети.</span><span class="sxs-lookup"><span data-stu-id="1da48-264">This section displays your IP address and other network information.</span></span> <span data-ttu-id="1da48-265">С помощью этого метода можно скопировать и вставить IP-адрес на компьютер для разработки.</span><span class="sxs-lookup"><span data-stu-id="1da48-265">By using this method, you can copy and paste of the IP address on your development PC.</span></span>

## <a name="change-ip-address-to-static-address"></a><span data-ttu-id="1da48-266">Изменение IP-адреса на статический адрес</span><span class="sxs-lookup"><span data-stu-id="1da48-266">Change IP Address to static address</span></span>
### <a name="by-using-settings"></a><span data-ttu-id="1da48-267">С помощью приложения "Параметры"</span><span class="sxs-lookup"><span data-stu-id="1da48-267">By using Settings</span></span>
 
1. <span data-ttu-id="1da48-268">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="1da48-268">Open the **Start** menu.</span></span>
1. <span data-ttu-id="1da48-269">Выберите приложение **Параметры** в меню **Пуск** или в списке **Все программы** справа от меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="1da48-269">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="1da48-270">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="1da48-270">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="1da48-271">Выберите **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="1da48-271">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="1da48-272">Прокрутите список доступных сетей Wi-Fi вниз до пункта **Свойства оборудования**.</span><span class="sxs-lookup"><span data-stu-id="1da48-272">Scroll down to beneath the list of available Wi-Fi networks and select **Hardware properties**.</span></span>
1. <span data-ttu-id="1da48-273">В окне **Изменение параметров IP-адреса** задайте для первого поля значение **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="1da48-273">In the **Edit IP settings** window, change the first field to **Manual**.</span></span>
1. <span data-ttu-id="1da48-274">Задайте требуемую IP-конфигурацию в остальных полях и щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1da48-274">Input the desired IP configuration in the remaining fields and then click **Save**.</span></span>

### <a name="by-using-windows-device-portal"></a><span data-ttu-id="1da48-275">С помощью портала устройств Windows</span><span class="sxs-lookup"><span data-stu-id="1da48-275">By using Windows Device Portal</span></span>

1. <span data-ttu-id="1da48-276">В веб-браузере на компьютере откройте [портал устройств](/windows/mixed-reality/using-the-windows-device-portal.md#networking).</span><span class="sxs-lookup"><span data-stu-id="1da48-276">In a web browser on your PC, open the [device portal](/windows/mixed-reality/using-the-windows-device-portal.md#networking).</span></span>
1. <span data-ttu-id="1da48-277">Перейдите к разделу **Сеть**.</span><span class="sxs-lookup"><span data-stu-id="1da48-277">Navigate to the **Networking** section.</span></span>
1. <span data-ttu-id="1da48-278">Нажмите кнопку **Конфигурация IPv4**.</span><span class="sxs-lookup"><span data-stu-id="1da48-278">Select the **IPv4 Configuration** button.</span></span>
1. <span data-ttu-id="1da48-279">Выберите **Использовать следующий IP-адрес** и введите нужную конфигурацию TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1da48-279">Select **Use the following IP address** and input the desired TCP/IP configuration.</span></span>
1. <span data-ttu-id="1da48-280">Выберите **Использовать следующие адреса DNS-серверов** и введите предпочитаемые и альтернативные адреса DNS-серверов (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="1da48-280">Select **Use the following DNS server addresses** and enter the Preferred and Alternate DNS server addresses, if needed.</span></span>
1. <span data-ttu-id="1da48-281">Выберите команду **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1da48-281">Click **Save**.</span></span> 
