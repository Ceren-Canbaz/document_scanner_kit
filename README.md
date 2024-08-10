# Document Scanner Kit

![coverage][coverage_badge]
[![style: very good analysis][very_good_analysis_badge]][very_good_analysis_link]
[![License: MIT][license_badge]][license_link]


Generated by the [Very Good CLI][very_good_cli_link] 🤖

> Plugin is under development right now.

Flutter plugin that scans documents with using MLKit for Android and VisionKit for iOS.

## Project Setup

Follow the steps below to set up your Flutter project on Android and iOS

### Android

#### Requirements

- minSdkVersion: 21
- targetSdkVersion: 33
- compileSdkVersion: 34

### iOS

#### Minimum Version Configuration

Ensure you meet the minimum version requirements to run the application on iOS devices. In the ios/Podfile file, make sure the iOS platform version is at least 13.0:

```
platform :ios, '13.0'
```

#### Permission Configuration

Add a String property to the app's Info.plist file with the key [NSCameraUsageDescription](https://developer.apple.com/documentation/bundleresources/information_property_list/nscamerausagedescription) and the value as the description for why your app needs camera access.

```
<key>NSCameraUsageDescription</key>
<string>Camera Usage is Required</string>
```



## Using

```
import 'package:document_scanner_kit/document_scanner_kit.dart' as DocumentScanner;

// Check Permissions before use for iOS, Android doesn't need camera usage permission.

try {
    final result = await DocumentScanner.scan();
    if(result != null) {
        // Do whatever you need with paths.
    }
} catch (e) {
    // Handle Error
}
```




### Integration tests 🧪

Very Good Flutter Plugin uses [fluttium][fluttium_link] for integration tests. Those tests are located 
in the front facing package `document_scanner_kit` example. 

**❗ In order to run the integration tests, you need to have the `fluttium_cli` installed. [See how][fluttium_install].**

To run the integration tests, run the following command from the root of the project:

```sh
cd document_scanner_kit/example
fluttium test flows/test_platform_name.yaml
```

[coverage_badge]: document_scanner_kit/coverage_badge.svg
[license_badge]: https://img.shields.io/badge/license-MIT-blue.svg
[license_link]: https://opensource.org/licenses/MIT
[logo_black]: https://raw.githubusercontent.com/VGVentures/very_good_brand/main/styles/README/vgv_logo_black.png#gh-light-mode-only
[logo_white]: https://raw.githubusercontent.com/VGVentures/very_good_brand/main/styles/README/vgv_logo_white.png#gh-dark-mode-only
[very_good_analysis_badge]: https://img.shields.io/badge/style-very_good_analysis-B22C89.svg
[very_good_analysis_link]: https://pub.dev/packages/very_good_analysis
[very_good_cli_link]: https://github.com/VeryGoodOpenSource/very_good_cli
[very_good_ventures_link]: https://verygood.ventures/?utm_source=github&utm_medium=banner&utm_campaign=core
[very_good_ventures_link_dark]: https://verygood.ventures/?utm_source=github&utm_medium=banner&utm_campaign=core#gh-dark-mode-only
[very_good_ventures_link_light]: https://verygood.ventures/?utm_source=github&utm_medium=banner&utm_campaign=core#gh-light-mode-only
[fluttium_link]: https://fluttium.dev/
[fluttium_install]: https://fluttium.dev/docs/getting-started/installing-cli# document_scanner_kit
