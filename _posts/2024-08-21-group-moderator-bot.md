---
categories: [Advanced Examples]
tags: []
---

<h1 align="right" dir="rtl">بات مدیریت گروه</h1>

<p align="right" dir="rtl"><strong>یک بات مدیریت گروه ساده<br/>
اون رو توی گروهتون ادمین کنید<br/>
دارای قابلیت حذف لینک ها، حذف پیام ها و حذف ممبرها</strong></p>

```python
from balethon import Client
from balethon.conditions import reply, regex

bot = Client("TOKEN")


@bot.on_command()
async def start(*, message):
    await message.reply(
        "Hello I'm the group moderator bot\nI can delete links, delete messages and ban members"
    )


@bot.on_command(reply)
async def delete(*, message):
    await message.reply_to_message.delete()

    await message.reply("Deleted 1 message")


@bot.on_command(reply)
async def ban(*, message):
    await message.chat.ban_member(message.reply_to_message.chat.id)

    await message.reply(f"Banned {message.reply_to_message.chat}")


@bot.on_message(regex(r"(http|ftp|https):\/\/([\w_-]+(?:(?:\.[\w_-]+)+))([\w.,@?^=%&:\/~+#-]*[\w@?^=%&\/~+#-])"))
async def delete_links(message):
    await message.delete()


bot.run()
```