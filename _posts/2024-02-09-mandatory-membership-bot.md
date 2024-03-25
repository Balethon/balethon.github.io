---
categories: [Examples]
tags: []
---

<h1 align="right" dir="rtl">بات عضویت اجباری</h1>

<p align="right" dir="rtl"><strong>به این بات یه پیام بدید<br/>
اگه عضو کانال مورد نظر نباشید از شما درخواست عضویت میکنه<br/>
اگه عضو باشید جواب شما رو میده</strong></p>

```python
from balethon import Client
from balethon.conditions import is_joined

bot = Client("TOKEN")

CHAT_ID = 1234567890


@bot.on_message(~is_joined(CHAT_ID))
async def not_joined(message):
    await message.reply("Please join our chat first")


@bot.on_message()
async def answer_message(message):
    await message.reply("Thank you for using this bot")


bot.run()
```

<br>

<p align="center" dir="rtl">پست قبلی: <a href="https://balethon.ir/posts/payment-bot">Payment Bot</a></p>

<p align="center" dir="rtl">پست بعدی: <a href="https://balethon.ir/posts/downloader-bot">Downloader Bot</a></p>