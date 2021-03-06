--- 
title: "تحديد تبعية تكوينات التقارير الإلكترونية على مكونات أخرى"
description: "لإتمام هذه الخطوات، يجب عليك أولاً إكمال الخطوات الموجودة في دليل المهام، \"التقارير الإلكترونية - إدارة تكوينات تعيينات النموذج‬\"، ويجب أن يكون لديك حق الوصول إلى Microsoft Dynamics Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 18eb8de7c851e5477d93a00f744fe56929c43ca2
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a>تحديد تبعية تكوينات التقارير الإلكترونية على مكونات أخرى

[!include [task guide banner](../../includes/task-guide-banner.md)]

لإتمام هذه الخطوات، يجب عليك أولاً إكمال الخطوات الموجودة في دليل المهام، "التقارير الإلكترونية - إدارة تكوينات تعيينات النموذج‬"، ويجب أن يكون لديك حق الوصول إلى Microsoft Dynamics Lifecycle Services (LCS).

يظهر هذا الإجراء كيفية تصميم تكوين التقارير الإلكترونية وتحديد تبعيته بالنسبة إلى مكونات البرامج الأخرى، بحيث يمكنك المساعدة في ضمان تنزيل التكوين بشكل صحيح إلى إصدار معين من Microsoft Dynamics 365 for Finance and Operations. في هذا المثال، ستقوم بإنشاء تكوينات التقارير الإلكترونية المطلوبة للشركة النموذجية Litware, Inc. 

تم تخصيص هذا الإجراء للمستخدمين الذين تم تعيين دور مسؤول النظام أو مطور التقارير الإلكترونية لهم. يمكن تنفيذ الخطوات في أي شركة، نظرًا لمشاركة تكوينات التقارير الإلكترونية بين الشركات. 

1. انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.
    * تأكد من أن شجرة التكوينات تحتوي على تكوين "عينة نموذج البيانات‬" والأصناف التابعة. وبخلاف ذلك، أكمل الخطوات الواردة في دليل المهام، التقارير الإلكترونية - إدارة تكوينات تعيينات النموذج‬، ثم ابدأ هذا الدليل من جديد.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>تحديد تبعية تكوينات التقارير الإلكترونية بالنسبة إلى مكونات أخرى
1. في الشجرة، قم بتوسيع "عينة نموذج البيانات"
2. في الشجرة، حدد "عينة نموذج البيانات\تعيين نموذجي".
    * لقد حددنا الإصدار التمهيدي من تكوين تعيين النموذج "تعيين نموذجي". سوف نقوم الآن بتعريف تبعيته بالنسبة إلى مكونات البرامج الأخرى. تعتبر هذه الخطوة مطلبًا أساسيًا للتحكم في تنزيل إصدار التكوين هذا من مستودع التقارير الإلكترونية وأي استخدام إضافي لهذا الإصدار.   
3. قم بتوسيع أو طي مقطع "المتطلبات الأساسية‬".
    * لاحظ أن مجموعة المتطلبات الأساسية‬ "عمليات التنفيذ" أضيفت بشكل تلقائي في هذه المرحلة. تحتوي هذه المجموعة على مكون المتطلبات الأساسية الذي يشير إلى تكوين نموذج البيانات وتم وضع علامة "التنفيذ" عليه. تشير هذه العلامة إلى أن تكوين التعيين "تعيين نموذجي" يعتبر بمثابة تنفيذ لنموذج البيانات تكوين تعيين النموذج لهذا التعيين النموذجي يعتبر تنفيذ لنموذج البيانات "عينة نموذج البيانات‬". سيقوم هذا المكون بإجبار التقارير الإلكترونية على تنزيل تكوين تعيين النموذج، "تعيين نموذجي" من مستودع التقارير الإلكترونية كلما تم تنزيل تكوين النموذج، "عينة نموذج البيانات‬".   
4. انقر فوق "تحرير".
    * يمكن تحديد تبعية واحدة من الإصدار الحالي لتكوين من مكون برامج باستخدام تعريف نوع المكون، وإما إصدار المكون أو مجموعة من إصدارات المكونات.  
    * يمكن تجميع التبعيات المطلوبة معًا. عند تحديد نوع التجميع "كل ما يلي‬"، يتم اعتبار شرط التبعية لهذه المجموعة على أنه شرط تمت تلبيته عندما تتم تلبية كل شرط تبعية بالنسبة إلى هذه المجموعة والمجموعة التابعة. عند تحديد نوع التجميع "أحد ما يلي‬‬"، يتم اعتبار شرط التبعية لهذه المجموعة على أنه شرط تمت تلبيته عندما تتم تلبية شرط تبعية واحد على الأقل بالنسبة إلى هذه المجموعة والمجموعة التابعة.   
5. انقر فوق "جديد".
6. حدد مكون المتطلبات الأساسية للمنتج.
7. حدد Microsoft Dynamics 365 for Operations (1611).
8. في حقل "الإصدار"، اكتب '[7.1.1541.3036,8)'.
    * [7.1.1541.3036,8)  
    * يتم تقييم التبعيات التي تقوم بإدخالها عندما يتم تنزيل هذا التكوين من مستودع التقارير الإلكترونية. سيتم تنزيل إصدار التكوين هذا من مستودع التقارير الإلكترونية عندما يكون الإصدار 1 من "عينة نموذج البيانات" إما موجودًا في مكانه أو تم تنزيله بشكل مسبق. إذا تم تنزيله بشكل مسبق، فيجب إكماله في Finance and Operations، في الإصدار 7.1.1541.3036 أو إصدار لاحق، ولكن دون تجاوز الإصدار الرئيسي 8.   
9. انقر فوق "حفظ".
10. قم بإغلاق الصفحة.
11. انقر فوق "تغيير الحالة".
12. انقر فوق "مكتمل".
13. انقر فوق "موافق".
14. في الشجرة، حدد "عينة نموذج البيانات\تعيين نموذجي (بديل)".
15. انقر فوق "تحرير".
16. انقر فوق "جديد".
17. حدد مكون المتطلبات الأساسية للمنتج.
18. حدد Microsoft Dynamics AX 7.0 RTW.
19. في حقل "الإصدار"، اكتب '[7.0.1265.3015,7.1)'.
    * [7.0.1265.3015,7.1)  
    * سيتم تقييم التبعيات عندما يتم تنزيل هذا التكوين من مستودع التقارير الإلكترونية. سيتم تنزيل إصدار التكوين هذا من مستودع التقارير الإلكترونية عندما يكون الإصدار 1 من "عينة نموذج البيانات" إما موجودًا في مكانه أو تم تنزيله بشكل مسبق. إذا تم تنزيله بشكل مسبق، فيجب إكماله في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، في الإصدار 7.0.1265.3015 أو إصدار لاحق، ولكن دون تجاوز الإصدار الثانوي 1.   
20. انقر فوق "حفظ".
21. قم بإغلاق الصفحة.
22. انقر فوق "تغيير الحالة".
23. انقر فوق "مكتمل".
24. انقر فوق "موافق".

## <a name="configure-the-er-repository"></a>تكوين مستودع التقارير الإلكترونية
1. قم بإغلاق الصفحة.
2. انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.
    * افتح قائمة بمستودعات التقارير الإلكترونية لموفر التقارير الإلكترونية الحالي، شركة Litware, inc.  
3. في القائمة، قم بوضع علامة للصف المحدد.
4. انقر فوق "المستودعات".
5. انقر فوق "إظهار عوامل التصفية".
6. أدخل قيمة عامل التصفية "LCS" في حقل "اسم النوع" باستخدام عامل التصفية "يحتوي".
    * إذا كان مستودع LCS مسجلاً لموفر التقارير الإلكترونية الحالي، فيمكنك تخطي الخطوات المتبقية في هذه المهمة الفرعية. إذا لم يكن مستودع LCS مسجلاً، فعليك استكمال الخطوات المتبقية.   
7. انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.
8. في الحقل "نوع مستودع التكوين"، أدخل "LCS".
9. انقر فوق إنشاء مستودع.
10. في الحقل "المشروع"، أدخل قيمة أو حددها.
    * حدد مشروع LCS المطلوب من البحث في حقل "المشروع".  
11. انقر فوق "موافق".
12. قم بإغلاق الصفحة.

## <a name="upload-configurations-to-lcs"></a>تحميل تكوينات إلى LCS
1. انقر فوق "تكوينات إعداد التقارير‬".
2. في الشجرة، حدد "عينة نموذج البيانات"
3. حدد الإصدار المكتمل لهذا التكوين.
4. انقر فوق "تغيير الحالة".
5. انقر فوق "مشاركة".
6. انقر فوق "موافق".
    * تم تحميل الإصدار 1 من تكوين النموذج هذا إلى LCS عن طريق استخدام مشروع LCS لمستودع التقارير الإلكترونية الذي تم تكوينه في السابق.   
7. في الشجرة، قم بتوسيع "عينة نموذج البيانات"
8. في الشجرة، حدد "عينة نموذج البيانات\تعيين نموذجي".
9. حدد الإصدار المكتمل لهذا التكوين.
10. انقر فوق "تغيير الحالة".
11. انقر فوق "مشاركة".
12. انقر فوق "موافق".
    * تم تحميل الإصدار 1.1 من تكوين تعيين النموذج هذا إلى LCS عن طريق استخدام مشروع LCS لمستودع التقارير الإلكترونية الذي تم تكوينه في السابق.   
13. في الشجرة، حدد "عينة نموذج البيانات\تعيين نموذجي (بديل)".
14. حدد الإصدار المكتمل لهذا التكوين.
15. انقر فوق "تغيير الحالة".
16. انقر فوق "مشاركة".
17. انقر فوق "موافق".
    * تم تحميل الإصدار 1.1 من تكوين تعيين النموذج هذا إلى LCS عن طريق استخدام مشروع LCS لمستودع التقارير الإلكترونية الذي تم تكوينه في السابق.   

## <a name="evaluate-er-configuration-dependencies"></a>تقييم تبعيات تكوين التقارير الإلكترونية
    * سوف نحذف التكوينات التي تم إنشاؤها من النظام ونعيد تنزيلها مرة أخرى من مستودع LCS.  
1. في الشجرة، حدد "عينة نموذج البيانات\تعيين نموذجي".
2. انقر فوق حذف.
3. انقر فوق نعم.
4. في الشجرة، حدد "عينة نموذج البيانات\تعيين نموذجي (بديل)".
5. انقر فوق حذف.
6. انقر فوق نعم.
7. في الشجرة، حدد "عينة نموذج البيانات\تنسيق نموذجي".
8. انقر فوق حذف.
9. انقر فوق نعم.
10. في الشجرة، حدد "عينة نموذج البيانات"
11. انقر فوق حذف.
12. انقر فوق نعم.
13. قم بإغلاق الصفحة.
    * افتح قائمة بمستودعات التقارير الإلكترونية لموفر التقارير الإلكترونية الحالي، شركة Litware, inc.  
14. انقر فوق "المستودعات".
15. انقر فوق "إظهار عوامل التصفية".
16. أدخل قيمة عامل التصفية "LCS" في حقل "اسم النوع" باستخدام عامل التصفية "يحتوي".
17. انقر فوق "فتح".
18. في الشجرة، حدد "عينة نموذج البيانات"
    * لاحظ أنه يمكنك مراجعة تقييم لما إذا تمت تلبية شروط المتطلبات الأساسية لكل إصدار من تكوينات التقارير الإلكترونية للمستودع الحالي. لعرض هذا التقييم، انقر فوق "التحقق من المتطلبات الأساسية‬".   
19. انقر فوق "التحقق من المتطلبات الأساسية".
20. انقر فوق "استيراد".
21. انقر فوق نعم.
22. قم بإغلاق الصفحة.
23. قم بإغلاق الصفحة.
24. قم بإغلاق الصفحة.
25. انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.
26. في الشجرة، قم بتوسيع "عينة نموذج البيانات"
    * لاحظ أنه قد تم تحميل تكوين تعيين النموذج "تعيين نموذجي" جنبًا إلى جنب مع تكوين نموذج البيانات المحدد. يتم تنزيل الملفين معًا نظرًا لتحديد "التعيين النموذجي" على أنه ينفذ نموذج البيانات المحدد، ولأنه ينطبق على Finance and Operations. لم يتم تنزيل تكوين "تعيين نموذجي (بديل)‬" نظرًا لعدم تلبية الشرط المتعلق بإصدار التطبيق المطلوب.   
    * إذا قمت بتسجيل الدخول إلى Dynamics 365 for Finance and Operations, Enterprise edition وتسجيل الموفر نفسه والوصول إلى مشروع LCS نفسه وتنزيل تكوين نموذج البيانات نفسه، فسيتم تنزيل تكوين "تعيين نموذجي (بديل)‬"، في حين سيتم تخطي تكوين "تعيين نموذجي".  


