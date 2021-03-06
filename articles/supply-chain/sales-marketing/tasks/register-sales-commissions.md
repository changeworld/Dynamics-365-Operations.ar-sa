--- 
title: "تسجيل عمولات المبيعات"
description: "يوضح هذا الإجراء كيفية حساب عمولات المبيعات وتسجيلها."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5535f1627526b97ddc9ca2c210db4e332782d656
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="register-sales-commissions"></a>تسجيل عمولات المبيعات

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية حساب عمولات المبيعات وتسجيلها. يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة. قبل تشغيل هذا الدليل، قم بتشغيل الدليل المُسمى "إعداد قواعد عمولات المبيعات" للتأكد من وجود توفر إعداد حساب العمولات الضروري بالكامل.

قم بتدوين ملاحظة بالعميل وأرقام الأصناف التي قمت باختيارها لعملية العمولات واستخدمها عندما يُطلبك منك إنشاء أمر مبيعات في هذا الدليل.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>فوترة أمر مبيعات يؤهل مندوب مبيعات لعمولة
1. انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.
2. انقر فوق "جديد".
3. في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
6. انقر فوق "موافق".
7. في جزء الإجراءات، انقر فوق "خيارات".
8. انقر فوق "تغيير طريقة العرض‬".
9. انقر فوق "عرض الرأس".
10. قم بتوسيع قسم "الإعداد".
    * تمثل القيمة الموجودة في الحقل "مجموعة المبيعات" مجموعة معين لها مندوب مبيعات واحد أو أكثر. ويمثل الأشخاص الذين تحتوي عليهم المجموعة من سيحصل على العمولات عند فوترة الأمر، وفقًا للنسب والتوزيع المحدد مسبقاً.   يتم نسخ القيمة من بطاقة العميل، ولكن يمكنك تغييرها إذا أردت.  ويتم أيضا نسخ مجموعة المبيعات لبند أمر المبيعات. ويمكنك تغيير القيمة بحيث قد تختلف عن القيمة المضمنة في الرأس و/أو بين السطور.  
    * تمثل القيمة الموجودة في الحقل "مجموعة العمولات" مجموعة قمت بإنشائها لعميل واحد أو أكثر لتتبع العمولات.   يتم نسخ القيمة من بطاقة العميل، ولكن يمكنك تغييرها إذا أردت.   
11. في جزء الإجراءات، انقر فوق "خيارات".
12. انقر فوق "تغيير طريقة العرض‬".
13. انقر فوق "عرض البند".
14. في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.
15. في القائمة، حدد العنصر الذي قمت بإعداده للعمولات. 
16. في حقل الكمية، أدخل رقمًا.
    * قم بتدوين ملاحظة بالمبلغ الصافي للبند. فهو يمثل إيراد المبيعات، والذي يُعد أساس حساب العمولة في هذا المثال.  
17. انقر فوق "حفظ".
18. في جزء "الإجراءات"، انقر فوق "فاتورة".
19. انقر فوق "فاتورة".
20. وسّع مقطع "المحددات".
21. في الحقل "الكمية"، حدد "الكل".
22. حدد "نعم" في الحقل "الترحيل".
23. انقر فوق "موافق".
24. انقر فوق "موافق".
    * قد يستغرق الأمر دقيقة أو نحو ذلك لترحيل الحركة. اترك المعالجة تكتمل ولا تغلق الصفحة.  

## <a name="review-the-registered-sales-commissions"></a>مراجعة عمولات المبيعات المسجلة
1. في جزء "الإجراءات"، انقر فوق "فاتورة".
2. انقر فوق "فاتورة".
3. في جزء "الإجراءات"، انقر فوق "فاتورة".
4. انقر فوق "حركات العمولات".
    * تعرض علامة التبويب "نظرة عامة" البنود التي تمثل مبالغ العمولات التي تُدفع لمندوبي المبيعات المرتبطين بأمر المبيعات المفوتر. فلنراجع التفاصيل.     
    * إذا استخدمتَ الدليل "إعداد قواعد عمولات المبيعات" لإعداد مجموعة مبيعات العمولة، هناك مندوبا مبيعات سيحصلان على عمولة مبيعات وسيتم تقسيم العمولة بينهما بالتساوي.  
    * في هذا المثال، يُحسب إجمالي مبلغ العمولة كنسبة مئوية لإيراد المبيعات (المبلغ الصافي لبند الأمر).   
5. قم بإغلاق الصفحة.
6. انقر فوق "الإيصال".
    * يمكنك مراجعة حركات الإيصال لمبالغ العمولات التي تم ترحيلها إلى حسابات مصروفات العمولة والحسابات الدائنة للعمولة المعرفة مسبقاً.  


