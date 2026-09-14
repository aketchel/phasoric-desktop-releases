# Recovering from a desktop update

## If the application still opens

1. Save your notes and close the editor.
2. Open **Phasoric → Check for updates**. A recovery release may already be available.
3. If offered, choose **Restart to update** after reviewing the release notes.

The usual recovery is a newer release containing the last known-good behavior. This allows affected installations to recover through the normal authenticated update channel.

## If the application cannot open

1. Keep your vault folder intact. Make a backup before troubleshooting.
2. Download the recovery installer identified in the newest [release notes](https://github.com/aketchel/phasoric-desktop-releases/releases).
3. Close Phasoric, including its tray process, and run that installer.
4. Reopen your vault and verify that your notes are present.

The installer updates application files; it does not intentionally delete vaults or reset your local application data. Reinstalling does not undo changes already made to Markdown files.

## Older installers

Previous installers are retained, but installing an older version is not an automatic database rollback. An older application may not understand data written by a newer version. Back up both your vault and Phasoric application data, and follow the compatibility guidance in the release notes before downgrading. Prefer a documented recovery release.

## An update is unavailable or fails to download

Continue using the installed application and try again when connected. A phased rollout may not yet include your installation, or a release may have been paused. Invalid update metadata or a damaged download is rejected; it does not replace the running application.

For help, contact **support@phasoric.com** or open a repository issue with the app version and a description of the problem. Do not include private notes, credentials, or tokens.
