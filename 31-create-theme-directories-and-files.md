---
description: إنشاء الفُلدر الخاص بالـوردبريس
---

# 31 Create Theme Directories and Files

هنبدأ مع بعض يجماعة إنشاء الـ Derictory **** أو الفلدر الخاص بالـTheme بتاعنا هنا ذى ما أحنا شايفين ذى الـThemes الموجوده الأصليه اللى بينزلة مع الـWordpress&#x20;

{% hint style="info" %}
C:\xampp\htdocs\wordpress\wp-content\themes
{% endhint %}

أنا هعمل Folder هنا فى المسار دا&#x20;

{% hint style="info" %}
C:\xampp\htdocs\wordpress\wp-content\themes
{% endhint %}

وليكن هسمية الـelzero داخل الـFolder دا هننشأ 2 file وهما

1. style.css
2. index.php

> بعد ما تنشأ الملفين دول هيظهللك فى الـThemes

![Themes](<.gitbook/assets/WordPress - create theme directories and files.png>)



## <mark style="color:blue;">داخل ملف الـindex.php هنكتب التالى</mark>

1. هنستدعى الـHeader دا الجزء العلوى من الصفحه اللى بيبقى فيه اللوجو و الـTagline
2. هنستدعى الـsearch form علشان يعملنا form
3. هنستدعى الـFooter لازم لازم لازم تستدعيه شوفت أنا قولتها كام مره حتى لو معندكش footer علشان متعملكش مشاكل

{% code title="index.php" %}
```php
<?php get_header(); ?>

This Is Content

<? php get_search_form(); ?>

<? php get_footer(); ?>
```
{% endcode %}

> ما تنساش تكتب Comment فوق كل Function الـFunction دى بتعمل 1 2 3 لأن دا مش هيوفر عليك بس لا هيوفر على الشخص اللى هيشترى منك الـTheme
