---
title: Глобальный ограниченный доступ
description: Руководство по использованию OMA-URI для терминалов глобального ограниченного доступа
author: evmill
ms.author: v-evmill
ms.date: 9/21/2020
ms.topic: article
keywords: hololens, hololens 2, ограниченный доступ, терминал
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: lavinds
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: c2be1123d0e8a09d6955fb6e5da782daebc96bcf
ms.sourcegitcommit: 89ce6cdc0fc6d70a88217791c5f6d613778af614
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "11052628"
---
# <span data-ttu-id="8d05b-104">Глобальный ограниченный доступ — терминал</span><span class="sxs-lookup"><span data-stu-id="8d05b-104">Global Assigned Access – Kiosk</span></span>

<span data-ttu-id="8d05b-105">Эта функция настраивает устройство Hololens 2 для режима терминала с несколькими приложениями, который применяется на уровне системы, не похож на удостоверения в системе и применяется ко всем, кто входит в устройство.</span><span class="sxs-lookup"><span data-stu-id="8d05b-105">This feature configures Hololens 2 device for multiple app kiosk mode which is applicable at system level, has no affinity with any identity on the system and applies to everyone who signs into the device.</span></span> 

> [!NOTE]
> <span data-ttu-id="8d05b-106">Эта функция в настоящее время доступна только в сборках участников программы предварительной оценки Windows.</span><span class="sxs-lookup"><span data-stu-id="8d05b-106">This feature is currently only avalible in Windows Insider builds.</span></span> <span data-ttu-id="8d05b-107">Если вы хотите опробовать эту функцию до ее общей доступности в выпусках HoloLens, см. дополнительные сведения о сборках [программы предварительной оценки Windows](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="8d05b-107">If you would like to try this feature before it is generally avalible in HoloLens releases please read more about [Windows Insider](hololens-insider.md) builds.</span></span>
 
## <span data-ttu-id="8d05b-108">Как использовать ее в Intune?</span><span class="sxs-lookup"><span data-stu-id="8d05b-108">How to use this in Intune?</span></span> 

> [!NOTE]
> <span data-ttu-id="8d05b-109">Обратите внимание на области с пометкой "<!-".</span><span class="sxs-lookup"><span data-stu-id="8d05b-109">Please be aware of the areas marked with "<!-".</span></span> <span data-ttu-id="8d05b-110">В этих областях вам потребуется внести изменения в соответствии со своими предпочтениями.</span><span class="sxs-lookup"><span data-stu-id="8d05b-110">These areas will require you to make modifications based on your preferences.</span></span> 

1.  <span data-ttu-id="8d05b-111">Создайте настраиваемый профиль конфигурации устройства OMA URI, как показано ниже, и примените его к группе устройств HoloLens: ![Глобальный ограниченный доступ OMA-URI в Intune</span><span class="sxs-lookup"><span data-stu-id="8d05b-111">Create a custom OMA URI device configuration profile as follows and apply it to HoloLens device group: ![Global Assigned Access OMA-URI in Intune</span></span>](images/global-assigned-access-omauri.png)

2.  <span data-ttu-id="8d05b-112">Для значения обновите и вставьте следующее содержимое:</span><span class="sxs-lookup"><span data-stu-id="8d05b-112">For value, update and paste following content:</span></span> 

    :::code language="xml" source="samples/global-assigned-access.xml" highlight="12-13,23":::

## <span data-ttu-id="8d05b-113">Как использовать это в конструкторе конфигураций Windows?</span><span class="sxs-lookup"><span data-stu-id="8d05b-113">How to use this in Windows Configuration Designer?</span></span> 
 
1.  <span data-ttu-id="8d05b-114">Обновите и сохраните большой двоичный объект XML, упомянутый выше как XML-файл.</span><span class="sxs-lookup"><span data-stu-id="8d05b-114">Update and save XML blob mentioned above as XML file.</span></span> 

2.  <span data-ttu-id="8d05b-115">Выполните действия, описанные в разделе [Использование пакета подготовки для настройки терминала с одним или несколькими приложениями](https://docs.microsoft.com/hololens/hololens-kiosk#use-a-provisioning-package-to-set-up-a-single-app-or-multi-app-kiosk), в частности в секции "Пакет</span><span class="sxs-lookup"><span data-stu-id="8d05b-115">Follow the steps in [Use a provisioning package to set up a single-app or multi-app kiosk](https://docs.microsoft.com/hololens/hololens-kiosk#use-a-provisioning-package-to-set-up-a-single-app-or-multi-app-kiosk), specifically the section "Prov.</span></span> <span data-ttu-id="8d05b-116">подготовки, шаг 2 — Добавление XML-файла конфигурации терминала в пакет подготовки" и см. XML-файл, сохраненный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="8d05b-116">package, step 2 – Add the kiosk configuration XML file to a provisioning package" and refer to the XML file that was saved in the previous step.</span></span> 

## <span data-ttu-id="8d05b-117">Могу ли я создать конфигурацию, которая глобально применяется ко всем, и отдельную конфигурацию для 1 учетной записи AAD или группы AAD?</span><span class="sxs-lookup"><span data-stu-id="8d05b-117">Can I create a configuration where global applies to everyone and separate configuration applies to 1 AAD account or AAD group?</span></span> 

<span data-ttu-id="8d05b-118">Да, см. пример большого двоичного объекта XML ниже.</span><span class="sxs-lookup"><span data-stu-id="8d05b-118">Yes, please refer to the example XML blob below.</span></span> <span data-ttu-id="8d05b-119">Профиль глобального ограниченного доступа применяется к Hololens, если не обнаружен специальный профиль для вошедшего пользователя, поэтому это стандартная конфигурация режима терминала для вошедшего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d05b-119">Global Assigned Access profile is applied on Hololens when a specific one for the signed in user is not found, so it is default kiosk mode configuration for signed-in user.</span></span> <span data-ttu-id="8d05b-120">Пример большого двоичного объекта XML для использования:</span><span class="sxs-lookup"><span data-stu-id="8d05b-120">Here is an example of XML blob to be used:</span></span> 

> [!NOTE]
> <span data-ttu-id="8d05b-121">Обратите внимание на выделенные области с пометкой "<!-". В этих областях вам потребуется внести изменения в соответствии со своими предпочтениями.</span><span class="sxs-lookup"><span data-stu-id="8d05b-121">Please be aware of the highlighted areas marked with <!-  these areas will require you to make modifications based on your preferences.</span></span> 

 :::code language="xml" source="samples/exclude-one-aad-user-or-group.xml" highlight="8,11,17":::

## <span data-ttu-id="8d05b-122">Исключение DeviceOwners из профиля глобального ограниченного доступа</span><span class="sxs-lookup"><span data-stu-id="8d05b-122">Excluding DeviceOwners from Global Assigned Access Profile</span></span>

<span data-ttu-id="8d05b-123">Эта функция позволяет исключить пользователя, который считается "[владельцем устройства](security-adminless-os.md)" Hololens, из глобального ограниченного доступа.</span><span class="sxs-lookup"><span data-stu-id="8d05b-123">This feature allows a user who is considered “[Device owner](security-adminless-os.md)" on Hololens to be excluded from Global Assigned Access.</span></span> <span data-ttu-id="8d05b-124">Чтобы воспользоваться этой функцией, в большом двоичном объекте XML для конфигурации терминала с несколькими приложениями добавьте выделенные строки:</span><span class="sxs-lookup"><span data-stu-id="8d05b-124">In order to take advantage of this feature, in the XML blob for multiple-app kiosk configuration, ensure highlighted lines are added:</span></span> 

 :::code language="xml" source="samples/exclude-device-owners-from-global.xml" highlight="6,16-18":::
 
