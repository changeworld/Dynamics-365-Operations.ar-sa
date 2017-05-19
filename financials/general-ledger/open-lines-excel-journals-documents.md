---
title: "نشر المستندات وبنود دفتر اليومية من Excel"
description: "‏‫يشرح هذا الموضوع كيفية إدخال ونشر بنود لدفاتر اليومية العامة من Microsoft Excel. كما يتضمن معلومات حول القوالب المتعددة التي يمكنك استخدامها، اعتماداً على نوع الحركات التي تقوم بإدخالها."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 9726c61b69f79bdd56803ced4c06044dd517ac13
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>نشر المستندات وبنود دفتر اليومية من Excel

[!include[banner](../includes/banner.md)]


‏‫يشرح هذا الموضوع كيفية إدخال ونشر بنود لدفاتر اليومية العامة من Microsoft Excel. كما يتضمن معلومات حول القوالب المتعددة التي يمكنك استخدامها، اعتماداً على نوع الحركات التي تقوم بإدخالها.

يمكن للمستخدمين إدخال ونشر بنود دفاتر اليومية المالية من Microsoft Excel. بعد أن يقوم مستخدم بإنشاء دفتر يومية، يعرض الزر **‬‏‫فتح البنود في Excel** القوالب المتوفرة. يتم تصميم القوالب لدعم سيناريوهات محددة، لكن لا يتم دعم كل مجموعة من أنواع الحسابات في دفتر اليومية. يعرض الجدول التالي القوالب المتوفرة وأنواع الحسابات التي تدعمها.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **القالب**             | **أنواع الحسابات المعتمدة**                                                                                             | **كيفية الوصول إلى القالب**                                                          |
| بنود دفتر يومية دفتر الأستاذ     | الحساب: دفتر الأستاذ، العميل، المورد، البنك، الحساب المقابل: دفتر الأستاذ، العميل، المورد، البنك، عمليات الشركات الشقيقة غير معتمدة.       | دفتر اليومية العام                                                                         |
| سجل الفواتير         | الحساب: المورد، الحساب المقابل: دفتر الأستاذ، عمليات الشركات الشقيقة غير معتمدة.                                                    | سجل فواتير الحسابات الدائنة                                                                     |
| دفتر يومية الفواتير          | الحسابات: المورد، الحساب المقابل: دفتر الأستاذ، عمليات الشركات الشقيقة معتمدة.                                                      | دفتر يومية فاتورة الحسابات الدائنة                                                                      |
| فاتورة المورّد           |                                                                                                                         | فاتورة المورّد                                                                          |
| دفتر يومية فواتير العميل | الحساب: العميل، الحساب المقابل: دفتر الأستاذ، عمليات الشركات الشقيقة معتمدة.                                                     | دفتر اليومية العام                                                                         |
| فاتورة ذات نص حر        |                                                                                                                         | في صفحة **فاتورة النص الحر**، انقر فوق **فتح في Excel** (رمز Microsoft Office). |
| دفتر يومية الأصول الثابتة     | الأصل لدفتر الأستاذ، أو البنك، أو العميل، أو المورد. عمليات الشركات الشقيقة غير معتمدة.                                               | دفتر يومية الأصول الثابتة                                                                     |
| دفتر يومية المدفوعات للمورد   | الحساب: المورد، الحساب المقابل: دفتر الأستاذ، البنك، عمليات الشركات الشقيقة معتمدة.                                                 | دفتر يومية المدفوعات للمورد                                                                  |
| دفتر يومية المدفوعات للعميل | الحساب: العميل، الحساب المقابل: دفتر الأستاذ، البنك، عمليات الشركات الشقيقة معتمدة.                                               | دفتر يومية المدفوعات للعميل                                                                |
| دفتر يومية مصروفات المشروع  | الحساب: المشروع، دفتر الأستاذ، العميل، المورد، الحساب المقابل: المشروع، دفتر الأستاذ، العميل، المورد، عمليات الشركات الشقيقة غير معتمدة. | مصروفات دفتر اليومية العام‬ (ضمن ‏‫‏‫إدارة المشروع‬ والمحاسبة)                       |

عند نشر البنود، يتم التحقق من صحتها للتأكد من امتثالها للقواعد التي تم إعدادها في دفاتر اليومية المالية. بعد نشر البنود، يمكن للمستخدمين تحرير أو ترحيل الإيصالات من Microsoft Dynamics 365 for Operations. 

لإضافة أبعاد مالية إلى قالب، يلزم إجراء تغييرات إضافية. للحصول على مزيد من المعلومات، انظر [إضافة الأبعاد إلى قالب Microsoft Excel](/dynamics365/operations/dev-itpro/financial/add-dimensions-excel-templates). بعد إضافة أبعاد إلى الكيان، فإنها تتوفر في مصمم Excel ويمكن إضافتها إلى القالب.





