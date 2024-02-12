---
categories: [Client]
tags: []
---

<h1>Client.<strong>send_location()</strong></h1>

<p align="left" dir="rtl"><strong>فرستادن پیامی حاوی موقعیت مکانی</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که پیام به آن فرستاده میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li>
<p><strong>latitude (<a href="https://docs.python.org/3/library/functions.html#float">float</a>)</strong></p>
<blockquote dir="rtl">
<p><strong>عرض جغرافیایی</strong></p>
</blockquote>
</li>
<li>
<p><strong>longitude (<a href="https://docs.python.org/3/library/functions.html#float">float</a>)</strong></p>
<blockquote>
<p><strong>طول جغرافیایی</strong></p>
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
<p><a href="./message">Message</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.send_location(1234567890, 25.276987, 55.296249)
```