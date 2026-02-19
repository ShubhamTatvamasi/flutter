# flutter

### Setup

Install OpenJDK and flutter:
```bash
brew install openjdk@17
brew install --cask flutter
brew install --cask android-platform-tools
brew install --cask android-commandlinetools
```

Set ANDROID_HOME and JAVA_HOME paths:
```bash
echo 'export JAVA_HOME="/opt/homebrew/opt/openjdk@17"' >> ~/.zshrc
echo 'export ANDROID_HOME="$HOME/Library/Android/sdk"' >> ~/.zshrc
echo 'export ANDROID_SDK_ROOT="$HOME/Library/Android/sdk"' >> ~/.zshrc
echo 'export PATH="$JAVA_HOME/bin:$ANDROID_HOME/emulator:$ANDROID_HOME/platform-tools:$ANDROID_HOME/cmdline-tools/latest/bin:$PATH"' >> ~/.zshrc

source ~/.zshrc
```

Link cmdline-tools:
```bash
ln -s /opt/homebrew/share/android-commandlinetools/cmdline-tools \
  $ANDROID_HOME

ln -s /opt/homebrew/share/android-commandlinetools/system-images \
  $ANDROID_HOME
```

Install SDK Components:
```bash
sdkmanager --sdk_root=$ANDROID_HOME \
  "platform-tools" \
  "platforms;android-34" \
  "build-tools;34.0.0" \
  "platforms;android-36" \
  "build-tools;36.0.0" \
  "build-tools;28.0.3" \
  "ndk;26.1.10909125" \
  "emulator"
```

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

