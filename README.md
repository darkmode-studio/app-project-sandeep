# Settings App (`app-project-sandeep`)

An offline-first Android WebView application featuring an iOS-style left-aligned grouped Settings UI with native Android integration and automated GitHub Actions APK builds.

## What's New in v2.0

- **Fixed Android & CI Build Pipeline**: Added `gradle.properties` (`android.useAndroidX=true`), declared AndroidX dependencies (`core-ktx`, `appcompat`, `activity-ktx`), migrated to AGP 8.5.2 / Gradle 8.7 / Kotlin 1.9.24, removed deprecated manifest `package` attribute, and added manual `workflow_dispatch` support.
- **Native Android Bridge (`MainActivity.kt`)**:
  - Live Dark/Light status bar and navigation bar theming
  - Hardware Back button navigation for WebView sub-pages
  - Real device info readout (manufacturer, model, Android OS version)
  - Haptic feedback and native Toast notifications
  - Direct launchers for Android System Settings (Wi-Fi, Bluetooth, Display, Sound, Battery, Storage, Apps, Privacy)
- **Interactive Grouped Settings UI (`index.html`)**:
  - Real-time search bar across all settings groups
  - Persistent preferences saved in `localStorage`
  - Dark Mode toggle, customizable accent colors, and adjustable text scale (Compact / Default / Large)
  - Dedicated sub-pages for Connectivity, Display & Accent, Notifications & Haptics, Android System Shortcuts, and General & About

## Downloading the APK

Every push to `main` (or manual trigger via **Actions -> Build Android APK**) compiles and uploads `settings-app-v2.0-debug-apk` as a downloadable build artifact.
