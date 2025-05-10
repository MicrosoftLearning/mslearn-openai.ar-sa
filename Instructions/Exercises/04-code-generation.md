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
  <td><div dir="rtl">إنشاء التعليمات البرمجية وتحسينها باستخدام خدمة Azure OpenAI</div></td>
  <td><div dir="rtl">stale</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">إنشاء التعليمات البرمجية وتحسينها باستخدام خدمة Azure OpenAI</h1><a id="user-content-إنشاء-التعليمات-البرمجية-وتحسينها-باستخدام-خدمة-azure-openai" class="anchor" aria-label="Permalink: إنشاء التعليمات البرمجية وتحسينها باستخدام خدمة Azure OpenAI" href="#إنشاء-التعليمات-البرمجية-وتحسينها-باستخدام-خدمة-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">يمكن لنماذج خدمة Azure OpenAI إنشاء تعليمة برمجية لك باستخدام مطالبات اللغة الطبيعية، وإصلاح الأخطاء في التعليمة البرمجية المكتملة، وتوفير تعليقات التعليمة البرمجية. يمكن لهذه النماذج أيضًا شرح التعليمة البرمجية الموجودة وتبسيطها لمساعدتك على فهم ما يفعله وكيفية تحسينه.</p>
<p dir="rtl">في سيناريو هذا التمرين، ستؤدي دور مطور برامج يستكشف كيفية استخدام الذكاء الاصطناعي التوليدي لجعل مهام الترميز أسهل وأكثر كفاءة. يمكن تطبيق التقنيات المستخدمة في التمرين على ملفات التعليمات البرمجية الأخرى ولغات البرمجة وحالات الاستخدام.</p>
<p dir="rtl">سيستغرق هذا التمرين حوالي <strong>25</strong> دقيقة.</p>
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
<p dir="rtl">* موارد Azure OpenAI مقيدة بالحصص النسبية الإقليمية. تتضمن المناطق المدرجة الحصة النسبية الافتراضية لنوع (أنواع) النموذج المستخدمة في هذا التمرين. يؤدي اختيار منطقة عشوائيًا إلى تقليل مخاطر وصول منطقة واحدة إلى حد الحصة النسبية في السيناريوهات التي تشارك فيها اشتراكًا مع مستخدمين آخرين. في حالة الوصول إلى حد الحصة النسبية لاحقًا في التمرين، فمن المحتمل أنك قد تحتاج إلى إنشاء مورد آخر في منطقة مختلفة.</p>
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
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء تعليمة برمجية في البيئة التجريبية للدردشة</h2><a id="user-content-إنشاء-تعليمة-برمجية-في-البيئة-التجريبية-للدردشة" class="anchor" aria-label="Permalink: إنشاء تعليمة برمجية في البيئة التجريبية للدردشة" href="#إنشاء-تعليمة-برمجية-في-البيئة-التجريبية-للدردشة"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">قبل الاستخدام في تطبيقك، افحص كيفية قدرة Azure OpenAI على إنشاء التعليمات البرمجية وشرحها في البيئة التجريبية للدردشة.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في قسم <strong>البيئة التجريبية</strong>، حدد صفحة <strong>دردشة</strong>. تتكون صفحة بيئة <strong>الدردشة</strong> من صف من الأزرار ولوحتين رئيسيتين (والتي يمكن ترتيبها من اليمين إلى اليسار أفقيًا، أو من أعلى إلى أسفل عموديًا حسب دقة الشاشة لديك):</p>
<ul dir="rtl">
<li><strong>التكوين</strong> - يُستخدم لتحديد التوزيع الخاص بك، وتحديد رسالة النظام، وتعيين معلمات للتفاعل مع توزيعك.</li>
<li><strong>جلسة الدردشة</strong> - تستخدم لإرسال رسائل الدردشة وعرض الاستجابات.</li>
</ul>
</li>
<li>
<p dir="rtl">في جزء <strong>عمليات التوزيع</strong>، تأكد من تحديد توزيع نموذجك.</p>
</li>
<li>
<p dir="rtl">في مساحة <strong>رسالة النظام</strong>، قم بتعيين رسالة النظام إلى <code>You are a programming assistant helping write code</code> وقم بتطبيق التغييرات.</p>
</li>
<li>
<p dir="rtl">في <strong>جلسة دردشة</strong>، أرسل الاستعلام التالي:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Write a function in python that takes a character and a string as input, and returns how many times the character appears in the string
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl">من المرجح أن يستجيب النموذج بدالة، مع بعض التوضيحات حول ما تفعله الوظيفة وكيفية استدعائها.</p>
</li>
<li>
<p dir="rtl">بعد ذلك، أرسل المطالبة <code>Do the same thing, but this time write it in C#</code>.</p>
<p dir="rtl">من المرجح أن النموذج استجاب بشكل مشابه جدًا للمرة الأولى، ولكن هذه المرة باستخدام الترميز بلغة C#. يمكنك أن تطلب منه مرة أخرى لغة مختلفة من اختيارك، أو دالة لإكمال مهمة مختلفة مثل عكس سلسلة الإدخال.</p>
</li>
<li>
<p dir="rtl">بعد ذلك، دعونا نستكشف استخدام الذكاء الاصطناعي لفهم التعليمة البرمجية. أرسل المطالبة التالية كرسالة المستخدم.</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>What does the following function do?  
---  
def multiply(a, b):  
    result = 0  
    negative = False  
    if a &lt; 0 and b &gt; 0:  
        a = -a  
        negative = True  
    elif a &gt; 0 and b &lt; 0:  
        b = -b  
        negative = True  
    elif a &lt; 0 and b &lt; 0:  
        a = -a  
        b = -b  
    while b &gt; 0:  
        result += a  
        b -= 1      
    if negative:  
        return -result  
    else:  
        return result  
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl">يجب أن يصف النموذج ما تفعله الدالة، وهو ضرب رقمين معًا باستخدام تكرار حلقي.</p>
</li>
<li>
<p dir="rtl">أرسل المطالبة <code>Can you simplify the function?</code>.</p>
<p dir="rtl">يجب أن يكتب النموذج إصدارًا أبسط من الدالة.</p>
</li>
<li>
<p dir="rtl">إرسال المطالبة: <code>Add some comments to the function.</code></p>
<p dir="rtl">يضيف النموذج تعليقات إلى التعليمة البرمجية.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية</h2><a id="user-content-الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية" class="anchor" aria-label="Permalink: الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية" href="#الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن دعنا نستكشف كيفية إنشاء تطبيق مخصَّص يستخدم خدمة Azure OpenAI لإنشاء التعليمة البرمجية. ستقوم بتطوير تطبيقك باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في مستودع GitHub.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: إذا نسخت بالفعل مستودع <strong>mslearn-openai</strong>، فافتحه في تعليمة Visual Studio البرمجية. وإلا فاتبع هذه الخطوات لاستنساخه إلى بيئة تطويرك.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">ابدأ تشغيل Visual Studio Code.</p>
</li>
<li>
<p dir="rtl">افتح عرض لوحة الأوامر (SHIFT+CTRL+P أو <strong>عرض لوحة الأوامر</strong> &gt; <strong>Command Palette</strong>)، ثم نفّذ أمر <strong>Git: Clone</strong> لاستنساخ المستودع <code>https://github.com/MicrosoftLearning/mslearn-openai</code> إلى مجلد محلي (لا يهم أي مجلد تختاره).</p>
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
<p dir="rtl">تم توفير تطبيقات لكل من C# وPython، وكذلك ملف نصي نموذجي ستستخدمه لاختبار التلخيص. يتميز كلا التطبيقين بالوظيفة نفسها. أولاً، ستكمل بعض الأجزاء الرئيسية من التطبيق لتمكين استخدام مورد Azure OpenAI الخاص بك.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في تعليمة Visual Studio البرمجية في جزء <strong>المستكشف</strong>، انتقِل إلى المجلد <strong>Labfiles/04-code-generation</strong> وعليك توسيع المجلد <strong>CSharp</strong> أو <strong>Python</strong> حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي تريد دمج وظيفة Azure OpenAI فيه.</p>
</li>
<li>
<p dir="rtl">انقر بزر الماوس الأيمن فوق المجلد <strong>CSharp</strong> أو <strong>Python</strong> الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وافتح وحدة طرفية متكاملة. ثم، عليك تثبيت حزمة Azure OpenAI SDK عن طريق تشغيل الأمر المناسب لتفضيل اللغة لديك:</p>
<p dir="rtl"><strong>:C#</strong></p>
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
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إضافة تعليمة برمجية لاستخدام نموذج خدمة Azure OpenAI</h2><a id="user-content-إضافة-تعليمة-برمجية-لاستخدام-نموذج-خدمة-azure-openai" class="anchor" aria-label="Permalink: إضافة تعليمة برمجية لاستخدام نموذج خدمة Azure OpenAI" href="#إضافة-تعليمة-برمجية-لاستخدام-نموذج-خدمة-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">أنت الآن جاهز لاستخدام Azure OpenAI SDK لاستهلاك نموذجك الموزع.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في جزء <strong>المستكشف</strong>، في مجلد <strong>CSharp</strong> أو <strong>Python</strong>، افتح ملف التعليمة البرمجية الخاص باللغة المفضلة لديك. في الدالة التي تستدعي نموذج Azure OpenAI، ضمن <em><strong>تنسيق التعليق وإرسال الطلب إلى النموذج</strong></em>، أضف التعليمات البرمجية لتنسيق وإرسال الطلب إلى النموذج.</p>
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
        <span class="pl-k">new</span> <span class="pl-smi">SystemChatMessage</span><span class="pl-kos">(</span><span class="pl-s1">systemPrompt</span><span class="pl-kos">)</span><span class="pl-kos">,</span>
        <span class="pl-k">new</span> <span class="pl-smi">UserChatMessage</span><span class="pl-kos">(</span><span class="pl-s1">userPrompt</span><span class="pl-kos">)</span><span class="pl-kos">,</span>
    <span class="pl-kos">]</span><span class="pl-kos">,</span>
    <span class="pl-s1">chatCompletionsOptions</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl"><strong>Python</strong>: code-generation.py</p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c"># Format and send the request to the model</span>
<span class="pl-s1">messages</span> <span class="pl-c1">=</span>[
    {<span class="pl-s">"role"</span>: <span class="pl-s">"system"</span>, <span class="pl-s">"content"</span>: <span class="pl-s1">system_message</span>},
    {<span class="pl-s">"role"</span>: <span class="pl-s">"user"</span>, <span class="pl-s">"content"</span>: <span class="pl-s1">user_message</span>},
]

<span class="pl-c"># Call the Azure OpenAI model</span>
<span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">client</span>.<span class="pl-c1">chat</span>.<span class="pl-c1">completions</span>.<span class="pl-c1">create</span>(
    <span class="pl-s1">model</span><span class="pl-c1">=</span><span class="pl-s1">model</span>,
    <span class="pl-s1">messages</span><span class="pl-c1">=</span><span class="pl-s1">messages</span>,
    <span class="pl-s1">temperature</span><span class="pl-c1">=</span><span class="pl-c1">0.7</span>,
    <span class="pl-s1">max_tokens</span><span class="pl-c1">=</span><span class="pl-c1">1000</span>
)</pre><div class="zeroclipboard-container">
 
  </div></div>
</li>
<li>
<p dir="rtl">احفظ التغييرات في ملف التعليمة البرمجية.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="auto">شغّل التطبيق</h2><a id="user-content-شغّل-التطبيق" class="anchor" aria-label="Permalink: شغّل التطبيق" href="#شغّل-التطبيق"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن تم تكوين التطبيق الخاص بك، قم بتشغيله لمحاولة إنشاء التعليمة البرمجية لكل حالة استخدام. يتم ترقيم حالة الاستخدام في التطبيق، ويمكن تشغيلها بأي ترتيب.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: قد يواجه بعض المستخدمين تحديدًا للمعدّل في حالة استدعاء النموذج بشكل متكرر للغاية. إذا واجهت خطأً بخصوص تحديد معدّل الرمز المميز، فانتظر لمدة دقيقة ثم حاول مرة أخرى.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">في جزء <strong>المستكشف</strong>، عليك توسيع المجلد <strong>Labfiles/04-code-generation/sample-code</strong> وراجع الدالة وتطبيق <em>go-fish</em> للغتك. سيتم استخدام هذه الملفات للمهام في التطبيق.</p>
</li>
<li>
<p dir="rtl">في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.</p>
<ul dir="rtl">
<li><strong>C#:</strong> <code>dotnet run</code></li>
<li><strong>Python</strong>: <code>python code-generation.py</code></li>
</ul>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يمكنك استخدام أيقونة <strong>تكبير حجم اللوحة</strong> (<strong>^</strong>) في شريط أدوات المحطة الطرفية لرؤية المزيد من نص وحدة التحكم.</p>
</blockquote>
</li>
<li>
<p dir="rtl">اختر الخيار 1 لإضافة تعليقات إلى التعليمة البرمجية الخاص بك وأدخل المطالبة التالية. لاحظ أن الاستجابة قد تستغرق بضع ثوانٍ لكل من هذه المهام.</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Add comments to the following function. Return only the commented code.\n---\n
</code></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl">سيتم وضع النتائج في <strong>result/app.txt</strong>. افتح هذا الملف، وقارنه بملف الدالة الموجود في <strong>sample-code</strong>.</p>
</li>
<li>
<p dir="rtl">بعد ذلك، اختر الخيار <strong>2</strong> لكتابة اختبارات الوحدة لنفس الدالة وأدخل المطالبة التالية.</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Write four unit tests for the following function.\n---\n
</code></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl">ستحل النتائج محل ما كان موجودًا في <strong>result/app.txt</strong>، وتفاصيل أربع اختبارات وحدة لهذه الدالة.</p>
</li>
<li>
<p dir="rtl">بعد ذلك، اختر الخيار <strong>3</strong> لإصلاح الأخطاء في التطبيق للعب Go Fish. أدخل المطالبة التالية.</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Fix the code below for an app to play Go Fish with the user. Return only the corrected code.\n---\n
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl">ستحل النتائج محل ما كان موجودًا في <strong>result/app.txt</strong>، ويجب أن يكون لها تعليمة برمجية مشابهة جدًا مع تصحيح بعض الأشياء.</p>
<ul dir="rtl">
<li><strong>C#</strong>: يتم إجراء إصلاحات على السطرين 30 و59</li>
<li><strong>Python</strong>: يتم إجراء إصلاحات على السطرين 18 و31</li>
</ul>
<p dir="rtl">يمكن تشغيل تطبيق Go Fish في <strong>sample-code</strong> إذا قمت باستبدال الأسطر التي تحتوي على أخطاء بالاستجابة من Azure OpenAI. إذا قمت بتشغيله دون الإصلاحات، فلن يعمل بشكل صحيح.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: من الأهمية بمكان ملاحظة أنه على الرغم من تصحيح التعليمات البرمجية لتطبيق Go Fish هذا لبعض بناء الجملة، إلا أنه ليس تمثيلاً دقيقًا تمامًا للعبة. إذا تمعنت بدقة، ستجد مشاكل تتعلق بعدم التحقق مما إذا كانت المجموعة فارغة عند سحب البطاقات، وعدم إزالة الأزواج من يد اللاعب عندما يحصل على زوج، وبعض الأخطاء الأخرى التي تتطلب فهم ألعاب البطاقات لتحقيقها. يُعدَّ هذا مثالاً رائعًا لكيفية مساعدة نماذج الذكاء الاصطناعي التوليدي المفيدة في إنشاء التعليمات البرمجية، ولكن لا يمكن الوثوق بصحتها ويجب التحقق منها من قِبل المطور.</p>
</blockquote>
<p dir="rtl">إذا كنت ترغب في رؤية الاستجابة الكاملة من Azure OpenAI، يمكنك تعيين متغيّر <strong>printFullResponse</strong> إلى <code>True</code>، وإعادة تشغيل التطبيق.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">عند الانتهاء من مورد Azure OpenAI، تذكر حذف التوزيع أو المورد بأكمله في <strong>مدخل Microsoft Azure</strong> في <code>https://portal.azure.com</code>.</p>
</article></div>
