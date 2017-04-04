---
title: "طلبات العملاء المختلطة"
description: "طلب عميل مختلط هو أمر مفرد يحتوي على المنتجات التي يمكن حملها خارج المتجر بالعميل، بالإضافة إلى المنتجات التي سيتم التقاطها أو شحنها لاحقاً."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>طلبات العملاء المختلطة

طلب عميل مختلط هو أمر مفرد يحتوي على المنتجات التي يمكن حملها خارج المتجر بالعميل، بالإضافة إلى المنتجات التي سيتم التقاطها أو شحنها لاحقاً.

في Microsoft Dynamics 365-عمليات البيع بالتجزئة، يمكنك تحديد أما القيام بكافة المنتجات أو تنفيذ المنتجات المحددة لأمر عميل. المنتج التي تم وضع علامة تضطلعون يتم تلقائياً فوترة سطور بعد إنشاء الأمر، بالمثل هذا هو نفس ترتيب الذي يتم انتقاؤها لأعلى بعد إنشاء الأمر. المبلغ المستحق على المختلط أوامر يتحدد بواسطة إضافة نسبة الودائع على انتقاء وخطوط الإنتاج الشحن بالمبلغ الكامل لتنفيذ بنود. أوامر المختلط، النظام بالتبديل بين وضع أمر العميل ووضع الموازنات والنقدية كما يلي:

-   إذا تم تعيين كافة المنتجات في العربة إلى **تنفيذ التسليم**، سيتم التعامل مع الترتيب كحركة النقدية والمبالغ.
-   أي أو جميع البنود في سلة التسوق في حالة تعيين أما إلى **بيك** أو **شحن التسليم**، سيتم التعامل مع الترتيب كحركة أمر عميل.

إذا تم تحديد خط عربة و **اختيار تحديد**، **الشحن المحددة**، أو **المحدد تنفيذ** هو تحديد، يحدد خط عربة محددة فقط بهذه الطريقة التسليم. في هذه الحالة، يستمر تدفق المراحل النهائية من العملية كالمعتاد. ومع ذلك، إذا **اختيار تحديد**، **الشحن المحددة**، أو **المحدد تنفيذ** محدداً دون خط عربة المحددة، يفتح صفحة جديدة يقوم بسرد كافة بنود سلة. في هذه الشاشة، يمكنك تحديد بنود متعددة مرة واحدة لتعيين طريقة التسليم. عند استخدام هذا الأسلوب لتحديد الخطوط، سيتم تجاوز أي أسلوب التسليم السابق تم تعيينها إلى الخط.

<a name="see-also"></a>راجع أيضًا
--------

[نظرة عامة حول أوامر العملاء](customer-orders-overview.md)

