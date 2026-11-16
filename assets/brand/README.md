# The Wasla mark

The Link: two loops, the phone and the PC, around a link node, upright on a
deep-sea tile with a lagoon glow. The loops are the connection itself —
Wasla means "link / connection".

| File | What it is |
|---|---|
| `icon.svg` | The full-color app icon: deep-sea tile, lagoon glow, aqua rim |
| `icon-flat.svg` | The same without the glow, for flat contexts |
| `icon-mono.svg` | The mark alone in white, for one-color uses (notifications, themed icons) |
| `icon-512.png` | `icon.svg` at 512 × 512 |

The apps draw the mark themselves from the same geometry:
`desktop/app/src/mark.rs` (the Windows icon, tray and notifications at every
size) and `android/app/src/main/res/drawable/ic_launcher_*.xml` and
`ic_notification.xml`.

Colors (Lagoon palette, `docs/design/tokens.json`): tile `#0B3D5C`, glow
`#0E7C7B`, phone loop `#F4FAF9`, PC loop `#7ED4CE`, link node `#0E7C7B`.

The Wasla name and mark are new for this fork. Wasla is based on NectarLink
(see the README); the NectarLink name and logo are covered by that project's
trademark policy and are not used here.
