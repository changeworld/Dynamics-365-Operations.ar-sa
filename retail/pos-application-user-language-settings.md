---
title: "تطبيق نقطة البيع وإعدادات اللغة المستخدمة"
description: "يصف هذا الموضوع كيفية تغيير إعدادات اللغة في نقطة البيع التجزئة الحديثة (مبوس) و &quot;نقاط البيع مجموعة النظراء&quot;."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>تطبيق نقطة البيع وإعدادات اللغة المستخدمة

يصف هذا الموضوع كيفية تغيير إعدادات اللغة في نقطة البيع التجزئة الحديثة (مبوس) و "نقاط البيع مجموعة النظراء".

<a name="overview"></a>نظرة عامة
========

البيع بالتجزئة الحديثة نقطة البيع (مبوس) و "نقاط البيع سحابة" دعم بيئات حيث يمكن أن تختلف إعدادات اللغة وتحويلات بين إعدادات المستخدم ومخزن. على سبيل المثال، يكون موجوداً في المخزن في منطقة حيث اللغة الإنجليزية الأكثر شيوعاً للعملاء، ولكن بعض العاملين يفضلون استخدام التطبيق بالترجمات الفرنسية.

## <a name="data-language"></a>لغة البيانات
بغض النظر عن إعدادات المستخدم، مبوس ونقاط البيع سحابة سيتم دائماً استخدام إعدادات اللغة المخزن لتحديد الترجمات المستخدمة للبيانات. هذا يؤكد أن كافة المستخدمين والزبائن سيكون متناسقة.  أمثلة للبيانات:

-   المنتجات
-   السمات والقيم
-   أسماء الفئة
-   إيصالات حركة المطبوعة أو مرسلة عبر البريد الإلكتروني
-   أسماء طريقة الدفع
-   رسائل شاشة عرض سطرية

سيتم استخدام اللغة المتجر أيضا لشاشة تسجيل الدخول نقطة البيع الرئيسية، نظراً للمستخدم غير معروف قبل تسجيل الدخول. إذا لم يتوفر ترجمة للغة للمتجر، نقطة البيع ستعود إلى اللغة الخاصة بالشركة.

### <a name="configuring-the-stores-language-setting"></a>تكوين إعدادات لغة المتجر

يتم تعيين إعداد اللغة المتجر من **جميع متاجر التجزئة** على **متجر** الصفحة ضمن * * عام &gt; "الإعدادات الإقليمية" &gt;اللغة. * * استخدم القائمة أسفل باختيار لغة لكل متجر.

## <a name="user-interface-language"></a>لغة واجهة المستخدم
يحدد إعداد لغة المستخدم POS الترجمات المستخدمة في واجهة مستخدم التطبيق. يتضمن ذلك كافة تسميات القوائم والقوائم التي لا تعتبر البيانات. الاستثناء الوحيد هو النص الذي يتم عرضه على أشرطة الأوامر نقطة البيع. لا تدعم أشرطة الأوامر الترجمة، حيث أنها سوف تظهر دائماً النص كما هو محدد في الزر. ولدعم أزرار المترجم، سيكون لديك لنسخ وصيانة شبكات زر منفصل وتعيينها للمستخدمين حسب الحاجة.

### <a name="configuring-the-users-language-setting"></a>تكوين إعدادات لغة المستخدم

يتم تعيين إعداد لغة المستخدم نقاط البيع من **جميع العمال** على **العامل** الصفحة ضمن **البيع بالتجزئة &gt;لغة**.  لم يتم تعيين علامة التبويب ملف التعريف الأساسي.  لا يتم استخدام هذا الإعداد بنقطة البيع. إذا لم يتم تعيين لغة المستخدم أو إذا تم تعيينها إلى لغة لا تتوفر فيها ترجمات، ستعود نقطة البيع إلى لغة المتجر.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **لغة واجهة المستخدم** * * * *      | **لغة البيانات (المنتجات، تنسيقات الإيصالات، عرض الخط، إلخ)** |
| **الشركة** | افتراضي                    | افتراضي                                                           |
| **المتجر**   | يتجاوز الشركة          | يتجاوز الشركة                                                 |
| **User**    | يتجاوز المتجر أو الشركة | أبدًا                                                             |



