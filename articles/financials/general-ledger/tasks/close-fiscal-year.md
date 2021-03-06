--- 
title: "إقفال السنة المالية"
description: "ينقلك هذا الإجراء عبر عملية إقفال نهاية السنة التي تحول الأرصدة إلى سنة مالية جديدة."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4f2f1f1206f3cb3534ef93923d4945bb63814514
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="close-the-fiscal-year"></a>إقفال السنة المالية

[!include [task guide banner](../../includes/task-guide-banner.md)]

ينقلك هذا الإجراء عبر عملية إقفال نهاية السنة التي تحول الأرصدة إلى سنة مالية جديدة.


## <a name="validate-year-end-close-parameters"></a>التحقق من صحة محددات إقفال نهاية السنة
1. انتقل إلى دفتر الأستاذ العام > إعداد دفتر الأستاذ‬ > معلمات دفتر الأستاذ العام.
2. قم بتوسيع مقطع "إقفال نهاية السنة".
3. حدد "نعم" أو "لا" للخيار "حذف حركات الإقفال السنوية أثناء التحويل‬".
    * إذا تم بالفعل إقفال السنة المالية ويجري تشغيل إقفال نهاية السنة مرة أخرى، فإن هذا الإعداد يُعد مهمًا. إذا تم تعيين الخيار إلى "نعم"، فسيتم حذف الإيصال الخاص بإقفال نهاية السنة الماضية، وسيتم إنشاء إيصال جديد لكل الأرصدة الأولية للحسابات. أما إذا تم تعيينه إلى "لا"، فإن الإيصال السابق سوف يبقى وسيتم إنشاء إيصال جديد فقط لتسوية الإدخالات التي تم ترحيلها بعد إقفال نهاية السنة الماضية.  
4. حدد "نعم" أو "لا" للخيار "إنشاء حركات إقفال أثناء التحويل‬‬".
    * إذا تم تعيين الخيار إلى "نعم"، فسيتم إنشاء حركتين. يتم إنشاء إيصال واحد في السنة المالية الجاري إقفالها لكي تصبح أرصدة حسابات دفتر الأستاذ للأرباح والخسائر بقيمة صفر، ويتم إنشاء إيصال ثانٍ في السنة المالية التالية للأرصدة الأولية. أما إذا تم تعيين الخيار إلى "لا"، فسيتم إنشاء إيصال واحد في السنة المالية التالية للأرصدة الأولية.  
5. حدد "نعم" أو "لا" لتعيين حالة السنة المالية إلى "تم الإقفال بشكل دائم‬".
    * إذا تم تعيين الخيار إلى "نعم"، فسيتم تعيين حالة السنة المالية إلى "تم الإقفال بشكل دائم‬".  ونظرًا لتعذر إعادة فتح سنة مقفلة بشكل دائم، فمن المستحسن تعيين هذا الخيار إلى "لا".  
6. حدد "نعم" أو "لا" لتعيين ما إذا كان يجب إدخال رقم إيصال أثناء عملية إقفال نهاية السنة.
    * إذا تم تعيين هذا الخيار إلى "نعم"، فيجب إدخال رقم إيصال يدويًا أثناء عملية إقفال نهاية السنة. لا يستخدم تسلسل الرقمي لإنشاء رقم الإيصال هذا. من المستحسن تعيين هذا الخيار إلى "نعم".  
7. قم بإغلاق الصفحة.
8. انتقل إلى دفتر الأستاذ العام > إقفال الفترة > إقفال نهاية السنة.
9. انقر فوق "جديد" لإنشاء قالب إقفال نهاية السنة.
    * يمكن إنشاء قالب لمجموعة من الكيانات القانونية لتشغيل إقفال نهاية السنة لها. يمكنك إعادة استخدام هذا القالب سنة بعد سنة.  
10. في الحقل "اسم المجموعة"، أدخل اسمًا لقالب إقفال نهاية السنة.
11. حدد السنة المالية التي سيتم إنشاء القالب لها.
    * يمكن تجميع معًا فقط الكيانات القانونية التي تستخدم السنة المالية نفسها في قالب إقفال نهاية السنة. وهذا لأن تنفيذ إقفال نهاية السنة يتم عن طريق تحديد سنة مالية، وليس تاريخ.  
12. استخدام الاختصار لحفظ سجل.
13. انقر فوق "إضافة" لتحديد الكيانات القانونية لهذا القالب.
    * يمكن إضافة الكيانات القانونية إما بتحديد الكيانات القانونية أو بتحديد تدرج هرمي تنظيمي.  ستُضاف فقط الكيانات القانونية مع التدرج الهرمي التنظيمي حيث تم تحديد تقويم السنة المالية نفسها.  
14. حدد الكيانات القانونية أو التدرج الهرمي التنظيمي.
15. انقر فوق "موافق".
16. حدد ما إذا كان سيتم تحويل الأبعاد المالية إلى السنة المالية التالية.
    * من المستحسن تعيين هذا الخيار إلى "نعم" لحسابات الميزانية العمومية.  من شأن هذا الأمر أن يؤدي إلى المحافظة على الأبعاد المالية على الحركات التي تم ترحيلها عند إنشاء الأرصدة الأولية لحسابات الميزانية العمومية.  لحسابات الأرباح والخسائر، يمكنك اختيار المحافظة على الأبعاد المالية (‏‫إغلاق الكل‬) عندما يتم نقل الأرصدة إلى الأرباح المحتجزة‬ أو يمكنك اختيار استبدال الأبعاد المالية بقيمة بُعد مختلفة (إغلاق واحد‬). إذا اخترت "إغلاق واحد"، فيمكنك تحديد قيمة بعد محددة لكل بعد أو حتى اختيار ترك القيمة فارغة.  
17. انقر فوق "حفظ".
18. ابدأ إقفال نهاية السنة باختيار "‏‫إجراء الإقفال المالي‬" في جزء الإجراءات.
    * سيتم تشغيل إقفال نهاية السنة للقالب المحدد.  
19. حدد كل الكيانات القانونية أو مجموعة فرعية لها من القالب لتشغيل إقفال نهاية السنة لها.
    * عند تشغيل إقفال نهاية السنة للمرة الأولى، وللحصول على الأرصدة الأولية، قد تختار معظم المؤسسات تشغيل إقفال نهاية السنة لجميع الكيانات القانونية داخل القالب. إذا تمت تسوية الإدخالات بعد ذلك، فقد تختار تشغيل إقفال نهاية السنة فقط للكيانات القانونية التي تتضمن تسوية.  
20. انقر فوق "موافق".
21. حدد السنة المالية لتشغيل إقفال نهاية السنة لها.
22. في حقل "الإيصال"، اكتب قيمة.
    * من المستحسن تضمين السنة المالية في رقم الإيصال، لتسهيل العثور على إيصال إقفال نهاية السنة المنشأ.  
23. يتم تشغيل إقفال نهاية السنة بشكل افتراضي في الوضع الدفعي.
    * من المستحسن تشغيل العمليات طويلة الأمد في الوضع الدفعي. هذه هي عادة إحدى هذه العمليات، ولهذا السبب فإن الإعداد الافتراضي هو استخدام الوضع الدفعي.  
24. انقر فوق "موافق".


