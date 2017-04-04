---
title: "استيراد أسعار صرف العملات"
description: "إذا تلقي كيان قانوني الفواتير بالعملات الأجنبية، من الضروري تحويل العملات الأجنبية إلى العملة المحلية. وهذا يعني أن هناك حاجة إلى تحديث أسعار صرف عملات مختلفة. يوفر هذا الموضوع نظرة عامة حول معالجة لاستيراد نشرة عبر الإنترنت بواسطة موفري سعر الصرف، مثل مصرف روسيا المركزي والبنك المركزي الأوروبي أسعار مرجع صرف العملات الأجنبية والإعدادات المطلوبة."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>استيراد أسعار صرف العملات

إذا تلقي كيان قانوني الفواتير بالعملات الأجنبية، من الضروري تحويل العملات الأجنبية إلى العملة المحلية. وهذا يعني أن هناك حاجة إلى تحديث أسعار صرف عملات مختلفة. يوفر هذا الموضوع نظرة عامة حول معالجة لاستيراد نشرة عبر الإنترنت بواسطة موفري سعر الصرف، مثل مصرف روسيا المركزي والبنك المركزي الأوروبي أسعار مرجع صرف العملات الأجنبية والإعدادات المطلوبة.

تصف المقاطع التالية تدفق المعلومات المستخدمة لإعداد وتجهيز استيراد أسعار الصرف الأجنبي.

## <a name="configure-an-exchange-rate-provider"></a>تكوين موفر سعر الصرف
قبل أن يمكنك استيراد أسعار الصرف، يجب إعداد المعلومات المطلوب من قبل الموفرين الذين يقدمون أسعار الصرف. استخدام **تكوين موفري سعر الصرف** الصفحة لتحديد موفري سعر الصرف. بعض موفري سعر الصرف يتم تضمين بيانات تجريبية في Microsoft Dynamics 365 للعمليات. يعرض الجدول التالي الأوصاف الخاصة بعناصر التحكم الموجودة في هذه الصفحة.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | اسم موفر أسعار الصرف.                                                                                                                                                                                     |
| **مفتاح**   | المعرف الفريد لكل معلومة تكوين يطلبها الموفر. يتم إضافة هذه المعلومات تلقائياً لكل موفر سعر الصرف عند النقر فوق إضافة **إضافة** الزر. |
| **Value** | معلومات لكل مفتاح. يتم إضافة هذه المعلومات لكل موفر سعر الصرف عند النقر فوق إضافة **إضافة** الزر.                                                                                         |

## <a name="import-currency-exchange-rates"></a>استيراد أسعار صرف العملات
يمكنك استيراد أسعار الصرف من مصدر موفري سعر الصرف، وإعدادها **أسعار صرف العملات** الصفحة. استخدام **استيراد أسعار صرف العملات** الصفحة لاستيراد أسعار الصرف. يوفر الجدول التالي وصف الحقول المطلوبة لإكمال عملية الاستيراد بنجاح.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | نوع سعر الصرف.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | موفر سعر الصرف.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | وتدير هذه المعلمة ما إذا كان سيتم استيراد اعتبارا من تاريخ اليوم أو نطاق تاريخ. إذا كنت تريد استخدام نطاق تاريخ، أدخل أو حدد تواريخ البدء والانتهاء.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | خانة الاختيار إدارة الإنشاء التلقائي لأزواج العملات، في حالة عدم وجود زوج العملة التي يتم استيرادها. قد لا يكون هذا الخيار متوفر لبعض الموفرين.                                                                                                                                                                                               |
| **Override existing exchange rates**   | إدارة خانة الاختيار تحديث سعر الصرف الموجودة لزوج عمله عند وجود سعر الصرف لتاريخ محدد مسبقاً. إذا لم تختر هذا الخيار، لا يتم استيراد أسعار الصرف لتواريخ معينة إذا كان سعر الصرف آخر موجود بالفعل.                                                                                       |
| **Prevent import on national holiday** | خانة الاختيار إدارة الاستيراد لسعر الصرف لتاريخ عطلة رسمية. على سبيل المثال، في حالة تحديد خانة الاختيار هذه واستخدام "البنك المركزي الأوروبي" كموفر أسعار الصرف، النظام لن يتم تحديث سعر الصرف في العطلات عامة المرتبطة بالكيان القانوني الحالي. قد لا يكون هذا الخيار متوفر لبعض الموفرين. |



