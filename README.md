<div align="center">

# EUP Converter

### Turn GTA 5 EUP & clothing mods into ready-to-use FiveM resources — in seconds.

![Version](https://img.shields.io/badge/version-3.0.0-ffb000)
![Platform](https://img.shields.io/badge/platform-Windows-0d1014)
![Framework](https://img.shields.io/badge/FiveM-ESX%20%7C%20QB%20%7C%20standalone-39d98a)
![License](https://img.shields.io/badge/license-proprietary-ff5d5d)

*Drag your extracted clothing folder in. Click one button. Get a server-ready resource out.*

</div>

---

## What is EUP Converter?

Bringing GTA 5 uniform and clothing mods into FiveM is a tedious, error-prone job:
every `.ydd` and `.ytd` file has to be renamed by hand to the exact FiveM stream
format, sorted into the right folders, and wrapped in a working resource. One typo
and the uniform simply won't load in-game.

**EUP Converter does that entire renaming and packaging step for you** — in its own
clean desktop app. No command line, no manual typing, no guesswork. You drop in the
files you extracted from a mod, and it hands you back a finished, correctly named
FiveM resource you can drop straight into your server.

> **Important:** EUP Converter is a renaming & packaging tool, **not** a 3D model
> converter. You extract the clothing files from the mod once with OpenIV/CodeWalker,
> then EUP Converter handles the rest. See [How it works](#how-it-works).

---

## Features

- **One-click conversion** — drop a folder, click convert, download your resource.
- **Native desktop app** — its own window, dark UI, no browser tab, no console.
- **Works fully offline** — nothing is uploaded anywhere; everything runs on your PC.
- **Smart auto-detection** — recognizes male/female peds and props automatically.
- **Pre-scan check** — see exactly how many files were found and which names look off,
  *before* you convert.
- **Collision protection** — if two packs share a file name, it's flagged, never
  silently overwritten.
- **Clear results** — every file shows up as *converted*, *skipped*, or *collision*,
  with the full list. No more "nothing happened" mystery.
- **Built-in self-check** — the app verifies its own conversion logic on every launch.
- **Automatic updates** — new versions install themselves; you never re-download by hand.
- **Ready-to-run output** — a complete `Converted_Eup` resource with a valid
  `fxmanifest.lua`, ready for `ensure`.

---

## Screenshots

> *Add your own screenshots here — drag images into the GitHub editor.*

| Main window | Conversion results |
|-------------|--------------------|
| `screenshot-1.png` | `screenshot-2.png` |

---

## How it works

```
   GTA 5 mod          OpenIV / CodeWalker        EUP Converter           Your server
 ┌────────────┐      ┌──────────────────┐      ┌───────────────┐      ┌──────────────┐
 │  uniform   │  →   │  extract .ydd /  │  →   │  rename + pack │  →   │ ensure       │
 │   .rpf     │      │  .ytd files      │      │  → resource    │      │ Converted_Eup│
 └────────────┘      └──────────────────┘      └───────────────┘      └──────────────┘
```

1. **Extract** the clothing files from your mod once, using OpenIV or CodeWalker.
2. **Drop** the extracted folder into EUP Converter.
3. **Convert** — it renames everything to FiveM's `mp_x_freemode_01^...` format and
   builds the resource.
4. **Install** — unzip `Converted_Eup` into `resources/`, add `ensure Converted_Eup`.

---

## Getting started

### 1. Install
Run the installer (`EUP Converter Setup x.x.x.exe`). The app installs and opens its
own window. From now on it keeps itself up to date.

### 2. Prepare your files
Extract the clothing from your mod with **OpenIV** or **CodeWalker** into a folder.
Tip: put male and female clothing in separate folders named with `mp_m` / `mp_f`
(or "female") so the app can tell them apart.

### 3. Convert
- Drag the folder onto the drop area (or click to browse).
- Review the pre-scan, then click **Convert & build resource**.
- Click **Download Converted_Eup.zip** and save it.

### 4. Add to your server
```cfg
# server.cfg
ensure Converted_Eup
```
Drop the unzipped `Converted_Eup` folder into your `resources/`, restart, and apply
the uniform in-game through your clothing/EUP/job menu.

---

## Requirements

- **Windows** 10 or 11
- **OpenIV** or **CodeWalker** (free) to extract the mod files
- A FiveM server (ESX, QBCore, or standalone — the output is plain streamed clothing)

---

## Automatic updates

EUP Converter updates itself. When a new version is released, your app detects it on
launch, downloads it in the background, and applies it after a quick restart — no
manual re-installs, ever.

---

## FAQ

**Does it convert 3D models?**
No. It renames and packages files you've already extracted. The actual extraction is
done with OpenIV/CodeWalker — that's a one-time step for any clothing mod.

**Will it work with any EUP pack?**
It targets the standard freemode clothing naming. Packs with unusual names are flagged
in the *skipped* list so you always know exactly what happened.

**Does it touch the internet?**
Only to check for app updates. The conversion itself is 100% local — your files never
leave your PC.

**Which frameworks are supported?**
The output is standard streamed clothing, so it works with ESX, QBCore, and standalone
servers alike.

---

## Important notes

- EUP Converter does **not** grant any rights to the clothing assets you process.
  All mod assets remain the property of their original creators and are subject to
  **their** license terms. You are responsible for using only mods you're allowed to use.
- The tool is provided **as is**, without warranty. Always keep a backup of your
  source files.

---

## License

Proprietary. **Resale and redistribution are strictly forbidden.** This software is
licensed for use by the original purchaser only and may not be shared, re-uploaded,
or resold. See [`LICENSE.txt`](LICENSE.txt) for full terms.

---

## Support

> *Add your support channel here.*

- Discord: `[your invite link]`
- Purchase: `[your Tebex / store link]`

<div align="center">

**Made by [YOUR NAME / WV Roleplay]**

</div>
