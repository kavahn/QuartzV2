# What is Amperes Law
- its a much easier version of [[Biot-Savart Law]] as its not only simpler but more consise 
- #### Formula
	- $\int \vec{B}\cdot d\vec{l} \,=\mu_{0}I_{enclosed}$
		- ##### what does this mean? 
			- ###### B is the magnetic field in the "amperian" loop we chose 
			- ###### dl is the dl of the amprerian loop so
				- so if its a circle we would use $2\pi r$ 
			- ###### $I_{enclosed}$ is the current enclosed in the amperian loop 
- ### NOTE!!! 
	- this only works if B is uniform in the amperian loop

# Solid wire carrying uniform current I
- ![[Amperes Law-20240712001351243.png|620]]
	- #### r < R
		- $B(2\pi r)=\mu_{0}\left( \frac{I}{\pi R^2} \right)(\pi r^2)$
	- #### r > R
		- $B(2\pi r)=\mu_{0}I$

# Hollow wire with uniform current I
- ![[Amperes Law-20240712001607168.png|339]]
	- #### r < a
		- B = 0
	- #### a < r < b
		- $B(2\pi r)=\mu_{0}\left( \frac{I}{\pi b^2-\pi a^2} \right)(\pi r^2-\pi a^2)$
	- #### r > b
		- $B(2\pi r)=\mu_{0}I$