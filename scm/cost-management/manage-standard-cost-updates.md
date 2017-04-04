---
title: "إدارة تحديثات التكلفة المعيارية"
description: "يمكن إدارة تحديثات بيانات التكلفة المعيارية باستخدام نهجين مختلفين-منهج أحادي الإصدار ومنهج تناول إصداري."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7e0f0817ff37c82ed98a51f10bcdde7e785a19a3
ms.lasthandoff: 03/31/2017


---

# <a name="manage-standard-cost-updates"></a>إدارة تحديثات التكلفة المعيارية

يمكن إدارة تحديثات بيانات التكلفة المعيارية باستخدام نهجين مختلفين-منهج أحادي الإصدار ومنهج تناول إصداري. 

يستخدم النهج أحادي الإصدار إصدار تكاليف واحد يحتوي على كافة سجلات التكاليف. وتشمل هذه السجلات التكاليف الأصلية وكافة تحديثات التكلفة.
ويستخدم النهج ثنائي الإصدار إصدارًا واحدًا يحتوي على سجلات التكاليف الأصلية وإصدار ثاني يحتوي على سجلات لكافة تحديثات التكلفة. ويتمتع منهج تناول إصداري تكاليف بميزة أساسية ألا وهي التخطيط الواضح لتحديثات التكاليف وتعقبها في إصدار تكاليف منفصل، دون التأثير على إصدار التكاليف الأصلي. ويمكن استخدام النهج ثنائي الإصدار لتحديد التحديثات المتزايدة المتعددة، بحيث يكون لكل تحديث تزايدي إصدار تكاليف منفصل يحتوي على سجلات التكاليف المتزايدة. **المثال** يوضح المثال التالي الكيفية التي يمكن بها استخدام النهج إحادي الإصدار والنهج ثنائي الإصدار لتحديث التكاليف القياسية في بيئة تصنيع. على سبيل المثال، التحديثات التي تعكس الأصناف الجديدة أو تصحيحات الأخطاء. افترض أن إصدار تكاليف واحد يمثل التكاليف القياسية عن السنة الحالية. المعرف الخاص بهذا الإصدار هو 2016-STD. ويحتوي إصدار 2016-STD على التكاليف النشطة الحالية لكافة الأصناف. بالإضافة إلى ذلك، فإنه يحتوي على كافة فئات التكلفة المتعلقة بالتوجيه ومعادلات حساب المصروفات الزائدة التي كانت معروفة في بداية عام 2016. الانحراف 2016 إصدار التكاليف الأصلي.
-   **النهج أحادي الإصدار لتحديثات بيانات التكاليف** − في النهج إحادي الإصدار، يحتوي إصدار التكاليف الأصلية 2016-STD على كافة سجلات التكاليف. تحديثات التكلفة المسجلة في عام 2016 الانحراف وتم تعيينها إلى حالة "معلق". يمكن يدوياً إدخال التكاليف المعلقة للأصناف المشتراة الجديدة، أو يمكن حسابها للأصناف مصنعة لتعكس التصحيحات. عند استخدام منهج أحادي الإصدار، لا تتطلب حسابات شجرة المواد بمصدر بيانات البديلة لأن كافة التكاليف النشطة الموجودة في إصدار التكاليف. بعد تنشيط التكاليف المعلقة، يحتوي إصدار التكاليف الأصلي 2016-STD مرة أخرى على كافة التكاليف النشطة الحالية.
-   **النهج ثنائي الإصداري لتحديثات بيانات التكلفة** − يتطلب النهج ثنائي الإصدار وجود إصدار تكاليف إضافي يحتوي على تحديثات التكلفة فقط. المعرف الخاص بهذا الإصدار هو 2016-STD-CHANGES. ويتم تسجيل تحديثات التكلفة في 2016-STD-CHANGES، ويتم تعيينها إلى حالة "معلقة". وباستخدام النهج ثنائي الإصدار، تتطلب العمليات الحسابية لقائمة مكونات الصنف للتكاليف المعلقة للأصناف المصنعة وجود مصدر بيانات بديل. ويرجع ذلك إلى أن إصدار التكاليف الإضافي 2016-STD-CHANGES يشتمل على مجموعة فرعية واحدة فقط لبيانات التكلفة. ويمكن التعبير عن الاحتياطي بالتكاليف النشطة أو إصدار التكاليف 2016-STD، حيث إن كليهما يقصد به مصدر بيانات التكاليف عندما لا يكون موجودًا في 2016-STD-CHANGES. بعد أن تصبح التكاليف المعلقة نشطة، سوف يشتمل إصدار التكاليف 2016-STD-CHANGES على التكاليف الحالية النشطة التي تعكس التحديثات، حيث لن يطرأ أي تغيير على إصدار التكاليف الأصلي 2016-STD-CHANGES. عند استخدام منهج الإصدارين، يجب أن يتم إعداد سياسات الحظر لإصدار التكاليف الأصلي لمنع التحديثات. ويجب إعداد سياسات الحظر المماثلة لإصدار التكاليف الإضافي، باستثناء "من تاريخ" المحدد والاستخدام الانتقائي لسياسات الحظر للسماح بإجراء التحديثات. ويجب تحديث "من تاريخ" مع كل مجموعة تغييرات لكي يعكس تاريخ التنشيط المجدول.

يستخدم هذا المثال إصدار تكاليف إضافي واحد لإدارة التحديثات عبر عام 2016. يمكن استخدام إصدار تكاليف إضافي واحد أو أكثر، مثل إصدار منفصل لكل مجموعة من التحديثات. عند استخدام أكثر من تكلفة إضافية واحدة، يجب التعبير البديل باعتباره التكاليف النشطة، لأنه يتم توزيع التكاليف النشطة على عدة إصدارات للتكاليف.



