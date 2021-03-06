---
title: Корпоративная регистрация устройств HoloLens в среде Wi-Fi с ограниченным количеством MAC-адресов
description: Как настроить MAC-адрес для сети на устройствах HoloLens 2
ms.prod: hololens
ms.sitesec: library
author: evmill
ms.author: mata
ms.topic: article
ms.localizationpriority: high
ms.date: 10/01/2020
ms.reviewer: v-evmill
audience: ITPro
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: fe365248332f8e78b15ab362f169b84e48dfe594
ms.sourcegitcommit: 07ffe1bf2f45dcb2ba9d7fbe54b4773a0fb9d525
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "11393843"
---
# <a name="enterprise-enrollment-of-hololens-devices-in-mac-address-restricted-wi-fi-environment"></a><span data-ttu-id="369eb-103">Корпоративная регистрация устройств HoloLens в среде Wi-Fi с ограниченным количеством MAC-адресов</span><span class="sxs-lookup"><span data-stu-id="369eb-103">Enterprise Enrollment of HoloLens Devices in MAC address restricted Wi-Fi Environment</span></span>

<span data-ttu-id="369eb-104">В этом документе будет описан общий сценарий, который был определен в средах клиента, где Wi-Fi ограничен MAC-адресами, или где для подключения к беспроводным сетям требуются сертификаты.</span><span class="sxs-lookup"><span data-stu-id="369eb-104">This document will describe a common scenario we have identified within customer environments where the Wi-Fi is restricted by MAC addresses, or certificates are required to join Wireless networks.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="369eb-105">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="369eb-105">Example Scenario</span></span>

<span data-ttu-id="369eb-106">Многие клиенты в безопасных средах имеют ограничения на беспроводные или проводные сети, которые позволяют успешно подключаться только утвержденным устройствам (на основе MAC-адресов).</span><span class="sxs-lookup"><span data-stu-id="369eb-106">Many customers in secure environments have restrictions on their Wireless or wired networks which will only allow approved devices (based on MAC Addresses) to connect successfully.</span></span> <span data-ttu-id="369eb-107">Это может быть реализовано с помощью фильтрации MAC-адресов на точке беспроводного доступа или через DHCP-сервер.</span><span class="sxs-lookup"><span data-stu-id="369eb-107">This may be enforced through MAC Address filtering on a Wireless Access Point or through a DHCP server.</span></span> <span data-ttu-id="369eb-108">Кроме того, в некоторых беспроводных сетях можно использовать для защиты протокол PEAP, при котором для успешной проверки подлинности беспроводной сети необходимо применить сертификат к устройству.</span><span class="sxs-lookup"><span data-stu-id="369eb-108">Additionally, some Wireless networks can be protected with PEAP, which requires that a certificate be applied to the device prior to authenticating on the Wireless network.</span></span>

<span data-ttu-id="369eb-109">В этом сценарии при подключении устройств HoloLens к сети два ключевых требования могут привести к задержкам или потребовать ручного вмешательства.</span><span class="sxs-lookup"><span data-stu-id="369eb-109">In this scenario, two key requirements may introduce delays or require manual intervention when joining HoloLens devices to the network:</span></span>

- <span data-ttu-id="369eb-110">Сертификат Wireless PEAP должен быть применен к устройству до того, как устройство успешно подключится к беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="369eb-110">The Wireless PEAP certificate must be applied to the device prior to the device successfully joining the wireless network.</span></span>
- <span data-ttu-id="369eb-111">MAC-адрес адаптера Wi-Fi HoloLens должен быть зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="369eb-111">The MAC Address of the HoloLens Wi-Fi adaptor must be registered.</span></span>

<span data-ttu-id="369eb-112">Основные проблемы, связанные с приведенными выше требованиями:</span><span class="sxs-lookup"><span data-stu-id="369eb-112">The core challenges with the requirements above are:</span></span>

1. <span data-ttu-id="369eb-113">В настоящее время MAC-адрес можно определить только из приложения "Параметры" на устройстве или из Intune после успешной регистрации.</span><span class="sxs-lookup"><span data-stu-id="369eb-113">The MAC Address can currently only be identified from the Settings app on the device, or from Intune after a successful enrollment.</span></span>
2. <span data-ttu-id="369eb-114">Без MAC-адреса устройство не может присоединиться к сети Wi-Fi для начала регистрации.</span><span class="sxs-lookup"><span data-stu-id="369eb-114">Without the MAC address, the device cannot join the Wi-Fi Network to begin enrollment.</span></span>
3. <span data-ttu-id="369eb-115">Для решения этих задач вручную требуется, чтобы с устройством взаимодействовал технический специалист.</span><span class="sxs-lookup"><span data-stu-id="369eb-115">Manual workarounds to these challenges require a technician to interact with the device.</span></span>

## <a name="solutions"></a><span data-ttu-id="369eb-116">Решения</span><span class="sxs-lookup"><span data-stu-id="369eb-116">Solutions</span></span>

<span data-ttu-id="369eb-117">Существует множество способов улучшить эту ситуацию в зависимости от инфраструктуры, доступной в среде.</span><span class="sxs-lookup"><span data-stu-id="369eb-117">There are many ways to improve this situation, depending on the infrastructure available within the environment.</span></span>

| <span data-ttu-id="369eb-118">Решение</span><span class="sxs-lookup"><span data-stu-id="369eb-118">Solution</span></span> | <span data-ttu-id="369eb-119">Преимущества</span><span class="sxs-lookup"><span data-stu-id="369eb-119">Benefits</span></span> | <span data-ttu-id="369eb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="369eb-120">Requirements</span></span> |
| --- | --- | --- |
| <span data-ttu-id="369eb-121">Пакет подготовки с адаптером Ethernet</span><span class="sxs-lookup"><span data-stu-id="369eb-121">Provisioning Package with Ethernet Adaptor</span></span> | <span data-ttu-id="369eb-122">Улучшает возможности OOBE и обеспечивает более быстрый опыт работы с техническим специалистом.</span><span class="sxs-lookup"><span data-stu-id="369eb-122">Improves OOBE experience and allows for a quicker technician experience.</span></span> | <span data-ttu-id="369eb-123">Совместимый с HoloLens адаптер USB-C Hub + Ethernet. Для записи MAC-адресов и финализации OOBE по-прежнему потребуется взаимодействие технического специалиста с устройством.</span><span class="sxs-lookup"><span data-stu-id="369eb-123">HoloLens compatible USB-C Hub + Ethernet adaptor, and technician will still need to interact with the device for MAC capture and OOBE finalisation</span></span> |
| <span data-ttu-id="369eb-124">Автопилот с регистрацией в Intune через Ethernet</span><span class="sxs-lookup"><span data-stu-id="369eb-124">Autopilot with Intune Registration over Ethernet</span></span> | <span data-ttu-id="369eb-125">Это одношаговое подключение и регистрация устройства в клиентской среде.</span><span class="sxs-lookup"><span data-stu-id="369eb-125">This is a single step connection and registration of the device to the customer environment.</span></span> <span data-ttu-id="369eb-126">Запись MAC-адреса может быть завершена без взаимодействия с устройством</span><span class="sxs-lookup"><span data-stu-id="369eb-126">MAC capture can be completed without needing to interact with the device</span></span> | <span data-ttu-id="369eb-127">Включение Intune для клиента AAD и совместимого с HoloLens адаптера USB-C Ethernet</span><span class="sxs-lookup"><span data-stu-id="369eb-127">Intune enabled for the customer AAD tenant and a HoloLens compatible USB-C Ethernet adaptor</span></span> |
| <span data-ttu-id="369eb-128">Автоматизированная отчетность о MAC-адресах</span><span class="sxs-lookup"><span data-stu-id="369eb-128">Automated reporting of MAC Addresses</span></span> | <span data-ttu-id="369eb-129">Когда устройства зарегистрированы в клиенте Intune, сценарий может сообщить MAC-адрес техническому специалисту.</span><span class="sxs-lookup"><span data-stu-id="369eb-129">When devices are registered with the Intune tenant, a script can report the MAC address to the technician.</span></span> | <span data-ttu-id="369eb-130">Командлеты Intune PowerShell</span><span class="sxs-lookup"><span data-stu-id="369eb-130">Intune Powershell Commandlets</span></span> |

## <a name="provisioning-package-with-ethernet-adaptor"></a><span data-ttu-id="369eb-131">Пакет подготовки с адаптером Ethernet</span><span class="sxs-lookup"><span data-stu-id="369eb-131">Provisioning Package with Ethernet Adaptor</span></span>

> [!NOTE] 
> <span data-ttu-id="369eb-132">Если на проводную сеть также распространяются ограничения MAC, то MAC-адрес адаптера USB-C Hub + Ethernet также должен быть предварительно утвержден.</span><span class="sxs-lookup"><span data-stu-id="369eb-132">If the wired network is also subject to MAC restrictions, then the MAC address of the USB-C Hub + Ethernet adaptor will also need to be pre-approved.</span></span> <span data-ttu-id="369eb-133">Будьте внимательны при использовании этого адаптера, так как он позволяет получить доступ к сети с других устройств.</span><span class="sxs-lookup"><span data-stu-id="369eb-133">Care should be taken with this adapter as it will allow access to the network from other devices.</span></span>

### <a name="requirements"></a><span data-ttu-id="369eb-134">Требования</span><span class="sxs-lookup"><span data-stu-id="369eb-134">Requirements</span></span>

- <span data-ttu-id="369eb-135">Порт проводной сети с доступом к клиентской сети</span><span class="sxs-lookup"><span data-stu-id="369eb-135">Wired network port with access to the customer network</span></span>
- <span data-ttu-id="369eb-136">Совместимый с HoloLens концентратор USB-C с адаптером Ethernet — любой адаптер, не требующий дополнительных драйверов или установки приложений, должен подходить.</span><span class="sxs-lookup"><span data-stu-id="369eb-136">HoloLens Compatible USB-C Hub with Ethernet adaptor – Any adapter that doesn&#39;t require any additional drivers or application installs should be suitable.</span></span>
- <span data-ttu-id="369eb-137">Пакет подготовки:</span><span class="sxs-lookup"><span data-stu-id="369eb-137">Provisioning Package containing:</span></span>
  - <span data-ttu-id="369eb-138">Содержащий информацию и сертификат о беспроводной сети</span><span class="sxs-lookup"><span data-stu-id="369eb-138">Containing Wireless Network information and Certificate</span></span>
  - <span data-ttu-id="369eb-139">Содержащий информацию о регистрации для Azure AD организации (необязательно)</span><span class="sxs-lookup"><span data-stu-id="369eb-139">Optionally containing enrollment information for the Organization&#39;s Azure AD</span></span>
  - <span data-ttu-id="369eb-140">Содержащий любые другие необходимые параметры подготовки</span><span class="sxs-lookup"><span data-stu-id="369eb-140">Containing any other required provisioning settings</span></span>

### <a name="process"></a><span data-ttu-id="369eb-141">Process</span><span class="sxs-lookup"><span data-stu-id="369eb-141">Process</span></span>

<span data-ttu-id="369eb-142">Процесс может отличаться в зависимости от уровня программного обеспечения устройства.</span><span class="sxs-lookup"><span data-stu-id="369eb-142">The Process may vary depending on the software level of the device.</span></span> <span data-ttu-id="369eb-143">Если на устройстве установлено [обновление от мая 2004 г.](hololens-release-notes.md#windows-holographic-version-2004), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="369eb-143">If the device has the [May 2004 update](hololens-release-notes.md#windows-holographic-version-2004), follow the steps below.</span></span>

1. <span data-ttu-id="369eb-144">Поместите пакет подготовки в корень USB-накопителя и подключите к концентратору.</span><span class="sxs-lookup"><span data-stu-id="369eb-144">Place the provisioning package onto the root of a USB stick, and plug into the Hub.</span></span>
2. <span data-ttu-id="369eb-145">Подключите кабель Ethernet к адаптеру Hub + Ethernet.</span><span class="sxs-lookup"><span data-stu-id="369eb-145">Connect Ethernet cable to the Hub + Ethernet adapter.</span></span>
3. <span data-ttu-id="369eb-146">Подключите USB-C Hub к устройству HoloLens.</span><span class="sxs-lookup"><span data-stu-id="369eb-146">Connect USB-C Hub to HoloLens device.</span></span>
4. <span data-ttu-id="369eb-147">Включите HoloLens и наденьте устройство.</span><span class="sxs-lookup"><span data-stu-id="369eb-147">Turn on the HoloLens and put on the device.</span></span>
5. <span data-ttu-id="369eb-148">Нажмите **кнопку уменьшения громкости и кнопку питания**, чтобы применить пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="369eb-148">Press the **Volume Down and Power button** to apply the Provisioning Package.</span></span>
6. <span data-ttu-id="369eb-149">Теперь технический специалист может следить за OOBE, а по завершении открыть приложение "Параметры" и извлечь MAC-адрес устройства.</span><span class="sxs-lookup"><span data-stu-id="369eb-149">The technician can now follow OOBE, and when complete, open the Settings App to retrieve the MAC Address of the device.</span></span>

<span data-ttu-id="369eb-150">Если на устройстве установлена сборка ОС до [обновления от мая 2004 г.](hololens-release-notes.md#windows-holographic-version-2004), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="369eb-150">If the device has an OS build before the [May 2004 update](hololens-release-notes.md#windows-holographic-version-2004), follow the steps below.</span></span>

1. <span data-ttu-id="369eb-151">Включите устройство HoloLens и подключите его к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="369eb-151">Turn on the HoloLens and plug the device into a PC.</span></span>
2. <span data-ttu-id="369eb-152">Устройство должно отображаться на компьютере как запоминающее устройство файлов.</span><span class="sxs-lookup"><span data-stu-id="369eb-152">The device should show up on the PC as a file storage device.</span></span>
3. <span data-ttu-id="369eb-153">Скопируйте пакет подготовки на устройство</span><span class="sxs-lookup"><span data-stu-id="369eb-153">Copy the Provisioning Package to the Device</span></span>
4. <span data-ttu-id="369eb-154">Подключите кабель Ethernet к концентратору.</span><span class="sxs-lookup"><span data-stu-id="369eb-154">Connect Ethernet cable to the hub.</span></span>
5. <span data-ttu-id="369eb-155">Подключите USB-C Hub к устройству HoloLens.</span><span class="sxs-lookup"><span data-stu-id="369eb-155">Connect USB-C Hub to HoloLens device.</span></span>
6. <span data-ttu-id="369eb-156">Наденьте HoloLens</span><span class="sxs-lookup"><span data-stu-id="369eb-156">Put on the HoloLens</span></span>
7. <span data-ttu-id="369eb-157">Нажмите кнопку **уменьшения громкости и кнопку питания**, чтобы применить пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="369eb-157">Press the **Volume Down and Power** button to apply the Provisioning Package.</span></span>
8. <span data-ttu-id="369eb-158">Теперь технический специалист может следить за OOBE, а по завершении открыть приложение "Параметры" и извлечь MAC-адрес устройства.</span><span class="sxs-lookup"><span data-stu-id="369eb-158">The technician can now follow OOBE, and when complete, open the Settings App to retrieve the MAC Address of the device.</span></span>

### <a name="benefits"></a><span data-ttu-id="369eb-159">Преимущества</span><span class="sxs-lookup"><span data-stu-id="369eb-159">Benefits</span></span>

<span data-ttu-id="369eb-160">Это позволит &quot;традиционным сенсорным вводом&quot; на устройстве применить правильный пакет подготовки и собрать MAC-адрес устройства.</span><span class="sxs-lookup"><span data-stu-id="369eb-160">This will allow a &quot;Single touch&quot; of the device, to apply the correct provisioning package and gather the MAC address of the device.</span></span> [<span data-ttu-id="369eb-161">Пакеты подготовки можно создавать с помощью приведенных здесь инструкций.</span><span class="sxs-lookup"><span data-stu-id="369eb-161">Provisioning packages can be created following the guidance here.</span></span>](https://docs.microsoft.com/hololens/hololens-provisioning)

## <a name="autopilot-with-intune-enrollment"></a><span data-ttu-id="369eb-162">Autopilot с регистрацией в Intune</span><span class="sxs-lookup"><span data-stu-id="369eb-162">Autopilot with Intune Enrollment</span></span>

### <a name="requirements"></a><span data-ttu-id="369eb-163">Требования</span><span class="sxs-lookup"><span data-stu-id="369eb-163">Requirements</span></span>

- <span data-ttu-id="369eb-164">Порт проводной сети с доступом к сети клиента</span><span class="sxs-lookup"><span data-stu-id="369eb-164">Wired network port with access to the customer network</span></span>
- <span data-ttu-id="369eb-165">Устройства HoloLens под управлением Windows Holographic 2004</span><span class="sxs-lookup"><span data-stu-id="369eb-165">HoloLens devices running Windows Holographic 2004</span></span>
- <span data-ttu-id="369eb-166">Совместимый c HoloLens адаптер USB-C Ethernet</span><span class="sxs-lookup"><span data-stu-id="369eb-166">HoloLens Compatible USB-C Ethernet adapter</span></span>
- <span data-ttu-id="369eb-167">Настройка и включение Intune для клиента</span><span class="sxs-lookup"><span data-stu-id="369eb-167">Intune set up and enabled for the customer Tenant</span></span>
- <span data-ttu-id="369eb-168">Устройство зарегистрировано для автопилота и импортировано в клиент</span><span class="sxs-lookup"><span data-stu-id="369eb-168">Device registered for Autopilot and imported into the Customer Tenant</span></span>
- <span data-ttu-id="369eb-169">Политики Intune, определенные для устройства:</span><span class="sxs-lookup"><span data-stu-id="369eb-169">Intune Policies defined for the device:</span></span>
   - <span data-ttu-id="369eb-170">Содержащий информацию и сертификат о беспроводной сети</span><span class="sxs-lookup"><span data-stu-id="369eb-170">Containing Wireless Network information and Certificate</span></span>
   - <span data-ttu-id="369eb-171">Содержащий любые другие необходимые параметры подготовки</span><span class="sxs-lookup"><span data-stu-id="369eb-171">Containing any other required provisioning settings</span></span>

<span data-ttu-id="369eb-172">Это позволит клиентам с расширенными требованиями к сети регистрировать устройства в рамках более свободного, масштабируемого подхода</span><span class="sxs-lookup"><span data-stu-id="369eb-172">This will allow a customer with advanced networking requirements to enroll the devices in a hands-off, scalable approach</span></span>

<span data-ttu-id="369eb-173">Требуются дополнительные предварительные требования, как указано ниже:</span><span class="sxs-lookup"><span data-stu-id="369eb-173">Additional pre-requisites will be needed as below:</span></span>
1. [<span data-ttu-id="369eb-174">Включите клиент для предварительного просмотра автопилота</span><span class="sxs-lookup"><span data-stu-id="369eb-174">Enable the Tenant for the Autopilot preview</span></span>](https://docs.microsoft.com/hololens/hololens2-autopilot)
1. <span data-ttu-id="369eb-175">Создайте политики HoloLens, чтобы заменить пакет подготовки в Intune.</span><span class="sxs-lookup"><span data-stu-id="369eb-175">Create the HoloLens policies to replace the Provisioning Package within Intune.</span></span>
1. <span data-ttu-id="369eb-176">Создайте политики HoloLens Intune.</span><span class="sxs-lookup"><span data-stu-id="369eb-176">Create the HoloLens Intune Policies.</span></span>
1. <span data-ttu-id="369eb-177">Назначьте устройства в нужную группу.</span><span class="sxs-lookup"><span data-stu-id="369eb-177">Assign the devices to the correct group.</span></span>

### <a name="process"></a><span data-ttu-id="369eb-178">Процесс</span><span class="sxs-lookup"><span data-stu-id="369eb-178">Process</span></span>

1. <span data-ttu-id="369eb-179">Подключите кабель Ethernet к адаптеру и подключите адаптер к порту USB-C на устройстве HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="369eb-179">Connect the ethernet cable to the adapter and plug the adapter into the USB-C port on the HoloLens 2 device.</span></span>
2. <span data-ttu-id="369eb-180">Включите HoloLens.</span><span class="sxs-lookup"><span data-stu-id="369eb-180">Turn on the HoloLens.</span></span>
3. <span data-ttu-id="369eb-181">Устройство должно автоматически подключаться к Интернету во время OOBE с помощью адаптера Ethernet.</span><span class="sxs-lookup"><span data-stu-id="369eb-181">The device should automatically connect to the internet during OOBE via the Ethernet adaptor.</span></span> <span data-ttu-id="369eb-182">Он должен обнаруживать конфигурацию автопилота и автоматически регистрироваться в Azure AD и Intune.</span><span class="sxs-lookup"><span data-stu-id="369eb-182">It should detect the Autopilot configuration and automatically register with Azure AD and Intune</span></span>
4. <span data-ttu-id="369eb-183">Устройство будет применять необходимые сертификаты Wi-Fi и другие настройки по мере необходимости через Intune.</span><span class="sxs-lookup"><span data-stu-id="369eb-183">The Device will apply the required Wi-Fi Certificates and other configuration as needed via Intune</span></span>
5. <span data-ttu-id="369eb-184">По завершении технический специалист сможет загрузить портал Intune (диспетчер конечных точек) и перейти на страницу свойств устройства по адресу **Домашняя страница -> Устройства -> Имя устройства -> Оборудование**</span><span class="sxs-lookup"><span data-stu-id="369eb-184">When complete, the technician can load the Intune (Endpoint Manager) Portal and drill into the device properties page at **Home -> Devices -> DeviceName -> Hardware**</span></span>
6. <span data-ttu-id="369eb-185">MAC-адрес Wi-Fi будет виден на портале Intune</span><span class="sxs-lookup"><span data-stu-id="369eb-185">The Wifi MAC address will be visible within the Intune Portal</span></span>

![MAC-адрес через Intune](images/mac-address-intune.jpg)

7. <span data-ttu-id="369eb-187">Технический специалист добавит этот MAC-адрес в качестве разрешенного устройства.</span><span class="sxs-lookup"><span data-stu-id="369eb-187">The technician will add this MAC address as an allowed device.</span></span>

### <a name="benefits"></a><span data-ttu-id="369eb-188">Преимущества</span><span class="sxs-lookup"><span data-stu-id="369eb-188">Benefits</span></span>

<span data-ttu-id="369eb-189">Это позволит техническому специалисту выполнить развертывание &quot;обходным путем&quot;, при котором он может зарегистрировать устройство в Azure AD и Intune прямо из коробки, без необходимости носить его или вручную взаимодействовать со средой HoloLens.</span><span class="sxs-lookup"><span data-stu-id="369eb-189">This will allow a &quot;Heads off&quot; deployment experience for the Technician, with the device being able to go from the box to enrolled in Azure AD and Intune without the technician having to wear the device or manually interact with the HoloLens environment.</span></span>

## <a name="reporting-of-mac-addresses-to-the-technician"></a><span data-ttu-id="369eb-190">Создание отчетов о MAC-адресах техническому специалисту</span><span class="sxs-lookup"><span data-stu-id="369eb-190">Reporting of MAC addresses to the Technician</span></span>

### <a name="requirements"></a><span data-ttu-id="369eb-191">Требования</span><span class="sxs-lookup"><span data-stu-id="369eb-191">Requirements</span></span>

- <span data-ttu-id="369eb-192">Авторизация &quot;Intune Graph PowerShell&quot; для клиента</span><span class="sxs-lookup"><span data-stu-id="369eb-192">Authorization of the &quot;Intune Graph PowerShell&quot; against the customer Tenant</span></span>
- <span data-ttu-id="369eb-193">Установка Intune Graph PowerShell на компьютере технического специалиста.</span><span class="sxs-lookup"><span data-stu-id="369eb-193">Installation of the Intune Graph PowerShell on the technicians machine.</span></span>
- [https://www.powershellgallery.com/packages/Microsoft.Graph.Intune/6.1907.1.0](https://www.powershellgallery.com/packages/Microsoft.Graph.Intune/6.1907.1.0)
- <span data-ttu-id="369eb-194">Доступ для чтения элементам &quot;управляемых устройств&quot; Intune.</span><span class="sxs-lookup"><span data-stu-id="369eb-194">Read access to the &quot;Managed Devices&quot; elements of Intune.</span></span> <span data-ttu-id="369eb-195">(Оператор службы поддержки или выше, или пользовательская роль)</span><span class="sxs-lookup"><span data-stu-id="369eb-195">(Help Desk Operator or above, or a custom role)</span></span>

<span data-ttu-id="369eb-196">В настоящее время не существует &quot;простого&quot; способа запустить команду автоматизации на основе регистрации нового устройства в Intune.</span><span class="sxs-lookup"><span data-stu-id="369eb-196">At present, there is no &quot;simple&quot; way to trigger an automation command based on the enrolment of a new device within Intune.</span></span> <span data-ttu-id="369eb-197">Следовательно, эта команда предоставит техническому специалисту простой способ получить MAC-адрес без необходимости входа на портал и извлечения его вручную.</span><span class="sxs-lookup"><span data-stu-id="369eb-197">Therefore, this command will provide the technician a simple way to retrieve the MAC address without needing to log onto the portal and manually retrieve it.</span></span>

```powershell
Import-Module Microsoft.Graph.Intune

Connect-MSGraph

Get-IntuneManagedDevice -Filter "model eq 'Hololens 2'" | where {$_.enrolledDateTime -gt (get-date).AddDays(-30)}  | select deviceName, wiFiMacAddress 
```

<span data-ttu-id="369eb-198">Это вернет имя и MAC-адрес всех устройств HoloLens, которые были зарегистрированы за последние 30 дней.</span><span class="sxs-lookup"><span data-stu-id="369eb-198">This will return the name and MAC address of any HoloLens devices which have been enrolled in the last 30 days.</span></span>

![MAC-адрес через PowerShell](images/mac-address-powershell.jpg)

### <a name="process"></a><span data-ttu-id="369eb-200">Process</span><span class="sxs-lookup"><span data-stu-id="369eb-200">Process</span></span>

<span data-ttu-id="369eb-201">После завершения регистрации Intune технический специалист запустит указанный выше сценарий для извлечения MAC-адреса.</span><span class="sxs-lookup"><span data-stu-id="369eb-201">After the Intune enrolment has completed, the Technician would run the above script to retrieve the MAC address.</span></span>
