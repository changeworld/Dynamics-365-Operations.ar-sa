---
title: "نظرة عامة حول ترقية دفتر الإهلاك"
description: "في الإصدارات السابقة، كان هناك مفهومان لتقييم الأصول الثابتة- نماذج القيم ودفاتر الإهلاك. في Microsoft Dynamics 365 for Operations (1611)، تم دمج وظيفة نموذج القيم ووظيفة دفتر الإهلاك في مفهوم واحد يعرف باسم الدفتر. يوفر هذا الموضوع بعض الأشياء الواجب مراعاتها عند إجراء الترقية."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 116f9e8fbf8ed6ecbd2a1163f17e52ba80061694
ms.contentlocale: ar-sa
ms.lasthandoff: 06/13/2017

---

# <a name="depreciation-book-upgrade-overview"></a>نظرة عامة حول ترقية دفتر الإهلاك

[!include[banner](../includes/banner.md)]


في الإصدارات السابقة، كان هناك مفهومان لتقييم الأصول الثابتة- نماذج القيم ودفاتر الإهلاك. في Microsoft Dynamics 365 for Operations (1611)، تم دمج وظيفة نموذج القيم ووظيفة دفتر الإهلاك في مفهوم واحد يعرف باسم الدفتر. يوفر هذا الموضوع بعض الأشياء الواجب مراعاتها عند إجراء الترقية. 

ستقوم عملية الترقية بنقل إعدادك الموجود وكافة الحركات الموجودة إلى بنية الدفتر الجديد. سوف تبقى نماذج القيم على حالها، كدفتر يتم ترحيله إلى دفتر الأستاذ العام. سيتم نقل دفاتر الإهلاك إلى دفتر حيث تم تعيين الخيار **الترحيل إلى دفتر الأستاذ العام** إلى **لا**. سيتم نقل أسماء دفاتر اليومية لدفتر الإهلاك إلى اسم دفتر يومية دفتر أستاذ عام تم فيه تعيين طبقة الترحيل إلى **بلا**. سوف يتم نقل حركات دفتر الإهلاك إلى حركات الأصول الثابتة. 

قبل تشغيل عملية ترقية البيانات، يجب عليك فهم اثنين من الخيارات المتاحة لتحديث بنود دفتر يومية دفتر الإهلاك إلى إيصالات الحركة والتسلسل الرقمي الذي سيتم استخدامه لمسلسل الإيصال. 

الخيار 1:  **التسلسل الرقمي المعرّف من قِبل النظام** - هذا هو الخيار الافتراضي لتحسين أداء الترقية. لن تستخدم عملية الترقية إطار عمل التسلسلات الرقمية، ولكن بدلاً من ذلك ستقوم بتخصيص الإيصالات من خلال نهج يستند إلى المجموعة. بعد الترقية، سوف يتم إنشاء التسلسل الرقمي الجديد باستخدام **تعيين الرقم التالي** والتي تستند بشكل مناسب على الحركات التي تمت ترقيتها. بشكل افتراضي، سوف يكون استخدام التسلسل الرقمي في تنسيق\#\#\#\#\#\#\#\#\# . يوجد عدد قليل من المعلمات المتاحة لك لضبط التنسيق عند استخدام هذه الطريقة:

-   **كود التسلسل الرقمي** - وهو الكود المستخدم لتحديد التسلسل الرقمي. لا يُمكن إيجاد كود التسلسل الرقمي هذا حيث سيتم إنشاؤه من خلال الترقية.
    -   اسم الثابت: **NumberSequenceDefaultCode**
    -   القيمة الافتراضية: "FADBUpgr"
-   **البادئة** – قيمة السلسلة الثابتة التي سيتم استخدامها كبادئة لأرقام الإيصالات.
    -   اسم الثابت: **NumberSequenceDefaultParameterPrefix**
    -   القيمة الافتراضية: "FADBUpgr"
-   **الطول الأبجدي الرقمي‬** – طول الجزء الأبجدي الرقمي‬ في التسلسل الرقمي.
    -   اسم الثابت: **NumberSequenceDefaultParameterAlpanumericLength **
    -   القيمة الافتراضية: 9
-   **رقم البدء** - الرقم الأول لاستخدامه في التسلسل الرقمي.
    -   اسم الثابت: **NumberSequenceDefaultParameterStartNumber **
    -   القيمة الافتراضية: 1

الخيار 2: **التسلسل الرقمي المعرّف من قبل مستخدم موجود** - يتيح هذا الخيار إمكانية تحديد التسلسل الرقمي لاستخدامه للترقية. يمكنك استخدام هذا الخيار إذا احتجت إلى تكوين متقدم للتسلسل الرقمي. لاستخدام تسلسل رقمي، يجب عليك تعديل فئة ترقية ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans بالمعلومات التالية:

-   **كود التسلسل الرقمي** - كود التسلسل الرقمي.
    -   اسم الثابت: **NumberSequenceExistingCode **
    -   القيمة الافتراضية: لا قيمة افتراضية، يجب تحديثها إلى كود التسلسل الرقمي.
-   **التسلسل الرقمي المشترك** – قيمة منطقية لتحديد نطاق التسلسل الرقمي. استخدم "true" للتسلسلات الرقمية المشتركة عبر كافة الشركات و "false" لنطاق خاص بالشركة. عند استخدام "false"، يجب أن يكون التسلسل الرقمي بالاسم المحدد موجودًا في كل شركة تحتوي على حركات دفتر الإهلاك. توجد التسلسلات الرقمية المشتركة في كل قسم يحتوي على حركات دفتر الإهلاك.
    -   اسم الثابت: **NumberSequenceExistingIsShared **
    -   القيمة الافتراضية: true

توجد المحددات في بداية الفئة ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class. 

*// تحديد نهج مفضل لتوزيع الإيصالات* 
*// صحيح,إذا أردت استخدام كود تسلسل رقمي موجود* 
*// خطأ,إذا كنت تخطط لاستخدام التسلسل الرقمي المُعرّف من قبل النظام (افتراضي)* const boolean NumberSequenceUseExistingCode = false;  

*//إذا كنت تستخدم نهج التسلسل الرقمي المُعرف من قبل النظام، فعيّن محددات للتسلسل الرقمي..*
*// سيتم إنشاء تسلسل رقمي جديد مع هذه المحددات.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*//إذا كنت تستخدم نهج التسلسل الرقمي الموجود، فحدد كود التسلسل الرقمي الموجود.* 
*//سينتقل توزيع الإيصالات من صف إلى آخر للتسلسلات الرقمية الموجودة.* const str NumberSequenceExistingCode = ''; *// حدد نطاق رمز التسلسل الرقمي الموجود* 
*// صحيح, إذا كان التسلسل الرقمي المحدد مشتركًأ* 
*// خطأ, إذا كان التسلسل الرقمي المحدد حسب الشركة* 
*// سيتم استخدام التسلسل الرقمي الافتراضي المُعرّف من قبل النظام إذا لم يتم العثور على كود تسلسل رقمي مع النطاق المحدد.* const boolean NumberSequenceExistingIsShared = true; 

إعادة بناء المشروع الذي يحتوي على الفئة بعد تعديل الثوابت. 

عند استخدام نهج التسلسل الرقمي المُنشأ بواسطة النظام (الخيار 1)، سوف تستخدم عملية الترقية المعالجة المستندة إلى مجموعة لتوزيع أرقام الإيصالات كما هو محدد في محددات البرنامج النصي للترقية. وستقوم أيضًا بإنشاء تسلسل رقمي جديد باستخدام المحددات المعينة بعد التوزيع. 

عند استخدام نهج التسلسل الرقمي المعرّف من قِبل المستخدم (الخيار 2)، سوف تقوم عملية الترقية بالتحقق مما إذا كان التسلسل الرقمي مع النطاق المحدد موجودًا في قاعدة البيانات لكل قسم وشركة مع حركات كتب الإهلاك. إذا كان موجودًا، فإن عملية الترقية ستستخدم معالجة كل صف بعد الآخر لتوزيع أرقام الإيصالات كما هو محدد بواسطة التسلسل الرقمي باستخدام إطار عمل التسلسل الرقمي. إذا لم يكن التسلسل الرقمي موجودًا مع النطاق المُحدد، فإن عملية الترقية سوف تستخدم نهج التسلسل الرقمي الافتراضي المُعرّف من قبل النظام لتوزيع أرقام الإيصالات، وسوف تنشأ تسلسل رقمي جديد مع المحددات الافتراضية المحددة بعد التوزيع.

باستخدام أي من النهجين، سيستخدم أيضًا البرنامج النصي للترقية بيانات التسلسل الرقمي لحقل **مسلسل الإيصال** على أسماء دفاتر يومية دفتر الأستاذ العام الجديد التي تم إنشاؤها لأسماء دفاتر يومية دفتر الإهلاك السابق.



