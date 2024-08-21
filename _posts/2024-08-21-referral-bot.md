---
categories: [Examples]
tags: []
---

<h1 align="right" dir="rtl">بات دعوت</h1>

<p align="right" dir="rtl"><strong>به این بات یک پیام بدهید تا لینک دعوت مخصوص شما را بفرستید<br/>
سپس با آن یک کاربر را به بات دعوت کنید</strong></p>

```python
from balethon import Client
from balethon.conditions import private

bot = Client("TOKEN")


@bot.on_command(private)
async def start(referrer, *, client, message):
    referrer = await client.get_chat(referrer)
    await message.reply(f"You were invited by {referrer}!")


@bot.on_message(private)
async def answer_message(*, client, message):
    referral_link = client.create_referral_link("start", message.author.id)
    await message.reply(
        f"Hello {message.author}\nyou can invite users to this bot using:\n{referral_link}"
    )


bot.run()
```
