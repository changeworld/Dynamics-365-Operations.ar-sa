---
title: "تقدير تكلفة أمر الإنتاج"
description: "توفر هذه المقالة معلومات حول تقدير تكلفة الإنتاج. يزودك تقدير تكلفة الإنتاج بتكاليف المواد المرتقبة واستهلاك القدرة لإنتاج صنف في كمية أمر الإنتاج المخطط."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 151445c751b73ea11c2d0e8da2f0e77fcd9e5fbc
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="production-order-cost-estimation"></a>تقدير تكلفة أمر الإنتاج

[!include[banner](../includes/banner.md)]


توفر هذه المقالة معلومات حول تقدير تكلفة الإنتاج. يزودك تقدير تكلفة الإنتاج بتكاليف المواد المرتقبة واستهلاك القدرة لإنتاج صنف في كمية أمر الإنتاج المخطط. 

بعد إنشاء أمر إنتاج، يجب تقدير تكاليف الإنتاج. ويهدف ذلك إلى تقدير استهلاك الأصناف والمسارات فيما يتعلق بعملية الإنتاج، إذ يتم استخدام هذه التقديرات كأساس لعمليات الجدولة والإنتاج التالية.

## <a name="production-cost-estimation"></a>تقدير تكلفة الإنتاج
تستند تقديرات تكاليف الإنتاج إلى المعلومات التالية:

-   كمية أمر الإنتاج
-   المكونات على قائمة مكونات الصنف الخاصة بالإنتاج
-   عمليات التوجيه في مسار الإنتاج.
-   التكاليف غير المباشرة التي تنطبق على المكونات والعمليات
-   بيانات التكلفة النشطة اعتبارًا من تاريخ الحساب

في حال وجود صنف بند وهمي في قائمة مكونات الصنف الخاصة بالإنتاج، تقوم الحسابات بعكس مكونات الصنف الوهمي وعمليات مساره. يمكنك استخدام مهمة التقدير لإعادة حساب التكاليف التقديرية بحيث تعكس المعلومات المحدّثة. على سبيل المثال، قد تكون المعلومات المحدّثة تغييرات في كمية أمر الإنتاج، أو المكونات في قائمة مكونات الصنف الخاصة بالإنتاج، أو عمليات التوجيه في مسار الإنتاج، أو التكاليف غير المباشرة التي تنطبق على هذه المكونات والعمليات، أو بيانات التكلفة النشطة اعتبارًا من تاريخ إعادة الحساب. وتقترح أيضًا حسابات التكلفة التقديرية سعرًا لمبيعات صنف الإنتاج استنادًا إلى منهج التكلفة إضافة إلى زيادة السعر. بإمكان حسابات التكلفة التقديرية أن تنطبق بشكل اختياري على أوامر مرجعية تعكس أوامر إنتاج أخرى ترتبط بأمر الإنتاج.

## <a name="view-the-estimated-costs"></a>اعرض التكاليف التقديرية
بعد تشغيل التقدير، يمكنك عرض النتائج في صفحة **حساب السعر**. يحسب التقدير القيم التالية:

-   **تكلفة الإنتاج** - تكلفة الإنتاج هي البند الأول في التقدير. حيث توضح التكلفة الكاملة لتشغيل أمر الإنتاج وسعر إجمالي المبيعات للإنتاج. وهي مجموع كافة بنود التكلفة في التقدير.
-   **تكاليف المسارات أو الموارد** – تكاليف المسارات أو الموارد هي تكاليف عمليات الإنتاج. وهي تشمل تكلفة عناصر مثل وقت الإعداد ووقت التشغيل والنفقات العامة.
-   **تكاليف المواد** - تكاليف المواد هي تكاليف وأسعار قائمة مكونات الصنف اللازمة لإنتاج الصنف. وقد تم إنشاء هذه التكاليف في السابق وإدخالها في النظام.

## <a name="other-uses-of-cost-estimation"></a>استخدامات أخرى لتقدير التكلفة
يوفر أيضًا تقدير التكلفة المعلومات التالية:

-   عروض أسعار ذات معنى
-   تقديرات لربحية الأمر
-   تقديرات لاستخدام المواد الخام
-   مقارنات بين معلومات التكلفة من عمليات إنتاج سابقة
-   معلومات الميزانية والتنبؤ
-   تقديرات لحجم الإنتاج اللازم للحفاظ على تكلفة معينة




