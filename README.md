# RMK Configuration for Cornix Keyboard

This repository contains an unofficial [RMK](https://rmk.rs/) configuration for
the Cornix keyboard by Jezail Funder. It aims to help users to customize their
own RMK firmware for Cornix, not to replicate the official firmware.

# Features

- It supports all keys and rotary encoders.
- It supports Vial.
- Its Vial layout is compatible with the official firmware, which means you can
  load your existing Vial layout (`.vil` file). Macros, combos, tap dances, and some other
  things may lost, though.

# Notes

- LED lighting is not supported.
- Battery level reporting seems not working properly.
- Optimization on BLE or power consumption is not made.

# Usage

1. Make any changes you want for the firmware.
2. Build the firmware. Execute
   ```sh
   cargo build --release
   ```
   in the repository root. This will generate two `.uf2` files in the repository
   root. Make sure you have the Rust toolchain.
3. Flash the two `.uf2` files to the left and right halves of the keyboard
   respectively. You may need to delete Bluetooth pairing on your computer first
   and re-pair after flashing.
