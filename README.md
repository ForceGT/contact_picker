# fluttercontactpicker
[![pub.dev](https://img.shields.io/badge/pub-2.4.3-green.svg)](https://pub.dev/packages/fluttercontactpicker#-readme-tab-)

Interact with native OS contact pickers using Flutter

## Getting Started

### Permissions

#### Android

If you intend to use the FullContact class through the ```pickContact``` method (which grabs the entire Contact info **only on Android**), you need to add the following to the ```android/app/src/AndroidManifest.xml``` file

 ``` <uses-permission android:name="android.permission.READ_CONTACTS"/> ```

**Note**: Permission on Android not needed for PhoneContact through the ```pickPhoneContact``` method (which grabs the name and the number) and EmailContact through the ```pickEmailContact``` method (which grabs the name and the email)

#### IOS

**You cannot use the ```pickContact``` method as there is no native mechanism on IOS to do so**
For other methods
Add the following to the ```ios/Runner/Info.plist```
```
<key>NSContactsUsageDescription</key>
<string>Your reason here</string>
```


### Grab contact.
```dart
final PhoneContact contact =
                    await FlutterContactPicker.pickPhoneContact();
```

For more info read the docs or take a look at the example
