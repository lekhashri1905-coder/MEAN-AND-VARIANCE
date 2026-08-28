# MEAN-AND-VARIANCE

# AIM 
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

# EQUIPMENTS NEEDED

. Computer with i3 Processor
. SCI LAB

# Algorithm

1.Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.

2.Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.

3.Evaluate the Function: Compute the function values at each of these sample points.

4.Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.

5.Display Results: Output the computed mean variance and Cross Correlation

# PROCEDURE

.Refer Algorithms and write code for the experiment.
.Open SCILAB in System
.Type your code in New Editor
.Save the file
.Execute the code
.If any Error, correct it in code and execute again
.Verify the generated results

~~~
function z = f(x)
    z = 2 * (1 - x)^2;
endfunction

a = 0;
b = 1;

function z = fx(x)
    z = x * 2 * (1 - x)^2;
endfunction

EX = intg(a, b, fx);
disp("Mean of X = ");
disp(EX);

function z = g(y)
    z = 2 * (1 - y)^2;
endfunction

function z = fy(y)
    z = y * 2 * (1 - y)^2;
endfunction

EY = intg(a, b, fy);
disp("Mean of Y = ");
disp(EY);

function z = g(x)
    z = x^2 * 2 * (1 - x)^2;
endfunction

a = 0;
b = 1;

EX2 = intg(a, b, g);

function z = h(y)
    z = y^2 * 2 * (1 - y)^2;
endfunction

EY2 = intg(a, b, h);

vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;

disp("Variance of X = ");
disp(vX2);

disp("Variance of Y = ");
disp(vY2);

x= input("type in the reference sequence=");
y= input("type in the second sequence="); 
n1=max(size(y))-1;

n2=max(size(x))-1;

r=corr(x,y,n1);

plot2d3('gnn',r);
~~~
# TABULATION 

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/e0229e86-aeaf-4ae9-b675-54d4e83bda04" />


# OUTPUT WAVEFORM

<img width="1076" height="864" alt="image" src="https://github.com/user-attachments/assets/9e42a4a4-de01-43ba-a654-b2da52f65695" />



# RESULT
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.

