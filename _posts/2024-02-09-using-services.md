---
categories: [Quick Start]
tags: []
---

<h1 align="right" dir="rtl">استفاده از سرویس ها</h1>

<p align="right" dir="rtl">توی این مقاله استفاده از سرویس های بله آموزش داده میشه</p>

<p align="right" dir="rtl">اول باید یه Client بسازیم</p>

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here
```

<br>

<p align="right" dir="rtl">حالا قبل از هر کاری اول باید باتمون رو به بله وصل کنیم</p>

```python
bot.connect()
```

<br>

<p align="right" dir="rtl">
حالا میتونیم با بات خودمون از سرویس های بله استفاده کنیم<br>
مثلا اطلاعات خود بات رو بگیریم و پرینتشون کنیم
</p>

```python
me = bot.get_me()
print(me)
```

<br>

<p align="right" dir="rtl">یا یک پیامی به یک نفر بفرستیم</p>

```python
bot.send_message("@username", "Hello")  # Replace "@username" with your actual username here
```

<br>

<p align="right" dir="rtl">ولی با این روش باید یادمون باشه که بعد از تموم شدن کار اتصال بات رو با بله قطع کنیم</p>

```python
bot.disconnect()
```

<br>

<p align="right" dir="rtl">یعنی برای مثال کد کامل ما اینجوری میشه</p>

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here

bot.connect()
bot.send_message("@username", "Hello")  # Replace "@username" with your actual username here
bot.disconnect()
```

<br>

<p align="right" dir="rtl">یه روش بهتر برای وصل کردن بات به بله هست</p>

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here

with bot:
    bot.send_message("@username", "Hello")  # Replace "@username" with your actual username here
```

<p align="right" dir="rtl">
وقتی این شکلی انجام بدیم دیگه نیاز نیست خودمون اتصال با بله رو قطع کنیم و خودکار قطع میشه<br>
این روش پیشنهاد میشه چون حتی اگر کد به طور ناگهانی متوقف بشه قطع شدن ارتباط تضمین شده
</p>