# PitchPlan Android starter

This package contains the supplied PitchPlan website plus a Capacitor Android wrapper configuration and basic service-worker caching.

## Build APK
Requirements: Node.js LTS, Android Studio, Android SDK.

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

In Android Studio: Build > Build Bundle(s) / APK(s) > Build APK(s).

## Offline notes
The service worker caches the entry page and same-origin resources as they are visited. For reliable offline poster creation, test every poster workflow and ensure its fonts, templates, images, and rendering libraries are local. Features requiring live scores, remote APIs, or cloud AI will still require internet. Offline AI image generation needs a compatible on-device model and is not included automatically.

## Automatic APK build (GitHub Actions)
1. Create a private GitHub repository and upload this project.
2. Open Actions and run **Build PitchPlan Android APK** (or push to main/master).
3. Download the `pitchplan-debug-apk` artifact from the completed workflow run.
4. The artifact contains `app-debug.apk`, ready for testing on Android.

The supplied PitchPlan logo is prepared as `assets/icon.png` and the workflow generates Android launcher icons.
