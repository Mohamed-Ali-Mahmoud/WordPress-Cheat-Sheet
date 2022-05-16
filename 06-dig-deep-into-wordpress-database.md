---
description: التعمق فىقاعدة البيانات
---

# 06 Dig Deep Into WordPress Database

> النهارده يا جماعة هنعمل جولة داخل الـDatabase بتاعة الـwordpress هناخد فكرة عن الجداول وكل جدول بيتخزن فيه اية ونعرف امتى الحالات اللى ممكن ادخل بيها على الـDatabase بنفسى&#x20;
>
> واعدل فيها من غير ما ادخل على لوحه التحكم

ندخل على الـDatabase اولا أضغط على اللينك&#x20;

{% hint style="info" %}
&#x20;[http://localhost/phpmyadmin/](http://localhost/phpmyadmin/)&#x20;
{% endhint %}

![PHP My Admin ](<.gitbook/assets/WordPress - Database.png>)

قبل ما نقول اى حاجه هنقول امتى محتاج ادخل على الـDatabase بتاعتى ؟!

> تخيل معايا انا اخدت ويب سايت من عميل وعاوز يطورة وكان مخترق وعاوز اشيل منه الأكواد الضاره وعاوز اغير باسورد الأدمن لأنى معرفش مين الأدمن ولا أسمه ولا إيميلة بتحتاج انى ادخل هنا انت معكش بيانات عشان تدخل لوحه التحكم ولا معاك username ولا password

### &#x20;<mark style="color:blue;">جدول الـ wp\_user</mark>

![](<.gitbook/assets/wordPress - wp\_user.png>)

> داخل الـ wp\_user تقدر تغييير الـpassword أقدر اغير الـEmail

![](<.gitbook/assets/wordPress - wp\_user edit.png>)

### <mark style="color:blue;">جدول الـ wp\_posts</mark>

> تخيل معايا الشخص اللى اخترق الموقع دا كتب اسمه فى كل المقالات تقدر عن طريق أمر من أوامر الـ Sql وهو الـreplace تمسح اسمه وتستبدلة

> تخيل معايا لو عندك 40 الف مقال هتروح تعدلهم من اللوحه طبعا مستحيل

![](<.gitbook/assets/wordPress - wp\_post.png>)

### <mark style="color:blue;">جدول الـ wp\_comments و wp\_commentmeta</mark>

> يتكلمة عن التعليقات كل مقال انت بتكتبة فيه ناس ممكن تعلق علية التعليق دا بيكون مرتبط بالبوست الى انت كاتبتها



### <mark style="color:blue;">جدول الـ wp\_option</mark>&#x20;

> دا عن طريقة تقدر تغيير اسم الموقع و الـ url الخاص بالموقع وحجات تانية كتير

![مثلا هغير الـblogname بدل Mohamed Ali الى Mo Ali](<.gitbook/assets/wordPress - wp\_option.png>)

> لاحظ هنا الTitle الخاص بالويب سايت Mohamed Ali لما اغيره فى الـblogname الى Mo Ali واعمل Refresh هيتغير الى Mo Ali

![](<.gitbook/assets/wordPress - wp\_option change title.png>)

### <mark style="color:blue;">جدول الـ wp\_terms و Wp\_termsmeta</mark>

> عبارة عن الأقسام الـCategorize والـTags

### <mark style="color:blue;">**جدول الـ wp\_term\_relationships**</mark>

> بيربط الـTags بالـCategorize بالـTag بالـpost

> مثلا عندنا الـobject\_id = 5 و term\_taxonomy\_id = 2 (التصنيف)

![](<.gitbook/assets/wordPress - wp\_term\_relationships.png>)

> دا معناه اية?! اية الأرقام دى 5 و 1 دا معناه ان عندنا بوست الـpost\_id = 5 ومربوط بـ Categorise الـid الخاص بيها = 2

انا هنا عامل post اسمو Learn React وعطيلو Categories اسمها react

![تعالا نضغط على على Learn React وكأننا هنعدل المقال](<.gitbook/assets/wordPress - Learn React.png>)

![لاحظ هنا ان الـpost دا الـid الخاص بيه 5 ودا الى مكتوب فى الـwp\_term\_relationships](<.gitbook/assets/wordPress - post\_id.png>)

> طب اية رقم 2 الموجود فى الـtoxonomy ?! دا ليه علاقة بالـCategorise
>
> تعالا نفتح الـCategorise وندخل على react categorise

![تعالا نضغط على كلمة react ونشوف كأننا هنعدلها](<.gitbook/assets/wordpress - categories.png>)

![لاحظ هنا ان الـCatogries دا الـid الخاص بيها 2 ودا الى مكتوب فى الـwp\_term\_relationships](<.gitbook/assets/wordPress - categories id.png>)

> <mark style="color:blue;">**فى النهاية هقول كلمة مهمة جدا جدا عن الدرس دا ممكن يكون بالنسبه للناس صعب جدا وممكن بالنسبه لناس هايف جدا الخلاصة فى الموضوع متخدش الدرس دا على محمل الجد ان هو حاجه لازم افهما وافهم اية العلاقة ما بين الجداول ممكن تعيش حياتك لحد ما تموت محترف الوردبريس متعرفش حاجه عن الجداول لاكن انت كمبرمج المفروض ان انت تبقى فاهم يعنى ايه علاقات ما بين الجداول**</mark>
