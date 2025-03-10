Battery Draining Circuit

Project Overview

This project is a Battery Draining Circuit that discharges a smartphone battery by applying a controlled load. The circuit uses an Arduino Uno, an XL4015 buck converter, and an IRLB MOSFET to regulate the discharge process.
We have implemented a logical ON/OFF signal from the Arduino to control the MOSFET, but the battery drain effect can be increased by using PWM (Pulse Width Modulation) instead of a simple ON/OFF approach.
Additionally, we are monitoring the voltage drop across the load resistor using the Arduino to observe how the battery voltage decreases over time.

Hardware Components

Arduino Uno – Controls the MOSFET switching
IRLB MOSFET – Acts as an electronic switch to control current flow
XL4015 Buck Converter – Provides stable voltage to the circuit
Load Resistors (100Ω, 1Ω 5W) – Creates a discharge path for the battery
1N5819 Schottky Diode – Ensures correct current flow and protects components
Capacitor (1000µF) – Helps stabilize voltage fluctuations

Working Principle

1️⃣ The smartphone is connected to the circuit via a USB-A connection.
2️⃣ The MOSFET controls the current flow from the phone’s battery to the load resistors.
3️⃣ The Arduino sends either a logical ON/OFF signal or a PWM signal to the MOSFET’s gate, regulating power dissipation.
4️⃣ Higher load = faster discharge, but to prevent excessive battery stress, the resistor values are chosen carefully.
5️⃣ Voltage monitoring is done by measuring the voltage drop across the load resistor using Arduino’s analog input (A0 pin).

Improvement Ideas for Faster Discharge

✅ Using PWM control instead of a static ON/OFF signal for better power dissipation.
✅ Increasing the load resistance in parallel to draw more current.
✅ Adding active cooling to handle higher power dissipation without overheating components.
✅ Implementing automatic discharge cut-off when the battery reaches a certain voltage.

How to Use

1️⃣ Connect the smartphone to the USB-A port in the circuit.
2️⃣ Power the Arduino with 5V via USB.
3️⃣ Start the Arduino program to monitor voltage and control MOSFET switching.
4️⃣ Observe the voltage drop and battery discharge behavior in the serial monitor.
5️⃣ Adjust resistor values or MOSFET switching logic for different discharge rates.

Future Enhancements

🚀 Use a boost converter to simulate higher current draw.
🚀 Integrate a display to show battery status.
🚀 Implement mobile app control for remote discharge monitoring.
