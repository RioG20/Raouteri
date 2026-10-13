# التحقق / Validation

| Platform | Version | Evidence |
|---|---|---|
| Windows 11 x64 | 1.2.9 | 23 core checks; Arabic/English UI checks for IP hiding/persistence, inbox/SIM bulk controls, confirmation and cancellation. Installed successfully; published DLL matches the installed DLL. |
| Android | 1.0.0 | 16 unit tests and 6 emulator scenarios; signed release APK installed and launched; live router authentication, SMS retrieval and foreground notification checked. Android Lint: no errors. |

Android testing used an Android 16 emulator; a physical handset has not been tested. Background restrictions can differ by device. Windows compatibility testing used the developer's Windows 11 machine; installation on other PCs may reveal environment-specific issues.

Router: Huawei E6888-982, firmware 4.0.0.1(H3568SP6C983), WEBUI 4.0.0.1(W11SP6C7001). Per-device counters that remain zero are not represented as verified usage.

No actual user SMS was marked as read by the bulk-operation tests. Pagination, cancellation, rejection and partial results were tested with simulated providers; the UI requires explicit confirmation for real changes.

Public screenshots were visually reviewed. Windows screenshots use synthetic snapshots with addresses hidden; Android screenshots use labeled demo data and omit device-address pages. Real SMS, user names, serial numbers, IMEI/IMSI, credentials, private keys and diagnostics files are not part of this repository.

Windows ZIP includes the complete published runtime folder, excluding development PDB/XML files. It contains no user settings or history. Android APK signing was verified with Android SDK apksigner, using signature scheme v2. SHA-256 checksums are provided alongside the binaries.

Windows is not Authenticode-signed. Android signer certificate SHA-256:

```text
9bbe9b27278d68819f4566a61da10d134d9527384d076bc807ee5f4ad635d6c0
```

هذه الصفحة تلخص فحوص الإصدار، ولا تضمن التوافق مع كل راوتر أو هاتف أو برنامج ثابت. / These checks do not establish compatibility with every router, handset or firmware version.
