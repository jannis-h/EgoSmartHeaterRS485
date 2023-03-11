# EgoSmartHeaterRS485

[![license](https://img.shields.io/github/license/th-hock/EgoSmartHeaterRS485.svg)][license]

[license]:          LICENSE

## Overview

Library for controlling E.G.O. RS485 Smart Heaters.

Description from users manual:  
The EGO Smart Heater is a screwin heater controlled by a communication interface to heat up water and aqueous solutions (e.g. hot water storage).
The EGO Smart Heater is suitable to optimise the own power consumption by converting electrical energy, for example from the photovoltaic system, into thermal energy.
The power of the EGO Smart Heater can be adjusted within the range 0W to 3500W in 500W steps.

## Features

Please refer to the [Assembly und User manual](https://github.com/th-hock/EgoSmartHeaterRS485/blob/main/extras/smart_heater.pdf).  
The [protocol description](https://github.com/th-hock/EgoSmartHeaterRS485/blob/main/extras/Protocol%2090.60034.744_001_1.pdf) document contains a description of all the registers.  
Some important functions:
- setPowerNominalValue: Activate the heater in manual mode, to switch ich to a specific power consumption.
- setHomeTotalPower: Activate the heater in automatic mode. Provide the current metering value of a two-way meter. Negative values will cause the heater to be turned on.
- getRelaisStatus: Get current power consumption. Multiply the Relais-Status value by 500 to get the current power consumption of the heater.

Renew the activation at least every 60 seconds. Otherwise the heater is automatically turned off.

## Installation

### Manual

Refer to Arduino Tutorials > Libraries [Manual Installation](https://www.arduino.cc/en/Guide/Libraries#toc5).


## Hardware

This library has been tested with an Arduino [NodeMCU ESP8266](https://components101.com/development-boards/nodemcu-esp8266-pinout-features-and-datasheet) controller, connected via RS485 using a MAX485 [MAX485](https://microcontrollerslab.com/rs485-serial-communication-esp32-esp8266-tutorial/) transceiver.


## Example

The library contains a sketche that demonstrate use of the library. You can find these in the [examples](https://github.com/th-hock/EgoSmartHeaterRS485/tree/main/examples/) folder.


## Documentation

The library is documented by a <a href="https://github.com/th-hock/EgoSmartHeaterRS485/blob/main/doc/html/index.html" target="_blank">Doxygen documentation</a>


## Support

Please [submit an issue](https://github.com/th-hock/EgoSmartHeaterRS485/issues) for all questions, bug reports, and feature requests. Email requests will be politely redirected to the issue tracker so others may contribute to the discussion and requestors get a more timely response.
