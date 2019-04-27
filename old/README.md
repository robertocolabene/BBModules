# BBModules

### Notes
You can find my modules to purchase <a href="https://gumroad.com/bbmodules">here</a>.<br>

# The Manual

## Complex Oscillator

![alt text](img/complex.png)

<b>SIN, TRI, SAW, SQR, SPL</b> knobs - to control the amount for each signal;<br>
<b>|o|</b> - it's the out produced by <b>sSRCbP</b><br>
<b>|s|</b> - it's the sum of all the 5 signals;<br>
<b>|c|</b> - it's the sum of all the 5 signals not controlled by fine knob;<br>
<b>|≈|</b> - it's the sum of 5 not conventional waves;<br>

<b>sSRCbP</b> stands for <b>source signal replacement controlled by phase</b> 

<b>ã|</b> - to control the source to modulate<br>
<b>ḅ|</b> - to control the group of signals to replace<br>
<b>ö|</b> - to control the amount of <b>sSRCbP</b><br>
<b>ŧ|</b> - to shift the phase angle<br>

### The Aim
I like find and create new sounds, my sounds. Well, why not a customizable sound generator? I built this complex oscillator to have the most personal waveform as possible. I hope you like it.<br>

### What's new?
I added 4 inputs on the top that allow you to modulate different destinations. Those inputs are splitted in two groups, the first two on the top are called <b>1 - 2</b>, the other two under are called <b>3 - 4</b>.<br>

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
<br>

## Einstein-Rosen Bridge (discontinued)

![alt text](img/erb.jpg)

The "Einstein-Rosen bridge" module is a probabilistic <b>delayer</b> and, I have to say it, this module is easy to learn but it could be pretty hard to master.<br>
Basically this module have one input and one output, the signal on the input will be buffered and delayed on the output.<br>
<b>Attention it's not a classical delay, there's no wet, there's no feedback... on the out there's the signal delayed.</b><br>

### The Knobs
- <b>distance</b> : from 0 to 10 seconds, when you're on 0 you're not moving, anyway the signal will exit from the out.
- <b>time</b> : let you change the range of distance between 0-1s and 0-100s.
- <b>data loss</b> : erase the input data during the journey.
- <b>opening</b> : the bridge could be not opened so there's 1 on N possibilities to have success.

For convenience the "opening" and "data loss" proccesses will be available from 0.<br>

## The probabilistic side
<b>One of the most important thing to predict what will be your out is to understand how to use Probability Computing.</b><br>
Cause of that it's also very important to put on the input a signal that returns on a real zero voltage. (for example a filter out with some resonance can return a not zero voltage.)<br>
Let me advice you, you should use a VCA before of this module, if you're sending a gate or a trigger there's no need.<br>
So, this module recognize when a signal is active or not, which means a different from zero signal.<br>
It follows that the probability of every event, except for data loss, it's influenced by the presence of the signal.<br>

### Probability Computing
- <b>One shot, signal on</b>: the probability is computed one time when the signal is active.<br>
- <b>One shot, signal off</b>: the probability is computed one time when the signal is not active.<br>
- <b>Meanwhile, signal on</b>: the probability is computed continuously when the signal is active.<br>
- <b>Meanwhile, signal off</b>: the probability is computed continuously when the signal is not active.<br>
- <b>Always</b>: the probability is computed continuously.<br>

### Journey: Probability of Success
The distance parameter can be influenced by probability. It follows that the distance can be randomly increased or decreased in relation to the setted distance.<br>

- <b>likely on long distance</b>: the journey will be sure and accurate near 1 parsec.<br>
- <b>likely on short distance</b>: the journey will be sure and accurate near 0 parsec.<br>
- <b>not affected by probability</b>: the journey won't be affeceted by probability.<br>

<b>The limits of this function.</b><br>
- This function cannot work in continuum mode.
- If you're working with a signal you have to be sure that returns to 0 to recompute probability for the next one.
- Working in not continuum mode  may cause attached notes or gates or triggers, read under.

<b>Musically Talking</b><br>
While attached notes can be part of a style, the sequenced notes that this function can't handle it's a real limitation. <br>
You should use this function away from fast incoming signals to have results. In the other cases just stay in continuum.<br>

### The Continuum
There are two modes of working.<br>
<b>When the button of continuum is off</b>: every note played while the buffer is not empty will be attached on the previous one.<br> <b>When the button is on</b>: every pause between the notes will be granted in the out but you can't change the distance knob.<br>

<b>The buffer is empty when the led is blue, not empty while is green.</b><br>
Changing the distance <b>while the buffer is active</b> can produce two results.<br>
<b>If you decrease the distance nothing happen until the buffer goes empty.</b><br>
<b>If you increase the distance the out will be delayed up to the next distance.</b><br>

As you noticed you can't use probability variations on the distance knob while continuum button is active. The main reason is that the buffer is always active and can't rewind the time, so once the delay time is passed it can only be increased, that's a useless action.<br>

### Some advices
You can use data loss to make some noise.<br>
You should use the opening probability in combination with "one shot, signal off" or "meanwhile, signal off".<br>
You should use the distance probability variations in combination with "one shot, signal on".<br>
In most of the cases "one shot, signal off" will be the best option.<br>

<br><br>
