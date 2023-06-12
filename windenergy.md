# Wind Turbine
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
=github:climate-action-kits/pxt-fwd-edu
=github:climate-action-kits/pxt-fwd-edu
```
## @showdialog
Welcome to Wind Turbine Coding Tutorial
![built project](https://raw.githubusercontent.com/mbakhtar/iste-wind-energy-v1/master/project%20-%20windturbine.png)

## Step 1 @showdialog
Plug your USB cable into the micro:bit and insert it into the 
Climate Action Kit board. 
![breakout board](https://raw.githubusercontent.com/mbakhtar/wind-turbine-lesson-tutorial/master/breakout-resized.png)

## Step 2 @showhint
Click three dots besides ``|Download|`` button and follow the steps to pair your micro:bit.
![pair gif](https://raw.githubusercontent.com/mbakhtar/iste-electric-vehicle-v1/master/pair%20microbit-280x203.gif)


## Step 3
Click ``||fwdSensors:Sensors||`` drag and drop
``||fwdSensors:on dial1 turned delta||`` block on workspace. 
```blocks
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
```
## Step 4
Right click ``||fwdSensors:on dial1 turned delta||`` block and duplicate. _Note: New block will be grey._
```blocks
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
```
## Step 5
Change the direction arrow of the greyed out ``||fwdSensors:on dial1 turned delta||`` block. 
![dial direction](https://raw.githubusercontent.com/mbakhtar/wind-turbine-lesson-tutorial/master/dial%20direction%20change.gif)
```blocks
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    })
```
## Step 6
Click ``||fwdSensors:Sensors||`` drag and drop 
``||fwdSensors:on touch down||`` block to workspace.
```blocks
fwdSensors.touch.fwdOnTouch(jacdac.ButtonEvent.Down, function () {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.cw, function (delta) {
    })
fwdSensors.dial1.fwdOnDialTurned(fwdSensors.dialDirection.ccw, function (delta) {
    })
```
## Step 7
Click ``||fwdMotors:Motors||`` drag and drop 
``||fwdMotors:set servo1 to 50 %||`` inside
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
Right click ``||fwdMotors:set servo1 to 50 %||`` block and duplicate.
Drag and drop inside the second ``||fwdSensors:on dial1 turned delta||`` block.
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
Click ``||fwdSensors:Sensors||``. Drag ``||fwdSensors:dial1 absolute position||`` oval block close to ``||fwdMotors:set servo1 50 %||`` replace ``||fwdMotors:50 %||`` of ``||fwdMotors:set servo1 50 %||`` block. 
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
Click ``||fwdSensors:Sensors||``. Drag ``||fwdSensors:dial1 absolute position||`` oval block close to ``||fwdMotors:set servo1 50 %||`` replace ``||fwdMotors:50 %||`` of ``||fwdMotors:set servo1 50 %||`` block. 
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
Click ``||fwdMotors:Motors||`` drag and drop ``||fwdMotors:set servo1 50 %||`` block inside ``||fwdSensors:on touch down||`` block.
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
Change speed of ``||fwdMotors:set servo1 50 %||`` block inside ``||fwdSensors:on touch down||``
to ``||0||``.
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
