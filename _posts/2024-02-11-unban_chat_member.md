---
categories: [Client]
tags: []
---

<h1>Client.<strong>unban_chat_member()</strong></h1>

<p align="left" dir="rtl"><strong>برداشتن محرومیت یک کاربر از عضویت در یک چت</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که محرومیت کاربر از عضویت در آن برداشته میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>user_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی کاربری که محرومیت از او برداشته میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li>only_if_banned (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>فقط در صورتی که کاربر محروم باشد</p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/functions.html#bool">bool</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.unban_chat_member(1234567890, 123456789, True)
```