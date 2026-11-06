# Knowledge Universe for Windows

Version 1.0.0 · first build · Windows 10 / 11, 64-bit

## Files

| File | What it is |
| --- | --- |
| `KnowledgeUniverse_1.0.0_x64-setup.exe` | Installer (recommended). Installs for the current user, no administrator rights needed. |
| `KnowledgeUniverse.exe` | Portable program. No installation: put it anywhere and start it. |
| `SHA256SUMS.txt` | Checksums to verify the downloads. |
| `THIRD-PARTY-LICENSES.txt` | Licenses of the components and fonts used. |

## Install

1. Download `KnowledgeUniverse_1.0.0_x64-setup.exe` (click the file, then the download button).
2. Start it and follow the steps.
3. Open Knowledge Universe, choose **Select folder…** and pick a folder with Markdown notes, or try **Open demo knowledge base**.

## Windows shows a security warning

The app is not signed with a paid code-signing certificate, so Windows SmartScreen may show "Windows protected your PC" on the first start.

1. Click **More info**.
2. Click **Run anyway**.

The warning refers to the missing signature, not to a problem found in the file. If you want to be sure the file is unchanged, compare its checksum (next section).

## Verify the download (optional)

In PowerShell, in the folder with the download:

```powershell
Get-FileHash .\KnowledgeUniverse_1.0.0_x64-setup.exe -Algorithm SHA256
```

The value must match the one in `SHA256SUMS.txt`.

## Uninstall

Settings → Apps → Installed apps → Knowledge Universe → Uninstall. Your notes are never touched. The portable version: just delete the file.

## Privacy

The app works fully offline, collects nothing and sends nothing. Your notes stay in your folder. Settings are stored on your device only.

## License

[MIT License](../LICENSE). See `THIRD-PARTY-LICENSES.txt` for third-party components.
