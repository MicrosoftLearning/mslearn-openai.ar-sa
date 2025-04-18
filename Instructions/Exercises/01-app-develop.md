---
lab:
  title: تطوير التطبيقات باستخدام خدمة Azure OpenAI
  status: new
---

# تطوير التطبيقات باستخدام خدمة Azure OpenAI

باستخدام خدمة Azure OpenAI، يُمكن للمطورين إنشاء روبوتات دردشة وتطبيقات أخرى تتفوق في فهم اللغة البشرية الطبيعية من خلال استخدام REST APIs أو SDKs الخاصة باللغة. عند العمل مع نماذج اللغة هذه، فإن كيفية قيام المطورين بتشكيل مطالباتهم تؤثر بشكل كبير على كيفية استجابة نموذج الذكاء الاصطناعي التوليدي. يمكن لنماذج Azure OpenAI تخصيص المحتوى وتنسيقه، إذا طلب ذلك بطريقة واضحة وموجزة. في هذا التمرين، ستتعلم كيفية ربط تطبيقك بـ Azure OpenAI ورؤية كيف تساعد المطالبات المختلفة للمحتوى المماثل في تشكيل رد نموذج الذكاء الاصطناعي لتلبية متطلباتك بشكل أفضل.

في سيناريو هذا التمرين، ستؤدي دور مطور برامج يعمل على حملة تسويقية للحياة البرية. أنت تستكشف كيفية استخدام الذكاء الاصطناعي التوليدي لتحسين رسائل البريد الإلكتروني الإعلانية وتصنيف المقالات التي قد تنطبق على فريقك. يمكن تطبيق تقنيات هندسة التلقين المستخدمة في التدريب بشكل مماثل لمجموعة متنوعة من حالات الاستخدام.

سيستغرق هذا التدريب حوالي **30** دقيقة.

## استنساخ المستودع لهذه الدورة التدريبية

إذا لم تقم بالاستنساخ بالفعل، يجب عليك استنساخ مستودع التعليمات البرمجية لهذه الدورة التدريبية:

1. ابدأ تشغيل Visual Studio Code.
2. افتح عرض لوحة الأوامر (SHIFT+CTRL+P أو **عرض لوحة الأوامر** > **Command Palette**)، ثم نفّذ أمر **Git: Clone** لاستنساخ المستودع `https://github.com/MicrosoftLearning/mslearn-openai` إلى مجلد محلي (لا يهم أي مجلد تختاره).
3. عند استنساخ المستودع، افتح المجلد في تعليمة Visual Studio البرمجية.
4. انتظر حتى تثبيت ملفات إضافية لدعم مشاريع التعليمات البرمجية C# في المستودع.

    > **ملاحظة**: إذا جرت مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد **ليس الآن**.

## توفير مورد Azure OpenAI

إذا لم يكن لديك موردًا بالفعل، يمكنك توفير مورد Azure OpenAI في اشتراك Azure الخاص بك.

1. سجّل الدخول إلى **Azure portal** من `https://portal.azure.com`.

1. إنشاء مورد **Azure OpenAI** بالإعدادات التالية:
    - **اشتراك**: *حدد اشتراك Azure الذي جرت الموافقة عليه للوصول إلى خدمة Azure OpenAI*
    - **مجموعة الموارد**: *اختيار مجموعة موارد أو إنشاءها*
    - **المنطقة**: *إجراء اختيار **عشوائي** من أي من المناطق التالية*\*
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

1. يُرجى الانتظار لاكتمال التوزيع. ثم انتقل إلى مورد Azure OpenAI الموزّع في مدخل Microsoft Azure.

## توزيع النموذج

بعد ذلك، ستقوم بنشر مورد نموذج Azure OpenAI من CLI. راجع هذا المثال واستبدل المتغيرات التالية بالقيم الخاصة بك من الأعلى:

```dotnetcli
az cognitiveservices account deployment create \
   -g <your_resource_group> \
   -n <your_OpenAI_service> \
   --deployment-name gpt-4o \
   --model-name gpt-4o \
   --model-version 2024-05-13 \
   --model-format OpenAI \
   --sku-name "Standard" \
   --sku-capacity 5
```

> **ملاحظة**: يتم قياس سعة Sku بالآلاف من الرموز المميزة في الدقيقة. حد المعدل البالغ 5,000 رمز في الدقيقة يُعد كافيًا تمامًا لإكمال هذا التمرين، مع ترك سعة متاحة لمستخدمين آخرين ضمن نفس الاشتراك.

## تكوين تطبيقك

تم توفير تطبيقات لكل من C# وPython، ويمتلك كلا التطبيقين نفس الوظيفة. أولاً، ستكمل بعض الأجزاء الرئيسية من التطبيق لتمكين استخدام مورد Azure OpenAI الخاص بك مع استدعاءات واجهة برمجة التطبيقات (API) غير المتزامنة.

1. في Visual Studio Code، في جزء **المستكشف**، انتقل إلى المجلد **Labfiles/01-app-develop** ووسّع نطاق المجلد **CSharp** أو **Python** وفقًا لتفضيلات اللغة الخاصة بك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي تريد دمج وظيفة Azure OpenAI فيه.
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
    - **اسم عملية النشر** الذي حددته لنشر نموذجك.
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

    **Python**: application.py

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

    **Python**: application.py

    ```python
    # Configure the Azure OpenAI client
    client = AsyncAzureOpenAI(
        azure_endpoint = azure_oai_endpoint, 
        api_key=azure_oai_key,  
        api_version="2024-02-15-preview"
    )
    ```

3. في الوظيفة التي تستدعي نموذج Azure OpenAI، ضمن التعليق ***الحصول على رد من Azure OpenAI***، أضف التعليمة البرمجية للتنسيق وأرسل الطلب إلى النموذج.

    **C#**: Program.cs

    ```csharp
    // Get response from Azure OpenAI
    ChatCompletionOptions chatCompletionOptions = new ChatCompletionOptions()
    {
        Temperature = 0.7f,
        MaxOutputTokenCount = 800
    };

    ChatCompletion completion = chatClient.CompleteChat(
        [
            new SystemChatMessage(systemMessage),
            new UserChatMessage(userMessage)
        ],
        chatCompletionOptions
    );

    Console.WriteLine($"{completion.Role}: {completion.Content[0].Text}");
    ```

    **Python**: application.py

    ```python
    # Get response from Azure OpenAI
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
    - **Python**: `python application.py`

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
    \n Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits.
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
    \n Include a list of the current animals we have at our rescue after the signature, in the form of a table. These animals include elephants, zebras, gorillas, lizards, and jackrabbits.
    ```

1. مراقبة المخرجات. وفي هذه المرة، من المحتمل أن ترى البريد الإلكتروني بتنسيق مماثل، ولكن بنبرة غير رسمية أكثر بكثير. من المحتمل أن ترى النكات مضمنة!

## استخدم السياق الأساسي واحتفظ بسجل المحادثة.

1. في التكرار الأخير، ننتقل بعيدًا عن توليد البريد الإلكتروني ونستكشف *السياق الأساسي* والحفاظ على سجل المحادثة. هنا يمكنك توفير رسالة نظام بسيطة، وتغيير التطبيق لتوفير السياق الأساسي كبداية لمطالبة المستخدم. وبعد ذلك، سيُلحق التطبيق إدخال المستخدم، واستخراج المعلومات من السياق الأساسي للرد على مطالبة المستخدم.
1. افتح الملف `grounding.txt` واقرأ بإيجاز السياق الأساسي الذي ستقوم بإدراجه.
1. في تطبيقك مباشرة بعد ***تنسيق التعليق وإرسال الطلب إلى النموذج*** وقبل أي تعليمات برمجية موجودة، أضف القصاصة البرمجية التالية لقراءة النص من `grounding.txt` لزيادة مطالبة المستخدم بالسياق الأساسي.

    **C#**: Program.cs

    ```csharp
    // Initialize messages list
    Console.WriteLine("\nAdding grounding context from grounding.txt");
    string groundingText = System.IO.File.ReadAllText("grounding.txt");
    var messagesList = new List<ChatMessage>()
    {
        new UserChatMessage(groundingText),
    };
    ```

    **Python**: application.py

    ```python
    # Initialize messages array
    print("\nAdding grounding context from grounding.txt")
    grounding_text = open(file="grounding.txt", encoding="utf8").read().strip()
    messages_array = [{"role": "user", "content": grounding_text}]
    ```

1. ضمن التعليق ***أضف تعليمة برمجية لإرسال الطلب...***، استبدل كل التعليمة البرمجية من التعليق **حتى** نهاية الحلقة يالتعليمة البرمجية التالية ثم احفظ الملف. التعليمة البرمجية هي نفسها في الغالب، ولكن الآن تستخدم صفيف الرسائل لإرسال الطلب إلى النموذج.

    **C#**: Program.cs
   
    ```csharp
    // Format and send the request to the model
    messagesList.Add(new SystemChatMessage(systemMessage));
    messagesList.Add(new UserChatMessage(userMessage));
    GetResponseFromOpenAI(messagesList);
    ```

    **Python**: application.py

    ```python
    # Format and send the request to the model
    messages_array.append({"role": "system", "content": system_text})
    messages_array.append({"role": "user", "content": user_text})
    await call_openai_model(messages=messages_array, 
        model=azure_oai_deployment, 
        client=client
    )
    ```

1. ضمن التعليق ***تعريف الدالة التي ستجلب الاستجابة من نقطة نهاية Azure OpenAI***، استبدل تعريف الدالة بالتعليمة البرمجية التالية لاستخدام قائمة سجل المحادثة عند استدعاء الدالة `GetResponseFromOpenAI` للغة C# أو `call_openai_model` للغة Python.

    **C#**: Program.cs
   
    ```csharp
    // Define the function that gets the response from Azure OpenAI endpoint
    private static void GetResponseFromOpenAI(List<ChatMessage> messagesList)
    ```

    **Python**: application.py

    ```python
    # Define the function that will get the response from Azure OpenAI endpoint
    async def call_openai_model(messages, model, client):
    ```
    
1. وأخيرا، استبدل جميع التعليمات البرمجية ضمن ***الحصول على استجابة من Azure OpenAI***. التعليمة البرمجية هي نفسها في الغالب، ولكن الآن تستخدم صفيف الرسائل لتخزين محفوظات المحادثات.

    **C#**: Program.cs
   
    ```csharp
    // Get response from Azure OpenAI
    ChatCompletionOptions chatCompletionOptions = new ChatCompletionOptions()
    {
        Temperature = 0.7f,
        MaxOutputTokenCount = 800
    };

    ChatCompletion completion = chatClient.CompleteChat(
        messagesList,
        chatCompletionOptions
    );

    Console.WriteLine($"{completion.Role}: {completion.Content[0].Text}");
    messagesList.Add(new AssistantChatMessage(completion.Content[0].Text));
    ```

    **Python**: application.py

    ```python
    # Get response from Azure OpenAI
    print("\nSending request to Azure OpenAI model...\n")

    # Call the Azure OpenAI model
    response = await client.chat.completions.create(
        model=model,
        messages=messages,
        temperature=0.7,
        max_tokens=800
    )   

    print("Response:\n" + response.choices[0].message.content + "\n")
    messages.append({"role": "assistant", "content": response.choices[0].message.content})
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

   لاحظ أن النموذج يستخدم معلومات النص المرجعي للإجابة على سؤالك.

1. دون تغيير رسالة النظام، أدخل المطالبة التالية كرسالة من المستخدم:

    **رسالة المستخدم:**

    ```prompt
    How can they interact with it at Contoso?
    ```

    لاحظ أن النموذج يتعرف على "هم" على أنهم الأطفال، و"هو" على أنه الحيوان المفضل لديهم، وذلك لأنه يمتلك الآن إمكانية الوصول إلى سؤالك السابق ضمن سجل المحادثة.
   
## تنظيف

عند الانتهاء من مورد Azure OpenAI، تذكر حذف التوزيع أو المورد بأكمله في **مدخل Microsoft Azure** في `https://portal.azure.com`.
