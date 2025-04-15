---
lab:
  title: استخدام Azure OpenAI SDKs في تطبيقك
  status: stale
---

# استخدام Azure OpenAI APIs في تطبيقك

باستخدام خدمة Azure OpenAI، يمكن للمطورين إنشاء روبوتات الدردشة ونماذج اللغة والتطبيقات الأخرى التي تتفوق في فهم اللغة البشرية الطبيعية. يوفر Azure OpenAI الوصول إلى نماذج الذكاء الاصطناعي المدربة مسبقاً، بالإضافة إلى مجموعة من واجهات برمجة التطبيقات والأدوات لتخصيص هذه النماذج وضبطها لتلبية المتطلبات المحددة للتطبيق الخاص بك. في هذا التمرين، ستتعلم كيفية نشر نموذج في Azure OpenAI واستخدامه في تطبيقك الخاص.

في سيناريو هذا التمرين، ستؤدي دور مطور برامج مكلف بتنفيذ تطبيق يمكنه استخدام الذكاء الاصطناعي التوليدي للمساعدة في تقديم توصيات المشي لمسافات طويلة. يمكن تطبيق التقنيات المستخدمة في التمرين على أي تطبيق يريد استخدام Azure OpenAI APIs.

سيستغرق هذا التدريب حوالي **30** دقيقة.

## توفير مورد Azure OpenAI

إذا لم يكن لديك موردًا بالفعل، يمكنك توفير مورد Azure OpenAI في اشتراك Azure الخاص بك.

1. سجّل الدخول إلى **Azure portal** من `https://portal.azure.com`.
2. إنشاء مورد **Azure OpenAI** بالإعدادات التالية:
    - **اشتراك**: *حدد اشتراك Azure الذي جرت الموافقة عليه للوصول إلى خدمة Azure OpenAI*
    - **مجموعة الموارد**: *اختيار مجموعة موارد أو إنشاءها*
    - **المنطقة**: *إجراء اختيار **عشوائي** من أي من المناطق التالية*\*
        - شرق أستراليا
        - شرق كندا
        - شرق الولايات المتحدة
        - East US 2
        - وسط فرنسا
        - شرق اليابان
        - وسط شمال الولايات المتحدة
        - منطقة السويد الوسطى
        - شمال سويسرا
        - جنوب المملكة المتحدة
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

## الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية

ستضع تطبيقك Azure OpenAI APIs باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في GitHub repo.

> **تلميح**: إذا نسخت بالفعل مستودع **mslearn-openai**، فافتحه في تعليمة Visual Studio البرمجية. وإلا فاتبع هذه الخطوات لاستنساخه إلى بيئة تطويرك.

1. ابدأ تشغيل Visual Studio Code.
2. افتح عرض لوحة الأوامر (SHIFT+CTRL+P أو **عرض لوحة الأوامر** > **Command Palette**)، ثم نفّذ أمر **Git: Clone** لاستنساخ المستودع `https://github.com/MicrosoftLearning/mslearn-openai` إلى مجلد محلي (لا يهم أي مجلد تختاره).
3. عند استنساخ المستودع، افتح المجلد في Visual Studio Code.

    > **ملاحظة**: إذا عرضت لك Visual Studio Code رسالة منبثقة لمطالبتك بالثقة في التعليمات البرمجية التي تفتحها، فانقر فوق **نعم، أثق في خيار الكُتاب** في النافذة المنبثقة.

4. انتظر حتى تثبيت ملفات إضافية لدعم مشاريع التعليمات البرمجية C# في المستودع.

    > **ملاحظة**: في حالة مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد **ليس الآن**.

## تكوين تطبيقك

تم توفير تطبيقات لكل من C# وPython. يتميز كلا التطبيقين بالوظيفة نفسها. أولاً، ستكمل بعض الأجزاء الرئيسية من التطبيق لتمكين استخدام مورد Azure OpenAI الخاص بك.

1. في تعليمة Visual Studio البرمجية في جزء **المستكشف**، انتقِل إلى المجلد **Labfiles/02-azure-openai-api** ويمكنك توسيع المجلد **CSharp** أو **Python** حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي ستدمج وظيفة Azure OpenAI فيه.
2. انقر بزر الماوس الأيمن فوق المجلد **CSharp** أو **Python** الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وافتح محطة طرفية متكاملة. ثم، عليك تثبيت حزمة Azure OpenAI SDK عن طريق تشغيل الأمر المناسب لتفضيل اللغة لديك:

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
    // Add Azure OpenAI packages
    using Azure.AI.OpenAI;
    using OpenAI.Chat;
    ```

    **Python**: test-openai-model.py

    ```python
    # Add Azure OpenAI package
    from openai import AzureOpenAI
    ```

1. في التعليمات البرمجية للتطبيق الخاص بلغتك، استبدل التعليق ***تهيئة عميل Azure OpenAI...*** بالتعليمات البرمجية التالية لتهيئة العميل وتحديد رسالة النظام الخاصة بنا.

    **C#**: Program.cs

    ```csharp
    // Initialize the Azure OpenAI client
    AzureOpenAIClient azureClient = new (new Uri(oaiEndpoint), new ApiKeyCredential(oaiKey));
    ChatClient chatClient = azureClient.GetChatClient(oaiDeploymentName);
    
    // System message to provide context to the model
    string systemMessage = "I am a hiking enthusiast named Forest who helps people discover hikes in their area. If no area is specified, I will default to near Rainier National Park. I will then provide three suggestions for nearby hikes that vary in length. I will also share an interesting fact about the local nature on the hikes when making a recommendation.";
    ```

    **Python**: test-openai-model.py

    ```python
    # Initialize the Azure OpenAI client
    client = AzureOpenAI(
            azure_endpoint = azure_oai_endpoint, 
            api_key=azure_oai_key,  
            api_version="2024-02-15-preview"
            )
    
    # Create a system message
    system_message = """I am a hiking enthusiast named Forest who helps people discover hikes in their area. 
        If no area is specified, I will default to near Rainier National Park. 
        I will then provide three suggestions for nearby hikes that vary in length. 
        I will also share an interesting fact about the local nature on the hikes when making a recommendation.
        """
    ```

1. استبدل التعليق ***إضافة تعليمة برمجية لإرسال الطلب...*** بالتعليمات البرمجية اللازمة لإنشاء الطلب؛ لتحديد المعلمات المختلفة للنموذج الخاص بك مثل `Temperature` و `MaxOutputTokenCount`.

    **C#**: Program.cs

    ```csharp
    // Add code to send request...
    // Get response from Azure OpenAI
    ChatCompletionOptions chatCompletionOptions = new ChatCompletionOptions()
    {
        Temperature = 0.7f,
        MaxOutputTokenCount = 800
    };

    ChatCompletion completion = chatClient.CompleteChat(
        [
            new SystemChatMessage(systemMessage),
            new UserChatMessage(inputText)
        ],
        chatCompletionOptions
    );

    Console.WriteLine($"{completion.Role}: {completion.Content[0].Text}");
    ```

    **Python**: test-openai-model.py

    ```python
    # Add code to send request...
    # Send request to Azure OpenAI model
    response = client.chat.completions.create(
        model=azure_oai_deployment,
        temperature=0.7,
        max_tokens=400,
        messages=[
            {"role": "system", "content": system_message},
            {"role": "user", "content": input_text}
        ]
    )
    generated_text = response.choices[0].message.content

    # Print the response
    print("Response: " + generated_text + "\n")
    ```

1. احفظ التغييرات في ملف التعليمات البرمجية خاصتك.

## اختبار التطبيق الخاص بك

الآن بعد أن نجح تكوين التطبيق الخاص بك، عليك تشغيله لإرسال طلبك إلى النموذج الخاص بك ومراقبة الاستجابة.

1. في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.

    - **C#:** `dotnet run`
    - **Python**: `python test-openai-model.py`

    > **تلميح**: يمكنك استخدام أيقونة **تكبير حجم اللوحة** (**^**) في شريط أدوات المحطة الطرفية لرؤية المزيد من نص وحدة التحكم.

1. عند المطالبة، أدخل النص `What hike should I do near Rainier?`.
1. لاحظ الإخراج، مع ملاحظة أن الاستجابة تتبع الإرشادات المقدمة في رسالة النظام التي أضفتها إلى صفيف *الرسائل*.
1. قدم المطالبة `Where should I hike near Boise? I'm looking for something of easy difficulty, between 2 to 3 miles, with moderate elevation gain.` ولاحظ الإخراج.
1. في ملف التعليمات البرمجية للغتك المفضلة، يمكنك تغيير قيمة معلمة *درجة الحرارة* في طلبك إلى **1.0** واحفظ الملف.
1. يمكنك تشغيل التطبيق مرة أخرى باستخدام المطالبات أعلاه، ولاحظ الإخراج.

غالباً ما تؤدي زيادة درجة الحرارة إلى اختلاف الاستجابة، حتى عند توفير نفس النص، بسبب زيادة العشوائية. يمكنك تشغيله عدة مرات لمعرفة كيفية تغيير الإخراج. حاول استخدام قيم مختلفة لدرجة الحرارة بالإدخال نفسه.

## حفظ محفوظات المحادثات

في معظم تطبيقات العالم الحقيقي، تسمح القدرة على الرجوع إلى الأجزاء السابقة من المحادثة بتفاعل أكثر واقعية مع عامل الذكاء الاصطناعي. واجهة برمجة تطبيقات Azure OpenAI عديمة الحالة حسب التصميم، ولكن من خلال توفير محفوظات للمحادثة في مطالبتك، يمكنك تمكين نموذج الذكاء الاصطناعي للإشارة إلى الرسائل السابقة.

1. شغل التطبيق مرة أخرى وقدم المطالبة `Where is a good hike near Boise?`.
1. لاحظ الإخراج، ثم استخدم المطالبة `How difficult is the second hike you suggested?`.
1. من المحتمل أن تشير الاستجابة من النموذج إلى عدم القدرة على فهم الرفع الذي تشير إليه. لإصلاح ذلك، يمكننا تمكين النموذج من الحصول على رسائل المحادثة السابقة للرجوع إليها.
1. في التطبيق الخاص بك، نحتاج إلى إضافة المطالبة السابقة والاستجابة إلى المطالبة المستقبلية التي نرسلها. فيما يلي تعريف **رسائل النظام**، أضف التعليمات البرمجية التالية.

    **C#**: Program.cs

    ```csharp
    // Initialize messages list
    var messagesList = new List<ChatMessage>()
    {
        new SystemChatMessage(systemMessage),
    };
    ```

    **Python**: test-openai-model.py

    ```python
    # Initialize messages array
    messages_array = [{"role": "system", "content": system_message}]
    ```

1. ضمن التعليق ***أضف تعليمة برمجية لإرسال الطلب...***، استبدل كل التعليمة البرمجية من التعليق **حتى** نهاية الحلقة يالتعليمة البرمجية التالية ثم احفظ الملف. التعليمة البرمجية هي نفسها في الغالب، ولكن الآن تستخدم صفيف الرسائل لتخزين محفوظات المحادثات.

    **C#**: Program.cs

    ```csharp
    // Add code to send request...
    // Build completion options object
    messagesList.Add(new UserChatMessage(inputText));

    ChatCompletionOptions chatCompletionOptions = new ChatCompletionOptions()
    {
        Temperature = 0.7f,
        MaxOutputTokenCount = 800
    };

    ChatCompletion completion = chatClient.CompleteChat(
        messagesList,
        chatCompletionOptions
    );

    // Return the response
    string response = completion.Content[0].Text;

    // Add generated text to messages list
    messagesList.Add(new AssistantChatMessage(response));

    Console.WriteLine("Response: " + response + "\n");
    ```

    **Python**: test-openai-model.py

    ```python
    # Add code to send request...
    # Send request to Azure OpenAI model
    messages_array.append({"role": "user", "content": input_text})

    response = client.chat.completions.create(
        model=azure_oai_deployment,
        temperature=0.7,
        max_tokens=1200,
        messages=messages_array
    )
    generated_text = response.choices[0].message.content
    # Add generated text to messages array
    messages_array.append({"role": "assistant", "content": generated_text})

    # Print generated text
    print("Summary: " + generated_text + "\n")
    ```

1. حفظ الملف. في التعليمات البرمجية التي أضفتها، لاحظ أننا الآن نلحق الإدخال والاستجابة السابقين إلى صفيف المطالبة الذي يسمح للنموذج بفهم محفوظات محادثتنا.
1. في الجزء الطرفي، أدخل الأمر التالي لتشغيل التطبيق.

    - **C#:** `dotnet run`
    - **Python**: `python test-openai-model.py`

1. شغل التطبيق مرة أخرى وقدم المطالبة `Where is a good hike near Boise?`.
1. لاحظ الإخراج، ثم استخدم المطالبة `How difficult is the second hike you suggested?`.
1. من المحتمل أن تحصل على استجابة حول الرفع الثاني الذي اقترحه النموذج، والذي يوفر محادثة أكثر واقعية. يمكنك طرح أسئلة متابعة إضافية تشير إلى الإجابات السابقة، وفي كل مرة توفر المحفوظات سياقاً للنموذج للإجابة عليه.

    > **تلميح**: تم ضبط عدد رموز الإخراج على 800 فقط، لذا إذا استمرت المحادثة لفترة طويلة، ستنفد الرموز المتاحة للتطبيق، مما يؤدي إلى مطالبة غير مكتملة. في استخدامات الإنتاج، سيساعد تقييد طول المحفوظات على أحدث المدخلات والاستجابات في التحكم في عدد الرموز المميزة المطلوبة.

## تنظيف

عند الانتهاء من مورد Azure OpenAI، تذكر حذف التوزيع أو المورد بأكمله في **مدخل Microsoft Azure** في `https://portal.azure.com`.
