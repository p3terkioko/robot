# robot
# Bluetooth-Controlled Robot with Dual L293D Motor Drivers

This project allows you to control a 4-wheel robot using an HC-05 Bluetooth module and the Dabble app. The robot uses two L293D motor drivers to control front and back motors independently.

## Components

- Arduino Uno
- HC-05 Bluetooth Module
- Two L293D Motor Drivers
- Four Motors (DC Motors with red and black wires)
- Power Supply (6V)
- Jumper Wires

## Connections

### Motors and Motor Drivers (L293D)

#### Front Motors
Connect the output pins of the first L293D motor driver to the front motors as follows:
- **Front Left Motor**: Connect to L293D #1 Pins 3 and 6.
- **Front Right Motor**: Connect to L293D #1 Pins 11 and 14.

#### Back Motors
Connect the output pins of the second L293D motor driver to the back motors as follows:
- **Back Left Motor**: Connect to L293D #2 Pins 3 and 6.
- **Back Right Motor**: Connect to L293D #2 Pins 11 and 14.

### Arduino to L293D Connections

#### First L293D Motor Driver (Front Motors)
- IN1 (Pin 2) to Arduino Pin 4
- IN2 (Pin 7) to Arduino Pin 5
- IN3 (Pin 10) to Arduino Pin 6
- IN4 (Pin 15) to Arduino Pin 7
- Enable Pin 1 (Pin 1) to Arduino Pin 10
- Enable Pin 9 (Pin 9) to Arduino Pin 11

#### Second L293D Motor Driver (Back Motors)
- IN1 (Pin 2) to Arduino Pin 8
- IN2 (Pin 7) to Arduino Pin 9
- IN3 (Pin 10) to Arduino Pin 12
- IN4 (Pin 15) to Arduino Pin 13
- Enable Pin 1 (Pin 1) to Arduino Pin A0
- Enable Pin 9 (Pin 9) to Arduino Pin A1

### Power
- Connect both L293D motor drivers’ VCC pins to the 6V power supply.
- Connect all GND pins on both L293D ICs and the Arduino GND.

### HC-05 Bluetooth Module
- **VCC**: Connect to Arduino 5V
- **GND**: Connect to Arduino GND
- **TX**: Connect to Arduino Pin 2
- **RX**: Connect to Arduino Pin 3 (use a voltage divider for RX if necessary to protect the HC-05).

## Software

1. Upload the Arduino code (provided in this repository) to control the robot movements using the Dabble app.
2. Pair your phone with the HC-05 module.
3. Open the Dabble app and select the Gamepad mode to control the robot.

## Control Commands
- **F**: Forward
- **B**: Backward
- **L**: Turn Left
- **R**: Turn Right
- **S**: Stop

Ensure all connections are secure before powering up your robot.

---

### Troubleshooting
- **One Wheel Not Moving**: Check if the power supply is sufficient and if all connections to the motor drivers are correct.
- **Bluetooth Connectivity Issues**: Ensure the HC-05 module is properly paired with your phone and that the Dabble app is connected.

