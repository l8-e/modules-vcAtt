# Hack an der Ruhr - 2026 version

For Hack an der Ruhr (Hadr, https://hadr26.un-hack-bar.de/) i created one version of cvAtt to build together. 
This is the documentation for that very version. 

## About
Eurorack is a system / standart for modules which together build a synthesizer. It is very much the _unix approach to music_.
This means, a module is a simple basic tool, serving on purpose. It has inputs and outputs and transforms somehow inputs into outputs.
Connecting multiple modules allows to freely work with sound in a very creative and most of the time chaotic way. 

This is a very simple module, which can be easily built by yourself. It is a voltage controlled attentuator and does not require power supply. 
It has two inputs: an Input signal (`In`) and a control signal (`cv`). It adjustes the _loudness_ of the input depending on the control signal.
If the control signal is `0`, i.e. no power, the output signal will also be `0`. The the control signal has some constant power, the output matches the input, but the amplitude of the signal is damped,
depending on the power level of the control signal. 

Besides doing that, the module has tree optional elements:

* an LED
* a capacitor
* a diode

all three can be added, but do not have to. They can also easily be added or removed later. Changing this, also changes the behaviour of the output signal slightly,
so as a first way to play with the module and vary the sound characteristics, adding or removing the optional elements yields different sounds. 

## Testing

I you do not have Eurorack modules to test this module with, you can connect the input to the audio output of a mobile phone or pc (note: the vcAtt is mono, not stereo!)
and connect the output to some headphones. To hear a sound you now have to provide some power (0 - 5 V) to the control input.
The more power you provide the louder the signal will be. 

*Note:* Do this in your own risk! If you make mistakes in assembly this might harm headphones and/or the audio source! 

## List of Items

* front panel
* BC107 transistor
* capacitor
* diode
* led
* resistor
* 3 x 3,5 mm jack

## Schematics

##  Assembly

### Step 1
Use a bit of superglue to glue the three 3,5 mm jacks together, side by side and screw them in the front panel before the glue hardens. 

### Step 2
The 3,5 mm jacks have 5 connectors, but we need only three (for two the upper two of the jacks) or two (for the lowest one) of them. 
Remove the obsolete connectors

### Step 3 
Ground the jacks, i.e. connect the three ground connectors of the jacks. in addition, connect the the switch connectors of the two upper jacks also to ground


### Step 4
Insert LED and resistor. It is important to insert the led correctly! 
Connect LED and resistor. In addition, if wanted, connect the LED and resistor. 

*Note*: This is optional! They change the sound characteristics of the module and both can be spared without altering 
the functionality. 

### Step 5
Insert Capacitor and Diode if you want. *Note*: Both components are optional! They change the sound characteristics of the module and both can be spared without altering 
the functionality. 

### Step 6

Insert the transistor and connect the three legs to the three signal connectors of the three jacks

And you are done. 
