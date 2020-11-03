---
title: Как загрузить и установить приложения с помощью установщика приложений HoloLens 2
description: Загрузка и установка приложений через пользовательский интерфейс
keywords: Управление приложениями, приложение, hololens, установщик приложений
author: evmill
ms.author: v-evmill
ms.reviewer: qizho
ms.date: 10/26/2020
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 415733bb2809b7ae2808edc097423f8928910c57
ms.sourcegitcommit: c4fd9a87bb7c728c73418f95a1b15dd93b0af7c6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2020
ms.locfileid: "11150920"
---
# <span data-ttu-id="4b4f0-104">Установка приложений на HoloLens 2 с помощью установщика приложений</span><span class="sxs-lookup"><span data-stu-id="4b4f0-104">Install Apps on HoloLens 2 via App Installer</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b4f0-105">Эта функция в настоящее время avalible только в сборках участников программы предварительной оценки Windows (19041.1377 +).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-105">This feature is currently only avalible in Windows Insider builds 19041.1377+.</span></span> <span data-ttu-id="4b4f0-106">[Узнайте больше о том, как зарегистрироваться в сборках для участников программы предварительной оценки Windows](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-106">[Learn more on how to enroll in Windows Insider builds](hololens-insider.md).</span></span>

<span data-ttu-id="4b4f0-107">В нашем выпуске программы предварительной оценки Windows мы **добавляем новую возможность (установщик приложений), позволяющую вам более эффективно устанавливать приложения** на устройствах HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-107">In our Windows Insider release, we are **adding a new capability (App Installer) to allow you to install applications more seamlessly** on your HoloLens 2 devices.</span></span> <span data-ttu-id="4b4f0-108">Функция будет включена по **умолчанию для неуправляемых устройств**.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-108">The feature will be **on by default for unmanaged devices**.</span></span> <span data-ttu-id="4b4f0-109">Чтобы предотвратить перерывы в работе предприятий, в настоящее время установщик приложений будет **недоступен для управляемых устройств** .</span><span class="sxs-lookup"><span data-stu-id="4b4f0-109">To prevent disruption to enterprises, app installer will be **not be available for managed devices** at this time.</span></span>  

<span data-ttu-id="4b4f0-110">Устройство считается "управляемым", если выполняется **одно** из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="4b4f0-110">A device is considered “managed” if **any** of the following are true:</span></span>
- <span data-ttu-id="4b4f0-111">[Регистрация](hololens-enroll-mdm.md) для MDM</span><span class="sxs-lookup"><span data-stu-id="4b4f0-111">MDM [Enrolled](hololens-enroll-mdm.md)</span></span>
- <span data-ttu-id="4b4f0-112">Настройка с помощью [пакета подготовки](hololens-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="4b4f0-112">Configured with [provisioning package](hololens-provisioning.md)</span></span>
- <span data-ttu-id="4b4f0-113">[Удостоверение](hololens-identity.md) пользователя — AAD</span><span class="sxs-lookup"><span data-stu-id="4b4f0-113">User [Identity](hololens-identity.md) is AAD</span></span>

<span data-ttu-id="4b4f0-114">Теперь вы можете устанавливать приложения, не требуя включения режима разработчика или портала устройств.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-114">You are now able to install Apps without needing to enable Developer Mode or using Device Portal.</span></span>  <span data-ttu-id="4b4f0-115">Просто загрузите пакет appx (через USB или через EDGE) на устройство и перейдите в комплект appx в проводнике, чтобы получить запрос на отключение установки.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-115">Simply download (over USB or through Edge) the Appx Bundle to your device and navigate to the Appx Bundle in the File Explorer to be prompted to kick off the installation.</span></span>  <span data-ttu-id="4b4f0-116">Кроме того, можно [начать установку с веб-страницы](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-116">Alternatively, [initiate an install from a web page](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web).</span></span>  <span data-ttu-id="4b4f0-117">Точно так же, как и приложения, устанавливаемые из Microsoft Store или неопубликованного с помощью [средства](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool) развертывания бизнес-приложений для MDM, приложения должны иметь цифровую подпись на устройстве HoloLens, и [сертификат, используемый для подписания, должен быть надежным для](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool#security-considerations) того, чтобы приложение могло быть развернуто.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-117">Just like apps you install from the Microsoft Store or sideload using MDM’s LOB App deployment capability, apps need to be digitally signed with the [Sign Tool](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool) and the [certificate used to sign must be trusted](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool#security-considerations) by the HoloLens device before the app can be deployed.</span></span>   

## <span data-ttu-id="4b4f0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4b4f0-118">Requirements</span></span>

### <span data-ttu-id="4b4f0-119">Для ваших устройств:</span><span class="sxs-lookup"><span data-stu-id="4b4f0-119">For your devices:</span></span> 
> [!NOTE]
> <span data-ttu-id="4b4f0-120">Эта функция в настоящее время avalible только в сборках участников программы предварительной оценки Windows (19041.1377 +).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-120">This feature is currently only avalible in Windows Insider builds 19041.1377+.</span></span> <span data-ttu-id="4b4f0-121">[Узнайте больше о том, как зарегистрироваться в сборках для участников программы предварительной оценки Windows](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-121">[Learn more on how to enroll in Windows Insider builds](hololens-insider.md).</span></span>

### <span data-ttu-id="4b4f0-122">Для ваших приложений:</span><span class="sxs-lookup"><span data-stu-id="4b4f0-122">For your apps:</span></span> 
<span data-ttu-id="4b4f0-123">Конфигурация решения для вашего приложения должна быть **основной** или **выпуском** , так как установщик приложения будет использовать зависимости из магазина.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-123">Your app’s Solution Configuration must be either **Master** or **Release** as the App Installer will use dependencies from the store.</span></span> <span data-ttu-id="4b4f0-124">Ознакомьтесь с дополнительными сведениями о [создании пакетов приложений](https://docs.microsoft.com/windows/msix/app-installer/create-appinstallerfile-vs).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-124">See more about [creating app packages](https://docs.microsoft.com/windows/msix/app-installer/create-appinstallerfile-vs).</span></span>

<span data-ttu-id="4b4f0-125">Приложения, установленные с помощью этого метода, должны иметь цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-125">Apps that are installed via this method must be digitally signed.</span></span> <span data-ttu-id="4b4f0-126">Для подписывания приложения вам потребуется использовать сертификат.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-126">You'll need to use a certificate to sign the app.</span></span> <span data-ttu-id="4b4f0-127">Вы можете получить сертификат из списка, который является [доверенным центром сертификации MS](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT), и в этом случае вам не потребуется предпринимать дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-127">You can either get a certificate from the [MS Trusted CA List](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT), in which case you won't need to take any additional action.</span></span> <span data-ttu-id="4b4f0-128">Кроме того, вы можете подписать собственный сертификат, но этот сертификат нужно будет подавать на устройство.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-128">Or you can sign your own certificate however that certificate will need to be pushed onto the device.</span></span> 
- <span data-ttu-id="4b4f0-129">Как подписывать приложения [с помощью средства Sign.](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool)</span><span class="sxs-lookup"><span data-stu-id="4b4f0-129">How to sign apps [using the Sign Tool.](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool)</span></span>

**<span data-ttu-id="4b4f0-130">Параметры сертификата.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-130">Certificate options:</span></span>** 
- [<span data-ttu-id="4b4f0-131">Список доверенных центров сертификации MS</span><span class="sxs-lookup"><span data-stu-id="4b4f0-131">MS Trusted CA List</span></span>](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT)

**<span data-ttu-id="4b4f0-132">Выберите способ развертывания сертификата.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-132">Pick a certificate deployment method.</span></span>** 
- <span data-ttu-id="4b4f0-133">[Пакеты подготовки](hololens-provisioning.md) можно применять к локальным устройствам.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-133">[Provisioning Packages](hololens-provisioning.md) can be applied to local devices.</span></span>
- <span data-ttu-id="4b4f0-134">MDM можно использовать для [применения сертификатов в конфигурациях устройств](https://docs.microsoft.com/mem/intune/protect/certificates-configure).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-134">MDM can be used to [apply certificates with device configurations](https://docs.microsoft.com/mem/intune/protect/certificates-configure).</span></span>
- <span data-ttu-id="4b4f0-135">Используйте [Диспетчер сертификатов](hololens-insider.md#certificate-manager)устройств.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-135">Use the on device [Certificate Manager](hololens-insider.md#certificate-manager).</span></span> 

## <span data-ttu-id="4b4f0-136">Способ установки</span><span class="sxs-lookup"><span data-stu-id="4b4f0-136">Installation method</span></span>

1.  <span data-ttu-id="4b4f0-137">Убедитесь, что ваше устройство не считается управляемым.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-137">Ensure that your device is not considered managed.</span></span>
1.  <span data-ttu-id="4b4f0-138">Убедитесь, что устройство HoloLens 2 включено и вы вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-138">Ensure that your HoloLens 2 device is powered on and you are signed in.</span></span>
1.  <span data-ttu-id="4b4f0-139">На своем ПК перейдите в свое собственное приложение и скопируйте yourapp. appxbundle в yourdevicename\Internal Storage\Downloads.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-139">On your PC navigate to your custom app, and copy yourapp.appxbundle to yourdevicename\Internal Storage\Downloads.</span></span> 
    <span data-ttu-id="4b4f0-140">После того как вы закончите копирование файла, вы можете отключить устройство и завершить установку позже.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-140">After your finish copying your file you may disconnect your device and finish the install later.</span></span>
1.  <span data-ttu-id="4b4f0-141">На устройстве HoloLens 2 Откройте **меню Пуск**, выберите **все приложения** и запустите приложение **проводник** .</span><span class="sxs-lookup"><span data-stu-id="4b4f0-141">From your HoloLens 2 device Open the **Start Menu**, select **All apps** and launch the **File Explorer** app.</span></span>
1.  <span data-ttu-id="4b4f0-142">Перейдите в папку Downloads (загрузки).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-142">Navigate to the Downloads folder.</span></span> <span data-ttu-id="4b4f0-143">Вам может потребоваться сначала выбрать **это устройство** на левой панели приложения, а затем перейти к разделу Downloads (загрузки).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-143">You may need to on the left panel of the app select **This device** first, then navigate to Downloads.</span></span>
1.  <span data-ttu-id="4b4f0-144">Выберите файл yourapp. appxbundle.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-144">Select the yourapp.appxbundle file.</span></span> 
1.  <span data-ttu-id="4b4f0-145">Запустится установщик приложения.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-145">The App Installer will launch.</span></span> <span data-ttu-id="4b4f0-146">Нажмите кнопку " **установить** ", чтобы установить приложение.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-146">Select the **Install** button to install your app.</span></span> 

<span data-ttu-id="4b4f0-147">Установленное приложение будет автоматически запускаться после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-147">The installed app will automatically launch upon the completion of installing.</span></span> 

![Установка примеров MRTK с помощью установщика приложений](images/hololens-app-installer-picture.jpg)

### <span data-ttu-id="4b4f0-149">Устранение неполадок при установке</span><span class="sxs-lookup"><span data-stu-id="4b4f0-149">Troubleshooting Installs</span></span>
<span data-ttu-id="4b4f0-150">Если не удалось установить приложение, проверьте следующее:</span><span class="sxs-lookup"><span data-stu-id="4b4f0-150">If your app failed to install check the following:</span></span>
-   <span data-ttu-id="4b4f0-151">Ваше приложение является либо главным, либо построением выпуска.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-151">Your app is either a Master or Release build.</span></span>
- <span data-ttu-id="4b4f0-152">Ваше устройство обновится до сборки, для которой эта функция доступна.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-152">Your device is updated to a build on which this feature is available.</span></span> 
-   <span data-ttu-id="4b4f0-153">Вы [подключены к Интернету](hololens-network.md).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-153">You are [connected to the internet](hololens-network.md).</span></span>
-   <span data-ttu-id="4b4f0-154">Ваши [конечные точки для Microsoft Store](hololens-offline.md) настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-154">Your [endpoints for the Microsoft Store](hololens-offline.md) are correctly configured.</span></span>  

## <span data-ttu-id="4b4f0-155">Веб-установщик</span><span class="sxs-lookup"><span data-stu-id="4b4f0-155">Web Installer</span></span>

<span data-ttu-id="4b4f0-156">Пользователи могут установить приложение непосредственно с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-156">Users can install an app directly from a web server.</span></span> <span data-ttu-id="4b4f0-157">Это позволяет использовать установщик приложений в сочетании с простым способом загрузки и установки.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-157">This takes use of the App Installer combined with an easy download and install distribution method.</span></span> 

### <span data-ttu-id="4b4f0-158">Настройка веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-158">How to set up web install:</span></span>
1.  <span data-ttu-id="4b4f0-159">Убедитесь, что ваше приложение правильно настроено для установки.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-159">Ensure your app is correctly configured to install.</span></span>
1.  <span data-ttu-id="4b4f0-160">[Чтобы включить эту функцию на веб-странице](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web#how-to-enable-this-on-a-webpage), выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-160">Follow these [steps to enable this on a web page](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web#how-to-enable-this-on-a-webpage).</span></span> 

### <span data-ttu-id="4b4f0-161">Работа с конечными пользователями:</span><span class="sxs-lookup"><span data-stu-id="4b4f0-161">End user experience:</span></span>
1. <span data-ttu-id="4b4f0-162">Пользователь получает и устанавливает сертификат на устройство с помощью метода, ранее выбранного выше.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-162">User receives and installs certificate to the device using a method previously chosen above.</span></span> 
1. <span data-ttu-id="4b4f0-163">Пользователь посещает URL-адрес, созданный на этапе, описанном выше.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-163">User visits the URL created from the step above.</span></span>

<span data-ttu-id="4b4f0-164">Теперь приложение будет установлено на устройстве.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-164">The app will now install to the device.</span></span> <span data-ttu-id="4b4f0-165">Чтобы найти приложение, откройте **меню "Пуск** " и нажмите кнопку " **все приложения** ", чтобы найти приложение.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-165">To find the app open the **Start menu** and select the **All apps** button to find your app.</span></span> 

-   <span data-ttu-id="4b4f0-166">Инструкции по устранению неполадок, возникающих при установке, можно найти в статье [Устранение неполадок установщика приложений](https://docs.microsoft.com/windows/msix/app-installer/troubleshoot-appinstaller-issues).</span><span class="sxs-lookup"><span data-stu-id="4b4f0-166">For help troubleshooting this installation method please visit [troubleshoot app installer issues](https://docs.microsoft.com/windows/msix/app-installer/troubleshoot-appinstaller-issues).</span></span> 

> [!NOTE]
> <span data-ttu-id="4b4f0-167">Пользовательский интерфейс в процессе обновления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-167">UI during the update process is not supported.</span></span> <span data-ttu-id="4b4f0-168">Таким образом, параметр ShowPrompt на [этой странице](https://docs.microsoft.com/windows/msix/app-installer/update-settings) и соответствующие параметры не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-168">So the ShowPrompt option on [this page](https://docs.microsoft.com/windows/msix/app-installer/update-settings) and related options are not supported.</span></span>

## <span data-ttu-id="4b4f0-169">Примеры приложений</span><span class="sxs-lookup"><span data-stu-id="4b4f0-169">Sample Apps</span></span>

<span data-ttu-id="4b4f0-170">Если вы хотите сделать это с помощью некоторых примеров приложений, ознакомьтесь с некоторыми из наших примеров:</span><span class="sxs-lookup"><span data-stu-id="4b4f0-170">If you'd like to try this out with some sample apps please check out some of our available samples:</span></span>
- [<span data-ttu-id="4b4f0-171">Центр примеров MRTK</span><span class="sxs-lookup"><span data-stu-id="4b4f0-171">MRTK Examples Hub</span></span>](https://microsoft.github.io/MixedRealityToolkit-Unity/Documentation/README_ExampleHub.html)
- [<span data-ttu-id="4b4f0-172">Ложк</span><span class="sxs-lookup"><span data-stu-id="4b4f0-172">Surfaces</span></span>](https://docs.microsoft.com/windows/mixed-reality/develop/unity/sampleapp-surfaces)
- [<span data-ttu-id="4b4f0-173">Примеры приложений UWP, которые можно использовать для тестирования</span><span class="sxs-lookup"><span data-stu-id="4b4f0-173">UWP Sample Apps that can be used for testing</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples)
