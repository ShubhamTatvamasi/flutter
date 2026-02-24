# Emulator

List of available devices:
```bash
avdmanager list devices
```

Check system images:
```bash
sdkmanager --list | grep system-images
```

Install system images for `mobile` and `tablet`:
```bash
sdkmanager --install "system-images;android-35;google_apis;arm64-v8a"
sdkmanager --install "system-images;android-35;google_apis_tablet;arm64-v8a"
```

List installed images:
```bash
sdkmanager --list_installed
```

Create Pixel Device for mobile:
```bash
avdmanager create avd \
  -n Pixel7Mobile \
  -k "system-images;android-35;google_apis;arm64-v8a" \
  -d "pixel_7"
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
avdmanager list avd
```

Start emulator:
```bash
emulator -avd Pixel7Mobile
emulator -avd Nexus7Tablet
emulator -avd Nexus10Tablet
```

Run app on emulator:
```bash
flutter run -d emulator-5556
flutter run -d Pixel
```

Delete system image:
```bash
avdmanager delete avd -n Pixel7Mobile
avdmanager delete avd -n Nexus7Tablet
avdmanager delete avd -n Nexus10Tablet
```



