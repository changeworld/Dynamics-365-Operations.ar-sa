---
title: "نظرة عامة على فواتير الموردين"
description: "توفر هذه المقالة معلومات عامة حول فواتير المورد. فواتير المورد هي طلبات دفع للمنتجات والخدمات التي تم تلقيها. بإمكان فواتير المورد أن تمثل فاتورة في مقابل خدمات مستمرة، أو يمكنها أن تستند إلى أوامر شراء لأصناف وخدمات معينة."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a6b18343337ca7058c5027c8d4325c4301f1abed
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-invoices-overview"></a>نظرة عامة على فواتير الموردين

[!include[banner](../includes/banner.md)]


توفر هذه المقالة معلومات عامة حول فواتير المورد. فواتير المورد هي طلبات دفع للمنتجات والخدمات التي تم تلقيها. بإمكان فواتير المورد أن تمثل فاتورة في مقابل خدمات مستمرة، أو يمكنها أن تستند إلى أوامر شراء لأصناف وخدمات معينة. 

<a name="vendor-invoices"></a>فواتير المورد
---------------

فاتورة المورد من أمر شراء عبارة عن فاتورة يتم إنتاجها عند تلقي المنتجات أو الخدمات وفقًا لأمر شراء الذي تم وضعه مع أحد الموردين. ‏‫وتحتوي فاتورة المورد على رأس، وبند واحد أو أكثر للأصناف أو الخدمات. وتُكمل فاتورة المورد الدورة من أمر الشراء حتى إيصال استلام المنتجات حتى فاتورة المورد.‬ 

وعلى الرغم من أن بعض فواتير المورد متصلة بأمر شراء، إلا أن فواتير المورد يمكنها أن تتضمن البنود التي لا تتوافق مع بنود أمر الشراء. كما يمكنك إنشاء فواتير المورد غير المرتبطة بأي أمر شراء. وقد تمثل فواتير المورد هذه الخدمات الجارية، مثل فاتورة الأداء، ولا يكون لديك مرجع أمر شراء عند إضافتها. 

هناك عدة طرق لإدخال فاتورة مورد:

-   ‏‫يتيح لك سجل فواتير المورد إمكانية إدخال الفواتير التي لا تشير إلى أمر شراء بسرعة بحيث يمكنك استحقاق المصروفات. وباستخدام دفتر يومية اعتماد فواتير المورد، يمكنك تحديد هذه الفواتير وترحيلها إلى رصيد المورد لإلغاء الاستحقاق.‬
-   ويتيح لك دفتر يومية فاتورة المورد إدخال الفواتير التي لا تشير إلى أمر شراء بسرعة، في خطوة واحدة.
-   ومع وعاء فواتير المورد، يتيح لك سجل فواتير المورد إدخال الفواتير لاستحقاق المصروفات بشكل سريع. ويمكنك فتح أوامر الشراء المرتبطة لاحقاً لترحيل فاتورة في مقابل حساب المصروفات.
-   تتيح لك صفحتا **فواتير المورد المفتوحة** و**فواتير المورد المعلقة** إنشاء فواتير المورد من أوامر الشراء المؤكدة.

توفر المناقشة التالية المزيد من المعلومات حول كيفية استخدام صفحة **فواتير المورد المفتوحة** أو **فواتير المورد المعلقة** لإنشاء فاتورة مورد من أمر شراء.

## <a name="understanding-invoice-line-quantities"></a>استيعاب كميات بند الفاتورة
عندما تفتح فاتورة مورد من أمر شراء مرتبط، يتم إنشاء بنود فاتورة من أمر الشراء. وبشكل افتراضي، يتم اخذ الكميات من كمية إيصال استلام المنتجات. ومع ذلك، يمكنك استخدام أي من السلوكيات الافتراضية التالية:

-   **كمية الاستلام الآن‬** – استخدم هذا الخيار للشحنات الجزئية. يتم أخذ القيمة الافتراضية الموجودة في حقل **الكمية** من حقل كمية **الاستلام الآن** في أمر الشراء.
-   **الكمية المطلوبة** – استخدم هذا الخيار للشحنات الكاملة. يتم أخذ القيمة الافتراضية الموجودة في حقل **الكمية** من حقل الكمية **المطلوبة** في أمر الشراء.
-   **الكمية المسجلة** – استخدم هذا الخيار إذا كان الصنف يتطلب التسجيل، مثلما ما هو محدد في صفحة **مجموعات نماذج الصنف**. تعد القيمة الافتراضية في حقل **الكمية** كمية التحديث الفعلية التي سبق تسجيلها.
-   **كمية إيصال استلام المنتجات** – استخدم هذا الخيار إذا تم استلام إيصال منتج بالفعل للأمر. يتم أخذ القيمة الافتراضية في حقل **الكمية** من الكمية الإجمالية لإيصالات استلام المنتجات المتاحة.
-   **الكمية والخدمات المسجلة** – استخدم هذا الخيار إذا تم تسجيل الكميات في دفاتر يومية الوصول للأصناف المخزنة أو الأصناف التي لم يتم تخزينها. هذا الخيار يشمل الخدمات أيضًا، بغض النظر عما إذا كانت مسجلة.

وفي حالة استخدام الكيان القانوني لمطابقة الفاتورة، يمكنك عرض نتائج مطابقة الكمية في عمود **مطابقة كمية إيصال استلام المنتجات**. كما يمكنك استخدام أمر قائمة **تفاصيل المطابقة** في علامة التبويب **مراجعة** لعرض نتائج مطابقة الكمية.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>إضافة بند لم يكن موجودًا في أمر الشراء
يمكنك إضافة بند جديد لم يكن موجودًا في أمر الشراء إلى فاتورة المورد. ويجب عليك تحديد فئة التدبير أو رقم صنف. ويمكنك فيما بعد إضافة الكميات والأسعار والمبالغ إلى البند. سيتم تضمين البند فقط في سياسات مطابقة إجماليات الفواتير.

## <a name="submitting-a-vendor-invoice-for-review"></a>إرسال فاتورة مورد للمراجعة
يمكن أن تستخدم مؤسستك عمليات سير العمل لإدارة عملية مراجعة فواتير الموردين. قد تكون مراجعة سير العمل مطلوبة من أجل رأس القائمة، أو بند الفاتورة، أو كليهما. تنطبق عناصر التحكم في سير العمل على الرأس أو البند، اعتمادًا على موضع التركيز عندما تنقر فوق عنصر التحكم. وبدلاً من الزر **ترحيل** سترى الزر **إرسال** الذي يمكنك استخدامه لإرسال فاتورة المورد من خلال عملية المراجعة.

## <a name="matching-vendor-invoices-to-product-receipts"></a>مطابقة فواتير الموردين بإيصالات استلام المنتجات
يمكنك إدخال معلومات عن فواتير الموردين وحفظها، كما يمكنك مطابقة بنود الفاتورة مع بنود إيصال استلام المنتجات. يمكنك أيضًا مطابقة الكميات الجزئية للبند. 

يمكنك إنشاء فاتورة مورد استنادًا إلى أصناف بند إيصال استلام المنتجات التي تم استلامها حتى الآن، حتى ولو كان جميع الأصناف الخاصة بأمر شراء معين لم يتم استلامها بعد. على سبيل المثال، يمكنك استخدام هذا الخيار إذا أرسل المورد فاتورة واحدة كل شهر تغطي جميع التسليمات التي يرسلها المورد خلال ذلك الشهر. يمثل كل إيصال استلام منتجات تسليمًا جزئيًا أو كاملاً للأصناف الواردة في أمر الشراء. 

وعند ترحيل الفاتورة، يتم تحديث كمية **باقي الفاتورة** لكل صنف بإجمالي الكميات المستلمة من إيصالات استلام المنتجات المحددة. وإذا كان كلُّ من كمية **باقي الفاتورة** وكمية **تسليم البافي**لكافة الأصناف في أمر الشراء تساوي 0 (صفر)، فإنه يتم تغيير حالة أمر الشراء إلى **مفوتر**. وإذا كانت كمية **باقي الفاتورة** لا تساوي 0 (صفر)، فإن حالة أمر الشراء تبقى دون تغيير، ويمكن إدخال الفواتير الإضافية لها.

يفترض هذا الخيار أن يتم ترحيل إيصال استلام منتجات واحد على الأقل لأمر الشراء. تعتمد فاتورة المورد على إيصالات الاستلام هذه ويعكس الكميات من خلالها. وتعتمد المعلومات المالية للفاتورة على المعلومات التي يتم إدخالها عند ترحيلك للفاتورة.

## <a name="working-with-multiple-invoices"></a>العمل مع العديد من الفواتير

يمكنك العمل بفواتير متعددة في وقت واحد وترحيلها جميعًا في وقت واحد. إذا كان يجب عليك إنشاء فواتير متعددة، فاستخدم صفحة **فواتير المورد المعلقة**. وإذا كان يجب عليك ترحيل وطباعة فواتير موردين متعددة، فاستخدم صفحة دفتر يومية اعتماد الفاتورة. وإذا كنت تستخدم دفتر يومية اعتماد الفاتورة، فيجب ترحيل إيصال استلام منتج واحد على الأقل لطلب الشراء وترحيل فاتورة لأمر الشراء في سجل الفاتورة. ترد المعلومات المالية الخاصة بالفاتورة من الفاتورة التي تم ترحيلها في السجل.




