---
title: Разблокировка функций Windows Holographic for Business
description: При переходе на Windows holographic для бизнеса HoloLens предоставляет дополнительные функции, разработанные для бизнеса.
ms.prod: hololens
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.localizationpriority: medium
ms.date: 9/16/2019
ms.reviewer: ''
manager: jarrettr
appliesto:
- HoloLens (1st gen)
ms.openlocfilehash: 8d42c935e698f156aed894e4fa5012c9f04d8d49
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10829338"
---
# <span data-ttu-id="68197-103">Разблокировка функций Windows Holographic for Business</span><span class="sxs-lookup"><span data-stu-id="68197-103">Unlock Windows Holographic for Business features</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68197-104">Эта страница относится только к HoloLens 1-го поколения.</span><span class="sxs-lookup"><span data-stu-id="68197-104">This page only applies to HoloLens 1st Gen.</span></span>

<span data-ttu-id="68197-105">Microsoft HoloLens поддерживается в версии для *разработчиков*, которые работают под управлением Windows holographic (выпуск Windows 10, разработанный для HoloLens), и в [коммерческом наборе](hololens-commercial-features.md), который предоставляет дополнительные функции, разработанные для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="68197-105">Microsoft HoloLens is available in the *Development Edition*, which runs Windows Holographic (an edition of Windows 10 that is designed for HoloLens), and in the [Commercial Suite](hololens-commercial-features.md), which provides extra features designed for business.</span></span>

<span data-ttu-id="68197-106">При покупке Commercial Suite вы получите лицензию для обновления версии Windows Holographic до Windows Holographic for Business.</span><span class="sxs-lookup"><span data-stu-id="68197-106">When you purchase the Commercial Suite, you receive a license that upgrades Windows Holographic to Windows Holographic for Business.</span></span> <span data-ttu-id="68197-107">Вы можете применить эту лицензию к устройству с помощью [поставщика управления мобильными устройствами (MDM)](#edition-upgrade-by-using-mdm) организации или [пакета подготовки](#edition-upgrade-by-using-a-provisioning-package).</span><span class="sxs-lookup"><span data-stu-id="68197-107">You can apply this license to the device either by using the organization's [mobile device management (MDM) provider](#edition-upgrade-by-using-mdm) or a [provisioning package](#edition-upgrade-by-using-a-provisioning-package).</span></span>

> [!TIP]
> <span data-ttu-id="68197-108">В Windows 10 версии 1803 вы можете убедиться, что HoloLens был обновлен до выпуска Business Edition, выбрав пункт **Параметры**  >  **системы**.</span><span class="sxs-lookup"><span data-stu-id="68197-108">In Windows 10, version 1803, you can check that the HoloLens has been upgraded to the business edition by selecting **Settings** > **System**.</span></span>

## <span data-ttu-id="68197-109">Обновление выпуска с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="68197-109">Edition upgrade by using MDM</span></span>

<span data-ttu-id="68197-110">Корпоративная лицензия может применяться любым поставщиком MDM, который поддерживает [поставщик служб конфигурации (CSP) WindowsLicensing](https://msdn.microsoft.com/library/windows/hardware/dn904983.aspx).</span><span class="sxs-lookup"><span data-stu-id="68197-110">The enterprise license can be applied by any MDM provider that supports the [WindowsLicensing configuration service provider (CSP)](https://msdn.microsoft.com/library/windows/hardware/dn904983.aspx).</span></span> <span data-ttu-id="68197-111">Последняя версия API Microsoft MDM будет поддерживать WindowsLicensing CSP.</span><span class="sxs-lookup"><span data-stu-id="68197-111">The latest version of the Microsoft MDM API will support WindowsLicensing CSP.</span></span>

<span data-ttu-id="68197-112">Пошаговые инструкции по обновлению HoloLens с помощью Microsoft Intune можно найти в статье [обновление устройств под управлением Windows holographic и Windows holographic для бизнеса](https://docs.microsoft.com/intune/holographic-upgrade).</span><span class="sxs-lookup"><span data-stu-id="68197-112">For step-by-step instructions for upgrading HoloLens by using Microsoft Intune, see [Upgrade devices running Windows Holographic to Windows Holographic for Business](https://docs.microsoft.com/intune/holographic-upgrade).</span></span>

 <span data-ttu-id="68197-113">Определенные инструкции по настройке и развертыванию политики для других поставщиков систем MDM могут отличаться.</span><span class="sxs-lookup"><span data-stu-id="68197-113">On other MDM providers, the specific steps for setting up and deploying the policy might vary.</span></span>

## <span data-ttu-id="68197-114">Обновление выпусков с помощью пакета подготовки</span><span class="sxs-lookup"><span data-stu-id="68197-114">Edition upgrade by using a provisioning package</span></span>

<span data-ttu-id="68197-115">Пакеты подготовки — это файлы, создаваемые конструктором конфигураций Windows, которые применяются к заданной конфигурации на устройстве.</span><span class="sxs-lookup"><span data-stu-id="68197-115">Provisioning packages are files created by the Windows Configuration Designer tool that apply a specified configuration to a device.</span></span>

### <span data-ttu-id="68197-116">Создание пакета подготовки, который выполняет обновление выпуска Windows Holographic</span><span class="sxs-lookup"><span data-stu-id="68197-116">Create a provisioning package that upgrades the Windows Holographic edition</span></span>

1. [<span data-ttu-id="68197-117">Создание пакета подготовки для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="68197-117">Create a provisioning package for HoloLens.</span></span>](hololens-provisioning.md)
1. <span data-ttu-id="68197-118">Перейдите в раздел **Параметры среды выполнения** > **EditionUpgrade**и выберите **EditionUpgradeWithLicense**.</span><span class="sxs-lookup"><span data-stu-id="68197-118">Go to **Runtime settings** > **EditionUpgrade**, and select **EditionUpgradeWithLicense**.</span></span>

    ![Обновление выпуска с использованием выбранного параметра лицензии](images/icd1.png)

1. <span data-ttu-id="68197-120">Найдите файл лицензии XML, предоставленный при приобретении коммерческого набора.</span><span class="sxs-lookup"><span data-stu-id="68197-120">Find the XML license file that was provided when you purchased the Commercial Suite.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68197-121">Вы можете настроить [дополнительные параметры в пакете подготовки](hololens-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="68197-121">You can configure [additional settings in the provisioning package](hololens-provisioning.md).</span></span>

1. <span data-ttu-id="68197-122">В меню **файл** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="68197-122">On the **File** menu, select **Save**.</span></span> 

1. <span data-ttu-id="68197-123">Ознакомьтесь с предупреждением о том, что файлы проекта могут содержать конфиденциальные данные, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="68197-123">Read the warning that project files may contain sensitive information and click **OK**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="68197-124">При создании пакета подготовки вы можете включить конфиденциальную информацию в файлы проекта и файл пакета подготовки (. ppkg).</span><span class="sxs-lookup"><span data-stu-id="68197-124">When you build a provisioning package, you may include sensitive information in the project files and provisioning package (.ppkg) file.</span></span> <span data-ttu-id="68197-125">Несмотря на то что у вас есть возможность шифрования PPKG-файла, файлы проекта не шифруются.</span><span class="sxs-lookup"><span data-stu-id="68197-125">Although you have the option to encrypt the .ppkg file, project files are not encrypted.</span></span> <span data-ttu-id="68197-126">Файлы проекта следует хранить в безопасном месте и удалять их, когда они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="68197-126">You should store the project files in a secure location and delete the project files when no longer needed.</span></span>

1. <span data-ttu-id="68197-127">В меню **Экспорт** выберите пункт **Пакет подготовки**.</span><span class="sxs-lookup"><span data-stu-id="68197-127">On the **Export** menu, select **Provisioning package**.</span></span>

1. <span data-ttu-id="68197-128">Измените **владельца** для **ИТ-администратора**, чтобы настроить приоритет этого пакета подготовки на более высоком уровне, чем другие, примененные к этому устройству из разных источников, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="68197-128">Change **Owner** to **IT Admin**, which sets the precedence of this provisioning package to be higher than others applied to this device from different sources, and then select **Next**.</span></span>

1. <span data-ttu-id="68197-129">Задайте значение параметра **Версия пакета**.</span><span class="sxs-lookup"><span data-stu-id="68197-129">Set a value for **Package Version**.</span></span>

    > [!TIP]
    > <span data-ttu-id="68197-130">Можно внести изменения в существующие пакеты и изменить номер версии для обновления ранее примененных пакетов.</span><span class="sxs-lookup"><span data-stu-id="68197-130">You can make changes to existing packages and change the version number to update previously applied packages.</span></span>

1. <span data-ttu-id="68197-131">На странице **Выбор параметров безопасности для пакета подготовки**нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="68197-131">On **Select security details for the provisioning package**, select **Next**.</span></span>

1. <span data-ttu-id="68197-132">Нажмите кнопку **Далее** , чтобы указать расположение, в которое нужно добавить пакет подготовки после его сборки.</span><span class="sxs-lookup"><span data-stu-id="68197-132">Select **Next** to specify the output location where you want the provisioning package to go once it's built.</span></span> <span data-ttu-id="68197-133">По умолчанию Windows ICD использует папку проекта в качестве расположения выходных данных.</span><span class="sxs-lookup"><span data-stu-id="68197-133">By default, Windows ICD uses the project folder as the output location.</span></span>

    <span data-ttu-id="68197-134">Кроме того, вы можете нажать кнопку **Обзор** , чтобы изменить расположение для вывода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="68197-134">Optionally, you can select **Browse** to change the default output location.</span></span>

1. <span data-ttu-id="68197-135">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="68197-135">Select **Next**.</span></span>

1. <span data-ttu-id="68197-136">Нажмите кнопку **построить** , чтобы приступить к созданию пакета.</span><span class="sxs-lookup"><span data-stu-id="68197-136">Select **Build** to start building the package.</span></span> <span data-ttu-id="68197-137">На странице "сборка" отображаются сведения о проекте, а индикатор выполнения показывает состояние сборки.</span><span class="sxs-lookup"><span data-stu-id="68197-137">The build page displays the project information, and the progress bar indicates the build status.</span></span>

1. <span data-ttu-id="68197-138">Когда сборка завершится, нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="68197-138">When the build completes, select **Finish**.</span></span>

### <span data-ttu-id="68197-139">Применение пакета подготовки к HoloLens</span><span class="sxs-lookup"><span data-stu-id="68197-139">Apply the provisioning package to HoloLens</span></span>

1. <span data-ttu-id="68197-140">Подключите устройство к компьютеру с помощью USB-кабеля.</span><span class="sxs-lookup"><span data-stu-id="68197-140">Using the USB cable, connect the device to a PC.</span></span> <span data-ttu-id="68197-141">Запустите устройство, но не продолжайте пользоваться страницей **вписать** в начальной настройке (первая страница с синим прямоугольником).</span><span class="sxs-lookup"><span data-stu-id="68197-141">Start the device, but do not continue past the **fit** page of the initial setup experience (the first page with the blue box).</span></span> <span data-ttu-id="68197-142">На компьютере HoloLens отображается как устройство в проводнике.</span><span class="sxs-lookup"><span data-stu-id="68197-142">On the PC, HoloLens shows up as a device in File Explorer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68197-143">Если устройство HoloLens работает под управлением Windows 10 версии 1607 или более ранней, откройте проводник, ненадолго нажав и открыв на устройстве кнопки **громкости** **и отключения** звука.</span><span class="sxs-lookup"><span data-stu-id="68197-143">If the HoloLens device is running Windows 10, version 1607 or earlier, open File Explorer by briefly pressing and releasing the **Volume Down** and **Power** buttons simultaneously on the device.</span></span>

1. <span data-ttu-id="68197-144">В проводнике перетащите пакет подготовки (.ppkg) в раздел хранения данных на устройстве.</span><span class="sxs-lookup"><span data-stu-id="68197-144">In File Explorer, drag and drop the provisioning package (.ppkg) onto the device storage.</span></span>

1. <span data-ttu-id="68197-145">Несмотря на то, что HoloLens по-прежнему находится на странице " **вписать** ", ненадолго нажимайте и отпустите кнопки " **Громкость** " и " **включить** " одновременно.</span><span class="sxs-lookup"><span data-stu-id="68197-145">While HoloLens is still on the **fit** page, briefly press and release the **Volume Down** and **Power** buttons simultaneously again.</span></span>

1. <span data-ttu-id="68197-146">HoloLens попросит вас подтвердить, что вы доверяете пакету и хотите применить его.</span><span class="sxs-lookup"><span data-stu-id="68197-146">HoloLens asks you if you trust the package and would like to apply it.</span></span> <span data-ttu-id="68197-147">Подтвердите, что доверяете пакету.</span><span class="sxs-lookup"><span data-stu-id="68197-147">Confirm that you trust the package.</span></span>

1. <span data-ttu-id="68197-148">Вы увидите, успешно ли прошло применение пакета.</span><span class="sxs-lookup"><span data-stu-id="68197-148">You will see whether the package was applied successfully or not.</span></span> <span data-ttu-id="68197-149">Если он не был успешно применен, вы можете исправить пакет и повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="68197-149">If it was not applied successfully, you can fix your package and try again.</span></span> <span data-ttu-id="68197-150">В случае успеха продолжайте настройку устройства.</span><span class="sxs-lookup"><span data-stu-id="68197-150">If successful, proceed with device setup.</span></span>
