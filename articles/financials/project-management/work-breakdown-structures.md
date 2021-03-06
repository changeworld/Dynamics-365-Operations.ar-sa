---
title: "هياكل تنظيم العمل"
description: "إن هيكل تنظيم العمل (WBS) عبارة عن وصف للعمل الذي سيتم إنجازه لمشروع. إنها تدرج هرمي للمهام التي تمثل فهم فريق المشروع لتكوين العمل، وحجم، وتكلفة، ومدة كل مكون أو مهمة."
author: KimANelson
manager: AnnBe
ms.date: 06/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8bc3d23fac6112622e722e57b61fdb686f5a98ed
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="work-breakdown-structures"></a>هياكل تنظيم العمل

[!include [banner](../includes/banner.md)]

إن هيكل تنظيم العمل (WBS) عبارة عن وصف للعمل الذي سيتم إنجازه لمشروع. إنها تدرج هرمي للمهام التي تمثل فهم فريق المشروع لتكوين العمل، وحجم، وتكلفة، ومدة كل مكون أو مهمة. تشتمل WBS على ثلاثة أغراض رئيسية:

-   وصف تنظيم أو تأليف العمل في مهام.
-   جدولة عمل المشروع.
-   تقدير تكلفة كل مهمة.

تعتمد درجة التفصيل في WBS على مستوى الدقة المطلوبة في التقديرات ومستوى التعقب المطلوب مقابل تلك التقديرات. وغالبًا ما تتطلب المشاريع التي تشتمل على تفاوت منخفضة جداً للتعثرات في جدول أو تكلفة  WBS أكثر تفصيلاً وتعقب بعناية لتقدم العمل والتكلفة في مقابل WBS. وهذا النوع من المشاريع شائع في صناعات الهندسة والبناء. 

وفي المقابل، تميل إلى أن تكون المشاريع في صناعات مثل الوسائط والإعلانات والبرامج والبنية التحتية لتكنولوجيا المعلومات من نوع واحد، وتتناسب الإنتاجية مع خبرة واختصاص الشخص الذي يقوم بتنفيذ المهمة. ولذلك، تستخدم هذه الصناعات WBS للحصول على تقريب حجم المشروع، وعدم تتبع التقدم المحرز في هذا المشروع بالتفصيل. 

وإنشاء هيكل تنظيم العمل عبارة عن عملية مكثفة وعادةً ما تتم لفترة طويلة، وتتطلب التعاون والمعلومات الواردة من مجموعة متنوعة من الأشخاص. يصف هذا الموضوع كيفية استخدام تحسينات WBS في Microsoft Dynamics 365 for Finance and Operations لتلبية متطلبات التعقب والتقديرات.

## <a name="prerequisites-for-creating-a-wbs"></a>المتطلبات الأساسية لإنشاء WBS
لإنشاء WBS، يجب أن تكون قادراً على إنشاء جدول عمل وتقدير تكلفة العمل.

### <a name="prerequisites-for-creating-a-work-schedule"></a>المتطلبات الأساسية لإنشاء جدول العمل

لاستخدام إمكانيات الجدولة الكاملة لميزات WBS، أكمل الإعداد التالي:

1.  قم بإعداد تقويم مشروع وتقويم افتراضي:
    1.  انقر فوق **إدارة المشاريع‬ والمحاسبة** &gt; **الإعدادات** &gt; **محددات إدارة المشاريع‬ والمحاسبة** &gt; **الجدولة**. في حقل **تقويم العمل الافتراضي** ، حدد تقويمًا افتراضيًا. سيكون هذا تقويم العمل الافتراضي لأي مشروع جديد يتم إنشاؤه.
    2.  يمكنك تغيير التقويم الافتراضي لمشروع محدد. انقر فوق صفحة تفاصيل المشروع، ثم، في لعامة التبويب السريعة **جدولة وفريق المشروع**، قم بتحديث حقل **تقويم الجدولة** بتحديد تقويم آخر.

2.  إعداد أيام العمل وساعات العمل القياسية. سيتم استخدام التقويم الذي تقوم بتعيينه كتقويم عمل للمشروع في هيكل تنظيم العمل لتحديد المعلومات التالية:

-   أيام العمل وأيام العطل
-   عدد ساعات العمل في اليوم

لإعداد أيام العمل وساعات العمل لوضع جدول زمني، أو لإنشاء تقويم جديد، انقر فوق **إدارة المؤسسة** &gt; **عام** &gt; **‎تقويمات**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>المتطلبات المسبقة لتقدير تكلفة العمل

لاستخدام إمكانيات التكلفة الكاملة في هيكل تنظيم العمل، يجب عليك إعداد التكاليف وأسعار المبيعات للعاملين، وفئات العمالة، والرسوم، والمصروفات، والأصناف.

-   لإعداد التكلفة وسعر المبيعات الخاص بالعمالة والمصروفات وفئات الرسوم، انقر فوق **محاسبة وإدارة المشروع** &gt; **‎الإعداد** &gt; **الأسعار**.
-   لإعداد التكلفة وسعر المبيعات للأصناف، استخدم صفحة **الاتفاقيات التجارية** لكل صنف في صفحة قوائم **المنتجات التي تم إصدارها** في إدارة معلومات المنتج.

## <a name="creating-a-wbs"></a>إنشاء WBS
يشمل إنشاء هيكل تنظيم العمل ثلاثة أنشطة:

1.  **تجزئة العمل** – إنشاء تقسيم الأعمال إلى أجزاء أو مهام يمكن إدارتها.
2.  **جدول العمل** – تقدير الوقت المطلوب لإكمال مهمة وتعيين التبعيات الداخلية للمهام وتحديد تواريخ البدء والانتهاء للمهام.
3.  **تقدير التكلفة** -تقدير التكاليف لكل مهمة.

تناقش المقاطع التالية مدى المساعدة التي تقدمها قدرات WBS لكل نشاط من هذه الأنشطة.

### <a name="work-decomposition"></a>تجزئة العمل

إنشاء تقسيم أو تجزئة العمل عادةً ما تكون الخطوة الأولى في عملية إنشاء WBS. وتدعم وظيفة WBS البنيات الأساسية التالية لتقسيم وتجزئة العمل. 

**المهمة الجذر للمشروع** المهمة الجذر للمشروع هي المهمة الموجزة على المستوى الأعلى لمشروع. يتم إنشاء كافة مهام المشروع ضمنها. ويتم تعيين اسم المهمة الجذر دائماً إلى اسم المشروع. ويلخص جهد وتواريخ ومدة العقدة الجذر قيم المهام ضمن المهمة الجذر. لا يمكنك تعديل خصائص عقدة الجذر أو حذفها.

**مهام الحاوية أو الملخص** مهمة الموجزة هي مهمة تشتمل على مهام فرعية أو المهام مكونة ضمنها. ولا تتضمن المهمة الموجزة أي جهود عمل أو تكلفة خاصة به. وبدلاً من ذلك، جهود العمل وتكلفة المهمة الموجزة هي مجموع جهود العمل وتكاليف المهام المكونة لها. ويتم استخدام أقرب تاريخ بدء للمهام المكونة كتاريخ بدء للمهمة الموجزة، ويُستخدم أحدث تاريخ انتهاء للمهام المكونة كتاريخ انتهاء. ويمكنك تعديل اسم المهمة الموجزة، ولكن لا يمكنك تعديل خصائص الجدولة للجهد والتواريخ والمدة. وإذا قمت بحذف مهمة موجزة، يمكنك أيضًا حذف كافة المهام المكونة لها. 

**مهام العقدة الطرفية** تمثل مهمة العقدة الطرفية حزمة العمل الأكثر تفصيلاً في المشروع. وتشتمل العقدة الطرفية على الحهد المقدر، وعدد الموارد المخطط، وتاريخ البدء والانتهاء المخطط، والمدة. 

ويمكنك إكمال عمليات التدرج الهرمي التالية لتمكين إنشاء تدرج هرمي العمل أو تجزئة المشروع. 

**المهمة الجديدة** يتم تلقائياً إضافة أي مهمة جديدة تقوم بإنشائها ضمن العقدة الجذر، ويتم تلقائياً تعيين رقم WBS للمهمة. ويمثل رقم WBS مستوى المهمة في التدرج الهرمي. وبالنسبة للمهام في المستوى الأول ضمن المهمة الجذر للمشروع، يتم استخدام نظام ترقيم 1، و2، و3، وهكذا. وبالنسبة للمهام ضمن المستوى الأول، يتم استخدام نظام الترقيم 1.1، و1.2، و1.3، وهكذا. وبالنسبة لكل مستوى يُضاف ضمن مستوى سابق، تتم إضافة سلسلة منقطة من الأرقام. 

وحاليًا، لا يمكنك تخصيص ترقيم WBS. 

**تقليل مستوى المهمة** عند تقليل مستوى مهمة، تصبح تابعة للمهمة التي تسبقها. ويتم حساب رقم WBS للمهمة الجديدة التابعة تلقائياً بناءً على رقم WBS للأصل الجديد. والمهمة الأصلية هي الآن مهمة ملخص أو حاوية، ولذلك تصبح ملخصاً للمهام المكونة لها. 

> [!NOTE] 
> عند قيامك بتقليل مستوى المهام ضمن مهمة كانت عقدة طرفية قبل عملية المسافة البادئة، تفقد المهمة الموجزة التي تم إنشاؤها حديثا التواريخ والجهد وعدد الموارد الخاصة بها. وتستخدم الآن ملخصاً للقيم المهام المكونة الجديدة. 

**تحريك المهمة إلى مستوى أعلى** عند تحريك مهمة إلى مستوى أعلى، لا تُعد مهمة مكونة في الأصل الخاص بها. وتتم إعادة حساب رقم WBS هذه المهمة تلقائياً ليعكس المستوى الجديد للمهمة في التسلسل الهرمي. وتتم إعادة حساب الجهد، والتكلفة، والتواريخ لمهمة الأصل السابقة للمهمة لاستبعاد تلك المهمة. 

**تحريك لأعلى وتحريك لأسفل** عند النقر فوق **تحريك لأعلى** و**تحريك لأسفل**، يمكنك تغيير موضع المهمة ضمن التسلسل الهرمي للأصل الخاص بها. لا يؤثر موضع مهمة على جهد أو تكلفة أو تواريخ أو مدة المهمة. ومع ذلك، تتم إعادة حساب رقم WBS للمهمة تلقائياً ليعكس الموضع الجديد للمهمة.

### <a name="schedule-estimation"></a>تقدير الجدولة

تقدير الجدولة هو عادةً الخطوة الثانية في إنشاء هيكل تنظيم العمل. وكممارسة مثلى، يجب إكمال تقدير الجدولة بعد إنشاء المهام. تشتمل صفحة **هيكل تنظيم العمل** في Finance and Operations على قسمين. ويتم استخدام الجزء العلوي بغرض تقدير الجدولة، ويتضمن الجزء السفلي علامة التبويب **التكاليف والإيرادات المقدرة** التي يمكن استخدامها لتقدير التكلفة. 
**تبعيات المهام** في WBS، يمكنك إنشاء علاقة سابقة بين المهام. وعند تعيين المهام السابقة لمهمة، لا يمكن بدء تلك المهمة إلا بعد إكمال كافة المهام السابقة الخاصة به. ويتم تلقائياً تعيين تاريخ البدء المخطط للمهمة لآخر تاريخ لكافة المهام السابقة. 

**مهام الجدولة في Microsoft Dynamics 365 for Finance and Operations** تحدد العوامل التالية جدولة مهام العقدة الطرفية:

-   العناصر السابقة
-   الجهد
-   عدد الموارد
-   تاريخا البدء والانتهاء

يتم تعيين تاريخ البدء لمهمة العقدة الطرفية التي لا تشتمل على مهام سابقة تلقائياً إلى تاريخ بدء جدولة المشروع. ويتم حساب مدة مهمة العقدة الطرفية دائماً بعدد أيام العمل بين تاريخي البدء والانتهاء الخاصين بها. 

*<strong><em>قواعد الجدولة</em></strong>* عندما يتم تشغيل مساعدة الجدولة التلقائية، يتم تطبيق القواعد التالية على جدولة المهام لمهام العقدة الطرفية:

-   يجب أن تكون تواريخ البدء والانتهاء لمهمة أيام عمل، وفقًا لتقويم جدولة المشروع.
-   ويتم تلقائياً تعيين تاريخ بدء مهمة تشتمل على مهام سابق لها إلى آخر تاريخ نهاية لكافة المهام السابقة لها.
-   يتم حساب جهد المهمة تلقائياً كما يلي:

عدد الأشخاص × المدة × عدد الساعات في يوم عمل قياسي في تقويم المشروع. 

في بعض الحالات، قد تحتاج إلى الخروج عن هذه القواعد. ويمكنك إيقاف الجدولة التلقائية لمنع Finance and Operations من تعيين أو تصحيح أية خصائص لمهام العقدة الطرفية تلقائيًا. وعند إدخال معلومات لمهمة تؤدي إلى مخالفة لأيٍّ من قواعد الجدولة، يتم عرض رمز خطأ جدولة للمهمة. وإذا كنت لا تريد جدولة الأخطاء لعرضها، فانقر فوق **يتم عرض أخطاء الجدولة** لإيقاف تشغيل الميزة. 

> [!NOTE] 
> يستمر حساب القيم الخاصة بمهمة ملخص أو حاوية باعتبارها مجموع قيم المهام المكونة، بغض النظر عن تشغيل مساعدة الجدولة التلقائية أو إيقاف تشغيلها. 

**إصلاح أخطاء الجدولة** عند تشغيل مساعدة الجدولة التلقائية، من غير المحتمل أن تحدث أخطاء جدولة. ومع ذلك، إذا قمت بإيقاف تشغيل مساعدة الجدولة التلقائية وقم بتشغيلها مرة أخرى في وقت لاحق، قد تظهر رموز خطأ في هيكل تنظيم العمل. 

**إصلاح أخطاء الجدولة حسب المهمة** عند النقر المزدوج فوق رمز خطأ جدولة لمهمة معينة، يعرض مربع حوار كافة أخطاء الجدولة لهذه المهمة. يمكنك أن تقرر أخطاء الجدولة لإصلاحها للمهمة. 

**إصلاح كافة أخطاء الجدولة** إذا أردت من Finance and Operations إصلاح كافة أخطاء الجدولة في هيكل تنظيم العمل، في "جزء الإجراءات"، انقر فوق **إصلاح كافة تعارضات الجدولة**. 

> [!NOTE] 
> يمكن أن تسبب هذه الميزة تعديلات كبيرة على هيكل تنظيم العمل. يتم تصحيح الأخطاء بالترتيب التالي:

1.  يتم تعديل الجهد المقدر في كافة المهام حيث إنها تساوي القدرة المحددة في تقويم المشروع.
2.  ويتم تعديل تاريخ بدء كل مهمة بحيث تبدأ المهمة بعد اكتمال حميع المهام السابقة لها.
3.  تم تعديل تاريخ بدء كل مهمة لإزالة الثغرات في تواريخ بدء المهام السابقة.

### <a name="cost-estimation"></a>تقدير التكلفة

كما ذُكر سابقًا في هذا المستند، يمكنك إدخال تقدير التكلفة لكل مهمة عقدة طرفية باستخدام علامة التبويب **التكاليف والإيرادات المقدرة** في الجزء السفلي من صفحة **هيكل تنظيم العمل**. 

> [!NOTE] 
> لا يمكنك تعديل تقدير التكلفة لمهمة ملخص أو حاوية. يساوي تقدير التكلفة لكل مهمة ملخص مجموع تقدير التكلفة لمهام العقدة الطرفية الخاصة بها. يتم حساب التكلفة الإجمالية المقدرة لكل مهمة كمجموع مبالغ التكلفة المقدرة لأنواع الحركات التالية:

-   عمالة
-   الصنف أو المادة
-   المصروفات

يتم استخدام نوع حركة **الرسوم** لتقدير الدخل القائم على الرسوم. ولا ينطوي نوع الحركة هذا على مكون تكلفة، وبالتالي لا تتم مراعاة ذلك عند تقدير التكاليف. 

ويتم استخدام نوع الحركة **على الحساب** لتسجيل قيمة المبيعات المتعاقد عليه في نوع القيمة الثابتة للمشروع. ولا تتم مراعاة هذا النوع من الحركة أيضًا عندما يتم تقدير التكاليف. 

وعندما تقوم بتقدير التكاليف للمواد والعمالة والمصروفات لكل مهمة، يجب أن تقوم بتعيين فئة مشروع للتكلفة المقدرة. 

**تكاليف العمالة المقدرة** بالنسبة لكل مهمة عقدة طرفية، تقوم بتعيين جهد عمل بالساعات وفئة افتراضية. ولذلك، عند إعداد جدولة لمهمة، يُضاف تقدير تكلفة العمالة لهذه المهمة تلقائياً في الفئة الافتراضية للعمالة. ويتم عرض تقدير التكلفة هذا في علامة التبويب **التكاليف والإيرادات المقدرة** في شبكة **تفاصيل البند** لهذه المهمة. إذا احتجت إلى المزيد من تقديرات تكلفة العمالة، فيمكنك إضافتها على علامة التبويب هذه. إذا قمت بزيادة أو إنقاص الساعات على تقدير تكلفة العمالة، فسيُعاد حساب الجدولة للمهمة بشكل تلقائي. 

**تقدير تكاليف المواد والمصروفات** كما تتيح علامة التبويب **التكاليف والإيرادات المقدرة** لك إمكانية تقدير تكاليف المواد والمصروفات لمهمة، إذا كنت تحتاج إلى تقديرات. 

وتعتمد التكلفة وسعر المبيعات لكل بند تقرير المصروفات والعمالية الإعداد المحدد لكل فئة في جداول التسعير في **محاسبة وإدارة المشروع** &gt; **‎الإعداد** &gt; **التسعير**. وبالنسبة للأصناف، تتم إضافة التكلفة وسعر المبيعات افتراضيًا من اتفاقيات التجارة أو الصنف في صفحة قائمة **المنتجات الصادرة** في إدارة معلومات المنتج.

## <a name="tracking-progress-on-the-wbs"></a>تتبع التقدم المحرز في هيكل تنظيم العمل
تتعقب بعض الصناعات تقدم المشروع مقابل WBS في مستوى مرغوب جداً، بينما تتعقب الصناعات الأخرى التقدم المحرز على مستوى أعلى لهيكل تنظيم العمل. يصف هذا القسم كيفية استخدام تعقب WBS لمتطلبات المشروع. 

يحتوي Finance and Operations على ثلاث طرق عرض لهيكل تنظيم العمل لمشروع: عرض التخطيط، وعرض تعقب الجهد، وعرض تعقب التكلفة.

### <a name="planning-view"></a>عرض التخطيط

تعرض طريقة عرض التخطيط التقدير الأساسي أو المخطط لمعلومات التكاليف والجدول. وعلى الرغم من عدم وجود أي ميزات لتعقب الإصدار وخط الأساس لهيكل تنظم عمل مشروع، فإنه يتم استخدام القيم الموجودة في طريقة العرض هذه لعرض الإصدار الأساسي. ويصف قسما تقدير الجدولة وتقدير التكاليف في هذا الموضوع طريقة العرض هذه وكيفية استخدامها لإنشاء هيكل تنظيم العمل.

### <a name="effort-tracking-view"></a>طريقة عرض تعقب الجهد

تعرض طريقة عرض تعقب الجهد تقدم المهام في هيكل تنظيم العمل. وتقارن ساعات الجهد التراكمية الفعلية لمهمة بساعات الجهد المخططة. توفر المعادلات التالية القيم في طريقة عرض تعقب الجهد:

-   النسبة المئوية للتقدم = الجهد الفعلي حتى الآن ÷ الجهد المخطط للمهمة
-   الجهد المتبقي (يُعرف أيضًا بالتقدير حتى الاكتمال \[ETC\]) = الجهد المخطط – الجهد الفعلي حتى تاريخه
-   التقدير عند الاكتمال (EAC) = الجهد المتبقي + الجهد الفعلي حتى الآن
-   فرق الجهد المتوقع‬ = الجهد المخطط – EAC

تعرض طريقة عرض تعقب الجهد فرق الجهد للمهمة، استناداً إلى ما إذا كان التقدير عند الاكتمال أكثر أو أقل من الجهد المخطط:

-   إذا كان التقدير حتى الاكتمال أكثر من الجهد المخطط، يُتوقع من المهمة استغراق وقت أطول مما هو مخطط له أصلاً وتكون متأخرة عن موعدها.
-   إذا كان التقدير حتى الاكتمال أقل من الجهد المخطط، يُتوقع من المهمة استغراق وقت أقل مما هو مخطط له أصلاً وتكون متقدمة عن موعدها.

**إعادة توقع جهد مدير المشروع** في بعض الأحيان، سيلزم مدير المشروع أو شخص آخر يقوم بتعقب تقدم المشروع مراجعة التقديرات الأصلية في مهمة. وقد تتحرك المهمة بشكل أسرع أو أبطأ مما كان متوقعًا لأسباب مختلفة. على سبيل المثال، تم تقليص النطاق أو أن العاملين لديهم خبرة أقل مما كان مخططًا له أصلاً. والتوقعات هي إدراك مدير المشروع للتقديرات، استناداً إلى الحالة الحالية لمشروع. وبشكل عام، يجب عليك عدم تغيير الأرقام الأساسية، لأن أساس المشروع يقدم وثيقة منشورة جيدًا لتقدير التكلفة والجدولة لمشروع يج على جميع أصحاب المصلحة في المشروع الموافقة عليها. 

هناك طريقتان يستطيع بها مديرا المشاريع تعديل الجهد في المهام:

-   تعديل الجهد المتبقي الذي تم تعيينه لتحديث الجهد المتبقي الفعلي في المهمة تلقائيًا.
-   تعديل النسبة المئوية للتقدم الذي يتم تعيينه تلقائيًا لتحديث التقدم الحقيقي في المهمة.

يؤدي كلا النهجين إلى إعادة حساب التقدير حتى الاكتمال والتقدير عند الاكتمال للمهمة، والنسبة المئوية للتقدم، وفرق جهد المتوقع في المهمة. كما تتم إعادة حساب التقدير حتى الاكتمال والتقدير عند الاكتمال والنسبة المئوية للتقدم في مهام الملخص، ويتم تحديث فرق الجهد المتوقع الخاصة بها. 

**تعديل الجهد في مهام الملخص** يمكنك تعديل الجهد في مهام الملخص أو الحاوية. بغض النظر عن ما إذا كنت تقوم بتعديل هذه القيم باستخدام الجهد المتبقي أو النسبة المئوية للتقدم في مهام الملخص، وتحدث العمليات الحسابية تلقائياً في الترتيب التالي:

1.  يتم حساب التقدير حتى الاكتمال والتقدير عند الاكتمال والنسبة المئوية للتقدم في المهمة.
2.  يتم توزيع التقدير عند الاكتمال على المهام التابعة بنفس نسبة مبلغ التقدير عند الاكتمال الأصلي.
3.  يتم حساب التقدير عند الاكتمال الجديد في كل مهمة عقدة طرفية جديدة.
4.  تتم إعادة حساب الجهد المتبقي والنسبة المئوية للتقدم لكافة المهام التابعة المتأثرة، استناداً قيمة التقدير عند الاكتمال الجديدة. كما تتم إعادة حساب فرق الجهد للمهام.
5.  كما تتم إعادة حساب التقدير عند الاكتمال لمهام الملخص من العقد الطرفية.

انقر فوق **توسيع إلى مستوى** في طريقة عرض تعقب الجهد لتعيين المستوى الذي يجب فيه تعقب والاحتفاظ بهيكل تنظيم العمل الخاص بك. يتم توسيع هيكل تنظيم العمل تلقائياً إلى هذا المستوى في طريقة عرض تعقب الجهد عندما تقوم بفتحها.

### <a name="cost-tracking-view"></a>طريقة عرض تعقب التكلفة

تعرض طريقة عرض تعقب التكلفة تعقب استهلاك التكلفة لإحدى مهام. وفي طريقة العرض هذه، تتم مقارنة التكلفة الفعلية التي أُنفقت مقابل مهمة حتى تاريخه بالتكلفة المخططة للمهمة. توفر المعادلات التالية القيم في طريقة عرض تعقب التكلفة:

-   النسبة المئوية للتكلفة المستهلكة = التكلفة الفعلية حتى تاريخه ÷ التكلفة المخططة للمهمة
-   تكلفة الإكمال‬ (CTC) = التكلفة المخططة - التكلفة الفعلية حتى تاريخه
-   التقدير عند الاكتمال (EAC) = تكلفة الإكمال + التكلفة الفعلية حتى تاريخه
-   فرق التكلفة المتوقع = التكلفة المخططة – التقدير عند الاكتمال

تعرض طريقة عرض تعقب التكلفة فرق الجهد للمهمة، استناداً إلى ما إذا كان التقدير عند الاكتمال أكثر أو أقل من التكلفة المخططة:

-   إذا كان التقدير عند الاكتمال أكثر من التكلفة المخططة، يُتوقع من المهمة استخدام أموال أكثر مما هو مخطط له أصلاً وتكون زائدة عن الموازنة.
-   إذا كان التقدير عند الاكتمال أقل من التكلفة المخططة، يُتوقع من المهمة استخدام أموال أقل مما هو مخطط له أصلاً وتكون ناقصة عن الموازنة.

**إعادة توقع التكلفة لمدير المشروع** يجب على مديري المشاريع استخدام تكلفة الإكمال لتنقيح تقدير التكلفة الأصلية في مهمة. يمكن لمدير المشروع تعديل قيمة تكلفة الإكمال إلى التكلفة المطلوبة لإكمال المهمة. وإذا قمت بتعديل قيمة تكلفة الإكمال، فإنه تتم إعادة حساب تكلفة الإكمال والتقدير عند الاكتمال للمهمة والنسبة المئوية للتكلفة المستهلكة وفرق التكلفة المتوقع في مهمة. كما تتم إعادة حساب التقدير حتى الاكتمال والتقدير عند الاكتمال والنسبة المئوية للتكلفة المستهلكة في مهام الملخص، ويتم تحديث فرق التكلفة المتوقع الخاصة بها. 

> [!NOTE] 
> عندما تراجع جهدًا لمهمة هيكل تنظيم العمل في طريقة عرض تعقب الجهد، تتم إعادة حساب كل من تكلفة الإكمال والتقدير عند الاكتمال للمهمة والنسبة المئوية للتكاليف المستهلكة، وفرق التكلفة المتوقع في طريقة عرض تعقب التكلفة. ومع ذلك، لا تؤثر المراجعات في القيم الموجودة في طريقة عرض تعقب الجهد، نظراً لأنه لا تتم مراجعة التكلفة حسب نوع الحركة (العمالة أو المادة أو المصروفات) أو فئة المشروع. 

**مراجعة التوقع للتكاليف في مهام الملخص** يمكنك مراجعة التكاليف في مهام الملخص، وتتم العمليات الحسابية تلقائياً بالترتيب التالي:

1.  تتم إعادة حساب التقدير عند الاكتمال وتكلفة الإكمال والنسبة المئوية للتكاليف المستهلكة في المهمة.
2.  يتم توزيع التقدير عند الاكتمال على المهام التابعة بنفس نسبة مبلغ التقدير عند الاكتمال في المهام.
3.  يتم حساب التقدير الجديد عند الاكتمال لكل مهمة.
4.  تتم إعادة حساب CTS ونسبة التكلفة المستهلكة للمهام الفرعية المتأثرة، استناداً إلى قيمة التقدير عند الاكتمال. كما تتم إعادة حساب فرق التكلفة للمهام.
5.  تتم إعادة حساب التقدير عند الاكتمال لكافة مهام الملخص استناداً إلى هذا التغيير.

انقر فوق **توسيع إلى مستوى** في طريقة عرض تعقب التكلفة لتعيين المستوى الذي يجب فيه تعقب والاحتفاظ بهيكل تنظيم العمل الخاص بك. يتم توسيع هيكل تنظيم العمل تلقائياً إلى هذا المستوى في طريقة عرض تعقب التكلفة عندما تقوم بفتحها.

### <a name="earned-value-management"></a>إدارة القيمة المكتسبة

يمكنك استخدام طريقة القيمة المكتسبة (EVM) لتعقب تقدم المشروع. ويمكنك عرض قياسات القيمة المكتسبة في مركز أدوار مدير المشروع. ويعرض مكون مخطط القيمة المكتسبة القيم الموزعة على الوقت للقيمة المخططة والتكلفة الفعلية. ويتم عرض القيمة المكتسبة اعتبارًا من التاريخ الحالي كنقطة. البيانات الموزعة على الوقت للقيمة المكتسبة غير متوفرة حاليًا. 

ويتم عرض المرحلة الزمنية في مخطط القيمة المكتسبة حسب الأسبوع أو الشهر. ويصف هذا القسم ثلاثة أركان لطريقة القيمة المكتسبة: القيمة المخططة، والقيمة المكتسبة، والتكلفة الفعلية. 

**القيمة المخططة** تذكر نظرية طريقة القيمة المكتسبة أن رسم القيمة المخططة يمثل المعدل الذي يعتزم به فريق المشروع كسب قيمة في المشروع. 

ويستخدم Finance and Operations قاعدة الكسب 0:100 عندما يرسم القيمة المخططة. وعملاً بهذه المادة، يتم ترحيل قيمة المهمة إلى المهمة اعتبارًا من تاريخ انتهائها. لا يتم ترحيل أية قيمة حتى اكتمال المهمة بنسبة 100 بالمائة. 

وفي محاسبة وإدارة المشروع، يمكنك إدخال تاريخ انتهاء العقد الطرفية والتكلفة المخططة لها. وعندما يتم عرض الرسم البياني للقيمة المخططة حسب الأسبوع، يتم تلخيص القيمة المخططة حسب الأسبوع لكافة مهام العقد الطرفية طوال مدة المشروع. 

**القيمة المكتسبة** تذكر نظرية طريقة القيمة المكتسبة أن رسم القيمة المكتسبة يمثل المعدل الذي يعتزم به فريق المشروع كسب قيمة بالفعل في المشروع. 

ويستخدم Finance and Operations قاعدة الكسب 0:100 عندما يرسم القيمة المكتسبة. وعملاً بهذه المادة، يتم ترحيل قيمة المهمة إلى المهمة اعتبارًا من تاريخ انتهائها. لا يتم ترحيل أية قيمة حتى اكتمال المهمة بنسبة 100 بالمائة. 

وعند حساب القيمة المكتسبة، تتم مراعاة نسبة التقدم لكل مهمة. وضمن قاعدة الكسب 0:100، لا تتم مراعاة سوى المهام التي تم إكمالها في فترة محددة لحساب القيمة المكتسبة اعتبارًا من نهاية تلك الفترة. ويتم حساب القيمة المكتسبة في المشروع لكافة المهام التي تم إكمالها عند إنشاء الرسم البياني. 

> [!NOTE] 
> حاليًا، لا يشتمل النظام لتعقب هيكل تنظيم العمل على هياكل بيانات لتخزين النسب المئوية التاريخية للتقدم في كل مهمة. ولذلك، يمكن الإبلاغ عن القيمة المكتسبة فقط اعتبارًا من وقت معالجة المكعب. وقم بمعالجة معالجة المكعب بشكل دوري لتحديث بيانات القيمة المكتسبة التي يتم عرضها في مركز الأدوار. 

**التكلفة الفعلية** تذكر نظرية طريقة القيمة المكتسبة أن رسم التكلفة الفعلية يمثل معدل يتم عنده إنفاق المال في المشروع. 

ويتم استخدام الحركات التي تم ترحيلها إلى مشروع لرسم بند التكلفة الفعلية. ويتم تلخيص التكاليف حسب التاريخ. ويتمفيما بعد استخدام هذه البيانات لإنشاء رسم بياني للتكاليف الفعلية حسب الأسبوع أو الشهر في المخطط القيمة المكتسبة.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>كيفية استخدام مفاهيم القيمة المخططة والقيمة المكتسبة والتكلفة الفعلية

**فرق الجدولة** أثناء التخطيط، تقوم بإنشاء تنبؤ للعمل في جدول زمني. ولذلك، القيمة المخططة هي المعدل الذي يعتقد به مخططو المشروع أن العمل سينتهي في المشروع. وبعد أن يصبح المشروع قيد التقدم، يكتمل العمل، ويكسب المشروع قيمة. وبمقارنة القيمة المخططة بالقيمة المكتسبة، يمكنك عرض مدى تقدم العمل في مشروع. وتُسمى نتيجة هذه المقارنة بفرق الجدولة. 

وإذا كانت القيمة المخططة لفترة أكبر من القيمة المكتسبة، فإن مقدار العمل الذي تم إنجازه في مشروع يكون أقل مما كان مخططًا له. ولذلك، يكون المشروع متأخراً عن موعده. ولأن القيمة المخططة والقيمة المكتسبة يتم التعبير عنها بمبالغ نقدية، يتم إعطاء قيمة نقدية للمدة الانتقالية في المشروع أيضًا. 

وإذا كانت القيمة المخططة لفترة أقل من القيمة المكتسبة، فإن مقدار العمل الذي تم إنجازه في مشروع يكون أكبر مما كان مخططًا له. ولذلك، يكون المشروع متقدمًا عن موعده. كما يتم إعطاء قيمة نقدية لوقت الإنتاج هذا.

**فرق التكلفة** لأن القيمة المكتسبة تستخدم سعر التكلفة المضاعف، تشير القيمة المكتسبة إلى تكلفة العمل الذي يتم إنجازه في مشروع. وأثناء تقدم مشروع، يوفر سجل الحركات سجل أموال يتم إنفاقها فعلياً على ذلك المشروع. وبمقارنة القيمة المكتسبة بالتكلفة الفعلية، يمكنك عرض مبلغ المال الذي يتم إنفاقه مقابل القيمة التي يتم كسبها. وتُسمى نتيجة هذه المقارنة بفرق التكلفة. 

وإذا كانت التكلفة الفعلية التي يتم إنفاقها لفترة أكبر من القيمة المكتسبة، يتم إنفاق أموال أكثر مما تم اكتسابه. ولذلك، يشتمل المشروع على مبالغ زائدة على الموازنة. 

وإذا كانت التكلفة الفعلية التي يتم إنفاقها لفترة أقل من القيمة المكتسبة، فإنه يتم كسب أموال أكثر مما يتم إنفاقه. ولذلك، يشتمل المشروع على مبالغ ناقصة عن الموازنة.

## <a name="wbs-templates"></a>قوالب WBS
‏‫يمكنك استخدام وظيفة قوالب هيكل تنظيم العمل لإنشاء قوالب موحدة للمشاريع.‬ وإذا كانت المشاريع التي تقدمها شركتك تشتمل على كثير من العمل القابل للتكرار، يجب عليك مراعاة إنشاء قالب هيكل تنظيم العمل. 

يمكنك إنشاء قالب هيكل تنظيم عمل من هيكل تنظيم عمل مشروع موجود، بحيث يمكن إعادة استخدام المعرفة وأفضل الممارسات التي حصلت عليها أثناء التخطيط لذلك المشروع في مشاريع مماثلة في المستقبل. ومع ذلك، في بعض الأحيان، قد لا يعقل حفظ هيكل تنظيم العمل الكامل كقالب. ولذلك، يمكنك أيضًا إنشاء قوالب من أجزاء من هيكل تنظيم العمل لمشروع.

### <a name="saving-a-projects-wbs-as-a-template"></a>حفظ هيكل تنظيم العمل للمشروع كقالب

بعد إنشاء قالب، يمكنك استيراده إلى هيكل تنظيم عمل مشروع جديد في إطار العقدة الجذر أو ضمن أي مهمة في هيكل تنظيم عمل المشروع.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>استيراد قالب هيكل تنظيم العمل إلى هيكل تنظيم عمل المشروع

عندما تقوم باستيراد المهام، يتم تنظيم المهام في القالب بناءً على تاريخ البدء للمهمة التي تم استيرادها ضمنها. وأثناء عملية الاستيراد، يتم استخدام العلاقات السابقة في مهام القوالب لحساب تواريخ البدء للمهام المستوردة. ويتم استخدام تقويم العمل القياسي لمشروع الوجهة لحساب تواريخ انتهاء المهام المستوردة، بحيث يتم الاحتفاظ بأيام العمل وساعات العمل القياسية التي تم تحديدها في تقويم عمل المشروع الحالي. 

يتم استخدام مبالغ التكلفة وأسعار المبيعات على بنود التقدير لضمان أن تشتمل الأسعار الخاصة بالمشروع أو عقد المشروع على تواريخ صالحة.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>الاختلافات بين هيكل تنظيم عمل المشروع وقالب هيكل تنظيم العمل

-   لا تشتمل المهام في قوالب هيكل تنظيم العمل على تواريخ البدء وتواريخ الانتهاء.

لم يتم تعيين أيام العمل وأيام غير العمل لقوالب هيكل تنظيم العمل.

-   تستخدم قوالب هيكل تنظيم العمل دائماً تقويم الجدولة الذي تم إعداده كتقويم افتراضي لكافة المشاريع.

يتم استخدام جدولة التقويم الافتراضي فقط لمعرفة الساعات في يوم العمل القياسي.

-   لا يتم نسخ العلاقات السابقة إلى قالب هيكل تنظيم العمل.

لأن قوالب هيكل تنظيم العمل لا تشتمل على تواريخ، لا يُتطلب وجود منطق تاريخ البدء المستند إلى تاريخ انتهاء مهمة سابقة.

-   يتم إنشاء بند تقدير تكلفة عمالة تلقائياً عندما يتم إنشاء مهمة في قالب هيكل تنظيم العمل. يتم نسخ سعر المبيعات ومبلغ التكلفة من العامل المحدد.

يمكن إنشاء تكاليف المصروفات والأصناف يدوياً، تمامًا كما هو الحال في هيكل تنظيم عمل المشروع.

-   يتم عرض أخطاء الجدولة عند وجود انحرافات عن المعادلة التالية:

الجهد = عدد الموارد × المدة × عدد الساعات في يوم عمل قياسي 

يمكنك تصحيح كافة أخطاء الجدولة في الوقت نفسه بالنقر فوق **إصلاح كافة أخطاء جدولة**. 

وبدلاً من ذلك، يمكنك تصحيح أخطاء الجدولة كل على حدة بواسطة النقر فوق رمز تحذير لكل مهمة.




