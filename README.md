# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB-
__AIM:__

To write a program for mean, variance and cross correlation in SCILAB and verify the output. 

__EQUIPMENTS NEEDED:__

.Computer with i3 Processor 

.SCI LAB 

__ALGORITHM:__

1. Define the Function: Specify the function you want to simulate. For example, 
f(x)=sin⁡(x)f(x)=sin(x) or any other function. 
2. Generate Sample Points: Decide on the range and the number of sample points. Generate 
these sample points within the desired range. 
3. Evaluate the Function: Compute the function values at each of these sample points. 
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the 
mean and variance of the computed function values. 
5. Display Results: Output the computed mean variance and Cross Correlation 

__PROCEDURE:__ 

1.Refer Algorithms and write code for the experiment. 

2.Open SCILAB in System 

3.Type your code in New Editor 

4.Save the file 

5.Execute the code If any Error, correct it in code and execute again 
  
6.Verify the generated results

__PROGRAM:__
```
clear;
 clc; 
clear; 
//Mean Value 
function X=f(x), 
z=3*(1-x)^2,
//Marginal Probability Density Function 
X=x*z; 
endfunction 
a=1.5; 
b=2; 
EX=intg(a,b,f); //Mean value of X
function Y=c(y), 
z=3*(1-y)^2, //Marginal Probability Density Function 
Y=y*z;
endfunction
 EY=intg(a,b,c);//Mean value of Y
 disp(EX,"i)Mean of X =") 
disp(EY," Mean of Y =")
//Variance 
function X=g(x),
 z=3*(1-x)^2,
//Marginal Probability Density Function
 X=x^2*z; 
endfunction 
a=1.5; 
b=2; 
EX2=intg(a,b,g); 
function Y=h(y), z=3*(1-y)^2,
//Marginal Probability Density Function
 Y=y^2*z;
endfunction 
EY2=intg(a,b,h); 
vX2=EX2-(EX)^2; //Variance of X 
vY2=EY2-(EY)^2;//Variance of Y 
disp(vX2,"ii)Variance of X"); 
disp(vY2," Variance of Y");
//Cross Correlation
 x= input("type in the reference sequence=");
 y= input("type in the second sequence=");
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1); 
plot2d3('gnn',r);
```

__OUTPUT GRAPH:__
<img width="1917" height="1076" alt="image" src="https://github.com/user-attachments/assets/1ac16d4b-c410-4e24-aaa2-c75e854037c7" />

__RESULT:__

Hence, mean and variance are simulated in Scilab using the program mentioned above.
