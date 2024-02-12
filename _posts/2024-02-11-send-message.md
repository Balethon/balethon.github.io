---
categories: [Client]
tags: []
---

<h1>Client.<strong>send_message()</strong></h1>

<p align="left" dir="rtl"><strong>فرستادن پیام متنی</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که پیام به آن فرستاده میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>text (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>متن پیام</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li>reply_markup (<code>ReplyMarkup</code>)<blockquote dir="rtl">
<p>یک کیبورد که همراه با پیام به کاربر فرستاده میشود</p>
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
await bot.send_message(1234567890, "Hello!")
```