# PowerProf Hardware Resources

PowerProf is a current monitor for embedded systems.

There are currently two PowerProf boards - the Teensy version and the Wemos D1 Mini version. The Teensy version supports communication over USB, while the Wemos D1 Mini supports USB and WiFi.

## Wiring Diagrams

![wiring diagram](./png/wiring-diagram.png)

## Teensy

The Teensy board is a carrier board which houses the microcontroller and the INA260 current sensor.

### Schematic

![teensy schematic](./png/teensy-schematic.png)

### Board

![teensy board](./png/teensy-board.png)

### BOM

| Mfg      | Name            | Qty | Buy                                                                                                           |
| -------- | --------------- | --- | ------------------------------------------------------------------------------------------------------------- |
| PJRC     | Teensy 3.6      | 1   | [Link](https://www.pjrc.com/store/teensy36.html)                                                              |
| Adafruit | INA260 Breakout | 1   | [Link](https://www.mouser.com/ProductDetail/Adafruit/4226?qs=PzGy0jfpSMvb8foRR1BpJA%3D%3D)                    |
| TE Conn. | 282834-2        | 1   | [Link](https://www.mouser.com/ProductDetail/TE-Connectivity/282834-2?qs=A%252Bip%252BNCYi6N8cVKuk8xDog%3D%3D) |

## Wemos D1 Mini

The D1 Mini board is a "shield" which houses the INA260 current sensor and is installed on top of the D1 Mini.

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
