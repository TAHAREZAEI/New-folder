# نت‌لب | NetLab Pocket

اپلیکیشن آموزشی فارسی برای شبکه، Network+، Windows Server/MCSA، Linux، Cisco/CCNA، MikroTik و VMware.

## اجرای محلی

```bash
python3 -m http.server 4173 --directory dist
```

سپس به آدرس `http://localhost:4173` بروید.

## انتشار روی GitHub Pages

مخزن را روی GitHub بسازید و این پروژه را Push کنید. Workflow داخل `.github/workflows/deploy-pages.yml` به‌صورت خودکار پوشهٔ `dist` را منتشر می‌کند.

در GitHub از مسیر **Settings → Pages → Source** گزینهٔ **GitHub Actions** را انتخاب کنید.

## ساخت نسخهٔ Android

این پروژه یک PWA است و با Capacitor به اپ Android تبدیل می‌شود:

```bash
npm install
npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap add android
npx cap sync android
npx cap open android
```

برای خروجی APK در Android Studio از مسیر **Build → Generate App Bundles or APKs → Generate APKs** استفاده کنید.

## ساخت نسخهٔ نصب‌شونده بدون Android Studio

```bash
npm install
npx cap add android
npx cap sync android
cd android
./gradlew assembleDebug
```

فایل خروجی در مسیر `android/app/build/outputs/apk/debug/app-debug.apk` ساخته می‌شود.

## محتوا

- ۲۴ مبحث آموزشی مستقل
- ۴۸۰ سؤال چهارگزینه‌ای
- PDFهای ارسالی Windows Server، Linux Essentials و LPIC
- رسم توپولوژی تعاملی
- افزودن ویدیوهای شخصی
- Service Worker و قابلیت نصب روی موبایل
