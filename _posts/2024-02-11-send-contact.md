---
categories: [Client]
tags: []
---

<h1>Client.<strong>send_contact()</strong></h1>

<p align="left" dir="rtl"><strong>فرستادن پیامی حاوی اطلاعات مخاطب</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که پیام به آن فرستاده میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li>
<p><strong>phone_number (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong></p>
<blockquote dir="rtl">
<p><strong>شماره تلفن کاربر</strong></p>
</blockquote>
</li>
<li>
<p><strong>first_name (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong></p>
<blockquote>
<p><strong>نام کوچک کاربر</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>last_name (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>نام خانوادگی کاربر</strong></p>
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
await bot.send_contact(1234567890, "989*********", "Ali", "Naseri")
```