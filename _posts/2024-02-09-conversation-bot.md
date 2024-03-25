---
categories: [Examples]
tags: []
---

<h1 align="right" dir="rtl">بات گفتگو</h1>

<p align="right" dir="rtl"><strong>به این بات یه پیام بدید تا گفتگو رو با شما شروع کنه</strong></p>

```python
from balethon import Client
from balethon.conditions import at_state

bot = Client("TOKEN")


@bot.on_message(at_state(None))
async def home_state(message):
    await message.reply(
        "Hello, I'm the conversation bot\nWhat is your name?"
    )
    message.author.set_state("NAME")


@bot.on_message(at_state("NAME"))
async def name_state(message):
    name = message.text
    await message.reply(
        f"Nice to meet you, {name}!\nHow old are you?"
    )
    message.author.set_state("AGE")


@bot.on_message(at_state("AGE"))
async def age_state(message):
    age = message.text
    await message.reply(
        f"You are {age} years old, good for you!\nHave a nice day!"
    )
    message.author.del_state()


bot.run()
```


<br>

<p align="center" dir="rtl">پست قبلی: <a href="https://balethon.ir/posts/commands-bot">Commands Bot</a></p>

<p align="center" dir="rtl">پست بعدی: <a href="https://balethon.ir/posts/client">Client</a></p>