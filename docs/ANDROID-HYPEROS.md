# أندرويد: نسبة بطارية الراوتر / Android router battery status

## العربية

في Android 1.1.0 يظهر **رقم بطارية الراوتر نفسه** في خانة أيقونة إشعار «راوتري» أعلى الشاشة: `68` يعني 68%. لا تُضاف علامة % لضمان وضوح الرقم في المساحة الصغيرة. بطارية الهاتف الأصلية لا تتغير. موضع الرقم ولونه وعدد الأيقونات الظاهرة يحددها النظام. القراءة تتحدث أثناء المتابعة؛ عند تعذر الوصول للراوتر أو غياب قراءة صحيحة تعود أيقونة الراوتر. تفاصيل الشحن والسرعة موجودة داخل الإشعار.

1. ثبّت APK 1.1.0 فوق 1.0.0 دون حذف التطبيق. احفظ البيانات المحلية بالحفاظ على التطبيق وتوقيعه الأصلي.
2. اتصل بوايفاي الراوتر. من ملفات الاتصال أدخل العنوان واسم مستخدم الإدارة وكلمة الإدارة، واحفظ، ثم ابدأ المتابعة.
3. اسمح بإشعارات «راوتري» وقناة حالة الراوتر. من إعدادات التطبيق اترك إبراز الأيقونة وعرض نسبة بطارية الراوتر مفعّلين.
4. على POCO / HyperOS، إذا ظهر الإشعار عند السحب ولم يظهر الرقم أعلى الشاشة: ابحث في إعدادات النظام عن **إظهار أيقونات الإشعارات** ضمن الإشعارات وشريط الحالة، وراجع الحد الأقصى للأيقونات إن وُجد. المسميات تختلف حسب المنطقة والإصدار. مع مركز تحكم منفصل، اسحب من جانب الإشعارات.
5. إن توقفت المتابعة عند قفل الشاشة، افتح إعدادات بطارية التطبيق واختر «بلا قيود»، وراجع التشغيل التلقائي. يوفر التطبيق اختصارات لهذه الصفحات؛ لا يغيرها تلقائيًا.

الشكل الافتراضي «النسبة مع موجتي Wi-Fi»؛ الموجتان للتعريف بالراوتر وليستا قوة الإشارة. يمكن اختيار «النسبة فقط» أو «أيقونة الراوتر» من إعدادات التطبيق، وإيقاف المتابعة من الإشعار. اختيار المتابعة الهادئة قد يجعل النظام يخفي الأيقونة؛ أبقِ اختيار إبرازها مفعّلًا لعرض الرقم.

![رقم الراوتر في شريط الحالة؛ بيانات تجريبية](../images/android/ar-status-bar-router-68.png)

<img src="../images/android/ar-notification-settings.png" width="320" alt="إعدادات النسبة والإشعار">

تم التحقق على محاكي Android 16. الهاتف المستهدف POCO F4 / HyperOS 1.00.15.0 Stable EU لم يكن متصلًا للاختبار؛ لا يستطيع التطبيق تجاوز إخفاء الأيقونات أو قيود الخلفية التي يختارها النظام.

## English

Android 1.1.0 draws the **router battery percentage** in Raouteri's notification icon slot at the top: `68` means 68%. The % sign is omitted to keep digits legible in the small slot. Your phone's battery indicator is unchanged. Android controls placement, tint and icon count. Monitoring updates the reading; disconnection or missing battery data restores the router glyph. Charging and traffic details remain inside the notification.

1. Install 1.1.0 over 1.0.0 without uninstalling. Keep the original app/signature to retain local data.
2. Connect to router Wi-Fi. Save the management address, administration username and password in a connection profile, then start monitoring.
3. Allow Raouteri notifications and its Router status channel. Keep the prominent-icon and router-battery-number settings enabled.
4. On POCO / HyperOS, if the drawer notification exists but its top number is absent, find **Show notification icons** under system notification/status-bar settings. Check any maximum icon-count setting. Names vary by region/version. With separate control-center panels, pull from the notification side.
5. If monitoring stops with the screen locked, review app battery settings (No restrictions) and autostart. The app provides shortcuts; these choices remain yours.

The default style is Percentage with Wi-Fi waves; the waves identify the router and do not measure signal strength. Settings also offers Percentage only and Router icon. You can stop monitoring from the notification. Quiet monitoring may hide status icons under system policy; keep prominence enabled for the number.

<img src="../images/android/en-notification-settings.png" width="320" alt="Notification and battery-number options">

Verified on an Android 16 emulator. The target POCO F4 / HyperOS 1.00.15.0 Stable EU was not connected for testing. App code cannot override system-wide status-icon or background restrictions.

Official references: [Xiaomi status-bar icons](https://www.mi.com/my/support/article/KA-33188/), [POCO F4 notification permissions](https://www.mi.com/fr/support/faq/details/KA-785217/), [Android notification permission](https://developer.android.com/develop/ui/compose/notifications/notification-permission).
