# 32 Dig Deep Into Blog Info Function

النهاردة يجماعة إن شاء الله هنرفع صورة الـTheme بتاعنا علشان ذى ما أنتو شايفين ملهوش أى صورة وهنعرف على Function مهمة إسمها Blog Info الـFunction دى فيها معلومات كتيرة هتفيدناو أحنا بننشأ الـDesign بتاعنا بأذن الله

أول حاجه مطلوب منك أن أنت تعمل صورة للـTheme اى مقاس هى كده كده بتتحجم لـ 402\*302 بس أنا بلنسبالى عملت صورة 900\*1200.

هنضيف الصورة داخل folder الـzero فى folder الـTheme

{% hint style="info" %}
C:\xampp\htdocs\wordpress\wp-content\themes\elzero .
{% endhint %}

{% hint style="danger" %}
لاحظ لو صورة الـTheme مظهرتش معاك خلى إسمها screenshot.png وأعمل Refrash
{% endhint %}

![](<.gitbook/assets/WordPress - dig deep into blog function.png>)

### <mark style="color:blue;">Blog Info Function</mark>

طيب نروح نبص على الـFunction اللى إسمها _**Blog Info**_ بتطبعلنا أية

```php
bloginfo( string $show = '' )
```

1. الـName الـموجود فى الـSettings داخل الـGeneral اللى هو الـSite Title
2. بتجيب الـDescription الـموجود فى الـSettings داخل الـGeneral اللى هو الـTagline

```php
<?php get_header();?>

This Is Content
<?php get_search_form(); ?>

<?php bloginfo("name");?>
<br/>
<?php bloginfo("description");?>

<?php get_footer();?>
```

\


##

\
