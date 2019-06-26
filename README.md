# firebase-auth-tensor-update
"Authenticating Users with Google in Firebase and Firestore inside of Dart's Flutter Framework" **UPDATE**

This is an updated codebase reflecting the latest libraries for tensor prgramming's excellent video on the subject. It corrects the error with `_googleSignIn.signIn()` in `api.dart`. I also added `!snapshot.hasData` and `snapshot.hasData` into `home.dart` to avoid errors.

If you're looking for keytool on Windows: `"C:\Program Files\Android\Android Studio\jre\bin\keytool" -list -v -alias androiddebugkey -keystore %USERPROFILE%\.android\debug.keystore`

video: https://youtu.be/ZNt_e5ojGzQ


```
pubspec.yaml:
cloud_firestore: ^0.12.5
firebase_storage: ^3.0.2
firebase_core: ^0.4.0
firebase_auth: ^0.11.0
google_sign_in: ^4.0.2

../android/app/src/build.gradle:
defaultConfig {
        ...
        targetSdkVersion 28
        ...
        multiDexEnabled true
 }
 dependencies {
    implementation 'com.google.firebase:firebase-core:16.0.9'
    implementation 'com.google.firebase:firebase-auth:16.1.0'
    implementation 'com.android.support:multidex:1.0.3'
}

../android/gradle.properties:
android.useAndroidX=true
android.enableJetifier=true
```
