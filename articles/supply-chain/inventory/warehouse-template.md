---
title: "إعداد مستودع باستخدام قالب تكوين مستودع"
description: "يشرح هذا الموضوع طريقة إعداد مستودع باستخدام قالب تكوين مستودع."
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 90a4276f261affd8c90f2deb7cd0b773d43e5485
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a><span data-ttu-id="7da61-103">إعداد مستودع باستخدام قالب تكوين مستودع</span><span class="sxs-lookup"><span data-stu-id="7da61-103">Set up a warehouse by using a warehouse configuration template</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7da61-104">يشرح هذا الموضوع طريقة إعداد مستودع باستخدام قالب تكوين مستودع.</span><span class="sxs-lookup"><span data-stu-id="7da61-104">This topic explains how to set up a warehouse by using a warehouse configuration template.</span></span> <span data-ttu-id="7da61-105">هناك العديد من قوالب التكوين المعرفة مسبقاً التي يمكنك استخدامها.</span><span class="sxs-lookup"><span data-stu-id="7da61-105">There are several predefined configuration templates that you can use.</span></span> <span data-ttu-id="7da61-106">لمزيد من المعلومات حول كيفية استخدام هذه القوالب، راجع [قوالب بيانات التكوين](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="7da61-106">For information about how to use these templates, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a><span data-ttu-id="7da61-107">السيناريوهات التي تكون فيها قوالب التكوين مفيدة</span><span class="sxs-lookup"><span data-stu-id="7da61-107">Scenarios where configuration templates can be helpful</span></span>

<span data-ttu-id="7da61-108">يمكن لقوالب التكوين أن تكون مفيدة في عدة سيناريوهات.</span><span class="sxs-lookup"><span data-stu-id="7da61-108">Configuration templates can be helpful in many scenarios.</span></span> <span data-ttu-id="7da61-109">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="7da61-109">Here are some examples:</span></span>

- <span data-ttu-id="7da61-110">إذا أكملت إعداد تكوين واختبرته في بيئة اختبار، وترغب الآن في نسخ الإعداد إلى بيئة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="7da61-110">You've completed and tested a configuration setup in a test environment, and you now want to copy the setup to a production environment.</span></span>
- <span data-ttu-id="7da61-111">إذا كنت بحاجة إلى نشر إعداد المستودع للعديد من الكيانات القانونية أو إنشاء مستودع جديد في نفس الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="7da61-111">You want to roll the warehouse setup out to several legal entities or create a new warehouse in the same legal entity.</span></span>
- <span data-ttu-id="7da61-112">إذا كنت بحاجة إلى سرعة إعداد عرض توضيحي للوظيفة المستودع.</span><span class="sxs-lookup"><span data-stu-id="7da61-112">You want to quickly prepare for a demo of the warehouse functionality.</span></span>
- <span data-ttu-id="7da61-113">إذا كنت تريد أن تستخدم الأصناف الموجودة والمستودعات الوظيفة في إدارة المستودعات بدلاً من الوظيفة في إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="7da61-113">You want existing items and warehouses to use the functionality in Warehouse management instead of the functionality in Inventory management.</span></span>

<span data-ttu-id="7da61-114">يركز هذا الموضوع على أول هذه السيناريوهات.</span><span class="sxs-lookup"><span data-stu-id="7da61-114">This topic focuses on the first of these scenarios.</span></span> <span data-ttu-id="7da61-115">حيث يشرح هذا السيناريو كيفية استخدام قالب تكوين لنسخ إعداد تكوين من بيئة اختبار إلى بيئة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="7da61-115">It shows how you can use a configuration template to copy a configuration setup from a test environment to a production environment.</span></span>

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a><span data-ttu-id="7da61-116">نسخ إعداد تكوين من بيئة اختبار إلى بيئة إنتاج</span><span class="sxs-lookup"><span data-stu-id="7da61-116">Copy a configuration setup from a test environment to a production environment</span></span>

<span data-ttu-id="7da61-117">بالنسبة لهذا السيناريو، يوجد إعداد التكوين لأحد المستودعات وبعض عمليات الحركة بالفعل في بيئة اختبار.</span><span class="sxs-lookup"><span data-stu-id="7da61-117">For this scenario, the configuration setup for a warehouse and some transaction processes already exist in a test environment.</span></span> <span data-ttu-id="7da61-118">تحتاج الآن لنسخ إعداد التكوين الخاص بالمستودع من بيئة الاختبار إلى بيئة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="7da61-118">You now want to copy the configuration setup for the warehouse from the test environment to a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="7da61-119">من المهم أن تقوم بتضمين بيانات الإعداد المرتبطة الأخرى عندما تقوم بنسخ إعداد تكوين.</span><span class="sxs-lookup"><span data-stu-id="7da61-119">It's important that you include other related setup data when you copy a configuration setup.</span></span> <span data-ttu-id="7da61-120">على سبيل المثال، تحتاج إلى إعداد المنتجات عن طريق نسخ الإعداد من بيئة اختبار.</span><span class="sxs-lookup"><span data-stu-id="7da61-120">For example, you want to set up products by copying the setup from a test environment.</span></span> <span data-ttu-id="7da61-121">ومع ذلك، لا يمكنك إعداد موقع انتقاء ثابت لمنتج قبل إنشاء ذلك المنتج.</span><span class="sxs-lookup"><span data-stu-id="7da61-121">However, you can't set up a fixed picking location for a product before that product is created.</span></span> <span data-ttu-id="7da61-122">على الرغم من أن قوالب التكوين الفردي لا تدعم هذا النوع من التبعية، فإن قوالب البيانات الافتراضية تدعمه.</span><span class="sxs-lookup"><span data-stu-id="7da61-122">Although individual configuration templates don't support this type of dependency, there are default data templates that support it.</span></span> <span data-ttu-id="7da61-123">يمكن تضمين قوالب البيانات الافتراضية هذه بسهولة في عملية تكوين.</span><span class="sxs-lookup"><span data-stu-id="7da61-123">You can easily include these default data templates in a configuration process.</span></span>

### <a name="export-a-default-warehouse-template"></a><span data-ttu-id="7da61-124">تصدير قالب مستودع افتراضي</span><span class="sxs-lookup"><span data-stu-id="7da61-124">Export a default warehouse template</span></span> 

1. <span data-ttu-id="7da61-125">افتح مساحة العمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="7da61-125">Open the **Data management** workspace.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7da61-126">إذا كنت تستخدم مساحة العمل هذه لأول مرة، فإنه يجب عليك تحميل كيان البيانات كافة قبل المتابعة.</span><span class="sxs-lookup"><span data-stu-id="7da61-126">If you're using this workspace for the first time, you must load all the data entities before you continue.</span></span>

2. <span data-ttu-id="7da61-127">حدد التجانب **القوالب**، ثم حدد **تحميل القوالب الافتراضية** لتحميل القوالب الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="7da61-127">Select the **Templates** tile, and then select **Load default templates** to load the default templates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7da61-128">يتوفر **تحميل القوالب الافتراضية** فقط في طريقة العرض **‏‫مُحسّن‬**.</span><span class="sxs-lookup"><span data-stu-id="7da61-128">**Load default templates** is available only in the **Enhanced** view.</span></span> <span data-ttu-id="7da61-129">حدد **‏‫محددات إطار العمل‬**، ثم في الحقل **‏‫عرض القيم الافتراضية‬**، حدد **‏‫طريقة العرض المحسنة‬**.</span><span class="sxs-lookup"><span data-stu-id="7da61-129">Select **Framework parameters**, and then, in the **View defaults** field, select **Enhanced view**.</span></span>

3. <span data-ttu-id="7da61-130">بعد تحميل القوالب الافتراضية، يمكنك تغييرها كي تفي بمتطلبات العمل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="7da61-130">After the default templates are loaded, you can change them so that they meet your business requirements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7da61-131">لتحميل القوالب الافتراضية واستيراد قوالب، يجب أن يكون لديك حق الوصول كمسؤول النظام.</span><span class="sxs-lookup"><span data-stu-id="7da61-131">To load default templates and import templates, you must have system administrator access.</span></span> <span data-ttu-id="7da61-132">يساعد هذا المتطلب في ضمان أن يتم تحميل كافة الكيانات بشكل صحيح في القالب.</span><span class="sxs-lookup"><span data-stu-id="7da61-132">This requirement helps guarantee that all entities are correctly loaded into the template.</span></span>

4. <span data-ttu-id="7da61-133">تأكد من وجودك في الكيان القانوني الذي ترغب في تصدير البيانات الخاصة بالشركة منه.</span><span class="sxs-lookup"><span data-stu-id="7da61-133">Make sure that you're in the legal entity that you want to export the company-specific data from.</span></span>
5. <span data-ttu-id="7da61-134">في مساحة العمل، حدد **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="7da61-134">In the workspace, select **Export**.</span></span>
6. <span data-ttu-id="7da61-135">قم بإنشاء تصدير مشروع جديد.</span><span class="sxs-lookup"><span data-stu-id="7da61-135">Create a new export project.</span></span>
7. <span data-ttu-id="7da61-136">حدد **+ إضافة قالب**، وابحث عن قالب المستوع الافتراضي **WMS 400-**.</span><span class="sxs-lookup"><span data-stu-id="7da61-136">Select **+ Add template**, and find the **400 - WMS** default warehouse template.</span></span> <span data-ttu-id="7da61-137">يضيف هذا القالب كيانات البيانات لتكوين المستودع.</span><span class="sxs-lookup"><span data-stu-id="7da61-137">This template adds data entities for warehouse configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7da61-138">إذا كان من اللازم تصفية البيانات التي تقوم بتصديرها (على سبيل المثال، تحتاج إلى تصدير البيانات المرتبطة بمستودع معين فقط)، فإنه يجب عليك تقييم كل كيان بيانات وإضافة التصفية من خلال استعلام.</span><span class="sxs-lookup"><span data-stu-id="7da61-138">If the data that you're exporting must be filtered (for example, you want to export only the data that is related to a specific warehouse), you must evaluate each data entity and add filtering via a query.</span></span> <span data-ttu-id="7da61-139">بدلاً من ذلك، يمكنك تصدير البيانات بالكامل ثم حذف السجلات غير المطلوبة في ملفات الوجهة.</span><span class="sxs-lookup"><span data-stu-id="7da61-139">Alternatively, you can export all data and then delete the records that aren't required in the destination files.</span></span>

8. <span data-ttu-id="7da61-140">حدد **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="7da61-140">Select **Export**.</span></span> <span data-ttu-id="7da61-141">تم تصدير البيانات المرتبطة بجميع كيانات البيانات في المشروع.</span><span class="sxs-lookup"><span data-stu-id="7da61-141">Data that is related to all the data entities in the project is exported.</span></span>

<span data-ttu-id="7da61-142">يمكنك تحميل ملف zip لحزمة البيانات.</span><span class="sxs-lookup"><span data-stu-id="7da61-142">You can download a zip file for the data package.</span></span> <span data-ttu-id="7da61-143">يحتوي هذا الملف على جميع البيانات بالتنسيق المحدد (على سبيل المثال، تنسيق Excel).</span><span class="sxs-lookup"><span data-stu-id="7da61-143">This file contains all the data in the selected format (for example, Excel format).</span></span> <span data-ttu-id="7da61-144">كما ذُكر، قد يكون من الواجب تحديث بعض السجلات في ملفات حزمة البيانات قبل أن يمكنك استيرادها في بيئة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="7da61-144">As has been mentioned, some records in the data package files might have to be updated before you can import them into the production environment.</span></span> <span data-ttu-id="7da61-145">إذا قمت بتحديث أحد السجلات، تأكد من أنك لم تقم بتغيير اسم الملف.</span><span class="sxs-lookup"><span data-stu-id="7da61-145">If you update a record, make sure that you don't change the file name.</span></span>

### <a name="import-a-warehouse-configuration-setup"></a><span data-ttu-id="7da61-146">استيراد إعداد تكوين مستودع</span><span class="sxs-lookup"><span data-stu-id="7da61-146">Import a warehouse configuration setup</span></span>

1. <span data-ttu-id="7da61-147">في بيئة الوجهة، تأكد من وجودك في الشركة التي ترغب في استيراد بيانات المستودع إليها.</span><span class="sxs-lookup"><span data-stu-id="7da61-147">In the destination environment, make sure that you're in the company that you want to import the warehouse data into.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7da61-148">قبل القيام بعملية الاستيراد، يجب عليك تحديد تبعيات البيانات.</span><span class="sxs-lookup"><span data-stu-id="7da61-148">Before you do the import, you should identify any data dependencies.</span></span> <span data-ttu-id="7da61-149">على سبيل المثال، يحتوي القالب **إدارة المستودعات** على كيان بيانات يحمل الاسم **‏‫أكواد إرجاع المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="7da61-149">For example, the **Warehouse management** template includes a data entity that is named **Warehouse disposition codes**.</span></span> <span data-ttu-id="7da61-150">يحتوي هذا الكيان على البيانات المتعلقة بصفحة الإعداد **أكواد الترتيب** (**إدارة المستودعات** > **الإعداد** > **جهاز محمول** > **ترتيب رموز**).</span><span class="sxs-lookup"><span data-stu-id="7da61-150">This entity contains data that is related to the **Disposition codes** setup page (**Warehouse management** > **Setup** > **Mobile device** > **Disposition codes**).</span></span> <span data-ttu-id="7da61-151">إذا كان هناك إعداد موجود قد عالج بالفعل عملية الإرجاع لأوامر المبيعات، فسوف يحتوي الحقل **‏‫إرجاع رمز الإرجاع‬**على قيمة.</span><span class="sxs-lookup"><span data-stu-id="7da61-151">If an existing setup already handles the return process for sales orders, the **Return disposition code** field contains a value.</span></span> <span data-ttu-id="7da61-152">يرتبط كود الترتيب في هذا الحقل بكيان البيانات **كود الترتيب** الذي يُعد جزءًا من القالب **المبيعات والتسويق**.</span><span class="sxs-lookup"><span data-stu-id="7da61-152">The disposition code in this field is related to the **Disposition code** data entity, which is part of the **Sales and marketing** template.</span></span> <span data-ttu-id="7da61-153">إذا كانت البيانات من كيان البيانات **كود الترتيب** لم يتم استيرادها من الحقل **‏‫أكواد إرجاع المستودعات‬**، فسوف تفشل عملية الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="7da61-153">If the data from the **Disposition code** data entity isn't imported before the data from the **Warehouse disposition codes** field, the import will fail.</span></span>

2. <span data-ttu-id="7da61-154">في مساحة العمل **إدارة البيانات**، حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="7da61-154">In the **Data management** workspace, select **Import**.</span></span>
3. <span data-ttu-id="7da61-155">قم بإنشاء استيراد مشروع جديد.</span><span class="sxs-lookup"><span data-stu-id="7da61-155">Create a new import project.</span></span>
4. <span data-ttu-id="7da61-156">حدد **+ إضافة ملف**، وقم بتحميل ملف zip لحزمة البيانات.</span><span class="sxs-lookup"><span data-stu-id="7da61-156">Select **+ Add file**, and upload the zip file for the data package.</span></span>
5. <span data-ttu-id="7da61-157">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="7da61-157">Select **Import**.</span></span> <span data-ttu-id="7da61-158">في طريقة العرض **مُحسن**، يمكنك استخدام الخيار **عامل تصفية** لسرعة الحصول على نظرة عامة حول المشكلات المحتمل حدوثها أثناء عملية الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="7da61-158">In the **Enhanced** view, you can use the **Filter** option to quickly get an overview of issues that might occur during the import.</span></span>

<span data-ttu-id="7da61-159">يوفر عرض **سجل التنفيذ** معلومات مفصلة حول كيان البيانات التي تم استيرادها.</span><span class="sxs-lookup"><span data-stu-id="7da61-159">The **View execution** log provides detailed information about each data entity that is imported.</span></span> <span data-ttu-id="7da61-160">يمكنك استخدام ‏‫عرض بيانات التشغيل المرحلي‬ للوصول بسرعة إلى البيانات الهدف.</span><span class="sxs-lookup"><span data-stu-id="7da61-160">You can use the staging data view to quickly get to the target data.</span></span> <span data-ttu-id="7da61-161">وبهذه الطريقة، يمكنك مشاهدة الطريقة التي تبدو عليها البيانات المستوردة في الصفحات ذات الصلة في استمارة التقديم.</span><span class="sxs-lookup"><span data-stu-id="7da61-161">In this way, you can see what the imported data looks like on the related pages in the application.</span></span> <span data-ttu-id="7da61-162">عند استخدام قوالب البيانات الافتراضية، يعمل استيراد التسلسل لكل كيان من كيانات البيانات بالطريقة المحددة مسبقاً، للمساعدة في ضمان أن يتم استيراد كافة البيانات التابعة أولاً.</span><span class="sxs-lookup"><span data-stu-id="7da61-162">When you use the default data templates, the import sequence for each data entity works in the predefined manner, to help guarantee that all dependent data is imported first.</span></span> <span data-ttu-id="7da61-163">إذا كانت كيانات البيانات المخصصة جزءًا من المشروع، فيجب التأكد من تحديد التسلسل الصحيح.</span><span class="sxs-lookup"><span data-stu-id="7da61-163">If custom data entities are part of the project, you must make sure that the correct sequence is defined.</span></span> <span data-ttu-id="7da61-164">لمزيد من المعلومات، راجع [‬‏‫قوالب بيانات التكوين](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="7da61-164">For more information, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="related-topic"></a><span data-ttu-id="7da61-165">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="7da61-165">Related topic</span></span>

[<span data-ttu-id="7da61-166">قوالب بيانات التكوين</span><span class="sxs-lookup"><span data-stu-id="7da61-166">Configuration data templates</span></span>](../../dev-itpro/data-entities/configuration-data-templates.md)
