# NIARC 2017

## Rule

https://github.com/congthanh184/niarc-2017-software/blob/master/Documents/Task%20and%20Rules%20NI%20ARC%202017.pdf

## Mechanical design

![mechanical design](https://github.com/congthanh184/niarc-2017-software/blob/master/Documents/mechanical-design.png)

## Software

- `/NIARC-Simulation`: simulating NIARC competition map

![map](https://github.com/congthanh184/niarc-2017-software/blob/master/Documents/simulate_ni_map.PNG)

- `/myRIO-Library/StateVI`: all state machines implemented to control robot:
    - `FollowingWall.vi` : control robot to detect and run along the wall
        of the map.
    - `/Running VI`: implementing P controller to drive robot to goal
    - `/IMU VI`: to initialize and collect data from MPU-6050
    - `/StageVI`: to control robot based on where it is or which stage
        it is on the map
    - `/WaitVI`: state machine to wait for an action finishes
    - `State Controller Test.vi`: unit test for controllers
    - `TestFollowVI.vi`: unit test for following wall controller
- `/myRIO-Library/MotorControl`: PID controller for motors' speeds and
    feedback encoders' readings
- `/myRIO-Library/DistanceSensor`: functions to read infrared sensors
- `/myRIO-Library/DrivingVI`: functions to drive robot to goal pose while avoiding obstacles
- `/myRIO-Library/FilterVIs`: implementing median filter and test
- `/myRIO-Library/I2CdevLib`: port I2Cdev C/C++ to VI
- `/myRIO-Library/TestVI`: all the test units
- `/TwoWheelObject.vi`: mathematic model of the robot
