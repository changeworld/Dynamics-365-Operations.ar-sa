---
title: "إعداد قواعد مطابقة التسوية البنكية"
description: "تشرح هذه المقالة كيفية إعداد قواعد مطابقة التسوية ومجموعات قواعد مطابقة التسوية لمساعدة عملية التسوية البنكية. قواعد مطابقة التسوية هي مجموعة من المعايير المستخدمة لتصفية بنود كشف الحساب البنكي وبنود المستند البنكي أثناء عملية التسوية."
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b48accdc7aaaa65b4c620777546b20056038905b
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-bank-reconciliation-matching-rules"></a>إعداد قواعد مطابقة التسوية البنكية

[!include [banner](../includes/banner.md)]

تشرح هذه المقالة كيفية إعداد قواعد مطابقة التسوية ومجموعات قواعد مطابقة التسوية لمساعدة عملية التسوية البنكية. قواعد مطابقة التسوية هي مجموعة من المعايير المستخدمة لتصفية بنود كشف الحساب البنكي وبنود المستند البنكي أثناء عملية التسوية.

يمكنك إعداد قواعد مطابقة التسوية ومجموعات قواعد مطابقة التسوية لمساعدة عملية التسوية البنكية. وقاعدة مطابقة التسوية هي مجموعة من المعايير المستخدمة لتصفية بنود كشف الحساب البنكي وبنود الحركات البنكية في Microsoft Dynamics 365 for Finance and Operations أثناء عملية التسوية. واستخدم صفحة **قواعد مطابقة التسوية** لإعداد قواعد مطابقة التسوية. ويمكنك إعداد أكثر من قاعدة مطابقة واحدة، ثم إنشاء مجموعة قواعد مطابقة تسوية في صفحة **مجموعات قواعد مطابقة التسوية**. 

> [!NOTE] 
> تستخدم قواعد مطابقة التسوية البنكية إذا كنت قيد تسوية كشف بنكي إلكتروني باستخدام تسوية بنكية متقدمة. 

في صفحة **قواعد مطابقة التسوية**، يمكنك تحديد الإجراءات ومعايير التحديد التي تُستخدم عند تشغيل قاعدة المطابقة. ‏‫في مجموعة حقول **الإجراءات‬‏‫**‬‏‫، حدد الإجراء الذي سيتم تنفيذه عند تشغيل قاعدة المطابقة أثناء عملية التسوية.  

> [!NOTE] 
> يحدد الخيار الذي تختاره، الحقول التي تظهر.‬

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **الإجراء**                         |                                                                                                                                                                                                                                                                                                               | **توفر معايير الاختيار عند تحديد إجراء**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **مطابقة مع مستند البنك**       | قم بإنشاء معايير لتحديد كيفية مطابقة بنود المستندات البنكية وبنود الكشف البنكي عند تشغيل قاعدة المطابقة من صفحة **ورقة عمل التسوية البنكية**. ويتم تحديد بنود الحركة طبقًا للإعداد الإضافي للمعايير في علامات التبويب السريعة.                                | **الخطوة 1: تعريف قاعدة المطابقة** – حدد المعايير لتحديد كشوف الحسابات البنكية التي تجب مطابقتها مع الحركات البنكية في Finance and Operations. **الخطوة 2 (اختياري): تحديد بنود كشف الحساب لتشغيل قواعد المطابقة مقابلها:** تطبيق عامل تصفية على أي بند كشف حساب لتشغيل القواعد مقابله.                                                                                                                                                                                                                                                                                                               |
| **مسح بنود كشف الحساب المعكوسة** | قم بإنشاء معايير لتحديد كيف ينبغي إزالة بنود كشف الحساب المعكوس‬ من صفحة **ورقة عمل التسوية البنكية** عند تشغيل قاعدة المطابقة. ويتم استخدام هذا الخيار عندما يقوم البنك بارتكاب خطأ، ويكون هناك بندين لكشوف بنكية مدرجة في الكشف البنكي المستورد، وتجب تسوية البنود. | **الخطوة 1**:**البحث عن بنود كشف الإلغاء**– إضافة معايير التحديد لتحديد بنود كشف الحساب البنكي المعكوس. على سبيل المثال، لتحديد الشيكات فقط، حدد **كود الحركة البنكية** في حقل الحقل، وحدد علامة زائد (+) في حقل **عامل التشغيل**، ثم أدخل **الشيكات** في حقل القيمة. **الخطوة 2: البحث عن بنود كشف الحساب الأصلي**‎ - يمكنك إضافة معايير تحديد لمطابقة بنود المستند البنكي ببنود كشف الحساب البنكي. **الخطوة 3: البحث عن الحركات البنكية في Finance and Operations**– يمكنك إضافة معايير تحديد لمطابقة الحركات البنكية في Finance and Operations ببنود كشف الحساب البنكي. |
| **وضع علامة على الحركات الجديدة**          | قم بإنشاء معايير لتحديد الكيفية التي ينبغي بها وضع علامات على الحركات الجديدة في صفحة **ورقة عمل التسوية البنكية** عند تشغيل قاعدة المطابقة.                                                                                                                                                                 | **الخطوة 1: البحث عن بنود الكشف**– إضافة حقول تحديد لتحديد بنود كشف الحساب البنكي التي ينبغي تحديدها من صفحة **ورقة عمل التسوية البنكية**. **الخطوة 2: البحث عن Finance and Operations**– يمكنك إضافة معايير التحديد للبحث عن بنود المستند البنكي. إذا لم يتم العثور على أي مستند بنكي، سيتم وضع علامة على بند الكشف باعتباره حركة جديدة.                                                                                                                                                                                                                                             |









