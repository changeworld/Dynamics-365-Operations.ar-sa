---
title: "محتوى Power BI لإدارة الممارسات"
description: "يوضح هذا الموضوع العناصر المضمنة في محتوى Power BI لإدارة الممارسات. وهو يوضح كيفية الوصول إلى التقارير التي تم تضمينها في المحتوى، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى."
author: KimANelson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 7b2c13573aca2ceb0eca36cf4aeee80d2f56ab8a
ms.contentlocale: ar-sa
ms.lasthandoff: 08/13/2018

---

# <a name="practice-manager-power-bi-content"></a>محتوى Power BI لإدارة الممارسات

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع العناصر المضمنة في محتوى Microsoft Power BI **إدارة الممارسات**. فهو يوضح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات التي يتم استخدامها لإنشاء المحتوى.

## <a name="overview"></a>نظرة عامة

تم إنشاء محتوى Power BI **إدارة الممارسات** لمدراء الممارسات ومدراء المشاريع. وهو يوفر المقاييس الرئيسية المرتبطة بالمشاريع التي تعمل مؤسستك على تنفيذها. توفر لوحة المعلومات نظرة عامة حول المشاريع والعملاء المرتبطين بها. يمكن استخدام عامل تصفية على مستوى التقرير لإعداد تقارير لكيانات قانونية محددة. يقوم محتوى Power BI هذا بسحب البيانات من القياسات التجميعية لمحاسبة المشروع.

يتضمن محتوى Power BI **إدارة الممارسات** خمس صفحات تقرير: صفحة النظرة العامة وأربع صفحات توفر تفاصيل حول تكاليف المشروع والإيرادات وإدارة القيمة المكتسبة ومقاييس الساعة المقسمة عبر أبعاد مختلفة.

يتم عرض كافة المبالغ الموجودة في المحتوى بعملة النظام. يمكنك تعيين عملة النظام في صفحة **محددات النظام**.

## <a name="accessing-the-power-bi-content"></a>الوصول إلى محتوى Power BI

يتم عرض محتوى Power BI **مدير الممارسة** في مساحة عمل **إدارة المشاريع**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>التقارير المضمنة في محتوى Power BI

يوفر الجدول التالي تفاصيل حول المقاييس التي يتم العثور عليها في كل صفحة من صفحات التقرير في محتوى Power BI **إدارة الممارسات**.

| صفحة التقرير       | المقاييس |
|-------------------|---------|
| نظرة عامة على المشروعات | <ul><li>إنشاء مشاريع</li><li>المشاريع المقدرة</li><li>المشاريع قيد التنفيذ</li><li>الإيراد الفعلي حسب العميل</li><li>إجمالي هامش الربح في الموازنة حسب المشروع</li><li>نظرة عام على إدارة القيمة المكتسبة</li></ul> |
| التكلفة              | <ul><li>التكلفة الفعلية في مقابل تكلفة الموازنة بالشهر</li><li>التكلفة الفعلية في مقابل تكلفة الموازنة بالسنة</li><li>التكلفة الفعلية في مقابل تكلفة الموازنة حسب الفئة</li><li>التكلفة الفعلية حسب نوع الحركة</li></ul> |
| الإيراد           | <ul><li>الإيراد الفعلي بالشهر</li><li>الإيراد الفعلي حسب الرمز البريدي</li><li>الإيراد الفعلي في مقابل إيراد الموازنة حسب الفئة</li><li>الإيراد الفعلي حسب مجال العميل</li></ul> |
| EVM               | مؤشر أداء التكلفة والجدول حسب المشروع |
| الساعات             | <ul><li>الساعات الفعلية المستخدمة القابلة للفوترة‬ في مقابل الساعات الفعلية غير المحسوبة على العميل القابلة للفوترة‬ في مقابل ساعات الميزانية</li><li>الساعات الفعلية المستخدمة القابلة للفوترة‬ في مقابل الساعات الفعلية غير المحسوبة على العميل القابلة للفوترة‬ حسب المشروع</li><li>الساعات الفعلية المستخدمة القابلة للفوترة‬ في مقابل الساعات الفعلية غير المحسوبة على العميل القابلة للفوترة‬ حسب المورد</li><li>نسبة الساعات الفعلية القابلة للفوترة حسب المشروع</li><li>نسبة الساعات الفعلية القابلة للفوترة حسب المورد</li></ul> |

يمكنك تصفية المخططات والإطارات المتجانبة الموجودة على كافة هذه التقارير وتثبيتها بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). يمكنك أيضًا استخدام وظيفة تصدير البيانات الأساسية لتصدير البيانات الأساسية التي تم تلخيصها في المرئيات.

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات

تُستخدم البيانات التالية لملء صفحات التقارير في محتوى Power BI **إدارة الممارسات**. يتم تمثيل هذه البيانات كقياسات مجمعة تم تجهيزها في مخزن الكيانات. مخزن الكيانات هو قاعدة بيانات لخادم Microsoft SQL تم تحسينها للتحليلات. لمزيد من المعلومات، راجع [نظرة عامة عن تكامل Power BI مع متجر الكيان](power-bi-integration-entity-store.md).

تصف الأقسام التالية القياسات التجميعية‬ التي يتم استخدامها في كل كيان.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>الكيان: ProjectAccountingCube\_ActualHourUtilization
**مصدر البيانات:** ProjEmplTrans

| القياسات التجميعية الرئيسية      | الحقل                              | ‏‏الوصف |
|--------------------------------|------------------------------------|-------------|
| الساعات الفعلية المستخدمة القابلة للفوترة | المجموع(ActualUtilizationBillableRate) | إجمالي الساعات المستخدمة الفعلية القابلة للفوترة. |
| الساعات الفعلية غير المحسوبة على العميل القابلة للفوترة   | المجموع(ActualBurdenBillableRate)      | إجمالي معدل القيمة الفعلية غير المحسوبة على العميل. |

### <a name="entity-projectaccountingcubeactuals"></a>الكيان: ProjectAccountingCube\_Actuals
**مصدر البيانات:** ProjTransPosting

| القياسات التجميعية الرئيسية | الحقل              | ‏‏الوصف |
|---------------------------|--------------------|-------------|
| الإيراد الفعلي            | المجموع(ActualRevenue) | إجمالي الإيرادات المرحلة لكل الحركات. |
| التكلفة الفعلية               | المجموع(ActualCost)    | إجمالي التكلفة المرحلة لكافة أنواع الحركات. |

### <a name="entity-projectaccountingcubecustomer"></a>الكيان: ProjectAccountingCube\_Customer
**مصدر البيانات:** CustTable

| القياسات التجميعية الرئيسية | الحقل                                             | ‏‏الوصف |
|---------------------------|---------------------------------------------------|-------------|
| عدد المشاريع        | COUNTA(ProjectAccountingCube\_Projects\[PROJECTS\]) | عدد المشاريع المتوفرة |

### <a name="entity-projectaccountingcubeforecasts"></a>الكيان: ProjectAccountingCube\_Forecasts
**مصدر البيانات:** ProjTransBudget

| القياسات التجميعية الرئيسية | الحقل                  | ‏‏الوصف |
|---------------------------|------------------------|-------------|
| تكلفة الموازنة               | المجموع(BudgetCost)        | إجمالي التكلفة المتوقعة‬ لكافة أنواع الحركات. |
| إيرادات الموازنة            | المجموع(BudgetRevenue)     | إجمالي الإيراد المتوقع المستحق/المفوتر. |
| إجمالي هامش ربح الموازنة       | المجموع(BudgetGrossMargin) | الفرق بين مجموع إجمالي الإيراد المتوقع ومجموع إجمالي التكلفة المتوقعة. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>الكيان: ProjectAccountingCube\_ProjectPlanCostsView
**مصدر البيانات:** Project

| القياسات التجميعية الرئيسية | الحقل                    | ‏‏الوصف |
|---------------------------|--------------------------|-------------|
| التكلفة المخططة              | المجموع(SumOfTotalCostPrice) | إجمالي سعر التكلفة في تقديرات كافة أنواع حركات المشروع مع المهام المخططة. |

### <a name="entity-projectaccountingcubeprojects"></a>الكيان: ProjectAccountingCube\_Projects
**مصدر البيانات:** Project

| القياسات التجميعية الرئيسية    | الحقل | الوصف |
|------------------------------|-------|-------------|
| مؤشر أداء التكلفة       | ProjectAccountingCube\_Projects\[القيمة المكتسبة\] ÷ ProjectAccountingCube\_Projects\[إجمالي التكلفة الفعلية للمهام المكتملة\] | حساب إجمالي القيمة المكتسبة مقسومًا على إجمالي التكلفة الفعلية. |
| مؤشر أداء الجدول   | ProjectAccountingCube\_Projects\[القيمة المكتسبة\] ÷ ProjectAccountingCube\_Projects\[إجمالي التكلفة المخططة للمهام المكتملة\] | حساب إجمالي القيمة المكتسبة مقسومًا على إجمالي التكلفة المخططة. |
| النسبة المئوية للعمل المكتمل | النسبة المئوية للعمل المكتمل = ProjectAccountingCube\_Projects\[إجمالي التكلفة الفعلية للمهام المكتملة\] ÷ (ProjectAccountingCube\_Projects\[إجمالي التكلفة الفعلية للمهام المكتملة\] + ProjectAccountingCube\_Projects\[إجمالي التكلفة المخططة للمشروع\] – ProjectAccountingCube\_Projects\[إجمالي التكلفة المخططة للمهام المكتملة\]) | إجمالي النسبة المئوية للعمل المكتمل استنادًا إلى إجمالي التكلفة الفعلية للمهام المكتملة والتكلفة المخططة للمشروع. |
| نسبة الساعات الفعلية القابلة للفوترة  | ProjectAccountingCube\_Projects\[إجمالي الساعات المستخدمة الفعلية القابلة للفوترة للمشروع\] ÷ (ProjectAccountingCube\_Projects\[إجمالي الساعات المستخدمة الفعلية القابلة للفوترة للمشروع\] + ProjectAccountingCube\_Projects\[إجمالي الساعات الفعلية غير المحسوبة على العميل القابلة للفوترة\]) | إجمالي الساعات الفعلية القابلة للفوترة، استنادًا إلى عدد الساعات المستخدمة والساعات المحسوبة على العميل. |
| القيمة المكتسبة                 | ProjectAccountingCube\_Projects\[إجمالي التكلفة المخططة للمشروع\] × ProjectAccountingCube\_Projects\[النسبة المئوية للعمل المكتمل\] | إجمالي التكلفة المخططة مضروبًا في النسبة المئوية للعمل المكتمل. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>الكيان: ProjectAccountingCube\_TotalEstimatedCosts 
**مصدر البيانات:** ProjTable

| القياسات التجميعية الرئيسية       | الحقل               | ‏‏الوصف |
|---------------------------------|---------------------|-------------|
| التكلفة المخططة للنشاط المكتمل | المجموع(TotalCostPrice) | إجمالي سعر التكلفة في تقديرات كافة أنواع حركات المشروع مع المهام المكتملة. |

