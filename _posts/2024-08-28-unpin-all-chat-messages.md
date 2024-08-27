---
categories: [Client]
tags: []
---

<h1>Client.<strong>unpin_all_chat_messages()</strong></h1>

<p align="left" dir="rtl"><strong>حذف سنجاق از همه پیام ها در یک چت</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که سنجاق همه پیام ها در آن حذف میشود</strong></p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/functions.html#bool">bool</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.unpin_all_chat_messages(1234567890)
```