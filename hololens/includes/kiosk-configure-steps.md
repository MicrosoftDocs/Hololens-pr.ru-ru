---
ms.openlocfilehash: 7a7122790d3e0257c07cdd8bc8c7f658b3a0e279
ms.sourcegitcommit: 6ce962ede986ebfab21d1665722694eaee13c280
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2021
ms.locfileid: "122859430"
---
# <a name="microsoft-intune-single-app-kiosk-template"></a>[шаблон киоска для одного приложения Microsoft Intune](#tab/uisak)

## <a name="microsoft-intune-single-app-kiosk-template"></a>шаблон киоска для одного приложения Microsoft Intune

1. Создание профиля конфигурации <br> 
<kbd>
    <img alt="Create a configuration profile" src="../images/kiosk-steps/kiosk-template-sa-1.png"/>
</kbd>

<br>

2. Выбор шаблона киоска <br> 
<kbd>
    <img alt="Create a kiosk profile" src="../images/kiosk-steps/kiosk-template-sa-2.png" width="415" height="530" />
</kbd>

<br>

3. Выберите одно приложение или несколько киосков приложений, а также выберите тип назначения пользователей для режима киоска. <br> 
<kbd>
    <img alt="Select single app kiosk mode" src="../images/kiosk-steps/kiosk-template-sa-3.png"/>
</kbd>

<br>

4. Выберите приложение для запуска в режиме киоска <br> 
<kbd>
    <img alt="Choose the app" src="../images/kiosk-steps/kiosk-template-sa-4.png"/>
</kbd>

<br>

5. Оставьте оставшиеся параметры как есть. <br> 
<kbd>
    <img alt="Leave options" src="../images/kiosk-steps/kiosk-template-sa-5.png"/>
</kbd>

<br>

6. Выберите группы, устройства или пользователей, которым должен быть назначен этот профиль конфигурации <br> 
<kbd>
    <img alt="Choose how to assign" src="../images/kiosk-steps/kiosk-template-sa-6.png"/>
</kbd>

7. Проверка и создание для сохранения профиля конфигурации
8. Выполните синхронизацию MDM, начиная с любого устройства или Intune, чтобы применить конфигурацию к устройству. [синхронизация устройств из Intune](/mem/intune/remote-actions/device-sync#sync-a-device) или на устройстве с помощью **учетных записей Параметры-> — > работы или учебного заведения, >** выберите подключенную учетную запись **— > сведения — > синхронизировать**
9. Войдите в систему от имени целевого пользователя для работы в киоске.

# <a name="microsoft-intune-multi-app-kiosk-template"></a>[шаблон Microsoft Intune нескольких приложений киоска](#tab/uimak)

## <a name="microsoft-intune-multi-app-kiosk-template"></a>шаблон Microsoft Intune нескольких приложений киоска

1. Создание профиля конфигурации <br> 
<kbd>
    <img alt="Create a configuration profile" src="../images/kiosk-steps/kiosk-template-sa-1.png"/>
</kbd>

<br>

2. Выбор шаблона киоска <br> 
<kbd>
    <img alt="Create a kiosk profile" src="../images/kiosk-steps/kiosk-template-sa-2.png" width="415" height="530" />
</kbd>

<br>

3. Выберите одно приложение или несколько киосков приложений, а также выберите тип назначения пользователей для режима киоска. <br> 
<kbd>
    <img alt="Select single app kiosk mode" src="../images/kiosk-steps/kiosk-template-mak-3.png"/>
</kbd>

<br>

4. Выберите приложения для запуска в режиме киоска <br> 
<kbd>
    <img alt="Choose the app(s)" src="../images/kiosk-steps/kiosk-template-mak-4.png"/>
</kbd>

<br>

5. Оставьте оставшиеся параметры как есть. <br> 
<kbd>
    <img alt="Leave options" src="../images/kiosk-steps/kiosk-template-sa-5.png"/>
</kbd>

<br>

6. Выберите группы, устройства или пользователей, которым должен быть назначен этот профиль конфигурации <br> 
<kbd>
    <img alt="Choose how to assign" src="../images/kiosk-steps/kiosk-template-sa-6.png"/>
</kbd>

<br>

7. Проверка и создание для сохранения профиля конфигурации
8. Выполните синхронизацию MDM, начиная с любого устройства или Intune, чтобы применить конфигурацию к устройству. [синхронизация устройств из Intune](/mem/intune/remote-actions/device-sync#sync-a-device) или на устройстве с помощью **учетных записей Параметры-> — > работы или учебного заведения, >** выберите подключенную учетную запись **— > сведения — > синхронизировать**
9. Войдите в систему от имени целевого пользователя для работы в киоске.

# <a name="microsoft-intune-custom-template"></a>[Microsoft Intune настраиваемый шаблон](#tab/intunecustom)

## <a name="microsoft-intune-custom-template"></a>Microsoft Intune настраиваемый шаблон

1. Создайте конфигурацию XML для требуемого режима работы киоска. См. [примеры](../hololens-kiosk-reference.md#kiosk-xml-code-samples) для начала.

1. Создание настраиваемого профиля конфигурации <br>
<kbd>
    <img alt="Create a custom configuration profile" src="../images/kiosk-steps/kiosk-custom-1.png"/>
</kbd>

<br>

3. Укажите имя настраиваемого профиля конфигурации и щелкните "Добавить" в разделе "параметры конфигурации", чтобы добавить параметры OMA-URI. <br>
<kbd>
    <img alt="Name and add" src="../images/kiosk-steps/kiosk-custom-2.png"/>
</kbd>

<br>

4. Укажите имя параметров OMA-URI.

    1. В текстовое поле OMA-URI введите **./девице/вендор/мсфт/ассигнедакцесс/конфигуратион.**
    1. Выберите тип данных **строка**.
    1. В текстовом поле значение скопируйте и вставьте назначенный XML-файл конфигурации доступа (см. ссылки на примеры в зависимости от вашего сценария и обновите его в соответствии с ситуацией копирования).
    1. Нажмите кнопку Сохранить, чтобы сохранить параметры и конфигурацию.

    <kbd>
        <img alt="Specify OMA-URI settings" src="../images/kiosk-steps/kiosk-custom-3.png"/>
    </kbd>

<br>

5. Выберите группы, устройства или пользователей, которым должен быть назначен этот профиль конфигурации. <br>
<kbd>
    <img alt="Choose how to assign" src="../images/kiosk-steps/kiosk-custom-4.png"/>
</kbd>

<br>

6. Проверьте и создайте, чтобы сохранить профиль конфигурации.
1. Выполните синхронизацию MDM, начиная с любого устройства или Intune, чтобы применить конфигурацию к устройству. [синхронизация устройств из Intune](/mem/intune/remote-actions/device-sync#sync-a-device) или на устройстве с помощью **учетных записей Параметры-> — > работы или учебного заведения, >** выберите подключенную учетную запись **— > сведения — > синхронизировать**
1. Войдите в систему от имени целевого пользователя для работы в киоске.

# <a name="runtime-provisioning---multi-app"></a>[Подготовка среды выполнения — множественное приложение](#tab/ppkgmak)

## <a name="runtime-provisioning---multi-app"></a>Подготовка среды выполнения — множественное приложение

1. Создайте конфигурацию XML для требуемого режима работы киоска. См. [примеры](../hololens-kiosk-reference.md#kiosk-xml-code-samples) для начала.

1. откройте [конструктор конфигураций Windows](https://www.microsoft.com/store/apps/9nblggh4tx22).

1. на начальной странице выберите **подготавливать HoloLens устройства.** <br>
<kbd>
    <img alt="Selecting provision HoloLens" src="../images/kiosk-steps/kiosk-provision-1.png"/>
</kbd>

<br>

4. выберите **подготавливать HoloLens 2 устройства,** а затем нажмите кнопку далее. <br>
<kbd>
    <img alt="Select HoloLens 2" src="../images/kiosk-steps/kiosk-provision-2.png"/>
</kbd>

<br>

5. Присвойте проекту имя. При необходимости напишите описание. Для продолжения нажмите кнопку **Готово** .

6. В левом нижнем углу экрана выберите **Переключиться в расширенный редактор.** Подтвердите переключение в расширенный редактор, выбрав **Да.** <br>

    <kbd>
        <img alt="Switch to advanced editor" src="../images/kiosk-steps/kiosk-provision-2.png"/>
    </kbd>

<br>

7. В левой части разверните параметры среды выполнения, Ассигнедакцесс и выберите **мултиаппассигнедакцесс**. <br>

    <kbd>
        <img alt="select MultiAppAssignedAccess" src="../images/kiosk-steps/kiosk-provision-3.png"/>
    </kbd>

<br>

8. Нажмите кнопку **Обзор...**, , чтобы открыть обозреватель файлов. И выберите настроенный XML-файл киоска.

9. Выберите **Экспорт** , а затем **Подготовка пакета**.

    <kbd>
        <img alt="Export package" src="../images/kiosk-steps/kiosk-provision-4.png"/>
    </kbd>

<br>

10. Измените тип владельца на **ИТ Admin**. <br>

    <kbd>
        <img alt="Exporting as IT Admin" src="../images/kiosk-steps/kiosk-provision-5.png"/>
    </kbd>

<br>

11. Нажмите кнопку **Далее** три раза. Затем выберите **Сборка**.

12. После сборки пакета подготовки откройте папку выходного расположения. Ppkg-файл — это пакет подготовки. Необязательный шаг. Сохраните проект.

13. Теперь вы можете применить пакет подготовки. можно либо [применить пакет подготовки для HoloLens во время установки](../hololens-provisioning.md#apply-a-provisioning-package-to-hololens-during-setup) , либо [применить пакет подготовки для HoloLens после установки](../hololens-provisioning.md#applyremove-a-provisioning-package-to-hololens-after-setup).

14. Войдите в систему от имени целевого пользователя для работы в киоске.

# <a name="runtime-provisioning---single-app"></a>[Подготовка среды выполнения — одно приложение](#tab/ppkgsak)

## <a name="runtime-provisioning---single-app"></a>Подготовка среды выполнения — одно приложение

1. откройте [конструктор конфигураций Windows](https://www.microsoft.com/store/apps/9nblggh4tx22).

1. на начальной странице выберите **подготавливать HoloLens устройства.** <br>

    <kbd>
        <img alt="Selecting provision HoloLens" src="../images/kiosk-steps/kiosk-provision-1.png"/>
    </kbd>

<br>

3. выберите **подготавливать HoloLens 2 устройства,** а затем нажмите кнопку далее. <br>

    <kbd>
        <img alt="Select HoloLens 2" src="../images/kiosk-steps/kiosk-provision-2.png"/>
    </kbd>

<br>

4. Присвойте проекту имя. При необходимости напишите описание. Для продолжения нажмите кнопку **Готово** .

5. В левом нижнем углу экрана выберите **Переключиться в расширенный редактор.** Подтвердите переключение в расширенный редактор, выбрав **Да.** <br>

    <kbd>
        <img alt="Switch to advanced editor" src="../images/kiosk-steps/kiosk-provision-2.png"/>
    </kbd>

<br>

6. В левой части разверните параметры среды выполнения, Ассигнедакцесс и выберите **ассигнедакцесссеттингс**. <br>

    <kbd>
        <img alt="Navigate to assigned access settings" src="../images/kiosk-steps/kiosk-provision-sak-1.png"/>
    </kbd>

<br>

7. Определите свое киоск в текстовом поле. Например, в следующем примере создается единое приложение киоска для локальной учетной записи с именем LocalAccount, которое является приложением параметров.
```{"Account":"LocalAccount","AUMID":"BAEAEF15-9BAB-47FC-800B-ACECAD2AE94B_cw5n1h2txyewy!App"}```

8. Выберите **Экспорт** , а затем **Подготовка пакета**. <br>

    <kbd>
        <img alt="Export package" src="../images/kiosk-steps/kiosk-provision-4.png"/>
    </kbd>

<br>

9. Измените тип владельца на **ИТ Admin**. <br>

    <kbd>
        <img alt="Exporting as IT Admin" src="../images/kiosk-steps/kiosk-provision-5.png"/>
    </kbd>

<br>

10. Нажмите кнопку **Далее** три раза. Затем выберите **Сборка**.

11. После сборки пакета подготовки откройте папку выходного расположения. Ppkg-файл — это пакет подготовки. Необязательный шаг. Сохраните проект.

12. Теперь вы можете применить пакет подготовки. можно либо [применить пакет подготовки для HoloLens во время установки](../hololens-provisioning.md#apply-a-provisioning-package-to-hololens-during-setup) , либо [применить пакет подготовки для HoloLens после установки](../hololens-provisioning.md#applyremove-a-provisioning-package-to-hololens-after-setup).