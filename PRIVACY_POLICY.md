# Privacy Policy for MotoKey+ & MotoKey Action

**Effective Date:** September 27, 2026  
**Last Updated:** September 27, 2026

**MotoKey+** and its companion engine **MotoKey Action** (collectively, "the Applications") are developed as local device utilities designed to empower users to customize and expand the physical Action Button on supported Motorola smartphones.

We believe strongly in user privacy and data minimization. This Privacy Policy explains our practices regarding user data and device permissions.

---

## 1. Summary: Zero Data Collection

* **No Data Collection:** MotoKey+ does **not** collect, store, log, or track any personal information, device identifiers, or usage telemetry.
* **No Network Transmission:** The Applications do not request or utilize Android's `INTERNET` permission (`android.permission.INTERNET`). It is technically impossible for the Applications to transmit any data off your device.
* **No Third-Party SDKs:** The Applications do not contain any advertising networks, behavioral tracking tools, or external analytics SDKs.
* **No User Accounts:** You do not need to register, create an account, or provide personal credentials to use MotoKey+.

---

## 2. Accessibility Service Usage (Prominent Disclosure)

MotoKey+ includes an optional Android Accessibility Service (`MotoKeyAccessibilityService`).

* **Purpose:** The Accessibility Service is utilized solely to execute Android's built-in global screenshot action (`GLOBAL_ACTION_TAKE_SCREENSHOT`) when you press your phone's physical Action Button.
* **Privacy & Least Privilege:**
  * The service does **not** read, inspect, capture, or record your screen content, passwords, personal messages, or notifications.
  * The service does **not** perform automated gestures, user interface scraping, or keystroke logging.
  * In compliance with the Principle of Least Privilege, the service requests zero window content inspection capabilities (`canRetrieveWindowContent="false"`) and registers no event listeners.
* **Consent:** The Accessibility Service is disabled by default. It is only enabled when you explicitly review the in-app disclosure and grant permission in Android's Accessibility Settings. You may revoke this permission at any time in system settings.

---

## 3. Other Device Permissions

The Applications request only the minimum Android permissions required to fulfill user-triggered actions:

* **Camera (`android.permission.CAMERA`):**  
  Used exclusively to access `CameraManager.setTorchMode()` to toggle your phone's flashlight/LED. The Applications never access camera sensors, preview streams, or record photo/video content.
* **Vibrate (`android.permission.VIBRATE`):**  
  Used solely to deliver short tactile haptic feedback when the Action Button is pressed.
* **Do Not Disturb Access (`android.permission.ACCESS_NOTIFICATION_POLICY`):**  
  Optionally requested if you configure the Action Button to toggle Do Not Disturb (DND) modes.
* **Ignore Battery Optimization (`android.permission.REQUEST_IGNORE_BATTERY_OPTIMIZATIONS`):**  
  Ensures instant, zero-latency response when pressing the hardware Action Button without being terminated by Android's background app killer.

---

## 4. Children’s Privacy

The Applications do not collect data from anyone, including children under the age of 13.

---

## 5. Changes to This Privacy Policy

If we make updates to this Privacy Policy, the revised policy will be posted within this repository and updated in the application store listing.

---

## 6. Contact Us

If you have questions about this Privacy Policy or MotoKey+, please contact the developer via GitHub:
[https://github.com/XandarNull/motokeyplus](https://github.com/XandarNull/motokeyplus)
