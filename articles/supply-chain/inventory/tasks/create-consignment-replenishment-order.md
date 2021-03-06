--- 
title: "إنشاء أمر تزويد شحن"
description: "يوضح هذا الإجراء كيفية إنشاء أمر تزويد الشحن حيث يمكنك تعقب التسليم المتوقع من مورّد إلى مخزون الشحن."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7f8005ec9e723c94d53e6ab81f04ee388c83faa
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-consignment-replenishment-order"></a>إنشاء أمر تزويد شحن

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء أمر تزويد الشحن حيث يمكنك تعقب التسليم المتوقع من مورّد إلى مخزون الشحن. ويوضح أيضًا كيفية تسجيل إيصال استلام المنتجات بحيث يتم تسجيل مخزون الشحن كمخزون فعلي يملكه المورّد. يقوم عادةً أخصائي التدبير بتنفيذ هذا الإجراء. ويمكنك استخدام هذا الدليل في شركة بيانات العرض التوضيحي USMF. يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.




## <a name="create-a-consignment-replenishment-order"></a>إنشاء أمر تزويد شحن
1. انتقل إلى التدبير وتحديد الموارد‬ > الشحن‬ > أوامر تزويد الشحن‬.
2. انقر فوق "جديد".
3. في حقل "حساب المورّد‬"، أدخل المورّد "US-104".
    * يجب تحديد مورّد تم تسجيله كمالك في الصفحة "ملاك المخزون‬".  
4. انقر فوق "موافق".
5. انقر فوق "إضافة بند".
6. في الحقل "رقم الصنف" اكتب "M9211CI".
    * يجب تحديد عنصر تم إعداده لمخزون الشحن‬.  
7. في حقل الكمية، أدخل رقمًا.
8. في حقل "‏‫تاريخ التسليم المطلوب‬‬"، أدخل تاريخًا.
    * يتم استخدام التواريخ المطلوبة والمؤكدة بواسطة محرك MRP لوصول البضائع المنتظر.  
9. في حقل "‏‫تاريخ التسليم المؤكد‬"، أدخل تاريخًا.
10. قم بتوسيع قسم "تفاصيل البند".
11. انقر فوق علامة التبويب "أبعاد المخزون".
12. لإظهار المالك في الحقل "مالك أبعاد المخزون"، قم بتحديث الصفحة.
    * تم الآن إدراج المورّد US-104 كالمالك.  

## <a name="check-the-inventory-transaction-status"></a>التحقق من حالة حركة المخزون
1. انقر فوق المخزون.
2. انقر فوق "الحركات".
3. في القائمة، قم بوضع علامة للصف المحدد.
    * لاحظ أنه تم تعيين حقل "الاستلام" إلى "مطلوب‬".  
4. قم بإغلاق الصفحة.

## <a name="receive-items"></a>استلام الأصناف
1. انقر فوق "إيصال استلام المنتجات".
2. في الحقل "إيصال استلام المنتجات الخارجي‬"، اكتب قيمة.
3. في حقل "الكمية"، أدخل رقمًا أقل من الرقم الذي يظهر هناك. 
4. انقر فوق "موافق".

## <a name="check-the-on-hand-inventory"></a>التحقق من المخزون الفعلي
1. انقر فوق المخزون.
2. انقر فوق "الكمية المتاحة‬".
3. انقر فوق "نظرة عامة".
    * تتوفر الأصناف التي تم استلامها كمخزون شحن مملوك من قِبل المورّد بشكل فعلي. وتظهر الكمية المتبقية في أمر تزويد الشحن في حقل "الكمية المطلوبة إجمالاً‬".  
4. قم بإغلاق الصفحة.
5. انقر فوق "إغلاق".


