<div align="center">

# 🛡️ السجل العام للقائمة السوداء

### منصة رقمية لعرض الكيانات والأماكن المحظورة، وتمكين المستخدمين من الإبلاغ عن كيانات جديدة بسهولة وأمان

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com/)
[![Telegram API](https://img.shields.io/badge/Telegram_API-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://core.telegram.org/bots/api)

[![License](https://img.shields.io/badge/License-MIT-gold?style=flat-square)](#-الترخيص)
[![RTL Support](https://img.shields.io/badge/RTL-مدعوم-c9a24b?style=flat-square)]()
[![Status](https://img.shields.io/badge/الحالة-نشط-3ecf8e?style=flat-square)]()

</div>

---

## 📖 نبذة عن المشروع

**السجل العام للقائمة السوداء** هو تطبيق ويب من صفحة واحدة (Single Page App) مصمم بواجهة عربية كاملة (RTL) بهوية بصرية فاخرة تجمع بين اللون الكحلي العميق والذهبي، مخصص لعرض سجل موثّق للأماكن والكيانات (مطاعم، كافيهات، متاجر إلكترونية، صفحات سوشيال ميديا... إلخ) التي تم إدراجها ضمن قائمة سوداء، مع نظام بحث وفلترة فوري، وآلية إبلاغ تفاعلية ترسل البلاغات مباشرة إلى تيليجرام للمراجعة.

> 🎯 **الهدف:** توفير مرجع عام شفاف يساعد المستخدمين على تجنّب التعامل مع كيانات موثّقة بسلوكيات مخالفة، مع إتاحة قناة سهلة وسريعة للإبلاغ عن أي كيان جديد.

---

## ✨ أبرز المزايا

| الميزة | الوصف |
|---|---|
| 🔍 **بحث فوري** | بحث لحظي بالاسم أو العنوان دون إعادة تحميل الصفحة |
| 🗂️ **فلترة حسب التصنيف** | تصفية النتائج حسب نوع الكيان (مطعم، كافيه، فندق، متجر إلكتروني...) |
| 🖼️ **عرض تفصيلي لكل كيان** | مودال تفاعلي يعرض كافة بيانات الكيان مع إمكانية تكبير الصور (Lightbox) |
| 📝 **نموذج إبلاغ متكامل** | إرسال بلاغات جديدة مع صورة توضيحية ورابط الموقع الجغرافي |
| 📡 **تكامل مباشر مع تيليجرام** | إرسال البلاغات فوراً كرسائل/صور إلى بوت تيليجرام مخصص للمراجعة |
| 🗄️ **قاعدة بيانات حيّة** | تخزين واسترجاع البيانات في الوقت الفعلي عبر Supabase |
| 🎨 **تصميم فاخر ومتجاوب** | هوية بصرية رسمية (كحلي + ذهبي) متجاوبة بالكامل مع جميع الأجهزة |
| 🌙 **دعم كامل للعربية RTL** | بُنية وتصميم مخصصان للغة العربية من الاتجاه إلى الخطوط |
| ⚡ **تحميل هيكلي (Skeleton)** | شاشات تحميل أنيقة أثناء جلب البيانات لتجربة استخدام أفضل |
| ♿ **إمكانية وصول** | دعم `aria-*` وتقليل الحركة لذوي الاحتياجات الخاصة |

---

## 🧰 التقنيات المستخدمة

- **HTML5 / CSS3** — بنية دلالية وتنسيقات مخصصة بالكامل (بدون أي إطار عمل CSS خارجي)
- **JavaScript (Vanilla JS)** — منطق التطبيق بالكامل دون أي مكتبات إضافية
- **[Supabase](https://supabase.com/)** — قاعدة بيانات ومحرك خلفي لتخزين واسترجاع بيانات الكيانات
- **[Telegram Bot API](https://core.telegram.org/bots/api)** — استقبال البلاغات الجديدة فور إرسالها
- **[Font Awesome 6](https://fontawesome.com/)** — مكتبة الأيقونات
- **خطوط Google Fonts** — `Tajawal` و `Cairo` لهوية بصرية عربية أنيقة

---

## 📁 هيكل قاعدة البيانات (Supabase)

يعتمد المشروع على جدول باسم `places` بالحقول التالية:

| الحقل | النوع | الوصف |
|---|---|---|
| `id` | `int` | المعرّف الفريد للكيان |
| `name` | `text` | اسم الكيان أو المكان |
| `address` | `text` | العنوان أو رابط الصفحة/الموقع |
| `category` | `text` | تصنيف الكيان |
| `image_url` | `text` | رابط صورة الكيان (اختياري) |
| `is_blacklisted` | `boolean` | يحدد ما إذا كان الكيان معروضاً في السجل العام |

---

## 🚀 التشغيل محلياً

هذا مشروع **Frontend فقط** (بدون خطوة بناء)، لذا يمكن تشغيله مباشرة:

```bash
# 1) استنساخ المستودع
git clone https://github.com/ibrahimmustafacv/Test2.git

# 2) الدخول إلى مجلد المشروع
cd Test2

# 3) تشغيل الملف مباشرة عبر أي سيرفر محلي، مثال:
npx serve .
# أو ببساطة افتح index.html في المتصفح
```

### ⚙️ الإعداد المطلوب

قبل التشغيل، تأكد من ضبط بيانات الاتصال الخاصة بك داخل ملف `index.html`:

```js
const SUPABASE_URL = 'YOUR_SUPABASE_URL';
const SUPABASE_ANON_KEY = 'YOUR_SUPABASE_ANON_KEY';

const TELEGRAM_BOT_TOKEN = 'YOUR_TELEGRAM_BOT_TOKEN';
const TELEGRAM_CHAT_ID = 'YOUR_TELEGRAM_CHAT_ID';
```

> ⚠️ **تنبيه أمني هام:** لاحظت أن مفاتيح Supabase وتوكن بوت تيليجرام مكتوبة حالياً بشكل مباشر (Hardcoded) داخل كود الواجهة الأمامية، وهذا يعني أنها **مرئية لأي زائر** يفتح "عرض المصدر" في المتصفح. يُنصح بشدة بـ:
> - نقل هذه المفاتيح إلى **متغيرات بيئة (Environment Variables)** عبر خدمة Backend وسيطة (مثل Supabase Edge Function أو Cloudflare Worker) بدلاً من استدعاء تيليجرام مباشرة من المتصفح.
> - تفعيل **Row Level Security (RLS)** على جدول `places` في Supabase للسماح بالقراءة العامة فقط ومنع أي كتابة أو تعديل غير مصرّح به.
> - توليد توكن تيليجرام جديد وإلغاء التوكن الحالي إذا كان قد نُشر بالفعل في مستودع عام.

---

## 🗺️ خارطة الطريق (مقترحات مستقبلية)

- [ ] لوحة تحكم للمشرفين لمراجعة البلاغات والموافقة عليها مباشرة
- [ ] نظام صفحات (Pagination) لدعم عدد كبير من الكيانات
- [ ] إشعارات فورية عند إدراج كيان جديد
- [ ] دعم تعدد اللغات (عربي/إنجليزي)

---

## 🤝 المساهمة

المساهمات مرحّب بها دائماً! لإضافة تحسين أو ميزة جديدة:

1. اعمل Fork للمشروع
2. أنشئ فرعاً جديداً (`git checkout -b feature/AmazingFeature`)
3. Commit للتغييرات (`git commit -m 'إضافة ميزة رائعة'`)
4. Push للفرع (`git push origin feature/AmazingFeature`)
5. افتح Pull Request

---

## 📄 الترخيص

هذا المشروع متاح بموجب رخصة **MIT**. راجع ملف `LICENSE` لمزيد من التفاصيل.

---

## 👤 المطوّر

<div align="center">

### **Ibrahim Mustafa**

[![GitHub](https://img.shields.io/badge/GitHub-ibrahimmustafacv-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ibrahimmustafacv)

</div>

---

<div align="center">

صُمم وطُوّر بعناية بواسطة **Ibrahim Mustafa** 💛

</div>
