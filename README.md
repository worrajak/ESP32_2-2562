# ESP32_2-2562

ESP32 pinout 
![ScreenShot](https://github.com/worrajak/ESP32_2-2562/blob/master/images.jpeg?raw=true)

See the ESP32 Datasheet for information on ESP32 chips and the ESP32-PICO-D4 Datasheet for information on the SiP module.

* Processors:
- Main processor: Tensilica Xtensa 32-bit LX6 microprocessor
- Cores: 2 or 1 (depending on variation)
- All chips in the ESP32 series are dual-core except for ESP32-S0WD, which is single-core.
- Clock frequency: up to 240 MHz
- Performance: up to 600 DMIPS
- Ultra low power co-processor: allows you to do ADC conversions, computation, and level thresholds while in deep sleep.
* Wireless connectivity:
- Wi-Fi: 802.11 b/g/n/e/i (802.11n @ 2.4 GHz up to 150 Mbit/s)
- Bluetooth: v4.2 BR/EDR and Bluetooth Low Energy (BLE)
Memory:
Internal memory:
ROM: 448 KiB
For booting and core functions.
SRAM: 520 KiB
For data and instruction.
RTC fast SRAM: 8 KiB
For data storage and main CPU during RTC Boot from the deep-sleep mode.
RTC slow SRAM: 8 KiB
For co-processor accessing during deep-sleep mode.
eFuse: 1 Kibit
Of which 256 bits are used for the system (MAC address and chip configuration) and the remaining 768 bits are reserved for customer applications, including Flash-Encryption and Chip-ID.
Embedded flash:
Flash connected internally via IO16, IO17, SD_CMD, SD_CLK, SD_DATA_0 and SD_DATA_1 on ESP32-D2WD and ESP32-PICO-D4.
0 MiB (ESP32-D0WDQ6, ESP32-D0WD, and ESP32-S0WD chips)
2 MiB (ESP32-D2WD chip)
4 MiB (ESP32-PICO-D4 SiP module)
External flash & SRAM: ESP32 supports up to four 16 MiB external QSPI flashes and SRAMs with hardware encryption based on AES to protect developers' programs and data. ESP32 can access the external QSPI flash and SRAM through high-speed caches.
Up to 16 MiB of external flash are memory-mapped onto the CPU code space, supporting 8-bit, 16-bit and 32-bit access. Code execution is supported.
Up to 8 MiB of external flash/SRAM memory are mapped onto the CPU data space, supporting 8-bit, 16-bit and 32-bit access. Data-read is supported on the flash and SRAM. Data-write is supported on the SRAM.
ESP32 chips with embedded flash do not support the address mapping between external flash and peripherals.
Peripheral input/output: Rich peripheral interface with DMA that includes capacitive touch, ADCs (analog-to-digital converter), DACs (digital-to-analog converter), I²C (Inter-Integrated Circuit), UART (universal asynchronous receiver/transmitter), CAN 2.0 (Controller Area Network), SPI (Serial Peripheral Interface), I²S (Integrated Inter-IC Sound), RMII (Reduced Media-Independent Interface), PWM (pulse width modulation), and more.
Security:
IEEE 802.11 standard security features all supported, including WFA, WPA/WPA2 and WAPI
Secure boot
Flash encryption
1024-bit OTP, up to 768-bit for customers
Cryptographic hardware acceleration: AES, SHA-2, RSA, elliptic curve cryptography (ECC), random number generator (RNG)

