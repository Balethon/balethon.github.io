---
categories: [Client]
tags: []
---

<h1>Client.<strong>promote_chat_member()</strong></h1>

<p align="left" dir="rtl"><strong>تغییر دسترسی های یک عضو از یک چت</strong></p>

<h2>Parameters</h2>

<ul>
<li><strong>chat_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی چت موردنظر</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li><strong>user_id (<a href="https://docs.python.org/3/library/functions.html#int">int</a> | <a href="https://docs.python.org/3/library/stdtypes.html#str">str</a>)</strong><blockquote dir="rtl">
<p><strong>آیدی عضو موردنظر</strong></p>
</blockquote>
</li>
</ul>
<ul>
<li>can_edit_messages (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند پیام های چت را ویرایش کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_delete_messages (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند پیام های چت را حذف کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_manage_video_chats (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند ویدیو چت های چت را مدیریت کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_restrict_members (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند اعضای چت را محدود کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_promote_members (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند اعضای چت را ادمین کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_change_info (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند اطلاعات چت را ویرایش کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_invite_users (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند کاربران را به چت دعوت کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_pin_messages (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند پیام ها را در چت سنجاق کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_send_messages (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند در چت پیام ارسال کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_send_media_messages (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند در چت پیام های دارای رسانه ارسال کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_send_media (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند در چت رسانه ارسال کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_send_gif_stickers (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)</li>
</ul>
<ul>
<li>can_reply_to_story (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند به وضعیت های چت ریپلای کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_forward_message_from (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)</li>
</ul>
<ul>
<li>can_send_gift_packet (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)</li>
</ul>
<ul>
<li>can_start_call (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند در چت تماس شروع کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_send_link_message (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند پیام های دارای لینک در چت ارسال کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_send_forwarded_message (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند در چت پیام باز ارسال کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_kick_user (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند اعضای چت را حذف کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_send_message (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند در چت پیام ارسال کند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_see_members (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند اعضای چت را ببیند</p>
</blockquote>
</li>
</ul>
<ul>
<li>can_add_story (<a href="https://docs.python.org/3/library/functions.html#bool">bool</a>)<blockquote dir="rtl">
<p>آیا عضو موردنظر میتواند برای چت وضعیت اضافه کند</p>
</blockquote>
</li>
</ul>

<h2>Returns</h2>

<blockquote>
<p><a href="https://docs.python.org/3/library/functions.html#bool">bool</a></p>
</blockquote>

<h2>Example</h2>

```python
await bot.promote_chat_member(1234567890, 123456789, can_promote_members=True, can_pin_messages=True)
```