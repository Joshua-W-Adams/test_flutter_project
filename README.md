# flutter_firebase_boilerplate

Boilerplate for apps using Flutter & Firebase.

## Getting Started

1. Configure flutter development environment as per Flutter online instructions

2. Clone the git repository

```
git clone url
```

3. Get flutter dependencies

```
flutter pub get
```

4. Prepare firebase project for web use

```
flutter channel beta
flutter upgrade
flutter config --enable-web
```

4. Configure firebase project

- Create a new project with the Firebase console
- Enable email/password signin method in the firebase console
- Enable firestore database in the firebase console

5. Configure android and ios apps

- Add iOS and Android apps in the Firebase project settings
- On Android, use `com.example.flutter_firebase_boilerplate` as the package name
- then, [download and copy](https://firebase.google.com/docs/flutter/setup#configure_an_android_app) `google-services.json` into `android/app`
- On iOS, use `com.example.flutter_firebase_boilerplate` as the bundle ID
- then, [download and copy](https://firebase.google.com/docs/flutter/setup#configure_an_ios_app) `GoogleService-Info.plist` into `iOS/Runner`, and add it to the Runner target in Xcode

6. Configure web app

- Add a web app in the Firebase project settings
- Export the generated `firebaseConfig` variable inside a `./firebase-config.js` file in your project

```
export var firebaseConfig = {
    apiKey: "<your-api-key>",
    authDomain: "<your-auth-domain>",
    databaseURL: "<your-database-url>",
    projectId: "<your-project-id>",
    storageBucket: "<your-storage-bucket>",
    messagingSenderId: "<your-messaging-sender-id>",
    appId: "<your-app-id>",
    measurementId: "<your-measurement-id>"
};
```

7. Configure CI / CD

    1. Go to https://codemagic.io/

    2. Setup workflow for new project

## References

This project borrows many ideas from the existing repository https://github.com/bizz84/starter_architecture_flutter_firebase with additions and modifications made to customise and improve functionality.
