---
title: "التسلسلات الهرمية للبيع بالتجزئة"
description: "توضح هذه المقالة التدرجات الهرمية للبيع بالتجزئة في Microsoft Dynamics AX."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 4dc4fdfa8abf65ba13f5c94042a8eb28a3d7c046
ms.contentlocale: ar-sa
ms.lasthandoff: 04/26/2017


---

# <a name="retail-hierarchies"></a>التسلسلات الهرمية للبيع بالتجزئة

[!include[banner](includes/banner.md)]


توضح هذه المقالة التدرجات الهرمية للبيع بالتجزئة في Microsoft Dynamics AX.

يمكنك إنشاء تدرج هرمي لفئات البيع بالتجزئة لتنظيم المنتجات التي تبيعها عبر قنوات البيع بالتجزئة لديك. ويمكنك استخدام التدرجات الهرمية لمنتجات البيع بالتجزئة لتصنيف أو تجميع المنتجات. ويمكنك بعد ذلك استخدام هذه المنتجات لإنشاء عمليات فرز المنتجات وبرامج ولاء العملاء. كما يمكنك تعيين خصائص وسمات المنتجات، وتعيين هيكل تسعير، وتضمين المنتجات في عروض المنتجات، واستخدام المنتجات للإبلاغ. يمكنك إنشاء تدرج هرمي واحد لفئات البيع بالتجزئة لتمثيل كافة المنتجات والفئات في مؤسستك، ثم استخدام ذلك التدرج الهرمي للفئات لأغراض متعددة. وبدلاً من ذلك، يمكنك إنشاء تدرجات هرمية متعددة لفئات البيع بالتجزئة لأغراضٍ خاصة، مثل عروض المنتجات. عند إنشاء تدرج هرمي لمنتجات بيع بالتجزئة، يجب تعيين نوع تدرج هرمي للفئات لتحديد غرض التدرج الهرمي للفئات. على سبيل المثال، يتم الرجوع إلى التدرجات الهرمية للمنتجات فقط التي تم تعيين نوع **التدرج الهرمي للتنقل للبيع بالتجزئة** لها، عند استعراض المنتجات حسب الفئة عبر الإنترنت أو في نقطة البيع (POS).

## <a name="retail-hierarchy-types"></a>أنواع التدرج الهرمي للبيع بالتجزئة
يسرد الجدول التالي أنواع التدرجات الهرمية لفئات اليع بالتجزئة المتوفرة والغرض العام لكل نوع.

| نوع التدرج الهرمي للفئات       | الغرض                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| التسلسل الهرمي لمنتج البيع بالتجزئة      | استخدم نوع التدرج الهرمي هذا لتحديد التدرج الهرمي الشامل للمنتجات لمؤسستك. ويمكنك استخدام هذا النوع من التدرج الهرمي للترويج للسلع والتسعير والعروض، والتقارير، وتخطيط الفرز. ويمكن تعيين نوع التدرج الهرمي هذا لتدرج هرمي واحد لمنتجات البيع بالتجزئة.                                       |
| التدرج الهرمي التكميلي للبيع بالتجزئة | استخدم نوع التدرج الهرمي هذا لأي تدرجات هرمية للفئات الإضافية للبيع بالتجزئة التي تريد إنشائها. على سبيل المثال، في فصل الربيع، يكون لديك ترويج لملابس السباحة. ولذلك، تقوم بتضمين المنتجات ملابس السباحة في تدرج هرمي منفصل للفئات وتطبيق الأسعار الترويجية على مختلف فئات المنتجات. |
| التدرج الهرمي للتنقل في البيع بالتجزئة   | استخدم هذا النوع من التدرج الهرمي لتجميع وتنظيم المنتجات في فئات بحيث يمكنك استعراض المنتجات على الإنترنت أو في نقطة البيع.                                                                                                                                                                                       |

باستخدام تدرج هرمي لفئات البيع بالتجزئة لتنظيم منتجاتك، يمكن إعداد وصيانة سمات وخصائص المنتجات على مستوى الفئة. وتتضمن هذه السمات والخصائص إعدادات أبعاد المنتج وإعدادات نقطة البيع. وترث منتجات تقوم بتعيينها إلى الفئات تلقائياً السمات والخصائص التي تحددها. كما يمكنك نسخ إعدادات الخصائص لأي منتج لعدة منتجات في فئة محددة في نفس الوقت.



