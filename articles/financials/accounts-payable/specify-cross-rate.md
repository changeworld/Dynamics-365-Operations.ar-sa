---
title: "تحديد سعر الصرف المتداخل"
description: "يوفر هذا الموضوع معلومات حول أسعار الصرف المتداخلة في Microsoft Dynamics 365 for Finance and Operations."
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.contentlocale: ar-sa
ms.lasthandoff: 05/22/2018

---

# <a name="specify-the-cross-rate"></a><span data-ttu-id="cb862-103">تحديد سعر الصرف المتداخل</span><span class="sxs-lookup"><span data-stu-id="cb862-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb862-104">يشرح هذا الموضوع الغرض من سعر الصرف المتداخل وكيفية تحديد سعر الصرف المتداخل عند تسوية دفع باستخدام فاتورة.</span><span class="sxs-lookup"><span data-stu-id="cb862-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="cb862-105">استخدم سعر الصرف المتداخل عند تطبيق جميع المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="cb862-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="cb862-106">تسوية دفعة بفاتورة.</span><span class="sxs-lookup"><span data-stu-id="cb862-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="cb862-107">يستخدم كل من بند الدفع وبند الفاتورة عملات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="cb862-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="cb862-108">عمله المحاسبة ليست إحدى هاتين العملتين.</span><span class="sxs-lookup"><span data-stu-id="cb862-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="cb862-109">لا تستخدم أسعار الصرف المتداخلة لحساب تحويل عملة حركة الدفع إلى عملة محاسبة الدفع.</span><span class="sxs-lookup"><span data-stu-id="cb862-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="cb862-110">بدلًا من ذلك، يتم استرداد أسعار الصرف من جداول أسعار الصرف لحساب قيمة مبلغ عملة حركة الدفع ومبلغ عملة محاسبة الدفع.</span><span class="sxs-lookup"><span data-stu-id="cb862-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="cb862-111">على سبيل المثال، عملة المحاسبة هي الدولار الأمريكي وعملة الفاتورة هي الدولار الكندي وعملة الدفع هي اليورو.</span><span class="sxs-lookup"><span data-stu-id="cb862-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="cb862-112">يسمح لك سعر الصرف المتداخل من إدخال سعر الصرف للتحويل مباشرةً بين اليورو والدولار الكندي، وليس من الضروري التحويل من الدولار الأمريكي.</span><span class="sxs-lookup"><span data-stu-id="cb862-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="cb862-113">وعند تحديد فاتورة وعملية دفع أساسية، يمكن إدخال سعر الصرف المتداخل لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="cb862-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="cb862-114">ويكون سعر البند المتداخل هو سعر الصرف بين العملات لهذه الحركات كما هي في تاريخ التسوية.</span><span class="sxs-lookup"><span data-stu-id="cb862-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="cb862-115">انتقل إلى أحد الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="cb862-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="cb862-116">**الحسابات المدينة > مشترك > العملاء > كافة العملاء**</span><span class="sxs-lookup"><span data-stu-id="cb862-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="cb862-117">**الحسابات الدائنة > مشترك > المورّدون‬ > كافة الموردين**</span><span class="sxs-lookup"><span data-stu-id="cb862-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="cb862-118">** ‏‫التدبير والتوريد > مشترك > الموردون > كافة الموردين‏‫.**</span><span class="sxs-lookup"><span data-stu-id="cb862-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="cb862-119">حدد العميل أو المورد الذي تقوم بتسوية الحركات المفتوحة الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="cb862-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="cb862-120">بالنسبة لعميل، في صفحة قائمة **كافة العملاء** ، انتقل إلى **تحصيل > تسوية الحركات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="cb862-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="cb862-121">بالنسبة للمورد، في صفحة قائمة **كافة الموردين** ، انتقل إلى **فاتورة > تسوية الحركات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="cb862-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="cb862-122">حدد الحركة التي تعتبر عملية دفع أساسية، ثم انقر فوق زر **تمييز عملية الدفع**.</span><span class="sxs-lookup"><span data-stu-id="cb862-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="cb862-123">يتم تحديد خانة الاختيار الموجودة في العمود **وضع علامة** ، كما يتم عرض رمز معلومات في عمود **عملية دفع أساسية** .</span><span class="sxs-lookup"><span data-stu-id="cb862-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="cb862-124">في حقل **سعر الصرف المتداخل** ، ادخل سعر الصرف بين عملة الفاتورة وعملة الدفع، اعتبارًا من تاريخ التسوية.</span><span class="sxs-lookup"><span data-stu-id="cb862-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
