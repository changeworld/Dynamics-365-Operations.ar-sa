---
title: "اتفاقيات على مستوى الخدمة"
description: "في اتفاقية مستوى الخدمة، يوافق العميل على أدنى وقت للاستجابة استنادًا إلى الوقت الذي تقوم فيه شركة الخدمة بتسجيل المشكلة ومتى تم حل المشكلة."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a>اتفاقيات على مستوى الخدمة        

[!include [banner](../includes/banner.md)]


اتفاقية مستوى الخدمة (SLA) هي عبارة عن اتفاقية بين شركة خدمة وعميل خدمة. في اتفاقية مستوى الخدمة، يوافق العميل على أدنى وقت للاستجابة استنادًا إلى الوقت الذي تقوم فيه شركة الخدمة بتسجيل المشكلة ومتى تم حل المشكلة.

تطبق اتفاقية مستوى الخدمة أسلوبًا قياسيًا للخدمةالمقدمة للعملاء، كما توضح لشركة الخدمة متى ينبغي إكمال إحدى مهام الخدمات.

ويمكن إنشاء أي عدد من اتفاقيات مستوى الخدمة وذلك لتوفير مستويات مختلفة من الخدمة لعميل الخدمة.

## <a name="create-a-service-level-agreement"></a>إنشاء اتفاقية مستوى الخدمة

1.  انقر فوق **إدارة الخدمة** \> **الإعداد** \> **اتفاقيات الخدمة** \> **اتفاقيات مستوى الخدمة**.

2.  اكتب اسم اتفاقية مستوى الخدمة في الحقل **اتفاقية مستوى الخدمة**.

3.  اكتب الوقت الذي تريد فيه السماح بإكمال استدعاءات الخدمة المرفقة باتفاقية مستوى الخدمة. ثم حدد تقويماً إذا كنت ترغب في أن تستند اتفاقية مستوى الخدمة إلى تقويم معين.

## <a name="apply-a-service-level-agreement"></a>تطبيق اتفاقية مستوى الخدمة

يتم تطبيق اتفاقية مستوى الخدمة مباشرة على اتفاقية خدمة.

يتم قياس أوامر الخدمة التي يتم إنشاؤها يدويًا وإرفاقها باتفاقية خدمة تتضمن اتفاقية مستوى خدمة مقابل اتفاقية مستوى الخدمة تلك.

لا يتم إرفاق أوامر الخدمة التي يتم إنشاؤها تلقائيًا باتفاقية مستوى خدمة.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>تطبيق اتفاقية مستوى الخدمة على اتفاقية الخدمة

1.  انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**. حدد اتفاقية الخدمة التي ترغب في تطبيق اتفاقية مستوى الخدمة عليها، ثم انقر فوق **تحرير** في **جزء الإجراءات**.

2.  في حقل **اتفاقية مستوى الخدمة**، حدد اتفاقية مستوى الخدمة التي تريد تعيينها.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>تطبيق اتفاقية مستوى الخدمة على ‏‏مجموعة اتفاقيات الخدمات

1.  انقر فوق **إدارة الخدمة** \> **الإعداد** \> **اتفاقيات الخدمة** \> **مجموعات اتفاقيات الخدمة**.

2.  في حقل **اتفاقية مستوى الخدمة**، حدد اتفاقية مستوى الخدمة التي تريد تعيينها.

## <a name="track-time-on-a-service-order-against-an-sla"></a>تتبع الوقت في أمر خدمة مقابل اتفاقية مستوى خدمة

عند إنشاء أمر خدمة جديد لاتفاقية خدمة تم تعيين اتفاقية مستوى خدمة إليها، يتم بدء الفترة الزمنية لتسليم الخدمة، ويبدأ النظام في تعقب وقت التسليم. فضلاً عن ذلك، يمكن تعيين الخيارات التالية:

  - يمكن تشغيل تسجيل الوقت وإيقافه في أمر الخدمة وذلك لتسجيل إجمالي الوقت المستغرق في أوامر الخدمة.

  - يمكن مراقبة الالتزام بالفاصل الزمني الذي تم تعيينه في اتفاقية مستوى الخدمة.

  - يمكن تحديد أكواد السبب التي يلزم تعيينها في حالة تجاوز الفاصل الزمني المحدد باتفاقية مستوى الخدمة.

## <a name="see-also"></a>راجع أيضًا

[عرض التوافق مع اتفاقيات مستوى الخدمة](view-compliance-with-service-level-agreements.md)

  



