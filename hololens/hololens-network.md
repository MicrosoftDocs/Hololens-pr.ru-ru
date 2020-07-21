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
ms.openlocfilehash: 0f46ff4a1bef95d153d9fa93c746c8977dc49771
ms.sourcegitcommit: 47bc3b696936dd7011b3f9dd683deb872ed25b90
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "10883153"
---
# <span data-ttu-id="3421e-104">Подключение HoloLens к сети</span><span class="sxs-lookup"><span data-stu-id="3421e-104">Connect HoloLens to a network</span></span>

<span data-ttu-id="3421e-105">Для выполнения большинства задач на устройстве HoloLens устройство должно быть подключено к сети.</span><span class="sxs-lookup"><span data-stu-id="3421e-105">To do most things on your HoloLens, you have to be connected to a network.</span></span> <span data-ttu-id="3421e-106">Это руководство поможет вам:</span><span class="sxs-lookup"><span data-stu-id="3421e-106">This guide will help you:</span></span>

- <span data-ttu-id="3421e-107">Подключиться к сети с помощью Wi-Fi или (только для HoloLens 2) Ethernet через USB-C</span><span class="sxs-lookup"><span data-stu-id="3421e-107">Connect to a network using Wi-Fi or (for HoloLens 2 only) Ethernet over USB-C</span></span>
- <span data-ttu-id="3421e-108">Отключить и повторно включить Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="3421e-108">Disable and re-enable Wi-Fi</span></span>

<span data-ttu-id="3421e-109">Подробнее об [использовании HoloLens в автономном режиме](hololens-offline.md).</span><span class="sxs-lookup"><span data-stu-id="3421e-109">Read more about [using HoloLens offline](hololens-offline.md).</span></span>

## <span data-ttu-id="3421e-110">Первое подключение</span><span class="sxs-lookup"><span data-stu-id="3421e-110">Connecting for the first time</span></span>

<span data-ttu-id="3421e-111">При первом использовании HoloLens вам будет предложено пройти процедуру подключения к сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="3421e-111">The first time you use your HoloLens, you'll be guided through connecting to a Wi-Fi network.</span></span> <span data-ttu-id="3421e-112">При наличии проблем с подключением к сети Wi-Fi во время настройки проверьте, открыта ли ваша сеть или она защищена паролем и имеет ли она портал авторизации.</span><span class="sxs-lookup"><span data-stu-id="3421e-112">If you have trouble connecting to Wi-Fi during setup, make sure that your network is either an open, password-protected network or a captive portal network.</span></span> <span data-ttu-id="3421e-113">Убедитесь, что для подключения к сети не требуется использование сертификата.</span><span class="sxs-lookup"><span data-stu-id="3421e-113">Make sure that the network doesn't require you to use a certificate to connect.</span></span> <span data-ttu-id="3421e-114">После завершения настройки можно будет подключаться к другим типам сетей Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="3421e-114">After setup, you can connect to other types of Wi-Fi networks.</span></span>

## <span data-ttu-id="3421e-115">Подключение к сети Wi-Fi после настройки</span><span class="sxs-lookup"><span data-stu-id="3421e-115">Connecting to Wi-Fi after setup</span></span>

1. <span data-ttu-id="3421e-116">Выполните **жест "Пуск"**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="3421e-116">Preform the **Start gesture** and select **Settings**.</span></span> <span data-ttu-id="3421e-117">Приложение "Параметры" будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="3421e-117">The Settings app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="3421e-118">Выберите пункты **Сеть и Интернет** > **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="3421e-118">Select **Network & Internet** > **Wi-Fi**.</span></span> <span data-ttu-id="3421e-119">Убедитесь, что функция Wi-Fi включена.</span><span class="sxs-lookup"><span data-stu-id="3421e-119">Make sure Wi-Fi is turned on.</span></span> <span data-ttu-id="3421e-120">Если вы не видите сеть, прокрутите список вниз.</span><span class="sxs-lookup"><span data-stu-id="3421e-120">If you don't see your network, scroll down the list.</span></span>
1. <span data-ttu-id="3421e-121">Выберите сеть и нажмите **Подключение**.</span><span class="sxs-lookup"><span data-stu-id="3421e-121">Select a network, then select **Connect**.</span></span>
1. <span data-ttu-id="3421e-122">В ответ на соответствующий запрос введите сетевой пароль и нажмите кнопку **Далее.**</span><span class="sxs-lookup"><span data-stu-id="3421e-122">If you are prompted for a network password type it and then select **Next**.</span></span>

<span data-ttu-id="3421e-123">HoloLens содержит радио Wi-Fi с поддержкой стандарта 802.11 ac 2x2.</span><span class="sxs-lookup"><span data-stu-id="3421e-123">HoloLens contains a 802.11ac-capable, 2x2 Wi-Fi radio.</span></span> <span data-ttu-id="3421e-124">Подключение HoloLens к сети Wi-Fi происходит так же, как подключение к сети Wi-Fi настольного или мобильного устройства с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="3421e-124">Connecting HoloLens to a Wi-Fi network is similar to connecting a Windows 10 Desktop or Mobile device to a Wi-Fi network.</span></span>

![Параметрами Wi-Fi HoloLens.](./images/wifi-hololens-600px.jpg)

<span data-ttu-id="3421e-126">Вы также можете убедиться, что вы подключены к сети Wi-Fi, проверив состояние Wi-Fi в **меню "Пуск"**.</span><span class="sxs-lookup"><span data-stu-id="3421e-126">You can also confirm you are connected to a Wi-Fi network by checking the Wi-Fi status in the **Start** menu:</span></span>

1. <span data-ttu-id="3421e-127">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="3421e-127">Open the **Start** menu.</span></span>
1. <span data-ttu-id="3421e-128">Проверьте состояние сети Wi-Fi в верхнем левом углу меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="3421e-128">Look at the top left of the **Start** menu for Wi-Fi status.</span></span> <span data-ttu-id="3421e-129">Будет отображено состояние Wi-Fi и SSID подключенной сети.</span><span class="sxs-lookup"><span data-stu-id="3421e-129">The state of Wi-Fi and the SSID of the connected network will be shown.</span></span>

## <span data-ttu-id="3421e-130">Устранение неполадок с подключением к Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="3421e-130">Troubleshooting your connection to Wi-Fi</span></span>

<span data-ttu-id="3421e-131">Если у вас возникают проблемы с подключением к Wi-Fi, см. раздел [Не удается подключиться к Wi-Fi](./hololens-faq.md#i-cant-connect-to-wi-fi).</span><span class="sxs-lookup"><span data-stu-id="3421e-131">If you experience problems connecting to Wi-Fi, see [I can't connect to Wi-Fi](./hololens-faq.md#i-cant-connect-to-wi-fi).</span></span>

<span data-ttu-id="3421e-132">Когда выполняется вход в учетную запись предприятия или организации на устройстве, также может применяться политика управления мобильными устройствами (MDM), если она настроена ИТ-администратором.</span><span class="sxs-lookup"><span data-stu-id="3421e-132">When you sign into an enterprise or organizational account on the device, it may also apply Mobile Device Management (MDM) policy, if the policy is configured by your IT administrator.</span></span>

## <span data-ttu-id="3421e-133">VPN</span><span class="sxs-lookup"><span data-stu-id="3421e-133">VPN</span></span>
<span data-ttu-id="3421e-134">Подключение к сети VPN позволяет обеспечить более безопасное подключение и доступ к сети организации и Интернету.</span><span class="sxs-lookup"><span data-stu-id="3421e-134">A VPN connection can help provide a more secure connection and access to your company's network and the Internet.</span></span> <span data-ttu-id="3421e-135">HoloLens 2 поддерживает встроенный подключаемый модуль VPN-клиента и универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="3421e-135">HoloLens 2 supports built-in VPN client and Universal Windows Platform (UWP) VPN plug-in.</span></span> 

<span data-ttu-id="3421e-136">Поддерживаемые встроенные протоколы VPN:</span><span class="sxs-lookup"><span data-stu-id="3421e-136">Supported Built-in VPN protocols:</span></span>
- <span data-ttu-id="3421e-137">IKEv2</span><span class="sxs-lookup"><span data-stu-id="3421e-137">IKEv2</span></span>
- <span data-ttu-id="3421e-138">L2TP</span><span class="sxs-lookup"><span data-stu-id="3421e-138">L2TP</span></span>
- <span data-ttu-id="3421e-139">PPTP</span><span class="sxs-lookup"><span data-stu-id="3421e-139">PPTP</span></span>

<span data-ttu-id="3421e-140">Если для проверки подлинности для встроенного VPN-клиента используется сертификат, то необходимый сертификат клиента следует добавить в хранилище сертификатов пользователя.</span><span class="sxs-lookup"><span data-stu-id="3421e-140">If certificate is used for authentication for built-in VPN client, the required client certificate needs to be added to user certificate store.</span></span> <span data-ttu-id="3421e-141">Если подключаемый модуль VPN стороннего производителя поддерживает HoloLens 2, то перейдите в Хранилище, чтобы найти приложение VPN, и проверьте, содержится ли HoloLens в списке поддерживаемых устройств, а на странице требований к системе убедитесь, что приложение поддерживает архитектуру ARM или ARM64.</span><span class="sxs-lookup"><span data-stu-id="3421e-141">To find if a 3rd party VPN plug-in supports HoloLens 2, go to Store to locate VPN app and check if HoloLens is listed as a supported device and in the System Requirement page the app supports ARM or ARM64 architecture.</span></span> <span data-ttu-id="3421e-142">HoloLens поддерживает только приложения универсальной платформы Windows для сторонних сетей VPN.</span><span class="sxs-lookup"><span data-stu-id="3421e-142">HoloLens only supports Universal Windows Platform applications for 3rd party VPN.</span></span>

<span data-ttu-id="3421e-143">По умолчанию сеть VPN отключена, но ее можно включить вручную, открыв **Параметры** приложения и перейдя к пункту **Сеть и Интернет > VPN**.</span><span class="sxs-lookup"><span data-stu-id="3421e-143">VPN is not enabled by default but can be enabled manually by opening **Settings** app and navigating to  **Network & Internet -> VPN**.</span></span> <span data-ttu-id="3421e-144">VPN можно управлять с помощью MDM в пункте [Параметры/Разрешить VPN](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn)и настраивать с помощью политики [Vpnv2-csp](https://docs.microsoft.com/windows/client-management/mdm/vpnv2-csp).</span><span class="sxs-lookup"><span data-stu-id="3421e-144">VPN can be managed by MDM via [Settings/AllowVPN](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-allowvpn), and set via  [Vpnv2-csp policy](https://docs.microsoft.com/windows/client-management/mdm/vpnv2-csp).</span></span>
<span data-ttu-id="3421e-145">Узнайте больше о [процедуре настройки VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) с помощью [этих руководств](https://docs.microsoft.com/windows/security/identity-protection/vpn/vpn-guide).</span><span class="sxs-lookup"><span data-stu-id="3421e-145">Learn more about [how to configure VPN](https://support.microsoft.com/help/20510/windows-10-connect-to-vpn) with [these guides](https://docs.microsoft.com/windows/security/identity-protection/vpn/vpn-guide).</span></span>  

## <span data-ttu-id="3421e-146">Отключение сети Wi-Fi на HoloLens (1-е поколение)</span><span class="sxs-lookup"><span data-stu-id="3421e-146">Disabling Wi-Fi on HoloLens (1st gen)</span></span>

### <span data-ttu-id="3421e-147">С помощью приложения "Параметры" на HoloLens</span><span class="sxs-lookup"><span data-stu-id="3421e-147">Using the Settings app on HoloLens</span></span>

1. <span data-ttu-id="3421e-148">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="3421e-148">Open the **Start** menu.</span></span>
1. <span data-ttu-id="3421e-149">Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="3421e-149">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="3421e-150">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="3421e-150">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="3421e-151">Выберите пункт **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="3421e-151">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="3421e-152">Выберите переключатель "Wi-Fi", чтобы переместить его в положение **Выкл.**.</span><span class="sxs-lookup"><span data-stu-id="3421e-152">Select the Wi-Fi slider switch to move it to the **Off** position.</span></span> <span data-ttu-id="3421e-153">Это приведет к отключению радиочастотных компонентов радиомодуля Wi-Fi и отключению всех функций Wi-Fi на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="3421e-153">This will turn off the RF components of the Wi-Fi radio and disable all Wi-Fi functionality on HoloLens.</span></span>

    > [!WARNING]
    > <span data-ttu-id="3421e-154">Если радио Wi-Fi отключено, HoloLens не сможет автоматически загружать ваши [пространства](hololens-spaces.md).</span><span class="sxs-lookup"><span data-stu-id="3421e-154">When the Wi-Fi radio is disabled, HoloLens will not be able to automatically load your [spaces](hololens-spaces.md).</span></span>

1. <span data-ttu-id="3421e-155">Переведите переключатель в положение **Вкл.**, чтобы включить радио Wi-Fi и восстановить функции Wi-Fi на Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="3421e-155">Move the slider switch to the **On** position to turn on the Wi-Fi radio and restore Wi-Fi functionality on Microsoft HoloLens.</span></span> <span data-ttu-id="3421e-156">Выбранное состояние радио Wi-Fi (**Включено** или **Выключено**) будет сохранено при перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="3421e-156">The selected Wi-Fi radio state (**On** or **Off**) will persist across reboots.</span></span>

## <span data-ttu-id="3421e-157">Определение IP-адреса HoloLens в сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="3421e-157">Identifying the IP Address of your HoloLens on the Wi-Fi network</span></span>

### <span data-ttu-id="3421e-158">С помощью приложения "Параметры"</span><span class="sxs-lookup"><span data-stu-id="3421e-158">By using the Settings app</span></span>

1. <span data-ttu-id="3421e-159">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="3421e-159">Open the **Start** menu.</span></span>
1. <span data-ttu-id="3421e-160">Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="3421e-160">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="3421e-161">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="3421e-161">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="3421e-162">Выберите пункт **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="3421e-162">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="3421e-163">Прокрутите список доступных сетей Wi-Fi вниз до пункта **Свойства оборудования**.</span><span class="sxs-lookup"><span data-stu-id="3421e-163">Scroll down to beneath the list of available Wi-Fi networks and select **Hardware properties**.</span></span>

    ![Свойства оборудования в параметрах Wi-Fi](./images/wifi-hololens-hwdetails.jpg)

   <span data-ttu-id="3421e-165">IP-адрес будет указан рядом с пунктом **IPv4-адрес**.</span><span class="sxs-lookup"><span data-stu-id="3421e-165">The IP address appears next to **IPv4 address**.</span></span>

### <span data-ttu-id="3421e-166">С использованием голосовых команд</span><span class="sxs-lookup"><span data-stu-id="3421e-166">By using voice commands</span></span>

<span data-ttu-id="3421e-167">В зависимости от сборки вашего устройства на некоторых устройствах можно использовать встроенные голосовые команды или Кортану для отображения вашего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3421e-167">Depending on your devices build you can either use built in voice commands or Cortana to display your IP address.</span></span> <span data-ttu-id="3421e-168">В сборках версий после [19041,1103](hololens-release-notes.md#windows-holographic-version-2004) произнесите "What's my IP address?" (Какой у меня IP адрес?)</span><span class="sxs-lookup"><span data-stu-id="3421e-168">On builds after [19041.1103](hololens-release-notes.md#windows-holographic-version-2004) speak "What's my IP address?"</span></span> <span data-ttu-id="3421e-169">и он будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="3421e-169">and it will be displayed.</span></span> <span data-ttu-id="3421e-170">Для более ранних сборок или HoloLens (1-ого поколения) произнесите "Hey Cortana, What's my IP address?" (Привет, Кортана! Какой у меня IP-адрес?).</span><span class="sxs-lookup"><span data-stu-id="3421e-170">For earlier builds or HoloLens (1st gen) say "Hey Cortana, What's my IP address?"</span></span> <span data-ttu-id="3421e-171">Кортана отобразит и прочитает ваш IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3421e-171">and Cortana will display and read out your IP address.</span></span>

### <span data-ttu-id="3421e-172">С помощью портала устройств Windows</span><span class="sxs-lookup"><span data-stu-id="3421e-172">By using Windows Device Portal</span></span>

1. <span data-ttu-id="3421e-173">Откройте [портал устройств](/windows/mixed-reality/using-the-windows-device-portal.md#networking) в веб-браузере на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3421e-173">In a web browser on your PC, open the [device portal](/windows/mixed-reality/using-the-windows-device-portal.md#networking).</span></span>
1. <span data-ttu-id="3421e-174">Перейдите в раздел **Сети**.</span><span class="sxs-lookup"><span data-stu-id="3421e-174">Navigate to the **Networking** section.</span></span>  
   <span data-ttu-id="3421e-175">В этом разделе отображается ваш IP-адрес и другая информация о сети.</span><span class="sxs-lookup"><span data-stu-id="3421e-175">This section displays your IP address and other network information.</span></span> <span data-ttu-id="3421e-176">С помощью этого метода можно скопировать и вставить IP-адрес на компьютер для разработки.</span><span class="sxs-lookup"><span data-stu-id="3421e-176">By using this method, you can copy and paste of the IP address on your development PC.</span></span>
