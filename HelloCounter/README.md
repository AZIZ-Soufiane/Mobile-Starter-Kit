# 📱 HelloCounter

**HelloCounter** is a simple Android application built with **Jetpack Compose**.  
It demonstrates the use of **Material 3**, **accessibility (a11y)**, and APK generation.

---

## ✨ Features

- 📝 **Form**: enter a first name and display a greeting message
- 🔢 **Interactive counter** with **+ / -** buttons
- 🎨 **Material 3 theme** with dynamic colors (Android 12+)
- ♿ **Accessibility**: TalkBack support, `contentDescription`, tappable areas ≥ 48dp
- 💾 **State persistence** with `rememberSaveable`

---

## 🚀 Build & Install

### Command line

```bash

./gradlew assembleDebug
adb install -r app/build/outputs/apk/debug/app-debug.apk
📱 Tested on
Pixel 7a API 34 (emulator)

✨ Includes

Material 3 + dynamic colors

Accessibility (a11y): TalkBack descriptions, 48dp touch targets

Persistent states (rememberSaveable)

✅ DoD
 Global theme AppTheme applied.

 Texts centralized in strings.xml.

 Accessibility validated (contentDescription, sizes, focus order).

 Debug APK built and installable.

 README + screenshots included in the repository.

🩹 Troubleshooting
Empty Preview → Build → Rebuild Project

Text not read by TalkBack → check contentDescription

APK not installable → check applicationId, uninstall previous version

Unreadable colors → disable dynamicColor if Android < 12

⚡ Cheatsheet
kotlin
Copy code
// Global theme
AppTheme { MainScreen() }

// Accessibility for meaningful icon
.semantics { contentDescription = stringResource(R.string.cd_increment) }

// Build APK
./gradlew assembleDebug
adb install -r app/build/outputs/apk/debug/app-debug.apk
1) Generate APK
Option 1 – Android Studio
Open the project in Android Studio

Go to Build → Build Bundle(s) / APK(s) → Build APK(s)

A notification will appear → click Locate to access the generated file

📂 The APK will be located in:
app/build/outputs/apk/debug/