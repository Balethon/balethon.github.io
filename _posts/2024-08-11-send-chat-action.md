---
categories: [Client]
tags: []
---

<h1>Client.<strong>send_chat_action()</strong></h1>

<p align="left" dir="rtl"><strong>این سرویس برای وقتی که بات کار زمانبری انجام میده و میخواید به کاربر نمایش بدید که بات داره کاری انجام میده کاربرد داره</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که اکشن به آن فرستاده میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li>action (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)<blockquote dir="rtl">
<p>اکشن مورد نظر</p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://balethon.ir/posts/chat">Chat</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.send_chat_action(1234567890, "typing")
```