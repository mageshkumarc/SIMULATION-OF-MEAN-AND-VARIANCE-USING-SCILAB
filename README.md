# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB
## AIM
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB


## ALGORITHM
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation
   
## PROCEDURE
•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated results


## PROGRAM
```
clc; clear;

function y=f(x)
    y = x * 3 * (1-x)^2;
endfunction

EX = intg(0,1,f);

function y=g(y1)
    y = y1 * 3 * (1-y1)^2;
endfunction

EY = intg(0,1,g);

disp(EX, "i) Mean of X = ");
disp(EY, "   Mean of Y = ");

function y=f2(x)
    y = (x^2) * 3 * (1-x)^2;
endfunction

EX2 = intg(0,1,f2);

vX2 = EX2 - (EX^2);

function y=g2(y1)
    y = (y1^2) * 3 * (1-y1)^2;
endfunction

EY2 = intg(0,1,g2);

vY2 = EY2 - (EY^2);

disp(vX2, "ii) Variance of X = ");
disp(vY2, "    Variance of Y = ");

x= evstr(input("Type in the reference sequence (e.g. [1 2 3]): "));
y = evstr(input("Type in the second sequence (e.g. [2 4 6]): "));

x = x(:)';
y = y(:)';

N = length(x);
M = length(y);

xc = conv(x, y($:-1:1));
lags = -(M-1):(N-1);

disp([lags' xc'], "Lag   Cross-correlation");

clf();
plot2d3(lags, xc);
xtitle("Full Cross-correlation");
xlabel("Lag");
ylabel("Correlation");
```
## CALCULATION
![WhatsApp Image 2025-11-23 at 11 33 04_0402b6b1](https://github.com/user-attachments/assets/c616761f-b0b8-4b50-befa-5701e8441413)

![WhatsApp Image 2025-11-23 at 11 33 04_04205155](https://github.com/user-attachments/assets/0f2dad9e-8bb4-40f9-ad3a-8acd92a31bc9)

## OUTPUT
<img width="1622" height="967" alt="AC EXP5" src="https://github.com/user-attachments/assets/599ffcaf-b4b2-42f2-9ddc-3c8ce8263a5e" />

## RESULT
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
