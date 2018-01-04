---
title: "توسيع وظائف Microsoft Dynamics 365 for Talent"
description: "إذا قمت بإنشاء أي Microsoft PowerApps، فإنه يمكنك بدء تشغيل تلك التطبيقات من الارتباطات الموجودة في Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: Talent
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cfd3b475b113fdab4ceeb3e636fea6c9134ab982
ms.openlocfilehash: 0ab829803634871c9060daa381bd02d7d2bbdf42
ms.contentlocale: ar-sa
ms.lasthandoff: 12/01/2017

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="40875-103">توسيع وظائف Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="40875-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>
<span data-ttu-id="40875-104">إذا قمت بإنشاء أي Microsoft PowerApps، فإنه يمكنك بدء تشغيل تلك التطبيقات من الارتباطات الموجودة في Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="40875-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="40875-105">لإعداد وصول إلى التطبيقات الخاصة بك، ستحتاج إلى إعداد بعض المعلومات في Talent في صفحة تكوين يمكنك فتحها من مساحة عمل **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="40875-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="40875-106">تكوين PowerApps المضمن داخل Talent</span><span class="sxs-lookup"><span data-stu-id="40875-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="40875-107">استخدم صفحة **تعيين Microsoft PowerApps المضمنة** لتكوين صفحات Talent لبدء تشغيل تطبيقات PowerApps.</span><span class="sxs-lookup"><span data-stu-id="40875-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="40875-108">لفتح صفحة **تعيين Microsoft PowerApps المضمنة**، افتح مساحة عمل **إدارة النظام**، ثم افتح علامة التبويب **ارتباطات**. حدد **Microsoft PowerApps** من مجموعة **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="40875-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="40875-109">يتم إدخال المعلومات التالية أو تعيينها في هذه الصفحة:</span><span class="sxs-lookup"><span data-stu-id="40875-109">The following information is entered or set on this page:</span></span> 

> - <span data-ttu-id="40875-110">اسم وصفي أو معرف لكل تطبيق PowerApps.</span><span class="sxs-lookup"><span data-stu-id="40875-110">A descriptive name or identifier for each PowerApps application.</span></span>
> - <span data-ttu-id="40875-111">معرف فريد (GUID) لكل تطبيق تضيفه إلى صفحة Talent.</span><span class="sxs-lookup"><span data-stu-id="40875-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="40875-112">معرف التطبيق متوفر على موقع PowerApps، [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="40875-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
> - <span data-ttu-id="40875-113">الصفحة التي يستطيع المستخدمون منها فتح تطبيق أو تقرير.</span><span class="sxs-lookup"><span data-stu-id="40875-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="40875-114">لا تدعم جميع صفحات Talent تطبيقات PowerApps المضمنة وتقارير Power BI.</span><span class="sxs-lookup"><span data-stu-id="40875-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="40875-115">أدخل الاسم الداخلي للصفحة بدلاً من اسم العرض الذي يظهر في أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="40875-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="40875-116">للعثور على الاسم الداخلي، افتح الصفحة التي تحتاج إلى اسمها الداخلي، وانقر نقرًا مزدوجًا فوق أي مكان على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="40875-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="40875-117">عند فتح القائمة، قم بالتمرير فوق عنصر **معلومات النموذج**.</span><span class="sxs-lookup"><span data-stu-id="40875-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="40875-118">يتم عرض اسم النموذج الداخلي بجوار عنصر **معلومات النموذج** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="40875-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
> - <span data-ttu-id="40875-119">حدد عنصر تحكم النموذج الذي يمكن للتطبيق استرداد بيانات السياق منه.</span><span class="sxs-lookup"><span data-stu-id="40875-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="40875-120">على سبيل المثال، قد يستخدم تطبيق بيانات حول عامل.</span><span class="sxs-lookup"><span data-stu-id="40875-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="40875-121">إذا قمت بإدخال صفحة **العامل** في حقل **السياق**، فسيتم فتح صفحة **العامل** عند بدء تشغيل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="40875-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="40875-122">إدخال في **حقل السياق** اختياري.</span><span class="sxs-lookup"><span data-stu-id="40875-122">An entry in the **Context field** is optional.</span></span> 
> - <span data-ttu-id="40875-123">قم بتعيين حجم مربع الحوار الذي سيتم تشغيل تطبيق PowerApps عليه.</span><span class="sxs-lookup"><span data-stu-id="40875-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="40875-124">تم تعيين مربعات الحوار كـ "صغيرة" أو "كبيرة" لتحسين واجهة عند قيامك بتشغيل تطبيق على هاتف أو جهاز أكبر، على التوالي.</span><span class="sxs-lookup"><span data-stu-id="40875-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 

<span data-ttu-id="40875-125">يمكنك أيضًا تحديد الكيانات القانونية التي سيكون أحد التطبيقات متوفرًا لها، أو يمكنك توفيرها لجميع الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="40875-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="40875-126">بشكل افتراضي، تتوفر تطبيقات PowerApps لجميع الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="40875-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="40875-127">فتح تطبيق</span><span class="sxs-lookup"><span data-stu-id="40875-127">Opening an application</span></span>
<span data-ttu-id="40875-128">عندما تنتهي من تكوين تطبيقات PowerApps المضمنة، ستتم إضافة ارتباطات خاصة بالتطبيقات التي حددتها إلى الصفحات داخل Talent.</span><span class="sxs-lookup"><span data-stu-id="40875-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="40875-129">انقر فوق ارتباط لفتح تطبيق.</span><span class="sxs-lookup"><span data-stu-id="40875-129">Click a link to open an application.</span></span> 


