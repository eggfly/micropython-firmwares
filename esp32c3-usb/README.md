## ESP32-C3 with USB

![](https://micropython.org/resources/micropython-media/boards/GENERIC_C3_USB/esp32c3_devkitmini.jpg)

**Vendor:** Espressif

**Features:** BLE, WiFi

**Source on GitHub:** [esp32/GENERIC_C3_USB](https://github.com/micropython/micropython/tree/master/ports/esp32/boards/GENERIC_C3_USB)

**More info:** [Website](https://www.espressif.com/en/products/modules)

## Installation instructions

Program your board using the esptool.py program, found [here](https://github.com/espressif/esptool).

If you are putting MicroPython on your board for the first time then you should first erase the entire flash using:

```bash
esptool.py --chip esp32c3 --port /dev/ttyUSB0 erase_flash
```

From then on program the firmware starting at address 0x0:

```bash
esptool.py --chip esp32c3 --port /dev/ttyUSB0 --baud 460800 write_flash -z 0x0 esp32c3-20220117-v1.18.bin
```
