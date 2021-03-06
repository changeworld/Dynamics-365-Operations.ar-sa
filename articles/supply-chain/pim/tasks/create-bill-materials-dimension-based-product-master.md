--- 
title: "إنشاء قائمة مكونات الصنف لأصل منتج يستند إلى البعد"
description: "لتنفيذ هذا الإجراء، ينبغي عليك إكمال الأدلة 4 السابقة في هذا التسلسل من التسجيلات الثمانية."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4f9f9473d0872d68571b87409b93e0cf5455364c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>إنشاء قائمة مكونات الصنف لأصل منتج يستند إلى البعد

[!include [task guide banner](../../includes/task-guide-banner.md)]

لتنفيذ هذا الإجراء، ينبغي عليك إكمال الأدلة 4 السابقة في هذا التسلسل من التسجيلات الثمانية. تعمل التسجيلات الأربعة الأولى على إعداد البيانات المطلوبة لإكمال هذا الإجراء. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. عادة ما تتم معالجة هذه المهمة بواسطة مصمم المنتج.


## <a name="select-the-product"></a>تحديد المنتج
1. انقر فوق "صيانة المنتج الذي تم إصداره".
2. انقر فوق "المنتجات التي تم إصدارها".
3. في القائمة، قم بوضع علامة للصف المحدد.
    * ابحث عن أصل المنتج الذي تم إصداره باستخدام تقنية التكوين المستندة إلى البعد الذي قمت بإنشائه في دليل المهمة الأولى في هذا التسلسل.  
4. في جزء الإجراءات، انقر فوق "المهندس".
5. انقر فوق "إصدارات قائمة مكونات الصنف".

## <a name="create-new-bom-and-bom-version"></a>قم بإنشاء قائمة مكونات صنف جديدة وإصدار قائمة مكونات الصنف.
1. انقر فوق "جديد".
2. انقر فوق قائمة مكونات الصنف وإصدار قائمة مكونات الصنف.
3. في حقل "الاسم"، اكتب قيمة.
    * إعداد موقع  
    * في هذا الإجراء، لا نحدد موقع معين لقائمة مكونات الصنف.  
4. انقر فوق "موافق".
5. انقر فوق "جديد".
    * في هذا الإجراء، سنقوم بإضافة أربعة بنود إلى قائمة مكونات الصنف. يمثل بندين خيارات الكبل ويمثل بندين خيارات الكابينة.  
6. في القائمة، قم بوضع علامة للصف المحدد.
7. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
    * حدد رقم الصنف A0001، كبلات HDMI 6.  
8. في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.
    * حدد مجموعة تكوين الكبل التي تم إنشاؤها في دليل 4 في هذا التسلسل.  
9. انقر فوق "جديد".
    * حدد رقم الصنف A0002، كبلات HDMI 12.  
10. في القائمة، قم بوضع علامة للصف المحدد.
11. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
12. في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.
    * قم بتحديد مجموعة تكوين الكبل مرة أخرى.  
13. انقر فوق "جديد".
14. في القائمة، قم بوضع علامة للصف المحدد.
15. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
    * حدد رقم الصنف، كابينة D0002.  
16. في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.
    * قم بتحديد مجموعة التكوين الخاصة ببند قائمة مكونات الصنف.  
17. انقر فوق "جديد".
18. في القائمة، قم بوضع علامة للصف المحدد.
19. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
    * حدد رقم الصنف M0007 StandardCabinet كآخر بند في قائمة مكونات الصنف.  
20. في الحقل "مجموعة التكوين"، أدخل قيمة أو حددها.
    * قم بتحديد مجموعة التكوين الخاصة بالكابينة لبند قائمة مكونات الصنف الأخير.  

## <a name="approve-and-activate"></a>الموافقة والتنشيط
1. قم بإغلاق الصفحة.
2. انقر فوق "‏‫موافقة".
3. في الحقل "تم اعتماده بوساطة"، أدخل قيمة أو حددها.
4. حدد "نعم" في "هل تريد أيضًا الموافقة على قائمة مكونات الصنف؟ الحقل.
5. انقر فوق "موافق".
6. انقر فوق تنشيط.


