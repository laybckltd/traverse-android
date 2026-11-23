# Traverse — Android App Source Kit

This project wraps **Traverse** (`https://wonderful-creponne-588f15.netlify.app`) as a native Android application (`com.laybck.traverse`) with hardware-accelerated WebView, offline Service Worker / DOM cache fallback, pull-to-refresh, file backup/CSV export support, and native launcher icons.

---

## Option A — Build APK in the Cloud via GitHub Actions (No Android Studio needed)

1. Unzip this folder and push it to a new GitHub repository.
2. Open the **Actions** tab on GitHub and run **Build Traverse Android APK**.
3. Download the generated **`traverse-debug-apk`** artifact and install `app-debug.apk` on your Android phone.

---

## Option B — Build APK Locally in Android Studio

1. Open this folder in **Android Studio (Ladybug / Hedgehog or newer)**.
2. Wait for Gradle sync to finish.
3. Choose **Build → Build Bundle(s) / APK(s) → Build APK(s)** (or run `./gradlew assembleDebug` if Gradle is installed).
4. Copy `app/build/outputs/apk/debug/app-debug.apk` to your Android device and tap to install.

---

## Option C — Trusted Web Activity (Bubblewrap Play Store APK)

If you want a lightweight Play-Store-ready TWA backed directly by Chrome:

```bash
npx @bubblewrap/cli init --manifest=https://wonderful-creponne-588f15.netlify.app/manifest.webmanifest
npx @bubblewrap/cli build
```
