Smart Coin Machine PCB (v2.1)

![Smart Coin PCB Version 2 1](https://github.com/user-attachments/assets/ca069f5e-9c23-4e36-bfbb-2b26aa98db8c)

This project is a custom PCB for smart coin and bill acceptor machines, designed to simplify wiring, assembly, and integration with GSM modules, Arduino, and Raspberry Pi.

✨ Features

Plug & Play Wiring

Just connect +12V DC input via screw terminals.

Direct connections for coin acceptor, bill acceptor, buzzer, and status LEDs.

GSM Module Support

Compatible with SIM800L and SIM800C.

On-board relay to enable/disable GSM module.

Reset GSM via dedicated relay (Arduino Pin 7).

Built-in DC-DC step-down regulator (LM2596S) provides stable +4V supply for GSM.

Relays & Control

Coin Enable Relay → controlled by Raspberry Pi (Pin 17).

GSM Enable Relay → power cycle or disable GSM when needed.

Power Loss Relay → detect and respond to AC mains failures.

Indicators & Status LEDs

Arduino Pin 8 → Blue LED status output.

Raspberry Pi Pin 27 → Green LED status output.

GSM status LED indicators (Orange).

220VAC Detection

Input and output connectors for 220VAC detection sensor.

Useful for monitoring AC mains availability.

----------------------------------------------------------------------------------------

📐 Hardware Overview

Main components visible on the PCB:

LM2596S DC-DC Buck Converter (12V → 4V for GSM).

3 Relays:

Coin Enable Relay

GSM Enable/Reset Relay

Power Loss Relay

Connectors:

12V DC input

Coin acceptor

Bill acceptor

Buzzer

LEDs (Arduino, Raspberry Pi, GSM)

220VAC detection input/output

GSM Module Slot (SIM800L/SIM800C footprint).

(See PCB layout in uno-r4-shield-template__Assembly.pdf
 for detailed pinouts)
.

----------------------------------------------------------------------------------------

🔌 Pin Mapping
Function	Controller	Pin
Coin Enable	Raspberry Pi	GPIO17
LED Status (Green)	Raspberry Pi	GPIO27
LED Status (Blue)	Arduino	Pin 8
GSM Reset	Arduino	Pin 7
⚡ Power

Input: +12V DC

Internal Regulator: LM2596S → +4V for GSM

Relays and acceptors powered directly from +12V line.

----------------------------------------------------------------------------------------

🚀 Use Case

This PCB is ideal for:

Smart vending or refill machines.

Coin/bill based Bitcoin Lightning machines.

GSM-enabled kiosks requiring reliable reset and status handling.

----------------------------------------------------------------------------------------

📂 Repository Contents

Smart Coin PCB Version 2.1.JPG → Rendered 3D PCB view.

uno-r4-shield-template__Assembly.pdf → PCB layout & assembly reference.

README.md → This documentation.

----------------------------------------------------------------------------------------

🛠️ Assembly Notes

Connect +12V DC power input.

Wire coin and bill acceptors into screw terminals.

Install GSM module (SIM800L or SIM800C).

Connect buzzer and LED indicators.

Connect Raspberry Pi/Arduino control lines as per pin mapping.

----------------------------------------------------------------------------------------

📜 License

This project is free to use as hobby project or commercial
