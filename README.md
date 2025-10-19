# 🤖 RubiBot – بات ساده برای Rubika با Python

این پروژه یک نمونهٔ ساده و کاربردی از ساخت بات Rubika با استفاده از کتابخانهٔ [**RubiBot**](https://rubibot.ir) است.  
هدف آن نمایش نحوهٔ پاسخ به پیام‌ها و ارسال پیام خوش‌آمدگویی به کاربران جدید است.

---

## 🚀 شروع سریع

### 1. نصب کتابخانه

ابتدا مطمئن شوید که کتابخانهٔ `RubiBot` روی سیستم شما نصب است:

```bash
pip install RubiBot
```
### 1. نمونه استفاده
```
from RubiBot import Client, Update

bot = Client("Token_bot")



@bot.on_message()
def handle_message(update: Update):
	if update.text == "/start":
		name = bot.get_chat(update.chat_id)['data']['chat']['first_name']
		update.reply(f'hello, {name} welcome to the library RubiBot💗')

bot.run()
