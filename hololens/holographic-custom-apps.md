---
title: управление пользовательскими приложениями для HoloLens (1-й общий)
description: узнайте, как устанавливать, удалять и загружать неопубликованные пользовательские приложения holographic на HoloLens устройствах с помощью портала устройств и Visual Studio.
ms.assetid: 6bd124c4-731c-4bcc-86c7-23f9b67ff616
ms.date: 12/10/2020
manager: v-miegge
keywords: hololens, загружать неопубликованные, Загрузка на стороне сервера, Загрузка, сохранение, UWP, приложение, установка
ms.prod: hololens
ms.sitesec: library
author: mattzmsft
ms.author: mazeller
ms.topic: article
ms.localizationpriority: medium
ms.custom:
- CI 111456
- CSSTroubleshooting
appliesto:
- HoloLens (1st gen)
ms.openlocfilehash: 7d564fd00567033060428d5b47b34ddf827dea2fdeeb8955c73bc22e4ba87164
ms.sourcegitcommit: f8e7cc2fbdcdf8962700fd50b9c017bd83d1ad65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "115664963"
---
# <a name="manage-custom-apps-for-hololens-1st-gen"></a>управление пользовательскими приложениями для HoloLens (1-й общий)

HoloLens поддерживает множество существующих приложений из Microsoft Store, а также новые приложения, разработанные специально для HoloLens. В этой статье рассматриваются пользовательские приложения Holographic.  

Дополнительные сведения о приложениях Магазина см. [в статье Управление приложениями с помощью магазина](holographic-store-apps.md).

> [!IMPORTANT]
> следующие сведения были созданы для HoloLens (1-го поколения), также называемого HoloLens Developer Edition. такие приложения для загрузки неопубликованных приложений с помощью портала устройств и установки приложений с помощью Visual Studio были распространены. Для корпоративных развертываний не рекомендуется включать режим разработчика, который используется обоими методами. Если вы заинтересованы в безопасном методе развертывания приложений, ознакомьтесь с нашим [руководством по управлению приложениями: обзор](app-deploy-overview.md).
>
> если вы ищете метод установки приложения для HoloLens 2 устройств, обратитесь по следующим ссылке:
>
> - [Портал устройств: Установка приложения](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal#installing-an-app)
> - [использование Visual Studio для развертывания и отладки приложений](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-visual-studio)

## <a name="install-custom-apps"></a>Установка пользовательских приложений

вы можете установить собственные приложения на HoloLens либо с помощью портала устройств, либо путем развертывания приложений из Visual Studio.

### <a name="installing-an-application-package-with-the-device-portal"></a>Установка пакета приложения с помощью портала устройств

1. Установите подключение с [портала устройств](/windows/mixed-reality/using-the-windows-device-portal) к целевой HoloLens.

1. В левой области навигации перейдите на страницу **приложения** .

1. В разделе **пакет приложения** найдите appx-файл, связанный с вашим приложением.

   > [!IMPORTANT]
   > Обязательно сослаться на все связанные файлы зависимостей и сертификатов.

1. Выберите **Перейти**.

   > [!div class="mx-imgBorder"]
   > ![установите форму приложения на портале устройств Windows на Microsoft HoloLens](images/deviceportal-appmanager.jpg)

### <a name="deploying-from-microsoft-visual-studio-2015"></a>развертывание из Microsoft Visual Studio 2015

1. откройте решение Visual Studio приложения (sln-файл).

1. Откройте **Свойства** проекта.

1. Выберите следующую конфигурацию сборки: **master/x86/удаленный компьютер**.

1. При выборе **удаленного компьютера**:
   - Убедитесь, что адрес указывает на Wi-Fi IP-адрес HoloLens.
   - Задайте для параметра Проверка подлинности значение **универсальный (незашифрованный протокол)**.
   
1. Выполните построение решения.

1. чтобы развернуть приложение с компьютера разработки на HoloLens, выберите **удаленный компьютер**. если у вас уже есть сборка на HoloLens, выберите **да** , чтобы установить эту новую версию.  

   ![развертывание удаленного компьютера для приложений для Microsoft HoloLens в Visual Studio](images/vs2015-remotedeployment.jpg)  
   
1. Приложение будет установлено и запущено на HoloLens.

После установки приложения его можно найти в списке **все приложения** (**запустить**  >  **все приложения**).
