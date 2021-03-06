---
title: "إنشاء الحقول المخصصة واستخدامها"
description: "يوضح هذا الموضوع الكيفية التي يتيح بها لبعض المستخدمين Dynamics 365 for Finance and Operations إمكانية إنشاء حقول مخصصة لتكييف التطبيق لتلبية أعمالهم."
author: jasongre
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 1ce709a4b5cce145d841b844a21a5218ba250c87
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="create-and-work-with-custom-fields"></a>إنشاء الحقول المخصصة واستخدامها

[!include [banner](../includes/banner.md)]

بينما يوفر Microsoft Dynamics 365 for Finance and Operations مجموعة شاملة من الحقول المبتكرة لإدارة مجموعة كبيرة من عمليات الأعمال، في بعض الأحيان تكون هناك حاجة لإحدى الشركات لتعقب المعلومات الإضافية في النظام. لتلبية هذه الحاجة، يتيح لك Finance and Operations إمكانية إنشاء حقول مخصصة لتكييف التطبيق ليناسب عملك، بشرط أن يكون لديك أذونات لهذه الميزة. 

تتوفر القدرة على إضافة حقول مخصصة في تحديث النظام الأساسي 13 والإصدارات الأحدث.

يوضح هذا الفيديو مدى سهولة إضافة حقل مخصص إلى صفحة: [إضافة حقول مخصصة في Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>إنشاء الحقول المخصصة
بعد قيامك بتحديد المعلومات الإضافية التي تريد أن تتعقبها في التطبيق، يمكنك إنشاء الحقل في الجدول المناسب وعرض هذا الحقل الجديد على صفحة.   

توضح الخطوات التالية عملية إنشاء حقل مخصص ووضع هذا الحقل في نموذج.  

1.   انتقل إلى النموذج الذي تظهر فيه الحاجة إلى الحقل الجديد. 
2.   نظرًا لأن الهدف النهائي هو عرض الحقل المخصص في نموذج، توجد نقطة الإدخال لإنشاء الحقول المخصصة داخل تجربة التخصيص. افتح شريط أدوات التخصيص عن طريق تحديد **خيارات**، ثم **تخصيص النموذج**. 
3.   انقر فوق **إدراج** ثم **الحقل**.  
4.   حدد منطقة النموذج الذي تريد فيه عرض الحقل الجديد. بعد التحديد، سيعرض مربع حوار **إدراج الحقول** قائمة بالحقول الموجودة التي يمكن إدراجها في المنطقة المحددة للنموذج.  
5.   تأكد من أن الحقل الذي يهمك غير موجود بالفعل في القائمة. إذا كان الأمر كذلك، فيمكنك ببساطة تحديد هذا الحقل في القائمة وانقر فوق **إدراج**.   
6.   انقر فوق الزر **إنشاء حقل جديد** أعلى القائمة لبدء عملية إنشاء حقل مخصص. سيؤدي هذا إلى فتح مربع الحوار **إنشاء حقل جديد**. 

     إذا لم تشاهد الزر **إنشاء حقل جديد**، فإنه ليس لديك الأذونات اللازمة لاستخدام هذه الميزة.  
     
7.   في مربع الحوار **إنشاء حقل جديد**، أدخل المعلومات التالية.
     1.   حدد جدول قاعدة البيانات التي يجب إضافة هذا الحقل إليها. لاحظ أن الجداول التي تدعم الحقول المخصصة فقط ستظهر في القائمة المنسدلة. راجع القسم التالي للحصول على التفاصيل الفنية في الجداول المدعومة.  
     2.   حدد نوع بيانات الحقل الجديد. أنواع البيانات المتوفرة هي خانة الاختيار، والتاريخ، والوقت والتاريخ، والعشرية، والرقم، وقائمة الاختيار، والنص.   
          - إذا اخترت نوع بيانات النص، يمكنك أيضًا تحديد الحد الأقصى لطول النص الذي يمكن إدخاله في هذا الحقل. 
          - إذا اخترت نوع بيانات قائمة الخيارات، يمكنك أيضًا تحديد مجموعة القيم الصالحة لهذا الحقل.  
     3.   قم بتوفير اسم وعنوان ونص تعليمات للحقل. يتطابق الاسم مع اسم الحقل الفعلي في قاعدة البيانات، حيث تكون التسمية ونص التعليمات هي النص المستخدم لتمثيل هذا الحقل في واجهة المستخدم.  
8.   إذا كان هذا هو الحقل الوحيد الذي تحتاج إلى إنشائه لهذا النموذج، فانقر فوق **حفظ**. إذا كنت تحتاج إلى إنشاء حقول إضافية، فانقر فوق **حفظ وجديد** ثم أرجع إلى الخطوة 7. لاحظ أنه يوجد حاليًا حد أقصى قدره **20 حقلاً مخصصًا لكل جدول**.
9.   ستعيدك مغادرة مربع الحوار **إنشاء حقل جديد** إلى مربع الحوار **إدراج حقول**. سيتم تمييز أي حقول مخصصة تمت إضافتها للتو تلقائيًا في قائمة الحقول المُراد إدراجها في النموذج.  
10.   انقر فوق **إدراج** لإدراج الحقول المميزة في المنطقة المحددة للنموذج. 
11.   **اختياري:** قم بتمكين وضع **النقل** من شريط أدوات التخصيص لنقل الحقول الجديدة إلى موقعها المطلوب في المنطقة المحددة. راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) للحصول على مزيد من المعلومات حول كيفية استخدام إمكانيات التخصيص المختلفة لتحسين نموذج لاستخدامك الشخصي.  

## <a name="sharing-custom-fields-with-other-users"></a>مشاركة الحقول المخصصة مع مستخدمين آخرين
بعد أن تقوم بإنشاء حقل مخصص وعرضه في نموذج، فقد تحتاج إلى تقديم طريقة عرض الصفحة المحدثة هذه التي تتضمن الحقل الجديد للمستخدمين الآخرين في النظام. يمكن أن يتم ذلك بطريقتين مختلفتين باستخدام إمكانات تخصيص المنتج:

-   يتم التوجيه الموصى به من خلال مسؤول النظام، الذي يمكنه تقديم تخصيص لجميع المستخدمين أو مجموعة فرعية من المستخدمين. راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) لمزيد من التفاصيل. 

-   وبدلاً من ذلك، يمكنك تصدير التغييرات الخاصة بك (تسمى *عمليات التخصيص*) وإرسالها إلى مستخدم واحد أو أكثر وجعل كل واحد من هؤلاء المستخدمين يستورد التغييرات الخاصة بك. يتيح لك الخيار **إدارة** في شريط أدوات التخصيص إمكانية تصدير واستيراد التخصيصات.

## <a name="managing-custom-fields"></a>إدارة الحقول المخصصة

يمكن إنجاز إدارة جميع الحقول المخصصة في النظام من خلال صفحة **الحقول المخصصة** في وحدة إدارة النظام.  تتيح هذه الصفحة للمستخدمين حق الوصول إلى العديد من الإمكانات، بما في ذلك: 
-   عرض قائمة بجميع الحقول المخصصة في النظام.
-   تحرير محدود للحقول المخصصة الموجودة.
-   حذف الحقول المخصصة.
-   عرض الحقول المخصصة في كيانات البيانات.
-   تقديم ترجمات تسميات الحقول المخصصة ونص التعليمات.

### <a name="viewing-all-custom-fields"></a>عرض جميع الحقول المخصصة
توفر صفحة **الحقول المخصصة** الرؤية لجميع الحقول المخصصة التي تم تحديدها في النظام. حدد ببساطة الجدول الذي تهتم به، وسيتم تحديث الصفحة لعرض قائمة الحقول المخصصة المقترنة بهذا الجدول. سيتيح لك اختيار حقل مخصص من القائمة إمكانية عرض جميع تفاصيل هذا الحقل.

### <a name="editing-custom-fields"></a>تحرير الحقول المخصصة
بعد إنشاء حقل مخصص، يمكن تعديل أجزاء معينة فقط من المعلومات حول الحقل المخصص في صفحة **الحقول المخصصة**.   

*يمكنك* تعديل هذه السمات: 
-   التسمية 
-   نص تعليمات
-   الطول، للحقول النصية

*لا يمكنك* تحرير السمات التالية: 
-   اسم الحقل
-   نوع البيانات

بالإضافة إلى ذلك، بالنسبة لحقول قائمة الاختيار، يمكن إعادة ترتيب مجموعة القيم الصالحة للحقل المخصص، ويمكن إضافة القيم الجديدة; ومع ذلك، لا يمكن إزالة القيمة الموجودة لحقل قائمة الاختيار. تذكر أن تنقر فوق **تطبيق التغييرات** عندما تنتهي من تحرير الحقول لجدول محدد حتى يتم حفظ التغييرات. 

### <a name="exposing-custom-fields-on-data-entities"></a>عرض الحقول المخصصة في كيانات البيانات
كما قد يكون من المهم السماح بظهور الحقول المخصصة في كيانات البيانات. يتم استخدام كيانات البيانات في الميزة [فتح في Office](../../dev-itpro/office-integration/office-integration.md)، فضلاً عن سيناريوهات استيراد/تصدير البيانات.  

اتبع هذه الخطوات لعرض حقل مخصص في كيان بيانات: 
1.   حدد الحقل المخصص في نموذج **الحقول المخصصة**. 
2.   قم بتوسيع قسم **الكيانات** لعرض مجموعة الكيانات ذات الصلة.  
3.   انقر فوق الزر **تحرير**.
4.   قم بتعديل الحقل **ممكّن** المراد تحديده لكل كيان يجب أن يعرض هذا الحقل.  
5.   انقر فوق **تطبيق التغييرات** لحفظ التحديدات.  

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>السماح بعرض الحقول المخصصة بلغات أخرى
نظرًا لأنه قد تظهر الحاجة إلى وصول المستخدمين إلى الحقول المخصصة بلغات مختلفة، توفر صفحة **الحقول المخصصة** آلية للسماح بترجمة نص التعليمات والتسمية لحقل مخصص بلغات أخرى.  

توضح الخطوات التالية عملية ترجمة الحقول المخصصة بلغات أخرى: 
1.   حدد الحقل المخصص في صفحة **الحقول المخصصة**. 
2.   حدد الزر **ترجمات** في "جزء الإجراءات". سيؤدي هذا إلى فتح قائمة منسدلة بالترجمات الموجودة لهذا الحقل.
3.   تعرض القائمة المنسدلة **لغة** مجموعة اللغات التي توفير الترجمات لها بالفعل. 
     1.   إذا كنت ترغب في تحرير ترجمة موجودة، فحدد اللغة المطلوبة من القائمة وقم بتعديل القيم للتسمية ونص التعليمات.  
     2.   وإلا، انقر فوق الزر **إضافة لغة**، وحدد اللغة المطلوبة من القائمة، ثم قم بتوفير القيم المترجمة لنص التعليمات والتسمية.  
4.   انقر فوق **موافق** عند الانتهاء.  

### <a name="deleting-custom-fields"></a>حذف الحقول المخصصة
في بعض الحالات النادرة، قد تقرر أن حقل مخصص لم يعد مطلوبًا. عند حدوث ذلك، يستطيع مسؤول نظام اختيار حذف الحقل من صفحة **الحقول المخصصة**. للقيام بذلك، تأكد من تحديد الحقل الصحيح، وانقر فوق **حذف**، ثم انقر فوق **نعم** لتأكيد الحذف، وأخيرًا انقر فوق **تطبيق التغييرات**. 

> [!Note]
> لا يمكن التراجع عن هذا الإجراء، وسيؤدي ذلك إلى حذف البيانات المقترنة بهذا الحقل نهائيًا من قاعدة البيانات. 

## <a name="appendix"></a>الملحق 
### <a name="who-can-create-custom-fields"></a>مَن الذي يمكنه إنشاء الحقول المخصصة؟
كحماية للنظام، يستطيع مسؤولو النظام فقط إنشاء حقول مخصصة بشكل افتراضي. ومع ذلك، يمكن منح هؤلاء المستخدمين المحترفين الذين تعتبرهم المؤسسة ضروريين حقوق إنشاء حقول مخصصة من قِبل مسؤول نظام باستخدام دور الأمان **المستخدم المحترف للتخصيص في وقت التشغيل**. لن يتمكن المستخدمون الذين ليس لديهم دور الأمان هذا من إنشاء الحقول المخصصة، ولكن سيظل بإمكانهم رؤية والتفاعل مع الحقول المخصصة التي تمت إضافتها بواسطة مستخدمين آخرين في النظام.    

### <a name="what-tables-support-custom-fields"></a>ما الجداول التي تدعم الحقول المخصصة؟
بالنسبة للأداء والأسباب الفنية، تتيح الجداول التي تفي بالشروط التالية حاليًا إمكانية إضافة الحقول المخصصة.

- يجب أن يتم تمييز الجدول كإحدى هذه المجموعات: 
     -   مجموعة
     -   WorksheetHeader
     -   الرئيسي
     -   متنوع
     -   المحددة
     -   المرجع
     -   TransactionHeader
- لا يمكن للجدول توسيع جدول آخر.
- لا يمكن تمييز الجدول كجدول نظام.
- لا يمكن أن يكون الجدول جدولاً مؤقتًا.

