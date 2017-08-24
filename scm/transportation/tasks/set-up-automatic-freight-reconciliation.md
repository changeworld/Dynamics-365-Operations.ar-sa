--- 
title: "إعداد تسوية الشحن التلقائية"
description: "يوضح هذا الإجراء كيفية إعداد البيانات لتسوية الشحن التلقائية."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 61b795d52d4d2586db7f42a976790ee8608e179b
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a>إعداد تسوية الشحن التلقائية

[!include[task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إعداد البيانات لتسوية الشحن التلقائية. عادة ما يتم تنفيذ هذه العملية عن طريق مدير المستودع. يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.


## <a name="set-up-the-freight-bill-type"></a>إعداد نوع فاتورة الشحن
1. انتقل إلى إدارة النقل > الإعداد > تسوية الشحن > نوع فاتورة الشحن.
    * يعرف نوع فاتورة الشحن كيف يجب أن تتطابق فواتير الشحن وفواتير شركة النقل.  
2. انقر فوق "جديد".
3. في الحقل "نوع فاتورة الشحن"، اكتب قيمة.
4. في حقل "تجميع المحرك"، اكتب 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.
    * هذه هي إدارة النقل القياسية المطابقة لمكتبة أكواد المحرك.  
5. في حقل "فئة المحرك"، اكتب 'Microsoft.Dynamics.Ax.Tms.dll'.
    * هذه هي إدارة النقل القياسية المطابقة لفئة المحرك.  
6. انقر فوق "جديد".
7. في حقل "الوصف"، اختر القيمة التي يجب أن تتطابق على فاتورة الشحن وفاتورة شركة النقل.  
8. في الحقل "المطابقة مطلوبة"، حدد "نعم".
    * إذا قمت بتعيين هذا الحقل إلى "نعم"، فهذا يعني أن القيمة المحددة في حقل "الوصف" يجب أن تكون مطابقة على كل من فاتورة الشحن وفاتورة شركة النقل. إما إذا قمت بتعيينه إلى "لا"، فبإمكان الحقل أن يكون فارغًا في إحدى القيمتين.  
9. انقر فوق "حفظ".

## <a name="set-up-the-freight-bill-type-assignment"></a>إعداد تعيين نوع فاتورة الشحن
1. قم بإغلاق الصفحة.
2. انتقل إلى إدارة النقل > الإعداد > تسوية الشحن > تعيينات نوع كمبيالة الشحن.
    * يُستخدم تعيين نوع فاتورة الشحن لتحديد نوع فاتورة الشحن المستخدم لشركة معينة.   
3. انقر فوق "جديد".
4. في الحقل "الوضع"، أدخل قيمة أو حددها.
5. في الحقل "شركة الشحن"، أدخل قيمة أو حددها.
6. في الحقل "نوع فاتورة الشحن"، حدد نوع فاتورة الشحن التي قمت بإنشائها سابقًا.
7. قم بإغلاق الصفحة.

## <a name="set-up-the-audit-master"></a>إعداد أصل التدقيق
1. انتقل إلى إدارة النقل > الإعداد > تسوية الشحن > أصل التدقيق.
    * يحدد السجل الرئيسي للتدقيق حدود السماح لتسوية الشحن التلقائية. فهو يحدد مقدار الاختلاف الممكن بين المبالغ النقدية على فاتورة الشحن والمبالغ النقدية على فاتورة شركة النقل ومع ذلك يسمح بحدوث التسوية. وهو يحدد أيضًا كيفية التعامل مع الاختلافات.  
2. انقر فوق "جديد".
3. في الحقل "معرف أصل التدقيق‬"، اكتب قيمة.
4. في حقل "شركة الشحن"، حدد شركة الشحن نفسها كما فعلت سابقًا.
5. في الحقل "نوع فاتورة الشحن"، حدد نوع فاتورة الشحن التي قمت بإنشائها سابقًا.
6. قم بتوسيع مقطع "السماح".
7. في حقل "‏‫الحد الأدنى لمستوى السماح"، أدخل رقمًا.
8. في حقل "‏‫الحد الأقصى لمستوى السماح"، أدخل رقمًا.
9. قم بتوسيع مقطع "النتيجة".
10. في حقل "‏‫كود سبب الدفع بالزيادة‬"، أدخل قيمة أو حددها.
    * إذا كانت المبالغ النقدية على فاتورة الشحن مختلفة عما هي عليه على فاتورة شركة النقل، فإن أكواد أسباب الدفع بالزيادة والدفع بالنقصان تحدد الحسابات التي يجب تسجيل الفرق عليها، طالما وقع الفرق ضمن مستويات السماح.  
11. في حقل "‏‫كود سبب الدفع بالنقصان"، أدخل قيمة أو حددها.
12. قم بإغلاق الصفحة.

