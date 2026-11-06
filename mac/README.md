# Knowledge Universe for macOS

Version 1.0.0 · first build · macOS 11 or newer · Apple Silicon and Intel (universal)

## Files

| File | What it is |
| --- | --- |
| `KnowledgeUniverse_1.0.0_universal.dmg` | Disk image with the app. One file for Apple Silicon (M1 and newer) and Intel Macs. |
| `SHA256SUMS.txt` | Checksum to verify the download. |
| `THIRD-PARTY-LICENSES.txt` | Licenses of the components and fonts used. |

## Install

1. Download `KnowledgeUniverse_1.0.0_universal.dmg` (click the file, then the download button).
2. Open the disk image and drag **Knowledge Universe** into the **Applications** folder.
3. Eject the disk image.
4. Start the app the first time as described in the next section.
5. Choose **Select folder…** and pick a folder with Markdown notes, or try **Open demo knowledge base**.

## First start: macOS shows a warning

The app is not notarized by Apple, because that requires a paid developer account. It is signed with an ad-hoc signature, so the code is unchanged, but macOS Gatekeeper does not know the developer and blocks the normal double-click start the first time. This happens only once.

**Option 1: right-click, Open**

1. In **Applications**, right-click (or Control-click) **Knowledge Universe**.
2. Choose **Open**.
3. Click **Open** in the dialog.

**Option 2: Privacy & Security** (on macOS 15 Sequoia and newer this is often the only way in the interface)

1. Try to open the app once by double-click. macOS refuses.
2. Open **System Settings → Privacy & Security** and scroll down.
3. Next to the message about "Knowledge Universe", click **Open Anyway** and confirm with your password or Touch ID.

**Option 3: Terminal** (if the options above do not work, or macOS says the app is "damaged")

```bash
xattr -dr com.apple.quarantine /Applications/Knowledge\ Universe.app
```

This only removes the "downloaded from the internet" mark. Afterwards the app starts normally.

The warning refers to the missing notarization, not to a problem found in the file. If you want to be sure the file is unchanged, compare its checksum (next section).

## Verify the download (optional)

In Terminal, in the folder with the download:

```bash
shasum -a 256 KnowledgeUniverse_1.0.0_universal.dmg
```

The value must match the one in `SHA256SUMS.txt`.

## Keyboard shortcuts

On the Mac the shortcuts use the Command key instead of Control.

| Action | Shortcut |
| --- | --- |
| Search | `Cmd+K` |
| New note | `Cmd+N` |
| Quick capture into the inbox note | `Cmd+Shift+N` |
| Today's note | `Option+T` |
| Options | `Cmd+,` |
| Save (in the editor) | `Cmd+S` |

## Uninstall

Quit the app and drag **Knowledge Universe** from **Applications** to the Trash. Your notes are never touched. To remove the settings as well, delete these two folders:

- `~/Library/Application Support/de.berkbytes.knowledge-universe`
- `~/Library/WebKit/de.berkbytes.knowledge-universe`

## Privacy

The app works fully offline, collects nothing and sends nothing. Your notes stay in your folder. Settings are stored on your device only.

## License

[MIT License](../LICENSE). See `THIRD-PARTY-LICENSES.txt` for third-party components.
