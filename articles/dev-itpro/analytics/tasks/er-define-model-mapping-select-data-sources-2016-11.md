--- 
title: "تحديد تعيينات نماذج التقارير الإلكترونية وتحديد مصادر بيانات لها"
description: "تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تحديد مصادر البيانات لنموذج بيانات التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b5f2f2c699514d723f42f5d1fb25724f46dfc4f4
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>تحديد تعيينات نماذج التقارير الإلكترونية وتحديد مصادر بيانات لها

[!include [task guide banner](../../includes/task-guide-banner.md)]

تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تحديد مصادر البيانات لنموذج بيانات التقارير الإلكترونية. سيتم ربط مصادر البيانات بالمكونات الفردية لنموذج البيانات المحدد في مرحلة التصميم وسيتم نشر بيانات الأعمال إلى نموذج البيانات المشار إليه في مرحلة التشغيل. في هذا المثال، ستحدد مصادر البيانات لنموذج بيانات موجود تم إنشاؤه لشركة عينة، .Litware, Inc. ولإكمال هذه الخطوات، يجب عليك أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء نموذج بيانات جديد".


## <a name="open-the-electronic-reporting-configurations-tree"></a>فتح شجرة تكوينات التقارير الإلكترونية
1. انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.
2. انقر فوق "تكوينات إعداد التقارير‬".

## <a name="insert-a-new-model-mapping"></a>إدراج تعيين طراز جديد
1. في الشجرة، حدد "المدفوعات (نموذج مبسط)".
2. انقر فوق المصمم.
3. انقر فوق "تعيين النموذج لمصدر البيانات".
4. انقر فوق "جديد".
    * سيؤدي ذلك إلى إنشاء سجل جديد سيعين نموذج البيانات إلى مصادر البيانات. في هذا المثال، ستعيِّنُ نموذج البيانات إلى مصادر البيانات لنوع الدفع المطلوب: تحويل الائتمان.     ومن الممكن تصميم أكثر من عملية تعيين واحدة لنموذج بيانات معين. على سبيل المثال، يمكنك إنشاء تعيين لأنواع مختلفة من المدفوعات، مثل الدين المباشر أو التحويلات الدائنة. في هذا المثال، ستقوم بإنشاء تعيين للتحويلات الدائنة.  
5. في الحقل "الاسم"، اكتب "تعيين CT".
    * تعيين CT  
6. في حقل الوصف، اكتب "تعيين نموذج الدفع CT".
    * ***تعيين نموذج الدفع  
7. في حقل التعريف، اكتب 'CustomerCreditTransferInitiation'.
    * CustomerCreditTransferInitiation  
8. حل تغييرات التعريف.
9. انقر فوق "حفظ".

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>تحديد مصادر البيانات المطلوبة لتعيين النموذج الحالي
1. انقر فوق المصمم.
2. في الشجرة، حدد "Dynamics 365 for Operations\سجلات جدول".
3. انقر فوق "إضافة جذر".
    * أدخل مصدر هذه البيانات للوصول إلى حركات الدفع.  
4. في الحقل "الاسم"، اكتب "الحركات".
    * الحركات  
5. في الحقل "التسمية"، أدخل "الحركات".
    * الحركات  
6. في الحقل "التعليمات"، أدخل "بنود دفتر يومية دفتر الأستاذ".
    * بنود دفتر يومية دفتر الأستاذ  
7. حدد "نعم" في حقل "طلب الاستعلام".
    * حدد "نعم".  
8. في الحقل "الجدول"، اكتب 'LedgerJournalTrans".
    * LedgerJournalTrans  
9. انقر فوق "موافق".
    * حدد الجدول LedgerJournalTrans كمصدر بيانات لنموذج البيانات الحالي.  
10. في الشجرة، حدد "الدوال/المحسوب".
11. وانقر فوق إضافة.
    * انقر فوق "إضافة" لإضافة حقل محسوب جديد.  
12. في الحقل "الاسم"، اكتب "$EndToEndID".
    * $EndToEndID  
13. انقر فوق "تحرير المعادلة".
14. في الشجرة، حدد "سلسلة/تسلسل".
15. انقر فوق "إضافة دالة".
16. في الشجرة، قم بتوسيع "الحركات".
17. في الشجرة، حدد "الحركات/الإيصال".
18. انقر فوق "إضافة مصدر بيانات".
19. في حقل الصيغة، أدخل 'CONCATENATE(Transactions.Voucher, "-", '.
    * النوع [، "-"،] في نهاية المعادلة.  
20. في الشجرة، حدد "السلسلة/النص".
21. انقر فوق "إضافة دالة".
22. في الشجرة، حدد 'Transactions\Record-ID(RecId)'.
23. انقر فوق "إضافة مصدر بيانات".
24. في حقل الصيغة، أدخل 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.
    * النوع [))] في نهاية المعادلة.  
25. انقر فوق "حفظ".
    * تأكد من أنه لم يتم اكتشاف أية أخطاء للمعادلة التي تم إنشاؤها. راجع علامة التبويب "أخطاء" أسفل عنصر التحكم في محرر المعادلة.  
26. قم بإغلاق الصفحة.
27. انقر فوق "موافق".
    * أضف الحقل المحسوب إلى مصدر البيانات هذا.  
28. وانقر فوق إضافة.
    * انقر فوق "إضافة" لإضافة حقل محسوب جديد.  
29. في الحقل "الاسم"، اكتب "$Amount".
    * $Amount  
30. انقر فوق "تحرير المعادلة".
31. في الشجرة، قم بتوسيع "الحركات".
32. في الشجرة، حدد "Transactions\Debit(AmountCurDebit)".
33. انقر فوق "إضافة مصدر بيانات".
34. في حقل الصيغة، أدخل 'Transactions.AmountCurDebit - '.
    * النوع [ - ] في نهاية المعادلة.  
35. في الشجرة، حدد "الحركات/Credit(AmountCurCredit)".
36. انقر فوق "إضافة مصدر بيانات".
37. انقر فوق "حفظ".
38. قم بإغلاق الصفحة.
39. انقر فوق "موافق".
    * سيؤدي هذا إلى إضافة حقل $Amount المحسوب إلى مصدر البيانات المحدد لنموذج البيانات الحالي.  
40. في الشجرة، حدد "الحركات\$المبلغ".
41. في الشجرة، قم بتوسيع "الحركات".
42. في الشجرة، قم بتوسيع أو طي "الحركات\$المبلغ".
43. في الشجرة، قم بتوسيع أو طي 'الحركات'.
44. في الشجرة، حدد "Dynamics 365 for Operations\سجلات جدول".
45. انقر فوق "إضافة جذر".
    * أدخل مصدر البيانات هذا للوصول إلى تفاصيل الحساب البنكي للشركة.  
46. في الحقل "الاسم"، اكتب "BankAccount".
    * BankAccount  
47. في الحقل "التسمية"، أدخل "Bank Account".
    * الحساب البنكي  
48. في الحقل "العليمات"، أدخل "حساب البنك".
    * الحساب البنكي  
49. حدد "نعم" في حقل "طلب الاستعلام".
    * حدد "نعم".  
50. في الحقل "الجدول"، اكتب "BankAccountTable".
    * BankAccountTable  
51. انقر فوق "موافق".
    * حدد الجدول BankAccountTable كمصدر بيانات لنموذج البيانات الحالي.  
52. انقر فوق "إضافة جذر".
    * أدخل مصدر البيانات هذا للوصول إلى متطلبات الشركة.  
53. في الحقل "الاسم"، اكتب "الشركة".
    * الشركة  
54. في الحقل "التسمية"، اكتب قيمة.
    * معلومات الشركة  
55. في الحقل "التعليمات"، أدخل "معلومات الشركة".
    * معلومات الشركة  
56. حدد "نعم" في حقل "طلب الاستعلام".
    * حدد "نعم".  
57. في الحقل "الجدول"، اكتب "CompanyInfo".
    * CompanyInfo  
58. انقر فوق "موافق".
    * حدد الجدول CompanyInfo كمصدر بيانات لنموذج البيانات الحالي.  
59. في الشجرة، حدد "الدوال/المحسوب".
60. انقر فوق "إضافة جذر".
    * أدرج حقلاً محسوبًا كمصدر بيانات جديد.  
61. في الحقل "الاسم، اكتب "ProcessingDateTime".‬
    * ProcessingDateTime  
62. في الحقل "التسمية"، أدخل "تاريخ المعالجة ووقتها".
    * تاريخ المعالجة ووقتها  
63. انقر فوق "تحرير المعادلة".
64. في الشجرة، حدد "التاريخ/الوقت\SESSIONNOW".
65. انقر فوق "إضافة دالة".
66. انقر فوق "حفظ".
67. قم بإغلاق الصفحة.
68. انقر فوق "موافق".
    * أضف الحقل المحسوب ProcessingDateTime ***كمصدر بيانات لنموذج البيانات الحالي.  
69. انقر فوق "حفظ".
70. قم بإغلاق الصفحة.
71. قم بإغلاق الصفحة.
72. قم بإغلاق الصفحة.


