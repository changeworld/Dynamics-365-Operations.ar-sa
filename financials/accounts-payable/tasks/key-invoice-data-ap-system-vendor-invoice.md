--- 
title: "بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام فاتورة المورد"
description: "سيساعدك دليل المهمة هذا على إنشاء فاتورة مورّد من أمر شراء وعرض نتائج مطابقة أمر الشراء والإيصال والفاتورة (مطابقة ثلاثية)."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a365c52af49a66d6af5bb38f0053bd9c0fd34301
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a>بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام فاتورة المورد

[!include[task guide banner](../../includes/task-guide-banner.md)]

سيساعدك دليل المهمة هذا على إنشاء فاتورة مورّد من أمر شراء وعرض نتائج مطابقة أمر الشراء والإيصال والفاتورة (مطابقة ثلاثية).


## <a name="create-a-purchase-order"></a>إنشاء أمر شراء
1. انتقل إلى الحسابات الدائنة > أوامر الشراء > جميع أوامر الشراء.
2. انقر فوق "جديد".
3. في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. ابحث عن مورّد لتحديده. على سبيل المثال، انتقل لأسفل إلى US-104.
5. حدد المورّد US-104.
6. انقر فوق موافق.
7. في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.
8. حدد صنف المخزون. على سبيل المثال، حدد رقم الصنف 1000.
9. قم بتوسيع المقطع "تفاصيل البند" أو طيّه.
10. انقر فوق علامة التبويب "إعداد".
    * يمكنك تجاوز سياسة المطابقة لاستخدام عدم المطابقة أو سياسة المطابقة الثنائية أو سياسة المطابقة الثلاثية.  
11. قم بتوسيع المقطع "تفاصيل البند" أو طيّه.
12. في جزء الإجراءات، انقر فوق "شراء".
13. انقر فوق "تأكيد".

## <a name="receive-the-products"></a>استلام المنتجات
1. في جزء الإجراءات، انقر فوق "استلام".
2. انقر فوق "إيصال استلام المنتجات".
3. في حقل "إيصال استلام المنتجات"، أدخل رقم إيصال استلام المنتجات. على سبيل المثال، أدخل PR123.
4. انقر فوق "موافق" لترحيل إيصال استلام المنتجات.
5. قم بإغلاق الصفحة.

## <a name="create-a-vendor-invoice"></a>إنشاء فاتورة المورّد
1. انتقل إلى الحسابات الدائنة > أوامر الشراء > أوامر الشراء التي تم استلامها ولم تتم فوترتها‬.
2. حدد أمر الشراء الذي أنشأته.
3. في جزء الإجراءات، انقر فوق "فاتورة".
4. انقر فوق "فاتورة".
5. في حقل "الرقم"، قم بإدخال رقم الفاتورة.
6. في حقل وصف الفاتورة، اكتب قيمة.
7. في حقل تاريخ الفاتورة، قم بإدخال تاريخ.
8. في حقل "سعر الوحدة"، أدخل 1200.
9. انقر فوق "إضافة بند".
10. في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.
11. في القائمة، ابحث عن رقم صنف تكلفة التثبيت. على سبيل المثال، S0001
12. حدد رقم صنف تكلفة التثبيت.
    * لاحظ أن المطابقة لم يتم تنفيذها منذ قيامك بإدخال التغييرات.  
13. انقر فوق تحديث حالة المطابقة.
14. في جزء الإجراءات، انقر فوق "مراجعة".
15. انقر فوق "تفاصيل المطابقة".
    * لا حاجة إلى مطابقة البند الجديد حتى تبقى الحالة "لم يتم التنفيذ‬".  
16. حدد إيصال استلام المنتجات لصنف المخزون الذي تلقيته.
    * تمت مطابقة البند مع إيصال استلام المنتج، ولكن يوجد عدم تطابق في السعر أو الكمية وهذا سبب الفشل.  
17. في حقل "سعر الوحدة"، أدخل رقمًا.
    * الآن بعد أن أصبح سعر الوحدة مطابقًا، تم تحديث الحالة إلى "تم الاجتياز‬". إذا كانت سياستك تسمح بوجود اختلافات أو إذا كانت المطابقة عبارة عن مجرد تحذير، فلا يزال بإمكانك ترحيل الفاتورة.  
18. قم بإغلاق الصفحة.
19. انقر فوق "ترحيل".
20. وقم بغلق النموذج.
    * لاحظ أن أمر الشراء لم يعد مدرجًا على أنه تم استلامه ولكن بدون فوترة.‬  

