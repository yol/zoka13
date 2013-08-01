zoka13
======

Arduino sketches and Python scripts for Zomerkamp 2013

What should it do?
------------------

The automagical shoesize measurer consists of [a servo with 2 arms](http://i.imgur.com/PAlHHej.jpg?1), attached to the base and rotator of the servo.
On each arm's end, there is a copper plate and a screw. Together, the copper plate and the screw are a simple switch.

The servo rotates the arms together, bringing the sensors closer together. 
Then they both touch something and make contact, the servo stops, the arduino signals via the serial port the current servo angle. 
(At least, thats the plan)

When the PC receives the signal, the angle is converted to a shoe size and possible read aloud, when I have the time. 
The PC then send back a string (ATM does not care what) and then the arms open up again.
When a second signal arrives, the arms start closing again and everything repeats.

I still have to build a state machine (Why is it always state machines!?) or something to make this behavior.
