Sanduni Edirisinghe

BJT Fixed-Bias Configuration Analysis

1. Objective
   
To determine the operating point (Q-point) of a fixed-bias BJT circuit using mathematical calculations, graphical characteristics, and LTspice simulation.

3. Circuit Parameters

Supply Voltage VCC = 20V
Base Resistor RB = 470k ohms
Collector Resistor RC = 910 ohms
Transistor Beta = 135
Base-Emitter Voltage VBE = 0.7V


3. Mathematical Calculations

Base Loop (KVL)

VCC - IBRB -VBE = 0
20V - IB(470k) - 0.7V = 0
$I_B \approx 41.06\mu\text{A}$

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
