# 🛠️ سیس‌هلپر (SysHelper)

[![نسخه](https://img.shields.io/badge/version-2.5-blue.svg)](https://github.com/MeXenon/syshelper)
[![لایسنس](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![پلتفرم](https://img.shields.io/badge/platform-Ubuntu-orange.svg)](https://ubuntu.com)

🇮🇷 فارسی | [🇺🇸 English](README.md)

**سیس‌هلپر** یک ابزار جامع مدیریت سیستم برای سرورهای اوبونتو با قابلیت بهینه‌سازی میرورهای ایرانی، مدیریت شبکه و نصب خودکار پنل‌ها است.

## ✨ قابلیت‌ها

- 📊 **نمایش اطلاعات سیستم**: نظارت زنده CPU، RAM، آپ‌تایم و بار سیستم
- 🌐 **اطلاعات شبکه**: شناسایی IP، تنظیمات DNS و جزئیات ISP
- 🔧 **مدیریت شبکه**: کنترل IPv6 و پاسخ‌دهی به ping
- 🚀 **تست سرعت میرور**: رتبه‌بندی خودکار ۲۹+ میرور اوبونتو
- ⚡ **پیکربندی خودکار**: تغییر میرور با یک کلیک برای دانلود بهینه پکیج‌ها
- 📦 **پنل 3X-UI**: نصب چند نسخه‌ای (v2.6.0 و v2.6.2)
- 🔐 **یکپارچگی ACME.sh**: نصب مدیر گواهی SSL
- 🎨 **رابط مدرن**: UI تمیز و رنگی ترمینال با ASCII art و نوار پیشرفت

## 🔧 نصب

### گزینه 1: مستقیم از GitHub
```bash
wget https://raw.githubusercontent.com/MeXenon/syshelper/main/xenonnet.sh && chmod +x xenonnet.sh && ./xenonnet.sh
```

### گزینه 2: دانلود و اجرا مرحله به مرحله
```bash
wget https://raw.githubusercontent.com/MeXenon/syshelper/main/xenonnet.sh
chmod +x xenonnet.sh
./xenonnet.sh
```

### ✅️ گزینه 3: منبع جایگزین (پشتیبان) ( منبع ایرانی - توصیه شده برای VPS های ایرانی )
```bash
wget -O syshelper2.5.tar.gz https://uploadkon.ir/uploads/302608_25syshelper2-5-tar.gz && tar -xzvf syshelper2.5.tar.gz && chmod +x xenonnet.sh && ./xenonnet.sh
```

## 📋 پیش‌نیازها

اسکریپت به صورت خودکار وابستگی‌های مورد نیاز را بررسی می‌کند:
- `curl` - برای عملیات شبکه
- `wget` - برای دانلود فایل‌ها
- `bc` - برای محاسبات ریاضی
- `tar` - برای استخراج آرشیو
- `iptables` - برای مدیریت شبکه (اختیاری)

در صورت نبود، نصب کنید:
```bash
sudo apt-get update
sudo apt-get install curl wget bc tar iptables-persistent
```

## 🚀 نحوه استفاده

1. **اسکریپت را اجرا کنید** با استفاده از هر روش نصب بالا
2. **اطلاعات سیستم** به صورت خودکار نمایش داده می‌شود
3. **از گزینه‌های منو انتخاب کنید**:
   - `1` - تست و اعمال بهترین میرور
   - `2` - نصب پنل 3X-UI
   - `3` - نصب ACME.sh
   - `4` - مدیریت شبکه
   - `5` - به‌روزرسانی اطلاعات سیستم
   - `6` - خروج

### فرآیند تست میرور
- بررسی ۲۹+ میرور اوبونتو
- تست سرعت موازی برای نتایج سریع‌تر
- بررسی تازگی میرور و تاریخ انتشار
- رتبه‌بندی بر اساس عملکرد و قابلیت اطمینان
- اعمال خودکار سریع‌ترین میرور
- به‌روزرسانی فهرست پکیج‌ها

### نصب 3X-UI
- انتخاب بین v2.6.0 (قدیمی) و v2.6.2 (جدید)
- استخراج هوشمند آرشیو با پشتیبانی تو در تو
- استخراج و تنظیم خودکار
- منابع نصب بومی‌سازی شده
- مناسب برای دیتاسنترهای ایرانی

### مدیریت شبکه
- **کنترل IPv6**: فعال/غیرفعال کردن IPv6 (موقت یا دائمی)
- **پاسخ Ping**: مسدود/اجازه دادن پاسخ ping از طریق iptables
- **وضعیت زنده**: نظارت زنده پیکربندی‌های شبکه
- **یکپارچگی سیستم**: تنظیمات پایدار در طول راه‌اندازی مجدد

### یکپارچگی ACME.sh
- نصب خودکار مدیر گواهی SSL
- آخرین نسخه با استخراج هوشمند
- اتوماسیون گواهی آماده استفاده
- مناسب برای تنظیمات وب سرور

## 📊 نمایش اطلاعات سیستم

این ابزار نمای جامعی ارائه می‌دهد شامل:

| دسته‌بندی | اطلاعات |
|----------|-------------|
| **پردازنده** | مدل، تعداد هسته، درصد استفاده، متوسط بار |
| **حافظه** | RAM استفاده شده/کل با درصد |
| **شبکه** | IP عمومی، موقعیت، ISP، سرورهای DNS |
| **سیستم** | آپ‌تایم، نسخه اوبونتو، میرور فعلی APT |
| **وضعیت شبکه** | وضعیت IPv6، پیکربندی پاسخ ping |

## 🌍 لیست میرورها

پایگاه داده گسترده میرورهای اوبونتو:
- NetCologne — http://mirror.netcologne.de/ubuntu/
- University of Erlangen — http://ftp.fau.de/ubuntu/
- Scaleway — http://mirrors.scaleway.com/ubuntu/
- NLUUG — http://ftp.nluug.nl/os/Linux/distr/ubuntu/
- University of Groningen — http://ftp.calyx.nl/ubuntu/
- Verinomi — http://mirror.verinomi.com/ubuntu/
- Linux Users Group Turkey — http://ftp.linux.org.tr/ubuntu/
- Maeen Network — http://mirror.maeen.sa/ubuntu/
- UAE Archive — http://ae.archive.ubuntu.com/ubuntu/
- Zagrio WebHosting — https://archive.ubuntu.mirrors.zagrio.net/ubuntu
- Iranserver — https://mirror.iranserver.com/ubuntu
- Shatel — https://mirror.shatel.ir/ubuntu
- HostIran — https://mirror.hostiran.ir/ubuntu
- KimiaHost — https://ubuntu-mirror.kimiahost.com/ubuntu
- Avina Host — https://ubuntu.avinahost.com/ubuntu
- Mobinhost — https://ubuntu.mobinhost.com/ubuntu
- Pishgaman — https://ubuntu.pishgaman.net/ubuntu
- Sindad LLC — https://ir.ubuntu.sindad.cloud/ubuntu
- Amin IDC — http://mirror.aminidc.com/ubuntu
- ArvanCloud — https://mirror.arvancloud.ir/ubuntu
- Pardis Co. — https://mirrors.pardisco.co/ubuntu
- Petiak — https://archive.ubuntu.petiak.ir/ubuntu
- LinuxMirrors.ir — https://linuxmirrors.ir/ubuntu
- Pars.host — https://ubuntu.pars.host
- ParsvDS — https://ubuntu.parsvds.com/ubuntu
- Faraso — http://mirror.faraso.org/ubuntu
- Dimit Network — https://mirrors.ubuntu.dimit.cloud
- IUT University — http://repo.iut.ac.ir/repo/Ubuntu
- Official Iran Archive — https://ir.archive.ubuntu.com/ubuntu

## 🛡️ امنیت و مجوزها

- **تشخیص Root**: نمایش سطح دسترسی کاربر فعلی
- **عملیات ایمن**: بدون دستورات مخرب بدون تأیید
- **دوستدار پشتیبان**: حفظ پیکربندی‌های اصلی
- **ردپای کمینه**: پاکسازی خودکار فایل‌های موقت
- **امنیت شبکه**: تغییرات ایمن iptables و sysctl

## 🔍 عیب‌یابی

### مشکلات رایج

**اسکریپت اجرا نمی‌شود:**
```bash
chmod +x xenonnet.sh
```

**نبود وابستگی‌ها:**
```bash
sudo apt-get install curl wget bc tar
```

**اتمام زمان شبکه:**
- اتصال اینترنت را بررسی کنید
- روش نصب جایگزین را امتحان کنید

**عدم دسترسی:**
- با دسترسی‌های مناسب اجرا کنید
- از `sudo` برای تغییرات سیستمی استفاده کنید

**مدیریت IPv6/Ping کار نمی‌کند:**
- اطمینان حاصل کنید که iptables نصب شده است
- دسترسی‌های root برای تغییرات شبکه را بررسی کنید

## 📝 تاریخچه نسخه‌ها

### v2.5 (فعلی)
- **جدید**: پنل مدیریت شبکه با کنترل IPv6/ping
- **جدید**: نصب مدیر گواهی SSL ACME.sh
- **جدید**: پشتیبانی چند نسخه‌ای 3X-UI (v2.6.0 و v2.6.2)
- **بهبود یافته**: پایگاه داده گسترده میرورهای اوبونتو
- **بهبود یافته**: تست میرور موازی برای نتایج سریع‌تر
- **بهبود یافته**: استخراج هوشمند آرشیو با پشتیبانی تو در تو
- **بهبود یافته**: هدر ASCII art و طراحی UI حرفه‌ای
- **بهبود یافته**: تأیید تاریخ انتشار برای میرورها
- **بهبود یافته**: مدیریت خطا و تشخیص بهتر

### v2.0
- بازطراحی کامل UI
- بهبود الگوریتم تست میرور
- بهبود نشانگرهای پیشرفت
- اضافه شدن نصب 3X-UI
- بهتر شدن مدیریت خطا

### v1.x
- اطلاعات پایه سیستم
- تست ساده میرور

## 🤝 مشارکت

مشارکت‌ها خوش آمدند! لطفاً در ارسال مسائل، درخواست ویژگی‌ها یا Pull Request تردید نکنید.

1. مخزن را Fork کنید
2. شاخه ویژگی خود را ایجاد کنید (`git checkout -b feature/amazing-feature`)
3. تغییرات خود را Commit کنید (`git commit -m 'Add amazing feature'`)
4. به شاخه Push کنید (`git push origin feature/amazing-feature`)
5. یک Pull Request باز کنید

## 📞 پشتیبانی

- 🐛 **گزارش باگ**: [GitHub Issues](https://github.com/MeXenon/syshelper/issues)
- 💬 **تلگرام**: [@XenonNet](https://t.me/XenonNet)
- 📧 **توسعه‌دهنده**: [@XenonNet](https://t.me/XenonNet)

## 📄 لایسنس

این پروژه تحت لایسنس MIT منتشر شده است - فایل [LICENSE](LICENSE) را برای جزئیات مشاهده کنید.

## ⭐ حمایت از پروژه

اگر این پروژه به شما کمک کرد، لطفاً یک ⭐ در GitHub بدهید!

---

**با ❤️ ساخته شده توسط [@XenonNet](https://github.com/MeXenon)**
