---
title: Add the predictive back gesture
shortTitle: Predictive back
description: >-
  Learn how to support the predictive back gesture in your Android app.
---

Flutter supports the predictive back gesture on Android by default.
However, to opt in to the platform feature,
you must configure your Android app.

## Configure your app

To support the predictive back gesture,
your app must target Android API level 33 (Android 13) or higher.

To opt in, add the `android:enableOnBackInvokedCallback="true"` attribute
to the `<application>` tag
in your `android/app/src/main/AndroidManifest.xml` file:

```xml
<application
    ...
    android:enableOnBackInvokedCallback="true">
</application>
```

## Configure your device

Depending on the Android version of your test device,
you might need to enable the gesture in the system settings:

*   **Android 13 (API level 33):**
    Enable **Predictive back animations** under
    **Settings** > **System** > **Developer options**.
*   **Android 14 (API level 34) and higher:**
    The gesture and its animations are enabled by default.

## Run your app

To run your app with predictive back support,
use Flutter 3.38 or higher.

## See also

For details,
see [Android predictive back][].

[Android predictive back]: /release/breaking-changes/android-predictive-back
