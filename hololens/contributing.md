---
title: Сопутствующие инструкции
description: узнайте, как вносить вклад в документацию по HoloLens на платформе docs.microsoft.com, используя Markdown с флагами GitHub.
author: hferrone
ms.author: mattwoj
ms.date: 01/04/2021
ms.topic: article
ms.prod: hololens
ms.openlocfilehash: 73b6e8bcd634cb4d45171bda0a85f2e991a977c9
ms.sourcegitcommit: c43cd2f450b643ad4fc8e749235d03ec5aa3ffcf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "113635676"
---
# <a name="contributing-to-the-hololens-documentation"></a><span data-ttu-id="fee7d-103">дополнение к документации по HoloLens</span><span class="sxs-lookup"><span data-stu-id="fee7d-103">Contributing to the HoloLens documentation</span></span>

<span data-ttu-id="fee7d-104">добро пожаловать в [HoloLensную документацию](https://github.com/MicrosoftDocs/Hololens)!</span><span class="sxs-lookup"><span data-stu-id="fee7d-104">Welcome to the [HoloLens documentation](https://github.com/MicrosoftDocs/Hololens)!</span></span> <span data-ttu-id="fee7d-105">Все статьи, созданные или измененные в этом репозитории, **будут доступны для общего пользования.**</span><span class="sxs-lookup"><span data-stu-id="fee7d-105">Any articles you create or edit in this repo **will be visible to the public.**</span></span> 

<span data-ttu-id="fee7d-106">HoloLensные документы отображаются на платформе docs.microsoft.com, в которой используются GitHub Markdown с функциями маркдиг.</span><span class="sxs-lookup"><span data-stu-id="fee7d-106">HoloLens docs are displayed on the docs.microsoft.com platform, which uses GitHub-flavored Markdown with Markdig features.</span></span> <span data-ttu-id="fee7d-107">Содержимое, которое вы редактируете в этом репозитории, форматируется на стилизованные страницы, отображаемые по адресу/хололенс.</span><span class="sxs-lookup"><span data-stu-id="fee7d-107">The content you edit in this repo gets formatted into stylized pages that show up at /hololens.</span></span>

<span data-ttu-id="fee7d-108">На этой странице описаны основные шаги и рекомендации по созданию и ссылкам на основы Markdown.</span><span class="sxs-lookup"><span data-stu-id="fee7d-108">This page covers the basic steps and guidelines for contributing and links to Markdown basics.</span></span> <span data-ttu-id="fee7d-109">Спасибо за ваше участие!</span><span class="sxs-lookup"><span data-stu-id="fee7d-109">Thanks for your contribution!</span></span>

## <a name="available-repos"></a><span data-ttu-id="fee7d-110">Доступные репозиториев</span><span class="sxs-lookup"><span data-stu-id="fee7d-110">Available repos</span></span>

| <span data-ttu-id="fee7d-111">Имя репозитория</span><span class="sxs-lookup"><span data-stu-id="fee7d-111">Repository name</span></span> | <span data-ttu-id="fee7d-112">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="fee7d-112">URL</span></span> |
| --- | --- |
| <span data-ttu-id="fee7d-113">HoloLens</span><span class="sxs-lookup"><span data-stu-id="fee7d-113">HoloLens</span></span> | [<span data-ttu-id="fee7d-114">MicrosoftDocs/HoloLens</span><span class="sxs-lookup"><span data-stu-id="fee7d-114">MicrosoftDocs/HoloLens</span></span>](https://github.com/MicrosoftDocs/Hololens) |
| <span data-ttu-id="fee7d-115">Смешанная реальность</span><span class="sxs-lookup"><span data-stu-id="fee7d-115">Mixed Reality</span></span> | [<span data-ttu-id="fee7d-116">MicrosoftDocs/Mixed-Reality</span><span class="sxs-lookup"><span data-stu-id="fee7d-116">MicrosoftDocs/mixed-reality</span></span>](/windows/mixed-reality) |
| <span data-ttu-id="fee7d-117">Руководством для энтузиастов</span><span class="sxs-lookup"><span data-stu-id="fee7d-117">VR Enthusiasts Guide</span></span> | [<span data-ttu-id="fee7d-118">MicrosoftDocs/Mixed-Reality/энтузиаст-Guide</span><span class="sxs-lookup"><span data-stu-id="fee7d-118">MicrosoftDocs/mixed-reality/enthusiast-guide</span></span>](https://github.com/MicrosoftDocs/mixed-reality/tree/docs/enthusiast-guide) |

## <a name="before-you-start"></a><span data-ttu-id="fee7d-119">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="fee7d-119">Before you start</span></span>

<span data-ttu-id="fee7d-120">если у вас его еще нет, необходимо [создать учетную запись GitHub](https://github.com/join).</span><span class="sxs-lookup"><span data-stu-id="fee7d-120">If you don't already have one, you'll need to [create a GitHub account](https://github.com/join).</span></span>

>[!NOTE]
><span data-ttu-id="fee7d-121">если вы являетесь сотрудником корпорации майкрософт, свяжите свою учетную запись GitHub с псевдонимом майкрософт на [портале microsoft Open Source](https://repos.opensource.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="fee7d-121">If you're a Microsoft employee, link your GitHub account to your Microsoft alias on the [Microsoft Open Source portal](https://repos.opensource.microsoft.com/).</span></span> <span data-ttu-id="fee7d-122">Присоединяйтесь к организациям **"Microsoft"** и **"MicrosoftDocs"** .</span><span class="sxs-lookup"><span data-stu-id="fee7d-122">Join the **"Microsoft"** and **"MicrosoftDocs"** organizations.</span></span>

<span data-ttu-id="fee7d-123">при настройке учетной записи GitHub также рекомендуются следующие меры безопасности:</span><span class="sxs-lookup"><span data-stu-id="fee7d-123">When setting up your GitHub account, we also recommend these security precautions:</span></span>
- <span data-ttu-id="fee7d-124">создайте [надежный пароль для учетной записи GitHub](https://github.com/settings/admin).</span><span class="sxs-lookup"><span data-stu-id="fee7d-124">Create a [strong password for your GitHub account](https://github.com/settings/admin).</span></span>
- <span data-ttu-id="fee7d-125">Включите [двухфакторную проверку подлинности](https://github.com/settings/two_factor_authentication/configure).</span><span class="sxs-lookup"><span data-stu-id="fee7d-125">Enable [two-factor authentication](https://github.com/settings/two_factor_authentication/configure).</span></span>
- <span data-ttu-id="fee7d-126">Сохраняйте [коды восстановления](https://github.com/settings/auth/recovery-codes) в надежном месте.</span><span class="sxs-lookup"><span data-stu-id="fee7d-126">Save your [recovery codes](https://github.com/settings/auth/recovery-codes) in a safe place.</span></span>
- <span data-ttu-id="fee7d-127">Обновите [Параметры общего профиля](https://github.com/settings/profile).</span><span class="sxs-lookup"><span data-stu-id="fee7d-127">Update your [public profile settings](https://github.com/settings/profile).</span></span>
   - <span data-ttu-id="fee7d-128">Задайте свое имя и рассмотрите возможность установки *общедоступного адреса электронной почты* , чтобы *не показывать свой адрес электронной почты*.</span><span class="sxs-lookup"><span data-stu-id="fee7d-128">Set your name, and consider setting your *Public email* to *Don't show my email address*.</span></span>
   - <span data-ttu-id="fee7d-129">Рекомендуется отправить изображение профиля, так как на страницах документов, на которые вы участвуете, отображается эскиз.</span><span class="sxs-lookup"><span data-stu-id="fee7d-129">We recommend you upload a profile picture because a thumbnail is shown on docs pages you contribute to.</span></span>
- <span data-ttu-id="fee7d-130">Если вы планируете использовать командную строку, рассмотрите возможность настройки [диспетчера учетных данных Git для Windows](https://github.com/Microsoft/Git-Credential-Manager-for-Windows/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="fee7d-130">If you plan to use the command line, consider setting up [Git Credential Manager for Windows](https://github.com/Microsoft/Git-Credential-Manager-for-Windows/releases/latest).</span></span> <span data-ttu-id="fee7d-131">Таким образом, вам не придется вводить пароль каждый раз, когда вы вносите вклад.</span><span class="sxs-lookup"><span data-stu-id="fee7d-131">That way, you won't have to enter your password every time you make a contribution.</span></span>

<span data-ttu-id="fee7d-132">система публикации связана с GitHub, поэтому эти действия важны.</span><span class="sxs-lookup"><span data-stu-id="fee7d-132">The publishing system is tied to GitHub, so these steps are important.</span></span> <span data-ttu-id="fee7d-133">в каждой статье вы будете входить как автор или участник, используя псевдоним GitHub.</span><span class="sxs-lookup"><span data-stu-id="fee7d-133">You'll be listed as either author or contributor to each article using your GitHub alias.</span></span>

## <a name="editing-an-existing-article"></a><span data-ttu-id="fee7d-134">Изменение существующей статьи</span><span class="sxs-lookup"><span data-stu-id="fee7d-134">Editing an existing article</span></span>

<span data-ttu-id="fee7d-135">используйте следующий рабочий процесс для обновления *существующей статьи* с помощью GitHub в веб-браузере:</span><span class="sxs-lookup"><span data-stu-id="fee7d-135">Use the following workflow to make updates to *an existing article* via GitHub in a web browser:</span></span>

1. <span data-ttu-id="fee7d-136">Перейдите к статье, которую вы хотите изменить, в папке "Mixed-Reality-документы".</span><span class="sxs-lookup"><span data-stu-id="fee7d-136">Navigate to the article you wish to edit in the "mixed-reality-docs" folder.</span></span>

2. <span data-ttu-id="fee7d-137">Нажмите кнопку "Изменить" (значок карандаша) в правом верхнем углу, которая автоматически развилкует удаляемую ветвь из "главной" ветви.</span><span class="sxs-lookup"><span data-stu-id="fee7d-137">Select the edit button (pencil icon) in the top right, which will automatically fork a disposable branch off the 'master' branch.</span></span>

   ![Изменение статьи.](images/editpage.png)
   
3. <span data-ttu-id="fee7d-139">Измените содержимое статьи согласно [«Markdown основы»](#markdown-basics).</span><span class="sxs-lookup"><span data-stu-id="fee7d-139">Edit the content of the article according to the ["Markdown basics"](#markdown-basics).</span></span>

4. <span data-ttu-id="fee7d-140">Обновите метаданные в верхней части каждой статьи:</span><span class="sxs-lookup"><span data-stu-id="fee7d-140">Update metadata at the top of each article:</span></span>

   * <span data-ttu-id="fee7d-141">**Title**: заголовок страницы, который отображается на вкладке браузер при просмотре статьи.</span><span class="sxs-lookup"><span data-stu-id="fee7d-141">**title**: Page title that appears in the browser tab when the article is being viewed.</span></span> <span data-ttu-id="fee7d-142">Заголовки страниц используются для SEO и индексирования, поэтому не следует изменять заголовок, если это не требуется (хотя это менее важно, прежде чем документация станет общедоступной).</span><span class="sxs-lookup"><span data-stu-id="fee7d-142">Page titles are used for SEO and indexing, so don't change the title unless necessary (though this is less critical before documentation goes public).</span></span>
   * <span data-ttu-id="fee7d-143">**Описание**. Напишите краткое описание содержимого статьи, которое увеличивает SEO и Discovery.</span><span class="sxs-lookup"><span data-stu-id="fee7d-143">**description**: Write a brief description of the article's content, which boosts SEO and discovery.</span></span>
   * <span data-ttu-id="fee7d-144">**автор**: если вы являетесь основным владельцем страницы, добавьте здесь псевдоним GitHub.</span><span class="sxs-lookup"><span data-stu-id="fee7d-144">**author**: If you're the primary owner of the page, add your GitHub alias here.</span></span>
   * <span data-ttu-id="fee7d-145">**MS. Author**: Если вы являетесь основным владельцем страницы, добавьте здесь свой псевдоним Майкрософт (вам не нужно @microsoft.com просто псевдоним).</span><span class="sxs-lookup"><span data-stu-id="fee7d-145">**ms.author**: If you're the primary owner of the page, add your Microsoft alias here (you don't need @microsoft.com, just the alias).</span></span>
   * <span data-ttu-id="fee7d-146">**MS. Date**: обновите дату, если на страницу добавляется основное содержимое, но не для таких исправлений, как пояснение, форматирование, грамматика или Орфография.</span><span class="sxs-lookup"><span data-stu-id="fee7d-146">**ms.date**: Update the date if you're adding major content to the page, but not for fixes like clarification, formatting, grammar, or spelling.</span></span>
   * <span data-ttu-id="fee7d-147">**Ключевые слова**: вспомогательные слова в SEO (оптимизация поисковой системы).</span><span class="sxs-lookup"><span data-stu-id="fee7d-147">**keywords**: Keywords aid in SEO (search engine optimization).</span></span> <span data-ttu-id="fee7d-148">Добавьте ключевые слова, разделенные запятыми и пробелами, которые относятся к вашей статье, но без знаков препинания после последнего ключевого слова в списке.</span><span class="sxs-lookup"><span data-stu-id="fee7d-148">Add keywords, separated by a comma and a space, that are specific to your article, but no punctuation after the last keyword in your list.</span></span> <span data-ttu-id="fee7d-149">Вам не нужно добавлять глобальные ключевые слова, которые применяются ко всем статьям, так как они управляются в других местах.</span><span class="sxs-lookup"><span data-stu-id="fee7d-149">You don't need to add global keywords that apply to all articles, as those are managed elsewhere.</span></span> 
   
5. <span data-ttu-id="fee7d-150">После внесения изменений в статью прокрутите вниз и выберите пункт **предложить изменение файла**.</span><span class="sxs-lookup"><span data-stu-id="fee7d-150">When you've completed your article edits, scroll down and select **Propose file change**.</span></span>

6. <span data-ttu-id="fee7d-151">На следующей странице выберите **создать запрос на вытягивание** для слияния автоматически созданной ветви с главной.</span><span class="sxs-lookup"><span data-stu-id="fee7d-151">On the next page, select **Create pull request** to merge your automatically created branch into 'master.'</span></span>

7. <span data-ttu-id="fee7d-152">Повторите описанные выше действия для следующей статьи, которую необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="fee7d-152">Repeat the steps above for the next article you want to edit.</span></span>

## <a name="renaming-or-deleting-an-existing-article"></a><span data-ttu-id="fee7d-153">Переименование или удаление существующей статьи</span><span class="sxs-lookup"><span data-stu-id="fee7d-153">Renaming or deleting an existing article</span></span>

<span data-ttu-id="fee7d-154">Если изменение приведет к переименованию или удалению существующей статьи, обязательно добавьте перенаправление.</span><span class="sxs-lookup"><span data-stu-id="fee7d-154">If your change will rename or delete an existing article, be sure to add a redirect.</span></span> <span data-ttu-id="fee7d-155">Таким образом, любой пользователь, имеющий ссылку на существующую статью, останется в нужном месте.</span><span class="sxs-lookup"><span data-stu-id="fee7d-155">That way, anyone with a link to the existing article will still end up in the right place.</span></span> <span data-ttu-id="fee7d-156">Перенаправления управляются .openpublishing.redirection.jsв файле в корне репозитория.</span><span class="sxs-lookup"><span data-stu-id="fee7d-156">Redirects are managed by the .openpublishing.redirection.json file in the root of the repo.</span></span>

<span data-ttu-id="fee7d-157">Чтобы добавить перенаправление к .openpublishing.redirection.jsв, добавьте запись в `redirections` массив:</span><span class="sxs-lookup"><span data-stu-id="fee7d-157">To add a redirect to .openpublishing.redirection.json, add an entry to the `redirections` array:</span></span>

```json
{
    "redirections": [
        {
            "source_path": "hololens/old-article.md",
            "redirect_url": "new-article#section-about-old-topic",
            "redirect_document_id": false
        },
```

- <span data-ttu-id="fee7d-158">`source_path`— Это относительный путь к старой статье, которую вы удаляете.</span><span class="sxs-lookup"><span data-stu-id="fee7d-158">The `source_path` is the relative repository path to the old article that you're removing.</span></span> <span data-ttu-id="fee7d-159">Убедитесь, что путь начинается с `mixed-reality-docs` и заканчивается на `.md` .</span><span class="sxs-lookup"><span data-stu-id="fee7d-159">Be sure the path starts with `mixed-reality-docs` and ends with `.md`.</span></span>

- <span data-ttu-id="fee7d-160">`redirect_url`— Это относительный общедоступный URL-адрес от старой статьи до новой статьи.</span><span class="sxs-lookup"><span data-stu-id="fee7d-160">The `redirect_url` is the relative public URL from the old article to the new article.</span></span> <span data-ttu-id="fee7d-161">Убедитесь, что этот URL-адрес **не** содержит `mixed-reality-docs` или `.md` , так как он ссылается на общедоступный URL-адрес, а не путь к репозиторию.</span><span class="sxs-lookup"><span data-stu-id="fee7d-161">Be sure that this URL **doesn't** contain `mixed-reality-docs` or `.md`, as it refers to the public URL and not the repository path.</span></span> <span data-ttu-id="fee7d-162">Связывание с разделом в новой статье с помощью `#section` допускается.</span><span class="sxs-lookup"><span data-stu-id="fee7d-162">Linking to a section within the new article using `#section` is allowed.</span></span> <span data-ttu-id="fee7d-163">При необходимости можно также использовать абсолютный путь к другому сайту.</span><span class="sxs-lookup"><span data-stu-id="fee7d-163">You can also use an absolute path to another site here, if necessary.</span></span>

- <span data-ttu-id="fee7d-164">`redirect_document_id` Указывает, хотите ли вы использовать идентификатор документа из предыдущего файла.</span><span class="sxs-lookup"><span data-stu-id="fee7d-164">`redirect_document_id` indicates whether you would like to keep the document ID from the previous file.</span></span> <span data-ttu-id="fee7d-165">Значение по умолчанию — `false`.</span><span class="sxs-lookup"><span data-stu-id="fee7d-165">The default is `false`.</span></span> <span data-ttu-id="fee7d-166">Используйте `true` , если хотите сохранить `ms.documentid` значение атрибута из перенаправленной статьи.</span><span class="sxs-lookup"><span data-stu-id="fee7d-166">Use `true` if you want to preserve the `ms.documentid` attribute value from the redirected article.</span></span> <span data-ttu-id="fee7d-167">Если сохранить идентификатор документа, данные, такие как Просмотры страниц и ранжирования, будут переданы в целевую статью.</span><span class="sxs-lookup"><span data-stu-id="fee7d-167">If you preserve the document ID, data, such as page views and rankings, will be transferred to the target article.</span></span> <span data-ttu-id="fee7d-168">Это следует делать, если перенаправление является главным переименованием, а не указателем на другую статью, охватывающую только часть одного и того же содержимого.</span><span class="sxs-lookup"><span data-stu-id="fee7d-168">Do this if the redirect is primarily a rename, and not a pointer to different article that only covers some of the same content.</span></span>

<span data-ttu-id="fee7d-169">Если вы добавляете перенаправление, обязательно удалите и старый файл.</span><span class="sxs-lookup"><span data-stu-id="fee7d-169">If you add a redirect, be sure to delete the old file as well.</span></span>

## <a name="creating-a-new-article"></a><span data-ttu-id="fee7d-170">Создание новой статьи</span><span class="sxs-lookup"><span data-stu-id="fee7d-170">Creating a new article</span></span>

<span data-ttu-id="fee7d-171">используйте следующий рабочий процесс для *создания новых статей* в репозитории документации с помощью GitHub в веб-браузере:</span><span class="sxs-lookup"><span data-stu-id="fee7d-171">Use the following workflow to *create new articles* in the documentation repo via GitHub in a web browser:</span></span>

1. <span data-ttu-id="fee7d-172">Создайте вилку из главной ветви MicrosoftDocs/Mixed-Reality (с помощью кнопки **ветвления** в правом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="fee7d-172">Create a fork off the MicrosoftDocs/mixed-reality 'master' branch (using the **Fork** button in the top right).</span></span>

   ![Разветвление главной ветви.](images/forkbranch.png)
   
2. <span data-ttu-id="fee7d-174">В папке "Mixed-Reality-документы" выберите **создать новый файл** в правом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="fee7d-174">In the "mixed-reality-docs" folder, select **Create new file** in the top right.</span></span>

3. <span data-ttu-id="fee7d-175">Создайте имя страницы для статьи (используйте дефисы вместо пробелов и не используйте знаки препинания или апострофы) и добавьте ". md".</span><span class="sxs-lookup"><span data-stu-id="fee7d-175">Create a page name for the article (use hyphens instead of spaces and don't use punctuation or apostrophes) and append ".md"</span></span>

   ![Присвойте имя новой странице.](images/newpagetitle.png)
   
   >[!IMPORTANT]
   ><span data-ttu-id="fee7d-177">Убедитесь, что новая статья создана в папке "Mixed-Reality-документы".</span><span class="sxs-lookup"><span data-stu-id="fee7d-177">Make sure you create the new article from within the "mixed-reality-docs" folder.</span></span> <span data-ttu-id="fee7d-178">Это можно проверить, проверив "/миксед-реалити-Докс/" в новой строке имени файла.</span><span class="sxs-lookup"><span data-stu-id="fee7d-178">You can confirm this by checking for "/mixed-reality-docs/" in the new file name line.</span></span>

4. <span data-ttu-id="fee7d-179">В верхней части новой страницы добавьте следующий блок метаданных:</span><span class="sxs-lookup"><span data-stu-id="fee7d-179">At the top of your new page, add the following metadata block:</span></span>

   ```md
   ---
   title:
   description:
   author:
   ms.author:
   ms.date:
   ms.topic: article
   keywords:
   ---
   ```

5. <span data-ttu-id="fee7d-180">Заполните соответствующие поля метаданных в соответствии с инструкциями в [разделе выше](#editing-an-existing-article).</span><span class="sxs-lookup"><span data-stu-id="fee7d-180">Fill in the relevant metadata fields per the instructions in the [section above](#editing-an-existing-article).</span></span>

6. <span data-ttu-id="fee7d-181">Запись содержимого статьи с помощью [основ Markdown](#markdown-basics).</span><span class="sxs-lookup"><span data-stu-id="fee7d-181">Write article content using [Markdown basics](#markdown-basics).</span></span>

7. <span data-ttu-id="fee7d-182">Добавьте `## See also` раздел в нижнюю часть статьи со ссылками на другие важные статьи.</span><span class="sxs-lookup"><span data-stu-id="fee7d-182">Add a `## See also` section at the bottom of the article with links to other relevant articles.</span></span>

8. <span data-ttu-id="fee7d-183">По завершении выберите **зафиксировать новый файл**.</span><span class="sxs-lookup"><span data-stu-id="fee7d-183">When finished, select **Commit new file**.</span></span>

9. <span data-ttu-id="fee7d-184">Выберите **новый запрос на вытягивание** и объедините главную ветвь вилки в MicrosoftDocs/Mixed-Reality "Master" (убедитесь, что стрелка правильно указывает).</span><span class="sxs-lookup"><span data-stu-id="fee7d-184">Select **New pull request** and merge your fork's 'master' branch into MicrosoftDocs/mixed-reality 'master' (make sure the arrow is pointing the correct way).</span></span>

   ![Создание запроса на вытягивание из вилки в MicrosoftDocs/Mixed-Reality](images/pr-to-master.png)

## <a name="markdown-basics"></a><span data-ttu-id="fee7d-186">Базовые сведения о Markdown</span><span class="sxs-lookup"><span data-stu-id="fee7d-186">Markdown basics</span></span>

<span data-ttu-id="fee7d-187">Следующие ресурсы помогут узнать, как изменить документацию с помощью языка Markdown:</span><span class="sxs-lookup"><span data-stu-id="fee7d-187">The following resources will help you learn how to edit documentation using the Markdown language:</span></span>

- [<span data-ttu-id="fee7d-188">Основы Markdown</span><span class="sxs-lookup"><span data-stu-id="fee7d-188">Markdown basics</span></span>](https://help.github.com/articles/basic-writing-and-formatting-syntax/)
- [<span data-ttu-id="fee7d-189">Дополнительные ресурсы для записи Markdown для docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="fee7d-189">Additional resources for writing Markdown for docs.microsoft.com</span></span>](/contribute/how-to-write-use-markdown)

### <a name="adding-tables"></a><span data-ttu-id="fee7d-190">Добавление таблиц</span><span class="sxs-lookup"><span data-stu-id="fee7d-190">Adding tables</span></span>

<span data-ttu-id="fee7d-191">Из-за того, что таблицы стилей docs.microsoft.com, они не будут иметь границы или пользовательские стили, даже если вы попробуете использовать встроенный код CSS.</span><span class="sxs-lookup"><span data-stu-id="fee7d-191">Because of the way docs.microsoft.com styles tables, they won’t have borders or custom styles, even if you try inline CSS.</span></span> <span data-ttu-id="fee7d-192">Он будет работать в течение короткого периода времени, но в конечном итоге платформа будет выводить стили из таблицы.</span><span class="sxs-lookup"><span data-stu-id="fee7d-192">It will appear to work for a short period of time, but eventually the platform will strip the styling out of the table.</span></span> <span data-ttu-id="fee7d-193">Итак, планируйте и старайтесь не усложнять таблицы.</span><span class="sxs-lookup"><span data-stu-id="fee7d-193">So plan ahead and keep your tables simple.</span></span> <span data-ttu-id="fee7d-194">[Вот сайт, который упрощает Markdown таблицы](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="fee7d-194">[Here’s a site that makes Markdown tables easy](https://www.tablesgenerator.com/markdown_tables).</span></span>

<span data-ttu-id="fee7d-195">[расширение "документы Markdown" для Visual Studio Code](/teamblog/docs-extension) также упрощает создание таблиц, если вы используете [Visual Studio Code (см. ниже)](#using-visual-studio-code) , чтобы изменить документацию.</span><span class="sxs-lookup"><span data-stu-id="fee7d-195">The [Docs Markdown Extension for Visual Studio Code](/teamblog/docs-extension) also makes table generation easy if you're using [Visual Studio Code (see below)](#using-visual-studio-code) to edit the documentation.</span></span>

### <a name="adding-images"></a><span data-ttu-id="fee7d-196">Добавление изображений</span><span class="sxs-lookup"><span data-stu-id="fee7d-196">Adding images</span></span>

<span data-ttu-id="fee7d-197">Вам потребуется передать изображения в папку "Mixed-Reality-документы/изображения" в репозитории, а затем ссылаться на них соответствующим образом в статье.</span><span class="sxs-lookup"><span data-stu-id="fee7d-197">You’ll need to upload your images to the "mixed-reality-docs/images" folder in the repo, and then reference them appropriately in the article.</span></span> <span data-ttu-id="fee7d-198">Изображения будут автоматически отображаться в полном размере, что означает, что крупные изображения будут заполнять всю ширину статьи.</span><span class="sxs-lookup"><span data-stu-id="fee7d-198">Images will automatically show up at full-size, which means large images will fill the entire width of the article.</span></span> <span data-ttu-id="fee7d-199">Рекомендуется предварительно изменить размер изображений перед их отправкой.</span><span class="sxs-lookup"><span data-stu-id="fee7d-199">We recommend pre-sizing your images before uploading them.</span></span> <span data-ttu-id="fee7d-200">Рекомендуемая ширина составляет от 600 до 700 пикселей, хотя размер снимка экрана или части снимка экрана, соответственно, должен быть больше или меньше.</span><span class="sxs-lookup"><span data-stu-id="fee7d-200">The recommended width is between 600 and 700 pixels, though you should size up or down if it’s a dense screenshot or a fraction of a screenshot, respectively.</span></span>

>[!IMPORTANT]
><span data-ttu-id="fee7d-201">Вы можете отправлять изображения только в разветвленный репозиторий перед слиянием.</span><span class="sxs-lookup"><span data-stu-id="fee7d-201">You can only upload images to your forked repo before merging.</span></span> <span data-ttu-id="fee7d-202">таким образом, если вы планируете добавлять изображения в статью, вам потребуется [использовать Visual Studio Code](#using-visual-studio-code) , чтобы добавить изображения в папку "images" вилки, или убедиться в том, что в веб-браузере выполнены следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fee7d-202">So, if you plan on adding images to an article, you'll need to [use Visual Studio Code](#using-visual-studio-code) to add the images to your fork's "images" folder first or make sure you've done the following in a web browser:</span></span>
>
>1. <span data-ttu-id="fee7d-203">Разветвление репозитория MicrosoftDocs/Mixed-Reality.</span><span class="sxs-lookup"><span data-stu-id="fee7d-203">Forked the MicrosoftDocs/mixed-reality repo.</span></span>
>2. <span data-ttu-id="fee7d-204">Изменение статьи в вилке.</span><span class="sxs-lookup"><span data-stu-id="fee7d-204">Edited the article in your fork.</span></span>
>3. <span data-ttu-id="fee7d-205">В папку "Mixed-Reality-документы/изображения" в вилке отправлены изображения, на которые вы ссылаетесь в этой статье.</span><span class="sxs-lookup"><span data-stu-id="fee7d-205">Uploaded the images you're referencing in your article to the "mixed-reality-docs/images" folder in your fork.</span></span>
>4. <span data-ttu-id="fee7d-206">Создан **запрос на вытягивание** для объединения вилки в главную ветвь MicrosoftDocs/Mixed-Reality.</span><span class="sxs-lookup"><span data-stu-id="fee7d-206">Created a **pull request** to merge your fork into the MicrosoftDocs/mixed-reality 'master' branch.</span></span>
>
><span data-ttu-id="fee7d-207">Чтобы узнать, как настроить собственный разветвленный репозиторий, следуйте инструкциям по [созданию новой статьи](#creating-a-new-article).</span><span class="sxs-lookup"><span data-stu-id="fee7d-207">To learn how to set up your own forked repo, follow the instructions for [creating a new article](#creating-a-new-article).</span></span>

## <a name="previewing-your-work"></a><span data-ttu-id="fee7d-208">Предварительный просмотр работы</span><span class="sxs-lookup"><span data-stu-id="fee7d-208">Previewing your work</span></span>

<span data-ttu-id="fee7d-209">при редактировании в GitHub через веб-браузер можно выбрать вкладку **предварительный просмотр** в верхней части страницы для предварительного просмотра работы перед фиксацией.</span><span class="sxs-lookup"><span data-stu-id="fee7d-209">While editing in GitHub via a web browser, you can select the **Preview** tab near the top of the page to preview your work before committing.</span></span> 

>[!NOTE]
><span data-ttu-id="fee7d-210">Предварительный просмотр изменений в review.docs.microsoft.com доступен только для сотрудников Майкрософт</span><span class="sxs-lookup"><span data-stu-id="fee7d-210">Previewing your changes on review.docs.microsoft.com is only available to Microsoft employees</span></span>

<span data-ttu-id="fee7d-211">Сотрудники корпорации Майкрософт. После объединения публикаций в главную ветвь вы можете ознакомиться с содержимым, прежде чем оно станет общедоступным в </хололенс? Branch = Master>.</span><span class="sxs-lookup"><span data-stu-id="fee7d-211">Microsoft employees: once your contributions have been merged into the 'master' branch, you can review the content before it goes public at </hololens?branch=master>.</span></span> <span data-ttu-id="fee7d-212">Найдите статью, используя оглавление в левом столбце.</span><span class="sxs-lookup"><span data-stu-id="fee7d-212">Find your article using the table of contents in the left column.</span></span>

## <a name="editing-in-the-browser-vs-editing-with-a-desktop-client"></a><span data-ttu-id="fee7d-213">Редактирование в браузере и редактирование с помощью настольного клиента</span><span class="sxs-lookup"><span data-stu-id="fee7d-213">Editing in the browser vs. editing with a desktop client</span></span>

<span data-ttu-id="fee7d-214">Редактирование в браузере является самым простым способом внесения быстрых изменений, однако существует несколько недостатков.</span><span class="sxs-lookup"><span data-stu-id="fee7d-214">Editing in the browser is the easiest way to make quick changes, however, there are a few disadvantages:</span></span>

- <span data-ttu-id="fee7d-215">Вы не получаете проверку орфографии.</span><span class="sxs-lookup"><span data-stu-id="fee7d-215">You don't get spell-check.</span></span>
- <span data-ttu-id="fee7d-216">Вы не получаете никаких интеллектуальных связей с другими статьями (необходимо вручную ввести имя файла статьи).</span><span class="sxs-lookup"><span data-stu-id="fee7d-216">You don't get any smart-linking to other articles (you have to manually type the article's filename).</span></span>
- <span data-ttu-id="fee7d-217">Загрузка и ссылки на изображения могут быть трудной.</span><span class="sxs-lookup"><span data-stu-id="fee7d-217">It can be a hassle to upload and reference images.</span></span>

<span data-ttu-id="fee7d-218">если вы не будете работать с этими проблемами, используйте настольный клиент, например [Visual Studio Code](https://code.visualstudio.com/) , с помощью нескольких [полезных расширений](#useful-extensions) .</span><span class="sxs-lookup"><span data-stu-id="fee7d-218">If you'd rather not deal with these issues, use a desktop client like [Visual Studio Code](https://code.visualstudio.com/) with a couple [helpful extensions](#useful-extensions) when contributing.</span></span>

## <a name="using-visual-studio-code"></a><span data-ttu-id="fee7d-219">Использование Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="fee7d-219">Using Visual Studio Code</span></span>

<span data-ttu-id="fee7d-220">По указанным [выше](#editing-in-the-browser-vs-editing-with-a-desktop-client)причинам вы можете использовать Настольный клиент для редактирования документации вместо веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="fee7d-220">For the reasons listed [above](#editing-in-the-browser-vs-editing-with-a-desktop-client), you may prefer using a desktop client to edit documentation instead of a web browser.</span></span> <span data-ttu-id="fee7d-221">рекомендуется использовать [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="fee7d-221">We recommend using [Visual Studio Code](https://code.visualstudio.com/).</span></span>

### <a name="setup"></a><span data-ttu-id="fee7d-222">Настройка</span><span class="sxs-lookup"><span data-stu-id="fee7d-222">Setup</span></span>

<span data-ttu-id="fee7d-223">выполните следующие действия, чтобы настроить Visual Studio Code для работы с этим репозиторием:</span><span class="sxs-lookup"><span data-stu-id="fee7d-223">Follow these steps to configure Visual Studio Code to work with this repo:</span></span>

1. <span data-ttu-id="fee7d-224">В веб-браузере:</span><span class="sxs-lookup"><span data-stu-id="fee7d-224">In a web browser:</span></span>
    1. <span data-ttu-id="fee7d-225">Установите [Git для своего компьютера](https://git-scm.com/downloads).</span><span class="sxs-lookup"><span data-stu-id="fee7d-225">Install [Git for your PC](https://git-scm.com/downloads).</span></span>
    2. <span data-ttu-id="fee7d-226">Установите [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="fee7d-226">Install [Visual Studio Code](https://code.visualstudio.com/).</span></span>
    3. <span data-ttu-id="fee7d-227">[Разветвление MicrosoftDocs/Mixed-Reality](#creating-a-new-article) , если вы еще этого не сделали.</span><span class="sxs-lookup"><span data-stu-id="fee7d-227">[Fork MicrosoftDocs/mixed-reality](#creating-a-new-article) if you haven't already.</span></span>
    4. <span data-ttu-id="fee7d-228">В вилке выберите **клонировать или скачать** и скопируйте URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="fee7d-228">In your fork, select **Clone or download** and copy the URL.</span></span>
2. <span data-ttu-id="fee7d-229">Создайте локальный клон разветвления в Visual Studio Code:</span><span class="sxs-lookup"><span data-stu-id="fee7d-229">Create a local clone of your fork in Visual Studio Code:</span></span>
    1. <span data-ttu-id="fee7d-230">В меню **вид** выберите пункт **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="fee7d-230">From the **View** menu, select **Command Palette**.</span></span>
    2. <span data-ttu-id="fee7d-231">Введите "Git: Clone".</span><span class="sxs-lookup"><span data-stu-id="fee7d-231">Type "Git: Clone."</span></span>
    3. <span data-ttu-id="fee7d-232">Вставьте скопированный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="fee7d-232">Paste the URL you copied.</span></span>
    4. <span data-ttu-id="fee7d-233">Выберите место сохранения клона на компьютере.</span><span class="sxs-lookup"><span data-stu-id="fee7d-233">Choose where to save the clone on your PC.</span></span>
    5. <span data-ttu-id="fee7d-234">Выберите **Открыть репозиторий** во всплывающем окне.</span><span class="sxs-lookup"><span data-stu-id="fee7d-234">Select **Open repo** in the pop-up.</span></span>

### <a name="editing-documentation"></a><span data-ttu-id="fee7d-235">Редактирование документации</span><span class="sxs-lookup"><span data-stu-id="fee7d-235">Editing documentation</span></span>

<span data-ttu-id="fee7d-236">Используйте следующий рабочий процесс, чтобы внести изменения в документацию с помощью Visual Studio Code:</span><span class="sxs-lookup"><span data-stu-id="fee7d-236">Use the following workflow to make changes to the documentation with Visual Studio Code:</span></span>

>[!NOTE]
><span data-ttu-id="fee7d-237">все рекомендации по [редактированию](#editing-an-existing-article) и [созданию](#creating-a-new-article) статей, а также [основы редактирования Markdown](#markdown-basics), приведенные выше, применяются и при использовании Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="fee7d-237">All the guidance for [editing](#editing-an-existing-article) and [creating](#creating-a-new-article) articles, and the [basics of editing Markdown](#markdown-basics), from above applies when using Visual Studio Code as well.</span></span>

1. <span data-ttu-id="fee7d-238">Убедитесь, что клонированная вилка актуальна с официальным репозиторием.</span><span class="sxs-lookup"><span data-stu-id="fee7d-238">Make sure your cloned fork is up to date with the official repo.</span></span>

   1. <span data-ttu-id="fee7d-239">В веб-браузере создайте запрос на вытягивание, чтобы синхронизировать последние изменения от других участников в MicrosoftDocs/Mixed-Reality "Master" с вилкой (убедитесь, что стрелка правильно указывает).</span><span class="sxs-lookup"><span data-stu-id="fee7d-239">In a web browser, create a pull request to sync recent changes from other contributors in MicrosoftDocs/mixed-reality 'master' to your fork (make sure the arrow is pointing the right way).</span></span>
      
      ![Синхронизация изменений из MicrosoftDocs/Mixed-Reality с вилкой](images/sync-repos.png)
      
   2. <span data-ttu-id="fee7d-241">в Visual Studio Code нажмите кнопку синхронизация, чтобы синхронизировать обновленную вилку с локальным клоном.</span><span class="sxs-lookup"><span data-stu-id="fee7d-241">In Visual Studio Code, select the sync button to sync your freshly updated fork to the local clone.</span></span>
      
      ![Щелкните изображение кнопки синхронизации.](images/sync-clone.png)
      
2. <span data-ttu-id="fee7d-243&quot;>Создание или изменение статей в клонированном репозитории с помощью Visual Studio Code.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;fee7d-243&quot;>Create or edit articles in your cloned repo using Visual Studio Code.</span></span>

   1. <span data-ttu-id=&quot;fee7d-244&quot;>Измените одну или несколько статей (при необходимости добавьте изображения в папку &quot;изображения").</span><span class="sxs-lookup"><span data-stu-id="fee7d-244">Edit one or more articles (add images to “images” folder if necessary).</span></span>
   
   2. <span data-ttu-id="fee7d-245">**Сохраните** изменения в **обозревателе**.</span><span class="sxs-lookup"><span data-stu-id="fee7d-245">**Save** changes in **Explorer**.</span></span>
      
      ![Выбор "сохранить все" в обозревателе](images/explorer-save.png)
      
   3. <span data-ttu-id="fee7d-247">**Зафиксировать все** изменения в **системе управления версиями** (записать сообщение о фиксации при появлении запроса).</span><span class="sxs-lookup"><span data-stu-id="fee7d-247">**Commit all** changes in **Source Control** (write commit message when prompted).</span></span>
   
      ![Выбор команды "фиксировать все" в системе управления версиями](images/source-control-commit.png)
      
   4. <span data-ttu-id="fee7d-249">Нажмите кнопку **Синхронизация** , чтобы синхронизировать изменения с источником (вилка на GitHub).</span><span class="sxs-lookup"><span data-stu-id="fee7d-249">Select the **sync** button to sync your changes back to origin (your fork on GitHub).</span></span>
      
      ![Нажмите кнопку "Синхронизация"](images/sync-back.png)
      
3. <span data-ttu-id="fee7d-251">В веб-браузере создайте запрос на вытягивание, чтобы синхронизировать новые изменения в вилке с MicrosoftDocs/Mixed-Reality "Master" (убедитесь, что стрелка указывает на правильный способ).</span><span class="sxs-lookup"><span data-stu-id="fee7d-251">In a web browser, create a pull request to sync new changes in your fork back to MicrosoftDocs/mixed-reality 'master' (make sure the arrow is pointing the correct way).</span></span>

   ![Создание запроса на вытягивание из вилки в MicrosoftDocs/Mixed-Reality](images/pr-to-master.png)

### <a name="useful-extensions"></a><span data-ttu-id="fee7d-253">Полезные расширения</span><span class="sxs-lookup"><span data-stu-id="fee7d-253">Useful extensions</span></span>

<span data-ttu-id="fee7d-254">следующие расширения Visual Studio Code полезны при редактировании документации:</span><span class="sxs-lookup"><span data-stu-id="fee7d-254">The following Visual Studio Code extensions are useful when editing documentation:</span></span>

- <span data-ttu-id="fee7d-255">[документация расширения Markdown для Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) — используйте **сочетание клавиш Alt + M** , чтобы открыть меню параметров создания документов, таких как:</span><span class="sxs-lookup"><span data-stu-id="fee7d-255">[Docs Markdown Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) - Use **Alt+M** to bring up a menu of docs authoring options like:</span></span>
   - <span data-ttu-id="fee7d-256">Поиск и ссылки на отправленные образы.</span><span class="sxs-lookup"><span data-stu-id="fee7d-256">Search and reference images you've uploaded.</span></span>
   - <span data-ttu-id="fee7d-257">Добавьте форматирование, например списки, таблицы и связанные с документацией вызовы, такие как `>[!NOTE]` .</span><span class="sxs-lookup"><span data-stu-id="fee7d-257">Add formatting like lists, tables, and docs-specific call-outs like `>[!NOTE]`.</span></span>
   - <span data-ttu-id="fee7d-258">Поиск и ссылки на внутренние ссылки и закладки (ссылки на определенные разделы на странице).</span><span class="sxs-lookup"><span data-stu-id="fee7d-258">Search and reference internal links and bookmarks (links to specific sections within a page).</span></span>
   - <span data-ttu-id="fee7d-259">Ошибки форматирования выделяются (наведите указатель мыши на ошибку, чтобы узнать больше).</span><span class="sxs-lookup"><span data-stu-id="fee7d-259">Formatting errors are highlighted (hover your mouse over the error to learn more).</span></span>
- <span data-ttu-id="fee7d-260">[Средство проверки орфографии кода](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) — слова с ошибками будут подчеркнуты. Щелкните правой кнопкой мыши слово с ошибками, чтобы изменить его или сохранить в словаре.</span><span class="sxs-lookup"><span data-stu-id="fee7d-260">[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) - misspelled words will be underlined; right-click on a misspelled word to change it or save it to the dictionary.</span></span>
