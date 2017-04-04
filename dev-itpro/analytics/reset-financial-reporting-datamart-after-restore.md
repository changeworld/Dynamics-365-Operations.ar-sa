---
title: "إعادة تعيين مارت بيانات التقارير المالية بعد استعادة قاعدة البيانات"
description: "يصف هذا الموضوع كيفية إعادة تعيين مارت بيانات التقارير المالية بعد استعادة Microsoft Dynamics 365 لعمليات قاعدة البيانات."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>إعادة تعيين مارت بيانات التقارير المالية بعد استعادة قاعدة البيانات

يصف هذا الموضوع كيفية إعادة تعيين مارت بيانات التقارير المالية بعد استعادة Microsoft Dynamics 365 لعمليات قاعدة البيانات. 

هناك عدة سيناريوهات حيث قد تحتاج إلى استعادة 365 الديناميات الخاصة بك لعمليات قاعدة البيانات من نسخة احتياطية أو نسخة قاعدة البيانات من بيئة أخرى. عند حدوث ذلك، تحتاج أيضا إلى اتبع الخطوات المناسبة لضمان أن مارت بيانات التقارير المالية بشكل صحيح يستخدم 365 Dynamics المستعادة لعمليات قاعدة البيانات. إذا كانت لديك أسئلة حول إعادة تعيين مارت بيانات التقارير المالية لسبب خارج استعادة 365 Dynamics لعمليات قاعدة البيانات، راجع [رض البيانات "أداة إدارة" إعادة تعيين](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) للحصول على مزيد من المعلومات. لاحظ أن الخطوات الموجودة في هذه العملية معتمدة لديناميات 365 لعملية إصدار مايو 2016 (التطبيق 7.0.1265.23014 والماليه تقارير البناء 7.0.10000.4) والإصدارات الأحدث. إذا كان لديك إصدار سابق من 365 ديناميات عمليات، الرجاء الاتصال بفريق الدعم للحصول على المساعدة.

## <a name="export-report-definitions"></a>تصدير ملفات تعريف التقرير
أولاً، تصدير تصميمات التقارير الموجودة في "مصمم التقرير"، استخدام الخطوات التالية:

1.  في "مصمم التقرير"، انتقل إلى **شركة**&gt;**"كتلة إنشاء مجموعات"**.
2.  حدد مجموعة كتلة الإنشاء تصدير، ثم انقر فوق **تصدير**. **ملاحظة:** لديناميات 365 للعمليات، يتم اعتماد مجموعة واحدة فقط من كتل الإنشاء، **الافتراضي**.
3.  تحديد تعريفات التقرير للتصدير:
    -   لتصدير كافة تعريفات التقارير وكتل الإنشاء المقترنة، انقر فوق **تحديد الكل**.
    -   لتصدير مجموعات محددة من التقارير أو الصفوف أو الأعمدة أو الأشجار أو الأبعاد، انقر فوق علامة التبويب المناسبة ثم حدد العناصر المراد تصديرها. اضغط مع الاستمرار على مفتاح Ctrl لتحديد أصناف متعددة في علامة التبويب. عند تحديد التقارير للتصدير، يتم تحديد الصفوف المرتبطة الأعمدة والأشجار ومجموعات الأبعاد.

4.  انقر فوق **تصدير**.
5.  أدخل اسم ملف وحدد موقع أمن حيث تريد حفظ تعريفات التقرير الذي تم تصديره.
6.  Click **Save**.

يمكن نسخ الملف أو تحميلها إلى موقع أمن، يسمح باستيرادها إلى بيئة مختلفة في وقت آخر. يمكن العثور على معلومات حول استخدام حساب Microsoft Azure تخزين في [نقل البيانات باستخدام الأداة "المساعدة لسطر الأوامر أزكوبي"](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **ملاحظة:** لا تقدم Microsoft حساب تخزين كجزء من 365 الديناميات الخاصة بك لعمليات الاتفاقية. يجب شراء حساب تخزين أو استخدام حساب تخزين من اشتراك Azure منفصلة. **هام:** تكون على علم بسلوك محرك الأقراص D على الأجهزة الظاهرية Azure. لا تحتفظ بمجموعات المصدر البنائية هنا بشكل دائم. لمزيد من المعلومات حول محركات الأقراص المؤقتة، [فهم محرك أقراص مؤقت على الأجهزة الظاهرية من Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>إيقاف الخدمات
استخدام "سطح المكتب البعيد" للاتصال بكافة أجهزة الكمبيوتر الموجودة في البيئة وإيقاف خدمات Windows التالية باستخدام services.msc:

-   خدمة (على كافة أجهزة كمبيوتر AOS) نشر world wide web
-   Microsoft Dynamics 365 "عمليات دائرة إدارة المجموعة" (أجهزة الكمبيوتر العامة AOS فقط)
-   إدارة خدمة العمليات مراسل 2012 (على أجهزة كمبيوتر "المعلومات المهنية" فقط)

سيكون الاتصالات المفتوحة إلى 365 ديناميات عمليات قاعدة بيانات لهذه الخدمات.

## <a name="reset"></a>إعادة التعيين
#### <a name="locate-the-latest-dataupgradezip-package"></a>حدد موقع حزمة أحدث DataUpgrade.zip

حدد موقع حزمة DataUpgrade.zip أحدث الاتجاهات في استخدام [تحميل البرنامج النصي DataUpgrade.zip](..\migration-upgrade\upgrade-data-to-latest-update.md). توضح الإرشادات كيفية تحديد الإصدار الصحيح من حزمة ترقية البيانات للبيئة الخاصة بك.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>تنفيذ البرامج النصية لقاعدة بيانات عمليات ضد Dynamics 365

تشغيل البرامج النصية التالية 365 حيوية لعمليات قاعدة البيانات (ليس مقابل قاعدة بيانات التقارير المالية).

-   DataUpgrade.zip\\أوسيرفيسي\\البرامج النصية\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\أوسيرفيسي\\البرامج النصية\\GrantAzViewChangeTracking.sql

هذه البرامج النصية تأكد من المستخدمين والأدوار وتغيير إعدادات التتبع الصحيح.

#### <a name="execute-powershell-command-to-reset-database"></a>تنفيذ الأمر PowerShell لإعادة تعيين قاعدة البيانات

تنفيذ الأمر التالي مباشرة على جهاز كمبيوتر AOS، لإعادة التكامل بين ديناميات 365 للعمليات والتقارير المالية:

1.  قم بفتح Windows PowerShell كمسؤول.
2.  التنفيذ: واو:
3.  التنفيذ: القرص المضغوط f:\\مرابليكاتيونسيرفيسي\\مرينستالديريكتوري
4.  التنفيذ: استيراد وحدة. \\الخادم\\مرديبلوي\\MRDeploy.psd1
5.  تنفيذ: إعادة تعيين-داتامارتينتيجريشن-"أسباب أخرى"-ريسونديتايل "&lt;لي سبب إعادة تعيين&gt;"
    -   سيتم مطالبتك بإدخال "نعم" لتأكيد.

شرح المعلمات:

-   تكون القيم الصالحة لالسبب: صيانة، باداتا، أخرى.
-   أن المعلمة ريسونديتايل-النص الحر.
-   سيتم تسجيل السبب وريسونديتايل في مراقبة القياس عن بعد والبيئة.

## <a name="start-services"></a>بدء تشغيل الخدمات
لإعادة تشغيل الخدمات التي توقفت في وقت سابق، استخدم services.msc:

-   خدمة (على كافة أجهزة كمبيوتر AOS) نشر world wide web
-   Microsoft Dynamics 365 "عمليات دائرة إدارة المجموعة" (أجهزة الكمبيوتر العامة AOS فقط)
-   إدارة خدمة العمليات مراسل 2012 (على أجهزة كمبيوتر "المعلومات المهنية" فقط)

## <a name="import-report-definitions"></a>استيراد تعريفات التقرير
استيراد تصاميم التقرير من "مصمم التقرير"، استخدام ملف الذي تم إنشاؤه أثناء عملية التصدير:

1.  في "مصمم التقرير"، انتقل إلى **شركة**&gt;**"كتلة إنشاء مجموعات"**.
2.  حدد مجموعة كتلة الإنشاء تصدير، ثم انقر فوق **تصدير**. **ملاحظة:** لديناميات 365 للعمليات، يتم اعتماد مجموعة واحدة فقط من كتل الإنشاء، **الافتراضي**.
3.  حدد **الافتراضي** بناء كتلة وانقر **استيراد**.
4.  حدد الملف الذي يحتوي على تعريفات التقرير الذي تم تصديره ثم انقر فوق **فتح**.
5.  في مربع الحوار استيراد، حدد تعريفات التقرير المراد استيرادها.
    -   لاستيراد كافة تعريفات التقارير وكتل الإنشاء الداعمة، انقر فوق **تحديد الكل**.
    -   لاستيراد تقارير أو صفوف أو أعمدة أو أشجار أو مجموعات أبعاد محددة، حدد التقارير أو الصفوف أو الأعمدة أو الأشجار أو مجموعات الأبعاد لاستيرادها.

6.  انقر فوق **استيراد**.


