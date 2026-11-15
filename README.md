# Animefork Helper

The browser extension that lets [animefork.com](https://animefork.com) load videos from the source in your browser.

This repository is a read-only mirror. Each release is published here as one snapshot of the extension's source, built and attached by the release workflow.

## Install

Download `animefork-helper-chrome.zip` or `animefork-helper-firefox.zip` from the [latest release](../../releases/latest). Chrome, Brave and Opera install it unpacked. See [apps/extension/install-on-chrome.md](apps/extension/install-on-chrome.md).

## Build it yourself

```sh
pnpm install
pnpm build   # apps/extension/dist/chrome-mv3 and firefox-mv3
pnpm test
```

The extension's own README is at [apps/extension/README.md](apps/extension/README.md).

## License

MIT. See [apps/extension/LICENSE](apps/extension/LICENSE).
