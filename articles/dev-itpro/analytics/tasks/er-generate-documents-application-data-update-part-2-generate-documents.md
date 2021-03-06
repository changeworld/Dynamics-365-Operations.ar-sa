--- 
title: "تصميم تكوينات لإنشاء مستندات تتضمن بيانات التطبيق"
description: "لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 1 - استيراد التكوينات)‬."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8376107a33dd83e04f82fcab6847e7f073f08dbc
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>تصميم تكوينات لإنشاء مستندات تتضمن بيانات التطبيق

[!include [task guide banner](../../includes/task-guide-banner.md)]

لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 1: استيراد التكوينات)‬.



توضح الخطوات الواردة في هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني. في هذا الإجراء، ستقوم بتشغيل تكوين التنسيق المستورد للتقارير الإلكترونية الذي تم إنشاؤها للشركة النموذجية، Litware, Inc. لإنشاء المستندات الإلكترونية.



تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية. يمكن إتمام هذه الخطوات باستخدام مجموعة بيانات DEMF. 



قبل أن تبدأ، قم بتغيير سياق البلد لشركة DEMF من DEU (ألمانيا) إلى BEL (بلجيكا). انقر فوق إدارة المؤسسات > المؤسسات > الكيانات القانونية لتحديث رمز البلد في العنوان الرئيسي للكيان القانوني DEMF. أعد تشغيل التطبيق.


## <a name="run-imported-er-format"></a>تشغيل تنسيق التقارير الإلكترونية المستورد
1. انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.
2. في الشجرة، قم بتوسيع "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".
3. في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (تنسيق)".
4. انقر فوق "تشغيل".
    * قم بتشغيل إصدار المسودة لتكوين تنسيق التقارير الإلكترونية لإنشاء تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.  
5. في الحقل "إدخال اسم الملف"، اكتب "intrastat.xml".
    * حدد اسم الملف.  
6. انقر فوق "موافق".
    * راجع ملف XML المنشأ.  
7. قم بإغلاق الصفحة.
8. انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.
    * افتح هذا النموذج لعرض حركات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المضمنة في المستند الإلكتروني المنشأ.  
9. انقر فوق أرشيف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.
    * نظرًا لعدم احتواء تنسيق التقارير الإلكترونية الذي تم تنفيذه على أي إعدادات خاصة بتحديث بيانات التطبيق، لم تتم أرشفة تفاصيل تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المكتمل.  
10. قم بإغلاق الصفحة.
11. قم بإغلاق الصفحة.


