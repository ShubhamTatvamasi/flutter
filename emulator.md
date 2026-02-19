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

