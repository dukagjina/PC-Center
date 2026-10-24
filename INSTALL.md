# Install PC Center

## Requirements

- Windows 11 x64. Other Windows versions and ARM64 are not qualified by this release.
- Administrator permission to install the app and its Windows service.
- Microsoft Edge WebView2 Runtime. It is commonly present on Windows 11, but this installer checks for it and stops if it is missing.

## Download and install

1. Open the [official release page](https://github.com/dukagjina/PC-Center/releases/latest).
2. Under **Assets**, download **PC-Center-Setup.exe**. The ZIP and TAR source archives are not application installers.
3. If WebView2 is missing, use [Microsoft's WebView2 download page](https://developer.microsoft.com/en-us/microsoft-edge/webview2/#download-section). Choose the **Evergreen Standalone Installer — x64**, install it, then run PC Center setup again.
4. Run PC Center setup. It requests administrator permission because it installs a Windows service and Explorer menu entries.
5. Launch PC Center from its Desktop or Start menu shortcut.

Setup does not automatically restart Windows. If another PC Center operation is
using the service, finish or stop that operation and run setup again.

## Unsigned release

PC Center 0.14.9 does not have a trusted code-signing certificate. Windows may
show **Unknown publisher** or a SmartScreen reputation warning. Some security
policies will prevent installation. Publishing on GitHub does not add a digital
signature or Microsoft certification.

Keep Windows security protections enabled. If an organization manages your PC,
ask its administrator to review the app before installation.

## Check the download

The release includes **PC-Center-Setup.exe.sha256**. For version 0.14.9, the EXE's
SHA-256 is:

```text
49d33a2e7532ff63f716fac38125c4c43c5afaca1a0a17320bace3cb5cf71f78
```

To calculate your downloaded file's checksum, open PowerShell in its folder:

```powershell
Get-FileHash -LiteralPath .\PC-Center-Setup.exe -Algorithm SHA256
```

The result must match the value above, ignoring letter case. A checksum checks
that your download matches the published file; it is not a publisher certificate.

## Update or remove

To update an existing installation, finish active maintenance work, close PC
Center, and run the newer official installer. The application checks this
repository's release feed and only starts an offered installation after you choose it.

To uninstall, open **Windows Settings → Apps → Installed apps → PC Center → Uninstall**.
Uninstall removes the program, service and Explorer commands. Settings, backup
data and diagnostic or recovery records may remain so that uninstall does not
silently erase recovery information.

## Need help?

[Report an installation issue](https://github.com/dukagjina/PC-Center/issues/new/choose)
with the app version, Windows version and exact error message. Review logs and
screenshots before sharing; GitHub issues are public.
