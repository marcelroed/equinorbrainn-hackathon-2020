# Description of Wind Farm

A Wind Farm consists of a number of three-bladed horizontal-axis Wind Turbines (a.k.a. "Wind Energy Converter",  "Turbine", etc.).  Turbines at your field can generate up to XMW (=X000KW).

Each Turbine has:
	- 3 blades (marked A, B, C in the dataset). Blades change pitch (angle of attack) in order to adjust the rotation speed and the generated power. 
	- Nacelle (housing containing generator and other components). Nacelle changes its direction (yaw angle) corresponding to the current wind direction in order to optimize production
	- A number of sensors measuring electrical and mechanical parameters of the turbine
	- Other components, which are not important in the context of the current task

A turbine can be in "On" (production) or "Off" (stopped") modus. When in "Off" modus, the turbine does not produce, but consumes power. 

In addition, a turbine may operate in a "Curtailed" mode, when it cannot generate power over a given limit. Bringing turbine on/off, as well as reaching the requested production limit, is a timely process. 

Most of the sensors produce continuous stream of data, but some are discrete, producing values from time to time. For such sensors, value is considered unchanged until the next real reading arrives.