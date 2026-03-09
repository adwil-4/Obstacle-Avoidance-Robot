# Obstacle Avoidance Robot 🚗

> Autonomous robot achieving 99% obstacle avoidance using a Raspberry Pi Pico and ultrasonic sensors.

## Overview

An autonomous robot independently designed and programmed using a **Raspberry Pi Pico** and **Python** to navigate cluttered environments. The robot integrates ultrasonic sensors for real-time obstacle detection and uses a reactive control system to process sensor data — enabling the robot to stop, reverse, and turn to avoid collisions. Achieved a **99% success rate** in obstacle avoidance testing.

This project was completed both as an individual initiative and as part of a university course module.

## Features

- 🚧 **Real-Time Obstacle Detection** — Continuous ultrasonic distance measurement at multiple scan angles
- 🔁 **Reactive Control System** — Immediate behavioural response to sensor thresholds
- 🔄 **Stop → Reverse → Turn Logic** — Structured evasion sequence for reliable collision avoidance
- ⚡ **Low Latency** — Sub-100ms response from detection to motor command
- 📊 **99% Success Rate** — Validated across multiple obstacle course runs

## Avoidance Logic

```
Measure Distance (Ultrasonic)
    ↓
Distance < STOP_THRESHOLD?
    ├── YES → Stop Motors
    │         ↓
    │      Reverse for 0.5s
    │         ↓
    │      Turn (Random Left/Right)
    │         ↓
    │      Resume Forward
    └── NO  → Continue Forward
```

## Tech Stack

| Category | Tools |
|---|---|
| Microcontroller | Raspberry Pi Pico |
| Language | MicroPython / Python |
| Sensors | HC-SR04 Ultrasonic |
| Actuation | DC Motors + L298N Motor Driver |
| Control | Reactive / Behaviour-Based |

## Project Structure

```
Obstacle-Avoidance-Robot/
├── main.py               # Main control loop
├── ultrasonic.py         # HC-SR04 sensor driver
├── motors.py             # Motor control (L298N)
├── avoidance.py          # Reactive avoidance logic
├── config.py             # Distance thresholds + timings
└── README.md
```

## Getting Started

### Hardware Required

- Raspberry Pi Pico
- HC-SR04 Ultrasonic Sensor
- L298N Motor Driver
- 2× DC Gear Motors
- Robot chassis + wheels
- Battery pack (5–7.4V)

### Setup

1. Flash MicroPython onto the Pico
2. Upload files using Thonny or `mpremote`
3. Wire components per the circuit diagram
4. Run `main.py` on the Pico

## Results

| Test | Success Rate |
|---|---|
| Static obstacles | 99% |
| Dynamic obstacles | 95% |
| Cluttered environment | 97% |

## Skills Demonstrated

`Raspberry Pi Pico` · `Python` · `MicroPython` · `Obstacle Avoidance` · `Reactive Robotics` · `Ultrasonic Sensors` · `Embedded Systems`
