# Install Plainwright

Choose an asset from the [latest release](https://github.com/UglyEgg/Plainwright/releases/latest)
that matches your operating system and architecture. The commands below assume
you have changed into the folder containing the downloaded file. Replace each
example filename with the exact asset name from that release.

## Verify the download

Download `SHA256SUMS` from the same release. To verify one downloaded package:

```sh
sha256sum plainwright-package-filename
```

Compare its complete hash with the entry for that exact filename in `SHA256SUMS`.
Checksums detect corruption or mismatched files; they are not a separate digital
signature or proof of publisher identity.

## Fedora 44 — RPM

```sh
sudo dnf install ./plainwright-VERSION-1.fc44.x86_64.rpm
```

## Ubuntu 26.04 — DEB

```sh
sudo apt install ./plainwright_VERSION-1ubuntu26.04.1_amd64.deb
```

This package targets Ubuntu 26.04. It is not qualified for older Ubuntu releases,
Linux Mint or Debian simply because they also use `.deb` files.

Use **1.0.1 or later**. The original 1.0.0 DEB could make Plainwright's rendering
assets unreadable to an ordinary user. Upgrading from 1.0.0 to 1.0.1 repairs only
affected, root-owned directories owned solely by Plainwright. It does not change
shared system-directory permissions. Do not apply broad `chmod` commands to
system folders as a workaround.

## Flatpak

Install Flatpak using your distribution's instructions. The standalone bundle
requires the KDE Platform 6.11 runtime; make it available through your configured
Flatpak remote before installing the bundle.

```sh
flatpak install --user ./plainwright-VERSION.flatpak
flatpak run quest.entropy.plainwright
```

Plainwright is distributed here as a bundle, not through a Flathub app listing.
If you also have the native package installed, both may appear in your launcher.

## AppImage — releases that include it

Check the release's supported distribution/glibc baseline first. Download the
AppImage, mark it executable and run it without administrator privileges:

```sh
chmod +x Plainwright-VERSION-x86_64.AppImage
./Plainwright-VERSION-x86_64.AppImage
```

If your system cannot mount AppImages through FUSE, consult the release's
extract-and-run instructions. For 1.0.1:

```sh
APPIMAGE_EXTRACT_AND_RUN=1 ./Plainwright-1.0.1-x86_64.AppImage
```

The 1.0.1 AppImage was built on Ubuntu 26.04 with glibc 2.43. Portability does not
mean it is qualified on older distributions. Do not disable the rendering sandbox or run the
application as root to work around a startup problem.

## Open Markdown files

After installing a native package, select Plainwright in your desktop's
“Open With” menu for a Markdown file. You can make it the default using your
desktop's file-association settings. Installing a portable AppImage does not
automatically register it as the default application.
