# Spotifast

- [Dark palette](Helium%20Mustard%20Dark.json)
- [Light palette](Helium%20Mustard%20Light.json)

1. Open **Settings → Appearance → Open themes folder**.
2. Copy both JSON files into that folder.
3. If Spotifast is already running, run `spotifast reload-themes`, or quit and reopen the app.
4. Choose a palette under **Settings → Appearance → Theme**.

For automatic switching, choose **Follow system**, then assign **Helium Mustard Light** to **Light mode theme** and **Helium Mustard Dark** to **Dark mode theme**.

Turn off **Colour from album art** if you want pages to keep the fixed theme colors.

Spotifast uses one palette per file, with `base` set to `dark` or `light` and literal hex colors in `colors`. Both files specify all 16 documented color roles. Dark uses `#FFDB58`; light uses `#856300` because Spotifast shares its accent between buttons and other highlights.

The format, supported color names, and selected text/background contrasts have been checked. The palettes have not been applied to a running Spotifast instance as part of this repository setup.

[Official custom theme documentation](https://spotifast.rocks/settings-and-files/#custom-themes)
