---
title: "تنزيل تكوينات التقارير الإلكترونية من Lifecycle Services"
description: "يوضح هذا الموضوع كيفية تنزيل تكوينات التقارير الإلكترونية من Microsoft Dynamics Lifecycle Services ‏(LCS)."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 8686d2639a3ab7f2e79944cc5eed51571d463261
ms.contentlocale: ar-sa
ms.lasthandoff: 08/13/2018

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>تنزيل تكوينات التقارير الإلكترونية من Lifecycle Services

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية تنزيل تكوينات التقارير الإلكترونية من Microsoft Dynamics Lifecycle Services ‏(LCS).

يرشدك هذا البرنامج التعليمي عبر عملية تنزيل الإصدار الأحدث من تكوينات التقارير الإلكترونية من Microsoft Dynamics Lifecycle Services (LCS).

1. سجّل الدخول إلى Finance and Operations باستخدام أحد الأدوار التالية:

    - مطور إعداد التقارير الإلكتروني
    - مستشار وظيفي لإعداد التقارير الإلكتروني
    - مسؤول النظام

2. انتقل إلى **‎إدارة المؤسسة** &gt; **‎إعداد التقارير الإلكترونية**.
3. في مقطع **موفرو التكوين**، حدد لوحة **Microsoft**.
4. على لوحة **Microsoft**، انقر فوق **مستودعات**.

    [![تحديث التقارير الإلكترونية من LCS لـ MS - فتح قائمة المستودعات](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. في صفحة **مستودعات التكوين**، في الشبكة، حدد المستودع الموجود من النوع **LCS**. إذا لم يظهر هذا المستودع في الشبكة، فاتبع الخطوات التالية:

    1. انقر فوق **إضافة** لإضافة مستود جديد.
    2. حدد **LCS** كنوع المستودع.
    3. انقر فوق **إنشاء مستودع**.
    4. اتبع الإرشادات التخويل، إذا طلب منك ذلك.
    5. قم بإدخال اسم ووصف للمستودع.
    6. انقر فوق **موافق** لتأكيد إدخال المستودع الجديد.
    7. في الشبكة، حدد المستودع الجديد من النوع **LCS‎**.

6. انقر فوق **فتح** لعرض قائمة تكوينات التقارير الإلكترونية للمستودع المحدد.

    [![تحديث التقارير الإلكترونية من LCS لـ MS - عمل ‏‫مستودع LCS](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

7. في شجرة التكوينات في الجزء الأيمن، حدد تكوين التقارير الإلكترونية المطلوب.
8. على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.
9. انقر فوق **استيراد** لتنزيل الإصدار المحدد من LCS إلى مثيل Finance and Operations الحالي.

    > [!NOTE]
    > لا يتوفر الزر **استيراد**‏‎ لإصدارات تكوينات التقارير الإلكترونية الموجودة في مثيل Finance and Operations الحالي.

    [![تحديث التقارير الإلكترونية من LCS لـ MS - تنزيل التكوين](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> استنادًا إلى إعدادات التقارير الإلكترونية، يتم التحقق من صحة التكوينات بعد استيرادها. قد يتم إعلامك بأي مشكلات عدم التوافق التي يتم اكتشافها. يجب حل هذه المشكلات قبل أن تتمكن من استخدام إصدار التكوين المستورد. لمزيد من المعلومات، راجع قائمة المقالات ذات الصلة لهذا الموضوع.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على إعداد التقارير الإلكتروني](general-electronic-reporting.md)

