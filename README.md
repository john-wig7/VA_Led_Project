# ESP32

The working codes in this branch relate to coding the ESP32 with micropython

**Learning Curve**

Using the ESP32 is a new learning curve, although I am more familiary with python than I am am with C++/Java (arduino IDE).
THe advantage of using the ESP32 for this project is its significantly more powerful cpu in comparison to the Due. 
Setting the PWM frequency is very easy using the ESP32 which should allow more work to be done in between transitions while maintaining the perception of transition smoothness. These advantages over the Due in the end may not be perceived in the final product, and it is likely that both board can do this job equally effectively. 

**First stages**

The first steps in exploring the possibility of the ESP32 is learning the envioronment and the methods of the REPL which creates the interface with the files system on the ESP32. A python programme can be saved and uploaded to the ESP32 and if it replaces boot.py or main.py then the code will run automatically, just as the C++ code runs on an arduino.




