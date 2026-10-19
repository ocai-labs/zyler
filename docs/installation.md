# Install Zyler

Download from the official [Releases page](https://github.com/ocai-labs/zyler/releases/latest).
Open the release's **Assets** list if the files are collapsed.

## macOS

1. Download the `arm64.dmg` file for Apple Silicon.
2. Open the disk image and copy Zyler into **Applications**.
3. Launch Zyler from Applications, then eject the disk image.

The macOS app is signed and notarized. Current published macOS builds target
Apple Silicon; an Intel or universal build is not available in the current release.
If macOS reports a damaged or unverified download, download it again from the official
release and contact support if the problem persists.

## Windows

1. Download `Zyler-Setup-<version>.exe` for x64 Windows.
2. Run the installer and follow its prompts.
3. Open Zyler from the Start menu or its installed shortcut.

Windows installers are currently unsigned, so Windows may show a SmartScreen warning.
Check that the file came from the official release before deciding whether to run it.
On a managed computer, follow your organization's software-installation policy.

## Linux

Download `Zyler-<version>.AppImage` for x64 Linux. Make it executable using your file
manager's permissions, then open it. In a terminal, using the downloaded filename:

```sh
chmod +x ./Zyler-<version>.AppImage
./Zyler-<version>.AppImage
```

Replace `<version>` with the actual version. If your distribution reports missing
AppImage or FUSE support, consult its AppImage instructions or include the exact
message in a [support request](../SUPPORT.md).

## Updates

Check your installed version and update controls in **Settings → General**.
You can also install a newer published release manually. Close the app and
[back up your vault](local-vaults.md#back-up-a-vault) before changing versions.

An older app may not open a vault or note written in a newer format. Update Zyler
rather than changing the format version in a file.

Continue with [getting started](getting-started.md).
