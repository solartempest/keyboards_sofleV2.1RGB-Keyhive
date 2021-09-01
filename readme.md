# Sofle Keyboard

![SofleKeyboard version 2.1 RGB Keyhive](https://i.imgur.com/WH9OoWu.jpg)

Sofle is 6×4+5 keys column-staggered split keyboard. Based on Lily58, Corne and Helix keyboards.

More details about the keyboard on Josef's blog: [Sofle Keyboard - a split keyboard based on Lily58 and Crkbd](https://josef-adamcik.cz/electronics/let-me-introduce-you-sofle-keyboard-split-keyboard-based-on-lily58.html)

Build guide and log is available here: [SofleKeyboard build log/guide](https://josef-adamcik.cz/electronics/soflekeyboard-build-log-and-build-guide.html)

* Keyboard Maintainer: [Solartempest]
* Hardware Supported: SofleKeyboard V2.1 RGB PCB, ProMicro / Elite-C
* Hardware Availability: [Keyhive](https://keyhive.xyz/shop/sofle)

# Custom Features:

### OLED Features:
-   Includes Snakey keyboard pet! Slithers according to WPM, bites, and sticks its tongue out at you!
-	OLED displays current layer, lock key status, WPM, custom logo, and custom name.
-	OLED shuts off on idle and when computer is sleeping.
-	Includes working Luna keyboard pet.
-	Includes working Bongocat (disable RGB for sufficient space).
-   Includes stock OLED code as well.

### RGB Features:
-   Adds custom layer lighting with custom gradients for each layer.
-   RGB underglow support and remapped to physical locations (nicer gradients and effects).
-   Adds white caps lock, scroll lock, and num lock key indicators using the top row/underglow LEDs.

### Rotary Encoder and VIA Features:
-   Fully emappable left encoder controls volume up/down/mute. Right encoder PGUP/PGDOWN.
-   Allows for  live remapping of per-layer rotary encoder functions in VIA.
-   VIA support included by default.
-   This fixes the Keyhive left bottom row offset issue in VIA. You will need to import sofle.json in VIA.
-   Custom macro key in VIA for Super Alt Tab, which is fully compatible with rotary encoders.
-   Custom macro key in VIA for moving windows to other monitors in Windows, which is fully compatible with rotary encoders.

### Tap and Other Features:
-   Push left-shift + backspace to delete whole words. Right-shift + backspace to delete whole words in the opposite direction.
-   Double tap layers to stay on a layer instead of momentary push.
-   Adds key combo functionality.
-   Symmetric modifiers (CMD/Super, Alt/Opt, Ctrl, Shift).


# Compiling

Compile with the command below:

```sh
# for Elite C with Left Side Master builds
qmk compile -kb solartempest/sofle -km via
```

## Flashing

Flash using the correct command below (or use QMK Toolbox like me):

```sh
# for pro micro-based builds
qmk flash -kb solartempest/sofle -km via -bl avrdude-split-left
qmk flash -kb solartempest/sofle -km via -bl avrdude-split-right

# for Elite C or dfu bootloader builds
qmk flash -kb solartempest/sofle -km via -bl dfu-split-left
qmk flash -kb solartempest/sofle -km via -bl dfu-split-right
```

These commands can be mixed if, for example, you have an Elite C on the left and a pro micro on the right.
Press reset button on he keyboard when asked.

Disconnect the first half, connect the second one and repeat the process.


See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).
