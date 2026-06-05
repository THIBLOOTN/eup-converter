<div align="center">

# EUP Converter

### Turn GTA 5 EUP & clothing mods into ready-to-use FiveM resources — in seconds.

![Version](https://img.shields.io/badge/version-1.0.8-ffb000)
![Platform](https://img.shields.io/badge/platform-Windows-0d1014)
![FiveM](https://img.shields.io/badge/FiveM-ESX%20%7C%20QB%20%7C%20standalone-39d98a)
![Updates](https://img.shields.io/badge/updates-automatic-39d98a)
![License](https://img.shields.io/badge/license-activation%20required-ff5d5d)

*Drop your extracted clothing folder in. Click one button. Get a server-ready resource out.*

</div>

---

## What is EUP Converter?

Bringing GTA 5 uniform and clothing mods into FiveM is a slow, error-prone job: every
`.ydd` and `.ytd` file has to be renamed by hand to the exact FiveM stream format,
sorted, and wrapped in a working resource. One typo and the uniform simply won't load.

**EUP Converter does that entire renaming and packaging step for you** — in its own
clean desktop app. No command line, no manual typing, no guesswork. Drop in the files
you extracted from a mod, and it hands you back a finished, correctly named FiveM
resource you can drop straight into your server.

> **Note:** EUP Converter is a renaming & packaging tool, **not** a 3D model converter.
> You extract the clothing files from the mod once with OpenIV/CodeWalker, then EUP
> Converter handles the rest. See [How it works](#how-it-works).

---

## Features

- **One-click conversion** — drop a folder, click convert, download your resource.
- **Native desktop app** — its own window, dark UI, no browser tab, no console.
- **Works fully offline** — your files never leave your PC.
- **Smart auto-detection** — recognizes male/female peds and props automatically.
- **Pre-scan check** — see how many files were found and which names look off, *before*
  you convert.
- **Collision protection** — duplicate file names are flagged, never silently overwritten.
- **Clear results** — every file shows up as *converted*, *skipped*, or *collision*,
  with the full list. No "nothing happened" mystery.
- **Built-in self-check** — the app verifies its own conversion logic on every launch.
- **License activation** — your personal code unlocks the app; tied to your purchase.
- **Update access at a glance** — a live counter shows exactly how long your access to
  updates lasts (or *Lifetime access*).
- **Automatic updates** — new versions install themselves; you never re-download by hand.
- **Ready-to-run output** — a complete `Converted_Eup` resource with a valid
  `fxmanifest.lua`, ready for `ensure`.

---

## Screenshots

<img width="926" height="833" alt="image" src="https://github.com/user-attachments/assets/6ab2c0c1-5152-4c39-a2e5-b40cdfb237f5" />


| Main window | Conversion results | Activation |
|-------------|--------------------|------------|
| `screenshot-main.png` | `screenshot-results.png` | `screenshot-activation.png` |

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

## How to get it

EUP Converter is a paid tool. After purchase you receive:
1. The installer (`EUP Converter Setup.exe`).
2. Your personal **license code**.

Run the installer, open the app, paste your code on the activation screen once — done.
Your access (and the update counter) is tied to that code.


> Purchase & support: **(https://discord.gg/5VKZQ49y)**

---

## Using the app

1. Open **EUP Converter** and activate it with your code (first launch only).
2. Drag your extracted clothing folder onto the drop area. Use folder names with
   `mp_m` / `mp_f` (or "female") so gender is detected.
3. Click **Convert & build resource**.
4. Click **Download Converted_Eup.zip** and save it.
5. Add it to your server:
   ```cfg
   # server.cfg
   ensure Converted_Eup
   ```
   Restart and apply the uniform in-game through your clothing/EUP/job menu.

---

## Requirements

- **Windows** 10 or 11
- **OpenIV** or **CodeWalker** (free) to extract the mod files
- A FiveM server (ESX, QBCore, or standalone — the output is plain streamed clothing)

---

## Updates

EUP Converter keeps itself up to date. When a new version is released, your app detects
it on launch, downloads it in the background, and applies it after a quick restart — no
manual installs. The counter in the top-right shows how long your access to updates lasts.

---

## FAQ

**Does it convert 3D models?**
No. It renames and packages files you've already extracted. The extraction is a one-time
step with OpenIV/CodeWalker for any clothing mod.

**Will it work with any EUP pack?**
It targets the standard freemode clothing naming. Packs with unusual names are listed
under *skipped*, so you always know exactly what happened.

**What happens when my update access ends?**
The app keeps working — you simply stop receiving new updates until you renew.

**Does it touch the internet?**
Only to check for app updates. The conversion itself is 100% local.

**Which frameworks are supported?**
The output is standard streamed clothing, so it works with ESX, QBCore, and standalone.

---

## Important notes

- EUP Converter does **not** grant any rights to the clothing assets you process. All
  mod assets remain the property of their original creators and are subject to **their**
  license terms. Only convert mods you're allowed to use.
- Provided **as is**, without warranty. Always keep a backup of your source files.

---

## License

Proprietary. **Resale and redistribution are strictly forbidden.** Licensed to the
original purchaser only; it may not be shared, re-uploaded, or resold.

---

<div align="center">

**Made by THIBLOOTN**

[Get access](#how-to-get-it) · [Discord](#) · [Report an issue](../../issues)

</div>
