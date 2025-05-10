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
  <td><div dir="rtl">استخدام Azure OpenAI SDKs في تطبيقك</div></td>
  <td><div dir="rtl">stale</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استخدام Azure OpenAI APIs في تطبيقك</h1><a id="user-content-استخدام-azure-openai-apis-في-تطبيقك" class="anchor" aria-label="Permalink: استخدام Azure OpenAI APIs في تطبيقك" href="#استخدام-azure-openai-apis-في-تطبيقك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">باستخدام خدمة Azure OpenAI، يمكن للمطورين إنشاء روبوتات الدردشة ونماذج اللغة والتطبيقات الأخرى التي تتفوق في فهم اللغة البشرية الطبيعية. يوفر Azure OpenAI الوصول إلى نماذج الذكاء الاصطناعي المدربة مسبقاً، بالإضافة إلى مجموعة من واجهات برمجة التطبيقات والأدوات لتخصيص هذه النماذج وضبطها لتلبية المتطلبات المحددة للتطبيق الخاص بك. في هذا التمرين، ستتعلم كيفية نشر نموذج في Azure OpenAI واستخدامه في تطبيقك الخاص.</p>
<p dir="rtl">في سيناريو هذا التمرين، ستؤدي دور مطور برامج مكلف بتنفيذ تطبيق يمكنه استخدام الذكاء الاصطناعي التوليدي للمساعدة في تقديم توصيات المشي لمسافات طويلة. يمكن تطبيق التقنيات المستخدمة في التمرين على أي تطبيق يريد استخدام Azure OpenAI APIs.</p>
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
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية</h2><a id="user-content-الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية" class="anchor" aria-label="Permalink: الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية" href="#الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستضع تطبيقك Azure OpenAI APIs باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في GitHub repo.</p>
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
<p dir="rtl">تم توفير تطبيقات لكل من C# وPython. يتميز كلا التطبيقين بالوظيفة نفسها. أولاً، ستكمل بعض الأجزاء الرئيسية من التطبيق لتمكين استخدام مورد Azure OpenAI الخاص بك.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في تعليمة Visual Studio البرمجية في جزء <strong>المستكشف</strong>، انتقِل إلى المجلد <strong>Labfiles/02-azure-openai-api</strong> ويمكنك توسيع المجلد <strong>CSharp</strong> أو <strong>Python</strong> حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي ستدمج وظيفة Azure OpenAI فيه.</p>
</li>
<li>
<p dir="rtl">انقر بزر الماوس الأيمن فوق المجلد <strong>CSharp</strong> أو <strong>Python</strong> الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وافتح محطة طرفية متكاملة. ثم، عليك تثبيت حزمة Azure OpenAI SDK عن طريق تشغيل الأمر المناسب لتفضيل اللغة لديك:</p>
<p dir="rtl"><strong>C#:</strong></p>
</li>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre>dotnet add package Azure.AI.OpenAI <span class="pl-k">--</span>version <span class="pl-c1">2.1</span>.<span class="pl-c1">0</span></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>Python</strong>:</p>
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
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c">// Add Azure OpenAI packages</span>
<span class="pl-k">using</span> <span class="pl-s1">Azure</span><span class="pl-kos">.</span><span class="pl-s1">AI</span><span class="pl-kos">.</span><span class="pl-s1">OpenAI</span><span class="pl-kos">;</span>
<span class="pl-k">using</span> <span class="pl-s1">OpenAI</span><span class="pl-kos">.</span><span class="pl-s1">Chat</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>Python</strong>: test-openai-model.py</p>
</li>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto dir="auto"><pre><span class="pl-c"># Add Azure OpenAI package</span>
<span class="pl-k">from</span> <span class="pl-s1">openai</span> <span class="pl-k">import</span> <span class="pl-v">AzureOpenAI</span></pre><div class="zeroclipboard-container">
  </div></div>
</li>
<li>
<p dir="rtl">في التعليمات البرمجية للتطبيق الخاص بلغتك، استبدل التعليق <em><strong>تهيئة عميل Azure OpenAI...</strong></em> بالتعليمات البرمجية التالية لتهيئة العميل وتحديد رسالة النظام الخاصة بنا.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto dir="auto"><pre><span class="pl-c">// Initialize the Azure OpenAI client</span>
<span class="pl-smi">AzureOpenAIClient</span> <span class="pl-s1">azureClient</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-kos">(</span><span class="pl-k">new</span> <span class="pl-smi">Uri</span><span class="pl-kos">(</span><span class="pl-s1">oaiEndpoint</span><span class="pl-kos">)</span><span class="pl-kos">,</span> <span class="pl-k">new</span> <span class="pl-smi">ApiKeyCredential</span><span class="pl-kos">(</span><span class="pl-s1">oaiKey</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-smi">ChatClient</span> <span class="pl-s1">chatClient</span> <span class="pl-c1">=</span> <span class="pl-s1">azureClient</span><span class="pl-kos">.</span><span class="pl-en">GetChatClient</span><span class="pl-kos">(</span><span class="pl-s1">oaiDeploymentName</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-c">// System message to provide context to the model</span>
<span class="pl-smi">string</span> <span class="pl-s1">systemMessage</span> <span class="pl-c1">=</span> <span class="pl-s">"I am a hiking enthusiast named Forest who helps people discover hikes in their area. If no area is specified, I will default to near Rainier National Park. I will then provide three suggestions for nearby hikes that vary in length. I will also share an interesting fact about the local nature on the hikes when making a recommendation."</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>Python</strong>: test-openai-model.py</p>
</li>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto dir="auto"><pre><span class="pl-c"># Initialize the Azure OpenAI client</span>
<span class="pl-s1">client</span> <span class="pl-c1">=</span> <span class="pl-en">AzureOpenAI</span>(
        <span class="pl-s1">azure_endpoint</span> <span class="pl-c1">=</span> <span class="pl-s1">azure_oai_endpoint</span>, 
        <span class="pl-s1">api_key</span><span class="pl-c1">=</span><span class="pl-s1">azure_oai_key</span>,  
        <span class="pl-s1">api_version</span><span class="pl-c1">=</span><span class="pl-s">"2024-02-15-preview"</span>
        )

<span class="pl-c"># Create a system message</span>
<span class="pl-s1">system_message</span> <span class="pl-c1">=</span> <span class="pl-s">"""I am a hiking enthusiast named Forest who helps people discover hikes in their area. </span>
<span class="pl-s">    If no area is specified, I will default to near Rainier National Park. </span>
<span class="pl-s">    I will then provide three suggestions for nearby hikes that vary in length. </span>
<span class="pl-s">    I will also share an interesting fact about the local nature on the hikes when making a recommendation.</span>
<span class="pl-s">    """</span></pre><div class="zeroclipboard-container">
 
  </div></div>
</li>
<li>
<p dir="rtl">استبدل التعليق <em><strong>إضافة تعليمة برمجية لإرسال الطلب...</strong></em> بالتعليمات البرمجية اللازمة لإنشاء الطلب؛ لتحديد المعلمات المختلفة للنموذج الخاص بك مثل <code>Temperature</code> و <code>MaxOutputTokenCount</code>.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto dir="auto"><pre><span class="pl-c">// Add code to send request...</span>
<span class="pl-c">// Get response from Azure OpenAI</span>
<span class="pl-smi">ChatCompletionOptions</span> <span class="pl-s1">chatCompletionOptions</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-smi">ChatCompletionOptions</span><span class="pl-kos">(</span><span class="pl-kos">)</span>
<span class="pl-kos">{</span>
    <span class="pl-s1">Temperature</span> <span class="pl-c1">=</span> <span class="pl-c1">0.7f</span><span class="pl-kos">,</span>
    <span class="pl-s1">MaxOutputTokenCount</span> <span class="pl-c1">=</span> <span class="pl-c1">800</span>
<span class="pl-kos">}</span><span class="pl-kos">;</span>

<span class="pl-smi">ChatCompletion</span> <span class="pl-s1">completion</span> <span class="pl-c1">=</span> <span class="pl-s1">chatClient</span><span class="pl-kos">.</span><span class="pl-en">CompleteChat</span><span class="pl-kos">(</span>
    <span class="pl-kos">[</span>
        <span class="pl-k">new</span> <span class="pl-smi">SystemChatMessage</span><span class="pl-kos">(</span><span class="pl-s1">systemMessage</span><span class="pl-kos">)</span><span class="pl-kos">,</span>
        <span class="pl-k">new</span> <span class="pl-smi">UserChatMessage</span><span class="pl-kos">(</span><span class="pl-s1">inputText</span><span class="pl-kos">)</span>
    <span class="pl-kos">]</span><span class="pl-kos">,</span>
    <span class="pl-s1">chatCompletionOptions</span>
<span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-s1">Console</span><span class="pl-kos">.</span><span class="pl-en">WriteLine</span><span class="pl-kos">(</span><span class="pl-s"><span class="pl-s">$</span>"<span class="pl-kos">{</span><span class="pl-s1">completion</span><span class="pl-kos">.</span><span class="pl-s1">Role</span><span class="pl-kos">}</span>: <span class="pl-kos">{</span><span class="pl-s1">completion</span><span class="pl-kos">.</span><span class="pl-s1">Content</span><span class="pl-kos">[</span><span class="pl-c1">0</span><span class="pl-kos">]</span><span class="pl-kos">.</span><span class="pl-s1">Text</span><span class="pl-kos">}</span>"</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl"><strong>Python</strong>: test-openai-model.py</p>
</li>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto dir="auto"><pre><span class="pl-c"># Add code to send request...</span>
<span class="pl-c"># Send request to Azure OpenAI model</span>
<span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">client</span>.<span class="pl-c1">chat</span>.<span class="pl-c1">completions</span>.<span class="pl-c1">create</span>(
    <span class="pl-s1">model</span><span class="pl-c1">=</span><span class="pl-s1">azure_oai_deployment</span>,
    <span class="pl-s1">temperature</span><span class="pl-c1">=</span><span class="pl-c1">0.7</span>,
    <span class="pl-s1">max_tokens</span><span class="pl-c1">=</span><span class="pl-c1">400</span>,
    <span class="pl-s1">messages</span><span class="pl-c1">=</span>[
        {<span class="pl-s">"role"</span>: <span class="pl-s">"system"</span>, <span class="pl-s">"content"</span>: <span class="pl-s1">system_message</span>},
        {<span class="pl-s">"role"</span>: <span class="pl-s">"user"</span>, <span class="pl-s">"content"</span>: <span class="pl-s1">input_text</span>}
    ]
)
<span class="pl-s1">generated_text</span> <span class="pl-c1">=</span> <span class="pl-s1">response</span>.<span class="pl-c1">choices</span>[<span class="pl-c1">0</span>].<span class="pl-c1">message</span>.<span class="pl-c1">content</span>

<span class="pl-c"># Print the response</span>
<span class="pl-en">print</span>(<span class="pl-s">"Response: "</span> <span class="pl-c1">+</span> <span class="pl-s1">generated_text</span> <span class="pl-c1">+</span> <span class="pl-s">"<span class="pl-cce">\n</span>"</span>)</pre><div class="zeroclipboard-container">
 
  </div></div>
</li>
<li>
<p dir="rtl">احفظ التغييرات في ملف التعليمات البرمجية خاصتك.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">اختبار التطبيق الخاص بك</h2><a id="user-content-اختبار-التطبيق-الخاص-بك" class="anchor" aria-label="Permalink: اختبار التطبيق الخاص بك" href="#اختبار-التطبيق-الخاص-بك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن نجح تكوين التطبيق الخاص بك، عليك تشغيله لإرسال طلبك إلى النموذج الخاص بك ومراقبة الاستجابة.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.</p>
<ul dir="rtl">
<li><strong>C#:</strong> <code>dotnet run</code></li>
<li><strong>Python</strong>: <code>python test-openai-model.py</code></li>
</ul>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يمكنك استخدام أيقونة <strong>تكبير حجم اللوحة</strong> (<strong>^</strong>) في شريط أدوات المحطة الطرفية لرؤية المزيد من نص وحدة التحكم.</p>
</blockquote>
</li>
<li>
<p dir="rtl">عند المطالبة، أدخل النص <code>What hike should I do near Rainier?</code>.</p>
</li>
<li>
<p dir="rtl">لاحظ الإخراج، مع ملاحظة أن الاستجابة تتبع الإرشادات المقدمة في رسالة النظام التي أضفتها إلى صفيف <em>الرسائل</em>.</p>
</li>
<li>
<p dir="rtl">قدم المطالبة <code>Where should I hike near Boise? I'm looking for something of easy difficulty, between 2 to 3 miles, with moderate elevation gain.</code> ولاحظ الإخراج.</p>
</li>
<li>
<p dir="rtl">في ملف التعليمات البرمجية للغتك المفضلة، يمكنك تغيير قيمة معلمة <em>درجة الحرارة</em> في طلبك إلى <strong>1.0</strong> واحفظ الملف.</p>
</li>
<li>
<p dir="rtl">يمكنك تشغيل التطبيق مرة أخرى باستخدام المطالبات أعلاه، ولاحظ الإخراج.</p>
</li>
</ol>
<p dir="rtl">غالباً ما تؤدي زيادة درجة الحرارة إلى اختلاف الاستجابة، حتى عند توفير نفس النص، بسبب زيادة العشوائية. يمكنك تشغيله عدة مرات لمعرفة كيفية تغيير الإخراج. حاول استخدام قيم مختلفة لدرجة الحرارة بالإدخال نفسه.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">حفظ محفوظات المحادثات</h2><a id="user-content-حفظ-محفوظات-المحادثات" class="anchor" aria-label="Permalink: حفظ محفوظات المحادثات" href="#حفظ-محفوظات-المحادثات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في معظم تطبيقات العالم الحقيقي، تسمح القدرة على الرجوع إلى الأجزاء السابقة من المحادثة بتفاعل أكثر واقعية مع عامل الذكاء الاصطناعي. واجهة برمجة تطبيقات Azure OpenAI عديمة الحالة حسب التصميم، ولكن من خلال توفير محفوظات للمحادثة في مطالبتك، يمكنك تمكين نموذج الذكاء الاصطناعي للإشارة إلى الرسائل السابقة.</p>
<ol dir="rtl">
<li>
<p dir="rtl">شغل التطبيق مرة أخرى وقدم المطالبة <code>Where is a good hike near Boise?</code>.</p>
</li>
<li>
<p dir="rtl">لاحظ الإخراج، ثم استخدم المطالبة <code>How difficult is the second hike you suggested?</code>.</p>
</li>
<li>
<p dir="rtl">من المحتمل أن تشير الاستجابة من النموذج إلى عدم القدرة على فهم الرفع الذي تشير إليه. لإصلاح ذلك، يمكننا تمكين النموذج من الحصول على رسائل المحادثة السابقة للرجوع إليها.</p>
</li>
<li>
<p dir="rtl">في التطبيق الخاص بك، نحتاج إلى إضافة المطالبة السابقة والاستجابة إلى المطالبة المستقبلية التي نرسلها. فيما يلي تعريف <strong>رسائل النظام</strong>، أضف التعليمات البرمجية التالية.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c">// Initialize messages list</span>
<span class="pl-k">var</span> <span class="pl-s1">messagesList</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-smi">List</span><span class="pl-c1">&lt;</span><span class="pl-smi">ChatMessage</span><span class="pl-c1">&gt;</span><span class="pl-kos">(</span><span class="pl-kos">)</span>
<span class="pl-kos">{</span>
    <span class="pl-k">new</span> <span class="pl-smi">SystemChatMessage</span><span class="pl-kos">(</span><span class="pl-s1">systemMessage</span><span class="pl-kos">)</span><span class="pl-kos">,</span>
<span class="pl-kos">}</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl"><strong>Python</strong>: test-openai-model.py</p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c"># Initialize messages array</span>
<span class="pl-s1">messages_array</span> <span class="pl-c1">=</span> [{<span class="pl-s">"role"</span>: <span class="pl-s">"system"</span>, <span class="pl-s">"content"</span>: <span class="pl-s1">system_message</span>}]</pre><div class="zeroclipboard-container">
   </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">ضمن التعليق <em><strong>أضف تعليمة برمجية لإرسال الطلب...</strong></em>، استبدل كل التعليمة البرمجية من التعليق <strong>حتى</strong> نهاية الحلقة يالتعليمة البرمجية التالية ثم احفظ الملف. التعليمة البرمجية هي نفسها في الغالب، ولكن الآن تستخدم صفيف الرسائل لتخزين محفوظات المحادثات.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c">// Add code to send request...</span>
<span class="pl-c">// Build completion options object</span>
<span class="pl-s1">messagesList</span><span class="pl-kos">.</span><span class="pl-en">Add</span><span class="pl-kos">(</span><span class="pl-k">new</span> <span class="pl-smi">UserChatMessage</span><span class="pl-kos">(</span><span class="pl-s1">inputText</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-smi">ChatCompletionOptions</span> <span class="pl-s1">chatCompletionOptions</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-smi">ChatCompletionOptions</span><span class="pl-kos">(</span><span class="pl-kos">)</span>
<span class="pl-kos">{</span>
    <span class="pl-s1">Temperature</span> <span class="pl-c1">=</span> <span class="pl-c1">0.7f</span><span class="pl-kos">,</span>
    <span class="pl-s1">MaxOutputTokenCount</span> <span class="pl-c1">=</span> <span class="pl-c1">800</span>
<span class="pl-kos">}</span><span class="pl-kos">;</span>

<span class="pl-smi">ChatCompletion</span> <span class="pl-s1">completion</span> <span class="pl-c1">=</span> <span class="pl-s1">chatClient</span><span class="pl-kos">.</span><span class="pl-en">CompleteChat</span><span class="pl-kos">(</span>
    <span class="pl-s1">messagesList</span><span class="pl-kos">,</span>
    <span class="pl-s1">chatCompletionOptions</span>
<span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-c">// Return the response</span>
<span class="pl-smi">string</span> <span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">completion</span><span class="pl-kos">.</span><span class="pl-s1">Content</span><span class="pl-kos">[</span><span class="pl-c1">0</span><span class="pl-kos">]</span><span class="pl-kos">.</span><span class="pl-s1">Text</span><span class="pl-kos">;</span>

<span class="pl-c">// Add generated text to messages list</span>
<span class="pl-s1">messagesList</span><span class="pl-kos">.</span><span class="pl-en">Add</span><span class="pl-kos">(</span><span class="pl-k">new</span> <span class="pl-smi">AssistantChatMessage</span><span class="pl-kos">(</span><span class="pl-s1">response</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-s1">Console</span><span class="pl-kos">.</span><span class="pl-en">WriteLine</span><span class="pl-kos">(</span><span class="pl-s">"Response: "</span> <span class="pl-c1">+</span> <span class="pl-s1">response</span> <span class="pl-c1">+</span> <span class="pl-s">"<span class="pl-cce">\n</span>"</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container">
 
  </div></div>
<p dir="rtl"><strong>Python</strong>: test-openai-model.py</p>
</li>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="rtl"><pre><span class="pl-c"># Add code to send request...</span>
<span class="pl-c"># Send request to Azure OpenAI model</span>
<span class="pl-s1">messages_array</span>.<span class="pl-c1">append</span>({<span class="pl-s">"role"</span>: <span class="pl-s">"user"</span>, <span class="pl-s">"content"</span>: <span class="pl-s1">input_text</span>})

<span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">client</span>.<span class="pl-c1">chat</span>.<span class="pl-c1">completions</span>.<span class="pl-c1">create</span>(
    <span class="pl-s1">model</span><span class="pl-c1">=</span><span class="pl-s1">azure_oai_deployment</span>,
    <span class="pl-s1">temperature</span><span class="pl-c1">=</span><span class="pl-c1">0.7</span>,
    <span class="pl-s1">max_tokens</span><span class="pl-c1">=</span><span class="pl-c1">1200</span>,
    <span class="pl-s1">messages</span><span class="pl-c1">=</span><span class="pl-s1">messages_array</span>
)
<span class="pl-s1">generated_text</span> <span class="pl-c1">=</span> <span class="pl-s1">response</span>.<span class="pl-c1">choices</span>[<span class="pl-c1">0</span>].<span class="pl-c1">message</span>.<span class="pl-c1">content</span>
<span class="pl-c"># Add generated text to messages array</span>
<span class="pl-s1">messages_array</span>.<span class="pl-c1">append</span>({<span class="pl-s">"role"</span>: <span class="pl-s">"assistant"</span>, <span class="pl-s">"content"</span>: <span class="pl-s1">generated_text</span>})

<span class="pl-c"># Print generated text</span>
<span class="pl-en">print</span>(<span class="pl-s">"Summary: "</span> <span class="pl-c1">+</span> <span class="pl-s1">generated_text</span> <span class="pl-c1">+</span> <span class="pl-s">"<span class="pl-cce">\n</span>"</span>)</pre><div class="zeroclipboard-container">

  </div></div>
</li>
<li>
<p dir="rtl">حفظ الملف. في التعليمات البرمجية التي أضفتها، لاحظ أننا الآن نلحق الإدخال والاستجابة السابقين إلى صفيف المطالبة الذي يسمح للنموذج بفهم محفوظات محادثتنا.</p>
</li>
<li>
<p dir="rtl">في الجزء الطرفي، أدخل الأمر التالي لتشغيل التطبيق.</p>
<ul dir="rtl">
<li><strong>C#:</strong> <code>dotnet run</code></li>
<li><strong>Python</strong>: <code>python test-openai-model.py</code></li>
</ul>
</li>
<li>
<p dir="rtl">شغل التطبيق مرة أخرى وقدم المطالبة <code>Where is a good hike near Boise?</code>.</p>
</li>
<li>
<p dir="rtl">لاحظ الإخراج، ثم استخدم المطالبة <code>How difficult is the second hike you suggested?</code>.</p>
</li>
<li>
<p dir="rtl">من المحتمل أن تحصل على استجابة حول الرفع الثاني الذي اقترحه النموذج، والذي يوفر محادثة أكثر واقعية. يمكنك طرح أسئلة متابعة إضافية تشير إلى الإجابات السابقة، وفي كل مرة توفر المحفوظات سياقاً للنموذج للإجابة عليه.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: تم ضبط عدد رموز الإخراج على 800 فقط، لذا إذا استمرت المحادثة لفترة طويلة، ستنفد الرموز المتاحة للتطبيق، مما يؤدي إلى مطالبة غير مكتملة. في استخدامات الإنتاج، سيساعد تقييد طول المحفوظات على أحدث المدخلات والاستجابات في التحكم في عدد الرموز المميزة المطلوبة.</p>
</blockquote>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">عند الانتهاء من مورد Azure OpenAI، تذكر حذف التوزيع أو المورد بأكمله في <strong>مدخل Microsoft Azure</strong> في <code>https://portal.azure.com</code>.</p>
</article></div>
