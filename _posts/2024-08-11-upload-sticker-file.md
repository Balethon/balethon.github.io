---
categories: [Client]
tags: []
---

<h1>Client.<strong>upload_sticker_file()</strong></h1>

<p align="left" dir="rtl"><strong>این سرویس برای آپلود یک استیکر به بله و بعد استفاده از آن در سرویس های <a href="https://balethon.ir/posts/create-new-sticker-set">create_new_sticker_set</a> و <a href="https://balethon.ir/posts/add-sticker-to-set">add_sticker_to_set</a> کاربرد داره</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>user_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی کاربر صاحب پک استیکر</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>sticker (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a> | <a href="https://docs.python.org/3/library/stdtypes.html#bytes">bytes</a> | <a href="https://docs.python.org/3/library/typing.html#typing.BinaryIO">BinaryIO</a> | <code>InputMedia</code>)</strong><blockquote dir="rtl">
<p><strong>استیکری که فرستاده می شود، میتواند آیدی یک فایل که از قبل در بله آپلود شده باشد، میتواند لینک یک فایل در وب باشد، میتواند آدرس یک فایل در دستگاه شما باشد، میتواند یک آبجکت بایت یا باینری یا اینپوت مدیای حاوی اطلاعات لازم باشد</strong></p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/stdtypes.html#str">str</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.upload_sticker_file(123456789, "sticker.png")
```