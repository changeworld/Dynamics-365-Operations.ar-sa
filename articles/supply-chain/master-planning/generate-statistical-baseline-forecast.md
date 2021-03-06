---
title: "إنشاء التنبؤ الأساسي الإحصائي"
description: "توفر هذه المقالة معلومات حول المعلمات وعوامل التصفية التي يتم استخدامها في حساب التنبؤ بالطلب."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 42ea3a6cf85802fc42c53111d17afbce042a6d44
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="generate-a-statistical-baseline-forecast"></a>إنشاء التنبؤ الأساسي الإحصائي

[!include [banner](../includes/banner.md)]

توفر هذه المقالة معلومات حول المعلمات وعوامل التصفية التي يتم استخدامها في حساب التنبؤ بالطلب. 

عند إنشاء تنبؤ أساسي، يجب أولاً تحديد المعلمات وعوامل التصفية المستخدمة في عملية الحساب. على سبيل المثال، يمكنك إنشاء تنبؤ أساسي لتقدير الطلب على أساس بيانات الحركة من العام الماضي لشركة معينة للشهر القادم ولمجموعة محددة من الأصناف. 

لإنشاء التنبؤ بالطلب، انتقل إلى **التخطيط الأساسي &gt; التنبؤ &gt; التنبؤ بالطلب &gt; إنشاء التنبؤ الأساسي الإحصائي**. 

يمكن تحديد ‏‫الفترة الزمنية‬ للتنبؤ‬‬ في وقت إنشاء التنبؤ. القيم المتوفرة: اليوم والأسبوع والشهر. 

عندما يتم إعداد عدد الفترة الزمنية لإنشاء التنبؤ في الحقل**أفق التنبؤ**. 

عندما يتم إعداد إستراتيجية التنبؤ إلى **‏‫نسخ فوق الطلب التاريخي‬**، فإنه يتم تجاهل نهاية الأفق التاريخي. ينسخ النظام عدد الفترات المحددة في الحقل **أفق التنبؤ** لطلب التنبؤ، بدءًا من التاريخ المحدد في الحقل **من تاريخ** ضمن **الأفق التاريخي**. عن طريق نسخ الطلب التاريخي من تاريخ معين إلى الأمام، يمكن جعل مخططي الإنتاج خطة الربع القادم بطريقتين:

-   عن طريق نسخ الطلب من الربع نفسه العام الماضي.
-   عن طريق نسخ الطلب من الربع السابق.

لمنع حدوث أي ارتباك في خطط الإنتاج، فإنه يمكن تجميد عدد معين من مستودعات التنبؤ. يتم تعيين هذا الرقم في الحقل **‏‫الحد الزمني للتجمد‬**. على الصفحة **التنبؤ بالطلب المعدل**، فإنه يتم تعطيل الخلايا للمستودعات المجمدة، لإعطاء إشارة مرئية أنه لا ينبغي تغيير هذه القيم. 

لا يجب أن يحتوي تاريخ البدء للتنبؤ الأساسي بالطلب على التاريخ الحالي أو تاريخ في المستقبل. لتعيين تاريخ بدء مختلف، استخدم الحقل **تاريخ البدء للتنبؤ الأساسي - من تاريخ**. على سبيل المثال، في حزيران/يونيه، يمكن للمستخدمين إنشاء تنبؤ للسنة المقبلة. لأن مستودعات التنبؤ بين نهاية الطلب التاريخي وبداية الخط الأساسي المفقود، قد لا تكون التنبؤات دقيقة. إذا كنت تستخدم خدمة التنبؤ بالطلب في Dynamics 365 for Finance and Operations، هناك أربع طرق لملء الفجوات المفقودة. يمكنك اختيار الطريقة التي تريدها عن طريق تعيين المعلمة MISSING\_VALUE\_SUBSTITUTION على الصفحة **معلمات التنبؤ بالطلب**. 

يجب تعيين **تاريخ بدء التنبؤ الأساسي** - **‎من تاريخ** إلى بداية الفترة الزمنية للتنبؤ، على سبيل المثال، في الولايات المتحدة، يوم الأحد إذا كانت الفترة الزمنية للتنبؤ هي أسبوع. يقوم النظام تلقائيًا بتعديل الحقل **تاريخ بدء التنبؤ الأساسي** - **‎من تاريخ** لمطابقة بداية الفترة الزمنية للتنبؤ. 

يمكن تعيين الحقل **تاريخ البدء للتنبؤ الأساسي** - **من تاريخ** إلى تاريخ في الماضي. وبعبارة أخرى، من الممكن إنشاء التنبؤ بالطلب في الماضي. هذا مفيد، لأنه يتيح للمستخدمين قرص معلمات خدمة التنبؤ حيث يتطابق التنبؤ الإحصائي الذي تم إنشاؤه في الماضي مع الطلب الفعلي التاريخي. يستطيع المستخدمون حينها الاستمرار باستخدام إعدادات المعلمة هذه لإنشاء التنبؤ الأساسي الإحصائي للمستقبل. 

يمكن تطبيق التعديلات اليدوية التي تم القيام بها في تكرارات التنبؤ بالطلب السابق تلقائيًا على التنبؤ الأساسي الجديد إذا تم تحديد خانة الاختيار **‏‫نقل التسويات اليدوية إلى التنبؤ بالطلب‬**. في حالة إلغاء تحديد خانة الاختيار، فإنه لا تتم إضافة التعديلات اليدوية إلى التنبؤ الأساسي ولكن لا يتم حذفها. يمكن حذف التعديلات اليدوية التي تم القيام بها على لتنبؤ فقط في وقت استيراد التنبؤ، عن طريق مسح خانة الاختيار **‏‫حفظ التسويات اليدوية التي تم إدخالها على التنبؤ بالطلب الأساسي ‬**. يتم حفظ التسويات اليدوية في وقت التخويل. لذلك، إذا قام مستخدم بتسويات يدوية على التنبؤ، لكنه لا يخول التنبؤ مرة أخرى إلى Finance and Operations، فستُفقد التغييرات. لمزيد من المعلومات حول التسويات اليدوية وطريقة عملها، راجع [تخويل التنبؤ المعدل](authorize-adjusted-forecast.md). 

يمكن أن يكون لإنشاء التنبؤ بالطلب اسمًا وتعليقات لمساعدة المستخدمين على تحديد التنبؤ الذي تم إنشاؤه. هذه القيم مرئية في تاريخ إنشاء التنبؤ على الصفحة **تاريخ إنشاء التنبؤ الأساس الإحصائي**. 

يمكن تطبيق مجموعة التخطيط بين الشركات الشقيقة ومفاتيح توزيع الأصناف وعوامل التصفية الأخرى في وقت إنشاء التنبؤ. يمكن استخدامها لتحسين الأداء أو لتقسيم البيانات إلى أجزاء يمكن إدارتها. ومع ذلك، لاحظ أنه لا يتم إنشاء التنبؤ بالطلب لأعضاء أي مفتاح توزيع الصنف غير مرتبط بمجموع تخطيط بين الشركات الشقيقة، حتى إذا تم تحديد مفتاح تخصيص الصنف في الاستعلام. 

**تلميح**: في بعض الأحيان قد يتلقى المستخدمون أخطاء أثناء إنشاء التنبؤ بالطلب، أو يتم إكمال إنشاء التنبؤ بدون سجل جلسة العمل. قد يحدث هذا بسبب البيانات المتبقية في الاستعلام الذي تم استخدامها مسبقًا لإنشاء التنبؤ. لإصلاح هذه المشكلة، انقر فوق **حدد** لفتح صفحة **الاستعلام**، انقر فوق **إعادة التعيين**، وثم إعادة إنشاء التنبؤ الأساسي. 

إذا لم يتم إنشاء التنبؤ لمجموعة كبيرة من الأصناف، ولكن، على سبيل المثال، بالنسبة لصنف واحد أو مفتاح توزيع الصنف في المرة الواحدة، فمن أجل الحصول على أداء أفضل، يمكنك تحديد خانة الاختيار **استخدم وضع الاستجابة المطلوبة** في علامة التبويب **‎التخطيط الرئيسي - الإعداد - التنبؤ بالطلب** - **معلمات التنبؤ بالطلب - Azure Machine Learning**.

<a name="additional-resources"></a>الموارد الإضافية
--------

[إعداد التنبؤ بالطلب](demand-forecasting-setup.md)

[القيام بتسويات يدوية في تنبؤ الخط الأساسي](manual-adjustments-baseline-forecast.md)

[تخويل ‏‫التنبؤ الذي تمت تسويته](authorize-adjusted-forecast.md)




