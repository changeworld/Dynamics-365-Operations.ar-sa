---
title: "المتوسط المرجح مع القيمة الفعلية ووضع العلامات"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e4d753a4c267058f29443de3ff73aebc2a7d24f2
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="weighted-average-with-physical-value-and-marking"></a>المتوسط المرجح مع القيمة الفعلية ووضع العلامات

[!include[banner](../includes/banner.md)]




عند تشغيل إقفال المخزون، تتم تسوية كافة الإيصالات مقابل إصدار ظاهري يتضمن إجمالي الكمية المستلمة والقيمة. ويكون للإصدار الظاهري إيصالاً ظاهريًا تتم تسوية الإصدارات منه. في هذه الطريقة، تحصل كافة الإصدارات على نفس متوسط التكلفة. يظهر الإصدار الظاهري والإيصال الظاهري كتحويل ظاهري يُسمى "تحويل إقفال مخزون المتوسط المرجح".

في حالة وجود إيصال واحد فقط، تتم تسوية كافة الإصدارات من هذا الإيصال ولن يتم إنشاء التحويل الظاهري. 

عند استخدام المتوسط المرجح، يمكنك تمييز حركات المخزون بحيث تتم تسوية إيصال الصنف مقابل إصدار محدد بدلاً من استخدام قاعدة المتوسط المرجح. 

نوصي بإجراء إقفال المخزون شهريًا عند استخدام نموذج مخزون المتوسط المرجح. 

يتم حساب طريقة تكلفة مخزون المتوسط المرجح عن طريق اتباع المعادلة التالية:‬
-   المتوسط المرجح = (Q1\*P1 +‏ Q2\*P2 +‏ Qn\*Pn) /‏ (Q1 +‏ Q2 +‏ Qn)

حركات المخزون التي تترك مشكلات المخزون. يتضمن هذا أوامر المبيعات، ودفاتر يومية المخزون، وأوامر الإنتاج، التي تحدث بسعر تكلفة مقدر في تاريخ الترحيل. ويطلق أيضًا على سعر التكلفة المقدر هذا المتوسط الساري. في وقت إقفال المخزون، يقوم النظام بتحليل حركات المخزون للفترات السابقة والحالية وتحديد أي من قواعد الإقفال التالية ينبغي استخدامها.
-   تسوية مباشرة
-   تسوية ملخصة

التسويات هي ترحيلات إقفال المخزون التي تعمل على ضبط الإصدارات إلى المتوسط المرجح الصحيح بدءًا من تاريخ الإقفال. توضح الأمثلة التالية تأثير استخدام المتوسط المرجح مع خمسة تكوينات مختلفة:
-   التسوية المباشرة للمتوسط المرجح بدون استخدام الخيار تضمين القيمة الفعلية
-   التسوية الملخصة للمتوسط المرجح بدون تحديد الخيار تضمين القيمة الفعلية
-   التسوية المباشرة للمتوسط المرجح باستخدام الخيار تضمين القيمة الفعلية
-   التسوية الملخصة للمتوسط المرجح باستخدام الخيار تضمين القيمة الفعلية
-   المتوسط المرجح مع وضع علامة

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>التسوية المباشرة للمتوسط المرجح بدون تضمين القيمة الفعلية
تعد قاعدة التسوية المباشرة هي نفسها المستخدمة للمتوسط المرجح في الإصدارات السابقة. وسوف يقوم النظام بالتسوية مباشرة بين عمليات الاستلام والإصدارات. ويستخدم النظام قاعدة التسوية المباشرة هذه في مواقف محددة بعينها:
-   تم ترحيل استلام واحد وإصدار واحد أو أكثر في الفترة
-   تم ترحيل الإصدارات في الفترة فقط ويضم المخزون كمية حالية من الأصناف من الإقفال السابق

في السيناريو في الأقسام التالية، تم ترحيل إصدار وإيصال تم تحديثهما ماليًا. خلال إقفال المخزون، يتم من خلال النظام تسوية الاستلام مباشرةً في مقابل الإصدار، مع عدم لزوم إجراء تسوية لسعر التكلفة الخاص بالإصدار. يتم توضيح الحركات التالية في الرسوم البيانية.
-   1أ. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 5 بتكلفة مقدارها 10.00 دولارات أمريكية لكل وحدة
-   1ب. الاستلام المالي للمخزون الذي تم تحديثه لكمية قيمتها 5 بتكلفة مقدارها 10.00 دولارات أمريكية لكل وحدة
-   1أ. الإصدار الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 2 بتكلفة مقدارها 10.00 دولارات أمريكية لكل وحدة
-   2ب. الإصدار المالي للمخزون الذي تم تحديثه لكمية قيمتها 2 بتكلفة مقدارها 10.00 دولارات أمريكية لكل وحدة
-   3. تم إجراء إقفال المخزون باستخدام أسلوب التسوية المباشرة لتسوية الاستلام المالي للمخزون إلى الإصدار المالي للمخزون.

يوضح المخطط التالي سلسلة الحركات هذه مع تأثيرات اختيار نموذج المخزون المتوسط المرجح وقاعدة التسوية المباشرة دون خيار تضمين القيمة الفعلية. 

![ DS للتاريخ المتوسط المرجح مع تضمين قيمة فعلية ](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**مفتاح المخطط**
-   تتمثل حركات المخزون في شكل أسهم رأسية.
-   تتمثل عمليات الاستلام داخل المخزون في شكل أسهم رأسية فوق المخطط الزمني.
-   تتمثل الإصدارات خارج المخزون في شكل أسهم رأسية تحت المخطط الزمني.
-   ‏‫تتحدد قيمة حركة المخزون أعلى (أو أسفل) كل سهم رأسي،على أساس Quantity@Unitprice.
-   تحاط قيمة حركة المخزون بأقواس للإشارة إلى أنه قد تم ترحيل حركة المخزون بالفعل إلى المخزون.
-   تشير قيمة العملية المخزنية غير المحاطة بأقواس إلى أنه قد تم ترحيل العملية المخزنية ماليًا إلى المخزون.
-   يتم وضع تسمية جديدة لكل حركة إصدار أو استلام جديدة.
-   تتم تسمية كل سهم بواسطة معرف متسلسل، مثل *1a*. تشير المعرفات إلى تسلسل ترحيل العمليات المخزنية في المخطط الزمني.
-   تتمثل عمليات إقفال المخزون في شكل خط رأسي أحمر مقطع والتسمية "إقفال المخزون".
-   تتمثل التسويات، التي أجريت قبل إقفال المخزون، في شكل سهم أحمر منقط مائل يربط بين الاستلام والإصدار.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>التسوية الملخصة للمتوسط المرجح بدون تحديد الخيار تضمين القيمة الفعلية
يستخدم المتوسط المرجح قاعدة التسوية التي تفيد بأن كافة الإيصالات خلال فترة إقفال يتم تلخيصها في حركة تحويل تُعرف باسم إقفال مخزون المتوسط المرجح‏‏. وستتم تسوية كافة عمليات الاستلام للفترة مقابل إصدار حركة تحويل مخزون تم إنشاؤها حديثًا. وستتم تسوية كافة الإصدارات للفترة مقابل عملية الاستلام الخاصة بعملية التحويل المخزنية الجديدة. إذا كان المخزون الفعلي موجبًا بعد إقفال المخزون، يتم تلخيص هذا المخزون الفعلي وقيمة المخزون في عملية التحويل المخزنية الجديدة (عملية الاستلام). إذا كان المخزون الفعلي سالبًا بعد إقفال المخزون، يصبح إجمالي المخزون الفعلي وقيمة المخزون هو مجموع الإصدارات الفردية التي لم تتم تسويتها بشكل كامل. وفي السيناريو التالي، تم ترحيل إصدار واحد وعدة عمليات استلام تم تحديثها ماليًا. 

أثناء إقفال المخزون، سوف يقوم النظام بإنشاء حركة تحويل مخزون ملخصة وترحيلها لتسوية كافة عمليات استلام الفترة مقابل حركة إصدار تحويل مخزون ملخصة. وسوف تتم تسوية كافة الإصدارات التي تم ترحيلها للفترة مقابل حركة استلام تحويل مخزون ملخصة. ويتم حساب المتوسط المرجح ليكون 15.00 دولارًا أمريكيًا. تم ترحيل الإصدار أصلاً بسعر تكلفة مقدر يبلغ 14.67 دولار أمريكي. وبالتالي، سيتم إنشاء تسوية بمبلغ سالب قدره 0.33 دولار أمريكي وترحيله في الإصدار. أما بالنسبة لتاريخ إقفال المخزون، يكون المخزون الفعلي عبارة عن ثلاث قطع قيمتها 45.00 دولارًا أمريكيًا. 

توضح الرسوم اللاحقة الحركات التالية:
-   1أ. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 2 بتكلفة مقدارها 11.00 دولارًا أمريكيًا للوحدة.
-   1ب. الاستلام المالي للمخزون الذي تم تحديثه لكمية قيمتها 2 بتكلفة مقدارها 14.00 دولارًا أمريكيًا للوحدة.
-   2أ. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 12.00 دولارًا أمريكيًا للوحدة.
-   2ب. الاستلام المالي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 16.00 دولارًا أمريكيًا للوحدة.
-   3أ. الإصدار الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 14.67 دولارًا أمريكيًا للوحدة (المتوسط الساري).
-   3ب. الإصدار المالي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 14.67 دولارًا أمريكيًا للوحدة (المتوسط الساري).
-   4أ. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 14.00 دولارًا أمريكيًا للوحدة.
-   4ب. الاستلام المالي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 16.00 دولارًا أمريكيًا للوحدة.
-   5. يتم إجراء إقفال المخزون.
-   6أ. يتم إنشاء الإصدار المالي "حركة إقفال مخزون المتوسط المرجح" لتجميع تسويات كافة عمليات استلام المخزون المالية.
-   6ب. يتم إنشاء الاستلام المالي "حركة إقفال مخزون المتوسط المرجح" كمقابل لـ 5أ.

يوضح المخطط التالي سلسلة الحركات هذه مع تأثيرات اختيار نموذج المخزون المتوسط المرجح وقاعدة التسوية الملخصة دون خيار تضمين القيمة الفعلية. 

![ SS للتاريخ المتوسط المرجح بدون تضمين قيمة فعلية ](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**مفتاح المخطط**
-   تتمثل حركات المخزون في شكل أسهم رأسية.
-   تتمثل عمليات الاستلام داخل المخزون في شكل أسهم رأسية فوق المخطط الزمني.
-   تتمثل الإصدارات خارج المخزون في شكل أسهم رأسية تحت المخطط الزمني.
-   ‏‫تتحدد قيمة حركة المخزون أعلى (أو أسفل) كل سهم رأسي،على أساس Quantity@Unitprice.
-   تحاط قيمة حركة المخزون بأقواس للإشارة إلى أنه قد تم ترحيل حركة المخزون بالفعل إلى المخزون.
-   تشير قيمة العملية المخزنية غير المحاطة بأقواس إلى أنه قد تم ترحيل العملية المخزنية ماليًا إلى المخزون.
-   يتم وضع تسمية جديدة لكل حركة إصدار أو استلام جديدة.
-   تتم تسمية كل سهم بواسطة معرف متسلسل، مثل *1a*. تشير المعرفات إلى تسلسل ترحيل العمليات المخزنية في المخطط الزمني.
-   تتمثل عمليات إقفال المخزون في شكل خط رأسي أحمر مقطع والتسمية "إقفال المخزون".
-   تتمثل التسويات، التي أجريت قبل إقفال المخزون، في شكل سهم أحمر منقط مائل يربط بين الاستلام والإصدار.
-   تشير الأسهم الحمراء إلى حركات الاستلام التي تمت تسويتها إلى حركة الإصدار التي أنشأها النظام.
-   يمثل السهم الأخضر حركة الاستلام المقابلة المنشأة بواسطة النظام، والتي يتم على أساسها تسوية حركة الإصدار المرحَّلة في الأصل.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>التسوية المباشرة للمتوسط المرجح باستخدام الخيار تضمين القيمة الفعلية
تعمل معلمة تضمين القيمة الفعلية مع نموذج المخزون المتوسط المرجح بشكل مختلف عما كانت عليه في الإصدارات السابقة من المنتج. وحدد مربع تضمين القيمة الفعلية لكل صنف في مجموعة نماذج الصنف. وسيستخدم النظام فيما بعد عمليات الاستلام المحدَّثة فعليًا عند حساب سعر التكلفة المُقدَّر، أو حساب المتوسط الحالي. أما الإصدارات، فسيتم ترحيلها استنادًا إلى سعر التكلفة المُقدَّر هذا خلال الفترة المعنية. أثناء إقفال المخزون، ستتم مراعاة عمليات الاستلام المحدَّثة ماليًا فقط عند حساب المتوسط المرجح. يوصى بالإقفال الشهري للمخزون عند استخدام نموذج مخزون المتوسط المرجح. في هذا المثال الخاص بالتسوية المباشرة للمتوسط المرجح، يتم تمييز مجموعة نماذج الصنف وذلك لتضمين القيمة الفعلية. 

توضح الرسوم اللاحقة الحركات التالية:
-   1أ. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 11.00 دولارًا أمريكيًا للوحدة.
-   1ب. الاستلام المالي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 10.00 دولارات أمريكية للوحدة.
-   2أ. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 15.00 دولارًا أمريكيًا للوحدة.
-   3أ. الإصدار الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 12.50 دولارًا أمريكيًا للوحدة (تكلفة المتوسط الساري، حيث يتم وضع قيمة الاستلام الفعلي في الاعتبار).
-   3ب. الإصدار المالي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 12.50 دولارًا أمريكيًا للوحدة (تكلفة المتوسط الساري، حيث يتم وضع قيمة الاستلام الفعلي في الاعتبار).
-   4. يتم إجراء إقفال المخزون. أثناء إقفال المخزون، سيقوم النظام بتجاهل كافة حركات المخزون التي تم تحديثها فعليًا فقط. وبدلاً من ذلك، سوف تُستخدم قاعدة التسوية المباشرة نظرًا لوجود استلام مالي واحد فقط. وسوف يتم ترحيل تعديل قدره 2.50 دولارًا أمريكيًا إلى العملية المخزنية التي تم إصدارها ماليًا بدءًا من تاريخ إقفال المخزون. وبعد إقفال المخزون، ستكون قيمة كمية المخزون الفعلي 1 ويكون متوسط سعر التكلفة الساري هو 15.00 دولارًا أمريكيًا.

يوضح المخطط التالي سلسلة الحركات هذه مع تأثيرات اختيار نموذج المخزون المتوسط المرجح وقاعدة التسوية المباشرة مع خيار تضمين القيمة الفعلية. 

![ DS للتاريخ المتوسط المرجح مع تضمين قيمة فعلية](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**مفتاح المخطط**
-   تتمثل حركات المخزون في شكل أسهم رأسية.
-   تتمثل عمليات الاستلام داخل المخزون في شكل أسهم رأسية فوق المخطط الزمني.
-   تتمثل الإصدارات خارج المخزون في شكل أسهم رأسية تحت المخطط الزمني.
-   ‏‫تتحدد قيمة حركة المخزون أعلى (أو أسفل) كل سهم رأسي،على أساس Quantity@Unitprice.
-   تحاط قيمة حركة المخزون بأقواس للإشارة إلى أنه قد تم ترحيل حركة المخزون بالفعل إلى المخزون.
-   تشير قيمة العملية المخزنية غير المحاطة بأقواس إلى أنه قد تم ترحيل العملية المخزنية ماليًا إلى المخزون.
-   يتم وضع تسمية جديدة لكل حركة إصدار أو استلام جديدة.
-   تتم تسمية كل سهم بواسطة معرف متسلسل، مثل *1a*. تشير المعرفات إلى تسلسل ترحيل العمليات المخزنية في المخطط الزمني.
-   تتمثل عمليات إقفال المخزون في شكل خط رأسي أحمر مقطع والتسمية "إقفال المخزون".
-   تتمثل التسويات، التي أجريت قبل إقفال المخزون، في شكل سهم أحمر منقط مائل يربط بين الاستلام والإصدار.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>التسوية الملخصة للمتوسط المرجح باستخدام الخيار تضمين القيمة الفعلية
‏‫تعمل معلمة تضمين القيمة الفعلية مع المتوسط المرجح بشكل مختلف عما كانت عليه في الإصدارات السابقة. وحدد مربع تضمين القيمة الفعلية لكل صنف في صفحة مجموعة نماذج الصنف. وسيستخدم النظام فيما بعد عمليات الاستلام المحدَّثة فعليًا في حساب سعر التكلفة المُقدَّر، أو حساب المتوسط الحالي. أما الإصدارات، فسيتم ترحيلها استنادًا إلى سعر التكلفة المُقدَّر هذا خلال الفترة المعنية. أثناء إقفال المخزون، ستتم مراعاة عمليات الاستلام المحدَّثة ماليًا فقط عند حساب المتوسط المرجح. يوصى بالإقفال الشهري للمخزون عند استخدام نموذج مخزون المتوسط المرجح. في هذا المثال الخاص بالتسوية الملخصة للمتوسط المرجح، يتم تمييز نموذج المخزون وذلك لتضمين القيمة الفعلية. 

توضح الرسوم اللاحقة الحركات التالية:
-   1أ. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 2 بتكلفة مقدارها 11.00 دولارًا أمريكيًا للوحدة.
-   1ب. الاستلام المالي للمخزون الذي تم تحديثه لكمية قيمتها 2 بتكلفة مقدارها 14.00 دولارًا أمريكيًا للوحدة.
-   2. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 10.00 دولارًا أمريكيًا للوحدة.
-   3أ. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 12.00 دولارًا أمريكيًا للوحدة.
-   3ب. الاستلام المالي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 16.00 دولارًا أمريكيًا للوحدة.
-   4أ. الإصدار الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 13.50 دولارًا أمريكيًا للوحدة (تكلفة المتوسط الساري، حيث يتم وضع قيمة الاستلام الفعلي في الاعتبار).
-   4ب. الإصدار المالي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 13.50 دولارًا أمريكيًا للوحدة (تكلفة المتوسط الساري، حيث يتم وضع قيمة الاستلام الفعلي في الاعتبار).
-   5أ. الاستلام الفعلي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 14.00 دولارًا أمريكيًا للوحدة.
-   5ب. الاستلام المالي للمخزون الذي تم تحديثه لكمية قيمتها 1 بتكلفة مقدارها 16.00 دولارًا أمريكيًا للوحدة.
-   6. يتم إجراء إقفال المخزون. أثناء إقفال المخزون، سيقوم النظام بتجاهل كافة حركات المخزون التي تم تحديثها فعليًا فقط. وسوف تُستخدم قاعدة التسوية الملخصة نظرًا لوجود استلام مالي واحد فقط. وسوف يتم ترحيل تعديل قدره 1.50 دولارًا أمريكيًا إلى العملية المخزنية التي تم إصدارها ماليًا بدءًا من تاريخ إقفال المخزون. بعد إقفال المخزون، ستكون قيمة كمية المخزون الفعلي 3 بمتوسط سعر تكلفة ساري 15.00 دولارًا أمريكيًا.
-   7أ. يتم إنشاء الإصدار المالي "حركة إقفال مخزون المتوسط المرجح" لتجميع تسويات كافة عمليات استلام المخزون المالية.
-   7أ. يتم إنشاء الاستلام المالي "حركة إقفال مخزون المتوسط المرجح" كمقابل لـ 5أ.

يوضح المخطط التالي سلسلة الحركات هذه مع تأثيرات اختيار نموذج المخزون المتوسط المرجح وقاعدة التسوية الملخصة دون خيار تضمين القيمة الفعلية. 

![ SS للتاريخ المتوسط المرجح مع تضمين قيمة فعلية ](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**مفتاح المخطط**
-   تتمثل حركات المخزون في شكل أسهم رأسية.
-   تتمثل عمليات الاستلام داخل المخزون في شكل أسهم رأسية فوق المخطط الزمني.
-   تتمثل الإصدارات خارج المخزون في شكل أسهم رأسية تحت المخطط الزمني.
-   ‏‫تتحدد قيمة حركة المخزون أعلى (أو أسفل) كل سهم رأسي،على أساس Quantity@Unitprice.
-   تحاط قيمة حركة المخزون بأقواس للإشارة إلى أنه قد تم ترحيل حركة المخزون بالفعل إلى المخزون.
-   تشير قيمة العملية المخزنية غير المحاطة بأقواس إلى أنه قد تم ترحيل العملية المخزنية ماليًا إلى المخزون.
-   يتم وضع تسمية جديدة لكل حركة إصدار أو استلام جديدة.
-   يتم وضع تسمية لكل سهم رأسي تشتمل على معرف متسلسل، مثل 1a. تشير المعرفات إلى تسلسل ترحيل العمليات المخزنية في المخطط الزمني.
-   تتمثل عمليات إقفال المخزون في شكل خط رأسي أحمر مقطع والتسمية "إقفال المخزون".
-   تتمثل التسويات، التي أجريت قبل إقفال المخزون، في شكل سهم أحمر منقط مائل يربط بين الاستلام والإصدار.
-   تشير الأسهم الحمراء إلى حركات الاستلام التي تمت تسويتها إلى حركة الإصدار التي أنشأها النظام.
-   يمثل السهم الأخضر حركة الاستلام المقابلة المنشأة بواسطة النظام، والتي يتم على أساسها تسوية حركة الإصدار المرحَّلة في الأصل.

## <a name="weighted-average-with-marking"></a>المتوسط المرجح مع وضع علامة
وضع العلامة هي عملية تسمح لك بربط حركة الإصدار بحركة الاستلام، أو وضع علامة عليهما. يمكن وضع العلامة سواء قبل ترحيل الحركة أو بعده. يمكنك وضع علامات إذا أردت التأكد من التكلفة الدقيقة للمخزون عند ترحيل الحركة أو عند إقفال المخزون. 

على سبيل المثال، قبِل قسم خدمة العملاء لديك أمرًا متسرعًا من عميل مهم. نظرًا لأن هذا أمر عاجل، سيتعين عليك إنفاق المزيد على هذا الصنف لخدمة طلب العميل. وقد ترغب في التأكد من انعكاس تكلفة صنف المخزون هذا في الهامش، أو تكلفة السلع المبيعة (COGS)، لفاتورة أمر التوريد هذه. 

عند ترحيل أمر الشراء، يتم استلام المخزون بتكلفة 120.00 دولارًا أمريكيًا. على سبيل المقال، يتم وضع علامة على مستند أمر المبيعات لأمر الشراء قبل ترحيل إيصال التعبئة أو الفاتورة. وتكلفة البضائع المبيعة ستكون 120.00 دولاراً أمريكياً فيما بعد بدلاً من متوسط التكلفة الحالية للصنف. وإذا كان قد تم ترحيل كشف التعبئة أو الفاتورة قبل وضع العلامة، فسوف يتم ترحيل تكلفة البضائع المبيعة بالمتوسط الساري لسعر تكلفة. 

قبل إجراء إقفال المخزون، ما يزال يمكن ربط هاتين الحركتين مع بعضهما بعلامة. 

ويتم وضع علامة على حركة الاستلام لحركة إصدار. وبعد ذلك، سيتم تجاهل طريقة التقييم المحددة لمجموعة نماذج المخزون الخاصة بالصنف وسيعمل النظام على تسوية هذه الحركات مع بعضها البعض. 

يمكنك وضع علامة على حركة إصدار لتلقيها قبل ترحيل الحركة. ويمكنك القيام بذلك من بند أمر مبيعات في صفحة تفاصيل أمر المبيعات. ويتم عرض حركات الاستلام المفتوحة في صفحة وضع العلامات. 

يمكنك وضع علامة على حركة إصدار لتلقيها بعد ترحيل الحركة. يمكنك مطابقة أو وضع علامة على حركة إصدار لحركة إيصال مفتوحة لأحد الأصناف المخزنة من دفتر يومية تسوية مخزون تم ترحيله. 

توضح الرسوم اللاحقة الحركات التالية:
-   1أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 10.00.
-   1ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 10 ريالات سعودي
-   2أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 20.00.
-   2ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 20 ريالاً سعوديًا.
-   3أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 25.00.
-   4أ. الإيصال الفعلي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 30.00.
-   4ب. الإيصال المالي للمخزون لكمية قيمتها 1 بتكلفة مقدارها 30 ريالاً سعوديًا.
-   5أ. الإصدار الفعلي للمخزون لكمية قيمتها 1 بسعر تكلفة 21.25 دولارًا أمريكيًا (المتوسط الساري للحركات المالية والفعلية التي تم تحديثها).
-   5ب. يتم تمييز الإصدار المالي للمخزون للكمية 1 إلى إيصال استلام المخزون 2b قبل ترحيل الحركة. يتم ترحيل هذه الحركة مقابل سعر تكلفة يبلغ 20.00 دولارًا أمريكيًا.
-   6أ. الإصدار الفعلي للمخزون لكمية قدرها 1 بسعر تكلفة مقداره 21.25 دولارًا أمريكيًا لكل وحدة.
-   7 تم إقفال المخزون. ونظرًا لأنه تم وضع علامة على الحركة المحدثة ماليًا وربطها باستلام موجود، فسوف تتم تسوية هذه الحركات ببعضها البعض ولا يتم القيام بأي تعديل.

يعكس متوسط سعر تكلفة التشغيل متوسط الحركات التي تم تحديثها ماليًا وفعليًا عند 27.50 دولارًا أمريكيًا. 

يوضح المخطط التالي هذه السلسلة من الحركات مع تأثيرات اختيار نموذج مخزون المتوسط المرجح مع وضع علامة. 

![المتوسط المرجح مع وضع علامة](./media/weightedaveragewithmarking.gif) 

**مفتاح المخطط**
-   تتمثل حركات المخزون في شكل أسهم رأسية.
-   تتمثل عمليات الاستلام داخل المخزون في شكل أسهم رأسية فوق المخطط الزمني.
-   تتمثل الإصدارات خارج المخزون في شكل أسهم رأسية تحت المخطط الزمني.
-   ‏‫تتحدد قيمة حركة المخزون أعلى (أو أسفل) كل سهم رأسي،على أساس Quantity@Unitprice.
-   تحاط قيمة حركة المخزون بأقواس للإشارة إلى أنه قد تم ترحيل حركة المخزون بالفعل إلى المخزون.
-   تشير قيمة العملية المخزنية غير المحاطة بأقواس إلى أنه قد تم ترحيل العملية المخزنية ماليًا إلى المخزون.
-   يتم وضع تسمية جديدة لكل حركة إصدار أو استلام جديدة.
-   تتم تسمية كل سهم بواسطة معرف متسلسل، مثل *1a*. تشير المعرفات إلى تسلسل ترحيل العمليات المخزنية في المخطط الزمني.
-   تتمثل عمليات إقفال المخزون في شكل خط رأسي أحمر مقطع والتسمية "إقفال المخزون".
-   تتمثل التسويات، التي أجريت قبل إقفال المخزون، في شكل سهم أحمر منقط مائل يربط بين الاستلام والإصدار.





