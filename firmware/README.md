# Firmware

- [QMK and vial config](https://github.com/sporkus/qmk_userspace/tree/main/keyboards/sporkus/capybully)
- [Pre-compiled vial binary](./sporkus_capybully_vial.bin)

## First flash
Use tweezers to short the DFU pads while powering up the PCB will put it into DFU bootloader mode. Afterwards, you can use bootmagic or keycodes to enter the bootloader mode.

To flash, you can use `qmk flash` or `dfu-util` on cli. Alternatively, you can flash the binary using qmk toolbox.


## EC Matrix features
#### Tuning
The baseline for each key is different. Even if you use the same parts, they can change between assemblies. The very first time firmware is flashed, a quick auto tuning will be done (about half a minute). As long as you don't intentionally feather the keys, it should be immediately usable and not affect the tuning result.

To re-tune after assembly, you can either use the keycode `EC_CLR` to reset the configuration. 

#### Actuation point adjustment
Use the keycodes `EC_AP_I`/`EC_AP_D` to increase/decrease the actuation point.

#### Advanced users
More options can be enabled in the config.h file.
- `ECSM_TUNE_ON_BOOT`: re-tune on every boot. It's not really necessary and increases write cycles to the flash memory.
- `ECSM_DEBUG`: prints EC config and readings in console.
