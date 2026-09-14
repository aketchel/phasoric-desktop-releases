# Phasoric Desktop

**Keep Obsidian. Add Phasoric intelligence to the same vault.**

Phasoric Desktop opens an existing Markdown folder directly. Keep your files, folders, and Obsidian workflows while adding source-linked reviews, project context, decision memory, Watches, and approval-first agent workflows.

This repository distributes Windows preview installers, release notes, and authenticated update metadata. The application source and hosted services are maintained separately.

## Download and install

- [Download Windows preview 1.0.0-preview.1 (x64)](https://github.com/aketchel/phasoric-desktop-releases/releases/download/v1.0.0-preview.1/Phasoric-1.0.0-preview.1-win-x64.exe)
- [Read the release notes](https://github.com/aketchel/phasoric-desktop-releases/releases/tag/v1.0.0-preview.1)
- [Browse all releases](https://github.com/aketchel/phasoric-desktop-releases/releases)

1. Download the Windows x64 installer from the release page above.
2. Run the installer and choose the installation location. It installs for your Windows account.
3. Open Phasoric Desktop and choose your existing Obsidian vault or another Markdown folder.
4. Select a project and a few relevant notes to try a local review. Inspect its sources, save a private context, and choose whether to create a Watch.

Preview releases are intended for early adopters. Keep a backup of important notes, especially when trying agent edits or using multiple applications with the same folder. macOS, Linux, and Windows ARM64 downloads are not provided by this preview.

## Your vault stays yours

- Markdown files remain in the folder you choose. Opening a vault does not import or migrate it.
- Phasoric preserves `.obsidian` settings and plugin data. Obsidian plugins continue to run in Obsidian; Phasoric does not execute them.
- Filesystem watching detects external changes. Conflicting saves surface a recoverable draft instead of overwriting another application's edit.
- Local indexes and caches stay on your device. Opening a folder does not enable cloud sync or upload the vault to an AI provider.
- Connected models and sync require separate configuration. Git, Dropbox, and Drive can manage the underlying folder through their own filesystem tools.

Web, mobile, and desktop use the same core Phasoric workspace. Desktop adds the native filesystem, SQLite, operating-system integration, and local services.

## What you can try

- **Project, meeting, and research reviews:** choose local notes, inspect observations with source citations, and save reusable context.
- **Decision memory:** connect evidence, rationale, alternatives, and review history.
- **Watches:** track changes in selected contexts. Local checks require Phasoric to be running and the device to be awake.
- **Local MCP and agents:** explicitly enable access to the active vault; review supported file-change proposals in Forge before they execute.
- **Native workflows:** attachments, vault links, optional tray operation, and approval notifications.

## Automatic updates

The Windows preview checks for updates in the background and downloads an eligible update automatically. Use **Phasoric → Check for updates** to check immediately. When an update is ready, choose **Restart to update**.

Save your work, resolve any pending drafts, and use **Open another folder** to return to the desktop folder picker before restarting. If Phasoric cannot safely close the workspace, it leaves the application open so you can resolve the pending work. An update never silently restarts an active session.

Update metadata is authenticated using a Phasoric release key embedded in the application. The downloaded installer is checked against that metadata before installation. Update checks do not send vault content. GitHub receives ordinary download requests and their associated network metadata.

Preview updates can be released gradually or paused. All previously published versions remain available in [Releases](https://github.com/aketchel/phasoric-desktop-releases/releases). See [Recovery](RECOVERY.md) if an update causes a problem.

## Verify a download

Each release includes `SHA256SUMS.txt`. In PowerShell, calculate the downloaded installer's checksum:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\Phasoric-1.0.0-preview.1-win-x64.exe'
```

Compare the result with the matching entry in `SHA256SUMS.txt` from the same release. A checksum detects changed or incomplete downloads; obtain both files from this repository.

## Help and feedback

Open an issue in this repository or contact **support@phasoric.com**. Include the app version, Windows version, what you expected, and steps to reproduce. Use sample notes where possible. Do not attach private vaults, credentials, access tokens, or unredacted logs.

- [Phasoric](https://phasoric.com)
- [Desktop features](https://phasoric.com/apps/desktop)
- [Mobile features](https://phasoric.com/apps/mobile)

Phasoric is proprietary software. Public availability of these downloads does not grant rights to redistribute or modify the application beyond its applicable terms.
