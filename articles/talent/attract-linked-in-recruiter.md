---
title: "التوريد باستخدام LinkedIn Recruiter"
description: "يوفر هذا الموضوع معلومات حول استخدام التعلم الآلي‬ للحصول على توصيات بشأن وظيفة ومرشح الوظيفة."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: ar-sa
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a>التوريد باستخدام LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

يُعتبر LinkedIn أكبر قاعدة بيانات للمواهب في العالم، وهو في أغلب الأحيان النظام الرئيسي الذي يستعين به مسؤولو التعيين للبحث عن مرشحين للوظائف التي يسعون إلى ملئها وللتواصل مع هؤلاء المرشحين وتوريدهم. يسهل تكامل LinkedIn Recruiter مع Dynamics 365 for Talent: Attract المستخدمين عملية التوظيف للمستخدمين ويحافظ على مزامنة البيانات بين النظامين.

> [!NOTE]
> إنك تحتاج إلى المكون الإضافي Comprehensive Hiring ومقاعد LinkedIn Recruiter كي تتمكن من استخدام تكامل LinkedIn Recruiter مع Attract.

## <a name="set-up-linkedin-recruiter-with-attract"></a>إعداد LinkedIn Recruiter مع Attract 

قبل أن تتمكن من استخدام قدرات LinkedIn Recruiter، يجب عليك تكوين الوصول على مستوى العقد أو على مستوى الشركة مع مثيل Attract. لإكمال عملية التكوين، ستحتاج إلى العمل مع المستخدم الذي يؤدي دور المسؤول في عقد LinkedIn Recruiter. أكمل الخطوات التالية لتكوين LinkedIn Recruiter مع Attract.

1.  سجّل الدخول إلى Attract كمسؤول، وانتقل إلى **إعدادات المسؤول**.

2.  في الجزء الأيمن، انقر فوق علامة تبويب **تكامل LinkedIn**.

[![طريقة عرض مسؤول Attract لبدء تكامل LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  انقر فوق **اتصال** لبدء الإعداد وكي يتم توجيهك من خلال عملية تسجيل الدخول LinkedIn.

4.  إذا كان لديك مقاعد في عقود LinkedIn متعددة، فحدد العقد الذي تريد توصيله بنظام Attract. إذا كان لديك مقعد في عقد LinkedIn واحد فقط، فلن تحتاج إلى هذه الخطوة.

5.  يتم الآن تحميل عنصر واجهة مستخدم LinkedIn في إعدادات المسؤول مع قائمة عمليات التكامل التي تظهر. ضمن **Recruiter System connect**، انقر فوق **طلب**.

[![طريقة عرض مسؤول Attract لطلب تكامل LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  بعد طلب التكامل من Attract، سوف يظهر على شكل **الشريك جاهز** وسيكون جاهزًا لتشغيله من **إعدادات مسؤول التعيين**. إذا رأيت **إعلام الشريك** على هذه الصفحة، فانتظر بضع ثوان، وانقر فوق **إعلام الشريك**، ثم قم بتحديث الصفحة. يجب أن يظهر الآن على الشكل **الشريك جاهز**.

[![طريقة عرض المسؤول في Attract للإشارة إلى استكمال الطلبات من جانب Attract](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

لإكمال الخطوة التالية، تحتاج إلى امتياز المسؤول على عقد LinkedIn Recruiter.

7.  سجّل دخولك إلى LinkedIn باستخدام حساب المسؤول وانتقل إلى LinkedIn Recruiter في الجانب العلوي الأيسر. 

8. في قائمة **المزيد** في أعلى الشاشة، انقر فوق **إعدادات المسؤول**، ثم فوق علامة التبويب **ATS**.

سيكون نظام Attract مدرجًا مع بعض الخيارات التي يمكن تشغيلها.

9. إذا أردت تمكين التصدير بنقرة واحدة **لمؤشر In-ATS** و**عنصر واجهة مستخدم ملف تعريف In-ATS**، حدد **الوصول على مستوى الشركة**. إذا أردت تمكين كافة ميزات الوصول على مستوى الشركة بالإضافة إلى سجل InMail وسجل الملاحظات والوصول إلى ملف تعريف InMail الموجز، فحدد **الوصول على مستوى العقد**.

10. قم بتشغيل مستوى الوصول المطلوب من إعدادات LinkedIn Recruiter **Admin-ATS**.

[![تشغيل تكامل Attract من طريقة عرض مسؤول LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)

12. عد إلى إعدادات مسؤول Attract بصفتك AttractAdmin وحدد علامة التبويب **تكامل LinkedIn**. من المفترض أن ترى الآن تحميل عنصر واجهة مستخدم LinkedIn الذي يعرض **ممكّن** مع تشغيل مستوى الوصول المحدد.

[![اكتمال تكامل LinkedIn Recruiter](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>استخدام قدرات LinkedIn Recruiter

بعد تمكين قدرات LinkedIn بواسطة مسؤول Attract، يمكن لمسؤولي التعيين ومدراء التوظيف الوصول إليها. لاستخدام هذه القدرات، قم بتوصيل حسابك في LinkedIn ضمن **إعدادات المستخدم**. ستتوفر قدرات متعددة بعد توصيل إعدادات المسؤول والمستخدم.

### <a name="in-ats-profile-widget"></a>عنصر واجهة المستخدم لملف التعريف In-ATS

يمكن عرض ملف تعريف LinkedIn للمرشح في Attract. سيعرض عنصر واجهة مستخدم LinkedIn ملف تعريف المرشح عندما تتطابق معلومات ATS مع معلومات LinkedIn لمستخدميها.

لعرض ملف تعريف، انتقل إلى ملف تعريف المرشح من مجموعة وظائف أو مجموعة مواهب. في ملف تعريف المرشح، حدد علامة تبويب **LinkedIn**، وسيتم تحميل عنصر واجهة مستخدم ملف التعريف. باستخدام عنصر واجهة مستخدم ملف التعريف، يمكنك الإشارة إن كان هذا التطابق الصحيح. إذا لم يكن كذلك، فابحث عن الشخص المناسب. يمكنك أيضًا حفظ المرشح إلى مشاريعك في LinkedIn Recruiter من هذه الصفحة.

### <a name="1-click-export"></a>التصدير بنقرة واحدة 

أثناء توريد المرشحين في LinkedIn، يمكنك تصدير بنقرة واحدة مرشح الوظائف المفتوحة حاليًا. أكمل الخطوات التالية للتصدير بنقرة واحدة. قبل إتمام هذه الخطوات، تأكد من أنك تملك دور مدير التوظيف أو مسؤول التعيين للوظيفة وأن هذه الوظيفة موجودة في مرحلة **الموظف المحتمل**.

1.  أنشئ الوظيفة وعيّن الأدوار المناسبة وقم بتنشيط الوظيفة.

2.  عندما يتم تنشيط الوظيفة، انتقل إلى LinkedIn Recruiter.

3.  ابحث عن المرشح الذي تراه مناسبًا للوظيفة ثم انتقل إلى ملف تعريفه.

4.  باستخدام مربع بحث الوظيفة الموجود في بطاقة جهة الاتصال، ابحث عن الوظيفة باستخدام المسمى الوظيفي أو معرّف الوظيفة الذي تم تنشيطه في Attract. إذا لم تعثر على الوظيفة، فانقر فوق **تغيير ATS‎** للعثور على مثيل Attract الصحيح.

5. بعد تحديد الوظيفة، انقر فوق **تصدير**. تم الآن إحضار الموظف بواسطة Attract.

6.  انتقل إلى Attract وافتح الوظيفة المناظرة. سوف تعثر على المرشح الذي قمت للتوّ بتصديره في مرحلة **المرشح المحتمل** للوظيفة.

### <a name="in-ats-indicator"></a>مؤشر In-ATS 

باستخدام LinkedIn Recruiter، يمكنك تعقب ما إذا كان المرشح قد تقدم بطلبات حصول على وظائف أخرى في مؤسستك، والاطلاع على وجودهم في مختلف مراحل تقديم طلبات الوظائف وعرض الملاحظات والتعليقات من LinkedIn Recruiter.

1.  افتح LinkedIn Recruiter وحدد موقع ملف تعريف المرشح الذي تبحث عنه.

2.  قم بالتمرير لأسفل لعرض القسم **In-ATS** في ملف تعريف المرشح.

3.  يمكنك استخدام عنصر واجهة المستخدم هذا لعرض كافة المعلومات المتعلقة بالمرشح الموجود في Attract من ضمن طريقة عرض LinkedIn Recruiter.

4.  حدد علامة التبويب **الوظائف والحالات** للاطلاع على الوظائف التي هي عبارة عن جزء منها، والحالات الأخيرة، وكيف تم نقلها في مقابل كل وظيفة.

5.  حدد علامة التبويب **ملاحظات المقابلة** للاطلاع على الملاحظات التي أرسلها المحاورون في Attract.

6.  حدد علامة تبويب **الملاحظات** لمشاهدة الملاحظات التي تم التقاطها لمقدم الطلب هذا في Attract.

### <a name="inmail-history"></a>محفوظات InMail

تتوفر محفوظات LinkedIn InMail مع وصول على مستوى العقد مع LinkedIn Recruiter. عند تمكينها، يمكنك عرض محفوظات InMail بالكامل مع المرشح. يمكنك أيضًا معرفة من هم الأشخاص الآخرون في مؤسستك الذين تبادلوا InMailمع المرشح، ولكن لا يمكنك الاطلاع على محتوى الرسائل بينهم.

لعرض محفوظات InMail، انتقل إلى ملف تعريف المرشح، وانتقل إلى علامة التبويب **LinkedIn** وقم بالتمرير إلى أسفل الصفحة لعرض المحفوظات. يمكنك عرض محفوظات InMail فقط إذا كان المرشح قد استجاب لطلبك واختار مشاركة ملف تعريفه معك في LinkedIn. تتزامن الرسائل من InMail مع Attract كل ساعتين.

### <a name="notes-history"></a>محفوظات الملاحظات 

تتوفر محفوظات ملاحظات LinkedIn مع وصول على مستوى العقد مع LinkedIn Recruiter. عند تمكين هذه المحفوظات، يمكنك عرض الملاحظات حول المرشح التي التقطها مسؤولو تعيين مختلفين من مؤسستك.

لعرض محفوظات الملاحظات، انتقل إلى ملف تعريف المرشح، وانتقل إلى علامة التبويب **LinkedIn** وقم بالتمرير إلى أسفل الصفحة لعرض المحفوظات. يمكنك عرض كافة الملاحظات حول المرشح من LinkedIn Recruiter.

### <a name="inmail-stub-profile"></a>ملف تعريف InMail الموجز

يتوفر ملف تعريف InMail الموجز مع وصول على مستوى العقد مع LinkedIn Recruiter. إذا وافق المرشح على مشاركة ملفات تعريفه في LinkedIn مع أي مستخدم في مؤسستك، فيمكن تعقب المرشحين في Attract، وسيتم إنشاء سجل مرشح جديد لكل المرشح.

لعرض قائمة المرشحين، انتقل إلى **مجموعات المواهب** للاطلاع على مجموعة مواهب LinkedIn أنشأها النظام. تحتوي مجموعة المواهب هذه على المرشحين المدرجين وملفات تعريفهم الموجزة كما تم استلامها من LinkedIn، حيث يظهر الاسم الأول للمرشح واسم عائلته. سيظهر معرّف البريد الإلكتروني للمرشح إذا اختار المرشح مشاركة عنوان بريده الإلكتروني.

