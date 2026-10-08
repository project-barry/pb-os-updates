# pb-os-updates: update packages for pb-os devices

> [!IMPORTANT]
> **This repository was set up with a coding agent:
> [Claude Code](https://www.anthropic.com/claude-code), running Anthropic's
> Claude Opus 5.5 (`claude-opus-5-5`).** Claude wrote this README and builds
> the packages published here; people set the goals, made the decisions and
> did the hands-on testing. See the
> [note from lavachemist](https://github.com/project-barry/pb-os#a-note-from-lavachemist-written-by-a-human)
> in pb-os. Review before you rely on it.

**New to pb-os? You are in the wrong place.** To install pb-os, download an
image from [project-barry/pb-os releases](https://github.com/project-barry/pb-os/releases)
and follow its notes. Nothing here can be flashed.

This repository only holds the update packages that devices already running
pb-os download for themselves. Keeping them here keeps the pb-os release page
to what people flash.

## How devices use it

Open Quick Access → Decky → **PB-OS Utils** → **Update**. It checks the
releases here, offers the newest one your device can install and downloads
it. Then press **Restart and install**. Your games, saves, login and settings
stay.

Each release holds:

- A **full update** (`.update.tar.gz.001`, `.002`, …) for devices on an older
  version, or a small **patch** (`….from-<version>.delta.tar.gz.001`) for
  devices on the release it names.
- `SHA256SUMS`, and `SHA256SUMS.sig`, its signature with the pb-os release
  key. Devices check that signature before they install anything; the
  accepted key is
  [`allowed_signers`](https://github.com/project-barry/pb-os/blob/main/external-and-mods/konkr-update/allowed_signers)
  in pb-os.
- `release_notes.md`, what the update changes.

## Installing without internet

Download the package parts for your device, `SHA256SUMS` and
`SHA256SUMS.sig` from a release here. Copy them to the top folder of a
microSD card or USB drive, or to the Downloads folder in Desktop Mode, then
install them from PB-OS Utils → Update.

## Problems

Please report them in [pb-os issues](https://github.com/project-barry/pb-os/issues),
with your device and the version you were updating from. To talk with other
users, join the [Project Barry Discord](https://discord.gg/euPurKCWc4).
