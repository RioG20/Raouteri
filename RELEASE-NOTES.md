# راوتري / Raouteri — Windows & Android

العربية: [دليل التثبيت والاستخدام](https://github.com/RioG20/Raouteri#readme) · English: [Installation and usage](https://github.com/RioG20/Raouteri/blob/main/README.en.md)

| File | App version | Platform |
|---|---|---|
| [Raouteri-Windows-Setup-1.3.1.exe](https://github.com/RioG20/Raouteri/releases/download/v2026.10.23/Raouteri-Windows-Setup-1.3.1.exe) | 1.3.1 | Unchanged Windows 11 x64 installer, previous release |
| [Raouteri-Windows-Portable-1.3.1.zip](https://github.com/RioG20/Raouteri/releases/download/v2026.10.23/Raouteri-Windows-Portable-1.3.1.zip) | 1.3.1 | Unchanged Windows 11 x64 portable ZIP, previous release |
| Raouteri-Android-1.1.0.apk | 1.1.0 | Android 8.0+ signed APK |

**Tested specifically with Huawei E6888-982, firmware 4.0.0.1(H3568SP6C983), WEBUI 4.0.0.1(W11SP6C7001). Other configurations require separate testing.**

متابعة بطارية الراوتر وحالة الشحن وسرعة التنزيل والرفع والأجهزة والاستهلاك والرسائل، بواجهة عربية وإنجليزية. ويندوز يعرض شريط مهام/جزيرة ومؤشرات جنب الساعة؛ أندرويد يعرض إشعار متابعة وودجت وجزيرة اختيارية.

**Android 1.1.0:** نسبة بطارية الراوتر مع موجتي Wi-Fi في شريط الحالة العلوي، مع اختيار النسبة فقط أو الأيقونة العادية، ودليل POCO/HyperOS. إشعار متابعة بارز وبلا صوت افتراضيًا، وتحذير عند منعه. ملفات اتصال واسم مستخدم وكلمات محمية وسجل مستقل، واستعادة جلسة الدخول، وقراءة الجميع بتأكيد وإيقاف، وإخفاء IP ووحدات سرعة. غياب قراءة البطارية لا يعني 0%. ثبّته فوق 1.0.0 دون حذف التطبيق للحفاظ على البيانات.

**Android 1.1.0:** the router battery percentage with Wi-Fi waves in the top status bar, with number-only / normal-glyph options and a POCO/HyperOS guide. Prominent silent monitoring notification with blocked-permission guidance; connection profiles, editable usernames and protected credentials; read-session recovery; confirmed/cancellable mark-all-read; IP privacy and speed units. Missing battery data is not 0%. Install over 1.0.0 without uninstalling to preserve data.

The app's status-bar number represents the router, not the phone battery. System notification permissions/icon-count settings control visibility. [Bilingual notification guide](https://github.com/RioG20/Raouteri/blob/main/docs/ANDROID-HYPEROS.md). Signed update/migration, emulator UI and read-only live router/SMS checks passed; physical POCO/HyperOS validation is pending. Real SMS were not marked as read during verification.

**Windows 1.3.1 unchanged:** استعادة جلسة الدخول، انتظار عند رفض مؤقت، وزر «إعادة الاتصال» مع تعافي صفحة الرسائل تلقائيًا. رفض كلمة المرور أو حظر المحاولات لا يعاد تلقائيًا. كلمات الدخول والسجل والإعدادات محفوظة.

**Windows 1.3.1 fix:** recover expired read sessions, back off temporary sign-in refusals and offer Reconnect with automatic SMS-page recovery. Wrong-password/lockout errors stop automatic attempts. Saved credentials, settings and history are preserved; control commands are not replayed.

The implemented connector remains compatible Huawei WebUI/SCRAM only. Other Huawei models require independent testing; OpenWrt and MikroTik connectors are not implemented. [Profile setup and compatibility](https://github.com/RioG20/Raouteri/blob/main/docs/ROUTER-PROFILES.md).

Windows retains IP visibility, confirmed/cancellable mark-all-read and selectable strip speed units. This release leaves the Windows 1.3.1 binaries unchanged. Windows validation: 31 core checks, actual bilingual profile UI, native taskbar regression, read-only live Huawei authentication and successful installation preserving user data.

للـZIP: فك جميع الملفات وشغّل HuaweiRouterMonitor.exe من داخله؛ لا تنقل EXE وحده. / Extract the entire ZIP and run HuaweiRouterMonitor.exe inside it; do not copy the executable alone.

Files contain no preconfigured router password, personal settings, SMS history or private signing key. Source code is not included in this distribution repository. GitHub's automatic source archives contain documentation and images only.

Independent, unofficial app; not affiliated with or endorsed by Huawei. Android physical-device testing is pending. Windows installer is not Authenticode-signed. Check SHA256SUMS.txt for binary checksums.
