# 2026 RDC Controller

**Hardware/PCB** by:
- Hedy (Intelligent Racing)
- Kingslie (Intelligent Racing)

**Software** by:
- Kenyu (Intelligent Racing)

_A custom controller designed for the 2026 Robot Design Contest for HKUST
Robotics Team recruitment._

## Features

- 2 Joysticks with their own buttons
- Backup ADCs (activate by soldering `0R`)
- 8 Normal buttons
- 2 Limit switches
- Plug-and-play blue pill
- Plug-and-play HC-05
- Power with a single 18650 battery
- Battery protection and reverse indicators
- Plug-and-play 1.8' TFT
- On-board charging with USB-C and battery level indicators

## Integration

The controller PCB was essential in supporting the following software tutorials
in 2026:
- **Tutorial 1**: Basic IO, GPIO, TFT -- _taught by Hedy (IR)_
  - Controller features covered: debug LEDs, the bluepill, buttons, limit
  switches, TFT
- **Tutorial 2**: UART and Bluetooth -- _taught by Kenyu (IR)_
  - Controller features covered: UART, HC-05
- **Advanced Tutorial 1**: ADC, GPIO timing & I2C -- _taught by Tom (IR) and Tony (IR)_
  - Controller features covered: Joysticks (ADC)

An additional user manual was provided in the **additional-notes** folder in the
Software Tutorial repository for supplementary information on the usage and
further tips with working with the controller.

This repo provides the hardware schematic and the basic IOC file for reference,
and some additional resources for working with the hardware.

## Hardware design principles

The PCB was designed with a few principles in mind. The point of this
controller is to replace the MIT App Inventor which we use every year for RDC.
It was decided that allowing trainees to get more hands-on experience with STM
embedded programming with a physical, custom controller is much more rewarding
-- not just for aesthetics but also for the purpose of training embedded
development.

The controller should be able to offer all controls required by any current or
future RDC game rule, and should "just work" after relative simple embedded
programming, allowing trainees to focus more on the rest of the robot.

The design shouldn't be opinionated in that the placement of components and
ergonomics should be sensible and generic. Trainees should still be allowed to
roll their own solutions for the controller, but this controller should act as
a "common denominator" -- if you want to use the official controller, it should
be stable and fit most people's needs.

## Caveats & future considerations

- Reusing STM blue pill's USB for charging
