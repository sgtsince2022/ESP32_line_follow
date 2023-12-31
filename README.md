# Line Follow Robot with ESP32 (by SGT)

Welcome to the Line Follow Robot repository, where we've developed a simple line-following robot using an ESP32 microcontroller. This robot employs 5 infrared sensors to track lines on the ground. The core control algorithm leverages a PID controller, enabling the robot to follow lines with precision.

## Hardware Components

- **Microcontroller:** ESP32
- **Sensors:** 5 Infrared Sensors
- **Actuators:**
  - ZK-5AD Motor Driver
  - 2 N20 Motors

## Algorithm

The line-following algorithm is powered by a Proportional-Integral-Derivative (PID) controller. The PID controller dynamically adjusts motor PWM signals based on error calculations from sensor readings, thus ensuring the robot stays on its intended path.

## Development Environment

The code for this project was developed using PlatformIO on Visual Studio Code.

## Project Structure
```
ESP32_line_follow/
├── lib/
│   ├── ESP32_Motor_Controller/
│   │   ├── esp32_motor.h: Defines the class for controlling motors using the ESP32's LEDC module.
│   │   └── esp32_motor.cpp
│   ├── Line_status/
│   │   ├── line_status.h: Defines the class to manage infrared line sensor status.
│   │   └── line_status.cpp
│   └── PID_controller/
│       ├── PIDcontroller.h: Defines the class for the PID controller.
│       └── PIDcontroller.cpp
├── src/
│   ├── main.cpp: The main code that initializes motors, sensors, and PID controller.
│   └── main.h: Contains constants and configurations used throughout the project.
└── platformio.ini: Configuration file for PlatformIO.
```

## Folders Descriptions

### ESP32_Motor_Controller
This library encapsulates motor control for the ESP32 microcontroller. The `esp32_motor.h` header file defines the `esp32_motor` class, which provides methods for running, stopping, and configuring motors.

### Line_status
The `line_status` library manages the status of infrared line sensors. The `line_status.h` header file defines the `line_status` class, including methods for updating sensor status and calculating line position error.

### PID_controller
This library handles the PID controller. The `PIDcontroller.h` header file defines the `PIDcontroller` class, which calculates PID output based on error values.

## Code Components

### esp32_motor.h
This header file defines the `esp32_motor` class, allowing control of motors using the ESP32's LEDC module. It includes methods for running, stopping, and configuring motors.

### line_status.h
This header file defines the `line_status` class, used to manage infrared line sensor status. It provides methods to update sensor status and calculate the line position error.

### PIDcontroller.h
This header file defines the `PIDcontroller` class for the PID controller. It calculates the PID output based on error values.

## platformio.ini
The `platformio.ini` file configures the PlatformIO environment for the ESP32 project. It specifies the target board, platform, framework, and upload speed.

---

For more detailed explanations, please refer to the individual code files, headers, and comments within.
