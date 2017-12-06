This is a simple platform to control **SOME** devices that use the Tuya cloud for control.

It uses a slightly modified version of the pytuya library (https://github.com/clach04/python-tuya) to directly control the device.

Most devices that use the Tuya cloud should work. If port 6668 is open on the device then it will work.

switch id is if the device has multiple switches, the switch number.

See here for how to find localKey and devId: https://github.com/codetheweb/tuyapi/blob/master/docs/SETUP.md

Config Fields:
```
switch:
  - platform: tuya
    name: //switch name
    host: //ip of device
    password: //localKey
    username: //devId
    id: //switch id. if only one switch, use 1
```

Example:
```
switch:
  - platform: tuya
    name: Switch
    host: xxx.xxx.xxx.xxx
    password: xxxxxxxxxxxxxxxx
    username: xxxxxxxxxxxxxxxxxxxx
    id: 1
```