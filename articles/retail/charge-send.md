---
title: "شحن أوامر من متجر آخر باستخدام ميزة إرسال شحنة"
description: "يصف هذا الموضوع ميزة إرسال شحنة."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 50f51a7cc043b3c638ae58bffbd988a6db148004
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>شحن أوامر من متجر آخر باستخدام ميزة إرسال شحنة

[!include [banner](includes/banner.md)]

مع ميزة إرسال شحنة في Dynamics 365 for Retail، يمكن إجراء أوامر العملاء من متجر وشحنها من متجر آخر. فأوامر العميل في نقطة البيع (POS) تدعم العديد من خيارات التنفيذ. تتضمن بعض أمثلة خيارات التنفيذ ما يلي:
-   الاستلام من المتجر نفسه بتاريخ مختلف.
-   الاستلام من متجر آخر بنفس التاريخ أو بتاريخ مختلف.
-   الشحن من مستودع الشحن الافتراضي المُعين للمتجر والتسليم في تاريخ محدد.

تستخدم ميزة إرسال الشحنة هذه عمليات نقاط البيع التالية: شحن جميع المنتجات وشحن المنتجات المحددة. يسمح هذا لموظف المتجر بتحديد موقع "الشحن من" الذي يمكن تلبية الأمر أو سطر الأمر منه. بشكل افتراضي، يكون موقع "الشحن من" هو مستودع الشحن المقترن بالمتجر. ومع ذلك، يمكن لموظف المتجر تغيير هذا الموقع وتحديد أي متجر يكون محددًا في مجموعة محدد مواقع المتاجر المُعينة للمتجر. 

وتبقى إمكانية تحديد عناوين "الشحن إلى" دون تغيير. 

تستند طرق الشحن التي يمكن استخدامها لتنفيذ سطر الأمر إلى تكوين أوضاع التسليم الصالحة للمنتجات والعناوين. ونظرًا لأن القواعد الخاصة بأوضاع التسليم الصالحة يتم الاحتفاظ بها في إدارة البيع بالتجزئة فقط، يقوم عميل نقطة البيع باتصال في الوقت الفعلي لمعرفة أوضاع التسليم الصالحة لبند شحن. 


