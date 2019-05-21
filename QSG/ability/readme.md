# Mirror

Mirror is a multi-algorithm module.

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
### 5. Logic Gates*
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
When x and y are not connected noise generates between [-5,+5];<br>
A= noise;<br>
B= noise sample;
### 2. Dual S&H
z: trigger input;<br>
x: signal input;<br>
y: signal input;<br>
A= x sample;<br>
B= y sample;


## OTHER
### 1. Clock*
Z: bpm;<br>
A= Master;<br>
B= div 2;<br>
<b>Alternative outputs</b>:<br>
A= Master;<br>
B= div 4;
### 2. Dual Sequencer*
z: clock input;<br>
x: if active cv input to set SeqA;<br>
y: if active cv input to set SeqB;<br>
A= SeqA;<br>
B= SeqB;<br>
<b>Alternative outputs</b>:<br>
A= Serial;<br>
B= -Serial;
### 3. Seq Switch
z: trigger input;<br>
A= x,y;<br> 
B= y,x;
### 4. Prob Switch
Z: probability parameter;<br>
z: trigger input;<br>
A= x,y;<br> 
B= y,x;
### 5. Env Follower
A= envelope x;<br> 
B= envelope y;
### 6. Lin/Exp & Exp/Lin*
A= 2^x;<br>
B= log2(y);<br>
<b>Alternative outputs</b>:<br>
A= e^x;<br>
B= ln(y);


## WAVESHAPERS
### 1. Dual Sym
Z: [-1,1];<br>
z: cv input;<br>
A= processed x;<br> 
B= processed y;
### 2. Asymmetrical
x: cv input;<br>
y: cv input;<br>
A= processed z;<br> 
B= -processed z;
### 3. Asymmetrical tp.2
x: cv input;<br>
y: cv input;<br>
A= processed z;<br> 
B= -processed z;

## ENVELOPE GEN
### 1. Attack Decay
Z: shape;<br>
x: attack;<br>
y: decay;<br>
z: trigger input;<br>
A= AD;<br> 
B= -AD;
### 2. Attack Decay EOC
Z: shape;<br>
x: attack;<br>
y: decay;<br>
z: trigger input;<br>
A= AD;<br> 
B= EOC;
### 3. Attack Decay Cycle
Z: shape;<br>
x: attack;<br>
y: decay;<br>
z: trigger input;<br>
A= ENV;<br> 
B= -ENV;


## SOUND GEN
### 1. VCO*
Z: Oscillator Frequency;<br>
x: pitch CV;<br>
y: if active AM modulation;<br>
z: pulse width;<br>
A= sine;<br>
B= triangle;<br>
<b>Alternative outputs</b>:<br>
A= sawtooth;<br>
B= square;
### 2. Dual VCO*
Z: Oscillator Frequency;<br>
x: pitch CV;<br>
y: pitch CV;<br>
z: pulse width;<br>
A= sine;<br>
B= saw;<br>
<b>Alternative outputs</b>:<br>
A= triangle;<br>
B= square;


## LFOs
### 1. Double LFO*
x: freq CV;<br>
y: freq CV;<br>
A= sine;<br>
B= sine;<br>
<b>Alternative outputs</b>:<br>
A= triangle;<br>
B= saw;
### 2. Multi Wave*
Z: LFO Frequency;<br>
z: pulse width;<br>
A= sine;<br>
B= triangle;<br>
<b>Alternative outputs</b>:<br>
A= sawtooth;<br>
B= square;


## FILTERS
### 1. LP & HP Parallel
Z: cutoff;<br>
x: signal input;<br>
y: cutoff_cv;<br>
z: resonance_cv;<br>
A= LP;<br> 
B= HP;
### 2. LP & HP Serial
Z: blend;<br>
x: cutoff_cv;<br>
y: cutoff_cv;<br>
z: signal input;<br>
A= LP->HP;<br> 
B= HP->LP;

## EFFECTS
### 1. Delay
Z: Feedback;<br>
x: L input;<br>
y: R input;<br>
z: time delay;<br>
A= L;<br>
B= R;<br>
### 2. Ring Modulator*
Z: Wet Level;<br>
x: L input;<br>
y: R input;<br>
z: oscillator pitch;<br>
A= L;<br>
B= R;<br>
<b>Alternative outputs</b>:<br>
A= soft L;<br>
B= soft R;
### 2. Reverse*
Z: FX Level;<br>
x: L input;<br>
y: R input;<br>
A= dry;<br>
B= wet;<br>
<b>Alternative outputs</b>:<br>
A= L;<br>
B= R;
### 3. Autoswell
Z: Rise;<br>
x: input;<br>
z: exp-lin-log;<br>
y: lin to exp;<br>
A= swell;<br>
B= swell + delay;<br>
### 4. Looper
z: input;<br>
x: rec trigger;<br>
y: overdub trigger;<br>
A= loop;<br>
B= status;<br>
### 5. Tremolo
Z: lfo frequency;<br>
x: input;<br>
y: dry/wet if connected;<br>
A= standard;<br>
B= harmonic;<br>
