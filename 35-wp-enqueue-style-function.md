# 35 WP Enqueue Style Function

هنبدأ مع بعض يجماعة إن شاء الله مرحلة إضافة الـStyle ومرحلة أضافة الـJs بالطريقة الخاصة بالـWordPress

علشان تفهم الفكرة بتم ازاى أحنا بنعمل **Function** بتضيف ملفات الـStyle و **Function** بتضيف ملفات الـJs وبنستعمل حاجه إسمها Action أو Hook بتضفلنا الحاجات دى جوا الـWordPress كل حاجه من دى هنتكلم عنها بالتفصيل المفصل لاكن عاوزين دلوقتى نمشي واحدة واحدة وأمشى بالطريقة الصحيحه اللى متلغبطنيش

<mark style="color:blue;"></mark>

## <mark style="color:blue;">wp\_enqueue\_style</mark>

```php
wp_enqueue_style(
    string $handle,
    string $src='',
    String[] $deps=array(),
    string|bool|null  $ver = false,
    string $media = ' all ' 
)php
```

### <mark style="color:blue;">Handle and Src</mark>

* هحتاج منك تعرف الـHandle اللى هو إسم الـStylesheet ( إسمة اللى أنت بتسمية بيه ) ممكن مثلا الـbootstrab تسمية bs ذى ما تحب والـSrc بتاع الملف بيجبلى مسار الملف

### <mark style="color:blue;">Depend On (deps)</mark>

* بتوريللك فى حاجه بتعتمد على حاجه فى الـStyles هنيجى نعمل مثال عليها لما نيجى نعمل الـChild Theme حالياً هنركنها شوية

### <mark style="color:blue;">Version ( Ver )</mark>

* الـ Version أو أصدار الـTheme دايماً بنشوف ناس بتعمل للـ Theme لو أنتو دايما بتشوفو دايما فى ملف الـStyle يبقى مكتوب فيه styles and v1 يعنى الـVersion = 1 الحركه دى بيعملوها بسبب الـCashing

### <mark style="color:blue;">Media</mark>

* الميديا دى خاصة بالـPrint ولا الـAll ولا الـScreen وهى خاصة بالـResponsive ويب سايت

{% hint style="info" %}
[https://developer.wordpress.org/reference/functions/wp\_enqueue\_style/](https://developer.wordpress.org/reference/functions/wp\_enqueue\_style/)
{% endhint %}



### <mark style="color:blue;">**get\_template\_directory\_uri Function**</mark>

* الـFunction دى بتجبلك المسار يعنى أيه الكلام دا

{% hint style="info" %}
يعنى بتجبلك المسار دا

**C:\xampp\htdocs\wordpress\wp-content\themes\elzero**
{% endhint %}

* **علشان تبدأ تدخل على الـFolder الى جواها مثلا folder الـcss اللى جواها**
* فا أحنا هنضيفها جوا ملف الـindex.php هى مش هتطبع أى حاجه بس هتوصلك للمسار بس

{% code title="index.php" %}
```php
<?php get_header();?>

This Is Content
<?php get_template_directory_uri() ?>

<?php get_footer();?>dex.php
```
{% endcode %}

طبعاً لو كتبت قبلها echo هطتطبع المسار دا

{% hint style="info" %}
**C:\xampp\htdocs\wordpress\wp-content\themes\elzero**
{% endhint %}

![](<.gitbook/assets/WordPress - wp enqueue style function.png>)



**C:\xampp\htdocs\wordpress\wp-content\themes\elzero**\
\
\
داخل ملف الـ **functions.php** اتفقنا أن الملف دا هيبقى فيه كل المكتبات اللى هنستخدمها والfunction اللى مديهالنا الـ WordPress و الـ Functions بتاعتنا

{% code title="functions.php" %}
```php
<?php 

/*
   **Function To Add My Custom Styles
    **Add By @Mohamed_Ali
    **wp_enqueue_style();
*/

function mohamed_add_styles() {

// أتفقنا أن الفنكشن دى بتقبل إسم الملف اياً كان هتسميه ايه و مسار الملف  wp_enqueue_style

    wp_enqueue_style('my-bootstrap', get_template_directory_uri() . "/css/bootstrap.min.css");
}
```
{% endcode %}



