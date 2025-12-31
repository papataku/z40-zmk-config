# z40  ZMK Firmware

This repo contains the firmware for the z40 BLE PCB.

Should you desire to track ZMK `main` (or some other branch of ZMK), simply edit the `config/west.yml` file and replace the contents with:

```
manifest:
  remotes:
    - name: petejohanson
      url-base: https://github.com/petejohanson
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: z40-zmk-module
      remote: papataku
      revision: main
  self:
    path: config
```

And then comment out the line in `config/z40.conf`:

```
# CONFIG_ZMK_PM_SOFT_OFF=y
```
