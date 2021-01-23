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
ms.openlocfilehash: 6d11ae0907aa82df71d7c86bb37996dcce71d845
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283980"
---
# Подключение HoloLens к сети

Для выполнения большинства задач на устройстве HoloLens устройство должно быть подключено к сети. Это руководство поможет вам:

- Подключиться к сети с помощью Wi-Fi или (только для HoloLens 2) Ethernet через USB-C
- Отключить и повторно включить Wi-Fi

Подробнее об [использовании HoloLens в автономном режиме](hololens-offline.md).

## Первое подключение

При первом использовании HoloLens вам будет предложено пройти процедуру подключения к сети Wi-Fi. При наличии проблем с подключением к сети Wi-Fi во время настройки проверьте, открыта ли ваша сеть или она защищена паролем и имеет ли она портал авторизации. Убедитесь, что для подключения к сети не требуется использование сертификата. После завершения настройки можно будет подключаться к другим типам сетей Wi-Fi.

На устройствах HoloLens 2 пользователь может также [использовать адаптер USB-C/Ethernet](hololens-connect-devices.md#hololens-2-connect-usb-c-devices), чтобы напрямую подключиться к сети Wi-Fi для получения помощи в настройке устройства. После завершения настройки устройства пользователь может продолжать использовать адаптер или отключить его от устройства и [подключиться к сети Wi-Fi](hololens-network.md#connecting-to-wi-fi-after-setup). 

## Подключение к сети Wi-Fi после настройки

1. Выполните **жест "Пуск"**, а затем выберите **Параметры**. Приложение "Параметры" будет автоматически размещено перед вами.
1. Выберите пункты **Сеть и Интернет** > **Wi-Fi**. Убедитесь, что функция Wi-Fi включена. Если вы не видите сеть, прокрутите список вниз.
1. Выберите сеть и нажмите **Подключение**.
1. В ответ на соответствующий запрос введите сетевой пароль и нажмите кнопку **Далее.**

HoloLens содержит радио Wi-Fi с поддержкой стандарта 802.11 ac 2x2. Подключение HoloLens к сети Wi-Fi происходит так же, как подключение к сети Wi-Fi настольного или мобильного устройства с Windows 10.

![Параметрами Wi-Fi HoloLens.](./images/wifi-hololens-600px.jpg)

Вы также можете убедиться, что вы подключены к сети Wi-Fi, проверив состояние Wi-Fi в **меню "Пуск"**.

1. Откройте меню **Пуск**.
1. Проверьте состояние сети Wi-Fi в верхнем левом углу меню **Пуск**. Будет отображено состояние Wi-Fi и SSID подключенной сети.

## Устранение неполадок с подключением к Wi-Fi

Если у вас возникают проблемы с подключением к Wi-Fi, см. раздел [Не удается подключиться к Wi-Fi](./hololens-faq.md#i-cant-connect-to-wi-fi).

Когда выполняется вход в учетную запись предприятия или организации на устройстве, также может применяться политика управления мобильными устройствами (MDM), если она настроена ИТ-администратором.

## Подключение HoloLens к сети Wi-Fi предприятия

В корпоративных Wi-Fi профилях для проверки подлинности подключений по Wi-Fi используется протокол расширенной проверки подлинности (EAP). Корпоративный профиль HoloLens для Wi-Fi можно настроить с помощью пакета MDM или пакета подготовки, созданного с помощью [конструктора конфигураций Windows](https://docs.microsoft.com/windows/configuration/provisioning-packages/provisioning-packages).

Инструкции по настройке устройства, управляемого с помощью службы Microsoft Intune, приведены в разделе [Intune](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-windows#enterprise-profile).

Чтобы создать пакет подготовки Wi-Fi в конструкторе конфигураций Windows, необходимо наличие файла предварительно настроенного профиля Wi-Fi в формате XML. Ниже приведен пример профиля Wi-Fi для WPA2-Enterprise с проверкой подлинности EAP-TLS.

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


Сертификат корневого ЦС сервера и сертификат клиента в зависимости от типа EAP, возможно, придется подготовить на устройстве.

Дополнительные ресурсы:

- Схема WLANv1Profile: [[MS-GPWL]: Схема профиля беспроводной локальной сети v1 | Документация Майкрософт](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/34054c93-cfcd-44df-89d8-5f2ba7532b67)
- Схема EAP-TLS: [[MS-GPWL]: Схема протокола EAP TLS корпорации Майкрософт | Документация Майкрософт](https://docs.microsoft.com/openspecs/windows_protocols/ms-gpwl/9590925c-cba2-4ac5-b9a1-1e5292bb72cb)

### Устранение неполадок EAP

1. Необходимо внимательно проверить следующие настройки профиля Wi-Fi.
   1. Правильная настройка типа EAP, распространенные типы EAP: EAP-TLS (13), EAP-TTLS (21) и PEAP (25).
   1. Правильность идентификатора SSID Wi-Fi и его совпадение с шестнадцатеричной строкой.
   1. Наличие для EAP-TLS в TrustedRootCA хэша SHA-1 сертификата доверенного корневого центра сертификации сервера. На компьютере с Windows строку хэша SHA-1 сертификата можно увидеть с помощью команды &quot;certutil.exe -dump cert\_file\_name&quot;.
1. Чтобы узнать, в каких случаях происходит сбой сеанса EAP, запишите сетевые пакеты в журнале точки доступа, контроллера или сервера AAA.
   1. Если удостоверение EAP, предоставленное службой HoloLens, не соответствует ожидаемому, проверьте правильность удостоверения, предоставленного с помощью профиля Wi-Fi или клиентского сертификата.
   1. Если сервер отклонил сертификат клиента HoloLens, убедитесь, что на устройстве был установлен требуемый сертификат клиента.
   1. Если HoloLens отклонил сертификат сервера, убедитесь, что сертификат корневого ЦС сервера был установлен на HoloLens.
1. Если профиль предприятия предоставлен с помощью пакета подготовки Wi-Fi, рассмотрите возможность установки пакета подготовки на компьютер с Windows 10. Если на компьютере с Windows 10 он также не работает, следуйте [инструкциям по устранению неполадок с проверкой подлинности клиента Windows 802.1 x](https://docs.microsoft.com/windows/client-management/advanced-troubleshooting-802-authentication).
1. Отправьте нам отзыв через [Центр отзывов](https://docs.microsoft.com/hololens/hololens-feedback).

### Дополнительные ресурсы:
- [Экспорт параметров Wi-Fi с устройства с Windows](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-import-windows-8-1#export-wi-fi-settings-from-a-windows-device)

## VPN
Подключение к сети VPN позволяет обеспечить более безопасное подключение и доступ к сети организации и Интернету. HoloLens 2 поддерживает встроенный подключаемый модуль VPN-клиента и универсальной платформы Windows (UWP). 

Поддерживаемые встроенные протоколы VPN:
- IKEv2
- L2TP
- PPTP

Если для проверки подлинности для встроенного VPN-клиента используется сертификат, то необходимый сертификат клиента следует добавить в хранилище сертификатов пользователя. Если подключаемый модуль VPN стороннего производителя поддерживает HoloLens 2, то перейдите в Хранилище, чтобы найти приложение VPN, и проверьте, содержится ли HoloLens в списке поддерживаемых устройств, а на странице требований к системе убедитесь, что приложение поддерживает архитектуру ARM или ARM64. HoloLens поддерживает только приложения универсальной платформы Windows для сторонних сетей VPN.

 VPN можно управлять с помощью MDM в пункте [Параметры/Разрешить VPN](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn) и настраивать с помощью [политики Vpnv2-csp](https://docs.microsoft.com/windows/client-management/mdm/vpnv2-csp).

Дополнительные сведения о [процедуре настройки VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) можно получить из [этих руководств](https://docs.microsoft.com/windows/security/identity-protection/vpn/vpn-guide).  

### Настройка VPN с помощью пользовательского интерфейса

По умолчанию сеть VPN отключена, но ее можно включить вручную, открыв приложение **Параметры** и перейдя к пункту **Сеть и Интернет > VPN**.
1. Выберите поставщика услуг VPN.
1. Придумайте название подключения. 
1. Введите имя или адрес сервера.
1. Выберите тип VPN.
1. Выберите тип сведений для входа. 
1. При необходимости добавьте имя пользователя и пароль.
1. Примените параметры VPN. 

![Параметры VPN для HoloLens](./images/vpn-settings-ui.jpg)

### Настройка VPN с помощью пакета подготовки

> [!TIP] 
> В Windows Holographic версии 20H2 мы устранили проблему с конфигурацией прокси-сервера для подключения VPN. Если вы планируете использовать этот поток, попробуйте обновить устройства до этой сборки.

1. Запустите конструктор конфигураций Windows.
1. Щелкните **Подготовить устройства HoloLens**, затем выберите целевое устройство и нажмите кнопку **Далее**.
1. Введите имя пакета и путь к нему.
1. Нажмите кнопку **Переключиться в расширенный редактор**.
1. Откройте **Параметры среды выполнения** -> **ConnectivityProfiles** -> **VPN-** -> **VPNSettings**.
1. Настройка параметра VPNProfileName
1. Выберите ProfileType: **Встроенный** или **Стороннего производителя**.
    1. Для встроенного профиля выберите **NativeProtocolType**, затем настройте сервер, политику маршрутизации, тип проверки подлинности и другие параметры.
    1. Для профиля стороннего производителя настройте URL-адрес сервера, имя семейства пакетов подключаемого модуля приложения VPN (только три имени предварительно заданы) и настраиваемые конфигурации.
1. Экспортируйте пакет.
1. Подключите HoloLens и скопируйте файл .ppkg на устройство. 
1. Примените файл .ppkg VPN на HoloLens, открыв меню "Пуск" и выбрав **Параметры** -> **Учетная запись** -> **Рабочий или учебный доступ** -> **Добавление или удаление пакета подготовки** -> Выбор пакета VPN.


### Настройка VPN с помощью Intune
Чтобы приступить к работе, просто следуйте документации Intune. При выполнении этих действий следует учитывать встроенные протоколы VPN, поддерживаемые устройствами HoloLens. 

[Создание профилей VPN для подключения к серверам VPN в Intune](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-configure).

[Параметры устройства Windows 10 и Windows Holographic для добавления подключений VPN с помощью Intune](https://docs.microsoft.com/mem/intune/configuration/vpn-settings-windows-10).

После завершения настройки не забудьте [назначить профиль](https://docs.microsoft.com/mem/intune/configuration/device-profile-assign).

### Настройка VPN с помощью решений MDM сторонних производителей.
Пример подключения VPN стороннего производителя.
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

Пример встроенного VPN с использованием протокола IKEv2.
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
## Отключение Wi-Fi на HoloLens (1 поколение)

### С помощью приложения "Параметры" на HoloLens

1. Откройте меню **Пуск**.
1. Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**. Приложение **Параметры** будет автоматически размещено перед вами.
1. Выберите пункт **Сеть и Интернет**.
1. Выберите переключатель "Wi-Fi", чтобы переместить его в положение **Выкл.**. Это приведет к отключению радиочастотных компонентов радиомодуля Wi-Fi и отключению всех функций Wi-Fi на HoloLens.

    > [!WARNING]
    > Если радио Wi-Fi отключено, HoloLens не сможет автоматически загружать ваши [пространства](hololens-spaces.md).

1. Переведите переключатель в положение **Вкл.**, чтобы включить радио Wi-Fi и восстановить функции Wi-Fi на Microsoft HoloLens. Выбранное состояние радио Wi-Fi (**Включено** или **Выключено**) будет сохранено при перезагрузке.

## Определение IP-адреса HoloLens в сети Wi-Fi.

### С помощью приложения "Параметры"

1. Откройте меню **Пуск**.
1. Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**. Приложение **Параметры** будет автоматически размещено перед вами.
1. Выберите пункт **Сеть и Интернет**.
1. Прокрутите список доступных сетей Wi-Fi вниз до пункта **Свойства оборудования**.

    ![Свойства оборудования в параметрах Wi-Fi](./images/wifi-hololens-hwdetails.jpg)

   IP-адрес будет указан рядом с пунктом **IPv4-адрес**.

### С использованием голосовых команд

В зависимости от сборки вашего устройства на некоторых устройствах можно использовать встроенные голосовые команды или Кортану для отображения вашего IP-адреса. В сборках версий после [19041,1103](hololens-release-notes.md#windows-holographic-version-2004) произнесите "What's my IP address?" (Какой у меня IP адрес?) и он будет отображаться. Для более ранних сборок или HoloLens (1-ого поколения) произнесите "Hey Cortana, What's my IP address?" (Привет, Кортана! Какой у меня IP-адрес?). Кортана отобразит и прочитает ваш IP-адрес.

### С помощью портала устройств Windows

1. Откройте [портал устройств](/windows/mixed-reality/using-the-windows-device-portal.md#networking) в веб-браузере на компьютере.
1. Перейдите в раздел **Сети**.  
   В этом разделе отображается ваш IP-адрес и другая информация о сети. С помощью этого метода можно скопировать и вставить IP-адрес на компьютер для разработки.
