# Building off [[Odds]]

# What is Bayes' Rule

- #### A mathematical rule for updating the probability of a hypothesis based on new evidence.
    
    - Prior Probability $(P(H))$: The initial probability of the hypothesis.
    - Evidence Probability $(P(E|H))$: The probability of the evidence given that the hypothesis is true.
    - Updated Probability $(P(H|E))$: The new probability of the hypothesis after considering the evidence.

# Bayes' Rule Formula

- #### Bayes' Rule can be expressed mathematically as:
    

$[P(H|E) = \frac{P(E|H) \times P(H)}{P(E)}]$ - Where $P(E)$ is the total probability of the evidence: $[P(E) = P(E|H) \times P(H) + P(E|\neg H) \times P(\neg H)]$

# What is a Bayes' Box

- #### A visual tool for understanding Bayesian updates.
    
    - A Bayes' Box represents the probabilities involved in Bayes' Rule as areas within a box.

# Drawing a Bayes' Box

- #### Steps to create a Bayes' Box:
    
    - **Step 1**: Divide the box according to the prior probabilities of $H$ and $\neg H$.
        - Example: If prior odds are 1:3 (for $H$ and $\neg H$ respectively), the box is split accordingly.
    - **Step 2**: Divide the areas of $H$ and $\neg H$ based on the probability of evidence $E$ if $H$ is true or false.
        - Fill sections representing $P(E|H)$, $P(\neg E|H)$, $P(E|\neg H)$, and $P(\neg E|\neg H)$.
    - **Step 3**: Use the areas to visually estimate the updated probability.

# Interpreting the Bayes' Box

- EX.
    
    - a box is divided to show prior odds of $H$ of 1:3, making $P(H) = \frac{1}{4}$ and $P(\neg H) = \frac{3}{4}$.
        
    - **Evidence provided (e.g., a medical test)**:
        
        - $P(E|H) = 0.75$
        - $P(E|\neg H) = 0.25$
        - Updated calculation for $P(H|E)$ given by: [ P(H|E) = \frac{P(E|H) \times P(H)}{P(E|H) \times P(H) + P(E|\neg H) \times P(\neg H)} = \frac{0.75 \times 0.25}{0.75 \times 0.25 + 0.25 \times 0.75} = \frac{0.1875}{0.375} \approx 0.5 ]
- **Visual estimation**:
    
    - Compare shaded areas for $E$ within $H$ and $\neg H$. For $P(H|E)$, look at the ratio of shaded areas in the $H$ section to the total shaded area.

# Example Interpretation from Exercises

- **With Evidence (E)**:
    
    - Updated odds: approximately 2:3 (visually), translating to $P(H|E) \approx 2/5$ (probability).
- **Without Evidence ($\neg E$)**:
    
    - Updated odds: approximately 1:6 (visually), translating to $P(H|\neg E) \approx 1/7$.

# Useful Lessons

- ### Key Bayesian Lessons:
    
    - **Bayes Lesson #1**: Always consider the prior probability.
    - **Bayes Lesson #2**: Likely evidence if hypothesis is true confirms the hypothesis.
    - **Bayes Lesson #3**: If evidence ($E$) confirms the hypothesis, then lack of evidence ($\neg E$) disconfirms it.
    - **Bayes Lesson #4**: Yesterday's updated probability becomes today's new prior probability for further evidence.

# Sensitivity and Specifisity 
