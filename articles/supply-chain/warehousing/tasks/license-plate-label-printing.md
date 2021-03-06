--- 
title: "تمكين طباعة بطاقة لوحة الترخيص"
description: "يتيح هذا الإجراء الطباعة التلقائية لبطاقة كود مسلسل لحاوية الشحن (SSCC)‬ بعد انتقاء الصنف الأخير من المخزون في عملية انتقاء المبيعات."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
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
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="enable-license-plate-label-printing"></a>تمكين طباعة بطاقة لوحة الترخيص

[!include [task guide banner](../../includes/task-guide-banner.md)]

يتيح هذا الإجراء الطباعة التلقائية لبطاقة كود مسلسل لحاوية الشحن (SSCC)‬ بعد انتقاء الصنف الأخير من المخزون في عملية انتقاء المبيعات. يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF. إذا كنت تقوم بتشغيله باستخدام بياناتك الخاصة، فيجب إعداد تسلسل رقم للوحات الترخيص. تحتاج إلى إعداد طابعة بطاقات قبل البدء في هذه المهمة. انتقل إلى إدارة المؤسسة > إعداد > طابعات الشبكة‬. في جزء الإجراءات، انقر فوق "خيارات"، ثم فوق الزر "تنزيل مثبّت عامل توجيه المستند‬". شغّل المثبت، وتأكد من أن لديك طابعة شبكة صالحة معينة إلى "نشطة" قبل متابعة الإجراء.


## <a name="set-up-the-gs1-company-prefix"></a>إعداد بادئة الشركة GS1
1. انتقل إلى إدارة المستودعات > إعداد‬ > محددات إدارة المستودعات.
2. في الحقل "بادئة الشركة GS1"، أدخل الأرقام السبعة لرقم شركتك GS1.
3. انقر فوق "حفظ".
4. قم بإغلاق الصفحة.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>إعداد تسلسل لوحة ترخيص المستخدم
1. انتقل إلى إدارة المؤسسة > التسلسلات الرقمية > التسلسلات الرقمية.
2. في الحقل "المنطقة"، حدد خيارًا.
3. في الحقل "المرجع"، حدد خيارًا.
4. في الحقل "الشركة"، اكتب قيمة.
5. في القائمة، قم بوضع علامة للصف المحدد.
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
7. وسّع مقطع "المقاطع‬".
8. انقر فوق "تحرير".
9. في جدول المقاطع، حدد الصف الأول
10. انقر فوق "إزالة".
11. انقر فوق "إزالة".
12. انقر فوق "حفظ".
13. قم بإغلاق الصفحة.

## <a name="create-the-document-route-layout"></a>إنشاء تخطيط مسار المستند
1. انتقل إلى إدارة المستودعات > إعداد > توجيه المستند > تخطيطات توجيه المستند.
    * مكّن تخطيط SSCC.  
2. انقر فوق "جديد".
3. في الحقل "معرف التخطيط"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
6. انقر فوق "إدراج في نهاية النص".
7. انقر فوق "حفظ".
8. قم بإغلاق الصفحة.

## <a name="set-up-the-document-routing"></a>إعداد توجيه المستندات
1. انتقل إلى إدارة المستودعات > إعداد > توجيه المستند > توجيه المستند.
2. في الحقل "نوع أمر العمل‬"، حدد خيارًا.
3. انقر فوق جديد.
4. في الحقل "المستودع"، اكتب قيمة.
5. في حقل "الاسم"، اكتب قيمة.
6. انقر فوق جديد.
7. في الحقل "معرف التخطيط‬"، أدخل قيمة أو حددها.
8. في حقل "الاسم"، أدخل اسم الطابعة المراد استخدامها.
9. انقر فوق "حفظ".
10. قم بإغلاق الصفحة.

## <a name="create-mobile-device-menu"></a>إنشاء قائمة الجهاز المحمول
1. انتقل إلى إدارة المستودعات > إعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول.
2. انقر فوق "جديد".
3. في الحقل "اسم عنصر القائمة‬"، اكتب قيمة.
4. في الحقل "المسمى الوظيفي"، اكتب قيمة.
5. في الحقل "الوضع"، حدد خيارًا.
6. حدد "نعم" في الحقل "استخدام العمل الموجود‬".
7. حدد "نعم" في حقل "إنشاء لوحة ترخيص‬".
8. وسّع مقطع "فئات العمل".
9. انقر فوق "جديد".
10. في الحقل "معرف فئة العمل"، اكتب قيمة.
11. انقر فوق "حفظ".
12. قم بإغلاق الصفحة.
13. انتقل إلى إدارة المستودعات > إعداد > جهاز محمول > قائمة الجهاز المحمول.
14. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
15. في الشجرة، حدد "في الشجرة، حدد عنصر القائمة الذي قمت بإنشائه من قبل".
16. انقر فوق "تحرير".
17. انقر فوق السهم لإضافة عنصر القائمة إلى القائمة.
18. انقر فوق "حفظ".
19. قم بإغلاق الصفحة.

## <a name="update-a-work-template"></a>تحديث قالب عمل
1. انتقل إلى إدارة المستودعات > إعداد > العمل > قوالب العمل.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. انقر فوق "تحرير".
4. انقر فوق جديد.
5. في القائمة، قم بوضع علامة للصف المحدد.
6. في الحقل "نوع العمل"، حدد "طباعة".
7. في الحقل "معرف فئة العمل"، أدخل قيمة أو حددها.
8. في القائمة، انقر فوق الارتباط في الصف المحدد.
9. انقر فوق "تحريك لأعلى".
10. انقر فوق "حفظ".
11. قم بإغلاق الصفحة.


