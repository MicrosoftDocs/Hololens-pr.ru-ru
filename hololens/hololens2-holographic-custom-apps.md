---
title: Управление пользовательскими приложениями для HoloLens 2
description: Узнайте, как установить, удалить и загрузить неоконченные пользовательские голографические приложения на устройства HoloLens 2 с помощью портала устройств и Visual Studio.
ms.assetid: 6bd124c4-731c-4bcc-86c7-23f9b67ff616
ms.date: 01/21/2021
manager: yannisle
keywords: hololens, hololens 2, загрузка неогрузки, нео боковая загрузка, магазин, uwp, приложение, установка
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
ms.openlocfilehash: e3ae180697c889a426108992ba345dc23b96505c
ms.sourcegitcommit: 4c6d982bee72195bef955532738711f2b00ac8be
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297010"
---
# <span data-ttu-id="10fc6-104">Управление пользовательскими приложениями для HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="10fc6-104">Manage custom apps for HoloLens 2</span></span>

<span data-ttu-id="10fc6-105">Устройство HoloLens поддерживает множество существующих приложений в Microsoft Store, а также новые приложения, разработанные специально для HoloLens.</span><span class="sxs-lookup"><span data-stu-id="10fc6-105">HoloLens supports many existing applications from the Microsoft Store, as well as new apps built specifically for HoloLens.</span></span> 

<span data-ttu-id="10fc6-106">Дополнительные сведения о приложениях Магазина см. в под [управлением приложений с магазином.](holographic-store-apps.md)</span><span class="sxs-lookup"><span data-stu-id="10fc6-106">For more information about store apps, see [Manage apps with the store](holographic-store-apps.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10fc6-107">В корпоративных развертываниях не рекомендуется использовать режим разработчика, который используется в обоих этих методах.</span><span class="sxs-lookup"><span data-stu-id="10fc6-107">For enterprise deployments, we don't recommend enabling Developer Mode, which both of these methods use.</span></span> <span data-ttu-id="10fc6-108">Если вы заинтересованы в безопасном способе развертывания приложений, просмотрите наше руководство по управлению [приложениями: обзор.](app-deploy-overview.md)</span><span class="sxs-lookup"><span data-stu-id="10fc6-108">If you're interested in a secure app deployment method, please review our [App Management: Overview](app-deploy-overview.md).</span></span>

<span data-ttu-id="10fc6-109">Если вы ищете способ разработчика установки приложений для устройств HoloLens 2, обратитесь к:</span><span class="sxs-lookup"><span data-stu-id="10fc6-109">If you're looking for either developer method of app installation for HoloLens 2 devices, refer to:</span></span>
- [<span data-ttu-id="10fc6-110">Портал устройств: установка приложения</span><span class="sxs-lookup"><span data-stu-id="10fc6-110">Device Portal: Installing an App</span></span>](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal#installing-an-app)
- [<span data-ttu-id="10fc6-111">Использование Visual Studio для развертывания и отлаки приложений</span><span class="sxs-lookup"><span data-stu-id="10fc6-111">Using Visual Studio to deploy and debug Apps</span></span>](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-visual-studio)

<span data-ttu-id="10fc6-112">См. [наше руководство,](holographic-custom-apps.md) если вы хотите развернуть настраиваемые приложения на HoloLens (1-е поколения).</span><span class="sxs-lookup"><span data-stu-id="10fc6-112">See our [guide](holographic-custom-apps.md) if you'd like to deploy custom apps on HoloLens (1st gen).</span></span>