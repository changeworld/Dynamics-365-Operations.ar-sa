--- 
title: "إعداد الحسابات البنكية للشركة لتحويلات الائتمان ISO20022"
description: "يوضح هذا الإجراء كيفية إعداد المعلومات المحددة الخاصة بالحساب البنكي للشركة والمطلوبة لإنشاء ملف الدفع."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>إعداد الحسابات البنكية للشركة لتحويلات الائتمان ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إعداد المعلومات المحددة الخاصة بالحساب البنكي للشركة والمطلوبة لإنشاء ملف الدفع. يمكنك إعداد المعلومات المطلوبة لإنشاء تنسيق تحويل الائتمان 20022 ISO، ولكن استنادًا إلى التنسيق قد تكون هناك معلومات أخرى مطلوبة، مثل "معرف الشركة" أو "كود الفرز". 

شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.

هذه هو الإجراء الثاني من ضمن الإجراءات الخمسة، هدفه توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية. يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.


## <a name="set-up-iban-and-swift-code"></a>إعداد كود IBAN وكود التحويل الإلكتروني
1. انتقل إلى إدارة النقد والبنوك > الحسابات البنكية.
2. استخدم عامل التصفية السريع لإجراء التصفية على الحقل "الحساب البنكي‬" بالقيمة "DEMF OPER''.
3. انقر فوق "DEMF OPER" لفتح تفاصيل الحساب البنكي.
4. انقر فوق "تحرير".
5. ‏‫قم بتوسيع المقطع "تعريف إضافي".
6. في الحقل "IBAN"، اكتب ''DE89370400440532013000".
7. في الحقل "كود التحويل الإلكتروني‬"، اكتب "DEUTDEFF".
    * لاحظ أن SWIFT\BIC غير مطلوب للعديد من تنسيقات الدفع، لكن من المستحسن أن يتم تسجيله لحساب بنكي.  
8. انقر فوق "حفظ".

## <a name="set-up-bank-account-for-the-legal-entity"></a>إعداد الحساب البنكي للكيان القانوني
1. انتقل إلى إدارة المؤسسة > المؤسسات > الكيانات القانونية.
2. انقر فوق "تحرير".
3. ‏‫قم بتوسيع القسم "معلومات الحساب البنكي‬".
4. في الحقل "الحساب البنكي‬‬"، أدخل قيمة أو حددها.
5. انقر فوق "حفظ".


