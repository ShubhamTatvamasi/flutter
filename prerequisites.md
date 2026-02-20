# Prerequisites

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

ls -s /opt/homebrew/share/android-commandlinetools/emulator \
  $ANDROID_HOME
```

Install SDK Components:
```bash
sdkmanager --sdk_root=$ANDROID_HOME \
  "platform-tools" \
  "platforms;android-34" \
  "platforms;android-36" \
  "build-tools;34.0.0" \
  "build-tools;35.0.0" \
  "build-tools;36.0.0" \
  "build-tools;28.0.3" \
  "ndk;26.1.10909125"
```
