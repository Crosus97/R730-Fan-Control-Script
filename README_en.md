# Dell PowerEdge R730 Family Fan Control Script

## Description

This Bash script automatically adjusts the fan speeds of Dell PowerEdge R730 family servers based on ambient and processor temperatures. The goal is to reduce server noise while ensuring temperatures remain at safe levels.

## Features

- **Automatic fan control**: Adjusts fan speed based on ambient temperature.
- **Processor temperature priority**: Activates automatic fan mode if any processor reaches a critical temperature, regardless of ambient temperature.
- **Temperature ranges and fan speeds**:
  - 0 to 14 degrees: 20%
  - 15 to 19 degrees: 40%
  - 20 to 26 degrees: 60%
  - 27 to 30 degrees: 80%
  - Above 30 degrees: Activates automatic mode

## Requirements

- Dell PowerEdge R730 family server
- Linux operating system (Tested and works perfectly on Proxmox)
- `ipmitool` installed

## Installation

Install `ipmitool` on your system:

```sh
sudo apt-get install ipmitool
