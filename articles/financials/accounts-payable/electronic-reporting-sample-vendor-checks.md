---
title: "عينة شيكات المورد الخاصة بإعداد التقارير الإلكترونية"
description: "يوفر هذا الموضوع معلومات عامة حول كيفية استخدام عينات تنسيقات الشيكات الخاصة بإعداد التقارير الإلكترونية."
author: ShylaThompson
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6702ac241c41cc99d96bc46a515837235b3ae651
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---

[!include [banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a>عينات تنسيقات الشيكات الخاصة بإعداد التقارير الإلكترونية

يمكنك استخدام التقارير الإلكترونية (ER) لتنسيق شيكات المورد. تتوافر ‏‫العديد من تنسيقات الشيكات الخاصة بالبنوك والخاصة بموفري الخدمات في السوق> تم تضمين أمثلة لتنسيقات شيكات في نموذج شيك الدفع في مستودع أداة إعداد التقارير الإلكترونية. تسمى عينات الشيكات هذه بـ **الشيك في الوسط (الولايات المتحدة)** و **الشيك في أعلى والكعب أسفل (الولايات المتحدة)**.

## <a name="what-check-formats-are-currently-supported"></a>ما هي تنسيقات الشيكات المدعومة حاليًا؟

يجب عليك دائمًا الانتقال إلى مكتبة الأصول المشتركة في Microsoft Dynamics Lifecycle Services (LCS) وعرض قائمة بأحدث الملفات المتوفرة التي تحتوي على نوع أصل **تكوين GER**. يتضمن القسم التالي، "ما الذي يجب عليّ إعداده؟، ارتباطًا إلى الموضوع الذي يشرح كيفية إنشاء مستودع LCS، بحيث تتمكن من مراجعة التكوينات المتوفرة واستيراد تكوينات محددة.

يتضمن Microsoft Dynamics 365 for Finance and Operations عينة تنسيق يوجد فيه الشيك في الأعلى، ويليه قسمين للحوالات. ويتضمن أيضًا عينة تنسيق يكون فيها الشيك في الوسط بين قسمي الحوالة. تتوافق عينات التنسيقات هذه مع تنسيقات شيكات أعمال Deluxe.

## <a name="what-do-i-have-to-set-up"></a>ما الذي يجب عليَّ إعداده؟

- قبل أن تتمكن من طباعة الشيكات باستخدام التقارير الإلكترونية، فمن ثم يجب استيراد تكوين شيك نشط واحد على الأقل إلى تكوينات التقارير الإلكترونية الخاص بك. للمزيد من التعليمات، راجع [تنزيل تكوينات التقارير الإلكترونية من Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
- عندما تقوم بتكوين الشيكات النقدية وشيكات الإدارة البنكية للحساب البنكي، حدد خانة اختيار **تنسيق تصدير إلكتروني عام**، ثم حدد تنسيق الشيك المناسب كتكوين تنسيق ملف تصدير.
- يجب عليك أيضا تحديد عدد أسطر الإيصال التي سوف تتم طباعتها على الحوالة. تأكد من تضمين صفوف الرؤوس عند حساب هذا الرقم. بالنسبة لعينتي تنسيق الشيك، يبلغ عدد أسطر الإيصال الموصي بها هي 17 سطرًا. ولكن، سوف يختلف هذا الرقم، بناءً على مخزون الشيكات لديك، وبرامج تشغيل الطابعة الخاصة بك.
- نوصي بطباعة شيك كاختبار للتحقق من صحة تخطيط الشيك. لطباعة شيك اختبار، حدد خيار **اختبار طباعة**. تعمل عينات تنسيقات الشيكات بشكل أفضل عندما يتم تعيين الـ **هوامش** إلى **بلا** في خصائص الطابعة المتقدمة لـ Microsoft Excel. بعد إنشاء شيك اختبار، يتم تمكين التحرير مخرجات Excel، وتكوين تخطيط الصفحة بحيث يتم تعيين جميع الهوامش إلى **0** (صفر). قم بمقارنة نسخة اختبار الشيك بمخزون الشيكات لديك، ثم قم بضبط الإعدادات حتي تكون راضيًا عن المحاذاة.
- عندما تقوم بإنشاء المدفوعات الخاصة بالحساب البنكي الذي تم تكوينه في دفتر يومية المدفوعات، فسوف تتم طباعة الشيكات باستخدام التنسيق المحدد.

للمزيد من المعلومات، راجع [تعديل تنسيق تقارير إلكترونية](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).

