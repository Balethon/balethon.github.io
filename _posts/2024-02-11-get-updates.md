---
categories: [Client]
tags: []
---

<h1>Client.<strong>get_updates()</strong></h1>

<p align="left" dir="rtl"><strong>دریافت آپدیت های اخیر</strong></p>

<h2>Parameters</h2>

<ul>
<li>offset (<a href="https://docs.python.org/3/library/functions.html#int">int</a>)<blockquote dir="rtl">
<p>آیدی آپدیتی که به عنوان اولین آپدیت در لیست مقدار بازگشتی قرار میگیرد</p>
</blockquote>
</li>
</ul>
<ul>
<li>limit (<a href="https://docs.python.org/3/library/functions.html#int">int</a>)<blockquote dir="rtl">
<p>حداکثر تعداد آپدیت هایی که دریافت میشوند</p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/stdtypes.html#list">list</a>[<code>Update</code>]</p>
</blockquote>

<h2>Example</h2>

```python
await bot.get_updates(123, 5)
```