--- 
title: "تحديد عمليات جرد المخزون"
description: "ينقلك هذا الإجراء عبر تكوين عمليات جرد المخزون الأساسي عن طريق إنشاء مجموعة جرد ودفتر يومية جرد."
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c14c846c55a3d821945160835817cd4f467deda9
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="define-inventory-counting-processes"></a>تحديد عمليات جرد المخزون

[!include [task guide banner](../../includes/task-guide-banner.md)]

ينقلك هذا الإجراء عبر تكوين عمليات جرد المخزون الأساسي عن طريق إنشاء مجموعة جرد ودفتر يومية جرد. كما يوضح لك كيفية تمكين سياسات الجرد على مستوى الصنف والمستودع. وعادة ما تُنفذ هذه المهام عن طريق مشرف المستودع. من الضروري وجود بعض المنتجات الموجودة التي تم إصدارها بالإضافة إلى المستودعات. إذا كنت تستخدم شركة عرض توضيحي للبيانات، فيمكنك تنفيذ هذا الإجراء في شركة USMF مع أي صنف مخزّن.


## <a name="create-a-counting-group"></a>إنشاء مجموعة جرد
1. انتقل إلى إدارة المخزون > إعداد > المخزون > مجموعات الجرد.
2. انقر فوق "جديد".
3. في الحقل "مجموعة الجرد"، اكتب قيمة.
4. في حقل "الاسم"، اكتب قيمة.
5. في الحقل "كود الجرد"، حدد خيارًا.
    * يدوي – يحتوي على بنود في كل مرة تقوم فيها بتشغيل الوظيفة. وبعبارة أخرى، أنت تقرر الفاصل الزمني للجرد لمجموعة الجرد.  فترة – يتضمن بنودًا للفترة في دفتر يومية الجرد عندما تنتهي صلاحية الفاصل الزمني.   رصيد المخزن صفر‬ – في حالة وصول المخزون الفعلي إلى الصفر (0)، يتم إنشاء البنود في دفتر يومية الجرد عندما يتم تشغيل الوظيفة. إذا وصل المخزون الفعلي إلى 0 بعد جرد، فسيتم إنشاء بنود في المرة التالية التي تقوم فيها ببدء الجرد.   الحد الأدنى - يدرج البنود في دفتر يومية الجرد إذا كان المخزون الفعلي يساوي الحد الأدنى المحدد أو أقل منه.  
    * اختياري: إذا قمت بتحديد "الفترة" في الحقل "كود الجرد"، يجب كتابة الفاصل الزمني الخاص بالفترة في الحقل "فترة الجرد". وحدة الفواصل الزمنية هي الأيام.  
    * عند تشغيل الوظيفة لإنشاء بنود جديدة في دفتر يومية الجرد، يتم إنشاء بنود جديدة عند الفاصل الزمني المحدد في هذا الحقل، بغض النظر عن عدد مرات تشغيل نفس الوظيفة. على سبيل المثال، إذا تم تعيين فترة الجرد إلى 7 وتم توليد بنود دفتر اليومية لعملية جرد في المرة الأخيرة في الأول من يناير، وإذا بدأت وظيفة أخرى في 5 يناير، فلم تمر سبعة أيام وبالتالي لم يتم توليد اي بنود في دفتر اليومية لتلك الفترة الزمنية. إذا بدأت الوظيفة من جديد في 8 يناير، فسيتم إنشاء البنود للفترة الزمنية في دفتر يومية الجرد بسبب مرور 7 أيام.  
6. انقر فوق "حفظ".

## <a name="create-a-counting-journal-name"></a>إنشاء اسم دفتر يومية جرد
1. انتقل إلى إدارة المخزون > إعداد > أسماء دفاتر اليومية > المخزون.
2. انقر فوق "جديد".
3. في حقل "الاسم"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. في الحقل "نوع دفتر اليومية"، حدد "الجرد‬".
    * اختياري: يمكنك تحديد معرف مختلف لمسلسل الإيصال‬ إذا كنت تريد الحصول على تسلسل رقمي محدد لمعرفات الإيصالات التي تم إنشاؤها عند إنشاء دفاتر يومية الجرد. يتم إنشاء مسلسلات الإيصالات في صفحة "التسلسلات الرقمية‬".  
6. في الحقل "مستوى التفاصيل‬"، حدد خيارًا.
    * هذا هو مستوى التفاصيل الذي يتم تطبيقه عند ترحيل دفتر اليومية.  
    * اختياري: يمكنك تغيير القيمة في الحقل "الحجز‬". هذا هو الأسلوب المستخدم لحجز الأصناف أثناء الجرد.   
    * يدوي – يتم حجم الأصناف يدويًا في نموذج الحجز.   تلقائي – يتم حجز كمية الأمر من المخزون الفعلي المتوفر للصنف.   تحديد إجمالي المكونات المطلوبة‬ – يشكل الحجز‬ جزءًا من التخطيط الرئيسي للحركة.  
7. انقر فوق "حفظ".

## <a name="set-standard-counting-journal-name"></a>تعيين اسم دفتر يومية جرد قياسي
1. انتقل إلى إدارة المخزون > الإعداد > معلمات إدارة المستودعات والمخزون‬.
2. انقر فوق علامة تبويب "دفاتر اليومية".
3. في الحقل "الجرد"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. حدد دفتر اليومية الذي أنشأته في وقت سابق.
    * سيكون دفتر اليومية هذا عندئذٍ اسم دفتر اليومية الافتراضي لدفاتر يومية المخزون من النوع "جرد".  
5. انقر فوق علامة التبويب "عام".
    * اختياري: حدد هذا الخيار لتأمين صنف أثناء عملية الجرد لمنع إجراء أي تحديثات لإيصالات التعبئة أو قوائم الانتقاء أو تسجيلات قوائم الانتقاء.  

## <a name="set-the-counting-policy-for-an-item"></a>تعيين سياسة الجرد لصنف
1. انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.
2. في القائمة، انقر فوق الارتباط الخاص برقم الصنف للمنتج الذي تريد تعيين سياسات جرد له.
    * لاحظ أنك تحتاج إلى تحديد صنف يتم تعقبه في المخزون. لا يمكن جرد منتج غير مخزّن. إذا كنت تستخدم بيانات العرض التوضيحي USMF، فيمكنك تحديد الصنف A0001.  
3. انقر فوق "تحرير".
4. قم بتبديل توسيع المقطع "إدارة المخزون".
5. في الحقل "مجموعة الجرد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
6. في القائمة، انقر فوق مجموعة الجرد التي قمت بإنشائها مسبقًا.
    * سيتم تضمين هذا المنتج الآن عندما يتم إنشاء بنود دفتر يومية جرد المخزون باستخدام مجموعة الجرد هذه.  
7. انقر فوق "حفظ".

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>تعيين سياسة الجرد لصنف في مستودع معين
1. في جزء الإجراءات‬، انقر فوق "إدارة المخزون".
2. انقر فوق "أصناف المستودع".
3. انقر فوق جديد.
4. في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.
5. في القائمة، حدد المستودع الذي تريد إعداد سياسات جرد معينة له.
6. في الحقل "مجموعة الجرد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
7. في القائمة، حدد مجموعة جرد.
    * هنا يمكنك تحديد مجموعة جرد محددة يجب أن تنطبق على الصنف في المستودع المعين الذي حددته. عندما يتم تنفيذ الجرد في هذا المستودع، ستتجاوز سياسة الجرد هذه سياسة الجرد العامة لهذا الصنف.  
8. انقر فوق "حفظ".


