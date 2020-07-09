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
ms.openlocfilehash: 734176dcf8a789f130aa8b010f5f3c9ec1d22c72
ms.sourcegitcommit: 29755f5af0086a43c532fb5a9a4ae65c36bc82de
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2020
ms.locfileid: "10857797"
---
# <span data-ttu-id="5d983-104">Подключение HoloLens к сети</span><span class="sxs-lookup"><span data-stu-id="5d983-104">Connect HoloLens to a network</span></span>

<span data-ttu-id="5d983-105">Для выполнения большинства задач на устройстве HoloLens устройство должно быть подключено к сети.</span><span class="sxs-lookup"><span data-stu-id="5d983-105">To do most things on your HoloLens, you have to be connected to a network.</span></span> <span data-ttu-id="5d983-106">Это руководство поможет вам:</span><span class="sxs-lookup"><span data-stu-id="5d983-106">This guide will help you:</span></span>

- <span data-ttu-id="5d983-107">Подключиться к сети с помощью Wi-Fi или (только для HoloLens 2) Ethernet через USB-C</span><span class="sxs-lookup"><span data-stu-id="5d983-107">Connect to a network using Wi-Fi or (for HoloLens 2 only) Ethernet over USB-C</span></span>
- <span data-ttu-id="5d983-108">Отключить и повторно включить Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="5d983-108">Disable and re-enable Wi-Fi</span></span>

<span data-ttu-id="5d983-109">Подробнее об [использовании HoloLens в автономном режиме](hololens-offline.md).</span><span class="sxs-lookup"><span data-stu-id="5d983-109">Read more about [using HoloLens offline](hololens-offline.md).</span></span>

## <span data-ttu-id="5d983-110">Первое подключение</span><span class="sxs-lookup"><span data-stu-id="5d983-110">Connecting for the first time</span></span>

<span data-ttu-id="5d983-111">При первом использовании HoloLens вам будет предложено пройти процедуру подключения к сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="5d983-111">The first time you use your HoloLens, you'll be guided through connecting to a Wi-Fi network.</span></span> <span data-ttu-id="5d983-112">При наличии проблем с подключением к сети Wi-Fi во время настройки проверьте, открыта ли ваша сеть или она защищена паролем и имеет ли она портал авторизации.</span><span class="sxs-lookup"><span data-stu-id="5d983-112">If you have trouble connecting to Wi-Fi during setup, make sure that your network is either an open, password-protected network or a captive portal network.</span></span> <span data-ttu-id="5d983-113">Убедитесь, что для подключения к сети не требуется использование сертификата.</span><span class="sxs-lookup"><span data-stu-id="5d983-113">Make sure that the network doesn't require you to use a certificate to connect.</span></span> <span data-ttu-id="5d983-114">После завершения настройки можно будет подключаться к другим типам сетей Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="5d983-114">After setup, you can connect to other types of Wi-Fi networks.</span></span>

## <span data-ttu-id="5d983-115">Подключение к сети Wi-Fi после настройки</span><span class="sxs-lookup"><span data-stu-id="5d983-115">Connecting to Wi-Fi after setup</span></span>

1. <span data-ttu-id="5d983-116">Выберите **Пуск** > **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="5d983-116">Select **Start** > **Settings**.</span></span>
   - <span data-ttu-id="5d983-117">*Только для HoloLens (1-е поколение)*. Взглядом найдите приложение "Параметры" и коснитесь его, чтобы разместить перед собой, или скажите "Place" ("Разместить").</span><span class="sxs-lookup"><span data-stu-id="5d983-117">*HoloLens (1st gen) only*: Use your gaze to position the Settings app, then air tap to place it, or say "Place."</span></span>
1. <span data-ttu-id="5d983-118">Выберите пункты **Сеть и Интернет** > **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="5d983-118">Select **Network & Internet** > **Wi-Fi**.</span></span> <span data-ttu-id="5d983-119">Если вы не видите сеть, прокрутите список вниз.</span><span class="sxs-lookup"><span data-stu-id="5d983-119">If you don't see your network, scroll down the list.</span></span>
1. <span data-ttu-id="5d983-120">Выберите сеть и нажмите **Подключение**.</span><span class="sxs-lookup"><span data-stu-id="5d983-120">Select a network, then select **Connect**.</span></span>
1. <span data-ttu-id="5d983-121">В ответ на соответствующий запрос введите сетевой пароль и нажмите кнопку **Далее.**</span><span class="sxs-lookup"><span data-stu-id="5d983-121">If you are prompted for a network password type it and then select **Next**.</span></span>

## <span data-ttu-id="5d983-122">Подключение к сети Wi-Fi на HoloLens (1-е поколение)</span><span class="sxs-lookup"><span data-stu-id="5d983-122">Connecting to Wi-Fi on HoloLens (1st gen)</span></span>

<span data-ttu-id="5d983-123">HoloLens содержит радио Wi-Fi с поддержкой стандарта 802.11 ac 2x2.</span><span class="sxs-lookup"><span data-stu-id="5d983-123">HoloLens contains a 802.11ac-capable, 2x2 Wi-Fi radio.</span></span> <span data-ttu-id="5d983-124">Подключение HoloLens к сети Wi-Fi происходит так же, как подключение к сети Wi-Fi настольного или мобильного устройства с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5d983-124">Connecting HoloLens to a Wi-Fi network is similar to connecting a Windows 10 Desktop or Mobile device to a Wi-Fi network.</span></span>

![Параметрами Wi-Fi HoloLens.](./images/wifi-hololens-600px.jpg)

1. <span data-ttu-id="5d983-126">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="5d983-126">Open the **Start** menu.</span></span>
1. <span data-ttu-id="5d983-127">Выберите приложение "Параметры" из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="5d983-127">Select the Settings app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="5d983-128">Приложение "Параметры" будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="5d983-128">The Settings app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="5d983-129">Выберите пункт **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="5d983-129">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="5d983-130">Убедитесь, что функция Wi-Fi включена.</span><span class="sxs-lookup"><span data-stu-id="5d983-130">Make sure Wi-Fi is turned on.</span></span>
1. <span data-ttu-id="5d983-131">Выберите сеть Wi-Fi из списка.</span><span class="sxs-lookup"><span data-stu-id="5d983-131">Select a Wi-Fi network from the list.</span></span>
1. <span data-ttu-id="5d983-132">При необходимости введите пароль сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="5d983-132">If needed, type in the Wi-Fi network password.</span></span>

<span data-ttu-id="5d983-133">Вы также можете убедиться, что вы подключены к сети Wi-Fi, проверив состояние Wi-Fi в **меню "Пуск"**.</span><span class="sxs-lookup"><span data-stu-id="5d983-133">You can also confirm you are connected to a Wi-Fi network by checking the Wi-Fi status in the **Start** menu:</span></span>

1. <span data-ttu-id="5d983-134">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="5d983-134">Open the **Start** menu.</span></span>
1. <span data-ttu-id="5d983-135">Проверьте состояние сети Wi-Fi в верхнем левом углу меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="5d983-135">Look at the top left of the **Start** menu for Wi-Fi status.</span></span> <span data-ttu-id="5d983-136">Будет отображено состояние Wi-Fi и SSID подключенной сети.</span><span class="sxs-lookup"><span data-stu-id="5d983-136">The state of Wi-Fi and the SSID of the connected network will be shown.</span></span>

## <span data-ttu-id="5d983-137">Устранение неполадок с подключением к Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="5d983-137">Troubleshooting your connection to Wi-Fi</span></span>

<span data-ttu-id="5d983-138">Если у вас возникают проблемы с подключением к Wi-Fi, см. раздел [Не удается подключиться к Wi-Fi](./hololens-faq.md#i-cant-connect-to-wi-fi).</span><span class="sxs-lookup"><span data-stu-id="5d983-138">If you experience problems connecting to Wi-Fi, see [I can't connect to Wi-Fi](./hololens-faq.md#i-cant-connect-to-wi-fi).</span></span>

<span data-ttu-id="5d983-139">Когда выполняется вход в учетную запись предприятия или организации на устройстве, также может применяться политика управления мобильными устройствами (MDM), если она настроена ИТ-администратором.</span><span class="sxs-lookup"><span data-stu-id="5d983-139">When you sign into an enterprise or organizational account on the device, it may also apply Mobile Device Management (MDM) policy, if the policy is configured by your IT administrator.</span></span>

## <span data-ttu-id="5d983-140">Отключение сети Wi-Fi на HoloLens (1-е поколение)</span><span class="sxs-lookup"><span data-stu-id="5d983-140">Disabling Wi-Fi on HoloLens (1st gen)</span></span>

### <span data-ttu-id="5d983-141">С помощью приложения "Параметры" на HoloLens</span><span class="sxs-lookup"><span data-stu-id="5d983-141">Using the Settings app on HoloLens</span></span>

1. <span data-ttu-id="5d983-142">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="5d983-142">Open the **Start** menu.</span></span>
1. <span data-ttu-id="5d983-143">Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="5d983-143">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="5d983-144">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="5d983-144">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="5d983-145">Выберите пункт **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="5d983-145">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="5d983-146">Выберите переключатель "Wi-Fi", чтобы переместить его в положение **Выкл.**.</span><span class="sxs-lookup"><span data-stu-id="5d983-146">Select the Wi-Fi slider switch to move it to the **Off** position.</span></span> <span data-ttu-id="5d983-147">Это приведет к отключению радиочастотных компонентов радиомодуля Wi-Fi и отключению всех функций Wi-Fi на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5d983-147">This will turn off the RF components of the Wi-Fi radio and disable all Wi-Fi functionality on HoloLens.</span></span>

    > [!WARNING]
    > <span data-ttu-id="5d983-148">Если радио Wi-Fi отключено, HoloLens не сможет автоматически загружать ваши [пространства](hololens-spaces.md).</span><span class="sxs-lookup"><span data-stu-id="5d983-148">When the Wi-Fi radio is disabled, HoloLens will not be able to automatically load your [spaces](hololens-spaces.md).</span></span>

1. <span data-ttu-id="5d983-149">Переведите переключатель в положение **Вкл.**, чтобы включить радио Wi-Fi и восстановить функции Wi-Fi на Microsoft HoloLens.</span><span class="sxs-lookup"><span data-stu-id="5d983-149">Move the slider switch to the **On** position to turn on the Wi-Fi radio and restore Wi-Fi functionality on Microsoft HoloLens.</span></span> <span data-ttu-id="5d983-150">Выбранное состояние радио Wi-Fi (**Включено** или **Выключено**) будет сохранено при перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="5d983-150">The selected Wi-Fi radio state (**On** or **Off**) will persist across reboots.</span></span>

## <span data-ttu-id="5d983-151">Определение IP-адреса HoloLens в сети Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="5d983-151">Identifying the IP Address of your HoloLens on the Wi-Fi network</span></span>

### <span data-ttu-id="5d983-152">С помощью приложения "Параметры"</span><span class="sxs-lookup"><span data-stu-id="5d983-152">By using the Settings app</span></span>

1. <span data-ttu-id="5d983-153">Откройте меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="5d983-153">Open the **Start** menu.</span></span>
1. <span data-ttu-id="5d983-154">Выберите приложение **Параметры** из меню **Пуск** или из списка **Все приложения** в правой части меню **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="5d983-154">Select the **Settings** app from **Start** or from the **All Apps** list on the right of the **Start** menu.</span></span> <span data-ttu-id="5d983-155">Приложение **Параметры** будет автоматически размещено перед вами.</span><span class="sxs-lookup"><span data-stu-id="5d983-155">The **Settings** app will be auto-placed in front of you.</span></span>
1. <span data-ttu-id="5d983-156">Выберите пункт **Сеть и Интернет**.</span><span class="sxs-lookup"><span data-stu-id="5d983-156">Select **Network & Internet**.</span></span>
1. <span data-ttu-id="5d983-157">Прокрутите список доступных сетей Wi-Fi вниз до пункта **Свойства оборудования**.</span><span class="sxs-lookup"><span data-stu-id="5d983-157">Scroll down to beneath the list of available Wi-Fi networks and select **Hardware properties**.</span></span>

    ![Свойства оборудования в параметрах Wi-Fi](./images/wifi-hololens-hwdetails.jpg)

   <span data-ttu-id="5d983-159">IP-адрес будет указан рядом с пунктом **IPv4-адрес**.</span><span class="sxs-lookup"><span data-stu-id="5d983-159">The IP address appears next to **IPv4 address**.</span></span>

### <span data-ttu-id="5d983-160">С помощью Кортаны</span><span class="sxs-lookup"><span data-stu-id="5d983-160">By using Cortana</span></span>

<span data-ttu-id="5d983-161">Скажите "Hey Cortana, What's my IP address?" ("Привет, Кортана! Какой у меня IP-адрес?").</span><span class="sxs-lookup"><span data-stu-id="5d983-161">Say "Hey Cortana, What's my IP address?"</span></span> <span data-ttu-id="5d983-162">Кортана отобразит и прочитает ваш IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5d983-162">and Cortana will display and read out your IP address.</span></span>

### <span data-ttu-id="5d983-163">С помощью портала устройств Windows</span><span class="sxs-lookup"><span data-stu-id="5d983-163">By using Windows Device Portal</span></span>

1. <span data-ttu-id="5d983-164">Откройте [портал устройств](/windows/mixed-reality/using-the-windows-device-portal.md#networking) в веб-браузере на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5d983-164">In a web browser on your PC, open the [device portal](/windows/mixed-reality/using-the-windows-device-portal.md#networking).</span></span>
1. <span data-ttu-id="5d983-165">Перейдите в раздел **Сети**.</span><span class="sxs-lookup"><span data-stu-id="5d983-165">Navigate to the **Networking** section.</span></span>  
   <span data-ttu-id="5d983-166">В этом разделе отображается ваш IP-адрес и другая информация о сети.</span><span class="sxs-lookup"><span data-stu-id="5d983-166">This section displays your IP address and other network information.</span></span> <span data-ttu-id="5d983-167">С помощью этого метода можно скопировать и вставить IP-адрес на компьютер для разработки.</span><span class="sxs-lookup"><span data-stu-id="5d983-167">By using this method, you can copy and paste of the IP address on your development PC.</span></span>
