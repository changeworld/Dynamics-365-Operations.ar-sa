--- 
title: "إعداد توجيه موقع لتخزين أمر الشراء"
description: "يوضح لك هذا الإجراء كيفية إعداد موجه موقع بسيط."
author: ShylaThompson
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4bb4af7cb7aff101a8b9e6162823515f63b12886
ms.openlocfilehash: 98ce3ad38dddda33be5466490fcd39d81251679c
ms.contentlocale: ar-sa
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>إعداد توجيه موقع لتخزين أمر الشراء

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح لك هذا الإجراء كيفية إعداد موجه موقع بسيط. ينشئ المثال المعروض توجيه موقع سيتم استخدامه لتحديد مكان وضع الأصناف التي تم استلامها لأمر شراء. يمكنك تشغيل دليل المهام هذا مع البيانات المذكورة باستخدام شركة بيانات العرض التوضيحي USMF. الشروط المسبقة: تحتاج لإنشاء رمز إرجاع. في هذا الإجراء نستخدم رمز إرجاع يُسمى "إعادة تسمية". إذا كنت تقوم بإنشاء توجيه موقع في البيانات الخاصة بك، فستحتاج إلى إعداد إدارة المستودعات المتقدمة للمستودع والأصناف.  هذا الإجراء مخصص لمدير المستودعات.

1. انتقل إلى إدارة المستودعات > إعداد > توجيهات الموقع‬.
2. في الحقل "نوع أمر العمل"، حدد "أوامر الشراء".

## <a name="create-a-location-directive-header"></a>إنشاء رأس توجيه موقع
1. انقر فوق "جديد".
2. في الحقل "الرقم التسلسلي"، أدخل رقمًا.
    * هذا هو التسلسل الذي تتم به معالجة توجيه الموقع لنوع العمل المحدد. يمكنك أيضا تعديل التسلسل، إذا لزم الأمر.  
3. في حقل "الاسم"، اكتب قيمة.
    * هذا هو المعرف الفريد لهذا التوجيه.  
4. في الحقل "نوع العمل"، حدد "تم وضعه".
    * حدد نوع العمل المطلوب تنفيذه. بالنسبة للتوجيه الذي يكون نوع أمر العمل به هو أمر الشراء، ستكون القيمة "تم وضعه" هي القيمة المدعومة فقط.  
5. في الحقل "الموقع"، اكتب قيمة.
6. في الحقل "المستودع"، اكتب قيمة.
    * اترك رمز التوجيه فارغًا.  تُستخدم رموز التوجيهات لربط بند أمر عمل من النوع "تم وضعه" بتوجيه محدد. بالنسبة لأوامر الشراء، يتم حل موقع آخر بند أمر عمل من النوع "تم وضعه" قبل تحديد قالب العمل. ولذلك لا يمكن ربط البند الأخير من قالب عمل بتوجيه محدد.   
7. في الحقل "رمز الإرجاع"، اكتب قيمة.
    * يقيد رمز الإرجاع استخدام توجيه الموقع، بحيث لا يُستخدم توجيه الموقع إلا إذا أدخل عامل المستودع هذه القيمة المحددة أثناء تسجيل الصنف باستخدام جهاز محمول.  
8. انقر فوق "حفظ".

## <a name="edit-the-query-for-directive"></a>قم بتحرير الاستعلام للتوجيه
1. انقر فوق "تحرير استعلام".
    * يقتصر استخدام هذا التوجيه بالفعل على استخدامه للأصناف المسجلة في المستودع الذي قمت بتحديده، ومع رمز الإرجاع الذي قمت بتحديده. ويمكنك إضافة قيود أخرى باستخدام الاستعلام.  
2. انقر فوق "موافق".

## <a name="add-directive-lines"></a>إضافة بنود توجيه
1. انقر فوق "جديد".
    * هذا هو التسلسل الذي تتم به معالجة بنود توجيهات الموقع لنوع العمل المحدد. يمكنك أيضا تعديل التسلسل، إذا لزم الأمر.  
2. في الحقل "من الكمية"، أدخل رقمًا.
    * وهذه أقل كمية يصلح لها بند التوجيه هذا.  
3. في الحقل "إلى الكمية"، أدخل رقمًا.
4. في الحقل "الوحدة"، اكتب قيمة.
    * الوحدة التي يتم التعبير بها عن "من الكمية و"إلى الكمية". إذا تركتَ هذا الحقل فارغًا، سيتم استخدام وحدة المخزون "من الصنف".  
5. في الحقل "تحديد موقع الكمية"، حدد خيارًا.
    * بلا، أو كمية لوحة الترخيص: الكمية المسجلة بكل لوحة ترخيص. الكمية الموحدة: الكمية بأكملها التي تم تسجيلها. الكمية المتبقية: الكمية التي سيتم تسجيلها من بند أمر الشراء. الكمية المتوقعة: إجمالي الكمية المحددة في بند أمر الشراء.  
6. حدد خانة اختيار "التقييد حسب الوحدة" أو قم بإلغاء تحديدها.
    * إذا حددت هذا الخيار، وحددتَ الوحدة في الصفحة "التقييد حسب الوحدة"، فلن يتاح وضع أصناف في الموقع خلاف الأصناف ذات وحدة القياس هذه. على سبيل المثال، إذا كانت وحدة القياس هي البالتات، فلن يُمكن وضع أصناف في الموقع المحدد خلاف الأصناف التي تم قياسها بالبالتات.  
7. حدد خانة الاختيار "المساح بالتقسيم" أو قم بإلغاء تحديدها.
    * ويتيح هذا للتوجيه تقسيم الكمية عبر مواقع متعددة.  
8. انقر فوق "حفظ".

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>تقييد بند التوجيه على وحدة خاصة
1. انقر فوق "التقييد حسب الوحدة".
    * لا يتوفر هذا الزر إلا عندما الضغط على Save (حفظ) بعد تحديد خانة الاختيار "تقييد حسب الوحدة".  
2. في الحقل "الوحدة"، اكتب قيمة.
3. قم بإغلاق الصفحة.

## <a name="add-a-location-directive-action-line"></a>إضافة بند إجراء توجيه موقع
1. انقر فوق "جديد".
    * هذا هو التسلسل الذي تتم به معالجة بنود إجراءات توجيهات الموقع لنوع العمل المحدد. يمكنك أيضا تعديل التسلسل، إذا لزم الأمر.  
2. في حقل "الاسم"، اكتب قيمة.
    * هذ هو المعرف الفريد لإجراء التوجيه هذا.  
3. في الحقل "استخدام موقع ثابت"، حدد خيارًا.
    * المواقع الثابتة وغير الثابتة: تصلح جميع المواقع غير الثابتة بالإضافة للمواقع الثابتة الخاصة بالمنتج، ضمن النطاق المحدد في الاستعلام.  موقع المنتج الثابت فقط: تصلح المواقع الثابتة للمنتج، وتشترك جميع متغيرات المنتج في نفس المجموعة من المواقع الثابتة. الموقع الثابت فقط لمتغيرات المنتج: تصلح المواقع الثابتة المحددة لكل متغير منتج فقط.  
4. في الحقل "الإستراتيجية"، حدد خيارًا.
    * تدعم أوامر العمل من نوع الدعم أمر الشراء الإستراتيجيات التالية: بلا: يُوضع الصنف في الموقع الأول الذي تم العثور عليه. تجميع: يُوضع الصنف في موقع تتوفر به أصناف مماثلة بالفعل. موقع فارغ بلا عمل وارد: يُوضع الصنف في الموقع الأول الفارغ الذي تم العثور عليها. يعتبر الموقع فارغًا إذا لم يوجد به مخزون فعلي وعند عدم وجود عمل وارد متوقع.  
5. انقر فوق "حفظ".

## <a name="edit-the-query-for-directive-action-line"></a>تحرير الاستعلام لبند إجراء التوجيه
1. انقر فوق "تحرير استعلام".
2. وانقر فوق إضافة.
3. في الحقل "الحقل"، اكتب "معرف ملف تعريف الموقع".
    * في هذا المثال، سوف نقيد المواقع المحتملة باستخدام معرف ملف تعريف موقع.  
4. في الحقل "المعايير"، اكتب قيمة.
5. انقر فوق "موافق".
    * يمكنك الاستمرار في إضافة بنود التوجيهات وإجراءات التوجيهات حتى تتم تغطية جميع السيناريوهات المحتملة في المستودع.  


