---
title: "مطابقة فاتورة الحسابات الدائنة"
description: "مطابقة فاتورة الحسابات الدائنة هي عبارة عن عملية مطابقة فاتورة المورّد وأمر الشراء ومعلومات إيصال استلام المنتجات."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 8d4f84df5722aaff5589cb30314657578fec964f
ms.lasthandoff: 03/31/2017


---

# <a name="accounts-payable-invoice-matching"></a>مطابقة فاتورة الحسابات الدائنة

مطابقة فاتورة الحسابات الدائنة هي عبارة عن عملية مطابقة فاتورة المورّد وأمر الشراء ومعلومات إيصال استلام المنتجات.

عند مطابقة المستندات، تسمى الفروق بين هذه المستندات اختلافات في المطابقة. تتم مقارنة الاختلافات في المطابقة مع التفاوتات المحددة. إذا تجاوز اختلاف في المطابقة النسبة المئوية للتفاوت أو المبلغ، فستظهر أيقونات الفرق في المطابقة‬ في صفحة فاتورة المورّد وفي صفحة تفاصيل مطابقة ومحفوظات الفاتورة. 

على سبيل المثال، تقوم بإدخال أمر شراء ذي صنف بند واحد لعدد 1000 بطارية بسعر 1.00 لكل بطارية. يتم اعتماد أمر الشراء وإرساله إلى المورّد. ويقوم المورّد بشحن 1000 بطارية، ثم تقوم بإدخال إيصال استلام منتج لعدد 1000 بطارية بسعر 1.00 لكل بطارية. ويتم تحديث تكلفة المخزون للبطاريات بهذا السعر. 

تصل فاتورة لعدد 1000 بطارية بسعر 1.10 لكل بطارية. ويتيح نهج كيانك القانوني تفاوتًا بصافي سعر وحدة بنسبة 5 بالمائة لفئة الصنف هذه. فيُمكن قبول سعر 1.05، ًولكن 1.10 سيكون غير مقبول. عندما تقوم بإدخال معلومات الفاتورة، يحدد  وجود اختلاف في مطابقة السعر وأنه يُمكنك حفظ الفاتورة إلى أن يتم حل الاختلاف.

يمكنك استخدام الأنواع التالية من مطابقة فاتورة الحسابات الدائنة:

-   مطابقة إجماليات الفواتير – مطابقة المبالغ الإجمالية في الفاتورة بالمبالغ الإجمالية في أمر الشراء. ويتضمن هذا النوع من مطابقة الفاتورة أقل قدر من التفصيل، حيث يمكنك استخدام هذا الخيار لإعداد عناصر التحكم التي تقلل من وقت الموظفين المطلوب لمراجعة معلومات مطابقة الفاتورة.
-   المطابقة الثنائية - مطابقة معلومات السعر في الفاتورة بمعلومات السعر في أمر الشراء.
-   المطابقة الثلاثية - مطابقة معلومات السعر في الفاتورة بمعلومات السعر في أمر الشراء. قم أيضًا بمطابقة معلومات الكمية في الفاتورة بمعلومات الكمية في إيصالات استلام المنتجات التي يتم تحديدها للفاتورة.
-   مطابقة المصاريف - مطابقة معلومات المصاريف (المبالغ) في الفاتورة بمعلومات المصاريف (المبالغ) في أمر الشراء.

> [!NOTE]
> يمكن إكمال نماذج أخرى للتحقق من صحة الفواتير باستخدام سياسات فاتورة المورِّد. 

تقوم المطابقة الثنائية والثلاثية دائمًا بمطابقة معلومات الأسعار بسعر الوحدة. كما يمكنك تكوين سياسات المطابقة هذه لمطابقة معلومات الأسعار بإجمالي السعر.
-   مطابقة صافي سعر الوحدة - مطابقة معلومات الأسعار للمطابقة الثنائية أو المطابقة الثلاثية من خلال مقارنة صافي سعر الوحدة لكل بند في الفاتورة بصافي وحدة السعر المقابل في أمر الشراء. يتم تحديد صافي سعر الوحدة بالمعادلة التالية: صافي مبلغ البند / كمية البند
-   مطابقة إجماليات الأسعار - مطابقة معلومات الأسعار للمطابقة الثنائية أو المطابقة الثلاثية من خلال مقارنة صافي المبلغ (إجمالي السعر) لكل بند في الفاتورة بصافي المبلغ المقابل في أمر الشراء. المبلغ الصافي تحدد بواسطة الصيغة التالية: (سعر الوحدة \*خطية الكمية) + مصاريف البند-خط الخصومات

عادةً ما يتم تنفيذ العمليات الحسابية لمطابقة الفواتير تلقائياً عندما تقوم بتحرير فواتير المورد في صفحة فاتورة المورد. وبدلاً من ذلك، مطابقة الفاتورة تتم حسب الطلب، حسب الحاجة. يتم التحكم مطابقة الفاتورة على الطلب للكيان القانوني بتحديث الحالة رأس الفاتورة للحسابات الدائنة معلمات صفحة علامة التبويب التحقق من صحة الفواتير تلقائياً. كما يمكن إجراء مطابقة الفاتورة كجزء من عملية استعراض الفاتورة. يمكنك عرض نتائج مطابقة الفاتورة في صفحة فاتورة المورد وصفحات مطابقة الفاتورة ذات الصلة.

## <a name="invoice-totals-matching"></a> مطابقة إجماليات الفواتير
يمكنك استخدام مطابقة إجماليات الفواتير للمساعدة على التأكد من أن مبالغ الفواتير الإجمالية لا تحيد عن المبالغ المتوقعة بما يزيد على فرق مقبول. وتتم مقارنة ستة إجماليات في صفحة تفاصيل مطابقة إجماليات الفواتير، كما هو موضح في الجدول التالي. إذا كان الاختلاف المسموح به لمطابقة إجماليات الفاتورة 20%، تعتبر نسبة الفرق 100% لإجمالي مبلغ الخصم اختلاف مطابقة.

| حقل الإجمالي    | إجمالي الفاتورة الفعلي | إجمالي الفاتورة المتوقع | النسبة المئوية للفروق | حالة المطابقة |
|----------------|----------------------|------------------------|---------------------|--------------|
| الرصيد        | 495.00               | 495.00                 | 0%                  | تم الاجتياز       |
| الخصم الإجمالي | 0.00                 | 9.90                   | 100%                | فشل       |
| المصاريف        | 64.90                | 64.90                  | 0%                  | تم الاجتياز       |
| ضريبة المبيعات      | 139.98               | 137.50                 | 2%                  | تم الاجتياز       |
| تقريب العلامات العشرية      | 0.00                 | 0.00                   | 0%                  | تم الاجتياز       |
| مبلغ الفاتورة | 699.88               | 687.50                 | 2%                  | تم الاجتياز       |

يتم التحكم في مطابقة إجماليات الفواتير للكيان القانوني بخيار تبديل مطابقة إجماليات الفواتير في صفحة معلمات الحسابات الدائنة. ويتم إجراء المطابقة على إجماليات الفواتير المتوقعة وإجماليات الفواتير الفعلية. إجماليات الفاتورة المتوقع تُحسب على أساس الأسعار والتكاليف، ومعلومات ضريبة المبيعات من أمر الشراء والكميات من الفاتورة.

## <a name="two-way-price-totals-matching"></a> المطابقة الثنائية لإجماليات الأسعار
استخدم المطابقة الثنائية للمساعدة في التأكد من وجود فرق بين معلومات السعر في أمر الشراء والفاتورة الموجودة في نطاق الفروق المقبولة. ويمكنك مقارنة معلومات السعر للمبلغ الصافي لكل بند في الفاتورة وكافة بنود الفاتورة المعلقة والتي تم ترحيلها سابقًا، مع المبلغ الصافي لبند أمر الشراء المناظر. يسمى هذا بمطابقة إجماليات الأسعار. 

ومطابقة إجماليات السعر يمكن أن تستند إلى نسبة أو مبلغ أو نسبة مئوية أو مبلغ. 

وإذا تم تحديد النسبة المئوية لتفاوت إجمالي سعر الشراء، فإنه تتم مقارنة الحقول الخمسة، كما هو موضح في الجدول التالي. ونظراً لأن نسبة تفاوت إجمالي سعر الشراء 10%، تمثل نسبة النسبة المئوية لفرق إجمالي السعر البالغة 50% اختلاف مطابقة.

| حالة المطابقة | المبلغ الصافي الفاتورة | المبلغ الصافي المتوقع | إجمالي سعر الشراء غير المتطابق (مبلغ الفرق) | النسبة المئوية لإجمالي سعر الشراء غير المتطابق (نسبة الفرق) | نسبة تفاوت إجمالي سعر الشراء |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| تم الاجتياز       | 105.00             | 100.00              | 5.00                                             | 5%                                                              | 10%                                    |
| فشل       | 150.00             | 100.00              | 50.00                                            | 50%                                                             | 10%                                    |

وإذا تم تحديد مبلغ تفاوت إجمالي سعر الشراء، فإنه تتم مقارنة الحقول الخمسة، كما هو موضح في الجدول التالي. ونظراً لأن مبلغ تفاوت إجمالي سعر الشراء 100.00، يمثل مبلغ فرق إجمالي السعر البالغ 105.00 اختلاف مطابقة.

| حالة المطابقة | المبلغ الصافي الفاتورة | المبلغ الصافي المتوقع | إجمالي سعر الشراء غير المتطابق (مبلغ الفرق) | إجمالي سعر الشراء غير المتطابق بعملة المحاسبة (مبلغ الفرق) | تفاوت إجمالي سعر الشراء |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| تم الاجتياز       | 150.00             | 100.00              | 50.00                                            | 50.00                                                                   | 100.00                         |
| فشل       | 205.00             | 100.00              | 105.00                                           | 105.00                                                                  | 100.00                         |

إذا تم إعداد مطابقة إجماليات الأسعار مع تفاوت النسبة المئوية ومبلغ تفاوت، فإنه يُشار إليه أحياناً بعدم تجاوز المبلغ، وتتم مراعاة كلا التفاوتين عند تقييم ما إذا كان بند يحتوي على اختلاف مطابقة. أما إذا كانت النسبة المئوية أو المبلغ يتجاوز التفاوت، كما هو موضح في بنود 150.00 و205.00 في الجدول التالي، فإن البند يشتمل على اختلاف مطابقة.

| حالة المطابقة | المبلغ الصافي الفاتورة | المبلغ الصافي المتوقع | النسبة المئوية لإجمالي سعر الشراء غير المتطابق (نسبة الفرق) | نسبة تفاوت إجمالي سعر الشراء | إجمالي سعر الشراء غير المتطابق بعملة المحاسبة (مبلغ الفرق) | تفاوت إجمالي سعر الشراء |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| تم الاجتياز       | 105.00             | 100.00              | 5%                                                              | 10%                                    | 5.00                                                                    | 100.00                         |
| فشل       | 150.00             | 100.00              | 50%                                                             | 10%                                    | 50.00                                                                   | 100.00                         |
| فشل       | 205.00             | 100.00              | 105%                                                            | 10%                                    | 105.00                                                                  | 100.00                         |

يتم التحكم في المطابقة الثنائية للكيان القانوني بواسطة حقل "سياسة مطابقة البند" في صفحة معلمات الحسابات الدائنة. وبناءً على التحديد في حقل السماح بتجاوز سياسة المطابقة، يمكنك تحديد المطابقة الثنائية لمورد أو صنف أو مجموعة صنف ومورد محددة في صفحة سياسة المطابقة، ولأمر شراء محدد في صفحة أمر الشراء.

ويتم التحكم في مطابقة إجماليات الأسعار للكيان القانوني بواسطة حقل مطابقة إجماليات الأسعار في صفحة معلمات الحسابات الدائنة. كما يتم تحديد النسبة المئوية لتفاوت إجمالي سعر الشراء ومبلغ التفاوت (عدم تجاوز المبلغ) في هذه الصفحة.

## <a name="two-way-net-unit-price-matching"></a> المطابقة الثنائية لصافي سعر الوحدة
استخدم المطابقة الثنائية للمساعدة في التأكد من وجود فرق بين معلومات السعر في أمر الشراء والفاتورة الموجودة في نطاق الفروق المقبولة. يمكنك مقارنة معلومات السعر الخاصة بصافي سعر الوحدة لكل صنف في الفاتورة. ويُسمى هذا بمطابقة صافي سعر الوحدة. 

وتتم مقارنة تسعة مبالغ بنود في صفحة تفاصيل مطابقة الفواتير، كما هو موضح في الجدول التالي. إذا كان تفاوت الأسعار المسموح لمطابقة صافي سعر الوحدة هو 10%، تعتبر نسبة الفرق 22.61% لصافي مبلغ الوحدة اختلاف مطابقة.

| حقل البند                    | قيمة الفاتورة | قيمة أمر الشراء | النسبة المئوية للفروق | حالة المطابقة |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| سعر الوحدة                    | 55.40         | 55.38                | 0%                  | تم الاجتياز       |
| وحدة السعر                    | 1.00          | 1.00                 | 0%                  | تم الاجتياز       |
| تكاليف المشتريات          | 50.00         | 0.00                 | 100%                | فشل       |
| الخصم                      | 0.00          | 0.00                 | 0%                  | تم الاجتياز       |
| نسبة الخصم              | 0.00          | 0.00                 | 0%                  | تم الاجتياز       |
| خصم متعدد الأسطر            | 0.00          | 0.00                 | 0%                  | تم الاجتياز       |
| نسبة خصم متعددة الأسطر | 0.00          | 0.00                 | 0%                  | تم الاجتياز       |
| صافي المبلغ                    | 271.60        | 221.52               | 22.61%              | فشل       |
| صافي سعر الوحدة                | 67.9000       | 55.3800              | 22.61%              | فشل       |

يتم التحكم في المطابقة الثنائية للكيان القانوني بواسطة حقل "سياسة مطابقة البند" في صفحة معلمات الحسابات الدائنة. وبناءً على التحديد في حقل السماح بتجاوز سياسة المطابقة، يمكنك تحديد المطابقة الثنائية لمورد أو صنف أو مجموعة صنف ومورد محددة في صفحة سياسة المطابقة، ولأمر شراء محدد في صفحة أمر الشراء. 

ويتم التحكم في مطابقة صافي سعر الوحدة للكيان القانوني بواسطة حقل تمكين التحقق من صحة مطابقة الفاتورة‬ في صفحة معلمات الحسابات الدائنة. ويمكن تكوين النسبة المئوية لتفاوت صافي سعر الوحدة للأصناف، أو مجموعات الأصناف، أو الموردين، أو مجموعات الموردين، أو مجموعات الأصناف والموردين، أو الكيان القانوني باستخدام صفحة تفاوتات الأسعار.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a> المطابقة الثنائية، ومطابقة إجماليات الأسعار، ومطابقة صافي سعر الوحدة
يمكنك استخدام مطابقة إجماليات الأسعار ومطابقة صافي سعر الوحدة معًا. يفترض هذا المثال التكوين التالي:

-   تفاوت صافي سعر الوحدة لصنف محرك أقراص USB هو 10%.
-   تفاوت مطابقة إجماليات الأسعار للكيان القانوني هو 15% أو 500.00.

يحتوي أمر الشراء على البند التالي.

| رقم العنصر | الكمية | سعر الوحدة | صافي المبلغ |
|-------------|----------|------------|------------|
| محرك USB   | 1,000    | 10.00      | 10,000.00  |

يتم إدخال الفواتير الثلاث، كما هو موضح في الجدول التالي. يوجد اختلاف مطابقة فواتير للفاتورة 3 نظراً لأن الفرق البالغ 1,880.00 يتجاوز مبلغ تفاوت إجماليات أسعار الشراء البالغ 500.00. ولمطابقة إجماليات الأسعار، يتضمن صافي مبلغ الفاتورة كافة الفواتير التي تم ترحيلها مسبقاً بالإضافة إلى الفاتورة التي تعمل حاليًا فيها.

| رقم العنصر          | الكمية | سعر الوحدة | صافي المبلغ | مطابقة السعر | مطابقة إجمالي السعر |
|----------------------|----------|------------|------------|-------------|-------------------|
| الفاتورة 1: محرك أقراص USB | 800      | 10.80      | 8,640.00   | تم الاجتياز      | تم الاجتياز            |
| الفاتورة 2: محرك أقراص USB | 100      | 10.80      | 1,080.00   | تم الاجتياز      | تم الاجتياز            |
| الفاتورة 3: محرك أقراص USB | 200      | 10.80      | 2,160.00   | تم الاجتياز      | فشل            |
| الإجمالي                |          |            | 11,880.00  |             |                   |

## <a name="three-way-matching"></a>سياسة المطابقة الثلاثية

استخدم المطابقة الثلاثية للمساعدة على التأكد من وجود فرق بين معلومات الأسعار في أمر الشراء والفاتورة في نطاق التفاوتات مقبولة، والتأكد من أن الكمية الموجودة في الفاتورة تتطابق مع الكمية الموجودة على إيصالات استلام المنتج.

وتتم مقارنة نفس مبالغ البند في صفحة تفاصيل مطابقة الفواتير، كما هو الحال بالنسبة للمطابقة الثنائية. بالإضافة إلى ذلك، تتم مطابقة الكمية الموجودة في الفاتورة بكميات الموجودة في إيصال استلام المنتج والتي تم استلامها. إذا كانت كمية الفاتورة تختلف عن كمية إيصال المنتجات المتطابقة، فإنه يوجد خطأ في مطابقة الكمية.

| حقل البند                    | قيمة الفاتورة | قيمة أمر الشراء | النسبة المئوية للفروق | حالة المطابقة |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| سعر الوحدة                    | 55.40         | 55.38                | 0%                  | تم الاجتياز       |
| وحدة السعر                    | 1.00          | 1.00                 | 0%                  | تم الاجتياز       |
| تكاليف المشتريات          | 50.00         | 0.00                 | 100%                | فشل       |
| الخصم                      | 0.00          | 0.00                 | 0%                  | تم الاجتياز       |
| نسبة الخصم              | 0.00          | 0.00                 | 0%                  | تم الاجتياز       |
| خصم متعدد الأسطر            | 0.00          | 0.00                 | 0%                  | تم الاجتياز       |
| نسبة خصم متعددة الأسطر | 0.00          | 0.00                 | 0%                  | تم الاجتياز       |
| صافي المبلغ                    | 271.60        | 221.52               | 22.61%              | فشل       |
| صافي سعر الوحدة                | 67.9000       | 55.3800              | 22.61%              | فشل       |

| حقل البند                     | قيمة الفاتورة | حالة المطابقة |
|--------------------------------|---------------|--------------|
| كمية الفواتير               | 4.00          |              |
| إجمالي عدد إيصالات استلام المنتجات غير المتطابقة | 0.00          | فشل       |

يتم التحكم في المطابقة الثلاثية للكيان القانوني بواسطة حقل "سياسة مطابقة البند" في صفحة معلمات الحسابات الدائنة. وبناءً على التحديد في حقل السماح بتجاوز سياسة المطابقة، يمكنك تحديد المطابقة الثلاثية لمورد أو صنف أو مجموعة صنف ومورد محددة في صفحة سياسة المطابقة، ولأمر شراء محدد في صفحة أمر الشراء.

## <a name="charges-matching"></a> مطابقة المصروفات
يمكنك استخدام مطابقة المصاريف للمساعدة على التأكد من أن مبالغ المصاريف لا تحيد عن المبالغ المتوقعة بما يزيد على نسبة فرق مقبول. تتم مقارنة المبالغ الإجمالية لكل كود المصاريف التي تنطبق على أمر الشراء والفاتورة في قيم التكاليف المقارنة-الفاتورة: الصفحة، كما هو موضح في الجدول التالي. إذا كان التفاوت المسموح به لكود المصاريف هو 25%، تعتبر نسبة الفرق 99,999,999,999.99% لكود مصاريف الترخيص اختلاف مطابقة.

> [!NOTE] 
> تعني نسبة الفرق 99,999,999,999.99% أن المبلغ المتوقع استناداً إلى أمر الشراء هو صفر والمبلغ الفعلي في الفاتورة هو قيمة موجبة. 

| حالة مطابقة المصاريف | كود تكاليف الفاتورة | إجمالي القيمة المحسوبة الفعلية | إجمالي القيمة المحسوبة المتوقعة | مبلغ نسبة الفرق | النسبة المئوية للفروق | النسبة المئوية للاختلاف |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| فشل               | الترخيص              | 25                            | 0                               | 25              | 99,999,999,999.99%  | 25%                  |
| تم الاجتياز               | الشحن              | 200                           | 200                             | 0               | 0%                  | 25%                  |
| فشل               | تعجيل             | 4                             | 2                               | 2               | 100%                | 25%                  |

يتم التحكم في مطابقة المصاريف للكيان القانوني بخيار تبديل مطابقة المصاريف في صفحة معلمات الحسابات الدائنة. يمكنك إعداد النسب المئوية لتفاوت الفرق للمصاريف في صفحة تفاوتات المصاريف.

> [!NOTE]
> يتم إجراء مطابقة المصاريف فقط في أكواد المصاريف التي يتم لها تحديد خيار تبديل مقارنة قيم أمر الشراء والفاتورة في صفحة كود المصاريف.

## <a name="related-functionality"></a> الوظائف ذات الصلة
تعتمد فواتير المورّد غالبًا على إيصالات استلام المنتجات التي تُمثل الشحنات الفعلية، بدلاً من أوامر الشراء. ففي بعض الأحيان لا تطابق المبالغ المفوترة مبالغ أمر الشراء، ولا تتوافق الكميات المشحونة مع الكميات المفوترة. يمكنك المساعدة في إدارة هذه المعلومات بالطرق التالية:
-   إنشاء فاتورة مورد على أساس إيصالات استلام المنتجات. ويتم اقتراح إيصالات استلام المنتجات تلقائيًا للفواتير، ويُمكنك تحديد إيصالات استلام المنتجات لاستخدامها. كما يمكنك أيضًا أصناف بنود إيصالات استلام المنتجات المحددة من أوامر الشراء المتعددة، إذا لزم الأمر.
-   عرض فروق الكمية بين الكمية المفوترة في الفاتورة والكمية المستلمة في إيصال استلام المنتج واعتمادها. وفي حالة وجود فروق، يُمكنك حفظ الفاتورة ومطابقتها بإيصال استلام منتج مختلف في وقتٍ لاحق أو تغيير كمية الفاتورة لتتطابق مع الكمية المستلمة.
-   إدخال مبالغ الفاتورة التي لم يتم تضمينها في أمر الشراء الأصلي، بحيث تتطابق معلومات الفاتورة مع الفاتورة التي تسلمتها من المورّد. يُمكنك مقارنة المصاريف لأوامر الشراء بمصاريف الفواتير. وإذا لزم الأمر، يُمكنك إضافة المصاريف إلى الفواتير وتخصيصها إلى بنود الفاتورة.
-   عرض اختلافات مطابقة السعر بين صافي سعر وحدة الفاتورة وصافي سعر وحدة أمر الشراء واعتمادها. يُمكنك إعداد النسب المئوية لتفاوتات الأسعار للكيانات القانونية، والموردين، والأصناف. وإذا لم يقع سعر بند فاتورة المورد داخل نطاق تفاوت السعر المقبول، فيُمكنك حفظ الفاتورة إلى أن يتم اعتمادها للترحيل أو حتى تتسلم تصحيحًا من المورّد.

لمزيد من المعلومات، راجع [سياسات مطابقة ثلاثية](three-way-matching-policies.md).


