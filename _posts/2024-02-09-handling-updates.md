---
categories: [Quick Start]
tags: []
---

<h1 align="right" dir="rtl">رسیدگی به آپدیت ها</h1>

<p align="right" dir="rtl"><strong>توی این مقاله رسیدگی به آپدیت های فرستاده شده از طرف بله آموزش داده میشه</strong></p>

```python
from balethon.event_handlers import MessageHandler


def greet(message):
    message.reply("Hello")


bot.add_event_handler(MessageHandler(greet))
```

```python
@bot.on_message()
def greet(message):
    message.reply("Hello")
```

```python
@bot.on_message()
async def greet(message):
    await message.reply("Hello")
```

```python
from balethon import conditions


@bot.on_message(conditions.private)
def greet(message):
    message.reply("Hello")
```