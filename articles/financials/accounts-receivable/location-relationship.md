---
title: "إضافة موقع وأنواع علاقات الأطراف"
description: "يشرح هذا الموضوع كيفية إضافة موقع جديد وعلاقة طرف."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: e0ab9c9894fdd5fba224c166941abbf52172ae46
ms.openlocfilehash: 27819c922832a30eb0b20db6bffdbd4504e6d5e6
ms.contentlocale: ar-sa
ms.lasthandoff: 06/12/2018

---

# <a name="add-location-roles-and-party-relationship-types"></a>إضافة أدوار مواقع وأنواع علاقات الأطراف 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>إضافة أدوار المواقع

توجد طريقتان لإضافة أدوار مواقع جديدة للعنوان ومعلومات جهة الاتصال:

-  أضفها إلى صفحة **‏‫الغرض من معلومات العنوان وجهة الاتصال‬**. سيتم حفظ الدور الجديد في الجدول **LogisticsLocationRole** بنوع = 0، الذي يشير إلى أن الدور ليس دور نظام محدد في تعداد **LogisticsLocationRoleType** وملحقاته. سيكون المستخدم قادراً على استخدام هذا الدور عند إنشاء عنوان أو معلومات جهة الاتصال.

    ![الغرض من معلومات المحتوى وجهة الاتصال](media/Address-Contact.PNG)

-  أضفها إلى ملحق تعداد **LogisticsLocationRoleType**، وانشرها خلال عملية مزامنة قاعدة البيانات.

    1.  قم بإنشاء ملحق لتعداد **LogisticsLocationRoleType** وأضف الدور الجديد في الامتداد. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. قم بإنشاء ملف مورد للدور الجديد، ثم قم بتعيين قيمة للخصائص.
     
     ![ملف مورد جديد](media/Resource.PNG)
        
    3.  قم بإنشاء فئة لنشر البيانات واستخدم طريقة المعالج لنشر الدور الجديد. 

        ![نشر البيانات](media/Dirdata.PNG)

    4.  لاختبار نشر دور الموقع الجديد، فإنه يمكنك إنشاء فئة قابلة للتشغيل، واطلب DirDataPopulation::insertLogisticsLocationRoles() في Main(). بعد إكمال هذه العملية، فإنه ينبغي عليك رؤية الدور الجديد المنشور في الجدول **LogisticsLocationRole** من نوع \> 0. سيتم عرض الدور الجديد على **‏‫الغرض من معلومات العنوان وجهة الاتصال‬**.

        ![إدراج موقع جديد](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>إضافة أنواع علاقات الأطراف 

هناك طريقتان لإضافة نوع علاقة جديد:

-   إضافتها خلال الصفحة **أنواع العلاقات**. سيتم حفظ العلاقة الجديدة على **DirRelationshipTypeTable** باستخدام systemtype = 0.

    ![أنواع العلاقات](media/Relationship.PNG)

-  إضافتها في ملحق تعداد **DirSystemRelationshipType**، ونشرها خلال عملية مزامنة قاعدة البيانات.

    1.  قم بإنشاء التعداد **DirSystemRelationship** وأضف نوع العلاقة الجديد.

    2. قم بإنشاء مهيئ لهذا النوع الجديد. يمكنك العثور على أمثلة متعددة في الكود الأساسي، أحدها هو **DirRelationshipTypeChildInitialize**. إنها فئة مهيئ لنوع علاقة طرف "تابع". يمكنك البدء بالمهيئ الخاص بك عن طريق نسخ ولصق هذا الكود ثم قم بتحديث المناطق المميزة.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  لاختبار نشر نوع العلاقة الجديد، فإنه يمكنك إنشاء فئة قابلة للتشغيل، واطلب DirDataPopulation::insertDirRelationshipTypes() في Main(). ينبغي عليك رؤية نوع العلاقة الجديد في **DirRelationshipTypeTable**، ثم سيتوافر نوع العلاقة الجديد على صفحة **أنواع العلاقات**.

        ![فئة قابلة للتشغيل](media/Runnable.PNG)

