# Privacy Policy for MotoKey+

**Effective Date:** October 10, 2026  
**Last Updated:** October 10, 2026

**MotoKey+** ("the Application") is developed as an open, privacy-first, standalone local utility designed to empower users to customize and expand the physical Action Key on supported Motorola smartphones.

We believe uncompromisingly in user privacy, complete transparency, and data minimization. This Privacy Policy details our practices regarding user data, local storage, and device permissions.

---

## 1. Summary: Zero Data Collection & Pure Offline Operation

* **Zero Data Collection:** MotoKey+ does **not** collect, record, log, store, monitor, or transmit any personal information, device identifiers, hardware serials, location data, or telemetry.
* **Pure Offline Operation:** The Application does **not** declare, request, or use Android's Internet permission (`android.permission.INTERNET`). Because network access is completely omitted from the application manifest, it is technically impossible for MotoKey+ to send or receive data over the internet or communicate with remote servers.
* **Zero Third-Party SDKs & Trackers:** The Application incorporates no third-party tracking libraries, analytics frameworks (such as Firebase Analytics, Flurry, or Google Analytics), crash-reporting services, advertising SDKs, or external trackers.
* **No User Accounts:** You are never asked to register, create an account, log in, or provide personal credentials. The app operates 100% locally on your device.

---

## 2. Accessibility Service Usage (Prominent Disclosure)

MotoKey+ includes an optional Android Accessibility Service (`MotoKeyAccessibilityService`).

* **Purpose:** The Accessibility Service is used strictly and exclusively to:
  1. Intercept physical Action Key broadcasts and key events (`android.intent.action.PTT.down` / `android.intent.action.PTT.up`) to recognize your configured hardware gestures (Single Press, Double Press, and Press & Hold).
  2. Execute standard Android global actions directly via the official Accessibility API upon key press:
     - Taking screenshots (`GLOBAL_ACTION_TAKE_SCREENSHOT`)
     - Expanding the notification panel (`GLOBAL_ACTION_NOTIFICATIONS`)
     - Expanding the Quick Settings panel (`GLOBAL_ACTION_QUICK_SETTINGS`)
* **Privacy & Least Privilege Safeguards:**
  * **No Screen Content Reading:** The service explicitly configures `canRetrieveWindowContent="false"`. MotoKey+ cannot inspect, read, parse, extract, or log your screen contents, text, passwords, messages, contacts, or financial details.
  * **No Keystroke Logging:** The service does not log or monitor general keyboard input or touch typing.
  * **No Automated Touch Scraping:** The service does not simulate arbitrary screen taps, touch gestures, or UI automation macros.
  * **Event Types:** The service declares `android:accessibilityEventTypes="typeWindowStateChanged"` solely to ensure the Android operating system maintains service binding and hardware key responsiveness across device restarts and window transitions. The service performs zero event processing on window changes.
* **Explicit User Consent:** The Accessibility Service is disabled by default. It can only be activated when you explicitly review the in-app prominent disclosure dialog and manually enable the service within Android System Settings. You retain the right to revoke this permission at any time via *Settings → Accessibility*.

---

## 3. Device Permissions

The Application requests only the minimal set of Android permissions necessary to deliver local key-remapping functions:

* **Vibrate (`android.permission.VIBRATE`):**  
  Used solely to deliver haptic tactile vibration feedback when a hardware Action Key gesture is recognized.
* **Wake Lock (`android.permission.WAKE_LOCK`):**  
  Used solely to acquire a temporary partial CPU wake lock for sub-second fractions of a second during physical key gesture recognition windows (e.g. evaluating rapid double-presses or press-and-hold durations) while the screen is off. This guarantees zero hardware lag without CPU suspend latency. The wake lock is released immediately once an action dispatches and is never held while idle.
* **Do Not Disturb Access (`android.permission.ACCESS_NOTIFICATION_POLICY`):**  
  Used solely to toggle system Do Not Disturb (DND) modes when you explicitly assign the Action Key to the Do Not Disturb action.
* **Battery Optimization Exemption (`android.permission.REQUEST_IGNORE_BATTERY_OPTIMIZATIONS`):**  
  Used solely to prompt the native system dialog allowing MotoKey+ to remain active during Android Doze mode, ensuring physical hardware key presses are never dropped while the phone is asleep.
* **Direct Dial Phone Calls (`android.permission.CALL_PHONE`):**  
  Used optionally and strictly when you map an Action Key gesture to a contact's Direct Dial shortcut. If this permission is not granted by the user, MotoKey+ automatically and safely falls back to opening the system phone dialer (`Intent.ACTION_DIAL`) with the phone number pre-filled, never initiating automated calls without your consent.
* **Boot Completion (`android.permission.RECEIVE_BOOT_COMPLETED`):**  
  Used solely to initialize the background hardware listener (`BootReceiver`) upon device reboot, ensuring physical Action Key gestures function immediately after restarting your phone without requiring manual app launch.
* **Flashlight / Torch API:**  
  Controlled directly via the official Android `CameraManager.setTorchMode()` API. MotoKey+ does **not** request or use the Camera permission (`android.permission.CAMERA`), does not access camera image sensors, and does not capture photos or videos.
* **On-Screen Pop-Up Notifications:**  
  Transient visual feedback pills (such as "Ring" or "Vibrate") are rendered using the native `TYPE_ACCESSIBILITY_OVERLAY` window flag. MotoKey+ does **not** request notification posting permissions (`android.permission.POST_NOTIFICATIONS`) and never displays advertisements or status bar push notifications.

---

## 4. Local Preferences & App Shortcuts

* **Local Preference Storage:** All user configurations (selected gesture actions, timeout durations, haptic toggles, and shortcut mappings) are stored locally in private application preferences (`SharedPreferences`) sandboxed within your device's internal storage (`/data/data/app.xandar.motokeyplus`). They are never backed up to remote clouds or shared with third parties.
* **App Shortcuts & Deep Links:** When you assign an Action Key gesture to launch a specific installed app or third-party shortcut (such as a messaging contact, navigation destination, or web bookmark), MotoKey+ merely passes the public Android `Intent` to the target app via the Android framework. MotoKey+ does not monitor, collect, or log your interactions within third-party applications.

---

## 5. Children’s Privacy

MotoKey+ does not collect, store, or transmit personal data from any users, including children under the age of 13.

---

## 6. Changes to This Privacy Policy

Any future revisions or updates to this Privacy Policy will be published directly within the application repository and linked within the app settings and Google Play Store listing.

---

## 7. Contact Information

If you have questions, feedback, or inquiries regarding this Privacy Policy or MotoKey+, please contact the developer via GitHub:  
[https://github.com/XandarNull/motokeyplus](https://github.com/XandarNull/motokeyplus)
