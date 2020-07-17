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
# Глобальный ограниченный доступ — терминал

Эта функция настраивает устройство Hololens 2 для режима терминала с несколькими приложениями, который применяется на уровне системы, не похож на удостоверения в системе и применяется ко всем, кто входит в устройство. 

> [!NOTE]
> Эта функция в настоящее время доступна только в сборках участников программы предварительной оценки Windows. Если вы хотите опробовать эту функцию до ее общей доступности в выпусках HoloLens, см. дополнительные сведения о сборках [программы предварительной оценки Windows](hololens-insider.md).
 
## Как использовать ее в Intune? 

> [!NOTE]
> Обратите внимание на области с пометкой "<!-". В этих областях вам потребуется внести изменения в соответствии со своими предпочтениями. 

1.  Создайте настраиваемый профиль конфигурации устройства OMA URI, как показано ниже, и примените его к группе устройств HoloLens: ![Глобальный ограниченный доступ OMA-URI в Intune](images/global-assigned-access-omauri.png)

2.  Для значения обновите и вставьте следующее содержимое: 

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

## Как использовать это в конструкторе конфигураций Windows? 
 
1.  Обновите и сохраните большой двоичный объект XML, упомянутый выше как XML-файл. 

2.  Выполните действия, описанные в разделе [Использование пакета подготовки для настройки терминала с одним или несколькими приложениями](https://docs.microsoft.com/hololens/hololens-kiosk#use-a-provisioning-package-to-set-up-a-single-app-or-multi-app-kiosk), в частности в секции "Пакет подготовки, шаг 2 — Добавление XML-файла конфигурации терминала в пакет подготовки" и см. XML-файл, сохраненный на предыдущем шаге. 

## Могу ли я создать конфигурацию, которая глобально применяется ко всем, кроме 1 учетной записи AAD или группы AAD? 

Да, см. пример большого двоичного объекта XML ниже. Профиль глобального ограниченного доступа применяется к Hololens, если не обнаружен специальный профиль для вошедшего пользователя, поэтому это стандартная конфигурация режима терминала для вошедшего пользователя. Пример большого двоичного объекта XML для использования: 

> [!NOTE]
> Обратите внимание на области с пометкой "<!-". В этих областях вам потребуется внести изменения в соответствии со своими предпочтениями. 

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
