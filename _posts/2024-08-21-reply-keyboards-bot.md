---
categories: [Examples]
tags: []
---

<h2 align="right" dir="rtl">بات ریپلای کیبوردها</h2>

<p align="right" dir="rtl"><strong>به این بات یک پیام بدهید تا یک پیام همراه با کیبورد به شما بفرستد<br/>
سپس روی دکمه ها کلیک کنید</strong></p>

```python
from balethon import Client
from balethon.conditions import private, equals
from balethon.objects import ReplyKeyboard

bot = Client("TOKEN")


@bot.on_message(private & equals("Button 1", "Button 2"))
async def answer_buttons(message):
    await message.reply(
        f"Thank you for clicking on button {message.text}"
    )


@bot.on_message(private)
async def answer_message(message):
    await message.reply(
        "Click a button!",
        ReplyKeyboard(
            ["Button 1"],
            ["Button 2"]
        )
    )


bot.run()
```