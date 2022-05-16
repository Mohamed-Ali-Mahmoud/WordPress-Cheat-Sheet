# 33 Create The Header PHP File

هنبدأ مع بعض يجماعة نعمل الملف الخاص بالـHeader ذى ما أقولنا الـBolg Info فى الدرس اللى فات أتعلمنا منه ممكن نطلع معلومات عاملة أزاى وهنشوف لأن معظم المعلومات دى هنستخدمها إن شاء الله فى ملف الـHeader

## [header.php](33-create-the-header-php-file.md)

> هننشأ ملف جديد وهنسمية header.php طبعا داخل folder الـzero

{% hint style="info" %}
C:\xampp\htdocs\wordpress\wp-content\themes\elzero
{% endhint %}

{% code title="header.php" %}
```php
<!DOCTYPE html >
// هنا بيضيفلنا اللغة
<html <?php language_attributes(); ?>>
    <head>
	 // هنا بيضيف لنا الـCharset اللى هو UTF-8
        <meta charset="<?php bloginfo('charset') ?>"/>
	  // هنا بيضيف لنا الـName اللى هى موجوده فى اSettigns داخل الـGeneral  
        <title><?php bloginfo('name'); ?></title>
        <link rel="pingback" href="<?php bloginfo('bingback_url')?>" />
// هنا بيضيف الـScript والـ Styles
        <?php wp_head();?>
    </head>
    <body>
    </body>
</html>
```
{% endcode %}

![](<.gitbook/assets/wordPress - create the header php file.png>)
