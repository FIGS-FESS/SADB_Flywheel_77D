# SADB_Flywheel_77D

Brief:
  This is code to run the flywheel single axis dual bearing mode

Basic Operation:
  This setup utilizes two coils to provide both a positive and negative stabilization force in the x axis. If the sensor detects an offset, the coils will be activated to stabilize to a target position.

Pinouts:
  Current Sensors
  	-> Pin 09 (ADCA CH0) For H-Bridge 1	Coil 1
  	-> Pin 11 (ADCA CH1) For H-Bridge 2 Coil 2
  Displacement Sensor
  	-> Pin 12 (ADCB CH0) X axis
  PWM High
  	-> Pin 86 (GPIO 34) For H-Bridge 1
  	-> Pin 88 (GPIO 39) For H-Bridge 2
  PWM Low and Dir should be pluged into one of the 3.3V pins on the board to keep them at 	logic high. This garentees that when the PWM High pin is toggled the 

Reference Pins:
  ADCA Clock Signal -> Pin 49 (ePWM1 Compair A)
  ADCB Clock Signal -> Pin 53 (ePWM2 Compair A)
  Length of Displacement calculations -> Pin 89

Ussage:
  After the board is plugged in one should be able to debug the code. This code allows the user to operate a single axis of the upper stabilization bearing.

Considerations:
  I do not believe that the code is the best it can be but I can promise it is better than it was. The commenting on the other hand may need more work. Also I would recomend just skipping ahead to the DADB, it is much more fun.