---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

<h1 align="right" dir="rtl">بلتون</h1>

<p align="right" dir="rtl">پیام‌رسان بانکی <a href="https://www.bale.ai/">بله</a>، شبکۀ اجتماعی‌مالی بانک ملّی ایران است که هم‌زمان امکان گفتگو و پرداخت را برای شما فراهم می‌کند</p>

<p align="right" dir="rtl">بلتون یک کتابخانه برای ساختن بات در پیام‌رسان <a href="https://www.bale.ai/">بله</a> با زبان برنامه نویسی پایتون است</p>

<br>

<h2 align="right" dir="rtl">نمونه ساده</h2>

<p align="right" dir="rtl">کد یک بات که هر پیامی به آن بدهید، با متن «Hello» جواب میدهد</p>

```python
from balethon import Client

bot = Client("TOKEN")  # Replace "TOKEN" with your actual token here


@bot.on_message()
async def greet(client, message):
    await message.reply("Hello")


bot.run()
```

<blockquote align="right" dir="rtl">
<p>باید «TOKEN» را با توکنی که <a href="https://ble.ir/botfather">BotFather</a> در پیام‌رسان <a href="https://www.bale.ai/">بله</a> به شما میدهد عوض کنید</p>
</blockquote>

<br>

<h2 align="right" dir="rtl">امکانات کلیدی</h2>

<dl align="right" dir="rtl">
<dt>آسان</dt>
<dd>کار سنگین را انجام میدهد و به کار حداقلی توسط کاربر نیاز دارد</dd>
<dt>سریع</dt>
<dd>بهینه و ناهمزمان</dd>
<dt>دارای مستندات</dt>
<dd>بلتون را با کمک مستندات عمیق یاد بگیرید</dd>
<dt>کامیونیتی</dt>
<dd>انجمن فعال و دوستانه، حتما پاسخ سؤال های خود را دریافت میکنید</dd>
<dt>معماری</dt>
<dd>پشتیبانی از معماری های تابع گرا علاوه بر شیء گرا</dd>
<dt>قدرتمند</dt>
<dd>وب سرویس پیام‌رسان بله را پوشش میدهد و ابزارهای مفیدی برای ساده‌سازی کار شما دارد</dd>
<dt>انعطاف‌پذیر</dt>
<dd>غیرقابل منسوخ شدن و آماده برای پاسخ های غیرمنتظره از سمت وب سرویس پیام‌رسان بله</dd>
<dt>شهودی</dt>
<dd>تایپ هینت شده و دارای پشتیبانی عالی از ادیتورها</dd>
</dl>
