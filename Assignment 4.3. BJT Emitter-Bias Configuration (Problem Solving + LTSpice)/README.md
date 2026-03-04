Sanduni Edirisinghe

# BJT Emitter-Bias Configuration Analysis

## 1. Objective
To analyze a BJT emitter-bias circuit to determine the DC operating point and verify the stability provided by the emitter resistor ($R_E$) using mathematical calculations and LTspice simulation.

## 2. Circuit Parameters
* **Vcc:** 20V
* **Rb:** 270kΩ
* **Rc:** 470Ω
* **Re:** 2.2kΩ
* **Beta (β):** 125
* **Vbe:** 0.7V (Assumed)

## 3. Mathematical Calculations

| Parameter | Formula | Calculated Value |
| :--- | :--- | :--- |
| **Base Current ($I_B$)** | $(V_{CC} - V_{BE}) / (R_B + (\beta+1)R_E)$ | 35.27 µA |
| **Collector Current ($I_C$)** | $\beta \cdot I_B$ | 4.41 mA |
| **Emitter Voltage ($V_E$)** | $I_E \cdot R_E$ | 9.77 V |
| **Base Voltage ($V_B$)** | $V_E + V_{BE}$ | 10.47 V |
| **Collector Voltage ($V_C$)** | $V_{CC} - (I_C \cdot R_C)$ | 17.93 V |
| **Collector-Emitter Voltage ($V_{CE}$)** | $V_C - V_E$ | 8.16 V |

---

## 4. Conclusion
The addition of the emitter resistor $R_E$ provides feedback that stabilizes the Q-point against variations in $\beta$. The calculations confirm that the transistor is operating in the **Active Region** since $V_{CE} > V_{CE(sat)}$.
