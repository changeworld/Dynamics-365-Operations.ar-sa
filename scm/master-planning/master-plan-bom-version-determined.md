---
title: "تحديد إصدار قائمة مكونات الصنف"
description: "أثناء تحديد إجمالي المكونات المطلوبة للطلب، إذا تم تعيين نوع الأمر الافتراضي لصنف على الإنتاج، فإن محرك التخطيط يقوم بإيجاد إصدار قائمة مكونات صنف صالح يستند إلى الموقع."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 134b9f7fd46b5326eb6f1f4fec4ed2bda8a8576a
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="determine-the-bom-version"></a>تحديد إصدار قائمة مكونات الصنف

[!include[banner](../includes/banner.md)]


أثناء تحديد إجمالي المكونات المطلوبة للطلب، إذا تم تعيين نوع الأمر الافتراضي لصنف على الإنتاج، فإن محرك التخطيط يقوم بإيجاد إصدار قائمة مكونات صنف صالح يستند إلى الموقع. 

يكون بُعد الموقع معروفًا دائمًا ويتم تحديده في حركة الطلب. ويتم استخدام العملية التالية تحديد إصدار قائمة مكونات الصنف المراد استخدامه:

-   إذا تم تحديد إصدار قائمة مكونات الصنف للصنف في موقع الطلب، فإنه يتم استخدام قائمة مكونات الصنف الخاصة بالموقع.
-   وإذا لم يتم تحديد أي إصدار لقائمة مكونات الصنف الخاصة بالموقع لأي صنف في موقع الطلب، فإنه يتم استخدام قائمة مكونات صنف عامة. لا تحدد شجرة المواد العامة موقعًا، وهي صالحة للعديد من المواقع. وإذا كانت هناك قائمة مكونات صنف عامة، فإنه يتم استخدامها.
-   في حالة عدم وجود إصدار شجرة مواد عامة لاستخدامها، فإن تحديد إجمالي المكونات المطلوبة للطلب يتوقف عند هذه النقطة.

يجب أن يتوافق إصدار شجرة المواد الصالح مع المعايير المطلوبة للتاريخ والكمية، سواءً كان لموقع بعينه أو عامًا.





