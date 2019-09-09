# VA_Led_Project
Project for art exhibition at Village Arts Kohukohu.

Lighting design and build for an installation by New Zealand ceramic artist John Parker commencing 2 November 2019.

The installation consists of a cluster of white ceramic cones approx 200 mm high fixed to a white gallery wall.

Four colour sequenced lights will illuminate the cones in a relatively dark corner of the gallery.
The project will use high powered RGB LEDs driven by constant current source, femtobuck drivers.
The power supply is from an old ASX computer with an ample 650 watts.

The LEDs will be sequenced using pwm pins on an Arduino Due microprocessor.
I have chosen the Due because:

a) I have one!
b) It has the necessary 12 pwm output pins 
c) It has 12-bit pwm resolution (compared to 8-bit on Arduino Uno)
d) The 3.3 volt output pins suit the femtobuck driver

I have considered using an ESP32 as a secondary design branch. It has the potential to be a cost effective and higher performing substitutue for the Due. The ESP32 also has micropython capability.

The coding challenges for the Due are:

a) simultaneously sequencing 12 rgb channels
b) ensuring smooth fading at lower power levels
      - whether analog.write can achieve this or alternatively, directly controlling frequency and duty cycle
c) whether to use classes or public functions to control each channel
d) using state machine and sequencing techniques
e) perception of colour - logarithmic vs linear increments


