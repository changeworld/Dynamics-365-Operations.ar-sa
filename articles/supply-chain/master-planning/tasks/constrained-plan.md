--- 
title: "إنشاء خطة مقيدة"
description: "يوضح هذا الإجراء كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a>إنشاء خطة مقيدة

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة. تضمن الخطة عدم بدء التصنيع قبل أن تتوفر المواد وعدم تعرض الموارد لزيادة في الحجز. 

شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا الإجراء مخصص لمخطط الإنتاج‬.


## <a name="set-up-a-constrained-plan"></a>إعداد خطة مقيدة
1. انقر فوق "التخطيط الرئيسي‬".
2. انقر فوق "التخطيطات الرئيسية‬".
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * على سبيل المثال: StaticPlan  
4. حدد "نعم" في الحقل "قدرة محدودة‬".
5. في الحقل "الحد الزمني للقدرة المحدودة‬"، أدخل "30".
6. قم بتوسيع المقطع "الحدود الزمنية بالأيام‬".
7. حدد "نعم" في الحقل "قدرة".
8. في الحقل "الحد الزمني لجدولة القدرة (بالأيام)‬"، أدخل رقمًا.
    * على سبيل المثال: 60  
9. حدد "نعم" في الحقل "التأخيرات المحسوبة‬‬".
10. في الحقل "الحد الزمني لحساب التأخيرات (بالأيام)‬‬"، أدخل رقمًا.
    * على سبيل المثال: 60  
11. وسّع المقطع "التأخيرات المحسوبة".
12. حدد "نعم" في الحقل "إضافة التأخير المحسوب إلى تاريخ المتطلبات‬".
13. حدد "نعم" في الحقل "إضافة التأخير المحسوب إلى تاريخ المتطلبات‬".
14. حدد "نعم" في الحقل "إضافة التأخير المحسوب إلى تاريخ المتطلبات‬".
15. قم بإغلاق الصفحة.

## <a name="create-a-constrained-plan"></a>إنشاء خطة مقيدة
1. انقر فوق "تشغيل".
2. في حقل "الخطة الرئيسية‬"، أدخل قيمة أو حددها.
    * حدد الخطة التي قمت بإعداد القيود لها.  
3. انقر فوق "موافق".
    * قد يستغرق هذا الأمر بعض الوقت.  
4. انقر فوق "الأوامر المخططة".


