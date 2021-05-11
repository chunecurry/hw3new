# hw3new

To use this file, you need two terminals
one for main.cpp, and one for mqtt_client.py

first, you need to set up a mqtt wifi environment
then, you use gesture to select a threshold angle 
(+5 when movin forward, -5 when drawing a circle)
then, you need to press user button to confirm your selection
and after python program send a RPC instruction to mbed via mqtt network
it will start the tilt angle detection mode and stop gestureUI mode
so if you tilt the board larger than the angle you selected
mbed will pass out the tilting angle to python via mqtt network (10 times at most)
if the amount of message of tilting angle are already 10
python will send a RPC instruction to mbed via mqtt network
then the the tilt angle detection mode will be stopped

