[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

# SX1255
Minimalistic evaluation board for the SX1255 RF transceiver chip, with PMOD connectors.

<img src="https://github.com/M17-Project/SX1255/blob/main/front.png" width="450">

## Clocking
Remember to provide a clock signal at the PMOD *REF* pin or *EXT_REF* SMA connector. The source is selectable with a jumper.
A range of clock frequencies can be used, see the SX1255's documentation for details.

## Raspberry Pi GPIO header connections
| PMOD pin name       | RPi header pin number |
|---------------------|-----------------------|
| **VCC**             | **1** (*3.3V*)        |
| **OUT**             | **12** (*GPIO18*)     |
| **MOSI**            | **19** (*SPI_MOSI*)   |
| **MISO**            | **21** (*SPI_MISO*)   |
| **RST**             | **22** (*GPIO25*)     |
| **SCK**             | **23** (*SPI_CLK*)    |
| **/CS**             | **24** (*SPI_CE0_N*)  |
| **IO2**             | **35** (*GPIO19*)     |
| **I_OUT**           | **38** (*GPIO20*)     |
| **GND**             | **39** (*GND*)        |
| **I_IN**            | **40** (*GPIO21*)     |

Sample Raspberry Pi code for SX1255 control can be found [here](https://gist.github.com/sp5wwp/25fa989ebd98b3b707eadae9b63af679).
[I2S slave overlay](https://github.com/AkiyukiOkayasu/RaspberryPi_I2S_Slave) is required.

## License
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
