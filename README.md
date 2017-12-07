# tuya-homeassistant

**THIS WILL ONLY WORK FOR SWITCHES. WILL NOT WORK WITH DIMMERS.**

This is a simple platform to control **SOME** switch devices that use the Tuya cloud for control.

It uses a slightly modified version of the pytuya library (https://github.com/clach04/python-tuya) to directly control the switch device.

Most switch devices that use the Tuya cloud should work. If port 6668 is open on the switch device then it will work.

switch id is if the switch device has multiple switches, the switch number.

See here for how to find localKey and devId: http://seandev.org/tuyainst

To use, copy tuya.py to "<home assistant config dir>/custom_components/switch" and add config below to configuration.yaml

Config Fields:
```
switch:
  - platform: tuya
    name: //switch name
    host: //ip of device
    local_key: //localKey
    device_id: //devId
    id: //switch id. leave blank if only one switch
```

Example:
```
switch:
  - platform: tuya
    name: Switch
    host: xxx.xxx.xxx.xxx
    local_key: xxxxxxxxxxxxxxxx
    device_id: xxxxxxxxxxxxxxxxxxxx
    id: 1
```
