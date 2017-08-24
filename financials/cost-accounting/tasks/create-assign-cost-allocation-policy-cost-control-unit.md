--- 
title: "إنشاء وتعيين سياسة تخصيص التكلفة إلى وحدة التحكم في التكلفة"
description: "استخدم هذا الإجراء لإنشاء سياسة توزيع التكلفة‬ والقواعد المناظرة وتعيينها إلى وحدة التحكم بالتكاليف."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 82319d8d9c7b567f98dfd0e591cb99079fb577b7
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>إنشاء وتعيين سياسة تخصيص التكلفة إلى وحدة التحكم في التكلفة

[!include[task guide banner](../../includes/task-guide-banner.md)]

استخدم هذا الإجراء لإنشاء سياسة توزيع التكلفة‬ والقواعد المناظرة وتعيينها إلى وحدة التحكم بالتكاليف. يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.


## <a name="create-a-policy"></a>إنشاء سياسة
1. انتقل إلى محاسبة التكاليف > السياسات > سياسات توزيع التكاليف.
2. انقر فوق "جديد".
3. في الحقل "اسم السياسة"، اكتب قيمة.
4. في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.
    * حدد "المؤسسة".  
5. في الحقل "البعد الإحصائي"، أدخل قيمة أو حددها.
6. انقر فوق "حفظ".

## <a name="create-allocation-rules"></a>إنشاء قواعد التوزيع
1. انقر فوق "جديد".
2. في القائمة، قم بوضع علامة للصف المحدد.
3. في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.
4. حدد "إجمالي" في حقل "سلوك التكلفة".
5. في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.
6. انقر فوق "جديد".
7. في القائمة، قم بوضع علامة للصف المحدد.
8. في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.
9. حدد "إجمالي" في حقل "سلوك التكلفة".
10. في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.
11. انقر فوق "جديد".
12. في القائمة، قم بوضع علامة للصف المحدد.
13. في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.
14. حدد "إجمالي" في حقل "سلوك التكلفة".
15. في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.
    * تابع حتى إنشاء كافة القواعد.  
16. انقر فوق "حفظ".

## <a name="assign-the-policy-to-a-cost-control-unit"></a>تعيين السياسة إلى وحدة التحكم بالتكاليف
1. انقر فوق "تعيينات السياسة" لوحدة التحكم بالتكاليف.
2. انقر فوق "جديد".
3. في القائمة، قم بوضع علامة للصف المحدد.
4. أدخل تاريخًا في الحقل "صالح بدءًا من تاريخ المحاسبة‬‬".
    * القواعد لها تاريخ سريان. باستطاعة المستخدم أو النظام إنهاء تاريخ صلاحية القواعد إذا تم إنشاء إصدار أحدث.  
5. في الحقل "وحدة التحكم بالتكاليف‬"، أدخل قيمة أو حددها.
6. انقر فوق "حفظ".

