# Build and release an Android app in appcenter

- [Flutter](https://flutter.dev/docs/deployment/android)
- [appcenter](https://buildflutter.com/deploying-flutter-apps-via-appcenter/)

1- Signing the app

* Go to java/jdk/bin and inside execute this code changing USER_NAME for your user

./keytool -genkey -v -keystore c:\Users\USER_NAME\key.jks -storetype JKS -keyalg RSA -keysize 2048 -validity 10000 -alias key

* Go to your flutter project <app dir>/android/app/build.gradle and apply the changes that [Flutter](https://flutter.dev/docs/deployment/android)

2- Building the app for release (two options).

* flutter build appbundle (recommended however not supporting for some Stores)
* flutter build apk --split-per-abi 

-----------------------------------------------------------------------------------------------------------------------------

Appcenter: two options

1- Build the flutter app directly after signing the app you do not need to run flutter build appbundle [appcenter](https://buildflutter.com/deploying-flutter-apps-via-appcenter/) (complex)

This projects is about building the flutter app directly in appcenter.

2- Generate the apk with flutter build apk --split-per-abi after signing the app and release it in appcenter (simple)


