# STM32 OLED Designer 128×64

A desktop application for designing graphical user interfaces for 128×64 monochrome OLED displays on STM32 microcontrollers. Design your screens visually on a canvas that matches your physical display, then export clean C code for STM32CubeIDE.

![STM32 OLED Designer](screenshots/oled_designer_preview.png)

## Overview

STM32 OLED Designer lets you lay out widgets visually on a true 128×64 pixel canvas, then export clean C source and header files that drop straight into your STM32CubeIDE project — no hand-coding pixel coordinates or repetitive draw calls.

Built specifically for STM32 + STM32CubeIDE. Not a general-purpose tool for other platforms.

## Supported Controllers

- SSD1306 (default, most widely available)
- SSD1309
- SH1106 (column offset applied automatically)

All I²C and SPI variants supported. Controller is selected at compile time — not a designer setting.

## Widget Types

- **Text Labels** — Dynamic Text / Label Value (no-flicker live readouts)
- **Progress Bar** — horizontal or vertical
- **Bar / Bar Meter** — horizontal or vertical
- **Plot / Mini Scrolling Graph**
- **Rectangle / Frame / Circle / Ellipse**
- **Horizontal Line / Vertical Line**
- **Import Image** (bitmap, converted to C array)

## Key Capability — Flicker-Free Updates

The driver uses an in-RAM frame buffer. Dynamic Text and Bar Meter widgets erase and redraw only their own value region — not the whole screen. This means live sensor data updates look stable and clean with no visible flash.

## View Options (designer overlays — don't affect generated code)

- **Widget Bounds** — yellow outline showing each widget's footprint
- **Update Areas** — cyan outline showing exactly which regions are erased on live update
- **Grid / Column Guides** — alignment aids

## Runs On

- **Windows** — Setup installer (.exe)
- **macOS** — Disk image (.dmg), including Apple Silicon

## Lite vs PRO

### LITE (Free)
- ✅ All widget types
- ✅ All layout tools (AutoFit, Smart Fit, Find Off-Screen, Center Text in Rect)
- ✅ Edit menu: copy, paste, duplicate, delete
- ✅ Image import & C code export
- ✅ Full Properties panel
- ⚠️ 1 project screen (plus optional logo/splash screen)

### PRO ($35 — one-time, no subscription)
Everything in Lite, plus:
- ✅ Unlimited project screens

## Download

### Lite — Free
Download the latest release from the [Releases page](../../releases/latest).

Includes:
- Windows installer (.exe)
- macOS disk image (.dmg)
- Full user manual (PDF, 22 pages)

### PRO Version
Available on [Gumroad](https://carlosbarberis49.gumroad.com/l/cxsil) — one-time purchase, no subscription.

## Activating PRO

After purchase, email **carlos@bartek.com** with your registered email address. You will receive a license key by return email. Enter it via **License → Enter License Key** in the application.

## Getting Started

1. Download and run the installer for your platform
2. Launch STM32 OLED Designer
3. Set your OLED controller type in project settings
4. Drag and drop widgets onto the 128×64 canvas
5. Configure widget properties in the Properties panel
6. Export C source and header files
7. Add the generated files to your STM32CubeIDE project

## Generated Code

The exporter produces:
- A `.c` source file with all widget definitions and draw calls
- A `.h` header file for integration into your project
- Compatible with STM32 HAL and your existing display driver

## About

Developed by **Carlos Barberis** — [Bartek Technologies](https://bartek.com)

- 🔗 [LinkedIn](https://www.linkedin.com/in/bartektechnologies/)
- 🛒 [Gumroad Store](https://carlosbarberis49.gumroad.com)
- 📦 [STM32 TFT Designer](https://github.com/carlosabarberis/STM32-TFT-Designer) — companion tool for color TFT displays

## License

The Lite version is free for personal and commercial use.
The PRO version requires a valid license key.