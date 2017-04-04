---
title: "إعداد تنبيهات الاحتيال"
description: "يشرح هذا الموضوع كيفية إعداد قواعد لتنبيه ممثلي خدمة العملاء بمعلومات الاحتيال المحتمل عند معالجة الأوامر. يمكنك تعريف رموز محددة لاستخدامها لوضع الأوامر المشبوهة قيد الانتظار تلقائيًا أو يدويًا."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabb7ee23e90feca818bebfa29c7048987193e4c
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fraud-alerts"></a>إعداد تنبيهات الاحتيال

يشرح هذا الموضوع كيفية إعداد قواعد لتنبيه ممثلي خدمة العملاء بمعلومات الاحتيال المحتمل عند معالجة الأوامر. يمكنك تعريف رموز محددة لاستخدامها لوضع الأوامر المشبوهة قيد الانتظار تلقائيًا أو يدويًا. 

قبل إعداد قواعد التحقق من الاحتيال واستخدامها، يجب تمكين التحقق من الاحتيال وتعريف قيم التحقق من الاحتيال الأساسية في معلمات مراكز الاتصال. وهناك نوعان من قواعد الاحتيال:

-   **قواعد ثابتة** تستخدم قيمة معينة، مثل رقم هاتف تم إدراجه في القائمة السوداء.
-   **القواعد الحيوية** يمكن أن تتألف من الشروط والمتغيرات.

قبل إنشاء قاعدة ديناميكية، يجب إنشاء المتغيرات والشروط التي تعرّف من الذي يتم تطبيق القاعدة عليه ومتى يجب تطبيق القاعدة. على سبيل المثال، تريد إنشاء قاعدة تتطلب بأنه عندما يضع العميل 1202 أمر مبيعات بقيمة 1,000.00 أو أكثر، يجب وضع أمر المبيعات قيد الانتظار حتى يتم التحقق من دفع العميل. وفي هذه الحالة، المتغيرات هي العميل 1202 وإجمالي الأمر 1,000.00. يحدد الشرط أنه إذا قدم العميل 1202 أمرًا، وكان المبلغ الإجمالي للأمر يساوي أو أكثر من 1,000.00، فيجب تعليق أمر المبيعات حتى يتم التحقق من دفع العميل.

