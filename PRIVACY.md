# TouchPause privacy notice

Effective: 2026-10-12 (version 1.0.20)

TouchPause pauses touchscreen input locally. Version 1.0.20 has no usage
analytics, tracking SDK, advertising, account registration or developer-operated
server. There is no statistics prompt or statistics setting.

## Data collection and network access

TouchPause never sells data or sends touchscreen, stylus, hardware-key or screen
content to anyone. It does not collect setup, pause or purchase-path statistics.

The optional lifetime unlock uses Google Play Billing. The Billing Library
declares `INTERNET` and `ACCESS_NETWORK_STATE` and may exchange billing requests
and diagnostic information with Google under Google's terms. Google Play
returns localized product details and purchase status. TouchPause handles a
purchase token in memory long enough to grant and acknowledge access, but does
not store it or send it to the developer. Touch or key events are never part of
billing traffic.

## Earlier statistics builds

Versions 1.0.18 and 1.0.19 contained optional Google Analytics for Firebase.
Version 1.0.20 removes the SDK completely, including its startup components and
all usage-event collection. Previous choices cannot enable statistics in this
version. Update to 1.0.20 to stop collection from an older statistics build.

Removing the SDK does not retroactively delete reports already uploaded to
Google. The previous project used two-month user/event retention without renewal
on activity; aggregate reports may be retained longer. Contact us below about
previous data or deletion requests. No new analytics data is sent by 1.0.20.

## Data stored on the device

TouchPause stores these values in private app data:

- selected volume release key;
- whether Android has observed the Quick Settings tile;
- message and vibration choices;
- selected app language;
- the version of the Accessibility disclosure accepted by the user;
- number of successfully started free sessions;
- the current local day and daily free-use count;
- cached Google Play lifetime-access status;
- whether a valid store-review code enabled review access;
- short-lived advisory state indicating that a pause is active.


TouchPause disables Android backup and excludes app storage from cloud backup
and device-to-device transfer. Clearing app data or uninstalling removes local
preferences and the trial count. Google Play can restore a lifetime purchase
for the purchasing account.

## Accessibility service and input data

TouchPause requires Android 14 or newer. After the user accepts the in-app
disclosure and explicitly enables the service in Android settings, the service:

- cannot retrieve window content;
- requests touchscreen and stylus motion plus hardware-key filtering only
  while a user-started pause is active;
- prevents other apps from receiving the captured touchscreen and stylus
  motion;
- receives all hardware-key events during that pause, uses them only to detect
  the selected volume release key, and forwards unrelated keys;
- processes all input only in memory on the device; and
- immediately discards every received input event without storing or
  transmitting it.

Raw touchscreen and stylus motion can include coordinates, timing, pressure,
and tool information. TouchPause receives those fields only because Android
must route the motion to the Accessibility service in order to withhold it from
other apps.

TouchPause does not request root access and packages no native input helper.
Disabling its Accessibility service prevents all touch-pausing functionality.
Stopping the service or rebooting removes active capture.

## Changes and questions

Material changes update this notice and its effective date. The current public
policy is published at
[github.com/bzhangj13zzz/touchpause-privacy](https://github.com/bzhangj13zzz/touchpause-privacy/blob/main/PRIVACY.md).

Questions about privacy or support can be sent to
[bzhangj13@gmail.com](mailto:bzhangj13@gmail.com).
