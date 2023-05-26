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