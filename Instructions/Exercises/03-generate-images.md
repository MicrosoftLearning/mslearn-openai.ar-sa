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
  <th>description</th>
  <th>status</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div dir="rtl">إنشاء صور باستخدام الذكاء الاصطناعي</div></td>
  <td><div dir="rtl">تعرّف على كيفية استخدام نموذج DALL-E من OpenAI لإنشاء صور.</div></td>
  <td><div dir="rtl">new</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h1 tabindex="-1" dir="rtl" class="heading-element">إنشاء صور باستخدام الذكاء الاصطناعي</h1><a id="user-content-إنشاء-صور-باستخدام-الذكاء-الاصطناعي" class="anchor" aria-label="Permalink: إنشاء صور باستخدام الذكاء الاصطناعي" href="#إنشاء-صور-باستخدام-الذكاء-الاصطناعي"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-إنشاء-صور-باستخدام-الذكاء-الاصطناعي" aria-label="Permalink: إنشاء صور باستخدام الذكاء الاصطناعي" href="#إنشاء-صور-باستخدام-الذكاء-الاصطناعي"></a></div>
<p dir="rtl">في هذا التمرين، ستستخدم نموذج الذكاء الاصطناعي التوليدي OpenAI DALL-E لتوليد الصور. ستطوّر تطبيقك باستخدام Azure AI Foundry وخدمة Azure OpenAI.</p>
<p dir="rtl">سيستغرق هذا التدريب حوالي <strong>30</strong> دقيقة.</p>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">إنشاء مشروع في مصنع الذكاء الاصطناعي في Azure</h2><a id="user-content-إنشاء-مشروع-في-مصنع-الذكاء-الاصطناعي-في-azure" class="anchor" aria-label="Permalink: إنشاء مشروع في مصنع الذكاء الاصطناعي في Azure" href="#إنشاء-مشروع-في-مصنع-الذكاء-الاصطناعي-في-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-إنشاء-مشروع-في-مصنع-الذكاء-الاصطناعي-في-azure" aria-label="Permalink: إنشاء مشروع في مصنع الذكاء الاصطناعي في Azure" href="#إنشاء-مشروع-في-مصنع-الذكاء-الاصطناعي-في-azure"></a></div>
<p dir="rtl">دعنا نبدأ بإنشاء مشروع في مصنع الذكاء الاصطناعي في Azure.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في متصفح الويب، افتح <a href="https://ai.azure.com" rel="nofollow">مدخل Azure AI Foundry</a> على <code>https://ai.azure.com</code> وسجّل الدخول باستخدام بيانات اعتماد Azure الخاصة بك. أغلق أية تلميحات أو أجزاء تشغيل سريع يتم فتحها عندما تقوم بتسجيل الدخول، وإذا لزم الأمر، استخدم شعار <strong>مصنع الذكاء الاصطناعي في Azure</strong> في أعلى اليسار للانتقال إلى الصفحة الرئيسية، والتي تبدو مشابهة للصورة التالية:</p>
</li>
<p dir="auto"><a href="https://github.com/MicrosoftLearning/mslearn-openai.ar-sa/blob/main/Instructions/media/ai-foundry-home.png"><img src="https://github.com/MicrosoftLearning/mslearn-openai.ar-sa/raw/main/Instructions/media/ai-foundry-home.png" alt="لقطة شاشة لمدخل Azure AI Foundry." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في الصفحة الرئيسية، حدد <strong>+ إنشاء مشروع</strong>.</p>
</li>
<li>
<p dir="rtl">في معالج** إنشاء مشروع**، أدخل اسمًا مناسبًا لمشروعك وإذا تم اقتراح مركز موجود، فحدد خيار إنشاء مركز جديد. ثم راجع موارد Azure التي سيتم إنشاؤها تلقائيًا لدعم مركزك ومشروعك.</p>
</li>
<li>
<p dir="rtl">حدد <strong>تخصيص</strong> وحدد الإعدادات التالية لمركزك:</p>
<ul dir="rtl">
<li><strong>اسم المركز</strong>: <em>اسم صالح لمركزك</em></li>
<li><strong>Subscription</strong>: <em>اشتراكك في Azure</em></li>
<li><strong>Resource group</strong>: <em>إنشاء مجموعة موارد أو تحديدها</em></li>
<li><strong>الموقع</strong>: حدد <strong>ساعدني في الاختيار</strong> ثم حدد <strong>dalle</strong> في نافذة مساعد الموقع واستخدم المنطقة الموصى بها*</li>
<li><strong>الاتصال بخدمات Azure AI أو Azure OpenAI</strong>: <em>إنشاء مزود جديد لخدمات الذكاء الاصطناعي</em></li>
<li><strong>الاتصال بـ Azure AI Search</strong>: تخطي الاتصال</li>
</ul>
<blockquote>
<p dir="rtl">* موارد Azure OpenAI مقيدة بالحصص النسبية الإقليمية. في حالة الوصول إلى حد الحصة النسبية لاحقًا في التمرين، هناك احتمال أنك قد تحتاج إلى إنشاء مورد آخر في منطقة مختلفة.</p>
</blockquote>
</li>
<li>
<p dir="rtl">حدد <strong>التالي</strong> لمراجعة التكوين الخاص بك. ثم حدد <strong>إنشاء</strong> وانتظر حتى تكتمل العملية.</p>
</li>
<li>
<p dir="rtl">عند إنشاء مشروعك، أغلق أي تلميحات يتم عرضها وراجع صفحة المشروع في مدخل مصنع الذكاء الاصطناعي في Azure، والذي يجب أن يبدو مشابهة للصورة التالية:</p>
</li>
<p dir="auto"><a href="https://github.com/MicrosoftLearning/mslearn-openai.ar-sa/blob/main/Instructions/media/ai-foundry-project.png"><img src="https://github.com/MicrosoftLearning/mslearn-openai.ar-sa/raw/main/Instructions/media/ai-foundry-project.png" alt="لقطة شاشة توضح تفاصيل مشروع ذكاء اصطناعي في Azure في مدخل مصنع الذكاء الاصطناعي في Azure." style="max-width: 100%;"></a></p>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">نشر نموذج DALL-E</h2><a id="user-content-نشر-نموذج-dall-e" class="anchor" aria-label="Permalink: نشر نموذج DALL-E" href="#نشر-نموذج-dall-e"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-نشر-نموذج-dall-e" aria-label="Permalink: نشر نموذج DALL-E" href="#نشر-نموذج-dall-e"></a></div>
<p dir="rtl">الآن أنت مستعد لنشر نموذج DALL-E لدعم إنشاء الصور.</p>
<ol dir="rtl">
<li>في شريط الأدوات في الجزء العلوي الأيمن من صفحة مشروع مصنع الذكاء الاصطناعي في Azure، استخدم أيقونة <strong>ميزات المعاينة</strong> لتمكين ميزة <strong>توزيع النماذج على خدمة استدلال نموذج الذكاء الاصطناعي في Azure</strong>. تضمن هذه الميزة توفّر توزيع النموذج الخاص بك لخدمة الاستدلال بالذكاء الاصطناعي في Azure، والتي ستستخدمها في كود التطبيق الخاص بك.</li>
<li>في الجزء الموجود على يسار مشروعك، في قسم <strong>أصولي</strong>، حدد صفحة <strong>النماذج + نقاط النهاية</strong>.</li>
<li>في صفحة <strong>النماذج + نقاط النهاية</strong>، في علامة التبويب <strong>عمليات توزيع النماذج</strong>، في القائمة <strong>+ نشر النموذج</strong>، حدّد <strong>توزيع النموذج الأساسي</strong>.</li>
<li>ابحث عن نموذج <strong>dall-e-3</strong> في القائمة، ثم حدده وأكّده.</li>
<li>وافق على اتفاقية الترخيص إذا طلب منك ذلك، ثم وزّع النموذج بالإعدادات التالية عن طريق تحديد <strong>تخصيص</strong> في تفاصيل التوزيع:
<ul dir="rtl">
<li><strong>اسم النشر</strong>: <em>اسم صالح لنشر نموذجك</em></li>
<li><strong>نوع التوزيع</strong>: قياسي</li>
<li><strong>تفاصيل التوزيع</strong>: <em>استخدام الإعدادات الافتراضية</em></li>
</ul>
</li>
<li>انتظر حتى تصبح حالة التزويد للتوزيع <strong>مكتملة</strong>.</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">اختبر النموذج في مساحة التجربة</h2><a id="user-content-اختبر-النموذج-في-مساحة-التجربة" class="anchor" aria-label="Permalink: اختبر النموذج في مساحة التجربة" href="#اختبر-النموذج-في-مساحة-التجربة"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-اختبر-النموذج-في-مساحة-التجربة" aria-label="Permalink: اختبر النموذج في مساحة التجربة" href="#اختبر-النموذج-في-مساحة-التجربة"></a></div>
<p dir="rtl">قبل إنشاء تطبيق عميل، دعنا نختبر نموذج DALL-E في مساحة التجربة.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في صفحة نموذج DALL-E الذي نشرته، حدد <strong>فتح في مساحة التجربة</strong> (أو في صفحة <strong>مساحات التجربة</strong>، افتح <strong>مساحة تجربة الصور</strong>).</p>
</li>
<li>
<p dir="rtl">تأكد من تحديد نشر نموذج DALL-E. ثم، في مربع <strong>المطالبة</strong>، أدخل مطالبة مثل <code>Create an image of an robot eating spaghetti</code>.</p>
</li>
<li>
<p dir="rtl">راجع الصورة الناتجة في مساحة التجربة:</p>
</li>
<p dir="auto"><a href="https://github.com/MicrosoftLearning/mslearn-openai.ar-sa/blob/main/Instructions/media/images-playground.png"><img src="https://github.com/MicrosoftLearning/mslearn-openai.ar-sa/raw/main/Instructions/media/images-playground.png" alt="لقطة شاشة لمساحة تجربة الصور مع صورة تم إنشاؤها." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">أدخل مطالبة متابعة، مثل <code>Show the robot in a restaurant</code> وراجع الصورة الناتجة.</p>
</li>
<li>
<p dir="rtl">استمر في الاختبار باستخدام مطالبات جديدة لتحسين الصورة حتى تصبح راضيًا عنها.</p>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">أنشئ تطبيق عميل</h2><a id="user-content-أنشئ-تطبيق-عميل" class="anchor" aria-label="Permalink: أنشئ تطبيق عميل" href="#أنشئ-تطبيق-عميل"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-أنشئ-تطبيق-عميل" aria-label="Permalink: أنشئ تطبيق عميل" href="#أنشئ-تطبيق-عميل"></a></div>
<p dir="rtl">يبدو أن النموذج يعمل في مساحة التجربة. الآن يمكنك استخدام Azure OpenAI SDK لاستخدامه في تطبيق عميل.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يمكنك اختيار تطوير الحل الخاص بك باستخدام Python أو Microsoft C#. اتبع الإرشادات في القسم المناسب للغة التي اخترتها.</p>
</blockquote>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h3 tabindex="-1" dir="rtl" class="heading-element">إعداد تكوين التطبيق</h3><a id="user-content-إعداد-تكوين-التطبيق" class="anchor" aria-label="Permalink: إعداد تكوين التطبيق" href="#إعداد-تكوين-التطبيق"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-إعداد-تكوين-التطبيق" aria-label="Permalink: إعداد تكوين التطبيق" href="#إعداد-تكوين-التطبيق"></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">في مدخل مصنع الذكاء الاصطناعي في Azure، اعرض صفحة <strong>النظرة العامة</strong> لمشروعك.</p>
</li>
<li>
<p dir="rtl">في منطقة <strong>تفاصيل المشروع</strong>، لاحظ <strong>سلسلة الاتصال للمشروع</strong>. ستستخدم سلسلة الاتصال هذه للاتصال بمشروعك في تطبيق العميل.</p>
</li>
<li>
<p dir="rtl">افتح علامة تبويب جديدة للمتصفح (مع إبقاء مدخل مصنع الذكاء الاصطناعي في Azure مفتوحًا في علامة التبويب الموجودة). بعد ذلك في علامة التبويب الجديدة، انتقل إلى <a href="https://portal.azure.com" rel="nofollow">بوابة Azure</a> على <code>https://portal.azure.com</code>؛ وسجّل الدخول باستخدام بيانات اعتماد Azure الخاصة بك إذا طُلب منك ذلك.</p>
</li>
<li>
<p dir="rtl">استخدم الزر <strong>[&gt;_]</strong> الموجود على يمين شريط البحث أعلى الصفحة لإنشاء Cloud Shell جديد في بوابة Azure، وتحديد بيئة <em><strong>PowerShell</strong></em>. يوفّر Cloud Shell واجهة سطر أوامر في جزء أسفل بوابة Azure.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا كنت قد أنشأت مسبقًا Cloud Shell يستخدم بيئة <em>معالج Bash</em>، فبدّل إلى <em><strong>PowerShell</strong></em>.</p>
</blockquote>
</li>
<li>
<p dir="rtl">في شريط أدوات Cloud Shell، في قائمة <strong>الإعدادات</strong>، حدد <strong>الانتقال إلى الإصدار الكلاسيكي</strong> (هذا مطلوب لاستخدام محرر التعليمات البرمجية).</p>
<p dir="rtl"><strong>تأكد من التبديل إلى الإصدار الكلاسيكي من cloud shell قبل المتابعة.</strong></p>
</li>
<li>
<p dir="rtl">في جزء Cloud Shell، أدخل الأوامر التالية لاستنساخ مستودع GitHub الذي يحتوي على ملفات التعليمات البرمجية لهذا التمرين (اكتب الأمر أو انسخه إلى الحافظة ثم انقر بزر الماوس الأيمن في سطر الأوامر وقم بلصقه كنص عادي):</p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>rm -r mslearn-openai -f
git clone https://github.com/microsoftlearning/mslearn-openai mslearn-openai
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="rm -r mslearn-openai -f
git clone https://github.com/microsoftlearning/mslearn-openai mslearn-openai" tabindex="0" role="button">
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
<p dir="rtl"><strong>تلميح</strong>: عند لصق الأوامر في CloudShell، قد يشغل الإخراج مساحة كبيرة من ذاكرة التخزين المؤقت للشاشة. يمكنك مسح الشاشة عن طريق إدخال الأمر <code>cls</code> لتسهيل التركيز على كل مهمة.</p>
</blockquote>

<li>
<p dir="rtl">بعد استنساخ المستودع، انتقل إلى المجلد الخاص باللغة الذي يحتوي على ملفات كود التطبيق، استنادًا إلى لغة البرمجة التي تختارها (Python أو #C):</p>
<p dir="rtl"><strong>Python</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cd mslearn-openai/Labfiles/03-image-generation/Python
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cd mslearn-openai/Labfiles/03-image-generation/Python" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>
<p dir="rtl"><strong>#C</strong></p>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cd mslearn-openai/Labfiles/03-image-generation/CSharp
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cd mslearn-openai/Labfiles/03-image-generation/CSharp" tabindex="0" role="button">
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
<p dir="rtl">في جزء سطر أوامر Cloud Shell، أدخل الأمر التالي لتثبيت المكتبات التي ستستخدمها:</p>
<p dir="rtl"><strong>Python</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>python -m venv labenv
./labenv/bin/Activate.ps1
pip install python-dotenv azure-identity azure-ai-projects openai requests
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python -m venv labenv
./labenv/bin/Activate.ps1
pip install python-dotenv azure-identity azure-ai-projects openai requests" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>
<p dir="rtl"><strong>#C</strong></p>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>dotnet add package Azure.Identity
dotnet add package Azure.AI.Projects --prerelease
dotnet add package Azure.AI.OpenAI
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="dotnet add package Azure.Identity
dotnet add package Azure.AI.Projects --prerelease
dotnet add package Azure.AI.OpenAI" tabindex="0" role="button">
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
<p dir="rtl">أدخل الأمر التالي لتحرير ملف التكوين الذي تم توفيره:</p>
<p dir="rtl"><strong>Python</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>code .env
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="code .env" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>
<p dir="rtl"><strong>#C</strong></p>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>code appsettings.json
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="code appsettings.json" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>
<p dir="rtl">يتم فتح الملف في محرر التعليمات البرمجية.</p>

<li>
<p dir="rtl">في ملف التعليمات البرمجية، استبدل العنصر النائب <strong>your_project_endpoint</strong> بسلسلة الاتصال لمشروعك (المنسوخة من صفحة <strong>نظرة عامة</strong> في بوابة Azure AI Foundry)، واستبدل العنصر النائب <strong>your_model_deployment</strong> بالاسم الذي عيّنته لنشر نموذج dall-e-3.</p>
</li>
<li>
<p dir="rtl">بعد استبدال العناصر النائبة، استخدم الأمر <strong>CTRL+S</strong> لحفظ التغييرات ثم استخدم الأمر <strong>CTRL+Q</strong> لإغلاق محرر التعليمات البرمجية مع إبقاء سطر أوامر Cloud Shell مفتوحWا.</p>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h3 tabindex="-1" dir="rtl" class="heading-element">اكتب التعليمة البرمجية للاتصال بمشروعك والدردشة مع نموذجك</h3><a id="user-content-اكتب-التعليمة-البرمجية-للاتصال-بمشروعك-والدردشة-مع-نموذجك" class="anchor" aria-label="Permalink: اكتب التعليمة البرمجية للاتصال بمشروعك والدردشة مع نموذجك" href="#اكتب-التعليمة-البرمجية-للاتصال-بمشروعك-والدردشة-مع-نموذجك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-اكتب-التعليمة-البرمجية-للاتصال-بمشروعك-والدردشة-مع-نموذجك" aria-label="Permalink: اكتب التعليمة البرمجية للاتصال بمشروعك والدردشة مع نموذجك" href="#اكتب-التعليمة-البرمجية-للاتصال-بمشروعك-والدردشة-مع-نموذجك"></a></div>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: عند إضافة التعليمات البرمجية، تأكد من الحفاظ على المسافة البادئة الصحيحة.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">أدخل الأمر التالي لتحرير ملف التعليمات البرمجية الذي تم توفيره:</p>
<p dir="rtl"><strong>Python</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>code dalle-client.py
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="code dalle-client.py" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>
<p dir="rtl"><strong>#C</strong></p>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>code Program.cs
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="code Program.cs" tabindex="0" role="button">
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
<p dir="rtl">في ملف التعليمات البرمجية، لاحظ العبارات الموجودة في أعلى الملف والتي تمت إضافتها لاستيراد مساحات الأسماء (Namespaces) الضرورية لـ (SDK). ثم تحت التعليق <strong>إضافة المراجع</strong>، أضف التعليمة البرمجية التالية للإشارة إلى مساحات الأسماء (Namespaces) في المكتبات التي قمت بتثبيتها مسبقًا:</p>
<p dir="rtl"><strong>Python</strong></p>
</li>
<div dir="auto"><pre><span># Add references</span>
<span>from</span> <span>dotenv</span> <span>import</span> <span>load_dotenv</span>
<span>from</span> <span>azure</span>.<span>identity</span> <span>import</span> <span>DefaultAzureCredential</span>
<span>from</span> <span>azure</span>.<span>ai</span>.<span>projects</span> <span>import</span> <span>AIProjectClient</span>
<span>from</span> <span>openai</span> <span>import</span> <span>AzureOpenAI</span>
<span>import</span> <span>requests</span></pre><div dir="auto">
  </div></div>
<p dir="rtl"><strong>#C</strong></p>
<div dir="auto"><pre><span>// Add references</span>
<span>using</span> <span>Azure</span><span>.</span><span>Identity</span><span>;</span>
<span>using</span> <span>Azure</span><span>.</span><span>AI</span><span>.</span><span>Projects</span><span>;</span>
<span>using</span> <span>Azure</span><span>.</span><span>AI</span><span>.</span><span>OpenAI</span><span>;</span>
<span>using</span> <span>OpenAI</span><span>.</span><span>Images</span><span>;</span></pre><div dir="auto">
  </div></div>

<li>
<p dir="rtl">في الوظيفة <strong>الرئيسية</strong>، تحت التعليق <strong>الحصول على إعدادات التكوين</strong>، لاحظ أن التعليمة البرمجية تقوم بتحميل قيم سلسلة الاتصال بالمشروع واسم نشر النموذج التي قمت بتحديدها في ملف التكوين.</p>
</li>
<li>
<p dir="rtl">ضمن التعليق <strong>تهيئة عميل المشروع</strong>، أضف التعليمة البرمجية التالية للاتصال بمشروع مصنع الذكاء الاصطناعي في Azure باستخدام بيانات الاعتماد الخاصة بـ Azure التي قمت بتسجيل الدخول بها حاليًا:</p>
<p dir="rtl"><strong>Python</strong></p>
</li>
<div dir="auto"><pre><span># Initialize the project client</span>
<span>project_client</span> <span>=</span> <span>AIProjectClient</span>.<span>from_connection_string</span>(
    <span>conn_str</span><span>=</span><span>project_connection</span>,
    <span>credential</span><span>=</span><span>DefaultAzureCredential</span>())</pre><div dir="auto">
  </div></div>
<p dir="rtl"><strong>#C</strong></p>
<div dir="auto"><pre><span>// Initialize the project client</span>
<span>var</span> <span>projectClient</span> <span>=</span> <span>new</span> <span>AIProjectClient</span><span>(</span><span>project_connection</span><span>,</span>
                    <span>new</span> <span>DefaultAzureCredential</span><span>(</span><span>)</span><span>)</span><span>;</span></pre><div dir="auto">
  </div></div>

<li>
<p dir="rtl">تحت التعليق <strong>الحصول على عميل OpenAI</strong>، أضف التعليمات البرمجية التالية لإنشاء كائن عميل للدردشة مع نموذج:</p>
<p dir="rtl"><strong>Python</strong></p>
</li>
<div dir="auto"><pre><span># Get an OpenAI client</span>
<span>openai_client</span> <span>=</span> <span>project_client</span>.<span>inference</span>.<span>get_azure_openai_client</span>(<span>api_version</span><span>=</span><span>"2024-06-01"</span>)</pre><div dir="auto">
  </div></div>
<p dir="rtl"><strong>#C</strong></p>
<div dir="auto"><pre><span>// Get an OpenAI client</span>
<span>ConnectionResponse</span> <span>connection</span> <span>=</span> <span>projectClient</span><span>.</span><span>GetConnectionsClient</span><span>(</span><span>)</span><span>.</span><span>GetDefaultConnection</span><span>(</span><span>ConnectionType</span><span>.</span><span>AzureOpenAI</span><span>,</span> <span>withCredential</span><span>:</span> <span>true</span><span>)</span><span>;</span>
<p dir="auto"><span>var</span> <span>connectionProperties</span> <span>=</span> <span>connection</span><span>.</span><span>Properties</span> <span>as</span> <span>ConnectionPropertiesApiKeyAuth</span><span>;</span></p>
<p dir="auto"><span>AzureOpenAIClient</span> <span>openAIClient</span> <span>=</span> <span>new</span><span>(</span>
<span>new</span> <span>Uri</span><span>(</span><span>connectionProperties</span><span>.</span><span>Target</span><span>)</span><span>,</span>
<span>new</span> <span>AzureKeyCredential</span><span>(</span><span>connectionProperties</span><span>.</span><span>Credentials</span><span>.</span><span>Key</span><span>)</span><span>)</span><span>;</span></p>
<p dir="auto"><span>ImageClient</span> <span>openAIimageClient</span> <span>=</span> <span>openAIClient</span><span>.</span><span>GetImageClient</span><span>(</span><span>model_deployment</span><span>)</span><span>;</span></p></pre><div dir="auto"><p dir="auto"></p>
  </div></div>

<li>
<p dir="rtl">لاحظ أن التعليمات البرمجية تتضمن تكرار حلقي للسماح للمستخدم بإدخال مطالبة حتى يدخل "إنهاء". ثم في قسم التكرار، تحت التعليق <strong>إنشاء صورة</strong>، أضف التعليمات البرمجية التالية لإرسال المطالبة واسترجاع عنوان URL للصورة التي تم إنشاؤها من النموذج:</p>
<p dir="rtl"><strong>Python</strong></p>
</li>
<div dir="auto"><pre><span># Generate an image</span>
<span>result</span> <span>=</span> <span>openai_client</span>.<span>images</span>.<span>generate</span>(
    <span>model</span><span>=</span><span>model_deployment</span>,
    <span>prompt</span><span>=</span><span>input_text</span>,
    <span>n</span><span>=</span><span>1</span>
)
<p dir="auto"><span>json_response</span> <span>=</span> <span>json</span>.<span>loads</span>(<span>result</span>.<span>model_dump_json</span>())
<span>image_url</span> <span>=</span> <span>json_response</span>[<span>"data"</span>][<span>0</span>][<span>"url"</span>] </p></pre><div dir="auto"><p dir="auto"></p>
  </div></div>
<p dir="rtl"><strong>#C</strong></p>
<div dir="auto"><pre><span>// Generate an image</span>
<span>var</span> <span>imageGeneration</span> <span>=</span> <span>await</span> <span>openAIimageClient</span><span>.</span><span>GenerateImageAsync</span><span>(</span>
        <span>input_text</span><span>,</span>
        <span>new</span> <span>ImageGenerationOptions</span><span>(</span><span>)</span>
        <span>{</span>
            <span>Size</span> <span>=</span> <span>GeneratedImageSize</span><span>.</span><span>W1024xH1024</span>
        <span>}</span>
<span>)</span><span>;</span>
<span>imageUrl</span><span>=</span> <span>imageGeneration</span><span>.</span><span>Value</span><span>.</span><span>ImageUri</span><span>;</span></pre><div dir="auto">
  </div></div>

<li>
<p dir="rtl">لاحظ أن التعليمات البرمجية في الجزء المتبقي من الدالة <strong>main</strong> تمرر عنوان URL للصورة واسم ملف إلى دالة متوفرة، تنزل الصورة التي تم إنشاؤها وحفظها كملف png.</p>
</li>
<li>
<p dir="rtl">استخدم الأمر <strong>CTRL+S</strong> لحفظ التغييرات التي أجريتها على ملف التعليمات البرمجية، ثم استخدم الأمر <strong>CTRL+Q</strong> لإغلاق محرر التعليمات البرمجية مع إبقاء سطر أوامر Cloud Shell مفتوحًا.</p>
</li>
</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h3 tabindex="-1" dir="rtl" class="heading-element">شغّل تطبيق العميل</h3><a id="user-content-شغّل-تطبيق-العميل" class="anchor" aria-label="Permalink: شغّل تطبيق العميل" href="#شغّل-تطبيق-العميل"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-شغّل-تطبيق-العميل" aria-label="Permalink: شغّل تطبيق العميل" href="#شغّل-تطبيق-العميل"></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">في جزء سطر أوامر Cloud Shell، أدخل الأمر التالي لتشغيل التطبيق:</p>
<p dir="rtl"><strong>Python</strong></p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>python dalle-client.py
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python dalle-client.py" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>
<p dir="rtl"><strong>#C</strong></p>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>dotnet run
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="dotnet run" tabindex="0" role="button">
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
<p dir="rtl">عند المطالبة، أدخل طلبًا لإنشاء صورة، مثل <code>Create an image of a robot eating pizza</code>. بعد لحظات، من المفترض أن يؤكد التطبيق أنه تم حفظ الصورة.</p>
</li>
<li>
<p dir="rtl">جرّب المزيد من المطالبات. عند الانتهاء، أدخل <code>quit</code> للخروج من البرنامج.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: في هذا التطبيق البسيط، لم ننفّذ منطق للاحتفاظ بسجل المحادثة؛ لذلك سيعامل النموذج كل مطالبة على أنها طلب جديد دون أي سياق للمطالبة السابقة.</p>
</blockquote>
</li>
<li>
<p dir="rtl">لتنزيل وعرض الصور التي تم إنشاؤها بواسطة تطبيقك، استخدم أمر <strong>download</strong> في cloud shell - مع تحديد ملف .png الذي تم إنشاؤه:</p>
</li>
<div dir="auto"><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>download ./images/image_1.png
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="download ./images/image_1.png" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div><div dir="auto">
  </div></div>
<p dir="rtl">يُنشئ أمر التنزيل رابطًا منبثقًا في أسفل يمين متصفحك، والذي يمكنك تحديده لتنزيل الملف وفتحه.</p>

</ol>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">الملخص</h2><a id="user-content-الملخص" class="anchor" aria-label="Permalink: الملخص" href="#الملخص"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-الملخص" aria-label="Permalink: الملخص" href="#الملخص"></a></div>
<p dir="rtl">في هذا التمرين، استخدمت Azure AI Foundry وAzure OpenAI SDK لإنشاء تطبيق عميل يستخدم نموذج DALL-E لإنشاء الصور.</p>
<div dir="rtl"><div class="markdown-heading" dir="auto"><h2 tabindex="-1" dir="rtl" class="heading-element">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div><a id="user-content-تنظيف" aria-label="Permalink: تنظيف" href="#تنظيف"></a></div>
<p dir="rtl">إذا انتهيت من استكشاف DALL-E، يجب حذف الموارد التي أنشأتها في هذا التمرين لتجنب تكاليف Azure غير الضرورية.</p>
<ol dir="rtl">
<li>ارجع إلى علامة تبويب المتصفح التي تحتوي على بوابة Azure (أو أعد فتح <a href="https://portal.azure.com" rel="nofollow">بوابة Azure</a> في <code>https://portal.azure.com</code> في علامة تبويب متصفح جديدة) واعرض محتويات مجموعة الموارد التي نشرت فيها الموارد المستخدمة في هذا التدريب.</li>
<li>على شريط الأدوات، حدد <strong>حذف مجموعة الموارد</strong>.</li>
<li>أدخل اسم مجموعة الموارد وأكّد أنك تريد حذفها.</li>
</ol>
</div></div>
</article></div>
