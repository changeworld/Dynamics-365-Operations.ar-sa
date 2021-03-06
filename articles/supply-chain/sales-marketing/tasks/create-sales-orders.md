--- 
title: "إنشاء أوامر التوريد"
description: "يوضح هذا الإجراء كيفية إنشاء أمر مبيعات."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4ccd2c4ace41f07dce14498031e3cc29ecb61b1c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-orders"></a>إنشاء أوامر التوريد

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء أمر مبيعات. يمكنك تنفيذ الإجراء في شركة بيانات العرض التوضيحي USMF. يتم عادة إنشاء أوامر المبيعات بواسطة معالج أمر المبيعات. 




## <a name="enter-sales-order-header-details"></a>إدخال تفاصيل رأس أمر المبيعات
1. انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.
2. انقر فوق "جديد".
3. في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في القائمة، ابحث عن سجل العميل وحدده.
    * لهذا المثال، حدد رقم العميل US-004.  
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
6. انقر فوق "موافق".

## <a name="enter-sales-order-line-details"></a>إدخال تفاصيل بند أمر المبيعات
    * قد تأتي المنتجات التي تبيعها مؤسستك بأشكال مختلفة يتم التمييز بينها من خلال الأبعاد، مثل التكوين واللون والحجم والنمط. علاوةً على ذلك، يمكن إعداد المنتجات لاستخدام أبعاد التخزين، مثل أبعاد الموقع والمستودع والبالتة‬ والرفوف، مثل أرقام المجموعة والأرقام التسلسلية. عندما يتم تعيين هذه الأبعاد، يجب تحديد قيم لهذه الأبعاد في بند الأمر. ولتحسين كفاءة إدخال أمر، قد تحتاج إلى إضافة حقول الأبعاد المناظرة لشبكة الأمر.  
1. انقر فوق بند أمر المبيعات.
2. انقر فوق "الأبعاد".
    * على سبيل المثال، حدد أبعاد اللون والموقع والمستودع. وسوف تظهر الأبعاد التي قمت بتحديدها هنا في شبكة أمر المبيعات. إذا أردت استمرار تحديداتك، فعيّن خيار "حفظ الإعداد" إلى "نعم".   
3. انقر فوق "موافق".
4. في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.
5. لهذا المثال، حدد رقم الصنف T0004.
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * إذا كان الصنف جزءًا من فئة مبيعات، فسيظهر اسم الصنف تلقائيًا في الحقل "فئة المبيعات".  
    * إذا احتوت حقول أبعاد منتج على قيمة، فيعود سبب ذلك إلى نسخ القيمة من سجل المنتج حيث تم تعريفها كبعد منتج افتراضي. يمكن تغيير القيمة الافتراضية في أي وقت.   
7. في الحقل "اللون"، انقر فوق زر القائمة المنسدلة لفتح البحث.
8. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
9. في القائمة، انقر فوق الارتباط في الصف المحدد.
10. في حقل الكمية، أدخل رقمًا.
    * إذا تم بيع الصنف في وحدات مختلفة عند شرائه وإنتاجه وتخزينه، وتم تعيين "وحدة قياس مبيعات" في سجل المنتج، فستظهر هذه القيمة في حقل "الوحدة". يمكنك تغيير القيمة في أي وقت.   
    * إذا احتوى حقل "الموقع" على قيمة، فقد تم نسخ القيمة من رأس الأمر أو من إعدادات الأمر المقترنة بالمنتج. يمكنك تغيير القيمة في أي وقت. إذا كان الحقل فارغًا، فحدد قيمة.   
    * إذا احتوى حقل "سعر الوحدة" على قيمة، فقد تم نسخ القيمة من اتفاقية تجارية صالحة أو من سجل المنتج. (بإمكان سعر الوحدة أن ينشأ أيضًا من اتفاقية بيع، لكن عملية إنشاء أوامر المبيعات من اتفاقيات البيع تختلف عن تلك المعروضة هنا.) إذا كان الحقل فارغًا، فأدخل قيمة.   
    * يحتوي الحقل "الخصم" على مبلغ خصم لكل وحدة منتج. لحساب إجمالي مبلغ خصم البند، يتم ضرب قيمة خصم بكمية بند.    إذا احتوى حقل "الخصم" على قيمة، فقد تم نسخ القيمة من اتفاقية تجارية صالحة. إذا كان الحقل فارغًا، وتريد إعطاء العميل خصم بند، فأدخل قيمة.  
    * يحتوي الحقل "نسبة الخصم" على قيمة النسبة مئوية التي يجب استخدامها لخفض إجمالي مبلغ البند.  إذا احتوى الحقل "نسبة الخصم" على قيمة، فقد تم نسخها من اتفاقية تجارية صالحة. إذا كان الحقل فارغًا، وتريد إعطاء العميل خصم بند، فأدخل قيمة.  
    * يحتوي الحقل "المبلغ الصافي" على قيمة يتم حسابها بناء على كمية البند وسعر الوحدة المعدّل بواسطة الخصومات.  يمكنك تجاوز القيمة المحسوبة إلى أخرى مختلفة.  

## <a name="review-the-order-totals"></a>مراجعة إجماليات الأوامر
1. في جزء "الإجراءات"، انقر فوق "أمر المبيعات".
2. انقر فوق "الإجماليات".
    * تعرض صفحة "الإجماليات" تفاصيل حول الأمر بأكمله. ويشمل ذلك المبلغ الإجمالي الفرعي، وهو مجموع المبالغ الصافية لكل البنود وقد تم تعديله لخصومات البند النهائية، وإجمالي مبلغ الفاتورة، وهو مبلغ مجموع فرعي تم تعديله للخصم النهائي على مستوى الأمر، وضريبة المبيعات وحالة الحد الائتماني للعميل والمزيد.  مبلغ الفاتورة هو المبلغ الذي سيظهر على مستند الفاتورة للعميل.  
3. انقر فوق "موافق".


