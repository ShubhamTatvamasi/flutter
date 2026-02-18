# flutter

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
echo 'export PATH="$JAVA_HOME/bin:$ANDROID_HOME/platform-tools:/opt/homebrew/share/android-commandlinetools/cmdline-tools/latest/bin:$PATH"' >> ~/.zshrc

source ~/.zshrc
```

Install SDK Components:
```bash
sdkmanager --sdk_root=$ANDROID_HOME "platform-tools" "platforms;android-34" "build-tools;34.0.0"
```

Link cmdline-tools:
```bash
ln -s /opt/homebrew/share/android-commandlinetools/cmdline-tools \
  $ANDROID_HOME
```

Check Flutter doctor:
```bash
flutter doctor -v
```

Create a new flutter project:
```bash
flutter create \
  --org com.shubhamtatvamasi \
  --project-name flutter_bounce .
```

List all the devices:
```bash
flutter devices
```

Start the app on your device:
```bash
flutter run -d I2220
```
