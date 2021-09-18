# PowerProf Hardware Resources

PowerProf is a current monitor for embedded systems.

There are currently two PowerProf boards - the Teensy version and the Wemos D1 Mini version. The Teensy version supports communication over USB, while the Wemos D1 Mini supports USB and WiFi. Both boards use the [INA260 current sensor](https://www.ti.com/lit/ds/symlink/ina260.pdf) from Texas Instruments.

## Specifications

| Name                | Absolute         | Typical      |
| ------------------- | ---------------- | ------------ |
| Measurement Voltage | -0.3V - 40V      | 0 - 36V      |
| Measurement Current | 0 - 15A          | 0 - 10A      |
| Voltage Resolution  | 1.25mV           |              |
| Current Resolution  | 1.25mA           |              |
| Power Resolution    | 10mW             |              |
| Sample Rate         | 110Hz - 6.494kHz | 110Hz - 1kHz |
| Supply Voltage      | 5V               | 5V           |
| Supply Current      | 30-500mA         | 100mA        |

## Wiring Diagrams

![wiring diagram](./png/wiring-diagram.png)

## Teensy

The Teensy board is a carrier board which houses the microcontroller and the INA260 current sensor.

[Order this board from OSH Park](https://oshpark.com/shared_projects/RvujZ5At)

### Schematic

![teensy schematic](./png/teensy-schematic.png)

### Board

![teensy board](./png/teensy-board.png)

### BOM

| Mfg      | Name                | Qty | Buy                                                                                                           |
| -------- | ------------------- | --- | ------------------------------------------------------------------------------------------------------------- |
| PJRC     | Teensy 3.6          | 1   | [Link](https://www.pjrc.com/store/teensy36.html)                                                              |
| Adafruit | INA260 Breakout     | 1   | [Link](https://www.mouser.com/ProductDetail/Adafruit/4226?qs=PzGy0jfpSMvb8foRR1BpJA%3D%3D)                    |
| TE Conn. | 282834-2            | 1   | [Link](https://www.mouser.com/ProductDetail/TE-Connectivity/282834-2?qs=A%252Bip%252BNCYi6N8cVKuk8xDog%3D%3D) |
| DuPont   | 8-pin 2.54mm Header | 1   |                                                                                                               |

### Assembly

1. Solder the Teensy to the top of the board.
2. Solder the 8-pin header to the top of the board.
3. Solder the INA260 to the 8-pin header.
4. Solder the terminal block to the top of the board.

## Wemos D1 Mini

The D1 Mini board is a "shield" which houses the INA260 current sensor and is installed on top of the D1 Mini.

[Order this board from OSH Park](https://oshpark.com/shared_projects/EueeZyrV)

### Schematic

![d1 mini schematic](./png/d1-mini-schematic.png)

### Board

![d1 mini board](./png/d1-mini-board.png)

### BOM

| Mfg      | Name                            | Qty | Buy                                                                                        |
| -------- | ------------------------------- | --- | ------------------------------------------------------------------------------------------ |
| Wemos    | D1 Mini                         | 1   | [Link](https://www.wemos.cc/en/latest/d1/d1_mini.html)                                     |
| Adafruit | INA260 Breakout                 | 1   | [Link](https://www.mouser.com/ProductDetail/Adafruit/4226?qs=PzGy0jfpSMvb8foRR1BpJA%3D%3D) |
| DuPont   | 8-pin 2.54mm Header             | 2   |                                                                                            |
| DuPont   | 6-pin 2.54mm Header             | 1   |                                                                                            |
| DuPont   | 2-pin Right Angle 2.54mm Header | 1   |                                                                                            |

### Assembly

1. Solder the two 8-pin headers on the bottom of the board.
2. Solder the 6-pin header on the top of the board.
3. Solder the 2-pin right angle header on the top of the board.
4. Solder the INA260 to the 6-pin header - make sure that pins 7/8 of the INA260 breakout are not connected!
5. Install the shield on top of a D1 Mini.

## Roadmap

Some things we'd like to add, given the time:

- An ESP32-based board with Bluetooth communication
- Direct integration of the INA260 (obviating the Adafruit breakout board)
- One modular connector for the front-end instead of four separate wires

## Acknowledgements

Special thanks to [weeding-nerdy](https://github.com/weeding-nerdy) for their [gufu_gud](https://github.com/weeding-nerdy/gufu_gud), which was the inspiration for this project.
