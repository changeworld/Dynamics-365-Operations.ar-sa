---
title: "إدارة تحديثات التكلفة القياسية"
description: "يمكن إدارة تحديثات بيانات التكلفة القياسية باستخدام نهجين مختلفين؛ النهج أحادي الإصدار أو النهج ثنائي الإصدار."
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b64d9e53736fd3b81ee997ed28ccfa62ed7e9ce6
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="manage-standard-cost-updates"></a>إدارة تحديثات التكلفة القياسية

[!include [banner](../includes/banner.md)]

يمكن إدارة تحديثات بيانات التكلفة القياسية باستخدام نهجين مختلفين؛ النهج أحادي الإصدار أو النهج ثنائي الإصدار. 

يستخدم النهج أحادي الإصدار إصدار تكاليف واحد يحتوي على كافة سجلات التكاليف. وتشمل هذه السجلات التكاليف الأصلية وكافة تحديثات التكلفة.

ويستخدم النهج ثنائي الإصدار إصدارًا واحدًا يحتوي على سجلات التكاليف الأصلية وإصدار ثاني يحتوي على سجلات لكافة تحديثات التكلفة. ويتمتع منهج تناول إصداري تكاليف بميزة أساسية ألا وهي التخطيط الواضح لتحديثات التكاليف وتعقبها في إصدار تكاليف منفصل، دون التأثير على إصدار التكاليف الأصلي. ويمكن استخدام النهج ثنائي الإصدار لتحديد التحديثات المتزايدة المتعددة، بحيث يكون لكل تحديث تزايدي إصدار تكاليف منفصل يحتوي على سجلات التكاليف المتزايدة. 

**مثال** 

يوضح المثال التالي الكيفية التي يمكن بها استخدام النهج أحادي الإصدار والنهج ثنائي الإصدار لتحديث التكاليف القياسية في بيئة تصنيع. على سبيل المثال، التحديثات التي تعكس الأصناف الجديدة أو تصحيحات الأخطاء. افترض أن إصدار تكاليف واحد يمثل التكاليف القياسية عن السنة الحالية. المعرف الخاص بهذا الإصدار هو 2016-STD. ويحتوي إصدار 2016-STD على التكاليف النشطة الحالية لكافة الأصناف. بالإضافة إلى ذلك، يحتوي على كافة فئات التكلفة المتعلقة بالتوجيه وكذلك المعادلات الحسابية الخاصة بالمصروفات الزائدة عن الحد التي كانت معروفة في مطلع عام 2016. 2016-STD هو إصدار التكاليف الأصلية.‬

-   **النهج أحادي الإصدار لتحديثات بيانات التكاليف** − في النهج إحادي الإصدار، يحتوي إصدار التكاليف الأصلية 2016-STD على كافة سجلات التكاليف. ‏‫يتم تسجيل تحديثات التكلفة في 2016-STD، ويتم تعيينها إلى حالة "معلقة". يمكن إدخال التكاليف المعلقة يدويًا بالنسبة للأصناف المشتراة الجديدة، أو يمكن حسابها للأصناف المصنعة لتعكس التصحيحات. عند استخدام النهج أحادي الإصدار، لا تتطلب العمليات الحسابية الخاصة بقائمة مكونات الصنف وجود مصدر بيانات بديل، لأن كافة التكاليف النشطة مشمولة في إصدار التكاليف.‬‬ بعد تنشيط التكاليف المعلقة، يحتوي إصدار التكاليف الأصلي 2016-STD مرة أخرى على كافة التكاليف النشطة الحالية.
-   **النهج ثنائي الإصداري لتحديثات بيانات التكلفة** − يتطلب النهج ثنائي الإصدار وجود إصدار تكاليف إضافي يحتوي على تحديثات التكلفة فقط. المعرف الخاص بهذا الإصدار هو 2016-STD-CHANGES. ‏‫يتم تسجيل تحديثات التكلفة في 2016-STD-CHANGES، ويتم تعيينها إلى حالة "معلقة". وباستخدام النهج ثنائي الإصدار، تتطلب العمليات الحسابية لقائمة مكونات الصنف للتكاليف المعلقة للأصناف المصنعة وجود مصدر بيانات بديل.‬ ويرجع ذلك إلى أن إصدار التكاليف الإضافي 2016-STD-CHANGES يشتمل على مجموعة فرعية واحدة فقط لبيانات التكلفة. ويمكن التعبير عن الاحتياطي بالتكاليف النشطة أو إصدار التكاليف 2016-STD، حيث إن كليهما يقصد به مصدر بيانات التكاليف عندما لا يكون موجودًا في 2016-STD-CHANGES. بعد تنشيط التكاليف المعلقة، يحتوي إصدار التكاليف 2016-STD-CHANGES على التكاليف النشطة الحالية التي تعكس التحديثات، بينما يظل إصدار التكاليف الأصلي 2016-STD بدون أي تغيير. وعند استخدام النهج ثنائي الإصدار، يجب إعداد سياسات الحظر الخاصة بإصدار التكاليف الأصلية لمنع إجراء التحديثات. ويجب إعداد سياسات الحظر المماثلة لإصدار التكاليف الإضافي، باستثناء "من تاريخ" المحدد والاستخدام الانتقائي لسياسات الحظر للسماح بإجراء التحديثات. ويجب تحديث "من تاريخ" مع كل مجموعة تغييرات لكي يعكس تاريخ التنشيط المجدول.

‏‫استخدم هذا المثال إصدارًا واحدًا للتكاليف الإضافية لإدارة التحديثات خلال عام 2016. ويمكن استخدام أكثر من إصدار تكاليف إضافي واحد، مثل استخدام إصدار منفصل لكل مجموعة تحديثات. عند استخدام أكثر من تكلفة إضافية واحدة، يجب التعبير البديل باعتباره التكاليف النشطة، لأنه يتم توزيع التكاليف النشطة على عدة إصدارات للتكاليف.






