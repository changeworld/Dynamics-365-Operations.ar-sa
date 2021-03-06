---
title: "ميزات محتوى Power BI"
description: "يصف هذا الموضوع ميزات محتوى Power BI. يوضح هذا الموضوع كيفية الوصول إلى التقارير التي تم تضمينها في حزمة المحتوى، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء حزمة المحتوى."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBenefitWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 38610815e45926aa367011c8723494615e03ee38
ms.contentlocale: ar-sa
ms.lasthandoff: 08/13/2018

---

# <a name="benefits-power-bi-content"></a>ميزات محتوى Power BI

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع محتوى **ميزات** Microsoft Power BI. يوضح هذا الموضوع كيفية الوصول إلى التقارير التي تم تضمينها في حزمة المحتوى، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء حزمة المحتوى.

## <a name="accessing-the-power-bi-content"></a>الوصول إلى محتوى Power BI
يتم عرض محتوى **ميزات** Power BI في مساحة عمل **إدارة المزايا** إذا كنت تستخدم أحد المنتجات التالية:

- Microsoft Dynamics 365 for Finance and Operations
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>التقارير المضمنة في محتوى Power BI
تحتوي التقارير المضمنة في محتوى **ميزات** Power BI على كل من المخططات والجداول التي تحتوي على معلومات إضافية. يصف الجدول التالي التقارير.

| تقرير                      | المحتويات                                                                                       |
|-----------------------------|------------------------------------------------------------------------------------------------|
| نظرة عامة عن التسجيل في الميزات | معظم وأقل الخطط المسجل، والتسجيل حسب مجموعة الموظف، وخيارات خطط الميزات المُحددة |
| مزايا الموظف           | تسجيل الموظف بحسب الميزة المحددة                                                        |

يمكنك تصفية المخططات والتجانبات في هذه التقارير، وتثبيت المخططات والتجانبات بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات
تستخدم البيانات التالية لملء التقارير في محتوى **ميزات** Power BI. يوضح هذا الجدول الكيانات التي استند عليها المحتوى.

| الكيان                   | المحتويات                                                                                                   | العلاقات مع الكيانات الأخرى |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| مقاصة التقويم          | مقاصات التقويم إلى تقارير الشرائح                                                                          | مهمة المنصب السابق، اتجاه المنصب، اتجاه الموظف، موظفون تم إنهاء خدمتهم |
| الشركة                  | تقوم الشركات بتصفية التقارير حسب                                                                             | التعويض الحالي، الموظف الحالي، موظف تم إنهاء خدمته، اتجاه الموظف |
| التعويض             | معدل الدفع والتكرار على مدار الوقت                                                                           | التعويض الحالي، الموظف الحالي، موظف تم إنهاء خدمته، اتجاه الموظف |
| التعويض الحالي     | معدل الدفع والتكرار اعتبارًا من التاريخ الحالي                                                              | الشركة، التعويض، التوزيع الجغرافي، الوظيفة، المنصب |
| المنصب الحالي         | المناصب اعتبارًا من التاريخ الحالي، نظام مكافئ للدوام الكامل، والمناصب المفتوحة والمناصب المفتوحة لشغلها | الوظيفة، المنصب |
| الموظف الحالي         | العمال اعتبارًا من التاريخ الحالي والعمر، وعدد الأشخاص                                                         | الشركة، التعويض، الموقع الجغرافي، اسم الموظف، رفع التقارير إلى، المسمى الوظيفي للموظف، التوزيع الجغرافي، الوظيفة، التوظيف، المنصب، الميزات |
| التاريخ                     | الأيام والأسابيع والشهور والسنوات                                                                             | مهمة المنصب السابق، اتجاه المنصب، موظف تم إنهاء خدمته، اتجاه الموظف |
| التوزيع الجغرافي             | تاريخ الميلاد، والجنس والأصل العرقي والحالة الاجتماعية                                                   | الموظف الحالي، الموظف الذي تم إنهاء خدمته، اتجاه الموظف |
| التوظيف               | تاريخ البدء، وتاريخ الانتهاء، وتاريخ الانتقال                                                                  | الموظف الحالي، الموظف الذي تم إنهاء خدمته، اتجاه الموظف |
| الموقع الجغرافي      | المدينة، والمقاطعة، والرمز البريدي، والمنطقة أو المقاطعة                                                           | الموظف الحالي، الموظف الذي تم إنهاء خدمته، اتجاه الموظف |
| الوظيفة                      | الوظيفة، النوع والعنوان                                                                                  | المنصب الحالي، الموظف الحالي |
| مهمة المنصب السابق | سبب التعيين، وتاريخ البدء، وتاريخ الانتهاء، والوظيفة                                                           | مقاصة التقويم، التاريخ، الوظيفة، المنصب |
| المهنة                 | القسم، والنظام المكافئ للدوام الكامل، والمنصب، ونوع المنصب، والمسمى الوظيفي                                                        | المنصب الحالي، الموظف الحالي |
| اتجاه المنصب           | المناصب على مدار الوقت، ومكافئ الدوام الكامل، والوظيفة                                                                          | مقاصة التقويم، التاريخ، الوظيفة، المنصب |
| تقارير إلى               | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | العامل الحالي، الموظف الذي تم إنهاء خدمته، اتجاه الموظف |
| الموظف الذي تم إنهاء خدمته      | الموظفون الذين تم إنهاء خدمتهم، تاريخ الإنهاء، المسمى الوظيفي، المنصب، الوظيفة                                           | الشركة، والتعويض، والموقع الجغرافي، واسم الموظف، وتقارير إلى، ومقاصة التقويم، والتاريخ، والمسمى الوظيفي للموظف، والتوزيع الجغرافي، والتوظيف، والوظيفة، والمنصب والميزات |
| الميزات                 | تاريخ السريان، وخيار الميزة، وخطة الميزة، ونوع الميزة                                             | الاسم الحالي، الموظف الذي تم إنهاء خدمته، اتجاه الموظف |
| اسم الموظف            | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | الموظف الحالي، الموظف الذي تم إنهاء خدمته، اتجاه الموظف |
| المسمى الوظيفي للموظف           | المسمى الوظيفي وتاريخ الأقدمية                                                                                   | الموظف الحالي، الموظف الذي تم إنهاء خدمته، اتجاه الموظف |
| اتجاه الموظف           | الوقت الإضافي للعمال، وعدد الأشخاص، والشركة، والمنصب                                                        | الشركة، التعويض، الموقع الجغرافي، اسم الموظف، تقارير إلى، مقاصة التقويم، التاريخ، المسمى الوظيفي للموظف، التوزيع الجغرافي، التوظيف، الوظيفة، الميزات |

