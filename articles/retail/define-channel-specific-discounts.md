---
title: "تحديد الخصومات الخاصة بالقناة"
description: "يعيّن تجار البيع بالتجزئة في أغلب الأحيان خصومات مختلفة في قنوات مختلفة. يستعرض هذا الموضوع المفاهيم التي تحتاج إلى معرفتها لإنشاء خصم لقناة محددة."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0300ed4a10f6979fb673447323f7fdf61041529f
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="define-channel-specific-discounts"></a>تحديد الخصومات الخاصة بالقناة

[!include [banner](includes/banner.md)]

يعيّن تجار البيع بالتجزئة في أغلب الأحيان خصومات مختلفة في قنوات مختلفة. يستعرض هذا الموضوع المفاهيم التي تحتاج إلى معرفتها لإنشاء خصم لقناة محددة. 

<a name="channel-specific-discounts"></a>الخصومات الخاصة بالقناة
--------------------------

‏‫يقدم تجار التجزئة غالباً خصومات مختلفة في قنوات مختلفة. وقد يتم إجراء هذا في ظروف السوق المحلية أو للتعامل مع تجار التجزئة المنافسين.‬

يستخدم Microsoft Dynamics 365 for Retail مجموعات الأسعار لتحديد الخصومات الخاصة بالقناة. ويمكن تعيين مجموعات الأسعار لواحدة أو أكثر من الوحدات التالية: القنوات والكتالوجات والتبعيات وبرامج الولاء. وتتناول هذه المقالة القنوات، لكن نفس المفاهيم تنطبق على خصومات الكتالوج وخصومات التبعيات وخصومات الولاء.

## <a name="price-groups"></a>مجموعات الأسعار

[![مجموعات الأسعار](./media/price-groups-1024x608.png)](./media/price-groups.png)

‏‫يوضح الرسم البياني أعلاه العلاقة بين الكيانات التي قد تكون موجودة في حركة (القناة، الكتالوج، التبعيات، العميل، بطاقة الولاء) ومختلف أنواع الخصم التي يمكن تكوينها. وتتم كافة الحركات في قناة، حيث يتم ضمان القناة لتقديمها في حركة.‬ الكيانات المتبقية اختيارية. وفي كل صفحة من صفحات البيانات الرئيسية، هناك رابط إلى صفحة مجموعات الأسعار ذات الصلة، حيث يمكنك عرض وإضافة مجموعات الأسعار عند اللزوم. يتم استخدام مجموعة أسعار لربط أربعة أنواع مختلفة من الكيانات بتسويات الأسعار والخصومات والاتفاقيات التجارية. ونُوصي بأن تخطط إستراتيجية للطريقة التي ستسمي بها مجموعات الأسعار الخاصة بك للحفاظ على تنظيمها.‬ هناك خيار واحد يتمثل في استخدام حرف أو بادئة رقم أو لاحقة رقم للتمييز بين الأنواع المختلفة. على سبيل المثال، 1-xxxxx لمجموعات أسعار القنوات و2-xxxxx لمجموعات أسعار الكتالوج.‬ وهناك أربع صفحات استعلام تركز على كل كيان من كيانات البيع بالتجزئة يمكن أن تكون الخصومات مقترنة بها.

-   **مجموعات أسعار قنوات البيع بالتجزئة** - تعرض هذه الصفحة قائمة بالقنوات والخصومات المرتبطة ببعضها البعض لكل مجموعة أسعار.
-   **مجموعات أسعار الكتالوج** - تعرض هذه الصفحة قائمة بالكتالوجات والخصومات المرتبطة ببعضها البعض لكل مجموعة أسعار.
-   **مجموعات أسعار الولاء** - تعرض هذه الصفحة قائمة ببرامج الولاء والخصومات المرتبطة ببعضها البعض لكل مجموعة أسعار.
-   **مجموعات أسعار التبعيات** - تعرض هذه الصفحة قائمة بالتبعيات والخصومات المرتبطة ببعضها البعض لكل مجموعة أسعار.

## <a name="example-channel-discount-set-up"></a>مثال على إعداد خصومات القناة
يوضح المثال التالي المهام المتضمنة في إعداد خصم قناة.

1.  على سبيل المثال، لديك قناة تسمى **هيوستن**، وستقوم بإنشاء خصم جديد يسمى **العودة إلى المدرسة.**
2.  لأن استراتيجية التسعير والخصم تتضمن إمكانية خصومات القنوات، يمكنك دائمًا إنشاء مجموعة أسعار خاصة بالقناة عند إنشاء قناة.
3.  لديك مجموعة أسعار **هيوستن-بي جي** وتم تعيينها إلى قناة **هيوستن**.
4.  بعد إنشاء خصم **العودة إلى المدرسة** الجديد، يجب عليك النقر فوق **مجموعات الأسعار** في الجزء العلوي من صفحة **الخصم**. سيتم فتح صفحة **مجموعات أسعار الخصومات**. وبعد ذلك، انقر فوق **جديد**، وحدد مجموعة الأسعار **هيوستن-بي جي**.
5.  يمكنك الآن تمكين الخصم ودفعه للقناة.



<a name="additional-resources"></a>الموارد الإضافية
--------

[تعديلات الأسعار والخصومات](price-adjustments-discounts.md)




