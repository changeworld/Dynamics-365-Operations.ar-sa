--- 
title: "إنشاء كائنات تكلفة  "
description: "يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة في Dynamics 365 for Finance and Operations, Enterprise edition إلى محاسبة التكاليف عبر موصل بيانات."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
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
ms.openlocfilehash: 79cb18717c6b42ef0307f304d28902dd66f0f932
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-objects"></a>إنشاء كائنات تكلفة   

[!include[task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة في Dynamics 365 for Finance and Operations, Enterprise edition إلى محاسبة التكاليف عبر موصل بيانات. تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء. يتم استخدام هذا الإجراء لميزة محاسبة التكاليف التي تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.


## <a name="create-new-cost-objects"></a>إنشاء كائنات تكلفة جديدة
1. انتقل إلى محاسبة التكاليف > الأبعاد > أبعاد كائن التكلفة.
2. انقر فوق "جديد".
3. في حقل "الاسم"، اكتب قيمة.
4. في الحقل "موصل البيانات لأعضاء البُعد‬"، أدخل قيمة أو حددها.
5. في وصف الحقل، اكتب قيمة.
6. انقر فوق "حفظ".

## <a name="configure-the-data-connector"></a>تكوين موصل البيانات
1. انقر فوق "تكوين موفر عضو البُعد".
    * حدد CostCenter لاستيراد بُعد CostCenter إلى محاسبة التكاليف.  
2. حدد "مركز التكلفة" في حقل "اسم البُعد".
3. انقر فوق "موافق".

## <a name="import-cost-centers"></a>استيراد مراكز التكلفة
1. انقر فوق "استيراد أعضاء الأبعاد".
2. انقر فوق "موافق".

## <a name="view-the-imported-cost-centers"></a>عرض مراكز التكلفة المستوردة
1. انقر فوق "عرض أعضاء الأبعاد".

