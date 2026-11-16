# Publishing to the Chrome Web Store

## Build the package

1. Bump `version` in `package.json`. The store rejects a version it already has.
2. Run `pnpm nx build extension-animevsub-helper` and then `pnpm exec wxt zip` from this folder.
3. Upload `dist/extension-animevsub-helper-<version>-chrome.zip` in the developer dashboard.

The `release-extension.yml` workflow builds the same zip on a `v*` tag and attaches it to the public mirror release, so you can download it from there instead.

## Permission justifications

Paste these into the "Privacy practices" tab.

| Permission                | Justification                                                                                                                                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `cookies`                 | Reads and writes cookies for the site a request targets, so the HTTP API can send a request with that site's session, the way a browser would.                                                       |
| `declarativeNetRequest`   | Sets the `Referer` and `Origin` headers for allowlisted anime sites, and removes `X-Frame-Options` and `Content-Security-Policy` from `animevietsub.*` sub-frames so the embed bridge can load them. |
| `storage`                 | Keeps the user's referrer map in `storage.sync`.                                                                                                                                                     |
| Host permission `*://*/*` | The API is a CORS-free HTTP client for the Animefork web app, and the target sites are not known in advance.                                                                                         |

## Single purpose

Lets the Animefork web app make cross-origin requests to anime streaming sites that block browser CORS.

## Review risks

- `*://*/*` plus an `<all_urls>` content script triggers an in-depth review. Expect a longer wait on the first submission.
- The extension collects no user data. State that in the data-usage form.
- Link a privacy policy URL. The store requires one for any extension with host permissions.
