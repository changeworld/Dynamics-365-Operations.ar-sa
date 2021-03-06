--- 
title: "إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطابات الضمان"
description: "تنشئ هذه المهمة تسهيلاً بنكيًا وملف تعريف ترحيل مطلوب لمعالجة خطاب ضمان."
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 022b5d411b8240390c543ba726fe0d6838752944
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطابات الضمان

[!include [task guide banner](../../includes/task-guide-banner.md)]

تنشئ هذه المهمة تسهيلاً بنكيًا وملف تعريف ترحيل مطلوب لمعالجة خطاب ضمان.



تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF. 




## <a name="general-ledger-parameter"></a>معلمة دفتر الأستاذ العام
1. انتقل إلى إدارة النقد والبنك > الإعداد > معلمات إدارة النقد والبنوك.
2. قم بتوسيع القسم "المستند البنكي".
3. حدد الخيار "تمكين خطاب الضمان".
4. في الحقل "دفتر يومية الحركات"، انقر فوق زر القائمة المنسدلة لفتح البحث.
5. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
7. انقر فوق علامة التبويب "التسلسلات الرقمية".
    * تعريف كود التسلسل الرقمي لرقم خطاب الضمان ومراجع حركات خطابات الضمان  
8. انقر فوق "حفظ".
9. قم بإغلاق الصفحة.

## <a name="create-bank-facility"></a>إنشاء تسهيل بنكي
1. انتقل إلى إدارة النقد والبنك > الإعداد > التسهيلات البنكية.
2. انقر فوق "جديد".
3. في الحقل "مجموعة التسهيلات"، أدخل اسم مجموعة التسهيلات البنكية الخاصة بحركة خطاب الضمان.
4. في وصف الحقل، اكتب قيمة.
5. انقر فوق "حفظ".
6. انقر فوق علامة التبويب "أنواع التسهيلات".
7. انقر فوق "جديد".
8. في الحقل "نوع التسهيل"، أدخل اسم نوع التسهيل البنكي المرتبط باتفاقية التسهيلات البنكية.
9. في حقل "الوصف"، اكتب قيمة.
10. في الحقل "مجموعة التسهيلات"، انقر فوق زر القائمة المنسدلة لفتح البحث.
11. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
12. في القائمة، انقر فوق الارتباط في الصف المحدد.
13. في الحقل "طبيعة التسهيل"، حدد خيارًا.
14. انقر فوق "حفظ".
15. قم بإغلاق الصفحة.

## <a name="bank-posting-profile"></a>ملفات تعريف ترحيل بنكي
1. انتقل إلى إدارة النقد والبنك > الإعداد > ملف تعريف ترحيل المستندات البنكية.
2. انقر فوق "جديد".
3. في الحقل "رقم الحساب/المجموعة"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
6. في الحقل "حساب التسوية"، حدد الحساب الرئيسي للتسوية.
7. في الحقل "المصاريف"، حدد حساب حركات المصروفات.
8. في الحقل "حساب الهامش"، حدد الحساب لحركة الهامش.
9. في الحقل "حساب التصفية"، حدد حساب التصفية لحركة خطاب الضمان. 
10. انقر فوق حفظ.
11. قم بإغلاق الصفحة.


