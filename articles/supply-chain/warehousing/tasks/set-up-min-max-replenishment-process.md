--- 
title: "إعداد الحد الأدنى والحد الأقصى لعملية التزويد"
description: "يوضح هذا الإجراء كيفية إعداد عملية تزويد جديدة تستخدم استراتيجية الحد الأدنى/الحد الأقصى لعملية التزويد."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a>إعداد الحد الأدنى والحد الأقصى لعملية التزويد

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إعداد عملية تزويد جديدة تستخدم استراتيجية الحد الأدنى/الحد الأقصى لعملية التزويد. عندما يصبح المخزون أقل من الحد الأدنى، سيتم إنشاء العمل لتزويد الموقع. يوضح الإجراء أيضًا كيفية استخدام مواقع انتقاء ثابتة للسماح بإعادة التخزين إذا كان المخزون أقل من مستوى الحد الأدنى، وكيفية تمكين عملية التزويد للتشغيل بانتظام باستخدام وظيفة مجموعة. وعادة ما تُنفذ هذه المهام عن طريق مدير مستودع. يمكنك تشغيل هذا الإجراء في شركة بيانات العرض التوضيحي USMF باستخدام قيم المثال في الملاحظات أو يمكن تشغيله على البيانات الخاصة بك. إذا كنت تستخدم البيانات الخاصة بك، فتأكد من حصولك على مستودع يتم تمكينه لعمليات إدارة المستودع.


## <a name="create-a-fixed-picking-location"></a>إنشاء موقع انتقاء ثابت
1. انتقل إلى إدارة المستودعات > إعداد > المستودع > المواقع الثابتة.
    * هذه مهمة اختيارية للحد الأدنى والحد الأقصى لعملية التزويد‬، ولكن إذا كنت تستخدم موقع انتقاء ثابت، فهذا يسمح بتزويد المخزون حتى إذا كان أقل من مستوى الحد الأدنى، لأن النظام يمكنه تحديد الأصناف التي بحاجة إلى التزويد، حتى إذا لم يكن هناك أي أصناف متبقية.  
2. انقر فوق "جديد".
3. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
    * إذا كنت تستخدم USMF، يمكنك تحديد الصنف A0001.  
4. في حقل "الموقع"، أدخل قيمة أو حددها.
    * إذا كنت تستخدم USMF، يمكنك تحديد "الموقع 2".  
5. في الحقل "المستودع"، أدخل قيمة أو حددها.
    * إذا كنت تستخدم الصنف، فيمكنك تحديد المستودع 24.  
6. في الحقل "الموقع"، أدخل قيمة أو حددها.
    * إذا كنت تستخدم USMF، فإنه يمكنك تحديد "CP-003".  
7. قم بإغلاق الصفحة.

## <a name="create-a-replenishment-location-directive"></a>إنشاء توجيه موقع التزويد
1. انتقل إلى إدارة المستودعات > إعداد > توجيهات الموقع‬.
    * يتم استخدام توجيهات الموقع لتحديد المكان الذي ينبغي أن يتم انتقاء الأصناف منه في عملية التزويد.  
2. في الحقل "نوع أمر العمل‬"، حدد "تزويد".
3. انقر فوق "جديد".
4. في حقل "الاسم"، اكتب قيمة.
5. في الحقل "نوع العمل"، حدد "انتقاء".
6. في حقل "الموقع"، أدخل قيمة أو حددها.
    * إذا كنت تستخدم USMF، يمكنك تحديد "الموقع 2".  
7. في الحقل "المستودع"، أدخل قيمة أو حددها.
    * إذا كنت تستخدم الصنف، فيمكنك تحديد المستودع 24.  
8. انقر فوق "حفظ".
9. انقر فوق "جديد".
10. في القائمة، قم بوضع علامة للصف المحدد.
11. في الحقل "إلى الكمية"، أدخل رقمًا.
    * على سبيل المثال، يمكنك تعيينه على 9999.  
12. حدد خانة الاختيار "السماح بالتقسيم".
    * إذا قمت بتحديد هذا الخيار، فستسمح عملية إنشاء العمل بعمل كميات بنود ليتم تقسيمها خلال مواقع متعددة.  
13. انقر فوق "حفظ".
14. انقر فوق "جديد".
15. في القائمة، قم بوضع علامة للصف المحدد.
16. في حقل "الاسم"، اكتب قيمة.
17. انقر فوق "حفظ".
18. انقر فوق "تحرير استعلام".
    * يمكنك تحرير هذا الاستعلام لإضافة قيود حيث يمكن تحديد المخزون في عملية التزويد. على سبيل المثال، قد يكون هذا المخزون يجب استخدامه فقط من المنطقة الكبيرة من المستودع.  
19. انقر فوق "موافق".
20. قم بإغلاق الصفحة.

## <a name="create-a-replenishment-work-template"></a>إنشاء قالب عمل التزويد
1. انتقل إلى إدارة المستودعات > إعداد > العمل > قوالب العمل.
    * يتم استخدام قالب العمل لتوجيه النظام إلى كيفية إنشاء الحد الأدنى/الحد الأقصى لعملية التزويد. وكحد أدنى، يجب أن يكون هناك بند قالب عمل للانتقاء والوضع. سيخبر قالب العمل أنه غير صالح حتى يتم كتابة جميع المعلومات اللازمة.  
2. في الحقل "نوع أمر العمل‬"، حدد "تزويد".
3. انقر فوق "جديد".
4. في الحقل "قالب العمل"، اكتب قيمة.
5. انقر فوق "حفظ".
6. انقر فوق "جديد".
7. في الحقل "نوع العمل"، حدد "انتقاء".
8. في الحقل "معرف فئة العمل"، أدخل قيمة أو حددها.
    * ينبغي أن تكون فئة العمل المتعلقة بالتزويد. إذا كنت تستخدم USMF، فحدد "تزويد".  
9. انقر فوق "جديد".
10. في القائمة، قم بوضع علامة للصف المحدد.
11. في الحقل "نوع العمل"، حدد "تم وضعه".
12. في الحقل "معرف فئة العمل"، أدخل قيمة أو حددها.
13. انقر فوق "حفظ".
14. قم بإغلاق الصفحة.

## <a name="create-a-new-replenishment-template"></a>إنشاء قالب تزويد جديد
1. انتقل إلى إدارة المستودعات > إعداد > التزويد > قوالب التزويد.
    * يتم استخدام قالب التزويد لتحديد الأصناف والكميات والموقع للتزويد.  
2. انقر فوق "جديد".
3. في الحقل "قالب التزويد"، اكتب قيمة.
    * أطلق اسمًا على القالب للإشارة إلى أنه يخص الحد الأدنى/الحد الأقصى لعملية التزويد.  
4. في وصف الحقل، اكتب قيمة.
5. حدد خانة الاختيار "السماح لطلب الموجة باستخدام الكميات غير المحجوزة".
    * بتحديد هذا الخيار، يتم تمكين تزويد طلب الموجة لاستهلاك الكميات المتعلقة بالحد الأدنى/الحد الأقصى لعملية التزويد. على سبيل المثال، قد يكون ذلك مفيدًا إذا لم تتم معالجة الحد الأدنى/الحد الأقصى لعملية التزويد على الفور، لتجنب إنشاء عمل التزويد الطلب غير الضروري.  
6. انقر فوق "جديد".
7. في الحقل "الرقم التسلسلي"، أدخل رقمًا.
8. في وصف الحقل، اكتب قيمة.
9. في القائمة، قم بوضع علامة للصف المحدد.
10. في الحقل "وحدة التزويد"، أدخل قيمة أو حددها.
    * على سبيل المثال، حدد "أجزاء". هذا الإعداد إلزامي. يسمح لك بتحديد وحدة قياس مختلفة لعمل التزويد مقارنة بالوحدة المحددة لمستويات الحد الأدنى والحد الأقصى للمخزون في هذا القالب.  
11. في الحقل "قالب العمل"، أدخل قيمة أو حددها.
    * اختر قالب العمل الذي قمت بإنشائه سابقًا.  
12. في الحقل "الحد الأدنى للكمية"، أدخل رقمًا.
    * حدد الحد الأدنى للكمية الذي يمكنه تشغل التزويد. على سبيل المثال، قم بتعيين هذا على 50. من الممكن ترك هذه المجموعة على صفر، إذا كنت تقوم بتزويد موقع ثابت وتعيين خيار "تزويد المواقع الثابتة الفارغة" على "نعم". كما نوصي بتحديد الخيار "تزويد المواقع الثابتة فقط" لأسباب تتعلق بالأداء.  
13. في الحقل "الحد الأقصى للكمية"، أدخل رقمًا.
    * على سبيل المثال، قم بتعيين هذا على 100.  
14. في الحقل "وحدة"، أدخل قيمة أو حددها.
    * قم بتعيين الوحدة الخاصة بالحد الأدنى والحد الأقصى للكميات. على سبيل المثال، قم بتعيين هذا على "أجزاء".  
15. حدد خانة الاختيار "تزويد المواقع الثابتة الفارغة".
    * حدد خانة الاختيار هذه لتزويد المواقع الثابتة عندما تكون فارغة. وإلا، فقط سيتم تزويد المواقع التي يوجد بها كميات فعلية.  
16. حدد خانة الاختيار "تزويد المواقع الثابتة فقط".
17. انقر فوق "تحديد المنتجات".
    * هذا هو المكان حيث يتم تحديد المنتجات التي ينبغي تزويدها. إذا تم تحديد الخيار "مواقع الانتقاء الثابتة"، فإنك تحتاج أيضًا إلى تحديد المواقع في هذا الاستعلام. تتوافر الاستعلامات الخاصة بمتغير بالإضافة إلى الاستعلامات الخاصة بالمنتج.  
18. حدد صف الأصناف.
19. في الحقل "المعايير"، اكتب قيمة.
    * حدد الأصناف التي يجب تزويدها في المواقع الثابتة. على سبيل المثال، اكتب أ* لتحديد كل أرقام الأصناف التي تبدأ بحرف أ.  
20. وانقر فوق إضافة.
    * أضف كيان الموقع (إلا إذا كان موجودًا بالفعل) حتى تكون قادرًا على تقييد عمل التزويد إلى مواقع انتقاء ثابتة داخل منطقة معينة من المستودع.  
21. في القائمة، قم بوضع علامة للصف المحدد.
22. قم بتعيين الحقل "الجدول" على ''المواقع".
23. في الحقل "الحقل"، حدد "معرف ملف تعريف الموقع".
24. في الحقل "المعايير‬"، أدخل قيمة أو حددها.
25. انقر فوق "موافق".
26. قم بإغلاق الصفحة.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>تعيين عملية التزويد للتشغيل كوظيفة دفعية
1. انتقل إلى إدارة المستودعات > التزويد > عمليات التزويد‬.
    * تسمح لك صفحة التزويد بإعداد التزويد لتشغيله كوظيفة دفعية أو تتطلب أن يتم بدء التشغيل يدويًا.  
2. انقر فوق "عامل التصفية".
3. في القائمة، قم بوضع علامة للصف المحدد.
4. في الحقل "المعايير‬"، أدخل قيمة أو حددها.
5. انقر فوق موافق.
6. وسّع المقطع "تشغيل في الخلفية‬‬".
7. قم بتعيين خيار "معالجة الدفعة" على "نعم".
8. انقر فوق "تكرار".
9. حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".
10. قم بتعيين نمط التكرار.
    * على سبيل المثال: حدد "أيام".  
11. انقر فوق "موافق".
12. انقر فوق "موافق".


