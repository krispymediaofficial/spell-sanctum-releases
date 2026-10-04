# Spell Sanctum downloads

Spell Sanctum is a free table for playing Magic: The Gathering Commander online with
friends. One person hosts it on their Mac or PC, and everyone else joins from a browser.
There are no accounts, no sign-up and no tracking.

This repository only holds the downloads. The website is **https://spellsanctum.com**.

## Download

Go to the [**Releases**](https://github.com/krispymediaofficial/spell-sanctum-releases/releases/latest) page and pick the file for the host's computer:

| Computer | File |
| --- | --- |
| Mac (Apple silicon or Intel, macOS 13.5 or later) | `Spell-Sanctum-<version>-Mac.zip` |
| Windows 10 or 11 (64-bit) | `Spell-Sanctum-<version>-Windows.exe` |

Only the host installs Spell Sanctum. Players never download anything: they open the
host's link in Chrome, Edge, Firefox or Safari, type a name and knock.

## Starting a game

1. **Mac:** double-click the zip, then double-click **Spell Sanctum** inside the folder it makes.
   **Windows:** double-click the `.exe`.
2. A small window opens and your browser opens on your table, with its link already copied.
3. Send the link to your pod. When a friend knocks, click **Let in**.

Leave the small window open while you play. Closing it ends the game for everyone.

## "Unknown app" warnings

The beta is not code-signed yet, so Mac and Windows may stop and ask the first time each new
version opens. This is expected. It happens once per version.

**On a Mac**, if it says "Spell Sanctum" Not Opened:

1. Click **Done**.
2. Open **System Settings**, then **Privacy & Security**.
3. Scroll down to **Security** and click **Open Anyway** next to the note about Spell Sanctum.
4. Type your Mac's password, then click **Open Anyway** once more.

**On Windows**, if a blue box says "Windows protected your PC":

1. Click **More info**.
2. Click **Run anyway**.

If your browser says the file isn't commonly downloaded, choose **Keep** (in Edge: the `...`
menu, then **Keep**, then **Show more** and **Keep anyway**). If the Windows firewall asks,
tick **Private networks** and click **Allow access** so phones on your Wi-Fi can reach the table.

## Check your download (optional)

Each release lists a SHA-256 checksum for every file. To compare yours:

- **Mac:** `shasum -a 256 ~/Downloads/Spell-Sanctum-<version>-Mac.zip`
- **Windows (PowerShell):** `Get-FileHash $HOME\Downloads\Spell-Sanctum-<version>-Windows.exe`

The result should match the release page exactly.

## Your files

Saved tables, decks and settings are kept outside the app, so a new version carries on where
the old one stopped:

- **Mac:** `~/Library/Application Support/Spell Sanctum`
- **Windows:** `%LOCALAPPDATA%\Spell Sanctum`

At start-up the app asks `spellsanctum.com/version.json` whether a newer version exists. That
is a plain request that carries nothing about you, and it never downloads or replaces anything
by itself.

## Questions, bugs and ideas

Find the community and send feedback through the links on **https://spellsanctum.com**.

---

Spell Sanctum is unofficial Fan Content permitted under the Fan Content Policy. Not
approved/endorsed by Wizards. Portions of the materials used are property of Wizards of the
Coast. ©Wizards of the Coast LLC. Card images and card data come from
[Scryfall](https://scryfall.com). Spell Sanctum is not produced by or endorsed by Scryfall.
Free fan-made software. Includes Node.js (MIT) and cloudflared (Apache-2.0).
