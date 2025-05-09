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
  <td><div dir="rtl">تنفيذ استرداد الجيل المعزز (RAG) باستخدام خدمة Azure OpenAI</div></td>
  <td><div dir="rtl">stale</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">تنفيذ استرداد الجيل المعزز (RAG) باستخدام خدمة Azure OpenAI</h1><a id="user-content-تنفيذ-استرداد-الجيل-المعزز-rag-باستخدام-خدمة-azure-openai" class="anchor" aria-label="Permalink: تنفيذ استرداد الجيل المعزز (RAG) باستخدام خدمة Azure OpenAI" href="#تنفيذ-استرداد-الجيل-المعزز-rag-باستخدام-خدمة-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">تمكنك خدمة Azure OpenAI من استخدام بياناتك الخاصة مع ذكاء LLM الأساسي. يمكنك تقييد النموذج لاستخدام بياناتك فقط للمواضيع ذات الصلة، أو مزجها مع النتائج من النموذج المدرب مسبقاً.</p>
<p dir="rtl">في سيناريو هذا التمرين، ستؤدي دور مطور برامج يعمل لدى Margie's Travel Agency. ستكتشف كيفية استخدام بحث الذكاء الاصطناعي في Azure لفهرسة بياناتك واستخدامها مع Azure OpenAI لزيادة المطالبات.</p>
<p dir="rtl">سيستغرق هذا التدريب حوالي <b>30</b> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تزويد موارد Azure</h2><a id="user-content-تزويد-موارد-azure" class="anchor" aria-label="Permalink: تزويد موارد Azure" href="#تزويد-موارد-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لإكمال هذا التدريب، ستحتاج إلى:</p>
<ul dir="rtl">
    <li>مورد Azure OpenAI.</li>
    <li>مورد بحث الذكاء الاصطناعي في Azure</li>
    <li>مورد حساب تخزين Azure.</li>
</ul>
<ol dir="rtl">
    <li>سجّل الدخول إلى <b>Azure portal</b> من <code>https://portal.azure.com</code>.</li>
    <li>
        <p dir="rtl">إنشاء مورد <b>Azure OpenAI</b> بالإعدادات التالية:</p>
        <ul dir="rtl">
            <li><b>اشتراك</b>: <i>حدد اشتراك Azure الذي جرت الموافقة عليه للوصول إلى خدمة Azure OpenAI</i></li>
            <li><b>مجموعة الموارد</b>: <i>اختيار مجموعة موارد أو إنشاءها</i></li>
            <li>
                <p dir="rtl"><b>المنطقة</b>: <i>إجراء اختيار <b>عشوائي</b> من أي من المناطق التالية</i>*</p>
                <ul dir="rtl">
                    <li>شرق أستراليا</li>
                    <li>شرق كندا</li>
                    <li>شرق الولايات المتحدة</li>
                    <li>East US 2</li>
                    <li>وسط فرنسا</li>
                    <li>شرق اليابان</li>
                    <li>وسط شمال الولايات المتحدة</li>
                    <li>منطقة السويد الوسطى</li>
                    <li>شمال سويسرا</li>
                    <li>جنوب المملكة المتحدة</li>
                </ul>
            </li>
            <li><b>الاسم</b>: <i>اسم فريد من اختيارك</i></li>
            <li><b>مستوى التسعير</b>: قياسي S0</li>
        </ul>
    </li>
    <blockquote>موارد Azure OpenAI مقيدة بالحصص النسبية الإقليمية. تتضمن المناطق المدرجة الحصة النسبية الافتراضية لنوع (أنواع) النموذج المستخدمة في هذا التمرين. يؤدي اختيار منطقة عشوائيًا إلى تقليل مخاطر وصول منطقة واحدة إلى حد الحصة النسبية في السيناريوهات التي تشارك فيها اشتراكًا مع مستخدمين آخرين. في حالة الوصول إلى حد الحصة النسبية لاحقًا في التمرين، هناك احتمال أنك قد تحتاج إلى إنشاء مورد آخر في منطقة مختلفة.</blockquote>
    <li>
        <p dir="rtl">أثناء توفير مورد Azure OpenAI، قم بإنشاء <b>مورد بحث بالذكاء الاصطناعي في Azure</b> بالإعدادات التالية:</p>
        <ul dir="rtl">
            <li><b>الاشتراك</b>: <i>الاشتراك الذي قمت بتوفير مورد Azure OpenAI فيه</i></li>
            <li><b>مجموعة الموارد</b>: <i>مجموعة الموارد التي وفرت مورد Azure OpenAI الخاص بك فيها</i></li>
            <li><b>الاسم الخدمة</b>: <i>اسم فريد من اختيارك</i></li>
            <li><b>الموقع</b>: <i>المنطقة التي وفرت مورد Azure OpenAI الخاصة بك فيها</i></li>
            <li><b>مستوى التسعير</b>: أساسي</li>
        </ul>
    </li>
    <li>
        <p dir="rtl">أثناء توفير مورد بحث الذكاء الاصطناعي في Azure، قم بإنشاء مورد <b>حساب تخزين</b> بالإعدادات التالية:</p>
        <ul dir="rtl">
            <li><b>الاشتراك</b>: <i>الاشتراك الذي قمت بتوفير مورد Azure OpenAI فيه</i></li>
            <li><b>مجموعة الموارد</b>: <i>مجموعة الموارد التي وفرت مورد Azure OpenAI الخاص بك فيها</i></li>
            <li><b>اسم حساب التخزين</b>: <i>اسم فريدمن اختيارك</i></li>
            <li><b>المنطقة</b>: <i>المنطقة التي وفرت موارد Azure OpenAI الخاصة بك فيها</i></li>
            <li><b>الأداء:</b> قياسي</li>
            <li><b>التكرار</b>: التخزين المتكرر محليًا (LRS)</li>
        </ul>
    </li>
    <li>
        <p dir="rtl">بعد توزيع جميع الموارد الثلاثة بنجاح في اشتراك Azure، راجعها في بوابة Azure واجمع المعلومات التالية (التي ستحتاج إليها لاحقًا في التدريب):</p>
        <ul dir="rtl">
            <li><b>نقطة النهاية</b> و<b>مفتاح</b> من مورد Azure OpenAI الذي أنشأته (متوفر في صفحة <b>المفاتيح ونقطة النهاية</b> لمورد Azure OpenAI الخاص بك في مدخل Microsoft Azure)</li>
            <li>نقطة النهاية لخدمة البحث بالذكاء الاصطناعي في Azure الخاصة بك (قيمة عنوان <b>URL</b> في صفحة النظرة العامة لمورد البحث بالذكاء الاصطناعي في Azure في بوابة Azure).</li>
            <li>يكون <b>مفتاح المسؤول الأساسي</b> لمورد البحث بالذكاء الاصطناعي في Azure (متوفر في صفحة <b>المفاتيح</b> لمورد البحث بالذكاء الاصطناعي في Azure في بوابة Azure).</li>
        </ul>
    </li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تحميل بياناتك</h2><a id="user-content-تحميل-بياناتك" class="anchor" aria-label="Permalink: تحميل بياناتك" href="#تحميل-بياناتك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستقوم بإبطال المطالبات التي تستخدمها مع نموذج الذكاء الاصطناعي التوليدي باستخدام بياناتك الخاصة. في هذا التدريب، تتكون البيانات من مجموعة من كتيبات السفر من شركة <i>Margies Travel</i> الخيالية.</p>
<ol dir="rtl">
    <li>في علامة تبويب مستعرض جديدة، يمكنك تنزيل أرشيف بيانات الكتيب من <code>https://aka.ms/own-data-brochures</code>. استخرج الكتيبات إلى مجلد على جهاز الكمبيوتر الخاص بك.</li>
    <li>في بوابة Azure، انتقل إلى حساب التخزين الخاص بك، وقم بعرض صفحة <b>مستعرض التخزين</b></li>
    <li>حدد <b>حاويات الكائن الثنائي كبير الحجم</b> ثم أضف حاوية جديدة باسم <code>margies-travel</code>.</li>
    <li>حدد حاوية<b>margies-travel</b>، ثم قم بتحميل الكتيبات بتنسيق .pdf التي قمت باستخراجها مسبقًا إلى المجلد الجذر لحاوية الكائن الثنائي كبير الحجم.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توزيع نماذج الذكاء الاصطناعي</h2><a id="user-content-توزيع-نماذج-الذكاء-الاصطناعي" class="anchor" aria-label="Permalink: توزيع نماذج الذكاء الاصطناعي" href="#توزيع-نماذج-الذكاء-الاصطناعي"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستستخدم نموذجين للذكاء الاصطناعي في هذا التدريب:</p>
<ul dir="rtl">
    <li>نص يتضمن نموذج <i>لتحويل</i> النص في الكتيبات إلى رموز بحيث يمكن فهرسته بكفاءة للاستخدام في المطالبات الأساسية.</li>
    <li>نموذج GPT الذي يمكن لتطبيقك استخدامه لإنشاء استجابات للمطالبات المستندة إلى بياناتك.</li>
</ul>
<p dir="rtl">لنشر هذه النماذج، ستستخدم AI Foundry.</p>
<ol dir="rtl">
    <li>في بوابة Azure، انتقل إلى موارد Azure OpenAI. ثم استخدم الرابط لفتح موردك في <b>مدخل Azure AI Foundry</b>.</li>
    <li>
        <p dir="rtl">في مدخل Azure AI Foundry، على صفحة <b>عمليات النشر</b>، اعرض عمليات نشر النموذج الحالية لديك. ثم قم بإنشاء نشر نموذج أساسي جديد لنموذج </p>
        <p dir="rtl"><b>text-embedding-ada-002</b> بالإعدادات التالية:</p>
        <ul dir="rtl">
            <li><b>اسم التوزيع</b>: text-embedding-ada-002</li>
            <li><b>النموذج</b>: text-embedding-ada-002</li>
            <li><b>إصدار النموذج</b>: <i>الإصدار الافتراضي</i></li>
            <li><b>نوع التوزيع</b>: قياسي</li>
            <li><b>حد معدل الرموز المميزة في الدقيقة</b>: 5K*</li>
            <li><b>عامل تصفية المحتوى</b>: افتراضية</li>
            <li><b>تمكين الحصة النسبية الديناميكية</b>: تم التمكين</li>
        </ul>
    </li>
    <li>
        <p dir="rtl">بعد توزيع نموذج تضمين النص، ارجع إلى صفحة <b>عمليات التوزيع</b> وأنشئ توزيعًا جديدًا لنموذج <b>gpt-35-turbo-16k</b> بالإعدادات التالية:</p>
        <ul dir="rtl">
            <li><b>اسم التوزيع</b>: gpt-35-turbo-16k</li>
            <li><b>النموذج</b>: gpt-35-turbo-16k <i>(إذا لم يكن نموذج 16k متوفرًا، فاختر gpt-35-turbo)</i></li>
            <li><b>إصدار النموذج</b>: <i>الإصدار الافتراضي</i></li>
            <li><b>نوع التوزيع</b>: قياسي</li>
            <li><b>حد معدل الرموز المميزة في الدقيقة</b>: 5K*</li>
            <li><b>عامل تصفية المحتوى</b>: افتراضية</li>
            <li><b>تمكين الحصة النسبية الديناميكية</b>: تم التمكين</li>
        </ul>
    </li>
    <blockquote>*الحد الأقصى لمعدل 5000 رمز مميز في الدقيقة هو أكثر من كاف لإكمال هذا التمرين مع ترك سعة للأشخاص الآخرين الذين يستخدمون نفس الاشتراك.</blockquote>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء فهرس</h2><a id="user-content-إنشاء-فهرس" class="anchor" aria-label="Permalink: إنشاء فهرس" href="#إنشاء-فهرس"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لتسهيل استخدام بياناتك الخاصة في مطالبة، ستقوم بفهرستها باستخدام البحث بالذكاء الاصطناعي في Azure. ستستخدم نموذج تضمين النص الذي نشرته سابقًا أثناء عملية الفهرسة لتحويل البيانات النصية إلى <i>متجهات<i> (مما يؤدي إلى تمثيل كل رمز مميّز نصي في الفهرس بواسطة متجهات رقمية - مما يجعله متوافقًا مع الطريقة التي يمثل بها نموذج الذكاء الاصطناعي التوليدي النص)</i></i></p><i><i>
<ol dir="rtl">
    <li>في بوابة Azure، انتقل إلى مورد البحث بالذكاء الاصطناعي في Azure.</li>
    <li>ثم، في صفحة <b>نظرة عامة</b> حدد <b>استيراد البيانات ثم حوّل البيانات إلى رموز</b>.</li>
    <li>
        <p dir="rtl">في صفحة <b>إعداد اتصال البيانات</b>، حدد <b>تخزين الكائن الثنائي كبير الحجم في Azure</b> وقم بتكوين مصدر البيانات بالإعدادات التالية:</p>
        <ul dir="rtl">
            <li><b>الاشتراك</b>: اشتراك Azure الذي قمت بتوفير حساب التخزين الخاص بك فيه.</li>
            <li><b>حساب تخزين الكائن الثنائي كبير الحجم</b>: حساب التخزين الذي قمت بإنشائه سابقًا.</li>
            <li><b>حاوية الكائن الثنائي كبير الحجم</b>: margies-travel</li>
            <li><b>مجلد الكائن الثنائي كبير الحجم</b>: <i>اترك هذا فارغًا</i></li>
            <li><b>تمكين تعقب الحذف</b>: إلغاء التحديد</li>
            <li><b>المصادقة باستخدام الهوية المُدارة</b>: إلغاء التحديد</li>
        </ul>
    </li>
    <li>
        <p dir="rtl">في صفحة <b>تحويل نصك إلى رموز</b>، حدد الإعدادات التالية:</p>
        <ul dir="rtl">
            <li><b>النوع</b>: Azure OpenAI</li>
            <li><b>الاشتراك</b>: اشتراك Azure الذي قمت بتوفير خدمة Azure OpenAI الخاصة بك فيه.</li>
            <li><b>خدمة Azure OpenAI</b>: مورد خدمة Azure OpenAI الخاصة بك</li>
            <li><b>توزيع النموذج</b>: text-embedding-ada-002</li>
            <li><b>نوع المصادقة</b>: مفتاح API</li>
            <li><b>أقر بأن الاتصال بخدمة Azure OpenAI سيتكلف رسومًا إضافية على حسابي</b>: تحديد</li>
        </ul>
    </li>
    <li>في الصفحة التالية، لا تحدد خيار تحويل الصور إلى رموز أو استخراج البيانات باستخدام مهارات الذكاء الاصطناعي.</li>
    <li>في الصفحة التالية، قم بتمكين الترتيب الدلالي وجدولة المفهرس للتشغيل مرة واحدة.</li>
    <li>في الصفحة الأخيرة، قم بتعيين <b>بادئة اسم الغرض</b> إلى `margies-index` ثم قم بإنشاء الفهرس.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية</h2><a id="user-content-الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية" class="anchor" aria-label="Permalink: الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية" href="#الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لنستكشف الآن استخدام بياناتك الخاصة في تطبيق يستخدم SDK لخدمة Azure OpenAI. ستقوم بتطوير تطبيقك باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في مستودع GitHub.</p>
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
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تكوين تطبيقك</h2><a id="user-content-تكوين-تطبيقك" class="anchor" aria-label="Permalink: تكوين تطبيقك" href="#تكوين-تطبيقك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">التطبيقات لكل من C# وPython متوفرة، ويمتلك كلا التطبيقين الوظيفة نفسها. أولاً، ستكمل بعض الأجزاء الرئيسية من التطبيق لتمكين استخدام مورد Azure OpenAI الخاص بك.</p>
<ol dir="rtl">
    <li> في تعليمة Visual Studio البرمجية في جزء <b>المستكشف</b>، انتقِل إلى المجلد <b>Labfiles/06-use-own-data</b> وعليك توسيع المجلد <b>CSharp</b> أو <b>Python</b> حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي ستدمج وظيفة Azure OpenAI فيه.</li>
    <li>انقر بزر الماوس الأيمن فوق المجلد <b>CSharp</b> أو <b>Python</b> الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وافتح محطة طرفية متكاملة. ثم، عليك تثبيت حزمة Azure OpenAI SDK عن طريق تشغيل الأمر المناسب لتفضيل اللغة لديك:</li>
    <b>C#:</b>
    <div dir="rtl">
    <div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>dotnet add package Azure.AI.OpenAI --version 1.0.0-beta.14</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="dotnet add package Azure.AI.OpenAI --version 1.0.0-beta.14" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
    </div>
    <b>Python</b>:
    <div dir="rtl">
    <div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>pip install openai==1.55.3</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install openai==1.55.3" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
    </div>
    <li>
        <p dir="rtl">في جزء <b>مستكشف</b>، في مجلد <b>CSharp</b> أو <b>Python</b>، افتح ملف التكوين للغة المفضلة لديك</p>
        <ul dir="rtl">
            <li><b>C#</b>: appsettings.json</li>
            <li><b>Python</b>: .env</li>
        </ul>
    </li>
    <li>
        <p dir="rtl">تحديث قيم التكوين لتشمل:</p>
        <ul dir="rtl">
            <li><b>نقطة النهاية</b> و<b>مفتاح</b> من مورد Azure OpenAI الذي أنشأته (متوفر في صفحة <b>المفاتيح ونقطة النهاية</b> لمورد Azure OpenAI الخاص بك في مدخل Microsoft Azure)</li>
            <li><b>اسم النشر</b> الذي حددته لنشر نموذج gpt-35-turbo (متاح في صفحة <b>عمليات النشر</b> في مدخل Azure AI Foundry).</li>
            <li>نقطة النهاية لخدمة البحث الخاصة بك (قيمة عنوان <b>URL</b> في صفحة النظرة العامة لمورد البحث الخاص بك في مدخل Azure).</li>
            <li><b>مفتاح</b> لمورد البحث لديك (متوفر في صفحة <b>المفاتيح</b> لمورد البحث في مدخل Azure - يمكنك استخدام أي من مفاتيح المسؤول)</li>
            <li>اسم فهرس البحث (الذي يجب أن يكون <code>margies-index</code>).</li>
        </ul>
    </li>
    <li>احفظ ملف التكوين.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h3 tabindex="-1" class="heading-element" dir="rtl">أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI</h3><a id="user-content-أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai" class="anchor" aria-label="Permalink: أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI" href="#أضف-تعليمات-برمجية-لاستخدام-خدمة-azure-openai"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">أنت الآن جاهز لاستخدام Azure OpenAI SDK لاستهلاك نموذجك الموزع.</p>
<ol dir="rtl">
    <li>في جزء <b>مستكشف</b>، في المجلد <b>CSharp</b> أو <b>Python</b>، افتح ملف التعليمات البرمجية للغتك المفضلة، واستبدل التعليق <b><i>تكوين مصدر البيانات الخاص بك</i></b> باستخدام التعليمة البرمجية لإضافة مكتبة Azure OpenAI SDK:</li>
    <b>C#</b>: ownData.cs
    <div dir="rtl">
    <div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>// Configure your data source
AzureSearchChatExtensionConfiguration ownDataConfig = new()
{
    SearchEndpoint = new Uri(azureSearchEndpoint),
    Authentication = new OnYourDataApiKeyAuthenticationOptions(azureSearchKey),
    IndexName = azureSearchIndex
};</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="// Configure your data source
AzureSearchChatExtensionConfiguration ownDataConfig = new()
{
    SearchEndpoint = new Uri(azureSearchEndpoint),
    Authentication = new OnYourDataApiKeyAuthenticationOptions(azureSearchKey),
    IndexName = azureSearchIndex
};" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
    </div>
    <b>Python</b>: ownData.py
    <div dir="rtl">
    <div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code># Configure your data source
extension_config = dict(dataSources = [  
    { 
        "type": "AzureCognitiveSearch", 
        "parameters": { 
            "endpoint":azure_search_endpoint, 
            "key": azure_search_key, 
            "indexName": azure_search_index,
        }
    }]
)</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="# Configure your data source
extension_config = dict(dataSources = [  
    { 
        &quot;type&quot;: &quot;AzureCognitiveSearch&quot;, 
        &quot;parameters&quot;: { 
            &quot;endpoint&quot;:azure_search_endpoint, 
            &quot;key&quot;: azure_search_key, 
            &quot;indexName&quot;: azure_search_index,
        }
    }]
)" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
    </div>
    <li>راجع بقية التعليمة البرمجية، مع ملاحظة استخدام <i>الملحقات</i> في نص الطلب المستخدم لتوفير معلومات عن إعدادات مصدر البيانات.</li>
    <li>احفظ التغييرات في ملف التعليمة البرمجية.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تشغيل التطبيق الخاص بك</h2><a id="user-content-تشغيل-التطبيق-الخاص-بك" class="anchor" aria-label="Permalink: تشغيل التطبيق الخاص بك" href="#تشغيل-التطبيق-الخاص-بك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن نجح تكوين التطبيق الخاص بك، عليك تشغيله لإرسال طلبك إلى النموذج الخاص بك ومراقبة الاستجابة. ستلاحظ أن الفرق الوحيد بين الخيارات المختلفة هو محتوى المطالبة، وتظل جميع المعلمات الأخرى (مثل عدد الرموز المميزة ودرجة الحرارة) كما هي لكل طلب.</p>
<ol dir="rtl">
    <li>
        <p dir="rtl">في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.</p>
        <ul dir="rtl">
            <li><b>C#:</b> <code>dotnet run</code></li>
            <li><b>Python</b>: <code>python ownData.py</code></li>
        </ul>
        <blockquote><b>تلميح</b>: يمكنك استخدام أيقونة <b>تكبير حجم اللوحة</b> (<b>^</b>) في شريط أدوات المحطة الطرفية لرؤية المزيد من نص وحدة التحكم.</blockquote>
    </li>
    <li>راجع الاستجابة إلى المطالبة <code>Tell me about London</code>، والتي يجب أن تتضمن إجابة بالإضافة إلى بعض التفاصيل عن البيانات المستخدمة لفصل المطالبة، والتي جرى الحصول عليها من خدمة البحث الخاصة بك.</li>
    <blockquote><b>تلميح</b>: إذا أردت رؤية الاقتباسات من فهرس البحث، فعليك تعيين اقتباسات إظهار المتغير <b><i>بالقرب</i></b> من أعلى ملف التعليمات البرمجية على <b>صحيح</b>.</blockquote>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">عند الانتهاء من مورد Azure OpenAI، تذكر أن تقوم بحذف المورد بأكمله في <b>بوابة Azure</b> على <code><a href="https://portal.azure.com" rel="nofollow">https://portal.azure.com</a></code>. تأكد أيضاً من تضمين حساب التخزين ومورد البحث، حيث يمكن أن يؤدي ذلك إلى تكلفة كبيرة نسبياً.</p>
</i></i></article></div>
