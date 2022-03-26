# Cruise controller for car
## This project involves control problems related car's velocity


<img src="https://user-images.githubusercontent.com/92177410/160154176-ba6324f2-1548-4d1d-975f-b0ba487fb28b.png" width="400" height="200">

#### PID CONTROLLER

  
<img src="https://user-images.githubusercontent.com/92177410/160156713-d0ec7dbc-0caa-4295-a781-0e32baa81d9b.png" width="400" height="150">


- For a given referce value , error is calculated by subracting refernce value and current value.
- This error is fed to PID controller , where it is passesd to three paths:
1) error with multipied by porportional gain Kp.
2) error integrated over time and multipied by integral gain Ki.
3) error differentiated and  multiplied by differential gain Kd.
4) these three inputs  are combined as a single input to the system.
- this guarantees that the error coverges to zero exponentailly for suitable Kp,Ki,Kd.
### Approach:
we discretized both newton's motion law and control equation.
after discretiaing we get new eqautions:


**v = u + a(t2 - t1)**
- where v and u are final and initial velocity respectively.
- a is acceleration 
- t2 - t1 is time step which we have taken as 1 second.
 f = ma 
 a = f/m
 
 
