---
categories: [Examples]
tags: []
---

<h1 align="right" dir="rtl">بات پرداخت</h1>

<p align="right" dir="rtl"><strong>به این بات یه پیام بدید تا یه پیام دارای صورتحساب به شما بفرسته<br/>
بعد میتونید مبلغی رو توسط اون پرداخت کنید</strong></p>

```python
from balethon import Client
from balethon.conditions import private
from balethon.objects import LabeledPrice

bot = Client("TOKEN")

PROVIDER_TOKEN = "6037************"


@bot.on_message(private)
async def send_invoice(client, message):
    await client.send_invoice(
        chat_id=message.chat.id,
        title="Some title",
        description="Some description",
        provider_token=PROVIDER_TOKEN,
        prices=[LabeledPrice(label="Some label", amount=1000000)]
    )


@bot.on_pre_checkout_query()
async def show_pre_checkout_query(pre_checkout_query):
    user = pre_checkout_query.author.full_name
    payload = pre_checkout_query.invoice_payload
    print(f"{user} paid {payload}")


bot.run()
```

<br>

<p align="center" dir="rtl">پست قبلی: <a href="https://balethon.ir/posts/welcome-bot">Welcome Bot</a></p>

<p align="center" dir="rtl">پست بعدی: <a href="https://balethon.ir/posts/mandatory-membership-bot">Mandatory Membership Bot</a></p>