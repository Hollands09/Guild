<h1 align="center">
	Indicators
</h1>

<h3 align="center">
	Intial Planning
</h3>

<p align="center">
	This is the intial planning stage of the updated indicators.  Each indicator will have 4 states, off, 1 light, 2 lights and 3 lights.  There are multiple ways to
	implement this.  My first thought was a simple SIPO shift register using D flip-flops with CLR and PRE and a 555 timer connected to bank of LEDs.  The frequency at which the timer will run
	has been picked arbitrarily for the time being but will be adjusted later to achieve the desired look and design.  I may have to implement some logic at SET but for now this works.  We
	will find out what happens when its implemented of a bread board.  This could be implemented with a an upcounter and a 1 - 4 mux or something similiar but getting a SIPO shift register with 
	D flip-flops and 2 channels seemed like an easier for size constraints.

</p>
	<img src="https://github.com/Hollands09/Guild/blob/main/Volvo/taillights/images/indicator_d1.png">
</p>

<h5 align="center">
	This is the basic structure of how the taillights will work.
</h5>

</p>
	<img src="https://github.com/Hollands09/Guild/blob/main/Volvo/taillights/images/basic_indicator_circuit.png">
</p>