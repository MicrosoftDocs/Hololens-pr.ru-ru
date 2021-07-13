---
title: HoloLens Шифрование BitLocker
description: узнайте, как включить шифрование устройства BitLocker для защиты файлов, хранящихся на устройствах HoloLens mixed reality.
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
ms.openlocfilehash: 37efab3ef3d68a9641320e144619008612f6efa2
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113635251"
---
# <a name="hololens-1st-gen-bitlocker-encryption"></a><span data-ttu-id="89e16-103">Шифрование BitLocker для HoloLens (1-го поколения)</span><span class="sxs-lookup"><span data-stu-id="89e16-103">HoloLens (1st Gen) BitLocker Encryption</span></span>

<span data-ttu-id="89e16-104">HoloLens (1-й gen) и HoloLens 2 поддерживают шифрование устройств с помощью bitlocker, однако bitlocker всегда включен на HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="89e16-104">HoloLens (1st gen) and HoloLens 2 both support device encryption using BitLocker, however, BitLocker is always enabled on HoloLens 2.</span></span>

<span data-ttu-id="89e16-105">эта статья поможет вам включить BitLocker и управлять им на HoloLens (1 общий номер).</span><span class="sxs-lookup"><span data-stu-id="89e16-105">This article will help you enable and manage BitLocker on HoloLens (1st gen).</span></span>

<span data-ttu-id="89e16-106">на HoloLens (первое поколение) можно включить шифрование устройства BitLocker вручную или с помощью управления мобильными устройствами (MDM).</span><span class="sxs-lookup"><span data-stu-id="89e16-106">On HoloLens (1st gen) you can enable BitLocker device encryption manually or using mobile device management (MDM).</span></span> <span data-ttu-id="89e16-107">Выполните эти инструкции, чтобы включить [Шифрование устройства BitLocker](/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10#bitlocker-device-encryption) для защиты файлов и данных, хранящихся на HoloLens.</span><span class="sxs-lookup"><span data-stu-id="89e16-107">Follow these instructions to enable [BitLocker device encryption](/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10#bitlocker-device-encryption) to protect files and information stored on the HoloLens.</span></span> <span data-ttu-id="89e16-108">Шифрование устройств помогает защитить данные с помощью метода шифрования AES-CBC 128, который эквивалентен [методу енкриптионмесодбидриветипе 3](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype) в поставщике службы настройки BitLocker (CSP).</span><span class="sxs-lookup"><span data-stu-id="89e16-108">Device encryption helps protect your data using the AES-CBC 128 encryption method, which is equivalent to [EncryptionMethodByDriveType method 3](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype) in the BitLocker configuration service provider (CSP).</span></span> <span data-ttu-id="89e16-109">Персонал, имеющий правильный ключ шифрования (например, пароль), может расшифровать его или выполнить восстановление данных.</span><span class="sxs-lookup"><span data-stu-id="89e16-109">Personnel who have the correct encryption key (such as a password) can decrypt it or perform a data recovery.</span></span>

## <a name="enable-device-encryption-using-mdm"></a><span data-ttu-id="89e16-110">Включение шифрования устройств с помощью MDM</span><span class="sxs-lookup"><span data-stu-id="89e16-110">Enable device encryption using MDM</span></span>

<span data-ttu-id="89e16-111">Поставщик управления мобильными устройствами (MDM) можно использовать для применения политики, требующей шифрования устройства.</span><span class="sxs-lookup"><span data-stu-id="89e16-111">You can use your Mobile Device Management (MDM) provider to apply a policy that requires device encryption.</span></span> <span data-ttu-id="89e16-112">Используемая политика — это [параметр Security/рекуиредевицеенкриптион](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption) в CSP политики.</span><span class="sxs-lookup"><span data-stu-id="89e16-112">The policy to use is the [Security/RequireDeviceEncryption setting](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption) in the Policy CSP.</span></span>

[<span data-ttu-id="89e16-113">См. инструкции по включению шифрования устройств с помощью Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="89e16-113">See instructions for enabling device encryption using Microsoft Intune.</span></span>](/intune/compliance-policy-create-windows#windows-holographic-for-business)

<span data-ttu-id="89e16-114">Инструкции по другим инструментам MDM см. в документации вашего поставщика MDM.</span><span class="sxs-lookup"><span data-stu-id="89e16-114">For other MDM tools, see your MDM provider's documentation for instructions.</span></span> <span data-ttu-id="89e16-115">Если поставщику MDM требуется настраиваемый URI для шифрования устройства, используйте следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="89e16-115">If your MDM provider requires custom URI for device encryption, use the following configuration:</span></span>

- <span data-ttu-id="89e16-116">**Имя**: введите любое имя</span><span class="sxs-lookup"><span data-stu-id="89e16-116">**Name**: a name of your choice</span></span>
- <span data-ttu-id="89e16-117">**Описание**: необязательно</span><span class="sxs-lookup"><span data-stu-id="89e16-117">**Description**: optional</span></span>
- <span data-ttu-id="89e16-118">**OMA-URI**: `./Vendor/MSFT/Policy/Config/Security/RequireDeviceEncryption`</span><span class="sxs-lookup"><span data-stu-id="89e16-118">**OMA-URI**: `./Vendor/MSFT/Policy/Config/Security/RequireDeviceEncryption`</span></span>
- <span data-ttu-id="89e16-119">**Тип данных**: целое число</span><span class="sxs-lookup"><span data-stu-id="89e16-119">**Data type**: integer</span></span>
- <span data-ttu-id="89e16-120">**Значение**: `1`</span><span class="sxs-lookup"><span data-stu-id="89e16-120">**Value**: `1`</span></span>

## <a name="enable-device-encryption-using-a-provisioning-package"></a><span data-ttu-id="89e16-121">Включение шифрования устройств с помощью пакета подготовки</span><span class="sxs-lookup"><span data-stu-id="89e16-121">Enable device encryption using a provisioning package</span></span>

<span data-ttu-id="89e16-122">Пакеты подготовки — это файлы, создаваемые конструктором конфигураций Windows, которые применяются к заданной конфигурации на устройстве.</span><span class="sxs-lookup"><span data-stu-id="89e16-122">Provisioning packages are files created by the Windows Configuration Designer tool that apply a specified configuration to a device.</span></span> 

### <a name="create-a-provisioning-package-that-upgrades-the-windows-holographic-edition-and-enables-encryption"></a><span data-ttu-id="89e16-123">создание пакета подготовки, который обновляет Windows holographic edition и включает шифрование</span><span class="sxs-lookup"><span data-stu-id="89e16-123">Create a provisioning package that upgrades the Windows Holographic edition and enables encryption</span></span>

1. [<span data-ttu-id="89e16-124">Создайте пакет подготовки для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="89e16-124">Create a provisioning package for HoloLens.</span></span>](hololens-provisioning.md)
1. <span data-ttu-id="89e16-125">Перейдите в раздел **Параметры среды выполнения**  >  **политики**  >  **Безопасность** и выберите **рекуиредевицеенкриптион**.</span><span class="sxs-lookup"><span data-stu-id="89e16-125">Go to **Runtime settings** > **Policies** > **Security**, and select **RequireDeviceEncryption**.</span></span>

    ![Параметру "Требовать шифрования устройств" установлено значение "Да"](images/device-encryption.png)

1. <span data-ttu-id="89e16-127">Найдите файл лицензии XML, который был предоставлен при приобретении коммерческого набора.</span><span class="sxs-lookup"><span data-stu-id="89e16-127">Find the XML license file that was provided when you purchased the Commercial Suite.</span></span>

1. <span data-ttu-id="89e16-128">Найдите и выберите XML-файл лицензии, предоставленный при покупке Commercial Suite.</span><span class="sxs-lookup"><span data-stu-id="89e16-128">Browse to and select the XML license file that was provided when you purchased the Commercial Suite.</span></span>
    > [!NOTE]
    > <span data-ttu-id="89e16-129">Вы можете настроить [дополнительные параметры в пакете подготовки](hololens-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="89e16-129">You can configure [additional settings in the provisioning package](hololens-provisioning.md).</span></span>

1. <span data-ttu-id="89e16-130">В меню **File** (Файл) выберите пункт **Save** (Сохранить).</span><span class="sxs-lookup"><span data-stu-id="89e16-130">On the **File** menu, click **Save**.</span></span> 

1. <span data-ttu-id="89e16-131">Прочтите предупреждение о том, что файлы проекта могут содержать конфиденциальные сведения, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="89e16-131">Read the warning explaining that project files may contain sensitive information and click **OK**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="89e16-132">При создании пакета подготовки можно включить конфиденциальную информацию в файлы проекта и файл пакета подготовки (. ppkg).</span><span class="sxs-lookup"><span data-stu-id="89e16-132">When you build a provisioning package, you may include sensitive information in the project files and provisioning package (.ppkg) file.</span></span> <span data-ttu-id="89e16-133">Несмотря на то что у вас есть возможность шифрования PPKG-файла, файлы проекта не шифруются.</span><span class="sxs-lookup"><span data-stu-id="89e16-133">Although you have the option to encrypt the .ppkg file, project files are not encrypted.</span></span> <span data-ttu-id="89e16-134">Файлы проекта следует хранить в безопасном месте и удалять файлы проекта, если они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="89e16-134">You should store the project files in a secure location and delete the project files when no longer needed.</span></span>

1. <span data-ttu-id="89e16-135">В меню **Экспорт** выберите пункт **Пакет подготовки**.</span><span class="sxs-lookup"><span data-stu-id="89e16-135">On the **Export** menu, click **Provisioning package**.</span></span>
1. <span data-ttu-id="89e16-136">Измените значение Owner на **ИТ Admin**( **владелец** ), чтобы задать приоритет пакета подготовки выше, чем подготовка пакетов, примененных к этому устройству из других источников, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="89e16-136">Change **Owner** to **IT Admin**, which will set the precedence of this provisioning package higher than provisioning packages applied to this device from other sources, and then select **Next**.</span></span>
1. <span data-ttu-id="89e16-137">Задайте значение параметра **Версия пакета**.</span><span class="sxs-lookup"><span data-stu-id="89e16-137">Set a value for **Package Version**.</span></span>

    > [!TIP]
    > <span data-ttu-id="89e16-138">Можно внести изменения в существующие пакеты и изменить номер версии для обновления ранее примененных пакетов.</span><span class="sxs-lookup"><span data-stu-id="89e16-138">You can make changes to existing packages and change the version number to update previously applied packages.</span></span>

1. <span data-ttu-id="89e16-139">На этапе **Выбор данных безопасности для пакета подготовки** нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="89e16-139">On the **Select security details for the provisioning package**, click **Next**.</span></span>
1. <span data-ttu-id="89e16-140">Нажмите кнопку **Далее**, чтобы указать конечное расположение, в которое нужно поместить пакет подготовки после сборки.</span><span class="sxs-lookup"><span data-stu-id="89e16-140">Click **Next** to specify the output location where you want the provisioning package to go once it's built.</span></span> <span data-ttu-id="89e16-141">По умолчанию Windows ICD использует папку проекта в качестве расположения для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="89e16-141">By default, Windows ICD uses the project folder as the output location.</span></span>

    <span data-ttu-id="89e16-142">Вы также можете нажать Обзор , чтобы изменить расположение выходных данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89e16-142">Optionally, you can click Browse to change the default output location.</span></span>

1. <span data-ttu-id="89e16-143">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="89e16-143">Click **Next**.</span></span>
1. <span data-ttu-id="89e16-144">Щелкните **Выполнить сборку** , чтобы начать сборку пакета.</span><span class="sxs-lookup"><span data-stu-id="89e16-144">Click **Build** to start building the package.</span></span> <span data-ttu-id="89e16-145">Сведения о проекте отображаются на странице сборки, а индикатор выполнения указывает состояние сборки.</span><span class="sxs-lookup"><span data-stu-id="89e16-145">The project information is displayed in the build page and the progress bar indicates the build status.</span></span>
1. <span data-ttu-id="89e16-146">По завершении сборки нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="89e16-146">When the build completes, click **Finish**.</span></span>

### <a name="apply-the-provisioning-package-to-hololens"></a><span data-ttu-id="89e16-147">Применение пакета подготовки к HoloLens</span><span class="sxs-lookup"><span data-stu-id="89e16-147">Apply the provisioning package to HoloLens</span></span>

1. <span data-ttu-id="89e16-148">Подключите устройство через USB к компьютеру и запустите устройство, но остановитесь на странице **настройки** при первом включении (первая страница с синим прямоугольником).</span><span class="sxs-lookup"><span data-stu-id="89e16-148">Connect the device via USB to a PC and start the device, but do not continue past the **fit** page of the initial setup experience (the first page with the blue box).</span></span>
1. <span data-ttu-id="89e16-149">Одновременно и кратковременно нажмите и отпустите кнопки **уменьшения громкости** и **питания**.</span><span class="sxs-lookup"><span data-stu-id="89e16-149">Briefly press and release the **Volume Down** and **Power** buttons simultaneously.</span></span>
1. <span data-ttu-id="89e16-150">HoloLens отобразится в проводнике на компьютере в качестве внешнего устройства.</span><span class="sxs-lookup"><span data-stu-id="89e16-150">HoloLens will show up as a device in File Explorer on the PC.</span></span>
1. <span data-ttu-id="89e16-151">В проводнике перетащите пакет подготовки (.ppkg) в раздел хранения данных на устройстве.</span><span class="sxs-lookup"><span data-stu-id="89e16-151">In File Explorer, drag and drop the provisioning package (.ppkg) onto the device storage.</span></span>
1. <span data-ttu-id="89e16-152">Снова одновременно и кратковременно нажмите и отпустите кнопки **уменьшения громкости** и **питания**, находясь на странице **настройки**.</span><span class="sxs-lookup"><span data-stu-id="89e16-152">Briefly press and release the **Volume Down** and **Power** buttons simultaneously again while on the **fit** page.</span></span>
1. <span data-ttu-id="89e16-153">Устройство спросит, доверяете ли вы пакету и хотите ли применить его.</span><span class="sxs-lookup"><span data-stu-id="89e16-153">The device will ask you if you trust the package and would like to apply it.</span></span> <span data-ttu-id="89e16-154">Подтвердите, что доверяете пакету.</span><span class="sxs-lookup"><span data-stu-id="89e16-154">Confirm that you trust the package.</span></span>
1. <span data-ttu-id="89e16-155">Вы увидите, успешно ли прошло применение пакета.</span><span class="sxs-lookup"><span data-stu-id="89e16-155">You will see whether the package was applied successfully or not.</span></span> <span data-ttu-id="89e16-156">Если произойдет сбой, можно исправить пакет и повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="89e16-156">If it failed, you can fix your package and try again.</span></span> <span data-ttu-id="89e16-157">Если применение выполнено успешно, продолжите процедуру запуска при первом включении устройства.</span><span class="sxs-lookup"><span data-stu-id="89e16-157">If it succeeded, proceed with device setup.</span></span>

> [!NOTE]
> <span data-ttu-id="89e16-158">Если устройство приобретено до августа 2016 г., вам потребуется выполнить вход на устройство с использованием учетной записи Майкрософт, получить последнее обновление операционной системы и затем переустановить ОС, чтобы применить пакет подготовки.</span><span class="sxs-lookup"><span data-stu-id="89e16-158">If the device was purchased before August 2016, you will need to sign into the device with a Microsoft account, get the latest OS update, and then reset the OS in order to apply the provisioning package.</span></span>

## <a name="verify-device-encryption"></a><span data-ttu-id="89e16-159">Проверка шифрования устройств</span><span class="sxs-lookup"><span data-stu-id="89e16-159">Verify device encryption</span></span>

<span data-ttu-id="89e16-160">В HoloLens шифрование осуществляется в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="89e16-160">Encryption is silent on HoloLens.</span></span> <span data-ttu-id="89e16-161">Процедура проверки состояния шифрования устройства:</span><span class="sxs-lookup"><span data-stu-id="89e16-161">To verify the device encryption status:</span></span>

- <span data-ttu-id="89e16-162">на HoloLens перейдите в раздел **Параметры**  >  **система**  >  **о программе**.</span><span class="sxs-lookup"><span data-stu-id="89e16-162">On HoloLens, go to **Settings** > **System** > **About**.</span></span> <span data-ttu-id="89e16-163">**BitLocker** **включается** , если устройство зашифровано.</span><span class="sxs-lookup"><span data-stu-id="89e16-163">**BitLocker** is **enabled** if the device is encrypted.</span></span> 

    ![О снимке экрана с включенным BitLocker](images/about-encryption.png)
