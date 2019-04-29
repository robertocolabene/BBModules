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
A=-x; B=-y;
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
A= round(x);<br>
B= round(y);
### 6. Dual VCA*
z: cv input;<br>
A= linear x;<br>
B= linear y;<br>
<b>Alternative outputs</b>:<br>
A= exponential x;<br>
B= exponential y;




