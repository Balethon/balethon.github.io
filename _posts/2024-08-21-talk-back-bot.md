---
categories: [Advanced Examples]
tags: []
---

<h1 align="right" dir="rtl">بات حاظر جواب</h1>

<p align="right" dir="rtl"><strong>به این بات یکی از متن های تعریف شده رو بفرستید تا جواب بده<br/>
و قابلیت یادگیری با استفاده از دستور مثل زیر رو داره:<br/>
/learn text reply</strong></p>

```python
from balethon import Client

bot = Client("TOKEN")

replies = {
    "hello": "Hi",
    "hi": "Hey!",
    "how are you": "Fine thanks! And You?",
    "bot": "Yes, how can I help you?",
    "haha": "What's so funny?",
    "bye": "Good bye!"
}


@bot.on_command()
async def start(*, message):
    texts = "\n".join(replies)
    await message.reply(
        f"Send one of the following texts to me and I will reply:\n{texts}"
    )


@bot.on_command()
async def learn(text, reply, *, message):
    replies[text] = reply

    await message.reply(
        f"I got it\nWhen someone says {text}, I say {reply}"
    )


@bot.on_message(lambda client, event: event.text in replies)
async def reply_to_text(message):
    await message.reply(replies[message.text])


bot.run()
```