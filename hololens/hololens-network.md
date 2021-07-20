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
ms.openlocfilehash: c2a2fe1a20a4e9baa194b1037ccb6649d324b990
ms.sourcegitcommit: 4c15afc772fba26683d9b75e38c44a018b4889f6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113640225"
---
# <a name="connect-hololens-to-a-network"></a>Подключение HoloLens к сети

Для выполнения большинства задач на устройстве HoloLens оно должно быть подключено к сети. Устройство HoloLens оборудовано радиомодулем Wi-Fi 2x2 с поддержкой стандарта 802.11ac. Его подключение к сети осуществляется так же, как подключение к сети Wi-Fi классического или мобильного устройства с Windows 10. Это руководство поможет вам:

- подключиться к сети с помощью Wi-Fi, а также к (только для HoloLens 2) Wi-Fi Direct или Ethernet через USB-C;
- отключить и повторно включить Wi-Fi.

См. дополнительные сведения об [использовании HoloLens в автономном режиме](hololens-offline.md).

## <a name="connecting-for-the-first-time"></a>Первое подключение

При первом использовании HoloLens вам будет предложено пройти процедуру подключения к сети Wi-Fi. При наличии проблем с подключением к сети Wi-Fi во время настройки проверьте, открыта ли ваша сеть, защищена ли она паролем и имеет ли она портал авторизации. Кроме того, убедитесь, что для подключения к сети не требуется использование сертификата. После завершения настройки можно будет подключаться к другим типам сетей Wi-Fi.

На устройствах HoloLens 2 пользователь также может [использовать адаптер USB-C для Ethernet](hololens-connect-devices.md#hololens-2-connect-usb-c-devices) для подключения напрямую к Wi-Fi и настройки устройства. Завершив настройку устройства, пользователь может продолжать использовать адаптер или отключить его от устройства и [подключиться к Wi-Fi после настройки](hololens-network.md#connecting-to-wi-fi-after-setup). 

## <a name="connecting-to-wi-fi-after-setup"></a>Подключение к сети Wi-Fi после настройки

1. Выполните **жест "Пуск"** и выберите **Параметры**. Приложение "Параметры" будет автоматически размещено перед вами.
1. Выберите **Сеть и Интернет** > **Wi-Fi**. Убедитесь, что функция Wi-Fi включена. Если вы не видите сеть, прокрутите список вниз.
1. Выберите сеть и щелкните **Подключить**.
1. В ответ на соответствующий запрос введите пароль от сети и щелкните **Далее**.

![Параметры Wi-Fi для HoloLens](./images/hololens-2-wifi-settings.jpg)

Чтобы подтвердить подключение к сети Wi-Fi, проверьте состояние Wi-Fi в меню **Пуск**:

1. Откройте меню **Пуск**.
1. Проверьте состояние сети Wi-Fi в верхнем левом углу меню **Пуск**. Будет отображено состояние Wi-Fi и SSID подключенной сети.

> [!TIP]
> Если сеть Wi-Fi недоступна, вы также можете [подключиться к сотовым сетям или сетям 5G](hololens-cellular.md).

> [!IMPORTANT]
> Пользователи не могут точно настраивать поведение HoloLens 2 при поиске сетей Wi-Fi — **единственный способ обновить список Wi-Fi заключается в отключении и включении Wi-Fi**. Это предотвращает множество проблем, например с зависанием устройства в точке доступа после выхода из диапазона.

## <a name="connect-hololens-to-enterprise-wi-fi-network"></a>Подключение HoloLens к корпоративной сети Wi-Fi

В корпоративных профилях Wi-Fi для аутентификации подключений по Wi-Fi используется протокол расширенной аутентификации (EAP). Корпоративный профиль HoloLens для Wi-Fi можно настроить с помощью MDM или пакета подготовки, созданного с помощью [конструктора конфигураций Windows](/windows/configuration/provisioning-packages/provisioning-packages).

Инструкции по настройке устройства, управляемого с помощью службы Microsoft Intune, см. [здесь](/mem/intune/configuration/wi-fi-settings-windows#enterprise-profile).

Чтобы создать пакет подготовки Wi-Fi в конструкторе конфигураций Windows, требуется файл предварительно настроенного профиля Wi-Fi в формате XML. Ниже приведен пример профиля Wi-Fi для WPA2-Enterprise с аутентификацией EAP-TLS.

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


Сертификат корневого ЦС сервера и сертификат клиента, возможно, нужно будет подготовить на устройстве, в зависимости от типа EAP.

Дополнительные ресурсы:

- Схема WLANv1Profile: [[MS-GPWL]: Схема LAN Profile v1 | Документация Майкрософт](/openspecs/windows_protocols/ms-gpwl/34054c93-cfcd-44df-89d8-5f2ba7532b67)
- Схема EAP-TLS: [[MS-GPWL]: Схема Microsoft EAP TLS | Документация Майкрософт](/openspecs/windows_protocols/ms-gpwl/9590925c-cba2-4ac5-b9a1-1e5292bb72cb)

Если при подключении к Wi-Fi возникают проблемы, см. рекомендации по [устранению неполадок](hololens2-enterprise-troubleshooting.md#).

## <a name="configure-network-proxy"></a>Настройка сетевого прокси-сервера

В этом разделе рассматривается сетевой прокси-сервер для ОС HoloLens и приложений UWP с использованием стека HTTP Windows. Приложения, использующие стек HTTP без Windows, могут иметь собственную конфигурацию прокси-сервера и средства работы с ним. 

### <a name="proxy-configurations"></a>Конфигурации прокси-сервера 

- Скрипт автоматической конфигурации прокси-сервера (PAC): [файл PAC](https://developer.mozilla.org/en-US/docs/Web/HTTP/Proxy_servers_and_tunneling/Proxy_Auto-Configuration_PAC_file) (открывает сайт, не принадлежащий Майкрософт) содержит функцию JavaScript FindProxyForURL(url, host). 
- Статический прокси-сервер: в формате сервер:порт.  
- Протокол автоматического обнаружения прокси-сервера (WPAD): предоставляет URL-адрес для файла конфигурации прокси-сервера по DHCP или DNS. 

### <a name="proxy-provisioning-methods"></a>Методы подготовки прокси-сервера 
Существует три способа для подготовки прокси-серверов:

 

1.  **Пользовательский интерфейс "Параметры":** 
    1. Прокси-сервер на отдельного пользователя (20H2 и более ранних версий):
        1. Откройте меню "Пуск" и выберите Параметры.
        2. Выберите "Сеть и Интернет", а затем "Прокси-сервер" в меню слева.
        3. Прокрутите вниз до пункта "Настройка прокси-сервера вручную" и установите переключатель "Использовать прокси-сервер" в положение "Вкл.".
        4. Введите IP-адрес прокси-сервера.
        5. Введите номер порта.
        6. Нажмите кнопку «Сохранить».
      1. Прокси-сервер WiFi (21H1 и более поздние версии):
          1. Откройте меню "Пуск" и перейдите на страницу свойств сети Wi-Fi.
          1. Прокрутите вниз до раздела "Прокси-сервер".
          1. Выберите "Настройка вручную".
          1. Введите IP-адрес прокси-сервера.
          1. Введите номер порта.
          1. Нажмите кнопку "Применить".
        
 2. **MDM** 
     1. Intune — выполните эти [шаги](/mem/intune/configuration/wi-fi-settings-windows#enterprise-profile), чтобы настроить прокси-сервер в Intune. Вам нужно прокрутить в самый низ раздела.
     1. Другие решения MDM сторонних поставщиков — используйте [поставщик службы конфигурации Wi-Fi](/windows/client-management/mdm/wifi-csp).

3. **PPKG** 
    1. Откройте конструктор конфигураций Windows.
    1. Щелкните "Расширенная подготовка", введите имя нового проекта и щелкните "Далее".
    1. Выберите Windows Holographic (HoloLens 2) и щелкните "Далее".
    1. Импортируйте PPKG (необязательно) и щелкните "Готово".
    1. Выберите "Параметры среды выполнения" -> "Профили подключения" -> "Беспроводная сеть" -> "Прокси-сервер беспроводной сети".
    1. Введите идентификатор SSID сети Wi-Fi и щелкните "Добавить".
    1. Выберите свою сеть Wi-Fi в окне слева и настройте нужные параметры. Включенные параметры будут отображаться полужирным шрифтом в меню слева.
    1. Щелкните "Сохранить и выйти".
    1. [Примените](hololens-provisioning.md#applyremove-a-provisioning-package-to-hololens-after-setup) пакет подготовки к HoloLens.

[Поставщики службы конфигурации](/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) стоят за многими задачами и политиками управления для Windows 10 в Microsoft Intune и сторонних поставщиках служб MDM. Вы также можете использовать [конструктор конфигураций Windows](/windows/configuration/provisioning-packages/provisioning-install-icd) для создания [пакета подготовки](/windows/configuration/provisioning-packages/provisioning-packages) и его применения для HoloLens 2.
Наиболее вероятные поставщики службы конфигурации, которые будут применены к вашему устройству HoloLens 2:

- [поставщик службы конфигурации WiFi](/windows/client-management/mdm/wifi-csp) — прокси-сервер Wi-Fi на каждый профиль. 

[Другие поставщики службы конфигурации, поддерживаемые устройствами HoloLens.](/windows/client-management/mdm/configuration-service-provider-reference#hololens)





## <a name="vpn"></a>Виртуальная частная сеть
Подключение к сети VPN позволяет обеспечить более безопасное подключение и доступ к корпоративной сети и Интернету. HoloLens 2 поддерживает встроенный подключаемый модуль VPN-клиента и универсальной платформы Windows (UWP). 

Поддерживаемые встроенные протоколы VPN:
- IKEv2
- L2TP
- PPTP

Если для аутентификации для встроенного VPN-клиента используется сертификат, требуемый сертификат клиента следует добавить в хранилище сертификатов пользователя. Если подключаемый модуль VPN стороннего производителя поддерживает HoloLens 2, перейдите в Store, чтобы найти приложение VPN, и проверьте, содержится ли HoloLens в списке поддерживаемых устройств, а на странице требований к системе убедитесь, что приложение поддерживает архитектуру ARM или ARM64. HoloLens поддерживает только приложения универсальной платформы Windows для сторонних сетей VPN.

 VPN можно управлять с помощью MDM, выбрав политику [Settings/AllowVPN](/windows/client-management/mdm/policy-csp-settings#settings-allowvpn) и настроив с помощью [политики Vpnv2-csp](/windows/client-management/mdm/vpnv2-csp).

Дополнительные сведения о [настройке VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) см. в [этих руководствах](/windows/security/identity-protection/vpn/vpn-guide).  

### <a name="vpn-via-ui"></a>Настройка VPN с помощью пользовательского интерфейса

По умолчанию сеть VPN отключена, но ее можно включить вручную, открыв приложение **Параметры** и перейдя к пункту **Сеть и Интернет -> VPN**.
1. Выберите поставщик услуг VPN.
1. Присвойте подключению имя. 
1. Введите имя или адрес сервера.
1. Выберите тип VPN.
1. Выберите тип сведений для входа. 
1. При необходимости добавьте имя пользователя и пароль.
1. Примените параметры VPN. 

![Параметры VPN для HoloLens](./images/vpn-settings-ui.jpg)

### <a name="vpn-set-via-provisioning-package"></a>Настройка VPN с помощью пакета подготовки

> [!TIP] 
> В Windows Holographic версии 20H2 мы устранили проблему с конфигурацией прокси-сервера для подключения VPN. Если вы планируете использовать этот поток, попробуйте обновить устройства до этой сборки.

1. Запустите конструктор конфигураций Windows.
1. Щелкните **Подготовить устройства HoloLens**, а затем выберите целевое устройство и щелкните **Далее**.
1. Введите имя пакета и путь к нему.
1. Щелкните **Перейти в расширенный редактор**.
1. Откройте **Параметры среды выполнения** -> **Профили подключений** -> **VPN** -> **Параметры VPN**.
1. Настройка параметра VPNProfileName
1. Выберите значение для ProfileType: **Собственный** или **Сторонний**.
    1. Для собственного профиля выберите **NativeProtocolType**, затем настройте сервер, политику маршрутизации, тип аутентификации и другие параметры.
    1. Для стороннего профиля настройте URL-адрес сервера, имя семейства пакетов подключаемого модуля приложения VPN (только три имени предварительно заданы) и настраиваемые конфигурации.
1. Экспортируйте пакет.
1. Подключите HoloLens и скопируйте файл .ppkg на устройство. 
1. На устройстве HoloLens примените файл VPN .ppkg, открыв меню "Пуск" и выбрав **Параметры** -> **Учетные записи** -> **Доступ к учетной записи места работы или учебного заведения** -> **Добавление или удаление пакета подготовки** и выберите свой пакет VPN.


### <a name="setting-up-vpn-via-intune"></a>Настройка VPN с помощью Intune
Чтобы приступить к работе, просто следуйте документации Intune. При выполнении этих действий следует учитывать встроенные протоколы VPN, поддерживаемые устройствами HoloLens. 

[Создание профилей VPN для подключения к VPN-серверам в Intune.](/mem/intune/configuration/vpn-settings-configure)

[Параметры устройств Windows 10 и Windows Holographic для добавления VPN-подключений с помощью Intune.](/mem/intune/configuration/vpn-settings-windows-10)

По завершении не забудьте [назначить профиль](/mem/intune/configuration/device-profile-assign).

### <a name="vpn-via-3rd-party-mdm-solutions"></a>Настройка VPN с помощью сторонних решений MDM.
Пример стороннего подключения VPN:
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

Пример собственного VPN с использованием протокола IKEv2:
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
## <a name="disabling-wi-fi-on-hololens-1st-gen"></a>Отключение Wi-Fi на устройстве HoloLens (1-е поколение)

### <a name="using-the-settings-app-on-hololens"></a>С помощью приложения "Параметры" на устройстве HoloLens

1. Откройте меню **Пуск**.
1. Выберите приложение **Параметры** в меню **Пуск** или в списке **Все программы** справа от меню **Пуск**. Приложение **Параметры** будет автоматически размещено перед вами.
1. Выберите **Сеть и Интернет**.
1. Выберите переключатель Wi-Fi, чтобы переместить его в положение **Выкл.** Это приведет к отключению радиочастотных компонентов радиомодуля Wi-Fi и отключению всех функций Wi-Fi на устройстве HoloLens.

    > [!WARNING]
    > Если радиомодуль Wi-Fi отключен, HoloLens не сможет автоматически загружать ваши [пространства](hololens-spaces.md).

1. Переведите переключатель в положение **Вкл.** , чтобы включить радиомодуль Wi-Fi и восстановить функциональность Wi-Fi на устройстве Microsoft HoloLens. Выбранное состояние радиомодуля Wi-Fi (**Вкл.** или **Выкл.** ) будет сохранено при перезагрузке.

## <a name="identifying-the-ip-address-of-your-hololens-on-the-wi-fi-network"></a>Определение IP-адреса HoloLens в сети Wi-Fi

### <a name="by-using-the-settings-app"></a>С помощью приложения "Параметры"

1. Откройте меню **Пуск**.
1. Выберите приложение **Параметры** в меню **Пуск** или в списке **Все программы** справа от меню **Пуск**. Приложение **Параметры** будет автоматически размещено перед вами.
1. Выберите **Сеть и Интернет**.
1. Прокрутите список доступных сетей Wi-Fi вниз до пункта **Свойства оборудования**.

    ![Свойства оборудования в параметрах Wi-Fi](./images/wifi-hololens-hwdetails.jpg)

   IP-адрес отображается рядом с **адресом IPv4**.

### <a name="by-using-voice-commands"></a>С использованием голосовых команд

В зависимости от сборки вашего устройства на некоторых устройствах можно использовать встроенные голосовые команды или Кортану для отображения вашего IP-адреса. В сборках версий после [19041.1103](hololens-release-notes.md#windows-holographic-version-2004) произнесите What's my IP address? (Какой у меня IP адрес?), чтобы отобразить IP-адрес. Для более ранних сборок или HoloLens (1-ого поколения) произнесите Hey Cortana, What's my IP address? (Привет, Кортана! Какой у меня IP-адрес?). Кортана отобразит и прочитает ваш IP-адрес.

### <a name="by-using-windows-device-portal"></a>С помощью портала устройств Windows

1. В веб-браузере на компьютере откройте [портал устройств](/windows/mixed-reality/using-the-windows-device-portal.md#networking).
1. Перейдите к разделу **Сеть**.  
   В этом разделе отображается ваш IP-адрес и другая информация о сети. С помощью этого метода можно скопировать и вставить IP-адрес на компьютер для разработки.

## <a name="change-ip-address-to-static-address"></a>Изменение IP-адреса на статический адрес
### <a name="by-using-settings"></a>С помощью приложения "Параметры"
 
1. Откройте меню **Пуск**.
1. Выберите приложение **Параметры** в меню **Пуск** или в списке **Все программы** справа от меню **Пуск**. Приложение **Параметры** будет автоматически размещено перед вами.
1. Выберите **Сеть и Интернет**.
1. Прокрутите список доступных сетей Wi-Fi вниз до пункта **Свойства оборудования**.
1. В окне **Изменение параметров IP-адреса** задайте для первого поля значение **Вручную**.
1. Задайте требуемую IP-конфигурацию в остальных полях и щелкните **Сохранить**.

### <a name="by-using-windows-device-portal"></a>С помощью портала устройств Windows

1. В веб-браузере на компьютере откройте [портал устройств](/windows/mixed-reality/using-the-windows-device-portal.md#networking).
1. Перейдите к разделу **Сеть**.
1. Нажмите кнопку **Конфигурация IPv4**.
1. Выберите **Использовать следующий IP-адрес** и введите нужную конфигурацию TCP/IP.
1. Выберите **Использовать следующие адреса DNS-серверов** и введите предпочитаемые и альтернативные адреса DNS-серверов (при необходимости).
1. Выберите команду **Сохранить**. 
