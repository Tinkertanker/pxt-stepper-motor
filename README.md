# pxt-28byj-48-stepper

This extension also requires a driver board of some sort. I use the ULN2003. It works. 
Find out more about the 28byj-48 and ULN2003 driver here: 
https://www.seeedstudio.com/blog/2019/03/04/driving-a-28byj-48-stepper-motor-with-a-uln2003-driver-board-and-arduino/

## Basic Usage

`||set motor to motor at in1/in2/in3/in4||`
Create a motor and specify the 4 input pins connecting it to the micro:bit.

`||move motor 0 steps clockwise||`
`||move motor 0 steps anti-clockwise||`
Use move motor clockwise or anti-clockwise to rotate the motor. Change the number of steps or rotations as desired.

`||motor set delay between steps to 0 ms||`
Change the speed of rotation by increasing or decreasing the delay between steps.

## Example: Using moving anti-clockwise on button press A and clockwise on button press B

Use this program to get your stepper motor moving! Make sure your stepper motor is connected to pins P0, P1, P2 and P3 in that order. 

```
input.onButtonPressed(Button.A, function () {
    motor.moveAntiClockwise(0.5, stepUnit.Rotations)
})
input.onButtonPressed(Button.B, function () {
    motor.moveClockwise(0.5, stepUnit.Rotations)
})

let motor = stepperMotor.createMotor(
    DigitalPin.P0,
    DigitalPin.P1,
    DigitalPin.P2,  
    DigitalPin.P3
)
```

## Supported targets

* for PXT/microbit

## License
MIT

## Code of Conduct
This project has adopted the Microsoft Open Source Code of Conduct. For more information see the Code of Conduct FAQ or contact opencode@microsoft.com with any additional questions or comments.
