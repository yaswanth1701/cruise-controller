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
 
 
 **F = ma**
 
 **F** is input to system over which we apply our control law.
 ### Results:
 
  
 #### single desired velocity:
 ##### desired or reference velocity = 60 km/hr
 ##### only proportional gain Kp:
 only Kp value does not make car's velocity reach its desired velocity
 
 
 <img width="295" alt="ki=0   kd=0" src="https://user-images.githubusercontent.com/92177410/160253422-814f4004-a0b0-4431-939f-95e1f2a951a3.png">
 
 
 
 #### proportional and integral gain:
 integral gain makes velocity reach desired velocity but overshoot.
 
<img width="311" alt="kd=0" src="https://user-images.githubusercontent.com/92177410/160253519-963acd29-1cfa-4e9c-90d4-d1da9b0b4990.png">
  
  
  #### proportional, integral and derivate gain:
  derivate gain reduces the overshoot and for some value velocity smoothy converges to desired velocity 
 
 
<img width="282" alt="Screenshot 2022-03-21 230711" src="https://user-images.githubusercontent.com/92177410/160253626-da6ce142-e8f5-472d-9a19-c6f5bf153e5c.png">

#### multiple desired velocity:
##### desired velocity is 60 km/hr for first 30 seconds and then it changes to 100 km/hr




<img width="294" alt="variable desired velocity" src="https://user-images.githubusercontent.com/92177410/160253895-8adc3123-6ccb-4e43-8e81-1e7eaadef8ca.png">
## Reference:
### all dynamics are provided in pdf which attached above
