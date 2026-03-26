# Circuit Challenges 5, 6, and 7

## Overview
This document explains three practical electronics challenges using transistors, voltage dividers, LDRs, and RC circuits. These challenges focus on automation, timing, and delay circuits.

---

# 🔵 Challenge 5: Night Light Circuit

## Objective
Design a circuit where:
- LED turns ON in the dark
- LED turns OFF in the light

## Components Used
- LDR (Light Dependent Resistor)
- 100K Resistor
- NPN Transistor (PN2222)
- LED
- 200Ω Resistor
- Power Supply

## Working Principle
- A **voltage divider** is created using LDR and resistor
- Output voltage goes to the **base of the transistor**
- In darkness:
  - LDR resistance increases
  - Output voltage increases
  - Transistor turns ON → LED ON
- In light:
  - LDR resistance decreases
  - Output voltage decreases
  - Transistor OFF → LED OFF

## Key Concept
Light controls voltage → Voltage controls transistor → Transistor controls LED

---

# 🟢 Challenge 6: Cascade Fade Circuit

## Objective
Create 4 LEDs that fade out at different times when buttons are released.

## Working Principle
- Press button → Capacitor charges → LED ON
- Release button → Capacitor discharges → LED fades
- Different capacitor values → Different fade times

## Key Concept
Larger capacitance = Longer fade time

---

# 🔴 Challenge 7: RC Delayed Switch

## Objective
Keep an LED ON for about **75 seconds** after releasing a button.

## Components Used
- 100K Resistor
- Capacitors: 47µF + 100µF
- NPN Transistor
- LED
- Push Button

## Working Principle
- Button pressed → Capacitor charges → Transistor ON → LED ON
- Button released → Capacitor slowly discharges
- Transistor stays ON until voltage drops below 0.7V

## Key Concept
Capacitor stores energy → Slowly releases → Keeps transistor ON

---

# 🧠 Conclusion

From these challenges, we learned:
- How to use **LDR for automatic control**
- How to design **timing circuits using RC**
- How capacitors control **delay and fading**
- How transistors act as **switches**

These are important concepts for:
- Smart lighting systems
- Timers
- IoT projects

---
