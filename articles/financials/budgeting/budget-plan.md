---
title: "تخطيط الموازنة"
description: "يتمثل الهدف من هذا المعمل في تقديم عرض إرشادي لتحديثات وظائف Microsoft Dynamics 365 for Finance and Operations, Enterprise edition في مجال تخطيط الموازنة. الغرض من هذا المعمل هو توضيح مثال تكوين سريع لوحدة تخطيط الموازنة وإظهار كيف يمكن إنجاز تخطيط الموازنة باستخدام هذا التكوين.  سيركز هذا المعمل على وجه التحديد على العمليات التجارية أو مهام العمل التالية: - إنشاء التدرج الهرمي التنظيمي لتخطيط الموازنة وتكوين أمان المستخدم - تعريف سيناريوهات خطة الموازنة وأعمدة خطة الموازنة وتخطيطات وقوالب Excel - إنشاء عملية تخطيط الموازنة وتنشيطها - إنشاء مستند خطة الموازنة بسحب القيم الفعلية من دفتر الأستاذ العام - استخدام التوزيعات لضبط بيانات مستند خطة الموازنة - تحرير بيانات مستند خطة الموازنة في Excel"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 608ec87233acb05b0d46e367bcb7cd14985d7813
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---

# <a name="budget-planning"></a>تخطيط الموازنة

[!include[banner](../includes/banner.md)]


يتمثل الهدف من هذا المعمل في تقديم عرض إرشادي لتحديثات وظائف Microsoft Dynamics 365 for Finance and Operations, Enterprise edition في مجال تخطيط الموازنة. الغرض من هذا المعمل هو توضيح مثال تكوين سريع لوحدة تخطيط الموازنة وإظهار كيف يمكن إنجاز تخطيط الموازنة باستخدام هذا التكوين.  سيركز هذا المعمل على وجه التحديد على العمليات التجارية أو مهام العمل التالية: - إنشاء التدرج الهرمي التنظيمي لتخطيط الموازنة وتكوين أمان المستخدم - تعريف سيناريوهات خطة الموازنة وأعمدة خطة الموازنة وتخطيطات وقوالب Excel - إنشاء عملية تخطيط الموازنة وتنشيطها - إنشاء مستند خطة الموازنة بسحب القيم الفعلية من دفتر الأستاذ العام - استخدام التوزيعات لضبط بيانات مستند خطة الموازنة - تحرير بيانات مستند خطة الموازنة في Excel 

<a name="prerequisites"></a>المتطلبات الأساسية 
------------------

بالنسبة إلى البرنامج التعليمي، سوف تحتاج إلى الوصول إلى بيئة Finance and Operations مع بيانات تجريبية لشركة التعمير، ويتم توفيرها كمسؤول في المثيل. فلا تستخدم المستعرض الخاص لهذا المعمل - قم بتسجيل الخروج من أي حساب آخر في المستعرض إذا لزم الأمر وتسجيل الدخول باستخدام بيانات اعتماد مسؤول Finance and Operations. عند تسجيل الدخول إلى Finance and Operations، **يجب** عليك تحديد خانة اختيار "الاستمرار في تسجيل الدخول". ويؤدي هذا إلى إنشاء ملف تعريف ارتباط دائم يحتاج تطبيق Excel إليه حاليًا. وفي حالة تسجيل الدخول إلى Finance and Operations باستخدام مستعرض غير IE، فستتم مطالبتك بتسجيل الدخول في تطبيق Excel. وعند النقر فوق "تسجيل الدخول" في تطبيق Excel، سيتم فتح نافذة IE المنبثقة وعند تسجيل الدخول، **يجب** عليك تحديد خانة الاختيار "الاستمرار في تسجيل الدخول". إذا كان النقر فوق "تسجيل الدخول" في تطبيق Excel لا يبدو أنه يفعل أي شيء، فيجب مسح ذاكرة التخزين المؤقت لملف تعريف ارتباط مستعرض IE.

## <a name="scenario-overview"></a>**نظرة عامة على السيناريو**
تعمل ليلى كمدير مالي في شركة الرشيدي المحدودة في القاهرة. ومع اقتراب العام المالي 2016، تحتاج إلى العمل في إعداد موازنة الشركة للسنة المقبلة. يبدو إعداد الموازنة على النحو التالي:

1.  تستخدم ليلى المبالغ الفعلية للسنة السابقة كنقطة بداية لإنشاء الموازنة.
2.  واستناداً إلى المبالغ الفعلية في العام السابق، تقوم بإنشاء تقديرات لمدة 12 شهرًا في السنة المقبلة
3.  وتراجع ليلى الموازنة مع المدير المالي. وبمجرد أن تتنهي من المراجعة، تقوم بإجراء التعديلات اللازمة لخطة الموازنة وتتولى الصياغة النهائية لإعداد الموازنة.

يبدو مخطط تكوين التخطيط للموازنة لهذا السيناريو على النحو التالي:

![مخطط تكوين تخطيط الموازنة](./media/screenshot1-300x152.png)

تستخدم جوليا قالب Excel التالي في إعداد الموازنة:

[![قالب Excel](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>التمرين 1: التكوين
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**المهمة 1: إنشاء تدرج هرمي للمؤسسات**
نظرًا لأن عملية إعداد الموازنة تحدث في إدارة الشؤون المالية، يلزم ليلى إنشاء تدرجي هرمي للمؤسسات بسيطة جداً - يتكون من القسم المالي. 1.1. الانتقال إلى التدرجات الهرمية للمؤسسات (إدارة المؤسسة &gt; المؤسسات &gt; التدرجات الهرمية للمؤسسات)، وانقر فوق زر جديد

![التدرج الهرمي للمؤسسة](./media/screenshot3.png) 

1.2. اكتب اسم للتدرج الهرمي للمؤسسات، ثم انقر فوق زر تعيين الغرض

[![الاسم](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. حدد غرض تخطيط الموازنة، ثم انقر فوق زر "إضافة" وقم بتعيين التدرج الهرمي للمؤسسات الذي تم إنشاؤه حديثًا: 

[![تعيين غرض](./media/screenshot5.png)](./media/screenshot5.png)

1.4. كرر الخطوة أعلاه للأغراض التنظيمية الأمنية. وأغلق النموذج عند الانتهاء.

[![مؤسسة الأمان](./media/screenshot6.png)](./media/screenshot6.png)

1.5. في نموذج التدرجات الهرمية للمؤسسات، انقر فوق الزر عرض. انقر فوق "تحرير" في مصمم التدرج الهرمي وأنشئ تدرجًا هرميًا بواسطة النقر فوق الزر إدراج.

[![إدراج](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. حدد القسم المالي للتدرج الهرمي لإعداد الموازنة. 

[![المالية](./media/screenshot8.png)](./media/screenshot8.png)

1.7. عند الانتهاء، انقر فوق الزر نشر وإغلاق. حدد 1/1/2015 كتاريخ سريان لنشر التدرج الهرمي.

[![تاريخ السريان](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>المهمة 2: تكوين أمان المستخدم
يستخدم تخطيط الموازنة سياسات أمان خاصة لتكوين الوصول إلى بيانات خطط الموازنة. وتحتاج ليلى إلى منح حق الوصول إلى خطط الموازنة المالية لنفسها. 

2.1. التبديل إلى سياق الكيان القانوني لشركة الرشيدي المحدودة. 


2.2. انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة. في علامة تبويب "المعلمات"، قم بتعيين قيمة نموذج الأمان إلى "استنادًا إلى مؤسسات الأمان". 

[![المعلمات](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. انتقل إلى إدارة النظام &gt; المستخدمين &gt; المستخدمين. إعطاء مستخدم مسؤول (ليلى فوزي) دور مدير الموازنة. 

[![مدير الموازنة](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. اختر دور المستخدم وانقر فوق "تعيين مؤسسات". 

[![تعيين مؤسسات](./media/screenshot13.png)](./media/screenshot13.png)

2.5. حدد "منح الوصول إلى مؤسسات محددة". اختيار التدرج الهرمي للمؤسسات الذي تم إنشاؤه في الخطوة الأولى. اختر عقدة المالية وانقر فوق الزر "‏‫منح الوصول مع المؤسسات الفرعية‬". 

***هام!*** *تأكد من أنك موجود في سياق الكيان القانوني لشركة الرشيدي المحدودة عند تنفيذ هذه المهمة، إذ يتم تطبيق الأمان التنظيمي لكل كيان قانوني* 

[![منح الوصول](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>المهمة 3: إنشاء السيناريوهات
3.1. انتقل إلى إعداد الموازنة&gt;إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة. في صفحة السيناريوهات، لاحظ السيناريوهات التي سنقوم باستخدامها في هذا المعمل: القيم الفعلية والقيم المدرجة في الموازنة للسنة السابقة. 

*ملاحظة: يمكنك إنشاء سيناريوهات جديدة لهذه العملية عند الضرورة واستخدامها بدلاً من ذلك.* 

[![سيناريوهات جديدة](./media/screenshot15.png)](./media/screenshot15.png) 

*ملاحظة: بما أن ليلى لا تستخدم عملية الموافقة الرسمية لإعداد الموازنة، سوف نتخطى إعداد مهام سير العمل، والمراحل ومراحل سير العمل في هذا المعمل، وسنستخدم الإعداد الموجود لسير عمل الاعتماد التلقائي لسير العمل. انظر الملحق لتكوين سير العمل هذا.*

## <a name="task-4-create-budget-plan-columns"></a>المهمة 4: إنشاء أعمدة خطة الموازنة
وتكون اعمدة خطة الموازنة إما أعمدة مستندة إلى النقد أو الكمية ويمكن استخدامها في تخطيط مستند خطة الموازنة. وفي المثال الخاص بنا، نحتاج إلى إنشاء عمود للقيم الفعلية للسنة السابقة و12 عمودًا لتمثيل كل شهر في السنة المدرجة في الموازنة. ويمكن إنشاء الأعمدة أما بمجرد النقر فوق الزر "إضافة" وتعبئة القيم، أو بمساعدة من وحدة بيانات. في هذا المعمل، سوف نستخدم وحدة بيانات لتعبئة القيم. 

4.1. ‏‫في إعداد الموازنة&gt;إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة، افتح صفحة الأعمدة. انقر فوق زر Office في الركن العلوي الأيسر من النموذج واختر الأعمدة (غير المصفاة). 

[![أعمدة غير مصفاة](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. سيقوم النظام بفتح مصنف Excel لاستخدامه لتعبئة القيم. انقر فوق "تمكين التحرير والثقة في هذا التطبيق"، عند ظهور المطالبة 

[![تمكين ‏‏التحرير](./media/screenshot18.png)](./media/screenshot18.png) 

[![الثقة في هذا التطبيق](./media/screenshot17.png)](./media/screenshot17.png)

4.3. ‏‫وسنحتاج إلى مزيد من الأعمدة لتعبئة القيم. انقر فوق "تصميم" في الجزء الأيسر لإضافة الأعمدة إلى الشبكة: 

[![تصميم](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. ‏‫انقر فوق زر القلم الصغير بجوار أعمدة الخطة لمشاهدة الأعمدة المتوفرة لإضافتها إلى الشبكة. 

[![تحرير](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. ‏‫انقر نقرًا مزدوجًا فوق كل حقل متوفر لإضافته إلى الحقول المحددة وانقر فوق "تحديث" 

![تحديث](./media/screenshot21.png)](./media/screenshot21.png) 

4.6. في جدول Excel، أضف كافة الأعمدة التي يلزم إنشاؤها. استخدم ميزة الملء التلقائي في Excel لإضافة البنود بسرعة. ‏‫تأكد من إضافة البنود كجزء من الجدول (عند استخدام التمرير العمودي، يجب أن تتمكن من رؤية رؤوس الأعمدة أعلى الشبكة) 

[![تعبئة تلقائية](./media/screenshot22.png)](./media/screenshot22.png) 

4.7. قم بالرجوع إلى Finance and Operations، ثم قم بتحديث الصفحة. سوف تظهر القيم المنشورة في Finance and Operations. 

[![تحديث](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>المهمة 5: إنشاء قوالب وتخطيطات وثيقة خطة الموازنة
يحدد المخطط كيف ستبدو شبكة بنود وثيقة خطة الموازنة عندما يقوم المستخدم بفتح مستند خطة الموازنة. كما أنه من الممكن تبديل تخطيط مستند خطة الموازنة لعرض نفس البيانات الموجودة في زوايا مختلفة. والآن، عندما حصلت ليلى على الأعمدة المحددة لاستخدامها مع مستند خطة الموازنة، فهي تحتاج إلى إنشاء تخطيط مستند خطة موازنة يبدو مماثلاً لجدول Excel يمكنها استخدامه لإنشاء بيانات الموازنة (راجع قسم نظرة عامة على السيناريو في هذا المعمل) 

5.1. في إعداد الموازنة&gt;إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة، افتح صفحة التخطيطات. قم بإنشاء تخطيط جديد لإدخال الموازنة الشهرية:

-   اختر مجموعة الأبعاد MA+BU لتضمين الحسابات الرئيسية ووحدات الأعمال في التخطيط.
-   اسرد كافة أعمدة خطة الموازنة التي تم إنشاؤها في الخطوة السابقة في قسم العناصر. اجعل كافة القيم الفعلية قابلة للتحرير ما عدا القيم الفعلية للسنة السابقة.
-   انقر فوق الزر أوصاف لتحديد الأبعاد المالية التي ينبغي أن تعرض الأوصاف في الشبكة.

[![الأوصاف](./media/screenshot24.png)](./media/screenshot24.png) 

استنادًا إلى تعريف تخطيط خطة الموازنة، يمكننا إنشاء قالب Excel لاستخدامه كطريقة بديلة لتحرير بيانات الموازنة.‬ ونظرًا لأنه يجب أن يتطابق قالب Excel مع تعريف تخطيط خطة الموازنة، لن تتمكن من تحرير تخطيط خطة الموازنة بعد إنشاء قالب Excel، وبالتالي يجب تنفيذ هذه المهمة بعد أن يتم تحديد كافة مكونات تخطيط. 

5.2. بالنسبة للتخطيط الذي تم إنشاؤه في الخطوة 5.1. انقر فوق الزر قالب &gt; إنشاء. تأكيد رسالة التحذير. لعرض القالب، انقر فوق قالب &gt; عرض. 

*ملاحظة: تأكد من اختيار "حفظ باسم" وحدد المكان الذي ينبغي تخزين القالب فيه من أجل تحريره. إذا اختار المستخدم "فتح" في مربع الحوار بدون الحفظ، فلن يتم الاحتفاظ بالتغييرات التي أُجريت على الملف عند إغلاق الملف.* 
[![طريقة عرض القالب](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; خطوة اختيارية&gt; اعمل على تعديل قالب Excel لكي يكون مألوفًا أكثر بالنسبة إلى المستخدم – أضف المعادلات الإجمالية وحقول الرأس والتنسيقات وغير ذلك. احفظ التغييرات وقم بتحميل الملف إلى تخطيط خطة الموازنة بالنقر فوق تخطيط &gt; تحميل [![تحميل](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>المهمة 6: إنشاء عملية تخطيط موازنة
تحتاج ليلى إلى إنشاء وتنشيط عملية تخطيط موازنة جديدة تجمع كافة خطوات الإعداد السابقة للبدء في إدخال خطط الموازنة. تحدد عملية تخطيط الموازنة مؤسسات إعداد الموازنة، وسير العمل، والتخطيطات، والقوالب التي سيتم استخدامها لإنشاء خطط الموازنة. 

6.1. انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; عملية تخطيط الموازنة وإنشاء سجل جديد.

-   عملية تخطيط الموازنة - إعداد الموازنة لشركة الرشيدي المحدودة للعام المالي 2016
-   دورة الموازنة - العام المالي 2016
-   دفتر الأستاذ - شركة الرشيدي المحدودة
-   بنية الحساب الافتراضي - أرباح وخسائر التصنيع
-   التدرج الهرمي للمؤسسات – اختيار التدرج الهرمي الذي تم إنشاؤه في بداية المعمل
-   سير عمل تخطيط الموازنة – تعيين تلقائي – اعتماد سير العمل لإدارة الشؤون المالية
-   في قوالب وقواعد مرحلة تخطيط الموازنة، بالنسبة لكل مرحلة تخطيط موازنة سير عمل، اختر ما إذا كان مسموحًا بإضافة البنود وتعديل البنود والتخطيط الذي يجب استخدامه بشكل افتراضي

*ملاحظة: يمكنك إنشاء تخطيطات المستند الإضافية وقم بتعيينها لتكون متوفرة في مرحلة سير عمل تخطيط الموازنة عن طريق النقر فوق الزر تخطيطات بديلة.* 

[![التخطيطات البديلة](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. حدد الإجراءات &gt; تنشيط لتنشيط سير عمل تخطيط الموازنة هذا 

[![تنشيط](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>تمرين 2: محاكاة العملية
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>المهمة 7: إنشاء البيانات الأولية لخطة الموازنة من دفتر الأستاذ العام
7.1. انتقل إلى إعداد الموازنة &gt; دوري &gt; إنشاء خطة الموازنة من دفتر الأستاذ العام. قم بتعبئة معلمات العملية الدورية وانقر فوق الزر إنشاء. 

[![إنشاء](./media/screenshot29.png)](./media/screenshot29.png) 

7.2. انتقل إلى إعداد الموازنة &gt; خطط الموازنة للبحث عن خطة موازنة تم إنشاؤها بواسطة عملية الإنشاء. 

[![خطة الموازنة](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. افتح تفاصيل المستند بالنقر فوق الارتباط التشعبي رقم المستند. يتم عرض خطة الموازنة كما هو محدد في التخطيط الذي تم إنشاؤه أثناء الوجود في هذا المعمل 

[![عرض خطة الموازنة](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>المهمة 8: إنشاء موازنة السنة الحالية استناداً إلى القيم الافتراضية للسنة السابقة
يمكن استخدام طرق التوزيع في خطة الموازنة نسخ المعلومات الخاصة بخطط الموازنة بسهولة من سيناريو واحد إلى آخر / نشرها عبر فترات/توزيعها على أبعاد. سوف نستخدم التوزيعات لإنشاء موازنة السنة الحالية من القيم الفعلية للسنة السابقة. 

8.1. اختر كافة البنود في شبكة مستند خطة الموازنة، وانقر فوق الزر "توزيع الموازنة" 

[![كافة البنود](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. حدد طريقة التخصيص، والمفتاح الدوري، والمصدر وسيناريوهات الوجهة، ثم انقر فوق تخصيص 

[![توزيع](./media/screenshot33.png)](./media/screenshot33.png)

سوف يتم نسخ المبالغ الفعلية للعام الماضي إلى موازنة السنة الحالية، وتخصصيها عبر الفترات باستخدام مفتاح فترة منحنى المبيعات. 

[![منحنى المبيعات](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>المهمة 9: ضبط مستند خطة الموازنة باستخدام Excel ووضع الصيغة النهائية للمستند
9.1. انقر فوق الزر ورقة عمل لفتح محتويات المستند في Excel.

[![Excel](./media/screenshot35.png)](./media/screenshot35.png)

9.2. عند فتح مصنف Excel، اضبط الأرقام في مستند خطة الموازنة، وانقر فوق الزر نشر.

[![نشر](./media/screenshot36.png)](./media/screenshot36.png)

9.3. ارجع إلى مستند خطة الموازنة في Finance and Operations. انقر فوق سير العمل &gt; إرسال وذلك لاعتماد المستند تلقائيًا

[![الاعتماد التلقائي](./media/screenshot37.png)](./media/screenshot37.png) 

بمجرد اكتمال سير العمل، يتم تغيير مرحلة مستند خطة الموازنة إلى "معتمد". [![معتمد](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>الملحق
========

### <a name="auto-approve-workflow-configuration"></a>الاعتماد التلقائي لتكوين سير العمل

أ. إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; ‏‫عمليات سير عمل إعداد الموازنة‬ قم بإنشاء سير عمل جديد باستخدام قالب عمليات سير العمل لتخطيط الموازنة.

[![إنشاء سير عمل جديد](./media/screenshot39.png)](./media/screenshot39.png)

سوف يحتوي سير العمل هذا على مهمة واحدة فقط- مرحلة الانتقال لخطة الموازنة 

[![مرحلة انتقال خطة الموازنة](./media/screenshot40.png)](./media/screenshot40.png) 

احفظ سير العمل ونشّطه. 

ب. انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة. في علامة التبويب "المراحل" قم بإنشاء مرحلتين- الأولية والمرسلة 

[![الأولى والمرسلة](./media/screenshot41.png)](./media/screenshot41.png)

ج. انتقل إلى إعداد الموازنة &gt; إعداد &gt; تخطيط الموازنة &gt; تكوين تخطيط الموازنة. في علامة التبويب "مراحل سير العمل"، قم بإقران الاعتماد التلقائي لسير العمل الذي تم إنشاؤه في خطوة أ مع المرحلتين الأولية والمرسلة 

[![إعداد الموازنة‬ وتخطيط الموازنة‬](./media/screenshot42.png)](./media/screenshot42.png)  



