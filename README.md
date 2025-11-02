# Flare
WLED-compatible RGB Controller for WS2812B LED Strips.

![](https://github.com/user-attachments/assets/01897882-3171-4fea-9fe0-1f4a1d08b7ed)


> [!WARNING]
> This hardware design will not be revised or updated. If you decide to build one yourself, please be aware that my design is not ideal. The routing could be better, no decoupling near the LEDs. It still works tho.

## Features
- WLED compatible
- ESP32S microcontroller
- INMP441 microphone for audio reactivity
- Single USB Type-C port for power (PD 5V 3A) and flashing
- 3A fuse for protection
- WAGO connector for LED strips
- Two user programmable button
- Efficient DC-DC buck converter

## Power Indicators
- LED_PD - Lights up when the board successfully negotiates USB PD at 5V 3A.
- LED_PWR - Lights up when the board receives power.

> [!WARNING]
> When powered from a regular 5V source (non-PD), only LED_PWR will light up. Please avoid drawing more than 1A to prevent damage.

> [!NOTE]
> Both LEDs currently use the same color. Consider using a different color for PD and PWR so they can be easily distinguished.

## Flashing WLED
Please use this [web installer](https://wled-install.github.io/) (Chromium-based browser only)

Choose board: `ESP32 (4MB Flash, with Audio reactive Usermod)`

Or alternatively, download the latest build from WLED's [releases page](https://github.com/wled/WLED/releases) and flash with esptool.

## Configuring WLED

- MIC SD: GPIO26
- MIC WS: GPIO25
- MIC SCK: GPIO21
- SW1: GPIO18
- SW2: GPIO19
- OUT1: GPIO4
- OUT2: GPIO16

![](https://github.com/user-attachments/assets/8dd93d50-ebba-482c-a1d6-12f81acf830b)
![](https://github.com/user-attachments/assets/a39d3766-b2b2-47e5-8999-9ed977725edf)
![](https://github.com/user-attachments/assets/859ba2d6-f69f-4173-841e-33d3e83894c6)


Please follow the official WLED documentation: https://kno.wled.ge/

## TODO
- [ ] Upload STL files

## License
This project is licensed under the MIT License.

## Credits
- WLED, Akemi &copy; Aircookie
- Inspired by the awesome WLED community
