# Homebrew Tap for DevEco Code Desktop

<a href="https://github.com/SherlockGougou/homebrew-tap/actions/workflows/ci.yml"><img src="https://github.com/SherlockGougou/homebrew-tap/actions/workflows/ci.yml/badge.svg" alt="CI"></a>

Homebrew casks for [DevEco Code Desktop](https://github.com/SherlockGougou/devecocode-desktop),
a macOS desktop client for the DevEco Code CLI.

## Install

The Standard build requires a separately installed and signed-in
`@deveco/deveco-code` CLI:

```bash
brew trust sherlockgougou/tap
brew install --cask sherlockgougou/tap/devecocode-desktop
```

The Offline build bundles a pinned CLI:

```bash
brew trust sherlockgougou/tap
brew install --cask sherlockgougou/tap/devecocode-desktop-offline
```

Homebrew 7+ requires trusting a third-party tap before loading its casks. This only trusts
this tap; it does not disable macOS signature or quarantine checks.

Both casks select the correct DMG for Apple Silicon or Intel and verify the SHA-256 from
the corresponding GitHub Release. The tap is updated automatically after each release.

## Update

```bash
brew upgrade --cask devecocode-desktop
brew upgrade --cask devecocode-desktop-offline
```

## Uninstall

```bash
brew uninstall --cask devecocode-desktop
brew uninstall --cask devecocode-desktop-offline
```

Add `--zap` to remove the desktop configuration, logs, WebKit data, caches, and
preferences. The Standard and Offline builds share
`~/Library/Application Support/DevEco Code Desktop`, so zapping either one removes that
shared configuration.

## Unsigned Builds

The current release is ad-hoc signed and not notarized by Apple. macOS may block the first
launch. Right-click the app in Applications and choose **Open**, or allow it under
**System Settings → Privacy & Security**. Do not disable Gatekeeper globally.

## Links

- [Main repository](https://github.com/SherlockGougou/devecocode-desktop)
- [Installation guide](https://github.com/SherlockGougou/devecocode-desktop/blob/main/docs/installation.md)
- [Releases](https://github.com/SherlockGougou/devecocode-desktop/releases)
- [Project website](https://sherlockgougou.github.io/devecocode-desktop/)
