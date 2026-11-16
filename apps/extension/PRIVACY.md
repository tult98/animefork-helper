# Privacy policy for Animefork Helper

Last updated: 16 November 2026.

Animefork Helper is a browser extension that lets the Animefork web app (https://animefork.com) make requests to anime streaming sites that block normal browser requests.

## What we collect

Nothing. The extension has no server of its own, no analytics, no advertising and no crash reporting. The developer receives no data from it.

## What the extension handles on your device

- **Requests Animefork asks for.** When the Animefork web app asks for a page or a video file, the extension fetches that URL and hands the answer back to the web app. The request goes straight from your browser to the site you asked for.
- **Cookies of those sites.** To make a request look like it came from a normal visit, the extension reads and writes cookies for the site being requested. They are used for that request only and are not copied anywhere else.
- **Request headers.** The extension sets the `Referer` and `Origin` headers that the target sites expect, and removes the headers that stop `animevietsub` pages from loading in a frame.
- **Referrer settings.** The extension saves a list of which `Referer` to send to which site in `chrome.storage.sync`. Your browser may sync it between your own devices through your Google account. It holds no personal data.

The extension runs a small script on every page you open. It adds a helper that other pages can call, and it does not read or change what you do on the page.

## Sharing

We do not sell, share or transfer any data, because we do not have any.

The sites you ask Animefork to load receive the requests you make, as they would if you visited them yourself. Their own privacy policies apply to those requests.

## Permissions

| Permission                      | Why                                                                        |
| ------------------------------- | -------------------------------------------------------------------------- |
| `cookies`                       | Send a request with the session of the site being requested.               |
| `declarativeNetRequest`         | Set `Referer` and `Origin`, and allow `animevietsub` pages to be embedded. |
| `storage`                       | Keep the referrer settings.                                                |
| Access to all sites (`*://*/*`) | The sites Animefork needs are not known in advance and change over time.   |

## Changes

If this policy changes, the new version replaces this file in the extension's source repository.

## Contact

Open an issue at https://github.com/tult98/animefork-helper/issues.
