# Pencil Hi-Res Export

Patches [Pencil](https://pencil.dev) to export frames as full-resolution PNGs.

## Features

- **Full-resolution exports** — Screenshots render at native resolution (up to 2000px) instead of Pencil's default 512px cap
- **Export menu item** — Adds **File → Export Selected as PNG…** (`Cmd+Shift+E`) for single or multi-frame export

## Requirements

- macOS
- [Pencil](https://pencil.dev) installed in `/Applications/`
- Node.js

## Usage

### Quick Start

Double-click **Patch Pencil.app**. A patched `Pencil.app` appears in the same folder. Open it.

Or from the terminal:

```bash
./patch.sh
open ./Pencil.app
```

### Exporting Frames

1. Select one or more frames on the canvas
2. **File → Export Selected as PNG…** (or `Cmd+Shift+E`)
3. Single frame → save dialog / Multiple frames → folder picker

### Re-patching After Updates

When Pencil updates, just run the patcher again. It always patches from the latest installed version.

## Troubleshooting

| Issue | Fix |
|-------|-----|
| Patched app won't open | Run: `codesign --force --deep --sign - ./Pencil.app && xattr -rd com.apple.quarantine ./Pencil.app` |
| "Launch failed" error | Quit the original Pencil first — both copies share user data |
| Pencil updated, exports are 512px again | Re-run the patcher |

## Disclaimer

This is an **unofficial, third-party** tool. It is **not affiliated with, endorsed by, or sponsored by** High Agency, Inc. or [Pencil](https://pencil.dev).

Pencil is a product of High Agency, Inc. — all rights to Pencil belong to them. This patch modifies local application files, which may conflict with Pencil's [Terms of Use](https://www.pencil.dev/terms-of-use). Use at your own discretion.
