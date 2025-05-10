<div class="Box-sc-g0xbh4-0 eoaCFS js-snippet-clipboard-copy-unpositioned undefined" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div dir="rtl"><markdown-accessiblity-table data-catalyst=""><table>
  <thead>
  <tr>
  <th>lab</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div dir="rtl"><table>
  <thead>
  <tr>
  <th>title</th>
  <th>status</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div dir="rtl">استخدام هندسة التلقين في تطبيقك</div></td>
  <td><div dir="rtl">stale</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استخدام هندسة التلقين في تطبيقك</h1><a id="user-content-استخدام-هندسة-التلقين-في-تطبيقك" class="anchor" aria-label="Permalink: استخدام هندسة التلقين في تطبيقك" href="#استخدام-هندسة-التلقين-في-تطبيقك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">تؤثر كيفية تشكيل المطورين لمطالبتهم بشكل كبير على كيفية استجابة نموذج الذكاء الاصطناعي التوليدي عند استخدام خدمة Azure OpenAI. يمكن لنماذج Azure OpenAI تخصيص المحتوى وتنسيقه، إذا طلب ذلك بطريقة واضحة وموجزة. في هذا النموذج، ستتعلم كيف تساعد المطالبات المختلفة للمحتوى المماثل في تشكيل استجابة نموذج الذكاء الاصطناعي لتلبية متطلباتك بشكل أفضل.</p>
<p dir="rtl">في سيناريو هذا التدريب، سوف تقوم بدور مطور برامج يعمل على حملة إعلانية عن الحياة البرية. أنت تستكشف كيفية استخدام الذكاء الاصطناعي التوليدي لتحسين رسائل البريد الإلكتروني الإعلانية وتصنيف المقالات التي قد تنطبق على فريقك. يمكن تطبيق تقنيات هندسة التلقين المستخدمة في التدريب بشكل مماثل لمجموعة متنوعة من حالات الاستخدام.</p>
<p dir="rtl">سيستغرق هذا التدريب حوالي <strong>30</strong> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توفير مورد Azure OpenAI</h2><a id="user-content-توفير-مورد-azure-openai" class="anchor" aria-label="Permalink: توفير مورد Azure OpenAI" href="#توفير-مورد-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">إذا لم يكن لديك موردًا بالفعل، يمكنك توفير مورد Azure OpenAI في اشتراك Azure الخاص بك.</p>
<ol dir="rtl">
<li>
<p dir="rtl">سجّل الدخول إلى <strong>Azure portal</strong> من <code>https://portal.azure.com</code>.</p>
</li>
<li>
<p dir="rtl">إنشاء مورد <strong>Azure OpenAI</strong> بالإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>اشتراك</strong>: <em>حدد اشتراك Azure الذي جرت الموافقة عليه للوصول إلى خدمة Azure OpenAI</em></li>
<li><strong>مجموعة الموارد</strong>: <em>اختيار مجموعة موارد أو إنشاءها</em></li>
<li><strong>المنطقة</strong>: <em>إجراء اختيار <strong>عشوائي</strong> من أي من المناطق التالية</em>*
<ul dir="rtl">
<li>شرق الولايات المتحدة</li>
<li>East US 2</li>
<li>وسط شمال الولايات المتحدة</li>
<li>South Central US</li>
<li>منطقة السويد الوسطى</li>
<li>غرب الولايات المتحدة</li>
<li>غرب الولايات المتحدة الأمريكية 3</li>
</ul>
</li>
<li><strong>الاسم</strong>: <em>اسم فريد من اختيارك</em></li>
<li><strong>مستوى التسعير</strong>: قياسي S0</li>
</ul>
<blockquote>
<p dir="rtl">* موارد Azure OpenAI مقيدة بالحصص النسبية الإقليمية. تتضمن المناطق المدرجة الحصة النسبية الافتراضية لنوع (أنواع) النموذج المستخدمة في هذا التمرين. يؤدي اختيار منطقة عشوائيًا إلى تقليل مخاطر وصول منطقة واحدة إلى حد الحصة النسبية في السيناريوهات التي تشارك فيها اشتراكًا مع مستخدمين آخرين. في حالة الوصول إلى حد الحصة النسبية لاحقًا في التمرين، هناك احتمال أنك قد تحتاج إلى إنشاء مورد آخر في منطقة مختلفة.</p>
</blockquote>
</li>
<li>
<p dir="rtl">يُرجى الانتظار لاكتمال التوزيع. ثم انتقل إلى مورد Azure OpenAI الموزّع في مدخل Microsoft Azure.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توزيع النموذج</h2><a id="user-content-توزيع-النموذج" class="anchor" aria-label="Permalink: توزيع النموذج" href="#توزيع-النموذج"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">يوفر Azure بوابة على الويب يسمى <strong>بوابة Azure AI Foundry</strong>، والتي يمكنك استخدامها لنشر النماذج وإدارتها واستكشافها. ستبدأ استكشافك لـ Azure OpenAI باستخدام بوابة Azure AI Foundry لنشر نموذج.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: أثناء استخدام بوابة Azure AI Foundry، قد يتم عرض مربعات رسائل تقترح عليك تنفيذ مهام. يمكنك إغلاق هذه الخطوات واتباع الخطوات الواردة في هذا التمرين.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">في بوابة Azure، في صفحة <strong>نظرة عامة</strong> لمورد Azure OpenAI الخاص بك، مرّر لأسفل إلى قسم <strong>بدء الاستخدام</strong> وحدد الزر للانتقال إلى <strong>بوابة AI Foundry</strong> (المعروفة سابقًا باسم AI Studio).</p>
</li>
<li>
<p dir="rtl">في بوابة Azure AI Foundry، في الجزء الموجود على اليسار، حدد صفحة <strong>عمليات النشر</strong> واعرض عمليات نشر النموذج الحالية لديك. إذا لم يكن لديك واحد بالفعل، أنشئ نشرًا جديدًا لنموذج <strong>gpt-4o</strong> باستخدام الإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>اسم التوزيع</strong>: <em>اسم فريد من اختيارك</em></li>
<li><strong>النموذج</strong>: gpt-4</li>
<li><strong>إصدار النموذج</strong>: <em>استخدام الإصدار الافتراضي</em></li>
<li><strong>نوع التوزيع</strong>: قياسي</li>
<li><strong>حد معدل الرموز المميزة في الدقيقة</strong>: 5K*</li>
<li><strong>عامل تصفية المحتوى</strong>: افتراضية</li>
<li><strong>تمكين الحصة النسبية الديناميكية</strong>: معطّل</li>
</ul>
<blockquote>
<p dir="rtl">*الحد الأقصى لمعدل 5000 رمز مميز في الدقيقة هو أكثر من كاف لإكمال هذا التمرين مع ترك سعة للأشخاص الآخرين الذين يستخدمون نفس الاشتراك.</p>
</blockquote>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استكشف تقنيات هندسة التلقين</h2><a id="user-content-استكشف-تقنيات-هندسة-التلقين" class="anchor" aria-label="Permalink: استكشف تقنيات هندسة التلقين" href="#استكشف-تقنيات-هندسة-التلقين"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لنبدأ باستكشاف بعض تقنيات هندسة التلقين في دردشة playground.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في الجزء الجانبي الأيسر، في قسم <strong>البيئات</strong>، حدد صفحة <strong>دردشة</strong>. تتكون صفحة بيئة <strong>الدردشة</strong> من صف من الأزرار ولوحتين رئيسيتين (والتي يمكن ترتيبها من اليمين إلى اليسار أفقيًا، أو من أعلى إلى أسفل عموديًا حسب دقة الشاشة لديك):</p>
<ul dir="rtl">
<li><strong>الإعداد</strong> - يُستخدم لتحديد التوزيع الخاص بك، وتعريف رسالة النظام، وتعيين معلمات للتفاعل مع توزيعك.</li>
<li><strong>محفوظات الدردشة</strong> - تُستخدم لإرسال رسائل الدردشة وعرض الردود.</li>
</ul>
</li>
<li>
<p dir="rtl">في جزء <strong>عمليات التوزيع</strong>، تأكّد من تحديد نشر نموذج gpt-4o الخاص بك.</p>
</li>
<li>
<p dir="rtl">راجع رسالة النظام الافتراضية الموجودة في مربع النص الموجود أسفل التوزيع المحدد مباشرةً، والتي يجب أن تكون <em>أنت مساعد الذكاء الاصطناعي الذي يساعد الأشخاص في العثور على المعلومات.</em></p>
</li>
<li>
<p dir="rtl">في <strong>محفوظات الدردشة</strong>، أرسل الاستعلام التالي:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>What kind of article is this?
---
Severe drought likely in California

Millions of California residents are bracing for less water and dry lawns as drought threatens to leave a large swath of the region with a growing water shortage.

In a remarkable indication of drought severity, officials in Southern California have declared a first-of-its-kind action limiting outdoor water use to one day a week for nearly 8 million residents.

Much remains to be determined about how daily life will change as people adjust to a drier normal. But officials are warning the situation is dire and could lead to even more severe limits later in the year.
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl">توفر الاستجابة وصفاً للمقالة. ومع ذلك، افترض أنك تريد تنسيقاً أكثر تحديداً لتصنيف المقالات.</p>
</li>
<li>
<p dir="rtl">في قسم <strong>إعداد</strong>، قم بتغيير رسالة النظام إلى <code>You are a news aggregator that categorizes news articles.</code></p>
</li>
<li>
<p dir="rtl">في جزء رسالة النظام الجديدة، حدد زر <strong>إضافة قسم</strong>، ثم اختر <strong>أمثلة</strong>. ثم، أضف المثال التالي.</p>
<p dir="rtl"><strong>المستخدم:</strong></p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>What kind of article is this?
---
New York Baseballers Wins Big Against Chicago

New York Baseballers mounted a big 5-0 shutout against the Chicago Cyclones last night, solidifying their win with a 3 run homerun late in the bottom of the 7th inning.

Pitcher Mario Rogers threw 96 pitches with only two hits for New York, marking his best performance this year.

The Chicago Cyclones' two hits came in the 2nd and the 5th innings but were unable to get the runner home to score.
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>Assistant:</strong></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Sports
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="Sports" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">أضف مثالاً آخر باستخدام النص التالي.</p>
<p dir="rtl"><strong>المستخدم:</strong></p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Categorize this article:
---
Joyous moments at the Oscars

The Oscars this past week where quite something!

Though a certain scandal might have stolen the show, this year's Academy Awards were full of moments that filled us with joy and even moved us to tears.
These actors and actresses delivered some truly emotional performances, along with some great laughs, to get us through the winter.

From Robin Kline's history-making win to a full performance by none other than Casey Jensen herself, don't miss tomorrows rerun of all the festivities.
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>Assistant:</strong></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Entertainment
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="Entertainment" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">استخدم زر <strong>تطبيق التغييرات</strong> أسفل مربع نص رسالة النظام في قسم <strong>الإعداد</strong> لحفظ تغييراتك.</p>
</li>
<li>
<p dir="rtl">في قسم <strong>محفوظات الدردشة</strong>، أعد إرسال المطالبة التالية:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>What kind of article is this?
---
Severe drought likely in California

Millions of California residents are bracing for less water and dry lawns as drought threatens to leave a large swath of the region with a growing water shortage.

In a remarkable indication of drought severity, officials in Southern California have declared a first-of-its-kind action limiting outdoor water use to one day a week for nearly 8 million residents.

Much remains to be determined about how daily life will change as people adjust to a drier normal. But officials are warning the situation is dire and could lead to even more severe limits later in the year.
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl">يؤدي الجمع بين رسالة نظام أكثر تحديداً وبعض الأمثلة على الاستعلامات والاستجابات المتوقعة إلى تنسيق متسق للنتائج.</p>
</li>
<li>
<p dir="rtl">قم بتغيير رسالة النظام مرة أخرى إلى القالب الافتراضي، والذي يجب أن يكون <code>You are an AI assistant that helps people find information.</code> بدون أمثلة. ثم، قم بتطبيق التغييرات.</p>
</li>
<li>
<p dir="rtl">في قسم <strong>محفوظات الدردشة</strong>، أرسل المطالبة التالية:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code># 1. Create a list of animals
# 2. Create a list of whimsical names for those animals
# 3. Combine them randomly into a list of 25 animal and name pairs
</code></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl">من المحتمل أن يستجيب النموذج بإجابة لتلبية المطالبة، وتقسيمه إلى قائمة مرقمّة. هذه استجابة مناسبة، ولكن افترض أن ما أردته بالفعل هو أن يكتب النموذج برنامج Python الذي ينفذ المهام التي وصفتها؟</p>
</li>
<li>
<p dir="rtl">قم بتغيير رسالة النظام إلى <code>You are a coding assistant helping write python code.</code> وطبّق التغييرات.</p>
</li>
<li>
<p dir="rtl">أعد إرسال المطالبة التالية إلى النموذج:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code># 1. Create a list of animals
# 2. Create a list of whimsical names for those animals
# 3. Combine them randomly into a list of 25 animal and name pairs
</code></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl">يجب أن يستجيب النموذج بشكل صحيح مع تعليمات python البرمجية التي تفعل ما طلبته التعليقات.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية</h2><a id="user-content-الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية" class="anchor" aria-label="Permalink: الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية" href="#الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن دعونا نستكشف استخدام هندسة التلقين في تطبيق يستخدم SDK لخدمة Azure OpenAI. ستقوم بتطوير تطبيقك باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في مستودع GitHub.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: إذا نسخت بالفعل مستودع <strong>mslearn-openai</strong>، فافتحه في تعليمة Visual Studio البرمجية. وإلا فاتبع هذه الخطوات لاستنساخه إلى بيئة تطويرك.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">ابدأ تشغيل Visual Studio Code.</p>
</li>
<li>
<p dir="rtl">افتح لوحة الأوامر (SHIFT+CTRL+P أو <strong>View</strong> &gt; <strong>Command Palette...</strong>)، ثم نفّذ أمر <strong>Git: Clone</strong> لاستنساخ المستودع <code>https://github.com/MicrosoftLearning/mslearn-openai</code> إلى مجلد محلي (لا يهم أي مجلد تختاره).</p>
</li>
<li>
<p dir="rtl">عند استنساخ المستودع، افتح المجلد في Visual Studio Code.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا عرضت لك Visual Studio Code رسالة منبثقة لمطالبتك بالثقة في التعليمات البرمجية التي تفتحها، فانقر فوق <strong>نعم، أثق في خيار الكُتاب</strong> في النافذة المنبثقة.</p>
</blockquote>
</li>
<li>
<p dir="rtl">انتظر حتى تثبيت ملفات إضافية لدعم مشاريع التعليمات البرمجية C# في المستودع.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: في حالة مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد <strong>ليس الآن</strong>.</p>
</blockquote>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تكوين تطبيقك</h2><a id="user-content-تكوين-تطبيقك" class="anchor" aria-label="Permalink: تكوين تطبيقك" href="#تكوين-تطبيقك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">تم توفير تطبيقات لكل من C# وPython، ويمتلك كلا التطبيقين نفس الوظيفة. أولاً، ستكمل بعض الأجزاء الرئيسية من التطبيق لتمكين استخدام مورد Azure OpenAI الخاص بك مع استدعاءات واجهة برمجة التطبيقات (API) غير المتزامنة.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في تعليمات Visual Studio البرمجية في جزء <strong>المستكشف</strong>، انتقِل إلى المجلد <strong>Labfiles/03-prompt-engineering</strong>، وقم بتوسيع المجلد <strong>CSharp</strong> أو <strong>Python</strong> حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي تريد دمج وظيفة Azure OpenAI فيه.</p>
</li>
<li>
<p dir="rtl">انقر بزر الماوس الأيمن فوق المجلد <strong>CSharp</strong> أو <strong>Python</strong> الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وافتح وحدة طرفية متكاملة. ثم، عليك تثبيت حزمة Azure OpenAI SDK عن طريق تشغيل الأمر المناسب لتفضيل اللغة لديك:</p>
<p dir="rtl"><strong>:#C</strong></p>
</li>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre>dotnet add package Azure.AI.OpenAI <span class="pl-k">--</span>version <span class="pl-c1">2.1</span>.<span class="pl-c1">0</span></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl">:<strong>Python</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre>pip install openai<span class="pl-k">==</span><span class="pl-c1">1.65</span>.<span class="pl-c1">2</span></pre><div class="zeroclipboard-container">

  </div></div>
</li>
<li>
<p dir="rtl">في جزء <strong>مستكشف</strong>، في مجلد <strong>CSharp</strong> أو <strong>Python</strong>، افتح ملف التكوين للغة المفضلة لديك</p>
<ul dir="rtl">
<li><strong>C#</strong>: appsettings.json</li>
<li><strong>Python</strong>: .env</li>
</ul>
</li>
<li>
<p dir="rtl">تحديث قيم التكوين لتشمل:</p>
<ul dir="rtl">
<li><strong>نقطة النهاية</strong> و<strong>مفتاح</strong> من مورد Azure OpenAI الذي أنشأته (متوفر في صفحة <strong>المفاتيح ونقطة النهاية</strong> لمورد Azure OpenAI الخاص بك في مدخل Microsoft Azure)</li>
<li><strong>اسم عملية النشر</strong> الذي حددته لنشر النموذج الخاص بك (متوفر في صفحة <strong>عمليات النشر</strong> في بوابة Azure AI Foundry).</li>
</ul>
</li>
<li>
<p dir="rtl">احفظ ملف التكوين.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI</h2><a id="user-content-أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai" class="anchor" aria-label="Permalink: أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI" href="#أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">أنت الآن جاهز لاستخدام Azure OpenAI SDK لاستهلاك نموذجك الموزع.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في جزء <strong>مستكشف</strong>، في المجلد <strong>CSharp</strong> أو <strong>Python</strong>، افتح ملف التعليمات البرمجية للغة المفضلة لديك، واستبدل التعليق <em><strong>أضف حزمة Azure OpenAI</strong></em> بالتعليمات البرمجية لإضافة مكتبة Azure OpenAI SDK:</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c">// Add Azure OpenAI package</span>
<span class="pl-k">using</span> <span class="pl-s1">Azure</span><span class="pl-kos">.</span><span class="pl-s1">AI</span><span class="pl-kos">.</span><span class="pl-s1">OpenAI</span><span class="pl-kos">;</span>
<span class="pl-k">using</span> <span class="pl-s1">OpenAI</span><span class="pl-kos">.</span><span class="pl-s1">Chat</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>Python</strong>: prompt-engineering.py</p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c"># Add Azure OpenAI package</span>
<span class="pl-k">from</span> <span class="pl-s1">openai</span> <span class="pl-k">import</span> <span class="pl-v">AsyncAzureOpenAI</span></pre><div class="zeroclipboard-container">

  </div></div>
</li>
<li>
<p dir="rtl">في ملف التعليمات البرمجية، ابحث عن التعليق <em><strong>تكوين عميل Azure OpenAI</strong></em>، وأضف التعليمات البرمجية لتكوين عميل Azure OpenAI:</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c">// Configure the Azure OpenAI client</span>
<span class="pl-smi">AzureOpenAIClient</span> <span class="pl-s1">azureClient</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-kos">(</span><span class="pl-k">new</span> <span class="pl-smi">Uri</span><span class="pl-kos">(</span><span class="pl-s1">oaiEndpoint</span><span class="pl-kos">)</span><span class="pl-kos">,</span> <span class="pl-k">new</span> <span class="pl-smi">ApiKeyCredential</span><span class="pl-kos">(</span><span class="pl-s1">oaiKey</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-smi">ChatClient</span> <span class="pl-s1">chatClient</span> <span class="pl-c1">=</span> <span class="pl-s1">azureClient</span><span class="pl-kos">.</span><span class="pl-en">GetChatClient</span><span class="pl-kos">(</span><span class="pl-s1">oaiDeploymentName</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl"><strong>Python</strong>: prompt-engineering.py</p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c"># Configure the Azure OpenAI client</span>
<span class="pl-s1">client</span> <span class="pl-c1">=</span> <span class="pl-en">AsyncAzureOpenAI</span>(
    <span class="pl-s1">azure_endpoint</span> <span class="pl-c1">=</span> <span class="pl-s1">azure_oai_endpoint</span>, 
    <span class="pl-s1">api_key</span><span class="pl-c1">=</span><span class="pl-s1">azure_oai_key</span>,  
    <span class="pl-s1">api_version</span><span class="pl-c1">=</span><span class="pl-s">"2024-02-15-preview"</span>
    )</pre><div class="zeroclipboard-container">
 
  </div></div>
</li>
<li>
<p dir="rtl">في الدالة التي تستدعي نموذج Azure OpenAI، ضمن <em><strong>تنسيق التعليق وإرسال الطلب إلى النموذج</strong></em>، أضف التعليمات البرمجية لتنسيق وإرسال الطلب إلى النموذج.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c">// Format and send the request to the model</span>
<span class="pl-k">var</span> <span class="pl-s1">chatCompletionsOptions</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-smi">ChatCompletionOptions</span><span class="pl-kos">(</span><span class="pl-kos">)</span>
<span class="pl-kos">{</span>
    <span class="pl-s1">Temperature</span> <span class="pl-c1">=</span> <span class="pl-c1">0.7f</span><span class="pl-kos">,</span>
    <span class="pl-s1">MaxOutputTokenCount</span> <span class="pl-c1">=</span> <span class="pl-c1">800</span>
<span class="pl-kos">}</span><span class="pl-kos">;</span>

<span class="pl-c">// Get response from Azure OpenAI</span>
<span class="pl-smi">ChatCompletion</span> <span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-k">await</span> <span class="pl-s1">chatClient</span><span class="pl-kos">.</span><span class="pl-en">CompleteChatAsync</span><span class="pl-kos">(</span>
    <span class="pl-kos">[</span>
        <span class="pl-k">new</span> <span class="pl-smi">SystemChatMessage</span><span class="pl-kos">(</span><span class="pl-s1">systemMessage</span><span class="pl-kos">)</span><span class="pl-kos">,</span>
        <span class="pl-k">new</span> <span class="pl-smi">UserChatMessage</span><span class="pl-kos">(</span><span class="pl-s1">userMessage</span><span class="pl-kos">)</span><span class="pl-kos">,</span>
    <span class="pl-kos">]</span><span class="pl-kos">,</span>
    <span class="pl-s1">chatCompletionsOptions</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl"><strong>Python</strong>: prompt-engineering.py</p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c"># Format and send the request to the model</span>
<span class="pl-s1">messages</span> <span class="pl-c1">=</span>[
    {<span class="pl-s">"role"</span>: <span class="pl-s">"system"</span>, <span class="pl-s">"content"</span>: <span class="pl-s1">system_message</span>},
    {<span class="pl-s">"role"</span>: <span class="pl-s">"user"</span>, <span class="pl-s">"content"</span>: <span class="pl-s1">user_message</span>},
]

<span class="pl-en">print</span>(<span class="pl-s">"<span class="pl-cce">\n</span>Sending request to Azure OpenAI model...<span class="pl-cce">\n</span>"</span>)

<span class="pl-c"># Call the Azure OpenAI model</span>
<span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-k">await</span> <span class="pl-s1">client</span>.<span class="pl-c1">chat</span>.<span class="pl-c1">completions</span>.<span class="pl-c1">create</span>(
    <span class="pl-s1">model</span><span class="pl-c1">=</span><span class="pl-s1">model</span>,
    <span class="pl-s1">messages</span><span class="pl-c1">=</span><span class="pl-s1">messages</span>,
    <span class="pl-s1">temperature</span><span class="pl-c1">=</span><span class="pl-c1">0.7</span>,
    <span class="pl-s1">max_tokens</span><span class="pl-c1">=</span><span class="pl-c1">800</span>
)</pre><div class="zeroclipboard-container">
 
  </div></div>
</li>
<li>
<p dir="rtl">احفظ التغييرات في ملف التعليمة البرمجية.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تشغيل التطبيق الخاص بك</h2><a id="user-content-تشغيل-التطبيق-الخاص-بك" class="anchor" aria-label="Permalink: تشغيل التطبيق الخاص بك" href="#تشغيل-التطبيق-الخاص-بك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن نجح تكوين التطبيق الخاص بك، عليك تشغيله لإرسال طلبك إلى النموذج الخاص بك ومراقبة الاستجابة. ستلاحظ أن الفرق الوحيد بين الخيارات المختلفة هو محتوى المطالبة، وتظل جميع المعلمات الأخرى (مثل عدد الرموز المميزة ودرجة الحرارة) كما هي لكل طلب.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في مجلد اللغة المفضلة لديك، افتح <code>system.txt</code> في Visual Studio Code. لكل من التفاعلات، ستقوم بإدخال <strong>رسالة النظام</strong> في هذا الملف وحفظها. سيتوقف كل تكرار مؤقتاً أولاً لتغيير رسالة النظام.</p>
</li>
<li>
<p dir="rtl">في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.</p>
<ul dir="rtl">
<li><strong>C#:</strong> <code>dotnet run</code></li>
<li><strong>Python</strong>: <code>python prompt-engineering.py</code></li>
</ul>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يمكنك استخدام أيقونة <strong>تكبير حجم اللوحة</strong> (<strong>^</strong>) في شريط أدوات المحطة الطرفية لرؤية المزيد من نص وحدة التحكم.</p>
</blockquote>
</li>
<li>
<p dir="rtl">بالنسبة للتكرار الأول، أدخل المطالبات التالية:</p>
</li>
<p dir="rtl"><strong>رسالة النظام</strong></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>You are an AI assistant
</code></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>Write an intro for a new wildlife Rescue
</code></pre><div class="zeroclipboard-container">

  </div></div>
</li>
<li>
<p dir="rtl">مراقبة المخرجات. ومن المرجح أن ينتج نموذج الذكاء الاصطناعي مقدمة عامة جيدة حول إنقاذ الحياة البرية.</p>
</li>
<li>
<p dir="rtl">بعد ذلك، أدخل المطالبات التالية التي تحدد تنسيقاً للاستجابة:</p>
<p dir="rtl"><strong>رسالة النظام</strong></p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>You are an AI assistant helping to write emails
</code></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Write a promotional email for a new wildlife rescue, including the following: 
- Rescue name is Contoso 
- It specializes in elephants 
- Call for donations to be given at our website
</code></pre><div class="zeroclipboard-container">
 
  </div></div>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: قد تجد أن الكتابة التلقائية في الجهاز الظاهري (VM) لا تعمل بشكل جيد مع المطالبات التي تتكون من عدة أسطر. إذا كانت هذه هي مشكلتك، فانسخ المطالبة بأكملها ثم الصقها في التعليمة البرمجية لـ Visual Studio.</p>
</blockquote>
</li>
<li>
<p dir="rtl">مراقبة المخرجات. في هذه المرة، من المحتمل أن ترى تنسيق رسالة بريد إلكتروني تتضمن الحيوانات المحددة، بالإضافة إلى دعوة للتبرعات.</p>
</li>
<li>
<p dir="rtl">وبعد ذلك، أدخل المطالبات التالية التي تحدد المحتوى بالإضافة إلى ذلك:</p>
<p dir="rtl"><strong>رسالة النظام</strong></p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>You are an AI assistant helping to write emails
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Write a promotional email for a new wildlife rescue, including the following: 
- Rescue name is Contoso 
- It specializes in elephants, as well as zebras and giraffes 
- Call for donations to be given at our website 
Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits.
</code></pre><div class="zeroclipboard-container">

  </div></div>
</li>
<li>
<p dir="rtl">لاحظ النتائج، وشاهد كيفية تغيير البريد الإلكتروني استناداً إلى الإرشادات الواضحة.</p>
</li>
<li>
<p dir="rtl">بعد ذلك، أدخل المطالبات التالية حيث نضيف تفاصيل حول النبرة إلى رسالة النظام:</p>
<p dir="rtl"><strong>رسالة النظام</strong></p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>You are an AI assistant that helps write promotional emails to generate interest in a new business. Your tone is light, chit-chat oriented and you always include at least two jokes.
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Write a promotional email for a new wildlife rescue, including the following: 
- Rescue name is Contoso 
- It specializes in elephants, as well as zebras and giraffes 
- Call for donations to be given at our website 
Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits.
</code></pre><div class="zeroclipboard-container">

  </div></div>
</li>
<li>
<p dir="rtl">مراقبة المخرجات. وفي هذه المرة، من المحتمل أن ترى البريد الإلكتروني بتنسيق مماثل، ولكن بنبرة غير رسمية أكثر بكثير. من المحتمل أن ترى النكات مضمنة!</p>
</li>
<li>
<p dir="rtl">للتكرار النهائي، نحن نبتعد عن إنشاء البريد الإلكتروني واستكشاف <em>السياق الأساسي</em>. هنا يمكنك توفير رسالة نظام بسيطة، وتغيير التطبيق لتوفير السياق الأساسي كبداية لمطالبة المستخدم. وبعد ذلك، سيُلحق التطبيق إدخال المستخدم، واستخراج المعلومات من السياق الأساسي للرد على مطالبة المستخدم.</p>
</li>
<li>
<p dir="rtl">افتح الملف <code>grounding.txt</code> واقرأ بإيجاز السياق الأساسي الذي ستقوم بإدراجه.</p>
</li>
<li>
<p dir="rtl">في تطبيقك مباشرة بعد <em><strong>تنسيق التعليق وإرسال الطلب إلى النموذج</strong></em> وقبل أي تعليمات برمجية موجودة، أضف القصاصة البرمجية التالية لقراءة النص من <code>grounding.txt</code> لزيادة مطالبة المستخدم بالسياق الأساسي.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c">// Format and send the request to the model</span>
<span class="pl-s1">Console</span><span class="pl-kos">.</span><span class="pl-en">WriteLine</span><span class="pl-kos">(</span><span class="pl-s">"<span class="pl-cce">\n</span>Adding grounding context from grounding.txt"</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-smi">string</span> <span class="pl-s1">groundingText</span> <span class="pl-c1">=</span> <span class="pl-s1">System</span><span class="pl-kos">.</span><span class="pl-s1">IO</span><span class="pl-kos">.</span><span class="pl-s1">File</span><span class="pl-kos">.</span><span class="pl-en">ReadAllText</span><span class="pl-kos">(</span><span class="pl-s">"grounding.txt"</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">userMessage</span> <span class="pl-c1">=</span> <span class="pl-s1">groundingText</span> <span class="pl-c1">+</span> <span class="pl-s1">userMessage</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl"><strong>Python</strong>: prompt-engineering.py</p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c"># Format and send the request to the model</span>
<span class="pl-en">print</span>(<span class="pl-s">"<span class="pl-cce">\n</span>Adding grounding context from grounding.txt"</span>)
<span class="pl-s1">grounding_text</span> <span class="pl-c1">=</span> <span class="pl-en">open</span>(<span class="pl-s1">file</span><span class="pl-c1">=</span><span class="pl-s">"grounding.txt"</span>, <span class="pl-s1">encoding</span><span class="pl-c1">=</span><span class="pl-s">"utf8"</span>).<span class="pl-c1">read</span>().<span class="pl-c1">strip</span>()
<span class="pl-s1">user_message</span> <span class="pl-c1">=</span> <span class="pl-s1">grounding_text</span> <span class="pl-c1">+</span> <span class="pl-s1">user_message</span></pre><div class="zeroclipboard-container">

  </div></div>
</li>
<li>
<p dir="rtl">احفظ الملف وأعد تشغيل التطبيق.</p>
</li>
<li>
<p dir="rtl">أدخل المطالبات التالية (مع استمرار إدخال <strong>رسالة النظام</strong> وحفظها في <code>system.txt</code>).</p>
<p dir="rtl"><strong>رسالة النظام</strong></p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>You're an AI assistant who helps people find information. You'll provide answers from the text provided in the prompt, and respond concisely.
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>What animal is the favorite of children at Contoso?
</code></pre><div class="zeroclipboard-container">

  </div></div>
</li>
</ol>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: إذا كنت ترغب في رؤية الاستجابة الكاملة من Azure OpenAI، يمكنك تعيين متغيّر <strong>printFullResponse</strong> إلى <code>True</code>، وإعادة تشغيل التطبيق.</p>
</blockquote>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">عند الانتهاء من مورد Azure OpenAI، تذكر حذف التوزيع أو المورد بأكمله في <strong>مدخل Microsoft Azure</strong> في <code>https://portal.azure.com</code>.</p>
</article></div>
