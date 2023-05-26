
> Open this page at [https://mbakhtar.github.io/iste-wind-energy-v1/](https://mbakhtar.github.io/iste-wind-energy-v1/)

## Use as Extension

This repository can be added as an **extension** in MakeCode.

* open [Wind Energy Tutorial v1](https://makecode.microbit.org/#tutorial:github:mbakhtar/iste-wind-energy-v1/windenergy)
* click on **New Project**
* click on **Extensions** under the gearwheel menu
* search for **https://github.com/mbakhtar/iste-wind-energy-v1** and import

## Edit this project ![Build status badge](https://github.com/mbakhtar/iste-wind-energy-v1/workflows/MakeCode/badge.svg)

To edit this repository in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **Import** then click on **Import URL**
* paste **https://github.com/mbakhtar/iste-wind-energy-v1** and click import

## Blocks preview

This image shows the blocks code from the last commit in master.
This image may take a few minutes to refresh.

![A rendered view of the blocks](https://github.com/mbakhtar/iste-wind-energy-v1/raw/master/.github/makecode/blocks.png)
# Wind Mill 
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
=github:climate-action-kits/pxt-fwd-edu
=github:climate-action-kits/pxt-fwd-edu
```
## Step 1 
Plug your USB cable into the micro:bit and insert it into the 
Climate Action Kit board. Click on the button to the right of 
download and follow the steps to pair your micro:bit.


## Step 2
Click on the ``||fwdSensors:Sensors||`` drawer and find the 
``||fwdSensors:on dial1 turned delta||`` block. You will need two of these blocks 
Drag the block on the coding space and duplicate it.
Hit download to activate your ``||fwdSensors:Dial||`` and a ``||fwdSensors:Touch button||`` 
```blocks
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    })
```
## Step 3
Click the ``||fwdSensors: Sensors||`` drawer and add a 
``||fwdSensors:on touch down||`` block to the coding screen.
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    })
```

## Step 4
To control the motion of the ``||Wind Mill||`` the ``||fwdSensors:Dial's||``
clockwise and counter clockwise turn will increase and decrease the speed of it.
Click on ``||fwdMotors:Motors||`` drawers and drag 
``||fwdMotors:set servo1 to 0 %||`` to place it under 
``||fwdSensors:on dial1 turned delta||`` block. Duplicate ``||fwdSensors:set servo1 to 0 %||``
and placed it under the other ``||fwdSensors:on dial1 turned delta||`` block as well.
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed()
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed()
})
```
## Step 5
Now to set the speed of the ``||Wind Mill||`` according to the turn 
of the ``||fwdSensors:Dial||``. Click on ``||fwdSensors:Sensors||``
Drag the ``||fwdSensors:dial1 absolute position||`` oval block. 
It should click in place of ``||fwdMotors:0 %||`` of the ``||fwdMotors: set servo1 0%||``
block. Do it for the other block as well. The ``||fwdMotors:set servo1 0 %||``
under ``||fwdSensors: on touch down||`` block stays the same.
Check your code by downloading and turning the ``||fwdSensors:Dial||`` 
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    fwdMotors.servo1.fwdSetSpeed(0)
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(fwdSensors.dial1.fwdPosition())
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(fwdSensors.dial1.fwdPosition())
})
```
## Step 6
Congratulations on completing your Wind Energy - Wind Mill Project! - everyone can use tech to make the world a better place! Go back to the Forward Edu lesson for more activities and extensions"

#### Metadata (used for search, rendering)

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
