# Support and troubleshooting

For a bug or feature request, use [GitHub Issues](https://github.com/UglyEgg/Plainwright/issues).
For licensing or a private report, contact Rich Majewski at
[pwdev@entropy.quest](mailto:pwdev@entropy.quest).

## A useful bug report

Include the Plainwright version, package format, distribution/version, desktop
and whether the session uses Wayland or X11. Describe the steps, what happened
and what you expected. If a small example document helps, remove all private
content first. Do not attach recovery files, credentials or an unreviewed log dump.

## Before troubleshooting

- Check that the package supports your distribution and architecture.
- Verify the downloaded file against the same release's `SHA256SUMS`.
- Check which installation you launched if native and Flatpak versions coexist.
- Save your work before restarting an application or changing installations.

Do not delete your settings or recovery data as a first troubleshooting step.
Do not disable Chromium/Bubblewrap sandboxing, run as root, or grant broad
filesystem permissions just to make a rich-content preview work.

This repository is the public distribution and issue-reporting home. It does
not expose the private application source or accept source patches against it.
