# Polarization

## Concepts of Polarization

- **Definition**: Light is polarized when its electric fields oscillate in a single plane, rather than in any direction perpendicular to the direction of propagation.
	- basically, all light that propagates between a polarizer is all one orientation
		- ![[Polarization-20240716214134543.png|163]]

### Polarized Light and Polarizers

- **Transmission**: Polarized light will not be transmitted through a polarized film (polarizer or polarization filter) whose axis is perpendicular to the polarization direction.
- **Outgoing Intensity**:
    - When light passes through a polarizer, only the component parallel to the polarization axis is transmitted. If the incoming light is plane-polarized (linearly polarized), the outgoing intensity is proportional to the square of the cosine of the angle between the light's polarization direction and the axis of the polarizer.

### Behavior through Crossed Polarizers

- **Crossed Polarizers**: If initially unpolarized light passes through crossed polarizers (axes at 90°), no light will get through the second one.

### Examples

- **Two Polaroids at 60°**: Unpolarized light passes through two Polaroids; the axis of one is vertical and that of the other is at 60° to the vertical. Describe the orientation and intensity of the transmitted light.
    - Intensity: $I_2 = I_1 \cos^2 60° \approx \frac{1}{8} I_0$
- **Three Polaroids**: If a third Polaroid, with its axis at 45° to each of the other two (crossed at 90°), is placed between them, some light will pass through.
    - Intensity Pattern: $I = \frac{1}{8} I_0$.

## Brewster's Angle

- **Brewster's Angle**: At the polarizing angle or Brewster’s angle, reflected light is 100% polarized perpendicular to the plane of incidence.i
    - *we use*: $\tan \theta_{p}=\frac{n_{2}}{n_{1}}$ to find angle
    - **Example**:
        - Given $n_1 = 1.00$ (air) and $n_2 = 1.33$ (water), calculate:
            - Polarizing angle: $\theta_P = \tan^{-1}(1.33) = 53.1°$
            - Refraction angle: $\theta_r = \sin^{-1} \left(\frac{n_1 \sin \theta_P}{n_2}\right) \approx 36.9°$

## Circular Polarization

- **Relative Phase Change**: By changing the relative phase between $E_x$ and $E_y$ using a quarter wave plate (through birefringence), linear polarization can be converted to circular polarization.
- **Right Circular Polarization (RCP)**: Use the right-hand rule to determine the direction.
- **Behavior of Circular Light on a Linear Polarizer**: When circularly polarized light is put through a polarizer along the y (or x) axis:
    - Answer: Intensity $I = \frac{1}{2} I_0$

## Linear and Elliptical Polarization

- **Phase Difference**: Different phases between $E_x$ and $E_y$ produce elliptical or circular polarization.
- **Example**:
    - At $\phi_x - \phi_y = 90°$, using $t = 0$ $$ \begin{align} E_x = \frac{E_0}{2} \cos (kz - \omega t) \\E_y=\frac{E_0}{2} \sin (kz - \omega t) \end{align} $$ This configuration leads to circular polarization.

These notes have covered the main points presented in the lecture PDFs on polarization, including conceptual explanations, mathematical expressions, and examples.