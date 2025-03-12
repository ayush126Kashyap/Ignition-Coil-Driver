# Ignition-Coil-Driver
This project is a high-voltage ignition coil driver circuit using an IRF540N MOSFET and a 1N4007 flyback diode. It efficiently drives an ignition coil to generate high-voltage pulses. The circuit is designed for experimental and educational purposes, demonstrating MOSFET switching and flyback energy management.
# Ignition Coil Driver Circuit using IRF540N MOSFET

## Overview
This project demonstrates an **Ignition Coil Driver Circuit** using an **IRF540N MOSFET** and a **1N4007 flyback diode**. The circuit is designed to generate high-voltage pulses by switching the coil on and off rapidly. 

## Components Used
- **IRF540N MOSFET** (Power switching component)
- **1N4007 Diode** (Flyback protection)
- **Ignition Coil** (High-voltage generation)
- **Resistors** (To limit current and control gate drive)
- **Power Source** (12V battery or DC power supply)
- **Microcontroller (optional)** (For PWM control)

## Circuit Diagram 
(Add your circuit schematic here)

## Working Principle
- The **MOSFET** acts as a switch, controlled via a gate signal.
- When **turned ON**, current flows through the ignition coil, building up a magnetic field.
- When **turned OFF**, the collapsing magnetic field induces a high-voltage spike at the secondary coil.
- The **1N4007 diode** prevents voltage spikes from damaging the MOSFET.

## Code (For Arduino-based Control)
If using an Arduino to drive the MOSFET, you can use the following sample PWM code:

```cpp
int mosfetGate = 9; // PWM pin

void setup() {
    pinMode(mosfetGate, OUTPUT);
}

void loop() {
    digitalWrite(mosfetGate, HIGH);
    delay(10);  // Adjust for desired pulse duration
    digitalWrite(mosfetGate, LOW);
    delay(10);
}
```

## Testing & Results
- Observed **high-voltage spark** across the ignition coil output.
- Confirmed MOSFET heat dissipation and switching performance.
- Used an oscilloscope to check pulse waveform.

## Applications
- Automotive ignition systems
- High-voltage experiments
- Inductive energy transfer

## Future Improvements
- Use a **better flyback diode** (e.g., **UF4007** for faster recovery time).
- Implement **PWM frequency control** for better efficiency.
- Add a **heat sink** for prolonged operation.
