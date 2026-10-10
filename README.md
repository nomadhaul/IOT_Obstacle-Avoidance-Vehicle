# Autonomous IoT Obstacle-Avoidance Rover

> A physical robotics platform engineered for autonomous navigation, relying on real-time environmental telemetry fusion and dynamic collision-avoidance algorithms.

---

https://github.com/user-attachments/assets/372f0058-75ac-49c3-bb85-40b49ae9d17f


---

## System Overview
This project serves as a hardware-in-the-loop autonomous vehicle. It continuously polls environmental data through a front-mounted sensor array and dynamically calculates pathfinding decisions. When physical objects breach predefined proximity thresholds, the rover's state machine executes evasive maneuvers (stop, reverse, pivot) without manual operator intervention.

## Hardware Architecture
* **Primary Controller:** [Insert Arduino Uno / Raspberry Pi / ESP32]
* **Motor Driver:** [Insert L298N Dual H-Bridge or specific driver]
* **Sensor Array:** HC-SR04 Ultrasonic Distance Sensor, [Insert Infrared Proximity Sensors if applicable]
* **Actuators:** [Insert 2-Wheel or 4-Wheel] DC Geared Motors

## Software Stack
* **Languages:** C++ (Primary MCU Logic), Python
* **Control Logic:** Interrupt-driven state machine, Pulse Width Modulation (PWM) speed regulation, distance threshold processing.
* **Libraries:** [Insert specific libraries, e.g., Wire.h, NewPing, RPi.GPIO]

## Autonomous Navigation Algorithm
* **Continuous Polling:** The HC-SR04 ultrasonic sensor emits high-frequency sound waves, calculating real-time distance based on the acoustic echo return time.
* **Dynamic Decision-Making:** If a forward obstacle is detected within the critical threshold (e.g., < 15 cm), the primary loop interrupts forward locomotion.
* **Evasive Maneuvers:** The motor driver instantly reverses polarity to brake, followed by a differential steering routine (rotating left or right) until the acoustic path is confirmed clear.

## Deployment & Setup

> **Note:** Requires exact GPIO/Pin configurations matching the embedded C++ script. Ensure the motor driver shares a common ground with the MCU.

1. Clone the repository:
   ```bash
   git clone [https://github.com/michaelmorelli/Autonomous-Rover.git](https://github.com/michaelmorelli/Autonomous-Rover.git)
