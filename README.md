# flutter

Install OpenJDK and flutter:
```bash
brew install openjdk@17
brew install --cask flutter
brew install --cask android-platform-tools
```

Link OpenJDK:
```bash
sudo ln -sfn /opt/homebrew/opt/openjdk@17/libexec/openjdk.jdk \
  /Library/Java/JavaVirtualMachines/openjdk-17.jdk
```

Set JAVA_HOME:
```bash
echo 'export JAVA_HOME=$(/usr/libexec/java_home -v 17)' >> ~/.zshrc
echo 'export PATH="$JAVA_HOME/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
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
