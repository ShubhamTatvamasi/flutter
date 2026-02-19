# Debug

```bash
flutter build appbundle --release --verbose 2>&1 | grep -A 5 -i "error\|strip\|symbol"
```
