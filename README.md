<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# JARVIS Android app

This repository contains the JARVIS Android application.

## Build an APK locally

**Prerequisites:** [Android Studio](https://developer.android.com/studio), Android SDK 36, and JDK 17.

1. Open this repository in Android Studio.
2. Create a `.env` file in the project root and set `GEMINI_API_KEY` if the app uses Gemini features (see `.env.example`).
3. Build the debug APK:

```bash
gradle assembleDebug
```

The APK is generated at `app/build/outputs/apk/debug/app-debug.apk`.

## Download an APK from GitHub Actions

Every push to `main`, pull request, or manual workflow run builds the debug APK. Open the workflow run under **Actions** and download the `jarvis-debug-apk` artifact.

## Release builds

Release builds require a keystore and the `KEYSTORE_PATH`, `STORE_PASSWORD`, and `KEY_PASSWORD` environment variables. The generated release APK is unsigned unless those values are supplied.
