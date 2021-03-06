---
title: "مجموعات حسابات توحيد وحسابات توحيد إضافية"
description: "‏‫يقدم هذا الموضوع معلومات حول مجموعات حسابات التوحيد وحسابات التوحيد الإضافية ويشرح كيفية استخدامها في Microsoft Dynamics 365 for Finance and Operations."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 60486002b520fdf347ed2537cefa0a45e06d6271
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>مجموعات حسابات توحيد وحسابات توحيد إضافية

[!include [banner](../includes/banner.md)]

‏‫يقدم هذا الموضوع معلومات حول مجموعات حسابات التوحيد وحسابات التوحيد الإضافية ويشرح كيفية استخدامها في Microsoft Dynamics 365 for Finance and Operations.

<a name="consolidation-account-groups"></a>مجموعات حسابات الدمج
----------------------------

تتيح لك مجموعات حسابات التوحيد إنشاء مجموعات من الحسابات التي تريد استخدامها لتوحيد البيانات. في معظم الأحيان، تمثل مجموعة حسابات التوحيد مخطط حسابات حكومي أو تعيِّن الحسابات إلى مجموعة يتم تحديدها من قِبل المقر الرئيسي للشركة. يمكنك العثور على مجموعات حسابات التوحيد في جزء **الإعداد** بالوحدة النمطية **عمليات التوحيد**. عندما تقوم بإضافة مجموعة جديدة، أدخل معرفاً فريداً لمجموعة الحسابات واسمًا لها.

## <a name="additional-consolidation-accounts"></a>حسابات التوحيد الإضافية
تتيح لك ‏‫حسابات التوحيد الإضافية‬ تعيين حساب من مخطط حسابات موجود إلى إحدى مجموعات حسابات التوحيد. يمكنك بعد ذلك تحديد قيمة حساب التوحيد واسمه. 

يمكنك العثور على حسابات التوحيد الإضافية في جزء **الإعداد** بالوحدة النمطية **عمليات التوحيد**. عند إنشاء حساب توحيد جديد، يجب تحديد المعلومات التالية:

-   **الحساب الرئيسي** – يعتبر هذا الحقل هو حقل بحث يوضح كافة الحسابات الرئيسية التي تستند إلى مخطط الحسابات الذي قمت بتحديده في الصفحة. عند تحديد حساب، يتم تلقائياً إدخال الاسم في الحقل **اسم الحساب الرئيسي**.
-   **مجموعة حسابات التوحيد** – استخدم هذا الحقل لتحديد المجموعة لتعيين الحساب إليها. إذا أجريت التوحيد بطريقتين مختلفتين، يجب إضافة نفس الحساب لكافة مجموعات حسابات التوحيد الأربع.
-   **حساب التوحيد** - أدخل قيمة حساب التوحيد. وهذه القيمة لا يلزم أن تكون حساباً من مخطط حسابات. يمكن أن تكون أي قيمة تتطلبها.
-   **اسم حساب التوحيد** – أدخل اسم الحساب كما تريده أن يظهر في الاستعلامات والتقارير.
-   **مستوى SAT** – يُستخدم هذا الحقل لإعداد تقارير بخصوص كشوف الحسابات لهيئات الضرائب المكسيكية. 

عند الانتهاء من إنشاء مجموعات حسابات التوحيد وحسابات التوحيد الإضافية، يمكنك تحديد المجموعة في عملية التوحيد عبر الإنترنت.


لمزيد من المعلومات، راجع [إنشاء مجموعات توحيد وحسابات توحيد إضافية](../general-ledger/tasks/create-consolidation-groups.md). 




