---
categories: [Why Balethon]
tags: []
---

<h2 align="right" dir="rtl">بلتون شهودی است</h2>

<p align="right" dir="rtl">اگر از یک کد ادیتور خوب استفاده کنید که از زبان برنامه نویسی پایتون به خوبی پشتیبانی میکنه حتماً موقع کدنویسی با بلتون میتونه به شما کمک کنه</p>

<p align="right" dir="rtl">دلیلش اینه که type-hint ها در کد بلتون به کار گرفته شدن، که به ادیتور اجازه میدن بهتر کد رو درک کنه و بتونه موقع کدنویسی پیشنهادهای بهتری به شما نشون بده</p>

<h3 align="right" dir="rtl">تذکر در کالبک</h3>

<p align="right" dir="rtl">اما یه جاهایی هست که ممکنه ادیتور نتونه پیشنهادهای خوبی به شما ارائه بده
مثلاً این کد رو در نظر بگیرید</p>

```python
from balethon import Client

bot = Client("TOKEN")


@bot.on_message()
async def answer_message(client, message):
    message.
    client.
```

<p align="right" dir="rtl">اینجا ما وقتی بنویسیم <code>message.</code> یا <code>client.</code> ادیتور پیشنهاد خوبی به ما نمیده بخاطر اینکه نمیدونه این <code>message</code> و <code>client</code> چه نوع آبجکت هایی هستن</p>

<p align="right" dir="rtl">راه حلش اینه که به این شکل بنویسیم</p>

```python
from balethon import Client
from balethon.objects import Message

bot = Client("TOKEN")


@bot.on_message()
async def answer_message(client: Client, message: Message):
    message.
    client.
```

<p align="right" dir="rtl">اینجا ما خودمون اومدیم صرفاً مشخص کردیم که <code>client</code> یک آبجکت از نوع <code>Client</code> و <code>message</code> یک آبجکت از نوع <code>Message</code> هست و با این کار ادیتور متوجه نوع این آبجکت ها میشه و میتونه به ما پیشنهادهای مفیدی موقع کد زدن بده</p>