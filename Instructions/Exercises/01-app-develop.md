<div class="Box-sc-g0xbh4-0 eoaCFS js-snippet-clipboard-copy-unpositioned undefined" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div dir="auto"><div dir="rtl"><markdown-accessiblity-table data-catalyst=""><table>
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
  <td><div dir="rtl">تطوير التطبيقات باستخدام خدمة Azure OpenAI</div></td>
  <td><div dir="rtl">new</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h1 tabindex="-1" dir="rtl" class="heading-element">تطوير التطبيقات باستخدام خدمة Azure OpenAI</h1><a id="user-content-تطوير-التطبيقات-باستخدام-خدمة-azure-openai" class="anchor" aria-label="Permalink: تطوير التطبيقات باستخدام خدمة Azure OpenAI" href="#تطوير-التطبيقات-باستخدام-خدمة-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تطوير-التطبيقات-باستخدام-خدمة-azure-openai" aria-label="Permalink: تطوير التطبيقات باستخدام خدمة Azure OpenAI" href="#تطوير-التطبيقات-باستخدام-خدمة-azure-openai"></a></div>
<p dir="rtl">باستخدام خدمة Azure OpenAI، يُمكن للمطورين إنشاء روبوتات دردشة وتطبيقات أخرى تتفوق في فهم اللغة البشرية الطبيعية من خلال استخدام REST APIs أو SDKs الخاصة باللغة. عند العمل مع نماذج اللغة هذه، فإن كيفية قيام المطورين بتشكيل مطالباتهم تؤثر بشكل كبير على كيفية استجابة نموذج الذكاء الاصطناعي التوليدي. يمكن لنماذج Azure OpenAI تخصيص المحتوى وتنسيقه، إذا طلب ذلك بطريقة واضحة وموجزة. في هذا التمرين، ستتعلم كيفية ربط تطبيقك بـ Azure OpenAI ورؤية كيف تساعد المطالبات المختلفة للمحتوى المماثل في تشكيل رد نموذج الذكاء الاصطناعي لتلبية متطلباتك بشكل أفضل.</p>
<p dir="rtl">في سيناريو هذا التمرين، ستؤدي دور مطور برامج يعمل على حملة تسويقية للحياة البرية. أنت تستكشف كيفية استخدام الذكاء الاصطناعي التوليدي لتحسين رسائل البريد الإلكتروني الإعلانية وتصنيف المقالات التي قد تنطبق على فريقك. يمكن تطبيق تقنيات هندسة التلقين المستخدمة في التدريب بشكل مماثل لمجموعة متنوعة من حالات الاستخدام.</p>
<p dir="rtl">سيستغرق هذا التدريب حوالي <strong>30</strong> دقيقة.</p>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">استنساخ المستودع لهذه الدورة التدريبية</h2><a id="user-content-استنساخ-المستودع-لهذه-الدورة-التدريبية" class="anchor" aria-label="Permalink: استنساخ المستودع لهذه الدورة التدريبية" href="#استنساخ-المستودع-لهذه-الدورة-التدريبية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-استنساخ-المستودع-لهذه-الدورة-التدريبية" aria-label="Permalink: استنساخ المستودع لهذه الدورة التدريبية" href="#استنساخ-المستودع-لهذه-الدورة-التدريبية"></a></div>
<p dir="rtl">إذا لم تقم بالاستنساخ بالفعل، يجب عليك استنساخ مستودع التعليمات البرمجية لهذه الدورة التدريبية:</p>
<ol dir="rtl">
<li>
<p dir="rtl">ابدأ تشغيل Visual Studio Code.</p>
</li>
<li>
<p dir="rtl">افتح عرض لوحة الأوامر (SHIFT+CTRL+P أو <strong>عرض لوحة الأوامر</strong> &gt; <strong>Command Palette</strong>)، ثم نفّذ أمر <strong>Git: Clone</strong> لاستنساخ المستودع <code>https://github.com/MicrosoftLearning/mslearn-openai</code> إلى مجلد محلي (لا يهم أي مجلد تختاره).</p>
</li>
<li>
<p dir="rtl">عند استنساخ المستودع، افتح المجلد في تعليمة Visual Studio البرمجية.</p>
</li>
<li>
<p dir="rtl">انتظر حتى تثبيت ملفات إضافية لدعم مشاريع التعليمات البرمجية C# في المستودع.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا جرت مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد <strong>ليس الآن</strong>.</p>
</blockquote>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">توفير مورد Azure OpenAI</h2><a id="user-content-توفير-مورد-azure-openai" class="anchor" aria-label="Permalink: توفير مورد Azure OpenAI" href="#توفير-مورد-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-توفير-مورد-azure-openai" aria-label="Permalink: توفير مورد Azure OpenAI" href="#توفير-مورد-azure-openai"></a></div>
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
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">توزيع النموذج</h2><a id="user-content-توزيع-النموذج" class="anchor" aria-label="Permalink: توزيع النموذج" href="#توزيع-النموذج"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-توزيع-النموذج" aria-label="Permalink: توزيع النموذج" href="#توزيع-النموذج"></a></div>
<p dir="rtl">بعد ذلك، ستقوم بتوزيع مورد نموذج Azure OpenAI من Cloud Shell.</p>
<ol dir="rtl">
<li>
<p dir="rtl">استخدم الزر <strong>[&gt;_]</strong> الموجود على يمين شريط البحث أعلى الصفحة لإنشاء Cloud Shell جديد في بوابة Azure، وتحديد بيئة <em><strong>Bash</strong></em>. يوفّر Cloud Shell واجهة سطر أوامر في جزء أسفل بوابة Azure.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا كنت قد أنشأت مسبقًا Cloud Shell يستخدم بيئة <em>PowerShell</em>، فبدّل إلى <em><strong>Bash</strong></em>.</p>
</blockquote>
</li>
<li>
<p dir="rtl">راجع هذا المثال واستبدل المتغيرات التالية بالقيم الخاصة بك من الأعلى:</p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="dotnetcli" class="notranslate"><code>az cognitiveservices account deployment create \
   -g &lt;your_resource_group&gt; \
   -n &lt;your_OpenAI_service&gt; \
   --deployment-name gpt-4o \
   --model-name gpt-4o \
   --model-version 2024-05-13 \
   --model-format OpenAI \
   --sku-name "Standard" \
   --sku-capacity 5
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="az cognitiveservices account deployment create \
   -g <your_resource_group> \
   -n <your_OpenAI_service> \
   --deployment-name gpt-4o \
   --model-name gpt-4o \
   --model-version 2024-05-13 \
   --model-format OpenAI \
   --sku-name &quot;Standard&quot; \
   --sku-capacity 5" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>

</ol>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: يتم قياس سعة Sku بالآلاف من الرموز المميزة في الدقيقة. حد المعدل البالغ 5,000 رمز في الدقيقة يُعد كافيًا تمامًا لإكمال هذا التمرين، مع ترك سعة متاحة لمستخدمين آخرين ضمن نفس الاشتراك.</p>
</blockquote>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">تكوين تطبيقك</h2><a id="user-content-تكوين-تطبيقك" class="anchor" aria-label="Permalink: تكوين تطبيقك" href="#تكوين-تطبيقك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تكوين-تطبيقك" aria-label="Permalink: تكوين تطبيقك" href="#تكوين-تطبيقك"></a></div>
<p dir="rtl">تم توفير تطبيقات لكل من C# وPython، ويمتلك كلا التطبيقين نفس الوظيفة. أولاً، ستكمل بعض الأجزاء الرئيسية من التطبيق لتمكين استخدام مورد Azure OpenAI الخاص بك مع استدعاءات واجهة برمجة التطبيقات (API) غير المتزامنة.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في Visual Studio Code، في جزء <strong>المستكشف</strong>، انتقل إلى المجلد <strong>Labfiles/01-app-develop</strong> ووسّع نطاق المجلد <strong>CSharp</strong> أو <strong>Python</strong> وفقًا لتفضيلات اللغة الخاصة بك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي تريد دمج وظيفة Azure OpenAI فيه.</p>
</li>
<li>
<p dir="rtl">انقر بزر الماوس الأيمن فوق المجلد <strong>CSharp</strong> أو <strong>Python</strong> الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وافتح وحدة طرفية متكاملة. ثم، عليك تثبيت حزمة Azure OpenAI SDK عن طريق تشغيل الأمر المناسب لتفضيل اللغة لديك:</p>
<p dir="auto"><strong>C#:</strong></p>
</li>
<div dir="auto"><pre>dotnet add package Azure.AI.OpenAI <span>--</span>version <span>2.1</span>.<span>0</span></pre><div dir="auto">
  </div></div>
<p dir="rtl">:<strong>Python</strong></p>

<div dir="auto"><pre>pip install openai<span>==</span><span>1.65</span>.<span>2</span></pre><div dir="auto">
  </div></div>

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
<li><strong>اسم عملية النشر</strong> الذي حددته لنشر نموذجك.</li>
</ul>
</li>
<li>
<p dir="rtl">احفظ ملف التكوين.</p>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI</h2><a id="user-content-أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai" class="anchor" aria-label="Permalink: أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI" href="#أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai" aria-label="Permalink: أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI" href="#أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai"></a></div>
<p dir="rtl">أنت الآن جاهز لاستخدام Azure OpenAI SDK لاستهلاك نموذجك الموزع.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في جزء <strong>مستكشف</strong>، في المجلد <strong>CSharp</strong> أو <strong>Python</strong>، افتح ملف التعليمات البرمجية للغة المفضلة لديك، واستبدل التعليق <em><strong>أضف حزمة Azure OpenAI</strong></em> بالتعليمات البرمجية لإضافة مكتبة Azure OpenAI SDK:</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div dir="auto"><pre><span>// Add Azure OpenAI packages</span>
<span>using</span> <span>Azure</span><span>.</span><span>AI</span><span>.</span><span>OpenAI</span><span>;</span>
<span>using</span> <span>OpenAI</span><span>.</span><span>Chat</span><span>;</span></pre><div dir="auto">
  </div></div>
<p dir="rtl"><strong>Python</strong>: application.py</p>
<div dir="auto"><pre><span># Add Azure OpenAI package</span>
<span>from</span> <span>openai</span> <span>import</span> <span>AsyncAzureOpenAI</span></pre><div dir="auto">
  </div></div>

<li>
<p dir="rtl">في ملف التعليمات البرمجية، ابحث عن التعليق <em><strong>تكوين عميل Azure OpenAI</strong></em>، وأضف التعليمات البرمجية لتكوين عميل Azure OpenAI:</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div dir="auto"><pre><span>// Configure the Azure OpenAI client</span>
<span>AzureOpenAIClient</span> <span>azureClient</span> <span>=</span> <span>new</span> <span>(</span><span>new</span> <span>Uri</span><span>(</span><span>oaiEndpoint</span><span>)</span><span>,</span> <span>new</span> <span>ApiKeyCredential</span><span>(</span><span>oaiKey</span><span>)</span><span>)</span><span>;</span>
<span>ChatClient</span> <span>chatClient</span> <span>=</span> <span>azureClient</span><span>.</span><span>GetChatClient</span><span>(</span><span>oaiDeploymentName</span><span>)</span><span>;</span></pre><div dir="auto">
  </div></div>
<p dir="rtl"><strong>Python</strong>: application.py</p>
<div dir="auto"><pre><span># Configure the Azure OpenAI client</span>
<span>client</span> <span>=</span> <span>AsyncAzureOpenAI</span>(
    <span>azure_endpoint</span> <span>=</span> <span>azure_oai_endpoint</span>, 
    <span>api_key</span><span>=</span><span>azure_oai_key</span>,  
    <span>api_version</span><span>=</span><span>"2024-02-15-preview"</span>
)</pre><div dir="auto">
  </div></div>

<li>
<p dir="rtl">في الوظيفة التي تستدعي نموذج Azure OpenAI، ضمن التعليق <em><strong>الحصول على رد من Azure OpenAI</strong></em>، أضف التعليمة البرمجية للتنسيق وأرسل الطلب إلى النموذج.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div dir="auto"><pre><span>// Get response from Azure OpenAI</span>
<span>ChatCompletionOptions</span> <span>chatCompletionOptions</span> <span>=</span> <span>new</span> <span>ChatCompletionOptions</span><span>(</span><span>)</span>
<span>{</span>
    <span>Temperature</span> <span>=</span> <span>0.7f</span><span>,</span>
    <span>MaxOutputTokenCount</span> <span>=</span> <span>800</span>
<span>}</span><span>;</span>
<p dir="auto"><span>ChatCompletion</span> <span>completion</span> <span>=</span> <span>chatClient</span><span>.</span><span>CompleteChat</span><span>(</span>
<span>[</span>
<span>new</span> <span>SystemChatMessage</span><span>(</span><span>systemMessage</span><span>)</span><span>,</span>
<span>new</span> <span>UserChatMessage</span><span>(</span><span>userMessage</span><span>)</span>
<span>]</span><span>,</span>
<span>chatCompletionOptions</span>
<span>)</span><span>;</span></p>
<p dir="auto"><span>Console</span><span>.</span><span>WriteLine</span><span>(</span><span><span>$</span>"<span>{</span><span>completion</span><span>.</span><span>Role</span><span>}</span>: <span>{</span><span>completion</span><span>.</span><span>Content</span><span>[</span><span>0</span><span>]</span><span>.</span><span>Text</span><span>}</span>"</span><span>)</span><span>;</span></p></pre><div dir="auto"><p dir="auto"></p>
  </div></div>
<p dir="rtl"><strong>Python</strong>: application.py</p>
<div dir="auto"><pre><span># Get response from Azure OpenAI</span>
<span>messages</span> <span>=</span>[
    {<span>"role"</span>: <span>"system"</span>, <span>"content"</span>: <span>system_message</span>},
    {<span>"role"</span>: <span>"user"</span>, <span>"content"</span>: <span>user_message</span>},
]
<p dir="auto"><span>print</span>(<span>"<span>\n</span>Sending request to Azure OpenAI model...<span>\n</span>"</span>)</p>
<p dir="auto"><span># Call the Azure OpenAI model</span>
<span>response</span> <span>=</span> <span>await</span> <span>client</span>.<span>chat</span>.<span>completions</span>.<span>create</span>(
<span>model</span><span>=</span><span>model</span>,
<span>messages</span><span>=</span><span>messages</span>,
<span>temperature</span><span>=</span><span>0.7</span>,
<span>max_tokens</span><span>=</span><span>800</span>
)</p></pre><div dir="auto"><p dir="auto"></p>
  </div></div>

<li>
<p dir="rtl">احفظ التغييرات في ملف التعليمة البرمجية.</p>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">تشغيل التطبيق الخاص بك</h2><a id="user-content-تشغيل-التطبيق-الخاص-بك" class="anchor" aria-label="Permalink: تشغيل التطبيق الخاص بك" href="#تشغيل-التطبيق-الخاص-بك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تشغيل-التطبيق-الخاص-بك" aria-label="Permalink: تشغيل التطبيق الخاص بك" href="#تشغيل-التطبيق-الخاص-بك"></a></div>
<p dir="rtl">الآن بعد أن نجح تكوين التطبيق الخاص بك، عليك تشغيله لإرسال طلبك إلى النموذج الخاص بك ومراقبة الاستجابة. ستلاحظ أن الفرق الوحيد بين الخيارات المختلفة هو محتوى المطالبة، وتظل جميع المعلمات الأخرى (مثل عدد الرموز المميزة ودرجة الحرارة) كما هي لكل طلب.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في مجلد اللغة المفضلة لديك، افتح <code>system.txt</code> في Visual Studio Code. لكل من التفاعلات، ستقوم بإدخال <strong>رسالة النظام</strong> في هذا الملف وحفظها. سيتوقف كل تكرار مؤقتاً أولاً لتغيير رسالة النظام.</p>
</li>
<li>
<p dir="rtl">في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.</p>
<ul dir="rtl">
<li><strong>C#:</strong> <code>dotnet run</code></li>
<li><strong>Python</strong>: <code>python application.py</code></li>
</ul>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يمكنك استخدام أيقونة <strong>تكبير حجم اللوحة</strong> (<strong>^</strong>) في شريط أدوات المحطة الطرفية لرؤية المزيد من نص وحدة التحكم.</p>
</blockquote>
</li>
<li>
<p dir="rtl">بالنسبة للتكرار الأول، أدخل المطالبات التالية:</p>
<p dir="rtl"><strong>رسالة النظام</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>You are an AI assistant
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="You are an AI assistant" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
    
      
    

      
    

    
  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>

<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>Write an intro for a new wildlife Rescue
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="Write an intro for a new wildlife Rescue" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
    
      
    

      
    

    
  </div></div>

<li>
<p dir="rtl">مراقبة المخرجات. ومن المرجح أن ينتج نموذج الذكاء الاصطناعي مقدمة عامة جيدة حول إنقاذ الحياة البرية.</p>
</li>
<li>
<p dir="rtl">بعد ذلك، أدخل المطالبات التالية التي تحدد تنسيقاً للاستجابة:</p>
<p dir="rtl"><strong>رسالة النظام</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>You are an AI assistant helping to write emails
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="You are an AI assistant helping to write emails" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
    
      
    

      
    

    
  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>

<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>Write a promotional email for a new wildlife rescue, including the following: 
- Rescue name is Contoso 
- It specializes in elephants 
- Call for donations to be given at our website
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="Write a promotional email for a new wildlife rescue, including the following: 
- Rescue name is Contoso 
- It specializes in elephants 
- Call for donations to be given at our website" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
    
      
    

      
    

    
  </div></div>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: قد تجد أن الكتابة التلقائية في الجهاز الظاهري (VM) لا تعمل بشكل جيد مع المطالبات التي تتكون من عدة أسطر. إذا كانت هذه هي مشكلتك، فانسخ المطالبة بأكملها ثم الصقها في التعليمة البرمجية لـ Visual Studio.</p>
</blockquote>

<li>
<p dir="rtl">مراقبة المخرجات. في هذه المرة، من المحتمل أن ترى تنسيق رسالة بريد إلكتروني تتضمن الحيوانات المحددة، بالإضافة إلى دعوة للتبرعات.</p>
</li>
<li>
<p dir="rtl">وبعد ذلك، أدخل المطالبات التالية التي تحدد المحتوى بالإضافة إلى ذلك:</p>
<p dir="rtl"><strong>رسالة النظام</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>You are an AI assistant helping to write emails
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="You are an AI assistant helping to write emails" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
    
      
    

      
    

    
  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>

<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>Write a promotional email for a new wildlife rescue, including the following: 
- Rescue name is Contoso 
- It specializes in elephants, as well as zebras and giraffes 
- Call for donations to be given at our website 
Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits.
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="Write a promotional email for a new wildlife rescue, including the following: 
- Rescue name is Contoso 
- It specializes in elephants, as well as zebras and giraffes 
- Call for donations to be given at our website 
Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits." tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
    
      
    

      
    

    
  </div></div>

<li>
<p dir="rtl">لاحظ النتائج، وشاهد كيفية تغيير البريد الإلكتروني استناداً إلى الإرشادات الواضحة.</p>
</li>
<li>
<p dir="rtl">بعد ذلك، أدخل المطالبات التالية حيث نضيف تفاصيل حول النبرة إلى رسالة النظام:</p>
<p dir="rtl"><strong>رسالة النظام</strong></p>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>You are an AI assistant that helps write promotional emails to generate interest in a new business. Your tone is light, chit-chat oriented and you always include at least two jokes.
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="You are an AI assistant that helps write promotional emails to generate interest in a new business. Your tone is light, chit-chat oriented and you always include at least two jokes." tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
    
      
    

      
    

    
  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>Write a promotional email for a new wildlife rescue, including the following: 
- Rescue name is Contoso 
- It specializes in elephants, as well as zebras and giraffes 
- Call for donations to be given at our website 
Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits.
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="Write a promotional email for a new wildlife rescue, including the following: 
- Rescue name is Contoso 
- It specializes in elephants, as well as zebras and giraffes 
- Call for donations to be given at our website 
Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits." tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>

<li>
<p dir="rtl">مراقبة المخرجات. وفي هذه المرة، من المحتمل أن ترى البريد الإلكتروني بتنسيق مماثل، ولكن بنبرة غير رسمية أكثر بكثير. من المحتمل أن ترى النكات مضمنة!</p>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">استخدم السياق الأساسي واحتفظ بسجل المحادثة.</h2><a id="user-content-استخدم-السياق-الأساسي-واحتفظ-بسجل-المحادثة" class="anchor" aria-label="Permalink: استخدم السياق الأساسي واحتفظ بسجل المحادثة." href="#استخدم-السياق-الأساسي-واحتفظ-بسجل-المحادثة"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-استخدم-السياق-الأساسي-واحتفظ-بسجل-المحادثة" aria-label="Permalink: استخدم السياق الأساسي واحتفظ بسجل المحادثة." href="#استخدم-السياق-الأساسي-واحتفظ-بسجل-المحادثة"></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">في التكرار الأخير، ننتقل بعيدًا عن توليد البريد الإلكتروني ونستكشف <em>السياق الأساسي</em> والحفاظ على سجل المحادثة. هنا يمكنك توفير رسالة نظام بسيطة، وتغيير التطبيق لتوفير السياق الأساسي كبداية لمطالبة المستخدم. وبعد ذلك، سيُلحق التطبيق إدخال المستخدم، واستخراج المعلومات من السياق الأساسي للرد على مطالبة المستخدم.</p>
</li>
<li>
<p dir="rtl">افتح الملف <code>grounding.txt</code> واقرأ بإيجاز السياق الأساسي الذي ستقوم بإدراجه.</p>
</li>
<li>
<p dir="rtl">في تطبيقك مباشرة بعد <em><strong>تنسيق التعليق وإرسال الطلب إلى النموذج</strong></em> وقبل أي تعليمات برمجية موجودة، أضف القصاصة البرمجية التالية لقراءة النص من <code>grounding.txt</code> لزيادة مطالبة المستخدم بالسياق الأساسي.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div dir="auto"><pre><span>// Initialize messages list</span>
<span>Console</span><span>.</span><span>WriteLine</span><span>(</span><span>"<span>\n</span>Adding grounding context from grounding.txt"</span><span>)</span><span>;</span>
<span>string</span> <span>groundingText</span> <span>=</span> <span>System</span><span>.</span><span>IO</span><span>.</span><span>File</span><span>.</span><span>ReadAllText</span><span>(</span><span>"grounding.txt"</span><span>)</span><span>;</span>
<span>var</span> <span>messagesList</span> <span>=</span> <span>new</span> <span>List</span><span>&lt;</span><span>ChatMessage</span><span>&gt;</span><span>(</span><span>)</span>
<span>{</span>
    <span>new</span> <span>UserChatMessage</span><span>(</span><span>groundingText</span><span>)</span><span>,</span>
<span>}</span><span>;</span></pre><div dir="auto">
  </div></div>
<p dir="rtl"><strong>Python</strong>: application.py</p>

<div dir="auto"><pre><span># Initialize messages array</span>
<span>print</span>(<span>"<span>\n</span>Adding grounding context from grounding.txt"</span>)
<span>grounding_text</span> <span>=</span> <span>open</span>(<span>file</span><span>=</span><span>"grounding.txt"</span>, <span>encoding</span><span>=</span><span>"utf8"</span>).<span>read</span>().<span>strip</span>()
<span>messages_array</span> <span>=</span> [{<span>"role"</span>: <span>"user"</span>, <span>"content"</span>: <span>grounding_text</span>}]</pre><div dir="auto">
  </div></div>

<li>
<p dir="rtl">ضمن التعليق <em><strong>أضف تعليمة برمجية لإرسال الطلب...</strong></em>، استبدل كل التعليمة البرمجية من التعليق <strong>حتى</strong> نهاية الحلقة يالتعليمة البرمجية التالية ثم احفظ الملف. التعليمة البرمجية هي نفسها في الغالب، ولكن الآن تستخدم صفيف الرسائل لإرسال الطلب إلى النموذج.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div dir="auto"><pre><span>// Format and send the request to the model</span>
<span>messagesList</span><span>.</span><span>Add</span><span>(</span><span>new</span> <span>SystemChatMessage</span><span>(</span><span>systemMessage</span><span>)</span><span>)</span><span>;</span>
<span>messagesList</span><span>.</span><span>Add</span><span>(</span><span>new</span> <span>UserChatMessage</span><span>(</span><span>userMessage</span><span>)</span><span>)</span><span>;</span>
<span>GetResponseFromOpenAI</span><span>(</span><span>messagesList</span><span>)</span><span>;</span></pre><div dir="auto">
  </div></div>
<p dir="rtl"><strong>Python</strong>: application.py</p>

<div dir="auto"><pre><span># Format and send the request to the model</span>
<span>messages_array</span>.<span>append</span>({<span>"role"</span>: <span>"system"</span>, <span>"content"</span>: <span>system_text</span>})
<span>messages_array</span>.<span>append</span>({<span>"role"</span>: <span>"user"</span>, <span>"content"</span>: <span>user_text</span>})
<span>await</span> <span>call_openai_model</span>(<span>messages</span><span>=</span><span>messages_array</span>, 
    <span>model</span><span>=</span><span>azure_oai_deployment</span>, 
    <span>client</span><span>=</span><span>client</span>
)</pre><div dir="auto">
  </div></div>

<li>
<p dir="rtl">ضمن التعليق <em><strong>تعريف الدالة التي ستجلب الاستجابة من نقطة نهاية Azure OpenAI</strong></em>، استبدل تعريف الدالة بالتعليمة البرمجية التالية لاستخدام قائمة سجل المحادثة عند استدعاء الدالة <code>GetResponseFromOpenAI</code> للغة C# أو <code>call_openai_model</code> للغة Python.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div dir="auto"><pre><span>// Define the function that gets the response from Azure OpenAI endpoint</span>
<span>private</span> <span><span>static</span></span> <span>void</span> <span>GetResponseFromOpenAI</span><span>(</span><span>List</span><span>&lt;</span><span>ChatMessage</span><span>&gt;</span> <span>messagesList</span><span>)</span><span></span></pre><div dir="auto">
  </div></div>
<p dir="rtl"><strong>Python</strong>: application.py</p>

<div dir="auto"><pre><span># Define the function that will get the response from Azure OpenAI endpoint</span>
<span>async</span> <span>def</span> <span>call_openai_model</span>(<span>messages</span>, <span>model</span>, <span>client</span>):</pre><div dir="auto">
  </div></div>

<li>
<p dir="rtl">وأخيرا، استبدل جميع التعليمات البرمجية ضمن <em><strong>الحصول على استجابة من Azure OpenAI</strong></em>. التعليمة البرمجية هي نفسها في الغالب، ولكن الآن تستخدم صفيف الرسائل لتخزين محفوظات المحادثات.</p>
<p dir="rtl"><strong>C#</strong>: Program.cs</p>
</li>
<div dir="auto"><pre><span>// Get response from Azure OpenAI</span>
<span>ChatCompletionOptions</span> <span>chatCompletionOptions</span> <span>=</span> <span>new</span> <span>ChatCompletionOptions</span><span>(</span><span>)</span>
<span>{</span>
    <span>Temperature</span> <span>=</span> <span>0.7f</span><span>,</span>
    <span>MaxOutputTokenCount</span> <span>=</span> <span>800</span>
<span>}</span><span>;</span>
<p dir="auto"><span>ChatCompletion</span> <span>completion</span> <span>=</span> <span>chatClient</span><span>.</span><span>CompleteChat</span><span>(</span>
<span>messagesList</span><span>,</span>
<span>chatCompletionOptions</span>
<span>)</span><span>;</span></p>
<p dir="auto"><span>Console</span><span>.</span><span>WriteLine</span><span>(</span><span><span>$</span>"<span>{</span><span>completion</span><span>.</span><span>Role</span><span>}</span>: <span>{</span><span>completion</span><span>.</span><span>Content</span><span>[</span><span>0</span><span>]</span><span>.</span><span>Text</span><span>}</span>"</span><span>)</span><span>;</span>
<span>messagesList</span><span>.</span><span>Add</span><span>(</span><span>new</span> <span>AssistantChatMessage</span><span>(</span><span>completion</span><span>.</span><span>Content</span><span>[</span><span>0</span><span>]</span><span>.</span><span>Text</span><span>)</span><span>)</span><span>;</span></p></pre><div dir="auto"><p dir="auto"></p>
  </div></div>
<p dir="rtl"><strong>Python</strong>: application.py</p>

<div dir="auto"><pre><span># Get response from Azure OpenAI</span>
<span>print</span>(<span>"<span>\n</span>Sending request to Azure OpenAI model...<span>\n</span>"</span>)
<p dir="auto"><span># Call the Azure OpenAI model</span>
<span>response</span> <span>=</span> <span>await</span> <span>client</span>.<span>chat</span>.<span>completions</span>.<span>create</span>(
<span>model</span><span>=</span><span>model</span>,
<span>messages</span><span>=</span><span>messages</span>,
<span>temperature</span><span>=</span><span>0.7</span>,
<span>max_tokens</span><span>=</span><span>800</span>
)</p>
<p dir="auto"><span>print</span>(<span>"Response:<span>\n</span>"</span> <span>+</span> <span>response</span>.<span>choices</span>[<span>0</span>].<span>message</span>.<span>content</span> <span>+</span> <span>"<span>\n</span>"</span>)
<span>messages</span>.<span>append</span>({<span>"role"</span>: <span>"assistant"</span>, <span>"content"</span>: <span>response</span>.<span>choices</span>[<span>0</span>].<span>message</span>.<span>content</span>})</p></pre><div dir="auto"><p dir="auto"></p>
  </div></div>

<li>
<p dir="rtl">احفظ الملف وأعد تشغيل التطبيق.</p>
</li>
<li>
<p dir="rtl">أدخل المطالبات التالية (مع استمرار إدخال <strong>رسالة النظام</strong> وحفظها في <code>system.txt</code>).</p>
<p dir="rtl"><strong>رسالة النظام</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>You're an AI assistant who helps people find information. You'll provide answers from the text provided in the prompt, and respond concisely.
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="You're an AI assistant who helps people find information. You'll provide answers from the text provided in the prompt, and respond concisely." tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
    
      
    

      
    

    
  </div></div>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>

<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>What animal is the favorite of children at Contoso?
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="What animal is the favorite of children at Contoso?" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>
<p dir="rtl">لاحظ أن النموذج يستخدم معلومات النص المرجعي للإجابة على سؤالك.</p>

<li>
<p dir="rtl">دون تغيير رسالة النظام، أدخل المطالبة التالية كرسالة من المستخدم:</p>
<p dir="rtl"><strong>رسالة المستخدم:</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="prompt" class="notranslate"><code>How can they interact with it at Contoso?
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="How can they interact with it at Contoso?" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>
<p dir="rtl">لاحظ أن النموذج يتعرف على "هم" على أنهم الأطفال، و"هو" على أنه الحيوان المفضل لديهم، وذلك لأنه يمتلك الآن إمكانية الوصول إلى سؤالك السابق ضمن سجل المحادثة.</p>

</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تنظيف" aria-label="Permalink: تنظيف" href="#تنظيف"></a></div>
<p dir="rtl">عند الانتهاء من مورد Azure OpenAI، تذكر حذف التوزيع أو المورد بأكمله في <strong>مدخل Microsoft Azure</strong> في <code>https://portal.azure.com</code>.</p>
</div></div>
</article></div>
