---
title: "إنشاء مستندات إلكترونية وتحديث بيانات التطبيق باستخدام التقارير الإلكترونية​"
description: "يمكنك تصميم تنسيقات التقارير الإلكترونية التي يمكن استخدامها في تطبيق Finance and Operations لإنشاء مستندات إلكترونية صادرة. يمكنك أيضًا تصميم تنسيقات التقارير الإلكترونية التي تحلل المستندات الإلكترونية الواردة وتستخدم المحتوى في هذه المستندات لتحديث بيانات التطبيق."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 6bb2b2480b619a8aee72c2d65052ed419c9a7c7d
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>إنشاء مستندات إلكترونية وتحديث بيانات التطبيق باستخدام التقارير الإلكترونية​

[!include [banner](../includes/banner.md)]

يمكنك تصميم تنسيقات التقارير الإلكترونية التي يمكن استخدامها في تطبيق Finance and Operations لإنشاء مستندات إلكترونية صادرة. يمكنك أيضًا تصميم تنسيقات التقارير الإلكترونية التي تحلل المستندات الإلكترونية الواردة وتستخدم المحتوى في هذه المستندات لتحديث بيانات التطبيق.

باستخدام هذه الميزة، يمكن استخدام تنسيق تقارير إلكترونية واحد لإنشاء المستندات الإلكترونية الصادرة ثم تحديث بيانات التطبيق. يمكن استخدام هذه الميزة في السيناريوهات التالية:

- لمنع الاستخدام المتكرر لبيانات التطبيق في عمليات لاحقة، يمكنك وضع علامة على بيانات التطبيق مباشرة بعد استخدامها لإنشاء المستندات الإلكترونية. على سبيل المثال، يمكنك وضع علامة على حركات الدفع كحركات تمت معالجتها مباشرةً بعد تضمينها في رسالة الدفع الناشئة.
- لتخزين تفاصيل معالجة المستندات الإلكترونية التي تم إنشاؤها باستخدام منطق التقارير الإلكترونية. على سبيل المثال، تعريف رسالة دفع فريد يتم إنشاؤه باستخدام تعبير التقارير الإلكترونية. يستند التعبير إلى المعلومات التي تم إدخالها في مربع حوار التقارير الإلكترونية عند تشغيل تنسيق التقارير الإلكترونية لإنشاء المستندات.

لمزيد من المعلومات حول هذه الميزة، قم بتشغيل مجموعة دلائل المهام الخاصة بالتقارير الإلكترونية "إنشاء المستندات باستخدام تحديث بيانات التطبيق" (جزء من العملية التجارية اكتساب/تطوير مكونات الخدمات/الحلول الخاصة بتقنية المعلومات)، التي ستنقلك عبر تفاصيل التقارير والأرشفة في نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي. الملفات التالية مطلوبة لإكمال بعض الخطوات في دلائل المهام هذه. قم بتنزيل وحفظ هذه الملفات في جهازك المحلي.

- [تكوين نموذج بيانات التقارير الإلكترونية: نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)](https://go.microsoft.com/fwlink/?linkid=849038)
- [تكوين تعيين نموذج التقارير الإلكترونية: نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (التعيين)](https://go.microsoft.com/fwlink/?linkid=849038)
- [تكوين تنسيق التقارير الإلكترونية: نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (التنسيق)](https://go.microsoft.com/fwlink/?linkid=849038)

