--- 
title: "تشغيل التنسيق للقيام بالعد والجمع للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 90a0dc0fc32a448d859fbb0933ea6f12ea16668f
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="run-the-format-to-do-counting-and-summing-for-electronic-reporting-er"></a>تشغيل التنسيق للقيام بالعد والجمع للتقارير الإلكترونية (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل. يمكن تنفيذ هذه الخطوات في شركة DEMF.

لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع‬ (الجزء 3: استخدام العمليات الحسابية لإنشاء المخرجات)".

يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>اختبار هذا التكوين لإنشاء تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي
1. انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.
2. انقر فوق "تكوينات إعداد التقارير‬".
3. في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".
4. في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"
5. في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".
6. في جزء الإجراءات، انقر فوق "التكوينات".
7. انقر فوق "محددات المستخدم".
8. حدد "نعم" في حقل "تشغيل الإعدادات".
9. انقر فوق "موافق".
10. انقر فوق "تحرير".
11. حدد "نعم" في حقل "تشغيل المسودة‬".
12. انقر فوق "حفظ".
13. انتقل إلى الضريبة > الإعداد > التجارة الخارجية > معلمات التجارة الخارجية.
14. قم بتوسيع القسم "إعداد التقارير الإلكترونية".
15. حدد التكوين "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE) مع الجرد والجمع".
16. حدد التكوين "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE) مع الجرد والجمع".
17. انقر فوق "حفظ".
18. قم بإغلاق الصفحة.
19. انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.
20. انقر فوق "الإخراج".
21. انقر فوق "التقرير".
    * شغّل عملية إنشاء تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.  
22. في الحقل "من تاريخ"، قم بتعيين التاريخ على "2000/01/01".
    * حدد تاريخي البدء والانتهاء لفترة إعداد التقارير التي تشتمل على تلك الموجودة على حركات النموذج.  
23. في الحقل "إلى تاريخ"، قم بتعيين التاريخ على "2022/12/31".
    * حدد تاريخي البدء والانتهاء لفترة إعداد التقارير التي تشتمل على تلك الموجودة على حركات النموذج.  
24. في الحقل "اتجاه"، حدد "حركات الوصول".
25. حدد "نعم" في الحقل "إنشاء ملف".
26. انقر فوق "موافق".
    * راجع المخرجات المُنشأة مع بنود الملخص في النهاية.  
27. انقر فوق "جديد".
28. في القائمة، قم بوضع علامة للصف المحدد.
29. في الحقل "اتجاه"، حدد "حركات الإرسال".
30. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
31. في الحقل "السلعة"، أدخل قيمة أو حددها.
32. عيّن "الوزن" إلى"10".
33. عيّن "مبلغ الفاتورة" إلى "10000".
34. عيّن "المبلغ الإحصائي‬" إلى "10000".
35. انقر فوق "الإخراج".
36. انقر فوق "التقرير".
37. في الحقل "اتجاه"، حدد "حركات الإرسال".
38. انقر فوق "موافق".
    * راجع المخرجات المُنشأة مع بنود الملخص في النهاية. لاحظ أنه تم تغييرها بالمقارنة مع التشغيل الأول.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>تشغيل هذا التكوين في وضع التصحيح لمراجعة بيانات الجرد والجمع المجمّعة
1. انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.
2. في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".
3. في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"
4. في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".
5. في جزء الإجراءات، انقر فوق "التكوينات".
6. انقر فوق "محددات المستخدم".
7. حدد "نعم" في الحقل "تشغيل في وضع التصحيح‬".
8. انقر فوق "موافق".
9. قم بإغلاق الصفحة.
10. انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.
11. انقر فوق "الإخراج".
12. انقر فوق "التقرير".
13. انقر فوق "موافق".
14. قم بإغلاق الصفحة.
15. انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.
16. في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".
17. في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"
18. في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)\Intrastat (DE) مع الجرد والتجميع".
19. انقر فوق "سجلات التصحيح‬".
    * لاحظ أنه قد تم إنشاء سجل تصحيح لعملية تنفيذ التكوين الذي تم تحديده.  
20. انقر فوق "إرفاق".
21. انقر فوق "فتح".
    * راجع ملف XML المُنشأ الذي يحتوي على تفاصيل الجرد والتجميع التي تم جمعها أثناء تنفيذ التكوين الذي تم تحديده.  

