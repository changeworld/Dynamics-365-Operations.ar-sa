---
title: "إعداد الشحن"
description: "يشرح هذا الموضوع كيفية تكوين عمليات مخزون الشحن الوارد."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 48e3f7f33bedf33bee5a7c2882e90743feac8687
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-consignment"></a>إعداد الشحن

يشرح هذا الموضوع كيفية تكوين عمليات مخزون الشحن الوارد. 

إن مخزون الشحن هو المخزون الذي يملكه المورد، ولكنه مخزن في موقعك. عندما تصبح جاهزًا لاستهلاك المخزون أو استخدامه، يمكنك الحصول على ملكية المخزون. يصف هذا الموضوع الإعداد المطلوب لتمكين عمليات الشحن. للحصول على مزيد من المعلومات حول عمليات الشحن، راجع [الشحن](consignment.md).

## <a name="inventory-owners"></a>ملاك المخزون
من أجل تسجيل المخزون الفعلي للشحن الوارد، يجب تعريف المالك المورّد. ويتم ذلك في صفحة **مالك المخزون**. عند تحديد **حساب المورد**، يؤدي ذلك إلى إنشاء القيم الافتراضية لحقلي **الاسم** و **المالك**. ستكون القيمة في حقل **المالك** مرئية للمورد، لذا قد ترغب في تغييرها إذا لم يكن من السهل على الأشخاص الخارجيين التعرف على أسماء حسابات المورد. من الممكن تحرير حقل **المالك**، لكن فقط إلى المرحلة التي تقوم فيها بحفظ سجل **مالك المخزون**. تتم تعبئة حقل **الاسم** باسم الطرف الذي يقترن حساب المورد به، ولا يمكن تغيير ذلك. 

[![أصحاب المخزون](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>مجموعة أبعاد التعقب
يجب أن تقترن الأصناف التي سيتم استخدامها في عمليات الشحن **بمجموعة أبعاد التعقب** حيث تم تعيين بُعد **المالك** إلى **نشط**. في بُعد المالك، يكون الخياران **المخزون الفعلي** و**المخزون المالي** محددين بشكل دائم. ولا يتم تحديد الخيار **خطة التغطية حسب البُعد‬** إطلاقًا. 

[![مجموعة أبعاد التعقب](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>دفتر يومية تغييرات ملكية المخزون
يُستخدم **دفتر يومية تغيير ملكية المخزون **لتسجيل تحويل ملكية مخزون الشحن من المورّد إلى الكيان القانوني الذي يستهلكه. وكما هو الحال في أي دفتر يومية مخزون، يجب تعريفه بواسطة اسم دفتر يومية المخزون. يتم إنشاء هذه الأسماء في صفحة **أسماء دفتر يومية المخزون** الصفحة، ويجب تعيين **نوع دفتر اليومية** إلى **تغيير الملكية**. 

[![الملكية-التغيير-دفتر يومية المخزون](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>تعاون المورد في عمليات الشحن
عندما يستخدم الموردون واجهة تعاون المورد، يمكنهم استخدامها لمراقبة استهلاك المخزون في موقعك. لمزيد من المعلومات حول إعداد الموردين لاستخدام تعاون المورِّد‏‎، راجع [تكوين الأمان لمستخدمي تعاون المورِّد](../procurement/configure-security-vendor-portal-users.md).

