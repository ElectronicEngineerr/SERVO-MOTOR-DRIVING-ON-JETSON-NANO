# SERVO-MOTOR-DRIVING-ON-JETSON-NANO

Those who will rotate the servo motor for the first time in the jetson nano have generally rotated the arduino at least once.

We can take the analog signal on the arduino and have it calibrated by proportioning the angles with the map command...

But in Jetson nano this is not so easy, because Jetson nano does not have any analog input/output pins to read the analog signals of the sermo motor. There are two steps to solve this problem. But today we will perform the second step.

1) With Analog Digital Converter, you can convert and interpret analog signals by converting them to digital signals and rotate the servo motor.

2) We will convert analog signals to 'PWM' signals with the Pca9685 Servo Motor driver board. We will make the motor rotate by interpreting the pwm signals in Jetson nano.

# Let's rotate servo on jetson nano with pca9685 servo motor driver...

- First we have to start with the necessary installations.

1) We need a few libraries as we will write our codes in Jetson Nano using python 3x. some of them come while installing sdk manager on jetson nano, but some of them we have to download manually from the terminal. Most importantly, the versions of the libraries we will download must be compatible with the python3x version. Otherwise, you will get an error on the poles before you even start coding.

 I have a repository where I describe the versions in more detail:

" https://github.com/ElectronicEngineerr/DC-Motor-Driving-with-Jetson-Nano-"

2) Let's start by downloading pip3 first;

`sudo apt get install python3-pip`

3) We must get the necessary permits to drive the servo motors;

`sudo usermod -aG i2c 'your_username`

- `sudo usermod -a -G gpio`

- `sudo usermod -a -G gpio your_username`

✓ Please do not forget to enter the username you gave to jetson nano where your_ username is.

✓ you won't get any printouts, for your information

4) Let's put the necessary tools file for the library to work into the terminal

`pip3 install -- setuptools upgrade`

5) Finally, we will manually install the necessary and most important library, servokit, from the terminal.

`sudo pip3 install adafruit-circuitpython-servokit==1.3.0`

6 Now let's make the connections of the servo motor...

-
