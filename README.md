---
OpenSSH
---



<div dir="rtl">


پروتکل های مختلفی در سطح اینترنت و شبکه وجود دارند که می توان از آنها برای اتصال از راه دور میان سرور و کاربر استفاده کرد اما اکثر این پروتکل ها تفاوت های جزئی و کاربردی با یکدیگر دارند که مهم ترین این تفاوت ها ، سطح امنیت و رمزنگاری اطلاعات تبادلی به وسیله این پروتکل ها می باشد

 Secure Socket Shell یا  Secure Shell 
که SSH شناخته می شود از پروتکل های شبکه است و تحت پروتکل IEFT توسعه پیدا کرده که کاربران می توانند از آن در بستری امن به عنوان یک راه دسترسی به کامپیوتری دیگر استفاده کنند. Secure Shell وظیفه تایید هویت و رمزگذاری اطلاعاتی که در یک شبکه باز تبادل می شوند را بر عهده دارد.
 SSH امروزه بسیار کاربردی شده و مدیران شبکه می توانند از راه دور سیستم ها را مدیریت کنند ، دستورات خود را از راه دور وارد و اجرا کنند ، فایل ها را بین دو سیستم منتقل کنند و … . اصلی ترین تفاوتی که میان پروتکل SSH و سایر پروتکل ها مثل Telnet ، rLogin و … وجود دارد ، امنیت SSH و رمزگذاریی است که بر روی اطلاعات تبادل شده انجام می دهد. به کمک پروتکل SSH به راحتی می توان در یک بستر امن به ارتباط و تبادل اطلاعات میان Client و Server پرداخت.
 
 
 برای استفاده از SSH معمولا از سرویس ها و نرم افزار های ssh که امکان استفاده از قابلیت های SSH را فراهم می کنند ، استفاده می شود. نکته قابل ذکر این است که SSH بیانگر پروتکل است و ssh نشانه سرویس ها و نرم افزار های این پروتکل است.


 همانطور که در مورد وجود پروتکل های مختلف برای ارتباط سرور و کلاینت صحبت کردیم ، باید گفت که پروتکل SSH نسخه تکمیل و امن شده پروتکل Telnet می باشد که از پورت 22 استفاده می کند.
 
 از SSH برای ایجاد ارتباط با سیستم های لینوکسی به خصوص سرور ها استفاده می شود و از نرم افزار هایی که می توان از آن برای ارتباط تحت ویندوز با سرور های لینوکس استفاده کرد ، Putty می باشد. در لینوکس و مک نیز می توان به وسیله ترمینال ارتباط با SSH سرور را برقرار کرد.
 
 برخی از قابلیت های بارز SSH عبارت هستند از :
 
1- تایید هویت کاربر با روش های تایید مختلف
 
2-انتقال اطلاعات به صورت خودکار در بستری امن

3-امکان ارسال فرمان ها و دستورات از راه دور

4-مدیریت اجزای زیر ساخت شبکه به صورت امن

در مورد تایید هویت با SSH باید گفت که گزینه های مختلفی برای این مورد وجود دارد که رایج ترین آنها استفاده از SSH KEY یا Public Key است

پس از آن که پروتکل SSH به صورت انحصاری تبدیل شد ، در سال 1999 بسیاری از توسعه دهندگان که تمایل داشتند از SSH همچنان به عنوان یک نسخه منبع باز یا Open-source استفاده کنند ، به نسخه 1.2.12 که آخرین نسخه Open-source بود بازگشتند.

پس از این توسعه دهندگان OpenBSD اقدام به انتشار OpenSSH کردند که در حقیقت نسخه متن باز یا Open-source پروتکل SSH است و از سال 2005 به یکی از محبوب ترین نسخه های SSH تبدیل شده که به طور پیش فرض بر روی برخی از سیستم عامل ها عرضه می شود.

# پروتکل SSH چطور کار می کند

 جهت ارتباط با سرور SSH از پورت 22 که استاندارد TCP است ، استفاده می شود.
 
 SSH علاوه بر اجرای دستورات از راه دور ، از tunneling ، فوروارد پورت های TCP و اتصالات X11 پشتیبانی می کند و می تواند اطلاعات و فایل ها را با استفاده از پروتکل های SFTP یا CSP انتقال دهد.
 
 یک SSH client معمولا برای ایجاد اتصالات استفاده می شود و یک SSH daemon برای پذیرفتن اتصالات از راه دور که در اکثر سیستم عامل های امروزی مثل MacOS یا توزیع های GNU/Linux و OpenBSD ، FreeBSD ، NetBSD و OpenVMS به طور پیش فرض وجود دارند. همچنین از نسخه 1709 به بعد ویندوز SSH به طور پیش فرض وجود دارد.
 
 Secure Shell جایگزینی برای پروتکل ها و ترمینال های نا امن مثل Telnet و rlogin ایجاد شد و می تواند جایگزین پروتکل های انتقال فایل مثل FTP و rcp باشد و اساسی ترین استفاده آن برای اتصال از راه دور به یک هاست یا سرور لینوکس است.


فرم دستور اتصال به صورت ssh UserName@SSHserver.example.com است که SSHserver.example.com در حقیقت فرمان اتصال به سرور و UserName نام کاربری یا ID جهت اتصال است.

در صورتی که این اولین ارتباط بین کاربر و سرور باشد ، کاربر با استفاده از کلید عمومی می تواند درخواست اتصال کند و در صورتی برقرای اتصال ، کلید میزبان در فایل known_hosts سیستم ذخیره می شود و برای دفعات بعدی دیگر بدون نیاز به تایید دوباره اتصال برقرار می شود زیرا کلید میزان یا host key اتصال را تایید می کند.



#  نحوه تبدیل فایل Markdown به PDF
در ویندوز وارد cmd می شویم
سپس وارد دایرکتوری فایل Markdown شده 
و دستور زیر را می زنیم


 </div>
 
> pandoc -t beamer OpenSSH.md -o OpenSSH_slides.pdf