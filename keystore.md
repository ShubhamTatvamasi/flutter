# keystore

Generate upload Key:
```bash
keytool -genkey -v \
  -keystore ~/upload-keystore.jks \
  -keyalg RSA \
  -keysize 2048 \
  -validity 10000 \
  -alias upload
```

Verify:
```bash
keytool -list -v -keystore ~/upload-keystore.jks -alias upload
```

Setup `key.properties` inside flutter project:
```bash
vim android/key.properties
```

`key.properties` file:
```bash
storePassword=<password-from-previous-step>
keyPassword=<password-from-previous-step>
keyAlias=upload
storeFile=<keystore-file-location>
```
> Both passwords are same
