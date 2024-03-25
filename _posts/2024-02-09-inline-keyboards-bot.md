---
categories: [Examples]
tags: []
---

<h2 align="right" dir="rtl">بات اینلاین کیبوردها</h2>

<p align="right" dir="rtl"><strong>به این بات یک پیام بدهید تا یک پیام دارای دکمه به شما بفرستد<br/>
سپس روی دکمه ها کلیک کنید</strong></p>

```python
from balethon import Client
from balethon.conditions import private
from balethon.objects import InlineKeyboard

bot = Client("TOKEN")


@bot.on_message(private)
async def answer_message(message):
    await message.reply(
        "Click a button!",
        InlineKeyboard(
            [("Button 1", "1")],
            [("Button 2", "2")]
        )
    )


@bot.on_callback_query()
async def answer_callback_query(callback_query):
    await callback_query.answer(
        f"Thank you for clicking on button {callback_query.data}"
    )


bot.run()
```

<br>

<p align="center" dir="rtl">پست قبلی: <a href="https://balethon.ir/posts/echo-bot">Echo Bot</a></p>

<p align="center" dir="rtl">پست بعدی: <a href="https://balethon.ir/posts/welcome-bot">Welcome Bot</a></p>