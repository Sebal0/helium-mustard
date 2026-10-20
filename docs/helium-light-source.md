# Helium light palette: source mapping

The light mode is now based on Helium’s published neutral palette rather than the earlier custom cream/green-gray interpretation. This is an adaptation to two applications, not a pixel-for-pixel browser theme.

## Source snapshot

Reviewed on October 20, 2026:

- Helium revision: [`3423b1671a75826afc934558f20a30f8dc85f81d`](https://github.com/imputnet/helium/tree/3423b1671a75826afc934558f20a30f8dc85f81d).
- [Chromium version used by that revision](https://github.com/imputnet/helium/blob/3423b1671a75826afc934558f20a30f8dc85f81d/chromium_version.txt): `155.0.8059.84`.
- [Default theme patch](https://github.com/imputnet/helium/blob/3423b1671a75826afc934558f20a30f8dc85f81d/patches/helium/ui/default-theme.patch): enables the grayscale theme by default.
- [Color scheme patch](https://github.com/imputnet/helium/blob/3423b1671a75826afc934558f20a30f8dc85f81d/patches/helium/ui/helium-color-scheme.patch): supplies the neutral reference values and changes grayscale header/divider tokens.
- [Color mixer patch](https://github.com/imputnet/helium/blob/3423b1671a75826afc934558f20a30f8dc85f81d/patches/helium/ui/helium-color-mixers.patch): sets the light toolbar/frame to the system base and the grayscale omnibox/surface variant to Neutral92.
- Inherited Chromium sources: [ref_color_mixer.cc](https://github.com/chromium/chromium/blob/155.0.8059.84/ui/color/ref_color_mixer.cc) and [sys_color_mixer.cc](https://github.com/chromium/chromium/blob/155.0.8059.84/ui/color/sys_color_mixer.cc).

The two Helium patches were applied to the relevant Chromium reference/system mixer files in a temporary source directory to verify the resulting definitions. The alternative new-neutral branch is gated on dark mode; light mode uses the patched baseline `else` branch. In grayscale mode, light primary/on-surface text resolves to Neutral10. The light system base and surface resolve to Neutral100.

## Adaptation

| Helium token | Value | Use in this collection |
| --- | --- | --- |
| Neutral100 | `#FFFFFF` | T3 toolbar/chrome and raised surfaces |
| Neutral99 | `#FDFCFC` | Overlay surfaces |
| Neutral98 | `#FAF9F9` | Reading canvas and Spotifast window |
| Neutral96 | `#F4F3F3` | T3 muted/code surfaces |
| Neutral95 | `#F1F0F0` | Messages, sidebar, Spotifast panels |
| Neutral92 | `#E8E8E8` | Controls, subtle separators and hover surfaces |
| Neutral90 | `#E3E2E2` | Pressed/selected rows and hovered controls |
| Neutral50 | `#767777` | T3 input boundary |
| Neutral40 | `#5D5E5F` | Secondary text, placeholder text and muted icons |
| Neutral20 | `#2F3131` | Code text |
| Neutral10 | `#1A1C1C` | Primary text |

Choosing Neutral98 for the reading canvas and Neutral95 for panels/messages is an application-specific mapping. Helium’s native toolbar base is white, and its tabs and location bar also use alpha blending. Native window materials and platform settings can change the final browser appearance; these theme files use opaque colors for predictable results.

The T3 informational blue (`#3551D2`, with `#F0EFFF` / `#00218D` surfaces/text) and error red (`#BA1A1A`, with `#FFDAD6` / `#410002`) also come from Helium’s reference palette. Mustard accents, their hover shades, and amber warnings remain custom choices. Dark gold `#856300` is retained for readable accents on light backgrounds; T3 message action buttons retain `#FFDB58`.

## Validation

- T3: the existing dark `colors` object is unchanged; the complete 57-role light variant remains in the same file.
- Spotifast: its dark JSON is byte-for-byte unchanged; its light JSON contains the 16 supported/documented roles in hex format.
- 15 selected T3 text/background pairs and 20 Spotifast pairs exceed 4.5:1. The lowest measured pair in both groups is approximately 5.03:1. Primary text on the reading canvas is approximately 16.29:1.
- These figures describe opaque palette pairs. They do not establish full application accessibility, visual-fatigue benefits, or a verified live import.
