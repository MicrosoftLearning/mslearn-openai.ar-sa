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
  <td><div dir="rtl">تنفيذ استرداد الجيل المعزز (RAG) باستخدام خدمة Azure OpenAI</div></td>
  <td><div dir="rtl">new</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h1 tabindex="-1" dir="rtl" class="heading-element">تنفيذ استرداد الجيل المعزز (RAG) باستخدام خدمة Azure OpenAI</h1><a id="user-content-تنفيذ-استرداد-الجيل-المعزز-rag-باستخدام-خدمة-azure-openai" class="anchor" aria-label="Permalink: تنفيذ استرداد الجيل المعزز (RAG) باستخدام خدمة Azure OpenAI" href="#تنفيذ-استرداد-الجيل-المعزز-rag-باستخدام-خدمة-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تنفيذ-استرداد-الجيل-المعزز-rag-باستخدام-خدمة-azure-openai" aria-label="Permalink: تنفيذ استرداد الجيل المعزز (RAG) باستخدام خدمة Azure OpenAI" href="#تنفيذ-استرداد-الجيل-المعزز-rag-باستخدام-خدمة-azure-openai"></a></div>
<p dir="rtl">تمكنك خدمة Azure OpenAI من استخدام بياناتك الخاصة مع ذكاء LLM الأساسي. يمكنك تقييد النموذج لاستخدام بياناتك فقط للمواضيع ذات الصلة، أو مزجها مع النتائج من النموذج المدرب مسبقاً.</p>
<p dir="rtl">في سيناريو هذا التمرين، ستؤدي دور مطور برامج يعمل لدى Margie's Travel Agency. ستكتشف كيفية استخدام بحث الذكاء الاصطناعي في Azure لفهرسة بياناتك واستخدامها مع Azure OpenAI لزيادة المطالبات.</p>
<p dir="rtl">سيستغرق هذا التدريب حوالي <strong>30</strong> دقيقة.</p>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">تزويد موارد Azure</h2><a id="user-content-تزويد-موارد-azure" class="anchor" aria-label="Permalink: تزويد موارد Azure" href="#تزويد-موارد-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تزويد-موارد-azure" aria-label="Permalink: تزويد موارد Azure" href="#تزويد-موارد-azure"></a></div>
<p dir="rtl">لإكمال هذا التدريب، ستحتاج إلى:</p>
<ul dir="rtl">
<li>مورد Azure OpenAI.</li>
<li>مورد بحث الذكاء الاصطناعي في Azure</li>
<li>مورد حساب تخزين Azure.</li>
</ul>
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
<p dir="rtl">أثناء توفير مورد Azure OpenAI، قم بإنشاء <strong>مورد بحث بالذكاء الاصطناعي في Azure</strong> بالإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>الاشتراك</strong>: <em>الاشتراك الذي قمت بتوفير مورد Azure OpenAI فيه</em></li>
<li><strong>مجموعة الموارد</strong>: <em>مجموعة الموارد التي وفرت مورد Azure OpenAI الخاص بك فيها</em></li>
<li><strong>الاسم الخدمة</strong>: <em>اسم فريد من اختيارك</em></li>
<li><strong>الموقع</strong>: <em>المنطقة التي وفرت مورد Azure OpenAI الخاصة بك فيها</em></li>
<li><strong>مستوى التسعير</strong>: أساسي</li>
</ul>
</li>
<li>
<p dir="rtl">أثناء توفير مورد بحث الذكاء الاصطناعي في Azure، قم بإنشاء مورد <strong>حساب تخزين</strong> بالإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>الاشتراك</strong>: <em>الاشتراك الذي قمت بتوفير مورد Azure OpenAI فيه</em></li>
<li><strong>مجموعة الموارد</strong>: <em>مجموعة الموارد التي وفرت مورد Azure OpenAI الخاص بك فيها</em></li>
<li><strong>اسم حساب التخزين</strong>: <em>اسم فريدمن اختيارك</em></li>
<li><strong>المنطقة</strong>: <em>المنطقة التي وفرت موارد Azure OpenAI الخاصة بك فيها</em></li>
<li><strong>الخدمة الأساسية</strong>: تخزين Azure الكائن الثنائي كبير الحجم BLOB أوAzure Data Lake Storage Gen 2</li>
<li><strong>الأداء:</strong> قياسي</li>
<li><strong>التكرار</strong>: التخزين المتكرر محليًا (LRS)</li>
</ul>
</li>
<li>
<p dir="rtl">بعد توزيع جميع الموارد الثلاثة بنجاح في اشتراك Azure، راجعها في بوابة Azure واجمع المعلومات التالية (التي ستحتاج إليها لاحقًا في التدريب):</p>
<ul dir="rtl">
<li><strong>نقطة النهاية</strong> و<strong>مفتاح</strong> من مورد Azure OpenAI الذي أنشأته (متوفر في صفحة <strong>المفاتيح ونقطة النهاية</strong> لمورد Azure OpenAI الخاص بك في مدخل Microsoft Azure)</li>
<li>نقطة النهاية لخدمة البحث بالذكاء الاصطناعي في Azure الخاصة بك (قيمة عنوان <strong>URL</strong> في صفحة النظرة العامة لمورد البحث بالذكاء الاصطناعي في Azure في بوابة Azure).</li>
<li>يكون <strong>مفتاح المسؤول الأساسي</strong> لمورد البحث بالذكاء الاصطناعي في Azure (متوفر في صفحة <strong>المفاتيح</strong> لمورد البحث بالذكاء الاصطناعي في Azure في بوابة Azure).</li>
</ul>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">تحميل بياناتك</h2><a id="user-content-تحميل-بياناتك" class="anchor" aria-label="Permalink: تحميل بياناتك" href="#تحميل-بياناتك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تحميل-بياناتك" aria-label="Permalink: تحميل بياناتك" href="#تحميل-بياناتك"></a></div>
<p dir="rtl">ستقوم بإبطال المطالبات التي تستخدمها مع نموذج الذكاء الاصطناعي التوليدي باستخدام بياناتك الخاصة. في هذا التدريب، تتكون البيانات من مجموعة من كتيبات السفر من شركة <em>Margies Travel</em> الخيالية.</p>
<ol dir="rtl">
<li>في علامة تبويب مستعرض جديدة، يمكنك تنزيل أرشيف بيانات الكتيب من <code>https://aka.ms/own-data-brochures</code>. استخرج الكتيبات إلى مجلد على جهاز الكمبيوتر الخاص بك.</li>
<li>في بوابة Azure، انتقل إلى حساب التخزين الخاص بك، وقم بعرض صفحة <strong>مستعرض التخزين</strong></li>
<li>حدد <strong>حاويات الكائن الثنائي كبير الحجم</strong> ثم أضف حاوية جديدة باسم <code>margies-travel</code>.</li>
<li>حدد حاوية<strong>margies-travel</strong>، ثم قم بتحميل الكتيبات بتنسيق .pdf التي قمت باستخراجها مسبقًا إلى المجلد الجذر لحاوية الكائن الثنائي كبير الحجم.</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">توزيع نماذج الذكاء الاصطناعي</h2><a id="user-content-توزيع-نماذج-الذكاء-الاصطناعي" class="anchor" aria-label="Permalink: توزيع نماذج الذكاء الاصطناعي" href="#توزيع-نماذج-الذكاء-الاصطناعي"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-توزيع-نماذج-الذكاء-الاصطناعي" aria-label="Permalink: توزيع نماذج الذكاء الاصطناعي" href="#توزيع-نماذج-الذكاء-الاصطناعي"></a></div>
<p dir="rtl">ستستخدم نموذجين للذكاء الاصطناعي في هذا التدريب:</p>
<ul dir="rtl">
<li>نص يتضمن نموذج <em>لتحويل</em> النص في الكتيبات إلى رموز بحيث يمكن فهرسته بكفاءة للاستخدام في المطالبات الأساسية.</li>
<li>نموذج GPT الذي يمكن لتطبيقك استخدامه لإنشاء استجابات للمطالبات المستندة إلى بياناتك.</li>
</ul>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">توزيع النموذج</h2><a id="user-content-توزيع-النموذج" class="anchor" aria-label="Permalink: توزيع النموذج" href="#توزيع-النموذج"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-توزيع-النموذج" aria-label="Permalink: توزيع النموذج" href="#توزيع-النموذج"></a></div>
<p dir="rtl">بعد ذلك، ستقوم بتوزيع نماذج Azure OpenAI من Cloud Shell.</p>
<ol dir="rtl">
<li>
<p dir="rtl">استخدم الزر <strong>[&gt;_]</strong> الموجود على يمين شريط البحث أعلى الصفحة لإنشاء Cloud Shell جديد في بوابة Azure، وتحديد بيئة <em><strong>Bash</strong></em>. يوفّر Cloud Shell واجهة سطر أوامر في جزء أسفل بوابة Azure.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا كنت قد أنشأت مسبقًا Cloud Shell يستخدم بيئة <em>PowerShell</em>، فبدّل إلى <em><strong>Bash</strong></em>.</p>
</blockquote>
</li>
</ol>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="dotnetcli" class="notranslate"><code>az cognitiveservices account deployment create \
   -g &lt;your_resource_group&gt; \
   -n &lt;your_OpenAI_resource&gt; \
   --deployment-name text-embedding-ada-002 \
   --model-name text-embedding-ada-002 \
   --model-version "2"  \
   --model-format OpenAI \
   --sku-name "Standard" \
   --sku-capacity 5
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="az cognitiveservices account deployment create \
   -g <your_resource_group> \
   -n <your_OpenAI_resource> \
   --deployment-name text-embedding-ada-002 \
   --model-name text-embedding-ada-002 \
   --model-version &quot;2&quot;  \
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
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: يتم قياس سعة Sku بالآلاف من الرموز المميزة في الدقيقة. حد المعدل البالغ 5,000 رمز في الدقيقة يُعد كافيًا تمامًا لإكمال هذا التمرين، مع ترك سعة متاحة لمستخدمين آخرين ضمن نفس الاشتراك.</p>
</blockquote>
<p dir="rtl">بعد نشر نموذج تضمين النصوص، أنشئ عملية نشر جديدة لنموذج <strong>gpt-4o</strong> بالإعدادات التالية:</p>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="dotnetcli" class="notranslate"><code>az cognitiveservices account deployment create \
   -g &lt;your_resource_group&gt; \
   -n &lt;your_OpenAI_resource&gt; \
   --deployment-name gpt-4o \
   --model-name gpt-4o \
   --model-version "2024-05-13" \
   --model-format OpenAI \
   --sku-name "Standard" \
   --sku-capacity 5
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="az cognitiveservices account deployment create \
   -g <your_resource_group> \
   -n <your_OpenAI_resource> \
   --deployment-name gpt-4o \
   --model-name gpt-4o \
   --model-version &quot;2024-05-13&quot; \
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
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">إنشاء فهرس</h2><a id="user-content-إنشاء-فهرس" class="anchor" aria-label="Permalink: إنشاء فهرس" href="#إنشاء-فهرس"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-إنشاء-فهرس" aria-label="Permalink: إنشاء فهرس" href="#إنشاء-فهرس"></a></div>
<p dir="rtl">لتسهيل استخدام بياناتك الخاصة في مطالبة، ستقوم بفهرستها باستخدام البحث بالذكاء الاصطناعي في Azure. ستستخدم نموذج تضمين النص لتحويل بيانات النص إلى <em>متجهات</em> (مما يؤدي إلى تمثيل كل رمز مميّز نصي في الفهرس بواسطة متجهات رقمية - مما يجعله متوافقًا مع الطريقة التي يمثل بها نموذج الذكاء الاصطناعي التوليدي النص)</p>
<ol dir="rtl">
<li>في بوابة Azure، انتقل إلى مورد البحث بالذكاء الاصطناعي في Azure.</li>
<li>ثم، في صفحة <strong>نظرة عامة</strong> حدد <strong>استيراد البيانات ثم حوّل البيانات إلى رموز</strong>.</li>
<li>في صفحة <strong>إعداد اتصال البيانات</strong>، حدد <strong>تخزين الكائن الثنائي كبير الحجم في Azure</strong> وقم بتكوين مصدر البيانات بالإعدادات التالية:
<ul dir="rtl">
<li><strong>الاشتراك</strong>: اشتراك Azure الذي قمت بتوفير حساب التخزين الخاص بك فيه.</li>
<li><strong>حساب تخزين الكائن الثنائي كبير الحجم</strong>: حساب التخزين الذي قمت بإنشائه سابقًا.</li>
<li><strong>حاوية الكائن الثنائي كبير الحجم</strong>: margies-travel</li>
<li><strong>مجلد الكائن الثنائي كبير الحجم</strong>: <em>اترك هذا فارغًا</em></li>
<li><strong>تمكين تعقب الحذف</strong>: إلغاء التحديد</li>
<li><strong>المصادقة باستخدام الهوية المُدارة</strong>: إلغاء التحديد</li>
</ul>
</li>
<li>في صفحة <strong>تحويل نصك إلى رموز</strong>، حدد الإعدادات التالية:
<ul dir="rtl">
<li><strong>النوع</strong>: Azure OpenAI</li>
<li><strong>الاشتراك</strong>: اشتراك Azure الذي قمت بتوفير خدمة Azure OpenAI الخاصة بك فيه.</li>
<li><strong>خدمة Azure OpenAI</strong>: مورد خدمة Azure OpenAI الخاصة بك</li>
<li><strong>توزيع النموذج</strong>: text-embedding-ada-002</li>
<li><strong>نوع المصادقة</strong>: مفتاح API</li>
<li><strong>أقر بأن الاتصال بخدمة Azure OpenAI سيتكلف رسومًا إضافية على حسابي</strong>: تحديد</li>
</ul>
</li>
<li>في الصفحة التالية، <strong>لا</strong> تحدد خيار تحويل الصور إلى رموز أو استخراج البيانات باستخدام مهارات الذكاء الاصطناعي.</li>
<li>في الصفحة التالية، قم بتمكين الترتيب الدلالي وجدولة المفهرس للتشغيل مرة واحدة.</li>
<li>في الصفحة الأخيرة، قم بتعيين <strong>بادئة اسم الغرض</strong> إلى <code>margies-index</code> ثم قم بإنشاء الفهرس.</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية</h2><a id="user-content-الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية" class="anchor" aria-label="Permalink: الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية" href="#الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية" aria-label="Permalink: الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية" href="#الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية"></a></div>
<p dir="rtl">لنستكشف الآن استخدام بياناتك الخاصة في تطبيق يستخدم SDK لخدمة Azure OpenAI. ستقوم بتطوير تطبيقك باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في مستودع GitHub.</p>
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
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">تكوين تطبيقك</h2><a id="user-content-تكوين-تطبيقك" class="anchor" aria-label="Permalink: تكوين تطبيقك" href="#تكوين-تطبيقك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تكوين-تطبيقك" aria-label="Permalink: تكوين تطبيقك" href="#تكوين-تطبيقك"></a></div>
<p dir="rtl">التطبيقات لكل من C# وPython متوفرة، ويمتلك كلا التطبيقين الوظيفة نفسها. أولاً، ستكمل بعض الأجزاء الرئيسية من التطبيق لتمكين استخدام مورد Azure OpenAI الخاص بك.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في Visual Studio Code، في جزء <strong>المستكشف</strong>، انتقل إلى المجلد <strong>Labfiles/02-use-own-data</strong> ووسّع نطاق المجلد <strong>CSharp</strong> أو <strong>Python</strong> وفقًا لتفضيلات اللغة الخاصة بك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي ستدمج وظيفة Azure OpenAI فيه.</p>
</li>
<li>
<p dir="rtl">انقر بزر الماوس الأيمن فوق المجلد <strong>CSharp</strong> أو <strong>Python</strong> الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وافتح محطة طرفية متكاملة. ثم، عليك تثبيت حزمة Azure OpenAI SDK عن طريق تشغيل الأمر المناسب لتفضيل اللغة لديك:</p>
<p dir="auto"><strong>C#:</strong></p>
</li>
<div dir="auto"><pre>dotnet add package Azure.AI.OpenAI <span>--</span>version <span>2.1</span>.<span>0</span>
dotnet add package Azure.Search.Documents <span>--</span>version <span>11.6</span>.<span>0</span></pre><div dir="auto">
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
<li>اسم <strong>النشر</strong> الذي حددته لنشر نموذج gpt-4o (يجب أن يكون <code>gpt-4o</code>).</li>
<li>نقطة النهاية لخدمة البحث الخاصة بك (قيمة عنوان <strong>URL</strong> في صفحة النظرة العامة لمورد البحث الخاص بك في مدخل Azure).</li>
<li><strong>مفتاح</strong> لمورد البحث لديك (متوفر في صفحة <strong>المفاتيح</strong> لمورد البحث في مدخل Azure - يمكنك استخدام أي من مفاتيح المسؤول)</li>
<li>اسم فهرس البحث (الذي يجب أن يكون <code>margies-index</code>).</li>
</ul>
</li>
<li>
<p dir="rtl">احفظ ملف التكوين.</p>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h3 tabindex="-1" dir="rtl" class="heading-element">أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI</h3><a id="user-content-أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai" class="anchor" aria-label="Permalink: أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI" href="#أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai" aria-label="Permalink: أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI" href="#أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai"></a></div>
<p dir="rtl">أنت الآن جاهز لاستخدام Azure OpenAI SDK لاستهلاك نموذجك الموزع.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في جزء <strong>Explorer</strong>، داخل مجلد <strong>CSharp</strong> أو <strong>Python</strong>، افتح ملف الشيفرة للغة التي تفضلها، واستبدل التعليق <em><strong>تكوين مصدر بياناناتك</strong></em> باستخدام تعليمة برمجية تُعرّف الفهرس كمصدر بيانات لإكمال المحادثة:</p>
<p dir="rtl"><strong>C#</strong>: ownData.cs</p>
</li>
<div dir="auto"><pre><span>// Configure your data source</span>
<span>// Extension methods to use data sources with options are subject to SDK surface changes. Suppress the warning to acknowledge this and use the subject-to-change AddDataSource method.</span>
#pragma warning disable <span>AOAI001</span>
<p dir="auto"><span>ChatCompletionOptions</span> <span>chatCompletionsOptions</span> <span>=</span> <span>new</span> <span>ChatCompletionOptions</span><span>(</span><span>)</span>
<span>{</span>
<span>MaxOutputTokenCount</span> <span>=</span> <span>600</span><span>,</span>
<span>Temperature</span> <span>=</span> <span>0.9f</span><span>,</span>
<span>}</span><span>;</span></p>
<p dir="auto"><span>chatCompletionsOptions</span><span>.</span><span>AddDataSource</span><span>(</span><span>new</span> <span>AzureSearchChatDataSource</span><span>(</span><span>)</span>
<span>{</span>
<span>Endpoint</span> <span>=</span> <span>new</span> <span>Uri</span><span>(</span><span>azureSearchEndpoint</span><span>)</span><span>,</span>
<span>IndexName</span> <span>=</span> <span>azureSearchIndex</span><span>,</span>
<span>Authentication</span> <span>=</span> <span>DataSourceAuthentication</span><span>.</span><span>FromApiKey</span><span>(</span><span>azureSearchKey</span><span>)</span><span>,</span>
<span>}</span><span>)</span><span>;</span></p></pre><div dir="auto"><p dir="auto"></p>
  </div></div>
<p dir="rtl"><strong>Python</strong>: ownData.py</p>
<div dir="auto"><pre><span># Configure your data source</span>
<span>text</span> <span>=</span> <span>input</span>(<span>'<span>\n</span>Enter a question:<span>\n</span>'</span>)
<p dir="auto"><span>completion</span> <span>=</span> <span>client</span>.<span>chat</span>.<span>completions</span>.<span>create</span>(
<span>model</span><span>=</span><span>deployment</span>,
<span>messages</span><span>=</span>[
{
<span>"role"</span>: <span>"user"</span>,
<span>"content"</span>: <span>text</span>,
},
],
<span>extra_body</span><span>=</span>{
<span>"data_sources"</span>:[
{
<span>"type"</span>: <span>"azure_search"</span>,
<span>"parameters"</span>: {
<span>"endpoint"</span>: <span>os</span>.<span>environ</span>[<span>"AZURE_SEARCH_ENDPOINT"</span>],
<span>"index_name"</span>: <span>os</span>.<span>environ</span>[<span>"AZURE_SEARCH_INDEX"</span>],
<span>"authentication"</span>: {
<span>"type"</span>: <span>"api_key"</span>,
<span>"key"</span>: <span>os</span>.<span>environ</span>[<span>"AZURE_SEARCH_KEY"</span>],
}
}
}
],
}
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
<p dir="rtl">في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.</p>
<ul dir="rtl">
<li><strong>C#:</strong> <code>dotnet run</code></li>
<li><strong>Python</strong>: <code>python ownData.py</code></li>
</ul>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يمكنك استخدام أيقونة <strong>تكبير حجم اللوحة</strong> (<strong>^</strong>) في شريط أدوات المحطة الطرفية لرؤية المزيد من نص وحدة التحكم.</p>
</blockquote>
</li>
<li>
<p dir="rtl">راجع الاستجابة إلى المطالبة <code>Tell me about London</code>، والتي يجب أن تتضمن إجابة بالإضافة إلى بعض التفاصيل عن البيانات المستخدمة لفصل المطالبة، والتي جرى الحصول عليها من خدمة البحث الخاصة بك.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: إذا أردت رؤية الاقتباسات من فهرس البحث، فعليك تعيين اقتباسات إظهار المتغير <em><strong>بالقرب</strong></em> من أعلى ملف التعليمات البرمجية على <strong>صحيح</strong>.</p>
</blockquote>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تنظيف" aria-label="Permalink: تنظيف" href="#تنظيف"></a></div>
<p dir="rtl">عند الانتهاء من مورد Azure OpenAI، تذكر أن تقوم بحذف المورد بأكمله في <strong>بوابة Azure</strong> على <code>https://portal.azure.com</code>. تأكد أيضاً من تضمين حساب التخزين ومورد البحث، حيث يمكن أن يؤدي ذلك إلى تكلفة كبيرة نسبياً.</p>
</div></div>
</article></div>
