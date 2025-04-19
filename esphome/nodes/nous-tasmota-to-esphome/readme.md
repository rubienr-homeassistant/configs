**Brief instructions:**

Flashing from Tasmota to Esphome is possible OTA.
In case something went wrong, see [readme.md](./../../docs/readme.md).
1. edit wifi-> manual_ip
2. `esphome compile test.yaml`
3. upload compiled file via tasmota website -> reboot
4. `esphome -v upload-factory-ota test.yaml`

**Detailed instructions:**

[1] https://devices.esphome.io/devices/Nous-A8T
[2] steps 21 to 32: https://github.com/kadam12g/ESPHome-Shelly-Plus-Plug-S?tab=readme-ov-file

**Notes:**

- this file must be named `test.yaml` according to [2]
- `esphome` command must be invoked   according to [2]
