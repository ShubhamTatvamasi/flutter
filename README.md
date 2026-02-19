# flutter

Accept android licenses:
```bash
flutter doctor --android-licenses
```

Check Flutter doctor:
```bash
flutter doctor -v
```

### Build App 

Create a new flutter project:
```bash
flutter create \
  --org com.shubhamtatvamasi \
  --project-name flutter_bounce .
```

Check your build for error:
```bash
flutter analyze
```

List all the devices:
```bash
flutter devices
```

Start the app on your device:
```bash
flutter run -d I2220
```

Deletes all generated build artifacts:
```bash
cd android
./gradlew --stop

rm -rf ~/.gradle/caches
rm -rf ~/.gradle/daemon
rm -rf ~/.gradle/native
rm -rf ~/.gradle/wrapper

flutter clean

rm -rf android/.gradle
rm -rf android/build
```

Build APK for testing:
```bash
flutter build apk
flutter build apk --debug
```

After completion, your APK will be here:
```
build/app/outputs/flutter-apk/app-debug.apk
```

Build the final app for release:
```bash
flutter build appbundle --release
```

### Dart

Generate icon using dart file:
```bash
dart run tool/generate_icons.dart
```

