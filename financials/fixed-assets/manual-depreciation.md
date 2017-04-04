---
title: "الإهلاك اليدوي"
description: "توفر هذه المقالة نظرة عامة على أسلوب الإهلاك اليدوي."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 96d0ae3be15c792b04eae901577b160d1532801c
ms.lasthandoff: 03/31/2017


---

# <a name="manual-depreciation"></a>الإهلاك اليدوي

توفر هذه المقالة نظرة عامة على أسلوب الإهلاك اليدوي.

عند تحديد ملف تعريف إهلاك أصول ثابتة ثم تحديد **يدوي** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، فإنه يتم تحديد إهلاك الأصول الثابتة المعينة لملف تعريف الإهلاك هذا بالنسبة المئوية التي يتم إدخالها لكل فترة زمنية في سنة التقويم. ويتم ترحيل الفترات الزمنية التي تقوم بإعداد النسب المئوية لها وفقًا للقيمة التي تحددها في حقل **تكرار الفترة** في علامة التبويب السريع **عام** في صفحة **ملفات تعريف الإهلاك**. وفيما يلي القيم التي يمكن تحديدها:

-   سنويًا
-   شهريًا
-   ربع سنوي
-   نصف سنوي
-   يوميًا

بعد تحديد تكرار الفترة، انقر فوق **الجداول اليدوية**، وقم بإعداد نسب مئوية لكل فترة زمنية منفصلة للترحيل. وتحدد الجداول اليدوية بالاشتراك مع فترات الترحيل مبلغ الإهلاك، كما هو موضح في الأمثلة الواردة لاحقًا في هذا المقال. ويتم حساب الإهلاك اليدوي دومًا كنسبة مئوية من سعر الاستحواذ. وبالنسبة للإهلاك اليدوي، يجب ألا تبلغ النسب المئوية المدخلة في الفترات الزمنية للإهلاك 100 بالمائة. الإهلاك اليدوي عبارة عن طريقة إهلاك مرنة وعادةً ما تُستخدم لتحديد ملف تعريف إهلاك استثنائي في صفحة **الدفاتر**، مثل الإهلاك غير الدوري لأغراض خاصة (على سبيل المثال، الضرائب).

## <a name="examples"></a>أمثلة
سعر الاستحواذ: 11,000.00 قيمة الخردة المتوقعة: 1,000.00 يعرض الجدول التالي الفترات الزمنية والنسبة المئوية التي تقوم بإعدادها في صفحة **جداول ملف تعريف إهلاك الأصول الثابتة**.

| رقم الفترة | النسبة المئوية |
|-----------------|------------|
| 1               | 10.00      |
| 2               | 50.00      |
| 3               | 8.00       |

يتم حساب الإهلاك حسب الفترة كما هو موضح في الجدول التالي.

|  رقم الفترة | حساب مبلغ الإهلاك السنوي | صافي القيمة الدفترية بنهاية الفترة |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11,000 – 1,000) × 10% = 1,000                | 10,000 (11,000 – 1,000)                   |
| 2                | (11,000 – 1,000) × 50% = 5,000                | 5,000 (10,000 – 5,000)                    |
| 3                | (11,000 – 1,000) × 8% = 800                   | 4,200 (5,000 – 800)                       |

إذا قمت بتحديد **شهري** في حقل ** تكرار الفترة**، فقد قمت بإعداد 12 فترة زمنية لجدول يدوي. يبين الجدول التالي مبالغ الإهلاك للفترتين الأولى.

| الفاصل الزمني | مبلغ الإهلاك            |
|----------|--------------------------------|
| يناير  | (11,000 – 1,000) × 10% = 1,000 |
| فبراير | (11,000 – 1,000) × 50% = 5,000 |

إذا قمت بتحديد **نصف سنوي** في * الفترة تردد * * الميدان * *، قم بإعداد فترات جدول يدوي اثنين. يبين الجدول التالي مبالغ الإهلاك للفترتين الأولتين.

| الفاصل الزمني    | مبلغ الإهلاك            |
|-------------|--------------------------------|
| 30 يونيو     | (11,000 – 1,000) × 10% = 1,000 |
| 31 ديسمبر | (11,000 – 1,000) × 50% = 5,000 |

لا يكون مجموع النسب المئوية لكافة الفترات الزمنية أن 100. ومع ذلك، تتلقى رسالة إذا القيمة في **النسبة المئوية التراكمية** الحقل على **جداول ملف تعريف إهلاك الأصل الثابت** الصفحة ليست **100**.

