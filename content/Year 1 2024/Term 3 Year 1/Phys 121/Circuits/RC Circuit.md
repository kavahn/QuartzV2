# RC Circuits
- #### Overview
    
    - An RC (Resistor-Capacitor) circuit is a circuit that contains both resistors and capacitors.
    - These circuits are fundamental in understanding how electrical charge is stored and dissipated in various components.
- ### Charging a Capacitor
    
    - When a capacitor is charged through a resistor, the voltage across the capacitor and the current through the circuit change over time according to the following relationships:
        - $\displaystyle V_C(t) = V_{0} \left(1 - e^{-\frac{t}{RC}}\right)$
        - $\displaystyle I(t) = \frac{V_0}{R}e^{-\frac{t}{RC}}$
        - $V_0$ is the initial voltage, $R$ is the resistance, $C$ is the capacitance, and $t$ is time.
    - The time constant ($\tau$) of an RC circuit is defined as $\tau = RC$. It indicates how quickly the capacitor charges or discharges.
- ### Example of Charging RC Circuit
    
    - #### Given:
        
        - Capacitance: $C = 0.30\ \mu\text{F}$
        - Resistance: $R = 20 \text{k}\Omega$
        - Battery emf: $E = 12 \text{V}$
    - #### Calculate:
        
        - Time constant ($\tau$): $\tau = RC = (0.30 \times 10^{-6}\ \text{F})(20 \times 10^{3}\ \Omega) = 6\ \text{ms}$
        - Maximum charge ($Q_{\text{max}}$): $Q_{\text{max}} = CE = (0.30 \times 10^{-6}\ \text{F})(12\ \text{V}) = 3.6 \ \mu\text{C}$
        - Time to reach 99% of $Q_{\text{max}}$: Solve for $t$ in $Q(t) = Q_{\text{max}} \left(1 - e^{-\frac{t}{\tau}}\right)$
- ### Discharging a Capacitor
    
    - When a fully charged capacitor discharges through a resistor, the charge and the current through the circuit decrease over time as given by:
        - $\displaystyle Q(t) = Q_0 e^{-\frac{t}{RC}}$
        - $\displaystyle I(t) = -\frac{Q_0}{RC}e^{-\frac{t}{RC}}$
        - $Q_0$ is the initial charge on the capacitor.
- ### Example of Discharging RC Circuit
    
    - #### Given:
        - Capacitance: $C = 1.02 \mu\text{F}$
        - Battery emf: $E = 20\ \text{V}$
        - Current decreases to 0.50 of its initial value in $40\ \mu\text{s}$
    - #### Calculate:
        - Initial charge on the capacitor ($Q_0$): $Q_0 = CE = (1.02 \times 10^{-6}\ \text{F})(20\ \text{V}) = 20.4 \ \mu\text{C}$
        - Value of $R$: Derived from given info that current reduces by half in $40\ \mu\text{s}$`[1]``[2]``[3]`.
