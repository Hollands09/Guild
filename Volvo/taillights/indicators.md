<h1 align="center">
	Indicators
</h1>

<h3 align="center">
	Intial Planning
</h3>

<p align="center">
	This is the intial planning stage of the updated indicators.  Each indicator will have 4 states, off, 1 light, 2 lights and 3 lights.  There are multiple ways to
	implement this.  My first thought was a simple SIPO shift register using D flip-flops with CLR and PRE and a 555 timer connected to bank of LEDs.  The frequency at which the timer will run
	has been picked arbitrarily for the time being but will be adjusted later to achieve the desired look and design.  The ELI5 version of this is the indicator position will be selected,
	lets use right for this example.  When selected the output 1 will be fed into the shift register.  While the indicator is in that position a 1 will always be fed into the shift register.
	The shift register acts this way, imagine 4 boxes connected in a row that all contain a 0.  The contents of these boxes is updated every time the clock cycle is equal to 1.  The clock cycle
	looks like this 0, 1, 0, 1 ..... to when power to the timer is turned off (i.e. when the car is turned off).  On the initial clock cycle with the indicator in the right position, a 1 is fed into
	the first box.  On the next clock cycle the second box will contain whatever what in the first box.  On the next clock cycle the third box will contain whatever is in the second box.  And so on.
	Each box outputs to a specific bank of LEDs for the indicator.  So when the first box contains a 1 only the first bank will turn on, when the first and second box contain a 1, 2 banks of LEDs will
	turn on.  On the fourth cycle of the clock being equal to 1 the last box contains a 1.  This indicates that all 3 LED banks have been illuminated and we need to turn them all off.  So this box
	tells all the boxes to turn off.  As long as the indicator is in its selected position this cycle repeats.  If the indicator is switched off the first box accepts a 0 but what we really want is
	all the lights to turn off.  This 0 will also trigger all the lights to turn off.  The basic implementation of this circuit below.
</p>

</p>
	<img src="https://github.com/Hollands09/Guild/blob/main/Volvo/taillights/images/indicator_d1.png">
</p>