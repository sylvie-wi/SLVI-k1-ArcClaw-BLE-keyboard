# SLVI K1 ArcClaw

**A custom 12-key BLE macro pad with OLED display and rotary encoder for ESP32**

---

## Overview

SLVI K1 ArcClaw is a compact, custom-made BLE keyboard designed for my personal use, But feel free to adapt this to your preferences.
It features:

- 12-key layout in a 4×3 matrix
- OLED display for battery status, connection, and keypress feedback
- Indicator LEDs for Fn keys and others
- Rotary encoder for volume or customizable functions
- Multiple Fn layers for extra capabilities

This project is currently in development and the repository tracks design, firmware, and planned features.

---

## Key Features

- **12-key Matrix :** Efficient wiring using 4 rows × 3 columns, with optional diodes for anti-ghosting.  
- **Fn Layers :** Momentary or toggle layers to expand functionality (arrows, media keys, macros).  
- **OLED Display :** 0.91" I²C screen showing battery percentage, connection status, and key presses.  
- **Rotary Encoder :** Default: volume control. With Fn: scroll, page up/down, or custom mappings.  
- **Battery Powered :** Uses 1000 mAh Li-ion cell, planned runtime 20–30 hours with OLED and Fn LEDs.  

**Why doesn't this use QMK? : ** Although QMK seems like THE gold standard for custom keyboard firmware, in my experiance it's wireless side is a bit less polished. That was my main reason to choose to custom program an ESP32 for this. I'm aware that there are better ways to do this than an ESP32, but I'm just working with hardware that's easiest to find for me.

---

## Layout

7 8 9
4 5 6
1 2 3
0 Fn1 Fn2

---

## Planned Wiring

- **Matrix :** 4 rows × 3 columns → 7 GPIO pins  
- **OLED (12C) :** SDA / SCL → 2 GPIOs  
- **Fn LEDs :** 2 GPIOs  
- **Rotary Encoder :** 2 GPIOs + optional push switch  
- **Battery :** 1000 mAh Li-ion via TP4056 with protection  

---

## Project Roadmap

- [ ] Matrix scanning and key debouncing  
- [ ] Fn layer implementation  
- [ ] Rotary encoder functionality  
- [ ] OLED display updates (battery, status, keypresses)  
- [ ] Indicator LEDs for Fn keys  
- [ ] Power optimization (OLED sleep, LED only on Fn press)  
- [ ] Physical assembly / case design  
- [ ] GitHub documentation with photos and wiring diagrams  

---

## Libraries & Dependencies

- [ESP32 BLE Keyboard](https://github.com/T-vK/ESP32-BLE-Keyboard)  
- [Adafruit SSD1306](https://github.com/adafruit/Adafruit_SSD1306) (for OLED)

---

## License

MIT License © 2025 Chenuka W

