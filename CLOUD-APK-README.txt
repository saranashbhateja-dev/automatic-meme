JEE TRACKER — CLOUD APK BUILD

Base:
JEE-Tracker-8-Oct-3-Night-Then-6-Daily

Cloud:
Supabase project already configured.
The app uses email/password authentication and syncs tracker_state per signed-in user.
Local browser storage remains available as an offline fallback.

APK:
This folder is prepared for Capacitor Android packaging.
The included android-build.bat creates the Android project and builds a debug APK on a Windows PC with Node.js, Java, and Android SDK/Android Studio installed.

GitHub Actions:
.github/workflows/build-apk.yml can build the debug APK automatically on GitHub Actions.

Important:
The HTML app itself does not require the old Node server when packaged as an APK. server.js/start.bat are retained for the desktop localhost version.
