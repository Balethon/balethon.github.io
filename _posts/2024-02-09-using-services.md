---
categories: [Quick Start]
tags: []
---

<h1 align="right" dir="rtl">استفاده از سرویس ها</h1>

<p align="right" dir="rtl"><strong>توی این مقاله استفاده از سرویس های بله آموزش داده میشه</strong></p>

<p align="right" dir="rtl"><br/></p>

<h2 align="right" dir="rtl">نمونه سازی Client</h2>

<p align="right" dir="rtl">اول باید Client رو از داخل بلتون فراخوانی کنیم و یه Client بسازیم<br/>
من Client ساخته شده خودم رو توی متغیر bot ذخیره میکنم</p>

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here
```

<blockquote dir="rtl">
<p>باید «TOKEN» رو با توکن بات خودتون عوض کنید</p>
</blockquote>

<p align="right" dir="rtl"><br/></p>

<h2 align="right" dir="rtl">اتصال به بله</h2>

<p align="right" dir="rtl">حالا قبل از هر کاری اول باید باتمون رو به بله وصل کنیم</p>

```python
bot.connect()
```

<p align="right" dir="rtl"><br/></p>

<h2 align="right" dir="rtl">فراخوانی سرویس ها</h2>

<p align="right" dir="rtl">حالا میتونیم با بات خودمون از سرویس های بله استفاده کنیم<br/>
مثلا اطلاعات خود بات رو بگیریم و پرینتشون کنیم</p>

```python
me = bot.get_me()
print(me)
```

<p align="right" dir="rtl"><br/></p>

<p align="right" dir="rtl">یا یک پیامی به یک نفر بفرستیم</p>

```python
bot.send_message("@username", "Hello")  # Replace "@username" with your actual username here
```

<blockquote dir="rtl">
<p>باید «@username» رو با نام کاربری مورد نظر خودتون عوض کنید</p>
</blockquote>

<p align="right" dir="rtl"><br/></p>

<h2 align="right" dir="rtl">قطع اتصال از بله</h2>

<p align="right" dir="rtl">ولی با این روش باید یادمون باشه که بعد از تموم شدن کار اتصال بات رو با بله قطع کنیم</p>

```python
bot.disconnect()
```

<p align="right" dir="rtl"><br/></p>

<h2 align="right" dir="rtl">جمع بندی</h2>

<p align="right" dir="rtl">یعنی برای مثال کد کامل ما اینجوری میشه</p>

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here

bot.connect()
bot.send_message("@username", "Hello")  # Replace "@username" with your actual username here
bot.disconnect()
```

<p align="right" dir="rtl"><br/></p>

<h2 align="right" dir="rtl">کانتکست منیجر</h2>

<p align="right" dir="rtl">یه روش بهتر برای وصل کردن بات به بله استفاده از کانتکست منیجره</p>

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here

with bot:
    bot.send_message("@username", "Hello")  # Replace "@username" with your actual username here
```

<p align="right" dir="rtl">وقتی این شکلی انجام بدیم دیگه نیاز نیست خودمون اتصال با بله رو وصل یا قطع کنیم و خودکار انجام میشه<br/>
این روش پیشنهاد میشه چون حتی اگر کد به طور ناگهانی متوقف بشه قطع شدن ارتباط تضمینیه</p>

<p align="right" dir="rtl"><br/></p>

<h2 align="right" dir="rtl">برنامه نویسی Asynchronous</h2>

<p align="right" dir="rtl">یه کار دیگه که میتونیم بهتر انجام بدیم اینه که به صورت Asynchronous کد بزنیم</p>

```python
import asyncio

from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here


async def main():
    async with bot:
        await bot.send_message("@username", "Hello")  # Replace "@username" with your actual username here


asyncio.run(main())
```

<p align="right" dir="rtl">این روش پیشنهاد میشه چون از خاصیت برنامه نویسی Asynchronous بهره میگیریم و میتونه سرعت کدمون رو ببره بالا<br/>
اگر با برنامه نویسی Asynchronous آشنایی ندارید میتونید با همون روش ساده کد بزنید و مشکلی نداره</p>

<blockquote dir="rtl">
<p>اگر با برنامه نویسی Asynchronous آشنا باشید میدونید که یک کد Async باید حتما یک فانکشن ورودی داشته باشه</p>
</blockquote>

<blockquote dir="rtl">
<p>اگر از برنامه نویسی Asynchronous استفاده میکنید تمام سرویس های بله در بلتون رو هم باید به صورت Async فراخوانی کنید</p>
</blockquote>

<p align="right" dir="rtl">ولی کدمون هنوز هم قابل بهبود دادن هست</p>

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here


async def main():
    await bot.send_message("@username", "Hello")  # Replace "@username" with your actual username here


bot.run(main())
```

<p align="right" dir="rtl">اینجا به‌جای asyncio.run از bot.run استفاده کردیم تا کدمون خلاصه تر بشه<br/>
اینجوری هم خود بلتون قبل از اجرای main بات رو برای ما به بله وصل میکنه و بعد از تموم شدن کار اتصال رو قطع میکنه<br/>
توی این روش هم مثل کانتکست منیجر قطع ارتباط خودکار تضمینیه</p>

<br>

<p align="center" dir="rtl">پست قبلی: <a href="https://balethon.ir/posts/installing">Installing</a></p>

<p align="center" dir="rtl">پست بعدی: <a href="https://balethon.ir/posts/handling-updates">Handling Updates</a></p>