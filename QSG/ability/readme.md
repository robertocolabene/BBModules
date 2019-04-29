# Ability

Ability is a multi-algorithm module.

## Quickstart Guide

![alt text](../../img/ability.png)<br>


### Controls
1. <b>Control Knob</b>: to control the algorithms category
2. <b>Alt. button</b>: to activate the alternative output mode
3. <b>Mod knob</b>: to control the algorithm
4. <b>Z knob</b>: multifunctional parameter
5. <b>x,y,z</b>: inputs
6. <b>A,B</b>: outputs

<b>Notes</b><br>
The <b>*</b> character near an algorithm title remind you that there's an alternative output.<br>
If the functionality of an input or a parameter it's not specified then it's a temporary useless variable.<br>

## UTILITIES
### 1. Inverter
A= -x;<br> 
B= -y;
### 2. Half-Wave Rectifier
A= positive values for x;<br>
B= positive values for y;
### 3. Full-Wave Rectifier*
A= |x|;<br>
B= |y|;<br>
<b>Alternative outputs</b>:<br>
A= |x+y|;<br>
B= |x-y|;
### 4. Quantizer
A= round(x);<br>
B= round(y);
### 5. Slew Limiter
Z: shape;<br>
z: signal input;<br>
x: rise;<br>
y: fall;<br>
A= out;<br>
B= -out;
### 6. Dual VCA*
z: cv input;<br>
A= cv_linear * x;<br>
B= cv_linear * y;<br>
<b>Alternative outputs</b>:<br>
A= cv_exponential * x;<br>
B= cv_exponential * y;

## LOGIC
### 1. Min-Max
A= min;<br> 
B= max;
### 2. Logic 1*
Z: [-5,5];<br>
z: cv input;<br>
A= x+y+z;<br>
B= x-y-z;<br>
<b>Alternative outputs</b>:<br>
A= x+z;<br>
B= y-z;
### 3. Logic 2*
Z: [-5,5];<br>
z: cv input;<br>
A= x * y + z;<br>
B= x / y + z;<br>
<b>Alternative outputs</b>:<br>
A= x * z;<br>
B= y * z;
### 4. Logic 3*
Z: [-5,5];<br>
z: cv input;<br>
A= x * y * z;<br>
B= x * y ^ z;<br>
<b>Alternative outputs</b>:<br>
A= x^z;<br>
B= y^z;
### 5. Logic Ports*
Z: [-1,1];<br>
z: cv input;<br>
When Z+z >= 1 the not port is active;<br>
x: true when >=1;<br>
y: true when >=1;<br>
A= AND;<br>
B= OR;<br>
<b>Alternative outputs</b>:<br>
A= XOR;<br>
B= XNOR;

## SAMPLER
### 1. Sample & Hold
z: trigger input;<br>
x: noise threshold;<br>
y: noise threshold;<br>
When x and y are not connected noise generates between [-5,+5]
A= noise;<br>
B= noise sample;
### 2. Dual S&H
z: trigger input;<br>
x: signal input;<br>
y: signal input;<br>
A= x sample;<br>
B= y sample;


