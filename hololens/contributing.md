---
title: Инструкции по вкладам
description: Узнайте, как внести свой вклад в документы HoloLens на docs.microsoft.com с помощью Markdown с привязаниями к GitHub.
author: hferrone
ms.author: mattwoj
ms.date: 01/04/2021
ms.topic: article
ms.prod: hololens
ms.openlocfilehash: 311da6bc52098d5ba16e4684f68fec9a01e7c23b
ms.sourcegitcommit: 8cea4c04c6d2e22225f4de43e10c05dab840736a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "11253861"
---
# <span data-ttu-id="a473a-103">Участие в документации holoLens</span><span class="sxs-lookup"><span data-stu-id="a473a-103">Contributing to the HoloLens documentation</span></span>

<span data-ttu-id="a473a-104">Вас приветствует [документация по HoloLens!](https://github.com/MicrosoftDocs/Hololens)</span><span class="sxs-lookup"><span data-stu-id="a473a-104">Welcome to the [HoloLens documentation](https://github.com/MicrosoftDocs/Hololens)!</span></span> <span data-ttu-id="a473a-105">Все статьи, которые вы создаете или редактируете в этом репо, будут **видны для всех.**</span><span class="sxs-lookup"><span data-stu-id="a473a-105">Any articles you create or edit in this repo **will be visible to the public.**</span></span> 

<span data-ttu-id="a473a-106">Документы HoloLens отображаются на платформе docs.microsoft.com, которая использует markdown с docs.microsoft.com GitHub с функциями Markdig.</span><span class="sxs-lookup"><span data-stu-id="a473a-106">HoloLens docs are displayed on the docs.microsoft.com platform, which uses GitHub-flavored Markdown with Markdig features.</span></span> <span data-ttu-id="a473a-107">Содержимое, которое вы редактируете в этом репо, отформатировано на стилизованные страницы, которые будут отформатированы в https://docs.microsoft.com/hololens .</span><span class="sxs-lookup"><span data-stu-id="a473a-107">The content you edit in this repo gets formatted into stylized pages that show up at https://docs.microsoft.com/hololens.</span></span> 

<span data-ttu-id="a473a-108">На этой странице освещаются основные действия и рекомендации по подготовке к основам Markdown и ссылки на них.</span><span class="sxs-lookup"><span data-stu-id="a473a-108">This page covers the basic steps and guidelines for contributing and links to Markdown basics.</span></span> <span data-ttu-id="a473a-109">Благодарим за ваш вклад!</span><span class="sxs-lookup"><span data-stu-id="a473a-109">Thanks for your contribution!</span></span>

## <span data-ttu-id="a473a-110">Доступные репозитные данные</span><span class="sxs-lookup"><span data-stu-id="a473a-110">Available repos</span></span>

| <span data-ttu-id="a473a-111">Имя репозитория</span><span class="sxs-lookup"><span data-stu-id="a473a-111">Repository name</span></span> | <span data-ttu-id="a473a-112">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="a473a-112">URL</span></span> |
| --- | --- |
| <span data-ttu-id="a473a-113">HoloLens</span><span class="sxs-lookup"><span data-stu-id="a473a-113">HoloLens</span></span> | [<span data-ttu-id="a473a-114">MicrosoftDocs/HoloLens</span><span class="sxs-lookup"><span data-stu-id="a473a-114">MicrosoftDocs/HoloLens</span></span>](https://github.com/MicrosoftDocs/Hololens) |
| <span data-ttu-id="a473a-115">Смешанная реальность</span><span class="sxs-lookup"><span data-stu-id="a473a-115">Mixed Reality</span></span> | [<span data-ttu-id="a473a-116">MicrosoftDocs/mixed-reality</span><span class="sxs-lookup"><span data-stu-id="a473a-116">MicrosoftDocs/mixed-reality</span></span>](https://docs.microsoft.com/windows/mixed-reality) |
| <span data-ttu-id="a473a-117">Руководство для энтузиастов виртуальной реальности</span><span class="sxs-lookup"><span data-stu-id="a473a-117">VR Enthusiasts Guide</span></span> | [<span data-ttu-id="a473a-118">MicrosoftDocs/mixed-reality/enthusiast-guide</span><span class="sxs-lookup"><span data-stu-id="a473a-118">MicrosoftDocs/mixed-reality/enthusiast-guide</span></span>](https://github.com/MicrosoftDocs/mixed-reality/tree/docs/enthusiast-guide) |

## <span data-ttu-id="a473a-119">Прежде чем начать</span><span class="sxs-lookup"><span data-stu-id="a473a-119">Before you start</span></span>

<span data-ttu-id="a473a-120">Если у вас еще нет учетной записи, необходимо создать учетную запись [GitHub.](https://github.com/join)</span><span class="sxs-lookup"><span data-stu-id="a473a-120">If you don't already have one, you'll need to [create a GitHub account](https://github.com/join).</span></span>

>[!NOTE]
><span data-ttu-id="a473a-121">Если вы сотрудник Майкрософт, привяжете свою учетную запись GitHub к псевдониму Майкрософт на [портале Microsoft Open Source.](https://repos.opensource.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="a473a-121">If you're a Microsoft employee, link your GitHub account to your Microsoft alias on the [Microsoft Open Source portal](https://repos.opensource.microsoft.com/).</span></span> <span data-ttu-id="a473a-122">Присоединяйтесь к **организациям Microsoft и** **MicrosoftDocs.**</span><span class="sxs-lookup"><span data-stu-id="a473a-122">Join the **"Microsoft"** and **"MicrosoftDocs"** organizations.</span></span>

<span data-ttu-id="a473a-123">При настройке учетной записи GitHub также рекомендуется использовать указанные здесь меры безопасности.</span><span class="sxs-lookup"><span data-stu-id="a473a-123">When setting up your GitHub account, we also recommend these security precautions:</span></span>
- <span data-ttu-id="a473a-124">Создайте [надежный пароль для учетной записи GitHub.](https://github.com/settings/admin)</span><span class="sxs-lookup"><span data-stu-id="a473a-124">Create a [strong password for your GitHub account](https://github.com/settings/admin).</span></span>
- <span data-ttu-id="a473a-125">В [включить двух-факторную проверку подлинности.](https://github.com/settings/two_factor_authentication/configure)</span><span class="sxs-lookup"><span data-stu-id="a473a-125">Enable [two-factor authentication](https://github.com/settings/two_factor_authentication/configure).</span></span>
- <span data-ttu-id="a473a-126">Сохраните [коды восстановления](https://github.com/settings/auth/recovery-codes) в надежном месте.</span><span class="sxs-lookup"><span data-stu-id="a473a-126">Save your [recovery codes](https://github.com/settings/auth/recovery-codes) in a safe place.</span></span>
- <span data-ttu-id="a473a-127">Обновите [параметры общедоступных профилей.](https://github.com/settings/profile)</span><span class="sxs-lookup"><span data-stu-id="a473a-127">Update your [public profile settings](https://github.com/settings/profile).</span></span>
   - <span data-ttu-id="a473a-128">Укажите свое имя и задумайтесь, чтобы в общедоступных сообщениях *не* показывать мой *адрес электронной почты.*</span><span class="sxs-lookup"><span data-stu-id="a473a-128">Set your name, and consider setting your *Public email* to *Don't show my email address*.</span></span>
   - <span data-ttu-id="a473a-129">Мы рекомендуем отправить изображение профиля, так как эскиз отображается на страницах docs, на которые вы вносите свой вклад.</span><span class="sxs-lookup"><span data-stu-id="a473a-129">We recommend you upload a profile picture because a thumbnail is shown on docs pages you contribute to.</span></span>
- <span data-ttu-id="a473a-130">Если вы планируете использовать командную строку, рассмотрите возможность настройки [диспетчера учетных данных Git для Windows.](https://github.com/Microsoft/Git-Credential-Manager-for-Windows/releases/latest)</span><span class="sxs-lookup"><span data-stu-id="a473a-130">If you plan to use the command line, consider setting up [Git Credential Manager for Windows](https://github.com/Microsoft/Git-Credential-Manager-for-Windows/releases/latest).</span></span> <span data-ttu-id="a473a-131">Таким образом, вам не придется вводить пароль каждый раз, когда вы вносите свой вклад.</span><span class="sxs-lookup"><span data-stu-id="a473a-131">That way, you won't have to enter your password every time you make a contribution.</span></span>

<span data-ttu-id="a473a-132">Система публикации привязана к GitHub, поэтому эти действия важны.</span><span class="sxs-lookup"><span data-stu-id="a473a-132">The publishing system is tied to GitHub, so these steps are important.</span></span> <span data-ttu-id="a473a-133">You'll be listed as either author or contributor to each article using your GitHub alias.</span><span class="sxs-lookup"><span data-stu-id="a473a-133">You'll be listed as either author or contributor to each article using your GitHub alias.</span></span>

## <span data-ttu-id="a473a-134">Редактирование существующей статьи</span><span class="sxs-lookup"><span data-stu-id="a473a-134">Editing an existing article</span></span>

<span data-ttu-id="a473a-135">Используйте следующий рабочий процесс для обновления \*\* существующей статьи через GitHub в веб-браузере:</span><span class="sxs-lookup"><span data-stu-id="a473a-135">Use the following workflow to make updates to *an existing article* via GitHub in a web browser:</span></span>

1. <span data-ttu-id="a473a-136">Перейдите к статье, которую вы хотите изменить, в папке "mixed-reality-docs".</span><span class="sxs-lookup"><span data-stu-id="a473a-136">Navigate to the article you wish to edit in the "mixed-reality-docs" folder.</span></span>

2. <span data-ttu-id="a473a-137">Выберите кнопку редактирования (значок карандаша) в правом верхнем окне, которая автоматически разветвит высвоблимую ветвь за ветвь "главный".</span><span class="sxs-lookup"><span data-stu-id="a473a-137">Select the edit button (pencil icon) in the top right, which will automatically fork a disposable branch off the 'master' branch.</span></span>

   ![Редактирование статьи.](images/editpage.png)
   
3. <span data-ttu-id="a473a-139">Отредактируем содержимое статьи в соответствии с ["Основами Markdown"](#markdown-basics).</span><span class="sxs-lookup"><span data-stu-id="a473a-139">Edit the content of the article according to the ["Markdown basics"](#markdown-basics).</span></span>

4. <span data-ttu-id="a473a-140">Обновите метаданные в верхней части каждой статьи:</span><span class="sxs-lookup"><span data-stu-id="a473a-140">Update metadata at the top of each article:</span></span>

   * <span data-ttu-id="a473a-141">**title**: название страницы, которое отображается на вкладке браузера при просмотре статьи.</span><span class="sxs-lookup"><span data-stu-id="a473a-141">**title**: Page title that appears in the browser tab when the article is being viewed.</span></span> <span data-ttu-id="a473a-142">Заголовки страниц используются для SEO и индексирования, поэтому не изменяйте заголовок, если это не требуется (хотя это менее важно, прежде чем документация становится открытой).</span><span class="sxs-lookup"><span data-stu-id="a473a-142">Page titles are used for SEO and indexing, so don't change the title unless necessary (though this is less critical before documentation goes public).</span></span>
   * <span data-ttu-id="a473a-143">**description**: write a brief description of the article's content, which boosts SEO and discovery.</span><span class="sxs-lookup"><span data-stu-id="a473a-143">**description**: Write a brief description of the article's content, which boosts SEO and discovery.</span></span>
   * <span data-ttu-id="a473a-144">**author**: если вы основной владелец страницы, добавьте здесь псевдоним GitHub.</span><span class="sxs-lookup"><span data-stu-id="a473a-144">**author**: If you're the primary owner of the page, add your GitHub alias here.</span></span>
   * <span data-ttu-id="a473a-145">**ms.author:** если вы основной владелец страницы, добавьте здесь псевдоним Майкрософт (вам не нужен @microsoft.com, а только псевдоним).</span><span class="sxs-lookup"><span data-stu-id="a473a-145">**ms.author**: If you're the primary owner of the page, add your Microsoft alias here (you don't need @microsoft.com, just the alias).</span></span>
   * <span data-ttu-id="a473a-146">**ms.date**: обновите дату, если вы добавляете на страницу основной контент, но не для таких исправлений, как пояснение, форматирование, грамматика или правописание.</span><span class="sxs-lookup"><span data-stu-id="a473a-146">**ms.date**: Update the date if you're adding major content to the page, but not for fixes like clarification, formatting, grammar, or spelling.</span></span>
   * <span data-ttu-id="a473a-147">**keywords**: Keywords aid in SEO (search engine optimization).</span><span class="sxs-lookup"><span data-stu-id="a473a-147">**keywords**: Keywords aid in SEO (search engine optimization).</span></span> <span data-ttu-id="a473a-148">Добавьте ключевые слова, разделенные запятой и пробелом, которые специфичны для вашей статьи, но без знака препинания после последнего ключевого слова в списке.</span><span class="sxs-lookup"><span data-stu-id="a473a-148">Add keywords, separated by a comma and a space, that are specific to your article, but no punctuation after the last keyword in your list.</span></span> <span data-ttu-id="a473a-149">Вам не нужно добавлять глобальные ключевые слова, которые применяются во всех статьях, так как они управляются в другом месте.</span><span class="sxs-lookup"><span data-stu-id="a473a-149">You don't need to add global keywords that apply to all articles, as those are managed elsewhere.</span></span> 
   
5. <span data-ttu-id="a473a-150">Завершив редактирование статьи, прокрутите вниз и выберите **"Предложить изменение файла".**</span><span class="sxs-lookup"><span data-stu-id="a473a-150">When you've completed your article edits, scroll down and select **Propose file change**.</span></span>

6. <span data-ttu-id="a473a-151">На следующей странице выберите **"Создать** запрос на оттягивать", чтобы объединить автоматически созданную ветвь с "master".</span><span class="sxs-lookup"><span data-stu-id="a473a-151">On the next page, select **Create pull request** to merge your automatically created branch into 'master.'</span></span>

7. <span data-ttu-id="a473a-152">Повторите вышеперечисленные действия для следующей статьи, которая будет изменена.</span><span class="sxs-lookup"><span data-stu-id="a473a-152">Repeat the steps above for the next article you want to edit.</span></span>

## <span data-ttu-id="a473a-153">Переименование или удаление существующей статьи</span><span class="sxs-lookup"><span data-stu-id="a473a-153">Renaming or deleting an existing article</span></span>

<span data-ttu-id="a473a-154">Если изменение переименовет или удалит существующую статью, обязательно добавьте перенаправление.</span><span class="sxs-lookup"><span data-stu-id="a473a-154">If your change will rename or delete an existing article, be sure to add a redirect.</span></span> <span data-ttu-id="a473a-155">Таким образом, все, у кого есть ссылка на существующую статью, по-прежнему будут в правильном месте.</span><span class="sxs-lookup"><span data-stu-id="a473a-155">That way, anyone with a link to the existing article will still end up in the right place.</span></span> <span data-ttu-id="a473a-156">Перенаправление управляется .openpublishing.redirection.jsв файле в корне репо.</span><span class="sxs-lookup"><span data-stu-id="a473a-156">Redirects are managed by the .openpublishing.redirection.json file in the root of the repo.</span></span>

<span data-ttu-id="a473a-157">Чтобы добавить перенаправление в .openpublishing.redirection.js, добавьте запись в `redirections` массив:</span><span class="sxs-lookup"><span data-stu-id="a473a-157">To add a redirect to .openpublishing.redirection.json, add an entry to the `redirections` array:</span></span>

```json
{
    "redirections": [
        {
            "source_path": "hololens/old-article.md",
            "redirect_url": "new-article#section-about-old-topic",
            "redirect_document_id": false
        },
```

- <span data-ttu-id="a473a-158">Это `source_path` относительный путь репозитория к удаляемой старой статье.</span><span class="sxs-lookup"><span data-stu-id="a473a-158">The `source_path` is the relative repository path to the old article that you're removing.</span></span> <span data-ttu-id="a473a-159">Убедитесь, что путь начинается и `mixed-reality-docs` `.md` заканчивается.</span><span class="sxs-lookup"><span data-stu-id="a473a-159">Be sure the path starts with `mixed-reality-docs` and ends with `.md`.</span></span>

- <span data-ttu-id="a473a-160">Это `redirect_url` относительный общедоступный URL-адрес из старой статьи в новую.</span><span class="sxs-lookup"><span data-stu-id="a473a-160">The `redirect_url` is the relative public URL from the old article to the new article.</span></span> <span data-ttu-id="a473a-161">Убедитесь, что этот **URL-адрес** не содержит или, так как он ссылается на общедоступный `mixed-reality-docs` `.md` URL-адрес, а не путь к репозиторию.</span><span class="sxs-lookup"><span data-stu-id="a473a-161">Be sure that this URL **doesn't** contain `mixed-reality-docs` or `.md`, as it refers to the public URL and not the repository path.</span></span> <span data-ttu-id="a473a-162">Ссылка на раздел в новой статье `#section` разрешена.</span><span class="sxs-lookup"><span data-stu-id="a473a-162">Linking to a section within the new article using `#section` is allowed.</span></span> <span data-ttu-id="a473a-163">При необходимости можно также использовать абсолютный путь к другому сайту.</span><span class="sxs-lookup"><span data-stu-id="a473a-163">You can also use an absolute path to another site here, if necessary.</span></span>

- `redirect_document_id` <span data-ttu-id="a473a-164">указывает, хотите ли вы сохранить ИД документа из предыдущего файла.</span><span class="sxs-lookup"><span data-stu-id="a473a-164">indicates whether you would like to keep the document ID from the previous file.</span></span> <span data-ttu-id="a473a-165">Значение по `false` умолчанию: .</span><span class="sxs-lookup"><span data-stu-id="a473a-165">The default is `false`.</span></span> <span data-ttu-id="a473a-166">Используйте, `true` если вы хотите сохранить значение `ms.documentid` атрибута из перенаправленной статьи.</span><span class="sxs-lookup"><span data-stu-id="a473a-166">Use `true` if you want to preserve the `ms.documentid` attribute value from the redirected article.</span></span> <span data-ttu-id="a473a-167">Если сохранить ИД документа, данные, такие как представления страниц и ранжирование, будут перенесены в целевую статью.</span><span class="sxs-lookup"><span data-stu-id="a473a-167">If you preserve the document ID, data, such as page views and rankings, will be transferred to the target article.</span></span> <span data-ttu-id="a473a-168">Это необходимо, если перенаправление в основном связано с переименованием, а не указателем на другую статью, в которую распространяется только часть одного и того же содержимого.</span><span class="sxs-lookup"><span data-stu-id="a473a-168">Do this if the redirect is primarily a rename, and not a pointer to different article that only covers some of the same content.</span></span>

<span data-ttu-id="a473a-169">При добавлении перенаправления также удалите старый файл.</span><span class="sxs-lookup"><span data-stu-id="a473a-169">If you add a redirect, be sure to delete the old file as well.</span></span>

## <span data-ttu-id="a473a-170">Создание новой статьи</span><span class="sxs-lookup"><span data-stu-id="a473a-170">Creating a new article</span></span>

<span data-ttu-id="a473a-171">Используйте следующий рабочий процесс \*\* для создания новых статей в репозитарии документации через GitHub в веб-браузере:</span><span class="sxs-lookup"><span data-stu-id="a473a-171">Use the following workflow to *create new articles* in the documentation repo via GitHub in a web browser:</span></span>

1. <span data-ttu-id="a473a-172">Создайте разветвную ветвь MicrosoftDocs/mixed-reality \*\*\*\* 'master' (с помощью кнопки "Висяк" в правом верхнем направлении).</span><span class="sxs-lookup"><span data-stu-id="a473a-172">Create a fork off the MicrosoftDocs/mixed-reality 'master' branch (using the **Fork** button in the top right).</span></span>

   ![Разветвить ветвь master.](images/forkbranch.png)
   
2. <span data-ttu-id="a473a-174">В папке "mixed-reality-docs" выберите "Создать **новый** файл" в правом верхнем оке.</span><span class="sxs-lookup"><span data-stu-id="a473a-174">In the "mixed-reality-docs" folder, select **Create new file** in the top right.</span></span>

3. <span data-ttu-id="a473a-175">Создайте имя страницы для статьи (вместо пробелов используйте дефис и не используйте знаки препинания или апострофы) и примените ".md"</span><span class="sxs-lookup"><span data-stu-id="a473a-175">Create a page name for the article (use hyphens instead of spaces and don't use punctuation or apostrophes) and append ".md"</span></span>

   ![Назовите новую страницу.](images/newpagetitle.png)
   
   >[!IMPORTANT]
   ><span data-ttu-id="a473a-177">Убедитесь, что вы создали новую статью из папки "mixed-reality-docs".</span><span class="sxs-lookup"><span data-stu-id="a473a-177">Make sure you create the new article from within the "mixed-reality-docs" folder.</span></span> <span data-ttu-id="a473a-178">Это можно подтвердить, проверив наличие "/mixed-reality-docs/" в новой строке имени файла.</span><span class="sxs-lookup"><span data-stu-id="a473a-178">You can confirm this by checking for "/mixed-reality-docs/" in the new file name line.</span></span>

4. <span data-ttu-id="a473a-179">В верхней части новой страницы добавьте следующий блок метаданных:</span><span class="sxs-lookup"><span data-stu-id="a473a-179">At the top of your new page, add the following metadata block:</span></span>

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

5. <span data-ttu-id="a473a-180">Заполните соответствующие поля метаданных в соответствии с инструкциями в [разделе выше.](#editing-an-existing-article)</span><span class="sxs-lookup"><span data-stu-id="a473a-180">Fill in the relevant metadata fields per the instructions in the [section above](#editing-an-existing-article).</span></span>

6. <span data-ttu-id="a473a-181">Напишите содержимое статьи, используя [основы Markdown.](#markdown-basics)</span><span class="sxs-lookup"><span data-stu-id="a473a-181">Write article content using [Markdown basics](#markdown-basics).</span></span>

7. <span data-ttu-id="a473a-182">Добавьте раздел в нижней части статьи со ссылками `## See also` на другие важные статьи.</span><span class="sxs-lookup"><span data-stu-id="a473a-182">Add a `## See also` section at the bottom of the article with links to other relevant articles.</span></span>

8. <span data-ttu-id="a473a-183">По завершению выберите **"Зафиксировать новый файл".**</span><span class="sxs-lookup"><span data-stu-id="a473a-183">When finished, select **Commit new file**.</span></span>

9. <span data-ttu-id="a473a-184">Выберите **"Новый запрос** на оттягивать" и объединяйте ветвь "master" вашего ветвь разветвлива в MicrosoftDocs/mixed-reality 'master' (убедитесь, что стрелка правильно наведет указатель).</span><span class="sxs-lookup"><span data-stu-id="a473a-184">Select **New pull request** and merge your fork's 'master' branch into MicrosoftDocs/mixed-reality 'master' (make sure the arrow is pointing the correct way).</span></span>

   ![Создание запроса на оттягивать из висяча в MicrosoftDocs/mixed-reality](images/pr-to-master.png)

## <span data-ttu-id="a473a-186">Основы Markdown</span><span class="sxs-lookup"><span data-stu-id="a473a-186">Markdown basics</span></span>

<span data-ttu-id="a473a-187">Следующие ресурсы помогут вам узнать, как редактировать документацию с помощью языка Markdown:</span><span class="sxs-lookup"><span data-stu-id="a473a-187">The following resources will help you learn how to edit documentation using the Markdown language:</span></span>

- [<span data-ttu-id="a473a-188">Основы Markdown</span><span class="sxs-lookup"><span data-stu-id="a473a-188">Markdown basics</span></span>](https://help.github.com/articles/basic-writing-and-formatting-syntax/)
- [<span data-ttu-id="a473a-189">Дополнительные ресурсы для написания Markdown для docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a473a-189">Additional resources for writing Markdown for docs.microsoft.com</span></span>](https://docs.microsoft.com/contribute/how-to-write-use-markdown)

### <span data-ttu-id="a473a-190">Добавление таблиц</span><span class="sxs-lookup"><span data-stu-id="a473a-190">Adding tables</span></span>

<span data-ttu-id="a473a-191">Из-за docs.microsoft.com стилей они не будут иметь границ или пользовательских стилей, даже если вы попытались влиять на CSS.</span><span class="sxs-lookup"><span data-stu-id="a473a-191">Because of the way docs.microsoft.com styles tables, they won’t have borders or custom styles, even if you try inline CSS.</span></span> <span data-ttu-id="a473a-192">Он будет работать в течение короткого периода времени, но в конечном итоге платформа утери стиля из таблицы.</span><span class="sxs-lookup"><span data-stu-id="a473a-192">It will appear to work for a short period of time, but eventually the platform will strip the styling out of the table.</span></span> <span data-ttu-id="a473a-193">Поэтому запланируйте заранее и сохраняйте простоты таблиц.</span><span class="sxs-lookup"><span data-stu-id="a473a-193">So plan ahead and keep your tables simple.</span></span> <span data-ttu-id="a473a-194">[Вот сайт, который упрощает таблицы Markdown.](https://www.tablesgenerator.com/markdown_tables)</span><span class="sxs-lookup"><span data-stu-id="a473a-194">[Here’s a site that makes Markdown tables easy](https://www.tablesgenerator.com/markdown_tables).</span></span>

<span data-ttu-id="a473a-195">Расширение [Docs Markdown для Visual Studio Кода](https://docs.microsoft.com/teamblog/docs-extension) также упрощает генерацию таблиц, если вы используете Visual Studio Code (см. [ниже)](#using-visual-studio-code) для редактирования документации.</span><span class="sxs-lookup"><span data-stu-id="a473a-195">The [Docs Markdown Extension for Visual Studio Code](https://docs.microsoft.com/teamblog/docs-extension) also makes table generation easy if you're using [Visual Studio Code (see below)](#using-visual-studio-code) to edit the documentation.</span></span>

### <span data-ttu-id="a473a-196">Добавление изображений</span><span class="sxs-lookup"><span data-stu-id="a473a-196">Adding images</span></span>

<span data-ttu-id="a473a-197">Вам потребуется отправить изображения в папку "mixed-reality-docs/images" в репо, а затем соответствующим образом ссылаться на них в статье.</span><span class="sxs-lookup"><span data-stu-id="a473a-197">You’ll need to upload your images to the "mixed-reality-docs/images" folder in the repo, and then reference them appropriately in the article.</span></span> <span data-ttu-id="a473a-198">Изображения будут автоматически показываться в полном размере, что означает, что большие изображения заполнят всю ширину статьи.</span><span class="sxs-lookup"><span data-stu-id="a473a-198">Images will automatically show up at full-size, which means large images will fill the entire width of the article.</span></span> <span data-ttu-id="a473a-199">Перед отправкой мы рекомендуем предварительно назлать размер ваших изображений.</span><span class="sxs-lookup"><span data-stu-id="a473a-199">We recommend pre-sizing your images before uploading them.</span></span> <span data-ttu-id="a473a-200">Рекомендуемая ширина составляет от 600 до 700 пикселей, но ее размер должен быть вверх или вниз, если это плотность экрана или доля снимка экрана соответственно.</span><span class="sxs-lookup"><span data-stu-id="a473a-200">The recommended width is between 600 and 700 pixels, though you should size up or down if it’s a dense screenshot or a fraction of a screenshot, respectively.</span></span>

>[!IMPORTANT]
><span data-ttu-id="a473a-201">Перед объединением вы можете отправить изображения только в развивной репо.</span><span class="sxs-lookup"><span data-stu-id="a473a-201">You can only upload images to your forked repo before merging.</span></span> <span data-ttu-id="a473a-202">Поэтому если вы планируете добавить изображения в статью, вам потребуется сначала использовать [код Visual Studio,](#using-visual-studio-code) чтобы добавить изображения в папку изображений вашего висяча или убедиться, что вы сделали следующее в веб-браузере:</span><span class="sxs-lookup"><span data-stu-id="a473a-202">So, if you plan on adding images to an article, you'll need to [use Visual Studio Code](#using-visual-studio-code) to add the images to your fork's "images" folder first or make sure you've done the following in a web browser:</span></span>
>
>1. <span data-ttu-id="a473a-203">Forked the MicrosoftDocs/mixed-reality repo.</span><span class="sxs-lookup"><span data-stu-id="a473a-203">Forked the MicrosoftDocs/mixed-reality repo.</span></span>
>2. <span data-ttu-id="a473a-204">Изменена статья в вашей ветвь.</span><span class="sxs-lookup"><span data-stu-id="a473a-204">Edited the article in your fork.</span></span>
>3. <span data-ttu-id="a473a-205">Добавлены изображения, на которые вы ссылаетесь в своей статье, в папку "mixed-reality-docs/images" в вашем висячем тексте.</span><span class="sxs-lookup"><span data-stu-id="a473a-205">Uploaded the images you're referencing in your article to the "mixed-reality-docs/images" folder in your fork.</span></span>
>4. <span data-ttu-id="a473a-206">Создан запрос **на оттягку** для объединения ветвь MicrosoftDocs/mixed-reality 'master'.</span><span class="sxs-lookup"><span data-stu-id="a473a-206">Created a **pull request** to merge your fork into the MicrosoftDocs/mixed-reality 'master' branch.</span></span>
>
><span data-ttu-id="a473a-207">Чтобы узнать, как настроить собственный репо, следуйте инструкциям по [созданию новой статьи.](#creating-a-new-article)</span><span class="sxs-lookup"><span data-stu-id="a473a-207">To learn how to set up your own forked repo, follow the instructions for [creating a new article](#creating-a-new-article).</span></span>

## <span data-ttu-id="a473a-208">Предварительный просмотр работы</span><span class="sxs-lookup"><span data-stu-id="a473a-208">Previewing your work</span></span>

<span data-ttu-id="a473a-209">При редактировании в GitHub с помощью веб-браузера можно выбрать вкладку "Предварительный просмотр" в верхней части страницы, чтобы просмотреть свою работу, прежде чем примесить ее. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a473a-209">While editing in GitHub via a web browser, you can select the **Preview** tab near the top of the page to preview your work before committing.</span></span> 

>[!NOTE]
><span data-ttu-id="a473a-210">Предварительный просмотр изменений в review.docs.microsoft.com доступен только для сотрудников Майкрософт</span><span class="sxs-lookup"><span data-stu-id="a473a-210">Previewing your changes on review.docs.microsoft.com is only available to Microsoft employees</span></span>

<span data-ttu-id="a473a-211">Сотрудники Майкрософт: после того как ваши вклады будут объединены в ветвь "master", вы можете просмотреть содержимое, прежде чем оно будет открыто https://review.docs.microsoft.com/hololens?branch=master на сайте .</span><span class="sxs-lookup"><span data-stu-id="a473a-211">Microsoft employees: once your contributions have been merged into the 'master' branch, you can review the content before it goes public at https://review.docs.microsoft.com/hololens?branch=master.</span></span> <span data-ttu-id="a473a-212">Найдите статью с помощью осодержимого в левом столбце.</span><span class="sxs-lookup"><span data-stu-id="a473a-212">Find your article using the table of contents in the left column.</span></span>

## <span data-ttu-id="a473a-213">Редактирование в браузере и редактирование с помощью настольного клиента</span><span class="sxs-lookup"><span data-stu-id="a473a-213">Editing in the browser vs. editing with a desktop client</span></span>

<span data-ttu-id="a473a-214">Редактирование в браузере — это самый простой способ внести быстрые изменения, однако есть несколько недостатков:</span><span class="sxs-lookup"><span data-stu-id="a473a-214">Editing in the browser is the easiest way to make quick changes, however, there are a few disadvantages:</span></span>

- <span data-ttu-id="a473a-215">Проверка орфографии не проверяется.</span><span class="sxs-lookup"><span data-stu-id="a473a-215">You don't get spell-check.</span></span>
- <span data-ttu-id="a473a-216">Вы не получаете никаких интеллектуальных ссылок на другие статьи (необходимо вручную ввести имя файла этой статьи).</span><span class="sxs-lookup"><span data-stu-id="a473a-216">You don't get any smart-linking to other articles (you have to manually type the article's filename).</span></span>
- <span data-ttu-id="a473a-217">Отправка изображений и справочных изображений может быть очень трудной.</span><span class="sxs-lookup"><span data-stu-id="a473a-217">It can be a hassle to upload and reference images.</span></span>

<span data-ttu-id="a473a-218">Если вы не хотите решать эти проблемы, используйте настольный клиент, например [](#useful-extensions) [Visual Studio Code,](https://code.visualstudio.com/) с несколькими полезными расширениями при их использовании.</span><span class="sxs-lookup"><span data-stu-id="a473a-218">If you'd rather not deal with these issues, use a desktop client like [Visual Studio Code](https://code.visualstudio.com/) with a couple [helpful extensions](#useful-extensions) when contributing.</span></span>

## <span data-ttu-id="a473a-219">Использование Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="a473a-219">Using Visual Studio Code</span></span>

<span data-ttu-id="a473a-220">По причинам, перечисленным [выше,](#editing-in-the-browser-vs-editing-with-a-desktop-client)можно использовать настольный клиент для редактирования документации, а не веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="a473a-220">For the reasons listed [above](#editing-in-the-browser-vs-editing-with-a-desktop-client), you may prefer using a desktop client to edit documentation instead of a web browser.</span></span> <span data-ttu-id="a473a-221">Мы рекомендуем использовать [Visual Studio code.](https://code.visualstudio.com/)</span><span class="sxs-lookup"><span data-stu-id="a473a-221">We recommend using [Visual Studio Code](https://code.visualstudio.com/).</span></span>

### <span data-ttu-id="a473a-222">Настройка</span><span class="sxs-lookup"><span data-stu-id="a473a-222">Setup</span></span>

<span data-ttu-id="a473a-223">Выполните следующие действия, чтобы настроить Visual Studio code для работы с этим репо:</span><span class="sxs-lookup"><span data-stu-id="a473a-223">Follow these steps to configure Visual Studio Code to work with this repo:</span></span>

1. <span data-ttu-id="a473a-224">В веб-браузере:</span><span class="sxs-lookup"><span data-stu-id="a473a-224">In a web browser:</span></span>
    1. <span data-ttu-id="a473a-225">Установите [Git для компьютера.](https://git-scm.com/downloads)</span><span class="sxs-lookup"><span data-stu-id="a473a-225">Install [Git for your PC](https://git-scm.com/downloads).</span></span>
    2. <span data-ttu-id="a473a-226">Установите [Visual Studio кода.](https://code.visualstudio.com/)</span><span class="sxs-lookup"><span data-stu-id="a473a-226">Install [Visual Studio Code](https://code.visualstudio.com/).</span></span>
    3. <span data-ttu-id="a473a-227">[Fork MicrosoftDocs/mixed-reality](#creating-a-new-article) if you haven't already.</span><span class="sxs-lookup"><span data-stu-id="a473a-227">[Fork MicrosoftDocs/mixed-reality](#creating-a-new-article) if you haven't already.</span></span>
    4. <span data-ttu-id="a473a-228">В висяке выберите клонирование или **скачайте** и скопируйте URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a473a-228">In your fork, select **Clone or download** and copy the URL.</span></span>
2. <span data-ttu-id="a473a-229">Создайте локальный клон висяча в Visual Studio Code:</span><span class="sxs-lookup"><span data-stu-id="a473a-229">Create a local clone of your fork in Visual Studio Code:</span></span>
    1. <span data-ttu-id="a473a-230">В меню **"Вид"** выберите **"Палитра команд".**</span><span class="sxs-lookup"><span data-stu-id="a473a-230">From the **View** menu, select **Command Palette**.</span></span>
    2. <span data-ttu-id="a473a-231">Введите "Git: Clone".</span><span class="sxs-lookup"><span data-stu-id="a473a-231">Type "Git: Clone."</span></span>
    3. <span data-ttu-id="a473a-232">В paste the URL-адрес, который вы скопировали.</span><span class="sxs-lookup"><span data-stu-id="a473a-232">Paste the URL you copied.</span></span>
    4. <span data-ttu-id="a473a-233">Выберите место сохранения клона на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a473a-233">Choose where to save the clone on your PC.</span></span>
    5. <span data-ttu-id="a473a-234">Выберите **"Открыть репо"** во всплывающее ок.</span><span class="sxs-lookup"><span data-stu-id="a473a-234">Select **Open repo** in the pop-up.</span></span>

### <span data-ttu-id="a473a-235">Документация по редактированию</span><span class="sxs-lookup"><span data-stu-id="a473a-235">Editing documentation</span></span>

<span data-ttu-id="a473a-236">Используйте следующий рабочий процесс для внесения изменений в документацию с Visual Studio Code:</span><span class="sxs-lookup"><span data-stu-id="a473a-236">Use the following workflow to make changes to the documentation with Visual Studio Code:</span></span>

>[!NOTE]
><span data-ttu-id="a473a-237">Все инструкции [по](#editing-an-existing-article) [](#creating-a-new-article) редактированию и созданию статей, а также основные принципы редактирования [Markdown](#markdown-basics),, начиная с выше, применимы и при использовании Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="a473a-237">All the guidance for [editing](#editing-an-existing-article) and [creating](#creating-a-new-article) articles, and the [basics of editing Markdown](#markdown-basics), from above applies when using Visual Studio Code as well.</span></span>

1. <span data-ttu-id="a473a-238">Убедитесь, что клонированный висяк находится в курсе официального репо.</span><span class="sxs-lookup"><span data-stu-id="a473a-238">Make sure your cloned fork is up to date with the official repo.</span></span>

   1. <span data-ttu-id="a473a-239">В веб-браузере создайте запрос на оттягивать, чтобы синхронизировать недавние изменения от других участников в MicrosoftDocs/mixed-reality 'master' для вашего висячего (убедитесь, что стрелка указатель на правильный путь).</span><span class="sxs-lookup"><span data-stu-id="a473a-239">In a web browser, create a pull request to sync recent changes from other contributors in MicrosoftDocs/mixed-reality 'master' to your fork (make sure the arrow is pointing the right way).</span></span>
      
      ![Синхронизация изменений из MicrosoftDocs/mixed-reality в вашем висяке](images/sync-repos.png)
      
   2. <span data-ttu-id="a473a-241">В Visual Studio code выберите кнопку синхронизации, чтобы синхронизировать обновленный висяк с локальным клоном.</span><span class="sxs-lookup"><span data-stu-id="a473a-241">In Visual Studio Code, select the sync button to sync your freshly updated fork to the local clone.</span></span>
      
      ![Щелкните изображение кнопки синхронизации](images/sync-clone.png)
      
2. <span data-ttu-id="a473a-243">Создание или редактирование статей в клонированном репо с помощью Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="a473a-243">Create or edit articles in your cloned repo using Visual Studio Code.</span></span>

   1. <span data-ttu-id="a473a-244">Редактировать одну или несколько статей (при необходимости добавьте изображения в папку "изображения").</span><span class="sxs-lookup"><span data-stu-id="a473a-244">Edit one or more articles (add images to “images” folder if necessary).</span></span>
   
   2. <span data-ttu-id="a473a-245">**Сохраните** изменения в **проводнике.**</span><span class="sxs-lookup"><span data-stu-id="a473a-245">**Save** changes in **Explorer**.</span></span>
      
      ![Выберите "Сохранить все" в проводнике](images/explorer-save.png)
      
   3. <span data-ttu-id="a473a-247">**Зафиксировать все** изменения в **source Control** (запишите сообщение фиксации при запросе).</span><span class="sxs-lookup"><span data-stu-id="a473a-247">**Commit all** changes in **Source Control** (write commit message when prompted).</span></span>
      
   4. <span data-ttu-id="a473a-248">Выберите **кнопку синхронизации,** чтобы синхронизировать изменения с началом (ветвь на GitHub).</span><span class="sxs-lookup"><span data-stu-id="a473a-248">Select the **sync** button to sync your changes back to origin (your fork on GitHub).</span></span>
      
      ![Нажмите кнопку синхронизации](images/sync-back.png)
      
3. <span data-ttu-id="a473a-250">В веб-браузере создайте запрос на оттягивать, чтобы синхронизировать новые изменения в вашем висячем ответе на MicrosoftDocs/mixed-reality 'master' (убедитесь, что стрелка правильно наведет указатель).</span><span class="sxs-lookup"><span data-stu-id="a473a-250">In a web browser, create a pull request to sync new changes in your fork back to MicrosoftDocs/mixed-reality 'master' (make sure the arrow is pointing the correct way).</span></span>

   ![Создание запроса на оттягивать из висяча в MicrosoftDocs/mixed-reality](images/pr-to-master.png)

### <span data-ttu-id="a473a-252">Полезные расширения</span><span class="sxs-lookup"><span data-stu-id="a473a-252">Useful extensions</span></span>

<span data-ttu-id="a473a-253">При редактировании документации Visual Studio полезны следующие расширения кода:</span><span class="sxs-lookup"><span data-stu-id="a473a-253">The following Visual Studio Code extensions are useful when editing documentation:</span></span>

- <span data-ttu-id="a473a-254">[Расширение Docs Markdown для Visual Studio кода](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) . Используйте **ALT+M,** чтобы отвести меню параметров для работы с docs, например:</span><span class="sxs-lookup"><span data-stu-id="a473a-254">[Docs Markdown Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) - Use **Alt+M** to bring up a menu of docs authoring options like:</span></span>
   - <span data-ttu-id="a473a-255">Поиск и справочные изображения, которые вы загрузили.</span><span class="sxs-lookup"><span data-stu-id="a473a-255">Search and reference images you've uploaded.</span></span>
   - <span data-ttu-id="a473a-256">Добавьте форматирование, например списки, таблицы и вызовы для конкретных документы, `>[!NOTE]` например.</span><span class="sxs-lookup"><span data-stu-id="a473a-256">Add formatting like lists, tables, and docs-specific call-outs like `>[!NOTE]`.</span></span>
   - <span data-ttu-id="a473a-257">Поиск и ссылка на внутренние ссылки и закладки (ссылки на определенные разделы на странице).</span><span class="sxs-lookup"><span data-stu-id="a473a-257">Search and reference internal links and bookmarks (links to specific sections within a page).</span></span>
   - <span data-ttu-id="a473a-258">Выделяются ошибки форматирования (наведите указатель мыши на ошибку, чтобы узнать больше).</span><span class="sxs-lookup"><span data-stu-id="a473a-258">Formatting errors are highlighted (hover your mouse over the error to learn more).</span></span>
- <span data-ttu-id="a473a-259">[Проверка орфографии кода—](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) будут подчеркивается слова с ошибками; Щелкните правой кнопкой мыши неправильное слово, чтобы изменить его или сохранить в словаре.</span><span class="sxs-lookup"><span data-stu-id="a473a-259">[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) - misspelled words will be underlined; right-click on a misspelled word to change it or save it to the dictionary.</span></span>
