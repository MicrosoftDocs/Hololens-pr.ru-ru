---
title: Глобальный ограниченный доступ
description: Руководство по использованию OMA-URI для терминалов глобального ограниченного доступа
author: evmill
ms.author: v-evmill
ms.date: 7/13/2020
ms.topic: article
keywords: hololens, hololens 2, ограниченный доступ, терминал
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: lavinds
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: ad7f75ccfcae9fb42974abb43d87f2f1ce1571f8
ms.sourcegitcommit: 3db43bc4a007b10901d8edb045f66e1e299c57a9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882453"
---
# <span data-ttu-id="e5812-104">Глобальный ограниченный доступ — терминал</span><span class="sxs-lookup"><span data-stu-id="e5812-104">Global Assigned Access – Kiosk</span></span>

<span data-ttu-id="e5812-105">Эта функция настраивает устройство Hololens 2 для режима терминала с несколькими приложениями, который применяется на уровне системы, не похож на удостоверения в системе и применяется ко всем, кто входит в устройство.</span><span class="sxs-lookup"><span data-stu-id="e5812-105">This feature configures Hololens 2 device for multiple app kiosk mode which is applicable at system level, has no affinity with any identity on the system and applies to everyone who signs into the device.</span></span> 

> [!NOTE]
> <span data-ttu-id="e5812-106">Эта функция в настоящее время доступна только в сборках участников программы предварительной оценки Windows.</span><span class="sxs-lookup"><span data-stu-id="e5812-106">This feature is currently only avalible in Windows Insider builds.</span></span> <span data-ttu-id="e5812-107">Если вы хотите опробовать эту функцию до ее общей доступности в выпусках HoloLens, см. дополнительные сведения о сборках [программы предварительной оценки Windows](hololens-insider.md).</span><span class="sxs-lookup"><span data-stu-id="e5812-107">If you would like to try this feature before it is generally avalible in HoloLens releases please read more about [Windows Insider](hololens-insider.md) builds.</span></span>
 
## <span data-ttu-id="e5812-108">Как использовать ее в Intune?</span><span class="sxs-lookup"><span data-stu-id="e5812-108">How to use this in Intune?</span></span> 

> [!NOTE]
> <span data-ttu-id="e5812-109">Обратите внимание на области с пометкой "<!-".</span><span class="sxs-lookup"><span data-stu-id="e5812-109">Please be aware of the areas marked with "<!-".</span></span> <span data-ttu-id="e5812-110">В этих областях вам потребуется внести изменения в соответствии со своими предпочтениями.</span><span class="sxs-lookup"><span data-stu-id="e5812-110">These areas will require you to make modifications based on your preferences.</span></span> 

1.  <span data-ttu-id="e5812-111">Создайте настраиваемый профиль конфигурации устройства OMA URI, как показано ниже, и примените его к группе устройств HoloLens: ![Глобальный ограниченный доступ OMA-URI в Intune</span><span class="sxs-lookup"><span data-stu-id="e5812-111">Create a custom OMA URI device configuration profile as follows and apply it to HoloLens device group: ![Global Assigned Access OMA-URI in Intune</span></span>](images/global-assigned-access-omauri.png)

2.  <span data-ttu-id="e5812-112">Для значения обновите и вставьте следующее содержимое:</span><span class="sxs-lookup"><span data-stu-id="e5812-112">For value, update and paste following content:</span></span> 

    ```xml
    <?xml version="1.0" encoding="utf-8" ?> 
    <AssignedAccessConfiguration 
        xmlns="http://schemas.microsoft.com/AssignedAccess/2017/config" 
        xmlns:v2="http://schemas.microsoft.com/AssignedAccess/201810/config" 
        xmlns:v3="http://schemas.microsoft.com/AssignedAccess/2020/config" 
        xmlns:rs5="http://schemas.microsoft.com/AssignedAccess/201810/config" 
    > 
        <Profiles> 
            <Profile Id="{8739C257-184F-45DD-8657-C235819172A3}"> 
                <AllAppsList> 
                    <AllowedApps>                     
                        <!—TODO: Add AUMIDs of apps you want to be shown here, e.g. <App AppUserModelId="Microsoft.MicrosoftEdge_8wekyb3d8bbwe!MicrosoftEdge" rs5:AutoLaunch=”true” /> --> 
                         <!—TODO: Add AUMIDs of apps you want to be shown here, e.g. <App AppUserModelId="Microsoft.settingn_8wekyb3d8bbwe!MicrosoftEdge" /> --> 
                     </AllowedApps> 
                </AllAppsList> 
                <StartLayout> 
                    <![CDATA[<LayoutModificationTemplate xmlns:defaultlayout="http://schemas.microsoft.com/Start/2014/FullDefaultLayout" xmlns:start="http://schemas.microsoft.com/Start/2014/StartLayout" Version="1" xmlns="http://schemas.microsoft.com/Start/2014/LayoutModification"> 
                          <LayoutOptions StartTileGroupCellWidth="6" /> 
                          <DefaultLayoutOverride> 
                            <StartLayoutCollection> 
                              <defaultlayout:StartLayout GroupCellWidth="6"> 
                                <start:Group Name="Life at a glance"> 
                                  <!—This AUMID can be of any app and is not used on Hololens but is required for parity, so you can leave it as is. --> 
                                  <start:Tile Size="2x2" Column="0" Row="0" AppUserModelID="Microsoft.MicrosoftEdge_8wekyb3d8bbwe!MicrosoftEdge" />                               
                                </start:Group> 
                              </defaultlayout:StartLayout> 
                            </StartLayoutCollection> 
                          </DefaultLayoutOverride> 
                        </LayoutModificationTemplate> 
                    ]]> 
                </StartLayout> 
                <Taskbar ShowTaskbar="true"/> 
            </Profile> 
        </Profiles> 
        <Configs> 
            <v3:GlobalProfile Id="{8739C257-184F-45DD-8657-C235819172A3}"/> 
        </Configs> 
    </AssignedAccessConfiguration> 
    ```

## <span data-ttu-id="e5812-113">Как использовать это в конструкторе конфигураций Windows?</span><span class="sxs-lookup"><span data-stu-id="e5812-113">How to use this in Windows Configuration Designer?</span></span> 
 
1.  <span data-ttu-id="e5812-114">Обновите и сохраните большой двоичный объект XML, упомянутый выше как XML-файл.</span><span class="sxs-lookup"><span data-stu-id="e5812-114">Update and save XML blob mentioned above as XML file.</span></span> 

2.  <span data-ttu-id="e5812-115">Выполните действия, описанные в разделе [Использование пакета подготовки для настройки терминала с одним или несколькими приложениями](https://docs.microsoft.com/hololens/hololens-kiosk#use-a-provisioning-package-to-set-up-a-single-app-or-multi-app-kiosk), в частности в секции "Пакет</span><span class="sxs-lookup"><span data-stu-id="e5812-115">Follow the steps in [Use a provisioning package to set up a single-app or multi-app kiosk](https://docs.microsoft.com/hololens/hololens-kiosk#use-a-provisioning-package-to-set-up-a-single-app-or-multi-app-kiosk), specifically the section "Prov.</span></span> <span data-ttu-id="e5812-116">подготовки, шаг 2 — Добавление XML-файла конфигурации терминала в пакет подготовки" и см. XML-файл, сохраненный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="e5812-116">package, step 2 – Add the kiosk configuration XML file to a provisioning package" and refer to the XML file that was saved in the previous step.</span></span> 

## <span data-ttu-id="e5812-117">Могу ли я создать конфигурацию, которая глобально применяется ко всем, кроме 1 учетной записи AAD или группы AAD?</span><span class="sxs-lookup"><span data-stu-id="e5812-117">Can I create a configuration where global applies to everyone except 1 AAD account or AAD group?</span></span> 

<span data-ttu-id="e5812-118">Да, см. пример большого двоичного объекта XML ниже.</span><span class="sxs-lookup"><span data-stu-id="e5812-118">Yes, please refer to the example XML blob below.</span></span> <span data-ttu-id="e5812-119">Профиль глобального ограниченного доступа применяется к Hololens, если не обнаружен специальный профиль для вошедшего пользователя, поэтому это стандартная конфигурация режима терминала для вошедшего пользователя.</span><span class="sxs-lookup"><span data-stu-id="e5812-119">Global Assigned Access profile is applied on Hololens when a specific one for the signed in user is not found, so it is default kiosk mode configuration for signed-in user.</span></span> <span data-ttu-id="e5812-120">Пример большого двоичного объекта XML для использования:</span><span class="sxs-lookup"><span data-stu-id="e5812-120">Here is an example of XML blob to be used:</span></span> 

> [!NOTE]
> <span data-ttu-id="e5812-121">Обратите внимание на области с пометкой "<!-". В этих областях вам потребуется внести изменения в соответствии со своими предпочтениями.</span><span class="sxs-lookup"><span data-stu-id="e5812-121">Please be aware of the areas marked with <!-  these areas will require you to make modifications based on your preferences.</span></span> 

```xml
<?xml version="1.0" encoding="utf-8" ?> 
<AssignedAccessConfiguration xmlns="http://schemas.microsoft.com/AssignedAccess/2017/config" 
    xmlns:v2="http://schemas.microsoft.com/AssignedAccess/201810/config" 
    xmlns:v3="http://schemas.microsoft.com/AssignedAccess/2020/config" 
    xmlns:rs5="http://schemas.microsoft.com/AssignedAccess/201810/config"> 
    <Profiles> 
        <Profile Id="{9A2A490F-10F6-4764-974A-43B19E722C23}"> 
            <!—specify AUMIDs and other nodes as used in example above --> 
        </Profile> 
        <Profile Id="{8739C257-184F-45DD-8657-C235819172A3}"> 
            <!—specify AUMIDs and other nodes as used in example above --> 
        </Profile> 
    </Profiles> 
    <Configs> 
        <v3:GlobalProfile Id="{8739C257-184F-45DD-8657-C235819172A3}"/> 
        <Config> 
           <Account>AzureAD\<!-fully qualified AAD account name></Account> 
           <DefaultProfile Id="{9A2A490F-10F6-4764-974A-43B19E722C23}"/> 
        </Config> 
    </Configs> 
</AssignedAccessConfiguration> 
```
