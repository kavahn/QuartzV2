# Building off [[Electric Flux]]
$$
\phi_{net}=\oint \vec{E}*d\vec{A}=\frac{q_{enclosed}}{\epsilon_{0}}
$$
- this states the amount of flux in a Gaussian solid in an electric field
	- if the charge is not cetrered it stil/ is the *same* as the symmetrical one
		- ![[Gauss' Law-20240605184704489.png]]\
			- Gauss' law tells us that to find the E field in the enclosed space we integrate along all of the E arrows that pierce through the solid


# Spherical Symmetry
- ## Point Charges
	- #### Point charge
	- ![[Gauss' Law-20240605185917305.png]]
		- When we have a sphere with the cross section that looks like the picture above we can assume the sphere the potential is treated as a point charge (we dont need to get q enclosed because it is a point charge and the charge is given)
		- $E(4\pi r^{2})=\frac{q}{\epsilon_{0}}$
	- #### Point charge in metal shell
	- ![[Gauss' Law-20240605191117307.png]]
		- ###### its different from the point charge because we must under these 3 things
			- $E(4\pi r^{2})=\frac{q}{\epsilon_{0}},r<a$
			- $E(4\pi r^{2})=0,a<r<b$
			- $E(4\pi r^{2})=\frac{q}{\epsilon_{0}},r>b$
				- this is because when we are outside the shell the metal shell inherits the charge
	- #### Metal shell with net charge Q, surrounding point charge q
	- ![[Gauss' Law-20240606061157906.png]]
		- $E(4\pi r^{2})=\frac{q}{\epsilon_{0}},r<a$
			- i dont know why but im guessing its because of the charges inside and out fighting each other and it being always q
		- $E(4\pi r^{2})=0,a<r<b$
			- no matter what inside a metal the field will always be 0
		- $E(4\pi r^{2})=\frac{q+Q}{\epsilon_{0}},r>b$
			- additive
	- #### Metal shell with net charge Q
	- ![[Gauss' Law-20240606062511732.png]]
		- $E(4\pi r^{2})=0,a>r$
			- no charge inside
		- $E(4\pi r^{2})=0,a<r<b$
			- again no charge in metal
		- $E(4\pi r^{2})=\frac{Q}{\epsilon_{0}},r>b$
			- easy
	- 



### How to find E in the Gauss law
$$
E\int \, da =EA=\frac{Q_{enclosed}}{\epsilon_{0}}\implies E=\frac{Q_{enclosed}}{A\epsilon_{o}} 
$$

- THIS IS *NOT* a formula this is just the derivation  of it