---
layout: post
date: 2020-05-15
title: شرح مخطط الصنف UML مع الأمثلة
description: شرح UML Class Diagram بالأمثلة التوضيحية والصور
type: tutorial
comments: true
tags: تعليم
feature: /assets/posts/uml.jpg 
caption: uml ECE3574 by john7575doe is licensed under CC BY 2.0
author: husam
---


**ما هو الصنف؟**

الصنف (بالإنجليزية class) هو مخطط يستخدم لإنشاء عنصر (object)، يُحِّدد الصنف ما يمكن أن يقوم به العنصر.

**ما هو مخطط الصنف؟**

يوفر UML CLASS DIAGRAM نظرة عامة على نظام برمجي وذلك من خلال عرض الأصناف والمتغيرات والعمليات (الدالات) وعلاقاتها، يتضمن هذا الرسم التخطيطي اسم الصنف والمتغيرات والعمليات في حجرات محددة منفصلة.

يحدد مخطط الصنف أنواع العناصر في النظام و العلاقات الموجودة بينها، كما يعطي رؤية عالية المستوى للتطبيق كما يمكن تشغيل طريقة النمذجة هذه مع الطرق كائنية التوجه تقريبًا.
يمكن أن يشير الصنف إلى صنف آخر، كما يمكن أن يكون للصنف عناصره الخاصة أو قد يرث من أصناف أخرى.

يساعد Class Diagram في بناء الكود لتطوير تطبيق برمجي ما.

* Toc
{:toc}

# فوائد مخطط الصنف

* يوضح مخطط الصنف جميع نماذج البيانات في أنظمة المعلومات حتى تلك المعقدة منها

* يوفر نظرة عامة حول كيفية هيكلة التطبيق قبل دراسة الكود الفعلي، مما يجعل وقت العمل أسهل و أقل بكثير

* يساعد على فهم أفضل للتخطيطات العامة للتطبيق

* يسمح برسم مخططات تفصيلية توضح الكود المطلوب برمجته

* مفيد للمطورين و المستخدمين.

# العناصر الأساسية لمخطط الصنف في UML

العناصر الأساسية في مخطط الصنف UML هي:

1. اسم الصنف

2. المتغيرات

3. العمليات (الدالات)

## اسم الصنف

{% include image.html width="182" height="219" src="/assets/articles/elements.png" alt="لعناصر الأساسية في مخطط الصنف" %}

اسم الصنف مطلوب فقط في التمثيل الرسومي للصنف و نلاحظ أنه موجود في الجزء العلوي لمستطيل الصنف، الصنف هو مخطط عنصر يمكن أن يشترك في نفس العلاقات والمتغيرات والعمليات والدلالات، يتم تقديم الصنف كمستطيل، بما في ذلك اسمه ومتغيراته وعملياته في حجرات متفرقة.

يجب مراعاة القواعد التالية أثناء تمثيل الصنف:

1. يجب أن يبدأ اسم الصنف دائمًا بحرف كبير.

2. يجب أن يكون اسم الصنف دائمًا في وسط الحجرة الأولى.

3. يجب كتابة اسم الصنف دائمًا **بخط عريض**.

4. يجب كتابة اسم الصنف من نوع abstract (والذي يُورِّث للأصناف الأخرى)  *بخط مائل*.

## المتغيرات

المتغير هو خاصية الصنف التي تصف العنصر الذي يتم تصميمه، و يتم وضع هذا المكون في مخطط الصنف أسفل حجرة الاسم مباشرة.

{% include image.html width="166" height="264" src="/assets/articles/student.png" alt="سمات الطالب" %}

يتم احتساب بعض المتغيرات من خلال متغيرات أخرى، على سبيل المثال يمكن حساب عمر الطالب بسهولة من تاريخ ميلاده.

{% include image.html width="166" height="264" src="/assets/articles/student2.png" alt="   سمات الطالب مع العمر" %}

**خصائص المتغيرات**

* تتم كتابة المتغيرات بشكل عام مع نوع الرؤية.

* أنواع الرؤية هي: Public و  private و protected و package ويُشار إليها بالعلامات `+` و `-` و `#` و `~` على التوالي.

* تصف الرؤية إمكانية الوصول إلى متغير الصنف.

* يجب أن يكون للمتغيرات اسم ذو معنى يصف استخدامها في الصنف.

## العلاقات

هناك ثلاثة أنواع رئيسية من العلاقات في UML:

1. التبعيات

2. التعميمات 

3. الارتباطات

### التبعيات

التبعية تعني العلاقة بين صنفين أو أكثر حيث قد يؤدي التغيير في صنف إلى فرض تغييرات في الآخر و تعتبر هذه علاقة ضعيفة حيث تشير التبعية إلى أن صنف واحد يعتمد على صنف أخر.

في المثال التالي ، يعتمد الطالب على الكلية التي يتبع لها

{% include image.html width="450" height="88" src="/assets/articles/dependency.png" alt=" التبعية" %}

### التعميمات

{% include image.html width="196" height="240" src="/assets/articles/general.png" alt=" التعميم" %}

يساعد التعميم على توصيل صنف فرعي (subclass) بصنفه الأعلى (superclass)، يستمد الصنف الفرعي بياناته (يرث) من الصنف الأعلى، لكن لا يمكن استخدام علاقة التعميم هذه لنمذجة تنفيذ الواجهة (interface implementation)، و من الجدير بالذكر أيضاً أن مخطط الصنف يسمح بإستمداد البيانات (التوريث) من عدة أصناف أعلى.

في هذا المثال، يتم تعميم الطالب في الفصل الدراسي من صنف الشخص.

### الارتباطات

يمثل هذا النوع من العلاقات علاقات ثابتة بين الفئتين "أ" و "ب". يعني مثلا موظف يعمل في منظمة.

فيما يلي بعض قواعد الارتباط:

* الاقتران هو في الغالب فعل أو جملة فعلية أو جملة إسمية أو اسم.

* يجب تسميته للإشارة إلى الدور الذي يلعبه الصنف المرفق في نهاية مسار الارتباط.

* يجب توفر خاصية التبديل في الجمع

في هذا المثال ، تظهر العلاقة بين الطالب والكلية وهي الدراسات.

{% include image.html width="164" height="209" src="/assets/articles/1.png" alt=" العلاقة بين الطالب و الكلية" %}

**التعددية**

{% include image.html width="148" height="228" src="/assets/articles/2.png" alt="التعددية" %}

التعددية هي عامل مرتبط بمتغير، يحدد عدد مثيلات المتغيرات التي يتم إنشاؤها عند بدء الصنف، إذا لم يتم تحديد التعددية فإنه بشكل افتراضي تعتبر التعددية افتراضية.

لنفترض أن هناك 100 طالب في كلية واحدة حيث يمكن أن يكون لهذه الكلية العديد من الطلاب.

**التجميع**

التجميع هو نوع خاص من الارتباط يمثل نموذجًا لعلاقة كاملة بين المجموع وأجزائه.

{% include image.html width="466" height="96" src="/assets/articles/3.png" alt="التجميع" %}

على سبيل المثال، يتكون صنف الكلية من طالب واحد أو أكثر،  لا تعتمد الأصناف المتضمنة في التجميع بشكل كامل على المحتويات حيث سنرى هناأنه سيظل صنف الكلية حتى لو لم يكن الطالب متاحًا.

**التكوين**

{% include image.html width="466" height="96" src="/assets/articles/4.png" alt="االتكوين" %}

التكوين هو نوع خاص من التجميع الذي يشير إلى ملكية قوية بين صنفين عندما يكون صنف واحد جزءًا من صنف أخر.

على سبيل المثال، إذا كانت الكلية تتكون من فصول للطلبة حيث يمكن أن تحتوي الكلية على العديد من الطلاب، بينما ينتمي كل طالب إلى كلية واحدة فقط، لذلك إذا كانت الكلية لا تعمل فقد تمت إزالة جميع الطلاب أيضًا.

# مقارنة بين التجميع و التكوين

| التجميع | التكوين |
| ----- | --------- |
| يشير التجميع إلى علاقة  يمكن أن يكون الطفل فيها موجودًا بشكل منفصل عن صنف الوالدين. مثال: السيارات (الأصل) والسيارة (الطفل)، لذا إذا قمت بحذف السيارات، فإن السيارة الفرعية لا تزال موجودة. | علاقة تركيب ثابت حيث لن يكون الطفل موجودًا بشكل مستقل عن الوالد. مثال: المنزل (الوالد) والغرفة (الطفل)، لذلك نحن نعلم أنه لن تنفصل الغرف  عن المنزل أبدًا. |

# أصناف مجردة

أي abstract class وهي أصناف ذات نموذج أولي للعمليات حيث أنها غير معدة للتنفيذ فمن الممكن أيضًا أن يكون لديك صنف مجرد بدون أي دالات معلنة بداخلها. التجريد مفيد لتحديد الوظائف عبر الأصناف، دعونا نفكر في مثال لصنف مجرد، لنفترض أنه لدينا صنف مجرد يسمى الحركة مع طريقة أو عملية معلنة بداخله،ولنسمي الطريقة المعلنة داخل الصنف المجرد ب**move ()**.

يمكن استخدام طريقة الصنف المجرد من قبل أي موضوع مثل سيارة أو حيوان أو روبوت وما إلى ذلك لتغيير الوضع الحالي كما أنه من المفيد استخدامه مع موضوع ما عندما لا يتم توفير تطبيق للدالة المحددة، حيث يمكننا استخدامه بأي شكل من الأشكال لمواضيع متعددة.

يكون للصنف المجرد في UML نفس ترميز الصنف، و الفرق الوحيد بين الصنف والصنف التجريدي هو أن اسم الصنف يكتب بخط مائل دقيق.

لا يمكن تهيئة صنف مجرد أو إنشاء مثيل له.

{% include image.html width="249" height="308" src="/assets/articles/5.png" alt="تدوين الصنف المجرد" %}

في تدوين الصنف المجرد أعلاه، هناك طريقة مجردة واحدة فقط يمكن استخدامها من قبل مواضيع متعددة الأصناف.

# مثال على مخطط الصنف في UML

إنشاء مخطط الصنف هو عملية مباشرة خالية من التعقيد حيث أنها لا تنطوي على العديد من الجوانب التقنية. وإليكم المثال التالي:

نظام الصراف الآلي نظام بسيط للغاية حيث يحتاج العملاء فيه إلى الضغط على بعض الأزرار للحصول على أموالهم لكن بنفس الوقت هناك طبقات أمان متعددة يحتاج أي نظام ATM لتمريرها مما يساعد على منع الاحتيال وتقديم المال أو التفاصيل لعملاء الخدمات المصرفية عندما يحتاجون إليها.

فيما يلي مثال على مخطط UML Class:

{% include image.html width="744" height="655" src="/assets/articles/6.png" alt="مخطط الصنف للصراف الالي" %}

# مخطط الصنف في دورة حياة تطوير البرمجيات

يمكن استخدام مخطط الصنف في مراحل تطوير البرامج المختلفة كما أنه يساعد في نمذجة الرسوم البيانية لمخططات الأصناف في ثلاث وجهات نظر مختلفة.

**1. المنظور المفاهيمي:** تصف المخططات المفاهيمية الأشياء في العالم الحقيقي حيث أنه يجب عليك رسم مخطط يمثل المفاهيم في المجال الذي هو  قيد الدراسة حاليا كما أن هذه المفاهيم تتعلق دائما بالصنف و لا علاقة لها باللغة.

**2. منظور المواصفات:** يصف منظور المواصفات ملخصات البرامج أو المكونات التي تحتوي على مواصفات و واجهات غير أنه لا يلزم القيام بإجراء معين.

**3. منظور التنفيذ:** يستخدم هذا النوع من مخطط الصنف في عمليات التنفيذ التي تعتمد على لغة أو تطبيق معين حيث أنه يستخدم منظور التنفيذ لتنفيذ البرامج.

# أفضل التطبيقات لتصميم مخطط الصنف

مخططات الأصناف هي أهم مخططات مستخدمة في UML لتطوير تطبيقات البرمجيات حيث أنه هناك العديد من الخصائص التي يجب أخذها في عين الإعتبار أثناء رسم مخطط الصنف حيث أنها تمثل جوانب مختلفة من تطبيق البرمجيات.

إليك بعض النقاط التي يجب وضعها في عين الاعتبار أثناء رسم مخطط الفصل:

* يجب أن يكون الاسم المعطى لمخطط الصنف ذا معنى علاوة على ذلك يجب أن يصف الجانب الحقيقي للنظام.

* يجب تحديد العلاقة بين كل عنصر بشكل مسبق.

* يجب تحديد المسؤولية التي يتحملها كل صنف.

* يجب تحديد الحد الأدنى من الخصائص لكل صنف لأنه يمكن أن تجعل الخصائص غير المرغوب فيها مخطط الصنف معقدًا للغاية.

* يجب تضمين ملاحظات المستخدم عندما تحتاج إلى تحديد بعض جوانب مخطط الصنف حيث أنه في نهاية الرسم، يجب أن يكون مفهوما لفريق تطوير البرمجيات.

* في النهاية يجب رسم المخطط على ورق عادي قبل إنشاء النسخة النهائية، علاوة على ذلك يجب إعادة صياغتها حتى تصبح جاهزة للتسليم النهائي.

**نصيحة:** لإنشاء مخطط UML على الحاسوب بشكل عملي فهناك العديد من تطبيقات الوب التي تعمل على المتصفح وتساعدك في ذلك مثل أداة [Creately](https://creately.com/lp/uml-diagram-tool/) المجانية، ولكنها فقط للمخططات الصغيرة المؤلفة من ثلاث أصناف تقريبًا، حيث سيصبح العمل والمتصفح بطيئًا جدًا عند اتساع المخطط. لذا وللمخططات الكبيرة يفضل استخدام تطبيق على الحاسوب وأنصحك بـ [Eclipse Papyrus](https://www.eclipse.org/papyrus/download.html) المجاني.

# النهاية والملخص

* UML هي اللغة القياسية لتحديد وتصميم وتصور عناصر أنظمة البرامج

* الصنف هو مخطط لموضوع

* يصف مخطط الصنف أنواع المواضيع الموجودة في النظام وأنواع العلاقات المختلفة الموجودة بينها

* كما يسمح مخطط الصنف بتحليل وتصميم العرض الثابت لتطبيق البرنامج

* مخططات الأصناف هي أهم المخططات الموجودة في UML و التي تستخدم لتطوير تطبيقات البرمجيات

* العناصر الأساسية في مخطط الصنف في UML هي 1) إسم الصنف  2) السمات 3) العلاقات

* يوفر مخطط الصنف نظرة عامة حول كيفية هيكلة التطبيق قبل دراسة الكود الفعلي، مما يجعل وقت العمل أسهل و أقل بكثير

* يُعد مخطط الصنف مفيدًا في تعيين لغات البرمجة الموجهة للمواضيع مثل Java و C ++ و Ruby و Python وما إلى ذلك.


هذه المقالة مترجمة وبتصرّف، [المصدر](https://www.guru99.com/uml-class-diagram.html)


