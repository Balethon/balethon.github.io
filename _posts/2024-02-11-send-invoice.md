---
categories: [Client]
tags: []
---

<h1>Client.<strong>send_invoice()</strong></h1>

<p align="left" dir="rtl"><strong>فرستادن صورتحساب</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چتی که صورتحساب به آن فرستاده میشود</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>title (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>عنوان صورتحساب</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>description (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>توضیحات صورتحساب</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>provider_token (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>شماره کارت شماره کیف پول بله یا شماره درگاه و شماره پذیرنده که پول را دریافت میکند</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>prices (<a href="https://docs.python.org/3/library/stdtypes.html#list">list</a>[<code>LabeledPrice</code>])</strong><blockquote dir="rtl">
<p><strong>لیست قیمت های برچسب دار</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li>provider_data (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>photo_url (<a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>photo_size (<a href="https://docs.python.org/3/library/functions.html#int">int</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>photo_width (<a href="https://docs.python.org/3/library/functions.html#int">int</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>photo_height (<a href="https://docs.python.org/3/library/functions.html#int">int</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>need_name (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>need_phone_number (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>need_email (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>need_shipping_address (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>is_flexible (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>disable_notification (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>reply_to_message_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)<blockquote dir="rtl"></blockquote>
</li>
</ul>
<ul>
<li>reply_markup (<code>ReplyMarkup</code>)<blockquote dir="rtl"></blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://balethon.ir/posts/message">Message</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.send_invoice(
        1234567890,
        "Some title",
        "Some description",
        "6037************",
        LabeledPrice(label="Some label", amount=1000000)
    )
```