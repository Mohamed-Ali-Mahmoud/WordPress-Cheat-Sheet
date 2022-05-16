---
description: شرح تنصيب WordPress على الستضافة المحلية
---

# 04 Setup WordPress on Localhost



1. [Setup Xampp](04-setup-wordpress-on-localhost.md#1.-setup-xampp)
2. [Localhost](04-setup-wordpress-on-localhost.md#2.-localhost)
3. [Setup WordPress](04-setup-wordpress-on-localhost.md#3.-setup-wordpress)
4. [Database](04-setup-wordpress-on-localhost.md#4.-database)



Localhost على الـ WordPress للـ Setup بأن إحنا نعمل WordPress هنبدأ مع بعض اول الخطوات العميقة فى الـ

Web Server ويكون عندى Localhostعلشان يتم موضوع الـ

محتاجين برنامج يسطب لنا الـ PHP و الـ Server والـ Database

<mark style="color:blue;">****</mark>

* <mark style="color:blue;">**دى مجموعة من البرامج اللى هتسطب لى الـ PHP  و Database هنختار واحد بس**</mark>

<mark style="color:blue;">****</mark>

<mark style="color:blue;">**Lamp**</mark>   : ****&#x20;

* Linux ** **<mark style="color:blue;">**+**</mark>** ** Apache <mark style="color:blue;">**+**</mark>  MySql <mark style="color:blue;">**+**</mark>  PHP

<mark style="color:blue;">**MAMP**</mark> :&#x20;

* Mac <mark style="color:blue;">**+**</mark>  Apache <mark style="color:blue;">**+**</mark>  MySql <mark style="color:blue;">**+**</mark>  PHP

<mark style="color:blue;">**WAPM**</mark> :&#x20;

* Windows <mark style="color:blue;">**+**</mark> Apache <mark style="color:blue;">**+**</mark> MySql <mark style="color:blue;">**+**</mark> PHP

<mark style="color:blue;">**XAMPP**</mark> :&#x20;

* All OS <mark style="color:blue;">**+**</mark> Apache <mark style="color:blue;">**+**</mark>  MariaDB <mark style="color:blue;">**+**</mark> PHP <mark style="color:blue;">**+**</mark> PERL &#x20;



## <mark style="color:blue;">**1. Setup Xampp**</mark>

{% hint style="info" %}
**تقدر تحملة من هُنا** [**https://www.apachefriends.org/download.html**](https://www.apachefriends.org/download.html)****
{% endhint %}

> Mysql و Apache للـ Start اضغط على Setup بعد ما عملت
>
> localhostعشان تبدأ تشتغل عليهم هتدخل على مسار الـ



![Xampp Control Panel](.gitbook/assets/Xamp.png)

## <mark style="color:blue;">2. Localhost</mark>

* localhostعشان تبدأ تشتغل عليهم هتدخل على مسار الـ
* Browser يعنى لما نيجى نفتح الـ localhost المسار دا كلة يعتبر الـ C:\xampp\htdocsدا المسار

> localhost هنكتب كلمة

{% hint style="info" %}
Hyper Text Document الـكلمـة دي إختصار htdocs&#x20;
{% endhint %}

لو مثلاً داخل المسار دا  C:\xampp\htdocs عملت Folder إسمة Create تقدرت تدخل علية من الـBrowser بالشكل دا&#x20;

{% hint style="info" %}
localhost/create كدا folder بنضيف إسم الـ localhost بعد كلمة
{% endhint %}



## <mark style="color:blue;">3. Setup WordPress</mark>

{% hint style="info" %}
htdocsالـ folder داخل wordpress الـ folderأول حاجه هنعملها هنضيف
{% endhint %}

![](<.gitbook/assets/WordPress - setup - htdocs.png>)

{% hint style="info" %}
localhost/wordpress ونكتب browser تانى حاجه هنعملها هنفتح الـ
{% endhint %}



![setup عشان نبدأ نعمله wordpressالصورة بتوضح ان احنا دخلنا على ملف الـ ](<.gitbook/assets/wordpress - setup configration.png>)

let's go! أضغط على



## <mark style="color:blue;">4. Database</mark>

* phpmyadmin هنعملها داخل الـ

{% hint style="info" %}
localhost/phpmyadmin
{% endhint %}

* <mark style="color:blue;">**wordpress**</mark> وهنسميها <mark style="color:blue;">**database**</mark> هننشأ
* دا الترميز العالمى اللى مش هيعملك مشاكل <mark style="color:blue;">**utf8\_general\_ci**</mark>&#x20;

![Databaseالـ create علشان نـ Go أضغط على](.gitbook/assets/phpmyadmin.png)

&#x20; خامس حاجة هنروح نكمل خطوات الـwordpress بالشكل دا

* Database Host: localhost
* Username : root&#x20;
* Database Name : Wordpress



![submit أضغط على](<.gitbook/assets/WordPress Setup.png>)



![run installation هنضغط على connect وعمل database على check هنا عمل](<.gitbook/assets/run the instalation.png>)

*   هيطلب منك شوية بيانات بعد ما عملنا instalation

    * إسم الموقع&#x20;
    * log in إسم المستخدم هتحتاجة لما تعمل
    * log in كلمة المرور هتحتاجة برضو لما تعمل
    * الإيميل هتحتاجة لو حصل مشكلة او نسيت إسم المستخدم و الباسورد عشان ترجعة





![install wordpresss هنضغط على](<.gitbook/assets/wordpress - welcom screen.png>)

![loginأضغط على](<.gitbook/assets/wordpress - success (1).png>)



![بعد كده هيجبلك تسجيل الدخول وهيضفللك اسم المستخدم والباسورد اتوماتيك كل اللى عليك هتضغط على login](<.gitbook/assets/wordpress - login.png>)

![Dashboardودخلنا على الـ login كده الحمدلله عمل](<.gitbook/assets/wordpress - dashboard.png>)

