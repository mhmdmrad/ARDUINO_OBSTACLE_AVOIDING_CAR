# IN PROGRESS...
# Obstacle Avoiding Robot

This is an **Arduino-based obstacle-avoiding robot** that uses an **HC-SR04 ultrasonic sensor** to detect obstacles and an **L298N motor driver** to control two DC motors. The robot automatically moves forward and changes direction when an obstacle is detected.

## Features:
- **Ultrasonic Sensing**: Uses an HC-SR04 sensor to measure the distance of obstacles.
- **Servo Rotation**: Rotates a servo motor to scan for clear paths.
- **Autonomous Movement**: Moves forward and avoids obstacles by turning left or right.
- **Motor Control**: Uses an L298N motor driver to control two DC motors.

## Components Used:
- **Arduino Uno**
- **HC-SR04 Ultrasonic Sensor**
- **L298N Motor Driver Module**
- **Two Geared DC Motors**
- **Servo Motor**
- **9V DC Power Supply**

## Wire Connections:

| Component | Pin | Arduino Pin |
|-----------|-----|-------------|
| HC-SR04 Ultrasonic Sensor | VCC | 5V |
| | GND | GND |
| | Trig | 9 |
| | Echo | 8 |
| Servo Motor | VCC | 5V |
| | GND | GND |
| | Signal | 10 |
| L298N Motor Driver | IN1 | 4 |
| | IN2 | 5 |
| | IN3 | 6 |
| | IN4 | 7 |
| | Motor Power | External 9V |
| | GND | GND |
| Left Motor | Output A | Connected to Motor |
| Right Motor | Output B | Connected to Motor |

## How It Works:
1. The ultrasonic sensor continuously scans for obstacles.
2. If the path is clear (>15 cm distance), the robot moves forward.
3. If an obstacle is detected (<10 cm), the robot stops, rotates the servo motor to scan the surroundings, and determines a new direction.
4. The robot moves backward slightly and turns left or right to avoid the obstacle.

## Code & Circuit Diagram:
Check out the Arduino code and Circuit Diagram in the repository for full implementation.

## Future Improvements:
- Adding **IR sensors** for better obstacle detection.
- Implementing **AI-based pathfinding** using a Raspberry Pi.
- Integrating **Bluetooth/WiFi control** for manual operation.
