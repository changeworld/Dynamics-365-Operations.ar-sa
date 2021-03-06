---
title: "تعديل قيم تكلفة المخزون الفعلي"
description: "استخدم صفحة تسوية المخزون الفعلي لتسوية قيمة التكلفة لكميات المخزون الفعلي بعد إجراء عملية إغلاق المخزون."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 21942f7aa57d21f70e3014051c42328164b750a3
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="adjust-on-hand-inventory-cost-values"></a>تعديل قيم تكلفة المخزون الفعلي

[!include [banner](../includes/banner.md)]

استخدم صفحة تسوية المخزون الفعلي لتسوية قيمة التكلفة لكميات المخزون الفعلي بعد إجراء عملية إغلاق المخزون.

يمكنك استخدام صفحة **تسوية المخزون الفعلي** لتسوية قيمة التكلفة لكميات المخزون الفعلي بعد إجراء عملية إقفال المخزون. **ملاحظة:** لفتح صفحة **تسوية المخزون الفعلي**، في صفحة **الإقفال والتسوية**، حدد سجل عملية إقفال مخزون مكتملة، ثم انقر فوق **‎تسوية** &gt; **فعلي**. **مثال:** لديك الحركات التالية في فبراير:

-   1 فبراير: الإيصال المالي للمخزون لكمية قيمتها 2 بتكلفة مقدارها 10.00 دولار أمريكي
-   5 فبراير: الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 13.00 دولارًا أمريكيًا
-   19 فبراير: الإصدار المالي للمخزون لكمية مقدارها 1 بتكلفة متوسط تشغيل قدرها 11 دولارًا أمريكيًا

تم إعداد هذا الصنف بنموذج مخزون ما يرد أولاً يصرف أولاً FIFO، وتم إجراء غلق المخزون اعتبارًا من 28 فبراير. ستتم تسوية حركة الإصدار المالية بمقدار 11 ريالاً سعوديًا مقابل الإيصال المالي بتاريخ 1 فبراير وسيتم إجراء تسوية مقدارها 1 ريال سعودي. عندئذ سوف تحتوي إيصالات المخزون التالية على كميات مخزون مفتوحة:

-   1 فبراير: كمية مقدارها 1 بتكلفة 10.00 دولارات أمريكية
-   5 فبراير: كمية مقدارها 1 بتكلفة 13.00 دولارات أمريكية

لتعيين تكلفة هذين الصنفين إلى 15 ريالاً سعوديًا، استخدم خيار التسوية الفعلي لتسوية الكميات الفعلية المفتوحة اعتبارًا من فترة إغلاق المخزون الأخير. **ملاحظة:** سيكون تاريخ ترحيل حركة التسوية الفعلية هو تاريخ إغلاق المخزون الأخير. لا يمكن تعديل هذا التاريخ.

