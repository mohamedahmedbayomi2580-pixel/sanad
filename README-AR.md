# سند: نسخة أندرويد (APK)

## الأيقونة
ضع صورتك (مربعة، 1024×1024 مفضّل) مكان الملفين:
- `assets/icon-only.png`  (أيقونة التطبيق على الهاتف)
- `www/icon.png`          (شعار داخل التطبيق)
الملف الحالي صورة مؤقتة، وإن كان اسم صورتك "sand icon.png" فغيّر اسمها إلى icon-only.png للأول ونسخة باسم icon.png للثاني.

## الهيكل
```
sanad-android/
├── package.json
├── capacitor.config.json
├── README-AR.md
├── assets/icon-only.png
├── scripts/copy-vendor.js
└── www/index.html, icon.png, vendor/ (يُنشأ تلقائيًا)
```

## البناء (Node.js 18+ و Android Studio و JDK 17)
```
npm install
npm run android:add      # مرة واحدة
npm run android:icons    # يولّد أيقونات أندرويد من صورتك
npm run android:sync
npm run android:open
```
في Android Studio: Build ← Build APK(s)، ثم ثبّت الملف على هاتفك.
ملاحظة: يحاول التطبيق الحفظ في Documents/Sanad، وإن رفضها النظام ينتقل لمجلد التطبيق الخاص. الإشعارات المنبثقة خارج التطبيق لا تعمل في هذه النسخة.
