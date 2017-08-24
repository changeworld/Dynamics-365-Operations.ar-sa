--- 
title: "إعداد التعبئة في حاويات"
description: "يصف هذا الإجراء كيفية جعل تعبئة الأحمال في إدارة المستودع عملية تلقائية."
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 38b60098daa0389af596920682c30dcd9b17a7fb
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-containerization"></a>إعداد التعبئة في حاويات

[!include[task guide banner](../../includes/task-guide-banner.md)]

يصف هذا الإجراء كيفية جعل تعبئة الأحمال في إدارة المستودع عملية تلقائية. تعمل التعبئة التلقائية في الحاويات على إنشاء الحاويات وانتقاء العمل للشحن عند معالجة موجة ويمكن تقسيم بنود العمل إلى الكميات التي تناسب الحاويات. يساعد ذلك العاملين في المستودع على انتقاء الأصناف مباشرة في الحاوية المختارة. مقارنة بعملية التعبئة اليدوية، تتم أتمتة المهام مثل إنشاء حاويات وتعيين الأصناف وإغلاق الحاويات بواسطة النظام. يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF ويتم التنفيذ من قبل مدير المستودع.


## <a name="set-up-a-wave-template"></a>إعداد قالب موجة
1. انتقل إلى إدارة المستودعات > إعداد > الموجات > قوالب الموجة.
2. انقر فوق "جديد".
3. في الحقل "اسم قالب الموجة"، اكتب قيمة.
4. في الحقل "وصف قالب الموجة"، اكتب قيمة.
5. في حقل "الموقع"، أدخل قيمة أو حددها.
6. في الحقل "المستودع"، أدخل قيمة أو حددها.
7. قم بتوسيع قسم "الأساليب".
    * يسرد جزء الأساليب المحددة أساليب لنوع قالب الموجة المحدد. يجب أن يتضمن قالب الموجة أسلوب التعبئة في الحاويات.  
8. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
9. في حقل "كود خطوة الموجة"، اكتب قيمة.
    * أدخل كود خطوة الموجة للأسلوب المضاف، الذي يمكن يكون أي كود. من الممكن إضافة الأسلوب أكثر من مرة وتعيين أكواد خطوة موجة مختلفة. للقيام بذلك، حدد "قابل للتكرار" لهذا الأسلوب في صفحة أساليب معالجة الموجة.  
10. انقر فوق "حفظ".
11. قم بإغلاق الصفحة.

## <a name="set-up-a-container-type"></a>إعداد نوع حاوية
1. انتقل إلى إدارة المستودعات > إعداد > الحاويات > أنواع الحاويات.
    * يمكنك تحديد الحاويات الخاصة بك في صفحة أنواع الحاوية. يمكنك تكوين الأبعاد الفعلية للحاويات، بما في ذلك وزن الفارغ والحد الأقصى للوزن والحد الأقصى للحجم والطول والعرض والارتفاع. في هذا المثال، لدينا ثلاثة أحجام مختلفة من الصناديق.  
2. انقر فوق "جديد".
3. في حقل "كود نوع الحاوية"، اكتب قيمة.
4. في الحقل "وزن الفارغ‬"، أدخل رقمًا.
5. في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.
6. في الحقل "الحجم‬"، أدخل رقمًا.
7. في الحقل "الطول"، أدخل رقمًا.
8. في الحقل "العرض"، أدخل رقمًا.
9. في الحقل "الارتفاع"، أدخل رقمًا.
10. في وصف الحقل، اكتب قيمة.
11. انقر فوق "حفظ".
12. انقر فوق "جديد".
13. في حقل "كود نوع الحاوية"، اكتب قيمة.
14. في وصف الحقل، اكتب قيمة.
15. في الحقل "وزن الفارغ‬"، أدخل رقمًا.
16. في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.
17. في الحقل "الحجم‬"، أدخل رقمًا.
18. في الحقل "الطول"، أدخل رقمًا.
19. في الحقل "العرض"، أدخل رقمًا.
20. في الحقل "الارتفاع"، أدخل رقمًا.
21. انقر فوق "حفظ".
22. انقر فوق "جديد".
23. في حقل "كود نوع الحاوية"، اكتب قيمة.
24. في وصف الحقل، اكتب قيمة.
25. في الحقل "وزن الفارغ‬"، أدخل رقمًا.
26. في الحقل "الحد الأقصى للوزن"، أدخل رقمًا.
27. في الحقل "الحجم‬"، أدخل رقمًا.
28. في الحقل "الطول"، أدخل رقمًا.
29. في الحقل "العرض"، أدخل رقمًا.
30. في الحقل "الارتفاع"، أدخل رقمًا.
31. انقر فوق "حفظ".
32. قم بإغلاق الصفحة.

## <a name="set-up-a-container-group"></a>إعداد مجموعة حاويات
1. انتقل إلى إدارة المستودعات > إعداد > الحاويات > مجموعات الحاويات.
2. انقر فوق "جديد".
    * يمكنك إعداد مجموعات منطقية من أنواع الحاويات. لكل مجموعة، يمكنك تحديد التسلسل لحزم الحاويات به والنسبة المئوية لتعبئة الحاويات. تستخدم أبعاد حجم الصنف لتحديد ما إذا كانت مناسبة للحاوية أم لا. يتم استخدام الحاوية الأقرب إلى أبعاد حجم الصنف المستخدم. إذا كان لديك أنواع متعددة من الحاويات في مجموعة، نوصي بترتيب التسلسل حسب الحجم، حيث تكون الحاوية الأكبر أولاً، أي رقم 1 في التسلسل والحاوية الأصغر تكون الأخيرة.    
3. في الحقل "معرف مجموعة الحاوية"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. انقر فوق جديد.
6. في القائمة، قم بوضع علامة للصف المحدد.
7. في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.
8. انقر فوق جديد.
9. في القائمة، قم بوضع علامة للصف المحدد.
10. في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.
11. انقر فوق جديد.
12. في القائمة، قم بوضع علامة للصف المحدد.
13. في الحقل "نوع الحاوية"، أدخل قيمة أو حددها.
14. انقر فوق "حفظ".
15. قم بإغلاق الصفحة.

## <a name="set-up-a-container-build-template"></a>إعداد قالب إنشاء الحاوية
1. انتقل إلى إدارة المستودعات > إعداد > الحاويات > قوالب إنشاء الحاوية‬.
2. انقر فوق "جديد".
    * يعتمد قالب بناء الحاوية على عمليات التعبئة في الحاويات التي يتم إجراؤها. يعرف قالب بناء كل حاوية عملية النقل بالحاويات التي سيتم استخدامها بواسطة قالب الموجة. يسمح لك خيار تحرير الاستعلام بتحديد الشروط التي ستتم معالجة القالب المحدد بموجبها. على سبيل المثال، قد تريد تشغيل النقل بالحاويات فقط لعملاء معينين أو المنتجات أو المستودعات أو يمكنك إضافة نطاقي استعلام مقابلين إلى القالب. ويحدد حقل كود خطوة الموجة كيفية ارتباط قالب بناء حاوية بالخطوات في قالب موجة. عند تنفيذ موجة، فإنه يحدد أي قالب (قوالب) بناء الحاويات يتم استخدامه لبدء النقل بالحاويات. يحدد الحقل "نوع الاستعلام الأساسي" ما يتم حزمه وما الذي يستند إليه استعلام عامل التصفية.  
3. في القائمة، قم بوضع علامة للصف المحدد.
4. في الحقل "معرف قالب الحاوية"، اكتب قيمة.
5. في الحقل "معرف مجموعة الحاوية"، أدخل قيمة أو حددها.
6. في حقل "كود خطوة الموجة"، اكتب قيمة.
7. حدد خانة الاختيار "السماح بتقسيم الانتقاءات".
8. انقر فوق "حفظ".
9. انقر فوق قيود خلط الحاويات.
    * تسمح لك فواصل منطق الخلط بإعداد قواعد لتعبئة بنود التوزيع في حاويات. على سبيل المثال، إذا قمت بإضافة حقل رقم الصنف، عندما يتم تعيين الأصناف إلى الحاويات، فإنه سيتم إنشاء حاوية جديدة عند وجود رقم صنف جديد. وهذا سيمنع العمال من تعبئة بنود التوزيعات لعميلين مختلفين في الحاوية نفسها.  
10. انقر فوق "جديد".
11. في الحقل "جدول"، حدد خيارًا.
12. في حقل "تحديد الحقل"، أدخل قيمة أو حددها.
13. انقر فوق "موافق".

