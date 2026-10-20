# Helium Mustard

Helium-inspired themes with a mustard yellow accent (`#FFDB58`). Dark and light palettes for T3 Code, Spotifast, and future additions. Created with AI assistance and refined through personal use and feedback.

I like yellow. This collection pairs it with deep graphite backgrounds, softened text, and a matching warm light palette.

## Themes

| App | Files | Modes |
| --- | --- | --- |
| [T3 Code](themes/t3-code/) | [helium-mustard.json](themes/t3-code/helium-mustard.json) | One theme with dark and light variants |
| [Spotifast](themes/spotifast/) | [Dark](themes/spotifast/Helium%20Mustard%20Dark.json) · [Light](themes/spotifast/Helium%20Mustard%20Light.json) | Two palettes, assignable to system appearance |

## Palette

| Role | Dark | Light |
| --- | --- | --- |
| Main background | `#121414` | `#F4F3EE` |
| Main text | `#D8DAD7` | `#292D2E` |
| Accent | `#FFDB58` | `#856300` |

The light palette uses darker mustard for small accents so they remain visible against pale surfaces. T3 Code also uses `#FFDB58` for message action buttons; Spotifast has one shared accent color for buttons and other highlights.

Contrast calculations informed the palette, but they do not establish that a theme reduces eye strain. Comfort depends on the screen, lighting, text size, and the reader. Application transparency and rendering can also affect the final result.

## Installation

Download this repository with **Code → Download ZIP**, or clone it:

```sh
git clone https://github.com/Sebal0/helium-mustard.git
```

Follow the app-specific instructions:

- [T3 Code installation](themes/t3-code/README.md)
- [Spotifast installation](themes/spotifast/README.md)

## Inspiration and AI assistance

The neutral palette was inspired by [Helium](https://github.com/imputnet/helium). A supplied **Dracula PyCharm** theme by **YanivZalach** was the initial T3 Code JSON reference.

AI helped research color roles, propose variants, convert between formats, and calculate contrast. The direction, yellow accent, and successive refinements came from my preferences and feedback.

See [inspirations and credits](docs/inspirations.md) for details. This is an independent theme collection, not an official theme from those projects.

## Adding another app

Add a folder under `themes/<app-name>/` with the native theme files and a short installation README. Keep the palette recognizable, document any app-specific differences, and add the app to the table above.
