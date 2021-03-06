--- 
title: "وجهات تكوين التقارير الإلكترونية"
description: "يوضح هذا الإجراء كيفية الإعداد واستخدام وجهات مختلفة لمكونات إخراج التقارير الإلكترونية (ER)، مثل مجلد أو ملف."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 83c6b8db609b83f94b51800616976eb9ce08d79b
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="er-configure-destinations"></a>وجهات تكوين التقارير الإلكترونية

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية الإعداد واستخدام وجهات مختلفة لمكونات إخراج التقارير الإلكترونية (ER)، مثل مجلد أو ملف. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF. تُعد ألمانيا بلد/منطقة العنوان الأساسي للكيان القانوني، على الرغم من ذلك، يمكنك استخدام أي كيان قانوني لهذا الإجراء. 

التنسيق المستخدم في هذا المثال هو تحويل الائتمان ISO20022 (DE)، ولكن يمكنك استخدام أي تنسيق قمت باستيراده بالفعل. لاحظ أن هذا الإجراء عبارة عن مثال لملف واحد وإعداد وجهة واحدة. يمكن العثور على مزيد من المعلومات حول إدارة وجهات التقارير الإلكترونية في تعليمات Dynamics 365 for Finance and Operations.

1. انتقل إلى إدارة المؤسسة > التقارير الإلكترونية > وجهة إعداد التقارير الإلكترونية‬.
2. انقر فوق "جديد" لإنشاء مجموعة جديدة من وجهات لتنسيق.
3. في حقل "المرجع"، حدد التنسيق الذي تريد تكوين الوجهات له.
    * إذا لم يكن لديك قيمة لتحددها، فهذا يعني أنك لم تقم باستيراد أي تكوينات تنسيق إعداد التقارير الإلكترونية. يجب استيراد تكوين تنسيق قبل إعداد الوجهات.  
4. انقر فوق "جديد" لإنشاء وجهة ملف جديدة.
    * لاحظ أنه يمكنك إنشاء وجهة ملف واحد لكل مكون مخرجات من التنسيق نفسه، مثل مجلد أو ملف. ستكون قادرًا على تمكين الوجهات وتعطيلها بشكل منفصل في الإعدادات.  
5. في الحقل "الاسم"، أدخل اسم المستخدم المألوف لمكون المخرجات.
    * نوصي باستخدام أسماء ذات معنى، مثل "ملف الدفع" أو "التحكم في التقرير". سيتم تقديم هذه الأسماء للمستخدمين في وقت تشغيل التكوين جنبًا إلى جنب مع إعدادات الوجهة.  
6. في اسم "الملف"، حدد الملف أو المجلد الخاص بالتنسيق.
7. انقر فوق "إعدادات".
8. حدد "نعم" في الحقل "تمكين".
    * تعمل خانة الاختيار "تمكين" على كل علامة تبويب وتعطل كل جهة بشكل منفصل. في هذا المثال، ستقوم بتمكين إرسال ملف إخراج إلى متلقي بريد عند إنشاء الملف.  
9. انقر فوق "تحرير" لإعداد مستلمي البريد الإلكتروني.
10. وانقر فوق إضافة.
11. انقر فوق "بريد إلكتروني خاص بإدارة الطباعة‬".
12. في الحقل "مصدر البريد الإلكتروني"، حدد خيارًا.
    * يمكنك تحديد أنواع مصادر بريد إلكتروني مختلفة، مثل نوع المورّد أو العميل. يحدد هذا نوع الوسيطة التي سيتم إرجاعها بواسطة معادلة حساب البريد الإلكتروني. تُعد معادلة حساب البريد الإلكتروني, الموضحة في خطوة تالية، المكان حيث سيتم ربط مصدر البريد إلكتروني. حدد المود إذا كانت المعادلة ستعود على حساب المورد. استخدم المورد إذا كنت تستخدم مثال تكوين نقل ائتمان ISO 20022.  
13. انقر فوق الزر "ربط مصدر البريد الإلكتروني".
14. في المعادلة، أدخل مرجعًا خاصًا بمستند إلى نوع طرف حددته في وقت سابق.
    * بدلاً من الكتابة، يمكنك العثور على عقدة مصدر بيانات تمثل حساب الطرف، وانقر فوق الزر "إضافة مصدر البيانات" لتحديث المعادلة. على سبيل المثال، إذا كنت تستخدم تكوين تحويل الائتمان ISO 20022، فإن العقدة التي تمثل حساب المورّد هي "$PaymentsForCoveringLetter". Creditor.Identification.SourceID. وإلا، أدخل أي قيمة سلسلة، مثل "DE-001"، لحفظ المعادلة.  
15. انقر فوق "حفظ".
16. قم بإغلاق الصفحة.
17. انقر فوق "تحرير" لتكوين جهة الاتصال للطرف.
18. حدد "نعم" في الحقل "جهة الاتصال الرئيسية‬".
    * يمكنك استخدام خيارات مختلفة للإشارة إلى نوع جهة الاتصال للطرف التي يجب استخدامها كعنوان بريد إلكتروني لهذه الوجهة. نحن نستخدم جهة الاتصال الرئيسية في هذا المثال.  
19. انقر فوق "موافق".
20. انقر فوق "موافق".
21. في الحقل "الموضوع"، اكتب قيمة.
22. انقر فوق "موافق".


