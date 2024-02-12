---
categories: [Client]
tags: []
---

<h1>Client.<strong>forward_message()</strong></h1>

<p align="left" dir="rtl"><strong>باز ارسال کردن پیام</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که پیام در آن باز ارسال خواهد شد</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>from_chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که پیام در آن قرار دارد</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>message_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی پیامی که باز ارسال میشود</strong></p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://balethon.ir/posts/message">Message</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.forward_message(1234567890, 1234567890, 12)
```