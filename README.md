# RISE 365 — Android APK project

This is the Android Studio project for the RISE 365 mobile app. It wraps the complete RISE 365 planner in a native Android WebView shell and bundles the selected official logo and app icon.

## Build an APK in Android Studio
1. Install Android Studio on a computer.
2. Open this project folder (`RISE365_Android_Project`) in Android Studio.
3. Allow Gradle sync to finish. Use JDK 17 if prompted.
4. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. Android Studio creates the debug APK at:
   `app/build/outputs/apk/debug/app-debug.apk`

## Build through GitHub Actions (no local Android SDK needed)
1. Create a new GitHub repository.
2. Upload the contents of this folder to the repository's `main` branch.
3. Open the repository's **Actions** tab.
4. Select **Build RISE 365 APK** and click **Run workflow** (or push to `main`).
5. When it completes, open the workflow run and download the `RISE365-Android-debug` artifact. It contains `app-debug.apk`.

## Install on Redmi Note 13 Pro 5G
1. Download `app-debug.apk` to your phone.
2. Open it in File Manager.
3. If Android asks, allow your browser/file manager to install unknown apps.
4. Tap Install, then open **RISE 365**.

## Included
- Official selected RISE 365 logo and launcher icon
- Daily 365-day planner and checklists
- Five roadmap phases and complete side drawer
- Light/dark theme switch
- Progress, completion and streak counters
- Local progress persistence and JSON export
- External learning links open in the browser

## Important limitations in this first APK build
- Progress is saved locally in the app's WebView storage on this phone; it does not sync to other devices.
- This project does not yet include push notifications, account login, cloud backup or a signed Play Store release.
- The APK must be built using Android Studio or the included GitHub Actions workflow. This environment does not have the Android SDK/Gradle build toolchain installed, so it cannot compile and attach the APK directly here.
