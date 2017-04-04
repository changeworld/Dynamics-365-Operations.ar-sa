---
title: "تكامل الأصول الثابتة"
description: "يمكن تكامل الأصول الثابتة مع دفتر الأستاذ العام وإدارة المخزون وكذلك الحسابات المدينة والدائنة. كما يمكن إعداد أصول ثابتة بحيث تتكامل مع أوامر الشراء."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 9184e98c8afeef496aa709154d3bea26005fe611
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-assets-integration"></a>تكامل الأصول الثابتة

يمكن تكامل الأصول الثابتة مع دفتر الأستاذ العام وإدارة المخزون وكذلك الحسابات المدينة والدائنة. كما يمكن إعداد أصول ثابتة بحيث تتكامل مع أوامر الشراء.

<a name="general-ledger"></a>دفتر الأستاذ العام
--------------

في دفتر الأستاذ العام، يتم عادةً تلخيص قيمة كافة الأصول الثابتة في حسابات رئيسية متعددة مطلوبة للتقارير المالية. ومع ذلك، يمكنك إنشاء الكثير من سجلات الأصول الثابتة في صفحة **الأصول الثابتة**. يمكن أن تتضمن هذه السجلات معلومات مثل سعر الامتلاك والإهلاك والتقييم. ويتم تحديث الحسابات الرئيسية المناسبة في كل مرة تقوم فيها بترحيل حركة لأصل ثابت. ودائمًا ما تقوم الحسابات الرئيسية الخاصة بالأصول الثابتة بعرض القيمة المحدثة للأصول الثابتة.

في صفحة **ملفات تعريف ترحيل الأصول الثابتة**، يمكنك تحديد الحسابات الرئيسية التي يتم ترحيل حركات دفتر الأصول الثابتة إليها. يمكنك أيضًا تحديد أنواع حركات الأصول الثابتة التي يتم ترحيلها إلى الحساب الرئيسي. ويمكنك إنشاء مجموعات متنوعة من حسابات الرئيسية للأصول الثابتة وذلك وفقًا لمستوى التفاصيل المطلوب للأصول الثابتة في دفتر الأستاذ العام. بإمكان الحسابات الرئيسية أن تستند إلى أنواع الحركات والدفاتر وحسابات رئيسية أخرى.

## <a name="inventory-management"></a>إدارة المخزون
في دفتر يومية المخزون للأصول الثابتة، يمكنك إدخال قيمة امتلاك الأصول الثابتة التي تم إنتاجها الكيان القانوني أو إنشائها لصالحها. ثم يمكنك نقل أصناف المخزون إلى الأصول الثابتة كامتلاك أو كجزء من عملية امتلاك. 

ويمكن كذلك الحصول على أصول باستخدام أوامر الشراء. وعندما تحتوي أوامر الشراء على أصناف المخزون التي تم تعيينها كأصول ثابتة، فإن إعداد الخيار **السماح بالحصول على الأصل من الشراء‬** في صفحة **محددات الأصول الثابتة‬** يحدد ما إذا كان سيتم ترحيل استحواذ للأصل الثابت عند ترحيل الفاتورة أم لا. يعتمد تأثير امتلاك أصول ثابتة تحتوي على المخزون على الإعداد للكيان القانوني. 

عندما يصبح أحد أصناف المخزون جزءًا من عملية الاستحواذ على أصول ثابتة من خلال دفتر يومية المخزون أو أمر شراء أو مقترح استحواذ‬، يتم إنشاء حركة استحواذ‬ دفتر الأصول الثابتة. وإذا تضمن استحواذ الدفتر دفترًا مشتقًا، فسيتم أيضًا إنشاء حركة استحواذ الدفتر المشتق. 

إن قواعد الترحيل التي تم إعدادها في صفحة **الترحيل** في إدارة المخزون تتحكم في خفض المخزون عند ترحيل عملية استحواذ. ومع ذلك، فأنت لا تعمل دائمًا على خفض المخزون عند ترحيل فواتير مرتبطة بأصول ثابتة. في بعض الحالات، قد يتم شراء الأصول الثابتة للاستخدام الداخلي. من الأمثلة على ذلك، شراء كمبيوتر محمول لقسم المبيعات. وعند التعامل مع أوامر الشراء، يمكنك استخدام الأصناف التي تم إعدادها لإعادة البيع والاستخدام الداخلي معًا. 

إذا كنت تستخدم حسابات إيصالات وصرف محددة للأصول الثابتة الخاصة بمجموعات الأصناف، فيمكنك استخدام نفس صنف المخزون للمشتريات الداخلية وكمخزون لإعادة البيع. 

يتم إعداد الأصول الثابتة المخصصة للاستخدام الداخلي بحيث يكون لديها حساب من النوع **استلام الأصل الثابت‬**. يتم استخدام نوع الحساب هذا لتعقب استلام الأصل الثابت. عندما تقوم بترحيل فاتورة مورد، فقم باستخدام حساب إيصال الأصول الثابتة إذا تحققت أي من الحالات التالية:

-   بند فاتورة تتضمن أصل ثابت موجود لأغراض داخلية.
-   تم تحديد خانة الاختيار **أصل ثابت جديد؟** لبند إيصال استلام المنتجات التي تم ترحيلها.
-   تم تحديد خانة الاختيار **إنشاء أصل ثابت جديد‬** لبند فاتورة المورد.

يكون هذا الحساب عادة حساب مصروفات. يمكنك إعداد نوع حساب **استلام الأصل الثابت** لمجموعة أصناف أو صنف فردي عن طريق استخدام علامة التبويب **أمر الشراء** في صفحة **مجموعة الأصناف** أو صفحة **الترحيل**.

بطريقة مماثلة، يمكن إعداد الأصول الثابتة المخصصة للاستخدام الداخلي بحيث يكون لديها حساب من النوع **صرف أصل ثابت‬**. يتم استخدام نوع الحساب هذا لإصدار الأصل الثابت إلى المستلم. وعند الحصول على أحد الأصول باستخدام أمر شراء، فإن حساب إصدار الأصل الثابت سيعادل حساب الأصل الثابت المدين. يمكن ترحيل الاستحواذ على الأصول إما عند ترحيل فاتورة مورّد أو عند ترحيل الاستحواذ على الأصول في دفتر اليومية الأصول الثابتة، باستخدام مقترح استحواذ على الأرجح. ويمكنك إعداد نوع الحساب **صرف أصل ثابت** لمجموعة أصناف أو صنف فردي عن طريق استخدام علامة التبويب **المخزون** في صفحة **مجموعة الأصناف** أو صفحة **ترحيل الأصناف**. 

في النهاية، تتحدد الحسابات الرئيسية المستخدمة للترحيل بخيارات تكامل دفتر الأستاذ التي تم تحديدها لمجموعة نموذج الصنف. بالإضافة إلى ذلك، الحسابات الرئيسية المستخدمة تختلف تبعاً لما إذا كان هناك أصل معين لبند أمر الشراء. ويتم اشتقاق الحسابات من ملف تعريف الترحيل لكل مجموعة أصناف. 
**ملاحظة:** لا يمكن تعيين أصل ثابت أو إنشاء أصل ثابت من البند، في حالة وجود حجز مخزون عند ترحيل إيصالات استلام المنتجات. 

تعتمد الحسابات التي يتم ترحيل حركات الأصول الثابتة إليها على عاملين: أحد العاملين هو ما إذا كان قد تم شراء الأصول أو إنشاؤها بواسطة الكيان القانوني والعامل الثاني هو نوع حركة الأصل. 

يعمل نوع الحركة على ربط العملية المخزنية بملف تعريف الترحيل في الأصول الثابتة. ونظرًا لأن ملف تعريف الترحيل في الأصول الثابتة يقوم بتعريف الحسابات التي تم تحديثها، فإن تحديد نوع حركة الأصل الثابت يعد أيضًا، بشكلٍ غير مباشر، تحديدًا للحسابات الرئيسية التي تم ترحيل الحركة إليها. بالنسبة للأصول الثابتة التي تم إنشاؤها أو شراؤها، فعادةً ما يكون نوع الحركة **الاستحواذ‬** أو **تسوية الاستحواذ‬**.

## <a name="accounts-receivable"></a>الحسابات المدينة
تكامل الأصول الثابتة مع الحسابات المدينة يستخدم ملفات تعريف الترحيل التي تم إعدادها في الأصول الثابتة. يتم تنشيط ملفات تعريف الترحيل هذه عندما يتم تحديد أصل ثابت ودفتر ونوع حركة الأصل الثابت لفاتورة عميل قبل ترحيل فاتورة العميل. ولأن الأصول الثابتة لا تعتبر جزءًا من إدارة المخزون، فيجب عليك استخدام صفحة **فاتورة النص الحر** عند بيع أصل ثابت. 

إذا تضمن الدفتر دفترًا مشتقًا، فسيتم إنشاء حركة الدفتر المشتق عند ترحيل فاتورة العميل.

## <a name="accounts-payable"></a>حسابات دائنة
يتم عادة الاستحواذ على الحسابات الدائنة من موردين خارجيين. يمكنك استخدام صفحة **محددات الأصول الثابتة‬** لتحديد ما إذا كان ترحيل عمليات الاستحواذ على الأصول يتم دومًا عند ترحيل فواتير المورّد أو ما إذا كان من الممكن ترحيل عمليات الاستحواذ على الأصول من الأصول الثابتة فقط. عند تمكين بترحيل الاستحواذ على الأصول من الحسابات الدائنة، يتم تحديث حسابات الأصول الثابتة كلما تم ترحيل فاتورة مورّد لعملية استحواذ على أصل ثابت. 

إذا تم إعداد النظام بحيث يتم ترحيل عملية امتلاك أصل عند ترحيل فاتورة، فسيتم ترحيل الحركة وفقًا لملفات تعريف الترحيل التي تم إعدادها في الأصول الثابتة للأنواع المتنوعة من حركات الأصول الثابتة. ويتم التحكم في الترحيل بواسطة الأصل الثابت والدفتر ونوع حركة الأصل الثابت كما تم تحديدها في صفحة **أمر الشراء** قبل ترحيل فاتورة المورّد. 

إذا تضمن الدفتر دفترًا مشتقًا، فسيتم إنشاء حركة الدفتر المشتق عند ترحيل فاتورة المورد.

يتم تنشيط التكامل لكل بند من بنود الأمر من علامة التبويب **الأصول الثابتة** الموجودة في علامة التبويب السريعة **تفاصيل البند** في صفحة **أمر الشراء**. يمكنك إرسال أمر شراء لأصل ثابت للمورد. ومع ذلك، يتم يتم تحديث الأصول الثابتة والحسابات الرئيسية فقط عندما تقوم بترحيل فاتورة المورد استلام الأصل الثابت. ونظرًا لأن أوامر الشراء يمكن أن تتضمن أصناف المخزون فقط، فسيعتمد تأثير امتلاك الأصول الثابتة على المخزون وفقًا لإعداد الكيان القانوني.

## <a name="project-management-and-accounting"></a>إدارة المشاريع والمحاسبة
يمكنك إقران مشروع بأصل يتأثر بالمشروع. كما يمكنك إقران كل مرحلة أو مهمة أو مشروع فرعي بأصل مختلف. يمكن إقران كل سجل المشروع أحد الأصول. يمكنك إنشاء الاقتران عند إدخال رقم أصل ثابت في حقل رقم **الأصل الثابت** في صفحة **المشاريع**. يجب أن يكون المشروع من النوع **داخلي** أو **مشروع تكلفة**. 

يمكنك أيضًا استخدام صفحة **المشاريع** لعرض تفاصيل حول الأصول المقترنة بالمشاريع. لعرض سجل الأصول الثابتة، على علامة التبويب السريعة **الإعداد**، انقر فوق ارتباط الأصل لفتح صفحة **الأصول الثابتة**. ثم انقر فوق **المشاريع**&gt;**كافة المشاريع** لعرض المشروعات المرتبطة بالأصل الثابت. 

يمكنك عادةً إقران أصول ثابتة بالمشاريع عندما تتعلق المشاريع بالعمل أو الصيانة أو إدخال تحسينات على الأصل. وعند اكتمال المشروع، لا يتم إنشاء تعديل بالزيادة للأصل تلقائيًا. وبالتالي، يجب إنشاء التعديل بالزيادة يدويًا إذا كان مطلوبًا. 

لحذف اقتران بين مشروع وأصل، قم بإلغاء تحديد حقل **رقم الأصل الثابت** في صفحة **المشاريع**. 

يمكنك أيضًا تعيين الأصل الثابت الذي تقوم بإنشائه أو تصنيعه كجزء من مشروع تقديري. وفي نهاية المشروع التقديري، يمكنك ترحيل حركة امتلاك الأصل تلقائيًا.

لمزيد من المعلومات، راجع [الحصول على أصول عن طريق الشراء](acquire-assets-procurement.md)

