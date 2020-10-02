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
ms.openlocfilehash: 2b0ed266389ccc5a21117a604a6eb0abd214d4d1
ms.sourcegitcommit: 1793f53f9e1cc63ac40edc09e65bb4beb80a4575
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "11093248"
---
# <span data-ttu-id="3fbb7-103">Корпоративная регистрация устройств HoloLens в среде Wi-Fi с ограниченным количеством MAC-адресов</span><span class="sxs-lookup"><span data-stu-id="3fbb7-103">Enterprise Enrollment of HoloLens Devices in MAC address restricted Wi-Fi Environment</span></span>

<span data-ttu-id="3fbb7-104">В этом документе будет описан общий сценарий, который был определен в средах клиента, где Wi-Fi ограничен MAC-адресами, или где для подключения к беспроводным сетям требуются сертификаты.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-104">This document will describe a common scenario we have identified within customer environments where the Wi-Fi is restricted by MAC addresses, or certificates are required to join Wireless networks.</span></span>

## <span data-ttu-id="3fbb7-105">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="3fbb7-105">Example Scenario</span></span>

<span data-ttu-id="3fbb7-106">Многие клиенты в защищенных средах имеют ограничения на свои беспроводные или проводные сети, которые позволяют успешно подключаться только утвержденным устройствам (на основе MAC-адресов) (либо с фильтрацией MAC-адресов в беспроводной точке доступа, либо на DHCP-сервере).</span><span class="sxs-lookup"><span data-stu-id="3fbb7-106">Many customers in secure environments have restrictions on their Wireless or wired networks which will only allow approved devices (based on MAC Addresses) to connect successfully (either with MAC Address filtering on a Wireless Access Point or on a DHCP server).</span></span> <span data-ttu-id="3fbb7-107">Кроме того, в некоторых беспроводных сетях можно использовать протокол PEAP, при котором для успешной проверки подлинности беспроводной сети необходимо применить сертификат к устройству.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-107">Additionally, some Wireless networks can be protected with PEAP, which requires that a certificate be applied to the device prior to being able to successfully authenticate the Wireless network.</span></span>

<span data-ttu-id="3fbb7-108">При работе с устройствами HoloLens могут возникать две основные проблемы, которые могут привести к задержкам и работе вручную при подключении устройств HoloLens к сети.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-108">Two key issues can arise with HoloLens devices, which can cause delays and manual work in joining the HoloLens Devices to the network.</span></span>

- <span data-ttu-id="3fbb7-109">Сертификат Wireless PEAP должен быть применен к устройству до того, как устройство успешно подключится к беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-109">The Wireless PEAP certificate must be applied to the device prior to the device successfully joining the wireless network.</span></span>
- <span data-ttu-id="3fbb7-110">MAC-адрес адаптера Wi-Fi HoloLens должен быть зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-110">The MAC Address of the HoloLens Wi-Fi adaptor must be registered.</span></span>

<span data-ttu-id="3fbb7-111">Ключевые проблемы:</span><span class="sxs-lookup"><span data-stu-id="3fbb7-111">The key challenges to this are:</span></span>

1. <span data-ttu-id="3fbb7-112">В настоящее время MAC-адрес можно определить только из приложения «Параметры» на устройстве или из Intune после успешной регистрации в Intune.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-112">The MAC Address can currently only be identified from the Settings app on the device, or from Intune after a successful Intune enrollment.</span></span>
2. <span data-ttu-id="3fbb7-113">Без MAC-адреса устройство не может присоединиться к сети Wi-Fi для начала регистрации.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-113">Without the MAC address, the device cannot join the Wi-Fi Network to begin enrollment.</span></span>
3. <span data-ttu-id="3fbb7-114">Ручное решение этих проблем требует участия технического специалиста в работе с устройствами.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-114">Manual Solutions to these challenges require technician involvement with the devices.</span></span>

## <span data-ttu-id="3fbb7-115">Решения</span><span class="sxs-lookup"><span data-stu-id="3fbb7-115">Solutions</span></span>

<span data-ttu-id="3fbb7-116">Есть несколько способов улучшить эту ситуацию, в зависимости от инфраструктуры, доступной в среде.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-116">There are a number of ways to improve this situation, depending on the infrastructure available within the environment.</span></span>

| <span data-ttu-id="3fbb7-117">Решение</span><span class="sxs-lookup"><span data-stu-id="3fbb7-117">Solution</span></span> | <span data-ttu-id="3fbb7-118">Преимущества</span><span class="sxs-lookup"><span data-stu-id="3fbb7-118">Benefits</span></span> | <span data-ttu-id="3fbb7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3fbb7-119">Requirements</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3fbb7-120">Пакет подготовки с адаптером Ethernet</span><span class="sxs-lookup"><span data-stu-id="3fbb7-120">Provisioning Package with Ethernet Adaptor</span></span> | <span data-ttu-id="3fbb7-121">Улучшены возможности OOBE и обеспечивает более быстрый опыт работы с техническим специалистом.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-121">Improves OOBE experience and allows for a quicker technician experience.</span></span> | <span data-ttu-id="3fbb7-122">HoloLens, совместимый с USB C HubTechnician, все еще должен будет взаимодействовать с устройством для записи MAC и OOBE</span><span class="sxs-lookup"><span data-stu-id="3fbb7-122">HoloLens compatible USB C HubTechnician will still need to interact with the device for MAC Capture and OOBE finalisation</span></span> |
| <span data-ttu-id="3fbb7-123">Автопилот с регистрацией в Intune через Ethernet</span><span class="sxs-lookup"><span data-stu-id="3fbb7-123">Autopilot with Intune Registration over Ethernet</span></span> | <span data-ttu-id="3fbb7-124">Одношаговое подключение и регистрация устройства в среде клиента. Запись MAC можно выполнить без взаимодействия с устройством</span><span class="sxs-lookup"><span data-stu-id="3fbb7-124">Single Step connection and registration of the device to the customer environmentMAC capture can be completed without interacting with the device</span></span> | <span data-ttu-id="3fbb7-125">Intune включен для клиента — сетевого адаптера USB-C, совместимого с AAD TenantHoloLens</span><span class="sxs-lookup"><span data-stu-id="3fbb7-125">Intune enabled for the customer AAD TenantHoloLens Compatible USB-C network adaptor</span></span> |
| <span data-ttu-id="3fbb7-126">Автоматизированная отчетность о MAC-адресах</span><span class="sxs-lookup"><span data-stu-id="3fbb7-126">Automated reporting of MAC Addresses</span></span> | <span data-ttu-id="3fbb7-127">После регистрации устройств в клиенте Intune, запишите отчет MAC-адреса техническому специалисту.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-127">When devices have been registered within the Intune Tenant, Script the reporting of the MAC address to the technician.</span></span> | <span data-ttu-id="3fbb7-128">Командлеты Intune PowerShell</span><span class="sxs-lookup"><span data-stu-id="3fbb7-128">Intune Powershell Commandlets</span></span> |

## <span data-ttu-id="3fbb7-129">Пакет подготовки с адаптером Ethernet</span><span class="sxs-lookup"><span data-stu-id="3fbb7-129">Provisioning Package with Ethernet Adaptor</span></span>

> [!NOTE] 
> <span data-ttu-id="3fbb7-130">Если на проводную сеть также распространяются ограничения MAC, то MAC-адрес адаптера или концентратора USB-C Ethernet должен быть предварительно утвержден.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-130">If the wired network is also subject to MAC restrictions, then the MAC address of the USB-C Ethernet adaptor / Hub will need to be pre-approved.</span></span> <span data-ttu-id="3fbb7-131">Будьте внимательны при использовании этого концентратора, так как он позволяет получить доступ к сети с других устройств.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-131">Care should be taken with this hub as it will allow access to the network from other devices.</span></span>

### <span data-ttu-id="3fbb7-132">Требования</span><span class="sxs-lookup"><span data-stu-id="3fbb7-132">Requirements</span></span>

- <span data-ttu-id="3fbb7-133">Порт проводной сети с доступом к сети клиента</span><span class="sxs-lookup"><span data-stu-id="3fbb7-133">Wired network port with access to the customer network</span></span>
- <span data-ttu-id="3fbb7-134">Совместимый с HoloLens концентратор USB-C, содержащий адаптер Ethernet — любой концентратор, не требующий дополнительных драйверов или установки приложений, должен быть подходящим.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-134">HoloLens Compatible USB-C Hub containing an Ethernet adaptor – Any hub that doesn&#39;t require any additional drivers or application installs should be suitable.</span></span>
- <span data-ttu-id="3fbb7-135">Пакет подготовки, содержащий:</span><span class="sxs-lookup"><span data-stu-id="3fbb7-135">Provisioning Package containing:</span></span>
  - <span data-ttu-id="3fbb7-136">Содержащий информацию и сертификат о беспроводной сети</span><span class="sxs-lookup"><span data-stu-id="3fbb7-136">Containing Wireless Network information and Certificate</span></span>
  - <span data-ttu-id="3fbb7-137">Необязательно содержащий информацию о регистрации для Azure AD организации</span><span class="sxs-lookup"><span data-stu-id="3fbb7-137">Optionally containing enrollment information for the Organisation&#39;s Azure AD</span></span>
  - <span data-ttu-id="3fbb7-138">Содержащий любые другие необходимые параметры подготовки</span><span class="sxs-lookup"><span data-stu-id="3fbb7-138">Containing any other required provisioning settings</span></span>

### <span data-ttu-id="3fbb7-139">Process</span><span class="sxs-lookup"><span data-stu-id="3fbb7-139">Process</span></span>

<span data-ttu-id="3fbb7-140">Процесс может отличаться в зависимости от уровня программного обеспечения устройства.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-140">The Process may vary depending on the software level of the device.</span></span> <span data-ttu-id="3fbb7-141">Если на устройстве установлено [обновление от мая 2004 г.](hololens-release-notes.md#windows-holographic-version-2004), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-141">If the device has the [May 2004 update](hololens-release-notes.md#windows-holographic-version-2004), follow the steps below.</span></span>

1. <span data-ttu-id="3fbb7-142">Поместите пакет подготовки в корень USB-накопителя и подключите к концентратору.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-142">Place the provisioning package onto the root of a USB stick, and plug into the Hub.</span></span>
2. <span data-ttu-id="3fbb7-143">Подключите кабель Ethernet к концентратору.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-143">Connect Ethernet cable to the hub.</span></span>
3. <span data-ttu-id="3fbb7-144">Подключите концентратор USB-C к устройству HoloLens.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-144">Connect USB-C hub to HoloLens device.</span></span>
4. <span data-ttu-id="3fbb7-145">Включите устройство HoloLens и используйте его.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-145">Turn on HoloLens Device and wear the device.</span></span>
5. <span data-ttu-id="3fbb7-146">Нажмите кнопку **уменьшения громкости и кнопку питания**, чтобы применить пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-146">Press the **Volume Down and Power button** to apply the Provisioning Package.</span></span>
6. <span data-ttu-id="3fbb7-147">Теперь технический специалист может следить за OOBE, а по завершении открыть приложение «Параметры» и извлечь MAC-адрес устройства.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-147">The technician can now follow OOBE, and when complete, open the Settings App, and retrieve the MAC Address of the device.</span></span>

<span data-ttu-id="3fbb7-148">Если на устройстве установлена ОС до [обновления от мая 2004 г.](hololens-release-notes.md#windows-holographic-version-2004), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-148">If the device has an OS build before the [May 2004 update](hololens-release-notes.md#windows-holographic-version-2004), follow the steps below.</span></span>

1. <span data-ttu-id="3fbb7-149">Включите устройство HoloLens и подключите его к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-149">Turn on the HoloLens Device, and plug the device into a PC.</span></span>
2. <span data-ttu-id="3fbb7-150">Устройство должно отображаться на компьютере как запоминающее устройство файлов.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-150">The device should show up on the PC as a file storage device.</span></span>
3. <span data-ttu-id="3fbb7-151">Скопируйте пакет подготовки на устройство</span><span class="sxs-lookup"><span data-stu-id="3fbb7-151">Copy the Provisioning Package to the Device</span></span>
4. <span data-ttu-id="3fbb7-152">Подключите кабель Ethernet к концентратору.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-152">Connect Ethernet cable to the hub.</span></span>
5. <span data-ttu-id="3fbb7-153">Подключите концентратор USB-C к устройству HoloLens.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-153">Connect USB-C hub to HoloLens device.</span></span>
6. <span data-ttu-id="3fbb7-154">Используйте устройство.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-154">Wear the device.</span></span>
7. <span data-ttu-id="3fbb7-155">Нажмите кнопку **уменьшения громкости и кнопку питания**, чтобы применить пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-155">Press the **Volume Down and Power** button to apply the Provisioning Package.</span></span>
8. <span data-ttu-id="3fbb7-156">Теперь технический специалист может следить за OOBE, а по завершении открыть приложение «Параметры» и извлечь MAC-адрес устройства.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-156">The technician can now follow OOBE, and when complete, open the Settings App, and retrieve the MAC Address of the device.</span></span>

### <span data-ttu-id="3fbb7-157">Преимущества</span><span class="sxs-lookup"><span data-stu-id="3fbb7-157">Benefits</span></span>

<span data-ttu-id="3fbb7-158">Это позволит &quot;традиционным сенсорным вводом&quot; на устройстве применить правильный пакет подготовки и собрать MAC-адрес устройства.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-158">This will allow a &quot;Single touch&quot; of the device, to apply the correct provisioning package and gather the MAC address of the device.</span></span> [<span data-ttu-id="3fbb7-159">Пакеты подготовки можно создавать с помощью приведенных здесь инструкций.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-159">Provisioning packages can be created following the guidance here.</span></span>](https://docs.microsoft.com/hololens/hololens-provisioning)

## <span data-ttu-id="3fbb7-160">Автопилот с регистрацией в Intune</span><span class="sxs-lookup"><span data-stu-id="3fbb7-160">Autopilot with Intune Enrolment</span></span>

### <span data-ttu-id="3fbb7-161">Требования</span><span class="sxs-lookup"><span data-stu-id="3fbb7-161">Requirements</span></span>

- <span data-ttu-id="3fbb7-162">Порт проводной сети с доступом к сети клиента</span><span class="sxs-lookup"><span data-stu-id="3fbb7-162">Wired network port with access to the customer network</span></span>
- <span data-ttu-id="3fbb7-163">Устройства HoloLens под управлением Windows Holographic 2004</span><span class="sxs-lookup"><span data-stu-id="3fbb7-163">HoloLens devices running Windows Holographic 2004</span></span>
- <span data-ttu-id="3fbb7-164">HoloLens, совместимый с концентратором USB-C</span><span class="sxs-lookup"><span data-stu-id="3fbb7-164">HoloLens Compatible USB-C Hub</span></span>
- <span data-ttu-id="3fbb7-165">Настройка и включение Intune для клиента</span><span class="sxs-lookup"><span data-stu-id="3fbb7-165">Intune set up and enabled for the customer Tenant</span></span>
- <span data-ttu-id="3fbb7-166">Устройство зарегистрировано для автопилота и импортировано в клиент</span><span class="sxs-lookup"><span data-stu-id="3fbb7-166">Device registered for Autopilot and imported into the Customer Tenant</span></span>
- <span data-ttu-id="3fbb7-167">Политики Intune, определенные для устройства:</span><span class="sxs-lookup"><span data-stu-id="3fbb7-167">Intune Policies defined for the device:</span></span>
   - <span data-ttu-id="3fbb7-168">Содержащий информацию и сертификат о беспроводной сети</span><span class="sxs-lookup"><span data-stu-id="3fbb7-168">Containing Wireless Network information and Certificate</span></span>
   - <span data-ttu-id="3fbb7-169">Содержащий любые другие необходимые параметры подготовки</span><span class="sxs-lookup"><span data-stu-id="3fbb7-169">Containing any other required provisioning settings</span></span>

<span data-ttu-id="3fbb7-170">Это позволит клиентам с расширенными требованиями к сети регистрировать устройства в рамках более свободного, масштабируемого подхода</span><span class="sxs-lookup"><span data-stu-id="3fbb7-170">This will allow a customer with advanced networking requirements to enroll the devices in a hands-off, scalable approach</span></span>

<span data-ttu-id="3fbb7-171">Требуются дополнительные предварительные требования, как указано ниже:</span><span class="sxs-lookup"><span data-stu-id="3fbb7-171">Additional pre-requisites will be needed as below:</span></span>
1. [<span data-ttu-id="3fbb7-172">Включите клиент для предварительного просмотра автопилота</span><span class="sxs-lookup"><span data-stu-id="3fbb7-172">Enable the Tenant for the Autopilot preview</span></span>](https://docs.microsoft.com/hololens/hololens2-autopilot)
1. <span data-ttu-id="3fbb7-173">Создайте политики HoloLens, чтобы заменить пакет подготовки в Intune.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-173">Create the HoloLens policies to replace the Provisioning Package within Intune.</span></span>
1. <span data-ttu-id="3fbb7-174">Создайте политики HoloLens Intune.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-174">Create the HoloLens Intune Policies.</span></span>
1. <span data-ttu-id="3fbb7-175">Назначьте устройства в нужную группу.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-175">Assign the devices to the correct group.</span></span>

### <span data-ttu-id="3fbb7-176">Process</span><span class="sxs-lookup"><span data-stu-id="3fbb7-176">Process</span></span>

1. <span data-ttu-id="3fbb7-177">Подключите концентратор USB-C и кабель ethernet к устройству HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-177">Plug the USB-C hub and ethernet cable into the HoloLens 2 device.</span></span>
2. <span data-ttu-id="3fbb7-178">Включите HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-178">Turn on the HoloLens 2.</span></span>
3. <span data-ttu-id="3fbb7-179">Устройство должно автоматически подключаться к Интернету в OOBE через Ethernet-адаптер, определять настройку автопилота и автоматически регистрировать в Azure AD и Intune.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-179">The device should automatically connect to the internet at OOBE via the Ethernet adaptor, detect the Autopilot configuration, and automatically register with Azure AD and Intune</span></span>
4. <span data-ttu-id="3fbb7-180">Устройство будет применять необходимые сертификаты Wi-Fi и другую настройку по мере необходимости через Intune.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-180">The Device will apply the required Wi-Fi Certificates and other configuration as needed via Intune</span></span>
5. <span data-ttu-id="3fbb7-181">По завершении технический специалист сможет загрузить портал Intune (диспетчер конечных точек) и перейти на страницу свойств устройства на **главной странице -> Устройства -> Имя устройства -> Оборудование**</span><span class="sxs-lookup"><span data-stu-id="3fbb7-181">When complete, the technician will be able to load the Intune (Endpoint Manager) Portal, and drill into the device properties page at **Home -> Devices -> DeviceName -> Hardware**</span></span>
6. <span data-ttu-id="3fbb7-182">MAC-адрес Wi-Fi будет виден на портале Intune</span><span class="sxs-lookup"><span data-stu-id="3fbb7-182">The Wifi MAC address will be visible within the Intune Portal</span></span>

![MAC-адрес через Intune](images/mac-address-intune.jpg)

7. <span data-ttu-id="3fbb7-184">Технический специалист добавит этот MAC-адрес в качестве разрешенного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-184">The technician will add this MAC address as an allowed device.</span></span>

### <span data-ttu-id="3fbb7-185">Преимущества</span><span class="sxs-lookup"><span data-stu-id="3fbb7-185">Benefits</span></span>

<span data-ttu-id="3fbb7-186">Это позволит техническому специалисту выполнить развертывание &quot;Heads off&quot;, при этом устройство сможет перейти из коробки в систему для регистрации в AAD и Intune без необходимости использовать устройство или вручную взаимодействовать со средой HoloLens.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-186">This will allow a &quot;Heads off&quot; deployment experience for the Technician, with the device being able to go from the box to enrolled in AAD and Intune without the technician having to wear the device or manually interact with the HoloLens environment.</span></span>

## <span data-ttu-id="3fbb7-187">Создание отчетов о MAC-адресах техническому специалисту</span><span class="sxs-lookup"><span data-stu-id="3fbb7-187">Reporting of MAC addresses to the Technician</span></span>

### <span data-ttu-id="3fbb7-188">Требования</span><span class="sxs-lookup"><span data-stu-id="3fbb7-188">Requirements</span></span>

- <span data-ttu-id="3fbb7-189">Авторизация &quot;Intune Graph PowerShell&quot; от клиента</span><span class="sxs-lookup"><span data-stu-id="3fbb7-189">Authorisation of the &quot;Intune Graph Powershell&quot; against the customer Tenant</span></span>
- <span data-ttu-id="3fbb7-190">Установка Intune Graph PowerShell на компьютере технического специалиста.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-190">Installation of the Intune Graph Powershell on the technicians machine.</span></span>
- [https://www.powershellgallery.com/packages/Microsoft.Graph.Intune/6.1907.1.0](https://www.powershellgallery.com/packages/Microsoft.Graph.Intune/6.1907.1.0)
- <span data-ttu-id="3fbb7-191">Доступ для чтения элементам &quot;управляемых устройств&quot; Intune.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-191">Read access to the &quot;Managed Devices&quot; elements of Intune.</span></span> <span data-ttu-id="3fbb7-192">(Оператор службы поддержки или выше, или пользовательская роль)</span><span class="sxs-lookup"><span data-stu-id="3fbb7-192">(Help Desk Operator or above, or a custom role)</span></span>

<span data-ttu-id="3fbb7-193">В настоящее время не существует &quot;простого&quot; способа запустить команду автоматизации на основе регистрации нового устройства в Intune.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-193">At present, there is no &quot;simple&quot; way to trigger an automation command based on the enrolment of a new device within Intune.</span></span> <span data-ttu-id="3fbb7-194">Следовательно, эта команда предоставит техническому специалисту простой способ получить MAC-адрес без необходимости входа на портал и извлечения его вручную.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-194">Therefore, this command will provide the technician a simple way to retrieve the MAC address without needing to log onto the portal and manually retrieve it.</span></span>

```powershell
Import-Module Microsoft.Graph.Intune

Connect-MSGraph

Get-IntuneManagedDevice -Filter "model eq 'Hololens 2'" | where {$_.enrolledDateTime -gt (get-date).AddDays(-30)}  | select deviceName, wiFiMacAddress 
```

<span data-ttu-id="3fbb7-195">Это вернет имя и MAC-адрес всех устройств HoloLens, которые были зарегистрированы за последние 30 дней.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-195">This will return the name and MAC address of any HoloLens devices which have been enrolled in the last 30 days.</span></span>

![MAC-адрес через PowerShell](images/mac-address-powershell.jpg)

### <span data-ttu-id="3fbb7-197">Process</span><span class="sxs-lookup"><span data-stu-id="3fbb7-197">Process</span></span>

<span data-ttu-id="3fbb7-198">После завершения регистрации Intune технический специалист запустит указанный выше сценарий для извлечения MAC-адреса.</span><span class="sxs-lookup"><span data-stu-id="3fbb7-198">After the Intune enrolment has completed, the Technician would run the above script to retrieve the MAC address.</span></span>
