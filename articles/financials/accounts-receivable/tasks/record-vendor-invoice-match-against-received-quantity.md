--- 
title: "تسجيل فاتورة المورّد ومطابقتها بالكمية المستلمة"
description: "عندما تتلقى فاتورة من مورّد للبضائع أو الخدمات على أمر شراء، قد تتطلب العمليات التجارية تلقي البضائع أو الخدمات قبل اعتماد الفاتورة للدفع."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a64413ac1840ef535252bd2d9752d52b26ccade1
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>تسجيل فاتورة المورّد ومطابقتها بالكمية المستلمة

[!include [task guide banner](../../includes/task-guide-banner.md)]

عندما تتلقى فاتورة من مورّد للبضائع أو الخدمات على أمر شراء، قد تتطلب العمليات التجارية تلقي البضائع أو الخدمات قبل اعتماد الفاتورة للدفع. قبل أن تبدأ، تأكد من تحديد مفتاح تكوين مطابقة الفاتورة. 

في صفحة "محددات الحسابات الدائنة"، تأكد من تحديد الخيار "تمكين التحقق من صحة مطابقة الفاتورة‬"، ومن تعيين الحقل "ترحيل الفاتورة التي بها اختلافات إلى "طلب موافقة‬" ومن تعيين الحقل "سياسة مطابقة البند" إلى "سياسة المطابقة الثلاثية‬".

يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF. قد ينفذ دور مدير الحسابات الدائنة أو دور مدير الحسابات‬ هذه الخطوات.


## <a name="create-a-purchase-order"></a>إنشاء أمر شراء
1. انتقل إلى "كافة أوامر الشراء".
2. انقر فوق "جديد".
3. في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في الحقل "حساب المورّد‬"، اكتب قيمة.
5. انقر فوق "موافق".
6. انقر فوق "إضافة بند".
7. في الحقل "رقم الصنف" اكتب قيمة.
8. في جزء الإجراءات، انقر فوق "شراء".
9. انقر فوق "تأكيد".

## <a name="post-a-product-receipt"></a>ترحيل إيصال استلام المنتجات
1. في جزء الإجراءات، انقر فوق "استلام".
2. انقر فوق "إيصال استلام المنتجات".
3. في القائمة، قم بوضع علامة للصف المحدد.
4. في الحقل "إيصال استلام المنتجات"، اكتب قيمة.
5. انقر فوق "موافق".

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>تسجيل فاتورة مورّد ومطابقتها مع إيصالات استلام المنتجات
1. في جزء "الإجراءات"، انقر فوق "فاتورة".
2. انقر فوق "فاتورة".
3. في الحقل "الرقم"، اكتب قيمة.
4. انقر فوق افتراضي من: "الكمية المطلوبة" لفتح مربع حوار الإسقاط.
5. في الحقل "الكمية الافتراضية للبنود"، حدد خيارًا.
6. انقر فوق "موافق".
7. انقر فوق نعم.
8. انقر فوق "مطابقة إيصالات استلام المنتجات".
9. انقر فوق "موافق".
10. في جزء الإجراءات، انقر فوق "مراجعة".
11. انقر فوق "تفاصيل المطابقة".


