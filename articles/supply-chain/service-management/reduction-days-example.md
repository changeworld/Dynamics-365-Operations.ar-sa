---
title: "مثال أيام التخفيض"
description: "مثال أيام التخفيض."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69e4b1b0fe100b17e5b2c59be81604019347956f
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---


# <a name="reduction-days-example"></a>مثال أيام التخفيض 

[!include [banner](../includes/banner.md)]


لقد قمت بإنشاء حركة اشتراك للاشتراك في الحفاظ على العميل، كما هو موضح في الجدول التالي.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>من تاريخ</p></th>
<th><p>إلى تاريخ</p></th>
<th><p>الاشتراك</p></th>
<th><p>نوع الاشتراك</p></th>
<th><p>Project</p></th>
<th><p>الفئة</p></th>
<th><p>عملة المبيعات</p></th>
<th><p>سعر المبيعات</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01 مارس، 2011</p></td>
<td><p>31 مارس، 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>عادي</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>يورو</p></td>
<td><p>200.00</p></td>
</tr>
</tbody>
</table>


تقارير العملاء التي لا تحتاج لتغطية خدمة لمدة يومين (10 مارس و11 مارس). حيث توافق على تخفيض الاشتراك بمقدار هذين اليومين.

يمكنك إنشاء حركة جديدة من نوع **أيام التخفيض** كما هو موضح في الجدول التالي.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>من تاريخ</p></th>
<th><p>إلى تاريخ</p></th>
<th><p>الاشتراك</p></th>
<th><p>نوع الاشتراك</p></th>
<th><p>Project</p></th>
<th><p>الفئة</p></th>
<th><p>عملة المبيعات</p></th>
<th><p>سعر المبيعات</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10 مارس، 2011</p></td>
<td><p>11 مارس، 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>أيام التخفيض</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>يورو</p></td>
<td><p>12.90-</p></td>
</tr>
</tbody>
</table>


عندما تتم فوترة الحركات لشهر مارس 2011، سيتم تخفيض سعر البيع من 200 يورو إلى 12.90 يورو. وسيكون المبلغ الخاضع للرسوم لحركة الاشتراك هو 187.10 يورو، حيث تتم فوترة حركتين بإجمالي سعر يبلغ 187.10 يورو.

## <a name="see-also"></a>راجع أيضًا

[تقليل الأيام على رسوم الاشتراك](reduce-the-days-on-subscription-fees.md)

  



