# discrete point charges
- ###### (like the infinite long charge where we take the integral)
	- be *careful* with vector nature
- #### the summation is $\vec{E}=\sum_{i}k{\frac{Q_{i}}{r_{1}^2}}\hat{r}_{i}$ 
	- ##### But we need the integral $$\vec{E}=\int k{\frac{dq}{r^2}} \, \hat{r}$$
		- #### WHAT DOES THIS MEAN
			- conceptually is not different! 
			- integrating over all charges ($dq$)
			- $\vec{r}$ is the vector from $dq$ to the point at which $\vec{E}$ is defined
		- #### Example
			-  we have a wire that is charged with Q uniformly, and has a linear density of $\lambda=\frac{Q}{L}$ and we find the point P  at a arbitrary point 
			- ![[Continuous Charge Distributions-20240510171331799.webp]]
- #### Example 1
	- a straight wire of length 2L carries a uniform linear charge density $\rho_{e}$ ;determine the electric field $\vec{E}$at point P, a distance r from the wire along the perpendicular bisector
	- ![[Continuous Charge Distributions-20240513170054130.webp|236]]
		- $R'$is length of the distance from L
			- $dz$ is the varible of integration
		- by symmetry, $\vec{E}=\hat{r}E_{r}$
			- $R'=\sqrt{ R^{2}+z'^{{2}} }$
			- $\cos \alpha=\frac{r}{R'}$
		- Solving for $E_{r}$
			- $E_{r}=\frac{1}{4\pi \epsilon_{0}}\int \frac{dq*\cos \alpha}{R'^{2}} \, dx$ 
	- 
- #### Example 2
	- ###### The electri field at point P due to a thin uniformly charged rod located on the z axis givien by $\vec{E}=e_{z}\hat{k}+E_{R}\hat{R}$
$$
\begin{align}
E_{z}=\frac{k\lambda}{R}(\sin \theta_{2}-\sin \theta_{1})
\end{align}
$$