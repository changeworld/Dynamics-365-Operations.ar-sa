--- 
title: "جرد المخزون في مستودع"
description: "يوضح لك هذا الإجراء عملية إنشاء دفتر يومية جرد مخزون وترحيله لجرد صنف معين بأحد المواقع في المستودع."
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="count-inventory-in-a-warehouse"></a>جرد المخزون في مستودع

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح لك هذا الإجراء عملية إنشاء دفتر يومية جرد مخزون وترحيله لجرد صنف معين بأحد المواقع في المستودع. وينطبق الإجراء على وظيفة "التخزين الأساسي"، المتوفرة في الوحدة النمطية "إدارة المخزون"، وليس على وظيفة التخزين المتوفرة في الوحدة النمطية "إدارة المستودع". يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك. إذا كنت تستخدم البيانات الخاصة بك، فتأكد من إعداد المنتجات والمواقع، وتأكد أنك قد أنشأت اسم دفتر يومية لدفاتر يومية الجرد. يتم تنفيذ جرد المخزون عادة بواسطة موظف مستودع.


## <a name="create-an-inventory-counting-journal"></a>إنشاء دفتر يومية جرد مخزون
1. انتقل إلى إدارة المخزون > إدخالات دفتر اليومية > جرد الصنف > الجرد.
2. انقر فوق "جديد".
3. في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في القائمة، انقر فوق اسم دفتر يومية جرد المخزون الذي تريد استخدامه.
    * سيتم ملء بعض الحقول الأخرى حسب إعداد اسم دفتر يومية جرد المخزون الذي تحدده.  
5. في الحقل "العامل"، انقر فوق زر القائمة المنسدلة لفتح البحث.
6. في القائمة، حدد العامل الذي تريد استخدامه.
7. انقر فوق تحديد.
8. انقر فوق "موافق".

## <a name="create-journal-lines"></a>إنشاء بنود دفتر اليومية
1. انقر فوق "جديد".
2. في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد "A0001".  
4. في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.
5. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد "الموقع 2".  
6. في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.
7. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد "المستودع 24".  
8. في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.
9. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * إذا كنت تستخدم شركة بيانات العرض التوضيحي USMF، فحدد "مجمع-001".  
10. في الحقل "تم جرده"، أدخل رقمًا.
    * إذا أدخلتَ عددًا محسوبًا يختلف عن العدد الذي يظهر في الحقل "الكمية المتاحة"، سيتم تحديث الحقل "الكمية" لإظهار التباين.  
11. انقر فوق "حفظ".

## <a name="post-the-inventory-counting-journal"></a>ترحيل دفتر يومية جرد المخزون
1. انقر فوق "ترحيل".
    * عند ترحيل دفتر يومية جرد مخزون، إذا كان المبلغ المحسوب يختلف عن المبلغ الذي تم الإعلام عنه في الحقل "الكمية المتاحة"، سيتم ترحيل استلام مخزون أو إصداره وتغيير مستوى المخزون وقيمته وإنشاء حركات دفتر الأستاذ.  
2. انقر فوق "موافق".

## <a name="view-inventory-transactions"></a>عرض حركات المخزون
1. انقر فوق المخزون.
2. انقر فوق "الحركات".
    * هنا يمكنك أن ترى أي حركات ذات صلة سيتم إنشاؤها عند ترحيل دفتر يومية جرد المخزون الخاص بك.   


