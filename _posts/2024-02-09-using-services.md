---
categories: [Quick Start]
tags: []
---

# استفاده از سرویس ها

توی این مقاله استفاده از سرویس های بله آموزش داده میشه

اول باید یه Client بسازیم

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here
```

حالا قبل از هر کاری اول باید باتمون رو به بله وصل کنیم

```python
bot.connect()
```

حالا میتونیم با بات خودمون از سرویس های بله استفاده کنیم

مثلا اطلاعات خود بات رو بگیریم و پرینتشون کنیم

```python
me = bot.get_me()
print(me)
```

یا یک پیامی به یک نفر بفرستیم

```python
bot.send_message("@username", "Hello")
```

ولی با این روش باید یادمون باشه که بعد از تموم شدن کار اتصال بات رو با بله قطع کنیم

```python
bot.disconnect()
```

یعنی برای مثال کد کامل ما اینجوری میشه

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here

bot.connect()
bot.send_message("@username", "Hello")
bot.disconnect()
```

یک روش بهتر برای وصل کردن بات به بله هست

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here

with bot:
    bot.send_message("@username", "Hello")
```

وقتی این شکلی انجام بدیم دیگه نیاز نیست خودمون اتصال با بله رو قطع کنیم و خودکار قطع میشه
این روش پیشنهاد میشه چون حتی اگر کد به طور ناگهانی متوقف بشه قطع شدن ارتباط تضمین شده