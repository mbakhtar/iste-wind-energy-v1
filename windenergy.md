# Wind Turbine
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
=github:climate-action-kits/pxt-fwd-edu
=github:climate-action-kits/pxt-fwd-edu
```
## Step 1 @showdialog
Plug your USB cable into the micro:bit and insert it into the 
Climate Action Kit board. 
![breakout board](https://raw.githubusercontent.com/mbakhtar/wind-turbine-lesson-tutorial/master/breakout-resized.png)

## Step 2 @showhint
Click on the button to the right of download and follow the steps to pair your micro:bit.
![pair gif](https://raw.githubusercontent.com/mbakhtar/iste-electric-vehicle-v1/master/pair%20microbit-280x203.gif)


## Step 3
Click on the ``||fwdSensors:Sensors||`` drawer and find the 
``||fwdSensors:on dial1 turned delta||`` block. Drag and drop it on the coding space. 
```blocks
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
```
## Step 4
Right click on the ``||fwdSensors:on dial1 turned delta||`` block and duplicate it. It will grey out.
```blocks
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
```
## Step 5
Change the direction arrow of the second or greyed out ``||fwdSensors:on dial1 turned delta||`` block. 
![dial direction](https://raw.githubusercontent.com/mbakhtar/wind-turbine-lesson-tutorial/master/dial%20direction%20change.gif)
```blocks
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    })
```
## Step 6
Click the ``||fwdSensors: Sensors||`` drawer and add a 
``||fwdSensors:on touch down||`` block to the coding space.
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    })
```
## Step 7
To control the speed of the ``||Wind Mill||`` the ``||fwdSensors:Dial||`` is used.
From the ``||fwdMotors:Motors||`` drawer drag and drop 
``||fwdMotors:set servo1 to 50 %||`` under the
``||fwdSensors:on dial1 turned delta||`` block.
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(50)
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    })
```
## Step 8  
Right click on ``||fwdMotors:set servo1 to 50 %||`` block and duplicate it.
Place it under the second or other ``||fwdSensors:on dial1 turned delta||`` block.
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(50)
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(50)
})
```

## Step 9
To set the speed of the ``||Wind Mill||`` according to the turn 
of the ``||fwdSensors:Dial||``. Click on ``||fwdSensors:Sensors||``.
Find the ``||fwdSensors:dial1 absolute position||`` oval block drag it close to the ``||fwdMotors:set servo1 50 %||``.
It should click in place of ``||fwdMotors:50 %||`` of the ``||fwdMotors:set servo1 50 %||`` block. 
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(fwdSensors.dial1.fwdPosition())
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(50)
})
```
## Step 10
Repeat the last step for the other or second ``||fwdSensors:on dial1 turned delta||`` block. Click on ``||fwdSensors:Sensors||``.
Find the ``||fwdSensors:dial1 absolute position||`` oval block drag it close to the ``||fwdMotors:set servo1 50 %||``.
It should click in place of ``||fwdMotors:50 %||`` of the ``||fwdMotors:set servo1 50 %||``.
block. 
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
## Step 11
The ``||fwdSensors:Dial||`` push button is the ||STOP|| button for the ``||Wind Mill||``. Click on 
``||fwdMotors:Motors||`` and find the ``||fwdMotors:set servo1 50 %||`` block. Drag and place it under
the ``||fwdSensors:on touch down||`` block.
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    fwdMotors.servo1.fwdSetSpeed(50)
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(fwdSensors.dial1.fwdPosition())
})
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    fwdMotors.servo1.fwdSetSpeed(fwdSensors.dial1.fwdPosition())
})
```
## Step 12
Change the speed of ``||fwdMotors:set servo1 50 %||`` block nested or placed inside or under the ``||fwdSensors:on touch down||``
to ``||0||``. Whenever the ``||fwdSensors:Dial||`` will be pressed/pushed down the ``||Wind Mill||`` will stop turning.
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

## Step 12
``|Download|`` and test your code.
Congratulations on completing your Wind Turbine Project! - Go back to the lesson for more activities and extensions.
```package
