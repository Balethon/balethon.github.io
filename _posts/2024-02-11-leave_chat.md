---
categories: [Client]
tags: []
---

<h1>Client.<strong>leave_chat()</strong></h1>

<p align="left" dir="rtl"><strong>ترک کردن یک چت</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که بات آن را ترک میکند</strong></p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/functions.html#bool">bool</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.leave_chat(1234567890)
```