---
title: Установка приложений с помощью веб-установщика
description: Установка приложений с помощью веб-установщика для установщика приложений
keywords: Управление приложениями, приложение, hololens, установщик приложений, веб-установка
author: evmill
ms.author: v-evmill
ms.reviewer: qizho
ms.date: 9/17/2020
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 186cbefb2822455dcf922804ea09533b833b8663
ms.sourcegitcommit: 4ad9b6c73913808175b1a448d2be9e33592f65af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "11027485"
---
# <span data-ttu-id="4a29a-104">Установка приложений с веб-страницы</span><span class="sxs-lookup"><span data-stu-id="4a29a-104">Installing apps from a web page</span></span>

<span data-ttu-id="4a29a-105">Пользователи могут установить приложение непосредственно с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="4a29a-105">Users can install an app directly from a web server.</span></span> <span data-ttu-id="4a29a-106">Это позволяет использовать установщик приложений в сочетании с простым способом загрузки и установки.</span><span class="sxs-lookup"><span data-stu-id="4a29a-106">This takes use of the App Installer combined with an easy download and install distribution method.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="4a29a-107">Эта функция в настоящее время avalible только в сборках участников программы предварительной оценки Windows (19041.1366 +).</span><span class="sxs-lookup"><span data-stu-id="4a29a-107">This feature is currently only avalible in Windows Insider builds 19041.1366+.</span></span> <span data-ttu-id="4a29a-108">[Узнайте больше о том, как зарегистрироваться в сборках для участников программы предварительной оценки Windows](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="4a29a-108">[Learn more on how to enroll in Windows Insider builds](hololens-insider.md).</span></span>

## <span data-ttu-id="4a29a-109">Настройка:</span><span class="sxs-lookup"><span data-stu-id="4a29a-109">How to set this up:</span></span>
1.  <span data-ttu-id="4a29a-110">Убедитесь, что ваше приложение правильно настроено для установки.</span><span class="sxs-lookup"><span data-stu-id="4a29a-110">Ensure your app is correctly configured to install.</span></span>
1.  <span data-ttu-id="4a29a-111">[Чтобы включить эту функцию на веб-странице](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web#how-to-enable-this-on-a-webpage), выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4a29a-111">Follow these [steps to enable this on a web page](https://docs.microsoft.com/windows/msix/app-installer/installing-windows10-apps-web#how-to-enable-this-on-a-webpage).</span></span> 
1.  <span data-ttu-id="4a29a-112">Выберите способ развертывания сертификата.</span><span class="sxs-lookup"><span data-stu-id="4a29a-112">Pick a certificate deployment method.</span></span> 
    1.  <span data-ttu-id="4a29a-113">[Пакеты подготовки](hololens-provisioning.md) можно применять к локальным устройствам.</span><span class="sxs-lookup"><span data-stu-id="4a29a-113">[Provisioning Packages](hololens-provisioning.md) can be applied to local devices.</span></span>
    1.  <span data-ttu-id="4a29a-114">MDM можно использовать для [применения сертификатов в конфигурациях устройств](https://docs.microsoft.com/mem/intune/protect/certificates-configure).</span><span class="sxs-lookup"><span data-stu-id="4a29a-114">MDM can be used to [apply certificates with device configurations](https://docs.microsoft.com/mem/intune/protect/certificates-configure).</span></span>
    1.  <span data-ttu-id="4a29a-115">Используйте [Диспетчер сертификатов](hololens-insider.md#certificate-manager)устройств.</span><span class="sxs-lookup"><span data-stu-id="4a29a-115">Use the on device [Certificate Manager](hololens-insider.md#certificate-manager).</span></span> 

## <span data-ttu-id="4a29a-116">Работа с конечными пользователями:</span><span class="sxs-lookup"><span data-stu-id="4a29a-116">End User Experience:</span></span>
1.  <span data-ttu-id="4a29a-117">Пользователь получает и устанавливает сертификат на устройство с помощью метода, ранее выбранного выше.</span><span class="sxs-lookup"><span data-stu-id="4a29a-117">User receives and installs certificate to the device using a method previously chosen above.</span></span> 
1.  <span data-ttu-id="4a29a-118">Пользователь посещает URL-адрес, созданный на этапе, описанном выше.</span><span class="sxs-lookup"><span data-stu-id="4a29a-118">User visits the URL created from the step above.</span></span>

<span data-ttu-id="4a29a-119">Теперь приложение будет установлено на устройстве.</span><span class="sxs-lookup"><span data-stu-id="4a29a-119">The app will now install to the device.</span></span> <span data-ttu-id="4a29a-120">Чтобы найти приложение, откройте **меню "Пуск** " и нажмите кнопку " **все приложения** ", чтобы найти приложение.</span><span class="sxs-lookup"><span data-stu-id="4a29a-120">To find the app open the **Start menu** and select the **All apps** button to find your app.</span></span> 

-   <span data-ttu-id="4a29a-121">Инструкции по устранению неполадок, возникающих при установке, можно найти в статье [Устранение неполадок установщика приложений](https://docs.microsoft.com/windows/msix/app-installer/troubleshoot-appinstaller-issues).</span><span class="sxs-lookup"><span data-stu-id="4a29a-121">For help troubleshooting this installation method please visit [troubleshoot app installer issues](https://docs.microsoft.com/windows/msix/app-installer/troubleshoot-appinstaller-issues).</span></span> 

> [!NOTE]
> <span data-ttu-id="4a29a-122">Пользовательский интерфейс в процессе обновления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4a29a-122">UI during the update process is not supported.</span></span> <span data-ttu-id="4a29a-123">Таким образом, параметр ShowPrompt на [этой странице](https://docs.microsoft.com/windows/msix/app-installer/update-settings) и соответствующие параметры не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="4a29a-123">So the ShowPrompt option on [this page](https://docs.microsoft.com/windows/msix/app-installer/update-settings) and related options are not supported.</span></span>
