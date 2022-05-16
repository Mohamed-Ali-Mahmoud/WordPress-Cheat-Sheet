# 36 WP Enqueue Script Function

الدرس إنهارده يجماعة إن شاء الله هيتكلم عن ازاى اضيف الـ Script ذى ما عملت فى الـStyle بالظبط

الموضوع هيكون إن شاء الله هو هو مع أختلافات طفيفه جداً هتخلى الدرس بأذن الله أسرع بكتير .



{% hint style="info" %}
[ttps://developer.wordpress.org/reference/functions/wp\_enqueue\_script/](https://developer.wordpress.org/reference/functions/wp\_enqueue\_script/)
{% endhint %}

### <mark style="color:blue;">**wp\_enqueue\_script Function**</mark>

```php
wp_enqueue_style(

    string $handle,
    string  $src='',
    String[] $deps = array(),string|bool|null 
    $ver = false,
    bool $in_footer = false
)
```

الـ**Function** دى فيها كل حاجه ذى الـ **wp\_enqueue\_style** اللى أحنا شرحنها فى الدرس اللى فات على طول

### <mark style="color:blue;">**in\_footer**</mark>

* &#x20;دى لو خلتها True هتخليلى الـScript اللى عملتلها Include قبل قفلة وسم الـ`<body/>`

```php
<?php 

/*
   **Function To Add My Custom Styles
    **Add By @Mohamed_Ali
    **wp_enqueue_style();
*/

function mohamed_add_styles() {
   // هنا هيضيف الـcss    
    wp_enqueue_style('bootstrap-css', get_template_directory_uri() . "/css/bootstrap.min.css");
    wp_enqueue_style('font-Awesome-css', get_template_directory_uri() . "/css/fontawesome.min.css");
}

/*
   **Function To Add My Custom Script
    **Add By @Mohamed_Ali
    **wp_enqueue_style();
*/

function mohamed_add_script() {

    //Add Bootstrap JS File 
 // هنا هيضيف الـjs    
    wp_enqueue_script
    (
        // Name File It's Up To You 
        'bootstrap-js', 
        // Get Theme Path Directory 
        get_template_directory_uri() 
        // Src File , // True For In Footer 
        . "/js/bootstrap.min.js", array(), false, true 
    );

    //Add Font Awesome JS File 
    wp_enqueue_script(
        // Name File It's Up To You 
        'fontawesome-js', 
         // Get Theme Path Directory 
        get_template_directory_uri() 
         // Src File , True For In Footer 
        . "/js/fontawesome.min.js", array(), false, true 
    );
}
```



