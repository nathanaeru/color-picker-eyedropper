# Color Picker / Eyedropper Tool for Windows 11

A lightweight, system-wide color picker overlay mod for [Windhawk](https://windhawk.net/), inspired by [Microsoft PowerToys](https://github.com/microsoft/powertoys) Color Picker. It allows you to select any pixel on your screen via a customizable global hotkey, view a magnified pixel grid loupe, and automatically obtain the color value in **HEX**, **RGB**, **HSL**, and **CMYK** formats with one-click clipboard copying.

![Color Picker mod in action](https://raw.githubusercontent.com/nathanaeru/color-picker-eyedropper/refs/heads/main/demo.gif)

## Features

- **System-Wide Screen Freeze & Overlay**: Freezes the screen upon activation to prevent accidental click-throughs onto underlying windows.
- **Magnified Loupe Cursor**: Displays a magnified preview grid with a centered crosshair and a live color preview badge that follows your cursor.
- **Multi-Format Support**: Automatically converts and displays captured colors in:
  - **HEX** (e.g., `#FF5733` or `ff5733`)
  - **RGB** (e.g., `rgb(255, 87, 51)`)
  - **HSL** (e.g., `hsl(11, 100%, 60%)`)
  - **CMYK** (e.g., `cmyk(0%, 66%, 80%, 0%)`)
- **Native Windows 11 Dark Mode Support**: The result pop-up window automatically adapts to your system theme (Light or Dark mode).
- **Modern UI Styling**: Clean, dialog-style UI using Segoe UI font, smooth rounded corners, drop-shadow effects, and single-click copy buttons.
- **Customizable Mod Settings**: Directly configure hotkeys and color formatting preferences within the Windhawk UI.


## Hotkey & Controls

- **Activate Eyedropper**: Default hotkey is `Win + Alt + C` (customizable in Windhawk settings).
- **Pick Color**: **Left-Click** anywhere on the screen to capture the pixel color and open the copy window.
- **Cancel Eyedropper**: Press **Escape** or **Right-Click** to exit picking mode without selecting a color.


## Configuration Settings

You can customize the mod settings directly from the Windhawk Mod Manager UI:

| Setting | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| **Hotkey Key** | String | `C` | Single alphanumeric or symbol character used with `Win + Alt`. |
| **Include '#' Prefix in HEX** | Boolean | `true` | Choose whether HEX values include the `#` symbol (`#CDCDCD` vs `CDCDCD`). |
| **Uppercase HEX Characters** | Boolean | `true` | Toggle uppercase vs. lowercase HEX characters (`#ABCDEF` vs `#abcdef`). |

## Dependencies & Technical Details

- **Target Process**: `windhawk.exe` (runs as a Windhawk tool mod)
- **Libraries Linked**: `-lgdi32`, `-lmsimg32`, `-ldwmapi`, `-luxtheme`, `-lshcore`
- **Architecture**: Pure Win32 GDI & User32 APIs (no heavy external GUI dependencies).