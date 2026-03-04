# BJT Fixed-Bias Configuration Analysis

## 1. Objective
The goal of this assignment is to analyze a BJT fixed-bias circuit to determine the operating point ($Q$-point) through three distinct methods: mathematical derivation, graphical analysis, and LTspice simulation.

## 2. Circuit Parameters
The following parameters were provided for the analysis:
* **Supply Voltage ($V_{CC}$):** 20V
* **Base Resistor ($R_B$):** 470kΩ
* **Collector Resistor ($R_C$):** 910Ω
* **Transistor Beta ($\beta$):** 135
* **Base-Emitter Voltage ($V_{BE}$):** 0.7V (Assumed)

---

## 3. Mathematical Calculations

### Base Loop (KVL)
$$I_B = \frac{V_{CC} - V_{BE}}{R_B} = \frac{20\text{V} - 0.7\text{V}}{470\text{k}\Omega} = 41.06\mu\text{A}$$

### Collector Loop
$$I_C = \beta \cdot I_B = 135 \cdot 41.06\mu\text{A} = 5.54\text{mA}$$
$$V_{CE} = V_{CC} - (I_C \cdot R_C) = 20\text{V} - (5.54\text{mA} \cdot 910\Omega) = 14.96\text{V}$$

### Node Voltages
* **$V_E$:** 0V (Grounded)
* **$V_B$:** 0.7V
* **$V_C$:** 14.96V

---

## 4. Graphical Analysis (Q-Point)
By plotting the calculated values on the BJT characteristic curves:
* **Intersection:** $I_B \approx 41\mu\text{A}$ and $V_{CE} \approx 15\text{V}$.
* **Result:** The $Q$-point sits on the $I_C \approx 5.5\text{mA}$ horizontal line, validating the mathematical model.



---

## 5. LTspice Simulation
The circuit was constructed in LTspice using a custom NPN model with $B_f = 135$.

### Schematic


### Results Comparison
| Parameter | Calculated | LTspice Simulated | Difference |
| :--- | :--- | :--- | :--- |
| **$I_B$** | 41.06 µA | 41.06 µA | 0% |
| **$I_C$** | 5.54 mA | 5.54 mA | 0% |
| **$V_{CE}$** | 14.96 V | 14.96 V | 0% |

---

## 6. Conclusion
The theoretical calculations align perfectly with the simulation results. The BJT is operating in the **Active Region**, as $V_{CE}$ (14.96V) is well above the saturation voltage (~0.2V) and the base-emitter junction is forward-biased.
