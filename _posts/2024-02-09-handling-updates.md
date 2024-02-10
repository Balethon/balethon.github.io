---
categories: [Quick Start]
tags: []
---

<h1 align="right" dir="rtl">رسیدگی به آپدیت ها</h1>

<p align="right" dir="rtl"><strong>توی این مقاله رسیدگی به آپدیت های فرستاده شده از طرف بله آموزش داده میشه</strong></p>

<p align="right" dir="rtl">
آپدیت ها رویدادهایی هستن که توی بله اتفاق میفتن و بله خبرش رو به بات شما میده<br>
مثلا وقتی یک نفر یک پیامی به بات شما بده بله اطلاعات اون پیام رو به شما میده تا بتونید بهش رسیدگی کنید
</p>

<p align="right" dir="rtl">
اونت هندلرهای بلتون به شما کمک میکنن که به آپدیت ها رسیدگی کنید و در ادامه استفاده از اون ها آموزش داده میشه
</p>

<br>

<h2 align="right" dir="rtl">افزودن اونت هندلر</h2>

```python
from balethon.event_handlers import MessageHandler


def greet(message):
    message.reply("Hello")


bot.add_event_handler(MessageHandler(greet))
```

<p align="right" dir="rtl">
خب اینجا ما اول اومدیم <code>MessageHandler</code> رو از بلتون فراخوانی کردیم<br>
چون میخوایم اونت هندلرمون به آپدیت های از نوع پیام رسیدگی کنه<br>
بعد یه فانکشن تعریف کردیم که یه ورودی به نام message میگیره<br>
اون همون پیامیه که باتمون قراره بهش رسیدگی کنه<br>
و بعد کدی که داخل این فانکشن مینویسیم تصمیم میگیره که بات چطوری به این پیام رسیدگی کنه<br>
در آخر هم با <code>bot.add_event_handler</code> اونت هندلرمون رو اضافه میکنیم<br>
<code>MessageHandler(greet)</code> رو هم به عنوان ورودی بهش میدیم چون یک اونت هندلر میخوایم که به طوری که توی فانکشن <code>greet</code> مشخص کردیم به پیام ها رسیدگی کنه<br>
حالا معنی <code>message.reply("Hello")</code> هم اینه که با یک پیام با متن<code>Hello</code> به <code>message</code> جواب داده بشه
</p>

<br>

<h2 align="right" dir="rtl">دکوراتور</h2>

<p align="right" dir="rtl">یه راه قشنگ تر برای اینکه اونت هندلر اضافه کنیم اینه که از دکوراتور استفاده کنیم</p>

```python
@bot.on_message()
def greet(message):
    message.reply("Hello")
```

<br>

<h2 align="right" dir="rtl">برنامه نویسی Asynchronous</h2>

<p align="right" dir="rtl">
طبق معمول بهتره که به صورت Async از بلتون استفاده کنیم<br>
وابسته به کاری که هندلرتون انجام میده ممکنه برنامه نویسی Asynchronous به اپلیکیشن شما بسیار سرعت ببخشته و یا سرعتش هیچ تغییری نکنه<br>
امکانش توی بلتون وجود داره که برنامه نویسی Sync و Async رو با هم ترکیب کنید<br>
هر اونت هندلری که دوست دارید Async باشه رو با <code>async def</code> تعریف کنید و هر کدوم که دوست دارید Sync باشه رو با <code>def</code>
</p>

```python
@bot.on_message()
async def greet(message):
    await message.reply("Hello")
```

<br>

<h2 align="right" dir="rtl">کاندیشن ها</h2>

<p align="right" dir="rtl">
کاندیشن ها رو به اونت هندلر میدیم و اون اونت هندلر فقط به آپدیت های خاصی رسیدگی میکنه
برای مثال کاندیشن <code>conditions.private</code> رو اگر به یه هندلر بدیم اون هندلر فقط به آپدیت هایی که توی پیوی بات به وجود اومدن رسیدگی میکنه
مثلا اگر توی پیویش پیام بدید جواب میده اما توی گروه نه
</p>

<br>

<p align="right" dir="rtl">به این شکل میتونیم <code>conditions.private</code> رو به یک اونت هندلر که با روش داینامیک اضافه شده بدیم</p>

```python
from balethon import conditions
from balethon.event_handlers import MessageHandler


def greet(message):
    message.reply("Hello")


bot.add_event_handler(MessageHandler(greet, conditions.private))
```

<br>

<p align="right" dir="rtl">و به این شکل برای یک اونت هندلر که با دکوراتور اضافه شده</p>

```python
from balethon import conditions


@bot.on_message(conditions.private)
def greet(message):
    message.reply("Hello")
```