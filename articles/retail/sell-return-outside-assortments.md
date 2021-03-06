---
title: "بيع وإرجاع منتجات لا تشكل جزءًا من فرز المتجر"
description: "باستخدام Dynamics 365 for Retail، يمكنك بيع المنتجات وإرجاعها خارج عمليات الفرز."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 17981cef401085ad3af784950fff6260c2c6d9ee
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>بيع وإرجاع منتجات لا تشكل جزءًا من فرز المتجر

[!include [banner](includes/banner.md)]

هناك سيناريو شائع لأي بائع التجزئة وهو بيع المنتجات إلى العملاء أو قبول المرتجعات من العملاء حتى لو لم تكن بعض المنتجات المحددة موجودة في المتجر (بمعنى آخر، لا يتم فرز المنتجات في المتجر).
وفيما يلي بعض السيناريوهات النموذجية:

+ كافة المنتجات لدى بائع التجزئة غير متوفرة في متجر معين. يتم تخزين المنتجات المتبقية في المستودع. باستطاعة موظف المتجر مساعدة العميل عن طريق البحث عن منتجات معينة في المتجر أو استعراضها، وإضافتها إلى عربة التسوق، وإكمال عملية السداد والخروج عن طريق تحديد أسلوب تسليم، مثل الشحن إلى عنوان ما من المستودع أو السماح للعميل باستلام المنتج من المتجر الحالي أو متجر آخر.
+ لا توجد لدى بائع التجزئة منتجات محددة في المتجر أو هي غير متوفرة في المخزون في المتجر الذي زاره العميل، ولكن هذه المنتجات متوفرة في متاجر أخرى. باستطاعة موظف المتجر مساعدة العميل عن طريق البحث عن منتجات معينة في المتجر أو استعراضها، وإضافتها إلى عربة التسوق، وإكمال عملية السداد والخروج عن طريق تحديد أسلوب تسليم.
+ لدى بائع التجزئة الكثير من المتاجر في منطقة محددة أو رمز بريدي محدد أو حولهما، وهو لا يريد إجبار العملاء على إعادة المنتجات إلى المتجر نفسه حيث تمت عملية الشراء. بدلاً من ذلك، باستطاعة العملاء إرجاع المنتجات إلى أي متجر.


تتوفر هذه السيناريوهات الشائعة لبائعي التجزئة الذين يستخدمون Dynamics 365 for Retail. باستخدام Retail، يمكنك:
+ البحث عن منتجات في متاجر أخرى أو استعراضها.
+ البحث عن جميع المنتجات الصادرة أو استعراضها.
+ إنشاء حركات تعتمد على الدفع نقدًا والنقل أو أوامر العملاء.
+ تحديد خيارات التسليم الخاصة بأوامر العملاء.
+ استلام المنتجات في المتجر الحالي أو متجر آخر.
+ إلغاء أمر في المتجر الحالي أو متجر آخر.
+ إرجاع أمر مع أو بدون إيصال الاستلام في المتجر الحالي أو متجر آخر.

