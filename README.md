# Control of the SG-Ready interface based on Tibber prices
The json file contains the NodeRed flow to extract the Tibber energy prices on an hourerly basis via the Tibber API. Based on the Tibber price level, the script triggers twi Shelly switches to set the 4 possible smart grid stages according to the SG-Ready specification.
The Shellys are connected to the EVU-Blocking contact and the SG-Ready contact of your heatpump.
Note: your heatpump must be SG-Ready certified. Please check the documentation of your heatpump.

Supported SG Ready Modes:
Mode 1, Tibber Pricing “Very Expensive”:
Heatpump locked for max 2 hours and max 2 times per day.
Mode 2, Tibber Pricing “Normal oder Expensive”:
Normal operation of the heatpump
Mode 3 , Tibber Pricing “Cheap”:
Start recommendation sent to heatpump for warmwater or heating according to the heatpump SG-Ready settings.
Mode 4, Tibber Pricing “Very Cheap”:
Forced start of the heatpump according to the EVU and SG_ready settings of your heatpump.

Prerequisites:
- 2 Shelly devices
- iobroker or other home automation server installed 
- NodRed installed
