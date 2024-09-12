# Key take aways
- ### Every firstorder linear ODE $y'=p(t)y=g(t)$ is solvable
- ### the solution requires *TWO* integration steps

# Summary of the method of integrating factors
- ### 1. put the ODE in "standard form"
	- $y'+p(t)y=g(t)$
- ### Calculate the integrating factor
	- $u(t)=e^{\int p(t) \, dt}$
		- ###### for the integrating factor $u(t)$ we can ignore the constant of integration
- ### Calculate the integral $\int u(t)g(t) \, dt$ and use the formula
	- $y(t)=\frac{1}{u(t)}\left( \int u(t)g(t) \, dt \right)$
		- ###### where for the indefinite integral, we need the constant of integration to get the general solution 

# Note on integral notation:
- $\int _{t_{0}}^{t}u(s) \, ds$ 
	- a definite integral
	- t is independent varible
	- s is a dummy varible of integration
- $\int u(s) \, ds$ 
	- indefinite integralgenarl
	- a family of functions in s


# Ex:
- #### Find the genarl solution for $y'-2y=t^{2}e^{2t}$
	- write ode in standard form:
		- $y'-2y=t^{2}e^{2t}$ (left hand =p(t), right hand = (g(t)))
	- calculate IF:
		- $u(t)=e^{\int p(t) \, dt}\implies u(t)=e^{-2t}$
	- apply formula on the last slide (BUT ONLY DO THIS ONCE)
		- $\frac{d}{dt}(uy)=ut^{2}e^{2t}$
			- => $uy=\int ut^{2}e^{2t} \, dt\implies e^{2t}\left( \frac{t^{3}}{3}+k \right)$
	- *important:* always check by subsituting into the ODE
		- $y=\frac{e^{2t}t^{3}}{3}+ke^{2t}$
	- 
