---
categories: [Client]
tags: []
---

<h1>Client.<strong>set_webhook()</strong></h1>

<p align="left" dir="rtl"><strong>تنظیم وب هوک و دریافت آپدیت‌ ها از طریق http</strong></p>

<h2>Parameters</h2>

<ul>
<li>url (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)<blockquote dir="rtl">
<p>آدرسی که آپدیت ها به آن ارسال میشوند</p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/functions.html#bool">bool</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.set_webhook("URL")
```