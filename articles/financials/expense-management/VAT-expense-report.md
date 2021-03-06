---
title: "استرداد ضريبة القيمة المضافة في إدارة المصروفات"
description: "يوضح هذا المقال كيفية استلام المبالغ في حركات ضريبة القيمة المضافة المُستحقة."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: ar-sa
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a>استرداد ضريبة القيمة المضافة في إدارة المصروفات

[!include [banner](../includes/banner.md)]

للحصول على المبالغ عن حركات ضريبة القيمة المضافة المستحقة، يحب أن تقوم الشركة أو المؤسسة بتحديد وتجميع والتحقق من صحة وتقديم معلومات دقيقة. تتضمن هذه العملية العديد من المهام، وبناءً على حجم شركتك يمكنك تضمين العديد من الموظفين أو الأدوار.

لاسترداد ضريبة القيمة المضافة باستخدام إدارة المصروفات، يجب إكمال المتطلبات الأساسية التالية:

- يجب إنشاء الأكواد الضريبية للبلدان/المناطق التي تم تخصيصها لفئات المصروفات.
- يجب إنشاء مجموعة ضريبة مبيعات لكل كود ضريبي.
- يجب إنشاء كود ضريبة مبيعات صنف لكل مجموعة ضريبة مبيعات.

بعد إكمال المتطلبات الأساسية، يتبع الموظفون هذه الخطوات لطلب المبالغ المستردة لحركات ضريبة القيمة المضافة.

1. في تقرير مصروفات، قم بإدخال معلومات ضريبة حول حركات بطاقة الائتمان لتحديد المبالغ المستردة لضريبة القيمة المضافة المُستحقة.
2. تأكد من اكتمال كافة معلومات الضريبة، ثم قم بترحيل تقرير المصروفات.
3. قم بمعالجة المصروفات المؤهلة لاسترداد ضريبة القيمة المضافة الدولية.
4. قم بإرسال بيانات استرداد ضريبة القيمة المضافة إلى مورد جهة خارجية إلى ملف استرداد المبالغ الدولية.
5. قم بمعالجة المصروفات لاسترداد ضريبة القيمة المضافة المحلية.

توفر الأقسام التالية أمثلة تستعرض كيفية إتمام موظفي شركة Contoso لكل خطوة.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>في تقرير مصروفات، قم بإدخال معلومات ضريبة حول حركات بطاقة الائتمان لتحديد المبالغ المستردة لضريبة القيمة المضافة المُستحقة

نانسي، هي مندوبة مبيعات لدى شركة Contoso مقيمة في الولايات المتحدة، ولقد عادت مؤخرًا من جولة مبيعات إلى المملكة المتحدة. خلال رحلتها، تكبدت بعض المصروفات من بطاقة ائتمانها الشخصية فيما يتعلق بالوجبات. يجب على نانسي الآن إنشاء تقرير مصروفات لتسوية المصروفات الخاصة بها.

عندما تقوم نانسي بإدخال المعلومات في تقرير مصروفاتها، تقوم بتحديد **المملكة المتحدة** في حقل **البلد/المنطقة** على صفحة **تحرير تقرير المصروفات**. بعد ذلك تتم تصفية قائمة مجموعات ضريبة المبيعات بحيث تعرض فقط المجموعات التي تنطبق على المملكة المتحدة. قامت نانسي بتحديد مجموعة ضريبة مبيعات **المملكة المتحدة 001**، ثم حددت مجموعة ضريبة مبيعات صنف **الوجبات**. ثم تقوم بإضافة حركة جديدة لتكاليف الإقامة الخاصة بها. ونظرًا لوجود مجموعة ضريبة مبيعات واحدة ومجموعة ضريبة مبيعات صنف لتكاليف الإقامة في المملكة المتحدة، يتم تعبئة المعلومات تلقائيًا في تقرير مصروفات نانسي.

وفقًا لسياسة شركة Contoso، يجب أن تكون كافة المصروفات لها إيصال مطابق. لذلك، عندما تقوم نانسي بحفظ تقرير مصروفاتها، تتسلم رسالة تشير إلى أنه يجب عليها إرفاق إيصال عن كل حركة قامت بإدراجها في تقرير المصروفات الخاص بها. تحققت نانسي من قيامها بإرفاق صورة رقمية لكل إيصال حركة في تقرير مصروفاتها، ثم قامت بتقديم تقريرها للحصول على الموافقة. ثم قامت بإرسال الإيصالات الورقية إلى فريق مُعالجة مكتب الدعم. سوف يُرسل هذا الفريق بيانات استرداد ضريبة القيمة المضافة إلى مورد الجهة الخارجية الذي قدم طلب استرداد ضريبة القيمة المضافة الدولية لشركة Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>تأكد من اكتمال كافة معلومات الضريبة، ثم قم بترحيل تقرير المصروفات

يجب على إيهاب، منسق الحسابات الدائنة لشركة Contoso، إدخال أي معلومات ضريبية غير موجودة في تقرير مصروفات قبل ترحيل هذا التقرير. يقوم بفتح صفحة **تفاصيل تقرير المصروفات** ويطلع على تقرير مصروفات نانسي المعتمد. ثم يقوم إيهاب بفتح تقرير المصروفات لعرض تفاصيل الحركات. يلاحظ إيهاب أن نانسي لم تُدخل مجموعة ضريبة مبيعات صنف لإحدى الحركات. ونظرًا لعدم وجود هذه المعلومات، فلا يستطيع إيهاب ترحيل تقرير المصروفات. لذلك، يطلع إيهاب على صفحة **تكوينات الضريبة** في إدارة المصروفات، ويبحث عن مجموعة ضريبة مبيعات الصنف المناسبة للبلد/المنطقة ونوع الحركة. يٌمكن لإيهاب الآن ترحيل تقرير المصروفات إلى دفتر الأستاذ العام.

عندما يقوم إيهاب بترحيل تقرير المصروفات، يتم إنشاء عنصر عامل ضريبة قيمة مضافة قابلة للاسترداد. يتم تعيين عنصر العمل هذا لأحد أعضاء فريق معالجة مكتب الدعم. يتلقي إيهاب رسالة تؤكد نجاح عملية الترحيل. تسرد هذه الرسالة أيضًا عدد حركات ضريبة القيمة المضافة التي تم تحديدها للاسترداد.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>قم بمعالجة المصروفات المؤهلة لاسترداد ضريبة القيمة المضافة الدولية

تتولى رانيا، وهي عضو فريق المعالجة من مكتب الدعم في شركة Contoso، مسؤولية تأكيد تضمين كافة المعلومات المطلوبة لاسترداد ضريبة القيمة المضافة في تقارير المصروفات. تقوم بفتح صفحة **استرداد ضريبة المصروفات**، وتحديد تقرير المصروفات الذي قدمته نانسي. تتحقق رانيا من إرفاق كافة الإيصالات المطلوبة، فضلًا عن التأكد من إدخال مجموعة ضريبة المبيعات الصحيحة وأكواد ضريبة مبيعات صنف.

عند تلقي رانيا للإيصالات الورقية من نانسي، قامت بالتحقق من صحة الإيصالات الورقية في مقابل الإيصالات الرقمية، ثم قامت بتغيير حالة تقرير المصروفات إلى **جاهز للاسترداد**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>قم بإرسال بيانات استرداد ضريبة القيمة المضافة إلى مورد جهة خارجية إلى ملف استرداد المبالغ الدولية

عندما كانت رانيا جاهزة لإرسال بيانات تقرير المصروفات إلى مورد الجهة الخارجية الذي سوف يقوم بإرسال مرتجعات استرداد ضريبة القيمة المضافة، قامت بفتح صفحة **استرداد ضريبة المصروفات**. تقوم رانيا بتصفية الصفحة بحيث تعرض فقط تقارير المصروفات التي تم وضع علامة **جاهز للاسترداد** عليها. ثم تقوم رانيا بتحديد **ملف** &gt; **تصدير إلى Excel**. يتم تصدير معلومات ضريبة القيمة المضافة من تقارير المصروفات إلى ورقة عمل Microsoft Excel. ترسل رانيا ورقة العمل هذه إلى مورد الجهة الخارجية، وتقوم بتضمين رسالة تفيد بأن الإيصالات الورقية قد تم إرسالها بواسطة البريد.

## <a name="process-expenses-for-domestic-vat-recovery"></a>قم بمعالجة المصروفات لاسترداد ضريبة القيمة المضافة المحلية

يجب على رانيا التحقق من أن حركات تقرير المصروفات مستحقة لاسترداد ضريبة القيمة المضافة، وأن الإيصالات الرقمية مرفقة بالتقارير. لبدء مُعالجة المصروفات المستحقة للاسترداد محليًا، قامت رانيا بفتح صفحة **استرداد ضريبة المصروفات**، ثم قامت بتحديد تقرير المصروفات الذي يتطلب التحقق من صحته. تقوم رانيا بالتحقق من أن الايصالات باسم الشركة بدلًا من الموظف. بالنسبة لاسترداد ضريبة القيمة المضافة، يجب أن تكون الإيصالات باسم الشركة. ثم تؤكد رانيا أنه تم تطبيق أكواد مجموعة ضريبة المبيعات الصحيحة وضريبة مبيعات الصنف الصحيحة.

عند تلقي رانيا إيصالات ورقية، تقوم بتغيير حالة تقرير المصروفات إلى **جاهز للاسترداد**. ثم تقوم بعد ذلك بإيداع المُرتجع لدى هيئة الضرائب المناسبة. في هذه الحالة، فإن هيئة الضرائب المناسبة في الولايات المتحدة هي خدمة الإيرادات الداخلية (IRS).

