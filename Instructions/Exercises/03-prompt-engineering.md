---
lab:
  title: استخدام هندسة التلقين في تطبيقك
  status: stale
---

# استخدام هندسة التلقين في تطبيقك

تؤثر كيفية تشكيل المطورين لمطالبتهم بشكل كبير على كيفية استجابة نموذج الذكاء الاصطناعي التوليدي عند استخدام خدمة Azure OpenAI. يمكن لنماذج Azure OpenAI تخصيص المحتوى وتنسيقه، إذا طلب ذلك بطريقة واضحة وموجزة. في هذا النموذج، ستتعلم كيف تساعد المطالبات المختلفة للمحتوى المماثل في تشكيل استجابة نموذج الذكاء الاصطناعي لتلبية متطلباتك بشكل أفضل.

في سيناريو هذا التدريب، سوف تقوم بدور مطور برامج يعمل على حملة إعلانية عن الحياة البرية. أنت تستكشف كيفية استخدام الذكاء الاصطناعي التوليدي لتحسين رسائل البريد الإلكتروني الإعلانية وتصنيف المقالات التي قد تنطبق على فريقك. يمكن تطبيق تقنيات هندسة التلقين المستخدمة في التدريب بشكل مماثل لمجموعة متنوعة من حالات الاستخدام.

سيستغرق هذا التدريب حوالي **30** دقيقة.

## توفير مورد Azure OpenAI

إذا لم يكن لديك موردًا بالفعل، يمكنك توفير مورد Azure OpenAI في اشتراك Azure الخاص بك.

1. سجّل الدخول إلى **Azure portal** من `https://portal.azure.com`.
2. إنشاء مورد **Azure OpenAI** بالإعدادات التالية:
    - **اشتراك**: *حدد اشتراك Azure الذي جرت الموافقة عليه للوصول إلى خدمة Azure OpenAI*
    - **مجموعة الموارد**: *اختيار مجموعة موارد أو إنشاءها*
    - **المنطقة**: *إجراء اختيار **عشوائي** من أي من المناطق التالية*\*
        - شرق الولايات المتحدة
        - East US 2
        - وسط شمال الولايات المتحدة
        - South Central US
        - منطقة السويد الوسطى
        - غرب الولايات المتحدة
        - غرب الولايات المتحدة الأمريكية 3
    - **الاسم**: *اسم فريد من اختيارك*
    - **مستوى التسعير**: قياسي S0

    > \* موارد Azure OpenAI مقيدة بالحصص النسبية الإقليمية. تتضمن المناطق المدرجة الحصة النسبية الافتراضية لنوع (أنواع) النموذج المستخدمة في هذا التمرين. يؤدي اختيار منطقة عشوائيًا إلى تقليل مخاطر وصول منطقة واحدة إلى حد الحصة النسبية في السيناريوهات التي تشارك فيها اشتراكًا مع مستخدمين آخرين. في حالة الوصول إلى حد الحصة النسبية لاحقًا في التمرين، هناك احتمال أنك قد تحتاج إلى إنشاء مورد آخر في منطقة مختلفة.

3. يُرجى الانتظار لاكتمال التوزيع. ثم انتقل إلى مورد Azure OpenAI الموزّع في مدخل Microsoft Azure.

## توزيع النموذج

يوفر Azure بوابة على الويب يسمى **بوابة Azure AI Foundry**، والتي يمكنك استخدامها لنشر النماذج وإدارتها واستكشافها. ستبدأ استكشافك لـ Azure OpenAI باستخدام بوابة Azure AI Foundry لنشر نموذج.

> **ملاحظة**: أثناء استخدام بوابة Azure AI Foundry، قد يتم عرض مربعات رسائل تقترح عليك تنفيذ مهام. يمكنك إغلاق هذه الخطوات واتباع الخطوات الواردة في هذا التمرين.

1. في بوابة Azure، في صفحة **نظرة عامة** لمورد Azure OpenAI الخاص بك، مرّر لأسفل إلى قسم **بدء الاستخدام** وحدد الزر للانتقال إلى **بوابة AI Foundry** (المعروفة سابقًا باسم AI Studio).
1. في بوابة Azure AI Foundry، في الجزء الموجود على اليسار، حدد صفحة **عمليات النشر** واعرض عمليات نشر النموذج الحالية لديك. إذا لم يكن لديك واحد بالفعل، أنشئ نشرًا جديدًا لنموذج **gpt-4o** باستخدام الإعدادات التالية:
    - **اسم التوزيع**: *اسم فريد من اختيارك*
    - **النموذج**: gpt-4
    - **إصدار النموذج**: *استخدام الإصدار الافتراضي*
    - **نوع التوزيع**: قياسي
    - **حد معدل الرموز المميزة في الدقيقة**: 5K\*
    - **عامل تصفية المحتوى**: افتراضية
    - **تمكين الحصة النسبية الديناميكية**: معطّل

    > \*الحد الأقصى لمعدل 5000 رمز مميز في الدقيقة هو أكثر من كاف لإكمال هذا التمرين مع ترك سعة للأشخاص الآخرين الذين يستخدمون نفس الاشتراك.

## استكشف تقنيات هندسة التلقين

لنبدأ باستكشاف بعض تقنيات هندسة التلقين في دردشة playground.

1. في الجزء الجانبي الأيسر، في قسم **البيئات**، حدد صفحة **دردشة**. تتكون صفحة بيئة **الدردشة** من صف من الأزرار ولوحتين رئيسيتين (والتي يمكن ترتيبها من اليمين إلى اليسار أفقيًا، أو من أعلى إلى أسفل عموديًا حسب دقة الشاشة لديك):
    - **الإعداد** - يُستخدم لتحديد التوزيع الخاص بك، وتعريف رسالة النظام، وتعيين معلمات للتفاعل مع توزيعك.
    - **محفوظات الدردشة** - تُستخدم لإرسال رسائل الدردشة وعرض الردود.
1. في جزء **عمليات التوزيع**، تأكّد من تحديد نشر نموذج gpt-4o الخاص بك.
1. راجع رسالة النظام الافتراضية الموجودة في مربع النص الموجود أسفل التوزيع المحدد مباشرةً، والتي يجب أن تكون *أنت مساعد الذكاء الاصطناعي الذي يساعد الأشخاص في العثور على المعلومات.*
1. في **محفوظات الدردشة**، أرسل الاستعلام التالي:

    ```prompt
    What kind of article is this?
    ---
    Severe drought likely in California
    
    Millions of California residents are bracing for less water and dry lawns as drought threatens to leave a large swath of the region with a growing water shortage.
    
    In a remarkable indication of drought severity, officials in Southern California have declared a first-of-its-kind action limiting outdoor water use to one day a week for nearly 8 million residents.
    
    Much remains to be determined about how daily life will change as people adjust to a drier normal. But officials are warning the situation is dire and could lead to even more severe limits later in the year.
    ```

    توفر الاستجابة وصفاً للمقالة. ومع ذلك، افترض أنك تريد تنسيقاً أكثر تحديداً لتصنيف المقالات.

1. في قسم **إعداد**، قم بتغيير رسالة النظام إلى `You are a news aggregator that categorizes news articles.`

1. في جزء رسالة النظام الجديدة، حدد زر **إضافة قسم**، ثم اختر **أمثلة**. ثم، أضف المثال التالي.

    **المستخدم:**

    ```prompt
    What kind of article is this?
    ---
    New York Baseballers Wins Big Against Chicago
    
    New York Baseballers mounted a big 5-0 shutout against the Chicago Cyclones last night, solidifying their win with a 3 run homerun late in the bottom of the 7th inning.
    
    Pitcher Mario Rogers threw 96 pitches with only two hits for New York, marking his best performance this year.
    
    The Chicago Cyclones' two hits came in the 2nd and the 5th innings but were unable to get the runner home to score.
    ```

    **Assistant:**

    ```prompt
    Sports
      ```

1. أضف مثالاً آخر باستخدام النص التالي.

    **المستخدم:**

    ```prompt
    Categorize this article:
    ---
    Joyous moments at the Oscars
    
    The Oscars this past week where quite something!
    
    Though a certain scandal might have stolen the show, this year's Academy Awards were full of moments that filled us with joy and even moved us to tears.
    These actors and actresses delivered some truly emotional performances, along with some great laughs, to get us through the winter.
    
    From Robin Kline's history-making win to a full performance by none other than Casey Jensen herself, don't miss tomorrows rerun of all the festivities.
    ```

    **Assistant:**

    ```prompt
    Entertainment
    ```

1. استخدم زر **تطبيق التغييرات** أسفل مربع نص رسالة النظام في قسم **الإعداد** لحفظ تغييراتك.

1. في قسم **محفوظات الدردشة**، أعد إرسال المطالبة التالية:

    ```prompt
    What kind of article is this?
    ---
    Severe drought likely in California
    
    Millions of California residents are bracing for less water and dry lawns as drought threatens to leave a large swath of the region with a growing water shortage.
    
    In a remarkable indication of drought severity, officials in Southern California have declared a first-of-its-kind action limiting outdoor water use to one day a week for nearly 8 million residents.
    
    Much remains to be determined about how daily life will change as people adjust to a drier normal. But officials are warning the situation is dire and could lead to even more severe limits later in the year.
    ```

    يؤدي الجمع بين رسالة نظام أكثر تحديداً وبعض الأمثلة على الاستعلامات والاستجابات المتوقعة إلى تنسيق متسق للنتائج.

1. قم بتغيير رسالة النظام مرة أخرى إلى القالب الافتراضي، والذي يجب أن يكون `You are an AI assistant that helps people find information.` بدون أمثلة. ثم، قم بتطبيق التغييرات.

1. في قسم **محفوظات الدردشة**، أرسل المطالبة التالية:

    ```prompt
    # 1. Create a list of animals
    # 2. Create a list of whimsical names for those animals
    # 3. Combine them randomly into a list of 25 animal and name pairs
    ```

    من المحتمل أن يستجيب النموذج بإجابة لتلبية المطالبة، وتقسيمه إلى قائمة مرقمّة. هذه استجابة مناسبة، ولكن افترض أن ما أردته بالفعل هو أن يكتب النموذج برنامج Python الذي ينفذ المهام التي وصفتها؟

1. قم بتغيير رسالة النظام إلى `You are a coding assistant helping write python code.` وطبّق التغييرات.
1. أعد إرسال المطالبة التالية إلى النموذج:

    ```prompt
    # 1. Create a list of animals
    # 2. Create a list of whimsical names for those animals
    # 3. Combine them randomly into a list of 25 animal and name pairs
    ```

    يجب أن يستجيب النموذج بشكل صحيح مع تعليمات python البرمجية التي تفعل ما طلبته التعليقات.

## الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية

الآن دعونا نستكشف استخدام هندسة التلقين في تطبيق يستخدم SDK لخدمة Azure OpenAI. ستقوم بتطوير تطبيقك باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في مستودع GitHub.

> **تلميح**: إذا نسخت بالفعل مستودع **mslearn-openai**، فافتحه في تعليمة Visual Studio البرمجية. وإلا فاتبع هذه الخطوات لاستنساخه إلى بيئة تطويرك.

1. ابدأ تشغيل Visual Studio Code.
2. افتح لوحة الأوامر (SHIFT+CTRL+P أو **View** > **Command Palette...**)، ثم نفّذ أمر **Git: Clone** لاستنساخ المستودع `https://github.com/MicrosoftLearning/mslearn-openai` إلى مجلد محلي (لا يهم أي مجلد تختاره).
3. عند استنساخ المستودع، افتح المجلد في Visual Studio Code.

    > **ملاحظة**: إذا عرضت لك Visual Studio Code رسالة منبثقة لمطالبتك بالثقة في التعليمات البرمجية التي تفتحها، فانقر فوق **نعم، أثق في خيار الكُتاب** في النافذة المنبثقة.

4. انتظر حتى تثبيت ملفات إضافية لدعم مشاريع التعليمات البرمجية C# في المستودع.

    > **ملاحظة**: في حالة مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد **ليس الآن**.

## تكوين تطبيقك

تم توفير تطبيقات لكل من C# وPython، ويمتلك كلا التطبيقين نفس الوظيفة. أولاً، ستكمل بعض الأجزاء الرئيسية من التطبيق لتمكين استخدام مورد Azure OpenAI الخاص بك مع استدعاءات واجهة برمجة التطبيقات (API) غير المتزامنة.

1. في تعليمات Visual Studio البرمجية في جزء **المستكشف**، انتقِل إلى المجلد **Labfiles/03-prompt-engineering**، وقم بتوسيع المجلد **CSharp** أو **Python** حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي تريد دمج وظيفة Azure OpenAI فيه.
2. انقر بزر الماوس الأيمن فوق المجلد **CSharp** أو **Python** الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وافتح وحدة طرفية متكاملة. ثم، عليك تثبيت حزمة Azure OpenAI SDK عن طريق تشغيل الأمر المناسب لتفضيل اللغة لديك:

    **C#:**

    ```powershell
    dotnet add package Azure.AI.OpenAI --version 2.1.0
    ```

    **Python**:

    ```powershell
    pip install openai==1.65.2
    ```

3. في جزء **مستكشف**، في مجلد **CSharp** أو **Python**، افتح ملف التكوين للغة المفضلة لديك

    - **C#**: appsettings.json
    - **Python**: .env

4. تحديث قيم التكوين لتشمل:
    - **نقطة النهاية** و**مفتاح** من مورد Azure OpenAI الذي أنشأته (متوفر في صفحة **المفاتيح ونقطة النهاية** لمورد Azure OpenAI الخاص بك في مدخل Microsoft Azure)
    - **اسم عملية النشر** الذي حددته لنشر النموذج الخاص بك (متوفر في صفحة **عمليات النشر** في بوابة Azure AI Foundry).
5. احفظ ملف التكوين.

## أضف تعليمات برمجية لاستخدام خدمة Azure OpenAI

أنت الآن جاهز لاستخدام Azure OpenAI SDK لاستهلاك نموذجك الموزع.

1. في جزء **مستكشف**، في المجلد **CSharp** أو **Python**، افتح ملف التعليمات البرمجية للغة المفضلة لديك، واستبدل التعليق ***أضف حزمة Azure OpenAI*** بالتعليمات البرمجية لإضافة مكتبة Azure OpenAI SDK:

    **C#**: Program.cs

    ```csharp
    // Add Azure OpenAI package
    using Azure.AI.OpenAI;
    using OpenAI.Chat;
    ```

    **Python**: prompt-engineering.py

    ```python
    # Add Azure OpenAI package
    from openai import AsyncAzureOpenAI
    ```

2. في ملف التعليمات البرمجية، ابحث عن التعليق ***تكوين عميل Azure OpenAI***، وأضف التعليمات البرمجية لتكوين عميل Azure OpenAI:

    **C#**: Program.cs

    ```csharp
    // Configure the Azure OpenAI client
    AzureOpenAIClient azureClient = new (new Uri(oaiEndpoint), new ApiKeyCredential(oaiKey));
    ChatClient chatClient = azureClient.GetChatClient(oaiDeploymentName);
    ```

    **Python**: prompt-engineering.py

    ```python
    # Configure the Azure OpenAI client
    client = AsyncAzureOpenAI(
        azure_endpoint = azure_oai_endpoint, 
        api_key=azure_oai_key,  
        api_version="2024-02-15-preview"
        )
    ```

3. في الدالة التي تستدعي نموذج Azure OpenAI، ضمن ***تنسيق التعليق وإرسال الطلب إلى النموذج***، أضف التعليمات البرمجية لتنسيق وإرسال الطلب إلى النموذج.

    **C#**: Program.cs

    ```csharp
    // Format and send the request to the model
    var chatCompletionsOptions = new ChatCompletionOptions()
    {
        Temperature = 0.7f,
        MaxOutputTokenCount = 800
    };
    
    // Get response from Azure OpenAI
    ChatCompletion response = await chatClient.CompleteChatAsync(
        [
            new SystemChatMessage(systemMessage),
            new UserChatMessage(userMessage),
        ],
        chatCompletionsOptions);
    ```

    **Python**: prompt-engineering.py

    ```python
    # Format and send the request to the model
    messages =[
        {"role": "system", "content": system_message},
        {"role": "user", "content": user_message},
    ]
    
    print("\nSending request to Azure OpenAI model...\n")

    # Call the Azure OpenAI model
    response = await client.chat.completions.create(
        model=model,
        messages=messages,
        temperature=0.7,
        max_tokens=800
    )
    ```

4. احفظ التغييرات في ملف التعليمة البرمجية.

## تشغيل التطبيق الخاص بك

الآن بعد أن نجح تكوين التطبيق الخاص بك، عليك تشغيله لإرسال طلبك إلى النموذج الخاص بك ومراقبة الاستجابة. ستلاحظ أن الفرق الوحيد بين الخيارات المختلفة هو محتوى المطالبة، وتظل جميع المعلمات الأخرى (مثل عدد الرموز المميزة ودرجة الحرارة) كما هي لكل طلب.

1. في مجلد اللغة المفضلة لديك، افتح `system.txt` في Visual Studio Code. لكل من التفاعلات، ستقوم بإدخال **رسالة النظام** في هذا الملف وحفظها. سيتوقف كل تكرار مؤقتاً أولاً لتغيير رسالة النظام.
1. في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.

    - **C#:** `dotnet run`
    - **Python**: `python prompt-engineering.py`

    > **تلميح**: يمكنك استخدام أيقونة **تكبير حجم اللوحة** (**^**) في شريط أدوات المحطة الطرفية لرؤية المزيد من نص وحدة التحكم.

1. بالنسبة للتكرار الأول، أدخل المطالبات التالية:

    **رسالة النظام**

    ```prompt
    You are an AI assistant
    ```

    **رسالة المستخدم:**

    ```prompt
    Write an intro for a new wildlife Rescue
    ```

1. مراقبة المخرجات. ومن المرجح أن ينتج نموذج الذكاء الاصطناعي مقدمة عامة جيدة حول إنقاذ الحياة البرية.
1. بعد ذلك، أدخل المطالبات التالية التي تحدد تنسيقاً للاستجابة:

    **رسالة النظام**

    ```prompt
    You are an AI assistant helping to write emails
    ```

    **رسالة المستخدم:**

    ```prompt
    Write a promotional email for a new wildlife rescue, including the following: 
    - Rescue name is Contoso 
    - It specializes in elephants 
    - Call for donations to be given at our website
    ```

    > **تلميح**: قد تجد أن الكتابة التلقائية في الجهاز الظاهري (VM) لا تعمل بشكل جيد مع المطالبات التي تتكون من عدة أسطر. إذا كانت هذه هي مشكلتك، فانسخ المطالبة بأكملها ثم الصقها في التعليمة البرمجية لـ Visual Studio.

1. مراقبة المخرجات. في هذه المرة، من المحتمل أن ترى تنسيق رسالة بريد إلكتروني تتضمن الحيوانات المحددة، بالإضافة إلى دعوة للتبرعات.
1. وبعد ذلك، أدخل المطالبات التالية التي تحدد المحتوى بالإضافة إلى ذلك:

    **رسالة النظام**

    ```prompt
    You are an AI assistant helping to write emails
    ```

    **رسالة المستخدم:**

    ```prompt
    Write a promotional email for a new wildlife rescue, including the following: 
    - Rescue name is Contoso 
    - It specializes in elephants, as well as zebras and giraffes 
    - Call for donations to be given at our website 
    Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits.
    ```

1. لاحظ النتائج، وشاهد كيفية تغيير البريد الإلكتروني استناداً إلى الإرشادات الواضحة.
1. بعد ذلك، أدخل المطالبات التالية حيث نضيف تفاصيل حول النبرة إلى رسالة النظام:

    **رسالة النظام**

    ```prompt
    You are an AI assistant that helps write promotional emails to generate interest in a new business. Your tone is light, chit-chat oriented and you always include at least two jokes.
    ```

    **رسالة المستخدم:**

    ```prompt
    Write a promotional email for a new wildlife rescue, including the following: 
    - Rescue name is Contoso 
    - It specializes in elephants, as well as zebras and giraffes 
    - Call for donations to be given at our website 
    Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits.
    ```

1. مراقبة المخرجات. وفي هذه المرة، من المحتمل أن ترى البريد الإلكتروني بتنسيق مماثل، ولكن بنبرة غير رسمية أكثر بكثير. من المحتمل أن ترى النكات مضمنة!
1. للتكرار النهائي، نحن نبتعد عن إنشاء البريد الإلكتروني واستكشاف *السياق الأساسي*. هنا يمكنك توفير رسالة نظام بسيطة، وتغيير التطبيق لتوفير السياق الأساسي كبداية لمطالبة المستخدم. وبعد ذلك، سيُلحق التطبيق إدخال المستخدم، واستخراج المعلومات من السياق الأساسي للرد على مطالبة المستخدم.
1. افتح الملف `grounding.txt` واقرأ بإيجاز السياق الأساسي الذي ستقوم بإدراجه.
1. في تطبيقك مباشرة بعد ***تنسيق التعليق وإرسال الطلب إلى النموذج*** وقبل أي تعليمات برمجية موجودة، أضف القصاصة البرمجية التالية لقراءة النص من `grounding.txt` لزيادة مطالبة المستخدم بالسياق الأساسي.

    **C#**: Program.cs

    ```csharp
    // Format and send the request to the model
    Console.WriteLine("\nAdding grounding context from grounding.txt");
    string groundingText = System.IO.File.ReadAllText("grounding.txt");
    userMessage = groundingText + userMessage;
    ```

    **Python**: prompt-engineering.py

    ```python
    # Format and send the request to the model
    print("\nAdding grounding context from grounding.txt")
    grounding_text = open(file="grounding.txt", encoding="utf8").read().strip()
    user_message = grounding_text + user_message
    ```

1. احفظ الملف وأعد تشغيل التطبيق.
1. أدخل المطالبات التالية (مع استمرار إدخال **رسالة النظام** وحفظها في `system.txt`).

    **رسالة النظام**

    ```prompt
    You're an AI assistant who helps people find information. You'll provide answers from the text provided in the prompt, and respond concisely.
    ```

    **رسالة المستخدم:**

    ```prompt
    What animal is the favorite of children at Contoso?
    ```

> **تلميح**: إذا كنت ترغب في رؤية الاستجابة الكاملة من Azure OpenAI، يمكنك تعيين متغيّر **printFullResponse** إلى `True`، وإعادة تشغيل التطبيق.

## تنظيف

عند الانتهاء من مورد Azure OpenAI، تذكر حذف التوزيع أو المورد بأكمله في **مدخل Microsoft Azure** في `https://portal.azure.com`.
