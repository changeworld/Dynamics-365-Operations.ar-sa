---
title: "إنشاء الوثائق أو التدريب باستخدام تسجيلات المهام"
description: "يشرح هذا المقال ما هو مسجل المهام ودلائل المهام‬، وكيفية إنشاء تسجيلات المهام، وكيفية تخصيص دلائل مهام‬ Microsoft وتضمينها في نظام التعليمات الخاص بك."
author: josaw1
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fc5b0798397047d1adedfc19406a7875c853bea6
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="create-documentation-or-training-by-using-task-recordings"></a>إنشاء الوثائق أو التدريب باستخدام تسجيلات المهام

[!include [banner](../includes/banner.md)]

يشرح هذا المقال ما هو مسجل المهام ودلائل المهام‬، وكيفية إنشاء تسجيلات المهام، وكيفية تخصيص دلائل مهام‬ Microsoft وتضمينها في نظام التعليمات الخاص بك.

> [!IMPORTANT]
> يمكنك تسجيل دلائل المهام الخاصة بـ Dynamics 365 for Talent، لكن لن تتمكن من حفظها في مكتبة مصمم نماذج عملية أعمال (BPM) أو فتحها من جزء "التعليمات" في الوقت الحالي. يمكنك حفظها محلياً أو في موقع على الشبكة، ثم فتحها وإعادة تشغيلها باستخدام "مسجل المهام". 

<a name="learn-about-task-recorder"></a>التعرف على مسجل المهام
-------------------------

مسجل المهام عبارة عن أداة يمكنك استخدامها لتسجيل الإجراءات التي تنفذها في واجهة مستخدم المنتج. وعند استخدام مسجل المهام، يتم التقاط كافة الأحداث التي تقوم بها في واجهة المستخدم التي يتم تنفيذها على الخادم — بما في ذلك إضافة القيم، وتغيير الإعدادات، وإزالة البيانات. وتُسمى الخطوات التي تقوم بتسجيلها مجتمعة باسم *تسجيل المهام*. يمكن استخدام تسجيلات المهام بعدة طرق:

-   **يمكن تشغيل تسجيلات المهامة كأدلة مهام.** تمثل دلائل المهام جزءًا لا يتجزأ من تجربة نظام التعليمات. يُعد دليل المهمة عبارة عن خبرة إرشادية تفاعلية محكومة وموجهة خلال الخطوات الخاصة بعملية أعمال. ويتم توجيه المستخدم لإتمام كل خطوة عن طريق مطالبة منبثقة (أو "فقاعة") ستتحرك عبر واجهة المستخدم والإشارة إلى عنصر واجهة المستخدم الذي يجب على المستخدم التفاعل معه. توفر الـ"فقاعة" أيضُا معلومات حول كيفية التفاعل مع العنصر، مثل "انقر هنا" أو "في هذا الحقل، أو أدخل قيمة". يتعارض دليل المهمة مع مجموعة البيانات الحالية للمستخدم، ولقد حُفظت البيانات التي تم إدخالها في بيئة المستخدم.
-   **يمكن عرض تسجيلات المهام كخطوات إجرائية في جزء التعليمات.** يمكنك استخدام جزء "التعليمات" للبحث عن وعرض تسجيلات المهام. يمكنك الوصول إلى جزء المساعدة بالنقر فوق **؟** الرمز في شريط التنقل العلوي أو يمكك استخدام مجموعة مفاتيح الاختصار التالية، **Ctrl + Shift +؟**. يمكنك قراءة خطوات تسجيل المهمة في جزء التعليمات، أو يمكنك اختيار تشغيل التسجيل كدليل مهمة حيث يقوم بإرشادك من خلال واجهة المستخدم.
-   **يمكن حفظ تسجيلات المهام إلى BPM.** يمكنك حفظ تسجيل المهمة إلى بند التدرج الهرمي في مكتبة مصمم نماذج عملية أعمال (BPM) في Lifecycle Services ‏(LCS). وسيتم إنشاء قائمة بالخطوات ومخطط تدفق عمليات أعمال من التسجيل. ويمكن إظهار تسجيلات المهام التي تم حفظها إلى مكتبة BPM كتعليمات.
-   **يمكن حفظ تسجيلات المهام كمستندات Word.** هذا يسمح لك بإنتاج أدلة تدريب للطباعة بسهولة.

يمكنك إنشاء تسجيلات المهام الخاصة بك أو تشغيل تسجيلات المهام المتوفرة من قِبل Microsoft أو تعديل تسجيلات المهام المتوفرة من قِبل Microsoft لتعكس التكوين الخاص بك. لمزيد من المعلومات حول مسجل المهام، راجع [مسجل المهام](task-recorder.md).

## <a name="plan-your-task-recording"></a>تخطيط تسجيل المهمة
سواء أكنت تقوم بإنشاء تسجيل مهمة جديد أو وضع التسجيل الخاص بك في تسجيل مهمة Microsoft، ضع في الاعتبار المعلومات التالية.

-   قم بتخطيط التسجيل الخاص بك كما تفعل مع مقطع فيديو. اتخذ جميع القرارات قبل الموعد المحدد.
-   تنقل خلال عملية الأعمال مرة أو مرتين دون تسجيلها لفهم الخطوات.
-   عندما تتنقل خلال العملية قبل قيامك التسجيل، لاحظ الموضع الذي تستخدم فيه مفاتيح الاختصار أو مفتاح **الإدخال**، بحيث يمكنك تجنب استخدامها أثناء التسجيل الفعلي.
-   حدد ما يلي:
    -   هل تريد تجميع الخطوات معًا في المهام الفرعية؟ تفصل المهام الفرعية بصريًا الأقسام لعملية ما. على سبيل المثال، إذا كنت تقوم بإنشاء تسجيل لـ "إنشاء وإطلاق منتج"، قد تحتاج إلى تجميع الخطوات المطلوبة معًا لإنشاء منتج، ثم تجميع الخطوات المطلوبة لإصدار المنتج. كما تُنشئ المهام الفرعية عمليات أطول لتسهيل القراءة.
    -   هل تريد إضافة تعليقات توضيحية، وإذا كان الأمر كذلك، فأين؟ راجع "فهم الأنواع المختلفة للتعليقات التوضيحية" أدناه لمزيد من المعلومات.
    -   ما القيم التي ستتم إضافتها في الحقول المختلفة عندما تقوم بإكمال خطوات عملية إعمال؟ إنها فكرة جيدة معرفة ما سوف تحدده أو تُدخله أثناء المتابعة بحيث لا تتراجع أو تصلح الأخطاء التي تقوم بتسجيلها.

**كتابة الوصف والتعليقات التوضيحية قبل الموعد المحدد**

-   في بداية كل تسجيل مهمة، يوجد حقل وصف يسمح لك بإدخال مقدمة للتسجيل. إنها لفكرة جيدة كتابة وحفظ وصف قبل الموعد المحدد في وثيقة منفصلة بحيث يمكنك نسخه ولصقه في تسجيل المهمة عند قيامك بالتسجيل. وبهذه الطريقة، يمكنك قضاء الوقت في تحسين النص عندما لا تقوم بعملية تسجيل. ويؤدي قص ولصق النص إلى إتمام عملية التسجيل بسرعة وسلاسة أكبر.
-   في كل خطوة في تسجيل مهمة، يمكنك إنشاء التعليقات التوضيحية. وأثناء تشغيل أدلة المهام، تظهر التعليقات التوضيحية في "الفقاعة" كملاحظات أعلى أو أسفل النص للخطوة. وعند عرضها كنص في جزء "التعليمات"، تظهر التعليقات التوضيحية كنص مضمن في الخطوة. وفيما يتعلق بالوصف، إنها لفكرة جيدة كتابة وحفظ التعليقات التوضيحية في وثيقة منفصلة. عند قيامك بتسجيل تسجيل المهمة، قم بقص ولصق التعليقات التوضيحية في هذا المستند.

**فهم الأنواع المختلفة للتعليقات التوضيحية** كافة التعليقات التوضيحية اختيارية. فقط قم بإضافتها عندما توفر معلومات مفيدة للمستخدم.

-   **العنوان:** سيظهر تعليق العنوان قبل نص الخطوة الذي يقوم مسجل المهام بإنشائه تلقائياً. في دليل المهمة، يظهر تعليق العنوان فوق النص الذي تم إنشاؤه تلقائيًا. استخدم هذا النوع من التعليق التوضيحي لتوضيح لماذا يقوم المستخدم بالخطوة أو لإعطاء سياق إضافي.

وهذا جزء التحرير الذي تراه عندما تقوم بإضافة تعليق توضيحي أثناء إنشاء التسجيل الخاص بك. أدخل تعليقًا توضيحيًا للعنوان في مربع **العنوان**. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

هذا هو الشكل الذي يظهر به التعليق التوضيحي للعنوان في "فقاعة" دليل المهام. 

[![screen2](./media/screen2.png)](./media/screen2.png)

-   **ملاحظات:** سيظهر تعليق ملاحظات بعد نص الخطوة الذي يقوم مسجل المهام بإنشائه تلقائياً. وفي دليل المهمة، سيكون مرئيًا فقط في حالة قيام المستخدم بالنقر فوق رابط **إظهار المزيد** في فقاعة أدلة المهام. استخدم هذا النوع من التعليق التوضيحي لوصف أي شيء يحتاجه المستخدم إلى معرفته لإكمال الخطوة.

وهذا جزء التحرير الذي تراه عندما تقوم بإضافة تعليق توضيحي أثناء إنشاء التسجيل الخاص بك. أدخل تعليقًا توضيحيًا للملاحظات في مربع **الملاحظات**. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

هذا هو الشكل الذي يظهر به التعليق التوضيحي للعنوان في "فقاعة" في دليل المهام.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **خطوة المعلومات**: : هذه التعليقات التوضيحية يتم إنشاؤها بواسطة النقر بزر الماوس الأيمن فوق عنصر تحكم أو في أي مكان في نموذج &lt; **‎مسجل المهام** &lt; **إضافة خطوة المعلومات. **تظهر خطوات المعلومات كخطوة ذات تعداد رقمي في أي نقطة تقوم بإدراجها، حتى لو لم يتم تسجيل أي إجراء في واجهة المستخدم. ويمكنك إضافة خطوة المعلومات على مستوى النموذج أو خطوة المعلومات المقترنة بعنصر تحكم. وعندما تكون خطوة معلومات مقترنة بنموذج، ستظهر "فقاعة" دليل المهمة في مكان في النموذج، دون أي مؤشر، عند تشغيل دليل المهمة. وعندما تكون خطوة معلومات مقترنة بعنصر تحكم، سوف تشير "فقاعة" دليل المهمة إلى عنصر التحكم عند تشغيل دليل المهمة. في جزء "التعليمات"، سوف يظهر تعليق توضيحي لخطوة معلومات كخطوة ذات تعداد رقمي بأي نص قمت بإدخاله. استخدم خطوات المعلومات لتجهيز المستخدم للخطوات المقبلة أو لوصف الخطوات الواجب اتخاذها خارج Microsoft Dynamics 365 for Finance and Operations أو للإشارة إلى تسجيلات أخرى (على الرغم من أنه لا يمكنك إنشاء ارتباطات تشعبية في التعليقات التوضيحية.).

**تحديد مدة إنشاء التسجيل**

-   سيقوم المستخدم عمومًا بقراءة أو تشغيل التسجيل من البداية إلى النهاية، بحيث لا تقوم بالجمع بين الخطوات أو المهام التي يتم إجراؤها بشكل منفصل أفضل.
-   حاول عدم تسجيل سيناريو طويل يمتد عبر عدة عمليات فرعية. على سبيل المثال، "التشغيل في مكتب خدمة عملاء المتجر‬" واسع جداً؛ قم بتقسيمه إلى مهام أقصر مثل "قبول المرتجعات" و"إضافة إلى بطاقة هدايا".
-   إذا كان يمكن تنفيذ مهمة كجزء من عدة عمليات تجارية مختلفة، فقم بإنشاء تسجيل منفصل له، ويمكن الرجوع إليه في التسجيلات الأخرى.
-   إذا كانت العملية تتضمن عدة مهام يقوم الشخص المحتمل بها في وقت واحد، يمكنك الاحتفاظ بالمهام في تسجيل واحد، على سبيل المثال، "إعداد وتعيين ملفات تعريف الوظائف".
-   وإذا كانت هذه العملية شيء يفعله الشخص مرة واحدة (مثل التكوين) ثم مهمة أخرى يمكنه القيام بها فورًا بعد ذلك بشكل متكرر، ومن تلقاء نفسها، فقم بتقسيمها إلى تسجيلي مهام.

**تحديد مكان في واجهة المستخدم لبدء تسجيل** تؤثر الصفحة التي كنت عليها عند بدء تسجيل "تسجيل مهمة" على الصفحة التي يتم عرض دليل المهمة عليها. على سبيل المثال، إذا أردت أن يتم إدراج تسجيل المهام الخاص بك في جزء "تعليمات" عندما ينقر مستحدم فوق "تعليمات" الموجودة في صفحة معلمات دفتر الأستاذ العام، يجب عليك بدء تسجيلك في صفحة معلمات دفتر الأستاذ العام. **حفظ التسجيلات كملفات axtr.** عندما تنتهي من إنشاء أو تحرير مهمة التسجيل، يتم تقديم العديد من الخيارات لك لكيفية تنزيل أو حفظ التسجيل. ويمكنك تنزيل الملف كحزمة تسجيل مهمة (axtr.)، أو تنزيل ملف تسجيل أولي (xml.)، أو تنزيله كمستند Word، أو حفظ الملف إلى مكتبة LCS. إنها لفكرة جيدة أن يتم دائماً حفظ تسجيل المهمة كملف حزمة تسجيل مهمة (axtr.). وسوف يساعد هذا على تسهيل حفظ الملف إذا لزم تغيير الإجراءات أو التعليقات التوضيحية في وقت لاحق. إذا كنت ترغب في تحميل الملف كمستند Word، فاحفظه أيضًا كملف حزمة تسجيل مهمة.

## <a name="create-your-task-recording"></a>إنشاء تسجيل المهمة
للحصول على خطوات تفصيلية للتنقل، راجع [كيفية إنشاء تسجيل مهمة](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>نسخ وتخصيص تسجيلات المهام في Microsoft
يمكنك تنزيل وتحرير تسجيلات مهام Microsoft لاستخدامها لوثائق "تعليمات" الخاصة بك أو مواد التدريب. لتنزيل تسجيل مهمة Microsoft، اتبع الخطوات التالية:

1.  افتح مسجل المهام. يوجد مسجل المهام في قائمة **الإعدادات**.
2.  في جزء "مسجل المهام"، انقر فوق **الاحتفاظ بتسجيل.**
3.  ضمن **أين التسجيل**، انقر فوق **يوجد في مكتبة LCS‬**.
4.  انقر فوق **تحديد مكتبة LCS**.
5.  حدد مكتبة Microsoft العمومية.
6.  في الشجرة، حدد عقده مكتبة عملية الأعمال المقترن بها تسجيل المهمة.
7.  وانقر فوق **موافق**.
8.  انقر فوق **بدء**.
9.  عند هذه النقطة، قم بالتنقل خلال التسجيل، وتغيير أي خطوات عندما تقوم بإعادة تسجيلها. **ملاحظة**: إذا احتجت فقط إلى تغيير نص تسجيل، يمكنك فتح التسجيل في وضع **تحرير التعليقات التوضيحية لتسجيل**، ثم قم بحفظه.
10. بعد تشغيل التسجيل إلى النهاية، انقر فوق **إيقاف** في شريط مسجل المهام في الجزء العلوي من الشاشة.
11. قم باختيار الطريقة التي تريد بها حفظ تسجيل المهمة.

## <a name="include-your-task-recordings-in-the-help-pane"></a>تضمين تسجيلات المهام الخاصة بك في جزء التعليمات
لإظهار تسجيلات المهام المخصصة الخاصة بك في جزء "التعليمات" بحيث يمكنك تشغيلها كأدلة مهام أو عرضها كنص، يجب عليك حفظ تسجيلات المهام الخاصة بك إلى مكتبة BPM، ثم قم بتحديث معلمات نظام التعليمات للإشارة إلى مكتبة BPM. لمزيد من المعلومات، راجع [الاتصال بنظام التعليمات‬.](../../fin-and-ops/get-started/help-connect.md)

<a name="additional-resources"></a>الموارد الإضافية
--------

[نظرة عامة على التعليمات](../../fin-and-ops/get-started/help-overview.md)

[تعليمات الاتصال](../../fin-and-ops/get-started/help-connect.md)

[مسجل المهام](task-recorder.md)

[إنشاء مواضيع تعليمات باستخدام مسجل المهام" (ارتباط خارجي)](https://mbspartner.microsoft.com/AX/Videos/970)

