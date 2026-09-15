# Phasoric Desktop

**Keep Obsidian. Add Phasoric intelligence to the same vault.**

Phasoric Desktop opens an existing Markdown folder directly. Keep your files, folders, and Obsidian workflows while adding source-linked reviews, project context, decision memory, Watches, and approval-first agent workflows.

This repository distributes Windows preview installers, release notes, and authenticated update metadata. The application source and hosted services are maintained separately.

## Download and install

- [Download Windows preview 1.0.0-preview.3 (x64)](https://github.com/aketchel/phasoric-desktop-releases/releases/download/v1.0.0-preview.3/Phasoric-1.0.0-preview.3-win-x64.exe)
- [Read the release notes](https://github.com/aketchel/phasoric-desktop-releases/releases/tag/v1.0.0-preview.3)
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
- Large vaults index in background workers while the workspace stays usable. Progress appears above the workspace. A file that cannot be read is listed as skipped; its original bytes and any earlier indexed copy are kept.
- Connected models and sync require separate configuration. Git, Dropbox, and Drive can manage the underlying folder through their own filesystem tools.

Web, mobile, and desktop use the same core Phasoric workspace. Desktop adds the native filesystem, SQLite, operating-system integration, and local services.

## What you can try

- **Project, meeting, and research reviews:** choose local notes, inspect observations with source citations, and save reusable context.
- **Decision memory:** connect evidence, rationale, alternatives, and review history.
- **Watches:** track changes in selected contexts. Local checks require Phasoric to be running and the device to be awake.
- **Local MCP and agents:** explicitly enable access to the active vault; review supported file-change proposals in Forge before they execute.
- **Native workflows:** attachments, vault links, optional tray operation, and approval notifications.
- **Quick capture:** right-click the Phasoric taskbar icon or tray icon and choose **New quick note**. Use **Ctrl+Alt+N** from another application, or **Ctrl+Shift+N** inside Phasoric. The global shortcut can be disabled in the tray menu.
- **Sticky notes:** create a sticky from the tray or File menu, or use **Open as sticky note** in a vault note's actions. Keep it above other windows, edit it, and open its source in Phasoric. Saved stickies remain ordinary Markdown notes; conflicting edits are kept for review.
- **Portable properties:** assign a type, tags, project, status, priority, due date, owner, and area in a sticky's **Properties** panel. These properties stay in Markdown and travel with the note through any configured sync provider. Use the **Sticky notes** Pulse lens or Perspective to review notes marked `type: sticky-note`.
- **Capture from other apps:** copy text, then choose **Capture clipboard** from Phasoric's File or tray menu, or **Paste clipboard** in a quick note. Chrome clipper 2.0.1 adds **Copy for Desktop** with source and capture properties; paste it into Phasoric and choose its vault. Clipboard access happens only when you request it.
- **Quick vault switching:** use the vault switcher or **Ctrl+Alt+V**, type a vault name, and press Enter when one match remains. Pending saves finish before switching.
- **Fullscreen controls:** move the mouse to the top edge to reveal **Menu** and **Exit fullscreen**. **F11** toggles fullscreen; **Escape** exits it.

## Connect your local vault

Open **Settings → Vaults → Vault sync** or choose **Connect or manage vault sync…** in the vault switcher. Choose **Phasoric Hosted**, **Dropbox**, **Google Drive**, or **GitHub**. Existing connections use the same account and provider setup as the web application. You can create a Phasoric Hosted destination or open the shared connection settings to configure another provider.

Review the upload/download preview, then confirm to enable bidirectional Markdown sync. To bring a connected vault to your computer, choose the local working-copy option and select an empty folder. Local and connected copies remain available; pausing or disconnecting does not delete either copy. Sync checks run about once a minute while Phasoric is running and the device is awake. Enable tray operation for background use.

This preview requires the updated Phasoric sync service. Until it is available for your account, the app explains that a server update is needed and you can continue working locally. Attachments, Obsidian configuration, encrypted notes, and deletion propagation are excluded. Notes changed on both sides require conflict review. Files larger than 4 MB and unsupported paths are shown as excluded; oversized provider inventories stop before transfer. Provider connections and their credentials remain managed by Phasoric's server.

## Automatic updates

The Windows preview checks for updates in the background and downloads an eligible update automatically. Use **Phasoric → Check for updates** to check immediately. When an update is ready, choose **Restart to update**.

Save your work, resolve any pending drafts, and use **Open another folder** to return to the desktop folder picker before restarting. If Phasoric cannot safely close the workspace, it leaves the application open so you can resolve the pending work. An update never silently restarts an active session.

Update metadata is authenticated using a Phasoric release key embedded in the application. The downloaded installer is checked against that metadata before installation. Update checks do not send vault content. GitHub receives ordinary download requests and their associated network metadata.

Preview updates can be released gradually or paused. The [download page](https://phasoric.com/apps/desktop) selects the current published installer from this repository. Withdrawn releases are removed from public downloads; already installed copies can still receive the replacement through the update channel. See [Recovery](RECOVERY.md) if an update causes a problem.

## Verify a download

Each release includes `SHA256SUMS.txt`. In PowerShell, calculate the downloaded installer's checksum:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\Phasoric-1.0.0-preview.3-win-x64.exe'
```

Compare the result with the matching entry in `SHA256SUMS.txt` from the same release. A checksum detects changed or incomplete downloads; obtain both files from this repository.

## Help and feedback

Open an issue in this repository or contact **support@phasoric.com**. Include the app version, Windows version, what you expected, and steps to reproduce. Use sample notes where possible. Do not attach private vaults, credentials, access tokens, or unredacted logs.

- [Phasoric](https://phasoric.com)
- [Desktop features](https://phasoric.com/apps/desktop)
- [Mobile features](https://phasoric.com/apps/mobile)

Phasoric is proprietary software. Public availability of these downloads does not grant rights to redistribute or modify the application beyond its applicable terms.
