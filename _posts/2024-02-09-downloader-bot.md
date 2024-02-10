---
categories: [Examples]
tags: []
---

<h1 align="right" dir="rtl">بات دانلودر</h1>

<p align="right" dir="rtl"><strong>
این بات پیام هایی که فایل همراهشون دارن رو شناسایی میکنه و فایل رو دانلود میکنه<br>
فایل رو توی همون محلی که بات در حال اجراست ذخیره میکنه
</strong></p>

```python
from balethon import Client
from balethon.conditions import document

bot = Client("TOKEN")


@bot.on_message(document)
async def download_document(client, message):
    downloading = await message.reply("Downloading...")

    response = await client.download(message.document.id)

    mime_type = message.document.mime_type.split("/")[-1]
    file_format = mime_type.split(";")[0]
    with open(f"downloaded file.{file_format}", "wb") as file:
        file.write(response)

    await downloading.edit_text("Download completed")


bot.run()
```