--- 
title: "استيراد تكوين تحويل الائتمان ISO20022"
description: "يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات المورّد.‬"
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 71c0175178203006e297466c4a37cd3e6319b6ea
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="import-iso20022-credit-transfer-configuration"></a>استيراد تكوين تحويل الائتمان ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات المورّد.‬ يتم استخدام تنسيق تحويل الائتمان الألماني ISO 20022 كمثال. يمكنك استخدام هذا الإجراء لتنسيقات التقارير الإلكترونية الأخرى المتوفرة. 

تم إنشاء هذه المهمة باستخدام شركة بيانات العرض التوضيحي DEMF، ولكن يمكنك استخدام أي من شركات بيانات العرض التوضيحي لإكمال هذه المهمة.

هذه هي المهمة الأولى من ضمن خمس مهام، هدفها أن تعمل معًا على توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية. يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.

1. انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.
2. في قائمة "موفرو التكوين‬" المتوفرون، حدد Microsoft.
3. انقر فوق "تعيين كنشط".
4. انقر فوق "المستودعات".
5. انقر فوق "فتح".
6. انقر فوق "إظهار عوامل التصفية".
7. طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "تحويل الائتمان ISO20022 (DE)" في حقل "اسم التكوين" باستخدام مشغل عامل التصفية "يبدأ بـ".
    * أو، يمكنك العثور على التكوين في القائمة، وتحديده، ثم نقله إلى مهمة الاستيراد.  
8. انقر فوق "استيراد".
    * إذا لم يتوفر الزر "استيراد"، فهذا يعني أن التكوين قد تم استيراده.  
9. انقر فوق نعم.


