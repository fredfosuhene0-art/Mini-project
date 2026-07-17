# Mini-project
## Smart Device Management System

**Course:** EL 162 / 234 – Object Oriented Programming
**Lecturer:** Dr. Matthew Cobbinah
**Assignment:** OOP Mini Project

## 📌 Project Overview

This project simulates a **Smart Device Management System** used by a technology
company to manage smart home devices. Every device shares common information
(name, device ID, power status), but each device type also has its own unique
behavior. Sensitive attributes (device ID, power status) are **encapsulated**
and can only be changed through controlled methods, protecting the integrity
of the system.

The project was built to demonstrate the following OOP concepts:

- Variables and data types
- Input and output
- Conditional statements and loops
- Functions
- Classes and objects
- Constructors (`__init__`) and `super()`
- Methods
- Inheritance
- Encapsulation
- Getters and setters (`@property`)

## 🏗️ Class Structure

### `SmartDevice` (Parent class)
- Private attributes: `__device_id`, `__power_status`
- Public attribute: `name`
- Methods: `turn_on()`, `turn_off()`, `display_info()`
- Encapsulation enforced through `@property` getters/setters
  (device ID can never be empty; power status can only be `True`/`False`)

### `SecurityCamera` (inherits from `SmartDevice`)
- Additional attribute: `recording_status`
- Methods: `start_recording()`, `stop_recording()`

### `SmartLight` (inherits from `SmartDevice`)
- Additional attribute: `brightness` (validated to stay between 0 and 100)
- Methods: `increase_brightness()`, `decrease_brightness()`

### `TemperatureSensor` (inherits from `SmartDevice`)
- Additional attribute: `temperature`
- Method: `read_temperature()`

All child classes use `super().__init__()` to properly initialize the
attributes inherited from `SmartDevice`.

## ▶️ How to Run the Program

1. Make sure you have **Python 3** installed on your computer.
2. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/smart-device-management-system.git
   cd smart-device-management-system
   ```
3. Run the program:
   ```bash
   python3 smart_device_management_system.py
   ```
4. The program will:
   - First automatically demonstrate all devices and their methods.
   - Then present an interactive menu:
     ```
     1. Display Device Information
     2. Turn Device On
     3. Turn Device Off
     4. Read Temperature
     5. Adjust Brightness
     6. Start Recording
     7. Exit
     ```
   - Follow the on-screen prompts to interact with the Security Camera,
     Smart Light, and Temperature Sensor.

## 📁 File Structure

```
smart-device-management-system/
│
├── smart_device_management_system.py   # Main program (all classes + menu)
└── README.md                           # Project documentation
```

## ✅ Author's Note

This project was completed as part of the OOP Mini Project assignment,
demonstrating inheritance, encapsulation, constructors with `super()`,
and a fully functional menu-driven interface.
