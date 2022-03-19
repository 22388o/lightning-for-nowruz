# عیدی به سبک بیت کوین!

با استفاده از این برنامه، میتوانید با شبکه لایتنینگ به یکدیگر عیدی دهید!

![example](https://user-images.githubusercontent.com/55811147/159043625-2198255a-5a8f-4b5e-8829-f14472663c10.png)

## نصب پیشنیاز ها
ابتدا وارد فولدر پروژه شوید. سپس کامند زیر را اجرا کنید.
```terminal
pip install -r requirements.txt
```

## راهنمای شروع
### کار با lnbits
#### مشخص کردن مقدار `ADMIN_KEY` در فایل `config.py`
این برنامه، از سرویس lnbits استفاده میکند. پس لازم است وارد وبسایت https://legend.lnbits.com شوید و یک کیف پول بسازید و کیف پول خود را شارژ کنید. سپس در lnbits، در منوی سمت راست، روی گزینه `API info` کلیک کنید. سپس مقدار `Admin Key` را در فایل `config.py` قرار دهید. 
برای مثال:
```python
LNBITS_ADMIN_KEY = "a284bb02ab3a4e0eb6f3ffea4182c7g9"
```
### کار با lntxbot
> اگر میخواهید از `lntxbot` استفاده کنید، دیگر لازم نیست اطلاعات lnbits خود را در فایل `config.py`  بنویسید.

برای اینکار وارد بات شوید. [lntxbot](https://lntxbot.com)

حساب خود را در lntxbot شارژ کنید.
سپس برای برای بات، این پیغام را ارسال کنید.
```
/api_full
```
بات برای شما یک رشته ارسال میکند. مثل:
```
NDY0ODgxOjBkKLU4Mjg4MDA3YWJiYjNlMjEyOWUwZDRkTGSascmFhNDNGHcxNDRmOWU2ZmE1MDc3MTYzN2JiOThhNjk=
```
حالا این مقدار را کپی کنید و داخل فایل `config.py` به صورت زیر جایگذاری کنید:
```python
LNTXBOT_API_KEY = "NDY0ODgxOjBkKLU4Mjg4MDA3YWJiYjNlMjEyOWUwZDRkTGSascmFhNDNGHcxNDRmOWU2ZmE1MDc3MTYzN2JiOThhNjk="
```
### مشخص کردن مقدار عیدی
وارد فایل `config.py` شوید. میتوانید با تغیر مقدار متغیر `REWARD`، مقدار عیدی را مشخص کنید. مثلا میتوانید مقدار متغیر `REWARD`، را برابر `10000` ساتوشی قرار دهید. این بدین معناست که شما برای هر فرد، مقدار `10000` ساتوشی را به عنوان عیدی مشخص کرده اید.
حالا همه چیز برای ساخت کارت پستال آماده است!

## طریقه استفاده: 
```terminal
python3 main.py [-n NAME] [-t THEME] [-p PROVIDER]
```
> اگر `python3` کار نکرد، از `python` استفاده کنید.

وقتی این کامند را در ترمینال یا cmd اجرا کنید، فایل عکس، در فولدر پروژه ساخته خواهد شد.
نام پیشفرض فایل کارت پستال، `postalcard.png` است.

حالا میتوانید این عکس را به هرکسی که دوست دارید بدهید تا عیدی اش را دریافت کنید. میتواند از کیف پولی مثل bluewallet استفاده کند تا عیدی اش را به راحتی دریافت کند.
#### ارائه دهنده `LNURL`
 شما میتوانید در کامند خود، ارائه دهنده `LNURL` را انتخاب کنید. مثلا `lnbits` یا `lntxbot`. اگر در اجرای برنامه، مقدار `-p` را خالی بگذارید، به صورت پیشفرض، `lnbits` قرار خواهد گرفت.
#### تم ها
در این برنامه، دو تم وجود دارد. یک تم با نام dark و یک تم با نام light. 

### مثال 1
```terminal
python3 main.py -n اشکان -t dark -p lnbits
```

### نتیجه
![postalcard](https://user-images.githubusercontent.com/55811147/159044336-9a42629e-7f89-4481-a137-ab5f0a8bf2cc.png)

### مثال 2
```terminal
python3 main.py -n مریم -t light -p lntxbot
```

### نتیجه
![postalcard](https://user-images.githubusercontent.com/55811147/159054261-b6aa5553-6bae-4886-a1ba-7c1e3fd09efa.png)

## منابع
1. با تشکر از [@yasi30c](https://t.me/yasi30c) بابت عکس پس زمینه🙌
