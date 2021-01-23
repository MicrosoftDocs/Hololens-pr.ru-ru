---
title: Глобальный ограниченный доступ
description: Начните работать с нашим руководством по использованию OMA-URI для терминалов глобального ограниченного доступа с помощью Intune и конструктора конфигураций Windows.
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
ms.openlocfilehash: b86d88c7487043c6fcb057f03f353a57e44ef781
ms.sourcegitcommit: d20057957aa05c025c9838119cc29264bc57b4bd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11283180"
---
# <span data-ttu-id="5bd17-104">Глобальный ограниченный доступ — терминал</span><span class="sxs-lookup"><span data-stu-id="5bd17-104">Global Assigned Access – Kiosk</span></span>

<span data-ttu-id="5bd17-105">Эта функция настраивает устройство HoloLens 2 для работы в режиме мультипрограммного терминала, который применяется на уровне системы, не соответствует удостоверениям в системе и применяется ко всем, кто входит на устройство.</span><span class="sxs-lookup"><span data-stu-id="5bd17-105">This feature configures HoloLens 2 device for multiple app kiosk mode, which is applicable at system level, has no affinity with any identity on the system and applies to everyone who signs into the device.</span></span>

> [!NOTE]
> <span data-ttu-id="5bd17-106">В настоящее время эта функция доступна только в сборках программы предварительной оценки Windows.</span><span class="sxs-lookup"><span data-stu-id="5bd17-106">This feature is currently only available in Windows Insider builds.</span></span> <span data-ttu-id="5bd17-107">Если вы хотите попробовать эту функцию, прежде чем она станет общедоступной в выпусках HoloLens, узнайте больше о сборках [программы предварительной оценки Windows](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="5bd17-107">If you would like to try this feature before it is generally available in HoloLens releases please read more about [Windows Insider](hololens-insider.md) builds.</span></span>

## <span data-ttu-id="5bd17-108">Как использовать глобальный ограниченный доступ в Intune?</span><span class="sxs-lookup"><span data-stu-id="5bd17-108">How to use Global Assigned Access in Intune?</span></span>

> [!NOTE]
> <span data-ttu-id="5bd17-109">Обратите внимание на области с пометкой "<!-".</span><span class="sxs-lookup"><span data-stu-id="5bd17-109">Please be aware of the areas marked with "<!-".</span></span> <span data-ttu-id="5bd17-110">В этих областях вам потребуется внести изменения в соответствии со своими предпочтениями.</span><span class="sxs-lookup"><span data-stu-id="5bd17-110">These areas will require you to make modifications based on your preferences.</span></span>

1. <span data-ttu-id="5bd17-111">Создайте настраиваемый профиль конфигурации устройства OMA URI, как показано ниже, и примените его к группе устройств HoloLens:</span><span class="sxs-lookup"><span data-stu-id="5bd17-111">Create a custom OMA URI device configuration profile as follows and apply it to HoloLens device group:</span></span>

    <span data-ttu-id="5bd17-112">Значение универсального кода ресурса (URI): ./Device/Vendor/MSFT/AssignedAccess/Configuration</span><span class="sxs-lookup"><span data-stu-id="5bd17-112">URI value: ./Device/Vendor/MSFT/AssignedAccess/Configuration</span></span>

    > [!div class="mx-imgBorder"]
    > ![Глобальный ограниченный доступ OMA-URI в Intune](images/global-assigned-access-omauri.png)

2. <span data-ttu-id="5bd17-114">Для значения обновите и вставьте следующее содержимое:</span><span class="sxs-lookup"><span data-stu-id="5bd17-114">For value, update and paste following content:</span></span>

    :::code language="xml" source="samples/global-assigned-access.xml" highlight="12-13,23":::

## <span data-ttu-id="5bd17-115">Как использовать глобальный ограниченный доступ в конструкторе конфигураций Windows?</span><span class="sxs-lookup"><span data-stu-id="5bd17-115">How to use Global Assigned Access in Windows Configuration Designer?</span></span>

1. <span data-ttu-id="5bd17-116">Обновите и сохраните большой двоичный объект XML, упомянутый выше как XML-файл.</span><span class="sxs-lookup"><span data-stu-id="5bd17-116">Update and save XML blob mentioned above as XML file.</span></span> 

2. <span data-ttu-id="5bd17-117">Выполните действия, описанные в разделе [Использование пакета подготовки для настройки терминала с одним или несколькими приложениями](https://docs.microsoft.com/hololens/hololens-kiosk#use-a-provisioning-package-to-set-up-a-single-app-or-multi-app-kiosk), в частности в секции "Пакет</span><span class="sxs-lookup"><span data-stu-id="5bd17-117">Follow the steps in [Use a provisioning package to set up a single-app or multi-app kiosk](https://docs.microsoft.com/hololens/hololens-kiosk#use-a-provisioning-package-to-set-up-a-single-app-or-multi-app-kiosk), specifically the section "Prov.</span></span> <span data-ttu-id="5bd17-118">подготовки, шаг 2 — Добавление XML-файла конфигурации терминала в пакет подготовки" и см. XML-файл, сохраненный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="5bd17-118">package, step 2 – Add the kiosk configuration XML file to a provisioning package" and refer to the XML file that was saved in the previous step.</span></span>

## <span data-ttu-id="5bd17-119">Можно ли создать конфигурацию, которая глобально применяется ко всем, и отдельную конфигурацию для одной учетной записи Azure AD или группы Azure AD?</span><span class="sxs-lookup"><span data-stu-id="5bd17-119">Can I create a configuration where global applies to everyone and separate configuration applies to 1 Azure AD account or Azure AD group?</span></span> 

<span data-ttu-id="5bd17-120">Да, см. пример большого двоичного объекта XML ниже.</span><span class="sxs-lookup"><span data-stu-id="5bd17-120">Yes, refer to the example XML blob below.</span></span> <span data-ttu-id="5bd17-121">Профиль глобального ограниченного доступа применяется в HoloLens, если не обнаружен специальный профиль для вошедшего пользователя, и, таким образом, является стандартной конфигурацией режима терминала для вошедшего пользователя.</span><span class="sxs-lookup"><span data-stu-id="5bd17-121">Global Assigned Access profile is applied on HoloLens when a specific one for the signed in user is not found, so it is default kiosk mode configuration for signed-in user.</span></span>
<span data-ttu-id="5bd17-122">Пример большого двоичного объекта XML для использования:</span><span class="sxs-lookup"><span data-stu-id="5bd17-122">Here is an example of XML blob to be used:</span></span>

> [!NOTE]
> <span data-ttu-id="5bd17-123">Обратите внимание на выделенные области с пометкой `<!-`.</span><span class="sxs-lookup"><span data-stu-id="5bd17-123">Please be aware of the highlighted areas marked with `<!-`.</span></span> <span data-ttu-id="5bd17-124">В этих областях вам потребуется внести изменения в соответствии со своими предпочтениями.</span><span class="sxs-lookup"><span data-stu-id="5bd17-124">These areas will require you to make modifications based on your preferences.</span></span>

 :::code language="xml" source="samples/exclude-one-aad-user-or-group.xml" highlight="8,11,17":::

## <span data-ttu-id="5bd17-125">Исключение DeviceOwners из профиля глобального ограниченного доступа</span><span class="sxs-lookup"><span data-stu-id="5bd17-125">Excluding DeviceOwners from Global Assigned Access Profile</span></span>

<span data-ttu-id="5bd17-126">Эта функция позволяет исключить пользователя, который считается [владельцем устройства](security-adminless-os.md) HoloLens, из глобального ограниченного доступа.</span><span class="sxs-lookup"><span data-stu-id="5bd17-126">This feature allows a user who is considered “[Device owner](security-adminless-os.md)" on HoloLens to be excluded from Global Assigned Access.</span></span> <span data-ttu-id="5bd17-127">Чтобы воспользоваться этой функцией, в большом двоичном объекте XML для конфигурации терминала с несколькими приложениями добавьте выделенные строки:</span><span class="sxs-lookup"><span data-stu-id="5bd17-127">In order to take advantage of this feature, in the XML blob for multiple-app kiosk configuration, ensure highlighted lines are added:</span></span>

 :::code language="xml" source="samples/exclude-device-owners-from-global.xml" highlight="6,16-18":::

## <span data-ttu-id="5bd17-128">Дополнительные примеры глобального ограниченного доступа</span><span class="sxs-lookup"><span data-stu-id="5bd17-128">Additional Global Assigned Access Examples</span></span>

<span data-ttu-id="5bd17-129">Это пример терминала глобального ограниченного доступа. При входе пользователю предоставляется мультипрограммный терминал с приложением "Параметры", Центром отзывов и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5bd17-129">This is an example Global Assigned Access kiosk that when any user signs in they will have a multi-app kiosk with the Settings App, Feedback Hub, and Microsoft Edge.</span></span>

:::code language="xml" source="samples/kiosk-sample-global-assigned-access.xml":::

<span data-ttu-id="5bd17-130">Это пример терминала глобального ограниченного доступа, из которого исключен владелец устройства. При входе любого другого пользователя Azure AD ему предоставляется мультипрограммный терминал с приложением "Параметры", Центром отзывов и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5bd17-130">This example is a Global Assigned Access kiosk that excludes the device owner, when any other Azure AD user signs in they will have a multi-app kiosk with the Settings App, Feedback Hub, and Microsoft Edge.</span></span> <span data-ttu-id="5bd17-131">В этом терминале также есть вспомогательная конфигурация для гостевой учетной записи, в которую с экрана блокировки может войти любой пользователь.</span><span class="sxs-lookup"><span data-stu-id="5bd17-131">This kiosk also includes a secondary kiosk configuration for a Visitor account, which may be signed into by anyone on the lock screen.</span></span> <span data-ttu-id="5bd17-132">Когда пользователь входит в гостевую учетную запись, ему будет предоставлен мультипрограммный терминал, в котором есть только приложение центра отзывов и предложений.</span><span class="sxs-lookup"><span data-stu-id="5bd17-132">When a user signs into the Visitor account they will have a multi-app kiosk that only has the Feedback Hub app.</span></span>

:::code language="xml" source="samples/kiosk-sample-global-assigned-access-visitor-exclude.xml":::
