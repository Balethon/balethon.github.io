---
categories: [Client]
tags: []
---

<h1>Client.<strong>send_voice()</strong></h1>

<p align="left" dir="rtl"><strong>فرستادن پیام دارای صدا</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که پیام به آن فرستاده میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>voice (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a> | <a href="https://docs.python.org/3/library/stdtypes.html#bytes">bytes</a> | <a href="https://docs.python.org/3/library/typing.html#typing.BinaryIO">BinaryIO</a> | <code>InputMedia</code>)</strong><blockquote dir="rtl">
<p><strong>صدایی که فرستاده می شود، میتواند آیدی یک فایل که از قبل در بله آپلود شده باشد، میتواند لینک یک فایل در وب باشد، میتواند آدرس یک فایل در دستگاه شما باشد، میتواند یک آبجکت بایت یا باینری یا اینپوت مدیای حاوی اطلاعات لازم باشد</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li>caption (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)<blockquote dir="rtl">
<p>متن پیام</p>
</blockquote>
</li>
</ul>
<ul>
<li>duration (<a href="https://docs.python.org/3/library/functions.html#int">int</a>)<blockquote dir="rtl">
<p>مدت زمان صدا (به ثانیه)</p>
</blockquote>
</li>
</ul>
<ul>
<li>reply_to_message_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)<blockquote dir="rtl">
<p>آیدی یک پیام که این پیام به آن ریپلای شود</p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="./2024-02-12-message">Message</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.send_voice(1234567890, "voice.mp3", "Hello", 20)
```