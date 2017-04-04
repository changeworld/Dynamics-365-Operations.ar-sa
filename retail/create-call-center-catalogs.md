---
title: "إنشاء كتالوج مركز الاتصالات"
description: "توفر هذه المقالة نظرة عامة على عملية إنشاء كتالوج‬ لمركز اتصالات."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 857d280ab6d846c19102dd053a2c5f27fe14654c
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-call-center-catalog"></a>إنشاء كتالوج مركز الاتصالات

توفر هذه المقالة نظرة عامة على عملية إنشاء كتالوج‬ لمركز اتصالات. 

في مركز الاتصال، يمكنك استخدام كتالوجات منتجات لتحديد المنتجات التي تريد عرضها للعملاء. عادة، تستخدم مراكز الاتصال الكتالوجات المطبوعة. تتم معالجة تصميم وإنتاج الكتالوجات المطبوعة خارج Microsoft Dynamics 365 للعمليات. ومع ذلك، يمكنك إنشاء وتخزين نموذج رقمي لنشره مصورة في البيع بالتجزئة والتجارة في ديناميات 365 للعمليات باستخدام نفس النماذج التي استخدمت لإعداد كتالوجات التجزئة على الإنترنت. قبل إنشاء كتالوج، يجب إعداد عمليات فرز المنتجات وتعيين عمليات الفرز إلى مركز اتصال. يمكنك أيضا إضافة منتجات إلى الكتالوج من خلال تحديد المنتجات من عمليات الفرز هذه. بعد إضافة المنتجات إلى الكتالوج واكتمال الكتالوج، يجب التحقق من صحة الكتالوج للتحقق من البيانات. ثم يجب إرسال الكتالوج لمراجعته واعتماده. وبعد الموافقة على الكتالوج، يمكن نشره. عندما يتم إنشاء كتالوج مركز الاتصال، يمكنك أخذ لقطة من بيانات الكتالوج في الوقت الذي يتم نشر الكتالوج فيه. تتيح لك وظيفة اللقطة هذه الوصول إلى إصدار معين من الكتالوج حتى في حالة تغيير الكتالوج وتحديثه لاحقاً. يمكن أيضا إعداد كتالوجات مركز الاتصال لتتضمن الميزات الاختيارية التالية.

-   **رموز المصدر** – الرموز المستخدمة لتعقب استجابة العملاء للمراسلات البريدية لكتالوج معين.
-   **المنتجات المجانية** - المنتجات المضمنة في أمر العميل بدون تكلفة إضافية. تتم إضافة هذه المنتجات إلى الأمر تلقائياً عند إدخال التعليمات البرمجية المصدر للكتالوج في الأمر.
-   **البرامج النصية** – النصوص التي يقوم عامل مركز الاتصال بقرائتها للعميل عند إنشاء أمر مبيعات. يمكن أن تتضمن البرامج النصية التهاني أو اقتراحات الشراء.
-   **الأصناف الإضافية أو المكملة** - الأصناف التي يتم عرضها كاقتراح عند إضافة منتج معين إلى الأمر.

يجب إعداد هذه الخيارات قبل اعتماد الكتالوج ونشره.

## <a name="prerequisites"></a>المتطلبات الأساسية
يجب إكمال المهام التالية قبل البدء في:

-   إعداد منتجات وعمليات فرز المنتجات.
-   إعداد منتجات البيع بالتجزئة
-   إعداد عملية فرز.
-   إنشاء مركز اتصال.
-   إعداد مركز اتصال
-   إضافة مركز اتصال لتدرج هرمي للمؤسسات.
-   إنشاء تدرجي هرمي للمؤسسة وتعديله.

## <a name="create-a-catalog"></a>إنشاء كتالوج
يجب أولاً إنشاء كتالوج، ثم إضافة منتجات إلى الكتالوج ثم مراجعة وتحديث السمات الخاصة بالمنتجات.

## <a name="validate-the-catalog"></a>التحقق من صحة الكتالوج
بعد الانتهاء من إعداد الكتالوج، يجب التحقق من صحته. يتم من خلال هذه العملية التحقق من أن البيانات المطلوبة لسمات القناة وسمات المنتج كاملة وصحيحة، وأنه تم نشر الكتالوج.

## <a name="submit-the-catalog-for-review-and-approval"></a>إرسال الكتالوج للمراجعة والاعتماد
بعد التحقق من صحة كتالوج، يمكنه إرساله للمراجعة والموافقة عليه. يجب الموافقة على الكتالوج قبل نشره. يمكنك تكوين سير العمل حتى تتم الموافقة على الكتالوج تلقائيًا أو يجب الموافقة عليه يدويًا.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>اختياري: إضافة التعليمات البرمجية المصدر والمنتجات المجانية والبرامج النصية
يمكنك أيضًا إضافة الأصناف التالية إلى كتالوج مركز اتصال. هذه الأصناف اختيارية.

-   **الأكواد المصدر** يمكن استخدامها من قِبل الشركات التي تقدم الكتالوجات المطبوعة لتعقب استجابة العملاء لكتالوجات معينة. غالباً ما تطبع على الجزء الخلفي من كتالوج مصدر القوانين ويتم إدخالها في أمر التوريد عندما قام عميل بشراء. لإضافة رمز مصدر إلى النشرة المصورة، يجب أولاً إنشاء سوق هدف. يتم تعيين المنطقة المستهدفة عادة إلى قائمة مراسلات المملوكة أو المستأجرة.
-   **المنتجات المجانية** عبارة عن أصناف ترويجية يتم تضمينها بدون مقابل في أمر العميل عند الرجوع إلى الكتالوج.
-   **البرامج النصية** يمكن استخدامها لتوجيه تفاعلات العامل مع العملاء في سياق كتالوج أو منتج في كتالوج.

## <a name="publish-the-catalog"></a>نشر الكتالوج
إذا قمت بنشر الكتالوج لمركز الاتصالات، فإنك ستقوم بذلك بإنهاء معلومات المنتج في الكتالوج. المنشور أيضا يشير إلى أن الكتالوج جاهز لأي إجراءات إضافية تريد تنفيذها. على سبيل المثال، يمكنك إنشاء كتالوج مطبوع. يمكنك نشر كتالوجاتك يدوياً، أو يمكنك استخدام معالجة دُفعة للنشر استنادا إلى أحد الجداول. قبل نشر كتالوج، يجب التحقق من صحة الكتالوج والموافقة عليه. لتغيير الكتالوج بعد أن تم نشره، يمكنك سحب الكتالوج، ثم يمكنك إعادة نشره.

