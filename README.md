# EnterpriseCore AI Suite: free trial for companies

One Windows application for finance, payroll, HR, CRM, projects, inventory, documents, communication, marketing, construction and security. Your data stays on your own computers.

**[Download the latest version](https://github.com/abedinm/enterprisecore-trial/releases/latest)**

Each release has three files:

| File | What it is |
|---|---|
| `EnterpriseCore-AI-Suite-Setup-<version>-x64.exe` | The installer |
| `EnterpriseCore-Trial-Guide.pdf` | Installation, setup, what to try, how to send feedback |
| `SHA256SUMS.txt` | Checksums to confirm the download wasn't altered |

## Requirements

- Windows 10 or 11, 64-bit
- About 450 MB of free disk space, plus room for your data
- No administrator rights needed: it installs for the current Windows user
- No internet connection needed after download (AI features are optional)

## Install

1. Run the installer. It isn't code-signed yet, so Windows may show "Windows protected your PC": choose **More info → Run anyway**.
2. The first time it opens, a short setup creates your company, your own administrator account, and optional logins for each department head. There is no shared default password.
3. Colleagues can use it from their own PCs: on the host computer choose **Network → Share with other computers on this network**. They open the `https://` address shown under **Network → Show network address**. The connection is encrypted; each colleague installs the host's certificate once (the same dialog explains how) so the browser stops warning.
4. While sharing, closing the window keeps EnterpriseCore running in the notification area so colleagues stay connected; **File → Quit** stops it. Under **Network** you can also have it start when you sign in to Windows and keep the computer awake while sharing.

The Trial Guide PDF walks through all of this with screenshots.

## Check the download

In PowerShell, in the folder with the installer:

```powershell
Get-FileHash ".\EnterpriseCore-AI-Suite-Setup-<version>-x64.exe" -Algorithm SHA256
```

The hash must match the line for that file in `SHA256SUMS.txt`.

## Your data

- Everything is stored on the host computer in `%LOCALAPPDATA%\EnterpriseCore AI Suite` (**Help → Open data folder**).
- The software does not send your business data anywhere. Optional AI features send the text you submit to the AI provider you configure yourself.
- Daily backups go to the `storage\backups` folder inside the data folder. **Help → Restore a backup…** puts one back; the data it replaces is kept aside, not deleted.
- Installing a newer version over an older one keeps your data. **Help → Check for updates** tells you when a new version is published here, and from 0.6.0 on can download it, check it against `SHA256SUMS.txt` and install it for you.
- Your data is never locked in: **Export to Excel** on the main lists, and **Organization → Export data** (administrators) for everything, one Excel workbook per module.

## Feedback

Use the feedback button inside the app. At the end of the trial your administrator exports everything from **Organization → Trial feedback** and sends the file to the person who gave you the trial. Please don't post company information in this repository.

## License

© 2026 Minhazul Abedin (EnterpriseCore AI Suite). All rights reserved.

Evaluation use only. See [LICENSE.txt](LICENSE.txt), which is also shown during installation. This repository publishes the installer only; the source code is not public and is not licensed for copying, modification, redistribution or reverse engineering. The "Source code" archives GitHub adds to each release contain only this README and the license.
