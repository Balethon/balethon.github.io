---
categories: [Client]
tags: []
---

<h1>Client.<strong>send_media_group()</strong></h1>

<p align="left" dir="rtl"><strong>فرستادن پیام دارای یک گروه از رسانه های مختلف</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که پیام به آن فرستاده میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>media (<a href="https://docs.python.org/3/library/stdtypes.html#list">list</a>[<code>InputMedia</code> | <code>InputMediaPhoto</code> | <code>InputMediaVideo</code>])</strong><blockquote dir="rtl">
<p><strong>رسانه هایی که فرستاده می شوند، باید یک لیست باشد که آبجکت های اینپوت مدیا میتوانند در آن فرار بگیرند</strong></p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="balethon.ir/posts/message">Message</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.send_media_group(1234567890, [InputMediaPhoto("photo.jpg"), InputMediaVideo("video.mp4")])
```