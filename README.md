# RMK Configuration for Cornix Keyboard

This repository contains an unofficial [RMK](https://rmk.rs/) configuration for
the Cornix keyboard by Jezail Funder. It aims to help users to customize their
own RMK firmware for Cornix, not to replicate the official firmware.

# Features

- It supports all keys and rotary encoders.
- It supports Vial.
- Its Vial layout is roughlly compatible with the official firmware, so you can
  load your existing Vial layout (`.vil` file) without much modification.
  Macros, combos, tap dances, key maps for rotary encoders, and some other
  things may lost or be messed up, so you may need to reconfigure them.

# Notes

- LED lighting is not supported.
- Battery level reporting seems not working properly.
- Optimization on BLE or power consumption is not made.

# Usage

1. Make any changes you want for the firmware.

2. Build the firmware. Execute in the repository root:
   ```sh
   cargo build --release
   ```
   This will generate two `.uf2` files in the repository root. Make sure you
   have the Rust toolchain.

   Otherwise, fork this repository, go to GitHub Actions tab, tap *Build RMK
   firmware*, and download the artifacts when the build is done.

3. Flash the two `.uf2` files to the left and right halves of the keyboard
   respectively. You may need to delete Bluetooth pairing on your computer first
   and re-pair after flashing.
