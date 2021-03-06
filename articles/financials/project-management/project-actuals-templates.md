---
title: "مزامنة القيم الفعلية لمشروع مباشرةً من Project Service Automation إلى دفتر يومية تكامل المشروع للترحيل في Finance and Operations"
description: "يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة القيم الفعلية لمشروع مباشرةً من Microsoft Dynamics 365 for Project Service Automation إلى Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 0a965e8de596decf39a15977e6df8a6aa9dd35b0
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>مزامنة القيم الفعلية لمشروع مباشرةً من Project Service Automation إلى دفتر يومية تكامل المشروع للترحيل في Finance and Operations

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة القيم الفعلية لمشروع مباشرةً من Microsoft Dynamics 365 for Project Service Automation إلى Microsoft Dynamics 365 for Finance and Operations.

يقوم القالب بمزامنة الحركات من Project Service Automation إلى جدول مرحلي في Finance and Operations. بعد اكتمال المزامنة، **يجب** عليك استيراد البيانات من الجدول المرحلي إلى دفتر يومية التكامل.

> [!NOTE]
> - يتوافر تكامل القيم الفعلية للمشروع في Microsoft Dynamics 365 for Finance and Operations، الإصدار 8.01 أو إصدار لاحق.
> - إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستتمكن من استخدام القوالب لإجراء تكامل لمهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية ولتكوين تأمين الوظيفة. إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.
> - إذا كنت تستخدم Finance and Operations 7.3.0، وتعمل على إحضار حركات الرسوم من Project Service Automation، فيجب تثبيت KB 4345320 لتضمين تلك الرسوم في فاتورة المشروع.
> - إذا كنت تعمل على إدخال مبالغ ضريبة المبيعات في حركات الوقت أو المصروفات في Project Service Automation، فيجب تثبيت Project Service Automation Update 7. وإلا، فلن يتم ربط القيم الفعلية للضريبة بالقيم الفعلية للوقت أو المصروفات المقترنة، ولن تتم مزامنتها مع Finance and Operations. تواصل مع الدعم لمزيد من المعلومات.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>تدفق البيانات الخاصة بـ Project Service Automation إلى Finance and Operations

يستخدم الحل المتكامل لـ Project Service Automation إلى Finance and Operations ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Project Service Automation و Finance and Operations تتيح قوالب التكامل المتوفرة مع ميزة تكامل البيانات تدفق البيانات الخاصة بالقيم الفعلية لمشروع من Project Service Automation إلى Finance and Operations.

يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Project Service Automation و Finance and Operations.

[![تدفق البيانات الخاصة بـ Project Service Automation مع Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>القيم الفعلية من Project Service Automation

### <a name="template-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، في مركز إدارة Microsoft PowerApps ، حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب التالي والمهام الأساسية لمزامنة القيم الفعلية لمشروع من Project Service Automation إلى Finance and Operations.

- **اسم القالب في تكامل البيانات:** القيم الفعلية للمشروع (PSA إلى Fin and Ops)
- **أسماء المهام في المشروع:**

    - المبالغ الفعلية
    - TransactionConnections

### <a name="entity-set"></a>مجموعة الكيانات

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| المبالغ الفعلية                    | كيان التكامل للقيم الفعلية للمشروع                   |
| اتصالات الحركات    | كيان التكامل لعلاقات حركات المشروع |

### <a name="entity-flow"></a>تدفق الكيان

تتم إدارة القيم الفعلية للمشروع في Project Service Automation، ثم تتم مزامنتها إلى دفتر يومية تكامل المشروع في Finance and Operations. سوف يتم تطبيق المحاسبة استنادًا إلى الأبعاد المالية الافتراضية وإعداد الترحيل.

### <a name="prerequisites"></a>المتطلبات الأساسية

قبل القيام بمزامنة القيم الفعلية، يجب عليك تكوين محددات تكامل Project Service Automation ومزامنة المشاريع ومهام المشاريع وفئات حركة مصروفات المشروع.

### <a name="power-query"></a>Power Query

في قالب القيم الفعلية للمشروع، يجب عليك استخدام Microsoft Power Query لـ Excel لإكمال هذه المهام:

- تحويل نوع الحركة في Project Service Automation إلى نوع الحركة الصحيح في Finance and Operations. تكون عملية التحويل هذه معرّفة في قالب القيم الفعلية للمشروع (PSA إلى Fin and Ops).
- تحويل نوع الفوترة في Project Service Automation إلى نوع الفوترة الصحيح في Finance and Operations. تكون عملية التحويل هذه معرّفة في قالب القيم الفعلية للمشروع (PSA إلى Fin and Ops). بعد ذلك، يتم تعيين نوع الفوترة إلى خاصية البند استنادًا إلى التكوين في صفحة **محددات تكامل Project Service Automation**.
- تصفية وحدات تنظيمية لموارد محددة يجب مزامنتها مع هذا القالب.
- إذا كانت مزامنة القيم الفعلية للوقت أو القيم الفعلية للمصروفات بين الشركات الشقيقة ستتم إلى Finance and Operations، فيجب عليك تحويل الوحدة التنظيمية للعقد إلى الكيان القانوني الصحيح في Finance and Operations. يحتوي قالب القيم الفعلية للمشروع (PSA إلى Fin and Ops) على عمود شرطي محدد استنادًا إلى بيانات العرض التوضيحي. يجب عليك تحديث العمود الشرطي الأخير المُدرج إلى الكيانات القانونية الصحيحة. وإلا، فقد يحدث خطأ تكامل أو قد يتم استيراد حركات قيم فعلية غير صحيحة إلى Finance and Operations.
- إذا لم تتم مزامنة القيم الفعلية للوقت أو القيم الفعلية للمصروفات بين الشركات الشقيقة إلى Finance and operations، فيجب حذف العمود الشرطي الأخير المُدرج من قالبك. وإلا، فقد يحدث خطأ تكامل أو قد يتم استيراد حركات قيم فعلية غير صحيحة إلى Finance and Operations.

#### <a name="contract-organizational-unit"></a>الوحدة التنظيمية للعقد
لتحديث العمود الشرطي الأخير المُدرج في القالب، انقر فوق سهم **تعيين** لفتح التعيين. حدد الارتباط **الاستعلام المتقدم والتصفية** لفتح Power Query.

- إذا كنت تستخدم قالب القيم الفعلية للمشروع الافتراضي (PSA إلى Fin and Ops)، فحدد **الشرط المُدرج** الأخير من قسم **الخطوات المُطبقة** في Power Query. في إدخال **الوظيفة**، استبدل **USSI** باسم الكيان القانوني الذي الذي يجب استخدامه مع التكامل. قم بإضافة شروط إضافية حسب الحاجة إلى إدخال **الوظيفة**، وقم بتحديث شرط **else** من **USMF** إلى الكيان القانوني الصحيح.
- إذا كنت تقوم بإنشاء قالب جديد، يجب عليك إضافة العمود لدعم الوقت والمصروفات بين الشركات الشقيقة. حدد **إضافة عمود شرطي**، وأدخل اسمًا للعمود مثل **LegalEntity**. أدخل شرطًا للعمود، حيث إذا **msdyn\_contractorganizationalunitid.msdyn\_الاسم** هو \<وحدة تنظيمية\>، ثم \<أدخل الكيان القانوني\>؛ else null.

### <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية مثالاً لتعيين مهمة القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Project Service Automation إلى Finance and Operations.

[![تعيين القالب](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![تعيين القالب](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>الاستيراد من جدول مرحلي‬ بعد التكامل من Project Service Automation

يجب تشغيل الاستيراد من عملية دورية لجدول مرحلي بعد مزامنة القيم الفعلية من Project Service Automation إلى Finance and Operations. سوف تستورد هذه العملية حركات المشروع من الجدول المرحلي إلى دفتر يومية تكامل Project Service Automation، حيث يتم تطبيق المحاسبة ويمكن ترحيل الحركات التي تم استيرادها. ننصح بأن تقوم بتشغيل هذه العملية في الوضع الدفعي، ويمكنك بشكل اختياري إعداد التشغيل كمجموعة متكررة.

## <a name="update-actuals-from-finance-and-operations"></a>تحديث القيم الفعلية من Finance and Operations

### <a name="template-and-tasks"></a>القوالب والمهام

يتم استخدام القالب التالي والمهام الأساسية لمزامنة رقم الإيصال وضرائب المبيعات لحركات المشروعات المُرحلة من Finance and Operations إلى Project Service Automation:

- **اسم القالب في تكامل البيانات:** تحديث القيم الفعلية للمشروع (Fin and Ops إلى PSA)
- **أسماء المهام في المشروع:**

    - المبالغ الفعلية 
    - TransactionConnections

### <a name="entity-set"></a>مجموعة الكيانات

| Finance and Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| كيان التكامل للقيم الفعلية للمشروع                   | المبالغ الفعلية                    |
| كيان التكامل لعلاقات حركات المشروع | اتصالات الحركات    |

### <a name="entity-flow"></a>تدفق الكيان

تتم إدارة القيم الفعلية للمشروع في Project Service Automation، ثم تتم مزامنتها إلى دفتر يومية تكامل المشروع في Finance and Operations. بعد ترحيل القيم الفعلية في Finance and Operations، يتم تحديثها في Project Service Automation باستخدام رقم الإيصال من Finance and Operations. إذا تمت إضافة ضرائب المبيعات في Finance and Operations، سوف يتم إنشاء قيم ضريبية فعلية جديدة في Project Service Automation.

### <a name="power-query"></a>Power Query

في قالب تحديث القيم الفعلية للمشروع، يجب عليك استخدام Power Query لإكمال هذه المهام:

- تحويل نوع الحركة في Finance and Operations إلى نوع الحركة الصحيح في Project Service Automation. تكون عملية التحويل هذه معرّفة في تحديث قالب القيم الفعلية للمشروع (Fin Ops إلى PSA).
- تحويل نوع الفوترة في Finance and Operations إلى نوع الفوترة الصحيح في Project Service Automation. تكون عملية التحويل هذه معرّفة في تحديث قالب القيم الفعلية للمشروع (Fin Ops إلى PSA).

### <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي أمثلة لتعيينات مهام القالب في تكامل البيانات. يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Finance and Operations إلى Project Service Automation.

[![تعيين القالب](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![تعيين القالب](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)

