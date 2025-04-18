---
lab:
  title: إنشاء صور باستخدام الذكاء الاصطناعي
  description: تعرّف على كيفية استخدام نموذج DALL-E من OpenAI لإنشاء صور.
  status: new
---

# إنشاء صور باستخدام الذكاء الاصطناعي

في هذا التمرين، تستخدم نموذج الذكاء الاصطناعي التوليدي DALL-E من OpenAI لإنشاء صور. ستطوّر تطبيقك باستخدام Azure AI Foundry وخدمة Azure OpenAI.

سيستغرق هذا التدريب حوالي **30** دقيقة.

## إنشاء مشروع في مصنع الذكاء الاصطناعي في Azure

دعنا نبدأ بإنشاء مشروع في مصنع الذكاء الاصطناعي في Azure.

1. في متصفح الويب، افتح [مدخل Azure AI Foundry](https://ai.azure.com) على `https://ai.azure.com` وسجّل الدخول باستخدام بيانات اعتماد Azure الخاصة بك. أغلق أية تلميحات أو أجزاء تشغيل سريع يتم فتحها عندما تقوم بتسجيل الدخول، وإذا لزم الأمر، استخدم شعار **مصنع الذكاء الاصطناعي في Azure** في أعلى اليسار للانتقال إلى الصفحة الرئيسية، والتي تبدو مشابهة للصورة التالية:

    ![لقطة شاشة لمدخل Azure AI Foundry.](../media/ai-foundry-home.png)

1. في الصفحة الرئيسية، حدد **+ إنشاء مشروع**.
1. في معالج **إنشاء مشروع**، أدخل اسم مشروع مناسب لـ (على سبيل المثال، `my-ai-project`) ثم راجع موارد Azure التي سيتم إنشاؤها تلقائيا لدعم مشروعك.
1. حدد **تخصيص** وحدد الإعدادات التالية لمركزك:
    - **اسم المركز**: *اسم فريد - على سبيل المثال `my-ai-hub`*
    - **Subscription**: *اشتراكك في Azure*
    - **مجموعة الموارد**: *أنشئ مجموعة موارد جديدة باسم فريد (على سبيل المثال، `my-ai-resources`)، أو حدد مجموعة موجودة*
    - **الموقع**: حدد **ساعدني في الاختيار** ثم حدد **dalle** في نافذة مساعد الموقع واستخدم المنطقة الموصى بها\*
    - **توصيل خدمات الذكاء الاصطناعي في Azure أو Azure OpenAI**: *أنشيء مورد خدمات ذكاء اصطناعي جديد باسم مناسب (على سبيل المثال، `my-ai-services`) أو استخدام مورد موجود*
    - **الاتصال بـ Azure AI Search**: تخطي الاتصال

    > \* تخضع موارد Azure OpenAI للتقييد على مستوى المستأجر من خلال الحصص الإقليمية. في حالة الوصول إلى حد الحصة النسبية لاحقًا في التمرين، هناك احتمال أنك قد تحتاج إلى إنشاء مورد آخر في منطقة مختلفة.

1. حدد **التالي** لمراجعة التكوين الخاص بك. ثم حدد **إنشاء** وانتظر حتى تكتمل العملية.
1. عند إنشاء مشروعك، أغلق أي تلميحات يتم عرضها وراجع صفحة المشروع في مدخل مصنع الذكاء الاصطناعي في Azure، والذي يجب أن يبدو مشابهة للصورة التالية:

    ![لقطة شاشة توضح تفاصيل مشروع ذكاء اصطناعي في Azure في مدخل مصنع الذكاء الاصطناعي في Azure.](../media/ai-foundry-project.png)

## نشر نموذج DALL-E

الآن أنت مستعد لنشر نموذج DALL-E لدعم إنشاء الصور.

1. في شريط الأدوات في الجزء العلوي الأيمن من صفحة مشروع مصنع الذكاء الاصطناعي في Azure، استخدم أيقونة **ميزات المعاينة** لتمكين ميزة **توزيع النماذج على خدمة استدلال نموذج الذكاء الاصطناعي في Azure**.
1. في الجزء الموجود على يسار مشروعك، في قسم **أصولي**، حدد صفحة **النماذج + نقاط النهاية**.
1. في صفحة **النماذج + نقاط النهاية**، في علامة التبويب **عمليات توزيع النماذج**، في القائمة **+ نشر النموذج**، حدّد **توزيع النموذج الأساسي**.
1. ابحث عن نموذج **dall-e-3** في القائمة، ثم حدده وأكّده.
1. وافق على اتفاقية الترخيص إذا طلب منك ذلك، ثم وزّع النموذج بالإعدادات التالية عن طريق تحديد **تخصيص** في تفاصيل التوزيع:
    - **اسم التوزيع**: *اسم فريد لتوزيع النموذج الخاص بك - على سبيل المثال `dall-e-3` (تذكر الاسم الذي تعينه، ستحتاج إليه لاحقًا*)
    - **نوع التوزيع**: قياسي
    - **تفاصيل التوزيع**: *استخدام الإعدادات الافتراضية*
1. انتظر حتى تصبح حالة التزويد للتوزيع **مكتملة**.

## اختبر النموذج في مساحة التجربة

قبل إنشاء تطبيق عميل، دعنا نختبر نموذج DALL-E في مساحة التجربة.

1. في صفحة نموذج DALL-E الذي نشرته، حدد **فتح في مساحة التجربة** (أو في صفحة **مساحات التجربة**، افتح **مساحة تجربة الصور**).
1. تأكد من تحديد نشر نموذج DALL-E. ثم، في مربع **المطالبة**، أدخل مطالبة مثل `Create an image of an robot eating spaghetti`.
1. راجع الصورة الناتجة في مساحة التجربة:

    ![لقطة شاشة لمساحة تجربة الصور مع صورة تم إنشاؤها.](../media/images-playground.png)

1. أدخل مطالبة متابعة، مثل `Show the robot in a restaurant` وراجع الصورة الناتجة.
1. استمر في الاختبار باستخدام مطالبات جديدة لتحسين الصورة حتى تصبح راضيًا عنها.

## أنشئ تطبيق عميل

يبدو أن النموذج يعمل في مساحة التجربة. الآن يمكنك استخدام Azure OpenAI SDK لاستخدامه في تطبيق عميل.

> **تلميح**: يمكنك اختيار تطوير الحل الخاص بك باستخدام Python أو Microsoft C#. اتبع الإرشادات في القسم المناسب للغة التي اخترتها.

### إعداد تكوين التطبيق

1. في مدخل مصنع الذكاء الاصطناعي في Azure، اعرض صفحة **النظرة العامة** لمشروعك.
1. في منطقة **تفاصيل المشروع**، لاحظ **سلسلة الاتصال للمشروع**. ستستخدم سلسلة الاتصال هذه للاتصال بمشروعك في تطبيق العميل.
1. افتح علامة تبويب جديدة للمتصفح (مع إبقاء مدخل مصنع الذكاء الاصطناعي في Azure مفتوحًا في علامة التبويب الموجودة). بعد ذلك في علامة التبويب الجديدة، انتقل إلى [بوابة Azure](https://portal.azure.com) على `https://portal.azure.com`؛ وسجّل الدخول باستخدام بيانات اعتماد Azure الخاصة بك إذا طُلب منك ذلك.
1. استخدم الزر **[\>_]** الموجود على يمين شريط البحث أعلى الصفحة لإنشاء Cloud Shell جديد في بوابة Azure، وتحديد بيئة ***PowerShell***. يوفّر Cloud Shell واجهة سطر أوامر في جزء أسفل بوابة Azure.

    > **ملاحظة**: إذا كنت قد أنشأت مسبقًا Cloud Shell يستخدم بيئة *معالج Bash*، فبدّل إلى ***PowerShell***.

1. في شريط أدوات Cloud Shell، في قائمة **الإعدادات**، حدد **الانتقال إلى الإصدار الكلاسيكي** (هذا مطلوب لاستخدام محرر التعليمات البرمجية).

    > **تلميح**: عند لصق الأوامر في CloudShell، قد يشغل الإخراج مساحة كبيرة من ذاكرة التخزين المؤقت للشاشة. يمكنك مسح الشاشة عن طريق إدخال الأمر `cls` لتسهيل التركيز على كل مهمة.

1. في جزء PowerShell، أدخل الأوامر التالية لاستنساخ مستودع GitHub لهذا التمرين:

    ```
    rm -r mslearn-openai -f
    git clone https://github.com/microsoftlearning/mslearn-openai mslearn-openai
    ```

> **ملاحظة**: اتبع الخطوات الخاصة بلغة البرمجة التي اخترتها.

1. بعد استنساخ مخزن البيانات الخاصة انتقل إلى المجلد الذي يحتوي على ملفات التعليمات البرمجية للتطبيق:  

    **Python**

    ```
   cd mslearn-openai/Labfiles/03-image-generation/Python
    ```

    **C#**

    ```
   cd mslearn-openai/Labfiles/03-image-generation/CSharp
    ```

1. في جزء سطر أوامر Cloud Shell، أدخل الأمر التالي لتثبيت المكتبات التي ستستخدمها:

    **Python**

    ```
   pip install python-dotenv azure-identity azure-ai-projects openai requests
    ```

    *يمكنك تجاهل الأخطاء المتعلقة بإصدار pip والمسار المحلي*

    **C#**

    ```
   dotnet add package Azure.Identity
   dotnet add package Azure.AI.Projects --prerelease
   dotnet add package Azure.AI.OpenAI
    ```

1. أدخل الأمر التالي لتحرير ملف التكوين الذي تم توفيره:

    **Python**

    ```
   code .env
    ```

    **C#**

    ```
   code appsettings.json
    ```

    يتم فتح الملف في محرر التعليمات البرمجية.

1. في ملف التعليمات البرمجية، استبدل العنصر النائب **your_project_endpoint** بسلسلة الاتصال لمشروعك (المنسوخة من صفحة **نظرة عامة** في بوابة Azure AI Foundry)، واستبدل العنصر النائب **your_model_deployment** بالاسم الذي عيّنته لنشر نموذج dall-e-3.
1. بعد استبدال العناصر النائبة، استخدم الأمر **CTRL+S** لحفظ التغييرات ثم استخدم الأمر **CTRL+Q** لإغلاق محرر التعليمات البرمجية مع إبقاء سطر أوامر Cloud Shell مفتوحWا.

### اكتب التعليمة البرمجية للاتصال بمشروعك والدردشة مع نموذجك

> **تلميح**: عند إضافة التعليمات البرمجية، تأكد من الحفاظ على المسافة البادئة الصحيحة.

1. أدخل الأمر التالي لتحرير ملف التعليمات البرمجية الذي تم توفيره:

    **Python**

    ```
   code dalle-client.py
    ```

    **C#**

    ```
   code Program.cs
    ```

1. في ملف التعليمات البرمجية، لاحظ العبارات الموجودة في أعلى الملف والتي تمت إضافتها لاستيراد مساحات الأسماء (Namespaces) الضرورية لـ (SDK). ثم تحت التعليق **إضافة المراجع**، أضف التعليمة البرمجية التالية للإشارة إلى مساحات الأسماء (Namespaces) في المكتبات التي قمت بتثبيتها مسبقًا:

    **Python**

    ```
   from dotenv import load_dotenv
   from azure.identity import DefaultAzureCredential
   from azure.ai.projects import AIProjectClient
   from openai import AzureOpenAI
   import requests
    ```

    **C#**

    ```
   using Azure.Identity;
   using Azure.AI.Projects;
   using Azure.AI.OpenAI;
   using OpenAI.Images;
    ```

1. في الوظيفة **الرئيسية**، تحت التعليق **الحصول على إعدادات التكوين**، لاحظ أن التعليمة البرمجية تقوم بتحميل قيم سلسلة الاتصال بالمشروع واسم نشر النموذج التي قمت بتحديدها في ملف التكوين.
1. ضمن التعليق **تهيئة عميل المشروع**، أضف التعليمة البرمجية التالية للاتصال بمشروع مصنع الذكاء الاصطناعي في Azure باستخدام بيانات الاعتماد الخاصة بـ Azure التي قمت بتسجيل الدخول بها حاليًا:

    **Python**

    ```
   project_client = AIProjectClient.from_connection_string(
        conn_str=project_connection,
        credential=DefaultAzureCredential())
    ```

    **C#**

    ```
   var projectClient = new AIProjectClient(project_connection,
                        new DefaultAzureCredential());
    ```

1. تحت التعليق **الحصول على عميل OpenAI**، أضف التعليمات البرمجية التالية لإنشاء كائن عميل للدردشة مع نموذج:

    **Python**

    ```
   openai_client = project_client.inference.get_azure_openai_client(api_version="2024-06-01")

    ```

    **C#**

    ```
   ConnectionResponse connection = projectClient.GetConnectionsClient().GetDefaultConnection(ConnectionType.AzureOpenAI, withCredential: true);

   var connectionProperties = connection.Properties as ConnectionPropertiesApiKeyAuth;

   AzureOpenAIClient openAIClient = new(
        new Uri(connectionProperties.Target),
        new AzureKeyCredential(connectionProperties.Credentials.Key));

   ImageClient openAIimageClient = openAIClient.GetImageClient(model_deployment);

    ```

1. لاحظ أن التعليمات البرمجية تتضمن تكرار حلقي للسماح للمستخدم بإدخال مطالبة حتى يدخل "إنهاء". ثم في قسم التكرار، تحت التعليق **إنشاء صورة**، أضف التعليمات البرمجية التالية لإرسال المطالبة واسترجاع عنوان URL للصورة التي تم إنشاؤها من النموذج:

    **Python**

    ```python
   result = openai_client.images.generate(
        model=model_deployment,
        prompt=input_text,
        n=1
    )

    json_response = json.loads(result.model_dump_json())
    image_url = json_response["data"][0]["url"] 
    ```

    **C#**

    ```
   var imageGeneration = await openAIimageClient.GenerateImageAsync(
            input_text,
            new ImageGenerationOptions()
            {
                Size = GeneratedImageSize.W1024xH1024
            }
   );
   imageUrl= imageGeneration.Value.ImageUri;
    ```

1. لاحظ أن التعليمات البرمجية في الجزء المتبقي من الدالة **main** تمرر عنوان URL للصورة واسم ملف إلى دالة متوفرة، تنزل الصورة التي تم إنشاؤها وحفظها كملف png.

1. استخدم الأمر **CTRL+S** لحفظ التغييرات التي أجريتها على ملف التعليمات البرمجية، ثم استخدم الأمر **CTRL+Q** لإغلاق محرر التعليمات البرمجية مع إبقاء سطر أوامر Cloud Shell مفتوحًا.

### شغّل تطبيق العميل

1. في جزء سطر أوامر Cloud Shell، أدخل الأمر التالي لتشغيل التطبيق:

    **Python**

    ```
   python dalle-client.py
    ```

    **C#**

    ```
   dotnet run
    ```

1. عند المطالبة، أدخل طلبًا لإنشاء صورة، مثل `Create an image of a robot eating pizza`. بعد لحظات، من المفترض أن يؤكد التطبيق أنه تم حفظ الصورة.
1. جرّب المزيد من المطالبات. عند الانتهاء، أدخل `quit` للخروج من البرنامج.

    > **ملاحظة**: في هذا التطبيق البسيط، لم ننفّذ منطق للاحتفاظ بسجل المحادثة؛ لذلك سيعامل النموذج كل مطالبة على أنها طلب جديد دون أي سياق للمطالبة السابقة.

1. لتنزيل وعرض الصور التي تم إنشاؤها بواسطة التطبيق، استخدم زر **تحميل/تنزيل الملفات** في شريط الأدوات لجزء Cloud Shell لتنزيل ملف، ثم افتحه. لتنزيل ملف، أكمل مسار الملف في واجهة التنزيل؛ على سبيل المثال:

    **Python**

    /home/*user*`/mslearn-openai/Labfiles/03-image-generation/Python/images/image_1.png`

    **C#**

    /home/*user*`/mslearn-openai/Labfiles/03-image-generation/CSharp/images/image_1.png`

## الملخص

في هذا التمرين، استخدمت Azure AI Foundry وAzure OpenAI SDK لإنشاء تطبيق عميل يستخدم نموذج DALL-E لإنشاء الصور.

## تنظيف

إذا انتهيت من استكشاف DALL-E، يجب حذف الموارد التي أنشأتها في هذا التمرين لتجنب تكاليف Azure غير الضرورية.

1. ارجع إلى علامة تبويب المتصفح التي تحتوي على بوابة Azure (أو أعد فتح [بوابة Azure](https://portal.azure.com) في `https://portal.azure.com` في علامة تبويب متصفح جديدة) واعرض محتويات مجموعة الموارد التي نشرت فيها الموارد المستخدمة في هذا التدريب.
1. على شريط الأدوات، حدد **حذف مجموعة الموارد**.
1. أدخل اسم مجموعة الموارد وأكّد أنك تريد حذفها.
