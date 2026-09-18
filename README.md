# Analysis of P, PI and PID Controllers using MATLAB
## Aim:
To analyse the effect of P, PI and PID controllers for the system having open loop transfer function, G(S)=1/(S^2+10S+20) using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
	A controller is a device introduced in the system to modify the error signal and to produce a control signal. 
	The way the controller produces the control signal is called the control action.

Consider the following unity feedback system,
 <img width="823" height="281" alt="image" src="https://github.com/user-attachments/assets/36e49512-cf47-4fec-b00c-f79dc0af1c5f" />

### Proportional (P) Controller:
The proportional controller produces an output, which is proportional to error signal.<br>
u(t)∝e(t) <br>
⇒u(t)=Kpe(t) <br>
Apply Laplace transform on both the sides - <br>
U(s)=KpE(s) <br>
U(s)/E(s)=Kp <br>
Therefore, the transfer function of the proportional controller is Kp.

### Proportional Integral (PI) Controller:
The proportional integral controller produces an output, which is the combination of outputs of the proportional and integral controllers. <br>
u(t)=Kp e(t)+Ki ∫e(t)dt <br>
Apply Laplace transform on both sides - <br>
U(s)=(Kp+Ki/s)E(s) <br>
U(s)/E(s)=Kp+Ki/s <br>
Therefore, the transfer function of proportional integral controller is Kp+Kis. <br>

### Proportional Integral Derivative (PID) Controller:
The proportional integral derivative controller produces an output, which is the combination of the outputs of proportional, integral and derivative controllers. <br>
u(t)=Kp e(t)+Ki ∫e(t)dt+ Kd (de(t)/dt) <br>
Apply Laplace transform on both sides - <br>
U(s)=(Kp+Ki/s+Kds)E(s) <br>
U(s)/E(s)=Kp+Ki/s+Kd s <br>
Therefore, the transfer function of the proportional integral derivative controller is Kp+Ki/s+Kd s

### Characteristics of Kp, Ki and Kd terms:

Increasing the proportional gain ( ) has the effect of proportionally increasing the control signal for the same level of error. The fact that the controller will "push" harder for a given level of error tends to cause the closed-loop system to react more quickly, but also to overshoot more. Another effect of increasing   is that it tends to reduce, but not eliminate, the steady-state error.
The addition of a derivative term to the controller ( ) adds the ability of the controller to "anticipate" error. With derivative control, the control signal can become large if the error begins sloping upward, even while the magnitude of the error is still relatively small. This anticipation tends to add damping to the system, thereby decreasing overshoot. The addition of a derivative term, however, has no effect on the steady-state error.
The addition of an integral term to the controller ( ) tends to help reduce steady-state error. If there is a persistent, steady error, the integrator builds and builds, thereby increasing the control signal and driving the error down. 
 


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the steady state error and analyse the controllers.
## Program: 
## Simulink:
### With P-Controller
<img width="1307" height="552" alt="image" src="https://github.com/user-attachments/assets/bf5333ce-e97a-4701-8de3-e40f2087b610" />

### With PI Controller
<img width="1307" height="552" alt="image" src="https://github.com/user-attachments/assets/ec917ff8-f602-4f07-8d0d-2a51adce0987" />


### With PID Controller
<img width="1307" height="552" alt="image" src="https://github.com/user-attachments/assets/66e117c3-a66e-452c-a8e3-a292427c9843" />


## Output: 

### With P-Controller
<img width="1912" height="916" alt="image" src="https://github.com/user-attachments/assets/685b2163-bfed-435e-a4e7-a5b77c750937" />


### With PI Controller
<img width="1905" height="936" alt="image" src="https://github.com/user-attachments/assets/1690e89b-c13b-4567-97b9-cea66391ebd0" />

### With PID Controller
<img width="1917" height="923" alt="image" src="https://github.com/user-attachments/assets/8b5a73ed-423f-4562-ada2-6dbb95f8a282" />


## Result:
Thus the P, PI and PID controllers for the given system was analysed and the following conclusions were arrived using MATLAB. <br>

### With P Controller 
Delay time =0.06s <br>
Rise time = 0.10s <br>
Peak time =0.18s <br>
Settling time =1.2s <br>
Steady State Error =0.1 <br>
### With PI Controller 
Delay time =0.05s <br>
Rise time =0.08s<br>
Peak time =0.16s<br>
Settling time =3.8s<br>
Steady State Error =0  <br> 
### With PID Controller 
Delay time =0.04s  <br>
Peak time =0.08s <br>
Settling time =3.7s <br>
Steady State Error =0 <br>




