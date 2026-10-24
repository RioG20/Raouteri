# التحقق / Validation

| Platform | Version | Evidence |
|---|---|---|
| Windows 11 x64 | 1.3.1 | 31 core checks; actual Arabic/English profile add/save/switch controls, protected credential migration and isolation, independent history and aliases, endpoint-change reset, no-battery dashboard/island, and native taskbar regression checks. Read-only live Huawei login passed. Installed successfully; published DLL matches installed DLL and old settings/history were preserved. |
| Android | 1.1.1 | 30 unit tests; 7 device scenarios. All 202 native percentage drawables render within bounds; notification uses modern and legacy resource IDs. The 15-second synthetic indicator test expires and does not start monitoring. Stale settings/island restart failures reproduced before the stop fix and passed afterwards. Signed 1.1.0→1.1.1 upgrade preserved protected data; production APK native icon and notification/UI stop verified. Lint: 0 errors, 143 warnings (119 vector-path complexity warnings). |
| Android | 1.1.0 | 28 unit tests; 4 added emulator scenarios plus 6 previous regression scenarios. Actual bilingual profiles, encrypted migration/isolation, IP privacy, speed units, SMS confirmation/cancellation and notification permission/number toggles passed. Signed 1.0.0→1.1.0 upgrade preserved protected credentials/history/aliases. Production APK numeric icon, live authentication and read-only SMS retrieval checked. Lint: 0 errors, 25 warnings. |

Android testing used an Android 16 emulator; a physical handset has not been tested, including the target POCO F4 / HyperOS 1.00.15.0 Stable EU. Background restrictions and status-icon visibility can differ by device. Windows compatibility testing used the developer's Windows 11 machine; installation on other PCs may reveal environment-specific issues.

1.1.1 is a compatibility attempt for a report that HyperOS shows the app logo instead of the 1.1.0 numeric icon. The handset outcome is unconfirmed. It uses bundled native vector resource IDs rather than runtime bitmaps and adds a separately labeled 15-second test of 68. The original 1.1.0 evidence below remains historical. Stopping monitoring now cancels in-flight reads, removes the service notification, preserves disabled state across stale settings and ignores stale island actions. Permission-only requests no longer start monitoring.

The exact signed 1.1.1 APK authenticated with the live router and retrieved its SMS page in a read-only smoke check. No router-control command or real SMS read-state change was executed. Emulator credentials/data were cleared afterwards. APK size: 1,884,028 bytes; original signer retained. Memory figures below are historical 1.1.0 samples, not new 1.1.1 measurements.

Router: Huawei E6888-982, firmware 4.0.0.1(H3568SP6C983), WEBUI 4.0.0.1(W11SP6C7001). Per-device counters that remain zero are not represented as verified usage.

No actual user SMS was marked as read by the bulk-operation tests. Pagination, cancellation, rejection and partial results were tested with simulated providers; the UI requires explicit confirmation for real changes.

Public screenshots were visually reviewed. Windows screenshots use synthetic snapshots with addresses hidden; Android screenshots use labeled demo data, the sample router.local address/account, and device pages with IP hidden. The home-screen screenshot demonstrates the real notification slot rendering 68 from demo data. Real SMS, personal user names, serial numbers, IMEI/IMSI, credentials, private keys and diagnostics files are not part of this repository.

Windows ZIP includes the complete published runtime folder, excluding development PDB/XML files. It contains no user settings or history. Android APK signing was verified with Android SDK apksigner, using signature scheme v2. SHA-256 checksums are provided alongside the binaries.

Windows is not Authenticode-signed. Android signer certificate SHA-256:

```text
9bbe9b27278d68819f4566a61da10d134d9527384d076bc807ee5f4ad635d6c0
```

هذه الصفحة تلخص فحوص الإصدار، ولا تضمن التوافق مع كل راوتر أو هاتف أو برنامج ثابت. / These checks do not establish compatibility with every router, handset or firmware version.

Windows profile UI audit made zero router requests. The separate live check read the existing Huawei router only (12 requests over 16 seconds) and authenticated successfully. Custom usernames and refusal to authenticate against an incompatible response were tested with simulated HTTP responses. Other router models, OpenWrt and MikroTik have not been certified or enabled.

Android 1.1.0: the ongoing foreground notification publishes a monochrome bitmap percentage with two Wi-Fi waves in the small-icon slot by default. Real emulator home-screen captures verified the indicator beside the clock; 0, 9, 68, 99 and 100 passed glyph clipping/visibility checks in both numeric styles. Wave/numeric/resource style switching persisted through actual Arabic/English controls. The signed/minified APK was independently verified to publish the numeric icon. The waves identify the router, not signal strength. This changes the app's notification icon, not the phone battery indicator; Android/HyperOS still controls icon count, tint and visibility.

The signed upgrade check installed the original 1.0.0 APK, created synthetic protected credentials/aliases/history, then installed 1.1.0 without uninstalling. The exact encrypted value remained decryptable through Android Keystore, legacy history totals/path and aliases survived, and a private local pre-migration backup was created. No real SMS was modified and no router-control command was executed during Android live validation.

Short live-connection memory samples during Android 1.1.0 development, before the optional Wi-Fi-wave style was added: PSS 27.2 MiB foreground / 31.8 MiB background; RSS 145.9 / 152.1 MiB. These are emulator samples, not a long-run load test or a POCO memory guarantee. Final APK size: 1,466,666 bytes. Test credentials/data were cleared from the emulator afterwards.

Windows 1.3.1: session expiry, temporary refusals/cooldown, rejected-password/lockout suppression, bounded retries, SMS recovery and no control-command replay passed simulated-HTTP tests. Actual Arabic/English WinUI controls preserved the protected credential and recovered a failed SMS page without router requests. A separate live read-only check returned device/signal information and fetched 20 SMS without marking them read or printing their text. Upgrade preserved settings and history. The original long-running process did not retain its initial login error code, so that exact triggering response is not asserted.
