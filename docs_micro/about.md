![](/static/mb/device/pano.jpg)

# About

## @description A Blocks / Javascript code editor for the micro:bit, a pocket-size computer with 5x5 display, sensors and Bluetooth.

The [Teknikio Bluebird](https://www.teknikio.com/products/bluebird-beta-v1-6) is a [small blue gadget](/device) that can send and recive information wirelessly. The board has a Neopixel LED, speaker, Bluetooth and sensors that can be programmed by anyone. The development of Bluebird was funded by the National Science Foundation.

The Bluebird provides an easy and fun introduction to programming and making – switch on, program it to do something fun – wear it, customize it.
Just like Arduino, the Bluebird can be connected to and interact with sensors, displays, and other devices via the central connector.

* [Read the docs](/docs)

## [Hardware: The Device](/device)

The Bluebird is packaged with sensors, radio and other goodies. Learn about the [hardware components](/device) of the Bluebird to make the most of it!

## ~ hint

<!--(**Looking to buy a micro:bit?** See the [list of resellers](https://microbit.org/resellers).) -->

## ~

## Programming: [Blocks](/blocks) or [JavaScript](/javascript)

You can program the Bluebird using [Blocks](/blocks) or [JavaScript](/javascript) in your web browser via the [micro:bit APIs](/reference):

```block
input.onButtonPressed(Button.A, () => {
    basic.showString("Hi!");
})
```
```typescript
input.onButtonPressed(Button.A, () => {
    basic.showString("Hi!");
})
```

The editor work in [most modern browsers](/browsers), work [offline](/offline) once loaded and do not require any installation.

## [Compile and Flash: Your Program!](/device/usb)

When you have your code ready, you connect your Bluebird to a computer via a USB cable, so it appears as a mounted drive (named TEKBOOT).

Compilation to ARM thumb machine code from [Blocks](/blocks) or [JavaScript](/javascript) happens in the browser. You save the ARM binary
program to a file, which you then copy to the TEKBOOT drive, which flashes the Bluebird device with the new program.

## Simulator: Test Your Code

You can run your code using the Bluebird simulator, all within the confines of a web browser.
The simulator has support for the LED screen, buttons, as well as compass, accelerometer, and digital I/O pins.

```sim
basic.forever(() => {
  basic.showString("Hi!");
})
input.onButtonPressed(Button.A, () => {
    led.stopAnimation();
    basic.showLeds(`
. . . . .
. # . # .
. . . . .
# . . . #
. # # # .`);
});
input.onButtonPressed(Button.B, () => {
    led.stopAnimation();
    basic.showLeds(`
. # . # .
# . # . #
# . . . #
. # . # .
. . # . .`);
});
```

## Learn!

We have tons of [projects](/projects), [examples](/examples) and [courses](/courses) to get your started!

## C++ Runtime

The [C++ micro:bit runtime](http://lancaster-university.github.io/microbit-docs/), created at [Lancaster University](http://www.lancaster.ac.uk/), provides access to the hardware functions of the micro:bit,
as well as a set of helper functions (such as displaying a number/image/string on the LED screen).

The [micro:bit library](/reference) mirrors the functions of the C++ library.
When code is compiled to ARM machine code, the calls to JavaScript micro:bit functions are replaced with calls to the corresponding C++ functions.

## [Command Line Tools](/cli)

Looking to use @homeurl@ in your favorite editor? Install the [command line tools](/cli) and get rolling!

## [Extensions](/extensions)

Create, edit and distribute your own blocks and JavaScript using [extensions](/extensions). Extensions are hosted on GitHub and may be written using C++, JavaScript and/or ARM thumb.

## [Open Source](/open-source)

The code for the micro:bit is [open source](/open-source) on GitHub. Contributors are welcome!

```package
radio
```
