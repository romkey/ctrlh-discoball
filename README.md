# PDX Hackerspace Discoball LED Controller

![image](https://github.com/romkey/ctrlh-discoball/blob/master/img/bagged-discoball.jpg)

Congratulations on getting a Discoball!

Discoball is open source hardware which runs open source software that lets you control sets of RGB LEDs via a web page or MQTT broker. RGB LEDs are LEDs with built-in controllers (like the [Adafruit Neopixel](https://www.adafruit.com/category/168), not tricolor LEDs. The  Discoball includes a short strand of 5 LEDs, but you can use much longer strands with it if you want.

## Packing Slip Errata

Your package should also contain one 4 pin header, not listed on the packing slip. This header is for the optional I2C interface pins; you can  ignore it if you're not going to connect an external I2C device.

## Some Assembly Required

You can find instructions on assembling your discoball at https://github.com/romkey/discoball

Once you've assembled the circuit you can wire up the included LED strand by connecting its red wire to terminal "5" (+5V) on the screw terminal, white to terminal "D" (data) and blue to terminal "G" (ground).

## Software Included

Once you've assembled the discoball you'll need to build its software. You can find instructions on how to do that at https://github.com/romkey/vendo

Use this for your `src/config.h` file:
```
#define NUM_LEDS 5
#define LED_DATA_PIN 33
#define LED_TYPE WS2811
#define LED_RGB RGB

// #define USE_MQTT
// #define HAS_BME280

#define VERBOSE
```
