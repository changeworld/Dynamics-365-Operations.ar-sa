---
title: "معالجة دفتر اليومية العام"
description: "تصف هذه المقالة القدرات المتوفرة في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition التي يمكنها المساعدة في جعل معالجة دفتر اليومية العام تتم بشكل أسهل، والتي يمكنها أيضًا المساعدة في ضمان تسجيل البيانات الصحيحة وعدم اختراق التحكم الداخلي."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 68da281cb4793ed83f70c68d061d327aa8a8c772
ms.contentlocale: ar-sa
ms.lasthandoff: 08/01/2017

---

# <a name="general-journal-processing"></a>معالجة دفتر اليومية العام

[!include[banner](../includes/banner.md)]


تصف هذه المقالة القدرات المتوفرة في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition التي يمكنها المساعدة في جعل معالجة دفتر اليومية العام تتم بشكل أسهل، والتي يمكنها أيضًا المساعدة في ضمان تسجيل البيانات الصحيحة وعدم اختراق التحكم الداخلي.  

أسماء دفاتر اليومية

إحدى المناطق الأهم التي يتعين إعدادها هي أسماء دفاتر اليومية. وإنها لفكرة جيدة أن يتم تحديد أسماء دفاتر يومية محددة لكل غرض، مثل الشركات الشقيقة، وتسوية الاستحقاق، وتصحيح الخطأ. ويمكنك تعديل كل اسم دفتر يومية للمساعدة في جعل إدخال البيانات لكل غرض سهلاً وآمنًا.‬ 

وفي صفحة **أسماء دفاتر اليومية**، يمكنك إعداد العناصر التالية:

-   **اعتماد سير العمل** – لزيادة المراقبة الداخلية، حدد مهام سير عمل دفتر اليومية التي تضع حدود الأهمية النسبية لخطوات المراجعة والاعتماد، استناداً إلى معايير مثل إجمالي المبلغ المدين. وتقوم بإعداد مهام سير العمل لدفاتر اليومية العامة في صفحة **مهام سير العمل في دفتر الأستاذ العام**.
-   **القيم الافتراضية** – تحديد القيم الافتراضية للحسابات المقابلة والعملة والأبعاد المالية.
-   **التحكم في دفتر اليومية** – يمكنك إعداد قيود على الشركة ونوع الحساب وأيضًا قيم الشرائح. 

**أمثلة**

ويمكن استخدام اسم دفتر يومية للتسويات فقط. وفي هذه الحالة، يمكنك تحديد أن نوع حساب **دفتر الأستاذ** فقط صالح في كافة الشركات. [![أنواع حساب التحكم في دفتر اليومية](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

يمكن استخدام اسم دفتر اليومية فقط لمقطع محدد أو لمجموعة حسابات رئيسية. [![مقطع التحكم في دفتر اليومية](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

يتوفر خيار **الإلغاء التلقائي** في دفاتر اليومية العامة. على سبيل المثال، لديك تسوية استحقاق لم تتم فيها معالجة المستند الفعلي، كما هو مبين في التوضيح التالي.
[![عكس دفتر اليومية العام](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

يوفر مكون Microsoft Excel الإضافي لإدخال دفتر اليومية مستوى إضافيًا من التشغيل الآلي ويجعل إدخال البيانات أسهل. ويتوفر إجراء **فتح البنود في Excel** في صفحتي **دفتر اليومية العام** و**إيصال دفتر اليومية**. 

وفي صفحة **دفاتر اليومية الدورية**، يمكنك إعداد دفاتر اليومية المتكررة لإجراء معالجة دفتر اليومية تلقائيًا. 

يمكنك استخدام قوالب الإيصال في أي وقت. وفي صفحة **دفاتر اليومية العامة**، يتم العثور على إجراءات **الحفظ** و**تحديد قالب الإيصال** في صفحة **إيصال دفتر اليومية**، ضمن **الوظائف** لبنود الإيصال.

## <a name="related-setup"></a>الإعداد ذو الصلة
الإعداد التالي ليس خاصًا بدفاتر اليومية العامة، ولكنه سيساعد على ضمان أن يكون إدخال البيانات صحيحًا وسهلاً.

### <a name="main-account"></a>الحساب الرئيسي

ويوفر إعداد الحساب الرئيسي يوفر العديد من الخيارات لمعالجة دفتر اليومية العام:

-   **متطلبات DC/CR** – استخدم هذا الخيار إذا كان حساب رئيسي يقتصر على الحركات المدينة أو الدائنة. ويتم التحقق من الإعداد عندما يتم التحقق من صحة دفتر يومية أو ترحيله.
-   **الحساب المقابل الافتراضي**
-   **معلق** -تعليق حساب رئيسي لإدخال البيانات عبر كافة الشركات أو لكيانات قانونية/شركة محددة.
-   **عدم السماح بالإدخال اليدوي** – منع المستخدمين من إدخال قيمة يدوياً للحساب في دفاتر اليومية.
-   **العملة الافتراضية/التحقق من العملة**
-   **تجاوز الكيان القانوني** -هذا الإعداد خاص بالكيان القانوني/الشركة المحددة.
    -   **ضريبة المبيعات الافتراضية/التحقق منها**
    -   **البعد الافتراضي** - **قيمة غير ثابتة** أو **قيمة ثابتة**. ستساعد **القيمة الثابتة** على ضمان أن جميع عمليات الترحيل لهذا الحساب الرئيسي تستخدم دائماً أي قيمة بعد يتم إعدادها كـ **ثابتة**.
-   **التحقق من صحة الترحيل**
    -   **التحقق من صحة المستخدم** – يتحكم هذا الخيار في المستخدمين المسموح لهم بالترحيل إلى حساب رئيسي.
    -   **التحقق من صحة نوع الترحيل** – يتحكم هذا الخيار في أنواع الترحيل المسموح بها لحساب رئيسي.

### <a name="accounting-structures-and-advanced-rules-structures"></a>هياكل المحاسبة وهياكل القواعد المتقدمة

هياكل المحاسبة وهياكل القواعد المتقدمة تعتبر بالغة الأهمية لضمان أن يتم التقاط البيانات اللازمة للتقارير المالية وتتبع الأداء أثناء معالجة دفتر اليومية العام وأية وثائق. وتسمح لك هياكل المحاسبة وهياكل القواعد المتقدمة بتفصيل تجربة إدخال البيانات. ويمكنك السماح بإدخال البيانات فقط للأبعاد المالية ذات الصلة في كل حالة، ويمكن أيضًا فرض متطلب الحصول على البيانات اللازمة والصحيحة دائماً.

لمزيد من المعلومات، راجع الموضوعات التالية:
- [التخطيط: دليل الحسابات](plan-chart-of-accounts.md) 
- [إنشاء قواعد متقدمة لدفاتر اليومية](tasks/create-advanced-rules-journals.md)
- [إنشاء إدخال دفتر يومية باستخدام قالب](tasks/create-journal-entry-template.md)
- [إنشاء دفاتر اليومية والتحقق من صحتها](tasks/create-validate-journals.md)
- [ترحيل دفاتر اليومية الدورية](tasks/post-periodic-journals.md)
- [‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬](tasks/process-ledger-allocation-journal.md)


