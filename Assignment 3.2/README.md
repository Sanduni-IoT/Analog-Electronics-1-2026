Sanduni Edirisinghe
Simulation Parameters : To verify the theoretical outcomes of the bridge rectifier, the following parameters were configured in LTspice:                                  -AC Voltage Source ($V_{in}$): 100V Peak Amplitude, 50 Hz Frequency.                  -Stop Time: 40ms                                                                      -Components: 4 Diodes (Bridge configuration), Load Resistor ($R_L$), and Filter Capacitor ($C$).
Circuit Analysis & Behavior                                                            Part A: Without Capacito : The plot shows that the bridge rectifier flips the negative half-cycles of the AC input into the positive domain.Input ($V_1$): A standard sine wave swinging between +100V and -100V.Output ($V_0$): A series of positive "humps." Note that the peak output is slightly lower than 100V due to the voltage drop across two diodes (approx. $1.4\text{V}$ total).                          Part B: With Filter Capacitor : By adding a capacitor in parallel with the load resistor, the behavior changes:

Smoothing: The capacitor charges during the rising edge of the pulse and discharges slowly through the resistor during the gaps.

Ripple Voltage: The output is no longer pulsating to zero but remains near the peak voltage, creating a "smooth" DC signal with a small ripple.                          
