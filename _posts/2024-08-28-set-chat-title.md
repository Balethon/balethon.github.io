---
categories: [Client]
tags: []
---

<h1>Client.<strong>set_chat_title()</strong></h1>

<p align="left" dir="rtl"><strong>ویرایش عنوان یک چت</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که عنوان آن ویرایش میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>title (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>عنوان جدید</strong></p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/functions.html#bool">bool</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.set_chat_title(1234567890, "some title...")
```