# Mini-project
## Smart Device Management System

#**Course:** Object Oriented Programming
#**Built by:** Fosuhene Fred
#**Class:** EL 1B
#**Lecturer:** Dr. Matthew Cobbinah
#**Assignment:** OOP Mini Project

##  Project Overview

This project simulates a **Smart Device Management System** used by a technology
company to manage smart home devices. Every device shares common information
(name, device ID, power status), but each device type also has its own unique
behavior. Sensitive attributes (device ID, power status) are **encapsulated**
and can only be changed through controlled methods, protecting the integrity
of the system.

The project was built base on the following OOP concepts:

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

##  Class Structure

### `SmartDevice` (Parent class)
- Private attributes: `__device_id`and `__power_status`
- Public attribute: `name`
- Methods: `turn_on()`, `turn_off()`, `display_info()`
- Encapsulation enforced through `@property` getters/setters
  (device ID can never be empty; power status can only be `True`/`False`)

### `SecurityCamera` (a child class inherits from `SmartDevice`)
- Additional attribute: `recording_status`
- Methods: `start_recording()`, `stop_recording()`

### `SmartLight` (another child class inherits from `SmartDevice`)
- Additional attribute: `brightness` (validated to stay between 0 and 100)
- Methods: `increase_brightness()`, `decrease_brightness()`

### `TemperatureSensor` (also another child class inherits from `SmartDevice`)
- Additional attribute: `temperature`
- Method: `read_temperature()`

All child classes use `super().__init__()` to properly initialize the
attributes inherited from `SmartDevice`.


 

smart-device-management-system/
│
├── smart_device_management_system.py  
└── README.md                         
```

