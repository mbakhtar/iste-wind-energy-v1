# Wind Mill 
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
=github:climate-action-kits/pxt-fwd-edu
=github:climate-action-kits/pxt-fwd-edu
```
## Step 1 @showdialog
Plug your USB cable into the micro:bit and insert it into the 
Climate Action Kit board. Click on the button to the right of 
download and follow the steps to pair your micro:bit.
![Plug your USB cable into the micro:bit and insert it into the 
Climate Action Kit board. Click on the button to the right of 
download and follow the steps to pair your micro:bit.](https://raw.githubusercontent.com/mbakhtar/iste-wind-energy-v1/master/pair%20microbit-280x203.gif)



## Step 2
Click on the ``||fwdSensors:Sensors||`` drawer and find the 
``||fwdSensors:on dial1 turned delta||`` block. Duplicate it. Change the direction arrow on the second block.
Hit download to activate your ``||fwdSensors:Dial||`` and a ``||fwdSensors:Touch button||``. 
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
To control the speed of the ``||Wind Mill||`` use the ``||fwdSensors:Dial||``
from the ``||fwdMotors:Motors||`` drawer. Nest 
``||fwdMotors:set servo1 to 0 %||`` under the
``||fwdSensors:on dial1 turned delta||`` block.
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(0)
})
```
## Step 5
Duplicate ``||fwdMotors:set servo1 to 0 %||``
and placed it under the other ``||fwdSensors:on dial1 turned delta||`` block and the ``||fwdMotors:set servo block||``.
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(0)
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(0)
})
```

## Step 6
Set the speed of the ``||Wind Mill||`` according to the turn 
of the ``||fwdSensors:Dial||``. Click on ``||fwdSensors:Sensors||``.
Drag the ``||fwdSensors:dial1 absolute position||`` oval block. 
It should click in place of ``||fwdMotors:0 %||`` of the ``||fwdMotors: set servo1 0%||``
block. Do it for the other ``||fwdSensors:on dial1 turned delta||`` and ``||fwdMotors:set servo1 0%||`` as well. 
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(fwdSensors.dial1.fwdPosition())
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(fwdSensors.dial1.fwdPosition())
})
```
## Step 7
The ``||fwdMotors:set servo1 0%||``under ``||fwdSensors: on touch down||`` block stays the same.
Check your code by downloading and turning the ``||fwdSensors:Dial||``.
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
## Step 8
Congratulations on completing your Wind Turbine Project! - Go back to the lesson for more activities and extensions.
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
=github:climate-action-kits/pxt-fwd-edu
=github:climate-action-kits/pxt-fwd-edu
```
