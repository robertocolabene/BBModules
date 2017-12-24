# BBModules

### Notes
You can find my modules to purchase <a href="https://gumroad.com/bbmodules">here</a>.<br>

#### Attention
NEED a developer for linux.<br>
The developer will be always the same but he can't public the source code. Obviously he will have all my modules for free. <br>
Thanks to Jeremy for the help with mac environment.

#### To do


#### Bugs
Waiting...<br><br><br>

# The Manual

## Modded VCO

<b>SIN, TRI, SAW, SQR, SPECIAL</b> knobs - to control the amount for each signal;<br>
<b>out</b> - it's the sum of all the 5 signals;<br>
<b>clone</b> - it's the sum of all the 5 signals not controlled by fine knob;<br>
<b>spl</b> - it's the sum of 5 not conventional waves;<br>

SPECIAL from <b>out</b> and SPECIAL from <b>spl</b> are different waves<br>

<b>sSRCbP</b> stands for <b>source signal replacement controlled by phase</b> 

<b>alpha</b> - to control the source to modulate<br>
<b>beta</b> - to control the group of signals to replace<br>
<b>mphs</b> - it's the out for phase modding<br>
<b>omega</b> - to control the amount of <b>sSRCbP</b><br>

## Context Menu
### Input Mode

- <b>Standard</b>: fm and sync are properly dedicated to their function<br>
- <b>Alpha-Beta Mod</b>: fm and sync are dedicated to modulate alpha and beta parameters<br>
- <b>Special Amount Mod</b>: fm it's dedicated to modulate the SPECIAL knob and fmcv to control the amount<br>
- <b>Omega-Beta Mod</b>: fm and sync are dedicated to modulate omega and beta parameters and fmcv to control the amount for omega<br>

![alt text](https://github.com/soulbridge/BBModules/blob/master/free.jpg)

## Modded VCO (Complete Version)
### The Aim
I like find and create new sounds, my sounds. Well, why not a customizable sound generator? I built this complex oscillator to have the most personal waveform as possible. I hope you like it.<br>

### What's new?
I added 4 inputs on the top that allow you to modulate different destinations. Those inputs are splitted in two groups, the first two on the top are called <b>1 - 2</b>, the other two under are called <b>3 - 4</b>.<br>

![alt text](https://github.com/soulbridge/BBModules/blob/master/complete.jpg)

### Input Mode

- <b>AM</b>: Amplitude modulation, the first in <b>1 - 2</b> wait for an input signal from -5V to 5V , the second one in <b>3 - 4</b> wait for a signal from 0V to 10V. You're free to use both of them simultaneously.<br>
- <b>Spl</b>: Special wave modulation. (-5V,5V)<br>
- <b>Alpha</b>: Alpha parameter modulation, it changes the source in <b>sSRCbP</b> process, alpha knob is the offset. (-10V,10V)<br>
- <b>Beta</b>: Beta parameter modulation, it changes all the 4 waves to replace in the <b>sSRCbP</b>, the wave in memory is the offset. (-10V,10V)<br>
- <b>Beta N</b>: Beta parameter modulation, it changes just the N wave to replace in the <b>sSRCbP</b>, the wave in memory is the offset. (-10V,10V)<br>
- <b>Omega</b>: Omega parameter modulation, it changes the amount of <b>sSRCbP</b>, omega knob is the offset. (-5V,5V)<br>
- <b>Fine</b>: Fine parameter modulation. (-5V,5V)<br>
- <b>Theta</b>: Theta parameter modulation, theta knob is the offset (-5V,5V)<br>
- <b>Wave N</b>: Take in input the N wave to replace in <b>sSRCbP</b> process. (-10V,10V)<br>

#### Look Closer
<b>Theta</b> is the initial phase modulation for all the special waves.<br>
The <b>waves</b> you replace in the sSRCbP process are not synchronized, you have to manually sync one oscillator to the other, or maybe not... ?<br>
Using your <b>external waves</b> doesn't allow you to have a beta modulation.<br>
The <b>button on the top</b> is useful to quantize the tuning knob but you can always switch in digital mode to moving in semitones.<br>
You can use the <b>clone</b> out to detuning the second internal vco with the first using the fine knob or modulation too.<br>
The <b>special waves</b> emphasize different harmonics, so they could sound "strange" and, cause of their waveform, they could have a "strange" behaviour.<br>

### sSRCbP mode Selection
A way to have less complex replacement of the signals is to set a replacement based on the pole of the source signal or by the trend, in other words the derivative of the source function. So you would have a double replacement and you can use your external waves in the group <b>1 - 2</b>.<br>

### Donation
- if you want, you can... <a href="https://paypal.me/bbmodules">here</a><br>
