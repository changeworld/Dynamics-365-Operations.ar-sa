--- 
title: "إنشاء قاعدة كانبان لسحب"
description: "يظهر هذا الإجراء الإعداد المطلوب لإنشاء قاعدة كانبان للسحب لنقل المواد في بيئة محدودة."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02c7133d2e02b27fb428874deeda21e2bab28fb6
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a>إنشاء قاعدة كانبان لسحب

[!include [task guide banner](../../includes/task-guide-banner.md)]

يظهر هذا الإجراء الإعداد المطلوب لإنشاء قاعدة كانبان للسحب لنقل المواد في بيئة محدودة. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لتزويد مادة جديدة أو معدلة.


## <a name="create-new-kanban-rule"></a>إنشاء قاعدة كانبان جديدة
1. انتقل إلى قواعد كانبان.
2. انقر فوق "جديد".
3. في حقل "النوع"، حدد "انسحاب".
    * يتم استخدام نوع الانسحاب لقواعد كانبان لنقل المواد أو السلع.  
4. في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.
    * حدد ReplenishSpeakerComponents.   يتم إعداد هذا النشاط لنقل المكونات من المستودع 11 والموقع 11 إلى 12 المستودع والموقع 12.  
5. في الحقل "المنتج"، أدخل قيمة أو حددها.
    * حدد "M0007".  
6. في الحقل "وقت الإنتاج‬"، أدخل رقمًا.
    * على سبيل المثال، 60.  
7. في الحقل "وحدة القياس"، أدخل قيمة أو حددها.
    * فمثلاً، الدقائق.  

## <a name="set-quantities-for-kanban"></a>قم بإعداد كميات لكانبان
1. قم بتعيين الكمية الافتراضية على "5".
    * هذه هي الكمية التي سيتم تحويلها لكل كانبان.  
2. في الحقل "كانبان الكمية الثابتة"، أدخل "2".
    * وهذا هو كمية كانبان التي يجب أن تكون نشطة. في هذه الحالة، يوجد 2 كانبان تنقل كل منها 5.  
3. في الحقل "الحد الأدنى للتنبيه"، أدخل "1".
    * تُستخدم لتعقب الحد الأدنى لكمية كانبان الكاملة التي ينبغي أن تكون في الوجهة. على سبيل المثال، يتم استخدام ذلك في النظرة العامة على كمية كانبان.  
4. في الحقل "الحد الأقصى للتنبيه"، أدخل "2".
    * تُستخدم لتعقب الحد الأقصى لكمية كانبان الكاملة التي ينبغي أن تكون في الوجهة. على سبيل المثال، يتم استخدام ذلك في النظرة العامة على كمية كانبان.  

## <a name="create-kanbans"></a>إنشاء بطاقات كانبان
1. انقر فوق "حفظ".
    * يجب حفظ قاعدة كانبان قبل إنشاء كانبان.  
2. وانقر فوق إضافة.
    * لاحظ أنه لا وجود لكانبان نشطة، بسبب أن "عدد الكانبان الجديدة" المقترح هو 2، وهذا يساوي "كمية كانبان ثابتة".  
3. انقر فوق "إنشاء".
    * سيؤدي هذا إلى إنشاء 2 كانبان.  
    * لاحظ أنه تم إنشاء 2 كانبان، لكل منها 5، لقاعدة كانبان للسحب.  وهذه هي الخطوة الأخيرة في هذا الإجراء.  


