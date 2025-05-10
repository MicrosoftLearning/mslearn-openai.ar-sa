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
  <td><div dir="rtl">بدء استخدام خدمة OpenAI Azure</div></td>
  <td><div dir="rtl">stale</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">بدء استخدام خدمة OpenAI Azure</h1><a id="user-content-بدء-استخدام-خدمة-openai-azure" class="anchor" aria-label="Permalink: بدء استخدام خدمة OpenAI Azure" href="#بدء-استخدام-خدمة-openai-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">توفر خدمة Azure OpenAI نماذج الذكاء الاصطناعي التوليدي التي تم تطويرها بواسطة OpenAI إلى النظام الأساسي لـ Azure، مما يتيح لك تطوير حلول الذكاء الاصطناعي القوية التي تستفيد من أمان وقابلية توسع وتكامل الخدمات التي يوفرها النظام الأساسي السحابي لـ Azure. في هذا التمرين، ستتعلم كيفية البدء في استخدام Azure OpenAI من خلال توفير الخدمة كمورد Azure واستخدام Azure AI Foundry لنشر نماذج الذكاء الاصطناعي التوليدي واستكشافها.</p>
<p dir="rtl">في سيناريو هذا التمرين، ستودي دور مطور برامج مكلف بتنفيذ وكيل الذكاء الاصطناعي الذي يمكنه استخدام الذكاء الاصطناعي التوليدي لمساعدة مؤسسة تسويقية على تحسين فعاليتها في الوصول إلى العملاء والإعلان عن منتجات جديدة. يمكن تطبيق التقنيات المستخدمة في التمرين على أي سيناريو تريد فيه المؤسسة استخدام نماذج الذكاء الاصطناعي التوليدية لمساعدة الموظفين على أن يكونوا أكثر فعالية وإنتاجية.</p>
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
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استخدام بيئة الدردشة التجريبية</h2><a id="user-content-استخدام-بيئة-الدردشة-التجريبية" class="anchor" aria-label="Permalink: استخدام بيئة الدردشة التجريبية" href="#استخدام-بيئة-الدردشة-التجريبية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن نشرت نموذجًا، يمكنك استخدامه لإنشاء استجابات استنادًا إلى مطالبات اللغة الطبيعية. توفر بيئة <em>الدردشة</em> في مدخل Azure AI Foundry واجهة دردشة آلية لإصدارات GPT 4 والإصدارات الأحدث.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة:</strong> تستخدم بيئة <em>الدردشة</em> التجريبية واجهة برمجة تطبيقات <em>ChatCompletions</em> بدلاً من واجهة برمجة تطبيقات <em>الإكمال</em> الأقدم التي تستخدمها بيئة <em>الإكمال</em> التجريبية. بيئة الإكمال التجريبية متوفرة للتوافق مع النماذج القديمة.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">في قسم <strong>البيئة التجريبية</strong>، حدد صفحة <strong>دردشة</strong>. تتكون صفحة بيئة <strong>الدردشة</strong> من صف من الأزرار ولوحتين رئيسيتين (والتي يمكن ترتيبها من اليمين إلى اليسار أفقيًا، أو من أعلى إلى أسفل عموديًا حسب دقة الشاشة لديك):</p>
<ul dir="rtl">
<li><strong>التكوين</strong> - يُستخدم لتحديد التوزيع الخاص بك، وتحديد رسالة النظام، وتعيين معلمات للتفاعل مع توزيعك.</li>
<li><strong>جلسة الدردشة</strong> - تستخدم لإرسال رسائل الدردشة وعرض الاستجابات.</li>
</ul>
</li>
<li>
<p dir="rtl">في جزء <strong>عمليات التوزيع</strong>، تأكد من تحديد توزيع نموذج gpt-4o الخاص بك.</p>
</li>
<li>
<p dir="rtl">راجع <strong>رسالة النظام</strong> الافتراضية، والتي يجب أن تكون <em>أنت مساعد الذكاء الاصطناعي الذي يساعد الأشخاص في العثور على المعلومات.</em> رسالة النظام مضمنة في المطالبات المقدمة إلى النموذج، وتوفر سياقاً لاستجابات النموذج؛ وتحدد التوقعات حول كيفية تفاعل وكيل الذكاء الاصطناعي بناءً على النموذج مع المستخدم.</p>
</li>
<li>
<p dir="rtl">في جزء <strong>جلسة الدردشة</strong>، أدخل استعلام المستخدم <code>How can I use generative AI to help me market a new product?</code></p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: قد تتلقى استجابة تفيد بأن توزيع واجهة برمجة التطبيقات غير جاهز بعد. إذا كان الأمر كذلك، انتظر بضع دقائق وحاول مرة أخرى.</p>
</blockquote>
</li>
<li>
<p dir="rtl">راجع الاستجابة، مع ملاحظة أن النموذج قد أنشأ إجابة لغة طبيعية متماسكة ذات صلة بالاستعلام الذي جرت مطالبته به.</p>
</li>
<li>
<p dir="rtl">أدخل استعلام المستخدم <code>What skills do I need if I want to develop a solution to accomplish this?</code>.</p>
</li>
<li>
<p dir="rtl">راجع الاستجابة، مع ملاحظة أن جلسة الدردشة احتفظت بسياق المحادثة (لذلك يجري تفسير "هذا" كحل الذكاء الاصطناعي التوليدي للتسويق). هذا السياق محقق من خلال تضمين محفوظات المحادثة الأخيرة في كل إرسال مطالبة متتالي، وبالتالي فإن المطالبة المرسلة إلى النموذج للاستعلام الثاني تتضمن الاستعلام الأصلي والاستجابة بالإضافة إلى إدخال المستخدم الجديد.</p>
</li>
<li>
<p dir="rtl">في جزء <strong>جلسة الدردشة</strong>، حدد <strong>مسح الدردشة</strong> وتأكد من رغبتك في إعادة تشغيل جلسة الدردشة.</p>
</li>
<li>
<p dir="rtl">أدخل الاستعلام <code>Can you help me find resources to learn those skills?</code> وراجع الاستجابة، والتي يجب أن تكون إجابة لغة طبيعية صالحة، ولكن منذ فقد محفوظات الدردشة السابقة، من المحتمل أن تكون الإجابة حول العثور على موارد مهارة عامة بدلاً من الارتباط بالمهارات المحددة اللازمة لبناء حل تسويقي للذكاء الاصطناعي التوليدي.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تجربة رسائل النظام والمطالبات وأمثلة قليلة اللقطات</h2><a id="user-content-تجربة-رسائل-النظام-والمطالبات-وأمثلة-قليلة-اللقطات" class="anchor" aria-label="Permalink: تجربة رسائل النظام والمطالبات وأمثلة قليلة اللقطات" href="#تجربة-رسائل-النظام-والمطالبات-وأمثلة-قليلة-اللقطات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">شاركت حتى الآن في محادثة دردشة مع نموذجك استناداً إلى رسالة النظام الافتراضي. يمكنك تخصيص إعداد النظام للحصول على مزيد من التحكم في أنواع الاستجابات التي جرى إنشاؤها بواسطة النموذج الخاص بك.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في شريط الأدوات الرئيسي، حدد <strong>نماذج المطالبة</strong>، واستخدم قالب مطالبة <strong>مساعد كتابة التسويق</strong>.</p>
</li>
<li>
<p dir="rtl">راجع رسالة النظام الجديدة، التي تصف كيف يجب على عامل الذكاء الاصطناعي استخدام النموذج للاستجابة.</p>
</li>
<li>
<p dir="rtl">في جزء <strong>جلسة الدردشة</strong>، أدخل استعلام المستخدم <code>Create an advertisement for a new scrubbing brush</code>.</p>
</li>
<li>
<p dir="rtl">راجع الاستجابة، والتي يجب أن تتضمن نسخة إعلانية لفرشاة تنقية. قد تكون النسخة شاملة جداً وخلاقة.</p>
<p dir="rtl">في سيناريو حقيقي، من المحتمل أن يكون محترف التسويق يعرف بالفعل اسم منتج فرشاة التنظيف بالإضافة إلى بعض الأفكار حول الميزات الرئيسية التي يجب تمييزها في الإعلان. للحصول على النتائج الأكثر فائدة من نموذج الذكاء الاصطناعي التوليدي، يحتاج المستخدمون إلى تصميم مطالباتهم لتضمين أكبر قدر ممكن من المعلومات ذات الصلة.</p>
</li>
<li>
<p dir="rtl">أدخل المطالبة <code>Revise the advertisement for a scrubbing brush named "Scrubadub 2000", which is made of carbon fiber and reduces cleaning times by half compared to ordinary scrubbing brushes</code>.</p>
</li>
<li>
<p dir="rtl">راجع الاستجابة التي يجب أن تأخذ في الحسبان المعلومات الإضافية التي قدمتها عن منتج فرشاة التنظيف.</p>
<p dir="rtl">يجب أن تكون الاستجابة الآن أكثر فائدة، ولكن للحصول على مزيد من التحكم في الإخراج من النموذج، يمكنك تقديم مثال واحد أو أكثر من الأمثلة <em>قليلة اللقطات</em> التي يجب أن تستند إليها الاستجابات.</p>
</li>
<li>
<p dir="rtl">في مربع نص <strong>رسالة النظام</strong>، قم بتوسيع القائمة المنسدلة حتى الوصول إلى <strong>قسم الإضافة</strong> وحدد <strong>أمثلة</strong>. ثم اكتب الرسالة والاستجابة التالية في المربعات المعينة:</p>
<p dir="rtl"><strong>المستخدم</strong>:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Write an advertisement for the lightweight "Ultramop" mop, which uses patented absorbent materials to clean floors.
</code></pre><div class="zeroclipboard-container">

  </div></div>
<p dir="rtl"><strong>Assistant:</strong></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Welcome to the future of cleaning!

The Ultramop makes light work of even the dirtiest of floors. Thanks to its patented absorbent materials, it ensures a brilliant shine. Just look at these features:
- Lightweight construction, making it easy to use.
- High absorbency, enabling you to apply lots of clean soapy water to the floor.
- Great low price.

Check out this and other products on our website at www.contoso.com.
</code></pre><div class="zeroclipboard-container">

  </div></div>
</li>
<li>
<p dir="rtl">استخدم زر <strong>تطبيق التغييرات</strong> لحفظ الأمثلة وبدء جلسة عمل جديدة.</p>
</li>
<li>
<p dir="rtl">في قسم <strong>جلسة الدردشة</strong>، أدخل استعلام المستخدم <code>Create an advertisement for the Scrubadub 2000 - a new scrubbing brush made of carbon fiber that reduces cleaning time by half</code>.</p>
</li>
<li>
<p dir="rtl">راجع الاستجابة، والتي يجب أن تكون إعلانا جديدا لـ "Scrubadub 2000" الذي تم تصميمه على نموذج "Ultramop" المقدم في إعداد النظام.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تجربة المعلمات</h2><a id="user-content-تجربة-المعلمات" class="anchor" aria-label="Permalink: تجربة المعلمات" href="#تجربة-المعلمات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">استكشفت كيف يمكن أن تساعد رسالة النظام والأمثلة والمطالبات في تحسين الاستجابات التي يرجعها النموذج. يمكنك أيضاً استخدام المعلمات للتحكم في سلوك النموذج.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في جزء <strong>التكوين</strong>، حدد علامة تبويب <strong>المعلمات</strong> ثم عليك تعيين قيم المعلمات التالية:</p>
<ul dir="rtl">
<li><strong>الحد الأقصى للاستجابة</strong>: 1000</li>
<li><strong>درجة الحرارة</strong>: 1</li>
</ul>
</li>
<li>
<p dir="rtl">في قسم ** جلسة الدردشة**، استخدم زر <strong>مسح الدردشة</strong> لإعادة تعيين جلسة الدردشة. ثم أدخل استعلام المستخدم <code>Create an advertisement for a cleaning sponge</code> وراجع الاستجابة. يجب أن تتضمن نسخة الإعلان الناتجة 1000 رمز نصي كحد أقصى، وأن تتضمن بعض العناصر الإبداعية - على سبيل المثال، ربما يكون النموذج قد اخترع اسم منتج للإسفنج وقدم بعض المطالبات حول ميزاته.</p>
</li>
<li>
<p dir="rtl">استخدم زر <strong>مسح الدردشة</strong> لإعادة ضبط جلسة الدردشة مرة أخرى، ثم أعد إدخال نفس الاستعلام كما كان من قبل (<code>Create an advertisement for a cleaning sponge</code>) وراجع الرد. قد تختلف الاستجابة عن الاستجابة السابقة.</p>
</li>
<li>
<p dir="rtl">في جزء <strong>التكوين</strong>، في علامة التبويب <strong>المعلمات</strong>، يمكنك تغيير قيمة معلمة <strong>درجة الحرارة</strong> إلى 0.</p>
</li>
<li>
<p dir="rtl">فس قسم <strong>جلسة الدردشة</strong>، استخدم زر <strong>مسح الدردشة</strong> لإعادة ضبط جلسة الدردشة مرة أخرى، ثم أعد إدخال نفس الاستعلام كما كان من قبل (<code>Create an advertisement for a cleaning sponge</code>) وراجع الرد. هذه المرة، قد لا تكون الاستجابة خلاقة جداً.</p>
</li>
<li>
<p dir="rtl">استخدم زر <strong>مسح الدردشة</strong> لإعادة تعيين جلسة الدردشة مرة أخرى، ثم أعد إدخال نفس الاستعلام كما كان من قبل (<code>Create an advertisement for a cleaning sponge</code>) وراجع الاستجابة؛ والتي يجب أن تكون متشابهة جداً (إن لم تكن متطابقة) مع الاستجابة السابقة.</p>
<p dir="rtl">تتحكم معلمة <strong>درجة الحرارة</strong> في الدرجة التي يمكن أن يكون فيها النموذج مبدعاً في جيل الاستجابة. ينتج عن القيمة المنخفضة استجابة متسقة مع اختلاف عشوائي بسيط، بينما تشجع القيمة العالية النموذج على إضافة عناصر إبداعية إلى ناتجه؛ والتي قد تؤثر على دقة الاستجابة وواقعيتها.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توزيع نموذجك على تطبيق ويب</h2><a id="user-content-توزيع-نموذجك-على-تطبيق-ويب" class="anchor" aria-label="Permalink: توزيع نموذجك على تطبيق ويب" href="#توزيع-نموذجك-على-تطبيق-ويب"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن استكشفت بعض إمكانيات نموذج الذكاء الاصطناعي التوليدي في بيئة Azure AI Foundry، يمكنك نشر تطبيق ويب Azure لتوفير واجهة وكيل الذكاء الاصطناعي الأساسية التي يمكن للمستخدمين من خلالها الدردشة مع النموذج.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: بالنسبة لبعض المستخدمين، لا يمكن نشر التطبيق على الويب بسبب وجود خطأ في القالب في الاستوديو. إذا كانت هذه هي الحالة، فتخطى هذا القسم.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">في الجزء العلوي الأيسر من صفحة بيئة <strong>الدردشة</strong> التجريبية، في القائمة <strong>نشر إلى</strong>، حدد <strong>تطبيق ويب جديد</strong>.</p>
</li>
<li>
<p dir="rtl">في مربع حوار <strong>نشر إلى تطبيق ويب</strong>، أنشئ تطبيق ويب جديداً بالإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>الاسم</strong>: <em>اسم فريد</em></li>
<li><strong>Subscription</strong>: <em>اشتراكك في Azure</em></li>
<li><strong>مجموعة الموارد</strong>: <em>مجموعة الموارد التي وفرت مورد Azure OpenAI الخاص بك فيها</em></li>
<li><strong>المواقع</strong>: <em>المنطقة التي وفرت موارد Azure OpenAI الخاصة بك فيها</em></li>
<li><strong>خطة الأسعار</strong>: مجاني (F1) <em>إذا لم يكن هذا المستوى متاحاً، فاختر أساسياً (B)</em></li>
<li><strong>تمكين سجل الدردشة في تطبيق الويب</strong>: <strong>تم إلغاء</strong> التحديد</li>
<li><strong>أقر بأن تطبيقات الويب ستستخدم في حسابي</strong>: محدد</li>
</ul>
</li>
<li>
<p dir="rtl">وزع تطبيق الويب الجديد وانتظر حتى يكتمل النشر (والذي قد يستغرق 10 دقائق أو نحو ذلك)</p>
</li>
<li>
<p dir="rtl">بعد نشر تطبيق الويب الخاص بك بنجاح، استخدم الزر الموجود في الجزء العلوي الأيسر من صفحة بيئة <strong>الدردشة</strong> التجريبية لتشغيل تطبيق الويب. قد يستغرق تشغيل هذا التطبيق بضع دقائق. إذا طُلب منك، فعليك قبول طلب الأذونات.</p>
</li>
<li>
<p dir="rtl">في تطبيق الويب، أدخل رسالة الدردشة التالية:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto dir="auto"><pre lang="prompt" class="notranslate"><code>Write an advertisement for the new "WonderWipe" cloth that attracts dust particulates and can be used to clean any household surface.
</code></pre><div class="zeroclipboard-container">

  </div></div>
</li>
<li>
<p dir="rtl">راجع الاستجابة.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: نشرت <em>النموذج</em> إلى تطبيق ويب، ولكن هذا النشر لا يتضمن إعدادات النظام والمعلمات التي عينها في البيئة التجريبية لذلك قد لا تعكس الاستجابة الأمثلة التي حددتها في البيئة التجريبية. في سيناريو حقيقي، يمكنك إضافة منطق إلى التطبيق الخاص بك لتعديل المطالبة بحيث تتضمن البيانات السياقية المناسبة لنوع الاستجابة التي تريد إنشاءها. هذا النوع من التخصيص خارج نطاق هذا التمرين على المستوى التمهيدي، ولكن يمكنك التعرف على تقنيات الهندسة السريعة وواجهات برمجة تطبيقات Azure OpenAI في تمارين أخرى ووثائق المنتج.</p>
</blockquote>
</li>
<li>
<p dir="rtl">عند الانتهاء من تجربة نموذجك في تطبيق الويب، أغلق علامة تبويب تطبيق الويب في متصفحك للعودة إلى مدخل Azure AI Foundry.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">عند الانتهاء من مورد Azure OpenAI، تذكر حذف التوزيع أو المورد بأكمله في <strong>مدخل Microsoft Azure</strong> في <code>https://portal.azure.com</code>.</p>
</article></div>
