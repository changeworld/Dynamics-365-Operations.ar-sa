--- 
title: "التقارير الإلكترونية - تصميم تكوين لإنشاء التقارير بتنسيق OPENXML (نوفمبر 2016)"
description: "تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على قالب لإنشاء المستندات الإلكترونية بتنسيق OPENXML."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>التقارير الإلكترونية - تصميم تكوين لإنشاء التقارير بتنسيق OPENXML (نوفمبر 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على قالب لإنشاء المستندات الإلكترونية بتنسيق OPENXML. سيتم استخدام هذا التكوين لمعالجة مدفوعات المورد.



في هذا المثال، ستقوم بإنشاء تكوين لشركة نمودجية، .Litware, Inc ويمكن تنفيذ هذه الخطوات في شركة GBSI.



لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط". كما يجب أن يكون لديك ملف Excel سيتم استيراده عند إنشاء القالب. يمكن الوصول إلى هذا الملف من [قالب تقرير الدفع](https://go.microsoft.com/fwlink/?linkid=862266).


## <a name="upload-the-payments-data-model-configuration"></a>تحميل تكوين نموذج بيانات الدفعات
1. انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.
2. في القائمة، قم بوضع علامة للصف المحدد.
    * حدد موفر تكوين الشركة النموذجية، Litware, Inc. إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".  
3. انقر فوق "تعيين كنشط".
4. انقر فوق "المستودعات".
    * حدد مستودعًا لنوع موارد Operations، إذا كان متوفرًا. إذا كان متوفرًا، قم بتخطي الخطوات التالية حول إنشاء مستودع جديد.  
5. انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.
6. في الحقل "نوع مستودع التكوين"، أدخل "موارد العمليات".
7. انقر فوق إنشاء مستودع.
8. انقر فوق "موافق".
9. انقر فوق "فتح".
10. في الشجرة، حدد "نموذج الدفع".
11. انقر فوق "استيراد".
    * قم باستيراد نموذج البيانات هذا. سيتم استخدامه كمصدر بيانات في تكوين تنسيق جديد. قم بتخطي هذه الخطوة إذا لم يتم استيراد هذا التكوين الفعل.  
12. انقر فوق نعم.
13. قم بإغلاق الصفحة.
14. قم بإغلاق الصفحة.

## <a name="create-a-new-format-configuration"></a>قم بإنشاء تكوين تنسيق جديد
1. انقر فوق "تكوينات إعداد التقارير‬".
2. في الشجرة، حدد "نموذج الدفع".
3. انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.
4. في الحقل "جديد"، أدخل 'التنسيق استناداً إلى نموذج الدفع الخاص بنموذج البيانات".
    * ثم بإنشاء تنسيق يستند إلى نموذج البيانات "PaymentModel".  
5. في الحقل "الاسم"، اكتب "تقرير ورقة عمل العينة".
    * تقرير ورقة العمل للعينة  
6. في الحقل "الوصف"، اكتب تقرير ورقة عمل عينة لدقعات الموردين".
    * تقرير ورقة عمل عينة لدفعات الموردين.  
7. في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.
    * حدد تعريف "CustomerCreditTransferInitiation".  
8. وانقر فوق إنشاء تكوين.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>تصميم مستند جديد بتنسيق ورقة عمل OPENXML
1. في الشجرة، حدد "Payment model\Sample worksheet report".
2. انقر فوق المصمم.
3. في جزء الإجراءات، انقر فوق "استيراد".
4. انقر فوق استيراد من "Excel".
5. انقر فوق "المرفقات".
    * قم بإرفاق مستند Excel كقالب.  
6. انقر فوق "جديد".
7. انقر فوق "ملف".
    * قم بالإشارة إلى ملف Excel الموجود.  
8. قم بإغلاق الصفحة.
9. في حقل "القالب"، أدخل قيمة أو حددها.
    * حدد ملف Excel المرفق ليتم استخدامه كقالب.  
10. انقر فوق "موافق".
    * لاحظ أنه تم إنشاء مكونات تنسيق التقارير الإلكترونية في تنسيق التصميم الذي يستند إلى هيكل مستند MS Excel المرجعي (نطاقات مسماة).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>إنشاء مصدر بيانات جديد لحساب الإجماليات حسب أكواد العملة
1. انقر فوق علامة التبويب "التعيين".
2. انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.
3. في الشجرة، حدد "Functions\Group by".
4. في الحقل "اسم"، اكتب "PaymentByCurrency".
    * PaymentByCurrency  
5. انقر فوق تحرير تجميع حسب.
6. في الشجرة ، قم بتوسيع "النموذج"
7. في الشجرة، حدد "النموذج/المدفوعات".
8. انقر فوق إضافة حقل إلى.
9. انقر فوق ما يتم تجميعه.
10. في الشجرة، قم بتوسيع "النموذج/المدفوعات".
11. في الشجرة، حدد "model\Payments\Currency".
12. انقر فوق إضافة حقل إلى.
13. انقر فوق "الحقول مجمعَة".
14. في الشجرة، حدد "model\Payments\Instructed Amount(InstructedAmount)".
15. انقر فوق إضافة حقل إلى.
16. انقر فوق حقول التجميع.
17. في الحقل "الأسلوب‬"، حدد خيارًا.
    * حدد دالة التجميع SUM.  
18. في الحقل "اسم"، اكتب "TotalInstructuredAmount".
    * TotalInstructuredAmount  
19. انقر فوق "حفظ".
20. قم بإغلاق الصفحة.
21. انقر فوق "موافق".

## <a name="map-format-components-to-data-sources"></a>تعيين مكونات التنسيق بمصادر البيانات
1. في الشجرة ، قم بتوسيع "النموذج"
2. في الشجرة، قم بتوسيع "النموذج/المدفوعات".
3. في الشجرة، قم بتوسيع "model\Payments\Initiating Party(InitiatingParty)".
4. في الشجرة، حدد "model\Payments\Initiating Party(InitiatingParty)\Name".
5. في الشجرة، قم بتوسيع "Excel\ReportHeader".
6. في الشجرة، حدد "Excel\ReportHeader\CompanyName".
7. انقر فوق "ربط".
8. في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن".
9. في الشجرة، قم بتوسيع "model\Payments\Creditor\Identification".
10. في الشجرة، حدد "model\Payments\Creditor\Identification\Source ID(SourceID)".
11. في الشجرة، قم بتوسيع "Excel\PaymLines".
12. في الشجرة، حدد "Excel\PaymLines\VendAccountName".
13. انقر فوق "ربط".
14. في الشجرة، حدد "النموذج/المدفوعات/الدائن/الاسم".
15. في الشجرة، حدد "Excel\PaymLines\VendName".
16. انقر فوق "ربط".
17. في الشجرة، قم بتوسيع "model\Payments\Creditor Agent(CreditorAgent)".
18. في الشجرة، حدد "model\Payments\Creditor Agent(CreditorAgent)\Name".
19. في الشجرة، حدد "Excel\PaymLines\Bank".
20. انقر فوق "ربط".
21. في الشجرة، حدد "model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)".
22. في الشجرة، حدد "Excel\PaymLines\RoutingNumber".
23. انقر فوق "ربط".
24. في الشجرة ، قم بتوسيع "النموذج/المدفوعات/حساب الدائن(CreditorAccount)".
25. في الشجرة ، قم بتوسيع "النموذج/المدفوعات/حساب الدائن(CreditorAccount)/هوية".
26. في الشجرة، حدد "model\Payments\Creditor Account(CreditorAccount)\Identification\Number".
27. في الشجرة، حدد "Excel\PaymLines\AccountNumber".
28. انقر فوق "ربط".
29. في الشجرة، حدد "model\Payments\Instructed Amount(InstructedAmount)".
30. في الشجرة، حدد "Excel\PaymLines\Debit".
31. انقر فوق "ربط".
32. في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن".
33. في الشجرة ، قم بتوسيع "النموذج/المدفوعات/حساب الدائن(CreditorAccount)".
34. في الشجرة، قم بتوسيع "model\Payments\Creditor Agent(CreditorAgent)".
35. في الشجرة، حدد "model\Payments\Currency".
36. في الشجرة، حدد "Excel\PaymLines\العملة".
37. انقر فوق "ربط".
38. في الشجرة، قم بتوسيع "PaymentByCurrency".
39. في الشجرة، قم بتوسيع "PaymentByCurrency\grouped".
40. في الشجرة، حدد "PaymentByCurrency\grouped\Currency".
41. في الشجرة، قم بتوسيع "Excel\SummaryLines".
42. في الشجرة، حدد "Excel\SummaryLines\SummaryCurrency".
43. انقر فوق "ربط".
44. في الشجرة، قم بتوسيع "PaymentByCurrency\aggregated".
45. في الشجرة، حدد "PaymentByCurrency\aggregated\TotalInstructuredAmount".
46. في الشجرة، حدد "Excel\SummaryLines\SummaryAmount".
47. انقر فوق "ربط".
48. في الشجرة، حدد "PaymentByCurrency".
49. في الشجرة، حدد "Excel\SummaryLines".
50. انقر فوق "ربط".
51. في الشجرة، حدد "النموذج/المدفوعات".
52. في الشجرة، حدد "Excel\PaymLines".
53. انقر فوق "ربط".
54. انقر فوق "حفظ".
55. قم بإغلاق الصفحة.

## <a name="use-the-created-configuration-for-payments-processing"></a>استخدام التكوين الذي تم إنشاؤه لمعالجة المدفوعات
1. انقر فوق "تغيير الحالة".
2. انقر فوق "مكتمل".
3. انقر فوق "موافق".
4. قم بإغلاق الصفحة.
5. قم بإغلاق الصفحة.
6. انتقل إلى الحسابات المدينة > إعداد الدفع‬ > طرق الدفع.
7. استخدم عامل التصفية السريع لإجراء التصفية على حقل "طريقة الدفع" مع القيمة "إلكتروني".
    * إلكتروني  
8. انقر فوق "تحرير".
9. وسّع قسم المقطع "تنسيقات الملفات".
10. حدد "نعم" في الحقل "التقارير الإلكترونية العامة‬".
11. في الحقل "تصدير تكوين التنسيق‬"، أدخل قيمة أو حددها.
    * قم بتحديد تكوين "تقرير ورقة عمل العينة".  
12. انقر فوق "حفظ".
13. قم بإغلاق الصفحة.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>استخدم التكوين الذي تم إنشاؤه لاختبار معالجة دفاتر يومية الدفعات
1. انتقل إلى الحسابات الدائنة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.
2. انقر فوق "جديد".
    * إنشاء دفتر يومية مدفوعات جديد.  
3. في حقل "الاسم"، اكتب "VendPay".
    * VendPay  
4. انقر فوق البنود.
5. في حقل "الحساب"، حدد القيم "GB_SI_000001".
    * GB_SI_000001  
6. تعيين الخصم على "1000".
7. انقر فوق "جديد".
8. في حقل "الحساب"، حدد القيم "GB_SI_000005".
    * GB_SI_000005  
9. تعيين الخصم على "2000".
10. في الحقل "العملة"، اكتب "EUR".
    * يورو  
11. في الحقل "الحساب المقابل"، حدد القيم "GBSI OPER".
    * GBSI OPER  
12. في الحقل "طريقة الدفع"، اكتب "إلكتروني".
    * إلكتروني  
13. انقر فوق "حفظ".
14. انقر فوق إنشاء مدفوعات.
15. في الحقل "طريقة الدفع"، اكتب "إلكتروني".
    * إلكتروني  
16. في حقل "اسم الملف"، اكتب "دفعات".
    * على سبيل المثال، اكتب "دفعات".  
17. في الحقل "حساب البنك"، اكتب "GBSI OPER".
    * GBSI OPER  
18. انقر فوق "موافق".
19. انقر فوق "موافق".
    * قم بمراجعة ورقة العمل التي تم إنشاؤها، بما في ذلك تفاصيل بنود الدفع بالإضافة إلى الإجماليات لكل كود عملة مستخدم في رسالة الدفع هذه.  


