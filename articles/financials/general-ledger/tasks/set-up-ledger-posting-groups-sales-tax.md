--- 
title: "إعداد مجموعات ترحيل دفتر الأستاذ لضريبة المبيعات"
description: "يتم حساب ضريبة المبيعات وترحيلها إلى الحسابات الرئيسية التي تم تحديدها في مجموعات ترحيل دفتر الأستاذ."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 15421da6f325dfee22a303e9fe83a0e72895fa08
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>إعداد مجموعات ترحيل دفتر الأستاذ لضريبة المبيعات

[!include [task guide banner](../../includes/task-guide-banner.md)]

يتم حساب ضريبة المبيعات وترحيلها إلى الحسابات الرئيسية التي تم تحديدها في مجموعات ترحيل دفتر الأستاذ. يتم إرفاق مجموعات ترحيل دفتر الأستاذ بكل كود ضريبة مبيعات. ويمكنك إعداد مجموعات ترحيل فردية لدفتر الأستاذ بالنسبة لكل كود من أكواد ضريبة المبيعات؛ حيث يمكن استخدام مجموعة ترحيل دفتر أستاذ واحدة لكافة أكواد ضريبة المبيعات، أو تعيين بعض مجموعات متعددة لترحيل دفتر الأستاذ لأكواد ضريبة المبيعات. يستخدم هذا التسجيل شركة بيانات العرض التوضيحي DEMF. 

1. انتقل إلى الضريبة > إعداد > ضريبة المبيعات > مجموعات ترحيل دفتر الأستاذ.
2. انقر فوق "جديد".
3. في حقل "مجموعة ترحيل دفتر الأستاذ"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. في الحقل "ضريبة المبيعات مستحقة الدفع"، حدد الحساب الرئيسي لضرائب المبيعات الصادرة التي تدفع لهيئة الضرائب.
    * يتم تحصيل ضرائب المبيعات نيابة عن هيئة الضرائب عندما تبيع بضائع وخدمات خاضعة للضريبة.  
6. في الحقل "ضريبة المبيعات مستحقة القبض‬"، حدد الحساب الرئيسي لضرائب المبيعات الواردة التي يتم استلامها من هيئة الضرائب.
    * يقوم المورّدون بتحصيل الضرائب نيابة عن هيئة الضرائب عندما تبيع بضائع وخدمات خاضعة للضريبة. لا يتوفر هذا الحقل إذا كان الخيار "تطبيق قواعد فرض ضرائب على المبيعات‬" محددًا في صفحة محددات دفتر الأستاذ العام. كبديل لذلك، يتم خصم ضرائب المبيعات التي تُدفع إلى المورّدين إلى الحساب نفسه باعتبارها مشتريات.   
7. في الحقل "مصروفات ضريبة الانتفاع‬"، حدد الحساب الرئيسي لترحيل ضرائب الانتفاع الخاضعة للخصم التي لم يتم طلبها أو الإبلاغ عنها لدى هيئة الضرائب من قِبل المورّدين كجزء من الرسوم العكسية GST/HST في الاتحاد الأوروبي.
    * يجب تحديد الخيار "ضريبة الانتفاع" لكود ضريبة المبيعات في مجموعة ضريبة المبيعات المستخدمة في الحركة.  لا يتوفر هذا الحقل إذا كان الخيار "تطبيق قواعد فرض ضرائب على المبيعات‬" محددًا في صفحة محددات دفتر الأستاذ العام.   
8. في الحقل "ضريبة الانتفاع الدائنة‬"، حدد الحساب الرئيسي لترحيل ضرائب الانتفاع الواردة التي تدفع لهيئة الضرائب.
    * يجب تحديد الخيار "ضريبة الانتفاع" في كود ضريبة المبيعات في مجموعة ضريبة المبيعات لترحيل ضريبة الانتفاع. إذا تم تحديد الخيار "تطبيق قواعد فرض ضرائب على المبيعات‬" في محددات دفتر الأستاذ العام، فسيتم تعويض الحركة في حساب مصروفات الحركة.   
9. في الحقل "حساب التسوية"، حدد الحساب الرئيسي حيث سيتم ترحيل الرصيد الصافي لحسابات دفتر الأستاذ المحددة في الحقلين "ضريبة الانتفاع الدائنة‬" وضريبة المبيعات مستحقة القبض‬".
    * سيتم إنشاء الرصيد عند تسوية ضريبة المبيعات وتشغيل وظيفة ترحيل.  إذا كانت هيئة الضرائب‬ لفترة التسوية مقترنة بحساب مورّد، فسيتم ترحيل الرصيد إلى حساب المورّد بدلاً من ذلك.   
10. في الحقل "الخصم النقدي للمورد‬"، حدد الحساب الرئيسي لترحيل الخصم النقدي لأكواد ضريبة المبيعات المرتبطة بمجموعة ترحيل دفتر الأستاذ هذا.
    * هذا الأمر اختياري وإذا لم يتم إدخال أي حساب، فسيتم استخدام الحساب الرئيسي على أكواد الخصم النقدي. قد يكون من المفيد استخدام حسابات مختلفة لكل مجموعة ترحيل دفتر الأستاذ‬ باستخدام الخيار "قلب ضريبة المبيعات عند الخصم النقدي‬" على مجموعات ضرائب المبيعات.  
11. في الحقل "الخصم النقدي للعميل‬‬"، حدد الحساب الرئيسي لترحيل الخصم النقدي لأكواد ضريبة المبيعات المرتبطة بمجموعة ترحيل دفتر الأستاذ هذا.
    * هذا الأمر اختياري وإذا لم يتم إدخال أي حساب، فسيتم استخدام الحساب الرئيسي على أكواد الخصم النقدي. قد يكون من المفيد استخدام حسابات مختلفة لكل مجموعة ترحيل دفتر الأستاذ‬ باستخدام الخيار "قلب ضريبة المبيعات عند الخصم النقدي‬" على مجموعات ضرائب المبيعات.  
12. انقر فوق "حفظ".


