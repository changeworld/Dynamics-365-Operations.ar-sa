--- 
title: "حركة خطاب الضمان"
description: "يتناول هذا الإجراء عملية خطاب الضمان."
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c2e215f1ae16f907c8b64ea1f05cf67bfb0a04b6
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="letter-of-guarantee-transaction"></a>حركة خطاب الضمان

[!include[task guide banner](../../includes/task-guide-banner.md)]

يتناول هذا الإجراء عملية خطاب الضمان.



يجب إكمال المهام التالية قبل إكمال هذا الإجراء.

- إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطاب الضمان.

- إنشاء اتفاقية تسهيلات بنكية لخطاب الضمان.



يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.


## <a name="create-sales-order-with-letter-of-guarantee"></a>إنشاء أمر مبيعات بخطاب الضمان
1. انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.
2. انقر فوق "جديد".
3. في الحقل "حساب العميل"، أدخل قيمة أو حددها.
4. قم بتوسيع القسم "عام".
5. في حقل "الموقع"، أدخل قيمة أو حددها.
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
7. في الحقل "المستودع"، أدخل قيمة أو حددها.
8. في القائمة، انقر فوق الارتباط في الصف المحدد.
9. في حقل "‏‫نوع المستند البنكي‬"، حدد "خطاب الضمان".
10. انقر فوق موافق.
11. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
12. في حقل "سعر الوحدة"، أدخل رقمًا.
13. قم بتوسيع قسم "تفاصيل البند".
14. انقر فوق علامة التبويب "التسليم".
    * ملاحظة: حدد ‏‫التحكم في تاريخ التسليم‬ = بلا  
15. في حقل "‏‫تاريخ الشحن المطلوب‬"، أدخل تاريخًا.
16. في حقل "‏‫تاريخ الشحن المؤكد‬"، أدخل تاريخًا.

## <a name="process-letter-of-guaranteerequest"></a>عملية طلب خطاب الضمان
1. في جزء الإجراءات، انقر فوق "إدارة".
2. انقر فوق خطاب الضمان.
3. في جزء "الإجراءات"، انقر فوق خطاب الضمان.
4. انقر فوق طلب لفتح مربع حوار الإسقاط.
5. في حقل "النوع"، أدخل قيمة أو حددها.
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
7. في الحقل "القيمة"، أدخل رقمًا.
8. في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.
9. انقر فوق "موافق".
10. قم بإغلاق الصفحة.

## <a name="process-letter-of-guaranteesubmit-to-bank"></a>عملية إرسال خطاب الضمان إلى البنك
1. انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. انقر فوق "تقديم للبنك" لفتح مربع حوار الإسقاط‬.
4. في الحقل "الحساب البنكي‬‬"، أدخل قيمة أو حددها.
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
6. انقر فوق "موافق".

## <a name="process-letter-of-guaranteereceive-from-bank"></a>عملية استلام خطاب الضمان من البنك
1. انقر فوق "استلام من البنك‬" لفتح مربع حوار الإسقاط.
2. في حقل "رقم البنك"، اكتب قيمة.
    * تحقق من القيم الموجودة في الحقلين الهامش المحتسب والمصروفات.  
3. انقر فوق "موافق".
4. قم بتوسيع قسم "الإجراءات".
    * تحقق من سجل "‏‫استلام من البنك".  
5. انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".
6. انقر فوق البنود.
    * تحقق من ترحيل إدخالات دفتر اليومية.  
7. قم بإغلاق الصفحة.

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a>عملية إعطاء خطاب الضمان للمستفيد
1. انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.
2. في القائمة، انقر فوق الارتباط في الصف المحدد.
3. في جزء الإجراءات، انقر فوق "إدارة".
4. انقر فوق خطاب الضمان.
5. في جزء "الإجراءات"، انقر فوق خطاب الضمان.
6. انقر فوق "‏‫منح للمستفيد‬" لفتح مربع حوار الإسقاط‬.
7. انقر فوق "موافق".
8. انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.
9. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
10. انقر فوق "‏‫منح للمستفيد‬" لفتح مربع حوار الإسقاط‬.
11. انقر فوق "موافق".
12. قم بتوسيع قسم "الإجراءات".
    * تحقق من صحة سجل "منح للمستفيد".  

## <a name="process-letter-of-guaranteeincrease-value"></a>عملية زيادة قيمة خطاب الضمان
1. انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.
2. في القائمة، انقر فوق الارتباط في الصف المحدد.
3. في جزء الإجراءات، انقر فوق "إدارة".
4. انقر فوق خطاب الضمان.
5. في جزء "الإجراءات"، انقر فوق خطاب الضمان.
6. انقر فوق "‏‫زيادة القيمة‬" لفتح مربع حوار الإسقاط.
7. في حقل "‏‫القيمة المطلوب إضافتها‬"، أدخل رقمًا.
8. انقر فوق "موافق".
9. انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.
10. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
11. انقر فوق "‏‫زيادة القيمة‬" لفتح مربع حوار الإسقاط.
12. انقر فوق "موافق".
13. قم بتوسيع قسم "الإجراءات".
    * تحقق من سجل "زيادة القيمة".  
14. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
15. انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".
16. انقر فوق البنود.
    * تحقق من إدخالات دفتر اليومية المُرحلة.  

## <a name="process-letter-of-guaranteeliquidate"></a>عملية تصفية خطاب الضمان
1. انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.
2. في القائمة، انقر فوق الارتباط في الصف المحدد.
3. في جزء الإجراءات، انقر فوق "إدارة".
4. انقر فوق خطاب الضمان.
5. في جزء "الإجراءات"، انقر فوق خطاب الضمان.
6. انقر فوق "تصفية" لفتح مربع حوار الإسقاط‬.
7. انقر فوق "موافق".
8. انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.
9. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
10. انقر فوق "تصفية" لفتح مربع حوار الإسقاط‬.
11. انقر فوق "موافق".
12. قم بتوسيع قسم "الإجراءات".
    * تحقق من سجل "تصفية‬".  
13. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
14. انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".
15. انقر فوق البنود.
    * تحقق من إدخالات دفتر اليومية المُرحلة.  
16. قم بإغلاق الصفحة.

