--- 
title: "تأكيد أوامر المبيعات"
description: "يوضح هذا الإجراء كيفية تأكيد أوامر المبيعات."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="confirm-sales-orders"></a>تأكيد أوامر المبيعات

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية تأكيد أوامر المبيعات. ستتعرف على كيفية تأكيد أمر واحد وتأكيد أوامر متعددة في مرة واحدة. وعادة ما تُنفذ هذه المهام عن طريق معالج أمر مبيعات. يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك. قبل البدء، تأكد من وجود العديد من أوامر المبيعات المفتوحة لنفس العميل. إذا كنت تستخدم USMF، يمكنك استخدام العميل 027-الولايات المتحدة.


## <a name="confirm-a-single-sales-order"></a>قم بتأكيد أمر مبيعات.
1. انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.
2. في القائمة، ابحث عن الأمر الذي تريد تأكيده وحدده.
3. انقر فوق الارتباط الموجود في رقم أمر المبيعات لفتح الأمر المحدد.
4. في جزء الإجراءات، انقر فوق "بيع‬".
5. قم بتأكيد أمر المبيعات.
6. قم بتوسيع القسم "المعلمات" أو طيه.
    * تأكد من أن الحقل "ترحيل نعم" نشط.  
7. قم بتعيين خيار تأكيد الطباعة على "نعم".
    * يحدد الحقل "التحقق من حد الائتمان" الطريقة المُستخدمة لحساب ائتمان العميل المتبقي. ويُنسخ ائتمان العميل المتبقي افتراضيًا من صفحة معلمات الحسابات المدينة. إذا كنت ترغب في تخطي التحقق من حد الائتمان عند تأكيد أمر مبيعات معين، فقم بتعيين "التحقق من حد الائتمان" على "بلا". ومع ذلك، يجب أن تعلم أنه حتى إذا تم تعيين هذا الحقل على "بلا"، سيظل التحقق من حد الائتمان منفذًا إذا تم تحديد الخيار "حد الائتمان الإلزامي" في بيانات العميل الرئيسية.  
8. انقر فوق "موافق".
9. انقر فوق نعم.
10. قم بإغلاق الصفحة.
11. في جزء الإجراءات، انقر فوق "خيارات".
12. انقر فوق "تغيير طريقة العرض‬".
13. انقر فوق "عرض الرأس".
    * عند تأكيد أمر، يتم تعيين حالة المستند على "تأكيد".  
14. في جزء الإجراءات، انقر فوق "بيع‬".
15. انقر فوق "تأكيد أمر المبيعات".
16. قم بإغلاق الصفحة.

## <a name="confirm-multiple-sales-orders-at-once"></a>تأكيد أوامر مبيعات متعددة في وقت واحد
1. انتقل إلى المبيعات والتسويق > أوامر المبيعات > تأكيد الأمر > تأكيد أمر المبيعات.
2. انقر فوق تحديد.
3. في القائمة بعلامة التبويب "النطاق"، ابحث عن السجل الذي يشير إلى حقل حساب ثم حدده.
4. في الحقل "المعايير"، انقر فوق زر القائمة المنسدلة لفتح البحث.
5. في القائمة، ابحث عن حساب العميل الذي يحتوي على أوامر متعددة وترغب في إجراء تأكيد جماعي به ثم حدده.
    * إذا كنت تستخدم USMF، يمكنك تحديد حساب 027-الولايات المتحدة.  
6. انقر فوق "موافق".
    * تعرض علامة التبويب "نظرة عامة" قائمة بالأوامر التي تطابق معايير الاستعلام. سيتم تضمين هذه الأوامر في التأكيد.  
    * يحدد الحقل "تحديث الملخص لـ" المعلمة يتم من خلالها تلخيص أوامر متعددة في مستند تأكيد واحد. بشكل افتراضي، يُنسخ الخيار من القيم الافتراضية لإعداد تحديث الملخص في صفحة معلمات الحسابات المدينة.  
7. في تحديث الملخص للحقل، حدد "أمر".
    * ويتمثل الحد الأدنى للمعلمات المطلوبة لإنشاء تحديثات ملخص في حساب الفاتورة والعملة. وهذا يعني أن تحديثات الملخص التي لها حسابات فواتير مختلفة وعملات مختلفة غير مسموح بها. يمكن إعداد معلمات إضافية في صفحة معلمات تحديث الملخص التي يمكن الوصول إليها من صفحة معلومات الحسابات المدينة.  
8. في الحقل "أمر المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.
9. في القائمة، حدد العدد الذي تريده أن يمثل أمر الملخص.
10. انقر فوق "ترتيب".
11. انقر فوق "موافق".
12. انقر فوق "موافق".


