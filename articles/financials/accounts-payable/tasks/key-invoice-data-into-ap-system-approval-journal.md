--- 
title: "بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام دفتر يومية الموافقة"
description: "يوضح دليل المهمة هذا كيفية استخدام سجل الفواتير لإنشاء فواتير ثم استخدام دفتر يومية الموافقة لتحديث حسابات المصروفات."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام دفتر يومية الموافقة

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح دليل المهمة هذا كيفية استخدام سجل الفواتير لإنشاء فواتير ثم استخدام دفتر يومية الموافقة لتحديث حسابات المصروفات.


## <a name="create-and-post-and-invoice"></a>إنشاء فاتورة وترحيلها
1. انتقل إلى الحسابات الدائنة > الفواتير > سجل الفواتير.
2. انقر فوق "جديد".
3. حدد اسم سجل الفواتير الذي تريد استخدامه.
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
5. انقر فوق "البنود‬" لفتح السجل وإدخال بنود المصروفات.
6. حدد موردًا. على سبيل المثال، أدخل أو حدد US-104
7. في الحقل "الفاتورة"، اكتب قيمة.
8. في حقل "الوصف"، اكتب قيمة.
9. في الحقل "دائن"، أدخل رقمًا.
10. في الحقل "تمت الموافقة بواسطة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
11. ميّز أحد المعتمِدين ثم انقر فوق "تحديد" لتحديده.
12. انقر فوق "ترحيل".
13. قم بإغلاق الصفحة.
14. قم بإغلاق الصفحة.

## <a name="approve-an-invoice"></a>الموافقة على فاتورة
1. انتقل إلى الحسابات الدائنة > الفواتير > الموافقة على الفاتورة.
2. انقر فوق "جديد".
3. حدد اسم دفتر يومية الموافقة على الفواتير الذي تريد استخدامه.
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
5. انقر فوق "البنود" لعرض صفحة حيث يمكنك تحديد الفواتير التي تريد الموافقة عليها.
6. حدد "البحث عن إيصالات" لعرض كافة الفواتير الجاهزة للموافقة عليها.
7. ضع علامة على الفاتورة التي قمت بإنشائها.
8. انقر فوق تحديد.
    * يتم نقل الإيصالات التي حددتها أعلاه إلى هذه القائمة بعد تحديدها.  
9. انقر فوق "موافق".
10. انقر فوق حقل "رقم الحساب" لإضافة حساب مصروفات للفاتورة.
11. أدخل رقم حساب، واضغط على علامة جدولة للخروج من الحقل. على سبيل المثال، أدخل 600120.
12. انقر فوق "ترحيل".
13. انقر فوق "الإيصال" لعرض الإدخالات التي تم ترحيلها.
    * يتم عكس حساب "الفاتورة المعلقة للموافقة" واستبداله بحساب المصروفات الفعلية.  


