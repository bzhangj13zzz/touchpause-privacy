# TouchPause privacy notice

Effective: 2026-10-12 (regional statistics settings apply from version 1.0.19)

TouchPause pauses touchscreen input locally. It has no advertising, account
registration or developer-operated server. Version 1.0.18 introduces optional
usage statistics through Google Analytics for Firebase. Older versions have no
developer analytics. Version 1.0.18 requires an explicit opt-in everywhere.
Version 1.0.19 uses regional choices. Statistics are optional, and an existing
choice to keep them off is never changed by an update.

## Data collection and network access

TouchPause never sells data or sends touchscreen, stylus, hardware-key or screen
content to anyone. Optional statistics are described separately below.

The optional lifetime unlock uses Google Play Billing. The Billing Library
declares `INTERNET` and `ACCESS_NETWORK_STATE` and may exchange billing requests
and diagnostic information with Google under Google's terms. Google Play
returns localized product details and purchase status. TouchPause handles a
purchase token in memory long enough to grant and acknowledge access, but does
not store it or send it to the developer. Touch or key events are never part of
billing traffic.

## Optional usage statistics

Before collection starts on a new installation, the app explains the data and
purpose and lets you select your current country or region. The checkbox is
initially on for the United States, Australia, New Zealand, Singapore and Hong
Kong. You can uncheck it or choose **Keep off** before continuing. Elsewhere, or
without a specified region, it starts off and you must actively check it to allow
collection. Selecting a country alone, opening the policy, dismissing the notice
or leaving the app never authorizes collection. Statistics are unavailable for
declared mainland China and Russia pending cross-border/localization assessment.

Your choice has no effect on free uses, purchases or touch control. Change it
under **Settings → Privacy → Usage statistics**. Update **Your current country
or region** there when moving or traveling; a new consent-first region clears
the preselected checkbox. The declared region stays on device, not in our events.
We do not look up your location, read your SIM, infer jurisdiction from language,
or send your IP to a geolocation service. Google independently derives approximate
region as part of SDK measurement when statistics are enabled.

When enabled, TouchPause sends Google Firebase events describing setup readiness,
successful pauses, the end of the initial free allowance, attempts after the
daily limit, purchase-offer views, and the opening/outcome of a Play purchase
flow. Parameters describe the access stage, offer source and billing response
code. They never contain touch positions, key values, screen content, the name
of another app, purchase tokens, names, email addresses or a developer account ID.

The Google Analytics SDK also processes an app-instance identifier, app and
device information (such as app version, OS and model), approximate region
derived from masked IP addresses, app lifecycle information, and Google Play
purchase events. This is pseudonymous measurement, not completely anonymous
data. The developer can access reports and pseudonymous installation event
timelines through Google Analytics to understand setup and purchase drop-off,
not to identify people or personalize advertising.
An app-instance identifier represents an installation, not a verified person.

Advertising-ID collection, advertising storage, advertising user-data consent
and personalized advertising are disabled. TouchPause does not link Analytics
to advertising accounts or enable Google signals. Optional account data-sharing
settings are disabled. Statistics travel to Google over encrypted connections;
no analytics event is sent to a developer-operated server. Google acts as a
processor under accepted [data processing terms](https://business.safety.google/adsprocessorterms/).
It and its subprocessors may process data abroad, including in the United States;
its terms describe security, subprocessors and applicable transfer safeguards.
We remain responsible for the purpose and your choice. In Singapore, notice-based
collection relies on the PDPA legitimate interests exception for limited product
improvement, with a documented balancing assessment and immediate free opt-out.
Silence is not treated as consent. The business-improvement exception is not used
to justify collecting previously uncollected data.

Turning statistics off stops future collection and clears Analytics data stored
by the SDK on this device. It does not automatically erase previously collected
server reports. User and event data retention is set to two months and is not
extended by new activity; aggregate reports may be retained longer. Changes to
Google's retention settings can take 24 hours to apply. Contact us below about data questions
or deletion requests. Google processes this data under its
[privacy policy](https://policies.google.com/privacy) and
[Analytics disclosures](https://support.google.com/analytics/answer/11582702).

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
- short-lived advisory state indicating that a pause is active;
- statistics choice, declared country, notice version, choice time and local
  milestone/day deduplication flags;
- Google Analytics SDK data while statistics are enabled.

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
