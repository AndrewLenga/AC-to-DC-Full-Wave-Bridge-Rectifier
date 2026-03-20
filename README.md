# AC-to-DC-Full-Wave-Bridge-Rectifier
This repository contains the schematic and documentation for a standard Full-Wave Bridge Rectifier with a capacitive filter. This circuit is designed to convert an alternating current (AC) input into a steady, filtered direct current (DC) output suitable for powering electronic devices.
##🛠 Circuit Breakdown
The circuit is divided into four primary stages that process the electrical signal from "raw" AC to stable DC.
1. Input Stage
Component: J1 (Screw Terminal)
Function: This is the entry point for the AC power source, typically from a low-voltage step-down transformer.
Polarity: At this stage, the electricity is alternating; there is no fixed positive or negative terminal.
2. Rectification Stage (The Bridge)
Components: D1, D2, D3, D4 (1N4007 Diodes)
Function: Converts AC to pulsating DC. Diodes act as one-way valves, ensuring that current always flows in the same direction toward the positive rail regardless of the input cycle.
Efficiency: By using a "full-wave" bridge configuration, both the positive and negative halves of the AC cycle are utilized, making it significantly more efficient than a half-wave rectifier.
3. Filtering & Safety Stage
Component C1 (1000µF Capacitor): Acts as a reservoir to smooth out the "pulsating" ripples from the rectifier. It stores energy during peaks and releases it during troughs to maintain a steady DC voltage.
Component R2 (10kΩ Bleeder Resistor): A critical safety feature. It slowly discharges the capacitor when power is disconnected, preventing accidental electric shocks from stored energy.
4. Monitoring & Output Stage
Component D5 (LED) & R1 (2.2kΩ Resistor): Serves as a "Power On" indicator. R1 is a current-limiting resistor used to prevent the LED from burning out.
Component J2 (Screw Terminal): The final DC output point. Unlike the input, this terminal has fixed polarity:
Pin 1: Positive (+VE)
Pin 2: Ground (GND)
##📋 Component List
Reference	Value/Model	Description
D1 - D4	1N4007	Rectifier Diodes (1A, 1000V)
C1	1000µF	Electrolytic Filter Capacitor
R1	2.2kΩ	LED Current Limiting Resistor
R2	10kΩ	Bleeder Resistor (Safety)
D5	LED	Power Indicator
J1, J2	Screw Terminal	Input/Output Connectors
##⚠️ Safety Information
Ensure the input voltage does not exceed the voltage rating of the 1000µF capacitor.
Always verify the polarity of the capacitor (C1) and LED (D5) before applying power to avoid component failure.
