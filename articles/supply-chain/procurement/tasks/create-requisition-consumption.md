--- 
title: "إنشاء طلب للاستهلاك"
description: "يوضح لك هذا الإجراء عملية إنشاء طلب."
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7d8ca4e7eedea140f32e264c205b243027a06d03
ms.openlocfilehash: d1ea95d0bc283297fcedaee730e1829850f07998
ms.contentlocale: ar-sa
ms.lasthandoff: 11/20/2017

---
# <a name="create-a-requisition-for-consumption"></a>إنشاء طلب للاستهلاك

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح لك هذا الإجراء عملية إنشاء طلب. وهو يوضح لك الطرق المختلفة للبحث عن المنتجات في كتالوج التدبير وكيفية إضافة منتج غير موجودة في الكتالوج. قبل البدء في هذا الإجراء، يجب أن يكون لديك نهج شراء تم إعداد الاستهلاك به كنوع الطلب الافتراضي. يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك. لا يمكن تنفيذ الإجراء إلا بواسطة بملف تعريف مستخدم تم إعداده كعامل.  عادة ما يتم تنفيذ هذه المهمة بواسطة أحد الموظفين. سيتيح لك دور أمان التوظيف للموظف تنفيذ المهام، أو إذا كنت تستخدم USMF، يجب تسجيل الدخول إلى Alicia.


## <a name="create-a-new-requisition"></a>إنشاء طلب جديد
1. انتقل إلى التدبير والتوريد > طلبات الشراء > طلبات الشراء التي أعددتُها.
2. انقر فوق "جديد".
3. في الحقل "الاسم"، حدد اسمًا للطلب.
4. في الحقل "تاريخ الطلب، أدخل تاريخاً.
    * بشكل افتراضي، يُنسخ التاريخ المطلوب والتاريخ المحاسبي لبنود طلب الشراء. يمكن أن تتغير على مستوى البند. التاريخ المطلوب هو تاريخ التسليم المطلوب.  
5. في الحقل "تاريخ المحاسبة" أدخل تاريخاً.
    * يتم استخدام التاريخ المحاسبي لتسجيل القيد المحاسبي في دفتر الأستاذ العام، وللتحقق من صحة ما إذا كانت
الاعتمادات المالية متاحة أم لا.  
6. انقر فوق "موافق".
7. في الحقل "السبب"، انقر فوق زر القائمة المنسدلة لفتح البحث.
    * بشكل افتراضي، يظهر سبب تبرير العمل الذي قمت بتحديده لبنود طلب الشراء، ولكن يمكنك تغييره على مستوى البند.    
8. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
9. تحديد السبب
10. في حقل "التفاصيل" أدخل مبررات أكثر وصفية للطلب

## <a name="add-a-line-to-the-requisition"></a>إضافة بند إلى الطلب
1. انقر فوق "إضافة بند".
    * هناك طريقتان لإضافة بنود إلى طلب الشراء. إذا كنت تعرف رقم المنتج بالفعل أو كنت تعرف فعلا أنك تطلب منتجًا غير موجود في كتالوج المنتجات، فيمكنك إضافة البند مباشرة باستخدام الخيار "إضافة بند". والطريقة الأخرى هي استخدام "إضافة منتجات" حيث يمكنك استخدام البحث والتصفية للبحث عن أصناف في كتالوج المنتجات.    
2. انقر فوق الصف الذي قمت بإنشائه للتو.
    * الطالب هو العامل الذي قام بطلب الطلب.   
    * بشكل افتراضي، يكون الشخص الذي يجهز الطلب هو العامل الذي طلبه. يجب عليك الحصول على إذن لإعداد بند طلب نيابة عن عامل آخر. إذا كانت لديك هذه الأذونات، فسيتم عرض العاملين آخرين في هذا البحث.  
3. في الحقل "رقم الصنف" اكتب قيمة.
    * تتقيد العناصر المتوفرة للاختيار بسياسة الوصول إلى الكتالوج وكتالوج للكيان القانوني للشراء.   
4. في حقل الكمية، أدخل رقمًا.

## <a name="add-more-products-to-the-requisition"></a>إضافة المزيد من منتجات إلى الطلب
1. انقر فوق "إضافة المنتجات".
    * هذا هو الخيار الذي يمكنك من خلاله البحث عن المنتجات في كتالوج المنتجات.    
2. في الحقل "البحث عن عقدة التدبير"، اكتب الجزء الأول من اسم الفئة التي تبحث عنها، ثم انقر فوق "إدخال".
    * على سبيل المثال، اكتب حاسب.  
3. استخدم الاختصار InvokeDefaultButton.
4. استخدم عامل التصفية لتصفية قائمة المنتجات في الفئة المحددة.
5. حدد بطاقة المنتج الذين تريد إضافتها للطلب.
6. انقر فوق "إضافة إلى البنود".
7. في الحقل "الكمية"، أدخل رقمًا.
8. في الحقل "البحث عن عقدة التدبير"، اكتب الجزء الأول من اسم الفئة التي تبحث عنها، ثم انقر فوق "إدخال".
    * على سبيل المثال، اكتب قلم تم (أقلام التمييز).  
9. استخدم الاختصار InvokeDefaultButton.
10. انقر فوق "إضافة منتج غير مدرج في القائمة للبنود" لإضافة منتج غير مدرج في القائمة في كتالوج التدبير.
11. في الحقل "اسم المنتج"، اكتب قيمة.
12. في الحقل "الوحدة"، اكتب قيمة.
13. انقر فوق موافق.
14. في الحقل "وصف الصنف"، أضف وصفًا للمنتج.
15. في حقل الكمية، أدخل رقمًا.
16. في حقل "سعر الوحدة"، أدخل رقمًا.
    * إذا كنت تعرف السعر لمورد معين (السعر الذي تحدده في الحقل "حساب المورد") ثم يمكن إدخال هذا السعر   
17. في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
    * يعتمد الموردون المتوفرون في هذا الحقل على سياسات الشراء وحالة المورد بالنسبة لفئة التدبير الحالية. وكبديل لتحديد مورد هنا، يمكنك النقر فوق الزر "اقتراح مورد".    
18. في القائمة، حدد المورد الذي تريد استخدامه.
19. في الحقل "رقم الصنف الخارجي" اكتب قيمة.
    * وهذا رقم مرجعي للمنتج الذي يعرف بواسطة المورد. على سبيل المثال، قد يكون هذا رقم الصنف الخاص بالمنتج في كتالوج المورد الخاص.  
20. انقر فوق "موافق".

## <a name="distribute-amounts"></a>توزيع المبالغ
1. انقر فوق "الماليات‬".
2. انقر فوق "توزيع المبالغ".
    * توضح هذه العملية كيفية توزيع التكلفة للبند الأول بين حسابين. كما يمكن إجراء ذلك لاحقاً عندما يكون الطلب قيد المراجعة.  
3. انقر فوق "تقسيم" لإنشاء بند توزيع جديد.
4. في الحقل "حساب دفتر الأستاذ" حدد مركز التكلفة الأول الذي ينبغي أن يخصص له جزء من التكلفة.
5. حدد "بند التوزيع الآخر".
6. في الحقل "حساب دفتر الأستاذ" حدد مركز التكلفة الآخر.
7. انقر فوق "التوزيع بشكل متساوٍ".
8. قم بإغلاق الصفحة.

## <a name="view-line-details"></a>عرض تفاصيل البند
1. بدّل توسيع المقطع "تفاصيل البنود‬‬".

## <a name="submit-the-requisition"></a>إرسال الطلب
1. انقر فوق "سير العمل" لفتح مربع حوار الإسقاط‬.
2. انقر فوق تقديم.
3. قم بإغلاق الصفحة.
4. في الحقل "التعليق"، اكتب ملاحظة للموافق على الطلب.
5. انقر فوق تقديم.
6. قم بإغلاق الصفحة.
7. قم بتحديث الصفحة.


