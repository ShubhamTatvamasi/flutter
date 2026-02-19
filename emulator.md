# Emulator

List of available devices:
```bash
avdmanager list devices
```

Check system images:
```bash
sdkmanager --list | grep system-images
```

Install tablet emulator:
```bash
sdkmanager --install "system-images;android-35;google_apis_tablet;arm64-v8a"
```

Create 7 inch tablet:
```bash
avdmanager create avd \
  -n Nexus7Tablet \
  -k "system-images;android-35;google_apis_tablet;arm64-v8a" \
  -d "Nexus 7 2013"
```

Create 10 inch tablet:
```bash
avdmanager create avd \
  -n Nexus10Tablet \
  -k "system-images;android-35;google_apis_tablet;arm64-v8a" \
  -d "Nexus 10"
```

List virtual devices:
```bash
emulator -list-avds
```

Start emulator:
```bash
emulator -avd Nexus7Tablet
emulator -avd Nexus10Tablet
```

Run app on emulator:
```bash
flutter run -d Pixel
```

Delete system image:
```bash
avdmanager delete avd -n Nexus7Tablet
```



