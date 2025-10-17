# Idle-motor

Main objective: 
Simulating the idle control of a gasoline engine 

<p align="center">
  <img src="https://github.com/Yoyiberto/Idle-motor/blob/a20158ff99cd59b7fc08e401a78040bc36dc17d2/idle_motor.png" alt="Robot_img" width="50%">
</p>

Steps
1.	System analysis. For the idle control of a gasoline engine, what are the inputs and outputs of the system and control? Draw a general control diagram with all the units. What are the specifications of the control law? What are the criteria or indicators that should be used to specify the performance of the control?
2.	System model. What are the physical and algebraic equations that allow the system to be simulated? Draw the architecture of such a model using block diagrams.
3.	Simulation of the system model. Perform the dynamic model of the system in Matlab/Simulink with the help of the library provided (Tools.mdl found in n1_Bloc_Tests). The models provided in n1_Bloc_Tests gives the architecture block by block and it is necessary to fill in the "holes".
a.	Make the blocks one by one and validate them with the test blocks (unit tests),
b.	Validate the general model.
4.	Open loop: System identification. Excite system inputs around multiple operating points in order to understand how it works. Identify simple models (e.g. a second-order system) at these different points of operation.
Analyze the linearity properties of the system as much as possible.
5.	Specifications (CoC), expected behavior. In the perspective of closed-loop regulation, give the elements that will be observed in terms of performance criteria.
6.	Control "by hand". 
a.	Carry out the block diagram of the closed loop including two PID controls, i.e. a PID for the throttle valve and a PID for the ignition advance. 
b.	From the analysis in BO, propose a preset of the two correctors.
c.	Test your settings. Improve your settings as needed with regard to the expected performance.
d.	Write a script to evaluate performance (see CdC)
e.	Test the robustness of the chosen solution in the presence of noise.
A few remarks: 
Have physical common sense,
To test the operation in LF it is necessary to add the disturbance of the accessories,
It is (probably) best to first tune and test a scheme with a single regulator and then add the second. To think about which one first,

7.	Pole placement control 
a.	By the method of pole placement determine an analytical setting. 
b.	Compare the results (without noise) obtained according to the performance criteria established above.
c.	Test the robustness of the solution in the presence of noise.
d.	What is the impact of noise (measurement, accessories and combustion)?

8.	Frequency decoupling. 
a.	Imagine a solution that could, as its name suggests, achieve frequency decoupling in response to the problem.
b.	Implement frequency decoupling
c.	Compare the results (without noise) obtained according to the performance criteria established above.
d.	Test the robustness of the solution in the presence of noise.

9.	Elaborate + solutions. 
Several more elaborate solutions can be implemented in response to the problem of idle control, such as:
•	An order by inverse model: in a "business" version, this solution can be compared to the couple structures,
•	An RST control: advanced PID control that offers control/disturbance decoupling
•	Optimal control, LG, LQG, etc. which offers the advantage of explicitly integrating the trade-off between performance and loads
•	A numerical optimization control (fmin, fmincon, fminsearch, etc. from Matlab) that offers the advantages and disadvantages of any numerical optimization approach.
Depending on the progress of the work, in agreement with the teacher, you may study one or other of these proposals.

Deliverable: A summary of the work done in the tutorial
