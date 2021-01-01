---
title: Загрузка неоконной загрузки и установка приложений с помощью установщика приложений HoloLens 2
description: Загрузка слайдов и установка приложений с помощью пользовательского интерфейса
keywords: управление приложениями, приложение, hololens, установщик приложений
author: evmill
ms.author: v-evmill
ms.reviewer: qizho
ms.date: 11/10/2020
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: e52cc2f031c284b619c61ffa04f259f76397faf5
ms.sourcegitcommit: 96dcd015ad24169295690a8ed13ea1bf480e4b9e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/01/2021
ms.locfileid: "11253096"
---
# <span data-ttu-id="b6071-104">Установка приложений на HoloLens 2 с помощью установщика приложений</span><span class="sxs-lookup"><span data-stu-id="b6071-104">Install Apps on HoloLens 2 via App Installer</span></span>

<span data-ttu-id="b6071-105">Мы **добавляем новую** возможность (установщик приложений), которая позволяет легко устанавливать приложения на устройства HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="b6071-105">We are **adding a new capability (App Installer) to allow you to install applications more seamlessly** on your HoloLens 2 devices.</span></span> <span data-ttu-id="b6071-106">Эта функция будет по **умолчанию в неугодных устройствах.**</span><span class="sxs-lookup"><span data-stu-id="b6071-106">The feature will be **on by default for unmanaged devices**.</span></span> <span data-ttu-id="b6071-107">Во избежание нарушения работы предприятия установщик приложений в настоящее время не будет доступен для **управляемых** устройств.</span><span class="sxs-lookup"><span data-stu-id="b6071-107">To prevent disruption to enterprises, app installer will **not be available for managed devices** at this time.</span></span>  

> [!NOTE]
> <span data-ttu-id="b6071-108">Эта функция была доступна в [Windows Holographic версии 20H2 — обновлении за декабрь 2020 г.](hololens-release-notes.md)</span><span class="sxs-lookup"><span data-stu-id="b6071-108">This feature was made available in [Windows Holographic, version 20H2 – December 2020 Update](hololens-release-notes.md).</span></span> <span data-ttu-id="b6071-109">Убедитесь, что [устройство обновлено для](hololens-update-hololens.md) использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="b6071-109">Ensure your device is [updated](hololens-update-hololens.md) to use this feature.</span></span>

<span data-ttu-id="b6071-110">Мы **добавили новую возможность (установщик приложений),** которая позволяет легко устанавливать приложения на устройства HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="b6071-110">We have **added a new capability (App Installer) to allow you to install applications more seamlessly** on your HoloLens 2 devices.</span></span> <span data-ttu-id="b6071-111">Эта функция будет по **умолчанию в неугодных устройствах.**</span><span class="sxs-lookup"><span data-stu-id="b6071-111">The feature will be **on by default for unmanaged devices**.</span></span> <span data-ttu-id="b6071-112">Чтобы предотвратить нарушения работы предприятий, установщик приложений в настоящее время будет не доступен для **управляемых** устройств.</span><span class="sxs-lookup"><span data-stu-id="b6071-112">To prevent disruption to enterprises, app installer will be **not be available for managed devices** at this time.</span></span>  

<span data-ttu-id="b6071-113">Устройство считается управляемым, если **имеется** следующее:</span><span class="sxs-lookup"><span data-stu-id="b6071-113">A device is considered “managed” if **any** of the following are true:</span></span>

- <span data-ttu-id="b6071-114">Регистрация в [](hololens-enroll-mdm.md) MDM</span><span class="sxs-lookup"><span data-stu-id="b6071-114">MDM [Enrolled](hololens-enroll-mdm.md)</span></span>
- <span data-ttu-id="b6071-115">Настроено с [помощью пакета предоставления](hololens-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="b6071-115">Configured with [provisioning package](hololens-provisioning.md)</span></span>
- <span data-ttu-id="b6071-116">Удостоверение [пользователя](hololens-identity.md) — Azure AD</span><span class="sxs-lookup"><span data-stu-id="b6071-116">User [Identity](hololens-identity.md) is Azure AD</span></span>

<span data-ttu-id="b6071-117">Теперь вы можете устанавливать приложения, не влияя на режим разработчика и не используя портал устройств.</span><span class="sxs-lookup"><span data-stu-id="b6071-117">You are now able to install Apps without needing to enable Developer Mode or using Device Portal.</span></span>  <span data-ttu-id="b6071-118">Скачайте (через USB или Через Microsoft Edge) пакет Appx на свое устройство и перейдите к пакету Appx в проводнике, чтобы получить запрос на начало установки.</span><span class="sxs-lookup"><span data-stu-id="b6071-118">Download (over USB or through Microsoft Edge) the Appx Bundle to your device and navigate to the Appx Bundle in the File Explorer to be prompted to kick off the installation.</span></span>  <span data-ttu-id="b6071-119">Или же [инициировать установку с веб-страницы.](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web)</span><span class="sxs-lookup"><span data-stu-id="b6071-119">Alternatively, [initiate an install from a web page](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web).</span></span>  <span data-ttu-id="b6071-120">Как и в приложениях, устанавливаемых из Microsoft Store или загрузке неогрузки с помощью [](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool) возможности развертывания [](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool#security-considerations) LOB-приложений MDM, приложения должны иметь цифровую подпись с помощью средства подписи, а сертификат, используемый для подписи, должен быть доверенным для устройства HoloLens, прежде чем развертывать приложение.</span><span class="sxs-lookup"><span data-stu-id="b6071-120">Just like apps you install from the Microsoft Store or sideload using MDM’s LOB App deployment capability, apps need to be digitally signed with the [Sign Tool](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool) and the [certificate used to sign must be trusted](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool#security-considerations) by the HoloLens device before the app can be deployed.</span></span>

## <span data-ttu-id="b6071-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b6071-121">Requirements</span></span>

### <span data-ttu-id="b6071-122">Для устройств:</span><span class="sxs-lookup"><span data-stu-id="b6071-122">For your devices:</span></span>

 <span data-ttu-id="b6071-123">в настоящее время эта функция доступна в сборках Windows Holographic 20H2 для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="b6071-123">feature is currently available in Windows Holographic 20H2 builds for HoloLens 2 devices.</span></span> <span data-ttu-id="b6071-124">Убедитесь, что все устройства, использующие [этот метод, обновлены.](hololens-update-hololens.md)</span><span class="sxs-lookup"><span data-stu-id="b6071-124">Ensure any devices using this method are [updated](hololens-update-hololens.md).</span></span>

### <span data-ttu-id="b6071-125">Для ваших приложений:</span><span class="sxs-lookup"><span data-stu-id="b6071-125">For your apps:</span></span> 
<span data-ttu-id="b6071-126">Конфигурация решения вашего приложения должна быть либо **Master,** либо **Release,** так как установщик приложений будет использовать зависимости из Магазина.</span><span class="sxs-lookup"><span data-stu-id="b6071-126">Your app’s Solution Configuration must be either **Master** or **Release** as the App Installer will use dependencies from the store.</span></span> <span data-ttu-id="b6071-127">Узнайте больше о [создании пакетов приложений.](https://docs.microsoft.com/windows/msix/app-installer/create-appinstallerfile-vs)</span><span class="sxs-lookup"><span data-stu-id="b6071-127">See more about [creating app packages](https://docs.microsoft.com/windows/msix/app-installer/create-appinstallerfile-vs).</span></span>

<span data-ttu-id="b6071-128">Приложения, установленные с помощью этого метода, должны иметь цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="b6071-128">Apps that are installed via this method must be digitally signed.</span></span> <span data-ttu-id="b6071-129">Для подписывания приложения необходимо использовать сертификат.</span><span class="sxs-lookup"><span data-stu-id="b6071-129">You'll need to use a certificate to sign the app.</span></span> <span data-ttu-id="b6071-130">Вы можете получить сертификат из списка доверенных ЦС [MS,](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT)в этом случае вам не потребуется никаких дополнительных действий.</span><span class="sxs-lookup"><span data-stu-id="b6071-130">You can either get a certificate from the [MS Trusted CA List](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT), in which case you won't need to take any additional action.</span></span> <span data-ttu-id="b6071-131">Кроме того, вы можете подписать собственный сертификат, но этот сертификат необходимо будет на устройстве.</span><span class="sxs-lookup"><span data-stu-id="b6071-131">Or you can sign your own certificate however that certificate will need to be pushed onto the device.</span></span>

- <span data-ttu-id="b6071-132">Как подписывать приложения [с помощью средства подписи.](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool)</span><span class="sxs-lookup"><span data-stu-id="b6071-132">How to sign apps [using the Sign Tool.](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool)</span></span>

**<span data-ttu-id="b6071-133">Параметры сертификата:</span><span class="sxs-lookup"><span data-stu-id="b6071-133">Certificate options:</span></span>**

- [<span data-ttu-id="b6071-134">Список доверенных ЦС MS</span><span class="sxs-lookup"><span data-stu-id="b6071-134">MS Trusted CA List</span></span>](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT)

**<span data-ttu-id="b6071-135">Выберите метод развертывания сертификата.</span><span class="sxs-lookup"><span data-stu-id="b6071-135">Pick a certificate deployment method.</span></span>**

- <span data-ttu-id="b6071-136">[Пакеты подготовка можно](hololens-provisioning.md) применять к локальным устройствам.</span><span class="sxs-lookup"><span data-stu-id="b6071-136">[Provisioning Packages](hololens-provisioning.md) can be applied to local devices.</span></span>
- <span data-ttu-id="b6071-137">MDM можно использовать для применения [сертификатов с конфигурациями устройств.](https://docs.microsoft.com/mem/intune/protect/certificates-configure)</span><span class="sxs-lookup"><span data-stu-id="b6071-137">MDM can be used to [apply certificates with device configurations](https://docs.microsoft.com/mem/intune/protect/certificates-configure).</span></span>
- <span data-ttu-id="b6071-138">Используйте диспетчер сертификатов [на устройстве.](certificate-manager.md)</span><span class="sxs-lookup"><span data-stu-id="b6071-138">Use the on device [Certificate Manager](certificate-manager.md).</span></span>

## <span data-ttu-id="b6071-139">Метод установки</span><span class="sxs-lookup"><span data-stu-id="b6071-139">Installation method</span></span>

1. <span data-ttu-id="b6071-140">Убедитесь, что устройство не считается управляемым.</span><span class="sxs-lookup"><span data-stu-id="b6071-140">Check that your device is not considered managed.</span></span>
1. <span data-ttu-id="b6071-141">Убедитесь, что устройство HoloLens 2 питание и вы вошел.</span><span class="sxs-lookup"><span data-stu-id="b6071-141">Check that your HoloLens 2 device is powered on and you are signed in.</span></span>
1. <span data-ttu-id="b6071-142">На компьютере перейдите к пользовательскому приложению и скопируйте файл yourapp.appxbundle в файл yourdevicename\Internal Storage\Downloads.</span><span class="sxs-lookup"><span data-stu-id="b6071-142">On your PC navigate to your custom app, and copy yourapp.appxbundle to yourdevicename\Internal Storage\Downloads.</span></span>
    <span data-ttu-id="b6071-143">После завершения копирования файла можно отключить устройство и завершить установку позже.</span><span class="sxs-lookup"><span data-stu-id="b6071-143">After you finish copying your file, you may disconnect your device and finish the install later.</span></span>
1. <span data-ttu-id="b6071-144">На устройстве HoloLens 2 откройте \*\*\*\* меню "Пуск", выберите все приложения и запустите **приложение проводника.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b6071-144">From your HoloLens 2 device Open the **Start Menu**, select **All apps** and launch the **File Explorer** app.</span></span>
1. <span data-ttu-id="b6071-145">Перейдите в папку "Загрузки".</span><span class="sxs-lookup"><span data-stu-id="b6071-145">Navigate to the Downloads folder.</span></span> <span data-ttu-id="b6071-146">Возможно, вам потребуется сначала выбрать это \*\*\*\* устройство на левой панели приложения, а затем перейти к файлу "Загрузки".</span><span class="sxs-lookup"><span data-stu-id="b6071-146">You may need to on the left panel of the app select **This device** first, then navigate to Downloads.</span></span>
1. <span data-ttu-id="b6071-147">Выберите файл yourapp.appxbundle.</span><span class="sxs-lookup"><span data-stu-id="b6071-147">Select the yourapp.appxbundle file.</span></span>
1. <span data-ttu-id="b6071-148">Запустится установщик приложений.</span><span class="sxs-lookup"><span data-stu-id="b6071-148">The App Installer will launch.</span></span> <span data-ttu-id="b6071-149">Выберите **кнопку** "Установить", чтобы установить приложение.</span><span class="sxs-lookup"><span data-stu-id="b6071-149">Select the **Install** button to install your app.</span></span>

<span data-ttu-id="b6071-150">Установленное приложение автоматически запустится после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="b6071-150">The installed app will automatically launch upon the completion of installing.</span></span>

![Установка примеров MRTK с помощью установщика приложений](images/hololens-app-installer-picture.jpg)

### <span data-ttu-id="b6071-152">Устранение неполадок при установке</span><span class="sxs-lookup"><span data-stu-id="b6071-152">Troubleshooting Installs</span></span>

<span data-ttu-id="b6071-153">Если вашему приложению не удалось установить, проверьте следующее, чтобы устранить неполадки:</span><span class="sxs-lookup"><span data-stu-id="b6071-153">If your app failed to install check the following to troubleshoot:</span></span>

- <span data-ttu-id="b6071-154">Ваше приложение является сборкой Master или Release.</span><span class="sxs-lookup"><span data-stu-id="b6071-154">Your app is either a Master or Release build.</span></span>
- <span data-ttu-id="b6071-155">Устройство обновлено до сборки, на которой доступна эта функция.</span><span class="sxs-lookup"><span data-stu-id="b6071-155">Your device is updated to a build on which this feature is available.</span></span>
- <span data-ttu-id="b6071-156">Вы [подключены к Интернету.](hololens-network.md)</span><span class="sxs-lookup"><span data-stu-id="b6071-156">You are [connected to the internet](hololens-network.md).</span></span>
- <span data-ttu-id="b6071-157">Ваши [конечные точки для Microsoft Store](hololens-offline.md) настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="b6071-157">Your [endpoints for the Microsoft Store](hololens-offline.md) are correctly configured.</span></span>  

## <span data-ttu-id="b6071-158">Веб-установщик</span><span class="sxs-lookup"><span data-stu-id="b6071-158">Web Installer</span></span>

<span data-ttu-id="b6071-159">Пользователи могут установить приложение непосредственно с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="b6071-159">Users can install an app directly from a web server.</span></span> <span data-ttu-id="b6071-160">Этот поток использует установщик приложений в сочетании с простым способом скачивания и установки распространения.</span><span class="sxs-lookup"><span data-stu-id="b6071-160">This flow takes use of the App Installer combined with an easy download and install distribution method.</span></span>

### <span data-ttu-id="b6071-161">Настройка веб-установки:</span><span class="sxs-lookup"><span data-stu-id="b6071-161">How to set up web install:</span></span>

1. <span data-ttu-id="b6071-162">Убедитесь, что приложение правильно настроено для установки.</span><span class="sxs-lookup"><span data-stu-id="b6071-162">Ensure your app is correctly configured to install.</span></span>
1. <span data-ttu-id="b6071-163">Выполните [следующие действия, чтобы включить установку с веб-страницы.](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web#how-to-enable-this-on-a-webpage)</span><span class="sxs-lookup"><span data-stu-id="b6071-163">Follow these [steps to enable install from a web page](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web#how-to-enable-this-on-a-webpage).</span></span>

### <span data-ttu-id="b6071-164">Интерфейс конечных пользователей:</span><span class="sxs-lookup"><span data-stu-id="b6071-164">End user experience:</span></span>

1. <span data-ttu-id="b6071-165">Пользователь получает и устанавливает сертификат на устройство с помощью ранее выбранного метода.</span><span class="sxs-lookup"><span data-stu-id="b6071-165">User receives and installs certificate to the device using a method previously chosen above.</span></span>
1. <span data-ttu-id="b6071-166">Пользователь посещает URL-адрес, созданный на шаге выше.</span><span class="sxs-lookup"><span data-stu-id="b6071-166">User visits the URL created from the step above.</span></span>

<span data-ttu-id="b6071-167">Теперь приложение будет устанавливаться на устройство.</span><span class="sxs-lookup"><span data-stu-id="b6071-167">The app will now install to the device.</span></span> <span data-ttu-id="b6071-168">Чтобы найти приложение, \*\*\*\* откройте меню "Пуск" и выберите кнопку **"Все приложения",** чтобы найти приложение.</span><span class="sxs-lookup"><span data-stu-id="b6071-168">To find the app, open the **Start menu** and select the **All apps** button to find your app.</span></span>

- <span data-ttu-id="b6071-169">Дополнительные справки по устранению неполадок с методом установки установщика приложений можно найти в устранении [неполадок установщика приложений.](https://docs.microsoft.com/windows/msix/app-installer/troubleshoot-appinstaller-issues)</span><span class="sxs-lookup"><span data-stu-id="b6071-169">For more help with troubleshooting the app installer installation method visit [troubleshoot app installer issues](https://docs.microsoft.com/windows/msix/app-installer/troubleshoot-appinstaller-issues).</span></span>

> [!NOTE]
> <span data-ttu-id="b6071-170">Пользовательский интерфейс во время процесса обновления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b6071-170">UI during the update process is not supported.</span></span> <span data-ttu-id="b6071-171">Поэтому параметр ShowPrompt на этой странице [и](https://docs.microsoft.com/windows/msix/app-installer/update-settings) связанные параметры не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b6071-171">So the ShowPrompt option on [this page](https://docs.microsoft.com/windows/msix/app-installer/update-settings) and related options are not supported.</span></span>

## <span data-ttu-id="b6071-172">Примеры приложений</span><span class="sxs-lookup"><span data-stu-id="b6071-172">Sample Apps</span></span>

<span data-ttu-id="b6071-173">Чтобы попробовать установщик приложений с некоторыми примерами приложений, ознакомьтесь с некоторыми из доступных примеров:</span><span class="sxs-lookup"><span data-stu-id="b6071-173">To try the App Installer with some sample apps check out some of our available samples:</span></span>

- [<span data-ttu-id="b6071-174">MRTK Examples Hub</span><span class="sxs-lookup"><span data-stu-id="b6071-174">MRTK Examples Hub</span></span>](https://microsoft.github.io/MixedRealityToolkit-Unity/Documentation/README_ExampleHub.html)
- [<span data-ttu-id="b6071-175">Surfaces</span><span class="sxs-lookup"><span data-stu-id="b6071-175">Surfaces</span></span>](https://docs.microsoft.com/windows/mixed-reality/develop/unity/sampleapp-surfaces)
- [<span data-ttu-id="b6071-176">Примеры приложений UWP, которые можно использовать для тестирования</span><span class="sxs-lookup"><span data-stu-id="b6071-176">UWP Sample Apps that can be used for testing</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples)
