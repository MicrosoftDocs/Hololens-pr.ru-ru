---
title: Диспетчер сертификатов
description: Сведения о том, как вручную управлять сертификатами в HoloLens 2.
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
ms.openlocfilehash: 04d7e8cb78357b5398c58e0a0c55e6e530fa363a
ms.sourcegitcommit: 108b818130e2627bf08107f4e47ae159dd6ab1d2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "11163228"
---
# <span data-ttu-id="454a0-103">Диспетчер сертификатов</span><span class="sxs-lookup"><span data-stu-id="454a0-103">Certificate Manager</span></span>

- <span data-ttu-id="454a0-104">Улучшенные средства аудита, диагностики и проверки для обеспечения безопасности устройств и соответствия требованиям с помощью нового диспетчера сертификатов.</span><span class="sxs-lookup"><span data-stu-id="454a0-104">Improved auditing, diagnosis, and validation tooling for device security and compliance through the new Certificate Manager.</span></span> <span data-ttu-id="454a0-105">Эта возможность позволяет развертывать, устранять неполадки и проверять сертификаты в масштабах в коммерческой среде.</span><span class="sxs-lookup"><span data-stu-id="454a0-105">This capability will enable you to deploy, troubleshoot, and validate your certificates at scale in commercial environments.</span></span>

<span data-ttu-id="454a0-106">В Windows holographic версии 20H2 мы добавляем диспетчер сертификатов в приложение "Параметры HoloLens 2".</span><span class="sxs-lookup"><span data-stu-id="454a0-106">In Windows Holographic, version 20H2, we are adding a Certificate Manager in the HoloLens 2 Settings app.</span></span> <span data-ttu-id="454a0-107">Перейдите в раздел **настройки > обновление сертификатов & безопасности >**.</span><span class="sxs-lookup"><span data-stu-id="454a0-107">Go to **Settings > Update & Security > Certificates**.</span></span> <span data-ttu-id="454a0-108">Эта функция обеспечивает простой и удобный способ просмотра, установки и удаления сертификатов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="454a0-108">This feature provides a simple and user-friendly way to view, install and remove certificates on your device.</span></span> <span data-ttu-id="454a0-109">С помощью нового диспетчера сертификатов администраторы и пользователи теперь имеют улучшенные средства аудита, диагностики и проверки подлинности для обеспечения безопасности и соответствия устройств.</span><span class="sxs-lookup"><span data-stu-id="454a0-109">With the new Certificate Manager, admins and users now have improved auditing, diagnosis and validation tooling to ensure that devices remain secure and compliant.</span></span> 

-   <span data-ttu-id="454a0-110">**Аудит:** Убедитесь, что сертификат развертывается правильно, или подтвердит, что он был удален надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="454a0-110">**Auditing:** Ability to validate that a certificate is deployed correctly or to confirm that it was removed appropriately.</span></span> 
-   <span data-ttu-id="454a0-111">**Диагностика.** При возникновении проблем с проверкой наличия соответствующих сертификатов на устройстве экономит время и помогает в устранении неполадок.</span><span class="sxs-lookup"><span data-stu-id="454a0-111">**Diagnosis:** When issues arise, validating that the appropriate certificates exist on the device saves time and helps with troubleshooting.</span></span> 
-   <span data-ttu-id="454a0-112">**Проверка:** Проверка того, что сертификат предназначен для целей и является работоспособным, может значительно экономить время, особенно в коммерческих средах, прежде чем развертывать сертификаты на более крупных масштабах.</span><span class="sxs-lookup"><span data-stu-id="454a0-112">**Validation:** Verifying that a certificate serves the intended purpose and is functional, can save significant time, particularly in commercial environments before deploying certificates at larger scale.</span></span>

<span data-ttu-id="454a0-113">Чтобы быстро найти определенный сертификат в списке, можно выполнить сортировку по имени, дате или времени окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="454a0-113">To find a specific certificate in the list quickly, there are options to sort by name, store or expiration date.</span></span> <span data-ttu-id="454a0-114">Пользователи также могут прямо искать сертификат.</span><span class="sxs-lookup"><span data-stu-id="454a0-114">Users may also directly search for a certificate.</span></span> <span data-ttu-id="454a0-115">Чтобы просмотреть индивидуальные свойства сертификата, выберите сертификат и нажмите кнопку **сведения**.</span><span class="sxs-lookup"><span data-stu-id="454a0-115">To view individual certificate properties, select the certificate and click on **Info**.</span></span> 

<span data-ttu-id="454a0-116">Установка сертификата в настоящее время поддерживает файлы. cer и. CRT.</span><span class="sxs-lookup"><span data-stu-id="454a0-116">Certificate installation currently supports .cer and .crt files.</span></span> <span data-ttu-id="454a0-117">Владельцы устройств могут устанавливать сертификаты на локальный компьютер и в текущий пользователь;  все остальные пользователи могут устанавливаться только в текущий пользователь.</span><span class="sxs-lookup"><span data-stu-id="454a0-117">Device Owners can install certificates in Local Machine and Current User;  all other users can only install into Current User.</span></span> <span data-ttu-id="454a0-118">Пользователи могут удалять только сертификаты, установленные непосредственно из пользовательского интерфейса параметров.</span><span class="sxs-lookup"><span data-stu-id="454a0-118">Users can only remove certificates installed directly from the Settings UI.</span></span> <span data-ttu-id="454a0-119">Если сертификат установлен с другими средствами, его также необходимо удалить с помощью одного и того же механизма.</span><span class="sxs-lookup"><span data-stu-id="454a0-119">If a certificate has been installed through other means, it must also be removed by the same mechanism.</span></span>

## <span data-ttu-id="454a0-120">Чтобы установить сертификат, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="454a0-120">To install a certificate:</span></span> 

1.  <span data-ttu-id="454a0-121">Подключите устройство HoloLens 2 к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="454a0-121">Connect your HoloLens 2 to a PC.</span></span>
1.  <span data-ttu-id="454a0-122">Поместите файл сертификата, который вы хотите установить, в папку HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="454a0-122">Place the certificate file you want to install in a location on your HoloLens 2.</span></span>
1.  <span data-ttu-id="454a0-123">Перейдите к **приложению параметры > обновить сертификаты & безопасности >** и выберите установить сертификат.</span><span class="sxs-lookup"><span data-stu-id="454a0-123">Navigate to **Settings App > Update & Security > Certificates**, and select Install a certificate.</span></span>
1.  <span data-ttu-id="454a0-124">Нажмите кнопку **Импорт файла** и перейдите в папку, в которой вы сохранили сертификат.</span><span class="sxs-lookup"><span data-stu-id="454a0-124">Click **Import File** and navigate to the location you saved the certificate.</span></span>
1.  <span data-ttu-id="454a0-125">Выберите **Расположение магазина**.</span><span class="sxs-lookup"><span data-stu-id="454a0-125">Select **Store Location**.</span></span>
1.  <span data-ttu-id="454a0-126">Выберите **хранилище сертификатов**.</span><span class="sxs-lookup"><span data-stu-id="454a0-126">Select **Certificate Store**.</span></span>
1.  <span data-ttu-id="454a0-127">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="454a0-127">Click **Install**.</span></span>

<span data-ttu-id="454a0-128">Теперь сертификат должен быть установлен на устройстве.</span><span class="sxs-lookup"><span data-stu-id="454a0-128">The certificate should now be installed on the device.</span></span>

## <span data-ttu-id="454a0-129">Чтобы удалить сертификат, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="454a0-129">To remove a certificate:</span></span> 
1. <span data-ttu-id="454a0-130">Перейдите к **приложению "Параметры" > "обновление и безопасность > сертификаты**".</span><span class="sxs-lookup"><span data-stu-id="454a0-130">Navigate to **Settings App > Update and Security > Certificates**.</span></span>
1. <span data-ttu-id="454a0-131">Найдите сертификат по имени в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="454a0-131">Search for the certificate by name in the search box.</span></span>
1. <span data-ttu-id="454a0-132">Выберите сертификат.</span><span class="sxs-lookup"><span data-stu-id="454a0-132">Select the certificate.</span></span>
1. <span data-ttu-id="454a0-133">Нажмите кнопку **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="454a0-133">Click **Remove**</span></span>
1. <span data-ttu-id="454a0-134">При появлении запроса на подтверждение нажмите кнопку **Да** .</span><span class="sxs-lookup"><span data-stu-id="454a0-134">Select **Yes** when prompted for confirmation.</span></span>


![Средство просмотра сертификатов в приложении "Параметры" в разделе Ceritifcates](images/certificate-viewer-device.jpg)

![Рисунок, в котором показано, как использовать пользовательский интерфейс сертификата для установки сертификата в настройках.](images/certificate-device-install.jpg)
