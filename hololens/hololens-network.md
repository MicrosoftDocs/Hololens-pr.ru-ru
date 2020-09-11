---
title: Подключение HoloLens к сети
description: Инструкции по подключению HoloLens к Интернету и определению IP-адреса устройства.
ms.assetid: 0895606e-96c0-491e-8b1c-52e56b00365d
author: mattzmsft
ms.author: mazeller
keywords: HoloLens, wifi, беспроводной, интернет, ip, ip-адрес
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: ''
manager: jarrettr
ms.openlocfilehash: 0db64ffb4113ff948651c708c28b91da535cb09b
ms.sourcegitcommit: 72ff3174b34d2acaf72547b7d981c66aef8fa82f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11009527"
---
# <span data-ttu-id="4484e-104">Подключение HoloLens к сети</span><span class="sxs-lookup"><span data-stu-id="4484e-104">Connect HoloLens to a network</span></span>

<span data-ttu-id="4484e-105">Для выполнения большинства задач на устройстве HoloLens устройство должно быть подключено к сети.</span><span class="sxs-lookup"><span data-stu-id="4484e-105">To do most things on your HoloLens, you have to be connected to a network.</span></span> <span data-ttu-id="4484e-106">Это руководство поможет вам:</span><span class="sxs-lookup"><span data-stu-id="4484e-106">This guide will help you:</span></span>

- <span data-ttu-id="4484e-107">Подключиться к сети с помощью Wi-Fi или (только для HoloLens 2) Ethernet через USB-C</span><span class="sxs-lookup"><span data-stu-id="4484e-107">Connect to a network using Wi-Fi or (for HoloLens 2 only) Ethernet over USB-C</span></span>
- <span data-ttu-id="4484e-108">Отключить и повторно включить Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="4484e-108">Disable and re-enable Wi-Fi</span></span>

<span data-ttu-id="4484e-109">Подробнее об [использовании HoloLens в автономном режиме](hololens-offline.md).</span><span class="sxs-lookup"><span data-stu-id="4484e-109">Read more about [using HoloLens offline](hololens-offline.md).</span></span>

## <span data-ttu-id="4484e-110">Первое подключение</span><span class="sxs-lookup"><span data-stu-id="4484e-110">Connecting for the first time</span></span>

<span data-ttu-id="4484e-111">При первом использовании HoloLens вам будет предложено пройти процедуру подключения к сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="4484e-111">The first time you use your HoloLens, you'll be guided through connecting to a Wi-Fi network.</span></span> <span data-ttu-id="4484e-112">При наличии проблем с подключением к сети Wi-Fi во время настройки проверьте, открыта ли ваша сеть или она защищена паролем и имеет ли она портал авторизации.</span><span class="sxs-lookup"><span data-stu-id="4484e-112">If you have trouble connecting to Wi-Fi during setup, make sure that your network is either an open, password-protected network or a captive portal network.</span></span> <span data-ttu-id="4484e-113">Убедитесь, что для подключения к сети не требуется использование сертификата.</span><span class="sxs-lookup"><span data-stu-id="4484e-113">Make sure that the network doesn't require you to use a certificate to connect.</span></span> <span data-ttu-id="4484e-114">После завершения настройки можно будет подключаться к другим типам сетей Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="4484e-114">After setup, you can connect to other types of Wi-Fi networks.</span></span>

<span data-ttu-id="4484e-115">На устройствах HoloLens 2 пользователь может также [использовать адаптер USB-C/Ethernet](hololens-connect-devices.md#hololens-2-connect-usb-c-devices), чтобы напрямую подключиться к сети Wi-Fi для получения помощи в настройке устройства.</span><span class="sxs-lookup"><span data-stu-id="4484e-115">On HoloLens 2 devices a user may also [use a USB-C to Ethernet adapter](hololens-connect-devices.md#hololens-2-connect-usb-c-devices) to connect directly to Wi-Fi to help assist in setting up the device.</span></span> <span data-ttu-id="4484e-116">После завершения настройки устройства пользователь может продолжать использовать адаптер или отключить его от устройства и [подключиться к сети Wi-Fi](hololens-network.md#connecting-to-wi-fi-after-setup).</span><span class="sxs-lookup"><span data-stu-id="4484e-116">Once the device has been set up a user may continue to user the adapter or they may disconnect the device from the adapter and [connect to wi-fi after set up](hololens-network.md#connecting-to-wi-fi-after-setup).</span></span> 

## <span data-ttu-id="4484e-117">Подключение к сети Wi-Fi после настройки</span><span class="sxs-lookup"><span data-stu-id="4484e-117">Connecting to Wi-Fi after setup</span></span>

1. <span data-ttu-id="4484e-118">Выполните **жест "Пуск"**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="4484e-118">Preform the **Start gesture** and select **Settings**.</span></span> <span data-ttu-id="4484e-119">Приложение "Параметры" будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="4484e-119">The Settings app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="4484e-120">Выберите пункты **Сеть и Интернет** > **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="4484e-120">Select **Network & Internet** > **Wi-Fi**.</span></span> <span data-ttu-id="4484e-121">Убедитесь, что функция Wi-Fi включена.</span><span class="sxs-lookup"><span data-stu-id="4484e-121">Make sure Wi-Fi is turned on.</span></span> <span data-ttu-id="4484e-122">Если вы не видите сеть, прокрутите список вниз.</span><span class="sxs-lookup"><span data-stu-id="4484e-122">If you don't see your network, scroll down the list.</span></span>
1. <span data-ttu-id="4484e-123">Выберите сеть и нажмите **Подключение**.</span><span class="sxs-lookup"><span data-stu-id="4484e-123">Select a network, then select **Connect**.</span></span>
1. <span data-ttu-id="4484e-124">В ответ на соответствующий запрос введите сетевой пароль и нажмите кнопку **Далее.**</span><span class="sxs-lookup"><span data-stu-id="4484e-124">If you are prompted for a network password type it and then select **Next**.</span></span>

<span data-ttu-id="4484e-125">HoloLens содержит радио Wi-Fi с поддержкой стандарта 802.11 ac 2x2.</span><span class="sxs-lookup"><span data-stu-id="4484e-125">HoloLens contains a 802.11ac-capable, 2x2 Wi-Fi radio.</span></span> <span data-ttu-id="4484e-126">Подключение HoloLens к сети Wi-Fi происходит так же, как подключение к сети Wi-Fi настольного или мобильного устройства с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4484e-126">Connecting HoloLens to a Wi-Fi network is similar to connecting a Windows 10 Desktop or Mobile device to a Wi-Fi network.</span></span>

![Параметрами Wi-Fi HoloLens.](./images/wifi-hololens-600px.jpg)

<span data-ttu-id="4484e-128">Вы также можете убедиться, что вы подключены к сети Wi-Fi, проверив состояние Wi-Fi в **меню "Пуск"**.</span><span class="sxs-lookup"><span data-stu-id="4484e-128">You can also confirm you are connected to a Wi-Fi network by checking the Wi-Fi status in the **Start** menu:</span></span>

1. <span data-ttu-id="4484e-129">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="4484e-129">Open the **Start** menu.</span></span>
1. <span data-ttu-id="4484e-130">Проверьте состояние сети Wi-Fi в верхнем левом углу меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="4484e-130">Look at the top left of the **Start** menu for Wi-Fi status.</span></span> <span data-ttu-id="4484e-131">Будет отображено состояние Wi-Fi и SSID подключенной сети.</span><span class="sxs-lookup"><span data-stu-id="4484e-131">The state of Wi-Fi and the SSID of the connected network will be shown.</span></span>

## <span data-ttu-id="4484e-132">Устранение неполадок с подключением к Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="4484e-132">Troubleshooting your connection to Wi-Fi</span></span>

<span data-ttu-id="4484e-133">Если у вас возникают проблемы с подключением к Wi-Fi, см. раздел [Не удается подключиться к Wi-Fi](./hololens-faq.md#i-cant-connect-to-wi-fi).</span><span class="sxs-lookup"><span data-stu-id="4484e-133">If you experience problems connecting to Wi-Fi, see [I can't connect to Wi-Fi](./hololens-faq.md#i-cant-connect-to-wi-fi).</span></span>

<span data-ttu-id="4484e-134">Когда выполняется вход в учетную запись предприятия или организации на устройстве, также может применяться политика управления мобильными устройствами (MDM), если она настроена ИТ-администратором.</span><span class="sxs-lookup"><span data-stu-id="4484e-134">When you sign into an enterprise or organizational account on the device, it may also apply Mobile Device Management (MDM) policy, if the policy is configured by your IT administrator.</span></span>

## <span data-ttu-id="4484e-135">VPN</span><span class="sxs-lookup"><span data-stu-id="4484e-135">VPN</span></span>
<span data-ttu-id="4484e-136">Подключение к сети VPN позволяет обеспечить более безопасное подключение и доступ к сети организации и Интернету.</span><span class="sxs-lookup"><span data-stu-id="4484e-136">A VPN connection can help provide a more secure connection and access to your company's network and the Internet.</span></span> <span data-ttu-id="4484e-137">HoloLens 2 поддерживает встроенный подключаемый модуль VPN-клиента и универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="4484e-137">HoloLens 2 supports built-in VPN client and Universal Windows Platform (UWP) VPN plug-in.</span></span> 

<span data-ttu-id="4484e-138">Поддерживаемые встроенные протоколы VPN:</span><span class="sxs-lookup"><span data-stu-id="4484e-138">Supported Built-in VPN protocols:</span></span>
- <span data-ttu-id="4484e-139">IKEv2</span><span class="sxs-lookup"><span data-stu-id="4484e-139">IKEv2</span></span>
- <span data-ttu-id="4484e-140">L2TP</span><span class="sxs-lookup"><span data-stu-id="4484e-140">L2TP</span></span>
- <span data-ttu-id="4484e-141">PPTP</span><span class="sxs-lookup"><span data-stu-id="4484e-141">PPTP</span></span>

<span data-ttu-id="4484e-142">Если для проверки подлинности для встроенного VPN-клиента используется сертификат, то необходимый сертификат клиента следует добавить в хранилище сертификатов пользователя.</span><span class="sxs-lookup"><span data-stu-id="4484e-142">If certificate is used for authentication for built-in VPN client, the required client certificate needs to be added to user certificate store.</span></span> <span data-ttu-id="4484e-143">Если подключаемый модуль VPN стороннего производителя поддерживает HoloLens 2, то перейдите в Хранилище, чтобы найти приложение VPN, и проверьте, содержится ли HoloLens в списке поддерживаемых устройств, а на странице требований к системе убедитесь, что приложение поддерживает архитектуру ARM или ARM64.</span><span class="sxs-lookup"><span data-stu-id="4484e-143">To find if a 3rd party VPN plug-in supports HoloLens 2, go to Store to locate VPN app and check if HoloLens is listed as a supported device and in the System Requirement page the app supports ARM or ARM64 architecture.</span></span> <span data-ttu-id="4484e-144">HoloLens поддерживает только приложения универсальной платформы Windows для сторонних сетей VPN.</span><span class="sxs-lookup"><span data-stu-id="4484e-144">HoloLens only supports Universal Windows Platform applications for 3rd party VPN.</span></span>

<span data-ttu-id="4484e-145">По умолчанию сеть VPN отключена, но ее можно включить вручную, открыв **Параметры** приложения и перейдя к пункту **Сеть и Интернет > VPN**.</span><span class="sxs-lookup"><span data-stu-id="4484e-145">VPN is not enabled by default but can be enabled manually by opening **Settings** app and navigating to  **Network & Internet -> VPN**.</span></span> <span data-ttu-id="4484e-146">VPN можно управлять с помощью MDM в пункте [Параметры/Разрешить VPN](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn)и настраивать с помощью политики [Vpnv2-csp](https://docs.microsoft.com/windows/client-management/mdm/vpnv2-csp).</span><span class="sxs-lookup"><span data-stu-id="4484e-146">VPN can be managed by MDM via [Settings/AllowVPN](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn), and set via  [Vpnv2-csp policy](https://docs.microsoft.com/windows/client-management/mdm/vpnv2-csp).</span></span>
<span data-ttu-id="4484e-147">Узнайте больше о [процедуре настройки VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) с помощью [этих руководств](https://docs.microsoft.com/windows/security/identity-protection/vpn/vpn-guide).</span><span class="sxs-lookup"><span data-stu-id="4484e-147">Learn more about [how to configure VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) with [these guides](https://docs.microsoft.com/windows/security/identity-protection/vpn/vpn-guide).</span></span>  

## <span data-ttu-id="4484e-148">Отключение сети Wi-Fi на HoloLens (1-е поколение)</span><span class="sxs-lookup"><span data-stu-id="4484e-148">Disabling Wi-Fi on HoloLens (1st gen)</span></span>

### <span data-ttu-id="4484e-149">С помощью приложения "Параметры" на HoloLens</span><span class="sxs-lookup"><span data-stu-id="4484e-149">Using the Settings app on HoloLens</span></span>

1. <span data-ttu-id="4484e-150">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="4484e-150">Open the **Start** menu.</span></span>
1. <span data-ttu-id="4484e-151">Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="4484e-151">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="4484e-152">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="4484e-152">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="4484e-153">Выберите пункт **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="4484e-153">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="4484e-154">Выберите переключатель "Wi-Fi", чтобы переместить его в положение **Выкл.**.</span><span class="sxs-lookup"><span data-stu-id="4484e-154">Select the Wi-Fi slider switch to move it to the **Off** position.</span></span> <span data-ttu-id="4484e-155">Это приведет к отключению радиочастотных компонентов радиомодуля Wi-Fi и отключению всех функций Wi-Fi на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4484e-155">This will turn off the RF components of the Wi-Fi radio and disable all Wi-Fi functionality on HoloLens.</span></span>

    > [!WARNING]
    > <span data-ttu-id="4484e-156">Если радио Wi-Fi отключено, HoloLens не сможет автоматически загружать ваши [пространства](hololens-spaces.md).</span><span class="sxs-lookup"><span data-stu-id="4484e-156">When the Wi-Fi radio is disabled, HoloLens will not be able to automatically load your [spaces](hololens-spaces.md).</span></span>

1. <span data-ttu-id="4484e-157">Переведите переключатель в положение **Вкл.**, чтобы включить радио Wi-Fi и восстановить функции Wi-Fi на Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="4484e-157">Move the slider switch to the **On** position to turn on the Wi-Fi radio and restore Wi-Fi functionality on Microsoft HoloLens.</span></span> <span data-ttu-id="4484e-158">Выбранное состояние радио Wi-Fi (**Включено** или **Выключено**) будет сохранено при перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="4484e-158">The selected Wi-Fi radio state (**On** or **Off**) will persist across reboots.</span></span>

## <span data-ttu-id="4484e-159">Определение IP-адреса HoloLens в сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="4484e-159">Identifying the IP Address of your HoloLens on the Wi-Fi network</span></span>

### <span data-ttu-id="4484e-160">С помощью приложения "Параметры"</span><span class="sxs-lookup"><span data-stu-id="4484e-160">By using the Settings app</span></span>

1. <span data-ttu-id="4484e-161">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="4484e-161">Open the **Start** menu.</span></span>
1. <span data-ttu-id="4484e-162">Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="4484e-162">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="4484e-163">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="4484e-163">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="4484e-164">Выберите пункт **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="4484e-164">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="4484e-165">Прокрутите список доступных сетей Wi-Fi вниз до пункта **Свойства оборудования**.</span><span class="sxs-lookup"><span data-stu-id="4484e-165">Scroll down to beneath the list of available Wi-Fi networks and select **Hardware properties**.</span></span>

    ![Свойства оборудования в параметрах Wi-Fi](./images/wifi-hololens-hwdetails.jpg)

   <span data-ttu-id="4484e-167">IP-адрес будет указан рядом с пунктом **IPv4-адрес**.</span><span class="sxs-lookup"><span data-stu-id="4484e-167">The IP address appears next to **IPv4 address**.</span></span>

### <span data-ttu-id="4484e-168">С использованием голосовых команд</span><span class="sxs-lookup"><span data-stu-id="4484e-168">By using voice commands</span></span>

<span data-ttu-id="4484e-169">В зависимости от сборки вашего устройства на некоторых устройствах можно использовать встроенные голосовые команды или Кортану для отображения вашего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="4484e-169">Depending on your devices build you can either use built in voice commands or Cortana to display your IP address.</span></span> <span data-ttu-id="4484e-170">В сборках версий после [19041,1103](hololens-release-notes.md#windows-holographic-version-2004) произнесите "What's my IP address?" (Какой у меня IP адрес?)</span><span class="sxs-lookup"><span data-stu-id="4484e-170">On builds after [19041.1103](hololens-release-notes.md#windows-holographic-version-2004) speak "What's my IP address?"</span></span> <span data-ttu-id="4484e-171">и он будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="4484e-171">and it will be displayed.</span></span> <span data-ttu-id="4484e-172">Для более ранних сборок или HoloLens (1-ого поколения) произнесите "Hey Cortana, What's my IP address?" (Привет, Кортана! Какой у меня IP-адрес?).</span><span class="sxs-lookup"><span data-stu-id="4484e-172">For earlier builds or HoloLens (1st gen) say "Hey Cortana, What's my IP address?"</span></span> <span data-ttu-id="4484e-173">Кортана отобразит и прочитает ваш IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="4484e-173">and Cortana will display and read out your IP address.</span></span>

### <span data-ttu-id="4484e-174">С помощью портала устройств Windows</span><span class="sxs-lookup"><span data-stu-id="4484e-174">By using Windows Device Portal</span></span>

1. <span data-ttu-id="4484e-175">Откройте [портал устройств](/windows/mixed-reality/using-the-windows-device-portal.md#networking) в веб-браузере на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4484e-175">In a web browser on your PC, open the [device portal](/windows/mixed-reality/using-the-windows-device-portal.md#networking).</span></span>
1. <span data-ttu-id="4484e-176">Перейдите в раздел **Сети**.</span><span class="sxs-lookup"><span data-stu-id="4484e-176">Navigate to the **Networking** section.</span></span>  
   <span data-ttu-id="4484e-177">В этом разделе отображается ваш IP-адрес и другая информация о сети.</span><span class="sxs-lookup"><span data-stu-id="4484e-177">This section displays your IP address and other network information.</span></span> <span data-ttu-id="4484e-178">С помощью этого метода можно скопировать и вставить IP-адрес на компьютер для разработки.</span><span class="sxs-lookup"><span data-stu-id="4484e-178">By using this method, you can copy and paste of the IP address on your development PC.</span></span>
