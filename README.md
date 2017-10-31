plumpot-cellular
===================

A plumpot series base board with a sub-1GHz radio and a 2.5G cellular modem

Features
--------------------

- half-length, half-width form factor (80x50mm)
- mounting holes for half-length half-width and half-length quarter-width extension boards
- two extension bus connectors (UXB1 compatible - multidrop half-duplex SPI bus, I2C bus, wakeup request, interrupt request and 5V power)
- AX5243 sub-1GHz radio module with a 50ohm MMCX antenna connector
- Quectel M66 2.5G GPRS/EDGE cellular modem with a 50ohm MMCX antenna connector and network activity LED indicators
- 6-60Vin power supply step down regulator for providing system and bus power (5V, 0.2A)
- micro-B USB port with a CP2101 serial to USB bridge (console access and power input)
- RTC with a CR1220 lithium coin cell backup

The board is developed as an open source hardware using tools freely available for non-
commercial usage. It is able to run free and non-free commercial software without any
restrictions. It is not locked to a specific firmware and contains a standard 10-pin Cortex Debug
connector. A multitude of free and commercial development tools exist to develop and modify the
firmware for the board.

History
----------------

This is a uNodeX form-factor version of the qNode4 board (hence the previous name "unodex-connect-42").

I accepted a set of rules for board design, sizes, mounting types and board communication
to ease the development of new hardware. Such hardware could be easily connected together
to form wireless nodes for IoT/IoM and similar usages and enables you to do data acquisition,
data forwarding/communication, control, etc. I started to call this platform "uNodeX"
(micro node - extendable).

This is a rework of the previous qNode4 board to be compatible with the uNodeX platform,
with a slightly modified hardware:

- step-up converter for battery charging is removed
- RF connectors are changed to MMCX
- uNodeX bus connectors are added
- board dimensions are changed to 50x80mm (uNodeX half-width, half-depth)
- CP2102 USB to serial converter for console access
- VBUS power oring controller for uNodeX bus
- 6-60VDC step-down converter is added
- temperature sensor is removed

The board includes only a reduced set of hardware to fulfill the following requirements:

- to be a mainboard for HWHD or QWHD cards
- to provide power for them
- to enable them to communicate over the air (uMesh stack or GPRS/EDGE)

I started to call this board "plumpot" as it is mainly used to run the plumCore firmware.
