---
title: Включение шифрования Bitlocker для HoloLens (HoloLens)
description: Включение шифрования устройств BitLocker для защиты файлов, хранящихся в HoloLens
ms.prod: hololens
ms.mktglfcycl: manage
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.localizationpriority: medium
ms.date: 01/26/2019
ms.reviewer: ''
manager: laurawi
appliesto:
- HoloLens (1st gen)
ms.openlocfilehash: 29b9ce346456019dad8e9bc6fd02b104ed4a821d
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10828687"
---
# <span data-ttu-id="fc904-103">Включение шифрования для HoloLens</span><span class="sxs-lookup"><span data-stu-id="fc904-103">Enable encryption for HoloLens</span></span>

<span data-ttu-id="fc904-104">HoloLens (1-го поколения) и HoloLens 2 поддерживают шифрование устройства с помощью BitLocker, однако BitLocker всегда включен для HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="fc904-104">HoloLens (1st gen) and HoloLens 2 both support device encryption using BitLocker, however, BitLocker is always enabled on HoloLens 2.</span></span>

<span data-ttu-id="fc904-105">Эта статья поможет вам включить и настроить BitLocker для HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="fc904-105">This article will help you enable and manage BitLocker on HoloLens (1st gen).</span></span>

<span data-ttu-id="fc904-106">Для HoloLens (1-го поколения) шифрование устройства BitLocker можно включить вручную или с помощью управления мобильными устройствами (MDM).</span><span class="sxs-lookup"><span data-stu-id="fc904-106">On HoloLens (1st gen) you can enable BitLocker device encryption manually or using mobile device management (MDM).</span></span> <span data-ttu-id="fc904-107">Следуйте этим инструкциям, чтобы включить [Шифрование устройства BitLocker](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10#bitlocker-device-encryption) для защиты файлов и информации, хранящейся на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="fc904-107">Follow these instructions to enable [BitLocker device encryption](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10#bitlocker-device-encryption) to protect files and information stored on the HoloLens.</span></span> <span data-ttu-id="fc904-108">Шифрование устройства помогает защитить данные с помощью метода шифрования AES-CBC 128, который эквивалентен [методу EncryptionMethodByDriveType 3](https://docs.microsoft.com/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype) в поставщике службы настройки BitLocker (CSP).</span><span class="sxs-lookup"><span data-stu-id="fc904-108">Device encryption helps protect your data using the AES-CBC 128 encryption method, which is equivalent to [EncryptionMethodByDriveType method 3](https://docs.microsoft.com/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype) in the BitLocker configuration service provider (CSP).</span></span> <span data-ttu-id="fc904-109">Персонал с правильным ключом шифрования (например, паролем) может расшифровать его или выполнить восстановление данных.</span><span class="sxs-lookup"><span data-stu-id="fc904-109">Personnel who have the correct encryption key (such as a password) can decrypt it or perform a data recovery.</span></span>

## <span data-ttu-id="fc904-110">Включение шифрования устройств с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="fc904-110">Enable device encryption using MDM</span></span>

<span data-ttu-id="fc904-111">Поставщик управления мобильными устройствами (MDM) можно использовать для применения политики, требующей шифрования устройств.</span><span class="sxs-lookup"><span data-stu-id="fc904-111">You can use your Mobile Device Management (MDM) provider to apply a policy that requires device encryption.</span></span> <span data-ttu-id="fc904-112">Используемая политика — это [параметр безопасности или RequireDeviceEncryption](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption) в CSP политики.</span><span class="sxs-lookup"><span data-stu-id="fc904-112">The policy to use is the [Security/RequireDeviceEncryption setting](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption) in the Policy CSP.</span></span>

[<span data-ttu-id="fc904-113">Дополнительные сведения о том, как включить шифрование устройства с помощью Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="fc904-113">See instructions for enabling device encryption using Microsoft Intune.</span></span>](https://docs.microsoft.com/intune/compliance-policy-create-windows#windows-holographic-for-business)

<span data-ttu-id="fc904-114">Инструкции по другим инструментам MDM см. в документации вашего поставщика MDM.</span><span class="sxs-lookup"><span data-stu-id="fc904-114">For other MDM tools, see your MDM provider's documentation for instructions.</span></span> <span data-ttu-id="fc904-115">Если поставщику MDM требуется настраиваемый универсальный код ресурса (URI) для шифрования устройства, используйте следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="fc904-115">If your MDM provider requires custom URI for device encryption, use the following configuration:</span></span>

- <span data-ttu-id="fc904-116">**Имя**: введите любое имя</span><span class="sxs-lookup"><span data-stu-id="fc904-116">**Name**: a name of your choice</span></span>
- <span data-ttu-id="fc904-117">**Описание**: необязательно</span><span class="sxs-lookup"><span data-stu-id="fc904-117">**Description**: optional</span></span>
- <span data-ttu-id="fc904-118">**OMA-URI**:</span><span class="sxs-lookup"><span data-stu-id="fc904-118">**OMA-URI**:</span></span> `./Vendor/MSFT/Policy/Config/Security/RequireDeviceEncryption`
- <span data-ttu-id="fc904-119">**Тип данных:** целое число</span><span class="sxs-lookup"><span data-stu-id="fc904-119">**Data type**: integer</span></span>
- <span data-ttu-id="fc904-120">**Значение**:</span><span class="sxs-lookup"><span data-stu-id="fc904-120">**Value**:</span></span> `1`

## <span data-ttu-id="fc904-121">Включение шифрования устройств с помощью пакета подготовки</span><span class="sxs-lookup"><span data-stu-id="fc904-121">Enable device encryption using a provisioning package</span></span>

<span data-ttu-id="fc904-122">Пакеты подготовки — это файлы, создаваемые конструктором конфигураций Windows, которые применяются к заданной конфигурации на устройстве.</span><span class="sxs-lookup"><span data-stu-id="fc904-122">Provisioning packages are files created by the Windows Configuration Designer tool that apply a specified configuration to a device.</span></span> 

### <span data-ttu-id="fc904-123">Создание пакета подготовки для обновления Windows holographic Edition и включения шифрования</span><span class="sxs-lookup"><span data-stu-id="fc904-123">Create a provisioning package that upgrades the Windows Holographic edition and enables encryption</span></span>

1. [<span data-ttu-id="fc904-124">Создайте пакет подготовки для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="fc904-124">Create a provisioning package for HoloLens.</span></span>](hololens-provisioning.md)
1. <span data-ttu-id="fc904-125">Перейдите в раздел **Параметры среды выполнения** > **Политики** > **Безопасность** и выберите **RequireDeviceEncryption**.</span><span class="sxs-lookup"><span data-stu-id="fc904-125">Go to **Runtime settings** > **Policies** > **Security**, and select **RequireDeviceEncryption**.</span></span>

    ![Параметру "Требовать шифрования устройств" установлено значение "Да"](images/device-encryption.png)

1. <span data-ttu-id="fc904-127">Найдите файл лицензии XML, предоставленный при приобретении коммерческого набора.</span><span class="sxs-lookup"><span data-stu-id="fc904-127">Find the XML license file that was provided when you purchased the Commercial Suite.</span></span>

1. <span data-ttu-id="fc904-128">Найдите и выберите XML-файл лицензии, предоставленный при покупке Commercial Suite.</span><span class="sxs-lookup"><span data-stu-id="fc904-128">Browse to and select the XML license file that was provided when you purchased the Commercial Suite.</span></span>
    > [!NOTE]
    > <span data-ttu-id="fc904-129">Вы можете настроить [дополнительные параметры в пакете подготовки](hololens-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="fc904-129">You can configure [additional settings in the provisioning package](hololens-provisioning.md).</span></span>

1. <span data-ttu-id="fc904-130">В меню **Файл** выберите команду **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fc904-130">On the **File** menu, click **Save**.</span></span> 

1. <span data-ttu-id="fc904-131">Ознакомьтесь с предупреждением о том, что файлы проекта могут содержать конфиденциальные данные, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fc904-131">Read the warning explaining that project files may contain sensitive information and click **OK**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="fc904-132">При создании пакета подготовки вы можете включить конфиденциальную информацию в файлы проекта и файл пакета подготовки (. ppkg).</span><span class="sxs-lookup"><span data-stu-id="fc904-132">When you build a provisioning package, you may include sensitive information in the project files and provisioning package (.ppkg) file.</span></span> <span data-ttu-id="fc904-133">Несмотря на то что у вас есть возможность шифрования PPKG-файла, файлы проекта не шифруются.</span><span class="sxs-lookup"><span data-stu-id="fc904-133">Although you have the option to encrypt the .ppkg file, project files are not encrypted.</span></span> <span data-ttu-id="fc904-134">Файлы проекта следует хранить в безопасном месте и удалять их, когда они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="fc904-134">You should store the project files in a secure location and delete the project files when no longer needed.</span></span>

1. <span data-ttu-id="fc904-135">В меню **Экспорт** выберите пункт **Пакет подготовки**.</span><span class="sxs-lookup"><span data-stu-id="fc904-135">On the **Export** menu, click **Provisioning package**.</span></span>
1. <span data-ttu-id="fc904-136">Измените значение параметра **Владелец** на **ИТ-администратор** — это назначит этому пакету подготовки приоритет выше, чем у пакетов подготовки, применяемых к этому устройству из других источников — затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fc904-136">Change **Owner** to **IT Admin**, which will set the precedence of this provisioning package higher than provisioning packages applied to this device from other sources, and then select **Next**.</span></span>
1. <span data-ttu-id="fc904-137">Задайте значение параметра **Версия пакета**.</span><span class="sxs-lookup"><span data-stu-id="fc904-137">Set a value for **Package Version**.</span></span>

    > [!TIP]
    > <span data-ttu-id="fc904-138">Можно внести изменения в существующие пакеты и изменить номер версии для обновления ранее примененных пакетов.</span><span class="sxs-lookup"><span data-stu-id="fc904-138">You can make changes to existing packages and change the version number to update previously applied packages.</span></span>

1. <span data-ttu-id="fc904-139">На этапе **Выбор данных безопасности для пакета подготовки** нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fc904-139">On the **Select security details for the provisioning package**, click **Next**.</span></span>
1. <span data-ttu-id="fc904-140">Нажмите **Далее**, чтобы указать выходное расположение, куда нужно поместить пакет подготовки после сборки.</span><span class="sxs-lookup"><span data-stu-id="fc904-140">Click **Next** to specify the output location where you want the provisioning package to go once it's built.</span></span> <span data-ttu-id="fc904-141">По умолчанию Windows ICD использует папку проекта в качестве расположения выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fc904-141">By default, Windows ICD uses the project folder as the output location.</span></span>

    <span data-ttu-id="fc904-142">Вы также можете нажать Обзор , чтобы изменить расположение выходных данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc904-142">Optionally, you can click Browse to change the default output location.</span></span>

1. <span data-ttu-id="fc904-143">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fc904-143">Click **Next**.</span></span>
1. <span data-ttu-id="fc904-144">Щелкните **Выполнить сборку** , чтобы начать сборку пакета.</span><span class="sxs-lookup"><span data-stu-id="fc904-144">Click **Build** to start building the package.</span></span> <span data-ttu-id="fc904-145">Сведения о проекте отображаются на странице сборки, а индикатор выполнения указывает состояние сборки.</span><span class="sxs-lookup"><span data-stu-id="fc904-145">The project information is displayed in the build page and the progress bar indicates the build status.</span></span>
1. <span data-ttu-id="fc904-146">По завершении сборки нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="fc904-146">When the build completes, click **Finish**.</span></span>

### <span data-ttu-id="fc904-147">Применение пакета подготовки к HoloLens</span><span class="sxs-lookup"><span data-stu-id="fc904-147">Apply the provisioning package to HoloLens</span></span>

1. <span data-ttu-id="fc904-148">Подключите устройство через USB к компьютеру и запустите устройство, но остановитесь на странице **настройки** при первом включении (первая страница с синим прямоугольником).</span><span class="sxs-lookup"><span data-stu-id="fc904-148">Connect the device via USB to a PC and start the device, but do not continue past the **fit** page of the initial setup experience (the first page with the blue box).</span></span>
1. <span data-ttu-id="fc904-149">Одновременно и кратковременно нажмите и отпустите кнопки **уменьшения громкости** и **питания**.</span><span class="sxs-lookup"><span data-stu-id="fc904-149">Briefly press and release the **Volume Down** and **Power** buttons simultaneously.</span></span>
1. <span data-ttu-id="fc904-150">HoloLens отобразится в проводнике на компьютере в качестве внешнего устройства.</span><span class="sxs-lookup"><span data-stu-id="fc904-150">HoloLens will show up as a device in File Explorer on the PC.</span></span>
1. <span data-ttu-id="fc904-151">В проводнике перетащите пакет подготовки (.ppkg) в раздел хранения данных на устройстве.</span><span class="sxs-lookup"><span data-stu-id="fc904-151">In File Explorer, drag and drop the provisioning package (.ppkg) onto the device storage.</span></span>
1. <span data-ttu-id="fc904-152">Снова одновременно и кратковременно нажмите и отпустите кнопки **уменьшения громкости** и **питания**, находясь на странице **настройки**.</span><span class="sxs-lookup"><span data-stu-id="fc904-152">Briefly press and release the **Volume Down** and **Power** buttons simultaneously again while on the **fit** page.</span></span>
1. <span data-ttu-id="fc904-153">Устройство спросит, доверяете ли вы пакету и хотите ли применить его.</span><span class="sxs-lookup"><span data-stu-id="fc904-153">The device will ask you if you trust the package and would like to apply it.</span></span> <span data-ttu-id="fc904-154">Подтвердите, что доверяете пакету.</span><span class="sxs-lookup"><span data-stu-id="fc904-154">Confirm that you trust the package.</span></span>
1. <span data-ttu-id="fc904-155">Вы увидите, успешно ли прошло применение пакета.</span><span class="sxs-lookup"><span data-stu-id="fc904-155">You will see whether the package was applied successfully or not.</span></span> <span data-ttu-id="fc904-156">Если произойдет сбой, можно исправить пакет и повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="fc904-156">If it failed, you can fix your package and try again.</span></span> <span data-ttu-id="fc904-157">Если применение выполнено успешно, продолжите процедуру запуска при первом включении устройства.</span><span class="sxs-lookup"><span data-stu-id="fc904-157">If it succeeded, proceed with device setup.</span></span>

> [!NOTE]
> <span data-ttu-id="fc904-158">Если устройство приобретено до августа 2016 г., вам потребуется выполнить вход на устройство с использованием учетной записи Майкрософт, получить последнее обновление операционной системы и затем переустановить ОС, чтобы применить пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="fc904-158">If the device was purchased before August 2016, you will need to sign into the device with a Microsoft account, get the latest OS update, and then reset the OS in order to apply the provisioning package.</span></span>

## <span data-ttu-id="fc904-159">Проверка шифрования устройств</span><span class="sxs-lookup"><span data-stu-id="fc904-159">Verify device encryption</span></span>

<span data-ttu-id="fc904-160">В HoloLens шифрование осуществляется в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="fc904-160">Encryption is silent on HoloLens.</span></span> <span data-ttu-id="fc904-161">Процедура проверки состояния шифрования устройства:</span><span class="sxs-lookup"><span data-stu-id="fc904-161">To verify the device encryption status:</span></span>

- <span data-ttu-id="fc904-162">На устройстве HoloLens перейдите в раздел **Параметры** > **Система** > **О программе**.</span><span class="sxs-lookup"><span data-stu-id="fc904-162">On HoloLens, go to **Settings** > **System** > **About**.</span></span> <span data-ttu-id="fc904-163">**BitLocker** **включен** , если устройство зашифровано.</span><span class="sxs-lookup"><span data-stu-id="fc904-163">**BitLocker** is **enabled** if the device is encrypted.</span></span> 

    ![Сведения о том, на каком экране включена поддержка BitLocker](images/about-encryption.png)
