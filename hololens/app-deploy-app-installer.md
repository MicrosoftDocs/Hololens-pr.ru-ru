---
title: Как загрузить и установить приложения с помощью установщика приложений HoloLens 2
description: Узнайте, как устанавливать и устранять неполадки приложений с помощью установщика приложений, а также загружать и устанавливать приложения через пользовательский интерфейс.
keywords: Управление приложениями, приложение, hololens, установщик приложений
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
ms.openlocfilehash: 9e413963dbf34dd071fc9603487590065b967ee7
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309271"
---
# <a name="install-apps-on-hololens-2-via-app-installer"></a><span data-ttu-id="f6c63-104">Установка приложений в HoloLens 2 с помощью установщика приложений</span><span class="sxs-lookup"><span data-stu-id="f6c63-104">Install Apps on HoloLens 2 via App Installer</span></span>

> [!NOTE]
> <span data-ttu-id="f6c63-105">Эта функция стала доступна в [Windows holographic, версия 20H2 – декабрь 2020](hololens-release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="f6c63-105">This feature was made available in [Windows Holographic, version 20H2 – December 2020 Update](hololens-release-notes.md).</span></span> <span data-ttu-id="f6c63-106">Убедитесь, что устройство [Обновлено](hololens-update-hololens.md) для использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="f6c63-106">Ensure your device is [updated](hololens-update-hololens.md) to use this feature.</span></span>

<span data-ttu-id="f6c63-107">Мы **добавили новую возможность (установщик приложения), которая позволяет более эффективно устанавливать приложения** на устройствах HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="f6c63-107">We have **added a new capability (App Installer) to allow you to install applications more seamlessly** on your HoloLens 2 devices.</span></span> <span data-ttu-id="f6c63-108">Эта функция будет **включена по умолчанию для неуправляемых устройств**.</span><span class="sxs-lookup"><span data-stu-id="f6c63-108">The feature will be **on by default for unmanaged devices**.</span></span> <span data-ttu-id="f6c63-109">Чтобы предотвратить сбои в работе предприятий, в настоящее время установщик приложений будет **недоступен для управляемых устройств** .</span><span class="sxs-lookup"><span data-stu-id="f6c63-109">To prevent disruption to enterprises, app installer will be **not be available for managed devices** at this time.</span></span>  

<span data-ttu-id="f6c63-110">Устройство считается управляемым, если выполняется **одно** из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="f6c63-110">A device is considered “managed” if **any** of the following are true:</span></span>

- <span data-ttu-id="f6c63-111">[Зарегистрировано](hololens-enroll-mdm.md) в MDM</span><span class="sxs-lookup"><span data-stu-id="f6c63-111">MDM [Enrolled](hololens-enroll-mdm.md)</span></span>
- <span data-ttu-id="f6c63-112">Настроено с помощью [пакета подготовки](hololens-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="f6c63-112">Configured with [provisioning package](hololens-provisioning.md)</span></span>
- <span data-ttu-id="f6c63-113">[Удостоверение](hololens-identity.md) пользователя — Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f6c63-113">User [Identity](hololens-identity.md) is Azure AD</span></span>

<span data-ttu-id="f6c63-114">Теперь вы можете устанавливать приложения без необходимости включать режим разработчика или использовать портал устройств.</span><span class="sxs-lookup"><span data-stu-id="f6c63-114">You are now able to install Apps without needing to enable Developer Mode or using Device Portal.</span></span>  <span data-ttu-id="f6c63-115">Скачайте (через USB или через Microsoft погранично) пакет appx на устройство и перейдите к пакету appx в проводнике, чтобы получить запрос на запуск установки.</span><span class="sxs-lookup"><span data-stu-id="f6c63-115">Download (over USB or through Microsoft Edge) the Appx Bundle to your device and navigate to the Appx Bundle in the File Explorer to be prompted to kick off the installation.</span></span>  <span data-ttu-id="f6c63-116">Кроме того, можно [запустить установку с веб-страницы](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web).</span><span class="sxs-lookup"><span data-stu-id="f6c63-116">Alternatively, [initiate an install from a web page](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web).</span></span>  <span data-ttu-id="f6c63-117">Так же как и приложения, устанавливаемые из Microsoft Store или загружать неопубликованные с помощью возможности развертывания бизнес-приложений MDM, приложения должны быть снабжены цифровой подписью с помощью [средства Sign Tool](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool) , а [сертификат, используемый для подписи, должен быть доверенным для](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool#security-considerations) устройства HoloLens перед развертыванием приложения.</span><span class="sxs-lookup"><span data-stu-id="f6c63-117">Just like apps you install from the Microsoft Store or sideload using MDM’s LOB App deployment capability, apps need to be digitally signed with the [Sign Tool](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool) and the [certificate used to sign must be trusted](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool#security-considerations) by the HoloLens device before the app can be deployed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c63-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f6c63-118">Requirements</span></span>

### <a name="for-your-devices"></a><span data-ttu-id="f6c63-119">Для устройств:</span><span class="sxs-lookup"><span data-stu-id="f6c63-119">For your devices:</span></span>

<span data-ttu-id="f6c63-120">В настоящее время эта функция доступна в сборках Windows holographic 20H2 для устройств HoloLens 2.</span><span class="sxs-lookup"><span data-stu-id="f6c63-120">This feature is currently available in Windows Holographic 20H2 builds for HoloLens 2 devices.</span></span> <span data-ttu-id="f6c63-121">Убедитесь, что все устройства, использующие этот метод, [обновлены](hololens-update-hololens.md).</span><span class="sxs-lookup"><span data-stu-id="f6c63-121">Ensure any devices using this method are [updated](hololens-update-hololens.md).</span></span>

### <a name="for-your-apps"></a><span data-ttu-id="f6c63-122">Для приложений:</span><span class="sxs-lookup"><span data-stu-id="f6c63-122">For your apps:</span></span>

<span data-ttu-id="f6c63-123">Конфигурация решения приложения должна быть **основной** или **выпуском** , так как установщик приложения будет использовать зависимости из хранилища.</span><span class="sxs-lookup"><span data-stu-id="f6c63-123">Your app’s Solution Configuration must be either **Master** or **Release** as the App Installer will use dependencies from the store.</span></span> <span data-ttu-id="f6c63-124">См. Дополнительные сведения о [создании пакетов приложений](https://docs.microsoft.com/windows/msix/app-installer/create-appinstallerfile-vs).</span><span class="sxs-lookup"><span data-stu-id="f6c63-124">See more about [creating app packages](https://docs.microsoft.com/windows/msix/app-installer/create-appinstallerfile-vs).</span></span>

<span data-ttu-id="f6c63-125">Приложения, устанавливаемые с помощью этого метода, должны иметь цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="f6c63-125">Apps that are installed via this method must be digitally signed.</span></span> <span data-ttu-id="f6c63-126">Для подписи приложения необходимо использовать сертификат.</span><span class="sxs-lookup"><span data-stu-id="f6c63-126">You'll need to use a certificate to sign the app.</span></span> <span data-ttu-id="f6c63-127">Вы можете получить сертификат из [списка доверенных ЦС MS](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT), в этом случае вам не потребуется предпринимать никаких дополнительных действий.</span><span class="sxs-lookup"><span data-stu-id="f6c63-127">You can either get a certificate from the [MS Trusted CA List](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT), in which case you won't need to take any extra action.</span></span> <span data-ttu-id="f6c63-128">Можно также подписать собственный сертификат, но этот сертификат потребуется отправить на устройство.</span><span class="sxs-lookup"><span data-stu-id="f6c63-128">Or you can sign your own certificate however that certificate will need to be pushed onto the device.</span></span>

- <span data-ttu-id="f6c63-129">Как подписывать приложения [с помощью программы Sign Tool.](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool)</span><span class="sxs-lookup"><span data-stu-id="f6c63-129">How to sign apps [using the Sign Tool.](https://docs.microsoft.com/windows/win32/appxpkg/how-to-sign-a-package-using-signtool)</span></span>

<span data-ttu-id="f6c63-130">**Параметры сертификата:**</span><span class="sxs-lookup"><span data-stu-id="f6c63-130">**Certificate options:**</span></span>

- [<span data-ttu-id="f6c63-131">Список доверенных ЦС MS</span><span class="sxs-lookup"><span data-stu-id="f6c63-131">MS Trusted CA List</span></span>](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT)

<span data-ttu-id="f6c63-132">**Выберите метод развертывания сертификата.**</span><span class="sxs-lookup"><span data-stu-id="f6c63-132">**Pick a certificate deployment method.**</span></span>

- <span data-ttu-id="f6c63-133">[Пакеты подготовки](hololens-provisioning.md) можно применять к локальным устройствам.</span><span class="sxs-lookup"><span data-stu-id="f6c63-133">[Provisioning Packages](hololens-provisioning.md) can be applied to local devices.</span></span>
- <span data-ttu-id="f6c63-134">MDM можно использовать для [применения сертификатов с конфигурациями устройств](https://docs.microsoft.com/mem/intune/protect/certificates-configure).</span><span class="sxs-lookup"><span data-stu-id="f6c63-134">MDM can be used to [apply certificates with device configurations](https://docs.microsoft.com/mem/intune/protect/certificates-configure).</span></span>
- <span data-ttu-id="f6c63-135">Используйте [Диспетчер сертификатов](certificate-manager.md)устройств.</span><span class="sxs-lookup"><span data-stu-id="f6c63-135">Use the on device [Certificate Manager](certificate-manager.md).</span></span>

## <a name="installation-method"></a><span data-ttu-id="f6c63-136">Метод установки</span><span class="sxs-lookup"><span data-stu-id="f6c63-136">Installation method</span></span>

1. <span data-ttu-id="f6c63-137">Убедитесь, что устройство не считается управляемым.</span><span class="sxs-lookup"><span data-stu-id="f6c63-137">Check that your device is not considered managed.</span></span>
1. <span data-ttu-id="f6c63-138">Убедитесь, что устройство HoloLens 2 включено и вы вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="f6c63-138">Check that your HoloLens 2 device is powered on and you are signed in.</span></span>
1. <span data-ttu-id="f6c63-139">На своем ПК перейдите к пользовательскому приложению и скопируйте йоурапп. appxbundle в Йоурдевиценаме\интернал Стораже\довнлоадс.</span><span class="sxs-lookup"><span data-stu-id="f6c63-139">On your PC navigate to your custom app, and copy yourapp.appxbundle to yourdevicename\Internal Storage\Downloads.</span></span>
    <span data-ttu-id="f6c63-140">После завершения копирования файла вы можете отключить устройство и завершить установку позже.</span><span class="sxs-lookup"><span data-stu-id="f6c63-140">After you finish copying your file, you may disconnect your device and finish the install later.</span></span>
1. <span data-ttu-id="f6c63-141">На устройстве HoloLens 2 Откройте меню " **Пуск**", выберите " **все приложения** " и запустите приложение " **проводник** ".</span><span class="sxs-lookup"><span data-stu-id="f6c63-141">From your HoloLens 2 device Open the **Start Menu**, select **All apps** and launch the **File Explorer** app.</span></span>
1. <span data-ttu-id="f6c63-142">Перейдите в папку downloads.</span><span class="sxs-lookup"><span data-stu-id="f6c63-142">Navigate to the Downloads folder.</span></span> <span data-ttu-id="f6c63-143">Возможно, вам потребуется на левой панели приложения сначала выбрать **это устройство** , а затем перейдите к разделу загрузки.</span><span class="sxs-lookup"><span data-stu-id="f6c63-143">You may need to on the left panel of the app select **This device** first, then navigate to Downloads.</span></span>
1. <span data-ttu-id="f6c63-144">Выберите файл йоурапп. appxbundle.</span><span class="sxs-lookup"><span data-stu-id="f6c63-144">Select the yourapp.appxbundle file.</span></span>
1. <span data-ttu-id="f6c63-145">Будет запущен установщик приложения.</span><span class="sxs-lookup"><span data-stu-id="f6c63-145">The App Installer will launch.</span></span> <span data-ttu-id="f6c63-146">Нажмите кнопку " **установить** ", чтобы установить приложение.</span><span class="sxs-lookup"><span data-stu-id="f6c63-146">Select the **Install** button to install your app.</span></span>

<span data-ttu-id="f6c63-147">Установленное приложение будет автоматически запущено после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="f6c63-147">The installed app will automatically launch upon the completion of installing.</span></span>

![Установка примеров МРТК с помощью установщика приложений](images/hololens-app-installer-picture.jpg)

### <a name="troubleshooting-installs"></a><span data-ttu-id="f6c63-149">Устранение неполадок установки</span><span class="sxs-lookup"><span data-stu-id="f6c63-149">Troubleshooting Installs</span></span>

<span data-ttu-id="f6c63-150">Если не удалось установить приложение, для устранения неполадок проверьте следующее:</span><span class="sxs-lookup"><span data-stu-id="f6c63-150">If your app failed to install,  check the following to troubleshoot:</span></span>

- <span data-ttu-id="f6c63-151">Ваше приложение — это Главная или окончательная сборка.</span><span class="sxs-lookup"><span data-stu-id="f6c63-151">Your app is either a Master or Release build.</span></span>
- <span data-ttu-id="f6c63-152">Устройство будет обновлено до сборки, на которой доступна эта функция.</span><span class="sxs-lookup"><span data-stu-id="f6c63-152">Your device is updated to a build on which this feature is available.</span></span>
- <span data-ttu-id="f6c63-153">Вы [подключены к Интернету](hololens-network.md).</span><span class="sxs-lookup"><span data-stu-id="f6c63-153">You are [connected to the internet](hololens-network.md).</span></span>
- <span data-ttu-id="f6c63-154">[Конечные точки для Microsoft Store](hololens-offline.md) настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="f6c63-154">Your [endpoints for the Microsoft Store](hololens-offline.md) are correctly configured.</span></span>  

## <a name="web-installer"></a><span data-ttu-id="f6c63-155">Веб-установщик</span><span class="sxs-lookup"><span data-stu-id="f6c63-155">Web Installer</span></span>

<span data-ttu-id="f6c63-156">Пользователи могут устанавливать приложения непосредственно с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="f6c63-156">Users can install an app directly from a web server.</span></span> <span data-ttu-id="f6c63-157">Этот поток использует установщик приложений в сочетании с простым способом загрузки и установки распространения.</span><span class="sxs-lookup"><span data-stu-id="f6c63-157">This flow takes use of the App Installer combined with an easy download and install distribution method.</span></span>

### <a name="how-to-set-up-web-install"></a><span data-ttu-id="f6c63-158">Как настроить веб-установку:</span><span class="sxs-lookup"><span data-stu-id="f6c63-158">How to set up web install:</span></span>

1. <span data-ttu-id="f6c63-159">Убедитесь, что приложение правильно настроено для установки.</span><span class="sxs-lookup"><span data-stu-id="f6c63-159">Ensure your app is correctly configured to install.</span></span>
1. <span data-ttu-id="f6c63-160">Выполните следующие [действия, чтобы включить установку с веб-страницы](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web#how-to-enable-this-on-a-webpage).</span><span class="sxs-lookup"><span data-stu-id="f6c63-160">Follow these [steps to enable install from a web page](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web#how-to-enable-this-on-a-webpage).</span></span>

### <a name="end-user-experience"></a><span data-ttu-id="f6c63-161">Взаимодействие с конечным пользователем:</span><span class="sxs-lookup"><span data-stu-id="f6c63-161">End user experience:</span></span>

1. <span data-ttu-id="f6c63-162">Пользователь получает и устанавливает сертификат на устройство с помощью ранее выбранного метода.</span><span class="sxs-lookup"><span data-stu-id="f6c63-162">User receives and installs certificate to the device using a method previously chosen above.</span></span>
1. <span data-ttu-id="f6c63-163">Пользователь посещает URL-адрес, созданный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="f6c63-163">User visits the URL created from the step above.</span></span>

<span data-ttu-id="f6c63-164">Теперь приложение будет установлено на устройстве.</span><span class="sxs-lookup"><span data-stu-id="f6c63-164">The app will now install to the device.</span></span> <span data-ttu-id="f6c63-165">Чтобы найти приложение, откройте меню " **Пуск** " и нажмите кнопку " **все приложения** ", чтобы найти приложение.</span><span class="sxs-lookup"><span data-stu-id="f6c63-165">To find the app, open the **Start menu** and select the **All apps** button to find your app.</span></span>

- <span data-ttu-id="f6c63-166">Дополнительные сведения об устранении неполадок в методе установки установщика приложений см. в статье [Устранение неполадок установщика приложений](https://docs.microsoft.com/windows/msix/app-installer/troubleshoot-appinstaller-issues).</span><span class="sxs-lookup"><span data-stu-id="f6c63-166">For more help with troubleshooting the app installer installation method visit [troubleshoot app installer issues](https://docs.microsoft.com/windows/msix/app-installer/troubleshoot-appinstaller-issues).</span></span>

> [!NOTE]
> <span data-ttu-id="f6c63-167">Пользовательский интерфейс в процессе обновления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f6c63-167">UI during the update process is not supported.</span></span> <span data-ttu-id="f6c63-168">Поэтому параметр Шовпромпт на [этой странице](https://docs.microsoft.com/windows/msix/app-installer/update-settings) и связанные параметры не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="f6c63-168">So the ShowPrompt option on [this page](https://docs.microsoft.com/windows/msix/app-installer/update-settings) and related options are not supported.</span></span>

## <a name="sample-apps"></a><span data-ttu-id="f6c63-169">Примеры приложений</span><span class="sxs-lookup"><span data-stu-id="f6c63-169">Sample Apps</span></span>

<span data-ttu-id="f6c63-170">Чтобы попробовать установщик приложения с некоторыми примерами приложений, ознакомьтесь с некоторыми из наших доступных примеров:</span><span class="sxs-lookup"><span data-stu-id="f6c63-170">To try the App Installer with some sample apps check out some of our available samples:</span></span>

- [<span data-ttu-id="f6c63-171">Центр с примерами MRTK</span><span class="sxs-lookup"><span data-stu-id="f6c63-171">MRTK Examples Hub</span></span>](https://microsoft.github.io/MixedRealityToolkit-Unity/Documentation/README_ExampleHub.html)
- [<span data-ttu-id="f6c63-172">Surfaces</span><span class="sxs-lookup"><span data-stu-id="f6c63-172">Surfaces</span></span>](https://docs.microsoft.com/windows/mixed-reality/develop/unity/sampleapp-surfaces)
- [<span data-ttu-id="f6c63-173">Примеры приложений UWP, которые можно использовать для тестирования</span><span class="sxs-lookup"><span data-stu-id="f6c63-173">UWP Sample Apps that can be used for testing</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples)
