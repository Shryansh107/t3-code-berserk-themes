# Berserk themes for T3 Code

Two original theme exports from T3 Code, packaged on 2026-11-16:

| Theme ID | File | Description |
| --- | --- | --- |
| `berserk-eclipse` | `themes/berserk-eclipse.json` | Dark charcoal, crimson accents, warm text. |
| `berserk-eclipse-illustrated` | `themes/berserk-eclipse-illustrated.json` | Eclipse palette with custom CSS and embedded artwork. |

The illustrated theme is self-contained: its artwork is embedded in the JSON's CSS. Keep the complete JSON intact.

## Reapply in another T3 Code instance

1. Download `berserk-t3-code-themes.zip` from this repository's Releases and extract it on the machine running the other instance.
2. Open a T3 Code thread with access to the extracted folder.
3. Give its agent this instruction:

   > Read README.md and both JSON files in the extracted themes folder. Call t3_theme_read to inspect this instance's theme guide. Publish themes/berserk-eclipse.json as themeId berserk-eclipse using t3_theme_set with the full parsed JSON as theme. Then publish themes/berserk-eclipse-illustrated.json as themeId berserk-eclipse-illustrated the same way, and leave the illustrated theme active in dark mode. Preserve all colors and CSS exactly.

Each publish call activates that theme. Both remain available after publishing; use `t3_theme_set` with just the desired `themeId` to switch between them. To finish with the plain version instead, ask the agent to activate `berserk-eclipse` last.

## Manual file restore

For an instance using T3 Code's standard data location, close it, copy the two JSON files into `~/.t3/userdata/themes/` (Windows: `%USERPROFILE%\.t3\userdata\themes\`), then reopen T3 Code and select the theme in its appearance settings. Back up files with the same names before replacing them. Instances using a custom data directory need that directory's `themes` folder instead. The agent method above avoids having to locate the data directory.

Themes apply to T3 Code web and desktop clients; mobile does not use these themes. Custom CSS selectors may need adjustments after future T3 Code updates.

## Contents and integrity

`SHA256SUMS.txt` records the exact SHA-256 hashes of the original theme JSON files. The archive includes only those themes, this README, and the checksum list.
