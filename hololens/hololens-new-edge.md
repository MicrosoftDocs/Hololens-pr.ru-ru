---
title: Представляем новое приложение Microsoft Edge
description: Узнайте о новом приложении Edge.
author: joyjaz
ms.author: v-jjaswinski
keywords: HoloLens, Edge, Интернет, браузер
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
ms.reviewer: ''
manager: yannisle
ms.openlocfilehash: 41978c626328903cf480a3315d56841f187bc123
ms.sourcegitcommit: 4c15afc772fba26683d9b75e38c44a018b4889f6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113640191"
---
# <a name="introducing-the-new-microsoft-edge"></a>Представляем новое приложение Microsoft Edge

![Анимация: изменение старого логотипа Microsoft Edge на новый логотип Microsoft Edge](images/new-edge.gif)

Новое приложение Microsoft Edge [основано на проекте Chromium с открытым кодом](https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration/) для повышения совместимости для клиентов и уменьшения фрагментации для веб-разработчиков.

Новое приложение Microsoft Edge станет впервые доступно клиентам HoloLens 2 в [Windows Holographic версии 21H1](hololens-release-notes.md#windows-holographic-version-21h1). Мы просим вас оставлять свои отзывы и сообщать об ошибках нашей команде с помощью функции **отправки отзывов** в новом приложении Microsoft Edge или через [Центр отзывов](hololens-feedback.md).

> [!IMPORTANT]
> Новое приложение Microsoft Edge автоматически заменит устаревшее приложение Microsoft Edge, которое [больше не поддерживается](https://blogs.windows.com/msedgedev/2021/03/09/microsoft-edge-legacy-end-of-support/) в новых выпусках.

![Снимок экрана: новое приложение Microsoft Edge](images/new-edge-ui.png)

## <a name="launching-the-new-microsoft-edge"></a>Запуск нового приложения Microsoft Edge

Новая версия Microsoft Edge ![Значок нового приложения Microsoft Edge](images/new_edge_logo.png) (сине-зеленый значок вихря) закреплена в меню "Пуск" и запускается автоматически при открытии веб-ссылки.

> [!NOTE]
> При первом запуске нового приложения Microsoft Edge на HoloLens 2 ваши параметры и данные будут импортированы из устаревшего приложения Microsoft Edge.

## <a name="configuring-policy-settings-for-the-new-microsoft-edge"></a>Настройка параметров политики для нового приложения Microsoft Edge

Новое приложение Microsoft Edge предлагает ИТ-администраторам более широкий набор политик браузера на HoloLens 2 по сравнению с устаревшим приложением Microsoft Edge.

Ниже приведены некоторые полезные ресурсы, которые позволят вам узнать, как управлять параметрами политик для нового приложения Microsoft Edge.

- [Настройка параметров политик Microsoft Edge с помощью Microsoft Intune.](/deployedge/configure-edge-with-intune)
- [Сопоставление политик устаревшего приложения Microsoft Edge и нового приложения Microsoft Edge.](/deployedge/microsoft-edge-policy-map-legacy-to-newedge)
- [Сопоставление политик Google Chrome и Microsoft Edge.](/deployedge/microsoft-edge-policy-map-chrome-to-newedge)
- [Полная документация по корпоративной версии Microsoft Edge](/deployedge/)

> [!IMPORTANT]
> Так как новое приложение Microsoft Edge поддерживает большое число политик, наша команда не может гарантировать, что каждая новая политика будет работать с HoloLens 2. Но мы провели тестирование и убедились, что все политики нового приложения Microsoft Edge, эквивалентные политикам устаревшего приложения Microsoft Edge и ранее поддерживаемые для HoloLens 2, работают ожидаемым образом. В статье [Сопоставление политик устаревшего приложения Microsoft Edge и нового приложения Microsoft Edge](/deployedge/microsoft-edge-policy-map-legacy-to-newedge) вы найдете эквивалентные политики нового приложения Microsoft Edge для каждой политики устаревшего приложения Microsoft Edge, которые вы использовали с HoloLens 2.
>
> Есть по меньшей мере две политики нового приложения Microsoft Edge, которые *не будут* работать с HoloLens 2:
> - EnterpriseModeSiteList
> - EnterpriseSiteListServiceURL

## <a name="what-to-expect-from-the-new-microsoft-edge-on-hololens-2"></a>Чего ожидать от нового приложения Microsoft Edge в HoloLens 2

Так как новое приложение Microsoft Edge является собственным приложением Win32 с новым уровнем адаптера UWP, позволяющим запускать его на устройствах, которые поддерживают только UWP, например HoloLens 2, некоторые функции могут быть доступны не сразу. В ближайшие месяцы мы реализуем поддержку новых сценариев и функций, поэтому обязательно следите за новостями на этой странице.

**Сценарии и функции, которые должны работать:**
- Первый запуск, вход в профиль и синхронизация.
- Веб-сайты должны отображаться и работать правильно.
- Большинство функций браузера (избранное, история и т. д.) должны работать ожидаемым образом.
- Темный режим
- Установка веб-приложений на устройстве.
- Установка расширений (сообщите нам, если вы используете расширения, которые не работают надлежащим образом на HoloLens 2).
- Просмотр документов в формате PDF и создание пометок в них.
- Пространственный звук из одного окна браузера.
- Обновление браузера автоматически и вручную.
- Сохранение PDF-файла из меню "Печать" (с помощью пункта меню "Сохранить в PDF").
- Расширение WebXR и 360 Viewer.
- Восстановление содержимого в нужном окне при просмотре нескольких окон в вашей среде.

**Сценарии и функции, которые не работают надлежащим образом:**
- Пространственный звук из нескольких окон с параллельными аудиопотоками.
- Модель "Посмотри на это, произнеси это".
- Печать

**Самые известные проблемы с браузером:**
- Предварительная версия экранной лупы в голографической клавиатуре отключена для нового приложения Microsoft Edge. Мы надеемся включить эту функцию в будущем обновлении, после реализации корректной работы для экранной лупы.
- Аудио может воспроизводиться в неправильном окне браузера, если открыто и активно другое окно. Эту ошибку можно устранить, закрыв другое активное окно, которое не должно воспроизводить аудио.
- При воспроизведении аудио из окна браузера в режиме следования аудио будет воспроизводиться и дальше даже после отключения этого режима. Эту проблему можно устранить, остановив воспроизведение аудио перед отключением режима следования или закрыв окно с помощью кнопки "Х".
- Взаимодействие с активным окном Microsoft Edge может приводить к непредвиденному переходу двухмерных окон других приложений в неактивный режим. Вы можете повторно активировать эти окна путем взаимодействия с ними.

## <a name="microsoft-edge-insider-channels"></a>Каналы программы предварительной оценки Microsoft Edge

Команда Microsoft Edge предоставляет сообществу участников программы предварительной оценки следующие каналы версий: Beta, Dev и Canary. Установка предварительной версии не приводит к удалению выпущенной версии Microsoft Edge на устройстве HoloLens 2. Поэтому вы можете параллельно установить несколько версий. 

Посетите [страницу программы предварительной оценки Microsoft Edge](https://www.microsoftedgeinsider.com), чтобы узнать больше о сообществе участников этой программы. Чтобы узнать больше о различных каналах предварительной оценки и начать работу, посетите [страницу скачивания Edge для предварительной оценки](https://www.microsoftedgeinsider.com/download).

Есть несколько методов установки версий Microsoft Edge в рамках программы предварительной оценки на устройстве HoloLens 2:

**Прямая установка на устройстве (сейчас доступно только для неуправляемых устройств).**
  1. На устройстве HoloLens 2 откройте [страницу скачивания версии Edge для предварительной оценки](https://www.microsoftedgeinsider.com/download).
  1. Нажмите кнопку **Download for HoloLens 2** (Скачать для HoloLens 2) для нужной версии Edge для предварительной оценки.
  1. Запустите скачанный файл MSIX из очереди скачивания Edge или из папки "Загрузки" на устройстве (с помощью Проводника).
  1. Будет запущен [установщик приложений](app-deploy-app-installer.md).
  1. Нажмите кнопку **Установить**.
  1. После успешной установки вы найдете версию Microsoft Edge Beta, Dev или Canary в виде отдельной записи в списке **Все программы** в меню "Пуск".

**Установка с помощью ПК на портале устройств Windows (требует включение [режима разработчика](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal#setting-up-hololens-to-use-windows-device-portal) на устройстве HoloLens 2)**
  1. На своем ПК откройте [страницу скачивания Edge для предварительной оценки](https://www.microsoftedgeinsider.com/download).
  1. Нажмите **кнопку со стрелкой вниз** рядом с кнопкой "Download for Windows 10" (Скачать для Windows 10) для нужной вам версии Edge для предварительной оценки.
  1. Выберите **HoloLens 2** в раскрывающемся меню.
  1. Сохраните файл MSIX в папке "Загрузки" на компьютере (или в другой папке, которую легко найти).
  1. С помощью [портала устройств Windows](/windows/mixed-reality/develop/platform-capabilities-and-apis/using-the-windows-device-portal#installing-an-app) на ПК установите скачанный файл MSIX на устройстве HoloLens 2.
  1. После успешной установки вы найдете версию Microsoft Edge Beta, Dev или Canary в виде отдельной записи в списке **Все программы** в меню "Пуск".

## <a name="using-wdac-to-block-new-microsoft-edge"></a>Использование WDAC для блокировки нового приложения Microsoft Edge

Для ИТ-администраторов, которые хотят изменить свою [политику WDAC](windows-defender-application-control-wdac.md) для блокировки нового приложения Microsoft Edge, необходимо добавить следующую запись в политику.

``` <Deny ID="ID_DENY_D_3_0" FriendlyName="C:\Data\Programs FileRule" PackageVersion="65535.65535.65535.65535" FileName="msedge.exe" /> ```

## <a name="managing-endpoints-for-the-new-microsoft-edge"></a>Управление конечными точками для нового приложения Microsoft Edge

В некоторых средах требуется учитывать ограничения сети. Чтобы обеспечить бесперебойную работу с новым приложением Edge, [включите такие конечные точки Майкрософт](/deployedge/microsoft-edge-security-endpoints).

См. дополнительные сведения о [доступных конечных точках для HoloLens](hololens-offline.md).

## <a name="install-web-apps"></a>Установка веб-приложений
 > [!Note]
> Начиная с [Windows Holographic версии 21H1](hololens-release-notes.md#windows-holographic-version-21h1) веб-приложение Office не будет предустановлено в системе. 

Вы можете воспользоваться новым приложением Edge и установить веб-приложения вместе с приложениями из Microsoft Store. Например, можно установить веб-приложение Microsoft Office для просмотра и редактирования файлов, размещенных в SharePoint или OneDrive. Чтобы установить веб-приложение Office, откройте адрес https://www.office.com и выберите в адресной строке кнопку **Приложение доступно** или **Установить Office**. Выберите **Установить** для подтверждения.
> [!IMPORTANT]
> Функции веб-приложения Office доступны, только если у HoloLens 2 есть активное подключение к Интернету.

## <a name="webxr-and-360-viewer"></a>WebXR и 360 Viewer


Новое приложение Microsoft Edge включает поддержку WebXR (замена WebVR), нового стандарта для создания иммерсивных веб-взаимодействий. Многие иммерсивные веб-взаимодействия разработаны для виртуальной реальности (они заменяют поле обзора виртуальной средой), но они также поддерживаются HoloLens 2. Стандарт WebXR также позволяет использовать иммерсивные веб-взаимодействия на основе дополненной или смешанной реальности, которая использует данные о физической среде. По мере освоения WebXR разработчиками мы ожидаем, что клиентам HoloLens 2 станут доступны новые иммерсивные взаимодействия на основе дополненной и смешанной реальности.

Расширение 360 Viewer создано на основе WebXR и устанавливается автоматически вместе с новым приложением Microsoft Edge на HoloLens 2. Это веб-расширение позволяет просматривать панорамные видео (с обзором в 360 градусов). YouTube имеет самый большой выбор панорамных видео, поэтому мы рекомендуем начать именно с этой платформы.

### <a name="how-to-use-webxr"></a>Как использовать WebXR

1. Откройте веб-сайт с поддержкой WebXR.
1. Нажмите кнопку **Enter VR** (Войти в виртуальную реальность) на веб-сайте. Расположение и визуальное представление такой кнопки на разных сайтах может быть разным, но в целом похожим на такое:

    ![Пример кнопки входа в виртуальную реальность](images/75px-enter-vr.png)

1. При первом запуске WebXR на определенном домене браузер запросит согласие на вход в иммерсивный режим. Щелкните **Allow** (Разрешить).
1. С помощью [жестов HoloLens 2](hololens2-basic-usage.md#the-hand-tracking-frame) вы можете управлять взаимодействием.
1. Если во взаимодействии нет кнопки **выхода**, используйте [жест пуска](hololens2-basic-usage.md#start-gesture), чтобы вернуться на домашнюю страницу.

**Рекомендуемые примеры WebXR**
- 360 Viewer (см. следующий раздел)
- [XR Dinosaurs](https://www.xrdinosaurs.com/)
- [Barista Express](https://constructarca.de/game/barista-express/)
- [WebXR Paint](https://threejs.org/examples/webxr_vr_paint.html)

### <a name="how-to-use-360-viewer"></a>Как использовать 360 Viewer

1. Откройте панорамное видео в YouTube.
1. В кадре видео выберите кнопку гарнитуры смешанной реальности:

    ![Кнопка для активации 360 Viewer](images/enter-360-viewer.jpg)

1. При первом запуске 360 Viewer на определенном домене браузер запросит согласие на вход в иммерсивный режим. Выберите **Разрешить**.
1. Используйте [касание](hololens2-basic-usage.md#select-using-air-tap), чтобы отобразить элементы управления воспроизведением. Используйте [телекинез и касания](hololens2-basic-usage.md#select-using-air-tap), чтобы запускать и приостанавливать воспроизведение, переходить вперед или назад, включать или отключать субтитры или останавливать взаимодействие (при этом вы выйдете из иммерсивного режима). Элементы управления воспроизведением скрываются через несколько секунд бездействия.

### <a name="top-webxr-and-360-viewer-known-issues"></a>Основные известные проблемы, связанные с WebXR и 360 Viewer
- При большой сложности взаимодействия WebXR частота кадров может быть низкой или нестабильной.
- Поддержка суставной руки в WebXR не включена по умолчанию. Разработчики могут включить такую поддержку на странице edge://flags, включив параметр WebXR Hand Input (Ввод рукой в WebXR).
- Панорамные видео, размещенные не на YouTube, могут не воспроизводиться ожидаемым образом.

### <a name="providing-feedback-on-webxr-and-360-viewer"></a>Предоставление отзывов по WebXR и 360 Viewer

Мы просим вас оставлять свои отзывы и сообщать об ошибках нашей команде с помощью функции **отправки отзывов** в новом приложении Microsoft Edge.