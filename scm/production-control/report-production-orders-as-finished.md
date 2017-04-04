---
title: "الإبلاغ عن انتهاء أوامر الإنتاج"
description: "تم الإبلاغ عنها منتهية مرحلة إنتاج. في هذه المرحلة، هو الإبلاغ عن منتج النهائي ونقله من أمر الإنتاج إلى المخزون."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19a777a8e58e3c8b848e878956b457a4a730f6e2
ms.lasthandoff: 03/31/2017


---

# <a name="report-production-orders-as-finished"></a>الإبلاغ عن انتهاء أوامر الإنتاج

تم الإبلاغ عنها منتهية مرحلة إنتاج. في هذه المرحلة، هو الإبلاغ عن منتج النهائي ونقله من أمر الإنتاج إلى المخزون.

عند الإبلاغ عن كمية السلع المنتهية كمنتهية في أمر الإنتاج، فإنه يتم تحديثه كمتوفر في المخزون. ويمكن الإبلاغ عن الكميات الجزئية لكمية الأمر المخطط لها في الأصل كمنتهية. ومن الممكن أيضًا الإبلاغ عن كميات الأخطاء مع سبب خطأ مقترن عند الإبلاغ عن الكميات كمنتهية. وعند وصول أمر الإنتاج إلى مرحلة الإبلاغ عنه كمنتهٍ، فإنه يشير إلى أنه لم تعد هناك أي كمية أخرى يتعين الإبلاغ عنها في أمر الإنتاج.
كما أن الخصائص التالية مقترنة بعملية **الإبلاغ عنه كمنتهٍ**:
-   من الممكن إعداد استهلاك الوقت والمواد الخام المتناسبة مع الكمية التي تم الإبلاغ عنها (المسح الخلفي)
-   يمكن إنشاء عمل الإبعاد للأصناف التي تم تمكينها لعمليات المستودع.
-   يمكن إعداد قيمة التكلفة المخططة أو القياسية للسلع المنتهية للإبلاغ عنها لحسابات دفتر الأستاذ.
-   يمكن إنشاء أمر جودة للكمية التي تم الإبلاغ عنها استناداً إلى إعداد اقتران الجودة.

تم الإبلاغ عن الكمية لموقع الإخراج. ويتم فيما بعد إنشاء عمل المستودع لنقل الكمية من موقع الإخراج إلى وجهته النهائية بواسطة توجيه الموقع لعمل الإبعاد.

-   يمكن إنشاء أمر جودة عند الإبلاغ عن أمر إنتاج كمنتهٍ، إذا تم إعداد اقتران جودة.

## <a name="set-a-production-order-to-reporting-as-finished"></a>تعيين أمر إنتاج للإبلاغ عنه كمنتهٍ
يمكن تعيين أمر إنتاج إلى **الإبلاغ عنه كمنتهٍ** من خلال وظيفة تحديث أمر الإنتاج القياسي، أو من خلال دفاتر يومية بطاقة الوظيفة والمسار، أو من خلال دفتر يومية **الإبلاغ عنه كمنتهٍ**. كما يمكنك تحديث المرحلة إلى **الإبلاغ عنه كمنتهٍ** من خلال محطة بطاقة الوظيفة وصفحات جهاز بطاقة الوظيفة، عند الإبلاغ عن الوظيفة الأخيرة لأمر الإنتاج. وأخيراً، يمكنك تمكين خيار **الإبلاغ عنه كمنتهٍ** كعملية لحل جهاز المستودع المحمول يدويًا.  

