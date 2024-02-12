---
categories: [Client]
tags: []
---

<h1>Client.<strong>edit_message_text()</strong></h1>

<p align="left" dir="rtl"><strong>ویرایش متن پیام</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که پیام در آن ویرایش می شود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>message_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی پیامی که ویرایش می شود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>text (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>متن جدید</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li>reply_markup (<code>ReplyMarkup</code>)<blockquote dir="rtl">
<p>یک کیبورد که همراه با پیام ویرایش می شود</p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="./message">Message</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.edit_message_text(1234567890, 12, "Edited!")
```