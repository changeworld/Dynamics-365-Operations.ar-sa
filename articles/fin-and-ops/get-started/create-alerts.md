---
title: "إنشاء قواعد تنبيه"
description: "يشمل هذا الموضوع معلومات حول التنبيهات ويوضح كيفية إنشاء قاعدة تنبيه بحيث يتم إعلامك بالأحداث مثل تاريخ يتم بلوغه أو تغييرًا محددًا يحدث."
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 78e1e6f7be04e1d4fecae080cbd4a285358590fb
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="create-alert-rules"></a>إنشاء قواعد تنبيه

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>بدء الاستخدام
قبل إعداد قاعدة تنبيه، قرر متى وفي أي مواقف تحتاج فيها إلى تلقي التنبيهات. عندما تعرف الحدث الذي تريد إعلامك به، في Microsoft Dynamics 365 for Finance and Operations، ابحث عن الصحة التي توجد فيها البيانات التي تؤدي إلى ظهور هذا الحدث. يمكن أن يكون الحدث تاريخًا يتم بلوغه أو تغييرًا محددًا يحدث. لذلك، يجب البحث عن الصفحة التي يتم فيها تحديد التاريخ، أو الحقل الذي تظهر فيها هذه التغييرات أو السجل الجديد الذي تم إنشاؤه. بعد أن تتوفر لديك هذه المعلومات، يمكنك إنشاء قاعدة التنبيه.

عندما تقوم بإنشاء قاعدة تنبيه، يمكنك تحديد المعايير التي يجب أن تتحقق قبل أن يتم تشغيل أحد التنبيهات. ويمكنك التفكير في معايير تمثل حالة من التوافق بين حدوث حدث وتحقق شروط محددة. وعند حدوث حدث معين، يبدأ النظام في إجراء فحص وفقًا للشروط التي تم إعدادها في Finance and Operations.

## <a name="events"></a>الأحداث
قد يكون الحدث الذي يقوم بتشغيل قاعدة تنبيه تاريخ يتم بلوغه أو تغييرًا محددًا يحدث. يتم تحديد مشغلات الأحداث في علامة التبويب السريعة **تنبيهي عند** في مربع الحوار **إنشاء قاعدة تنبيه**. تعتمد الأحداث المتوفرة لحقل محدد على المشغل الذي تم تحديده.

على سبيل المثال، إذا كنت تقوم بإعداد قاعدة تنبيه لحقل **تاريخ البدء**، تكون أحداث تواريخ الاستحقاق‬ مناسبة. ولذلك، يكون نوع الحدث **مستحق في‬** متوفرًا لهذا الحقل. ومع ذلك، بالنسبة لحقل مثل **مركز التكلفة**، لا يكون حدث تاريخ الاستحقاق مناسبًا. ولذلك، يكون نوع الحدث **مستحق في‬** غير متوفر. بدلاً من ذلك، يكون نوع الحدث **تم تغييره** متوفرًا.

## <a name="event-types"></a>أنواع الحدث
يمكن أن تحدث ثلاثة أنواع من الأحداث:

- **أحداث إنشاء-نوع وحذف-نوع‬** - تشغل هذه الأحداث أحد التنبيهات عندما يتم إنشاء سجل أو حذفه.
- **أحداث من نوع التحديث** - تشغل هذه الأحداث أحد التنبيهات عندما تتغير البيانات الموجودة في حقل معين.
- **أحداث من نوع تاريخ الاستحقاق** - تشغل هذه الأحداث أحد التنبيهات عندما تصل إلى تاريخ.
    
يمكن للتغييرات التي تحدث أن تبدأ من قِبل مستخدم. على سبيل المثال، يقوم مستخدم بتغيير تاريخ التسليم لأمر الشراء. بدلاً من ذلك، يمكن أن تحدث التغييرات كجزء من عملية. على سبيل المثال، يتغير الحقل **حالة** في صفحة لإظهار دورة حياة العديد من العمليات في النظام.

## <a name="conditions"></a>الحالات
في علامة التبويب السريعة **التنبيه عن** في مربع الحوار **إنشاء قاعدة تنبيه‬**، يمكنك استخدام الشروط للتحكم عندما يتم تنبيهك بشأن أحداث.

على سبيل المثال، يمكنك تحديد أن النظام يجب أن يقوم بتنبيهك عندما تتغير حالة أوامر الشراء، ولكن فقط إذا كانت الحالة تتطابق مع مجموعة معينة من الشروط. بشكل خاص، أنت تريد أن تتلقى تنبيهًا عندما يتم تعيين حالة أمر الشراء إلى **مُستَلم**. هذا التغيير في الحالة هو الحدث الذي يشغل التنبيه.

بعد ذلك، يجب أن تحدد أوامر الشراء التي ترغب في أن يتم تنبيهك إليها. على سبيل المثال، يمكنك تحديد أحد الخيارات التالية. تحديد هذه الخيارات شروط قاعدة التنبيه.

- **السجل الحالي المحدد** -تتلقى تنبيهًا عندما تتغير حالة أمر شراء محدد إلى **مُستَلم‬**.
- **جميع السجلات** - تتلقى تحذيرًا عند تغيير حالة أمر شراء لصنف في طريقة عرض الصفحة النشطة. يمكنك استخدام التصفية المتقدمة المتوفرة على الصفحة لإنشاء قواعد لمجموعة معينة من السجلات. على سبيل المثال، يمكنك إنشاء تنبيه يتم تشغيله لجميع أوامر الشراء للعملاء في مجموعة عملاء محددة.
    
## <a name="expiry-of-rule"></a>انتهاء صلاحية القاعدة
في علامة التبويب **‏‫التنبيه حتى‬** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد المدة التي يجب أن تكون قاعدة التنبيه نشطة خلالها.

## <a name="alert-contents"></a>محتويات التنبيهات
في علامة التبويب السريعة **التنبيه باستخدام** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد نص الموضوع ونص الرسالة التي يجب أن تستخدمها رسائل التنبيه.

## <a name="user-id"></a>معرّف المستخدم
في علامة التبويب السريعة **‏‫التنبيه باستخدام‬** في مربع الحوار **إنشاء قاعدة تنبيه**، يمكنك تحديد المستخدم الذي يجب أن يتلقى رسائل التنبيه. بشكل افتراضي، يتم تحديد معرف المستخدم الخاص بك. يتم تقييد هذا الخيار على مسؤولي المؤسسة.

## <a name="create-an-alert-rule"></a>إنشاء قاعدة تنبيه
1. افتح الصفحة التي تحتوي على البيانات المطلوب مراقبتها.
2. في جزء الإجراءات، في علامة التبويب **خيارات**، في المجموعة **مشاركة**، حدد **إنشاء قاعدة تنبيه**.
3. في مربع الحوار **إنشاء قاعدة تنبيه**، في الحقل **حقل**، حدد الحقل المطلوب مراقبته.
4. في الحقل **حدث**، حدد نوع الحدث.
5. في علامة التبويب السريعة **‏‫التنبيه عن‬**، حدد أحد الخيارات.
6. إذا كان يجب أن تكون القاعدة غير نشطة في تاريخ معين، في علامة التبويب السريعة **التنبيه حتى‬**، فحدد تاريخ انتهاء.
7. في علامة التبويب السريعة **التنبيه باستخدام** في الحقل **موضوع**، اقبل عنوان الموضوع الافتراضي لرسالة البريد الإلكتروني أو أدخل موضوعًا جديدًا. يتم استخدام النص كعنوان للموضوع لرسالة البريد الإلكتروني التي تتلقاها عند تشغيل تنبيه.
8. في الحقل **رسالة**، أدخل رسالة اختيارية. يتم استخدام النص كرسالة تتلقاها عند تشغيل تنبيه.
9. حدد **موافق** لحفظ الإعدادات وإنشاء قاعدة التنبيه.

