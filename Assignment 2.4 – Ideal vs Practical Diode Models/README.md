Diode Model Analysis: Ideal vs. Practical (1N4148)

1. Comparison of Results
In this simulation, I analyzed a simple series circuit using two different diode models: a generic **Ideal Diode** and a practical **1N4148 Silicon Diode**.

Difference in Turn-on Voltage

The primary difference observed is the "threshold" at which the diode begins to conduct. 
Ideal Model:** Functions like a perfect switch; it shows a sharp transition almost immediately.
* **Practical Model (1N4148):** Exhibits an exponential "knee." It begins conducting a small amount of current around $0.5V$ and reaches full conduction near $0.7V$. This reflects the physical reality of the depletion region in a silicon $P-N$ junction.

### Difference in Current Behavior
* **Ideal Model:** Shows a perfectly linear relationship once "on".
* **Practical Model:** Accounts for internal bulk resistance. As voltage increases, the curve shows physical limits and internal losses that the ideal model ignores.

---

## 2. Engineering Judgment

### Why ideal models are still used:
Ideal models are invaluable for initial circuit design and "napkin math". When a system uses high voltages (e.g., $15V$ or $24V$), a $0.7V$ drop is negligible. It allows for quick verification of logic and current flow direction.

### When ideal models become inaccurate:
* **Low-Voltage Applications:** In $1.8V$ logic, a $0.7V$ drop is a massive percentage of the total signal.
* **Power & Heat:** They are insufficient for calculating power dissipation ($P = I \times V_f$) or thermal behavior.
