---
title: "منع الخصومات لمنتجات البيع بالتجزئة"
description: "هناك أسباب مختلفة تكمن خلف رغبة تجار التجزئة في منع تطبيق الخصومات على بعض المنتجات، سواء من عرض ترويجي أو أثناء عملية البيع في نقطة البيع."
author: jeffbl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c124ecf104bdb3de786c9dd98c2b07a4c9c04041
ms.openlocfilehash: 0debfe984a83295dde145fe4b8c2deb836345cd6
ms.contentlocale: ar-sa
ms.lasthandoff: 07/31/2017

---

# <a name="prevent-discounts-for-retail-products"></a>منع الخصومات لمنتجات البيع بالتجزئة

[!include[banner](includes/banner.md)]

هناك أسباب مختلفة تكمن خلف رغبة تجار التجزئة في منع تطبيق الخصومات على بعض المنتجات، سواء من عرض ترويجي أو أثناء عملية البيع في نقطة البيع.

سوف تسمح الخيارات التالية الموجودة على علامة تبويب **Retail** للمنتجات الصادرة بتكوين المنتج لمنع جميع الخصومات أو الخصومات اليدوية. يمكن أيضًا تحديد الإعدادات على مستوى الفئة من التدرج الهرمي لفئات البيع بالتجزئة.

**منع كافة الخصومات**: حدد هذا الخيار لمنع تطبيق كافة أنواع الخصومات على هذا المنتج. وهذا يشمل العروض الترويجية مثل خصومات أصناف الخلط والمطابقة والكمية وخصومات الحد، بالإضافة إلى خصومات البنود والحركات اليدوية التي يتم تطبيقها أثناء عملية البيع من قبل مستخدم نقطة البيع.

**منع الخصومات اليدوية**: حدد هذا الخيار لمنع فقط خصومات البنود أو الحركات أو اليدوية التي يتم تطبيقها أثناء عملية بيع من قبل مستخدم نقطة البيع. تبقى المنتجات التي تم تحديد هذا الخيار لها مؤهلة للعروض الترويجية، مثل خصومات أصناف الخلط والمطابقة والكمية وخصومات الحد.

**ملاحظة**: لا تقيد هذه الإعدادات عملية تجاوز السعر، حيث تقوم بتعيين السعر الأساسي ولا تتم معاملتها على أنها خصم.  

![حقل منع الخصومات](/media/prevent-discounts.png)
