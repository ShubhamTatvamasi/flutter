# Debug

```bash
flutter build appbundle --release --verbose 2>&1 | grep -A 5 -i "error\|strip\|symbol"
```



### Gradle

Stop all Gradle daemons
```bash
./android/gradlew --stop
pkill -f gradle
```

Delete ALL Gradle caches
```bash
rm -rf ~/.gradle/caches
rm -rf ~/.gradle/daemon
rm -rf ~/.gradle/kotlin-profile
```

Also delete project-level
```bash
rm -rf android/.gradle
```

Clean Flutter
```bash
flutter clean
```
