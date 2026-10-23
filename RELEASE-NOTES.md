# راوتري / Raouteri — Windows & Android

العربية: [دليل التثبيت والاستخدام](https://github.com/RioG20/Raouteri#readme) · English: [Installation and usage](https://github.com/RioG20/Raouteri/blob/main/README.en.md)

| File | App version | Platform |
|---|---|---|
| Raouteri-Windows-Setup-1.3.1.exe | 1.3.1 | Windows 11 x64 installer |
| Raouteri-Windows-Portable-1.3.1.zip | 1.3.1 | Windows 11 x64 complete runtime folder |
| Raouteri-Android-1.0.0.apk | 1.0.0 | Android 8.0+ signed APK |

**Tested specifically with Huawei E6888-982, firmware 4.0.0.1(H3568SP6C983), WEBUI 4.0.0.1(W11SP6C7001). Other configurations require separate testing.**

متابعة بطارية الراوتر وحالة الشحن وسرعة التنزيل والرفع والأجهزة والاستهلاك والرسائل، بواجهة عربية وإنجليزية. ويندوز يعرض شريط مهام/جزيرة ومؤشرات جنب الساعة؛ أندرويد يعرض إشعار متابعة وودجت وجزيرة اختيارية.

**إصلاح Windows 1.3.1:** استعادة جلسة الدخول، انتظار عند رفض مؤقت، وزر «إعادة الاتصال» مع تعافي صفحة الرسائل تلقائيًا. رفض كلمة المرور أو حظر المحاولات لا يعاد تلقائيًا. كلمات الدخول والسجل والإعدادات محفوظة.

**Windows 1.3.1 fix:** recover expired read sessions, back off temporary sign-in refusals and offer Reconnect with automatic SMS-page recovery. Wrong-password/lockout errors stop automatic attempts. Saved credentials, settings and history are preserved; control commands are not replayed.

The implemented connector remains compatible Huawei WebUI/SCRAM only. Other Huawei models require independent testing; OpenWrt and MikroTik connectors are not implemented. [Profile setup and compatibility](https://github.com/RioG20/Raouteri/blob/main/docs/ROUTER-PROFILES.md).

Windows also retains IP visibility, confirmed/cancellable mark-all-read and selectable strip speed units. **Android 1.0.0 is unchanged**, without these Windows additions. Windows validation: 31 core checks, actual bilingual profile UI, native taskbar regression, read-only live Huawei authentication and successful installation preserving user data.

للـZIP: فك جميع الملفات وشغّل HuaweiRouterMonitor.exe من داخله؛ لا تنقل EXE وحده. / Extract the entire ZIP and run HuaweiRouterMonitor.exe inside it; do not copy the executable alone.

Files contain no preconfigured router password, personal settings, SMS history or private signing key. Source code is not included in this distribution repository. GitHub's automatic source archives contain documentation and images only.

Independent, unofficial app; not affiliated with or endorsed by Huawei. Android physical-device testing is pending. Windows installer is not Authenticode-signed. Check SHA256SUMS.txt for binary checksums.
