***Sanduni Edirisinghe

# BJT Voltage-Divider Bias Analysis

## 1. Objective
To analyze the DC operating point ($Q$-point) of a BJT voltage-divider bias circuit using the approximate analysis method and verify the findings with LTspice simulation.

## 2. Circuit Parameters
* **Supply Voltage ($V_{CC}$):** 18V
* **$R_1$:** 39kΩ
* **$R_2$:** 8.2kΩ
* **$R_C$:** 3.3kΩ
* **$R_E$:** 1kΩ
* **$\beta$:** 120
* **$V_{BE}$:** 0.7V (Standard)

## 3. Stability Check
Approximate analysis is valid if $\beta R_E \geq 10R_2$:
* $120 \cdot 1\text{k}\Omega = 120\text{k}\Omega$
* $10 \cdot 8.2\text{k}\Omega = 82\text{k}\Omega$
* **Result:** $120\text{k}\Omega \geq 82\text{k}\Omega$ (Valid)

## 4. Mathematical Calculations (Approximate Method)

| Parameter | Formula | Calculated Value |
| :--- | :--- | :--- |
| **Base Voltage ($V_B$)** | $(R_2 \cdot V_{CC}) / (R_1 + R_2)$ | 3.13 V |
| **Emitter Voltage ($V_E$)** | $V_B - 0.7\text{V}$ | 2.43 V |
| **Collector Current ($I_C$)** | $V_E / R_E$ | 2.43 mA |
| **Collector Voltage ($V_C$)** | $V_{CC} - (I_C \cdot R_C)$ | 9.98 V |
| **Collector-Emitter Voltage ($V_{CE}$)** | $V_C - V_E$ | 7.55 V |
| **Base Current ($I_B$)** | $I_C / \beta$ | 20.25 µA |

---

## 5. LTspice Simulation

### Results Comparison
| Measurement | Theoretical (Approx) | LTspice Result |
| :--- | :--- | :--- |
| $V_B$ | 3.13 V | [Insert Value] |
| $V_C$ | 9.98 V | [Insert Value] |
| $I_C$ | 2.43 mA | [Insert Value] |
| $V_{CE}$ | 7.55 V | [Insert Value] |

## 6. Conclusion
The circuit is properly biased in the active region. The small differences between theory and simulation are expected due to the approximate nature of the manual calculation compared to the precision of the SPICE model.
