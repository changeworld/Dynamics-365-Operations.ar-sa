---
title: "تجميع النظام في قائمة عمل مفتوح‬"
description: "يصف هذا الموضوع كيفية تصفية قائمة العمل المفتوح‬ على جهاز محمول."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: dbf0e49b1156c54cd37bbbe57ca564cdbc45fb2d
ms.contentlocale: ar-sa
ms.lasthandoff: 06/20/2017


---

# <a name="system-grouping-on-an-open-work-list"></a>تجميع النظام في قائمة عمل مفتوح‬

[!include[banner](../includes/banner.md)]

باستخدام حقل تجميع النظام، يمكنك تصفية قائمة عمل مفتوح دون الحاجة إلى تحرير عنصر قائمة الجهاز المحمول.
حيث ينطبق الأمر، يعمل تجميع نظام لتصفية قائمة عمل على حقل رأس عمل واحد. لا يمكنك استخدام تجميع النظام للتصفية على حقول على مستوى البنود.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>إعداد تجميع النظام في قائمة عمل مفتوح
استخدم هذه الخطوات لإعداد تجميع النظام في قائمة عمل مفتوح.

-   من عنصر قائمة جهاز محمول، حدد **وضع: غير مباشر** و**كود النشاط‬: عرض قائمة العمل المفتوح**. يتوفر الخياران التاليان: هذان الخياران مطلوبان لتجميع النظام في قائمة عمل مفتوح. 

| الخيار        | ‏‏الوصف   | 
| ------------- | ------------- |
| السماح بتجميع النظام   | لتمكين تجميع النظام لعنصر قائمة عمل محدد.| 
| حقل تجميع النظام   | يتوفر فقط عند تعيين **السماح بعمل النظام** إلى **نعم**. حدد الحقل الذي يحدد كيفية تجميع عمل الانتقاء للعاملين. على سبيل المثال، إذا قمت بتحديد حقل **‏‫معرف الشحنة‬**، سيقوم العامل بفحص معرف الشحنة لتجميع عمل الانتقاء. ثم يتم تعيين جميع الأعمال للشحنة للعامل. ويتطلب هذا الحقل إنشاء صنف قائمة لاستخدام العمل الموجود الذي يتم تجميعه بواسطة النظام. استخدم الحقل **تسمية تجميع النظام** لإعلام العامل بما يجب عليه فحصه. |
| بطاقة تجميع النظام   | يتوفر فقط عند تعيين **السماح بعمل النظام** إلى **نعم**. أدخل معلومات للعامل عما يجب عليه فحصه عندما يتم تجميع عمل الانتقاء. على سبيل المثال، إذا كنت تستخدم حقل **معرف الشحنة** لتجميع عمل الانتقاء بالشحنة، يمكنك إدخال معرف الشحنة في الحقل. ويتطلب هذا الحقل إنشاء صنف قائمة لاستخدام العمل الموجود الذي يتم تجميعه بواسطة النظام. يجب أيضًا تحديد الحقل للتجميع بحسب في حقل **تجميع النظام**.|
