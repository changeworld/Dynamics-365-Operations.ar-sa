--- 
title: "إنشاء اتفاقية تجارية جديدة"
description: "يوضح لك هذا الإجراء كيفية إنشاء اتفاقية تجارة يتم فيها تسجيل منتج سعر جديد لمبيعات المنتجات اتفقتَ عليه مع عميل معين."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-trade-agreement"></a>إنشاء اتفاقية تجارية جديدة

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح لك هذا الإجراء كيفية إنشاء اتفاقية تجارة يتم فيها تسجيل منتج سعر جديد لمبيعات المنتجات اتفقتَ عليه مع عميل معين. يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة. إذا كنت تستخدم البيانات الخاصة بك، قبل أن تبدأ استخدام هذا الدليل فأنت بحاجة إلى أن تتأكد من وجود اسم لدفتر يومية اتفاقيات التجارة حيث يتم تعيين العلاقة الافتراضية إلى "السعر (مبيعات)".


## <a name="create-and-post-a-new-trade-agreement-journal"></a>قم بإنشاء دفتر يومية جديد لاتفاقيات التجارة وترحيله
1. انتقل للمبيعات والتسويق > الأسعار والخصومات > دفاتر يوميات اتفاقيات التجارة.
2. انقر فوق "جديد".
3. في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
6. انقر فوق البنود.
7. في الحقل "رمز الحساب" حدد "الجدول".
    * في هذا المثال، تقومُ بتحديث السعر لعميل معين، وهو ما يعني أنك تحتاج إلى اختيار الجدول. إذا كنت تحدث سعر قائمة المنتجات، يمكنك تحديد "الكل"، بحيث يكون السعر الجديد صالحاً لجميع العملاء. إذا كنت تميز الأسعار بين قطاعات مختلفة من العملاء، يمكنك تحديد "مجموعة". لتحديد مجموعة، يجب أن تقوم بإعداد مجموعات أسعار العملاء أولاً.  
8. في الحقل "اختيار الحساب"، انقر فوق زر القائمة المنسدلة لفتح البحث.
9. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
10. في الحقل "رمز الصنف"، حدد "الجدول".
    * عند إبرام اتفاقية تجارة من نوع "السعر (مبيعات)"، يجب عليك تحديد "جدول" فقط في رمز الصنف. وهذا لأن السعر يمثل قيمة مطلقة ولا يمكن أن يتكرر مع جميع المنتجات أو مجموعة من المنتجات.  
11. في الحقل "علاقة الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.
12. في القائمة، حدد المنتج الذي تريد تضمينه في الاتفاقية.
    * قم بتدوين ملاحظة بالمنتج الذي حددتَه.  
13. في القائمة، انقر فوق الارتباط في الصف المحدد.
14. في الحقل "من"، أدخل حدًا أدنى للكمية.
    * إذا كان العميل ملزمًا بطلب حد أدنى من كمية قبل أن يستطيع التأهل للسعر الجديد، فستحتاج إلى تحديد تلك الكمية هنا.  
    * أدخل قيمة في الحقل "إلى" لتحديد الحد الأقصى للكمية الذي لا تُعتبر الاتفاقية صالحة إذا تجاوزتْه. إذا قمت بتقديم الأسعار والخصومات استناداً إلى فواصل كميات متعددة، فقم بتحديد كل قوس كمية كزوج من الحد الأدنى والحد الأقصى للكمية في الحقلين 'من' و'إلى' على التوالي.  
15. في الحقل "المبلغ بالعملة"، أدخل سعراً.
16. في الحقل "من تاريخ"، أدخل تاريخًا ستكون الاتفاقية صالحة بدءًا منه.
17. انقر فوق "حفظ".
18. انقر فوق "التحقق من الصحة‬".
19. انقر فوق "التحقق من صحة البنود المحددة".
20. انقر فوق "موافق".
21. انقر فوق "ترحيل".
22. انقر فوق "موافق".

## <a name="view-trade-agreements-for-a-product"></a>عرض اتفاقيات التجارة لأحد المنتجات
1. انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.
2. في القائمة، ابحث عن المنتج الذي قمت بتحديث سعره للتو ثم حدده.
3. في جزء الإجراءات، انقر فوق "بيع‬".
4. انقر فوق "عرض اتفاقيات التجارة".
    * راجع تفاصيل اتفاقية التجارة للسعر التي قمت بإنشائها.    
5. قم بإغلاق الصفحة.


