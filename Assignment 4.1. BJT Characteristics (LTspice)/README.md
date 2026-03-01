Sanduni Edirisinghe

1. Linearity of $I_C \approx \beta I_B$

The relationship is mostly linear, as seen by the steady increase of Collector Current ($I_C$) relative to Base Current ($I_B$). However, it is not perfectly linear because the current gain ($\beta$) is not constant; it decreases slightly as the current increases.

2. Beta ($\beta$) Estimates at Operating Points

Using the mathematical trace Ic(Q1)/(I(I1)+1n) from the simulation:

At $I_B = 0.1\text{ mA}$: $I_C \approx 20\text{ mA}$, $\beta \approx 200$.
At $I_B = 0.5\text{ mA}$: $I_C \approx 90\text{ mA}$, $\beta \approx 180$.
At $I_B = 1.0\text{ mA}$: $I_C \approx 150\text{ mA}$, $\beta \approx 150$.

3. Role of $V_1 = 10\text{V}$

$V_1$ acts as the collector supply voltage. Its role is to provide the necessary $V_{CE}$ to keep the transistor in the Forward-Active region. If $V_{CE}$ were very small (e.g., $< 0.3\text{V}$), the transistor would enter the Saturation region, where it no longer effectively amplifies the base current.
