---
title: Диспетчер сертификатов
description: Узнайте, как вручную устанавливать, управлять и удалять сертификаты на устройствах смешанной реальности HoloLens 2.
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
ms.openlocfilehash: 9d221321adcb8062206695e3e610d35dee14523e
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283690"
---
# <span data-ttu-id="d11b0-103">Диспетчер сертификатов</span><span class="sxs-lookup"><span data-stu-id="d11b0-103">Certificate Manager</span></span>

- <span data-ttu-id="d11b0-104">Улучшены инструменты аудита, диагностики и проверки для обеспечения безопасности и соответствия устройств требованиям с помощью нового диспетчера сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d11b0-104">Improved auditing, diagnosis, and validation tooling for device security and compliance through the new Certificate Manager.</span></span> <span data-ttu-id="d11b0-105">Эта возможность позволяет развертывать, устранять неполадки и проверять сертификаты масштабно в коммерческих средах.</span><span class="sxs-lookup"><span data-stu-id="d11b0-105">This capability will enable you to deploy, troubleshoot, and validate your certificates at scale in commercial environments.</span></span>

<span data-ttu-id="d11b0-106">В Windows Holographic версии 20H2 мы добавляем диспетчер сертификатов в приложение "Параметры HoloLens 2".</span><span class="sxs-lookup"><span data-stu-id="d11b0-106">In Windows Holographic, version 20H2, we are adding a Certificate Manager in the HoloLens 2 Settings app.</span></span> <span data-ttu-id="d11b0-107">Перейдите **в > обновления & безопасности > сертификатов.**</span><span class="sxs-lookup"><span data-stu-id="d11b0-107">Go to **Settings > Update & Security > Certificates**.</span></span> <span data-ttu-id="d11b0-108">Эта функция предоставляет простой и простой способ просмотра, установки и удаления сертификатов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d11b0-108">This feature provides a simple and user-friendly way to view, install and remove certificates on your device.</span></span> <span data-ttu-id="d11b0-109">С помощью нового диспетчера сертификатов администраторы и пользователи теперь усовершенствовали средства аудита, диагностики и проверки, чтобы обеспечить безопасность и соответствие устройств требованиям.</span><span class="sxs-lookup"><span data-stu-id="d11b0-109">With the new Certificate Manager, admins and users now have improved auditing, diagnosis and validation tooling to ensure that devices remain secure and compliant.</span></span> 

-   <span data-ttu-id="d11b0-110">**Аудит:** Возможность проверки правильности развертывания сертификата или подтверждения правильности его удаления.</span><span class="sxs-lookup"><span data-stu-id="d11b0-110">**Auditing:** Ability to validate that a certificate is deployed correctly or to confirm that it was removed appropriately.</span></span> 
-   <span data-ttu-id="d11b0-111">**Диагностика:** При возникающих проблемах проверка на существования соответствующих сертификатов на устройстве экономит время и помогает устранять неполадки.</span><span class="sxs-lookup"><span data-stu-id="d11b0-111">**Diagnosis:** When issues arise, validating that the appropriate certificates exist on the device saves time and helps with troubleshooting.</span></span> 
-   <span data-ttu-id="d11b0-112">**Проверка:** Проверка того, что сертификат служит назначению и работает, может значительно сэкономить время, особенно в коммерческих средах, прежде чем развертывать сертификаты в крупных масштабах.</span><span class="sxs-lookup"><span data-stu-id="d11b0-112">**Validation:** Verifying that a certificate serves the intended purpose and is functional, can save significant time, particularly in commercial environments before deploying certificates at larger scale.</span></span>

<span data-ttu-id="d11b0-113">Чтобы быстро найти определенный сертификат в списке, можно отсортировать его по имени, даты хранения или срока действия.</span><span class="sxs-lookup"><span data-stu-id="d11b0-113">To find a specific certificate in the list quickly, there are options to sort by name, store or expiration date.</span></span> <span data-ttu-id="d11b0-114">Пользователи также могут напрямую искать сертификат.</span><span class="sxs-lookup"><span data-stu-id="d11b0-114">Users may also directly search for a certificate.</span></span> <span data-ttu-id="d11b0-115">Чтобы просмотреть свойства отдельных сертификатов, выберите сертификат и щелкните **"Сведения".**</span><span class="sxs-lookup"><span data-stu-id="d11b0-115">To view individual certificate properties, select the certificate and click on **Info**.</span></span> 

<span data-ttu-id="d11b0-116">В настоящее время установка сертификатов поддерживает CER- и CRT-файлы.</span><span class="sxs-lookup"><span data-stu-id="d11b0-116">Certificate installation currently supports .cer and .crt files.</span></span> <span data-ttu-id="d11b0-117">Владельцы устройств могут устанавливать сертификаты на локальном компьютере и текущем пользователе;  все остальные пользователи могут устанавливаться только в текущий пользователь.</span><span class="sxs-lookup"><span data-stu-id="d11b0-117">Device Owners can install certificates in Local Machine and Current User;  all other users can only install into Current User.</span></span> <span data-ttu-id="d11b0-118">Пользователи могут удалять только сертификаты, установленные непосредственно из пользовательского интерфейса параметров.</span><span class="sxs-lookup"><span data-stu-id="d11b0-118">Users can only remove certificates installed directly from the Settings UI.</span></span> <span data-ttu-id="d11b0-119">Если сертификат был установлен другими средствами, он также должен быть удален тем же механизмом.</span><span class="sxs-lookup"><span data-stu-id="d11b0-119">If a certificate has been installed through other means, it must also be removed by the same mechanism.</span></span>

## <span data-ttu-id="d11b0-120">Чтобы установить сертификат:</span><span class="sxs-lookup"><span data-stu-id="d11b0-120">To install a certificate:</span></span> 

1.  <span data-ttu-id="d11b0-121">Подключите HoloLens 2 к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="d11b0-121">Connect your HoloLens 2 to a PC.</span></span>
1.  <span data-ttu-id="d11b0-122">Поместите файл сертификата, который необходимо установить, в расположение на holoLens 2.</span><span class="sxs-lookup"><span data-stu-id="d11b0-122">Place the certificate file you want to install in a location on your HoloLens 2.</span></span>
1.  <span data-ttu-id="d11b0-123">Перейдите **в приложение "Параметры" > "Обновление &** безопасности > сертификатов" и выберите "Установить сертификат".</span><span class="sxs-lookup"><span data-stu-id="d11b0-123">Navigate to **Settings App > Update & Security > Certificates**, and select Install a certificate.</span></span>
1.  <span data-ttu-id="d11b0-124">Щелкните **"Импорт файла"** и перейдите в расположение, в который вы сохранили сертификат.</span><span class="sxs-lookup"><span data-stu-id="d11b0-124">Click **Import File** and navigate to the location you saved the certificate.</span></span>
1.  <span data-ttu-id="d11b0-125">Выберите **расположение магазина.**</span><span class="sxs-lookup"><span data-stu-id="d11b0-125">Select **Store Location**.</span></span>
1.  <span data-ttu-id="d11b0-126">Выберите **хранилище сертификатов.**</span><span class="sxs-lookup"><span data-stu-id="d11b0-126">Select **Certificate Store**.</span></span>
1.  <span data-ttu-id="d11b0-127">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="d11b0-127">Click **Install**.</span></span>

<span data-ttu-id="d11b0-128">Сертификат должен быть установлен на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d11b0-128">The certificate should now be installed on the device.</span></span>

## <span data-ttu-id="d11b0-129">Удаление сертификата:</span><span class="sxs-lookup"><span data-stu-id="d11b0-129">To remove a certificate:</span></span> 
1. <span data-ttu-id="d11b0-130">Перейдите **в приложение "Параметры> обновление и безопасность > сертификатов.**</span><span class="sxs-lookup"><span data-stu-id="d11b0-130">Navigate to **Settings App > Update and Security > Certificates**.</span></span>
1. <span data-ttu-id="d11b0-131">Поиск сертификата по имени в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="d11b0-131">Search for the certificate by name in the search box.</span></span>
1. <span data-ttu-id="d11b0-132">Выберите сертификат.</span><span class="sxs-lookup"><span data-stu-id="d11b0-132">Select the certificate.</span></span>
1. <span data-ttu-id="d11b0-133">Нажмите **кнопку "Удалить"**</span><span class="sxs-lookup"><span data-stu-id="d11b0-133">Click **Remove**</span></span>
1. <span data-ttu-id="d11b0-134">Выберите **"Да"** при запросе подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d11b0-134">Select **Yes** when prompted for confirmation.</span></span>


![Просмотр сертификатов в приложении "Параметры" в ceritifcates](images/certificate-viewer-device.jpg)

![Изображение использования пользовательского интерфейса сертификата для установки сертификата в параметрах.](images/certificate-device-install.jpg)
