---
title: "العملية الصادرة"
description: "يوفر هذا الموضوع نظرة عامة حول العملية الصادرة في إدارة المخزون."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: f2cae64263769b5168d2bb9614d6388b42e23b49
ms.contentlocale: ar-sa
ms.lasthandoff: 12/14/2017

---

# <a name="outbound-process"></a>العملية الصادرة

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع نظرة عامة حول العملية الصادرة في إدارة المخزون.

## <a name="output-orders"></a>أوامر المخرجات

يتم استخدام أوامر المخرجات لربط بنود أوامر المبيعات وبنود أوامر التحويل مع عمليات الانتقاء الصادرة التي تستخدم قوائم الانتقاء.

عندما يتم إنشاء قوائم الانتقاء إما من أوامر المبيعات أو من أوامر التحويل، يتم تلقائيًا إنشاء أوامر المخرجات والشحنات. هناك علاقة واحد بواحد بين قائمة الانتقاء والشحنة. يمكن معالجة شحنة أمر التحويل أو قائمة انتقاء أمر المبيعات من الشحنة. 

يعرض المخطط‬ التالي نظرة عامة على عملية الأوامر الصادرة. 

[![نظرة عامة على عملية الأوامر الصادرة](./media/outbound-order.png)](./media/outbound-order.png)

يمكنك إعداد قواعد الأوامر الصادرة لتحديد الطريقة التي تريد من خلالها أن يتعامل البرنامج مع عملية الأوامر الصادرة. يمكنك استخدام هذه القواعد للتحكم في عملية الشحن. وبشكل خاص، يمكنك استخدام القواعد لتحديد المرحلة في العملية التي يمكن خلالها إرسال الشحنة. تحدد الإعدادات التالية كيفية التعامل مع العمليات الصادرة.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>استخدام حالة مسار الانتقاء لأوامر المبيعات وأوامر التحويل 

انتقل إلى **الحسابات المدينة** \> **الإعداد** \> **محددات الحسابات المدينة‬‏‫**، ثم على علامة تبويب **التحديثات**، حدد قيمة في حقل **حالة مسار الانتقاء**.

[![حقل حالة مسار الانتقاء لأوامر المبيعات](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

إذا تم تعيين حقل **حالة مسار الانتقاء** الحقل إلى **مكتمل**، فإن عملية الانتقاء تحدث تلقائيًا كجزء من عملية إنشاء قوائم الانتقاء. إذا تم تعيين الحقل إلى **نشط**، فيجب تحديث بنود قائمة الانتقاء يدويًا.

ينطبق الإعداد نفسه على أوامر التحويل. انتقل إلى **إدارة المخزون** \> **الإعداد** \> **محددات إدارة المستودعات والمخزون‬**، ثم على علامة التبويب **نقل**، حدد قيمة في حقل **حالة مسار الانتقاء**.

[![حقل حالة مسار الانتقاء لأوامر التحويل](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>إنهاء أوامر مخزنية للمخرجات

انتقل إلى **إدارة المخزون** \> **الإعداد** \> **محددات إدارة المستودعات والمخزون‬**، ثم على علامة التبويب **عام**، عيّن الخيار **إنهاء أمر مخزني للمخرجات**.

[![الخيار إنهاء أمر مخزني للمخرجات](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

عندما يقلل عامل المستودع كميات قائمة الانتقاء، ستتم إزالة كميات أوامر المخزون المقابلة من الشحنة. عندما يتم تحديث قائمة الانتقاء عند نقطة زمنية ما، يتم تحديث الكميات المتبقية مرة أخرى في الأمر إذا كان الخيار **‏‫إنهاء أمر مخزني للمخرجات‬** مُعينًا إلى **نعم**. إذا كان الخيار **‏‫إنهاء أمر مخزني للمخرجات‬** معينًا إلى **لا**، يتم الاحتفاظ بالكميات المتبقية ككمية أمر مخرجات مفتوح ويجب إضافتها إلى قائمة انتقاء جديدة كجزء من الوظيفة **فتح أوامر المخرجات**. 

[![الأمر "فتح أوامر المخرجات" في قائمة "الوظائف"](./media/open-output-order.png)](./media/open-output-order.png)

[![قائمة "الوظائف" في صفحة "فتح أوامر المخرجات"](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>خفض الكمية

المعلمة الثالثة التي يمكنك استخدامها كجزء من عملية إنشاء قوائم الانتقاء هي المعلمة **خفض الكمية‬**. يعمل إعداد هذه المعلمة مع إعداد **الحجز** الذي يقوم بتشغيل عملية حجز كجزء من الإصدار إلى المستودع.

[![معلمة خفض الكمية](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>مثال عملية صادرة‬ لأمر مبيعات

بالنسبة إلى هذا المثال، هناك أمر مبيعات لصنفين. أثناء إنشاء قائمة الانتقاء، حدد معلمة **خفض الكمية**. لذلك، يمكنك إصدار وإنشاء بنود الانتقاء فقط للمخزون الفعلي المتاح. يجب الإعلام عن الانتقاء من خلال عملية تسجيل لقوائم الانتقاء (**حالة مسار الانتقاء** = **نشط**).

يتم حجز المخزون الذي لم يتم حجزه بالفعل أثناء إنشاء قائمة الانتقاء. يمكن إزالة المخزون غير المتوفر من أمر المبيعات أو يمكن إصداره إلى المستودع لمعالجة الصادر لاحقًا، عندما يكون المخزون متوفرًا للانتقاء.

[![تحديث قائمة الانتقاء](./media/update-picking-list.png)](./media/update-picking-list.png)

بمجرد انتقاء كافة بنود الانتقاء في صفحة **تسجيل قائمة الانتقاء**، يتم إكمال الشحنة المرتبطة. يمكن تهيئة عملية إيصالات التعبئة لأوامر المبيعات استنادًا إلى المخزون المنتقى.

[![تحديث الشحنات الصادرة](./media/outbound-shipments.png)](./media/outbound-shipments.png)

