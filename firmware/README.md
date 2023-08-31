# Firmware

- [QMK and vial config](https://github.com/sporkus/qmk_userspace/tree/main/keyboards/sporkus/capybully)
- [Pre-compiled vial binary](./sporkus_capybully_vial.bin)

## First flash
Use tweezers to short the DFU pads while powering up the PCB will put it into DFU bootloader mode. Afterwards, you can use bootmagic or keycodes to enter the bootloader mode.

To flash, you can use `qmk flash` or `dfu-util` on cli. Alternatively, you can flash the binary using qmk toolbox.

