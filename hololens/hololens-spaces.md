---
title: Сопоставление физических пространств с HoloLens
description: Устройство HoloLens постепенно знакомится с окружающим пространством. Пользователи могут упростить этот процесс, перемещая HoloLens в пространстве определенным образом.
ms.assetid: bd55ecd1-697a-4b09-8274-48d1499fcb0b
author: dorreneb
ms.author: dobrown
ms.custom:
- CI 111456
- CSSTroubleshooting
ms.date: 09/16/2019
keywords: hololens, Windows Mixed Reality, пространственное сопоставление, HoloLens, реконструкция поверхности, сетка, отслеживание головы, сопоставление
ms.prod: hololens
ms.sitesec: library
ms.topic: article
ms.localizationpriority: high
appliesto:
- HoloLens 1 (1st gen)
- HoloLens 2
ms.openlocfilehash: 7cedf2af90744477c33736087c85a43168167707
ms.sourcegitcommit: 6f2ec9ced776166f96eddcd601bef5de715703a5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931841"
---
# <span data-ttu-id="8c922-105">Сопоставление физических пространств с HoloLens</span><span class="sxs-lookup"><span data-stu-id="8c922-105">Map physical spaces with HoloLens</span></span>

<span data-ttu-id="8c922-106">Устройство HoloLens совмещает голограммы с физическим миром.</span><span class="sxs-lookup"><span data-stu-id="8c922-106">HoloLens blends holograms with your physical world.</span></span> <span data-ttu-id="8c922-107">Для этого HoloLens необходимо познакомиться с окружающим физическим миром и запомнить, куда в пространстве вы помещаете голограммы.</span><span class="sxs-lookup"><span data-stu-id="8c922-107">To do that, HoloLens has to learn about the physical world around you and remember where you place holograms within that space.</span></span>

<span data-ttu-id="8c922-108">С течением времени HoloLens построит *пространственную карту* увиденной окружающей среды.</span><span class="sxs-lookup"><span data-stu-id="8c922-108">Over time, the HoloLens builds up a *spatial map* of the environment that it has seen.</span></span>  <span data-ttu-id="8c922-109">HoloLens обновляет карту по мере изменения среды.</span><span class="sxs-lookup"><span data-stu-id="8c922-109">HoloLens updates the map as the environment changes.</span></span> <span data-ttu-id="8c922-110">После того как вы войдете в свою учетную запись и включите устройство, HoloLens начнет создавать и обновлять пространственные карты.</span><span class="sxs-lookup"><span data-stu-id="8c922-110">As long as you are logged in and the device is turned on, HoloLens creates and updates your spatial maps.</span></span> <span data-ttu-id="8c922-111">Когда камера устройства направлена в пространство, HoloLens пытается создать карту зоны.</span><span class="sxs-lookup"><span data-stu-id="8c922-111">If you hold or wear the device with the cameras pointed at a space, the HoloLens tries to map the area.</span></span> <span data-ttu-id="8c922-112">HoloLens обучается естественным образом с течением времени, однако вы можете упростить и ускорить процесс создания карты вашего пространства.</span><span class="sxs-lookup"><span data-stu-id="8c922-112">While the HoloLens learns a space naturally over time, there are ways in which you can help HoloLens map your space more quickly and efficiently.</span></span>  

> [!NOTE]
> <span data-ttu-id="8c922-113">Если HoloLens не может создать карту пространства или устройство не откалибровано, HoloLens может переключиться в ограниченный режим работы.</span><span class="sxs-lookup"><span data-stu-id="8c922-113">If your HoloLens can't map your space or is out of calibration, HoloLens may enter Limited mode.</span></span> <span data-ttu-id="8c922-114">В этом режиме размещение голограмм невозможно.</span><span class="sxs-lookup"><span data-stu-id="8c922-114">In Limited mode, you won't be able to place holograms in your surroundings.</span></span>

<span data-ttu-id="8c922-115">В данной статье рассмотрено, как HoloLens создает карты пространств, как улучшить этот процесс и как управлять пространственными данными, собранными устройством.</span><span class="sxs-lookup"><span data-stu-id="8c922-115">This article explains how HoloLens maps spaces, how to improve spatial mapping, and how to manage the spatial data that HoloLens collects.</span></span>

## <span data-ttu-id="8c922-116">Выбор и настройка пространства</span><span class="sxs-lookup"><span data-stu-id="8c922-116">Choosing and setting up and your space</span></span>

<span data-ttu-id="8c922-117">Характеристики окружающей среды могут затруднять для HoloLens процесс анализа пространства.</span><span class="sxs-lookup"><span data-stu-id="8c922-117">Features in your environment can make it difficult for the HoloLens to interpret a space.</span></span> <span data-ttu-id="8c922-118">Низкий уровень освещенности, материалы в пространстве, расположение объектов и многое другое— все это может влиять на результаты создания карты пространства.</span><span class="sxs-lookup"><span data-stu-id="8c922-118">Light levels, materials in the space, the layout of objects, and more can all affect how HoloLens maps an area.</span></span>

<span data-ttu-id="8c922-119">HoloLens работает максимально эффективно в определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="8c922-119">HoloLens works best in certain kinds of environments.</span></span> <span data-ttu-id="8c922-120">Для достижения наилучших результатов при создании пространственной карты выберите достаточно просторную и хорошо освещенную комнату.</span><span class="sxs-lookup"><span data-stu-id="8c922-120">To produce the best spatial map, choose a room that has adequate light and plenty of space.</span></span> <span data-ttu-id="8c922-121">Избегайте слабо освещенных комнат и комнат с большим количеством темных, блестящих и полупрозрачных поверхностей (например, зеркала или тонкие шторы).</span><span class="sxs-lookup"><span data-stu-id="8c922-121">Avoid dark spaces and rooms that have a lot of dark, shiny, or translucent surfaces (for instance, mirrors or gauzy curtains).</span></span>

<span data-ttu-id="8c922-122">Устройство HoloLens лучше всего работает внутри помещений.</span><span class="sxs-lookup"><span data-stu-id="8c922-122">HoloLens is optimized for indoor use.</span></span> <span data-ttu-id="8c922-123">Качество пространственного сопоставления также улучшается, когда включен Wi-Fi. При этом подключение к Интернету не требуется.</span><span class="sxs-lookup"><span data-stu-id="8c922-123">Spatial mapping also works best when Wi-Fi is turned on, although it doesn't have to be connected to a network.</span></span> <span data-ttu-id="8c922-124">HoloLens может использовать точки доступа Wi-Fi, даже если соединение не установлено и проверка подлинности не пройдена.</span><span class="sxs-lookup"><span data-stu-id="8c922-124">HoloLens can obtain Wi-Fi access points even if it is not connected or authenticated.</span></span> <span data-ttu-id="8c922-125">Функциональность HoloLens будет одинаковой независимо от того, подключены ли точки доступа к Интернету или только к интрасети/локальной сети.</span><span class="sxs-lookup"><span data-stu-id="8c922-125">HoloLens functionality does not change whether the access points are internet-connected or intranet/local only.</span></span>

<span data-ttu-id="8c922-126">Используйте HoloLens только в безопасных помещениях, где отсутствует риск спотыкания.</span><span class="sxs-lookup"><span data-stu-id="8c922-126">Only use HoloLens in safe places with no tripping hazards.</span></span> <span data-ttu-id="8c922-127">[Дополнительные сведения о безопасности](https://support.microsoft.com/help/4023454/safety-information).</span><span class="sxs-lookup"><span data-stu-id="8c922-127">[More on safety](https://support.microsoft.com/help/4023454/safety-information).</span></span>

## <span data-ttu-id="8c922-128">Создание карты пространства</span><span class="sxs-lookup"><span data-stu-id="8c922-128">Mapping your space</span></span>

<span data-ttu-id="8c922-129">Теперь вы готовы приступить к созданию карты пространства.</span><span class="sxs-lookup"><span data-stu-id="8c922-129">Now you're ready to start mapping your spare.</span></span>  <span data-ttu-id="8c922-130">В процессе создания карты HoloLens проецирует сетку сопоставления на окружающее пространство.</span><span class="sxs-lookup"><span data-stu-id="8c922-130">When HoloLens starts mapping your surroundings, you'll see a mesh graphic spreading over the space.</span></span>  <span data-ttu-id="8c922-131">В доме в смешанной реальности можно отобразить карту путем выбора сопоставленной поверхности.</span><span class="sxs-lookup"><span data-stu-id="8c922-131">In mixed reality home, you can trigger the map to show by selecting on a mapped surface.</span></span>

<span data-ttu-id="8c922-132">Далее приведены рекомендации для достижения наилучших результатов при создании пространственных карт.</span><span class="sxs-lookup"><span data-stu-id="8c922-132">Here are guidelines for building a great spatial map.</span></span>

### <span data-ttu-id="8c922-133">Общие сведения о сценариях для зоны использования</span><span class="sxs-lookup"><span data-stu-id="8c922-133">Understand the scenarios for the area</span></span>

<span data-ttu-id="8c922-134">Чтобы создать актуальную и полную карту, крайне важно провести достаточно времени в месте, где вы планируете использовать HoloLens.</span><span class="sxs-lookup"><span data-stu-id="8c922-134">It is important to spend the most time where you will be using the HoloLens, so that the map is relevant and complete.</span></span> <span data-ttu-id="8c922-135">Например, если сценарий использования HoloLens предусматривает перемещение из точкиА в точкуБ, пройдите по этой траектории 2–3раза, поворачивая при этом голову во все стороны.</span><span class="sxs-lookup"><span data-stu-id="8c922-135">For example, if a user scenario for HoloLens involves moving from Point A to Point B, walk that path two to three times, looking in all directions as you move.</span></span>  

### <span data-ttu-id="8c922-136">Перемещайтесь по пространству медленно.</span><span class="sxs-lookup"><span data-stu-id="8c922-136">Walk slowly around the space</span></span>

<span data-ttu-id="8c922-137">В случае быстрого прохождения HoloLens с большой вероятность пропустит некоторые зоны.</span><span class="sxs-lookup"><span data-stu-id="8c922-137">If you walk too quickly around the area, it's likely that the HoloLens will miss mapping areas.</span></span> <span data-ttu-id="8c922-138">Двигайтесь медленно, останавливаясь каждые 1,5–2,5метра, чтобы посмотреть вокруг.</span><span class="sxs-lookup"><span data-stu-id="8c922-138">Walk slowly around the space, stopping every 5-8 feet to look around at your surroundings.</span></span>  

<span data-ttu-id="8c922-139">Плавность движения также будет способствовать созданию более точной карты.</span><span class="sxs-lookup"><span data-stu-id="8c922-139">Smooth movements also help the HoloLens map more efficiently.</span></span>

### <span data-ttu-id="8c922-140">Смотрите во всех направлениях</span><span class="sxs-lookup"><span data-stu-id="8c922-140">Look in all directions</span></span>

<span data-ttu-id="8c922-141">Смотря во всех направления при создании карты, вы даете HoloLens возможность получить больше данных об относительном расположении точек в пространстве.</span><span class="sxs-lookup"><span data-stu-id="8c922-141">Looking around as you map the space gives the HoloLens more data on where points are relative to each other.</span></span>  

<span data-ttu-id="8c922-142">Например, если вы не посмотрите вверх, HoloLens не будет знать, где в комнате находится потолок.</span><span class="sxs-lookup"><span data-stu-id="8c922-142">If you don't look up, for example, the HoloLens may not know where the ceiling in a room is.</span></span>  

<span data-ttu-id="8c922-143">Также не забудьте посмотреть вниз на пол.</span><span class="sxs-lookup"><span data-stu-id="8c922-143">Don't forget to look down at the floor as you map the space.</span></span>

### <span data-ttu-id="8c922-144">Пройдите по основным зонам несколько раз</span><span class="sxs-lookup"><span data-stu-id="8c922-144">Cover key areas multiple times</span></span>

<span data-ttu-id="8c922-145">Многократный проход по зоне поможет охватить объекты, которые могли быть пропущены при первом проходе.</span><span class="sxs-lookup"><span data-stu-id="8c922-145">Moving through an area multiple times will help pick up features you may have missed on the first walkthrough.</span></span> <span data-ttu-id="8c922-146">Для создания идеальной карты рекомендуется пройти через зону 2–3раза.</span><span class="sxs-lookup"><span data-stu-id="8c922-146">To build an ideal map, try traversing an area two to three times.</span></span>

<span data-ttu-id="8c922-147">По возможности, пройдя в одном направлении, развернитесь и пройдите в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="8c922-147">If possible, while repeating these movements, spend time walking through an area in one direction, then turn around and walk back the way you came.</span></span>

### <span data-ttu-id="8c922-148">Выполняйте сопоставление зоны не спеша</span><span class="sxs-lookup"><span data-stu-id="8c922-148">Take your time mapping the area</span></span>

<span data-ttu-id="8c922-149">Для создания полной карты и ориентации в пространстве устройству HoloLens требуется от 15 до 20минут.</span><span class="sxs-lookup"><span data-stu-id="8c922-149">It can take between 15 and 20 minutes for the HoloLens to fully map and adjust itself to its surroundings.</span></span> <span data-ttu-id="8c922-150">Если вы планируете часто использовать HoloLens в какой-то определенной зоне, уделите достаточно времени созданию карты этого пространства, чтобы избежать проблем в будущем.</span><span class="sxs-lookup"><span data-stu-id="8c922-150">If you have a space in which you plan to use a HoloLens frequently, taking that time up front to map the space can prevent issues later on.</span></span>  

## <span data-ttu-id="8c922-151">Возможные ошибки в пространственной карте</span><span class="sxs-lookup"><span data-stu-id="8c922-151">Possible errors in the spatial map</span></span>

<span data-ttu-id="8c922-152">Ошибки пространственного сопоставления могут быть нескольких категорий:</span><span class="sxs-lookup"><span data-stu-id="8c922-152">Errors in spatial mapping data fall into a few categories:</span></span>

- <span data-ttu-id="8c922-153">*Дыры*— реально существующие поверхности, которые отсутствуют на пространственной карте.</span><span class="sxs-lookup"><span data-stu-id="8c922-153">*Holes*: Real-world surfaces are missing from the spatial mapping data.</span></span>
- <span data-ttu-id="8c922-154">*Галлюцинации*— поверхности на пространственной карте, которые не существуют в реальности.</span><span class="sxs-lookup"><span data-stu-id="8c922-154">*Hallucinations*: Surfaces exist in the spatial mapping data that do not exist in the real world.</span></span>
- <span data-ttu-id="8c922-155">*Кротовые норы*— HoloLens "теряет" часть пространственной карты, ошибочно принимая ее за какую-то другую часть карты.</span><span class="sxs-lookup"><span data-stu-id="8c922-155">*Wormholes*: HoloLens 'loses' part of the spatial map by thinking it is in a different part of the map than it actually is.</span></span>
- <span data-ttu-id="8c922-156">*Смещения*— поверхности на пространственной карте не совпадают в точности с реальными поверхностями (вдавленные или выступающие поверхности).</span><span class="sxs-lookup"><span data-stu-id="8c922-156">*Bias*: Surfaces in the spatial mapping data are imperfectly aligned with real-world surfaces, either pushed in or pulled out.</span></span>

<span data-ttu-id="8c922-157">Если вы заметили подобные ошибки, сообщите об этом через [FeedbackHub](hololens-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="8c922-157">If you see any of these errors please use the [FeedbackHub](hololens-feedback.md) to send feedback.</span></span>

## <span data-ttu-id="8c922-158">Безопасность и хранение пространственных данных</span><span class="sxs-lookup"><span data-stu-id="8c922-158">Security and storage for spatial data</span></span>

<span data-ttu-id="8c922-159">Начиная с Windows 10 версии 1803 данные сопоставлений Microsoft HoloLens хранятся в локальной базе данных (на устройстве).</span><span class="sxs-lookup"><span data-stu-id="8c922-159">Windows 10 version 1803 update for Microsoft HoloLens and later stores mapping data in a local (on-device) database.</span></span>

<span data-ttu-id="8c922-160">Пользователь HoloLens не может напрямую получить доступ к базе данных карт, даже когда устройство подключено к ПК или при использовании приложения Проводника.</span><span class="sxs-lookup"><span data-stu-id="8c922-160">HoloLens users cannot directly access the map database, even when the device is plugged into a PC or when using the File Explorer app.</span></span> <span data-ttu-id="8c922-161">Если на устройстве HoloLens включено шифрование BitLocker, хранимые данные карт также шифруются вместе со всем томом.</span><span class="sxs-lookup"><span data-stu-id="8c922-161">When BitLocker is enabled on HoloLens, the stored map data is also encrypted along with the entire volume.</span></span>

### <span data-ttu-id="8c922-162">Удаление из HoloLens данных карт и известных пространств</span><span class="sxs-lookup"><span data-stu-id="8c922-162">Remove map data and known spaces from HoloLens</span></span>

<span data-ttu-id="8c922-163">Данные карт из раздела **Настройки > Система > Голограммы** можно удалить двумя способами:</span><span class="sxs-lookup"><span data-stu-id="8c922-163">There are two options for deleting map data in **Settings > System > Holograms**:</span></span>

- <span data-ttu-id="8c922-164">Чтобы удалить близлежащие голограммы, выберите **Удалить голограммы рядом**.</span><span class="sxs-lookup"><span data-stu-id="8c922-164">To delete nearby holograms, select **Remove nearby holograms**.</span></span> <span data-ttu-id="8c922-165">Эта команда удаляет данные карты и закрепленные голограммы для текущего пространства.</span><span class="sxs-lookup"><span data-stu-id="8c922-165">This command clears the map data and anchored holograms for the current space.</span></span> <span data-ttu-id="8c922-166">Если вы продолжите использовать устройство в том же самом пространстве, будет создан новый раздел карты для замены удаленной информации.</span><span class="sxs-lookup"><span data-stu-id="8c922-166">If you continue to use the device in the same space, it creates and stores a brand new map section to replace the deleted information.</span></span>

   > [!NOTE]
   > <span data-ttu-id="8c922-167">"Близлежащие" голограммы— это голограммы, связанные с одним разделом карты в текущем пространстве.</span><span class="sxs-lookup"><span data-stu-id="8c922-167">"Nearby" holograms are holograms that are anchored within the same map section in the current space.</span></span>

   <span data-ttu-id="8c922-168">Например, с помощью этой команды можно удалить данные рабочих карт, сохранив при этом данные домашних карт.</span><span class="sxs-lookup"><span data-stu-id="8c922-168">For example, you can use this option to clear work-related map data without affecting any home-related map data.</span></span>

- <span data-ttu-id="8c922-169">Чтобы удалить все голограммы, выберите **Удалить все голограммы**.</span><span class="sxs-lookup"><span data-stu-id="8c922-169">To delete all holograms, select **Remove all holograms**.</span></span> <span data-ttu-id="8c922-170">Эта команда удаляет все данные карт, которые хранятся на устройстве, а также все связанные с ними голограммы.</span><span class="sxs-lookup"><span data-stu-id="8c922-170">This command clears all map data that is stored on the device as well as all anchored holograms.</span></span> <span data-ttu-id="8c922-171">После этого вам необходимо будет заново поместить все голограммы,</span><span class="sxs-lookup"><span data-stu-id="8c922-171">You will need to explicitly place any holograms.</span></span> <span data-ttu-id="8c922-172">так как восстановить ранее помещенные голограммы будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="8c922-172">You will not be able to rediscover the previously-placed holograms.</span></span>

> [!NOTE]
> <span data-ttu-id="8c922-173">В любом случае после удаления голограмм HoloLens моментально начнет сканирование и создание карты текущего пространства.</span><span class="sxs-lookup"><span data-stu-id="8c922-173">After you remove nearby or all holograms, HoloLens immediately starts scanning and mapping the current space.</span></span>

### <span data-ttu-id="8c922-174">Данные Wi-Fi в пространственных картах</span><span class="sxs-lookup"><span data-stu-id="8c922-174">Wi-Fi data in spatial maps</span></span>

<span data-ttu-id="8c922-175">HoloLens хранит характеристики Wi-Fi для соотнесения мест расположения голограмм с разделами карт, хранящихся в базе данных известных пространств.</span><span class="sxs-lookup"><span data-stu-id="8c922-175">HoloLens stores Wi-Fi characteristics to help correlate hologram locations and map sections that are stored within the HoloLens database of known spaces.</span></span> <span data-ttu-id="8c922-176">Характеристики Wi-Fi недоступны пользователям и не отправляются в Майкрософт с использованием облака или службы телеметрии.</span><span class="sxs-lookup"><span data-stu-id="8c922-176">Information about Wi-Fi characteristics is not accessible to users, and not sent to Microsoft using the cloud or using telemetry.</span></span>

<span data-ttu-id="8c922-177">Когда Wi-Fi включен, HoloLens соотносит данные карт с близлежащими точками доступа Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="8c922-177">As long as Wi-Fi is enabled, HoloLens correlates map data with nearby Wi-Fi access points.</span></span> <span data-ttu-id="8c922-178">Поведение устройства не зависит от того, подключено ли оно к сети или сеть только обнаружена, </span><span class="sxs-lookup"><span data-stu-id="8c922-178">There is no difference in behavior whether a network is connected or just detected nearby.</span></span> <span data-ttu-id="8c922-179">Когда Wi-Fi отключен, HoloLens так же выполняет поиск по пространству.</span><span class="sxs-lookup"><span data-stu-id="8c922-179">If Wi-Fi is disabled, HoloLens still searches the space.</span></span> <span data-ttu-id="8c922-180">Однако устройству при этом приходится обрабатывать больший объем данных карт в базе данных пространств, в результате чего нахождение голограмм может занимать больше времени.</span><span class="sxs-lookup"><span data-stu-id="8c922-180">However, HoloLens has to search more of the map data within the spaces database, and may need more time to find holograms.</span></span> <span data-ttu-id="8c922-181">Если данные Wi-Fi недоступны, для нахождения правильной части карты устройству HoloLens требуется сравнивать результаты текущего сканирования со всеми привязками голограмм и разделами карт, которые хранятся на устройстве.</span><span class="sxs-lookup"><span data-stu-id="8c922-181">Without the Wi-Fi info, the HoloLens has to compare active scans to all hologram anchors and map sections that are stored on the device in order to locate the correct portion of the map.</span></span>

## <span data-ttu-id="8c922-182">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8c922-182">Related topics</span></span>

- [<span data-ttu-id="8c922-183">Пространственное сопоставление</span><span class="sxs-lookup"><span data-stu-id="8c922-183">Spatial mapping design</span></span>](https://docs.microsoft.com/windows/mixed-reality/spatial-mapping)
