# 34 Create The Function PHP File

درس النهارده يجماعة إن شاء الله هيكون عباره عن نقاش و بسيط جداً و هنعمل شوية Edits كده فى لوحة التحكم عشان تسهلنا الأمور ونشوف الـTheme كامل ونشوف أكودنا قدام عنينا وهى بتظهر للنور .

فى طلب عاوز أطلبة قبل أى حاجه ♥ أحنا دلوقتى لما بنيجى نعمل أى Desgin فى الدنيا بجهز المكتبات بتعتى سواء Bootstrap او Font Awesome , jQuery , Px-Slider كل المكتبات اللى هتعامل بيها جوا الـDesign بجهزها عشان أحطها فى الـDesign بتاعى.



المطلوب منك علشان تتحدى نفسك وتطلع من الكورس إنسان محترف إنك تاخود بس من الكورس المعلومات لاكن الـDesign مطلعهوش ذى ما هو يعنى اية ؟! يعنى أنا عاوز تمشي فى Your On Way أمشى فى طريقك لوحدك لاكن أتعلم من الكورس أتعلم المعلومات وطبقها بطريقة تانية طبقها بـDesign مختلف بدل ما أنا أستعمل Bootstrap أستعمل أنت مثلا Fundation بدل ما أستعمل مكتبه الـIcon دى أستعمل واحده تانية ، غير كل شئ ، غير الألوان غير طريقة عرض الـHeader ، الـFooter كل حاجة أنا بعملها غيرها بس بعد ما تعرف وتتعلم المعلومات من الكورس الخلاصة من الموضوع أن أنا عاوزك تنطلق وتبدع مش تقلد الكورس وأخر الموضوع تقولى الـDesign اهو ذى ما أنت عاملو كده أنت مستفدش حاجة أتعلمت وبقيت كويس وفهمت الدنيا وطبقتها دى حاجه جمية جداً بس أنا عاوز الأجمل والأجمل وعايزين نقرب شويه من أن أنا أعمل الحاجه بنفسى يعنى مخليش الحاجه اللى أنا شوفتها تطلع هى هى لأ أنا عاوز أحط لمساتى الخاصة حتى لو طلعت وحشة مش مشكلة.



## <mark style="color:blue;">**functions.php**</mark>

> هنعمل مع بعض ملف الـ <mark style="color:blue;">**functions.php**</mark> طبعا داخل فلدر الـzero

{% hint style="info" %}
C:\xampp\htdocs\wordpress\wp-content\themes\elzero
{% endhint %}

> الملف دا هيكون فيه الـFunctions بتاعتك والـFunctions اللى بتتعامل مع الـWordpress ودى حاجه طبعاً من الحاجات الجميلة جداً أن الـWordpress بتدينى Function معينة أشتغل بيها علشان أطلع الـDesign بتاعى.

### <mark style="color:blue;">تجيهز المكتبات</mark>

{% hint style="info" %}
[<mark style="color:blue;">https://getbootstrap.com</mark>](https://getbootstrap.com)<mark style="color:blue;"></mark>

<mark style="color:blue;"></mark>[<mark style="color:blue;">https://fontawesome.com</mark>](https://fontawesome.com)<mark style="color:blue;"></mark>
{% endhint %}

هنضيف الملفات اللى أحنا حملنها للـBootstrap والـFont Awesome داخل folder جديد وهنسمية source مثلا داخل الـTheme اللى هو folder الـZero دا المسار

{% hint style="info" %}
&#x20;C:\xampp\htdocs\wordpress\wp-content\themes\elzero
{% endhint %}

![](<.gitbook/assets/WordPress - create the function php file.png>)



داخل folder الـ <mark style="color:blue;">**Bootstrap**</mark> فيه كذا folder أحنا مش محتاجين غير folder الـCss أو الـJs

داخل folder الـcss محتاجين file واحد هو bootstrap.min.css1

داخل folder الـjs محتاجين file واحد هو bootstrap.min.js



داخل folder الـ <mark style="color:blue;">**Font Awesome**</mark> فيه كذا folder أحنا مش محتاجين غير folder الـCss أو الـJs

داخل folder الـcss محتاجين file واحد هو fontawesome.min.css

داخل folder الـjs محتاجين file واحد هو fontawesome.min.js

> <mark style="color:blue;">بعد كدا هاخودهم وأضيفهم فى folder الـzero بره أحنا كنا بنرتبهم بس</mark>
>
> <mark style="color:blue;">ملحوظه وأنت بضيفهم بره فى folder الـzero ممكن تستغرب أن الـfolder فى المكتبتين شبه بعض لأ عادى مش هيحص مشاكل هيضفلك ملف الcss فيه ملفين واحد للـBootstrap وواحد للـ Font Awesome و folder الـ js هيعمل كدا برضة</mark>

{% hint style="info" %}
لو عاوز تلغى الـToolbar لما تعمل visit site من الـDashboard بيبقى فيه Toolbar فوق كده ممكن تلغيها من الـUser
{% endhint %}

<mark style="color:blue;">**وهنروح لملف**</mark><mark style="color:blue;">** **</mark>_<mark style="color:blue;">****</mark>_<mark style="color:blue;">** **</mark><mark style="color:blue;">**indexphp هنشيل منه الـget\_search\_form والـbloginfo**</mark>

{% code title="index.php" %}
```php
<?php get_search_form();?>

<?php bloginfo("name");?>

<br/>

<?php bloginfo("description");?>
```
{% endcode %}

{% code title="index.php" %}
```php

<?php get_header();?>

This Is Content

<?php get_footer();?>
```
{% endcode %}







