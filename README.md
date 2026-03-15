# Dell Inspiron 7560 Hackintosh (macOS 12.7)

Hackintosh EFI configuration for **Dell Inspiron 7560** running **macOS 12.7 Monterey** with **OpenCore**.

This repository provides a working EFI setup for the Dell 7560 with an **Intel i7-7200U** processor and a **DW1560 (BCM94352Z)** Wi-Fi card replacement.

The system is stable for daily use and supports Wi-Fi, Bluetooth, and AirDrop.
![About This Mac](About.PNG)
---

## Hardware

| Component | Model |
|---|---|
| Laptop | Dell Inspiron 7560 |
| CPU | Intel Core i7-7200U (Kaby Lake) |
| iGPU | Intel HD Graphics 620 |
| Wi-Fi / Bluetooth | Broadcom BCM94352Z (DW1560) |
| Ethernet | Realtek RTL8111 |
| Display | 1080p (HiDPI enabled) |
| Touchpad | I2C / PS2 Touchpad |

---

## macOS Version

**macOS Monterey 12.7**

This version was chosen for **stability and compatibility** with Kaby Lake hardware.

---

## Features / Working

✔ Intel HD 620 graphics acceleration  
✔ Wi-Fi working  
✔ Bluetooth working  
✔ AirDrop working  
✔ Ethernet (RealtekRTL8111)  
✔ Audio  
✔ USB ports  
✔ Battery status  
✔ HiDPI enabled via **onekey-hidpi**  
✔ Sleep / Wake  

---

## Touchpad

Touchpad works but **tap-drag is not very reliable**.

Recommended configuration:

Enable **Three-Finger Drag** in macOS accessibility settings.

This provides a much better user experience compared to tap-drag.

---

## HiDPI

HiDPI is enabled using:

`onekey-hidpi`

This allows Retina-like scaling on the internal display.

---

## Wi-Fi Card Replacement

The original Intel Wi-Fi card was replaced with:

**DW1560 (Broadcom BCM94352Z)**

Benefits:

- Native macOS Wi-Fi support  
- Bluetooth working  
- AirDrop / Continuity supported

---

## Important (SMBIOS)

Before using this EFI, **you must generate your own SMBIOS information**.

Do **NOT** use the included serial numbers.

Use **GenSMBIOS** to generate new values and update:

- SerialNumber
- MLB
- SystemUUID

After generating new SMBIOS values, update them in:
config.plist → PlatformInfo → Generic


---



## Notes

This EFI was built and tested specifically for:

Dell Inspiron 7560  
Intel i7-7200U

Other hardware variants may require additional configuration.

---

## Disclaimer

This repository is provided for **educational purposes only**.

Use at your own risk.
