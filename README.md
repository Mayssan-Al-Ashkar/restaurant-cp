# Restaurant App

A Flutter-based restaurant application (mobile, web, desktop) that provides menu browsing, ordering/cart, user authentication, and Firebase integration. This repository is the source for the app found in `lib/` and platform folders for Android, iOS, macOS, Windows and Linux.

**Status:** Development

**Contents:**
- `lib/` — Flutter app source; main entry is `lib/main.dart`.
- `android/`, `ios/`, `macos/`, `windows/`, `linux/`, `web/` — platform integration and build configs.
- `assets/` — fonts, icons, images, and video used by the app.
- `test/` — widget/unit tests.

## Features
- Menu browsing and categories
- Cart and order flow
- User authentication (Firebase)
- Firebase integrations (analytics, auth, remote config, etc. — repo contains `google-services.json` and `GoogleService-Info.plist` placeholders)

## Prerequisites
- Flutter SDK (stable channel recommended). See https://flutter.dev/docs/get-started/install
- Platform tooling as needed: Android SDK / Android Studio, Xcode for iOS/macOS, Visual Studio for Windows, etc.
- (Optional) Firebase CLI for configuring back-end services.

## Quick start

1. Clone the repository:

```
git clone <repo-url>
cd restaurant-app
```

2. Get Dart/Flutter dependencies:

```
flutter pub get
```

3. Run the app on a connected device or emulator:

```
flutter run -d <device-id>
```

Replace `<device-id>` with `android`, `ios`, `chrome`, or the device name from `flutter devices`.

## Firebase configuration
This project contains Firebase config files in platform folders (e.g. `android/app/google-services.json`, `ios/Runner/GoogleService-Info.plist`) and a generated `lib/firebase_options.dart`. If you need to re-configure Firebase for your own project:

- Create a Firebase project at https://console.firebase.google.com/
- Add Android and iOS apps there and download the platform config files.
- Replace the config files in the respective platform folders.
- Regenerate `lib/firebase_options.dart` by following the instructions from `flutterfire` CLI if you use it.

## Build

Build APK (Android):

```
flutter build apk --release
```

Build iOS (on macOS):

```
flutter build ios --release
```

Build web:

```
flutter build web
```

## Tests & Analysis

Run unit and widget tests:

```
flutter test
```

Static analysis:

```
flutter analyze
```

Format code:

```
dart format .
```

## Project structure (high level)

- `lib/main.dart` — app entrypoint
- `lib/src/` — modular app code
  - `features/` — feature folders (authentication, menus, ordering, etc.)
  - `view_models/` — state management classes
  - `service/` — API, storage, and network services
  - `components/` — reusable widgets

## Contributing
- Open issues or PRs for bugs and features.
- Follow the existing code style and run `flutter analyze` and `dart format` before submitting.

## Known files of interest
- `pubspec.yaml` — dependency list and assets
- `lib/firebase_options.dart` — auto-generated Firebase options
- `android/app/google-services.json` and `ios/Runner/GoogleService-Info.plist` — Firebase platform configs

## Contact
For questions about the project, contact the maintainer or open an issue in the repository.

---
Generated on 2025-12-14 by project assistant.

