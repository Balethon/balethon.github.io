---
categories: [What Is Balethon]
tags: []
---

<h2 align="right" dir="rtl">بلتون توسعه پذیر است</h2>

<p align="right" dir="rtl">تمام سیستم های بلتون به سادگی قابل توسعه دادن هستن</p>

<h3 align="right" dir="rtl">اونت هندلرها</h3>

<p align="right" dir="rtl">قابلیت ایجاد اونت هندلرهای کاستوم توی بلتون وجود داره</p>

<p align="right" dir="rtl">برای مثال فرض کنید میخوایم یک مسیج هندلر داشته باشیم ولی این مسیج هندلر تعداد بارهایی که کلمه «بلتون» داخل متن پیام به کار گرفته شده رو بشماره، اگر تعداد از 2 بار کمتر بود به پیام رسیدگی نکنه و اون تعداد رو هم داخل فانکشن کالبک در اختیار ما بذاره</p>

```python
from balethon.event_handlers import MessageHandler


class BalethonMessageHandler(MessageHandler):
    def __init__(self, callback, condition=None):
        super().__init__(callback, condition)
        self.balethon_count = 0

    async def check(self):
        if self.balethon_count < 2:
            return False
        return await super().check()

    async def __call__(self, *args, **kwargs):
        return super().__call__(*args, balethon_count=self.balethon_count, **kwargs)
```

<p align="right" dir="rtl">یک کلاس به اسم <code>BalethonMessageHandler</code> ساختیم که از مسیج هندلر ارث بری میکنه چون میخوایم مسیج هندلر مخصوصمون رو داشته باشیم<br/>
شما میتونید از هر اونت هندلری که بخواید ارث بری کنید</p>

<p align="right" dir="rtl">حالا برای اینکه از هندلر کاستوممون استفاده کنیم</p>

<p align="right" dir="rtl">به روش داینامیک:</p>

```python
async def callback(message, balethon_count):
    ...


bot.add_event_handler(BalethonMessageHandler(callback, condition))
```

<p align="right" dir="rtl"><br/></p>

<p align="right" dir="rtl">به روش دکوراتور:</p>

```python
@bot.add_event_handler(BalethonMessageHandler, callback, condition)
async def callback(message, balethon_count):
    ...
```
