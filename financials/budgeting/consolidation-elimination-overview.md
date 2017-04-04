---
title: "نظرة عامة على التجميع والاستبعاد"
description: "توفر هذه المقالة معلومات عامة حول عملية التوحيد والاستبعاد. وتتضمن أيضًا إجابات على بعض الأسئلة المتداولة."
author: RobinARH
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 3868605826e3c6f0714736ffa8630d1569e17d6f
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-and-elimination-overview"></a>نظرة عامة على التجميع والاستبعاد

توفر هذه المقالة معلومات عامة حول عملية التوحيد والاستبعاد. وتتضمن أيضًا إجابات على بعض الأسئلة المتداولة.

عند تجميع البيانات، يتم تجميع النتائج المالية لعدد من الشركات التابعة في نتائج شركة مجمعة واحدة. وقد تكون الشركات التابعة موجودة في إصدارات أو أنظمة مختلفة، وقد لا تكون مملوكة بالكامل، ويمكنها استخدام عملات مختلفة. وهناك عدة خيارات لتجميع البيانات:

-   **التجميع على الإنترنت** - يقوم هذا الخيار بتجميع الأرصدة اليومية حسب الحسابات والأبعاد المحددة، ويخزنها في شركة مجمعة.
-   **التقارير المالية** - يتيح هذا الخيار تجميع الحركات والأرصدة، ويمكن إنشاؤه في أي وقت. يمكن إنشاء مستويات متعددة من التدرج هرمي، ويمكن الاطلاع على عملات التقارير المتعددة.
-   **التجميع مع الاستيراد** - يستورد هذا الخيار أرصدة الواردات إلى شركة مجمعة.
-   **تصدير أرصدة الشركة** - يوفر هذا الخيار ملف تصدير لأرصدة الشركة. وبعد ذلك، يمكن استيراد الملف إلى حالات أو أنظمة أخرى. كما يمكن استخدام التقارير المالية لتصدير الأرصدة إلى ملف Microsoft Excel.

يمكن الإبلاغ عن عمليات الاستبعاد بطرق متعددة:

-   يمكن إعداد قواعد الاستبعاد في النظام، وبعد ذلك معالجتها أثناء عملية التجميع أو من خلال مقترح استبعاد. ويمكن ترحيل القواعد لأي شركة قامت بتحديد **‏‫يُستخدم لعملية الاستبعاد المالي‬** في إعداد الكيان القانوني.
-   يمكن إنشاء شركة مستقلة واستخدامها لتحديد وترحيل حركات الاستبعاد يدوياً. يمكن استخدام هذه الشركة في عملية التجميع أو في التقارير المالية.
-   يمكن تصفية الحسابات والأبعاد المالية التي يتم استخدامها لتحديد نشاط بين الشركات الشقيقة في تعريف صف أو عمود في التقارير المالية، ويمكن استخدام قدرات التنقل الكاملة. يمكن بعذلك استخدام عمود أو صف محسوب لإزالة الحسابات والأبعاد المالية من الإجمالي المجمع.

هناك العديد من سيناريوهات التجميع، ويمكن لكل طريقة معالجة السيناريوهات بطرق مختلفة.

## <a name="frequently-asked-questions"></a>الأسئلة المتداولة
1.  أفضل ترحيل عمليات الاستبعاد في قاعدة بيانات. ما خياراتي المتاحة؟

لديك خيارات متعددة. ويمكنك استخدام خيار **التجميع على الإنترنت** ، وتضمين عمليات الاستبعاد أثناء العملية أو كاقتراح. وسيتم ترحيل الحركات في الشركة الموحدة. وبدلاً من ذلك، يمكنك الحصول على شركة مستقلة تقوم يدوياً بإنشاء عمليات الاستبعاد فيها، ثم استخدام تلك الشركة في التقارير المالية أو في عملية التجميع.

2.  نحن بحاجة إلى نتائجنا المجمعة بعملات التقارير المتعددة.

يشتمل خيار **التقارير المالية** على خيار تقارير غير محدودة. ويتم تحويل البيانات أثناء إنشاء التقرير، استناداً إلى سعر صرف العملة وطريقة تحويل العملة اللذين تم تعيينهما في الحساب الرئيسي. ومع ذلك، نظراً لأن خيار **التجميع على الإنترنت** يشتمل على عملة تقارير واحدة فقط، يُتطلب وجود شركة موحدة لكل عملة تقارير إذا استخدمت هذا الخيار. خيار **التقارير المالية** هو الطريقة الموصى به.

3.  أريد أن أرى تفاصيل مستوى الحركة لكل شركة.

خيار **التقارير المالية** هو الحل، لأنه يمكن عرض تفاصيل مستوى الحركة للعديد من الشركات المدرجة في تعريف شجرة التقارير.

4.  نستخدم تخطيط الموازنة أو التحكم في الموازنة، ويجب أن يتم دمجها.
خيار **التقارير المالية** هو الحل لتجميع بيانات لتخطيط الموازنة أو مراقبة الموازنة.

5.  تنتشر الشركات التابعة لنا في جميع أنحاء العالم، ولدينا مخططات حسابات متعددة. ما أفضل طريقة لتجميع البيانات الخاصة بنا؟

لديك خيارات متعددة عندما يجب أن تقوم بمعالجة مخططات حسابات متعددة. ويمكنك استخدام خيار **التجميع على الإنترنت**، ثم اختيار استخدام إما حساب التجميع الذي تم تحديده في الحساب الرئيسي أو مجموعة حساب تجميع. كما يمكنك استخدام خيار **التقارير المالية**، وتضمين ارتباطات متعددة للأبعاد المالية في تعريف الصف، وتعيين الحسابات.

6.  نتطلب عدة مستويات للتجميع. وبعبارة أخرى، نقوم أولاً بتوحيد فروعنا الأوروبية بلجنيه الإسترليني (GBP). وبعد ذلك، نحصل على تلك البيانات ونقوم بتحويل المبلغ المجمع إلى الدولارات الأمريكية. كيف يمكننا أن نفعل ذلك؟

عند تطلب وجود مستويات متعددة للتجميع، يتم استخدام عملات مختلفة عند كل مستوى، ويجب عليك استخدام خيار **التجميع على الإنترنت**. ويجب إنشاء عدة شركات تجميع تختلف في عملات المحاسبة والتقارير الخاصة بها. ويجب إجراء التجميع عدة مرات بعد ذلك. ويقوم خيار **التقارير المالية** دائمًا بالتحويل من كل عملة محاسبة للشركة المصدر إلى العملة المحددة.

7.  لدينا فروع على نظام مختلف. كيف يمكننا دمجها؟

استخدم خيار **التجميع مع الاستيراد** لتجميع الأرصدة في شركة تجميع.

8.  بعض الشركات التابعة لنا ليست مملوكة لنا بالكامل. ما أفضل طريقة لدمجها؟

لديك العديد من الخيارات للشركات التابعة المملوكة جزئيًا. باستخدام خيار **التقارير المالية**، يمكنك تحديد تعريف شجرة تقارير والملكية. كما يمكنك استخدام صف أو عمود محسوب لتمثيل المقدار المملوك جزئيًا. ويمكنك حتى إظهار مصلحة الأقلية كصف خاص بها في تقرير. كما يمكنك استخدام خيار **التجميع على الإنترنت**. تشتمل علامة التبويب **الكيانات القانونية** على عمود **الملكية**، حيث يمكنك تحديد النسبة المئوية التي تملكها الشركة الأم.

9.  يجب على مؤسستنا إظهار عمليات التجميع حسب وحدة الأعمال أو تحتاج إلى استخدام التدرجات الهرمية للمؤسسات.

خيار **التقارير المالية** هو الحل. ويمكن الإبلاغ عن التدرجات الهرمية للمؤسسات التي تشمل الكيانات القانونية أو الأبعاد المالية فيها في التقارير المالية. كما يمكنك إنشاء التدرجات الهرمية متعددة المستويات الخاصة بك باستخدام تعريف شجرة تقرير يحتوي على مجموعة من الكيانات القانونية وقيم الأبعاد.

10. لدينا أكثر من مثيل واحد للنظام.

باستخدام خيار **تصدير أرصدة الشركة** للتصدير من مثيل واحد، ثم باستخدام خيار **التجميع مع الاستيراد** في المثيل الآخر، يمكنك تجميع البيانات.


لمزيد من المعلومات، راجع [ريفالوشن عمله في شركة موحدة](\finanicials\general-ledger\currency-revaluation-consolidation-company).
