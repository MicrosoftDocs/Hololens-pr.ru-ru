---
title: Управление пользовательскими приложениями для HoloLens 2
description: узнайте, как устанавливать, удалять и загружать неопубликованные пользовательские приложения holographic на HoloLens 2 устройствах с помощью портала устройств и Visual Studio.
ms.assetid: 6bd124c4-731c-4bcc-86c7-23f9b67ff616
ms.date: 01/21/2021
manager: yannisle
keywords: hololens, hololens 2, загружать неопубликованные, Загрузка на стороне, Загрузка, сохранение, UWP, приложение, установка
ms.prod: hololens
ms.sitesec: library
author: joyjaz
ms.author: v-jjaswinski
ms.topic: article
ms.localizationpriority: medium
ms.custom:
- CI 111456
- CSSTroubleshooting
appliesto:
- HoloLens 2
ms.openlocfilehash: d2280a794455090c61a7bf30bc5dc5b8faf5adbe
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113636407"
---
# <a name="manage-custom-apps-for-hololens-2"></a><span data-ttu-id="dbff7-104">Управление пользовательскими приложениями для HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="dbff7-104">Manage custom apps for HoloLens 2</span></span>

<span data-ttu-id="dbff7-105">HoloLens поддерживает множество существующих приложений из Microsoft Store, а также новые приложения, разработанные специально для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="dbff7-105">HoloLens supports many existing applications from the Microsoft Store, as well as new apps built specifically for HoloLens.</span></span> 

<span data-ttu-id="dbff7-106">Дополнительные сведения о приложениях Магазина см. [в статье Управление приложениями с помощью магазина](holographic-store-apps.md).</span><span class="sxs-lookup"><span data-stu-id="dbff7-106">For more information about store apps, see [Manage apps with the store](holographic-store-apps.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbff7-107">Для корпоративных развертываний не рекомендуется включать режим разработчика, который используется обоими методами.</span><span class="sxs-lookup"><span data-stu-id="dbff7-107">For enterprise deployments, we don't recommend enabling Developer Mode, which both of these methods use.</span></span> <span data-ttu-id="dbff7-108">Если вы заинтересованы в безопасном методе развертывания приложений, ознакомьтесь с нашим [руководством по управлению приложениями: обзор](app-deploy-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dbff7-108">If you're interested in a secure app deployment method, please review our [App Management: Overview](app-deploy-overview.md).</span></span>

<span data-ttu-id="dbff7-109">если вы ищете метод установки приложения для HoloLens 2 устройств, ознакомьтесь с:</span><span class="sxs-lookup"><span data-stu-id="dbff7-109">If you're looking for either developer method of app installation for HoloLens 2 devices, refer to:</span></span>

- [<span data-ttu-id="dbff7-110">Портал устройств: Установка приложения</span><span class="sxs-lookup"><span data-stu-id="dbff7-110">Device Portal: Installing an App</span></span>](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal#installing-an-app)
- [<span data-ttu-id="dbff7-111">использование Visual Studio для развертывания и отладки приложений</span><span class="sxs-lookup"><span data-stu-id="dbff7-111">Using Visual Studio to deploy and debug Apps</span></span>](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-visual-studio)

<span data-ttu-id="dbff7-112">ознакомьтесь с нашим [руководством](holographic-custom-apps.md) , если вы хотите развернуть пользовательские приложения на HoloLens (1-й общий).</span><span class="sxs-lookup"><span data-stu-id="dbff7-112">See our [guide](holographic-custom-apps.md) if you'd like to deploy custom apps on HoloLens (1st gen).</span></span>
