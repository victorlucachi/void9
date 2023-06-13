# VOID9
*A 3x3 handwired macropad*

![VOID9](https://i.imgur.com/Db82OaX.jpg)

The VOID9 is a 3d printed, handwired, 4x4 macropad running QMK Firmware on a Pro Micro controller.

I suggest printing the case using a 0.4 mm nozzle, supports are not needed for any of the parts.

You might want/need to use small dabs of hot glue to secure the switches in the plate depending on how well calibrated your printer is (if you're generous with it, it will add to the weight of the keyboard and it might change the feel of it).

Dont overtighten the screws as the threads might get stripped.

# WARNING

Comlumn pinout has been revised, if you have an older build of the macropad (built before October 2022, which was using pins D1, D0, D4) edit the info.json file in the firmware forks in order to reflect your wiring!

# Bill Of Materials

* 9 x diodes ([tme.eu](https://www.tme.eu/ro/en/details/1n4148-dio/tht-universal-diodes/diotec-semiconductor/1n4148/)/[aliexpress](https://www.aliexpress.com/item/32729204179.html))
* 9 x Cherry MX style mechanical switches
* 9 x keycaps of choice
* 1 x Pro Micro ([aliexpress](https://www.aliexpress.com/item/32902569443.html))
* 24 AWG (0.2 mm2) wire
* 4 x 8mm bumpons

### Redux
* 6 x M2x3x3.5 OD heat inserts ([aliexpress](https://www.aliexpress.com/item/4000585933306.html?spm=a2g0o.order_list.order_list_main.33.21ef1802vdSNrS))
* 4 x M2x10 Allen head screws ([aliexpress](https://www.aliexpress.com/item/32966941844.html?spm=a2g0o.order_detail.order_detail_item.9.722ff19cyjrixq))
* 2 x M2x6 Countersunk screws ([aliexpress](https://www.aliexpress.com/item/32968097507.html?spm=a2g0o.order_list.order_list_main.32.21ef1802vdSNrS))

### V1
* 4 x M3x10 Allen head bolts ([tme.eu](https://www.tme.eu/ro/en/details/m3x10_d912-a2/bolts/kraftberg/)/[aliexpress](https://www.aliexpress.com/item/32966941844.html))
* hotglue

# Community Mods

Contributions by @dlehman

Bottom - Angled - Short: Designed to be used with the middle ring (Middle - Angled: eg. if you want a contrasting color stripe). The short bottom + middle layer will be the same height as the regular bottom.

Bottom - Angled - Short - Teensy2: A version of the "Bottom - Angled - Short" model designed for a [Teensy 2.0 controller](https://www.pjrc.com/store/teensy.html) with a Mini (not "micro") USB port on it.

# Handwiring guide

I've also put together a pretty visual handwiring guide for the VOID9, that you can browse over [here](https://victorlucachi.ro/journal/void9-wiring-guide/).

| ![](https://i.imgur.com/01WknB5.jpg) 	| ![](https://i.imgur.com/GMMczAH.jpg) 	| ![](https://i.imgur.com/5NyUoJY.jpg) 	|
|---------------------------------------|---------------------------------------|---------------------------------------|

# Pin assignment

    ROW0    ROW1    ROW2
    F4      F5      F6
    
    
    COL0    COL1    COL2
    D1      D4      D0
    
    Encoder Pad A           Encoder Pad B
    B1                      F7
    B2                      B3

# QMK Vial Fork

A QMK Vial fork can be found [here](https://github.com/victorlucachi/vial-qmk/tree/dev_void/keyboards/handwired/void9).

Most features are disabled in order for the firmware to fit on the atmega32u4 present on the Pro Micro controllers, but if you want to tinker around with different features or if you're using a different MCU you can enable/disable them to suit your own needs by editing the rules.mk file in the vial keymap folder.

The web version of Vial is available at [vial.rocks](https://vial.rocks/); it runs in supported browsers (Chrome, Edge and Opera) without requiring an installation.

![VOID9 Vial](https://user-images.githubusercontent.com/2669084/198689647-d4c7ffd5-a325-413a-b2e1-e0ccaf95869d.png)

# QMK Fork

A fork containing the QMK config files can be found [here](https://github.com/victorlucachi/qmk_firmware/tree/dev_void/keyboards/handwired/void9). Edit them to suit your own needs and build the firmware following the QMK docs.

If you plan on using the VIA configurator dont forget to download the json definitions file linked in this repository.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-blue)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).
