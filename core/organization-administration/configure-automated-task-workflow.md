---
title: "تكوين مهمة تلقائية في سير عمل"
description: "يوضح هذا الموضوع كيفية تكوين خصائص مهمة تلقائية."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5fbdfc037daec295028a9ac4ca4608f0abe84112
ms.lasthandoff: 03/31/2017


---

# <a name="configure-an-automated-task-in-a-workflow"></a>تكوين مهمة تلقائية في سير عمل

يوضح هذا الموضوع كيفية تكوين خصائص مهمة تلقائية.

لتكوين مهمة تلقائية في محرر سير العمل، انقر بزر الماوس الأيمن فوق المهمة، وثم انقر فوق **خصائص** لفتح الصفحة **خصائص**. ثم استخدم الإجراءات التالية لتكوين خصائص المهمة التلقائية.

## <a name="name-the-task"></a>تسمية المهمة
اتبع الخطوات التالية لإدخال اسم للمهمة التلقائية.

1.  في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.
2.  في حقل **الاسم**، أدخل اسمًا فريدًا للمهمة.

## <a name="specify-when-notifications-are-sent"></a>تحديد وقت إرسال الإخطارات
يمكنك إرسال الإخطارات إلى الأشخاص عند تشغيل مهمة تلقائية أو إلغائها. اتبع هذه الخطوات لتحديد الوقت الذي يتم فيه ارسال الإخطارات، والأشخاص الذين يتم إرسال الإخطارات إليهم.

1.  في الجزء الأيمن، انقر فوق **الإخطارات‬**.
2.  حدد خانة الاختيار إلى جانب الأحداث التي يجب إرسال الإخطارات بشأنها:
    -   **التنفيذ** – يتم إرسال الإخطارات عند تشغيل المهمة.
    -   **مُلغى‬** – يتم إرسال الإخطارات عند إلغاء المهمة.

3.  حدد الصف المتعلق بحدث قمت بتحديده في الخطوة 2.
4.  على علامة التبويب **نص الإخطار‬**، في مربع النص، أدخل نص الإخطار‬.
5.  لتخصيص الإخطار، يمكنك إدراج عناصر نائبة. يتم استبدال العناصر النائبة بالبيانات المناسبة عندما يظهر الإخطار للمستخدمين. اتبع هذه الخطوات لإدراج عنصر نائب:
    1.  في مربع النص، انقر في تخصيص الذي يجب أن يظهر فيه العنصر النائب.
    2.  انقر فوق **إدراج عنصر نائب**.
    3.  في القائمة التي تظهر ، حدد العنصر النائب المراد إدراجه.
    4.  انقر فوق **إدراج**.

6.  لإضافة ترجمات الإخطارات، اتبع الخطوات التالية:
    1.  انقر فوق **الترجمات**.
    2.  في الصفحة التي تظهر، انقر فوق **إضافة**.
    3.  في القائمة التي تظهر، حدد اللغة التي تستخدمها لإدخال النص.
    4.  في حقل **النص المترجم‬**، أدخل النص.
    5.  لتخصيص النص، يمكنك إدراج عناصر نائبة كما ورد في الخطوة 5.
    6.  انقر فوق **إغلاق**.

7.  على علامة تبويب **المستلم**، حدد الشخص الذي يتم إرسال الإخطارات إليه. حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية لهذا الخيار قبل الانتقال إلى الخطوة 8.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>خيار</th>
    <th>مستلمو الإخطارات</th>
    <th>الخطوات الإضافية</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>المشارك</td>
    <td>المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</td>
    <td><ol>
    <li>بعد تحديد <strong>المشارك</strong>، على علامة التبويب <strong>مستند إلى الدور</strong>، في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لإرسال الإخطارات إليه.</li>
    <li>في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لإرسال الإخطارات له.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>مستخدم سير العمل</td>
    <td>المستخدمون المشاركون في سير العمل الحالي</td>
    <td><ul>
    <li>بعد تحديد <strong>سير عمل المستخدم</strong>، على علامة التبويب <strong>سير عمل المستخدم</strong>، في قائمة <strong>سير عمل المستخدم</strong>، حدد مستخدمًا يشارك في سير العمل.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>المستخدم</td>
    <td>365 Dynamics Microsoft معينة للمستخدمين العمليات</td>
    <td><ol>
    <li>بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</li>
    <li><strong>المستخدمين المتاحين</strong> 365 Dynamics كافة المستخدمين عمليات تتضمن القائمة. حدد المستخدمين لإرسال الإخطارات لهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  كرر الخطوات من 3 إلى 7 لكل الأحداث التي قمت بتحديدها في الخطوة 2.


