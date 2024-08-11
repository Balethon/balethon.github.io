---
categories: [Client]
tags: []
---

<h1>Client.<strong>create_new_sticker_set()</strong></h1>

<p align="left" dir="rtl"><strong>ساختن پک استیکر جدید</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>user_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی کاربر صاحب پک استیکر</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>name (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>اسم پک استیکر</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>title (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>عنوان پک استیکر</strong></p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/functions.html#bool">bool</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.create_new_sticker_set(123456789, "sticker_set_name_by_bot_username", "Sticker Set Title")
```