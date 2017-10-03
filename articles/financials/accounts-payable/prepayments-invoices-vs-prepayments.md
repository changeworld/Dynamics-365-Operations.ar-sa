---
title: "فواتير الدفع المسبق مقابل الدفعات المقدمة"
description: "توفر هذه المقالة وصفًا ومقارنة للأسلوبين اللذين يمكن للمؤسسات استخدامهما للدفعات المقدمة (الدفعات المسبقة). في أحد هذين الأسلوبين، يجب عليك إنشاء فاتورة الدفعة المقدمة المقترنة بأمر شراء. أما في الأسلوب الآخر، فيمكنك إنشاء إيصالات يومية دفعات مقدمة عن طريق إنشاء إدخالات دفتر اليومية ووضع علامة عليها كإيصالات يومية دفعات مقدمة."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c4f127007cea1d8ccd0b4e9ea637f0674775278d
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017

---

# <a name="prepayment-invoices-vs-prepayments"></a>فواتير الدفع المسبق مقابل الدفعات المقدمة

[!include[banner](../includes/banner.md)]


توفر هذه المقالة وصفًا ومقارنة للأسلوبين اللذين يمكن للمؤسسات استخدامهما للدفعات المقدمة (الدفعات المسبقة). في أحد هذين الأسلوبين، يجب عليك إنشاء فاتورة الدفعة المقدمة المقترنة بأمر شراء. أما في الأسلوب الآخر، فيمكنك إنشاء إيصالات يومية دفعات مقدمة عن طريق إنشاء إدخالات دفتر اليومية ووضع علامة عليها كإيصالات يومية دفعات مقدمة.

قد تصدر المؤسسات الدفعات المقدمة (المبالغ المدفوعة مقدمًا) للموردين مقابل البضائع أو الخدمات قبل استيفاء تلك البضائع أو الخدمات. ويمكن استخدام أسلوبين لإصدار الدفعات المقدمة للموردين. ولتقليل المخاطر، يمكنك تتبع الدفعات المقدمة من خلال تحديد الدفعة المقدمة في أمر شراء. وبالنسبة لهذا الأسلوب، يجب عليك إنشاء فاتورة الدفعة المقدمة المقترنة بأمر شراء. ويُشار إلى هذا الأسلوب باعتباره فوترة دفعة مقدمة. وتستطيع المؤسسات، التي لا ترغب في تعقب الدفعات المقدمة عن قرب أو لا تتلقي فاتورة دفعة مقدمة من المورد، استخدام إيصالات دفتر يومية الدفعة المقدمة بدلاً من أسلوب فوترة الدفعة المقدمة. ويمكنك إنشاء إيصالات دفتر يومةي الدفعات المقدمة عن طريق إنشاء إدخالات دفتر اليومية ووضع علامة عليها كإيصالات دفتر يومية دفعات مقدمة. وبالنسبة لهذا الأسلوب، لا يمكنك تتبع الدفعات المقدمة التي يتم إجراؤها في مقابل أوامر الشراء. ومع ذلك، يمكنك وضع علامة على دفعة مقدمة تم ترحيلها للتسوية مقابل أمر شراء.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>متى يمكن استخدام فوترة الدفعة المقدمة مقابل الدفعات المقدمة
| فوترة الدفعات المقدمة                                                                | دفعات مقدمة                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| تحديد قيمة الدفعة المقدمة في أمر الشراء.                                    | لا يتم تحديد أي قيمة دفعة مقدمة في أمر الشراء.                    |
| العامل الأساسي: يجب ترحيل فاتورة الدفعة المقدمة وفاتورة نهائية.                       | يجب ألا يتم ترحيل أي فاتورة للدفعة المقدمة.                                    |
| يتم الاحتفاظ بالالتزام الخاص بالدفعة المقدمة في حساب الدفعات المقدمة، وليس حساب الحسابات الدائنة. | يتم الاحتفاظ بالالتزام الخاص بالدفعة المقدمة في حساب الحسابات الدائنة.                  |
| لا يعكس رصيد المورد قيمة الدفعة المقدمة خلال العملية.     | يعكس رصيد المورد قيمة الدفعة المقدمة خلال العملية. |
| تتوفر فوترة الدفعات المقدمة في الحسابات الدائنة فقط.                         | تتوفر الدفعات المقدمة في الحسابات المدينة والحسابات الدائنة.    |

## <a name="overview-of-the-prepayment-process"></a>نظرة عامة على عملية الدفع المسبق
تتطلب ممارسات المحاسبة في العديد من البلدان/المناطق ألا يتم ترحيل الدفعات المقدمة من عميل أو إلى مورّد إلى حسابات ملخصة معتادة للعميل أو المورّد. فبدلاً من ذلك، يتم ترحيل هذه المدفوعات إلى حسابات دفتر أستاذ خاصة للدفعات المقدمة. وعند إنشاء أمر توريد أو أمر شراء، يتم إصدار فاتورة إلى العميل أو من المورد. وأثناء دفع الفاتورة، يتم إلغاء إيصال الدفعة المقدمة والدفعة المقدمة لضريبة المبيعات في حسابات دفتر الأستاذ للدفعة المقدمة، كما يتم ترحيل مبالغ الفاتورة تلقائيًا إلى حسابات ملخصة معتادة. اتبع هذه الخطوات لإنشاء دفعة مقدمة.

1.  قم بإعداد ملفات تعريف الترحيل للدفعات المقدمة.
2.  في معلمات الحسابات المدينة والحسابات الدائنة، ضمن **دفتر الأستاذ وضريبة المبيعات**، حدد ملف تعريف الترحيل الجديد باستخدام معلمة **ترحيل ملف تعريف لدفتر يومية الدفع بالدفعة المقدمة**.
3.  أنشئ دفتر يومية الدفعات، ثم أنشئ الدفعة الجديدة.
4.  يمكنك وضع علامة على الدفع كدفعة مقدمة. في حالة وضع علامة على دفعة كدفعة مقدمة، يتم ترحيل هذه الدفعة إلى حسابات دفتر الأستاذ التي يتم تحديدها في ملف تعريف الترحيل الذي تقوم بإعداده في الخطوتين 1 و2. بالإضافة إلى ذلك، في حالة وضع علامة على الدفعة كدفعة مقدمة، يتم حساب الضرائب. تتطلب بعض الحكومات أن يتم دفع الضرائب عند تسجيل دفعة مقدمة، حتى إذا لم تكن هناك فاتورة.
5.  قم بترحيل الدفعة المقدمة.
6.  ‏‫اختياري: يمكن تسوية الدفعة المقدمة مقابل أمر الشراء أو أمر التوريد قبل إنشاء الفاتورة. وفي صفحة أمر التوريد أو أمر الشراء، في "جزء الإجراءات"، استخدم **تسوية الحركات**.
7.  بعد أن يسلم المورد البضائع أو الخدمات، قم بتسجيل الفاتورة. وإذا قمت بتسوية دفعة مقدمة مقابل أمر الشراء أو أمر المبيعات في الخطوة 6، فإنه تتم تسوية الدفعة المقدمة تلقائياً مقابل الفاتورة التي قمت بإنشائها. وفي حالة عدم تسوية الدفعة المقدمة مقابل أمر الشراء أو أمر التوريد، فيمكنك يدوياً تسويتها مقابل الفاتورة باستخدام **تسوية الحركات** في صفحة العميل أو المورد. ويتم فيما بعد إلغاء مبلغ الدفعة المقدمة من حساب دفتر الأستاذ المؤقت للحسابات الدائنة/الحسابات المدينة. بالإضافة إلى ذلك، إذا تم حساب الضرائب، فإنه يتم إلغاؤها، لأن الفاتورة تتضمن الضرائب الفعلية.

## <a name="overview-of-the-prepayment-invoicing-process"></a>نظرة عامة على عملية فوترة الدفعات المقدمة
فواتير الدفعات المقدمة عبار عن ممارسة أعمال شائعة. يُصدر مورد فواتير الدفعات المقدمة لطلب إيداع خاص بالشراء قبل تنفيذ أمر الشراء. على سبيل المثال، يتطلب بعض الموردين دفعة مقدمة لخدمات أو سلع مخصصة. إذا أصدر مورد فاتورة تتطلب دفعة مقدمة، فيمكنك استخدام ميزة فوترة الدفعات المقدمة. يمكن تحديد قيمة الدفعة مقدمة في أمر الشراء، ويتم تسجيل فاتورة الدفعة المقدمة ودفعها، ثم يتم استخدام فاتورة الدفعة المقدمة في الفاتورة النهائية. اتبع هذه الخطوات لإنشاء دفعة مقدمة.

1.  يقوم وكيل الشراء بإنشاء وتأكيد ثم إرسال أمر شراء طلب المورد دفعة مقدمة له. يتم تحديد قيمة الدفعة المقدمة في أمر الشراء كجزء من الاتفاقية.
2.  يُرسل المورد فاتورة دفعة مقدمة.
3.  يقوم منسق الحسابات الدائنة بتسجيل فاتورة الدفعة المقدمة مقابل أمر الشراء، ثم يتم دفع فاتورة الدفعة المقدمة.
4.  وبعد أن يسلم المورد البضائع أو الخدمات، واستلام فواتير المورد ذات الصلة، يستخدم منسق الحسابات الدائنة مبلغ الدفعة المقدمة التي تم دفعها بالفعل مقابل الفاتورة.
5.  يتولى منسق الحسابات الدائنة دفع وتسوية المبلغ المتبقي من الفاتورة.




