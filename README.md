

# SkySweeper Rover Vacuum

### Wildfire Prevention | Robotics | Embedded Systems | Autonomous Navigation

**SkySweeper** is an autonomous robotic rooftop cleaning system designed to reduce wildfire-related property damage by removing combustible debris, such as dry leaves, pine needles, and twigs, from rooftops.

Accumulated rooftop debris poses a significant fire hazard in wildfire-prone regions across North America. During wildfires, windborne embers can ignite dry vegetation and other combustible materials collected on roofs and in gutters, potentially spreading fire to residential structures.

SkySweeper addresses this challenge through an automated rooftop cleaning solution that combines **robotic navigation, ultrasonic sensing, omnidirectional movement, and embedded motor control** to support safer, more efficient debris removal.

Developed as part of **ESC204: Praxis III at the University of Toronto (January 2025 - April 2025)**, the project explores how autonomous robotics can contribute to **wildfire risk mitigation, preventative property maintenance, and environmental safety**.

## Problem Statement

Wildfires pose a growing threat to communities across North America, causing extensive property damage, environmental destruction, and risks to human safety.

While wildfire prevention often focuses on vegetation management and defensible space around homes, rooftops remain a critical area of vulnerability.

Combustible debris, including leaves, pine needles, and twigs, can accumulate on rooftops and in gutters. When exposed to windborne embers, these materials can ignite and increase the likelihood of a structure catching fire.

Traditional rooftop cleaning methods also present challenges:

- **Safety Risks:** Manual rooftop maintenance exposes homeowners and workers to falls and other hazards.
- **Limited Accessibility:** Steep or elevated roofs can be difficult to clean safely.
- **Recurring Maintenance:** Debris accumulates over time, requiring repeated cleaning.
- **Labour-Intensive Processes:** Manual removal can be time-consuming and costly.

## Proposed Solution

SkySweeper is a robotic rooftop cleaning prototype designed to support preventative wildfire mitigation through automated debris removal.

The system integrates:

- **Omnidirectional robotic movement** to navigate and reposition across rooftop surfaces.
- **Ultrasonic distance sensing** to support environmental awareness and obstacle detection.
- **Python-based motor control** to coordinate movement, speed, and direction.
- **Servo-driven mechanical components** to support the cleaning mechanism.
- **Embedded control software** to integrate sensing, movement, and actuation.
- **Iterative hardware testing** to improve system responsiveness and reliability.

By exploring robotic automation for rooftop maintenance, SkySweeper aims to reduce the need for hazardous manual cleaning while addressing a preventable source of structural wildfire vulnerability.

## Project Objectives

1. **Wildfire Risk Reduction:** Develop a robotic solution for removing combustible rooftop debris.
2. **Safer Maintenance:** Reduce the need for people to perform potentially hazardous rooftop cleaning tasks.
3. **Autonomous Navigation:** Explore sensor-driven movement and obstacle awareness for rooftop environments.
4. **Integrated Robotics:** Combine mechanical systems, sensors, and embedded software into a functional prototype.
5. **Efficient Cleaning:** Investigate methods for improving the consistency and efficiency of rooftop debris removal.


## Key Features

### 1. Robotic Movement & Navigation

- Implemented Python-based control logic for robotic movement.
- Developed motor-driving functions supporting forward, backward, and lateral movement.
- Integrated pulse-width modulation (PWM) to regulate motor speed.
- Explored omnidirectional wheel control for multidirectional mobility.
- Implemented input filtering to smooth control signals.

### 2. Ultrasonic Sensor Integration

- Integrated ultrasonic distance sensors for environmental sensing.
- Developed distance measurement and calibration routines.
- Used multiple sensor readings to improve measurement stability.
- Implemented error handling for invalid or failed distance measurements.
- Supported sensor-driven responses to surrounding objects.

### 3. Motor & Actuator Control

- Implemented GPIO-based DC motor control for speed and direction.
- Developed servo control routines for mechanical movement.
- Coordinated motor operation through embedded Python scripts.
- Tested individual actuators before combining hardware subsystems.

### 4. Hardware-Software Integration

- Combined sensing, movement, and actuation within an integrated control program.
- Used embedded development libraries for hardware communication.
- Developed and tested functionality across individual modules.
- Refined system behavior through iterative debugging and physical testing.

## Technology Stack

| Technology | Application |
|------------|-------------|
| Python | Robotics programming and control logic |
| CircuitPython | Microcontroller programming |
| Raspberry Pi / GPIO | Hardware interfacing and motor control |
| PWM | Motor speed and servo positioning |
| Ultrasonic Sensors | Distance measurement and environmental sensing |
| DC Motors | Robotic locomotion |
| Servo Motors | Mechanical actuation |
| Serial Communication | Input and control signal processing |
| Git & GitHub | Version control and collaborative development |

## System Architecture

SkySweeper consists of three primary layers: sensing, control, and actuation.

```text
              SkySweeper Rover
                     |
          +----------+----------+
          |                     |
          v                     v
    Sensor Inputs          Control Inputs
          |                     |
    Ultrasonic Sensor      Buttons / Receiver
          |                     |
          +----------+----------+
                     |
                     v
             Embedded Python
               Control Logic
                     |
          +----------+----------+
          |                     |
          v                     v
     Motion Control       Actuator Control
          |                     |
    DC Motor Drivers        Servo Motor
          |                     |
          v                     v
    Omnidirectional        Mechanical Arm
        Wheels
```

The integrated system uses hardware inputs to coordinate motor operation and mechanical behavior.

## Repository Structure

```text
SkySweeper/
│
├── integrated.py       # Integrated sensor, motor, and servo control
├── omniwheels.py       # Omnidirectional drive and receiver input
├── wheelcontrol.py     # GPIO motor speed and direction control
├── arm.py              # Robotic arm and servo control
├── armtest.py          # Arm subsystem testing
├── servomotor.py       # Servo motor functionality
├── dc.py               # DC motor testing and control
├── ultrasonic.py       # Ultrasonic distance sensing
├── ultrasonic2.py      # Sensor calibration and measurement filtering
├── movementtest.py     # Movement experimentation
├── rotationtest.py     # Rotation behavior testing
├── test.py             # Additional hardware tests
└── README.md           # Project documentation
```

## Software Implementation

### Motor Control

The motor control system uses PWM signals and GPIO outputs to regulate wheel movement.

The implementation supports:
- Forward and reverse motor direction.
- Variable-speed movement.
- Coordinated operation of multiple motors.
- Movement testing across different directions.

Relevant files:
- [`wheelcontrol.py`](wheelcontrol.py)
- [`omniwheels.py`](omniwheels.py)

### Sensor Processing

Ultrasonic sensors provide distance measurements used for environmental awareness.

The code includes:
- Distance calibration.
- Repeated sampling.
- Invalid-reading filtering.
- Error handling.
- Measurement averaging.

Relevant files:
- [`ultrasonic.py`](ultrasonic.py)
- [`ultrasonic2.py`](ultrasonic2.py)

### Integrated Control

The integrated program coordinates several robotic subsystems, including sensor readings, DC motor operations, and servo positioning.

Relevant file:
- [`integrated.py`](integrated.py)

## Testing & Development

SkySweeper was developed through iterative hardware testing and software refinement.

Development activities included:

1. **Component Testing:** Testing individual motors, servos, sensors, and control circuits.
2. **Movement Validation:** Evaluating motor direction, movement, and rotation.
3. **Sensor Calibration:** Refining ultrasonic measurement accuracy and reliability.
4. **Subsystem Integration:** Combining sensing and actuation into shared control logic.
5. **Debugging & Optimization:** Identifying hardware and software issues through repeated testing.

The repository includes dedicated experimental scripts documenting this development process.

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/RishikaSinghal/SkySweeper.git
cd SkySweeper
```

### 2. Prepare Hardware

This project was developed for physical robotic hardware and is not intended to run as a standalone desktop application.

Execution requires compatible microcontroller or Raspberry Pi hardware, appropriate motor drivers, sensors, wiring, and the corresponding Python libraries.

### 3. Explore the Control Modules

Start by reviewing the individual subsystem files:

- `wheelcontrol.py` — motor movement
- `omniwheels.py` — omnidirectional control
- `ultrasonic2.py` — distance measurement
- `arm.py` — servo and arm control

### 4. Integrated Program

The primary integration script is:

`integrated.py`

**Note:** Review GPIO pin mappings and connected hardware before execution. Some scripts target different hardware environments, and the repository includes experimental code that may require adjustments for a particular setup.

## Engineering Challenges

SkySweeper provided hands-on experience with several practical robotics challenges:

- Coordinating multiple motors with independent speed and direction controls.
- Processing noisy sensor data to support reliable environmental sensing.
- Integrating mechanical components with electronic control systems.
- Debugging hardware-software interactions.
- Developing and evaluating control logic on physical hardware.
- Balancing functionality, responsiveness, and reliability.

## Future Improvements

Potential extensions include:

- More advanced autonomous obstacle avoidance.
- Improved motion planning and navigation.
- Computer vision for enhanced environmental perception.
- Sensor fusion for more reliable localization.
- Automated path optimization for cleaning coverage.
- Improved monitoring and visualization of sensor and motor data.

## Acknowledgements

Developed as part of **ESC204: Praxis III, University of Toronto**, through collaborative robotics engineering and software development.

This repository preserves the original project development history and contributions.

Original collaborative repository:
[aria-yang/SkySweeper](https://github.com/aria-yang/SkySweeper)

