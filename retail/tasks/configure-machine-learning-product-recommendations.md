--- 
title: " تكوين توصيات المنتجات المدعومة بنظام التعلم الآلي"
description: "يقوم هذا الإجراء بتحديث البيانات في مخزن الكيانات المستخدم من قبل نظام التعلم الآلي الذي يدعم التوصيات، ثم يمكّن توصيات المنتجات على عملاء نقطة البيع."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c51c5f82efb50db1e238f4046506920975f33218
ms.contentlocale: ar-sa
ms.lasthandoff: 07/28/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a> تكوين توصيات المنتجات المدعومة بنظام التعلم الآلي

[!include[task guide banner](../includes/task-guide-banner.md)]

يقوم هذا الإجراء بتحديث البيانات في مخزن الكيانات المستخدم من قبل نظام التعلم الآلي الذي يدعم التوصيات، ثم يمكّن توصيات المنتجات على عملاء نقطة البيع. ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.

1. انتقل إلى إدارة النظام > الإعداد > متجر الكيانات‬.
2. في القائمة، ابحث عن السجل "RetailSales" وحدده.
3. انقر فوق "تحديث".
4. انقر فوق "موافق".
5. قم بإغلاق الصفحة.
6. انتقل إلى البيع بالتجزئة والتجارة > إعداد المراكز الرئيسية > المعلمات > معلمات البيع بالتجزئة‬.
7. انقر فوق علامة التبويب "التعلم الآلي".
8. حدد "نعم" في حقل "تمكين توصيات المنتجات‬".
    * إذا تلقيت الرسالة "تعذر استرداد نماذج التوصية"، فسبب ذلك يعود إلى تحديث مخزن الكيانات مؤخرًا دون أن ينتهي النظام من استيعاب البيانات الجديدة. انتظر من ساعتين إلى ثلاث ساعات وحاول مرة أخرى.  
9. انقر فوق "حفظ".
10. قم بإغلاق الصفحة.

