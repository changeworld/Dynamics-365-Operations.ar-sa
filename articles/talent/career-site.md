---
title: "وظيفة موقع الوظائف في Attract"
description: "توفر هذه المقالة نظرة عامة على وظيفة موقع الوظائف المخصص للمرشحين في Microsoft Dynamics 365 for Talent - Attract. وتشرح أيضًا كيفية إعداد هذه الوظيفة."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: ar-sa
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>وظيفة موقع الوظائف في Attract

[!include [banner](includes/banner.md)]

توفر هذه المقالة نظرة عامة على وظيفة موقع الوظائف المخصص للمرشحين في Microsoft Dynamics 365 for Talent: Attract. وتشرح أيضًا كيفية إعداد هذه الوظيفة.

## <a name="overview"></a>نظرة عامة

يوفر Attract موقع وظائف لكل بيئة مستأجر. على سبيل المثال، إذا كان لدى إحدى المؤسسات بيئة تطوير وبيئة اختبار، فسيتم توفير موقع وظائف لبيئة التطوير، وموقع وظائف آخر لبيئة الاختبار. ويعتبر كل موقع وظائف **معزولاً بشكل كامل** ولديه آلية مصادقة خاصة به. لا تتم مشاركة ملفات تعريف المرشحين بين مواقع الوظائف.

بشكل افتراضي، موقع الوظائف هو موقع عام. وبالتالي، بإمكان المرشحين عرض جميع الوظائف الموضع عليها علامة كوظائف خارجية من دون الحاجة إلى تسجيل الدخول. ومع ذلك، تتطلب كافة الإجراءات الأخرى قيام المرشحين بتسجيل دخولهم.

## <a name="career-site-management"></a>إدارة موقع الوظائف

يتم التحكم في العناصر التالية في موقع الوظائف بواسطة الإعدادات:

- **اسم المؤسسة:** يظهر اسم المؤسسة على شريط التنقل الموجود أعلى موقع الوظائف. من خلال تحديد اسم المؤسسة، ينتقل المرشحون إلى صفحة تسرد جميع الوظائف المفتوحة.
- **شعار المؤسسة:** تظهر صورة شعار المؤسسة في الجزء الأيمن العلوي من موقع الوظائف. من خلال تحديد صورة الشعار، ينتقل المرشحون إلى صفحة تسرد جميع الوظائف المفتوحة.

لتعيين قيم لاسم وشعار المؤسسة، سجّل الدخول إلى Attract كمسؤول، وحدد **مركز الإدارة** في قائمة **الإعدادات** (رمز الترس)، ثم حدد علامة التبويب **معلومات الشركة**.

> [!NOTE]
> يبلغ الطول الثابت لصورة الشعار التي تظهر في موقع الوظائف 20 بكسل (px). ويتغير حجم الصورة التي تضيفها في مركز الإدارة لتمكين الاحتواء. وبالتالي، قد يتغير العرض استنادًا إلى الصورة.

## <a name="career-site-url"></a>عنوان URL لموقع الوظائف

عند [نشر وظيفة خارجية](./Creating-jobs-Attract.md#postings) للمرة الأولى، يمكنك نسخ الارتباط **تقديم طلب** من تطبيق Attract. سيكون عنوان URL لهذا الارتباط بالتنسيق التالي: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

عنوان URL لموقع الوظائف هو سلسلة فرعية من عنوان URL **تقديم طلب**. وهو يتكوّن من كل شيء وصولاً إلى اسم الشركة. وبالتالي، لعنوان URL السابق **تقديم طلب**، عنوان URL لموقع الوظائف هو `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>خيارات المصادقة

تتوفر للمرشحين خيارات تسجيل الدخول التالية في موقع وظائف Attract:

- الحساب الشخصي:

    - LinkedIn
    - Microsoft
    - Google
    - Facebook

- حساب عمل أو مدرسة:

    - Microsoft Azure Active Directory (Azure AD)

معلومات تسجيل الدخول إلى Azure AD مخصصة فقط للمرشحين الداخليين. وبالتالي، فهي تُستخدم فقط من قِبل المرشحين الداخليين الذين يستخدمون أوراق اعتماد Azure AD لشركتهم. على سبيل المثال، يريد مرشح يعمل حاليًا لدى Contoso Ltd تقديم طلب الحصول على وظيفة في شركة ليست ذات صلة بها، Alpine Ski House في هذه الحالة، لن ينجح التسجيل الدخول إذا حاول الموظف استخدام بيانات اعتماده في Azure AD من Contoso Ltd.

## <a name="create-and-maintain-a-profile"></a>إنشاء ملف تعريف والمحافظة عليه.

بعد قيام المرشحين بتسجيل الدخول إلى موقع الوظائف، بإمكانهم اختيار **ملف التعريف الخاص بي** على شريط التنقل الموجود أعلى الصفحة لإنشاء ملف تعريفهم والمحافظة عليه. يتضمن ملف التعريف معلومات شخصية ومعلومات حول الخبرة المهنية وتفاصيل حول التعليم ومستندات وارتباطات ومعلومات حول مجموعات المهارات. يمكن استخدام ملف التعريف، بعد إنشائه، لتقديم طلبات الحصول على الوظائف التي يهتم بها المرشح. باستطاعة ملفات تعريف أيضًا أن تساعد Attract على التوصية بالوظائف المناسبة للمرشحين.

## <a name="find-the-right-job"></a>العثور على الوظيفة الصحيحة

في صفحة القائمة الوظائف، بإمكان المرشحين البحث عن وظيفة معينة عن طريق إدخال مصطلحات البحث. تبحث وظيفة البحث عن مصطلحات البحث في المسميات الوظيفية وأوصاف الوظيفة، وتعرض الوظائف ذات الصلة كنتائج. بإمكان المرشحين تصفية النتائج في أي وقت، استنادًا إلى موقع الوظيفة أو مهمة الوظيفة.

وبإمكان المرشحين أيضًا عرض مجموعة من الوظائف الموصى بها في موقع الوظائف. تستند الوظائف الموصى بها لمرشح مرشح إلى استمارات التقديم السابقة للمرشح وملف تعريفه وسيرها الذاتية.

> [!NOTE]
> تظهر توصيات الوظائف فقط إذا تم نشر 10 وظائف على الأقل في موقع الوظائف، وإذا كان الموظف قد أكمل ملف تعريفها.

## <a name="apply-for-jobs"></a>تقديم طلبات للحصول على وظيفة

بعد عثور المرشحين على الوظيفة الصحيحة، يمكنهم تقديم الطلب باستخدام الزر **تقديم طلب** في صفحة تفاصيل الوظيفة. في هذه المرحلة، بإمكان المرشحين إنشاء ملف تعريف جديد بالكامل أو مراجعة المعلومات الموجودة في ملف تعريفهم الموجود. بإمكان المرشحين أيضًا تحميل سيرة ذاتية، كما هو مطلوب، ثم إرسال استمارة التقديم للوظيفة.

## <a name="check-application-status"></a>التحقق من حالة استمارة التقديم‬

بعد تقدم المرشحين بطلبات لوظيفة أو أكثر، يمكنهم تحديد **استمارات التقديم** على شريط التنقل الموجود أعلى الصفحة لعرض استمارات التقديم المفتوحة والمغلقة عندما يفتح المرشحون إحدى استمارات التقديم الخاصة بهم، يمكنهم الاطلاع على المرحلة الحالية وعلى أي إجراءات معلقة يجب عليهم إكمالها. على سبيل المثال، إذا كان يجب على المرشح توفير التواريخ المحتملة لموعد مقابلة شخصية، تعرض له الصفحة خياراته.

## <a name="internal-jobs"></a>الوظائف الداخلية

في الوقت الحالي، الوظائف المميزة كوظائف داخلية ومنشورة في موقع الوظائف في Attract لا تظهر في موقع الوظائف ويمكن الوصول إليها فقط عبر عنوان URL المباشر **تقديم طلب** الذي يمكن نسخه من استمارة التقديم في Attract.

