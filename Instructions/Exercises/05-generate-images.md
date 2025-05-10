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
  <td><div dir="rtl">إنشاء صور باستخدام نموذج DALL-E</div></td>
  <td><div dir="rtl">stale</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">إنشاء صور باستخدام نموذج DALL-E</h1><a id="user-content-إنشاء-صور-باستخدام-نموذج-dall-e" class="anchor" aria-label="Permalink: إنشاء صور باستخدام نموذج DALL-E" href="#إنشاء-صور-باستخدام-نموذج-dall-e"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">تتضمن خدمة Azure OpenAI نموذج إنشاء صور يسمى DALL-E. يمكنك استخدام هذا النموذج لإرسال مطالبات اللغة الطبيعية التي تصف الصورة المطلوبة، وسينشئ النموذج صورة أصلية استنادًا إلى الوصف الذي تقدمه.</p>
<p dir="rtl">في هذا التمرين، ستستخدم نموذج DALL-E الإصدار 3 لإنشاء صور استنادًا إلى مطالبات اللغة الطبيعية.</p>
<p dir="rtl">سيستغرق هذا التمرين حوالي <b>25</b> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توفير مورد Azure OpenAI</h2><a id="user-content-توفير-مورد-azure-openai" class="anchor" aria-label="Permalink: توفير مورد Azure OpenAI" href="#توفير-مورد-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">قبل أن تتمكن من استخدام Azure OpenAI لإنشاء الصور، يجب توفير مورد Azure OpenAI في اشتراك Azure الخاص بك. يجب أن يكون المورد في منطقة يتم فيها دعم نماذج DALL-E.</p>
<ol dir="rtl">
    <li>سجّل الدخول إلى <b>Azure portal</b> من <code>https://portal.azure.com</code>.</li>
    <li>
        <p dir="rtl">إنشاء مورد <b>Azure OpenAI</b> بالإعدادات التالية:</p>
        <ul dir="rtl">
            <li><b>اشتراك</b>: <i>حدد اشتراك Azure الذي جرت الموافقة عليه للوصول إلى خدمة Azure OpenAI، بما في ذلك DALL-E</i></li>
            <li><b>مجموعة الموارد</b>: <i>اختيار مجموعة موارد أو إنشاءها</i></li>
            <li><b>المنطقة</b>: <i>اختر إما <b>شرق الولايات المتحدة</b> أو <b>السويد الوسطى</b></i></li>
            <li><b>الاسم</b>: <i>اسم فريد من اختيارك</i></li>
            <li><b>مستوى التسعير</b>: قياسي S0</li>
            <blockquote>* لا تتوفر نماذج DALL-E 3 إلا في موارد خدمة Azure OpenAI في <b>منطقتي شرق الولايات المتحدة</b> والسويد <b>الوسطى</b>.</blockquote>
        </ul>
    </li>
    <li>يُرجى الانتظار لاكتمال التوزيع. ثم انتقل إلى مورد Azure OpenAI الموزّع في مدخل Microsoft Azure.</li>
    <li>في صفحة <b>نظرة عامة</b> لمورد Azure OpenAI الخاص بك، مرّر لأسفل إلى قسم <b>بدء الاستخدام</b> وحدد الزر للانتقال إلى <b>مدخل AI Foundry</b> (المعروف سابقًا باسم AI Studio).</li>
    <li>
        <p dir="rtl">في بوابة Azure AI Foundry، في الجزء الموجود على اليسار، حدد صفحة <b>عمليات النشر</b> واعرض عمليات نشر النموذج الحالية لديك. إذا لم يكن لديك واحدة بالفعل لـ DALL-E 3، فعليك إنشاء توزيع جديد لنموذج <b>dall-e-3</b> بالإعدادات التالية:</p>
        <ul dir="rtl">
            <li><b>اسم التوزيع</b>: dalle3</li>
            <li><b>إصدار النموذج</b>: <i>استخدام الإصدار الافتراضي</i></li>
            <li><b>نوع التوزيع</b>: قياسي</li>
            <li><b>وحدات السعة</b>: 1K</li>
            <li><b>عامل تصفية المحتوى</b>: افتراضية</li>
            <li><b>تمكين الحصة النسبية الديناميكية</b>: معطّل</li>
        </ul>
    </li>
    <li>تم توزيع واحد، انتقل مرة أخرى إلى صفحة <b>الصور</b> في الجزء الأيمن.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">اكتشاف إنشاء الصور في بيئة الصور</h2><a id="user-content-اكتشاف-إنشاء-الصور-في-بيئة-الصور" class="anchor" aria-label="Permalink: اكتشاف إنشاء الصور في بيئة الصور" href="#اكتشاف-إنشاء-الصور-في-بيئة-الصور"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">يمكنك استخدام البيئة الخاصة بالصور في <b>مدخل Azure AI Foundry</b> لتجربة توليد الصور.</p>
<ol dir="rtl">
    <li>في قسم <b>بيئة الصور</b>، يجب تحديد توزيع DALL-E 3 تلقائيًا. إذا لم يكن الأمر كذلك، فحدده من القائمة المنسدلة للتوزيع.</li>
    <li>في مربع<b>المطالبة</b>، أدخل وصفًا لصورة تريد إنشاءها. على سبيل المثال`An elephant on a skateboard` ثم حدد <b>إنشاء</b> وعرض الصورة التي يتم إنشاؤها.</li>
    <li>تعديل المطالبة لتوفير وصف أكثر تحديدًا. على سبيل المثال<code>An elephant on a skateboard in the style of Picasso</code>. ثم قم بإنشاء الصورة الجديدة ومراجعة النتائج.</li>
    <p dir="rtl"><a href="https://github.com/MicrosoftLearning/mslearn-openai.ar-sa/blob/main/Instructions/media/images-playground-new-style.png"><img src="https://github.com/MicrosoftLearning/mslearn-openai.ar-sa/raw/main/Instructions/media/images-playground-new-style.png" alt="بيئة الصور في مدخل Azure AI Foundry مع صورتين تم توليدهما." style="max-width: 100%;"></a></p>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استخدام واجهة برمجة تطبيقات REST لإنشاء الصور</h2><a id="user-content-استخدام-واجهة-برمجة-تطبيقات-rest-لإنشاء-الصور" class="anchor" aria-label="Permalink: استخدام واجهة برمجة تطبيقات REST لإنشاء الصور" href="#استخدام-واجهة-برمجة-تطبيقات-rest-لإنشاء-الصور"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">توفر خدمة Azure OpenAI واجهة برمجة تطبيقات REST التي يمكنك استخدامها لإرسال مطالبات لإنشاء المحتوى - بما في ذلك الصور التي تم إنشاؤها بواسطة نموذج DALL-E.</p>
<div class="markdown-heading" dir="rtl"><h3 tabindex="-1" class="heading-element" dir="rtl">الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية</h3><a id="user-content-الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية" class="anchor" aria-label="Permalink: الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية" href="#الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن دعنا نستكشف كيفية إنشاء تطبيق مخصَّص يستخدم خدمة Azure OpenAI لإنشاء الصور. ستقوم بتطوير تطبيقك باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في مستودع GitHub.</p>
<blockquote>
<p dir="rtl"><b>تلميح</b>: إذا نسخت بالفعل مستودع <b>mslearn-openai</b>، فافتحه في تعليمة Visual Studio البرمجية. وإلا فاتبع هذه الخطوات لاستنساخه إلى بيئة تطويرك.</p>
</blockquote>
<ol dir="rtl">
    <li>ابدأ تشغيل Visual Studio Code.</li>
    <li>افتح لوحة (SHIFT+CTRL+P) وشغّل <b>Git: استنسخ الأمر </b> لاستنساخ مستودع <code>https://github.com/MicrosoftLearning/mslearn-openai</code> إلى مجلد محلي (لا يُهم أي مجلد).</li>
    <li>عند استنساخ المستودع، افتح المجلد في Visual Studio Code.</li>
    <blockquote><b>ملاحظة</b>: إذا عرضت لك Visual Studio Code رسالة منبثقة لمطالبتك بالثقة في التعليمات البرمجية التي تفتحها، فانقر فوق <b>نعم، أثق في خيار الكُتاب</b> في النافذة المنبثقة.</blockquote>
    <li>انتظر حتى تثبيت ملفات إضافية لدعم مشاريع التعليمات البرمجية C# في المستودع.</li>
    <blockquote><b>ملاحظة</b>: في حالة مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد <b>ليس الآن</b>.</blockquote>
</ol>
<div class="markdown-heading" dir="rtl"><h3 tabindex="-1" class="heading-element" dir="rtl">تكوين تطبيقك</h3><a id="user-content-تكوين-تطبيقك" class="anchor" aria-label="Permalink: تكوين تطبيقك" href="#تكوين-تطبيقك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">تم توفير تطبيقات لكل من C# وPython. يتميز كلا التطبيقين بالوظيفة نفسها. أولاً، ستضيف نقطة النهاية والمفتاح لمورد Azure OpenAI لديك إلى ملف تكوين التطبيق.</p>
<ol dir="rtl">
    <li>في Visual Studio Code في جزء <b>المستكشف</b>، انتقِل إلى المجلد <b>Labfiles/05-image-generation</b> وعليك توسيع المجلد <b>CSharp</b> أو <b>Python</b> حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي تريد دمج وظيفة Azure OpenAI فيه.</li>
    <li>
        <p dir="rtl">في جزء<b>مستكشف</b>، في مجلد <b>CSharp</b> أو <b>Python</b>، افتح ملف التكوين للغة المفضلة لديك</p>
        <ul dir="rtl">
            <li><b>C#</b>: appsettings.json</li>
            <li><b>Python</b>: .env</li>
        </ul>
    </li>
    <li>قم بتحديث قيم التكوين لتضمين <b>نقطة النهاية</b> و<b>مفتاح</b> من مورد Azure OpenAI الذي أنشأته (متوفر في صفحة <b>المفاتيح ونقطة النهاية</b> لمورد Azure OpenAI في مدخل Microsoft Azure).</li>
    <li>احفظ ملف التكوين.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h3 tabindex="-1" class="heading-element" dir="rtl">عرض التعليمات البرمجية للتطبيق</h3><a id="user-content-عرض-التعليمات-البرمجية-للتطبيق" class="anchor" aria-label="Permalink: عرض التعليمات البرمجية للتطبيق" href="#عرض-التعليمات-البرمجية-للتطبيق"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">أنت الآن جاهز لاستكشاف التعليمات البرمجية المستخدمة لاستدعاء واجهة برمجة تطبيقات REST وإنشاء صورة.</p>
<ol dir="rtl">
    <li>
        <p dir="rtl">في جزء<b> Explorer</b>، حدد ملف التعليمات البرمجية الرئيسي للتطبيق لديك:</p>
        <ul dir="rtl">
            <li>C#: <code>Program.cs</code></li>
            <li>Python: <code>generate-image.py</code></li>
        </ul>
    </li>
    <li>
        <p dir="rtl">راجع التعليمات البرمجية التي يحتوي عليها الملف، مع ملاحظة الميزات الرئيسية التالية:</p>
        <ul dir="rtl">
            <li>تقدم التعليمات البرمجية طلب https إلى نقطة النهاية للخدمة الخاصة بك، بما في ذلك مفتاح الخدمة لديك في العنوان. يتم الحصول على كلتا القيمتين من ملف التكوين.</li>
            <li>يتضمن الطلب بعض المعلمات، بما في ذلك المطالبة التي يجب أن تستند إلى الصورة، وعدد الصور المراد إنشاؤها، وحجم الصورة (الصور) التي يتم إنشاؤها.</li>
            <li>تتضمن الاستجابة مطالبة منقحة قام نموذج DALL-E بالتوصل إليها من المطالبة المقدمة من المستخدم لجعلها أكثر وصفية، وعنوان URL للصورة التي تم إنشاؤها.</li>
        </ul>
        <blockquote><b>هام</b>: إذا قمت بتسمية التوزيع الخاص بك بأي شيء آخر غير <i>dalle3</i> لموصى بها، فستحتاج إلى تحديث التعليمة البرمجية لاستخدام اسم عملية توزيعك.</blockquote>
    </li>
</ol>
<div class="markdown-heading" dir="rtl"><h3 tabindex="-1" class="heading-element" dir="rtl">تشغيل التطبيق</h3><a id="user-content-تشغيل-التطبيق" class="anchor" aria-label="Permalink: تشغيل التطبيق" href="#تشغيل-التطبيق"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن راجعت التعليمات البرمجية، فقد حان الوقت لتشغيلها وإنشاء بعض الصور.</p>
<ol dir="rtl">
    <li>انقر بزر الماوس الأيمن فوق المجلد <b>CSharp</b> أو <b>Python</b> الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وافتح محطة طرفية متكاملة. ثم أدخل الأمر المناسب لتشغيل التطبيق لديك:</li>
    <b>C#</b>
    <div dir="rtl">
    <div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>dotnet run</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="dotnet run" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
    </div>
    <b>Python</b>
    <div dir="rtl">
    <div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>pip install requests
python generate-image.py</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install requests
python generate-image.py" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
    </div>
    <li>عند المطالبة، أدخل وصفًا لصورة. على سبيل المثال، <i>زرافة تطيّر طائرة ورقية</i>.</li>
    <li>انتظر حتى يتم إنشاء الصورة - سيتم عرض ارتباط تشعبي في جزء المحطة الطرفية. ثم حدد الارتباط التشعبي لفتح علامة تبويب جديدة للمستعرض وقم بمراجعة الصورة التي تم إنشاؤها.</li>
    <blockquote><b>تلميح</b>: إذا لم يرجع التطبيق استجابة، فانتظر دقيقة وحاول مرة أخرى. قد تستغرق الموارد المنشورة حديثًا ما يصل إلى 5 دقائق لتصبح متاحة.</blockquote>
    <li>أغلق علامة تبويب المستعرض التي تحتوي على الصورة التي تم إنشاؤها وأعد تشغيل التطبيق لإنشاء صورة جديدة باستخدام مطالبة مختلفة.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">عند الانتهاء من مورد Azure OpenAI، تذكر حذف المورد بأكمله في <b>مدخل Microsoft Azure</b> في <code><a href="https://portal.azure.com" rel="nofollow">https://portal.azure.com</a></code>.</p>
</article></div>
