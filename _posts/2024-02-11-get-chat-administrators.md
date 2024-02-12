---
categories: [Client]
tags: []
---

<h1>Client.<strong>get_chat_administrators()</strong></h1>

<p align="left" dir="rtl"><strong>دریافت ادمین های یک چت</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که ادمین های آن دریافت میشود</strong></p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/stdtypes.html#list">list</a>[<a href="https://balethon.ir/posts/chat-member">ChatMember</a>]</p>
</blockquote>

<h2>Example</h2>

```python
await bot.get_chat_administrators(1234567890)
```