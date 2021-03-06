---
title: "معلمات إدارة المصروفات"
description: "تتحكم المعلمات التالية بالسلوك في إدارة المصروفات."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 22f766b780d10d4fc615660990729f008007787a
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="expense-management-parameters"></a>معلمات إدارة المصروفات

[!include [banner](../includes/banner.md)]

-----------------------------

تتحكم المعلمات بالسلوك العام في إدارة المصروفات.

### <a name="general"></a>عام

| **الحقل**                                                | **الوصف**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **المعدل القياسي للمسافة بالميل**                             | أدخل معدل التعويض لمصروفات المسافة المقطوعة بالميل. وسيتم ضرب المعدل في المسافة المقطوعة بالميل التي تم إدخالها في المصروفات لحساب المبلغ المسترد لمصروفات السفر.                       |
|**المصروفات الشخصية مدفوعة بواسطة**                             | حدد الشخص المسؤول عن سداد أية مبالغ خاصة بحركات بطاقة الائتمان والمصنفة كشخصية.                                                                                                     |
|**عرض تقرير المصروفات الكامل في طريقة التصفح للخلف**               | حدد هذا الخيار لإظهار كافة المصروفات لتقرير مصروفات عند عرض التفاصيل الخاصة بالمستند الأصلي لقسيمة معينة تم إنشاؤها عند ترحيل تقرير المصروفات.              |
|**التخويل المسبق للسفر إلزامي**                 | حدد هذا الخيار للمطالبة بإرسال طلب سفر والموافقة عليه قبل أن يتمكن الموظف من إرسال تقرير المصروفات.                                                                    |
|**السماح بتحرير التوزيعات قبل الترحيل**            | حدد ما إذا كان يمكن تحرير توزيعات تقرير مصروفات قبل الترحيل.                                                                                                                 |
|**تقييم سياسات إدارة المصروفات**                     | حدد متى يتم تقييم المصروفات لتحديد ما إذا كانت سياسة المصروفات قد تعرضت لانتهاك. يمكن التحقق من المصروفات لمعرفة ما إذا كانت قد تعرضت لانتهاكات عند إدخال بند مصروفات وحفظه أو عند إرسال المصروفات للموافقة عليها. سيتم التدقيق في قواعد السياسة الخاصة بعمليات الاستلام عند حفظ بند المصروفات.                   |
|**السماح بأسطر المصروفات المشتركة بين الشركات الشقيقة**                         | حدد ما إذا كان سيتم السماح بإدخال المصروفات لكيانات قانونية أخرى داخل تقرير مصروفات.                                                                                                          |
|**السماح بتحرير سعر الصرف لمصروفات بطاقة الائتمان** | حدد هذا الخيار للسماح للمستخدم بتحرير سعر الصرف لمصروفات بطاقة الائتمان المستوردة.                                                                        |
|**حقول التدرج الهرمي متعدد المستويات المطلوب عرضها**                  | حدد حقول المعتمد التي يجب عرضها عند ضبط نوع تعيين سير عمل تقرير المصروفات ليكون التدرج الهرمي وعند ضبط اختيار التدرج الهرمي لاستخدام التدرج الهرمي للموافقة متعددة المستويات للمصروفات‬. عند استخدام التدرج الهرمي للموافقة متعددة المستويات لسير العمل، سوف تظهر الحقول المحددة وستكون قابلة للتحرير في تقرير المصروفات. |
|**إدخال رقم بطاقة ائتمان الموظف (تحديث يوليو 2017)**     | حدد ما إذا كان يمكن إدخال عدد يتكون من 15 أو 16 حرفًا وحفظه في حقل **معرف البطاقة** الموجود في صفحة **بطاقات الائتمان** لموظف.                                                                          |

### <a name="financial"></a>مالي

| **الحقل**                                                            | **الوصف**     |
|----------------------------------------------------------------------|------------------------------------|
|**‏‏اسم دفتر أستاذ اليومية**                                         | حدد اسم دفتر يومية دفتر الأستاذ المقرر ترحيل تقارير المصروفات المعتمدة إليه.            |
|**تمكين استرداد الضريبة من المصروفات**                                  | حدد هذا الخيار لتمكين استرداد ضريبة المصروفات للمصروفات المستحقة. لا يمكن تمكين هذا الخيار إذا تم تمكين ضريبة مبيعات الولايات المتحدة وقواعد ضريبة الانتفاع.      |
|**ترحيل السلفة النقدية مباشرةً**                                     | حدد هذا الخيار لترحيل سلفة نقدية تمت الموافقة عليها‬ عند اكتمال عملية الدفع والتحويل‬. إذا لم يكن هذا الخيار محددًا، فستنشئ عملية الدفع والتحويل دفتر يومية عامًا غير مرحل. |
|**تصحيح التاريخ المحاسبي أثناء الترحيل**                             | حدد هذا الخيار لتحديث التاريخ المحاسبي عند ترحيل المصروفات إذا كانت الفترة الحالية قيد الانتظار أو مقفلة. سيتم ضبط التاريخ المحاسبي إلى الفترة المفتوحة التالية.   |
|**السماح بتجميع الحركات بناءً على الحساب المقابل المحدد في طريقة الدفع**      | حدد هذا الخيار لتلخيص حركات المصروفات لتقرير مصروفات، استنادًا إلى الحساب المقابل المحدد في طريقة الدفع للمصروفات.   
|**الضريبة مضمنة**                                                   | حدد هذا الخيار لتضمين ضريبة المبيعات في مبلغ المصروفات بشكل افتراضي.             |
|**إصدار الالتزامات عند إقفال طلبات السفر**            | حدد هذا الخيار لإصدار أموال الالتزامات عند إقفال طلب سفر تمت الموافقة عليه.                                                                                   |
|**السماح بإرسال طلب السفر بشأن تجاوز الموازنة لسجل الموازنة وموازنة المشروع** | حدد هذا الخيار للسماح للموظفين بتقديم طلبات السفر للموافقة التي تتجاوز إما الموازنة المسموح بها التي تم تعيينها في سجل الموازنة أو الموازنة المسموح بها لمشروع.            |
|**السماح بإرسال تقرير المصروفات بشأن تجاوز الموازنة لسجل الموازنة وموازنة المشروع**    | حدد هذا الخيار للسماح للموظفين بتقديم طلبات تقارير المصروفات للموافقة التي تتجاوز إما الموازنة المسموح بها التي تم تعيينها في سجل الموازنة أو الموازنة المسموح بها لمشروع.                |
|**السماح بالموافقة على تقرير المصروفات على تجاوز الموازنة لسجل الموازنة فقط**                | حدد هذا الخيار للسماح للمعتمدين بالموافقة على تقارير المصروفات التي تتجاوز الموازنة المسموح بها التي تم تعيينها في سجل الموازنة.                                                                       |

### <a name="per-diem"></a>المصروف اليومي

| **الحقل**                             | **الوصف**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**الحد الأدنى للساعات في المصروف اليومي**           | أدخل الحد الأدنى الافتراضي لعدد الساعات التي يجب أن يعمل خلالها الموظف خلال اليوم لكي يتأهل لاستلام مصروف يومي لمصروفات السفر ذات الصلة.  تُستخدم هذه القيمة فقط كقيمة افتراضية للحقل "الحد الأدنى للساعات"‬ من مستويات معدل المصروفات اليومية.‬                                                                                      |
|**النسبة المئوية للوجبة**                          | أدخل النسبة المئوية الافتراضية للمصروف اليومي للوجبات المستخدم في اليومين الأول والأخير لمصروفات السفر عند تعيين الحقل **حساب خفض عدد الوجبات عن طريق‬** إلى **نوع الوجبات اليومية** أو **عدد الوجبات لكل يوم**. قد يكون يوم العمل في اليومين الأول والأخير أقصر من يوم عمل قياسي. وبالتالي، قد يختلف مبلغ المصروف اليومي في هذه الأيام عن المبلغ القياسي. إذا تم تعيين النسبة المئوية إلى 0، فستكون خصومات اليومين الأول والأخير 0.00. |
|**النسبة المئوية للفندق**                        | أدخل النسبة المئوية الافتراضية للمصروف اليومي للفنادق التي يتم استخدامها في اليومين الأول والأخير من مصروفات السفر ذات الصلة. قد يكون يوم العمل في اليومين الأول والأخير أقصر من يوم عمل قياسي. وبالتالي، قد يختلف مبلغ المصروف اليومي في هذه الأيام عن المبلغ القياسي. إذا تم تعيين النسبة المئوية إلى 0، فستكون خصومات اليومين الأول والأخير 0.00.                                              |
|**النسبة المئوية للعناصر الأخرى**                        | أدخل النسبة المئوية الافتراضية للمصروف اليومي للمصروفات المتنوعة التي يتم استخدامها في اليومين الأول والأخير من مصروفات السفر ذات الصلة. قد يكون يوم العمل في اليومين الأول والأخير أقصر من يوم عمل قياسي. وبالتالي، قد يختلف مبلغ المصروف اليومي في هذه الأيام عن المبلغ القياسي. إذا تم تعيين النسبة المئوية إلى 0، فستكون خصومات اليومين الأول والأخير 0.00.                                                                                                     |
|**خفض في نسبة الإفطار** | أدخل المبلغ الذي سيتم خفضه من المصروف اليومي لوجبة الإفطار. على سبيل المثال، إذا تناول أحد الموظفين وجبة إفطار مجانية، فقد تريد خفض مبلغ المصروف اليومي بنسبة 10 بالمائة.                               |
|**خفض في نسبة الغداء**    | أدخل المبلغ الذي سيتم خفضه من المصروف اليومي لوجبة الغداء. على سبيل المثال، إذا تناول أحد الموظفين وجبه غداء مجانية، فقد تريد خفض مبلغ المصروف اليومي بنسبة 15 بالمائة.                                       |
|**خفض نسبة العشاء**   | أدخل المبلغ الذي سيتم خفضه من المصروف اليومي لوجبة العشاء. على سبيل المثال، إذا تناول أحد الموظفين وجبه عشاء مجانية، فقد تريد خفض مبلغ المصروف اليومي بنسبة 25 بالمائة.                                     |
|**حساب خفض عدد الوجبات عن طريق**         | حدد الطريقة التي يجب أن يستخدمها النظام لحساب خفض عدد الوجبات للمصروفات اليومية عن طريق تحديد ما إذا كان التخفيض يستند إلى نوع الوجبة في الرحلة أو في اليوم، أو إذا كان التخفيض يستند إلى عدد الوجبات المسموح بها في اليوم.|
|**تقريب المصروف اليومي**                  | حدد نوع التقريب الذي يتم استخدامه للمصروفات اليومية. إذا حددت التقريب العادي، فإن أي مصروفات يومية بمبلغ 0.50 ستقرّب لأعلى إلى 1.00 وأية مصروفات يومية بمبلغ أقل من 0.50 ستقرّب لأسفل إلى 0.00.                                                                                              |
|**أساس احتساب المصروفات اليومية**         | حدد ما إذا كانت مبلغ المصروف اليومي يستند إلى يوم تقويم أو فترة 24 ساعة.       |

### <a name="fax-cover-pages"></a>صفحات تغطية الفاكس

| **الحقل**                      | **الوصف**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **الإرشادات**                   | أدخل الإرشادات التي يجب على الموظفين اتباعها عند إنشاء صفحة غلاف لفاكس يتم استخدامه لإرسال الإيصالات المرتبطة بتقرير مصروفات. انقر فوق زر **الترجمات** لإدخال نص بلغة محددة سيتم عرضه استنادًا إلى لغة المستخدم. |
|**معرف المستخدم (معلومات الكود الشريطي)** | حدد هذا الخيار لتخزين المعرف الفريد للموظف في الكود الشريطي الذي يتم استخدامه في صفحة غلاف الفاكس.                 |
|**الكود الشريطي**                      | حدد الكود الشريطي الذي يتم استخدامه على صفحة الغلاف للفاكس. يتم دعم الأكواد الشريطية 39 و128 في إدارة المصروفات.               |

### <a name="anti-corruption"></a>مكافحة الفساد

|                 <strong>الحقل</strong>                 |                                                                                                                                                                                            <strong>الوصف</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>عرض شهادة تصديق مكافحة الفساد</strong>  | حدد هذا الخيار لعرض نص مكافحة الفساد عند إنشاء تقرير مصروفات جديد. يمكن عندئذٍ تمكين فئات مصروفات خاصة سوف تحتاج إلى تحديد شهادة مكافحة الفساد في تقرير المصروفات. على سبيل المثال، قد تتطلب فئة هدايا مرتبطة بمصروفات حكومية رسمية تأكيد الموظف أن المصروفات تلبي سياسة الشركة المتعلقة بالمسؤولين الحكوميين. |
| <strong>رسالة مكافحة الفساد للمرسِل</strong> |                                                                                             أدخل النص الذي سيتم عرضه للموظف عند إنشاء تقرير مصروفات جديد. انقر فوق زر <strong>الترجمات</strong> لإدخال نص بلغة محددة سيتم عرضه استنادًا إلى لغة المستخدم.                                                                                             |
| <strong>رسالة مكافحة الفساد للمعتمد</strong>  |                                                                                             أدخل النص الذي سيتم عرضه للمعتمد عند إنشاء تقرير مصروفات جديد. انقر فوق زر <strong>الترجمات</strong> لإدخال نص بلغة محددة سيتم عرضه استنادًا إلى لغة المستخدم.                                                                                             |


