# Hack an der Ruhr - 2026 version

For Hack an der Ruhr (Hadr, https://hadr26.un-hack-bar.de/) i created one version of cvAtt to build together. 
This is the documentation for that very version. 

*WARNING: currently in my built there is some error! I do not know where and why so I am not sure that this works out as expected!**


## About
Eurorack is a system / standart for modules which together build a synthesizer. It is very much the _unix approach to music_.
This means, a module is a simple basic tool, serving on purpose. It has inputs and outputs and transforms somehow inputs into outputs.
Connecting multiple modules allows to freely work with sound in a very creative and most of the time chaotic way. 

![the completed built](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/completed.png)



This is a very simple module, which can be easily built by yourself. It is a voltage controlled attentuator and does not require power supply. 
It has two inputs: an Input signal (`In`) and a control signal (`cv`). It adjustes the _loudness_ of the input depending on the control signal.
If the control signal is `0`, i.e. no power, the output signal will also be `0`. The the control signal has some constant power, the output matches the input, but the amplitude of the signal is damped,
depending on the power level of the control signal. 

Besides doing that, the module has two optional elements:

* an LED
* a capacitor

all can be added, but do not have to. In addition, the LED can be added in two different ways, leading to six total variations of the module. They can also easily be added or removed later. Changing this, also changes the behaviour of the output signal slightly,
so as a first way to play with the module and vary the sound characteristics, adding or removing the optional elements yields different sounds. 

The idea to use that very transistor to build a vcAtt is not mine! This work is based on the circuit https://lookmumnocomputer.discourse.group/t/lpg-vca-circuit/69/2 from lookmumnocomputer! So all credits goes to him and not me.

## Testing

I you do not have Eurorack modules to test this module with, you can connect the input to the audio output of a mobile phone or pc (note: the vcAtt is mono, not stereo!)
and connect the output to some headphones. To hear a sound you now have to provide some power (0 - 5 V) to the control input.
The more power you provide the louder the signal will be. 

*Note:* Do this in your own risk! If you make mistakes in assembly this might harm headphones and/or the audio source! 

## List of Items

* front panel
* BC107 transistor
* capacitor, 2,2nf
* diode, in4146
* led, 2.5mm yellow
* resistor, roughly 470 Ohm
* 3 x 3,5 mm jack

![all required parts](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/parts.png)


## Schematics

### Basic version without optional elements

![panel, made from wooden spatula](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/plain.png)

### Adding the LED in serial option

![panel, made from wooden spatula](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/serial_led.png)


### Adding the LED in parallel option

![panel, made from wooden spatula](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/parallel_led.png)


### Adding the capacitor as low pass filter

In case you decide to add the capacitor, the schematic looks as follows. Note that there are three versions, depending on your 
choice of LED before (none, serial, or parallel setup):

![panel, made from wooden spatula](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/caps.png)
![panel, made from wooden spatula](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/parallel_led_caps.png)
![panel, made from wooden spatula](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/serial_led_caps.png)




##  Assembly

### Step 1
Use a bit of superglue to glue the three 3,5 mm jacks together, side by side and screw them in the front panel before the glue hardens. 

![mounting jacks](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/jacks1.png)

![mounting jacks](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/jacks2.png)

### Step 2

![the five connectors of a jack](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/jacks3.png)

The 3,5 mm jacks have 5 connectors, but we need only three (for two the upper two of the jacks) or two (for the lowest one) of them. 
Remove the obsolete connectors. Which ones are well visible in the image of Step 3. I failed to make a good image here, sorry. 

### Step 3 
Ground the jacks, i.e. connect the three ground connectors of the jacks. in addition, connect the the switch connectors of the two upper jacks also to ground. Use black wire for this. 

![grounded jacks](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/grounded.png)



### Step 4 (optional)
Insert LED and resistor. It is important to insert the led correctly! 
Connect the long leg of the LED and one leg of the resistor. Use yellow wire to create these connections.

![front view of led](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/led_front.png)
![back view of led](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/led_back.png)


#### Parallel LED Option
If you go for the parallel LED Option, you now connect the other/free leg of the resistor with the cv-input signal
and the short / free leg of the LED with ground. For the ground connection use black wire! 

![parallel led](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/parallel_led1.png)
![another view of parallel led](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/parallel_led2.png)


#### Serial LED Option
If you go for the serial LED option, you now connect the other/free leg of the resistor with the cv-input signal. 
The short / free legt of the LED will be connected directly to the diode input later. 

#### No LED Option
If you opted for no LED, you are done with this step. maybe shorten the legs a bit. 

### Step 5
Insert cap. Orientation does not matter.

![front view of cap](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/cap_front.png)

Then connect one leg to ground with black wire and the other leg with grey wire to the output signal:

![back view of cap](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/cap_back1.png)
![another back view of cap](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/cap_back2.png)


### Step 6
Insert diode.
![front view of diode](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/diode_front.png)

The orientation of this element is crucial! Insert the diode such that the black ring shows to the right!
Then connect the left leg, i.e. the leg without the black ring of the diode with the cv signal (or the free LED leg of you went for the serial option). Use 
yellow wire for this. *Note:* left and right switch when turning around the panel, so check at least twice before connecting! In my image i have a parallel LED setup. So this might look different for you!

![front view of diode](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/diode_back.png)



### Step 7
Insert transistor.

https://www.allelcoelec.com/blog/Understanding-the-BC107-Transistor.html?srsltid=AfmBOorVA2NBPfbJlrupQ_wQ-I_yuK2IqQBrZxm1x_9SKLc6y5Zss7ig shows for the BC107 which leg is which. For us it means put the transistor in its hole such that no leg points to the right.
Then connect the left leg with the free leg of the diode. 


![transistor wiring](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/transistor.png)

*Warning:* Do not bend done the transistors legs to far as I did for this image. Otherwise you might create a short 
with the metal casing of the transistor!

Now you are done and can fool around with the module! 


## Frontpanel

The front panel was via some spaghetti-python code, which creates svg files. 
One file tells where to mark the panel, on tells where to cut. The basic files can be found at https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/front-hadr-2026-vcAtt-cut.svg and https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/front-hadr-2026-vcAtt-mark.svg. *Note:* Do not scale the images when printing or laser-cutting! The size of Eurorack modules is precisely defined and if the dimensions are changed, the module will not fit into a case and holes for elements will also not have the right size. 

![panel, made from wooden spatula](https://github.com/l8-e/modules-vcAtt/blob/main/hadr-2026/images/panels_clipped.png)

I used a laser cutter to cut the panels from wooden spatulas ("Eisstiele"), which are roughly 16mm wide, so they are big enough to get one 3hp eurorack module plate out of them. 


# References
* https://lookmumnocomputer.discourse.group/t/lpg-vca-circuit/69/2 the original circuit of lookmumnocomputer

