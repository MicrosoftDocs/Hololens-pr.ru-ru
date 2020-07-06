---
title: Использование средства 3D-просмотра в HoloLens (1- го поколения)
description: В этой статье описаны типы файлов и функции, поддерживаемые средством 3D-просмотра в HoloLens (1-го поколения), а также порядок использования приложения и устранения неполадок в его работе.
ms.prod: hololens
ms.sitesec: library
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.localizationpriority: high
ms.date: 10/30/2019
ms.reviewer: scooley
audience: ITPro
manager: jarrettr
appliesto:
- HoloLens (1st gen)
ms.openlocfilehash: 47fe1fd5dc164c56ce22a09d7edf5bffdb60ea14
ms.sourcegitcommit: 7c057aeeaeebb4daffa2120491d4e897a31e8d0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10828887"
---
# <span data-ttu-id="f8e4e-103">Использование средства 3D-просмотра в HoloLens (1- го поколения)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-103">Using 3D Viewer on HoloLens (1st gen)</span></span>

<span data-ttu-id="f8e4e-104">Средство 3D-просмотра позволяет просматривать трехмерные модели в HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-104">3D Viewer lets you view 3D models on HoloLens (1st gen).</span></span> <span data-ttu-id="f8e4e-105">Открывать и просматривать *поддерживаемые* файлы .fbx можно помощью Microsoft Edge, OneDrive и других приложений.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-105">You can open and view *supported* .fbx files from Microsoft Edge, OneDrive, and other apps.</span></span>

>[!NOTE]
><span data-ttu-id="f8e4e-106">Эта статья относится к приложению **Средство 3D-просмотра** иммерсивной среды Unity, поддерживающему файлы .fbx и доступному только в HoloLens (1-го поколения).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-106">This article applies to the immersive Unity **3D Viewer** app, which supports .fbx files and is only available on HoloLens (1st gen).</span></span> <span data-ttu-id="f8e4e-107">Предустановленное приложение **Средство 3D-просмотра** в HoloLens 2 поддерживает открытие пользовательских трехмерных моделей .glb в помещениях с дополненной реальностью (дополнительные сведения см. в [Обзор требований к объекту](https://docs.microsoft.com/windows/mixed-reality/creating-3d-models-for-use-in-the-windows-mixed-reality-home#asset-requirements-overview)).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-107">The pre-installed **3D Viewer** app on HoloLens 2 supports opening custom .glb 3D models in the mixed reality home (see [Asset requirements overview](https://docs.microsoft.com/windows/mixed-reality/creating-3d-models-for-use-in-the-windows-mixed-reality-home#asset-requirements-overview) for more details.</span></span>

<span data-ttu-id="f8e4e-108">Если вам не удается открыть трехмерную модель в средстве 3D-просмотра или некоторые функции трехмерной модели не поддерживаются, см. [Характеристики поддерживаемого содержимого](#supported-content-specifications).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-108">If you're having trouble opening a 3D model in 3D Viewer, or certain features of your 3D model are unsupported, see [Supported content specifications](#supported-content-specifications).</span></span>

<span data-ttu-id="f8e4e-109">Сведения о создании и оптимизации трехмерных моделей для использования со средством 3D-просмотра см. в статье [Оптимизация трехмерных моделей для средства 3D-просмотра](#optimizing-3d-models-for-3d-viewer).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-109">To build or optimize 3D models for use with 3D Viewer, see [Optimizing 3D models for 3D Viewer](#optimizing-3d-models-for-3d-viewer).</span></span>

<span data-ttu-id="f8e4e-110">Трехмерную модель можно открыть в HoloLens двумя способами.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-110">There are two ways to open a 3D model on HoloLens.</span></span> <span data-ttu-id="f8e4e-111">Дополнительные сведения см. в статье [Просмотр файлов FBX в HoloLens](#viewing-fbx-files-on-hololens).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-111">See [Viewing FBX files on HoloLens](#viewing-fbx-files-on-hololens) to learn more.</span></span>

<span data-ttu-id="f8e4e-112">Если у вас возникли проблемы после чтения этих разделов, см. раздел [Поиск и устранение неисправностей](#troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-112">If you're having trouble after reading these topics, see [Troubleshooting](#troubleshooting).</span></span>

## <span data-ttu-id="f8e4e-113">Характеристики поддерживаемого содержимого</span><span class="sxs-lookup"><span data-stu-id="f8e4e-113">Supported content specifications</span></span>

### <span data-ttu-id="f8e4e-114">Формат файла</span><span class="sxs-lookup"><span data-stu-id="f8e4e-114">File format</span></span>

- <span data-ttu-id="f8e4e-115">Формат FBX</span><span class="sxs-lookup"><span data-stu-id="f8e4e-115">FBX format</span></span>
- <span data-ttu-id="f8e4e-116">Максимальный выпуск FBX — 2015.1.0</span><span class="sxs-lookup"><span data-stu-id="f8e4e-116">Maximum FBX release 2015.1.0</span></span>

### <span data-ttu-id="f8e4e-117">Размер файла</span><span class="sxs-lookup"><span data-stu-id="f8e4e-117">File size</span></span>

- <span data-ttu-id="f8e4e-118">Мин. 5КБ</span><span class="sxs-lookup"><span data-stu-id="f8e4e-118">Minimum 5 KB</span></span>
- <span data-ttu-id="f8e4e-119">Макс. 500 МБ</span><span class="sxs-lookup"><span data-stu-id="f8e4e-119">Maximum 500 MB</span></span>

### <span data-ttu-id="f8e4e-120">Геометрическая фигура</span><span class="sxs-lookup"><span data-stu-id="f8e4e-120">Geometry</span></span>

- <span data-ttu-id="f8e4e-121">Только модели с многоугольниками.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-121">Polygonal models only.</span></span> <span data-ttu-id="f8e4e-122">Дробление поверхности или NURBs отсутствуют</span><span class="sxs-lookup"><span data-stu-id="f8e4e-122">No subdivision surfaces or NURBs</span></span>
- <span data-ttu-id="f8e4e-123">Правосторонняя система координат</span><span class="sxs-lookup"><span data-stu-id="f8e4e-123">Right-handed coordinate system</span></span>
- <span data-ttu-id="f8e4e-124">Наклон в матрицах преобразования не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f8e4e-124">Shear in transformation matrices is not supported</span></span>

### <span data-ttu-id="f8e4e-125">Текстуры</span><span class="sxs-lookup"><span data-stu-id="f8e4e-125">Textures</span></span>

- <span data-ttu-id="f8e4e-126">Текстурные карты должны быть внедрены в файл FBX</span><span class="sxs-lookup"><span data-stu-id="f8e4e-126">Texture maps must be embedded in the FBX file</span></span>
- <span data-ttu-id="f8e4e-127">Поддерживаемые форматы изображений</span><span class="sxs-lookup"><span data-stu-id="f8e4e-127">Supported image formats</span></span>
  - <span data-ttu-id="f8e4e-128">Изображения в формате JPEG и PNG</span><span class="sxs-lookup"><span data-stu-id="f8e4e-128">JPEG and PNG images</span></span>
  - <span data-ttu-id="f8e4e-129">Изображения BMP (24-битный цвет RGB, естественный цвет)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-129">BMP images (24-bit RGB true-color)</span></span>
  - <span data-ttu-id="f8e4e-130">Изображения TGA (24-битный цвет RGB и 32-битный цвет RGBY, естественный цвет)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-130">TGA images (24-bit RGB and 32-bit RGBQ true-color)</span></span>
- <span data-ttu-id="f8e4e-131">Максимальное разрешение текстур 2048x2048</span><span class="sxs-lookup"><span data-stu-id="f8e4e-131">Maximum texture resolution of 2048x2048</span></span>
- <span data-ttu-id="f8e4e-132">Макс. одна диффузная карта, одна карта нормалей и одна кубическая карта отражения для одной сетки</span><span class="sxs-lookup"><span data-stu-id="f8e4e-132">Maximum of one diffuse map, one normal map, and one reflection cube map per mesh</span></span>
- <span data-ttu-id="f8e4e-133">При значении ниже 50% альфа-канал в диффузных текстурах способствует исключению пикселей</span><span class="sxs-lookup"><span data-stu-id="f8e4e-133">Alpha channel in diffuse textures causes pixels to be discarded if below 50%</span></span>

### <span data-ttu-id="f8e4e-134">Анимация</span><span class="sxs-lookup"><span data-stu-id="f8e4e-134">Animation</span></span>

- <span data-ttu-id="f8e4e-135">Анимация масштабирования, поворота и преобразования для отдельных объектов</span><span class="sxs-lookup"><span data-stu-id="f8e4e-135">Scale/rotation/translation animation on individual objects</span></span>
- <span data-ttu-id="f8e4e-136">Скелетная (подстроенная) анимация со скиннингом</span><span class="sxs-lookup"><span data-stu-id="f8e4e-136">Skeletal (rigged) animation with skinning</span></span>
  - <span data-ttu-id="f8e4e-137">Макс. 4 фактора влияния на одну вершину</span><span class="sxs-lookup"><span data-stu-id="f8e4e-137">Maximum of 4 influences per vertex</span></span>

### <span data-ttu-id="f8e4e-138">Материалы</span><span class="sxs-lookup"><span data-stu-id="f8e4e-138">Materials</span></span>

- <span data-ttu-id="f8e4e-139">Поддерживаются материалы для модели Ламберта (Lambert) и Фонга (Phong) с настраиваемыми параметрами</span><span class="sxs-lookup"><span data-stu-id="f8e4e-139">Lambert and Phong materials are supported, with adjustable parameters</span></span>
- <span data-ttu-id="f8e4e-140">Поддерживаемые свойства материалов для модели Ламберта</span><span class="sxs-lookup"><span data-stu-id="f8e4e-140">Supported material properties for Lambert</span></span>
  - <span data-ttu-id="f8e4e-141">Главная текстура (тест RGB + альфа)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-141">Main Texture (RGB + Alpha Test)</span></span>
  - <span data-ttu-id="f8e4e-142">Рассеянный цвет (RGB)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-142">Diffuse Color (RGB)</span></span>
  - <span data-ttu-id="f8e4e-143">Внешний цвет (RGB)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-143">Ambient Color (RGB)</span></span>
- <span data-ttu-id="f8e4e-144">Поддерживаемые свойства материалов для модели Фонга</span><span class="sxs-lookup"><span data-stu-id="f8e4e-144">Supported material properties for Phong</span></span>
  - <span data-ttu-id="f8e4e-145">Главная текстура (тест RGB + альфа)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-145">Main Texture (RGB + Alpha Test)</span></span>
  - <span data-ttu-id="f8e4e-146">Рассеянный цвет (RGB)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-146">Diffuse Color (RGB)</span></span>
  - <span data-ttu-id="f8e4e-147">Внешний цвет (RGB)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-147">Ambient Color (RGB)</span></span>
  - <span data-ttu-id="f8e4e-148">Отраженный цвет (RGB)</span><span class="sxs-lookup"><span data-stu-id="f8e4e-148">Specular Color (RGB)</span></span>
  - <span data-ttu-id="f8e4e-149">Блеск</span><span class="sxs-lookup"><span data-stu-id="f8e4e-149">Shininess</span></span>
  - <span data-ttu-id="f8e4e-150">Отражающая способность</span><span class="sxs-lookup"><span data-stu-id="f8e4e-150">Reflectivity</span></span>
- <span data-ttu-id="f8e4e-151">Пользовательские материалы не поддерживаются</span><span class="sxs-lookup"><span data-stu-id="f8e4e-151">Custom materials are not supported</span></span>
- <span data-ttu-id="f8e4e-152">Не более одного материала на сетку</span><span class="sxs-lookup"><span data-stu-id="f8e4e-152">Maximum of one material per mesh</span></span>
- <span data-ttu-id="f8e4e-153">Не более одного материала на уровень</span><span class="sxs-lookup"><span data-stu-id="f8e4e-153">Maximum of one material layer</span></span>
- <span data-ttu-id="f8e4e-154">Не более 8 материалов на файл</span><span class="sxs-lookup"><span data-stu-id="f8e4e-154">Maximum of 8 materials per file</span></span>

### <span data-ttu-id="f8e4e-155">Ограничения для файла и модели</span><span class="sxs-lookup"><span data-stu-id="f8e4e-155">File and model limitations</span></span>

<span data-ttu-id="f8e4e-156">Существуют жесткие ограничения относительно размера файлов, количества моделей, вершин и сеток, доступных для одновременного открытия в средстве 3D-просмотра:</span><span class="sxs-lookup"><span data-stu-id="f8e4e-156">There are hard limits on the size of files, as well as the number of models, vertices, and meshes that can be open simultaneously in 3D Viewer:</span></span>

- <span data-ttu-id="f8e4e-157">максимальный размер файла на модель: 500 МБ;</span><span class="sxs-lookup"><span data-stu-id="f8e4e-157">500 MB maximum file size per model</span></span>
- <span data-ttu-id="f8e4e-158">вершины: в общей сложности 600 000 во всех открытых моделях;</span><span class="sxs-lookup"><span data-stu-id="f8e4e-158">Vertices: 600,000 combined on all open models</span></span>
- <span data-ttu-id="f8e4e-159">сетки: в общей сложности 1600 во всех открытых моделях;</span><span class="sxs-lookup"><span data-stu-id="f8e4e-159">Meshes: 1,600 combined on all open models</span></span>
- <span data-ttu-id="f8e4e-160">макс. 40 одновременно открытых моделей.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-160">Maximum of 40 models open at one time</span></span>

## <span data-ttu-id="f8e4e-161">Оптимизация трехмерных моделей для средства 3D-просмотра</span><span class="sxs-lookup"><span data-stu-id="f8e4e-161">Optimizing 3D models for 3D Viewer</span></span>

### <span data-ttu-id="f8e4e-162">Особые примечания</span><span class="sxs-lookup"><span data-stu-id="f8e4e-162">Special considerations</span></span>

- <span data-ttu-id="f8e4e-163">Избегайте использования черных материалов или черных областей в текстурных картах.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-163">Avoid black materials or black areas in texture maps.</span></span> <span data-ttu-id="f8e4e-164">Голограммы состоят из света, следовательно, HoloLens отображает черный цвет (отсутствие света) в качестве прозрачного.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-164">Holograms are made of light, thus HoloLens renders black (the absence of light) as transparent.</span></span>
- <span data-ttu-id="f8e4e-165">Перед выполнением экспорта из средства создания в файл FBX убедитесь, что все геометрические фигуры отображаются и не заблокированы, а также в том, что слои, содержащие геометрическую фигуру, не отключены и не являются шаблонными.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-165">Before exporting to FBX from your creation tool, ensure all geometry is visible and unlocked and no layers that contain geometry are turned off or templated.</span></span> <span data-ttu-id="f8e4e-166">Видимость не учитывается.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-166">Visibility is not respected.</span></span>
- <span data-ttu-id="f8e4e-167">Не допускайте больших смещений при преобразовании между узлами (например, 100 000 единиц).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-167">Avoid very large translation offsets between nodes (for example, 100,000 units).</span></span> <span data-ttu-id="f8e4e-168">Это приведет к искажению модели при перемещении, масштабировании или повороте.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-168">This can cause the model to jitter while being moved/scaled/rotated.</span></span>

### <span data-ttu-id="f8e4e-169">Оптимизация производительности</span><span class="sxs-lookup"><span data-stu-id="f8e4e-169">Performance optimization</span></span>

<span data-ttu-id="f8e4e-170">Для получения оптимальных результатов в процессе создания и настройки содержимого учитывайте производительность, а также выполняйте проверку в приложении средства 3D-просмотра в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-170">Keep performance in mind while authoring content and validate in the 3D Viewer app on HoloLens during the authoring process for best results.</span></span> <span data-ttu-id="f8e4e-171">Средство 3D-просмотра отображает содержимое в режиме реального времени, а производительность зависит от возможностей аппаратного обеспечения HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-171">3D Viewer renders content real-time and performance is subject to HoloLens hardware capabilities.</span></span>  

<span data-ttu-id="f8e4e-172">В 3D-модели есть множество переменных, которые влияют на производительность.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-172">There are many variables in a 3D model that can impact performance.</span></span> <span data-ttu-id="f8e4e-173">При наличии более 150 000 вершин или более 400 сеток во время загрузки средства 3D-просмотра отобразится сообщение с предупреждением. </span><span class="sxs-lookup"><span data-stu-id="f8e4e-173">3D Viewer will show a warning on load if there are more than 150,000 vertices or more than 400 meshes.</span></span> <span data-ttu-id="f8e4e-174">Анимации могут повлиять на производительность других открытых моделей.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-174">Animations can have an impact on the performance of other open models.</span></span> <span data-ttu-id="f8e4e-175">Кроме того, существуют жесткие ограничения относительно общего количества моделей, вершин и сеток, доступных для одновременного открытия в средстве 3D-просмотра (см. [Ограничения для файла и модели](#file-and-model-limitations)).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-175">There are also hard limits on the total number models, vertices, and meshes that can be open simultaneously in 3D Viewer (see [File and model limitations](#file-and-model-limitations)).</span></span>  

<span data-ttu-id="f8e4e-176">Если сложность трехмерной модели сказывается на ее работе, постарайтесь:</span><span class="sxs-lookup"><span data-stu-id="f8e4e-176">If the 3D model isn't running well due to model complexity, consider:</span></span>

- <span data-ttu-id="f8e4e-177">сократить количество многоугольников;</span><span class="sxs-lookup"><span data-stu-id="f8e4e-177">Reducing polygon count</span></span>
- <span data-ttu-id="f8e4e-178">уменьшить количество костей в подстроенной анимации;</span><span class="sxs-lookup"><span data-stu-id="f8e4e-178">Reducing number of bones in rigged animation</span></span>
- <span data-ttu-id="f8e4e-179">предотвратить самозагораживание экрана.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-179">Avoiding self-occlusion</span></span>

<span data-ttu-id="f8e4e-180">Средство 3D-просмотра поддерживает функцию двусторонней визуализации, но она по умолчанию отключена для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-180">Double-sided rendering is supported in 3D Viewer, although it is turned off by default for performance reasons.</span></span> <span data-ttu-id="f8e4e-181">Чтобы включить ее, нажмите кнопку **Двусторонняя** на странице **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-181">This can be turned on via the **Double Sided** button on the **Details** page.</span></span> <span data-ttu-id="f8e4e-182">Для обеспечения оптимальной производительности старайтесь не использовать двустороннюю визуализацию в содержимом.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-182">For best performance, avoid the need for double-sided rendering in your content.</span></span>

### <span data-ttu-id="f8e4e-183">Проверка трехмерной модели</span><span class="sxs-lookup"><span data-stu-id="f8e4e-183">Validating your 3D model</span></span>

<span data-ttu-id="f8e4e-184">Проверьте модель, открыв ее в средстве 3D-просмотра в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-184">Validate your model by opening it in 3D Viewer on HoloLens.</span></span> <span data-ttu-id="f8e4e-185">Нажмите кнопку **Сведения**, чтобы просмотреть характеристики модели и предупреждения о неподдерживаемом содержимом (при наличии).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-185">Select the **Details** button to view your model's characteristics and warnings of unsupported content (if present).</span></span>

### <span data-ttu-id="f8e4e-186">Отображение трехмерных моделей с фактическими размерами</span><span class="sxs-lookup"><span data-stu-id="f8e4e-186">Rendering 3D models with true-to-life dimensions</span></span>

<span data-ttu-id="f8e4e-187">По умолчанию средство 3D-просмотра отображает трехмерные модели так, чтобы их размеры и расположение были удобны для восприятия пользователем.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-187">By default, 3D Viewer displays 3D models at a comfortable size and position relative to the user.</span></span> <span data-ttu-id="f8e4e-188">Если необходимо отобразить трехмерную модель с фактическими размерами (например, при рассмотрении моделей мебели в помещении), разработчик содержимого может установить флажок в метаданных файла, чтобы предотвратить изменение размера модели приложением и пользователем.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-188">However, if rendering a 3D model with true-to-life measurements is important (for example, when evaluating furniture models in a room), the content creator can set a flag within the file's metadata to prevent resizing of that model by both the application and the user.</span></span>

<span data-ttu-id="f8e4e-189">Чтобы предотвратить масштабирование модели, добавьте логический настраиваемый атрибут в любой объект сцены с именем Microsoft_DisableScale и задайте для него значение "истина".</span><span class="sxs-lookup"><span data-stu-id="f8e4e-189">To prevent scaling of the model, add a Boolean custom attribute to any object in the scene named Microsoft_DisableScale and set it to true.</span></span> <span data-ttu-id="f8e4e-190">Далее средство 3D-просмотра будет учитывать информацию FbxSystemUnit, имеющуюся в файле FBX.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-190">3D Viewer will then respect the FbxSystemUnit information baked into the FBX file.</span></span> <span data-ttu-id="f8e4e-191">Шкала в средстве 3D-просмотра: 1 метр на единицу FBX.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-191">Scale in 3D Viewer is 1 meter per FBX unit.</span></span>

## <span data-ttu-id="f8e4e-192">Просмотр файлов FBX в HoloLens</span><span class="sxs-lookup"><span data-stu-id="f8e4e-192">Viewing FBX files on HoloLens</span></span>

### <span data-ttu-id="f8e4e-193">Открытие файла FBX с помощью Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f8e4e-193">Open an FBX file from Microsoft Edge</span></span>

<span data-ttu-id="f8e4e-194">Microsoft Edge в HoloLens позволяет открывать файлы FBX непосредственно с помощью веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-194">FBX files can be opened directly from a website using Microsoft Edge on HoloLens.</span></span>

1. <span data-ttu-id="f8e4e-195">В Microsoft Edge откройте веб-страницу с файлом FBX, который необходимо просмотреть.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-195">In Microsoft Edge, navigate to the webpage containing the FBX file you want to view.</span></span>
1. <span data-ttu-id="f8e4e-196">Выберите файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-196">Select the file to download it.</span></span>
1. <span data-ttu-id="f8e4e-197">После завершения загрузки нажмите кнопку **Открыть** в Microsoft Edge, чтобы открыть файл в средстве 3D-просмотра.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-197">When the download is complete, select the **Open** button in Microsoft Edge to open the file in 3D Viewer.</span></span>

<span data-ttu-id="f8e4e-198">Скачанный файл доступен и может быть повторно открыт с помощью папки "Загрузки" в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-198">The downloaded file can be accessed and opened again later by using Downloads in Microsoft Edge.</span></span> <span data-ttu-id="f8e4e-199">Чтобы сохранить трехмерную модель и обеспечить непрерывный доступ, загрузите файл на ПК и сохраните его в своей учетной записи OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-199">To save a 3D model and ensure continued access, download the file on your PC and save it to your OneDrive account.</span></span> <span data-ttu-id="f8e4e-200">Далее можно открыть файл в приложении OneDrive в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-200">The file can then be opened from the OneDrive app on HoloLens.</span></span>

> [!NOTE]
> <span data-ttu-id="f8e4e-201">Некоторые веб-сайты с доступными для загрузки моделями FBX предоставляют их в сжатом виде в формате ZIP.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-201">Some websites with downloadable FBX models provide them in compressed ZIP format.</span></span> <span data-ttu-id="f8e4e-202">Средство 3D-просмотра не поддерживает непосредственное открытие ZIP-файлов.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-202">3D Viewer cannot open ZIP files directly.</span></span> <span data-ttu-id="f8e4e-203">Извлеките файл FBX с помощью ПК и сохраните его в учетной записи OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-203">Instead, use your PC to extract the FBX file and save it to your OneDrive account.</span></span> <span data-ttu-id="f8e4e-204">Далее можно открыть файл в приложении OneDrive в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-204">The file can then be opened from the OneDrive app on HoloLens.</span></span>

### <span data-ttu-id="f8e4e-205">Открытие файла FBX с помощью OneDrive</span><span class="sxs-lookup"><span data-stu-id="f8e4e-205">Open an FBX file from OneDrive</span></span>

<span data-ttu-id="f8e4e-206">Приложение OneDrive в HoloLens позволяет открывать файлы FBX непосредственно с помощью OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-206">FBX files can be opened from OneDrive by using the OneDrive app on HoloLens.</span></span> <span data-ttu-id="f8e4e-207">Убедитесь, что установка OneDrive в HoloLens выполнена с помощью приложения Microsoft Store и файл FBX загружен в OneDrive на ПК.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-207">Be sure you've installed OneDrive using Microsoft Store app on HoloLens and that you've already uploaded the FBX file to OneDrive on your PC.</span></span>

<span data-ttu-id="f8e4e-208">Загруженные в OneDrive файлы FBX можно открыть в HoloLens с помощью средства 3D-просмотра двумя способами.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-208">Once in OneDrive, FBX files can be opened on HoloLens using 3D Viewer in one of two ways:</span></span>

- <span data-ttu-id="f8e4e-209">Запустите OneDrive в HoloLens и выберите файл FBX, который необходимо открыть в средстве 3D-просмотра.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-209">Launch OneDrive on HoloLens and select the FBX file to open it in 3D Viewer.</span></span>
- <span data-ttu-id="f8e4e-210">Запустите средство 3D-просмотра, коснитесь для отображения панели инструментов, затем выберите **Открыть файл**.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-210">Launch 3D Viewer, air tap to show the toolbar, and select **Open File**.</span></span> <span data-ttu-id="f8e4e-211">Запустится OneDrive, что позволит выбрать файл FBX.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-211">OneDrive will launch, allowing you to select an FBX file.</span></span>

## <span data-ttu-id="f8e4e-212">Поиск и устранение неисправностей</span><span class="sxs-lookup"><span data-stu-id="f8e4e-212">Troubleshooting</span></span>

### <span data-ttu-id="f8e4e-213">При открытии трехмерной модели отображается сообщение с предупреждением</span><span class="sxs-lookup"><span data-stu-id="f8e4e-213">I see a warning when I open a 3D model</span></span>

<span data-ttu-id="f8e4e-214">Если выполняется открытие трехмерной модели с функциями, неподдерживаемыми средством 3D-просмотра, а также если чрезмерная сложность модели может повлиять на производительность, отобразится сообщение с предупреждением.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-214">You will see a warning if you attempt to open a 3D model that contains features that are not supported by 3D Viewer, or if the model is too complex and performance may be affected.</span></span> <span data-ttu-id="f8e4e-215">Средство 3D-просмотра загрузит трехмерную модель, но производительность и качество графического изображения будут снижены.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-215">3D Viewer will still load the 3D model, but performance or visual fidelity may be compromised.</span></span>

<span data-ttu-id="f8e4e-216">Дополнительные сведения см. в разделах [Характеристики поддерживаемого содержимого](#supported-content-specifications) и [Оптимизация трехмерных моделей для средства 3D-просмотра](#optimizing-3d-models-for-3d-viewer).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-216">For more info, see [Supported content specifications](#supported-content-specifications) and [Optimizing 3D models for 3D Viewer](#optimizing-3d-models-for-3d-viewer).</span></span>

### <span data-ttu-id="f8e4e-217">Отображается сообщение с предупреждением и трехмерная модель не загружается</span><span class="sxs-lookup"><span data-stu-id="f8e4e-217">I see a warning and the 3D model doesn't load</span></span>

<span data-ttu-id="f8e4e-218">Сообщение об ошибке отображается, если средству 3D-просмотра не удается загрузить трехмерную модель по причине ее сложности или размера файла, а также если файл FBX поврежден или является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-218">You will see an error message when 3D Viewer cannot load a 3D model due to complexity or file size, or if the FBX file is corrupt or invalid.</span></span> <span data-ttu-id="f8e4e-219">Сообщение об ошибке также отображается, если достигнут предел общего количества моделей, вершин или сеток, доступных для одновременного открытия.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-219">You will also see an error message if you have reached the limit on the total number of models, vertices, or meshes that can be open simultaneously.</span></span>  

<span data-ttu-id="f8e4e-220">Дополнительные сведения см. в разделах [Характеристики поддерживаемого содержимого](#supported-content-specifications) и [Ограничения для файла и модели](#file-and-model-limitations).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-220">For more info, see [Supported content specifications](#supported-content-specifications) and [File and model limitations](#file-and-model-limitations).</span></span>

<span data-ttu-id="f8e4e-221">Если вы считаете, что модель соответствует характеристикам поддерживаемого содержимого и ограничения для файла и модели не превышены, можно отправить файл FBX в службу поддержки средства 3D-просмотра по адресу: holoapps@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-221">If you feel your model meets the supported content specifications and has not exceeded the file or model limitations, you may send your FBX file to the 3D Viewer team at holoapps@microsoft.com.</span></span> <span data-ttu-id="f8e4e-222">Мы не оказываем персональную поддержку, но наличие примеров файлов, не загружаемых должным образом, поможет нашей команде усовершенствовать последующие версии приложения.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-222">We are not able to respond personally, but having examples of files that do not load properly will help our team improve on future versions of the app.</span></span>

### <span data-ttu-id="f8e4e-223">Трехмерная модель загружается, но не отображается должным образом</span><span class="sxs-lookup"><span data-stu-id="f8e4e-223">My 3D model loads, but does not appear as expected</span></span>

<span data-ttu-id="f8e4e-224">Если трехмерная модель не отображается в средстве 3D-просмотра должным образом, коснитесь для отображения панели инструментов, затем выберите **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-224">If your 3D model does not look as expected in 3D Viewer, air tap to show the toolbar, then select **Details**.</span></span> <span data-ttu-id="f8e4e-225">Будут выделены характеристики файла, не поддерживаемые средством 3D-просмотра.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-225">Aspects of the file which are not supported by 3D Viewer will be highlighted as warnings.</span></span>

<span data-ttu-id="f8e4e-226">Наиболее частой причиной является отсутствие текстур, вероятно, из-за того, что они не внедрены в файл FBX.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-226">The most common issue you might see is missing textures, likely because they are not embedded in the FBX file.</span></span> <span data-ttu-id="f8e4e-227">В этом случае модель будет отображаться белым.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-227">In this case, the model will appear white.</span></span> <span data-ttu-id="f8e4e-228">Данную проблему можно решить на этапе создания, выполнив экспорт из средства создания в файл FBX при включенном параметре внедрения текстур.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-228">This issue can be addressed in the creation process by exporting from your creation tool to FBX with the embed textures option selected.</span></span>

<span data-ttu-id="f8e4e-229">Дополнительные сведения см. в разделах [Характеристики поддерживаемого содержимого](#supported-content-specifications) и [Оптимизация трехмерных моделей для средства 3D-просмотра](#optimizing-3d-models-for-3d-viewer).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-229">For more info, see [Supported content specifications](#supported-content-specifications) and [Optimizing 3D models for 3D Viewer](#optimizing-3d-models-for-3d-viewer).</span></span>

### <span data-ttu-id="f8e4e-230">При просмотре трехмерной модели снижается производительность</span><span class="sxs-lookup"><span data-stu-id="f8e4e-230">I experience performance drops while viewing my 3D model</span></span>

<span data-ttu-id="f8e4e-231">Производительность при загрузке и просмотре трехмерной модели зависит от сложности модели, количества одновременно открытых моделей и количества моделей с активной анимацией.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-231">Performance when loading and viewing a 3D model can be affected by the complexity of the model, number of models open simultaneously, or number of models with active animations.</span></span>

<span data-ttu-id="f8e4e-232">Дополнительные сведения см. в статье [Оптимизация трехмерных моделей для средства 3D-просмотра](#optimizing-3d-models-for-3d-viewer) и [Ограничения для файла и модели](#file-and-model-limitations).</span><span class="sxs-lookup"><span data-stu-id="f8e4e-232">For more info, see [Optimizing 3D models for 3D Viewer](#optimizing-3d-models-for-3d-viewer) and [File and model limitations](#file-and-model-limitations).</span></span>

### <span data-ttu-id="f8e4e-233">При открытии файла FBX в HoloLens он не открывается в средстве 3D-просмотра</span><span class="sxs-lookup"><span data-stu-id="f8e4e-233">When I open an FBX file on HoloLens, it doesn't open in 3D Viewer</span></span>

<span data-ttu-id="f8e4e-234">При установке средства 3D-просмотра оно автоматически привязывается к расширению файла .fbx.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-234">3D Viewer is automatically associated with the .fbx file extension when it is installed.</span></span>

<span data-ttu-id="f8e4e-235">Если при открытии файла FBX отображается диалоговое окно, которое перенаправляет в Microsoft Store, в данный момент в HoloLens отсутствует приложение, привязанное к расширению файла .fbx.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-235">If you try to open an FBX file and see a dialog box that directs you to Microsoft Store, you do not currently have an app associated with the .fbx file extension on HoloLens.</span></span>

<span data-ttu-id="f8e4e-236">Убедись, что средство 3D-просмотра установлено.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-236">Verify that 3D Viewer is installed.</span></span> <span data-ttu-id="f8e4e-237">Если приложение не установлено, загрузите его из магазина Microsoft Store в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-237">If it is not installed, download it from Microsoft Store on HoloLens.</span></span>

<span data-ttu-id="f8e4e-238">Если средство 3D-просмотра установлено, запустите его, затем снова попытайтесь открыть файл.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-238">If 3D Viewer is already installed, launch 3D Viewer, then try opening the file again.</span></span> <span data-ttu-id="f8e4e-239">Если проблема не устранена, удалите и снова установите средство 3D-просмотра.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-239">If the issue persists, uninstall and reinstall 3D Viewer.</span></span> <span data-ttu-id="f8e4e-240">При этом расширение файла .fbx будет заново привязано к средству 3D-просмотра.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-240">This will re-associate the .fbx file extension with 3D Viewer.</span></span>

<span data-ttu-id="f8e4e-241">Если при попытке открыть файл FBX открывается приложение, не являющееся средством 3D-просмотра, вероятно, это приложение было установлено после установки средства 3D-просмотра и переняло привязку к расширению файла .fbx.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-241">If attempting to open an FBX file opens an app other than 3D Viewer, that app was likely installed after 3D Viewer and has taken over association with the .fbx file extension.</span></span> <span data-ttu-id="f8e4e-242">Если требуется привязка средства 3D-просмотра к расширению файла .fbx, удалите и снова установите средство 3D-просмотра.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-242">If you prefer 3D Viewer to be associated with the .fbx file extension, uninstall and reinstall 3D Viewer.</span></span>

### <span data-ttu-id="f8e4e-243">При нажатии кнопки открытия файла в средстве 3D-просмотра приложение не запускается</span><span class="sxs-lookup"><span data-stu-id="f8e4e-243">The Open File button in 3D Viewer doesn't launch an app</span></span>

<span data-ttu-id="f8e4e-244">При нажатии кнопки **Открыть файл** откроется приложение, связанное с функцией выбора файлов в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-244">The **Open File** button will open the app associated with the file picker function on HoloLens.</span></span> <span data-ttu-id="f8e4e-245">Если приложение OneDrive установлено, оно будет запускаться при нажатии кнопки **Открыть файл**.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-245">If OneDrive is installed, the **Open File** button should launch OneDrive.</span></span> <span data-ttu-id="f8e4e-246">Однако если в данный момент в HoloLens отсутствует приложение, связанное с функцией выбора файлов, будет выполняться перенаправление в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-246">However, if there is currently no app associated with the file picker function installed on HoloLens, you will be directed to Microsoft Store.</span></span>

<span data-ttu-id="f8e4e-247">Если при нажатии кнопки **Открыть файл** запускается приложение, не являющееся OneDrive, вероятно, это приложение было установлено после установки приложения OneDrive и переняло привязку к функции выбора файлов.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-247">If the **Open File** button launches an app other than OneDrive, that app was likely installed after OneDrive and has taken over association with the file picker function.</span></span> <span data-ttu-id="f8e4e-248">Если при нажатии кнопки **Открыть файл** в средстве 3D-просмотра требуется запускать приложение OneDrive, удалите и снова установите OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-248">If you prefer OneDrive to launch when selecting the **Open File** button in 3D Viewer, uninstall and reinstall OneDrive.</span></span>

<span data-ttu-id="f8e4e-249">Если кнопка **Открыть файл** неактивна, возможно, достигнуто предельное количество моделей, доступных для одновременного открытия в средстве 3D-просмотра.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-249">If the **Open File** button is not active, it's possible that you have reached the limit of models that can be open in 3D Viewer at one time.</span></span> <span data-ttu-id="f8e4e-250">Если в средстве 3D-просмотра открыто 40 моделей, потребуется закрыть некоторые из них перед дальнейшим открытием моделей.</span><span class="sxs-lookup"><span data-stu-id="f8e4e-250">If you have 40 models open in 3D Viewer, you will need to close some before you will be able to open additional models.</span></span>

## <span data-ttu-id="f8e4e-251">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f8e4e-251">Additional resources</span></span>

- [<span data-ttu-id="f8e4e-252">Форумы технической поддержки</span><span class="sxs-lookup"><span data-stu-id="f8e4e-252">Support forums</span></span>](http://forums.hololens.com/categories/3d-viewer-beta)
- [<span data-ttu-id="f8e4e-253">Уведомления третьих сторон</span><span class="sxs-lookup"><span data-stu-id="f8e4e-253">Third-party notices</span></span>](https://www.microsoft.com/{lang-locale}/legal/products)
