---
title: Диспетчер сертификатов
description: Узнайте, как вручную устанавливать, администрировать и удалять сертификаты на устройствах "смешанная реальность" HoloLens 2.
author: evmill
ms.author: v-evmill
manager: yannisle
ms.prod: hololens
ms.sitesec: library
ms.topic: article
ms.localizationpriority: medium
ms.date: 10/13/2020
audience: ITPro
appliesto:
- HoloLens 2
ms.openlocfilehash: f9dcf98cbd200ac54cd786648fdfe286bff1aa00
ms.sourcegitcommit: 29573e577381a23891e9557884a6dfdaac0c1c48
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110397455"
---
# <a name="certificate-manager"></a><span data-ttu-id="54697-103">Диспетчер сертификатов</span><span class="sxs-lookup"><span data-stu-id="54697-103">Certificate Manager</span></span>

- <span data-ttu-id="54697-104">Улучшенные средства аудита, диагностики и проверки для обеспечения безопасности устройств и обеспечения соответствия требованиям с помощью нового диспетчера сертификатов.</span><span class="sxs-lookup"><span data-stu-id="54697-104">Improved auditing, diagnosis, and validation tooling for device security and compliance through the new Certificate Manager.</span></span> <span data-ttu-id="54697-105">Эта возможность позволит вам развертывать, устранять неполадки и проверять сертификаты в коммерческих средах.</span><span class="sxs-lookup"><span data-stu-id="54697-105">This capability will enable you to deploy, troubleshoot, and validate your certificates at scale in commercial environments.</span></span>

<span data-ttu-id="54697-106">В Windows holographic, версия 20H2, мы добавляем диспетчер сертификатов в приложение "Параметры" HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="54697-106">In Windows Holographic, version 20H2, we are adding a Certificate Manager in the HoloLens 2 Settings app.</span></span> <span data-ttu-id="54697-107">Последовательно выберите **параметры > обновить & безопасность > сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="54697-107">Go to **Settings > Update & Security > Certificates**.</span></span> <span data-ttu-id="54697-108">Эта функция предоставляет простой и понятный пользователю способ просмотра, установки и удаления сертификатов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="54697-108">This feature provides a simple and user-friendly way to view, install and remove certificates on your device.</span></span> <span data-ttu-id="54697-109">Благодаря новому диспетчеру сертификатов администраторы и пользователи теперь имеют улучшенные средства аудита, диагностики и проверки, чтобы обеспечить безопасность и соответствие устройств.</span><span class="sxs-lookup"><span data-stu-id="54697-109">With the new Certificate Manager, admins and users now have improved auditing, diagnosis and validation tooling to ensure that devices remain secure and compliant.</span></span> 

-   <span data-ttu-id="54697-110">**Аудит:** Возможность проверить, правильно ли развернут сертификат, или подтвердить его удаление соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="54697-110">**Auditing:** Ability to validate that a certificate is deployed correctly or to confirm that it was removed appropriately.</span></span> 
-   <span data-ttu-id="54697-111">**Диагностика:** При возникновении проблем проверка наличия соответствующих сертификатов на устройстве экономит время и помогает устранять неполадки.</span><span class="sxs-lookup"><span data-stu-id="54697-111">**Diagnosis:** When issues arise, validating that the appropriate certificates exist on the device saves time and helps with troubleshooting.</span></span> 
-   <span data-ttu-id="54697-112">**Проверка:** Проверка того, что сертификат служит целью и является функциональным, может сэкономить значительное время, особенно в коммерческих средах, прежде чем развертывать сертификаты в крупном масштабе.</span><span class="sxs-lookup"><span data-stu-id="54697-112">**Validation:** Verifying that a certificate serves the intended purpose and is functional, can save significant time, particularly in commercial environments before deploying certificates at larger scale.</span></span>

<span data-ttu-id="54697-113">Чтобы быстро найти конкретный сертификат в списке, можно выполнить сортировку по имени, магазину или дате окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="54697-113">To find a specific certificate in the list quickly, there are options to sort by name, store or expiration date.</span></span> <span data-ttu-id="54697-114">Пользователи также могут напрямую искать сертификат.</span><span class="sxs-lookup"><span data-stu-id="54697-114">Users may also directly search for a certificate.</span></span> <span data-ttu-id="54697-115">Чтобы просмотреть отдельные свойства сертификата, выберите сертификат и щелкните **сведения**.</span><span class="sxs-lookup"><span data-stu-id="54697-115">To view individual certificate properties, select the certificate and click on **Info**.</span></span> 

<span data-ttu-id="54697-116">В настоящее время установка сертификата поддерживает CER-и CRT-файлы.</span><span class="sxs-lookup"><span data-stu-id="54697-116">Certificate installation currently supports .cer and .crt files.</span></span> <span data-ttu-id="54697-117">Владельцы устройств могут устанавливать сертификаты на локальном компьютере и у текущего пользователя.  все остальные пользователи могут устанавливаться только в текущий пользователь.</span><span class="sxs-lookup"><span data-stu-id="54697-117">Device Owners can install certificates in Local Machine and Current User;  all other users can only install into Current User.</span></span> <span data-ttu-id="54697-118">Пользователи могут удалять только сертификаты, установленные непосредственно из пользовательского интерфейса параметров.</span><span class="sxs-lookup"><span data-stu-id="54697-118">Users can only remove certificates installed directly from the Settings UI.</span></span> <span data-ttu-id="54697-119">Если сертификат был установлен с помощью других средств, он также должен быть удален тем же механизмом.</span><span class="sxs-lookup"><span data-stu-id="54697-119">If a certificate has been installed through other means, it must also be removed by the same mechanism.</span></span>

## <a name="to-install-a-certificate"></a><span data-ttu-id="54697-120">Чтобы установить сертификат, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="54697-120">To install a certificate:</span></span> 

1.  <span data-ttu-id="54697-121">Подключите HoloLens 2 к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="54697-121">Connect your HoloLens 2 to a PC.</span></span>
1.  <span data-ttu-id="54697-122">Поместите файл сертификата, который вы хотите установить, в расположение в HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="54697-122">Place the certificate file you want to install in a location on your HoloLens 2.</span></span>
1.  <span data-ttu-id="54697-123">Перейдите в раздел **Параметры приложение > обновить & безопасность > сертификаты** и выберите установить сертификат.</span><span class="sxs-lookup"><span data-stu-id="54697-123">Navigate to **Settings App > Update & Security > Certificates**, and select Install a certificate.</span></span>
1.  <span data-ttu-id="54697-124">Щелкните **Импорт файла** и перейдите к расположению, в котором сохранен сертификат.</span><span class="sxs-lookup"><span data-stu-id="54697-124">Click **Import File** and navigate to the location you saved the certificate.</span></span>
1.  <span data-ttu-id="54697-125">Выберите **расположение хранилища**.</span><span class="sxs-lookup"><span data-stu-id="54697-125">Select **Store Location**.</span></span>
1.  <span data-ttu-id="54697-126">Выберите **хранилище сертификатов**.</span><span class="sxs-lookup"><span data-stu-id="54697-126">Select **Certificate Store**.</span></span>
1.  <span data-ttu-id="54697-127">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="54697-127">Click **Install**.</span></span>

<span data-ttu-id="54697-128">Теперь сертификат должен быть установлен на устройстве.</span><span class="sxs-lookup"><span data-stu-id="54697-128">The certificate should now be installed on the device.</span></span>

## <a name="to-remove-a-certificate"></a><span data-ttu-id="54697-129">Чтобы удалить сертификат, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="54697-129">To remove a certificate:</span></span> 
>[!WARNING]
> <span data-ttu-id="54697-130">Несмотря на то, что сертификаты, развернутые в MDM, можно просматривать в диспетчере сертификатов, их нельзя удалить в диспетчере сертификатов.</span><span class="sxs-lookup"><span data-stu-id="54697-130">Although you can view MDM-deployed certificates in Certificate Manager, you cannot uninstall them in Certificate Manager.</span></span> <span data-ttu-id="54697-131">Их необходимо удалить с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="54697-131">You must uninstall them through MDM.</span></span>
1. <span data-ttu-id="54697-132">Последовательно выберите **Параметры приложение > обновления и безопасность > сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="54697-132">Navigate to **Settings App > Update and Security > Certificates**.</span></span>
1. <span data-ttu-id="54697-133">В поле поиска найдите сертификат по имени.</span><span class="sxs-lookup"><span data-stu-id="54697-133">Search for the certificate by name in the search box.</span></span>
1. <span data-ttu-id="54697-134">Выберите сертификат.</span><span class="sxs-lookup"><span data-stu-id="54697-134">Select the certificate.</span></span>
1. <span data-ttu-id="54697-135">Нажмите кнопку **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="54697-135">Click **Remove**</span></span>
1. <span data-ttu-id="54697-136">Выберите **Да** при запросе на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="54697-136">Select **Yes** when prompted for confirmation.</span></span>



![Средство просмотра сертификатов в приложении "Параметры" в разделе "сертификаты"](images/certificate-viewer-device.jpg)

![Рисунок, показывающий, как использовать пользовательский интерфейс сертификата для установки сертификата в параметрах.](images/certificate-device-install.jpg)
