## Generic ESP32-S3 (SPIRAM Octal)

**Vendor:** Espressif

**Features:** BLE, WiFi

**Source on GitHub:** [esp32/GENERIC_S3_SPIRAM_OCT](https://github.com/micropython/micropython/tree/master/ports/esp32/boards/GENERIC_S3_SPIRAM_OCT)

**More info:** [Website](https://www.espressif.com/en/products/modules)

## Installation instructions

Program your board using the esptool.py program, found [here](https://github.com/espressif/esptool).

If you are putting MicroPython on your board for the first time then you should first erase the entire flash using:

```bash
esptool.py --chip esp32s3 --port /dev/ttyACM0 erase_flash
```

From then on program the firmware starting at address 0:

```bash
esptool.py --chip esp32s3 --port /dev/ttyACM0 write_flash -z 0 board-20210902-v1.17.bin
```
