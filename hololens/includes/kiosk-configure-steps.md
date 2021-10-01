---
ms.openlocfilehash: 3d6b36124cd50dcc9f420227cb7787f0d787c013
ms.sourcegitcommit: c73cdefbdb4411f6a187cc38bb2570dadeb156bf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2021
ms.locfileid: "129220551"
---
# <a name="microsoft-intune-single-app-kiosk-template"></a>[Шаблон для режима киоска Microsoft Intune с одним приложением](#tab/uisak)

### <a name="microsoft-intune-single-app-kiosk-template"></a>Шаблон для режима киоска Microsoft Intune с одним приложением

1. Создайте профиль конфигурации. <br>
<kbd>
    <img alt="Create a configuration profile" src="../images/kiosk-steps/kiosk-template-sa-1.png"/>
</kbd>

<br>

2. Выберите шаблон для режима киоска. <br>
<kbd>
    <img alt="Create a kiosk profile" src="../images/kiosk-steps/kiosk-template-sa-2.png" width="415" height="530" />
</kbd>

<br>

3. Выберите режим киоска для одного или нескольких приложений, а также укажите, для каких пользователей он предназначен. <br>
<kbd>
    <img alt="Select single app kiosk mode" src="../images/kiosk-steps/kiosk-template-sa-3.png"/>
</kbd>

<br>

4. Выберите приложение для запуска в режиме киоска. <br>
<kbd>
    <img alt="Choose the app" src="../images/kiosk-steps/kiosk-template-sa-4.png"/>
</kbd>

<br>

5. Оставьте для остальных параметров значения по умолчанию. <br>
<kbd>
    <img alt="Leave options" src="../images/kiosk-steps/kiosk-template-sa-5.png"/>
</kbd>

<br>

6. Выберите группы, устройства или пользователей, которым должен быть назначен этот профиль конфигурации. <br> 
<kbd>
    <img alt="Choose how to assign" src="../images/kiosk-steps/kiosk-template-sa-6.png"/>
</kbd>

7. Щелкните "Просмотреть и создать", чтобы сохранить профиль конфигурации.
8. Выполните синхронизацию на сервере управления мобильными устройствами на устройстве или в Intune, чтобы применить конфигурацию к устройству. [Синхронизируйте устройства в Intune](/mem/intune/remote-actions/device-sync#sync-a-device) или на устройстве, выбрав **Параметры > Учетные записи > Рабочая или учебная >** используемая учетная запись   **> Сведения > Синхронизировать**.
9. Войдите в систему с учетными данными пользователя, чтобы проверить работу устройства в режиме киоска.

# <a name="microsoft-intune-multi-app-kiosk-template"></a>[Шаблон для режима киоска Microsoft Intune с несколькими приложениями](#tab/uimak)

### <a name="microsoft-intune-multi-app-kiosk-template"></a>Шаблон для режима киоска Microsoft Intune с несколькими приложениями

1. Создайте профиль конфигурации. <br>
<kbd>
    <img alt="Create a configuration profile" src="../images/kiosk-steps/kiosk-template-sa-1.png"/>
</kbd>

<br>

2. Выберите шаблон для режима киоска. <br>
<kbd>
    <img alt="Create a kiosk profile" src="../images/kiosk-steps/kiosk-template-sa-2.png" width="415" height="530" />
</kbd>

<br>

3. Выберите режим киоска для одного или нескольких приложений, а также укажите, для каких пользователей он предназначен. <br>
<kbd>
    <img alt="Select single app kiosk mode" src="../images/kiosk-steps/kiosk-template-mak-3.png"/>
</kbd>

<br>

4. Выберите приложения для запуска в режиме киоска <br>
<kbd>
    <img alt="Choose the app(s)" src="../images/kiosk-steps/kiosk-template-mak-4.png"/>
</kbd>

<br>

5. Оставьте для остальных параметров значения по умолчанию. <br>
<kbd>
    <img alt="Leave options" src="../images/kiosk-steps/kiosk-template-sa-5.png"/>
</kbd>

<br>

6. Выберите группы, устройства или пользователей, которым должен быть назначен этот профиль конфигурации. <br> 
<kbd>
    <img alt="Choose how to assign" src="../images/kiosk-steps/kiosk-template-sa-6.png"/>
</kbd>

<br>

7. Щелкните "Просмотреть и создать", чтобы сохранить профиль конфигурации.
8. Выполните синхронизацию на сервере управления мобильными устройствами на устройстве или в Intune, чтобы применить конфигурацию к устройству. [Синхронизируйте устройства в Intune](/mem/intune/remote-actions/device-sync#sync-a-device) или на устройстве, выбрав **Параметры > Учетные записи > Рабочая или учебная >** используемая учетная запись   **> Сведения > Синхронизировать**.
9. Войдите в систему с учетными данными пользователя, чтобы проверить работу устройства в режиме киоска.

# <a name="microsoft-intune-custom-template"></a>[Настраиваемый шаблон для режима киоска Microsoft Intune](#tab/intunecustom)

### <a name="microsoft-intune-custom-template"></a>Настраиваемый шаблон для режима киоска Microsoft Intune

1. Создайте XML-файл конфигурации для режима киоска. Сначала ознакомьтесь с [примерами](../hololens-kiosk-reference.md#kiosk-xml-code-samples).

1. Создайте настраиваемый профиль конфигурации. <br>
<kbd>
    <img alt="Create a custom configuration profile" src="../images/kiosk-steps/kiosk-custom-1.png"/>
</kbd>

<br>

3. Укажите имя профиля и в разделе "Параметры конфигурации" щелкните "Добавить", чтобы добавить параметры OMA-URI. <br>
<kbd>
    <img alt="Name and add" src="../images/kiosk-steps/kiosk-custom-2.png"/>
</kbd>

<br>

4. Укажите имя параметров OMA-URI.

    1. В текстовом поле рядом с параметром OMA-URI введите **./Device/Vendor/MSFT/AssignedAccess/Configuration**.
    1. В качестве типа данных выберите вариант **Строка**.
    1. Скопируйте XML-файл конфигурации ограниченного доступа и вставьте его в поле "Значение" (предварительно просмотрите доступные по ссылкам примеры и внесите в файл необходимые изменения с учетом своего сценария).
    1. Нажмите кнопку "Сохранить", чтобы сохранить параметры и конфигурацию.

    <kbd>
        <img alt="Specify OMA-URI settings" src="../images/kiosk-steps/kiosk-custom-3.png"/>
    </kbd>

<br>

5. Выберите группы, устройства или пользователей, которым должен быть назначен этот профиль конфигурации. <br>
<kbd>
    <img alt="Choose how to assign" src="../images/kiosk-steps/kiosk-custom-4.png"/>
</kbd>

<br>

6. Щелкните "Просмотреть и создать", чтобы сохранить профиль конфигурации.
1. Выполните синхронизацию на сервере управления мобильными устройствами на устройстве или в Intune, чтобы применить конфигурацию к устройству. [Синхронизируйте устройства в Intune](/mem/intune/remote-actions/device-sync#sync-a-device) или на устройстве, выбрав **Параметры > Учетные записи > Рабочая или учебная >** используемая учетная запись   **> Сведения > Синхронизировать**.
1. Войдите в систему с учетными данными пользователя, чтобы проверить работу устройства в режиме киоска.

# <a name="runtime-provisioning---multi-app"></a>[Подготовка среды выполнения для нескольких приложений](#tab/ppkgmak)

### <a name="runtime-provisioning---multi-app"></a>Подготовка среды выполнения для нескольких приложений

1. Создайте XML-файл конфигурации для режима киоска. Сначала ознакомьтесь с [примерами](../hololens-kiosk-reference.md#kiosk-xml-code-samples).

1. Откройте [конструктор конфигураций Windows](https://www.microsoft.com/store/apps/9nblggh4tx22).

1. На начальной странице выберите **Подготовка устройств HoloLens**. <br>
<kbd>
    <img alt="Selecting provision HoloLens" src="../images/kiosk-steps/kiosk-provision-1.png"/>
</kbd>

<br>

4. Выберите **Подготовить устройства HoloLens 2** и щелкните "Далее". <br>
<kbd>
    <img alt="Select HoloLens 2" src="../images/kiosk-steps/kiosk-provision-2.png"/>
</kbd>

<br>

5. Присвойте проекту имя. При необходимости добавьте описание. Щелкните **Готово**, чтобы продолжить.

6. В левом нижнем углу экрана щелкните **Переключиться в расширенный редактор**. Подтвердите действие, выбрав **Да**. <br>

    <kbd>
        <img alt="Switch to advanced editor" src="../images/kiosk-steps/kiosk-provision-2.png"/>
    </kbd>

<br>

7. В левой части разверните узел "Параметры среды выполнения" и выберите AssignedAccess > **MultiAppAssignedAccess**. <br>

    <kbd>
        <img alt="select MultiAppAssignedAccess" src="../images/kiosk-steps/kiosk-provision-3.png"/>
    </kbd>

<br>

8. Нажмите кнопку **Обзор...**, чтобы открыть проводник. Выберите настроенный XML-файл киоска.

9. Щелкните **Экспорт** и выберите **Пакет подготовки**.

    <kbd>
        <img alt="Export package" src="../images/kiosk-steps/kiosk-provision-4.png"/>
    </kbd>

<br>

10. Для параметра типа владельца выберите вариант **ИТ-администратор**. <br>

    <kbd>
        <img alt="Exporting as IT Admin" src="../images/kiosk-steps/kiosk-provision-5.png"/>
    </kbd>

<br>

11. Нажмите кнопку **Далее** три раза. Выберите **Сборка**.

12. После сборки пакета подготовки откройте папку с выходными данными. PPKG-файл — это пакет подготовки. При необходимости сохраните проект.

13. Теперь вы можете применить пакет подготовки к устройствам HoloLens. Это можно сделать [до](../hololens-provisioning.md#apply-a-provisioning-package-to-hololens-during-setup) или [после](../hololens-provisioning.md#applyremove-a-provisioning-package-to-hololens-after-setup) установки.

14. Войдите в систему с учетными данными пользователя, чтобы проверить работу устройства в режиме киоска.

# <a name="runtime-provisioning---single-app"></a>[Подготовка среды выполнения для одного приложения](#tab/ppkgsak)

### <a name="runtime-provisioning---single-app"></a>Подготовка среды выполнения для одного приложения

1. Откройте [конструктор конфигураций Windows](https://www.microsoft.com/store/apps/9nblggh4tx22).

1. На начальной странице выберите **Подготовка устройств HoloLens**. <br>

    <kbd>
        <img alt="Selecting provision HoloLens" src="../images/kiosk-steps/kiosk-provision-1.png"/>
    </kbd>

<br>

3. Выберите **Подготовить устройства HoloLens 2** и щелкните "Далее". <br>

    <kbd>
        <img alt="Select HoloLens 2" src="../images/kiosk-steps/kiosk-provision-2.png"/>
    </kbd>

<br>

4. Присвойте проекту имя. При необходимости добавьте описание. Щелкните **Готово**, чтобы продолжить.

5. В левом нижнем углу экрана щелкните **Переключиться в расширенный редактор**. Подтвердите действие, выбрав **Да**. <br>

    <kbd>
        <img alt="Switch to advanced editor" src="../images/kiosk-steps/kiosk-provision-2.png"/>
    </kbd>

<br>

6. В левой части разверните узел "Параметры среды выполнения" и выберите AssignedAccess > **AssignedAccessSettings**. <br>

    <kbd>
        <img alt="Navigate to assigned access settings" src="../images/kiosk-steps/kiosk-provision-sak-1.png"/>
    </kbd>

<br>

7. Определите режим киоска в текстовом поле. Например, следующая строка задает режим киоска с одним приложением ("Параметры") для локальной учетной записи с именем LocalAccount:
```{"Account":"LocalAccount","AUMID":"BAEAEF15-9BAB-47FC-800B-ACECAD2AE94B_cw5n1h2txyewy!App"}```

8. Щелкните **Экспорт** и выберите **Пакет подготовки**. <br>

    <kbd>
        <img alt="Export package" src="../images/kiosk-steps/kiosk-provision-4.png"/>
    </kbd>

<br>

9. Для параметра типа владельца выберите вариант **ИТ-администратор**. <br>

    <kbd>
        <img alt="Exporting as IT Admin" src="../images/kiosk-steps/kiosk-provision-5.png"/>
    </kbd>

<br>

10. Нажмите кнопку **Далее** три раза. Выберите **Сборка**.

11. После сборки пакета подготовки откройте папку с выходными данными. PPKG-файл — это пакет подготовки. При необходимости сохраните проект.

12. Теперь вы можете применить пакет подготовки к устройствам HoloLens. Это можно сделать [до](../hololens-provisioning.md#apply-a-provisioning-package-to-hololens-during-setup) или [после](../hololens-provisioning.md#applyremove-a-provisioning-package-to-hololens-after-setup) установки.