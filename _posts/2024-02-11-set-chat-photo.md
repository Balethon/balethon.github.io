---
categories: [Client]
tags: []
---

<h1>Client.<strong>set_chat_photo()</strong></h1>

<p align="left" dir="rtl"><strong>قرار دادن عکس پروفایل برای یک چت</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که عکس پروفایل برای آن قرار داده میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>photo (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a> | <a href="https://docs.python.org/3/library/stdtypes.html#bytes">bytes</a> | <a href="https://docs.python.org/3/library/typing.html#typing.BinaryIO">BinaryIO</a> | <code>InputMedia</code>)</strong><blockquote dir="rtl">
<p><strong>عکسی پروفایلی که برای چت قرار داده میشود، میتواند آیدی یک فایل که از قبل در بله آپلود شده باشد، میتواند لینک یک فایل در وب باشد، میتواند آدرس یک فایل در دستگاه شما باشد، میتواند یک آبجکت بایت یا باینری یا اینپوت مدیای حاوی اطلاعات لازم باشد</strong></p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/functions.html#bool">bool</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.set_chat_photo(1234567890, "photo.jpg")
```