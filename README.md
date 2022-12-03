# Operame

SecurAir is based on the source code of [ControlCO2-meter](https://controlco2.space), which is based on the original project [operame](https://operame.nl/Operame) launched by RevSpace.

SecuraAir was handed out as a free Christmas Gift (not for profit) December 2022 by [Secura](https://www.secura.com)

## Language

The default language is set to English; users can pick a different language using the
WiFi configuration portal. To change the default setting to Dutch, change
`#define LANGUAGE "en"` to `#define LANGUAGE "nl"`.

## Usage

Once the device is soldered and the software is uploaded, the device should work stand alone.
Please allow a couple of days to callibrate the sensor and make sure it is in a room with fresh air (so longer times without people). The sensor will automatically calibrate to the lowest value being 400.

The sensor is very sensitive to power fluctuations.  So please use the same powersupply (e.g. USB charger). If you change from one charger to the other (or to a USB port on your computer or Power Bank), it might need some callibration days again.

Please note that for convenience, we chose a "solder through" PCB. This means that the pins are exposed on the back side of the PCB. Don't place the PCB on a conducting surface (e.g. metal surface) while in use!

### Installation

This repository uses [PlatformIO](https://platformio.org/) for the installation on the TTGO Display.

1. Install PlatformIO.
2. Clone this repository.
3. In you command line or terminal, go to the cloned repository and run `pio run`.

## Tips

If the SecurAir board isn't detected by Windows, you could install the cp210x USB TO UART drivers by silicon labs.
https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers
  
## Windows 10 users  
-Windows 10 System

-Install visual studio code installeren

-Install PlatformIO extension in VSCode.

-Install python 3.11 and make sure the option to add to the PATH is selected!

-Install GIT to be able to clone the repository

-Connect the SecurAir board via USB and check if a COM port (e.g. COM 9) apears in the device manager. Otherwise, please install the drivers mentioned above.

-In the SecurAir folder, execute `pio run`.

## 4MB or 16MB

board = esp32thing
board_build.partitions = default.csv

If you have a 16MB TTGO T-Display board, you can change the env settings in the platformio.ini file.
board = esp32thing_plus
board_build.partitions = default_16MB.csv

## Support

If you have challenges soldering the device or installing the software, feel free to reach out to:

-Pieter (EHV)

-Luigi (AMS)

-Sjoerd (AMS)
