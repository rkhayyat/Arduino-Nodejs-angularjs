# arduino-nodejs-angularjs-socket.io3


The idea from this project is to present the ability to use arduino board (UNO R3 in this example) as a data capture device (in our case reading temperature), then presenting the captrued data on PC.
[demo](https://www.youtube.com/watch?v=IdU-cUy0SB0).

## The project consist of three parts:

###### Hardware part:

The circuit is very simple, I used LM35 as temperature detector as shown in the photo:

![alt tag](http://blog.rastating.com/content/images/2014/Feb/lm35_bb_1_.jpg)

I also installed [Standara Firmata](http://www.instructables.com/id/Arduino-Installing-Standard-Firmata/). Firmata is a protocol (set of rules) for communicating with microcontrollers from software on a computer, smartphone, or tablet. Standard Firmata is a software library that allows Arduino devices to communicate with your computer using the Firmata protocol. 

###### NODEJS part:

I used a javascript Platform named [johnny-five.io](http://johnny-five.io/), to achieve communication between arduino and nodejs.
In this [connecting with LM35](http://johnny-five.io/examples/temperature-lm35/), you can see the subroutine to read temperature from LM35 connected with arduino.

I also used [socket.io](http://socket.io/) engine to achieve realtime data communication between server side (nodejs) and client side (angularjs).

both Johnny-five.io and socket.io are libraries that can be used in nodejs.


**Important Note**: I tired **NODEJS 6.0.0** but it failed to initiate the communication with arduino.





