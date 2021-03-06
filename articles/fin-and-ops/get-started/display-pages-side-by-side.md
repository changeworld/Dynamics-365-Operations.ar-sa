---
title: "إظهار الصفحات جنبًا إلى جنب باستخدام الميزة \"فتح في نافذة جديدة\""
description: "تشرح هذه المقالة كيفية عرض الصفحات جنبًا إلى جنب في Microsoft Dynamics 365 for Finance and Operations."
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 8e3ef29618f11b0f247999e3a24e54bff44bf51a
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a>إظهار الصفحات جنبًا إلى جنب باستخدام الميزة "فتح في نافذة جديدة"

[!include [banner](../includes/banner.md)]

تشرح هذه المقالة كيفية عرض الصفحات جنبًا إلى جنب في Microsoft Dynamics 365 for Finance and Operations.

يساعدك Microsoft Dynamics 365 for Finance and Operations في تنفيذ المهام بكفاءة. وفي بعض الحالات، قد تحتاج إلى عرض عدة صفحات بجوار بعضها البعض لإنجاز المهام بسرعة. على سبيل مثال، قد تحتاج إلى التحقق من صحة أو إدخال بنود في أكثر من دفتر يومية واحد. وبشكل عام، ذلك يجب عليك الانتقال للأمام وللخلف بين الصفحة التي تعرض قائمة بدفاتر اليومية والصفحة التي تعرض بنود لدفتر يومية محدد. ومع ذلك، تتيح لك ميزة **فتح في نافذة جديدة** عرض هذه الصفحات جنبًا إلى جنب لكي تتمكن من تنفيذ مهامك بسرعة. 

ومن خلال المتابعة إلى المثال المذكور أعلاه، عند عرض البنود، يمكنك النقر فوق الأيقونة **فتح في نافذة جديدة**. 

[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) 

يؤدي النقر فوق الأيقونة **فتح في نافذة جديدة** إلى فتح صفحة البنود في نافذة مستعرض جديدة ومنبثقة، ثم العودة إلى نافذة المستعرض الأصلي السابقة التي عرضت قائمة بدفاتر اليومية. يمكنك بعد ذلك عرض كلا الصفحتين جنبًا إلى جنب. وعند الانتهاء من عرض دفتر يومية، يمكنك تغيير دفتر اليومية المحدد في صفحة قائمة دفتر اليومية، وستقوم صفحة البنود في النافذة المنبثقة تلقائيًا بعرض بنود دفتر اليومية المحددة حديثًا. 

[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) 

يحدث الربط والتحديث الحيويان نتيجة للعلاقات القائمة بين البيانات التي تدعم هذه الصفحات. إذا لم يكن النظام على علم بالعلاقة بين البيانات، فلن يتم تحديث النافذة المنبثقة بشكل تلقائي استجابة لتغيير في النافذة التي تأتي منها. 

وتحتوي بعض الصفحات على طرق عرض متعددة مثل عرض الشبكة وعرض الرأس وعرض التفاصيل. تتسبب الأيقونة **فتح في نافذة جديدة** في فتح الصفحة بأكملها في نافذة مستعرض جديدة. ولذلك، لا يمكنك الاحتفاظ بطريقتي عرض لنفس الصفحة جنبًا إلى جنب باستخدام ميزة **فتح في نافذة جديدة**. ومع ذلك، تشتمل معظم هذه الصفحات على قائمة تنقل يمكنك استخدامها للتنقل بين السجلات وتحقيق تجربة مماثلة. 

وقبل استخدام ميزة **الفتح في نافذة جديدة**، يجب عليك تكوين منع العناصر المنبثقة في المستعرض للسماح بالنوافذ المنبثقة من عنوان URL لموقع Finance and Operations. على سبيل مثال، قد تسمح بالنوافذ المنبثقة من "\*.dynamics.com". 

ولا تتوفر ميزة **فتح في نافذة جديدة** إلا عند وجود أكثر من صفحة واحدة مفتوحة في النافذة. وكذلك، تنغلق النافذة المنبثقة تلقائيًا عندما لا يعود هناك أي صفحات أخرى مفتوحة (أي، عند إغلاق الصفحة الأخيرة في هذه النافذة). ويقوم Finance and Operations أيضًا بإغلاق الصفحات المفتوحة عندما تنتقل إلى ناحية أخرى في التطبيق. وبالتالي، إذا كان لديك نوافذ منبثقة مفتوحة وانتقلت إلى منطقة أخرى في التطبيق، فسيتم إغلاق النوافذ المنبثقة تلقائيًا بسبب إغلاق الصفحات الموجودة في هذه النوافذ بواسطة النظام. 

ويعرض الشريط العلوي في النوافذ المنبثقة المعلومات حول الشركة التي تم فتح الصفحة فيها وتكون للقراءة فقط. وتعتمد النوافذ المنبثقة أيضًا على نافذة مستعرض Finance and Operations الرئيسية. وإذا تم إغلاق النافذة الرئيسية أو تحديثها، ستصبح كافة النوافذ المنبثقة المفتوحة للقراءة فقط. ويعني هذا أنه لا يزال يمكنك عرض المعلومات في هذه الإطارات، ولكن لن تكون قادراً على التعامل معها.




