# عرفان العلوم میراث کیلکولیٹر — Android بنانے کی ہدایات

یہ Capacitor پر مبنی Android source project ہے۔ ویب ایپ کے اصل حسابی JavaScript کو برقرار رکھا گیا ہے؛ ویب فائلیں `www/` میں ہیں۔ Google Fonts کا بیرونی لنک ہٹا دیا گیا ہے تاکہ ایپ فونٹ کے لیے نیٹ ورک پر منحصر نہ ہو (فونٹ Android کے دستیاب اردو فونٹ سے دکھے گا)۔

## ضروری سافٹ ویئر
- Node.js LTS اور npm
- Android Studio (موجودہ مستحکم ورژن)
- Android SDK / Build Tools، Android Studio کے SDK Manager سے

## Android پروجیکٹ بنائیں
پروجیکٹ فولڈر میں ٹرمینل کھول کر چلائیں:

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

Android Studio میں Gradle Sync مکمل ہونے دیں۔ فون پر USB debugging کے ذریعے Run کر کے پہلے ٹیسٹ کریں۔

## Google Play AAB
Android Studio میں Build > Generate Signed Bundle / APK > Android App Bundle منتخب کریں۔ نئی signing key بنائیں اور اسے محفوظ جگہ پر backup رکھیں۔ پھر release AAB بنائیں۔

## اہم اشاعتی امور
- `www/privacy.html` میں رابطے کا اصل ای میل درج کریں اور پرائیویسی پالیسی کی جانچ کریں۔
- Play Console میں app signing اور Data safety کے جوابات حقیقت کے مطابق دیں۔
- اس Capacitor build میں `.well-known/assetlinks.json` درکار نہیں؛ یہ TWA کے لیے تھا۔
- بنیادی حسابی انجن اور اثاثے ایپ کے اندر شامل ہیں؛ اس لیے حساب کے لیے مستقل ویب ہوسٹنگ درکار نہیں۔
- موجودہ کوڈ کے بعض غیر نافذ وراثتی ابواب ایپ کے اندر واضح طور پر درج ہیں۔
