---
title: "تحديد تكاليف الإصدار التلقائي"
description: "يقدم هذا الموضوع مفهوم تحديد تكاليف الإصدار التلقائي المستخدم من أجل Lean manufacturing."
author: YuyuScheller
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 35e202db8042eaed2cfab200cc43810bba14cc87
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="backflush-costing"></a>تحديد تكاليف الإصدار التلقائي

[!include[banner](../includes/banner.md)]


يقدم هذا الموضوع مفهوم تحديد تكاليف الإصدار التلقائي المستخدم من أجل Lean manufacturing. 

يسمح تحديد تكاليف Lean manufacturing لتدفق الإنتاج باستخدام طريقة تراكم التكلفة المعروفة باسم تحديد تكاليف الإصدار التلقائي. في طريقة تحديد تكاليف الإصدار التلقائي، يتم تجميع المواد المباشرة التي يتم استهلاكها في حساب تكلفة العمل قيد التقدم‬ (WIP) لتدفق الإنتاج. ويتم استخدام مجموعة نماذج مخزون التكلفة. يتم خصم المنتجات التي تم استلامها من تدفق الإنتاج من العمل قيد التقدم وفق تكلفتها المعيارية. يكمن الاختلاف الرئيسي بين تحديد تكاليف الإصدار التلقائي والتكلفة المعيارية من ناحية عدم حساب الفروق في تحديد تكاليف الإصدار التلقائي لكل كانبان أو منتج نهائي. بدلاً من ذلك، يتم حساب الفروق في تدفق الإنتاج عبر فترة زمنية. تقدم هذه الطريقة مفهومًا محدود الفاقد بالفعل للإبلاغ عن استهلاك المواد. لا يتم الإبلاغ عن كميات المواد المنتقاة المخصصة إلى كانبان أو أمر إنتاج. بدلاً من ذلك، يتم إظهار دفعات أو وحدات كاملة لمعالجة المواد في تدفق الإنتاج. بعد أن يتم تسجيل الدفعات أو وحدات معالجة المواد كفارغة، يتم الإعلان عنها على أنها مستهلكة. قد يتم استخدام الاستهلاك المتقدم، استنادًا إلى [تكوين تدفق الإنتاج](http://ax.help.dynamics.com/en/wiki/lean-manufacturing-modeling-the-lean-organization/). قبل أن يتم استخدام الاستهلاك المتقدم، يجب على المؤسسات أن تسمح لنفسها بجعل المواد تختفي في العمل قيد التقدم لتدفق الإنتاج. تحدد تكاليف الإصدار التلقائي الدورية القيمة الفعلية للعمل قيد التقدم إلى نهاية الفترة الزمنية. يستند هذا التحديد إلى وحدة معالجة المواد الخاصة بكانبان وحالة وظيفة كانبان. يتم حساب الانحرافات بين القيم الفعلية وقيم العمل قيد التقدم الفعلية لكل مجموعة تكاليف، ويتم حساب الأصناف وعرضها كفروق.

## <a name="configuring-backflush-costing"></a>تكوين تحديد تكاليف الإصدار التلقائي
لتمكين تحديد التكاليف، يجب إكمال الإعداد التالي:

-   **إعداد حسابات العمل قيد التقديم لمجموعة الإنتاج وتدفق الإنتاج.** يتم تحديد حسابات العمل قيد التقديم لتدفق الإنتاج في مجموعة الإنتاج. يقوم تدفق الإنتاج لتحديد تكاليف الإصدار التلقائي بحساب الفروق كاختلاف في قيمة العمل قيد التقدم، قبل تشغيل تحديد تكاليف الإصدار التلقائي لكل تدفق إنتاج وبعد تشغيله. لذلك، نوصي بأن تقوم بإنشاء حساب عمل قيد التقدم لكل تدفق إنتاج.
-   **تعيين فئة تكلفة لمجموعة الموارد.** يجب تعيين فئة تكلفة لفئة وقت التشغيل لخلية العمل. لتحديد الفروق حسب النشاط، يجب عليك إنشاء فئة تكلفة لكل خلية عمل. لا تؤخذ في الاعتبار فئات التكلفة للإعداد والكمية في تحديد تكاليف lean manufacturing. ويتم تجاهل حسابات العمل قيد التقدم في مجموعة الموارد في تحديد تكاليف الإصدار التلقائي. بالنسبة إلى الأنشطة المتعاقد عليها من الباطن، لا حاجة إلى فئة تكلفة. يتم استخدام بدلاً منها مجموعة التكلفة المعينة للخدمة النشطة.
-   **تعيين مجموعات التكلفة‬.** لتمكين تقسم مساهمة التكلفة في تدفق الإنتاج، يجب عليك تعيين مجموعات التكلفة حسب نوع مجموعة التكلفة:
    -   **مجموعة تكلفة المواد المباشرة** - تحتاج المواد المباشرة‏‎ إلى مجموعة تكلفة تحدد فئة المادة لتحديد التكاليف. تمكّن مجموعة التكلفة هذه طريقة عرض مجمعة للتكلفة والعمل قيد التقدم والفروق حسب المواد المباشرة.
    -   **مجموعة تكلفة التصنيع المباشر** - تلتقط مجموعة تكلفة التصنيع المباشر مساهمة التكلفة المباشرة للموارد التشغيلية في تدفق الإنتاج. تمكّن مجموعة التكلفة هذه طريقة عرض مجمعة للتكلفة والعمل قيد التقدم والفروق حسب التصنيع المباشر.
    -   **مجموعة التكلفة غير المباشرة** - تعتبر مجموعة التكلفة غير المباشرة مطلوبة لحساب مساهمة التكلفة غير المباشرة في تدفق الإنتاج. تمكّن مجموعة التكلفة هذه طريقة عرض مجمعة للتكلفة والعمل قيد التقدم والفروق حسب التكلفة غير المباشرة.
    -   **مجموعة تكلفة الإسناد المباشر** - تمكّن مجموعة التكلفة للخدمة طريقة عرض مجمعة للتكلفة المعينة والعمل قيد التقدم، وتحدد فروق التكلفة للخدمات المتعاقد عليها من الباطن.
    -   **مجموعة التكلفة لمنتج نهائي** - تحتاج المنتجات النهائية إلى مجموعة تكلفة تحدد فئة المنتج لتحديد التكاليف. تمكّن مجموعة التكلفة هذه طريقة عرض مجمعة للتكلفة والعمل قيد التقدم والفروق حسب فئة المنتج. يتم حساب التكلفة المعيارية للمنتجات باستخدام حساب التكلفة الذي يستند إلى قائمة مكونات الصنف، وإما تدفق الإنتاج وقواعد كانبان أو المسار.

### <a name="costing-sheet"></a>كشف التكاليف

يصمم كشف التكاليف بنية التكلفة للشركة وهو مبني بواسطة مجموعات التكلفة لتصنيف التكلفة. يتميز كشف التكاليف بأشكال متعددة. وهو يعرض معلومات التكلفة وفقًا للبنية المصممة فيه. في كشف التكاليف، يمكنك أيضًا تحديد المعادلة المستخدمة لحساب التكلفة غير المباشرة. بإمكان معادلة الحساب أن تستند إلى الكميات أو الوزن أو الحجم أو القيمة.

-   **تعريف إصدار التكاليف.** في إصدار التكاليف، تحدد الشركة كيف يجب أن تتم المحافظة على التكلفة. ويمكن أن يحتوي إصدار التكاليف على مجموعة من سجلات التكاليف المعيارية أو على مجموعة من سجلات التكاليف المخططة، وهذا يتوقف على نوع التكاليف الذي تم تعيينه لإصدار التكاليف. يجب أن يعتمد إصدار التكاليف المستخدم لتحديد تكاليف Lean manufacturing استنادًا إلى التكلفة المعيارية.
-   **تعيين مجموعة نماذج المخزون للمنتجات الصادرة.** يجب تعيين كافة المنتجات المرتبطة بتدفق الإنتاج إلى مجموعة نماذج المخزون التي تستخدم مجموعة نماذج المخزون **التكلفة المعيارية**. يتم الحفاظ على التكلفة المعيارية لكل موقع وتاريخ تنشيط. بالنسبة إلى أصول المنتجات، يمكن تحديد مجموعة نماذج المخزون إذا كانت تكلفة الصيانة تتم لكل متغير أو أصل منتج.
-   **الخدمات المتعاقد عليها من الباطن هي بطبيعتها خدمات غير مسجلة في المخزون.** ليس لدى الأنشطة المتعاقد عليها من الباطن مجموعة نماذج مخزون. لحساب تكاليف أنشطة متعاقد عليها من الباطن بشكل صحيح، يجب أن تتأكد من أن نشاط الخدمة ينتمي إلى مجموعة نماذج مخزون حيث تم تعيين سياسة المخزون إلى **منتج مخزن = False**.

بالنسبة إلى المنتجات المخرجة، يتطلب حساب التكلفة الذي يستند إلى تدفق الإنتاج المحافظة على تكلفة معيارية للخدمات المرتبطة بالأنشطة المتعاقد عليها من الباطن. يتم استخدام مجموعة التكلفة المعينة للخدمات لتحديد تباينات التكلفة للنشاط المتعاقد عليه من الباطن.

## <a name="cost-calculation-for-lean-manufacturing"></a>حساب تكلفة Lean manufacturing
للمنتجات التي تم توفيرها خارج تدفق الإنتاج، يجب أن يستند حساب قائمة مكونات الصنف على إصدار مسار أو تدفق إنتاج. يقوم حساب قائمة مكونات الصنف بحساب تكلفة المنتج والتصنيف ذي الصلة للموارد والمواد المطلوبة لإنشاء المنتج. تتم عملية الخصم من حساب العمل قيد التقدم لتدفق الإنتاج باستخدام تصنيف المنتج حسب مجموعة الأصناف‬ ومجموعة التكلفة.

### <a name="calculation-that-is-based-on-the-production-flow"></a>عملية الحساب التي تستند إلى تدفق الإنتاج

يُعتبر Lean manufacturing لـ Microsoft Dynamics 365 for Operations مستقلاً عن المسارات. بإمكان حساب التكلفة للمنتجات التي تم توفيرها من تدفق إنتاج أن يستند إلى تدفق الإنتاج نفسه. قبل إجراء عملية الحساب، يجب إنشاء قاعدة كانبان تقوم بتوريد المنتج من خارج تدفق الإنتاج. إذا كان من الممكن توفير منتج من تدفقات إنتاج متعددة في نفس الموقع في تاريخ الحساب، يمكنك تحديد تدفق الإنتاج من حساب قائمة مكونات الصنف. في صفحة **تدفق الإنتاج الافتراضي**، يمكنك تكوين تدفق إنتاج افتراضي لكل صنف. في حالة وجود عدة قواعد كانبان لنفس المنتج في نفس تدفق الإنتاج الذي يكون نشطًا في تاريخ عملية الحساب، تحدد عملية الحساب أول قاعدة كانبان نشطة لعملية الحساب.

### <a name="calculation-that-is-based-on-the-route"></a>عملية الحساب التي تستند إلى المسار

تُعتبر عملية الحساب التي تستند إلى مسار صالحة مثل عملية الحساب التي تستند إلى تدفق إنتاج. ومع ذلك، لا تستخدم عملية الحساب التي يستند إلى مسار تحديد تكاليف Lean manufacturing. من المفترض أن يستخدم المسار متطلبات الموارد لمجموعات الموارد. لتجنب الفروق النظامية، من المفترض أن يستخدم أيضًا نفس خلايا العمل، أو على الأقل نفس فئات التكلفة. مرة أخرى، يجب تجنب فئات التكلفة‬ للإعداد والكمية. فهي لا تساعد في حساب التكلفة في تصنيف أكثر دقة مقارنة بتحديد تكاليف الإصدار التلقائي من أجل Lean manufacturing. لتحديد الخيار الذي يجب استخدامه لحساب التكلفة (تدفق إنتاج أو مسار)، خذ بعين الاعتبار نتائج تصنيف التكاليف. الإصدار الذي يأتي أقرب إلى الحقيقة وينتج عنه إجمالي فروق أقل هو الخيار الأفضل. في بيئة Lean manufacturing حيث يتم توفير منتج بواسطة قاعدة كانبان واحدة وتدفق إنتاج واحد، تكون عملية الحساب التي تستند إلى تدفق الإنتاج أكثر دقة على الأرجح. بالنسبة إلى منتج يمكن توفيره من خلال Lean manufacturing وأوامر الإنتاج في الموقع نفسه أو منتج قد تكون لديه تدفقات إنتاج متعددة أو قواعد كانبان متعددة في التدفق نفسه، قد تكون عملية الحساب أكثر دقة إذا استندت إلى إصدار مسار تم بناؤه خصيصًا لحساب التكلفة، وليس الإنتاج. يجب استخدام عملية حساب تدفق الإنتاج لحساب المنتجات التي تتضمن التعاقد من الباطن. في Microsoft Dynamics 365 for Operations، تستخدم نماذج التكلفة الخاصة بالتعاقد من الباطن من خلال أوامر الإنتاج والتعاقد من الباطن في Lean manufacturing أسلوبين مختلفين. يقدم Lean manufacturing نوع مجموعة تكلفة جديدًا، وهو **الإسناد المباشر**، لحساب الخدمات المتعاقد عليها من الباطن.

## <a name="material-consumption"></a>استهلاك المادة
عند استهلاك المواد من المخزون إلى العمل قيد التقدم، تُضاف تكلفة المواد إلى العمل قيد التقدم كتكلفة معيارية فعلية لمجموعة تكلفة. تحدث هذه العملية في الحالات التالية:

-   يتم ترحيل إصدارات كانبان لبنود انتقاء كانبان التي تحدّث المخزون.
-   يتم إكمال مهام التحويل التي تحدّث المخزون عند الانتقاء وليس الاستلام (نقل المواد من المخزون إلى العمل قيد التقدم).

## <a name="receiving-products-from-the-production-flow"></a>استلام المنتجات من تدفق الإنتاج
يتم استلام المنتجات من تدفق الإنتاج في الحالات التالية:

-   يتم إكمال مهام المعالجة التي تم فيها تعيين **تحديث المخزون عند الاستلام** إلى **نعم**.
-   يتم إكمال مهام التحويل التي تحدّث المخزون عند الاستلام، ولكن تم فيها تعيين الخيار **تحديث المخزون عند الانتقاء** إلى **لا** (تحويل من عمل قيد التقدم إلى المخزون). يتيح هذا الخيار إمكانية استقبال أي منتجات من خارج تدفق إنتاج بشكل مستقل عن تكوين قائمة مكونات الصنف والمسار. تتبع العملية التدفقات الفعلية فقط. يُعد هذا الخيار مناسبًا على وجه التحديد لاستلام منتجات ثانوية أو منتجات مساعدة أو خردة من خارج تدفق الإنتاج ولتصحيح رصيد تكلفة عمل قيد التقدم في تدفق الإنتاج وفقًا لذلك.

يتم خصم المنتجات التي تم استلامها من تدفق الإنتاج من العمل قيد التقدم.

## <a name="products-in-wip"></a>المنتجات في عمل قيد التقدم.
يسمح لك نموذج العمل قيد التقدم لـ Lean manufacturing في Microsoft Dynamics 365 for Operations باستخدام حالة وحدة معالجة مواد كانبان لإدارة المواد والمنتجات غير النهائية والمنتجات النهائية التي تعد جزءًا من عمل قيد التقدم.

-   **معيَّن‬** - بإمكان كانبان أن يتضمن مواد مستهلكة تم حسابها في العمل قيد التقدم.
-   **مُستَلم‬** - إذا أشار كانبان إلى نشاط أخير حيث تم تعيين الخيار **تحديث المخزون عن الاستلام** إلى **لا**، فهو يمثل وحدة معالجة مواد كاملة لمنتج أو منتج غير نهائي لم يتم تسجيله في المخزون.

لاحظ أن المواد في العمل قيد التقدم لا تكون مرئية في النظرة العامة على المخزون الفعلي. ومع ذلك، فهي مرئية في النظرة العامة على كمية كانبان.

## <a name="consuming-products-in-wip"></a>استهلاك المنتجات في العمل قيد التقدم
يتم استهلاك المنتجات في العمل قيد التقدم عند إفراغ وحدات معالجة مواد كانبان المناظر. لا تنتج إشارة كانبان فارغ حركة نشطة لتحديد التكاليف، ولكنها ستكون سارية عند تشغيل تحديد تكاليف الإصدار التلقائي في المرة التالية. سيتوقف حساب وحدات معالجة مواد كانبان الفارغة على أنها متاحة، وبالتالي سيتم حسابها على أنها مستهلكة ضمن الفترة الزمنية.

### <a name="automatic-empty-registration"></a>تسجيل التفريغ التلقائي

يمكن تعيين الكانبانات المجدولة أو كانبانات الأحداث إلى تسجيل التفريغ التلقائي في قاعدة كانبان:

-   **عند استلام وحدات معالجة المواد‬** - بشكل افتراضي، يتم الإعلان عن المواد كمستهلكة، بالنسبة إلى الكانبانات المجدولة، عند اكتمال آخر وظيفة من وظائف كانبان. لكانبانات الكمية الثابتة، هذا الخيار مستحسن فقط لكانبانات السلة الواحدة، لأنها ترجع البطاقة إلى مصدر الطلب كلما تم استلام كانبان في الوجهة النهائية.
-   **عند تسجيل متطلبات المصدر** - هذا الخيار يتوفر فقط لكانبانات الأحداث وهو الخيار الافتراضي لها. فيما يتعلق بالعمل قيد التقدم، يكون هذا الخيار مفيدًا للاحتفاظ بالعمل قيد التقدم نظيفًا، إذ يتم تفريغ كانبانات المكونات في العمل قيد التقدم تلقائيًا، وبالتالي استهلاكها من العمل قيد التقدم، عند تحضير كانبان الأصل.

في الختام، يمكن تعيين وحدات معالجة مواد كانبان (= قيد المعالجة)، مستلمة (= كامل)، أو فارغة. لا يوجد إفراغ جزئي. لذلك، لتمكين التسجيل الدقيق للاستهلاك، من المهم تحديد كميات المنتجات الخاصة بكانبان كي تكون أقل من الاستهلاك لكل فترة زمنية. بالنسبة إلى المنتجات التي تم نقلها إلى المتجر في مجموعات كبيرة تغطي أيام أو أسابيع الطلب، فيجب ألا يتم استهلاكها إلى العمل قيد التقدم. بدلاً من ذلك، يجب الاحتفاظ بهذه المنتجات في المخزون.

## <a name="backflush-costing"></a>تحديد تكاليف الإصدار التلقائي
يجب تشغيل تحديد تكاليف الإصدار التلقائي لتقييم العمل قيد التقدم بشكل دوري وإنتاج حالة نهاية الفترة التي تقوم بحساب الفروق في تكاليف المواد والعمالة والتكاليف غير المباشرة. يتم ترحيل الفروق المحتسبة إلى حسابات الفروق. في عملية تحديد تكاليف الإصدار التلقائي، يتم استخدام كافة تدفقات الإنتاج للكيان القانوني في عملية تشغيل الدُفعة نفسها. عند تشغيل تحديد تكاليف الإصدار التلقائي في دُفعة، قد تكون المعالجة متعددة العمليات الجزئية حسب تدفق الإنتاج. يتم تعريف فترة الإصدار التلقائي بتاريخ انتهاء. لا يمكنك ترحيل الحركات الجديدة إلى تاريخ عند تشغيل حساب تحديد تكاليف الإصدار التلقائي. يجب ألا تقوم إطلاقًا بتشغيل تحديد تكاليف الإصدار التلقائي للتاريخ الحالي قبل انتهاء اليوم بشكل فعلي. تنفذ عملية تحديد تكاليف الإصدار التلقائي الخطوات التالية.

1.  تحديد الكميات غير المستخدمة في تدفق الإنتاج اعتبارًا من تاريخ انتهاء الفترة. بعد تشغيل تحديد تكاليف الإصدار التلقائي، يمكنك عرض الكميات غير المستخدمة في وقت تشغيل التكلفة في مربع حوار **الكميات غير المستخدمة**.
2.  حساب الاستخدام المحقق الصافي لتدفق الإنتاج عبر الفترة الزمنية.
3.  مسح العمل قيد التقدم من استهلاك الموارد المحققة والمنتجات.
4.  حساب فروق الإنتاج إلى التكلفة المعيارية للفترة. **بالنسبة إلى المكونات المستهلكة للفترة:**
    -   التحديث المالي للكميات المحققة الصافية للمواد التي استهلكها تدفق الإنتاج عبر الفترة. يعالج النظام أولاً أمر ما يرد أولاً يصرف أولاً (FIFO)‬ على حركات المخزون الفردية لإجراء تحديث مالي للحركات المحدّثة فعليًا لتدفق الإنتاج، حتى يتم الوصول إلى الكميات المحققة الصافية للفترة.
    -   يتم تقسيم الحركات ماليًا لتعيين الكميات المستهلكة الفعلية.
    -   تبقى الكميات غير المستخدمة في العمل قيد التقدم في تدفق الإنتاج في الحالة المحدّثة الفعلية.

    **بالنسبة إلى الكميات المكتملة للمنتجات للفترة:**
    -   إجراء تحديث مالي لحركات المخزون للكميات المكتملة للفترة.

    **بالنسبة إلى تكلفة التحويل:**
    -   يتم إجراء تحديث مالي لحركات تكلفة التحويل (حركات المسار) التي تم تسجيلها للفترة.
    -   يتم إجراء تحديث مالي لكل تكاليف التصنيع المباشرة. يتم تجميع كافة وظائف معالجة كانبان المكتملة خلال الفترة.
    -   يتم حساب كافة التكاليف غير المباشرة للمواد المستهلكة أثناء الفترة ويتم خصمها من العمل قيد التقدم. يتم ترحيل التكلفة غير المباشرة المتبقية كفرق.

5.  حساب فروق الإنتاج إلى التكلفة المعيارية. يتم حساب الفرق لكل مجموعة تكلفة.





