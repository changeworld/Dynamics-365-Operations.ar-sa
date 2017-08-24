---
title: "استلام لوحة ترخيص مختلطة"
description: "يصف هذا الموضوع كيفية استخدام استلام لوحة ترخيص مختلطة‬ لتسجيل وانشاء عمل لأصناف متعددة بواسطة جهاز محمول."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0e785d71e7ae3c5f60d36d8b190001b5e356c626
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---

# <a name="mixed-license-plate-receiving"></a>استلام لوحة ترخيص مختلطة

[!include[banner](../includes/banner.md)]

يسمح لك استلام لوحة ترخيص مختلطة بإنشاء لوحة ترخيص تتكون من العديد من الأصناف قبل أن تقوم بالتسجيل وإنشاء عمل تخزين. 

لا تحتاج لوحة الترخيص المكونة من عدة أصناف إلى تقسيمها في رصيف الاستلام لكي تتمكن من تسجيل كل صنف. 

عند استخدام تدفق ذي صلة بالأصناف لتحديد بنود المستند المصدر، يمكنك فحص الأكواد الشريطية في عنصر تحكم الصنف. إذا تضمن الكود الشريطي كمية ووحدة قياس تم تكوينهما عليه، فسيضاف الصنف والكمية تلقائيًا إلى لوحة الترخيص المختلطة، وسيعاد توجيهك إلى الشاشة لمسح صنف آخر. سيسمح لك ذلك بفحص كافة الأصناف من دون الحاجة إلى إجراء تأكيد في كل خطوة. 

في التدفق الخاص باستلام لوحة الترخيص المختلطة، يمكنك عرض قائمة بالأصناف التي تم فحصها على لوحة الترخيص، ومن هنا يمكنك تعديل أو تصحيح كمية أحد الأصناف.

## <a name="where-it-applies"></a>أين يتم التطبيق

إن استلام لوحة الترخيص المختلطة‬ عبارة عن تدفق استلام على جهاز محمول لتسجيل وانشاء عمل لأصناف/بنود متعددة في الوقت نفسه. يعتبر هذا الأمر مفيدًا إذا كنت تتلقى لوحات ترخيص واردة ذات أصناف متعددة. 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>كيفية إعداد استلام ‏‫لوحة الترخيص‬ المختلطة
يتم إعداد استلام ‏‫لوحة الترخيص‬ المختلطة وتخزينها كعنصر قائمة جهاز محمول.

تحتاج إلى إنشاء عنصر قائمة جديد باستخدام وضع العمل الذي لا يستخدم العمل الموجود واستخدام إحدى الطريقتين التاليتين:

- استلام لوحة ترخيص مختلطة
- استلام ‏‫لوحة الترخيص‬ المختلطة وتخزينها

هناك خيارات للتعرف على بنود المستند المصدر وهي صنف أمر الشراء وبند أمر الشراء وأمر الإرجاع‬ وصنف أمر التحويل‬ وبند أمر التحويل. باستطاعة هذه الخيارات تغيير أمر الاستلام على لوحة ترخيص واحدة. الخيار الأخير يتعلق بصنف حمل العمل. يمكنك إضافة عدة عناصر إلى لوحة الترخيص، ولكن لا يمكنك التبديل بين أحمال عمل متعددة.
