# Privacy Policy — Header Override

_Last updated: 2026-04-25_

## Summary

Header Override is a developer tool that runs entirely in your browser. It does not collect, transmit, or share any personal data.

## Data handling

**What is stored**

The extension stores the following data **locally on your device** using the browser's `chrome.storage.local` API:

- Header override profiles you create (names, URL patterns, header rules, values)
- UI settings you configure (theme, master toggle state)
- A volatile log of recent rule matches (kept in `chrome.storage.session`, cleared when the browser restarts)

**What is NOT collected**

- No browsing history is sent anywhere.
- No analytics or telemetry.
- No user identifiers.
- No request bodies, response bodies, or cookies are transmitted.
- The extension does not phone home.

**Network activity initiated by the extension**

The extension only modifies HTTP request headers locally before they leave your browser, according to rules you define. The extension itself does not initiate any network traffic to its author or to any third party. The "Send" button in the Test URL sandbox issues a `fetch` to a URL **you type in**, exactly the same way as if you typed it in the address bar — no other destination is contacted.

**Third-party services**

None. The extension does not use external services, CDNs, analytics, error reporting, or any other third-party integration.

## Permissions justification

| Permission | Purpose |
|---|---|
| `declarativeNetRequest` (Chrome) / `webRequest`+`webRequestBlocking` (Firefox) | Modify HTTP request headers according to user-defined rules |
| `declarativeNetRequestFeedback` (Chrome) | Show matched rules in the optional Activity log inside the popup |
| `storage` | Persist user-defined profiles and settings locally |
| `tabs` | Read the current tab id when the user enables "lock to current tab" on a profile |
| `host_permissions: <all_urls>` | Allow rules to target any URL the user configures (no data is read from those URLs) |

## Your data, your control

- Profiles can be exported and imported as JSON via the **Import / Export** buttons.
- Uninstalling the extension removes all stored data.
- No sync to any cloud service is performed by the extension.

## Contact

For questions or issues open a ticket on the project repository, or contact the author directly.

## Changes

Substantial changes to this policy will be reflected by updating the date at the top of this file.
