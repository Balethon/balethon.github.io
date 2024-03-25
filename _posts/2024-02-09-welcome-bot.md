---
categories: [Examples]
tags: []
---

<h1 align="right" dir="rtl">بات خوش آمد گویی</h1>

<p align="right" dir="rtl"><strong>این بات رو توی یه گروه عضو کنید تا به اعضای جدید پیام خوش آمد گویی بفرسته</strong></p>

```python
from balethon import Client
from balethon.conditions import new_chat_members

bot = Client("TOKEN")


@bot.on_message(new_chat_members)
async def welcome_new_chat_members(message):
    members = [member.full_name for member in message.new_chat_members]
    await message.reply(
        f"Hello {', '.join(members)}, welcome to {message.chat.title}!"
    )


bot.run()
```

<br>

<p align="center" dir="rtl">پست قبلی: <a href="https://balethon.ir/posts/inline-keyboards-bot">Inline Keyboards Bot</a></p>

<p align="center" dir="rtl">پست بعدی: <a href="https://balethon.ir/posts/payment-bot">Payment Bot</a></p>