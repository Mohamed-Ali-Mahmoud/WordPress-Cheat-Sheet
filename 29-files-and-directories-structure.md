---
description: البنية الملفات الخاصة بالـوردب
---

# 29 Files and Directories Structure

&#x20;هنتكلم النهاردة يجماعة إن شاء الله عن البنية الخاصة بالملفات والفلدرات الموجوده فى الـWordpress

هناخد شوية معلومات عنهم هنعرف شويه Tricks بسيطة قبل ما ندخٌل بإذن الله فى التصميم وقبل ما نبدأ نصمم الـPrimuem Theme بتاعنا وننشأ الفلدر بتاعة



### <mark style="color:blue;">الـ Wordpress فيها 3 Folder</mark>

1. wp-admin
2. wp-content
3. wp-include

{% hint style="info" %}
دا المسار  C:\xampp\htdocs\wordpress
{% endhint %}

{% tabs %}
{% tab title="wp-include" %}
* إى حد شاف كورس برمجة و شاف كورس الـE-COMMERCE فى القناه عارفيين يعنى ايه Include فى الـPHP بعمل Include لمكتبات او file هينفعنى فى الشغل
* هنا فيها نفس الفكرة الـwp-include فيها الحاجات اللى بتستعملها فى الـWordpress كلها علشان تطلعلك الـApplication الجميل بتاعك دا .
* فى حاجه فيهم بس هنبُص عليها تحت خالص وهى إسمها version.php.
* حصل كتير وفى مواقع اخترقت وكان صاحب الموقع معيرفش الأصدار الخاص بالموقع كام وتعب جدا فى الموضوع دا وكان عنده مشكلة !
* &#x20;ف لو في يوم من الأيام لقيت موقع Wordpress مخترق والشخص اللى أخترقة او صاحب الموقع مش عارف يجيب الأصدار وتعبت انت هنا جوه ملف الـVersions هتلاقى رقم الأصدار



![version.php](<.gitbook/assets/wordPress - file struture - wp\_content.png>)

#### <mark style="color:blue;">طيب حد ممكن يقولى وأنا هعمل اية بأصدار الـWordpress أنا ؟</mark>

الملفات كلها أتشفرت الملفات كلها دخل فيها أكواد خبيثة ممكن تخترق الموقع تانى وتالت ورابع وأنا عاوز أستبدلها بـ Fresh Copy جديدة نظيفة طب ازاى أجيب الـVersion المناسب فبدخل على الملف دا هعرف الأصدار فانزلة من الموقع وارفع الملفات على القديمة اعملها override فبقت سليمه وابدأ بقا أتعامل مع الـDatabase

طيب جوا الـInclude هتلاقى حاجه أسمها Widgets فيها كل الـWidgets



{% hint style="info" %}
C:\xampp\htdocs\wordpress\wp-includes\widgets
{% endhint %}
{% endtab %}

{% tab title="wp-admin" %}
الـ **wp-admin** فى كل الحاجات اللى تخص الـAdmin او لوحة التحكم


{% endtab %}

{% tab title="wp-content" %}
* &#x20;الـ**wp-content** هو اللعب بتعانا كلة بقا هنا احنا شغلنا كلة موجود هنا هتلاقى بداخلة Folder الـPlugins فيه كل البلجين اللى انتا بتركبها و folder الـThemes فى كل الثيمات اللى انتا حملتها و folder الـLanguages طبعا لو ملقتش الفلدر دا تقدر تعملو بنفسك ممكن بسبب التراخيص النسخه مش عارفه تنشأها ما دام أنت داخل الـwp-content اطمن مفيش مشكلة
{% endtab %}
{% endtabs %}









