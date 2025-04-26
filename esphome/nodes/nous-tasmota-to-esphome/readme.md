**Brief instructions:**

Tested with A8T and D3T.

Flashing from Tasmota to Esphome is possible OTA.
In case something went wrong, see [readme.md](./../../docs/readme.md).
1. edit wifi-> manual_ip
2. `esphome compile test.yaml`
3. update FW:
   a. connect to device-AP `tasmota-xxxxxx`, `http://192.168.4.1`
   b. configure connection to local AP, wait on same site for the new ip
   c. re-connect to device via local ap (new ip)
   d. upload compiled file: `./.esphome/build/test/.pioenvs/test/firmware.bin` via tasmota website
   e. device reboots automatically
   f. device ip is now as configured in `test.yaml`
4. `esphome -v upload-factory-ota test.yaml`
5. done: device is now esphomed and can be flashed with real esphome config

**Detailed instructions:**

[1] https://devices.esphome.io/devices/Nous-A8T
[2] steps 21 to 32: https://github.com/kadam12g/ESPHome-Shelly-Plus-Plug-S?tab=readme-ov-file

**Notes:**

- the config file must be named `test.yaml` according to [2]
- `esphome` command must be invoked according to [2]
- `esphome` repository must be cloned at specific commit according to [2]
- after step 4 the device can be flashed with real config and up-to-date `esphome`
