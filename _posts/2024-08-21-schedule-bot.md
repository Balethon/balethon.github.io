---
categories: [Advanced Examples]
tags: []
---

<h1 align="right" dir="rtl">بات برنامه ریزی</h1>

<p align="right" dir="rtl"><strong>این بات علاوه بر اینکه جواب پیام های شما رو میده، برنامه ریزی شده تا هر دقیقه توی یک چت یک پیام ارسال کنه</strong></p>

```python
from asyncio import sleep

from balethon import Client

bot = Client("TOKEN")

CHAT_ID = 1234567890


@bot.on_initialize()
async def task(client):
    while True:
        await client.send_message(CHAT_ID, "Some scheduled message...")
        await sleep(60)


@bot.on_message()
async def answer_message(message):
    await message.reply("Hello I'm the schedule bot")


bot.run()
```