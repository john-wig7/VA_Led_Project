# VA_Led_Project
Project for art exhibition at Village Arts Kohukohu.
Lighting effects for ceramic art pieces by John Parker.
This work consists of ceramic cones approx 200 mm high fixed to wall.
Four colour sequenced lights will illuminate them in a relatively dark corner of the gallery.
THe project will use high powered rgbs driven by constant current source femtobuck drivers.
The power supply is from an old ASX computer with ample 650 watts.

The rgbs will be sequenced using pwm pins from an Arduino Due
I have chosen the Due because:

a) I have one!
b) It has the necessary 12 pwm output pins 
c) It can use 12 bit pwm resolution (only 8 bit on uno)
d) The 3.3 volt output pins suit the femtobuck driver

I have considered using an ESP32 and this is currently a secondary design branch with a learning curve, but has th epotential to be a cost effective and higher performing substitutue for the Due. The ESP32 also has the interesting micropython capability.

The coding challenges for the Due are:

a) simultaneously sequencing 12 rgb channels
b) ensuring smooth fading at lower power levels
      - whether analog.write can achieve this or controlling pwm frequency and duty cycle


