--- 
title: "تحديد الجرد الدوري"
description: "الجرد الدوري هو معالجة المستودع التي يمكنك استخدامها للتدقيق في أصناف المخزون الفعلي."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f0d598bbd13406b27a23dcf349f6c81e758a9e61
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="define-cycle-counting"></a>تحديد الجرد الدوري 

[!include[task guide banner](../../includes/task-guide-banner.md)]

الجرد الدوري هو معالجة المستودع التي يمكنك استخدامها للتدقيق في أصناف المخزون الفعلي. يظهر تسجيل هذه المهمة كيفية إعداد الأولوية الافتراضية لعمل الجرد وتمكين عنصر قائمة جهاز محمول لمعالجة علميات الانتقاء والجرد على حد سواء وتمكين مشغل عتبة جرد عندما يصبح الموقع فارغًا وتمكين خطة جرد دوري لصنف محدد داخل مستودع محدد. يقوم مدير المستودع عادةً بتنفيذ هذه المهام. يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو في بياناتك.


## <a name="set-the-priority-of-counting-work"></a>تعيين أولوية عمل الجرد
1. انتقل إلى إدارة المستودعات > إعداد‬ > محددات إدارة المستودعات.
2. انقر فوق علامة التبويب "الجرد الدوري".
3. في الحقل "أولوية عمل الجرد الدوري"، أدخل رقماً.
    * تقوم هذه الخطوة بتغيير أولوية عمل الجرد الدوري مقارنة بأنواع العمل الأخرى في المستودع. من خلال إدخال رقم أقل من رقم أنواع العمل الأخرى، ستقوم برفع الأولوية لعمل الجرد الدوري.  
4. انقر فوق "حفظ".
5. قم بإغلاق الصفحة.

## <a name="enable-the-mobile-device"></a>تمكين الجهاز المحمول
1. انتقل إلى إدارة المستودعات > إعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول.
2. انقر فوق "جديد".
3. في الحقل "اسم عنصر القائمة‬"، اكتب قيمة.
4. في الحقل "المسمى الوظيفي"، اكتب قيمة.
5. في الحقل "الوضع"، حدد "العمل".
6. قم بتعيين الخيار "استخدام العمل الموجود" على "نعم".
    * عند تعيين هذا الخيار إلى "نعم"، سيبحث النظام عن العمل الموجود عند استخدام عنصر قائمة الجهاز المحمول.  
7. في الحقل "موجه بواسطة"، حدد "موجه بواسطة النظام".
    * عند تحديد "توجيه النظام"، سيتم توجيه عامل المستودع لفتح العمل الموجود في فئات العمل المحددة. (سنقوم بعد ذلك بإنشاء فئات العمل هذه.)  
8. قم بتوسيع المقطع "فئات العمل‬" أو طيّه.
    * بعد ذلك، سنقوم بإنشاء فئتي عمل سيتم استخدامهما مع عنصر قائمة الجهاز المحمول هذا. عند استخدام عنصر القائمة، سيتم الاستعلام عن فئات العمل هذه، وسيتم إظهار العمل ذي الأولوية العليا للمستخدم.  
9. انقر فوق "جديد".
10. في الحقل "معرف فئة العمل"، حدد قيمة.
11. انقر فوق "جديد".
12. في الحقل "معرف فئة العمل"، حدد قيمة.
13. انقر فوق "حفظ".
14. قم بإغلاق الصفحة.
15. انتقل إلى إدارة المستودعات > إعداد > جهاز محمول > قائمة الجهاز المحمول.
16. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
17. في الشجرة، حدد "عنصر القائمة الذي قمت بإنشائه للتو".
18. انقر فوق "تحرير".
19. انقر فوق السهم لإضافة عنصر القائمة إلى القائمة.
20. انقر فوق "حفظ".

## <a name="create-a-counting-threshold"></a>إنشاء عتبة جرد
1. انتقل إلى إدارة المستودعات > إعداد > الجرد الدوري‬ > حدود الجرد الدوري‬.
2. انقر فوق "جديد".
3. في الحقل "معرف عتبة الجرد الدوري"، اكتب قيمة.
4. قم بتعيين الخيار "معالجة الجرد الدوري مباشرة" على "نعم".
5. في وصف الحقل، اكتب قيمة.
6. انقر فوق حفظ.
7. انقر فوق "تحديد المواقع".
8. في القائمة، قم بوضع علامة للصف المحدد.
9. في الحقل "المعايير"، حدد قيمة.
10. انقر فوق "موافق".
11. قم بإغلاق الصفحة.

## <a name="create-a-cycle-count-plan"></a>إنشاء خطة جرد دوري
1. انتقل إلى إدارة المستودعات > إعداد > الجرد الدوري > خطط الجرد الدوري.
2. انقر فوق "جديد".
3. في الحقل "معرف خطة الجرد الدوري"، اكتب قيمة.
4. في حقل "الوصف"، اكتب قيمة.
5. في الحقل "الحد الأقصى لعدد عمليات الجرد الدوري"، أدخل رقمًا.
6. انقر فوق حفظ.
7. انقر فوق "تحديد المواقع".
8. في القائمة، قم بوضع علامة للصف المحدد.
9. في الحقل "المعايير"، حدد قيمة.
10. انقر فوق "موافق".
11. في الحقل "الأيام الفاصلة بين عمليات الجرد الدوري"، أدخل رقمًا.
    * على سبيل المثال، إذا تم تعيين الحقل "الأيام الفاصلة بين الجرد الدوري" إلى 5، سيتم إنشاء عمل الجرد الدوري كل خمسة أيام. ومع ذلك، إذا تمت معالجة عمل الجرد الدوري في اليوم الثالث، فسيتم إنشاء عمل الجرد الدوري التالي خمسة أيام بعد معالجة آخر جرد دوري، في اليوم الثامن.  
12. انقر فوق "حفظ".
13. انقر فوق "جديد".
14. في الحقل "الرقم التسلسلي"، أدخل رقمًا.
    * الفرز هو من أصغر رقم إلى أكبر رقم. يجب أن تكون القيمة أكبر من 0 (صفر).  
15. في القائمة، قم بوضع علامة للصف المحدد.
16. في وصف الحقل، اكتب قيمة.
17. انقر فوق حفظ.
18. انقر فوق "تحديد استعلام المنتج".
19. في القائمة، قم بوضع علامة للصف المحدد.
20. في الحقل "المعايير‬"، أدخل قيمة أو حددها.
21. انقر فوق "موافق".
22. قم بإغلاق الصفحة.

