--- 
title: "‏‫تحديد شروط دفع المورّد‬"
description: "إعداد شرو الدفع لفواتير المورّد."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a00ca73b1bc301960132a86846749d12c39ed3f7
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="define-vendor-payment-terms"></a>‏‫تحديد شروط دفع المورّد‬

[!include [task guide banner](../../includes/task-guide-banner.md)]

إعداد شرو الدفع لفواتير المورّد. تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

1. انتقل إلى الحسابات المدينة > إعداد الدفع‬ > شروط الدفع.
2. انقر فوق "جديد".
    * تُستخدم صفحة "شروط الدفع" لتعريف الطريقة التي سيتم بها حساب تاريخ الاستحقاق. ولا تستخدم هذه الصفحة لتعريف كيف سيتم حساب تاريخ الخصم النقدي.  
3. في حقل "شروط الدفع"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. في الحقل "الأيام"، أدخل رقمًا.
    * سيستخدم الرقم الذي تم إدخاله هنا لإضافته إلى تاريخ الاستحقاق، أو إلى نهاية الفترة المحددة في طريقة الدفع. على سبيل المثال، إذا قمت بتحديد "الصافي"، فسيضاف الرقم إلى تاريخ الاستحقاق. أما إذا حددت "الشهر الحالي"، فسيتم إضافة الرقم إلى اليوم الأخير من الشهر الحالي لحساب تاريخ الاستحقاق.  
6. انقر فوق "حفظ".
7. قم بإغلاق الصفحة.
8. انتقل إلى الحسابات المدينة > إعداد الدفع > الخصومات النقدية‬‬.
9. انقر فوق "جديد".
10. في الحقل "الخصم النقدي"، أدخل معرفًا.
11. في وصف الحقل، اكتب قيمة.
12. إذا قدم المورّد خصمًا متدرجًا، فحدد الخصم النقدي التالي بعد انتهاء مدة صلاحية الحالي.
13. قم بإغلاق الصفحة.
14. في الحقل "الأيام"، أدخل رقمًا.
    * سيتم استخدام الكمية المدخلة في الحقل "أيام" لحساب تاريخ الخصم النقدي، استنادًا إلى الخيار الذي تم تحديده في الحقل "الصافي/الحالي‬". إذا تم تحديد "الصافي"، فستضاف الكمية إلى تاريخ الفاتورة لتحديد تاريخ الخصم النقدي. إذا تم تحديد "الشهر الحالي"، فستضاف الكمية إلى نهاية الشهر الحالي لتحديد تاريخ الخصم النقدي.  
15. أدخل النسبة المئوية للخصم النقدي في حقل "الخصم". 
16. أدخل الحساب الرئيسي الذي سيتم ترحيل ترحيل الخصم النقدي إليه لفواتير العميل.
17. أدخل الحساب الرئيسي الذي سيتم ترحيل ترحيل الخصم النقدي إليه لفواتير المورّد.
    * إذا تم تعيين "الحسابات المقابلة للخصومات" إلى "استخدام الحساب الرئيسي لخصم المورد"، فسيتم عندئذٍ استخدام الحساب الرئيسي.  إذا تم تعيين الخيار إلى "الحسابات الموجودة في بنود الفاتورة"، فسيتم ترحيل الخصم النقدي إلى حسابات الأصول/المصروفات على بنود الفاتورة.  
18. انقر فوق "حفظ".


