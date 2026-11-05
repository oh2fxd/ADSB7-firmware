# ADSB7 Firmware (OTA Releases)

Precompiled firmware binaries for **ADSB7** — a standalone 7-inch ESP32-S3 ADS-B Aircraft Radar & Flight Tracker display.

## Overview
ADSB7 connects to local or remote `readsb` / `dump1090` / `tar1090` feeds over Wi-Fi and renders real-time aircraft positions, flight vectors, altitude color-coding, callsigns, and range rings on an 800×480 RGB TFT touch display.

## Hardware Target
- **MCU**: ESP32-S3 (Dual-core XTensa LX7, 16 MB Flash, 8 MB Octal PSRAM)
- **Display**: Waveshare ESP32-S3-Touch-LCD-7 (800×480 RGB565, GT911 capacitive touch)

## Downloads & OTA Endpoints
- **Latest Version**: `v0.1.6`
- **OTA Binary**: [`ADSB7.bin`](https://raw.githubusercontent.com/oh2fxd/ADSB7-firmware/main/ADSB7.bin)
- **Full Factory Image (Merged)**: [`ADSB7.merged.bin`](https://raw.githubusercontent.com/oh2fxd/ADSB7-firmware/main/ADSB7.merged.bin) (flash at `0x0`)
- **OTA Manifest**: [`firmware.json`](https://raw.githubusercontent.com/oh2fxd/ADSB7-firmware/main/firmware.json)
- **Changelog**: [`CHANGELOG.md`](./CHANGELOG.md)

## Flashing Instructions

### 1. Automatic Over-The-Air (OTA)
The device checks `firmware.json` and updates directly from the on-screen settings menu or web portal.

### 2. USB / Serial Flashing (`esptool.py`)
To flash a blank board with the merged factory binary:
```bash
esptool.py --chip esp32s3 --port /dev/ttyACM0 --baud 921600 write_flash 0x0 ADSB7.merged.bin
```
To flash only the application partition:
```bash
esptool.py --chip esp32s3 --port /dev/ttyACM0 --baud 921600 write_flash 0x10000 ADSB7.bin
```

## License
Distributed under the [MIT License](./LICENSE). Copyright (c) 2026 OH2FXD.
