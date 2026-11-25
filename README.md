# EARTH LIVE 360 — V1.0.0
**سازنده: علیرضا نامداری**

فایل `index.html` یک وب‌سایت مستقل است. برای اجرای اولیه آن را در مرورگر باز کنید. اگر مرورگر درخواست‌های فایل محلی را مسدود کرد، آن را با GitHub Pages منتشر کنید یا از سرور محلی استفاده کنید:

```sh
python -m http.server 8000
```

سپس `http://localhost:8000` را باز کنید. برای GitHub Pages، `index.html` را در ریشه مخزن عمومی قرار دهید و Settings → Pages → Deploy from a branch → main → / (root) را انتخاب کنید.

## منابع
- USGS: https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php (زلزله‌های ۲۴ ساعت گذشته)
- NASA EONET: https://eonet.gsfc.nasa.gov/docs/v3 (رویدادهای باز ۳۰ روز گذشته که هندسه نقطه‌ای دارند؛ حداکثر ۳۰۰ رکورد)
- Where the ISS at?: https://docs.wheretheiss.at/w/developer (موقعیت تخمینی ISS و مسیر ثبت‌شده هنگام استفاده)
- NOAA SWPC: https://services.swpc.noaa.gov/products/noaa-planetary-k-index.json (شاخص Kp)
- Open-Meteo: https://open-meteo.com/en/docs (آب‌وهوای مدل‌محور؛ استفاده رایگان غیرتجاری)
- Natural Earth: https://www.naturalearthdata.com/about/terms-of-use/ (نقشه عمومی کم‌جزئیات)

بدون نیاز به کلید API یا سرور اختصاصی. اتصال واقعی تابع شبکه، CORS و محدودیت‌های منابع است. بدون داده، اعداد ساختگی نمایش داده نمی‌شوند. داده‌های قدیمی حداکثر تا ۲۴ ساعت در مرورگر نگه داشته می‌شوند. محل نشان ISS تصویر نقطه زیر ایستگاه روی زمین است؛ مدار کامل و همه ماهواره‌ها در این نسخه نیستند. نقشه برای ناوبری و هشدار اضطراری مناسب نیست.

آزمون توسعه: بررسی نحو JavaScript، آزمایش مرورگر با پاسخ‌های ساختگی صرفاً در محیط آزمون، کنترل زوم و انتخاب نقطه، آب‌وهوا و عرض موبایل. حالت Canvas سه‌بعدی در محیط آزمون اجرا شد؛ WebGL سخت‌افزاری و اتصال واقعی APIها در این محیط قابل تأیید نبودند.
