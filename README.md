# جودة إنشاء شبكة التوزيع الأرضية - TSC SP128

منصة ويب عربية RTL جاهزة للنشر على GitHub Pages، مبنية على ملف PDF المرفق.

## مهم قبل النشر
الملف الأصلي يتضمن في صفحاته تصنيفًا داخليًا. **لا ترفعي المشروع إلى مستودع Public إلا إذا كانت لديك صلاحية نشر واضحة.** استخدمي مستودع GitHub خاصًا عند عدم وجود تصريح.

## التشغيل محليًا
لأن ملفات JSON تُحمّل باستخدام fetch:
```bash
python -m http.server 8000
```
ثم افتحي `http://localhost:8000`

## GitHub Pages
1. أنشئي مستودعًا جديدًا.
2. ارفعي محتويات مجلد `attendance-system`.
3. من Settings > Pages اختاري النشر من Branch.
4. اختاري `main` و`/root`.
5. WebXR يحتاج HTTPS، وGitHub Pages يوفر HTTPS.

## مكونات المشروع
- `assets/docs/SP128.pdf` المصدر الأصلي.
- `data/pages.json` النص المستخرج من جميع الصفحات.
- `data/figures.json` الصور والأشكال وربطها بالصفحات.
- `data/tables.json` جداول HTML.
- `data/content-audit.json` سجل الصفحات.
- `ar.html` و`vr.html` و`mr.html` لتجارب WebXR مع fallback ثلاثي الأبعاد.
- `dashboard.html` للحضور والمتدربين.
- `reports.html` للتقارير والطباعة والتصدير.

## الأمان
`login.html` نموذج محلي فقط. لا توجد مصادقة خادمية حقيقية على GitHub Pages، ولا يجب تخزين كلمات مرور حقيقية في المشروع.
