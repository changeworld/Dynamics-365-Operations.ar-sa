--- 
title: "‏‫وضع طريقة دفع العميل‬"
description: "إنشاء طريقة دفع لمدفوعات العميل."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabcfe83ac83a8210ce4e0d46a08acdc48f4bf3b
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-method-of-payment"></a>‏‫وضع طريقة دفع العميل‬

[!include [task guide banner](../../includes/task-guide-banner.md)]

إنشاء طريقة دفع لمدفوعات العميل. تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

1. انتقل إلى الحسابات المدينة > إعداد الدفعات > طرق الدفع.
2. انقر فوق "جديد".
3. في الحقل "طريقة الدفع"، أدخل معرفًا لطريقة الدفع.
    * يظهر معرف طريقة الدفع على الفواتير والمدفوعات، لذا اجعله وصفيًا قدر الإمكان لفهم نوع الدفع الذي سيتم تسجيله، ولأي حساب بنكي.  
4. في الحقل "الوصف"، أدخل وصفًا.
5. حدد حالة الدفع المطلوبة لترحيل لمدفوعات.
    * عند إنشاء دفعة العميل، لا يمكن ترحيلها إلا عندما تكون حالة الدفع مطابقة لحالة الدفع التي قمت بتعريفها هنا.  
6. حدد كيفية إنشاء مدفوعات العملاء للفواتير.
    * يستخدم هذا الخيار فقط عند تشغيل مقترح دفع. يمكن استخدام مقترح الدفع لمدفوعات العميل عند إجراء خصومات مباشرة وسحب الأموال من الحسابات البنكية للعملاء.  
7. حدد نوع الدفع.
    * سيساعد نوع الدفع في تحديد ما إذا كانت عملية التحقق من الصحة ستحدث أم لا على الدفع.  
8. حدد أنواع الحسابات التي سيتم ترحيل المدفوعات إليها.
    * بشكل عام، يمكن تحديد "البنك" لهذا الخيار.  
9. حدد الحساب البنكي الذي سيتم تسجيل هذه الدفعة فيه.
10. أدخل نوع الحركة البنكية لتحديد نوع الدفع المستخدم من قبل البنك الذي تتعامل معه.
    * يُستخدم نوع الحركة البنكية المستخدمة أثناء عملية التسويات البنكية، وبإمكانه تسهيل عملية التسوية.  
11. حدد ما إذا كان سيتم ترحيل هذه الدفعة هذه مؤقتًا إلى حساب مؤقت.
    * إذا كنت تريد تجربة الوقت العائم لإجراء مخالصة مع المصرف، فاستخدم وظيفة المرحلة المؤقتة. سيتم ترحيل الدفع مؤقتًا إلى حساب دفتر أستاذ حتى تتم المخالصة مع البنك، وفي هذا الوقت ستتنقل الدفعة إلى الحساب البنكي الذي قمت بتعريفه هنا.  
12. أدخل الحساب الرئيسي المستخدم للترحيل المؤقت.
    * هذا هو الحساب الرئيسي الذي سيتم ترحيل الدفعة إليه بشكل مؤقت عند استخدام المرحلة المؤقتة.  
13. استخدم علامة التبويب "تنسيق الملف" لتحديد الإعداد لعمليات الدفع الإلكترونية.
14. استخدم علامة التبويب "التحكم في الدفع" لتحديد الحقول الإلزامية.
    * على سبيل المثال، إذا كنت تطالب بأن يتم إيداع كافة المدفوعات بطريقة الدفع هذه، فيمكنك تحديد هذا الخيار في علامة التبويب هذه.  
15. استخدم علامة التبويب "سمات الدفع‬" لتحديد سمات الدفع التي تريد استخدامه لطريقة الدفع هذه.
16. انقر فوق "حفظ".


