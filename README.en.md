# Yunatype

Activate the fonts you need, only when you need them (dynamic activation). Yunatype is a free font manager for Windows and macOS that lets you manage tens of thousands of fonts without installing them in your OS.

Your system stays light, and the font menus in Photoshop and Illustrator stay tidy. Search, compare, and drop a font straight onto the canvas of your design app. Less stress choosing fonts, and faster trial and error in your design work.

**Supported**: Windows 10 / 11 (64-bit), macOS 11 (Big Sur) or later (Apple Silicon and Intel)

**日本語**: [README.md](README.md)

---

## 🚀 Getting started

1. Download the installer from [Releases](https://github.com/yunatype/yunatype/releases/latest) (`Yunatype_<version>_x64-setup.exe` for Windows, the `.dmg` for macOS) and install it.
2. Start Yunatype and add the folders that hold your fonts (local, NAS, external drives) in **Preferences > Font Folders**. When the import finishes, the fonts appear in the list.
3. Find a font and press **Enter** to activate it. You can also drag and drop it onto a document in your design app.

If you see a warning while installing, see [Installation details](#-installation-details).

---

## ✨ Features

- **Dynamic activation, no installation**: Loads the fonts you need system-wide, only while Yunatype is running. When you quit, or after a crash, the activated fonts are cleaned up automatically.
- **Fast library**: Family view, per-weight lists and fast search. Scroll through tens of thousands of fonts without stutter, even while holding down a key.
- **NAS / LAN folders**: Scans folders in parallel and shows progress (count and the font being imported). You can cancel. Removing a folder in Preferences also removes its fonts from the library (the font files themselves are not deleted).
- **QuickLook (Space) and glyph map**: Large specimens, all weights of a family, detailed metadata and the full character set. Previews show each font exactly as it renders.
- **Compare fonts**: Select several fonts in the list and press Space (up to 4) to see them side by side. The sample text, size and tab apply to all of them at once.
- **Diagnose**: Finds out why an activated font does not show up in Photoshop and other apps (file state, recognition by Windows, duplicate fonts with the same name).
- **Design app integration**: Detects the fonts used in your Photoshop, Illustrator, Figma and Affinity documents and activates them automatically. When you close a document, only its fonts are deactivated.
- **Drop onto your design app to place text**: Drag and drop the selected fonts onto a document in your design app, and the sample text shown in the list is placed in that font. Drop several at once to stack them vertically (up to 10).
- **Search**: By name, PostScript name, English name, foundry, designer, tag and more. A foundry or style picked from the suggestions narrows the results to that field only.
- **Google Fonts in the same list** (optional, off by default): Turn it on in Preferences and the Google Fonts catalog appears in the same list as your own fonts. You can preview a font before downloading it, and only that family is downloaded when you activate it (Enter). If you already have the same font, yours takes priority.
- **Language filter**: Narrow fonts down by Japanese, Simplified Chinese, Korean, Latin, Cyrillic, Greek and more (multiple selections allowed).
- **14 languages and 5 themes**: 日本語 / English / 简体中文 / 繁體中文 / 한국어 / Deutsch / Français / Español / Italiano / Português / Nederlands / Dansk / Polski / Русский. The installer, the Adobe extension, the Figma plugin and the tray menu are localized as well. Sample texts are available for each language.

---

## ⌨️ Basic usage

Yunatype works well with the mouse, and also supports a fast, keyboard-driven workflow.

| What you want to do | How |
|---|---|
| 🔎 Find a font | Type a font name, PostScript name, foundry and so on in the search box at the top (`/` or Ctrl+F to jump there). Press Enter or pick a suggestion |
| 👀 See a large specimen (QuickLook) | Select a font and press **Space**. ↑↓ for the previous / next font, ←→ to switch weights |
| ✨ Activate a font | Press **Enter** in the list (press again to deactivate) |
| ⚖️ Compare fonts | Select several and press **Space** (up to 4). Or add them with **M** and open the comparison with **Shift+M** |
| 🎨 Place text in a design app | Drag and drop the selected fonts onto a document in Photoshop or another app |

Press **?** to see all keyboard shortcuts.

---

## 🎨 Design app integration

| App | First-time setup | Activates fonts when a document opens | Place text by dropping |
|---|---|---|---|
| Photoshop (Windows) | None (the installer adds the extension) | ✓ | ✓ |
| Photoshop (macOS) | Allow Automation (once) | ✓ | ✓ |
| Illustrator (Windows) | None (the installer adds the extension) | ✓ | ✓ |
| Illustrator (macOS) | Install the extension (once) | ✓ | ✓ |
| Figma Desktop | Register the plugin (once) | ✓ (while the plugin is open) | ✓ (while the plugin is open) |
| Affinity (3.2 or later) | Enable the MCP server (once) | ✓ | ✓ |

### Drop onto your design app to place text
Drag and drop the fonts selected in the list onto a document in one of the apps above. The sample text shown in the list is placed at the drop point, in that font. Fonts that are not active yet are activated automatically. The mouse pointer shows a busy cursor until the font is applied. Undo (Ctrl+Z / ⌘+Z) removes the placed text.

### Photoshop / Illustrator
When you open a document, Yunatype detects the fonts it uses and activates them automatically (when you close the document, only those fonts are deactivated).

- Photoshop and Illustrator on Windows: the installer adds the extension automatically.
- Photoshop on macOS: no extension needed. The first time, allow Yunatype to control Adobe Photoshop in **System Settings > Privacy & Security > Automation**.
- Illustrator on macOS: once, click "Reinstall / Update Extension" in Yunatype's **Preferences > Integrations** to install the extension.
- Apps with the extension work in the background without opening the panel. To check the connection, open **Window > Extensions > Yunatype** in the app.

### Figma
Use the Figma Desktop plugin "Yunatype". **Only once**, set it up as follows.

1. In Yunatype, open **Preferences > Integrations** and click **"Open plugin folder"** under "Figma Desktop Plugin Integration" (the folder opens with `manifest.json` selected).
2. In Figma Desktop, choose **Plugins > Development > Import plugin from manifest...** and select the `manifest.json` from step 1 (you can also paste its path with "Copy manifest.json path").
3. Click "Copy" next to **"External API Token"** in Preferences, paste it into the token field of the Figma plugin, and save.

How to use:
- After opening a document, run the plugin (**Plugins > Development > Yunatype**; from the second time, Ctrl+Alt+P / ⌘+Option+P). There are no buttons. Of the fonts used in the document, the ones Yunatype has are activated automatically. They are deactivated when you close the plugin.
- While the plugin is open, you can drop the selected fonts onto the document to place text.

### Affinity
Affinity (3.2 or later) needs no plugin.

1. Enable the **MCP server** in Affinity's settings.
2. Restart Affinity.

The fonts in the documents you open in Affinity are now activated automatically (and deactivated when you close them). You can check the status in Yunatype's **Preferences > Integrations**.

---

## 📥 Installation details

### Windows
1. Download the latest `Yunatype_<version>_x64-setup.exe` from [Releases](https://github.com/yunatype/yunatype/releases/latest).
2. Run the downloaded file. Choose a language, read the license agreement, and accept it to start the installation.

### macOS
1. Download the latest `.dmg` from [Releases](https://github.com/yunatype/yunatype/releases/latest) (it runs on both Apple Silicon and Intel).
2. In the window that opens, drag `Yunatype` to `Applications`.

### "Windows protected your PC"
Yunatype is not code-signed (signing requires a paid certificate), so Windows SmartScreen may show a warning the first time you run it.

1. Click **"More info"** in the warning.
2. Click **"Run anyway"**.

If your browser says the file "isn't commonly downloaded", choose "Keep" to continue.

### "Developer cannot be verified" (macOS)
Yunatype is not signed or notarized by Apple, so macOS may show a warning the first time you open it.

1. Click **"Done"** (or "OK") to close the warning.
2. Open **System Settings > Privacy & Security** and click **"Open Anyway"** next to Yunatype near the bottom.
3. Click **"Open"** in the confirmation that follows.

### Uninstall
- Windows: remove Yunatype in "Settings > Apps".
- macOS: move Yunatype in `Applications` to the Trash.

In both cases, your font files are not deleted.

---

## 🛟 Troubleshooting

- **An activated font does not show up in Photoshop or another app**: Use **"Diagnose"** at the bottom of the **"Details"** tab in QuickLook (Space). It checks whether Windows recognizes the font, whether there are duplicate fonts with the same name, and so on. If Windows recognizes it but the app still does not show it, restarting Photoshop may help.
- **The list is empty after importing fonts**: The list appears automatically when the import finishes. If it does not, quit Yunatype (you can also quit from the tray icon) and start it again.
- **Fonts on a NAS cannot be read**: Check the network connection and that the folder is accessible.
- **A yellow warning in Figma does not go away**: Press Ctrl+R (reload) once in the Figma file tab.
- **The Figma plugin says "App not running"**: Start Yunatype (it switches to connected in about 2 seconds).
- **Only one of two fonts with the same name works on Windows**: Windows shows only one font with the same family name, weight and italic setting. Yunatype tells you when you drop such a font onto a design app. Activate only the one you want to use.

---

## 🔒 Privacy

Yunatype does not collect or send your name, email address, the names of your fonts or the locations of your files. Settings and data are stored only on your computer (`%LOCALAPPDATA%\Yunatype` on Windows, `~/Library/Application Support/Yunatype` on macOS). Communication with the Adobe extension, the Figma plugin and Affinity stays on your computer.

Yunatype connects to the internet only in the following cases.

- **Usage statistics** (to learn which features are used): Once a day, Yunatype sends only the following: how often features are used (search, QuickLook, comparison), the number of errors and crashes, the number of fonts and whether you have Japanese / Simplified Chinese fonts (in rough ranges), the Yunatype version, OS, display language, country (from the OS region setting), a random ID for this device, the date of first use, and how often families in the public Google Fonts catalog are used. It does not send the names of your fonts, file locations or anything that identifies you. Your IP address reaches the server during the connection (the server does not store it).
  - In regions that require consent first, such as the EU, the UK, Switzerland, Korea and Brazil (and when the region is unknown), **nothing is sent until you agree**. In other regions, sending starts the day after the notice card is shown.
  - You can turn it off at any time in **Preferences > Privacy**. You can also review what is sent, reset the device ID and delete the data on the server there.
- **When Google Fonts is on** (off by default): Yunatype connects to Google (`fonts.google.com`), GitHub (`google/fonts`), `fonts.googleapis.com` and `raw.githubusercontent.com` to fetch the catalog and to preview and download fonts. Requests are limited in interval and concurrency. Your font information is not sent (the characters used for previews are). When it is off, Yunatype does not connect.
- **Update check**: At startup, Yunatype asks GitHub for the latest version (your IP address reaches GitHub). You can turn this off with **"Check for updates at startup"** under **Preferences > General > Software Updates**.

---

## 📄 License

- **Free** to use, for individuals and companies, for personal and commercial work alike (including installation on company computers).
- For details, read [LICENSE](LICENSE) (the license agreement; the Japanese text is authoritative and the English text is a reference translation). The licenses of the third-party software used in Yunatype are available in **Preferences > General > License** in the app.

## 💬 Bug reports and contact

Please use [Issues](https://github.com/yunatype/yunatype/issues) on this GitHub repository. For bug reports, include your Yunatype version, OS (Windows / macOS) version and the steps to reproduce.

---

Adobe, Photoshop and Illustrator are trademarks or registered trademarks of Adobe Inc.; Figma of Figma, Inc.; Windows of Microsoft Corporation; and macOS of Apple Inc. Affinity and other product names are trademarks or registered trademarks of their respective owners. Yunatype is not affiliated with or endorsed by these companies.

Copyright (c) 2026 yunatype. All rights reserved.
