# O Demo Pay — Android project

A student-project payment simulation inspired by common mobile-wallet layouts. It is not affiliated with or endorsed by O!/My O!.

## Features
- Demo wallet balance (starts at 25,000 KGS)
- Simulated transfers with local balance deduction
- Google Play Services QR scanner for compatible `ODEMO|name|account|purpose` codes
- QR generation for demo receiver profiles
- Persistent transaction history and demo receipt with a generated transaction ID
- Editable demo profile name with initials avatar
- Sample demo contacts for quick recipient selection
- Persistent on-screen DEMO warnings

## Safety / scope
- No bank APIs, payment gateways, real account credentials, or real transfers.
- Demo balance, transaction history, and profile name are saved locally with Android SharedPreferences and remain after app restarts.
- QR payloads are app-specific demo data. They do not represent bank payment QR codes.
- The app uses its own name and a generic blue/white layout; it does not copy My O! logos or claim to be the official app.

## Build
1. Install Android Studio (recent stable version) and Android SDK 35.
2. Open this folder in Android Studio.
3. Allow Gradle to sync and download dependencies.
4. Run on an Android device or emulator (internet may be needed once for dependencies and the Google code-scanner module).
5. Use the QR tab to scan a QR created by this app. Google Play Services may download the scanner module on first use.

To create an APK: **Build → Build Bundle(s) / APK(s) → Build APK(s)**.

## QR format
The app generates payloads in this format:
`ODEMO|Receiver Name|DEMO-ACCOUNT|Project payment`

Only this app's `ODEMO` QR payload is accepted as a receiver QR.
