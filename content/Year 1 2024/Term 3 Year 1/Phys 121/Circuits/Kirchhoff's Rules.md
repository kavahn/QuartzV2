
# Kirchhoff's Voltage Rules
- ###### Stats that the sum of the $\Delta V$ (voltage drops) caused by anything around a loop must be zero
	- why?? because the potential defference between them is 

# Kichhoff's Current Rule
- ###### Statse that the sum of the currents entering any given point in a circuit must equal the sum of all currens leaving the same point
- #### Ex
	- ![[Kirchhoff's Rules-20240615002317652.png|383]]
		- $I_{1}+I_{2}=I_{3}$ because the currents is flowing around and coming back to the junction at a

# How to solve
- ###### 1. Label each current (including its direction)
- ###### 2. Chose nodes and loops
- ###### 3. Apply node and loop rules; you will need as many independent equations as unknowns (we can just make them for free)
	- #### If we have N loops, only N-1 are independent

# Examples
- #### 1. Calculate the currents $I_{1}, I_{2},I_{3}$ in the three branches of the circuit
	- ![[Kirchhoff's Rules-20240615004655046.png]]
		- for each node we know that $I_{in}=I_{out}$ 
			- we can compare A and D
			- A: $I_{3}=I_{1}+I_{2}$
			- D: $I_{1}+I_{2}=I_{3}$ 
				- they are not independent because they are the same equation lol
		- And we know that the $\sum V=0$
			- and to solve we must isolate each loop (giving us an equastion each (V=IR for the entire guy =0))
		- ###### Upper;
			- $30I_{1}-45+1I_{3}+40I_{3}=0$
		- ###### Lower:
			- $-80+1I_{2}+20I_{2}-45+40I_{3}=0$