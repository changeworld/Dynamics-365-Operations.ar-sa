---
title: "قم بإعداد برنامج استمرارية لمركز اتصالات"
description: "تصف هذه المقالة كيفية إعداد ‏‫برنامج الاستمرارية لمركز الاتصال."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: e32961f2a0e0e41715d98075cbc5777d256eb187
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>قم بإعداد برنامج استمرارية لمركز اتصالات

تصف هذه المقالة كيفية إعداد ‏‫برنامج الاستمرارية لمركز الاتصال.

في برنامج استمرارية، ويعرف أيضًا ببرنامج الأمر المتكرر، يتلقى العملاء شحنات المنتجات العادية وفقًا لجدول معرف مسبقاً. يمكن أن يحتوي كل شحنة على منتج مختلف، كما في حالة نادي كتاب الشهر، أو يمكن إرسال المنتج نفسه مرارًا وتكرارًا. ولإعداد برنامج استمرارية، يجب عليك إكمال المهام التالية.

1.  تعيين معلمات الاستمرارية في صفحة **معلمات مركز الاتصالات**.
2.   أنشئ برنامج استمرارية والذي يحدد تفاصيل مثل جدول الدفع، توقيت الشحنات، وما إذا كانت الفوترة مقدمًا. يجب أيضًا إضافة قائمة بالمنتجات التي يتضمنها برنامج الاستمرارية. يتلقى كل منتج رقم معرف حدث الذي تم تعيين التسلسل، بدءاً من 1. تحديد معرفات الحدث بالترتيب الذي يتم إرسال المنتجات.
    -   إذا تلقي العملاء منتجًا مختلفًا في كل شحنة، يتم إرسال المنتجات بترتيب متسلسل وفقًا لمعرفات الأحداث الخاصة بها، بدءاً من الحدث الحالي.
    -   إذا تلقي العملاء نفس المنتج في كل شحنة، تحتوي القائمة على منتج واحد ذو معرف حدث واحد. يحدث نفس الحدث مرارًا وتكرارًا. يمكنك تحديد عدد المرات التي يتكرر بها كل حدث.

3.  قم بإنشاء منتج الأصلي الذي يمثل استمرارية البرنامج الذي قمت بإنشائه في المهمة الثانية. إذا قمت بإضافة هذا المنتج لأمر توريد، **استمرارية** فتح الصفحة. يمكنك فيما بعد استخدام هذه الصفحة لإنشاء أمر الاستمراية الفعلي. لا يحدد المنتج الأصل المنتجات الفردية التي يتلقاها العميل في كل شحنة.

بعد قيامك بإعداد برنامج استمرارية كما هو موضح أعلاه، يمكنك إنشاء أمر استمرارية لأحد العملاء. وقد تحتاج إلى تنفيذ مهام الصيانة الإضافية التالية.

-   **تحديث فترة حدث الاستمرارية الحالية** – إعداد وظيفة الدفعة التي تُعلم النظام بفترة الحدث الحالية.
-   **إنشاء أوامر استمرارية فرعية** – إنشاء أوامر الاستمرارية الفرعية من أمر الاستمرارية الأصلي.
-   **معالجة مدفوعات الاستمرارية** – معالجة الفواتير ورسائل الإعلام الخاصة بالمدفوعات المرتبطة بأوامر المبيعات الاستمرارية.
-   **توسيع بنود الاستمرارية** (عند اللزوم) – توسيع عدد المرات التي يمكن تكرارها حدثاً استمرارية. ويمكن لتكرار الشحنات فيما بعد تجاوز الحد الذي تم تعيينه في حقل **حد تكرار الاستمرارية** في معلمات مركز الاتصالات.
-   **تنفيذ عملية تحديث استمرارية** (عند اللزوم) – مزامنة التغييرات بين برنامج الاستمرارية وأوامر المبيعات الأصلية الاستمرارية.
-   **إغلاق بنود وأوامر الاستمرارية الأصلية** – إغلاق أوامر الاستمرارية.


