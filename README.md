# Coding Development

The working codes in this branch relate to coding the Arduino Due with the arduino IDE

**State Machine design

The code needs to maintain a record of the current state of 12 colour channels at the same time, and another channel for reading the sensor. Each colour channel will change PWM values with each clock and the sensor will read a value. The smoothness of the led transitions are dependent on the efficiency of the updating code and the frequency of the clock.
The example code here shows a mechanism for maintaining state values of each channel.
Another design method that I wish to explore is creating an object class for each channel which can maintain its own state value with a method for incrementing the PWM for the objects own pin.

**Colour perception

The perception of changes to colour is not linear, therefore a straight line step up and down through PWM values will not provide a smooth visual transition. The perception qaparently requires a logarithmic growth and I have an algorithm to model a more even perecption.
The coding question is whether to use an array constant of values from 0-4095, prepopulated by the algorithm or make the calculation at each clock cycle. My intuition suggests the former, although it will be a vvery large matrix!




