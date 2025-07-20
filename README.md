# Saudi SEO Pro - مشروع Laravel متكامل

## 🎯 نظرة عامة
مشروع Laravel متكامل لتحسين محركات البحث (SEO) مع ربط المتاجر الإلكترونية وتحليل البيانات.

## ✅ المشروع جاهز للعمل!
هذا المشروع **مكتمل 100%** وجاهز للرفع والعمل مباشرة على الدومين.

## 🚀 الميزات المكتملة

### 🔐 نظام المصادقة والأمان
- ✅ تسجيل دخول وإنشاء حسابات
- ✅ Google OAuth integration
- ✅ Rate limiting متقدم
- ✅ CSRF و XSS protection
- ✅ Security headers شاملة
- ✅ تشفير البيانات الحساسة

### 💳 نظام الدفع والاشتراكات
- ✅ PayPal integration كامل
- ✅ Stripe integration كامل
- ✅ نظام اشتراكات متعدد المستويات
- ✅ Webhook handlers آمنة
- ✅ إدارة المدفوعات والفواتير

### 🔗 التكامل مع المنصات
- ✅ Google Analytics & Search Console
- ✅ ربط مع سلة (Salla)
- ✅ ربط مع زد (Zid)
- ✅ ربط مع Shopify
- ✅ API متكامل مع Sanctum

### 📊 تحليل SEO
- ✅ تحليل الكلمات المفتاحية
- ✅ تتبع ترتيب المواقع
- ✅ تحليل المنافسين
- ✅ تقارير مفصلة
- ✅ تصدير البيانات لـ Excel

### 🎨 الواجهة والتجربة
- ✅ تصميم responsive
- ✅ دعم العربية والإنجليزية
- ✅ لوحة تحكم متقدمة
- ✅ واجهة مستخدم حديثة

## 📋 متطلبات النظام
- PHP 8.1+
- MySQL 8.0+
- Composer
- Node.js & NPM (اختياري للتطوير)

## 🛠️ التثبيت السريع

### 1. رفع الملفات
```bash
# ارفع جميع ملفات المشروع للخادم
# تأكد من رفع مجلد vendor/ أيضاً
```

### 2. إعداد الصلاحيات
```bash
chmod -R 755 storage/
chmod -R 755 bootstrap/cache/
```

### 3. إعداد قاعدة البيانات
```bash
# أنشئ قاعدة بيانات جديدة
# حدث إعدادات قاعدة البيانات في .env
php artisan migrate
```

### 4. إعداد الخادم
```bash
# تأكد من أن document root يشير إلى مجلد public/
# أو استخدم .htaccess المرفق
```

## ⚙️ إعداد ملف .env

### إعدادات قاعدة البيانات
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=saudi_seo_pro
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

### إعدادات Google
```env
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_REDIRECT_URI=https://yourdomain.com/auth/google/callback
```

### إعدادات PayPal
```env
PAYPAL_MODE=live
PAYPAL_LIVE_CLIENT_ID=your_paypal_client_id
PAYPAL_LIVE_CLIENT_SECRET=your_paypal_secret
```

### إعدادات Stripe
```env
STRIPE_KEY=pk_live_your_stripe_key
STRIPE_SECRET=sk_live_your_stripe_secret
```

## 🌐 إعداد الخادم

### Apache (.htaccess)
```apache
<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteRule ^(.*)$ public/$1 [L]
</IfModule>
```

### Nginx
```nginx
server {
    listen 80;
    server_name yourdomain.com;
    root /path/to/saudi-seo-pro/public;
    
    index index.php;
    
    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }
    
    location ~ \.php$ {
        fastcgi_pass unix:/var/run/php/php8.1-fpm.sock;
        fastcgi_index index.php;
        fastcgi_param SCRIPT_FILENAME $realpath_root$fastcgi_script_name;
        include fastcgi_params;
    }
}
```

## 🔧 الأوامر المفيدة

### تحسين الأداء
```bash
php artisan config:cache
php artisan route:cache
php artisan view:cache
```

### مسح التخزين المؤقت
```bash
php artisan cache:clear
php artisan config:clear
php artisan route:clear
php artisan view:clear
```

### تشغيل المهام المجدولة
```bash
# أضف هذا السطر لـ crontab
* * * * * cd /path/to/saudi-seo-pro && php artisan schedule:run >> /dev/null 2>&1
```

## 📊 الهيكل المكتمل

```
saudi-seo-pro-complete/
├── app/
│   ├── Http/
│   │   ├── Controllers/        # جميع الكنترولرز
│   │   ├── Middleware/         # الحماية والأمان
│   │   └── Requests/           # التحقق من البيانات
│   ├── Models/                 # نماذج البيانات
│   ├── Providers/              # مقدمي الخدمات
│   └── Services/               # الخدمات المخصصة
├── config/                     # ملفات التكوين
├── database/migrations/        # قاعدة البيانات
├── public/                     # الملفات العامة
├── resources/views/            # ملفات العرض
├── routes/                     # التوجيهات
├── storage/                    # التخزين
├── vendor/                     # التبعيات
├── .env                        # إعدادات البيئة
├── composer.json               # تبعيات PHP
└── README.md                   # هذا الملف
```

## 🎯 الميزات المتقدمة

### API متكامل
- جميع endpoints جاهزة
- مصادقة Sanctum
- Rate limiting
- توثيق شامل

### نظام الإشعارات
- إشعارات البريد الإلكتروني
- إشعارات الدفع
- تنبيهات النظام

### التقارير والتحليل
- تقارير SEO مفصلة
- تحليل الأداء
- إحصائيات شاملة

## 🛡️ الأمان

### الميزات المطبقة
- ✅ Input validation شامل
- ✅ SQL injection prevention
- ✅ XSS protection
- ✅ CSRF tokens
- ✅ Rate limiting
- ✅ Security headers
- ✅ تشفير البيانات

### أفضل الممارسات
- استخدم HTTPS في الإنتاج
- قم بتحديث التبعيات بانتظام
- راجع السجلات بانتظام
- استخدم كلمات مرور قوية

## 📞 الدعم

### المشاكل الشائعة
1. **خطأ 500**: تحقق من صلاحيات storage/
2. **خطأ قاعدة البيانات**: تحقق من إعدادات .env
3. **مشاكل الـ routes**: قم بتشغيل `php artisan route:clear`

### الاتصال
- البريد الإلكتروني: support@saudiseopro.com
- الموقع: https://saudiseopro.com

## 📄 الترخيص
هذا المشروع مرخص تحت رخصة MIT.

---

## 🎉 المشروع جاهز للعمل!

**تم اختبار جميع الميزات وهي تعمل بشكل مثالي.**

1. ارفع الملفات للخادم
2. أعد إعداد .env
3. شغل المشروع
4. استمتع! 🚀

---

تم تطوير هذا المشروع بـ ❤️ في السعودية

