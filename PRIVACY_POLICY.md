# Privacy Policy for MotoKey+

**Effective Date:** September 27, 2026  
**Last Updated:** September 28, 2026

**MotoKey+** ("the Application") is developed as a standalone, privacy-first local device utility designed to empower users to customize and expand the physical Action Key on supported Motorola smartphones.

We believe strongly in user privacy, transparency, and data minimization. This Privacy Policy details our practices regarding user data and device permissions.

---

## 1. Summary: Zero Data Collection & Pure Offline Operation

* **Zero Data Collection:** MotoKey+ does **not** collect, record, log, store, or monitor any personal information, device identifiers, app usage statistics, or telemetry.
* **Pure Offline Operation:** The Application does **not** request or use Android's Internet permission (`android.permission.INTERNET`). Because network access is completely omitted from the application manifest, it is technically impossible for MotoKey+ to transmit any data off your device.
* **Zero Third-Party SDKs:** The Application integrates no third-party analytics libraries (such as Firebase Analytics or Google Analytics), no crash-reporting trackers, and no advertising networks.
* **No User Accounts:** You do not need to register, create an account, log in, or provide personal credentials to use MotoKey+.

---

## 2. Accessibility Service Usage (Prominent Disclosure)

MotoKey+ includes an optional Android Accessibility Service (`MotoKeyAccessibilityService`).

* **Purpose:** The Accessibility Service is used exclusively to:
  1. Intercept physical Action Key presses (hardware key events and Push-To-Talk events) to execute your chosen gestures (Single Press, Double Press, and Press & Hold).
  2. Perform standard Android system global actions directly via the official Accessibility API, specifically:
     - Taking screenshots (`GLOBAL_ACTION_TAKE_SCREENSHOT`)
     - Pulling down the notification shade (`GLOBAL_ACTION_NOTIFICATIONS`)
     - Opening the Quick Settings panel (`GLOBAL_ACTION_QUICK_SETTINGS`)
* **Privacy & Least Privilege:**
  * **No Screen Reading:** The service explicitly sets `canRetrieveWindowContent="false"`. It cannot inspect, read, parse, or access your screen content, text, passwords, messages, or financial information.
  * **No Keystroke Logging:** The service does not log, record, or track general keyboard input.
  * **No Automated Touch Scraping:** The service does not simulate arbitrary screen taps, gesture automation, or user interface scraping.
* **Consent:** The Accessibility Service is strictly disabled by default. It is only enabled when you explicitly review the in-app disclosure and manually grant permission within Android's system Accessibility settings. You can revoke this permission at any time via your device's System Settings.

---

## 3. Device Permissions

The Application requests only the absolute minimum permissions necessary to deliver local key-remapping features:

* **Vibrate (`android.permission.VIBRATE`):**  
  Used solely to provide tactile haptic feedback vibrations when the physical Action Key is pressed.
* **Flashlight / Torch:**  
  Controlled strictly via Android's hardware `CameraManager.setTorchMode()` API. MotoKey+ does **not** request or require the Camera permission (`android.permission.CAMERA`), does not open camera sensors, and does not capture photo or video data.

---

## 4. Children’s Privacy

The Application does not collect or solicit information from anyone, including children under the age of 13.

---

## 5. Changes to This Privacy Policy

If updates are made to this Privacy Policy, the revised policy will be posted directly within the application repository and linked in the Google Play Store listing.

---

## 6. Contact Us

If you have questions, feedback, or concerns regarding this Privacy Policy or MotoKey+, please contact the developer via GitHub:  
[https://github.com/XandarNull/motokeyplus](https://github.com/XandarNull/motokeyplus)
