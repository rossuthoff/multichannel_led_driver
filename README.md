[![DOI](https://zenodo.org/badge/131809134.svg)](https://zenodo.org/badge/latestdoi/131809134)

# multichannel_led_driver
Switching boost LED driver based on the Linear Technology [LT3478-1](http://www.analog.com/en/products/power-management/led-driver-ic/buck-boost-led-drivers/lt3478.html) chip.

## related repositories
This design requires the footprints found in the [kicad_footprints](https://github.com/rossuthoff/kicad_footprints) repository. Make sure the library and .mod files are added to your folder search locations. This board utilizes the [ytai/IOIO](https://github.com/ytai/ioio) microcontroller (MCU) and is designed to match to its header layout. Other microcontrollers that can send 3.3 V signals and control an I2C interface may be used. 

## general use
### power supply
LED driver is used in boost mode. The battery voltage must be less than the voltage drop across each individual LED string. Header connnection between this board and the IOIO board provide power to the MCU.

### led strings
Connect the LED strings to V+ (anode) and V1 through V9 (cathodes) connections. The LED string to be illuminated is controlled through a 3.3V signal to the s1 through s9 pins. The applied current is controlled through a Analog Devices [AD5247](http://www.analog.com/en/products/digital-to-analog-converters/digital-potentiometers/ad5247.html) digital potentiometer with an I2C interface.

# references


