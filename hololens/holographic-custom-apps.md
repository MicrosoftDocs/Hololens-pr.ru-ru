---
title: Управление пользовательскими приложениями для HoloLens (1-й общий)
description: Узнайте, как устанавливать, удалять и загружать пользовательские приложения holographic на устройствах HoloLens с помощью портала устройств и Visual Studio.
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
ms.openlocfilehash: 721c169c8ad34acab6914448af8ffc6ceec97a0e
ms.sourcegitcommit: ad53ba5edd567a18f0c172578d78db3190701650
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "108309310"
---
# <a name="manage-custom-apps-for-hololens-1st-gen"></a>Управление пользовательскими приложениями для HoloLens (1-й общий)

HoloLens поддерживает множество существующих приложений из Microsoft Store, а также новые приложения, разработанные специально для HoloLens. В этой статье рассматриваются пользовательские приложения Holographic.  

Дополнительные сведения о приложениях Магазина см. [в статье Управление приложениями с помощью магазина](holographic-store-apps.md).

> [!IMPORTANT]
> Следующие сведения были созданы для HoloLens (1-го поколения), также называемого выпуском "HoloLens Developer Edition". Такие приложения для загрузки неопубликованных приложений с помощью портала устройств и установки приложений с помощью Visual Studio были распространены. Для корпоративных развертываний не рекомендуется включать режим разработчика, который используется обоими методами. Если вы заинтересованы в безопасном методе развертывания приложений, ознакомьтесь с нашим [руководством по управлению приложениями: обзор](app-deploy-overview.md).
>
> Если вы ищете метод установки приложения для устройств HoloLens 2, ознакомьтесь с разработкой:
> - [Портал устройств: Установка приложения](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal#installing-an-app)
> - [Развертывание и отладка приложений с помощью Visual Studio](https://docs.microsoft.com/windows/mixed-reality/develop/platform-capabilities-and-apis/using-visual-studio)

## <a name="install-custom-apps"></a>Установка пользовательских приложений

Вы можете установить собственные приложения на HoloLens с помощью портала устройств или путем развертывания приложений из Visual Studio.

### <a name="installing-an-application-package-with-the-device-portal"></a>Установка пакета приложения с помощью портала устройств

1. Установите подключение с [портала устройства](https://docs.microsoft.com/windows/mixed-reality/using-the-windows-device-portal) к целевому HoloLens.

1. В левой области навигации перейдите на страницу **приложения** .

1. В разделе **пакет приложения** найдите appx-файл, связанный с вашим приложением.

   > [!IMPORTANT]
   > Обязательно сослаться на все связанные файлы зависимостей и сертификатов.

1. Выберите **Перейти**.

   > [!div class="mx-imgBorder"]
   > ![Установка формы приложения на портале устройств Windows в Microsoft HoloLens](images/deviceportal-appmanager.jpg)

### <a name="deploying-from-microsoft-visual-studio-2015"></a>Развертывание из Microsoft Visual Studio 2015

1. Откройте решение Visual Studio приложения (SLN-файл).

1. Откройте **Свойства** проекта.

1. Выберите следующую конфигурацию сборки: **master/x86/удаленный компьютер**.

1. При выборе **удаленного компьютера**:
   - Убедитесь, что адрес указывает на Wi-Fi IP-адрес HoloLens.
   - Задайте для параметра Проверка подлинности значение **универсальный (незашифрованный протокол)**.
   
1. Выполните построение решения.

1. Чтобы развернуть приложение с компьютера разработки в HoloLens, выберите **Удаленный компьютер**. Если у вас уже есть сборка на HoloLens, выберите **Да** , чтобы установить эту новую версию.  

   ![Развертывание удаленного компьютера для приложений в Microsoft HoloLens в Visual Studio](images/vs2015-remotedeployment.jpg)  
   
1. Приложение будет установлено и запущено на HoloLens.

После установки приложения его можно найти в списке **все приложения** (**запустить**  >  **все приложения**).
