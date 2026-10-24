# راوتري / Raouteri — Windows & Android

العربية: [دليل التثبيت والاستخدام](https://github.com/RioG20/Raouteri#readme) · English: [Installation and usage](https://github.com/RioG20/Raouteri/blob/main/README.en.md)

| File | App version | Platform |
|---|---|---|
| [Raouteri-Windows-Setup-1.3.1.exe](https://github.com/RioG20/Raouteri/releases/download/v2026.10.23/Raouteri-Windows-Setup-1.3.1.exe) | 1.3.1 | Unchanged Windows 11 x64 installer, previous release |
| [Raouteri-Windows-Portable-1.3.1.zip](https://github.com/RioG20/Raouteri/releases/download/v2026.10.23/Raouteri-Windows-Portable-1.3.1.zip) | 1.3.1 | Unchanged Windows 11 x64 portable ZIP, previous release |
| Raouteri-Android-1.1.1.apk | 1.1.1 | Android 8.0+ signed APK |

**Tested specifically with Huawei E6888-982, firmware 4.0.0.1(H3568SP6C983), WEBUI 4.0.0.1(W11SP6C7001). Other configurations require separate testing.**

متابعة بطارية الراوتر وحالة الشحن وسرعة التنزيل والرفع والأجهزة والاستهلاك والرسائل، بواجهة عربية وإنجليزية. ويندوز يعرض شريط مهام/جزيرة ومؤشرات جنب الساعة؛ أندرويد يعرض إشعار متابعة وودجت وجزيرة اختيارية.

**تحديث توافق 1.1.1:** أيقونات النسبة مدمجة في التطبيق، وزر اختبار بقيمة 68 لمدة 15 ثانية بلا اتصال بالراوتر، وتحذير للقناة الهادئة. أكد المستخدم على POCO F4 / HyperOS ظهور اختبار 68 ثم النسبة الحقيقية بعد تعطيل «استخدام أيقونات التطبيقات للإشعارات» في إعدادات شريط الحالة، كما أكد عمل الإيقاف. تغيير نمط Android وحده لم يكفِ. ثبّت فوق 1.1.0 دون حذف البيانات.

**1.1 features:** نسبة بطارية الراوتر مع موجتي Wi-Fi في شريط الحالة العلوي، مع اختيار النسبة فقط أو الأيقونة العادية، ودليل POCO/HyperOS. إشعار متابعة بارز وبلا صوت افتراضيًا، وتحذير عند منعه. ملفات اتصال واسم مستخدم وكلمات محمية وسجل مستقل، واستعادة جلسة الدخول، وقراءة الجميع بتأكيد وإيقاف، وإخفاء IP ووحدات سرعة. غياب قراءة البطارية لا يعني 0%. ثبّته فوق 1.0.0 دون حذف التطبيق للحفاظ على البيانات.

**1.1.1 compatibility update:** native bundled percentage icons, a 15-second synthetic 68 test without router requests, and quiet-channel guidance. On POCO F4 / HyperOS, the user confirmed that disabling **Use app icons for notifications** revealed the test 68 and then the actual percentage; Stop monitoring also worked. Android notification style alone had not resolved it. Install over 1.1.0 without uninstalling.

**1.1 features:** the router battery percentage with Wi-Fi waves in the top status bar, with number-only / normal-glyph options and a POCO/HyperOS guide. Prominent silent monitoring notification with blocked-permission guidance; connection profiles, editable usernames and protected credentials; read-session recovery; confirmed/cancellable mark-all-read; IP privacy and speed units. Missing battery data is not 0%. Install over 1.0.0 without uninstalling to preserve data.

The app's status-bar number represents the router, not the phone battery. System notification permissions/icon settings control visibility. [Bilingual notification guide](https://github.com/RioG20/Raouteri/blob/main/docs/ANDROID-HYPEROS.md). Signed update/migration, emulator UI and read-only live router/SMS checks passed. The user's physical POCO confirmation covers the number, temporary test and stopping; long-running background behavior and other handsets are not certified. Real SMS were not marked as read during verification.

**إصلاح إيقاف أندرويد / Android stop fix:** إنهاء التحديث والخدمة والإشعار، وإلغاء الطلب الجاري، ومنع إعدادات أو أزرار جزيرة قديمة من إعادة المتابعة. / Ends polling, service and notification; cancels in-flight reads; ignores stale settings/island restarts. Granting notifications from Settings does not start polling. Stopping the app monitor sends no router-control command.

**Windows 1.3.1 unchanged:** استعادة جلسة الدخول، انتظار عند رفض مؤقت، وزر «إعادة الاتصال» مع تعافي صفحة الرسائل تلقائيًا. رفض كلمة المرور أو حظر المحاولات لا يعاد تلقائيًا. كلمات الدخول والسجل والإعدادات محفوظة.

**Windows 1.3.1 fix:** recover expired read sessions, back off temporary sign-in refusals and offer Reconnect with automatic SMS-page recovery. Wrong-password/lockout errors stop automatic attempts. Saved credentials, settings and history are preserved; control commands are not replayed.

The implemented connector remains compatible Huawei WebUI/SCRAM only. Other Huawei models require independent testing; OpenWrt and MikroTik connectors are not implemented. [Profile setup and compatibility](https://github.com/RioG20/Raouteri/blob/main/docs/ROUTER-PROFILES.md).

Windows retains IP visibility, confirmed/cancellable mark-all-read and selectable strip speed units. This release leaves the Windows 1.3.1 binaries unchanged. Windows validation: 31 core checks, actual bilingual profile UI, native taskbar regression, read-only live Huawei authentication and successful installation preserving user data.

للـZIP: فك جميع الملفات وشغّل HuaweiRouterMonitor.exe من داخله؛ لا تنقل EXE وحده. / Extract the entire ZIP and run HuaweiRouterMonitor.exe inside it; do not copy the executable alone.

Files contain no preconfigured router password, personal settings, SMS history or private signing key. Source code is not included in this distribution repository. GitHub's automatic source archives contain documentation and images only.

Independent, unofficial app; not affiliated with or endorsed by Huawei. Android handset confirmation is limited to the cases above. Windows installer is not Authenticode-signed. Check SHA256SUMS.txt for binary checksums.
