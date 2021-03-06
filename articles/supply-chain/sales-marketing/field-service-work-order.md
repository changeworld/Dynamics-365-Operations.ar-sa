---
title: "مزامنة أوامر العمل في Field Service إلى أوامر المبيعات في Finance and Operations"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل في Field Service لأوامر المبيعات في Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 8914723f6ef436bfc9e3a98cc82d5486042b0761
ms.openlocfilehash: 250b7caa1e1495140d0d4f688ecae4acb8814467
ms.contentlocale: ar-sa
ms.lasthandoff: 06/07/2018

---

# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>مزامنة أوامر العمل في Field Service إلى أوامر المبيعات في Finance and Operations

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل في Microsoft Dynamics 365 for Field Service لأوامر المبيعات في Microsoft Dynamics 365 for Finance and Operations.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/field-service-integration.png)](./media/field-service-integration.png)

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة أوامر العمل في Field Service لأوامر المبيعات في Finance and Operations.

## <a name="templates-and-tasks"></a>القوالب والمهام

يتم استخدام القوالب والمهام الأساسية التالية لتشغيل مزامنة أوامر العمل في Field Service لأوامر المبيعات في Finance and Operations.

### <a name="names-of-the-templates-in-data-integration"></a>أسماء القوالب في تكامل البيانات

يتم استخدام قالب **أوامر العمل لأوامر المبيعات (Field Service لـ Fin and Ops)** لتشغيل المزامنة.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>أسماء المهام في مشروع تكامل البيانات

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود أوامر المبيعات.

- منتجات Field Service ‏(Fin and Ops إلى Field Service)
- الحسابات (Sales إلى Fin and Ops)‬ - المباشرة

## <a name="entity-set"></a>مجموعة الكيانات

| **Field Service** | **Finance and Operations** |
|-------------------------|-------------------------|
| msdyn_workorders        | رؤوس أوامر مبيعات CDS |
| msdyn_workorderservices | بنود أمر مبيعات CDS   |
| msdyn_workorderproducts | بنود أمر مبيعات CDS   |

## <a name="entity-flow"></a>تدفق الكيان

يتم إنشاء أوامر العمل في Field Service. إذا كانت أوامر العمل تتضمن المنتجات التي تم الاحتفاظ بها خارجيًا فقط، وفي حالة اختلاف قيمة **حالة أمر العمل** عن **مفتوح - غير مجدول‬** و**مقفل - ملغي**، فإنه يمكن مزامنة لـ Finance and Operations عبر مشروع تكامل بيانات CDS. ستتم مزامنة تحديثات أوامر العمل كأوامر مبيعات في Finance and Operations. تتضمن هذه التحديثات معلومات حول نوع الأصل وحالته.

## <a name="estimated-versus-used"></a>المقدَّرة مقابل المستخدمة

في Field Service، تشتمل المنتجات والخدمات في أوامر العمل على كلٍّ من القيم **المقدَّرة** و**المستخدمة** للكميات والمبالغ. ومع ذلك، في Finance and Operations، لا تشمل أوامر المبيعات نفس مفهوم القيم **المقدَّرة** و**المستخدمة**. لدعم توزيع المنتجات الذي يستخدم الكمية المتوقعة في أمر المبيعات في Finance and Operations، ولكن للاحتفاظ بالكمية المستخدمة التي ينبغي استهلاكها وفوترتها، تقوم مجموعتان من المهام بمزامنة المنتجات والخدمات الموجودة في أمر العمل. هناك مجموعة مهام واحدة مخصصة للقيم **المقدَّرة**، ومجموعة المهام الأخرى مخصصة للقيم **المستخدمة**.

يعمل هذا السلوك على تمكين السيناريوهات التي يت فيها استخدام القيم المقدَّرة للتوزيع أو الحجز في Finance and Operations، بينما يتم استخدام القيم المستخدمة للاستهلاك والفوترة.

### <a name="estimated"></a>المقدر

لمزامنة خطوط الإنتاج، يتم استخدام القيم **المقدَّرة** عندما تكون قيمة **حالة الخط** **مقدَّرة**، ويت تعيين الخيار **تم التوزيع** إلى **نعم**، وقيمة **حالة النظام** لا تكون **مقفلة - مرّحلة**.

لمزامنة خطوط الخدمة، يتم استخدام القيم **المقدَّرة** عندما تكون قيمة **حالة الخط** **مقدَّرة** وقيمة **حالة النظام** لا تكون **مقفلة - مرّحلة**.

### <a name="used"></a>مستخدم

يتم استخدام القيم **المستخدمة** للاستهلاك والفوترة. في هذه الحالات، تتم مزامنة القيم **المستخدمة**.

يوفر الجدول التالي نظرة عامة على المجموعات المختلفة لخطوط الإنتاج.

| حالة النظام <br>(Field Service) | حالة الخط <br>(Field Service) | موزع <br>(Field Service) |القيمة المُزامنة <br>(Finance and Operations) |
|--------------------|-------------|-----------|---------------------------------|
| مفتوح - مجدول   | المقدر   | ‏‏نعم       | المقدر                       |
| مفتوح - مجدول   | المقدر   | لا        | مستخدم                            |
| مفتوح - مجدول   | مستخدم        | ‏‏نعم       | مستخدم                            |
| مفتوح - مجدول   | مستخدم        | لا        | مستخدم                            |
| مفتوح - قيد التقدم | المقدر   | ‏‏نعم       | المقدر                       |
| مفتوح - قيد التقدم | المقدر   | لا        | مستخدم                            |
| مفتوح - قيد التقدم | مستخدم        | ‏‏نعم       | مستخدم                            |
| مفتوح - قيد التقدم | مستخدم        | لا        | مستخدم                            |
| مفتوح - مكتمل   | المقدر   | ‏‏نعم       | المقدر                       |
| مفتوح - مكتمل   | المقدر   | لا        | مستخدم                            |
| مفتوح - مكتمل   | مستخدم        | ‏‏نعم       | مستخدم                            |
| مفتوح - مكتمل   | مستخدم        | لا        | مستخدم                            |
| مُقفل - مرحّل    | المقدر   | ‏‏نعم       | مستخدم                            |
| مُقفل - مرحّل    | المقدر   | لا        | مستخدم                            |
| مُقفل - مرحّل    | مستخدم        | ‏‏نعم       | مستخدم                            |
| مُقفل - مرحّل    | مستخدم        | لا        | مستخدم                            |

يوفر الجدول التالي نظرة عامة على المجموعات المختلفة لخطوط الخدمة.

| حالة النظام <br>(Field Service) | حالة الخط <br>(Field Service) | القيمة المُزامنة <br>(Finance and Operations) |
|--------------------|-------------|-----------|
| مفتوح - مجدول   | المقدر   | المقدر |
| مفتوح - مجدول   | مستخدم        | مستخدم      |
| مفتوح - قيد التقدم | المقدر   | المقدر |
| مفتوح - قيد التقدم | مستخدم        | مستخدم      |
| مفتوح - مكتمل   | المقدر   | المقدر |
| مفتوح - مكتمل   | مستخدم        | مستخدم      |
| مُقفل - مرحّل    | المقدر   | مستخدم      |
| مُقفل - مرحّل    | مستخدم        | مستخدم      |

تتم إدارة مزامنة القيم **المقدَّرة** مقابل القيم **المستخدمة** من خلال مجموعتي مهام خطوط الإنتاج وخطوط الخدمة. تقوم عوامل التصفية المحددة مسبقًا بتشغيل المهمة الصحيحة، ويساعد التعيين الأساسي على ضمان مزامنة القيم الصحيحة للقيم **المتوقعة** مقابل **المستخدمة**.

### <a name="example"></a>مثال

1. يتم إنشاء أمر عمل وجدولته في Field Service.

    قيمة **حالة النظام** هي **مفتوح - مجدول**.

    - **خط الإنتاج:** الكمية المقدرة = 5ea، الكمية المستخدمة = 0ea، حالة الخط = الكمية المقدرة، الموزعة = لا
    - **خط الخدمة:** الكمية المقدرة = 2h، الكمية المستخدمة = 0h، حالة الخط = المقدرة

    في هذا المثال، تتم مزامنة قيمة **الكمية المستخدمة** البالغة **0** (صفر) وقيمة **الكمية المقدرة** للخدمة والبالغة **2h** لـ Finance and Operations.

2. يتم توزيع المنتجات في Field Service.

    قيمة **حالة النظام** هي **مفتوح - مجدول**.

    - **خط الإنتاج:** الكمية المقدرة = 5ea، الكمية المستخدمة = 0ea، حالة الخط = الكمية المقدرة، الموزعة = نعم
    - **خط الخدمة:** الكمية المقدرة = 2h، الكمية المستخدمة = 0h، حالة الخط = المقدرة

    في هذا المثال، تتم مزامنة قيمة **الكمية المقدرة** البالغة **5ea** وقيمة **الكمية المقدرة** للخدمة والبالغة **2h** لـ Finance and Operations.

3. يبدأ فني الخدمة في العمل في أمر العمل ويسجل استخدام المادة 6.

    قيمة **حالة النظام** هي **مفتوحة - قيد التقدم**.

    - **خط الإنتاج:** الكمية المقدرة = 5ea، الكمية المستخدمة = 6ea، حالة الخط = الكمية المستخدمة، الموزعة = نعم
    - **خط الخدمة:** الكمية المقدرة = 2h، الكمية المستخدمة = 0h، حالة الخط = المقدرة

    في هذا المثال، تتم مزامنة قيمة **الكمية المستخدمة** البالغة **6** وقيمة **الكمية المقدرة** للخدمة والبالغة **2h** لـ Finance and Operations.

4. يُكمل فني الخدمة أمر العمل ويسجل الوقت المستخدم البالغ 1.5 ساعة.

    قيمة **حالة النظام** هي **مفتوح - مكتمل**.

    - **خط الإنتاج:** الكمية المقدرة = 5ea، الكمية المستخدمة = 6ea، حالة الخط = الكمية المستخدمة، الموزعة = نعم
    - **خط الخدمة:** الكمية المقدرة = 2h، الكمية المستخدمة = 1.5h، حالة الخط = المستخدمة

    في هذا المثال، تتم مزامنة قيمة **الكمية المستخدمة** البالغة **6** وقيمة **الكمية المستخدمة** للخدمة والبالغة **1.5h** لـ Finance and Operations.

## <a name="sales-order-origin-and-status"></a>أصل أمر المبيعات وحالته

### <a name="sales-origin"></a>أمر التوريد الأصلي

لتتبع أوامر المبيعات في Finance and Operations التي تنشأ من أوامر العمل، يمكنك إنشاء أصل مبيعات حيث يتم تعيين الخيار **مهمة نوع الأصل** إلى **نعم** وحقل **نوع أصل المبيعات** إلى **تكامل أمر العمل**.

بشكل افتراضي، يقوم التعيين بتحديد أصل المبيعات لنوه أصل مبيعات **تكامل أمر العمل** لجميع أوامر المبيعات التي تم إنشاؤها من أوامر العمل. قد يفيد هذا السلوك عندما تتعامل مع أمر المبيعات في Finance and Operations. يجب أن تتأكد من أنه لا تتم مزامنة أوامر المبيعات التي تنشأ من أوامر العمل مرة أخرى لـ Field Service كأوامر عمل.

للحصول على مزيد من التفاصيل حول كيفية إنشاء إعداد أصل المبيعات الصحيح في Finance and Operations، راجع قسم "إعداد الشروط المسبقة والتعيين" في هذا الموضوع.

### <a name="status"></a>الحالة

عند إنشاء أمر المبيعات من أمر عمل، يظهر حقل **حالة أمر العمل الخارجي** في علامة التبويب **الإعداد** في عنوان أمر المبيعات. يعرض هذا الحقل حالة النظام من أمر العمل في Field Service، للمساعدة في تعقب حالة أمر العمل الذي تمت مزامنة لأوامر المبيعات في Finance and Operations. كما يمكن لهذا الحقل أن يساعد مستخدم Finance and Operations على تحديد الوقت الذي ينبغي فيه شحن أمر المبيعات أو فوترته.

قد يشتمل حقل **حالة أمر العمل الخارجي** على القيم التالية:

- مفتوح - مجدول
- مفتوح - قيد التقدم
- مفتوح - مكتمل
- مُقفل - مرحّل

## <a name="field-service-crm-solution"></a>حل Field Service CRM

لدعم التكامل بين Field Service وFinance and Operations، يُتطلب وجود وظيفة إضافية من حل Field Service CRM. يشتمل الحل على التغييرات التالية.

### <a name="work-order-entity"></a>كيان أمر العمل

لقد تمت إضافة حقل **لدى عرض الأسعار منتجات تتم المحافظة عليها خارجيًا فقط‬‏‫** إلى كيان **أمر العمل** ويظهر في الصفحة. ويُستخدم لتعقب ما إذا كان أمر عمل يتكون من المنتجات التي تم الاحتفاظ بها خارجيًا بالكامل. يتكون أمر عمل من المنتجات التي تم الاحتفاظ بها خارجيًا عندما تم الاحتفاظ بجميع المنتجات ذات الصلة في Finance and Operations. يساعد هذا الحقل على ضمان عدم محاولة المستخدمين مزامنة أوامر العمل التي تشتمل على منتجات غير معروفة لـ Finance and Operations.

### <a name="work-order-product-entity"></a>كيان منتج أمر العمل

- لقد تمت إضافة حقل **أمر لديه عرض أسعار منتجات تم الاحتفاظ بها خارجيًا فقط‬‏‫** إلى كيان **منتج أمر العمل** ويظهر في الصفحة. يُستخدم لتعقب ما إذا كان يتم الاحتفاظ بمنتج أمر العمل باستمرار في Finance and Operations. يساعد هذا الحقل على ضمان عدم محاولة المستخدمين مزامنة منتجات أوامر العمل غير المعروفة لـ Finance and Operations.
- لقد تمت إضافة حقل **حالة نظام العنوان‬‏‫** إلى كيان **منتج أمر العمل** ويظهر في الصفحة. يتم استخدامه لتعقب حالة نظام أمر العمل باستمرار ويساعد على ضمان التصفية الصحيحة عند مزامنة منتجات أوامر العمل لـ Finance and Operations. عند تعيين عوامل التصفية في مهام التكامل، يتم أيضًا استخدام **حالة نظام العنوان** لتحديد ما إذا كان يجب أن تتم مزامنة القيم المقدرة أو المستخدمة.
- يعرض حقل **مبلغ الوحدة المفوتر** المبلغ الذي تمت فوترته لكل وحدة فعلية يتم استخدامها. يتم حساب القيمة باعتبارها قيمة **المبلغ الإجمالي** مقسمة على قيمة **الكمية الفعلية**. يتم استخدام الحقل للتكامل مع الأنظمة التي لا تدعم القيم المختلفة للكمية المستخدمة والكمية المفوترة. لا يظهر هذا الحقل في واجهة المستخدم (UI). 
- يتم حساب حقل **مبلغ الخصم المفوتر** كقيمة **مبلغ الخصم** بالإضافة إلى التقريب من حساب قيمة **مبلغ الوحدة المفوتر**. يتم استخدام هذا الحقل للتكامل ولا يظهر في واجهة المستخدم.
- يخزن حقل **الكمية العشرية** القيمة من حقل **الكمية** كرقم عشري. يتم استخدام هذا الحقل للتكامل ولا يظهر في واجهة المستخدم. 
- تتم إعادة تعيين القيمة الواردة في الحقول **المستخدمة** إلى **0** (صفر) إذا تم تغيير قيمة **حالة الخط** لمنتج أمر العمل من **مستخدم** إلى **مقدر**. يساعد هذا التغيير على منع حدوث المواقف التي يتم فيها إدخال كمية مستخدمة عن طريق الخطأ للمزامنة عندما تكون قيمة **حالة الخط** هي **مقدر** وعند تعيين الخيار **تم التوزيع** إلى **لا**.

### <a name="work-order-service-entity"></a>كيان خدمة أمر العمل

- لقد تمت إضافة حقل **أمر لديه عرض أسعار منتجات تم الاحتفاظ بها خارجيًا فقط‬‏‫** إلى كيان **خدمة أمر العمل** ويظهر في الصفحة. يُستخدم لتعقب ما إذا كان يتم الاحتفاظ بخدمة أمر العمل باستمرار في Finance and Operations. يساعد هذا الحقل على ضمان عدم محاولة المستخدمين مزامنة خدمات أوامر العمل غير المعروفة لـ Finance and Operations.
- لقد تمت إضافة حقل **حالة نظام العنوان‬‏‫** إلى كيان **خدمة أمر العمل** ويظهر في الصفحة. يتم استخدامه لتعقب حالة نظام أمر العمل باستمرار ويساعد على ضمان التصفية الصحيحة عند مزامنة خدمات أوامر العمل لـ Finance and Operations. عند تعيين عوامل التصفية في مهام التكامل، يتم أيضًا استخدام **حالة نظام العنوان** لتحديد ما إذا كان يجب أن تتم مزامنة القيم المقدرة أو المستخدمة.
- يخزن حقل **المدة بالساعات** القيمة من حقل **المدة** بعد تحويل هذه القيمة من دقائق إلى ساعات. يتم استخدام هذا الحقل للتكامل ولا يظهر في واجهة المستخدم.
- يخزن حقل **المدة المقدرة بالساعات** القيمة من حقل **المدة المقدرة** بعد تحويل هذه القيمة من دقائق إلى ساعات. يتم استخدام هذا الحقل للتكامل ولا يظهر في واجهة المستخدم.
- يخزن حقل **مبلغ الوحدة المفوتر** المبلغ الذي تمت فوترته لكل وحدة فعلية يتم استخدامها. يتم حساب القيمة باعتبارها قيمة **المبلغ الإجمالي** مقسمة على قيمة **الكمية الفعلية**. يتم استخدام هذا الحقل للتكامل مع الأنظمة التي لا تدعم القيم المختلفة للكمية المستخدمة والكمية المفوترة. لا يظهر الحقل في واجهة المستخدم (UI).
- يتم حساب حقل **مبلغ الخصم المفوتر** كقيمة **مبلغ الخصم** بالإضافة إلى التقريب من حساب قيمة **مبلغ الوحدة المفوتر**. يتم استخدام هذا الحقل للتكامل ولا يظهر في واجهة المستخدم.
- حقل **أمر الخط الخارجي** عبارة عن رقم أمر بند سالب محسوب يمكن استخدامه في أنظمة خارجية يتم فيها تجميع بنود خدمة ومنتج أمر العمل. يعمل هذا الحقل على تمكين منتجات أوامر العمل التي تم إدخالها للاشتمال على أرقام بنود موجية وخدمات أوامر العمل للاشتمال على أرقام بنود سالبة. يتم حساب قيمة هذا الحقل باعتبارها قيمة **أمر بند** مضروبة في -1. لا يظهر هذا الحقل في واجهة المستخدم (UI).
- تتم إعادة تعيين القيمة الواردة في الحقول **المستخدمة** إلى **0** (صفر) إذا تم تغيير قيمة **حالة الخط** من **مستخدم** إلى **مقدر** لسبب ما. يساعد هذا التغيير على منع حدوث المواقف التي يتم فيها إدخال كمية مستخدمة عن طريق الخطأ للمزامنة عندما تكون قيمة **حالة الخط** هي **مقدر** وتكون قيمة **حالة نظام العنوان** هي **مقفلة - مرّحلة**.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

قبل إجراء مزامنة لأوامر العمل، لا بد من تحديث الإعدادات التالية في النظام.

### <a name="setup-in-field-service"></a>الإعداد في Field Service

- تأكد من أن سلسلة الأرقام المستخدمة لأوامر العمل في Field Service لا تتداخل مع التسلسل الرقمي المستخدم لأوامر المبيعات في Finance and Operations. وبخلاف ذلك، يمكن تحديث أوامر المبيعات الموجودة بشكل غير صحيح في Field Service أو Finance and Operations.
- يجب تعيين حقل **إنشاء فاتورة أمر العمل** إلى **أبدًا**، لأنه سيتم إجراء الفوترة من Finance and Operations. انتقل إلى **Field Service**\>**الإعدادات**\>**الإدارة**\>**إعدادات Field Service**، وتأكد من تعيين حقل **إنشاء فاتورة أمر العمل** إلى **أبدًا**.

### <a name="setup-in-finance-and-operations"></a>الإعداد في Finance and Operations

يتطلب تكامل أمر العمل إعداد أصل المبيعات. يتم استخدام أصل المبيعات للتمييز أوامر المبيعات في Finance and Operations التي تم إنشاؤها من أوامر العمل في Field Service. عندما يشتمل أمر مبيعات على أصل مبيعات من نوع **تكامل أمر العمل**، يظهر حقل **حالة أمر العمل الخارجي** في عنوان أمر المبيعات. بالإضافة إلى ذلك، يساعد أصل المبيعات في ضمان تصفية أوامر المبيعات التي تم إنشاؤها من أوامر العمل في Field Service أثناء مزامنة أوامر المبيعات من Finance and Operations لـ Field Service.

1. انتقل إلى **المبيعات والتسويق** \> **الإعداد** \> **أوامر المبيعات** \> **أصل المبيعات**.
2. حدد **جديد** لإنشاء أصل مبيعات جديد.
3. في حقل **أصل المبيعات**، أدخل اسمًا لأصل المبيعات، مثل **WorkOrder**.
4. في حقل **الوصف**، أدخل وصفاً، مثل **أمر عمل Field Service**.
5. حدد خانة الاختيار **مهمة نوع الأصل**.
6. قم بتعيين حقل **نوع أصل المبيعات** إلى **تكامل أمر العمل**.
7. حدد **حفظ**.


### <a name="setup-in-data-integration"></a>إعداد تكامل البيانات

تأكد من وجود **مفتاح تكامل** لـ **msdyn_workorders**
1. اذهب إلى تكامل البيانات
2. حدد علامة التبويب **مجموعة الاتصال**
3. حدد مجموعة الاتصال المستخدمة لمزامنة أمر العمل
4. حدد علامة التبويب **مفتاح التكامل**
5. ابحث عن msdyn_workorders وتأكد أنه تمت إضافة المفتاح **msdyn_name (رقم أمر العمل)**. إذا كان غير معروض، فأضفه بالنقر فوق **إضافة مفتاح**، ثم انقر فوق **حفظ** في الجزء العلوي من الصفحة

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderheader"></a>أوامر العمل إلى أوامر المبيعات (Field Service إلى Fin and Ops): WorkOrderHeader

عامل التصفية: (msdyn_systemstatus ne 690970005) و(msdyn_systemstatus ne 690970000) و(msdynce_hasexternallymaintainedproductsonly eq true)

[![تعيين القالب في تكامل البيانات](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineestimate"></a>أوامر العمل إلى أوامر المبيعات (Field Service إلى Fin and Ops): WorkOrderServiceLineEstimate

عامل التصفية: (msdynce_headersystemstatus ne 690970005) و(msdynce_headersystemstatus ne 690970000) و(msdynce_orderhasexternalmaintainedproductsonly eq true) و (msdyn_linestatus eq 690970000) و (msdynce_headersystemstatus ne 690970004)

[![تعيين القالب في تكامل البيانات](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineused"></a>أوامر العمل إلى أوامر المبيعات (Field Service إلى Fin and Ops): WorkOrderServiceLineUsed

عامل التصفية: (msdynce_headersystemstatus ne 690970005) و(msdynce_headersystemstatus ne 690970000) و(msdynce_orderhasexternalmaintainedproductsonly eq true) و((msdyn_linestatus eq 690970001) أو (msdynce_headersystemstatus eq 690970004))

[![تعيين القالب في تكامل البيانات](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineestimate"></a>أوامر العمل إلى أوامر المبيعات (Field Service إلى Fin and Ops): WorkOrderProductLineEstimate

عامل التصفية: (msdynce_headersystemstatus ne 690970005) و(msdynce_headersystemstatus ne 690970000) و(msdynce_orderhasexternalmaintainedproductsonly eq true) و (msdyn_linestatus eq 690970000) و(msdynce_headersystemstatus ne 690970004) و(msdyn_allocated eq true)

[![تعيين القالب في تكامل البيانات](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineused"></a>أوامر العمل إلى أوامر المبيعات (Field Service إلى Fin and Ops): WorkOrderProductLineUsed

عامل التصفية: (msdynce_headersystemstatus ne 690970005) و(msdynce_headersystemstatus ne 690970000) و(msdynce_orderhasexternalmaintainedproductsonly eq true) و((msdyn_linestatus eq 690970001) أو (msdynce_headersystemstatus eq 690970004) أو (msdyn_allocated ne true))

[![تعيين القالب في تكامل البيانات](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)

