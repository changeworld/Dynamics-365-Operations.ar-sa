--- 
title: "تحديد خلايا عمل lean manufacturing"
description: "خلية العمل عبارة عن شكل معين لمجموعات الموارد التي يمكن استخدامها في أنشطة عمليات lean manufacturing."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: dc9793bd59e59c96532549d73c56bad518fa7394
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="define-lean-manufacturing-work-cells"></a>تحديد خلايا عمل lean manufacturing

[!include[task guide banner](../../includes/task-guide-banner.md)]

خلية العمل عبارة عن شكل معين لمجموعات الموارد التي يمكن استخدامها في أنشطة عمليات lean manufacturing. يتم تحديد مواقع الإدخال والإخراج لخلايا العمل وتعريف القدرة استناداً إلى نموذج تدفق إنتاج. لمعرفة المزيد حول المفاهيم الأساسية لخلايا عمل lean manufacturing وحساب القدرات، انظر المستندات التقنية حول lean manufacturing. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="create-a-work-cell"></a>قم بإنشاء خلية عمل. 
1. انتقل إلى إدارة المؤسسة > الموارد > مجموعات الموارد.
2. انقر فوق "جديد".
3. في حقل مجموعة "الموارد"، اكتب قيمة.
    * يكون معرف خلية العمل رمزًا نظاميا عادة ويجب أن يكون فريداً للكيان القانوني.  
4. في وصف الحقل، اكتب قيمة.
    * يحتوي الوصف على اسم خلية العمل أو عنوانها.  
5. في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.
    * توجد خلية العمل في موقع معين واحد. يجب أن يكون كل من مستودع وموقع الإدخال والإخراج في هذا الموقع.  
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
7. في الحقل "وحدة الإنتاج"، انقر فوق زر القائمة المنسدلة لفتح البحث.
8. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * حدد وحدة إنتاج تنتمي إليها خلية العمل هذه.  
9. حدد خانة اختيار "خلية العمل".
    * لاستخدام مجموعة موارد كخلية عمل محدودة الفاقد، يجب تحديد خانة الاختيار "خلية العمل".  لاحظ أنه لا يمكن تغيير هذه الخاصية بعد إنشاء مجموعة الموارد.  
10. في الحقل "مستودع الإدخال"، انقر فوق زر القائمة المنسدلة لفتح البحث.
11. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * بالنسبة لمراقبة المحاسبة والمواد، تُخصص المادة المخزنة في حالة العمل في العادة لمخزن افتراضي معين. ومع ذلك، إذا أردت تزويد المواقع باستخدام عمل المستودع، يجب أن تكون المواقع جزءًا من المستودع القابل للمادة الخام.  
12. في الحقل "موقع الإدخال"، انقر فوق زر القائمة المنسدلة لفتح البحث.
13. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * لاحظ أنه بالنسبة لأحد أنشطة العمليات، يمكن تجاوز موقع الإدخال بشكل عام أو يمكن تجاوزه لمنتج معين أو متغير منتج معين بواسطة تعريف أنشطة الانتقاء التي تغذي نشاط العملية. لا يمكن التحكم بمواقع الإدخال لخلية عمل من خلال لوحة التحكم.  
14. في الحقل "مستودع الإخراج"، انقر فوق زر القائمة المنسدلة لفتح البحث.
15. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * في تدفقات الإنتاج ذات الأنشطة المتعددة أو بنود الإنتاج، يكون هذا غالبًا مستودع الإدخال لخلية العمل أو المبيعات التالية أو مستودع بضاعة بالطريق يتم تحويل المنتج إليه بعد عملية الإنتاج أو. تذكر أنه عند تصميم عمليات lean manufacturing، يتم إهدار النقل عادة كما في حالة الإبلاغ عن النقل.  
16. في القائمة، انقر فوق الارتباط في الصف المحدد.
17. في الحقل "موقع الإخراج"، انقر فوق زر القائمة المنسدلة لفتح البحث.
    * في إنتاج تدفق بأنشطة متعددة العمليات، يكون هذا غالباً هو موقع الإدخال لخلية العمل التالية.  
18. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
19. في القائمة، انقر فوق الارتباط في الصف المحدد.
20. قم بتوسيع القسم "العملية" أو طيه.
    * يجب توفير فئة وقت تشغيل لتمكين حساب التكلفة ومعالجة وظائف كانبان محدودة الفاقد.  
21. في الحقل "فئة وقت التشغيل"، انقر فوق زر القائمة المنسدلة لفتح البحث.
22. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * تُستخدم فئة التكلفة وقت التشغيل في حساب التكلفة القياسية وتحديد تكاليف الإصدار التلقائي.  
23. في القائمة، انقر فوق الارتباط في الصف المحدد.
24. قم بتوسيع القسم "التقويمات" أو طيه.
25. وانقر فوق إضافة.
26. في الحقل "التقويم"، انقر فوق زر القائمة المنسدلة لفتح البحث.
27. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * عادة ما تستخدم خلايا العمل بموقع معين نفس تقويم وقت العمل. إذا تضمنت خلايا العمل أوقات عمل فردية، فقد تحتاج لإنشاء تقويم أوقات عمل محدد لخلية العمل. لاحظ أن التقويم يجب أن يتضمن وقت عمل قياسي محدد عند استخدامه لخلية عمل محدودة الفاقد لأن تعريف القدرة يرتبط عادة بوقت العمل القياسي ليوم العمل.  
28. في القائمة، انقر فوق الارتباط في الصف المحدد.
29. ‏‫قم بتوسيع القسم "قدرة خلية العمل‬‬" أو طيّه.
30. وانقر فوق إضافة.
31. في الحقل "نموذج تدفق الإنتاج"، انقر فوق زر القائمة المنسدلة لفتح البحث.
32. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * تتطلب هذه الإجراءات نوع الإنتاجية لنموذج تدفق الإنتاج لعرض تحديد قدرة الإنتاجية.  
33. في القائمة، انقر فوق الارتباط في الصف المحدد.
34. في الحقل "فترة القدرة"، حدد خيارًا.
    * وتتضمن الخيارات:   يوم العمل القياسي - يُعبر عن القدرة بطول يوم العمل القياسي لتقويم وقت العمل لخلية العمل. بالنسبة لكل يوم، يتم تحديد وقت العمل الفعلي من التقويم وتُحسب القدرة المتاحة الفعالة على ذلك الأساس.   الأسبوع-لإتاحة قدرة أسبوعية. لا يوجد أي تعديل عن طريق وقت العمل الفعلي.   الشهر-لإتاحة قدرة شهرية. لا يوجد أي تعديل عن طريق القدرة الفعلية.   عادة، يُستخدم يوم العمل القياسي للفترات اليومية وتُستخدم القدرة الأسبوعية لفترات القدرة الأسبوعية.  
35. في الحقل "متوسط كمية الإنتاجية"، أدخل رقمًا.
    * لاحظ أنه لن يتم إعداد عملية محدودة الفاقد للقدرة القصوى الممكنة في بيئة مثالية. وبدلاً من ذلك، يجب تحديد القدرة دائماً للعمليات التي يتم تشغيلها في الحالات النموذجية.  
36. في الحقل "الوحدة ‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
37. في القائمة، انقر فوق الارتباط في الصف المحدد.
38. ResolveChanges الوحدة.

## <a name="add-a-financial-dimension"></a>إضافة بعد مالي
1. قم بتوسيع القسم "الأبعاد المالية" أو طيه.
    * لاحظ أن الأبعاد المالية المحددة بتدفق الإنتاج تتجاوز البعد المالي لخلية عمل معينة.    تعتمد الأبعاد المالية التي يمكن تحديدها على تكوين الأبعاد المالية للنظام الخاص بك. توافق الخطوات التالية مجموعة بيانات العرض في شركة USMF. عند استخدام بيانات مختلفة، قد لا تكون الخطوات قابلة للتطبيق.  
2. في الحقل "CostCenter"، انقر فوق زر القائمة المنسدلة لفتح البحث.
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * تعتمد الأبعاد التي يجب تحديدها بخلايا العمل محدودة الفاقد على تنفيذ الأبعاد المالية في نموذج محاسبة لكيان قانوني معين.  
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
5. في الحقل "ItemGroup"، انقر فوق زر القائمة المنسدلة لفتح البحث.
6. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
7. في القائمة، انقر فوق الارتباط في الصف المحدد.

## <a name="save"></a>حفظ
1. انقر فوق "حفظ".

