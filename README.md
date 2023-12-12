# Wireless_Control_Of_Prototype_Car
Wireless control of a car via arduino and hc12 for telemetry

keyboard_control.py reads "w a s d" from the keyboard (w-> move forward, s-> move backwards, a-> turn left, d-> turn right). and sends it to the serial monitor of the arduino board connected to the computer. transmitter_control.ino reads these "wasd" inputs from the serial monitor and sends it to another arduino through hc12 module in a character structure form wirelessly. reciever_control.ino receives the data via its hc12 connected module and reads data from the serial monitor. 

If the command is to move forward an L298N module is used to regulate voltage into two dc motors of 12V from the power source(battery back) which rotates the motors in the forward direction while the motors are rotated backward if the command is to move backwards by reversing the polarity of current through an in-built H-bridge in the L298N module. PWM pins allow for speed control (not implemented yet). 



The turning of the vehicle is controlled by TB6600 microstep motor driver and a Nema stepper motor. The motor driver is set to 2.8A and 16 steps. 
![motor-driver-l298](https://github.com/Raman-Saini9/Wireless_Control_Of_Prototype_Car/assets/68729255/f1d8edc2-a8e6-4eb0-981f-4eb6af7c0ccb)


All the arduino to microstep driver, hc-12 and L298 connection pins are specified in the code itself. 
